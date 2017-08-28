# FAQ

### Sintoma (MSGID=501):
Al intentar registrar un servidor de SQL Server, se genera el mensaje MSGID=501

### Solución:
Algunos nombres de servidor están restringidos para evitar conflictos con los nombres internos del sistema. Si el nombre del servidor coincide con este nombre, no se podrá registrar. 


### Sintoma (MSGID=502):
Al intentar registrar un servidor de SQL Server, se genera el mensaje MSGID=502

### Solución:
El servidor de SQL Server tiene registrados varios nombres como servidores de origen de trabajos. Corriga los nombres antes de continuar. La siguiente instrucción T/SQL debería retornar un solo registro. 

```sql
select [originating_server] from [msdb].[dbo].[sysoriginatingservers_view]
```
