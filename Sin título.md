SELECT  SYSDATE "fecha1"
, to_char( SYSDATE -6/24) as fecha_real
FROM DUAL