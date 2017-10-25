---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Remove-MonitoredJob

## SYNOPSIS
Elimina la información de un Job del registro de monitoreo.

## SYNTAX

```powershell
Remove-MonitoredJob [-JobId] <Guid>
```

## DESCRIPTION
Elimina la información de un Job del registro de monitoreo.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob | Remove-MonitoredJob
```

## PARAMETERS

### -JobId
Identificador del job que se debe eliminar.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

## INPUTS
Puede canalizar el valor de InputObject desde la función Get-MonitoredJob.

## OUTPUTS
System.Void

## NOTES
Autor: Atorres

## RELATED LINKS

[Get-MonitoredJob](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/GetInfoJobs/Get-MonitoredJob.md)

[Get-MonitoredServer](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)

