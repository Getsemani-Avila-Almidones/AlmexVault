## 📘 Catálogo General de Servidores

|**ID/Nombre del Servidor**|**Ubicación Física**|**Tipo**|**Propósito**|**Sistema Operativo**|**IP Privada**|**IP Pública**|**Usuario SSH/Admin**|**Puerto SSH**|**Notas**|
|---|---|---|---|---|---|---|---|---|---|
|SRV-01|Rack A3 - Data Center 01|Rack|Servidor Web|Ubuntu Server 20.04|192.168.1.10|203.0.113.10|admin|22|Acceso sólo desde red interna|
|SRV-02|Oficina Principal|Torre|Servidor de Bases de Datos|Windows Server 2019|192.168.1.11|N/A|administrador|3389 (RDP)|Conexión por Escritorio Remoto|
|SRV-03|Rack B1 - Data Center 02|Blade|Plataforma CRM|Windows Server 2022|10.0.0.5|203.0.113.15|crm_admin|22|Uso exclusivo equipo de ventas|
|SRV-04|Rack C4 - Data Center 01|Rack|Contenedores y Virtualización|Proxmox VE 7.1|10.0.0.20|N/A|root|22|Admin vía web y SSH|
|SRV-05|Cuarto Servidores Planta|Torre|Servidor de respaldos|Debian 11|192.168.10.5|N/A|backup_user|2222|SSH con puerto alternativo|