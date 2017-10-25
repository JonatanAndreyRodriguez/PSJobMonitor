---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-SqlJobExecutionDelayed

## SYNOPSIS
Obtiene la información de los jobs que no han terminado de ejecutarse luego de un periodo de tiempo.
Se toma como base el valor configurado en el archivo config
en la variable "JobDelayIndicatorMinutes".

## SYNTAX

```powershell
Get-SqlJobExecutionDelayed [-InputObject] <Object> [[-Name] <String>]
```

## DESCRIPTION
Obtiene la información de los jobs que no han terminado de ejecutarse luego de un periodo de tiempo.
El periodo de tiempo (en minutos), se configura en el archivo PSJobMonitor.config.
Puede utilizar las funciones Get-Configuration y Set-Configuration para leer o actualizar este valor.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-SqlJobExecutionDelayed
```

Obtiene la información de todos los jobs/trabajos cuya finalización no ha terminado luego del periodo de tiempo configurado.

## PARAMETERS

### -InputObject
Datos del servidor en donde se buscan los jobs.

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

### -Name
Nombre del Job a buscar.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: *
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS
Puede canalizar el valor de InputObject desde la función Get-MonitoredServer.

## OUTPUTS
Processa.Management.Automation.PSJobMonitor.SqlJobOutcome

## NOTES
Autor: Atorres

## RELATED LINKS

[Get-MonitoredServer](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)

