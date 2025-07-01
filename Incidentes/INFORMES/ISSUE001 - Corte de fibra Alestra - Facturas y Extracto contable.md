---
tags:
  - Incidentes
Departamentos:
  - Finanzas
  - Tesorería
  - Facturación
Impacto:
  - Critico
---
# Informe Postmortem Técnico

**Incidente:** Problemas en el envío de Facturas y Extractos Contables  
**Fecha del incidente:** 11/06/2025  
**Fecha del informe:** 19/06/2025

---

## 1. Resumen Ejecutivo

El día 11 de junio de 2025 se presentaron dos incidencias críticas que afectaron los flujos operativos del área de Finanzas en Almex, específicamente en los procesos de **Tesorería** y **Facturación**. Ambos eventos fueron ocasionados por una **interrupción en la conectividad a internet**, derivada de un **corte de fibra óptica del proveedor Alestra**, provocado por actos de vandalismo (robo de fibra).

Como consecuencia, se interrumpió la comunicación entre nuestro ERP (Oracle) y servicios externos, afectando la recepción de extractos contables provenientes de BBVA y la entrega de facturas electrónicas a nuestros clientes mediante una API expuesta en el servidor **Almex05**.

---

## 2. Áreas Afectadas

- **Tesorería:** Interrupción en la recepción de extractos contables enviados por BBVA vía FTP.
- **Facturación:** Fallas en el envío de facturas electrónicas (PDF y XML) a clientes.
- **Cuentas por Pagar:** Imposibilidad de enviar archivos bancarios a través del FTP corporativo, los cuales son consumidos por BBVA para registrar pagos y otras operaciones en su plataforma.

---

## 3. Descripción del Incidente

### 3.1 Tesorería y Cuentas por Pagar

El equipo de Tesorería reportó que los extractos contables enviados por BBVA no estaban siendo recibidos en el ERP Oracle. La causa raíz fue la inestabilidad en el servicio de **VPN**, que utiliza un túnel sobre la red de Alestra para conectar con el servidor FTP corporativo.

Adicionalmente, el área de **Cuentas por Pagar**, que tiene la responsabilidad de **depositar archivos en el mismo FTP**, también se vio afectada. Estos archivos son consumidos directamente por BBVA para registrar operaciones bancarias en su sistema.  
Durante el incidente, BBVA no pudo acceder al FTP, por lo que **no se reflejaron movimientos ni se procesaron operaciones** originadas desde **Almex** en la plataforma bancaria.


> 🔎 **Nota:** Este servicio actualmente está vinculado directamente a la IP de Alestra, sin posibilidad de failover automático.

### 3.2 Facturación

Simultáneamente, el área de Facturación reportó que los clientes no estaban recibiendo sus facturas digitales. La investigación técnica determinó que la API utilizada para la entrega de facturas (alojada en **Almex05**) dependía de un **registro DNS configurado en GoDaddy**, apuntando a una dirección IP de Alestra.

Durante el corte de fibra, dicha IP fue inaccesible, impidiendo el acceso a la API y, por ende, el envío de los comprobantes fiscales.

> 🔎 **Nota adicional:** La URL afectada fue `https://www.paamxgdl.com`, configurada en GoDaddy y apuntando a una IP de Alestra (pendiente de documentación exacta).

---

## 4. Causa Raíz

- **Hora del corte:** Reportado oficialmente por Alestra a las **00:18 hrs** del 11/06/2025.
    
- **Restablecimiento del servicio:** Confirmado por el área de redes a las **15:00 hrs** del mismo día.
    
- El corte fue provocado por **vandalismo (robo de fibra óptica)**, afectando múltiples servicios en la zona.
    
- Se afectaron tanto las conexiones externas (túneles a BBVA y acceso público a la API).
    
- Falta de **mecanismos automáticos de conmutación (failover)** hacia el segundo proveedor de internet, **TotalPlay** de los servicios de VPN con BBVA y la API.

---

## 5. Acciones Correctivas Inmediatas

- **Tesorería y Cuentas por Pagar:**  
  Se evaluó la posibilidad de redireccionar la VPN al proveedor secundario (**TotalPlay**). No obstante, esta medida no fue viable, ya que el servicio de FTP utilizado por BBVA está configurado para establecer conexión únicamente con la IP pública de **Alestra**.  
  Esto no solo impidió la **recepción de extractos**, sino también el **acceso a archivos generados por Cuentas por Pagar**, provocando una interrupción en los registros bancarios de salidas.

  Como medida a mediano plazo, se encuentra en marcha la migración hacia un nuevo servicio proporcionado por BBVA, denominado **“BBVA – PIVOTE”**, que busca mejorar la disponibilidad y flexibilidad del canal de integración.

