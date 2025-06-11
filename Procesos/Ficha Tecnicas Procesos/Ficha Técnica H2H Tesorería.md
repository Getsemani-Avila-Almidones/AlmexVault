## **1. Identificación del Proceso**

H2H
## **2. Finalidad del Proceso**

Manipulación de extractos bancarios
## **3. Descripción del Procedimiento**

 **BBVA** envía los archivos todas las mañanas, con un límite contractual de envío antes de las 6:30 am. Normalmente, los archivos llegan antes de las 5:30 am, y se visualizan en la ruta correspondiente (_investigar_).
    
 Existe una instrucción dentro del proceso automático de Almex para la elaboración de los extractos y lotes. Si los archivos llegan después de las 6:30 am, el proceso se ejecuta, pero el sistema ERP marca un error.
    
 En caso de error, se solicita apoyo al departamento de Sistemas para generar los lotes manualmente y poder visualizar los archivos TXT con los movimientos del día anterior enviados por Bancomer.
    
 Si los extractos no se elaboran automáticamente a las 8:00 am en Oracle, se debe proceder a cargarlos manualmente.
### **Tabla de roles del proceso**

| **Rol**                 | **Aplicativo**       | **Descripción**                                                            | **Resultado**                                   |
| ----------------------- | -------------------- | -------------------------------------------------------------------------- | ----------------------------------------------- |
| Usuario                 | Excel                | Visualiza y verifica el extracto bancario si se ejecuta correctamente      | Si se ejecuta correctamente, se ve en ERP       |
| Administrador(sistemas) | Terminal (MOBAXTERM) | Procesa manualmente los extractos bancarios cuando el proceso H2H da error | Genera los lotes (TXT) y el archivo MT940 final |

---

## **4. Herramientas, Recursos, Plataforma ó Servidor**

- **Servidor:** Almex (10.10.1.11)

## **5. Indicadores de Éxito
