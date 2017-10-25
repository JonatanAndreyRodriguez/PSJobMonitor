---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-MonitoredJobHistory

## SYNOPSIS
Obtiene el historial de los Jobs de la base de datos de Monitoreo.

## SYNTAX

```powershell
Get-MonitoredJobHistory [-InputObject] <Object> [[-JobId] <Guid>] [[-Name] <String>] [[-Level] <String>]
 [[-Monitored] <String>]
```

## DESCRIPTION
Obtiene el historial de los Jobs de la base de datos de Monitoreo. El historial se registra a través de la 
función Import-MonitoredJobHistory.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJobHistory
```

Obtiene la informaci ³n de todos los historicos de todos los Jobs que est ¡n siendo monitoreados en todos los servidores.

### -------------------------- EXAMPLE 2 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJobHistory  -Level Critical
```

Obtiene la información de todos los historicos de todos los Jobs que están siendo monitoreados en todos los servidores.

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
Identificador único del Job.

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
Por ejemplo: '\*Pru\*'. Valor predeterminado \*.

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

### -Level
Establece el nivel de criticidad de los jobs a consultar.
Posible valores Critical, NonCritical y Both.
Valor predeterminado Both.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: Both
Accept pipeline input: False
Accept wildcard characters: False
```

### -Monitored
Establece si se desea traer los Jobs que están siendo monitoreados o no. 
Posible valores Monitored, Unmonitored y Both. Valor predeterminado Both.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: Both
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS
Puede canalizar el valor de InputObject desde la función Get-MonitoredServer.

## OUTPUTS
Processa.Management.Automation.PSJobMonitor.SqlJobHistoryDetail

## NOTES
Autor: Cfranco

## RELATED LINKS

[Get-MonitoredServer](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)

