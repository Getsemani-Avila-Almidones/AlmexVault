## 1. Nombre del Proceso
Almex services
## 2. Objetivo del Proceso
Almacenamiento de archivos
## 3. Pasos del Proceso
Este servicio de Windows se ejecuta 24/7 en el servidor almex05 y espera una solicitud por JSON de las interfaces de SOA que le envía documentos codificados en base64
Una vez recibida la solicitud esta se decodifica y se almacena en base de datos 
Se ejecuta un Store procedure donde transforma y almacena en el servidor almex16 los documentos 

| **Rol** | **Aplicativo** | **Descripción** | **Resultado** |
| ------- | -------------- | --------------- | ------------- |
|         |                |                 |               |
|         |                |                 |               |


## 4. Herramientas, Recursos ó Plataforma
servidor almex05, almex16, windows servicio, sql server

## 5. Indicadores de Éxito
Documento almacenado en almex16
