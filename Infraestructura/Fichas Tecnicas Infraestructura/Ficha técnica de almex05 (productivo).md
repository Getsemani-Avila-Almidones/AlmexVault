## **1 - 📓Información General:**

| **Modelo:**           | almex05      | Fabricante:    | [Fabricante del servidor] |
| --------------------- | ------------ | -------------- | ------------------------- |
| **Tipo de servidor:** | Rack         | **Ubicación:** | Virtual (Site)            |
| **Propósito:**        | IIS (ORACLE) | **Priridad**   | 🔴 Alta  <br>             |
> _doc:_ [[Clasificación de Prioridades para Servidores]]
> 
### **1.1 - ⚙️Hardware:**

| Procesador (CPU)    | **Fabricante:**                        | 🔹INTEL<br>  | **Modelo:**                              | xeon e5-2403      |
| ------------------- | -------------------------------------- | ------------ | ---------------------------------------- | ----------------- |
| **Memoria RAM:**:16 | **Tipo de memoria:**                   | DDR: 4       | **Configuración de los módulos:**        | 4                 |
| **Almacenamiento:** | **Tipo de almacenamiento:**            | 💾HDD <br>   | **Configuración RAID:**                  | ✅❌<br>Raid[# Num] |
|                     | **Capacidad total de almacenamiento:** | 1 100,1 189g | **Total de Unidades de almacenamiento:** | [2]               |
|                     |                                        |              |                                          |                   |

### **1.2 - 🐧Sistema Operativo:**

| **Sistema operativo:**             | 🪟Windows server 2012 r2 | **Versión del sistema operativo:** | 6.3 |
| ---------------------------------- | ------------------------ | ---------------------------------- | --- |
| **Controlador de virtualización:** | fisico                   |                                    |     |
- **Licencias de software:** [Detalles sobre licencias de sistemas operativos, aplicaciones o servicios que utilice]

## **2 - 🛜Red y Dirección IP:**
- **Dirección IP pública/privada:** PRIVADA
- **Configuración de DNS:** 10:10:10:9/10:10:10:10
- **Protocolos soportados:** IPv4, IPv6, DHCP

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
|                     |                       |                                           |                                              |                                         |

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
|                |                                                            |            |                                             |                                           |
