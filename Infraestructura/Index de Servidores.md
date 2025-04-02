## 📘 Catálogo General de Servidores

**Nomenclatura De Servidores:**

Ejemplo: _dcamxvapp01_

**dc**  data center  
**AMX** "Empresa"  
[**V** o **P**] (V: Virtual o P: Físico)  
**APP01** (Nombre del Servidor)

| **ID/Nombre del Servidor** | **Ubicación Física**                     | **Tipo** | **Propósito** | **Sistema Operativo** | 🖧**IP Privada** | 🖧**IP Pública** | **Usuario SSH/Admin** | **Puertos** | **Notas**                 | Entorno del Servidor: |
| -------------------------- | ---------------------------------------- | -------- | ------------- | --------------------- | ---------------- | ---------------- | --------------------- | ----------- | ------------------------- | --------------------- |
| dcamxvapp01 PROD           | virtual(dcamxpvm0)                       | rack     | solo apps     | 🪟win ser 2012 r2     | 10.10.10.25      | N/A              | TBC                   | TBC         | puertos abiertos algunos, | **Productivo**        |
| dcamxvsql01 PROD           | virtual(dcamxpvm0)                       | rack     | DBA MS_Server | 🪟win ser 2012 r2     | 10.10.10.23      | N/A              | SSO                   | SSO         | 1433                      | **Productivo**        |
| dcamxpvm01                 | site (almex16, dcamxapp01 y dcamxvsql01) | rack     |               |                       |                  |                  |                       |             |                           | **Productivo**        |
| dcamxpvm02                 | site(glpi)                               | rack     |               |                       |                  |                  |                       |             |                           | **Productivo**        |
| dcamxvglpi02               | virtual(dcamxvglpiX)                     | rack     | glpi          | 🐧linux               | 10.10.10.17      | N/A              | USER                  | PASS        | 80                        | **Productivo**        |
| dcamxvfs01                 | virtual(dcamxvfsX)                       | rack     | Archivos      | 🪟win                 | En Dominio       | N/A              | USER                  | PASS        |                           | Desarrollo            |
| dcamxvdes01                | decomisados                              | N/A      | N/A           | N/A                   | N/A              | N/A              | N/A                   | N/A         | N/A                       | N/A                   |
| dcamxvdes01                | decomisados                              | N/A      | N/A           | N/A                   | N/A              | N/A              | N/A                   | N/A         | N/A                       | N/A                   |
| almex05                    | site(fisico)                             | rack     | IIS (ORACLE)  | 🪟win ser 2012 r2     | 182.169.86.250   | 201.163.93.2     | SSO                   | SSO         | 80?:8080?3360?            | **Productivo**        |
| almex16                    | virtual(?)                               | rack     | Documentos    | 🪟win ser 2012 r2     | 10.10.10.16      | N/A              | SSO                   | SSO         |                           | **Productivo**        |

