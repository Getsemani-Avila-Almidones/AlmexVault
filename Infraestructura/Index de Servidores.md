## 📘 Catálogo General de Servidores

**Nomenclatura De Servidores:**

Ejemplo: _dcamxvapp01_

**dc**  data center  
**AMX** "Empresa"  
[**V** o **P**] (V: Virtual o P: Físico)  
**APP01** (Nombre del Servidor)

| **ID/Nombre del Servidor** | **Ubicación Física**                     | **Tipo** | **Propósito** | **Sistema Operativo** | 🖧**IP Privada** | 🖧**IP Pública** | **Usuario SSH/Admin** | **Puertos**               | Entorno del Servidor: |
| -------------------------- | ---------------------------------------- | -------- | ------------- | --------------------- | ---------------- | ---------------- | --------------------- | ------------------------- | --------------------- |
| dcamxvapp01 PROD           | virtual(dcamxpvm0)                       | Rack     | Solo Apps     | 🪟win ser 2012 r2     | 10.10.10.25      | N/A              | TBC                   | puertos abiertos algunos, | **Productivo**        |
| dcamxvsql01 PROD           | virtual(dcamxpvm0)                       | Rack     | DBA MS_Server | 🪟win ser 2012 r2     | 10.10.10.23      | N/A              | SSO                   | 1433                      | **Productivo**        |
| dcamxpvm01                 | site (almex16, dcamxapp01 y dcamxvsql01) | Rack     |               |                       |                  |                  |                       |                           | **Productivo**        |
| dcamxpvm02                 | Virtual(glpi)                            | Rack     |               |                       |                  |                  |                       |                           | **Productivo**        |
| dcamxvglpi02               | Virtual(dcamxvglpiX)                     | Rack     | Glpi          | 🐧linux               | 10.10.10.17      | N/A              | USER                  | 80                        | **Productivo**        |
| dcamxvfs01                 | Virtual(dcamxvfsX)                       | Rack     | Archivos      | 🪟win                 | En Dominio       | N/A              | USER                  | ?                         | Desarrollo            |
| dcamxvdes01                | Decomisados                              | N/A      | N/A           | N/A                   | N/A              | N/A              | N/A                   | N/A                       | N/A                   |
| dcamxvdes01                | Decomisados                              | N/A      | N/A           | N/A                   | N/A              | N/A              | N/A                   | N/A                       | N/A                   |
| almex05                    | Fisico                                   | Rack     | IIS (ORACLE)  | 🪟win ser 2012 r2     | 182.169.86.250   | 201.163.93.2     | SSO                   | S80?:8080?3360?           | **Productivo**        |
| almex16                    | virtual(?)                               | Rack     | Documentos    | 🪟win ser 2012 r2     | 10.10.10.16      | N/A              | SSO                   | ?                         | **Productivo**        |

