---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-MonitoredJobMissing

## SYNOPSIS
Obtiene la información de los jobs que se registraron para monitoreo, pero que ya no existen en el servidor de SQL Server.

## SYNTAX

```powershell
Get-MonitoredJobMissing [-InputObject] <Object>
```

## DESCRIPTION
Si un job se importa para monitoreo y luego se elimina del servidor de SQL, quedará "desaparecido".
Esta función permite identificarlos.
Puede utilizar la función Remove-MonitoredJob para eliminar esta información (ejemplo 2).

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJobMissing
```

Obtiene la información de todos los jobs "desaparecidos" en todos los servidores registrados.

### -------------------------- EXAMPLE 2 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJobMissing | Remove-MonitoredJob
```

Elimina la información de todos los jobs "desaparecidos" en todos los servidores registrados.

## PARAMETERS

### -InputObject
Cadena de conexión que se debe agregar a los servidores que están siendo monitoreados.
> NOTA: El usuario en la cadena de conexión debe tener permisos de conexión (al menos en modo lectura) con la base de datos msbd de la instancia especificada.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## INPUTS
Puede canalizar el valor de InputObject desde la función Get-MonitoredServer.

## OUTPUTS
Processa.Management.Automation.PSJobMonitor.SqlJobDetail

## NOTES
Autor: Atorres

## RELATED LINKS

[Get-MonitoredServer](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)

[Remove-MonitoredJob](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/RemoveInfoJobs/Remove-MonitoredJob.md)

