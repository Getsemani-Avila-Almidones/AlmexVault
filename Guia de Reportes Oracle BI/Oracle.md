## 🧾 Purchase Order (PO) – Órdenes de Compra

### Secciones del Reporte

- **Headers (Encabezados)**: Información general de la orden de compra.
    
- **TL (Technical Layer / Información Técnica)**: Detalles técnicos relacionados con la orden.
    
- **POZ (Proveedores)**: Información de los proveedores asociados.
    
- **Locación**:  
    Para visualizar o agregar una descripción de la locación:
    
    - Ir a la opción **"Más"** en el reporte.
        
    - Seleccionar **"Propiedades"**.
        

### 🔍 Origen del Data Model, Query y Reporte

Para identificar el origen de los datos en un reporte:

1. Seleccionar la opción **"Editar Reporte (Plantilla)"**.
    
2. En la parte superior izquierda, hacer clic sobre el nombre del **Data Model**.
    
3. Al abrir el Data Model:
    
    - Copiar el **query** y pegarlo en un editor SQL.
        
    - Identificar las tablas utilizadas en la cláusula **FROM**.
        
    - Analizar a qué módulo pertenecen estas tablas para determinar el **origen principal** de los datos.
        
4. Si el query contiene tablas de **múltiples módulos**:
    
    - Revisar la cláusula **SELECT** para identificar de qué módulo provienen la mayoría de los campos.
        
    - Esto ayuda a determinar el módulo predominante en el reporte.
        
### 📁 Exportación y Formatos

- **XML**: Usado para integración con proyectos o plataformas técnicas.
    
- **Excel, PDF, CSV**: Opciones disponibles para el usuario final desde la interfaz del reporte.