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

### -------------------------- EXAMPLE 3 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob -Name 'Cargue Bloqueos Tarjetas Cafam' | Set-MonitoredJobLevel -NonCritical
```

Marca el trabajo 'Cargue Bloqueos Tarjetas Cafam' como no crítico. También se puede usar el valor -JobId en lugar de -Name después de la función Get-MonitoredJob.

### -------------------------- EXAMPLE 4 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob -Name 'Cargue Bloqueos Tarjetas Cafam' | Set-MonitoredJobLevel -Critical
```

Marca el trabajo 'Cargue Bloqueos Tarjetas Cafam' como crítico.

## PARAMETERS

### -InputObject
Objetos para los cuales se establece el nivel de criticidad.

### -Critical
El job se marca como critico. Afecta los ANS con los clientes.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonCritical
El job se marca como no critico.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: True
Accept pipeline input: False
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

