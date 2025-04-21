## **1 - 📓Información General:**

| **Modelo:**           | dcamxvsql01   | Fabricante:    | [Fabricante del servidor] |
| --------------------- | ------------- | -------------- | ------------------------- |
| **Tipo de servidor:** | Virtual       | **Ubicación:** | Rack                      |
| **Propósito:**        | DBA MS_Server | **Priridad**   | 🔴 Alta  <br><br>         |
> _doc:_ [[Clasificación de Prioridades para Servidores]]
> 
### **1.1 - ⚙️Hardware:**

| Procesador (CPU)    | **Fabricante:**                        | 🔹INTEL<br>🔺AMD<br>🔸ARM | **Modelo:**                              | [modelo de la CPU]               |
| ------------------- | -------------------------------------- | ------------------------- | ---------------------------------------- | -------------------------------- |
| **Memoria RAM:**    | **Tipo de memoria:**                   | DDR: [4️⃣,5️⃣]            | **Configuración de los módulos:**        | [Número de módulos, canal, etc.] |
| **Almacenamiento:** | **Tipo de almacenamiento:**            | 💾HDD <br>💿SSD<br>💽NVMe | **Configuración RAID:**                  | ✅❌<br>Raid[# Num]                |
|                     | **Capacidad total de almacenamiento:** | [GB/TB]                   | **Total de Unidades de almacenamiento:** | [X]                              |

### **1.2 - 🐧Sistema Operativo:**

| **Sistema operativo:**             | Windows Server                            | **Versión del sistema operativo:** | [Número de versión] |
| ---------------------------------- | ----------------------------------------- | ---------------------------------- | ------------------- |
| **Controlador de virtualización:** | [Ej. VMware ESXi, Hyper-V, Proxmox, etc.] |                                    |                     |
- **Licencias de software:** [Detalles sobre licencias de sistemas operativos, aplicaciones o servicios que utilice]

## **2 - 🛜Red y Dirección IP:**
- **Dirección IP pública/privada:** [IP asignada o rango de IPs]
- **Configuración de DNS:** [Si aplica, especificar configuración DNS]
- **Protocolos soportados:** [IPv4, IPv6, DHCP, etc.]

### **2.1 - 🔌Catalogo Puertos Abiertos**
| **Puerto** | **Protocolo** | **Aplicativo**                    | **Justificación de por que se usa ese puerto** |
| ---------- | ------------- | --------------------------------- | ---------------------------------------------- |
| 80         | HTTP          | [Aplicativo que usa la conexión ] |                                                |
| 443        | HTTPS         |                                   |                                                |
| 3306       | MySQL         |                                   |                                                |

## **3 - 🔐Redundancia y Seguridad:**
- **Fuentes de alimentación redundantes:** [Sí/No]
- **UPS (sistema de alimentación ininterrumpida):** [Si aplica, especificar capacidad]
- **Controladores RAID:** [Especificar si incluye un controlador RAID y su configuración]    
- **Sistemas de seguridad:** [Firewall, cifrado de datos, protección contra ataques DDoS, etc.]

## **4 - 💻Máquinas Virtuales y Contenedores:**

### **4.1 - 🗂️Catálogo de Maquinas Virtuales:**

| **Máquina Virtual** | **Sistema Operativo** | **Recursos Asignados**                    | **Propósito**                                | **Notas**                               |
| ------------------- | --------------------- | ----------------------------------------- | -------------------------------------------- | --------------------------------------- |
| **VM-00**           | [Sistema Operativo]   | [X] vCPU, [X]GB RAM, [X]GB almacenamiento | [Propósito]                                  | [Notas]                                 |
| **VM-01**           | Ubuntu Server 20.04   | [X] vCPU, [X]GB RAM, [X]GB almacenamiento | Servidor web para la intranet                | Usado para alojar aplicaciones internas |
| **VM-02**           | Windows Server 2019   | [X] vCPU, [X]GB RAM, [X]GB almacenamiento | Base de datos MySQL para software de tickets | Accesible solo desde la red interna     |
| **VM-03**           | CentOS 7              | [X] vCPU, [X]GB RAM, [X]GB almacenamiento | Sistema de control de inventarios            | Conexión a base de datos de inventarios |
| **VM-04**           | Debian 10             | [X] vCPU, [X]GB RAM, [X]GB almacenamiento | Servidor de correo interno                   | Acceso sólo a empleados internos        |
| **VM-05**           | Windows Server 2022   | [X] vCPU, [X]GB RAM, [X]GB almacenamiento | Plataforma de CRM para ventas                | Accesible solo para el equipo de ventas |

### **4.2 - 📁Catálogo de Contenedores:**

| **Contenedor**    | **Plataforma** | **Imagen**               | **Recursos Asignados**                    | **Propósito**                                  | **Notas**                                     |         |
| ----------------- | -------------- | ------------------------ | ----------------------------------------- | ---------------------------------------------- | --------------------------------------------- | ------- |
| **Contenedor-01** | Docker         | php:8.3                  | [Nombre Imagen]:[Version]                 | [X] vCPU, [X]GB RAM, [X]GB almacenamiento      | [Propósito]                                   | [Notas] |
| **Contenedor-02** | Docker         | mysql:8                  | [X] vCPU, [X]GB RAM, [X]GB almacenamiento | Base de datos para la gestión de tickets       | Conexión a través de red interna              |         |
| **Contenedor-03** | Kubernetes     | redis:latest             | [X] vCPU, [X]GB RAM, [X]GB almacenamiento | Caché de datos para aplicaciones internas      | Usado para optimizar el rendimiento           |         |
| **Contenedor-04** | Docker         | wordpress:latest         | [X] vCPU, [X]GB RAM, [X]GB almacenamiento | Plataforma de gestión de contenido (CMS)       | Acceso solo para administradores de contenido |         |
| **Contenedor-05** | Docker         | custom/ticketing-app:1.0 | [X] vCPU, [X]GB RAM, [X]GB almacenamiento | Aplicación personalizada de gestión de tickets | Acceso restringido a usuarios internos        |         |

## **5 - 💿Aplicativos (Software Comercial o Legados) Corriendo en el Servidor:**

| **Aplicativo** | **Descripción**                                            | Requisitos | **Propósito**                               | **Notas**                                 |
| -------------- | ---------------------------------------------------------- | ---------- | ------------------------------------------- | ----------------------------------------- |
| [Aplicativo]   | [Descripción]                                              | [Notas]    | [Propósito]                                 | [Notas]                                   |
| **Intranet**   | Plataforma interna de comunicación y gestión de la empresa |            | Comunicación interna, gestión de documentos | Personalizado, accesible solo a empleados |
