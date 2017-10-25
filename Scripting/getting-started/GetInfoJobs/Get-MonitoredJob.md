---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-MonitoredJob

## SYNOPSIS
Obtiene el listado de los jobs que se han registrado para monitoreo.

## SYNTAX

```powershell
Get-MonitoredJob [-InputObject] <Object> [[-JobId] <Guid>] [[-Name] <String>] [[-Level] <String>]
```

## DESCRIPTION
Obtiene el listado de los jobs que se han registrado para monitoreo.
Los jobs se registran a través de la función Import-MonitoredJob.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob
```

Obtiene la información de todos los jobs que están siendo monitoreados en todos los servidores.

### -------------------------- EXAMPLE 2 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob  -Level Critical
```

Obtiene la información de todos los jobs que están siendo monitoreados en todos los servidores, marcados como críticos.

### -------------------------- EXAMPLE 3 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob  -Level NonCritical
```

Obtiene la información de todos los jobs que están siendo monitoreados en todos los servidores, marcados como no críticos.

### -------------------------- EXAMPLE 4 --------------------------
```powershell
Get-MonitoredServer | Get-MonitoredJob -Name 'Pru*'
```

Obtiene la información de todos los jobs que están siendo monitoreados en todos los servidores, y cuyo nombre comienza por Pru.

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

## INPUTS
Puede canalizar el valor de InputObject desde la función Get-MonitoredServer.

## OUTPUTS
Processa.Management.Automation.PSJobMonitor.SqlJobDetail

## NOTES
Autor: Atorres.

## RELATED LINKS

[Get-MonitoredServer](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)

