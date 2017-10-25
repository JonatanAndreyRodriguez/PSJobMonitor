---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-SqlJobDetail

## SYNOPSIS
Obtiene un objeto de trabajo del Agente de SQL Server para cada tarea/job que está presente en la instancia de destino del Agente de SQL.

## SYNTAX

```powershell
Get-SqlJobDetail [-InputObject] <Object> [[-Name] <String>]
```

## DESCRIPTION
Obtiene un objeto de trabajo del Agente de SQL Server para cada tarea/job que está presente en la instancia de destino del Agente de SQL.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-SqlJobDetail
```

Obtiene la información de todos los jobs/tareas en todos los servidores registrados.

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

### -Name
Nombre del Job que se desea obtener.
Se admiten expresiones con el caracter comodin (\*).
Por ejemplo: '\*Pru\*'.
Valor predeterminado \*.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: *
Accept pipeline input: False
Accept wildcard characters: True
```

## INPUTS
Puede canalizar el valor de ConnectionString desde la función Get-MonitoredServer.

## OUTPUTS
Processa.Management.Automation.PSJobMonitor.SqlJobDetail

## NOTES
Autor: Atorres

## RELATED LINKS

[Get-MonitoredServer](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)

