## **1. Identificación del Proceso**

Facturación Electrónica
## **2. Finalidad del Proceso**

Timbrado de documentos fiscales
## **3. Descripción del Procedimiento**

 En el ERP, se genera una transacción de tipo documento fiscal (Factura, Nota de Crédito y Complemento de Pago).

 A través de un reporte en **OTBI**, se extrae la transacción previamente estructurada, dependiendo del tipo de documento fiscal.

 La interfaz de **SOA** (**BSS Electronic Inv Manager**) procesa la extracción de los reportes de **OTBI**.

 El proceso de la interfaz (**BPEL**) realiza las validaciones automáticas correspondientes al tipo de documento y arma el **XML** y **Request** hacia los servicios del **PAC** (Proveedor de Autorización de Comprobantes) para timbrar y generar los archivos del documento fiscal.

 Una vez que se tienen los archivos timbrados, se consume el servicio **Almex Services (Windows)** que se encuentra en el servidor **Almex05**.

El servicio **Almex Services** decodifica el **Base64** recibido de la interfaz de **SOA** y lo almacena en la base de datos de **Almex**.
 En la base de datos de **Almex (ALMEXSERVICES)** se ejecuta una serie de **JOBS** que convierten y almacenan los archivos en el servidor **Almex16**.

 Posteriormente, la interfaz de **SOA** ejecuta la dispersión de correos con los documentos adjuntos hacia el cliente.

| **Rol**                          | **Aplicativo** | **Descripción**                                                                                                                 | **Resultado**                                 |
| -------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- |
| ERP                              |                | Se genera una transacción de tipo documento fiscal (Factura, Nota de Crédito y Complemento de Pago).                            | Documento fiscal generado                     |
| OTBI                             |                | Se extrae la transacción previamente estructurada, dependiendo del tipo de documento fiscal.                                    | Datos disponibles para la interfaz SOA        |
| SOA (BSS Electronic Inv Manager) |                | Procesa la extracción de los reportes de OTBI.                                                                                  | Datos procesados para validación              |
| BPEL                             |                | Realiza las validaciones automáticas correspondientes al tipo de documento y arma el XML y Request hacia los servicios del PAC. | XML generado y enviado al PAC                 |
| PAC                              |                | Timbra y genera los archivos del documento fiscal.                                                                              | Archivos fiscales timbrados                   |
| Almex Services (Windows)         |                | Decodifica el Base64 recibido de la interfaz de SOA y lo almacena en la base de datos de Almex.                                 | Información almacenada en base de datos       |
| ALMEXSERVICES                    |                | Ejecuta una serie de JOBS que convierten y almacenan los archivos en el servidor Almex16.                                       | Archivos disponibles en servidor Almex16      |
| SOA                              |                | Ejecuta la dispersión de correos con los documentos adjuntos hacia el cliente.                                                  | Cliente recibe documentos fiscales por correo |

## **4. Herramientas, Recursos, Plataforma ó Servidor**

- **Plataforma:** ERP
- **Herramienta:** OTBI
- **Plataforma:** SOA (BSS Electronic Inv Manager)
- **Plataforma:** PAC (Proveedor de Autorización de Comprobantes)
- **Recurso:** Base64
- **Herramienta:** Almex Services (Windows)
- **Servidor:** Almex05
- **Servidor:** Almex16
- **Base de datos:** ALMEXSERVICES


## **5. Indicadores de Éxito
