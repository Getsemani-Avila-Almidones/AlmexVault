## **1. Identificación del Proceso**

**Nombre:** Facturación Electrónica
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

| **Rol** | **Aplicativo** | **Descripción** | **Resultado** |
| ------- | -------------- | --------------- | ------------- |
|         |                |                 |               |
|         |                |                 |               |
|         |                |                 |               |
|         |                |                 |               |
|         |                |                 |               |

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
