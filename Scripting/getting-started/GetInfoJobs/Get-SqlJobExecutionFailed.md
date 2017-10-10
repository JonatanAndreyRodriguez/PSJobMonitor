---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-SqlJobExecutionFailed

## SYNOPSIS
Obtiene la información de los jobs cuya ejecución ha finalizado con errores.

## SYNTAX

### ByFrame (Default)
```
Get-SqlJobExecutionFailed -InputObject <Object> [-Name <String>] [-Level <String>] [-Since <String>]
```

### ByDate
```
Get-SqlJobExecutionFailed -InputObject <Object> [-Name <String>] [-Level <String>] -StartRunDate <DateTime>
```

## DESCRIPTION
Obtiene la información de los jobs que terminaron con errrores de ejecución.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MonitoredServer | Get-SqlJobExecutionFailed
```

Obtiene la información de todos los jobs que han terminado con errores en todos los servidores registrados.

## PARAMETERS

### -InputObject
Datos del servidor en donde se buscan los jobs.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Nombre del job.
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

### -Level
Nivel de criticidad de los jobs que terminaron con errores (Critical, NonCritical, Both).
Valor predeterminado Both.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Both
Accept pipeline input: False
Accept wildcard characters: False
```

### -Since
Especifica una abreviatura que puede utilizar en lugar del parámetro StartRunDate.
Valor predeterminado: Midnight

Valores admitidos:

| Abreviatura | Descripción |
|:-----:|-------------|
| Midnight | Trabajos que se han iniciado desde la media noche |
| Yesterday | Trabajos que se han iniciado desde ayer a la media noche |
| ThisWeek | Trabajos que se han iniciado desde el lunes inmediatamente anterior |
| LastWeek | Trabajos que se han iniciado en los últimos siete días |
| ThisMonth | Trabajos que se han iniciado desde el día 1 del mes actual |
| LastMonth | Trabajos que se han iniciado en los últimos 30 días |

```yaml
Type: String
Parameter Sets: ByFrame
Aliases: 

Required: False
Position: Named
Default value: Midnight
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRunDate
Fecha en que la se inició el(los) trabajo(s) que terminaron con errores.

```yaml
Type: DateTime
Parameter Sets: ByDate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### Puede canalizar el valor de InputObject desde la función Get-MonitoredServer.

## OUTPUTS

### Processa.Management.Automation.PSJobMonitor.SqlJobOutcome

## NOTES

## RELATED LINKS

[[Get-MonitoredServer](Get-MonitoredServer.md)]()

