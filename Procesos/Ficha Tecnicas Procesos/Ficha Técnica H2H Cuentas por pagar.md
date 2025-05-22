## **1. Identificación del Proceso**

H2H Cuentas por Pagar

## **2. Finalidad del Proceso**

## **3. Descripción del Procedimiento**

El Jefe de Cuentas por Pagar genera los pagos a proveedores en **Oracle**.  
El sistema **Oracle** deposita los archivos correspondientes en el servidor **FTP** con dirección **10.10.1.11**.
El servidor ejecuta automáticamente scripts que renombran los archivos y los mueven a una carpeta de **salida**.  
El banco **BBVA** accede al servidor **FTP**, toma los archivos ubicados en la carpeta de salida para su validación, registro y posterior ejecución del pago a proveedores.

 

| **Rol**        | **Aplicativo** | **Descripción**                                   | **Resultado**                      |
| -------------- | -------------- | ------------------------------------------------- | ---------------------------------- |
| Jefe de CxP    | Oracle         | Genera los pagos a proveedores                    | Inicio del proceso de pagos        |
| Sistema Oracle | -              | Deposita archivos en el servidor FTP              | Archivos disponibles para el banco |
| Servidor FTP   | Scripts        | Renombra y mueve los archivos a la carpeta salida | Archivos listos para el banco      |
| Banco BBVA     | -              | Accede, valida y procesa los archivos             | Ejecución del pago a proveedores   |

## **4. Herramientas, Recursos, Plataforma ó Servidor
- **Plataforma:** Oracle ERP
- **Servidor FTP:** 10.10.1.11
- **Herramienta:** Scripts de renombrado y traslado automático
- **Carpeta de procesamiento:** Carpeta de salida (para envío a BBVA)
- **Entidad externa:** BBVA
## **5. Indicadores de Éxito
Correcta ejecución de pago a proveedor