## **1 - 📓Información General:**

| **Modelo:**           | Phoenix                                                                  | Fabricante:    | [Fabricante del servidor]                                                       |
| --------------------- | ------------------------------------------------------------------------ | -------------- | ------------------------------------------------------------------------------- |
| **Tipo de servidor:** | [Rack, Torre, Blade, etc.]                                               | **Ubicación:** | [Localizacion fisica del Servidor]                                              |
| **Propósito:**        | [Uso específico del servidor, como virtualización, bases de datos, etc.] | **Priridad**   | 🔴 Alta  <br>🟡 Media  <br>🟢 Baja  <br>⚫ Obsoleto  <br>⚠️ A punto de decomisar |
> _doc:_ [[Clasificación de Prioridades para Servidores]]
> 
### **1.1 - ⚙️Hardware:**

| Procesador (CPU)    | **Fabricante:**                        | 🔹INTEL<br>🔺AMD<br>🔸ARM | **Modelo:**                              | [modelo de la CPU]               |
| ------------------- | -------------------------------------- | ------------------------- | ---------------------------------------- | -------------------------------- |
| **Memoria RAM:**    | **Tipo de memoria:**                   | DDR: [4️⃣,5️⃣]            | **Configuración de los módulos:**        | [Número de módulos, canal, etc.] |
| **Almacenamiento:** | **Tipo de almacenamiento:**            | 💾HDD <br>💿SSD<br>💽NVMe | **Configuración RAID:**                  | ✅❌<br>Raid[# Num]                |
|                     | **Capacidad total de almacenamiento:** | [GB/TB]                   | **Total de Unidades de almacenamiento:** | [X]                              |

### **1.2 - 🐧Sistema Operativo:**

| **Sistema operativo:**             | [Ej. Windows Server, Linux (especificar distribución), etc.] | **Versión del sistema operativo:** | [Número de versión] |
| ---------------------------------- | ------------------------------------------------------------ | ---------------------------------- | ------------------- |
| **Controlador de virtualización:** | [Ej. VMware ESXi, Hyper-V, Proxmox, etc.]                    |                                    |                     |
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



### **4.2 - 📁Catálogo de Contenedores:**



## **5 - 💿Aplicativos (Software Comercial o Legados) Corriendo en el Servidor:**

| **Aplicativo** | **Descripción**                                            | Requisitos | **Propósito**                               | **Notas**                                 |
| -------------- | ---------------------------------------------------------- | ---------- | ------------------------------------------- | ----------------------------------------- |
| [Aplicativo]   | [Descripción]                                              | [Notas]    | [Propósito]                                 | [Notas]                                   |
| **Intranet**   | Plataforma interna de comunicación y gestión de la empresa |            | Comunicación interna, gestión de documentos | Personalizado, accesible solo a empleados |