- **Facturación:**  
    Se procedió a actualizar los registros DNS en **GoDaddy**, redireccionando la URL de la API pública (`https://www.paamxgdl.com`) hacia las IPs asociadas a **TotalPlay**, con la intención de restablecer la conectividad hacia el servidor **Almex05** y reanudar el envío de comprobantes digitales (PDF, XML).  
    Sin embargo, esta acción **no fue suficiente para mitigar completamente el impacto**, debido a que múltiples elementos del proceso de facturación seguían dependiendo de la red de Alestra y no pudieron resolverse mediante DNS.  
    En consecuencia, el servicio fue **plenamente restablecido únicamente hasta que el proveedor Alestra solucionó el corte de fibra óptica** y se recuperó la conectividad original.
    
    > 🔧 **Nota técnica:**  
    > Tras el cambio de DNS, se detectó comportamiento irregular en la resolución y conectividad de la URL desde distintas ubicaciones. A continuación, se presenta un ejemplo real:
    

``` bash
$ ping a [www.paamxgdl.com](https://www.paamxgdl.com "https://www.paamxgdl.com/") [187.189.11.100] con 32 bytes de datos:  
Respuesta desde 187.189.11.100: bytes=32 tiempo=2ms TTL=126  
Respuesta desde 187.189.11.100: bytes=32 tiempo=3ms TTL=126  
Respuesta desde 187.189.11.100: bytes=32 tiempo=4ms TTL=126  
Respuesta desde 187.189.11.100: bytes=32 tiempo=3ms TTL=126
```

``` bash
$ tracert [www.paamxgdl.com](https://www.paamxgdl.com "https://www.paamxgdl.com/")

Traza a la dirección [www.paamxgdl.com](https://www.paamxgdl.com "https://www.paamxgdl.com/") [187.189.11.100]  
sobre un máximo de 30 saltos:

  1     2 ms     1 ms     2 ms  10.5.40.215  
  2     2 ms     2 ms     2 ms  almexportal.almex.dom [10.10.15.5]  
  3     3 ms     3 ms     3 ms  fixed-187-189-11-100.totalplay.net [187.189.11.100]
```

Desde Telcel así responde www.paamxgdl.com

![[ISSUE001_image001.png]]
Desde Totalplay Invitados así responde www.paamxgdl.com

![[ISSUE001_image002.png]]

> Como se observa, el servicio presentaba respuestas intermitentes, lo cual dificultaba establecer conexiones estables, incluso tras la modificación de los registros DNS.

---

## 6. Participantes Clave

| Nombre           | Rol                                |
| ---------------- | ---------------------------------- |
| Omar Romo        | Gerente de IT                      |
| Getsemani Ávila  | Jefe de Aplicaciones               |
| Gustavo Valencia | Administrador de Redes y Seguridad |

---

## 7. Lecciones Aprendidas

- La redundancia de enlaces debe incluir **mecanismos automáticos de failover**, especialmente en servicios de misión crítica como VPN y DNS.
    
- Es indispensable implementar **monitoreo en tiempo real** de conectividad y disponibilidad de proveedores de internet.
    
- La infraestructura de publicación (DNS, IPs públicas, firewalls) debe ser revisada regularmente para asegurar su resiliencia ante fallos externos.
    
- La colaboración entre Finanzas e IT es clave para documentar y entender las **dependencias técnicas** de cada flujo de negocio.
    
- Evaluar tecnologías alternativas como **redes de radiofrecuencia** puede ofrecer una vía adicional de conectividad en escenarios donde ambos proveedores de internet tradicionales (fibra óptica) resulten comprometidos.

---

## 8. Próximos Pasos

1. **Implementar conmutación automática (failover)** para túneles VPN y resolución DNS en servicios críticos.
    
2. **Migrar el servicio de BBVA** al nuevo esquema **"PIVOTE"**, permitiendo mayor flexibilidad y redundancia.
    
3. **Revisar y documentar todas las dependencias de IP/DNS** en servicios productivos.
    
4. **Realizar simulacros de desconexión controlada**, para evaluar la resiliencia de las áreas críticas.
    
5. Establecer un plan de comunicación entre áreas durante incidentes para asegurar respuestas coordinadas y efectivas.
    
6. **Analizar la factibilidad técnica y económica de una red por radiofrecuencia** como canal de respaldo adicional, independiente de los proveedores de internet actuales.
