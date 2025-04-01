## 📄 **Alcance del Catálogo de Servidores**

Este documento tiene como objetivo proporcionar una **vista clara, organizada y actualizada** del estado de todos los servidores de la infraestructura, su **nivel de criticidad** y **datos mínimos de acceso**. Permite tomar **decisiones rápidas ante fallas, mantenimientos o renovaciones**.

## Guía rápida para identificar prioridad o estado de **🔧 Servidores**

|**Clasificación**|**Cómo identificarlo**|
|---|---|
|🔴 Alta (Crítico)|Si se cae, afecta el negocio directamente. Es usado por muchas personas o sistemas.|
|🟡 Media (Importante)|Es importante, pero se puede trabajar sin él por un tiempo corto.|
|🟢 Baja (No crítica)|Su uso es ocasional o complementario. No detiene actividades si falla.|
|⚫ 🕸️ Obsoleto | Hardware viejo, sin soporte del fabricante o sin actualizaciones recientes.|
|⚠️ 🚧 A punto de decomisar | Ya se planea apagarlo o migrarlo. Tiene un reemplazo listo o en pruebas.|


### 🔴 **Alta (Crítico)**

> El servidor es **esencial para el funcionamiento diario** de la organización. Si falla, impacta de inmediato las operaciones, como el acceso a sistemas internos, correo, o servidores de producción.

📌 _Ejemplo:_ Un servidor que aloja la intranet corporativa, base de datos de clientes, o el sistema de ventas.

---

### 🟡 **Media (Importante)**

> El servidor es **útil y necesario**, pero su caída **no detiene completamente** las operaciones. Puede haber alternativas temporales o soluciones de respaldo.

📌 _Ejemplo:_ Servidor de respaldo, pruebas, o que aloja servicios complementarios como documentación interna.

---

### 🟢 **Baja (No crítica)**

> El servidor es **complementario o de apoyo**. Si deja de funcionar, **no hay un impacto significativo** en el día a día. Puede esperar mantenimiento o reemplazo.

📌 _Ejemplo:_ Servidor de desarrollo, sandbox, o de almacenamiento histórico.

--- 

### ⚫ **🕸️ Obsoleto**

> El servidor **ya no cumple con los estándares actuales**. Tiene hardware o software desactualizado, sin soporte, y puede representar un riesgo de seguridad o estabilidad. Sigue en uso solo por necesidad puntual o por falta de migración.

📌 _Ejemplo:_ Servidores con sistemas operativos antiguos o sin parches disponibles.

---

### ⚠️ **🚧 A punto de decomisar**

> El servidor está **marcado para ser retirado**. Ya se está migrando su contenido o funciones a otro equipo, o será apagado pronto. No debe agregarse nada nuevo en él y debe considerarse solo para uso temporal o en transición.

📌 _Ejemplo:_ Servidores que serán reemplazados por nuevas plataformas físicas o virtuales.