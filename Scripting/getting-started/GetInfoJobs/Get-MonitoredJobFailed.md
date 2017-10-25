---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-MonitoredJobFailed

## SYNOPSIS
Obtiene el listado de todos los jobs fallidos y registrados en la base de datos de Monitoreo.

## SYNTAX

```powershell
Get-MonitoredJobFailed [-InputObject <Object>] [-JobId <Guid>] [-Name <String>] [-FailureType <String>]
 [-StartRunDate <DateTime>]
```

## DESCRIPTION
Obtiene el listado de todos los jobs fallidos y registrados en la base de datos de Monitoreo.
Se pueden filtra por tipo de fallo, fecha, nombre y JobId.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJobFailed
```

Obtiene la información de todos los jobs que están siendo monitoreados en todos los servidores.

## PARAMETERS

### -InputObject
Datos del servidor en donde se buscan los jobs.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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
Position: Named
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
Position: Named
Default value: *
Accept pipeline input: False
Accept wildcard characters: True
```

### -FailureType
Establece el tipo de fallo.
Posible valores Delayed, NonCritical, y Critical.
Valor predeterminado Todos ($null).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: [string]::Empty
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRunDate
Fecha en que la se inició el(los) trabajo(s) que terminaron con errores.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS
Puede canalizar el valor de InputObject desde la función Get-MonitoredServer.

## OUTPUTS
Processa.Management.Automation.PSJobMonitor.SqlFailedJobDetail

## NOTES
Autor: CFranco

## RELATED LINKS

[Get-MonitoredServer](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)
