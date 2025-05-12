## 1. Nombre del Proceso
H2H 
## 2. Objetivo del Proceso
Manipulación de extractos bancarios
## 3. Pasos del Proceso
  
BBVA manda los archivos todas las mañanas, por contrato Bancomer tiene de límite enviarlo antes de las  6:30 am.  
llega antes de las 5:30 am lo visualizamos en la siguiente ruta:
![[Pasted image 20250505123618.jpg]]

 hay una instrucción por parte de Almex en el proceso automático para la elaboración de los extractos y los lotes, que si llegan después de las 6:30 am de la mañana se ejecuta pero el proceso de ERP marca error.
Cuando esto sucede pedimos ayuda a el departamento de Sistema para que ellos nos ayuden a realizar los lotes y que  podamos visualizar los archivos TXT, con la información que Bancomer nos envía con los movimientos del día anterior.

Los extractos si no se elaboraron automáticamente a las 8 am en Oracle, los tenemos que subir manualmente.

| **Rol**                 | **Aplicativo**      | **Descripción**                                                        | **Resultado**                            |
| ----------------------- | ------------------- | ---------------------------------------------------------------------- | ---------------------------------------- |
| Usuario                 | Excel               |                                                                        | si se ejecuta correctamente se ve en ERP |
| Administrador(sistemas) | Terminal(MOBAXTERM) | Procesado manual de extractos bancarios cuando el proceso h2h da error | Generar los lotes (TXT) y el MT940 final |


## 4. Herramientas, Recursos ó Plataforma
- Servidor Almex (10.10.1.11)

## 5. Indicadores de Éxito


