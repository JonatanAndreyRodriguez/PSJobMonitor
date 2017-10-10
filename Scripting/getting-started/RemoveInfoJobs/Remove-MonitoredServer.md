---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Remove-MonitoredServer

## SYNOPSIS
Elimina un servidor de monitoreo de SQLServer de la configuración.

## SYNTAX

```
Remove-MonitoredServer [-Name] <String[]>
```

## DESCRIPTION
Elimina un servidor de la configuracion de los servidores de SQLServer que se van a monitorear.
\> NOTA: Se necesitan permisos de Administrador para completar la función.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Remove-MonitoredServer -Name 'MyName'
```

Elimina de la configuracion el servidor identificado con el nombre MyName.

### -------------------------- EXAMPLE 2 --------------------------
```
Get-MonitoredServer | Remove-MonitoredServer
```

Elimina de la configuracion todos los servidores registrados.

## PARAMETERS

### -Name
Nombre con el que se identifica la coenxión en el archivo de configuración PSJobMonitor.config.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

### System.Void

## NOTES

## RELATED LINKS

[[Add-MonitoredServer](Add-MonitoredServer.md)]()

[[Set-MonitoredServer](Set-MonitoredServer.md)]()

