## **1. Identificación del Proceso**

Pesos báscula
## **2. Finalidad del Proceso**

Transmitir los pesos entre los diferentes sistemas ERP, OTM y base de datos Almex
## **3. Descripción del Procedimiento**

El operador de báscula consulta una orden de embarque en la aplicación de báscula en el momento del pesaje de un transporte.  
**El sistema genera los pesos de la carga.  
El operador ejecuta el guardado y envío de los pesos en el sistema.  
El sistema valida los lotes en el ERP de Oracle
El sistema valida los parámetros del producto y envía notificación a un grupo de usuarios sobre su validación.  
El sistema captura los pesos en el módulo de inventario del ERP y en el módulo de logística de OTM.

| **Rol**             | **Aplicativo**        | **Descripción**                                                  | **Resultado**                           |
| ------------------- | --------------------- | ---------------------------------------------------------------- | --------------------------------------- |
| Operador de báscula | Aplicación de báscula | Consulta la orden de embarque y ejecuta el pesaje                | Inicio del proceso de registro de carga |
| Sistema de báscula  | Aplicación de báscula | Genera los pesos de la carga                                     | Pesos generados automáticamente         |
| Operador de báscula | Aplicación de báscula | Guarda y envía los datos generados                               | Datos enviados al sistema               |
| Sistema ERP         | ERP Oracle            | Valida los lotes correspondientes                                | Lotes validados correctamente           |
| Sistema ERP         | ERP Oracle            | Verifica parámetros del producto y notifica al grupo de usuarios | Validación comunicada                   |
| Sistema ERP         | ERP Oracle / OTM      | Registra los pesos en el módulo de inventario y módulo logístico | Información registrada en ambos módulos |
## **4. Herramientas, Recursos, Plataforma ó Servidor**


- **Herramienta:** Aplicación de escritorio de báscula
- Plataforma: ERP Oracle

## **5. Indicadores de Éxito
registro correcto de pesos en ERP y OTM 


