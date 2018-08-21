---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Set-MonitoredJobDelayed

## SYNOPSIS
Establece si un job se marcara o no (1 ó 0 respectivamente), para ser reportado cuando se demore.

## DESCRIPTION
Establece si un job se marcara o no, para ser reportado cuando se demore. Por defecto los Jobs están marcados en la base de datos job_monitor.
Esta no-marcación no excluye al job de ser reportado como fallido.

## SYNTAX

```powershell
Set-MonitoredJobDelayed [-InputObject] <Object> [-Enable] <switch> [-Disable] <switch>
```

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob | Set-MonitoredJobDelayed -Enable
```

Establece todos los trabajos registrados como marcados para ser reportados cuando se demoren mas de x tiempo.

### -------------------------- EXAMPLE 2 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob | Set-MonitoredJobDelayed -Disable
```

Establece todos los trabajos registrados como no marcados para ser reportados cuando se demoren.

### -------------------------- EXAMPLE 3 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob -Name 'Backup1' | Set-MonitoredJobDelayed -Disable
```

Establece el trabajo 'Backup1' como no marcado para ser reportado cuando se demore.

### -------------------------- EXAMPLE 4 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob -JobId '161116E6-D65A-4228-96EF-4807697DDC32' | Set-MonitoredJobDelayed -Disable
```

Establece el trabajo con identificador '161116E6-D65A-4228-96EF-4807697DDC32' como no marcado para ser reportado cuando se demore.

## PARAMETERS

### -InputObject
Objetos que se marcarán.

### -Enable
El job se marcara para ser reportado si se demora más de x tiempo.

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

### -Disable
El job se desmarcara para ser reportado si se demora más de x tiempo.

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
Autor: CFranco

## RELATED LINKS

[Get-MonitoredJob](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/GetInfoJobs/Get-MonitoredJob.md)

[Get-MonitoredServer](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)
