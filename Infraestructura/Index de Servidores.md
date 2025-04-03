## 📘 Catálogo General de Servidores

**Nomenclatura De Servidores:**

Ejemplo: _dcamxvapp01_

**dc**  data center  
**AMX** "Empresa"  
[**V** o **P**] (V: Virtual o P: Físico)  
**APP01** (Nombre del Servidor)

| **ID/Nombre del Servidor** | **Ubicación Física**                     | **Tipo** | **Propósito** | **Sistema Operativo** | 🖧**IP Privada** | 🖧**IP Pública** | **Usuario SSH/Admin** | **Puertos**               | Entorno del Servidor: |
| -------------------------- | ---------------------------------------- | -------- | ------------- | --------------------- | ---------------- | ---------------- | --------------------- | ------------------------- | --------------------- |
| dcamxvapp01 PROD           | virtual(dcamxpvm01)                      | Rack     | Solo Apps     | 🪟win ser 2012 r2     | 10.10.10.25      | N/A              | TBC                   | puertos abiertos algunos, | **Productivo**        |
| dcamxvsql01 PROD           | virtual(dcamxpvm01)                      | Rack     | DBA MS_Server | 🪟win ser 2012 r2     | 10.10.10.23      | N/A              | SSO                   | 1433                      | **Productivo**        |
| dcamxpvm01                 | site (almex16, dcamxapp01 y dcamxvsql01) | Rack     |               |                       |                  |                  |                       |                           | **Productivo**        |
| dcamxpvm02                 | site(glpi)                               | Rack     |               |                       |                  |                  |                       |                           | **Productivo**        |
| dcamxvglpi02               | virtual(dcamxvglpi02)                    | Rack     | Glpi          | 🐧linux               | 10.10.10.17      | N/A              | USER                  | 80                        | **Productivo**        |
| dcamxvfs01                 | virtual(dcamxvfs01)                      | Rack     | Archivos      | 🪟win                 | En Dominio       | N/A              | USER                  | ?                         | Productivo            |
| dcamxvdes01                | decomisados                              | N/A      | N/A           | N/A                   | N/A              | N/A              | N/A                   | N/A                       | N/A                   |
| dcamxvdes01                | decomisados                              | N/A      | N/A           | N/A                   | N/A              | N/A              | N/A                   | N/A                       | N/A                   |
| almex05                    | site(fisico)                             | Rack     | IIS (ORACLE)  | 🪟win ser 2012 r2     | 182.169.86.250   | 201.163.93.2     | SSO                   | S80?:8080?3360?           | **Productivo**        |
| almex16                    | virtual(dcamxpvm01)                      | Rack     | Documentos    | 🪟win ser 2012 r2     | 10.10.10.16      | N/A              | SSO                   | ?                         | **Productivo**        |

