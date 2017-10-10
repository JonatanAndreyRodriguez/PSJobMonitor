---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Import-MonitoredJobHistory

## SYNOPSIS
Importa la informaci ³n del hist ³rico de jobs en una base de datos a la base de datos local de Monitoreo.

## SYNTAX

```
Import-MonitoredJobHistory [-InputObject] <Object>
```

## DESCRIPTION
Importa la informaci ³n del hist ³rico de jobs en una base de datos a la base de datos local de Monitoreo.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MonitoredServer | Get-SqlJobDetail | Get-SqlJobExecutionHistory | Import-MonitoredJobHistory
```

## PARAMETERS

### -InputObject
Inofrmaci ³n del job a importar.

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

### Puede canalizar el valor de InputObject desde la funci ³n Get-SqlJobExecutionHistory.

## OUTPUTS

### System.Void

## NOTES

## RELATED LINKS

[[Get-MonitoredServer](Get-MonitoredServer.md)]()

[[Get-SqlJobDetail](Get-SqlJobDetail.md)]()

[[Get-SqlJobExecutionHistory](Get-SqlJobExecutionHistory.md)

.NOTES:
Autor: CFranco]()

