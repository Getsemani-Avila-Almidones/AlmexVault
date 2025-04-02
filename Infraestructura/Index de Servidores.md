## 📘 Catálogo General de Servidores

**Definiciones  De Servidores:**
(**D**  data)  (**C**  Center)  (**AMX**  Almex)   (**V**  virtual) (**APP  Aplicativo ) (X donde se localiza)
- almex(X):  Servidor físico, dependiendo su localización es donde va la X)
- dcamxvfs(X): Servidor físico, dependiendo su localización es donde va la X
- dcamxvglpi(X): Servidor Virtual, dependiendo su localización es donde va la X
- dcamxvapp(X):  Servidor Virtual, dependiendo su localización es donde va la X

| **ID/Nombre del Servidor** | **Ubicación Física** | **Tipo** | **Propósito** | **Sistema Operativo** | 🖧**IP Privada**           | 🖧**IP Pública** | **Usuario SSH/Admin** | **Puerto SSH** | **Notas**                 |
| -------------------------- | -------------------- | -------- | ------------- | --------------------- | -------------------------- | ---------------- | --------------------- | -------------- | ------------------------- |
| Debian 11                  | 192.168.10.5         | N/A      | backup_user   | 2222                  | SSH con puerto alternativo |                  |                       |                |                           |
| dcamxvapp01 PROD           | virtual(dcamxpvm0)   | rack     | solo apps     | 🪟win ser 2012 r2     | 10.10.10.25                | N/A              | TBC                   | TBC            | puertos abiertos algunos, |
| dcamxvsql01 PROD           | virtual(dcamxpvm0)   | rack     | DBA MS_Server | 🪟win ser 2012 r2     | 10.10.10.23                | N/A              | SSO                   | SSO            | 1433                      |
| dcamxpvm01                 | site                 | rack     |               |                       |                            |                  |                       |                |                           |
| dcamxpvm02                 | site                 | rack     |               |                       |                            |                  |                       |                |                           |
| dcamxvglpi02               | virtual(dcamxvglpiX) | rack     | glpi          | 🐧linux               | 10.10.10.17                | N/A              | USER                  | PASS           | 80                        |
| dcamxvfs01                 | virtual(dcamxvfsX)   | rack     | Archivos      |                       |                            |                  |                       |                |                           |
| dcamxvdes01                | decomisados          | N/A      | N/A           | N/A                   | N/A                        | N/A              | N/A                   | N/A            | N/A                       |
| dcamxvdes01                | decomisados          | N/A      | N/A           | N/A                   | N/A                        | N/A              | N/A                   | N/A            | N/A                       |
| almex05                    | site(fisico)         | rack     | IIS (ORACLE)  | 🪟win ser 2012 r2     | 182.169.86.250             | 201.163.93.2     | SSO                   | SSO            | 80?:8080?3360?            |
| almex16                    | virtual(?)           | rack     | Documentos    | 🪟win ser 2012 r2     | 10.10.10.16                | N/A              | SSO                   | SSO            |                           |

