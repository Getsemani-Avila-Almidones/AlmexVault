## **1. Identificación del Proceso

 Extractos Concur

## **2. Finalidad del Proceso

Trasladar y convertir los extractos de Concur en registros de facturas dentro del módulo de Cuentas por Pagar del ERP de Oracle

## **3. Descripción del Procedimiento

 Obtener el extracto o reporte del portal de Concur (proporcionado por el usuario encargado del proceso).

Trasladar el extracto al disco C de la computadora de Ernesto, ubicada físicamente en el gabinete de la oficina de infraestructura (archivero de Santiago).

Al llegar el archivo, se ejecuta manualmente un script Desencriptado renombrando el archivo viejo por el nuevo y borrándolo de la carpeta procesando que envía el archivo por HTTPS (POST) a la API del OTM.

|**Rol**|**Aplicativo**|**Descripción**|**Resultado**|
|---|---|---|---|
|Jefe de Cuentas por Pagar (Daniel Gomez Mina)|Portal de Concur|Obtener el extracto|Obtener el extracto para mandarlo al técnico|
|Especialista de Soporte (Santiago Gonzalez Rodriguez)|EXE (Concur)|Ejecuta el programa para que el extracto mande el archivo|El extracto contable se deposite de forma correcta en la plataforma destino|
|Jefe de Cuentas por Pagar (Daniel Gomez Mina)|ERP|Revisa que esté generado correctamente|Visualización de gastos que estén correctos|

## **4. Herramientas, Recursos, Plataforma ó Servidor**


- **Plataforma:** Portal de Concur
- **Herramienta:** API (OTM)
- **Herramienta:** Ejecutable Concur (.NET)
- **Recurso:** Archivo
## **5. Indicadores de Éxito
Envió correcto del extracto a la plataforma de Oracle(OTM)
