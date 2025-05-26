## 🧭 ¿Qué es un Workspace en Oracle APEX?

Un **workspace** (espacio de trabajo) en Oracle APEX es un entorno lógico y aislado dentro de una instancia de APEX donde los desarrolladores pueden:

- Crear aplicaciones.
    
- Gestionar datos.
    
- Administrar usuarios y seguridad.
    

Un workspace actúa como una **caja independiente**, permitiendo que varios equipos trabajen en la misma instancia de APEX sin interferirse.

---

## 🧩 ¿Cómo funciona?

### 1. **Estructura general**

- Una **instancia de APEX** puede tener **múltiples workspaces**.
    
- Cada workspace está vinculado a uno o más **schemas de base de datos** (esquemas Oracle).
    
- Los objetos creados (tablas, vistas, paquetes PL/SQL) viven en esos **schemas asociados**, pero los usuarios desarrollan y administran aplicaciones desde el workspace.
    

---

## 🛠️ ¿Qué puedes hacer en un Workspace?

- Crear aplicaciones web (formulario, reportes, dashboards).
    
- Gestionar y consultar datos.
    
- Crear procesos automáticos con PL/SQL.
    
- Configurar autenticación y autorización.
    
- Definir usuarios de la app o del entorno de desarrollo.
    

---

## 🧑‍💼 Tipos de usuarios

1. **Administradores del Workspace**
    
    - Gestionan usuarios, esquemas y configuración general.
        
    - Pueden crear nuevas apps, importar/exportar objetos.
        
2. **Desarrolladores**
    
    - Crean y modifican aplicaciones.
        
    - Acceden a SQL Workshop, App Builder, REST services.
        
3. **Usuarios finales**
    
    - Usan las apps, pero **no acceden al entorno de desarrollo**.
        

---

## 🛑 ¿Qué NO es un Workspace?

- **No es un schema de base de datos**, aunque esté vinculado a uno.
    
- **No es compartido automáticamente** con otros workspaces.
    
- **No incluye acceso a otras apps de otros workspaces**, salvo que lo permitas explícitamente.
    

---

## ✍️ Crear un Workspace (como administrador)

1. Entra al link u otra instancia APEX.
    
2. Ve a “Administration” → “Manage Workspaces”.
    
3. Haz clic en “Create Workspace”.
    
4. Define:
    
    - **Nombre del workspace**.
        
    - **Schema(s)** asociados.
        
    - **Credenciales del administrador del workspace**.
        
5. Finaliza y accede con el usuario creado.