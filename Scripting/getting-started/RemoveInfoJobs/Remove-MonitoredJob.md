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

```
Remove-MonitoredJob [-JobId] <Guid>
```

## DESCRIPTION
{{Fill in the Description}}

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
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

### Puede canalizar el valor de InputObject desde la función Get-MonitoredJob.

## OUTPUTS

### System.Void

## NOTES

## RELATED LINKS

[[Get-MonitoredJob](Get-MonitoredJob.md)]()

[[Get-MonitoredServer](Get-MonitoredServer.md)]()

[[Enable-MonitoredJob](Enable-MonitoredJob.md)]()

