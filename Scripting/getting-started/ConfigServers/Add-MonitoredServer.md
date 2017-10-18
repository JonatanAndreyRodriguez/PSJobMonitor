---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Add-MonitoredServer

## SYNOPSIS
Crea o actualiza la configuracion de los servidores de SQLServer que se van a monitorear.

## SYNTAX

```powershell
Add-MonitoredServer [-ConnectionString] <String[]> [-Force]
```

## DESCRIPTION
Crea o actualiza la configuracion de los servidores que se van a monitorear guardar en el archivo PSJobMonitor.config.
Si la cadena de conexión existe, entonces reemplaza los valores actuales por los nuevos.
Si no existe, se crea una nueva entrada en el archivo.

> NOTA: Se necesitan permisos de Administrador para completar la función.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Add-MonitoredServer -ConnectionString 'Data Source=MyServer;Initial Catalog=Master;User ID=Usuario;Password=Pwd'
```

Agrega una entrada a la configuracion de los servidores de SQLServer que se van a monitorear.

## PARAMETERS

### -ConnectionString
Cadena de conexión que se debe agregar a los servidores que están siendo monitoreados.

> NOTA: El usuario en la cadena de conexión debe tener permisos de conexión (al menos en modo lectura) con la base de datos msbd de la instancia especificada.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Force
Cuando está presente, omite la validación de conexión, es decir, guarda el valor sin comprobar la conexión.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

Puede canalizar el valor de ConnectionString.

## OUTPUTS

Processa.Management.Automation.JobMonitor.MonitoredServer

## NOTES

- Autor: CFranco
- Modificaciones: 2017-07-26 Atorres. Se mejora documentación. Se corrige manejo del Pipeline.
- Modificaciones: 2017-10-11 Cfranco. Se elimina el Force.


## RELATED LINKS

[Get-MonitoredServer](Get-MonitoredServer.md)

[Remove-MonitoredServer](Remove-MonitoredServer.md)


