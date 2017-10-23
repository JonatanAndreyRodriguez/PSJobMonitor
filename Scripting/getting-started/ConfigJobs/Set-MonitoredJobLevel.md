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
Set-MonitoredJobLevel [-InputObject] <Object> [-Critical] <switch> [-NonCritical] <switch>
```
## DESCRIPTION
Establece el nivel de criticidad de un job. Este nivel determina el flujo de reporte cuando se encuentra una falla de ejecución del job.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob | Set-MonitoredJobLevel -Critical
```

Establece todos los trabajos registrados como criticos.

### -------------------------- EXAMPLE 2 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob | Set-MonitoredJobLevel -NonCritical
```

Establece todos los trabajos registrados como no criticos.

## PARAMETERS

### -InputObject
Objetos para los cuales se establece el nivel de criticidad.

### -Critical
El job se marca como critico. Afecta los ANS con los clientes.

### -NonCritical
El job se marca como no critico.

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

## INPUTS
Puede canalizar el valor de InputObject desde la función Get-MonitoredJob.

## OUTPUTS
System.Void

## NOTES
Autor: Atorres

## RELATED LINKS

[Get-MonitoredJob](Get-MonitoredJob.md)(https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/GetInfoJobs/Get-MonitoredJob.md)

[Get-MonitoredServer](Get-MonitoredServer.md)(https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)

