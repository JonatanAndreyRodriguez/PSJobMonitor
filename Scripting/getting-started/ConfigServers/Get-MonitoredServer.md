---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-MonitoredServer

## SYNOPSIS
Obtiene la configuracion de los servidores de SQLServer que se van a monitorear.

## SYNTAX

```
Get-MonitoredServer [[-Name] <String>]
```

## DESCRIPTION
Obtiene la configuracion de los servidores de SQLServer que se van a monitorear a partir de la información en el archivo PSJobMonitor.config

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MonitoredServer
```

Obtiene la información de todos los servidores que se están monitoreando.

### -------------------------- EXAMPLE 2 --------------------------
```
Get-MonitoredServer -Name '*MyServer*'
```

Obtiene la información del servidor con nombre MyServer que se está monitoreando.

## PARAMETERS

### -Name
Nombre del servidor.
Se admiten expresiones con el caracter comodin (\*).
Por ejemplo: '\*Pru\*'.
Valor predeterminado \*.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: *
Accept pipeline input: False
Accept wildcard characters: True
```

## INPUTS

### Ninguno

## OUTPUTS

### Processa.Management.Automation.PSJobMonitor.MonitoredServer

## NOTES

## RELATED LINKS

[[Set-MonitoredServer](Set-MonitoredServer.md)]()

[[Remove-MonitoredServer](Remove-MonitoredServer.md)]()

