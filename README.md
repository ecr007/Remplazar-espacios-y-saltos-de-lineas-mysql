# Remplazar-espacios-y-saltos-de-lineas-mysql

```sql
START TRANSACTION

UPDATE table SET first_name = TRIM(REPLACE(REPLACE(REPLACE(REPLACE(REPLACE(first_name,'  ',''),'\t',' '),'\n',''),'\r',''),'   ',' ')) WHERE id = 0

ROLLBACK

COMMIT

```
