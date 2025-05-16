## **1. Identificación del Proceso**

**Nombre:** Certificados de Calidad EALMEX
## **2. Finalidad del Proceso**

Generar un precertificado y certificado de calidad al final del proceso de cadena de suministros
## **3. Descripción del Procedimiento**

El operador de distribución ingresa al portal **eAlmex**.  
El operador consulta una orden de embarque.  
El sistema valida que se tenga el pesaje correcto dentro de sus parámetros objetivos y, si no, el sistema asigna automáticamente valores dentro del rango correcto.  
El operador agrega sellos y lotes.  
El operador ejecuta el envío de la solicitud de certificado de calidad.  
El sistema **eAlmex**, mediante una solicitud por API (**investigar**), actualiza la información del pesaje en el **ERP**.  
Una vez que se tiene la información en el **ERP**, los datos son extraídos mediante el reporte en **OTBI** y consultados por la interfaz de certificados de calidad en **SOA**.  
El sistema **SOA** transforma un PDF de acuerdo con las plantillas configuradas en el sistema y utiliza el servicio de almacenamiento de archivos (**Almex Services**).  
Se aloja el PDF del certificado de calidad.  
El operador puede consultar y descargar el certificado desde el portal **eAlmex**.

| **Rol** | **Aplicativo** | **Descripción** | **Resultado** |
| ------- | -------------- | --------------- | ------------- |
|         |                |                 |               |
|         |                |                 |               |
|         |                |                 |               |
|         |                |                 |               |
|         |                |                 |               |

## **4. Herramientas, Recursos, Plataforma ó Servidor**


- **Plataforma:** ERP
- **Herramienta:** API (**investigar**)
- **Plataforma:** SOA
- **Plataforma:** OTBI Oracle
- **Plataforma:** Portal eAlmex
- **Recurso:** Plantilla
- **Herramienta:** Almex Services
## **5. Indicadores de Éxito
PDF de certificado de calidad 


