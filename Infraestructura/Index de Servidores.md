## 📘 Catálogo General de Servidores

**Nomenclatura De Servidores:**

Ejemplo: _dcamxvapp01_

**dc**  data center  
**AMX** "Empresa"  
[**V** ** o** **P**] (V: Virtual o P: Físico)  
**APP01** (Nombre del Servidor)

| **ID/Nombre del Servidor** | Prioridad | **Ubicación Física**                        | **Tipo** | Entorno del Servidor: | **Propósito** | **Sistema Operativo** | 🖧**IP Privada** | 🖧**IP Pública** | **Usuario SSH/Admin** | **Puertos**               |
| -------------------------- | --------- | ------------------------------------------- | -------- | --------------------- | ------------- | --------------------- | ---------------- | ---------------- | --------------------- | ------------------------- |
| dcamxvapp01 PROD           |           | virtual(dcamxpvm01)                         | Rack     | **Productivo**        | Solo Apps     | 🪟win ser 2012 r2     | 10.10.10.25      | N/A              | TBC                   | puertos abiertos algunos, |
| -dcamxvsql01 PROD          |           | Virtual(dcamxpvm01)                         | Rack     | **Productivo**        | DBA MS_Server | 🪟win ser 2012 r2     | 10.10.10.23      | N/A              | SSO                   | 1433                      |
| dcamxpvm01                 |           | Virtual (almex16, dcamxapp01 y dcamxvsql01) | Rack     | **Productivo**        |               |                       |                  |                  |                       |                           |
| dcamxpvm02                 |           | Virtual(glpi)                               | Rack     | **Productivo**        |               |                       |                  |                  |                       |                           |
| dcamxvglpi02               |           | Virtual(dcamxvglpi02)                       | Rack     | **Productivo**        | Glpi          | 🐧linux               | 10.10.10.17      | N/A              | USER                  | 80                        |
| dcamxvfs01                 |           | Virtual(dcamxvfs01)                         | Rack     | Desarrollo            | Archivos      | 🪟win                 | En Dominio       | N/A              | USER                  | ?                         |
| dcamxvdes01                |           | Decomisados                                 | N/A      | N/A                   | N/A           | N/A                   | N/A              | N/A              | N/A                   | N/A                       |
| dcamxvdes01                |           | Decomisados                                 | N/A      | N/A                   | N/A           | N/A                   | N/A              | N/A              | N/A                   | N/A                       |
| almex05                    | 🔴 Alta   | Fisico(?)                                   | Rack     | **Productivo**        | IIS (ORACLE)  | 🪟win ser 2012 r2     | 182.169.86.250   | 201.163.93.2     | SSO                   | S80?:8080?3360?           |
| almex16                    |           | virtual(?)                                  | Rack     | **Productivo**        | Documentos    | 🪟win ser 2012 r2     | 10.10.10.16      | N/A              | SSO                   | ?                         |
| phoenix?                   |           | linux                                       | Oracle   | prod                  | ?             | ?                     | ?                | XXX.XXX.114.231  | SSH                   | ?                         |

