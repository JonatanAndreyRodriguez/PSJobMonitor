---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-UnmonitoredJob

## SYNOPSIS
Obtiene el listado de los jobs que no se están monitoreando.

## SYNTAX

```powershell
Get-UnmonitoredJob [-InputObject] <Object> [[-JobId] <Guid>] [[-Name] <String>] [[-Level] <String>]
```

## DESCRIPTION
Obtiene el listado de los jobs que no se están monitoreando.
Los jobs se registran a través de la función Import-MonitoredJob.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-UnmonitoredJob
```

Obtiene la información de todos los jobs que se no se están monitoreando en todos los servidores.

### -------------------------- EXAMPLE 2 --------------------------
```powershell
Get-MonitoredServer | Get-UnMonitoredJob  -Level Critical
```

Obtiene la información de todos los jobs que se no se están monitoreando en todos los servidores, marcados como críticos.

### -------------------------- EXAMPLE 3 --------------------------
```powershell
Get-MonitoredServer | Get-UnmonitoredJob  -Level NonCritical
```

Obtiene la información de todos los jobs que se no se están monitoreando en todos los servidores, marcados como no críticos.

### -------------------------- EXAMPLE 4 --------------------------
```powershell
Get-MonitoredServer | Get-UnmonitoredJob -Name 'Pru*'
```

Obtiene la información de todos los jobs que se no se están monitoreando en todos los servidores, y cuyo nombre comienza por Pru.

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
Processa.Management.Automation.PSJobMonitor.MonitoredJob

## NOTES
Autor: Atorres

## RELATED LINKS

[Get-MonitorServer](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)

[Get-MonitoredJob](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ImportInfoJobs/Import-MonitoredJob.md)

