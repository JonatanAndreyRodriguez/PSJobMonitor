---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-SqlJobExecutionOutcome

## SYNOPSIS
Obtiene la información del resultado de la ejecución de los jobs.

## SYNTAX

### ByFrame (Default)
```powershell
Get-SqlJobExecutionOutcome -InputObject <Object> [-Name <String>] [-OutcomesType <String>] [-Since <String>]
```

### ByDate
```powershell
Get-SqlJobExecutionOutcome -InputObject <Object> [-Name <String>] [-OutcomesType <String>]
 -StartRunDate <DateTime>
```

## DESCRIPTION
Obtiene la información del resultado de la ejecución de uno o más jobs de acuerdo a los valores de parámetros suministrados.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-SqlJobExecutionOutcome
```

Obtiene la información del resultado de todos los jobs en todos los servidores registrados.

### -------------------------- EXAMPLE 2 --------------------------
```powershell
Get-MonitoredServer -Name 'MyServer' | Get-SqlJobExecutionOutcome -Name 'MyJob'
```

Obtiene la información del resultado de la ejecución del job nombre MyJob en el servidor MyServer o null si el job no se encuentra.

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

### -OutcomesType
Especifica que solo se retornen los jobs que tienen el resultado especificado al finalizar.
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
Fecha en que la se inició el(los) trabajo(s).

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
Puede canalizar el valor de InputObject desde la función Get-MonitoredServer.

## OUTPUTS
Processa.Management.Automation.PSJobMonitor.SqlJobOutcome

## NOTES
Autor: Atorres

## RELATED LINKS

[Get-MonitoredServer](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)

