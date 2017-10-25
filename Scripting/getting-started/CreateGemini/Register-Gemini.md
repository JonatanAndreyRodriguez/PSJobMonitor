---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Register-Gemini

## SYNOPSIS
Registra o Actualiza un Gemini existente relacionado a un Job.

## SYNTAX

```powershell
Register-Gemini [-InputObject] <Object>
```

## DESCRIPTION
Registra o Actualiza un Gemini existente relacionado a un Job. Además, registra el 
Job en la base de Monitoreo si no existe y, hace envío de Push solamente para Geminis 
nuevos y de jobs críticos.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-SqlJobExecutionFailed | Register-Gemini
```

## PARAMETERS

### -InputObject
Información del job a reportar.

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
Puede canalizar el valor de InputObject.

## OUTPUTS
System.Void

## NOTES
Autor: Carlos Franco

## RELATED LINKS

[Get-MonitoredServer](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)

[Get-SqlJobExecutionFailed](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/GetInfoJobs/Get-SqlJobExecutionFailed.md)


