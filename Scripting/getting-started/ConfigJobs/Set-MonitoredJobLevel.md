---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Set-MonitoredJobLevel

## SYNOPSIS
Establece el nivel de criticidad de un job.

## SYNTAX

```powershell
Set-MonitoredJobLevel [-InputObject] <Object> 
```

### Critical
```
Set-MonitoredJobLevel -InputObject <Object> -Critical <switch> -NonCritical <switch>
```

### NonCritical
```
Set-MonitoredJobLevel -InputObject <Object> [-NonCritical]
```

## DESCRIPTION
Establece el nivel de criticidad de un job.
Este nivel determina el flujo de reporte cuando se encuentra una falla de ejecución del job.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MonitoredServer | Get-MonitoredJob | Set-MonitoredJobLevel -Level 'Critical'
```

Establece todos los trabajos registrados como criticos.

### -------------------------- EXAMPLE 2 --------------------------
```
Get-MonitoredServer | Get-MonitoredJob | Set-MonitoredJobLevel -Level 'NonCritical'
```

Establece todos los trabajos registrados como no criticos.

## PARAMETERS

### -InputObject
Objetos para los cuales se establece el nivel de criticidad.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Critical
{{Fill Critical Description}}

```yaml
Type: SwitchParameter
Parameter Sets: Critical
Aliases: 

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonCritical
{{Fill NonCritical Description}}

```yaml
Type: SwitchParameter
Parameter Sets: NonCritical
Aliases: 

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### Puede canalizar el valor de InputObject desde la función Get-MonitoredJob.

## OUTPUTS

### System.Void

## NOTES
Autor: Atorres

## RELATED LINKS

[[Get-MonitoredJob](Get-MonitoredJob.md)]()

[[Get-MonitoredServer](Get-MonitoredServer.md)]()

