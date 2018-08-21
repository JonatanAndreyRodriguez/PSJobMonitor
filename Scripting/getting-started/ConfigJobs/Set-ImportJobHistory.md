---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Set-ImportJobHistory

## SYNOPSIS
Establece si un job se marcara o no (1 ó 0 respectivamente), para guardar su historial de ejecuciones.

## DESCRIPTION
Establece si un job se marcara o no, para guardar su historial de ejecuciones. Por defecto los Jobs están marcados en la base de 
datos job_monitor.

## SYNTAX

```powershell
Set-ImportJobHistory [-InputObject] <Object> [-Enable] <switch> [-Disable] <switch>
```

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob | Set-ImportJobHistory -Enable
```

Establece todos los trabajos registrados como marcados para que se guarde su historico en la base de datos job_monitor.

### -------------------------- EXAMPLE 2 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob | Set-ImportJobHistory -Disable
```

Establece todos los trabajos registrados como no marcados para que se guarde su historico en la base de datos job_monitor.

### -------------------------- EXAMPLE 3 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob -Name 'Backup1' | Set-ImportJobHistory -Disable
```

Establece el trabajo 'Backup1' como no marcado para que se guarde su historico en la base de datos job_monitor.

### -------------------------- EXAMPLE 4 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob -JobId '161116E6-D65A-4228-96EF-4807697DDC32' | Set-ImportJobHistory -Disable
```

Establece el trabajo con identificador '161116E6-D65A-4228-96EF-4807697DDC32' como no marcado para que se guarde su historico en la 
base de datos job_monitor.

## PARAMETERS

### -InputObject
Objetos que se marcarán.

### -Enable
El job se marcara para que se guarde su historico en la base de datos job_monitor.

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
El job se desmarcara para que se guarde su historico en la base de datos job_monitor.

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
