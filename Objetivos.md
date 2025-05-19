
### ✅ **SMART01: Migración de Aplicaciones Legadas**
#MIGRACION_APPS 
- [[SMART01 - Bitácora]]

| Área                          | Tarea / Descripción                                                                                     | Estado      | Indicador / Entregable                                                                         |
| ----------------------------- | ------------------------------------------------------------------------------------------------------- | ----------- | ---------------------------------------------------------------------------------------------- |
| 📦 Inventario                 | Registro y clasificación de los 32 aplicativos del entorno operativo. Identificación de 9 como legados. | 🔄En Curso  | Tabla de inventario en Obsidian y Git, lista de apps legadas con IDs y nombres                 |
| 🔁 Control de versiones       | Subida de código a GitHub de AlmexDLL, Essentials, y otros sistemas (Concur, H2H, Segurinet).           | 🔄 En curso | Repositorios en GitHub por aplicación, con ramas versionadas, commits con cambios trazables    |
| 🧠 Base de Conocimiento       | Uso de Obsidian y Git para registrar conocimiento técnico junto a _Campa, Omar, Josué, y Victor_.       | 🔄 En curso | Repositorio de conocimiento con enlaces a infraestructuras y aplicaciones                      |
| 🔖 Etiquetado                 | Clasificación por criticidad, legado, mantenimiento requerido, dependencia con infra actual.            | 🔄 En curso | Etiquetas aplicadas en la base de conocimiento o sistema de documentación                      |
| 🐞 Reporte de errores         | Crear plantilla y repositorio para registrar errores detectados durante análisis y uso.                 | 🚧 TBD      | Archivo central con errores detectados, causa raíz, solución y responsable                     |
| 📊 Métricas de disponibilidad | Identificación de puntos de falla o soporte frecuente en apps como Concur, H2H y Oracle-CXP.            | ⚠️ Parcial  | Lista de eventos de soporte por app, causas recurrentes, estimación de frecuencia y criticidad |
| 📅 Plan de actualizaciones    | Crear un cronograma de refactor/migración con prioridades, fases, responsables.                         | 🚧 TBD      | Roadmap en Obsidian / Youtrack con fechas objetivo, prioridad, responsables, dependencias      |


> **Observaciones clave**
> - Se dio un primer acercamiento técnico a H2H, especialmente en procesos sensibles de **Nómina y Cuentas por Pagar**, con guía preliminar de _Josue Jimenez_ y _Victor Santillan_.

### 📊 **SMART02 – Diagrama de Integraciones**
#Diagramas_de_Integraciones 
- [[SMART02 - Bitácora]]

| Área                              | Tarea / Descripción                                                                            | Estado       | Indicador / Entregable                                                                 |
| --------------------------------- | ---------------------------------------------------------------------------------------------- | ------------ | -------------------------------------------------------------------------------------- |
| 🧭 Discovery tecnológico          | Investigación de herramientas para generar diagramas automáticos desde base de datos.          | 🔄 En curso  | Evaluación técnica de Mermaid.js, Graphviz, GoJS, etc.                                 |
| 🗃️ Base de datos de arquitectura | Registro planificado de servidores, contenedores, VMs, SaaS, etc., en app dedicada.            | ⚠️ Parcial   | Diseño de base de datos, definición de entidades y relaciones                          |
| 🔄 Integración con catálogo       | Dependencia directa con la iniciativa de JJ Campa para consolidar datos de aplicativos.        | ⚠️ Parcial   | Conectividad e interoperabilidad con el catálogo general                               |
| 📐 Prototipo gráfico              | Diagrama de ejemplo para sistema CONCUR usando Mermaid.js.                                     | ✅ Completado | Diagrama funcional de arquitectura con elementos del flujo actual y mejoras propuestas |
| 🧩 Proyecto formal                | Consolidar visión del _AlmexArchitectureTool_web_ y presentarlo como solución de arquitectura. | 🚧 WIP       | Presentación oficial con alcance, beneficios y roadmap de implementación               |

### 🏎️ **SMART03: Capacitación Individual (OCI)**

| Área                   | Tarea / Descripción                                                                   | Estado       | Indicador / Entregable                                                                 |
| ---------------------- | ------------------------------------------------------------------------------------- | ------------ | -------------------------------------------------------------------------------------- |
| 🎓 Diagnóstico inicial | Identificación de recursos gratuitos en Oracle MyLearn para comenzar la capacitación. | ✅ Completado | Registro en plataforma y selección de cursos iniciales                                 |
| 📘 Cursos básicos      | Completar módulos introductorios en OCI (despliegue, desarrollo y plataforma cloud).  | 🔄 En curso  | Módulos con 100% de avance: Deployment, Development Services, Intro to Platform        |
| 🏫 Learning Roadmap    | Diseño de un _Learning Path_ adecuado a las necesidades del negocio y del puesto.     | 🚧 TBD       | Plan personalizado con cursos prioritarios, niveles de profundidad y tiempos estimados |
| 📑 Evidencia de avance | Documentación de módulos, tiempos, y aplicabilidad práctica.                          | ⚠️ Parcial   | Capturas de pantalla, resumen técnico, archivo en Obsidian progreso personal           |

