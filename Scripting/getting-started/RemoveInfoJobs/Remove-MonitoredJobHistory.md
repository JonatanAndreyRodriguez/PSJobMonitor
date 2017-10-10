---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Remove-MonitoredJobHistory

## SYNOPSIS
Elimina la información del historial de todos los Job del registro de monitoreo, a partir del valor DaysReturnKeepHistoryJob.

## SYNTAX

```
Remove-MonitoredJobHistory [-JobId] <Guid>
```

## DESCRIPTION
Elimina la información del historial de todos los Job del registro de monitoreo, a partir del valor DaysReturnKeepHistoryJob.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MonitoredServer | Get-MonitoredJobHistory | Remove-MonitoredJobHistory
```

### -------------------------- EXAMPLE 2 --------------------------
```
Get-MonitoredServer | Get-MonitoredJobHistory -Name 'syspolicy_purge_history' | Remove-MonitoredJobHistory
```

## PARAMETERS

### -JobId
{{Fill JobId Description}}

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

[[Get-MonitoredServer](Get-MonitoredServer.md)]()

[[Get-MonitoredJobHistory](Get-MonitoredJobHistory.md)

.NOTES:
Autor: CFranco]()

