---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-MonitoredJobCritical

## SYNOPSIS
Obtiene la información de los jobs registrados como criticos que están siendo monitoreados.

## SYNTAX

```
Get-MonitoredJobCritical [-InputObject] <Object> [[-JobId] <Guid>] [[-Name] <String>]
```

## DESCRIPTION
Obtiene la información de los jobs registrados como criticos que están siendo monitoreados.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MonitoredServer | Get-MonitoredJobCritical
```

## PARAMETERS

### -InputObject
Datos del servidor en donde se buscan los jobs.

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

### -JobId
Identificador univoco del job.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: [System.Guid]::Empty
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nombre con el que se registró el job.
Se admiten expresiones con el caracter comodin (\*).
Por ejemplo: '\*Pru\*'.
Valor predeterminado \*.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: *
Accept pipeline input: False
Accept wildcard characters: True
```

## INPUTS

### Puede canalizar el valor de InputObject desde la función Get-MonitoredServer.

## OUTPUTS

### Processa.Management.Automation.PSJobMonitor.SqlJobDetail

## NOTES
Autor: Atorres

## RELATED LINKS

[[Get-MonitoredJobNonCritical](Get-MonitoredJobNonCritical.md)]()

