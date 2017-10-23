---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Disable-MonitoredJob

## SYNOPSIS
Deshabilita el Monitoreo de un Job para NO tenerlo en cuenta en los procesos de Jobs No Criticos, Cri-ticos y demorados.

## SYNTAX

```powershell
Disable-MonitoredJob [-InputObject] <Object>
```

## DESCRIPTION
Deshabilita el Monitoreo de un Job para NO tenerlo en cuenta en los procesos de Jobs No Criticos, Cri-ticos y demorados.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MonitoredServer | Get-MonitoredJob | Disable-MonitoredJob
```

### -------------------------- EXAMPLE 2 --------------------------
```
Get-MonitoredServer | Get-MonitoredJob -Name 'MyJob' | Disable-MonitoredJob
```

Deshabilita el monitoreo del job con nombre 'MyJob'

### -------------------------- EXAMPLE 3 --------------------------
```
Get-MonitoredServer | Get-MonitoredJob -JobId '255298ab-7712-49e6-a4e8-9fcb1ccd925d' | Disable-MonitoredJob
```

Deshabilita el monitoreo del job con identificador '255298ab-7712-49e6-a4e8-9fcb1ccd925d'

## PARAMETERS

### -InputObject
{{Fill InputObject Description}}

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

### Puede canalizar el valor de InputObject desde la función Get-MonitoredJob.

## OUTPUTS

### System.Void

## NOTES

## RELATED LINKS

[Get-MonitoredJob](Get-MonitoredJob.md)()

[Get-MonitoredServer](Get-MonitoredServer.md)()

[Enable-MonitoredJob](Enable-MonitoredJob.md)()