![[Pasted image 20250430085935.png]]


### 📖 **SMART04: Documentación**

### 📊 **Bitácora SMART04 – Documentación**

| Área                         | Tarea / Descripción                                                                                      | Estado       | Indicador / Entregable                                                                      |
| ---------------------------- | -------------------------------------------------------------------------------------------------------- | ------------ | ------------------------------------------------------------------------------------------- |
| 🧩 Aplicativos               | Documentación técnica y funcional de los sistemas registrados (32+) priorizando los legados.             | 🔄 En curso  | Fichas técnicas por aplicación, catálogos en Git/Obsidian, relaciones con infraestructura   |
| 🔁 Procesos                  | Registro de procesos clave con enfoque en operación y sistemas, documentación en conjunto con el equipo. | 🔄 Parcial   | 10 procesos identificados, documentados a alto nivel en Obsidian                            |
| 🖥️ Infraestructura          | Mapeo de servidores, clusters, VMs, SaaS, etc. con trazabilidad hacia aplicativos e integraciones.       | 🔄 En curso  | Fichas técnicas de activos, catálogos de infraestructura, dependencias documentadas         |
| 🛠️ Desarrollo               | Documentación de lógica técnica, scripts, flujos de integración y librerías internas.                    | 🚧 WIP       | GitHub con repositorios versionados (AlmexDLL, Essentials), estructura viva en Git/Obsidian |
| 🔧 Mantenimiento             | Manuales operativos, backups, tareas recurrentes, y acciones correctivas en servicios críticos.          | ⏳ Pendiente  | Fichas con tareas programadas, dependencias y responsables, integradas a herramienta o wiki |
| 🔂 Control de Cambios        | Registro de cambios relevantes en software, infraestructura y procesos.                                  | ⏳ Pendiente  | Bitácora de cambios con fechas, responsables y vínculos a tickets o commits                 |
| 🧪 QA / UAT                  | Documentación de pruebas de aceptación técnica funcional (ej. pruebas GLPI, apps críticas).              | 🚧 En piloto | Plantilla de UAT implementada y validación con equipo de soporte TI (micropiloto activo)    |
| ✅ DoD (Definition of Done)   | Establecer criterios de cierre para tareas de desarrollo e implementación de sistemas.                   | ⏳ Pendiente  | Checklist validado por QA o responsables de proyecto, vinculado al cierre formal de tareas  |
| 📂 Fichas Técnicas           | Estructura estándar para registrar activos (apps, infra, procesos) incluyendo datos clave y relaciones.  | ✅ Completado | Plantilla definida, ejemplos activos en Git/Obsidian                                        |
| 🗂️ Catálogos Documentales   | Organización de información en conjuntos por área: apps, procesos, infra y documentación funcional.      | ✅ Completado | Archivos ordenados, buscables, y versionados; relación uno a uno con la herramienta         |
| 🧰 AlmexArchitectureTool_web | Herramienta en desarrollo para gestionar toda la documentación y actualizar diagramas de arquitectura.   | 🚧 WIP       | Prototipo funcional, estructura validada, conexión futura con catálogos y fichas            |
### 🎫 **SMART05: Actualización del Sistema de Tickets e inventario (GLPI)**

- [[SMART 01 - Tareas Issues]]
- [[SMART 01  - Bitácora Update 9.3 a  10.03]]

| Área                            | Tarea / Descripción                                                                     | Estado         | Indicador / Entregable                                                                              |
| ------------------------------- | --------------------------------------------------------------------------------------- | -------------- | --------------------------------------------------------------------------------------------------- |
| 🗂️ Diagnóstico y documentación | Revisión del proceso oficial de migración y registro detallado en bitácora técnica.     | ✅ Completado   | Bitácora de migración actualizada con fuentes oficiales y pasos realizados                          |
| 🧪 Entorno de pruebas           | Clonación de servidor productivo para pruebas sin afectar operaciones reales.           | ✅ Completado   | Servidor espejo funcional, instalación validada, accesos confirmados                                |
| 🔄 Migración técnica            | Ejecución de scripts de actualización y despliegue de nueva versión de GLPI.            | ✅ Completado   | Nueva versión operativa en pruebas, base de datos migrada, validación básica completada             |
| 🔌 Pruebas de integración       | Verificación de conectividad, DNS, funciones críticas y acceso para usuarios técnicos.  | ✅ Completado   | Registro de resultados por componente y entorno                                                     |
| 🧪 Pruebas funcionales          | Pruebas UAT/QA realizadas por el equipo de soporte técnico sobre funcionalidades clave. | 🔄 En progreso | 80% de avance, retroalimentación en proceso, validación esperada para cierre en siguiente iteración |
| 🧾 Issues y mejoras             | Registro de problemas menores y solicitudes de ajuste por el equipo funcional y gerencia. | ⏳ Pendiente    | Documento de tareas e incidencias actualizado post-UAT                                              |
| ✅ Conclusión y cierre          | Evaluación del impacto y esfuerzo de la migración.                                       | ⏳ Pendiente    | Informe de cierre, lecciones aprendidas, acciones recomendadas                                      |

