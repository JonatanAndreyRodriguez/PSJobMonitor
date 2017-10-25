---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Import-MonitoredJobHistory

## SYNOPSIS
Importa la información del histórico de jobs en una base de datos a la base de datos local de Monitoreo.

## SYNTAX

```powershell
Import-MonitoredJobHistory [-InputObject] <Object>
```

## DESCRIPTION
Importa la información del histórico de jobs en una base de datos a la base de datos local de Monitoreo.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-SqlJobDetail | Get-SqlJobExecutionHistory | Import-MonitoredJobHistory
```

## PARAMETERS

### -InputObject
Inofrmación del job a importar.

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
Puede canalizar el valor de InputObject desde la función Get-SqlJobExecutionHistory.

## OUTPUTS
System.Void

## NOTES
Autor: CFranco

## RELATED LINKS

[Get-MonitoredServer](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)

[Get-SqlJobDetail](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/GetInfoJobs/Get-SqlJobDetail.md)

[Get-SqlJobExecutionHistory](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/GetInfoJobs/Get-SqlJobExecutionHistory.md)
