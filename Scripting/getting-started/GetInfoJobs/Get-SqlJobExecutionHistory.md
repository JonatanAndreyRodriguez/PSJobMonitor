---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-SqlJobExecutionHistory

## SYNOPSIS
Obtiene el historial de ejecuciones de los trabajos suministrados.

## SYNTAX

### ByFrame (Default)
```powershell
Get-SqlJobExecutionHistory -InputObject <Object> [-Since <String>] [-OutcomesType <String>]
```

### ByDate
```powershell
Get-SqlJobExecutionHistory -InputObject <Object> -StartRunDate <DateTime> [-OutcomesType <String>]
```

## DESCRIPTION
Obtiene el historial de ejecuciones de los trabajos suministrados en InputObject.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-SqlJobDetail | Get-SqlJobExecutionHistory
```

Obtiene el historial de ejecuciones de todos los trabajos en todos los servidores.

### -------------------------- EXAMPLE 2 --------------------------
```powershell
Get-MonitoredServer -Name 'Server' | Get-SqlJobDetail -Name 'Job' | Get-SqlJobExecutionHistory
```

Obtiene el historial de ejecuciones del trabajo con nombre 'Job' en el servidor con nombre 'Server'.

## PARAMETERS

### -InputObject
Trabajos para los que se obtiene el historial.

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

### -Since
Especifica una abreviatura que puede utilizar en lugar del parámetro StartRunDate.
Valor predeterminado: Yesterday

Valores admitidos:

| Abreviatura | Descripción |
|:-----:|-------------|
| Midnight | Historial de los trabajos que se han iniciado desde la media noche |
| Yesterday | Historial de los trabajos que se han iniciado desde ayer a la media noche |
| ThisWeek | Historial de los trabajos que se han iniciado desde el lunes inmediatamente anterior |
| LastWeek | Historial de los trabajos que se han iniciado en los últimos siete días |
| ThisMonth | Historial de los trabajos que se han iniciado desde el día 1 del mes actual |
| LastMonth | Historial de los trabajos que se han iniciado en los últimos 30 días |
| Beginning | Historial de los trabajos desde el primer día de ejecución |

```yaml
Type: String
Parameter Sets: ByFrame
Aliases: 

Required: False
Position: Named
Default value: Yesterday
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRunDate
Restringe los valores devueltos a la fecha en que se inició el trabajo.

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

### -OutcomesType
Especifica que solo se retornen el historial de los trabajaos que tienen el resultado especificado al finalizar.
Valor predeterminado All.

Valores admitidos:

| Resultado | Descripción |
|:-----:|-------------|
| Cancelled | Se canceló el trabajo |
| Failed | El trabajo se ha completado con un fallo |
| InProgress | El trabajo todavía está en curso |
| Retry | El trabajo está a la espera de ser lanzado nuevamente |
| Succeeded | El trabajo se ha completado correctamente |
| Unknown | Se desconoce el estado del trabajo |
| All | Incluir todos los resultados |

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: All
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS
Puede canalizar el valor de InputObject desde la función Get-SqlJobDetail.

## OUTPUTS
Processa.Automation.PSJobMonitor.SqlJobHistory

## NOTES
Autor: Atorres

## RELATED LINKS
[Get-SqlJobDetail](Get-SqlJobDetail)
