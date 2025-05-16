## **1. Identificación del Proceso**

**Nombre:** Almex Services

## **2. Finalidad del Proceso**

Almacenamiento de archivos
## **3. Descripción del Procedimiento**
El servicio (se investiga) de Windows se ejecuta de forma continua (24/7) en el servidor **almex05** y permanece a la espera de solicitudes en formato **JSON** provenientes de las interfaces de **SOA**, las cuales envían documentos codificados en **Base64**.  
Una vez recibida la solicitud, esta es decodificada y almacenada en la base de datos.  
Posteriormente, se ejecuta un **Store Procedure** que transforma y almacena los documentos en el servidor **almex16**.

| **Rol** | **Aplicativo** | **Descripción** | **Resultado** |
| ------- | -------------- | --------------- | ------------- |
|         |                |                 |               |


## **4. Herramientas, Recursos, Plataforma ó Servidor**


- **Servidor:** Almex05
    
- **Servidor:** Almex16
	    ´
- **Plataforma:** Servicio de Windows
    
- **Herramienta:** SQL Server

## **5. Indicadores de Éxito**
Documento almacenado en almex16
