- Crear data model nombre con terminación DM  EN CARPETA DM
![[Pasted image 20250522083056.png]]

- Después ve a https://docs.oracle.com/en/cloud/saas/index.html para poder ver e identificar las tablas que debes usar con sus módulos correctos
![[Pasted image 20250522083552.png]]
- Verificar en el ERP l modulo y ver información para poder hacer test
![[Pasted image 20250522083755.png]]

- Te metes al modulo y del modulo a APis y Schema, luego a tables and Views for SCM para visualizar la tabla

- Al identificar las tablas para saber que campo necesitas consúltala y extraer las columnas que necesitas para tu query
![[Pasted image 20250522090555.png]]

- Después de ir seleccionando los campos armas el query, quedaría de la siguiente forma Columnas, tablas (de donde se tomaran las columnas de las tablas)

``` sql
SELECT   ESIB.ITEM_NUMBER

        ,ESIB.CREATION_DATE

        ,ESIB.ANABLED_FLAG

        ,ESIB.APPROVAL_STATUS

        ,ESIB.START_DATE_ACTIVE

        ,ESIB.END_DATE_ACTIVE

        ,ESIB.INVENTORY_ITEM_ID

        ,ESIB.ORGANIZATION_ID

  

        ,ESITL.DESCRIPTION

        ,ESITL.LONG_DESCRIPTION

        ,ESITL.INVENTORY_ITEM_ID INVENTARY_ITEM_ID_TL

        ,ESITL.ORGANIZATION_ID ORGANIZATION_ID_TL

        ,ESITL.LANGUAGE

        ,ESITL.CREATION_DATE CREATION_DATE_TL

  

FROM EGP_SYSTEM_ITEMS_B ESIB

    ,EGP_SYSTEM_ITEMS_TL ESITL

  

WHERE 1 = 1

    AND ESIB.INVENTORY_ITEM_ID = ESITL.INVENTORY_ITEM_ID

    AND ESIB.ORGANIZATION_ID = ESITL.ORGANIZATION_ID

    AND ITEM_NUMBER = '100-010-403'
```
