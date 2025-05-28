## **1. Identificación del Proceso**

Almex Services

## **2. Finalidad del Proceso**

Almacenamiento de archivos
## **3. Descripción del Procedimiento**

Un servicio de **Windows** (pendiente de identificación) se ejecuta de forma continua (24/7) en el servidor **almex05**, permaneciendo a la espera de solicitudes en formato **JSON** enviadas por las interfaces de **SOA**. Estas solicitudes contienen documentos codificados en **Base64**.  
Una vez recibida la solicitud, el servicio decodifica el contenido y lo almacena en la base de datos.  
A continuación, se ejecuta un **Store Procedure** que transforma la información recibida y guarda los documentos en el servidor **almex16** para su posterior uso o procesamiento.

| **Rol**             | **Aplicativo**      | **Descripción**                                       | **Resultado**                                   |
| ------------------- | ------------------- | ----------------------------------------------------- | ----------------------------------------------- |
| SOA Interfaces      | SOA                 | Envían solicitudes JSON con documentos en Base64      | Inicio del proceso de carga de documentos       |
| Servicio en almex05 | Servicio de Windows | Recibe, decodifica y almacena en base de datos        | Información recibida y registrada correctamente |
| Base de datos       | (Investigar)        | Ejecuta Store Procedure que transforma la información | Datos transformados para procesamiento          |
| Servidor almex16    | -                   | Almacena documentos finales transformados             | Documentos disponibles para uso posterior       |

## **4. Herramientas, Recursos, Plataforma ó Servidor**


- **Servidor:** Almex05
- **Servidor:** Almex16
- **Plataforma:** Servicio de Windows
- **Herramienta:** SQL Server

## **5. Indicadores de Éxito**
Documento almacenado en almex16
