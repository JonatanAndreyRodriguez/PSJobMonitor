---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Import-MonitoredJob

## SYNOPSIS
Importa la información de jobs en una base de datos a la base de datos local de Monitoreo.

## SYNTAX

```powershell
Import-MonitoredJob [-InputObject] <Object> [-Force] [-WhatIf] [-Confirm]
```

## DESCRIPTION
Importa la información de jobs en una base de datos a la base de datos local de Monitoreo.
Por defecto los jobs se importan habilitados y marcados como no críticos.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
Get-MonitoredServer | Get-SqlJobDetail | Import-MonitoredJob
```

## PARAMETERS

### -InputObject
Inofrmación del job a importar.

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

### -Force
Cuando está presente, sobrescribe los datos del job (si existiera).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS
Puede canalizar el valor de InputObject desde la función Get-SqlJobDetail.

## OUTPUTS
Processa.Management.Automation.PSJobMonitor.ConflicingtJob

## NOTES
Autor: CFranco
Modificaciones: 2017-07-26 Atorres. Se mejora documentación. Se corrige manejo del Pipeline.

## RELATED LINKS

[Get-MonitoredServer](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/ConfigServers/Get-MonitoredServer.md)

[Get-SqlJobDetail](https://github.com/RD-Processa/PSJobMonitor/blob/master/Scripting/getting-started/GetInfoJobs/Get-SqlJobDetail.md)
