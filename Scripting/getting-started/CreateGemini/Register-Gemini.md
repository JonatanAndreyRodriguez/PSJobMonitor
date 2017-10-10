---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Register-Gemini

## SYNOPSIS
Registra  ³ Actualiza un Gemini existente relacionado a un Job.

## SYNTAX

```
Register-Gemini [-InputObject] <Object>
```

## DESCRIPTION
Registra  ³ Actualiza un Gemini existente relacionado a un Job.
Adem ¡s, crea el Job si no existe y, hace env -o de Push
solamente para Geminis nuevos y de jobs cr -ticos.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MonitoredServer | Get-SqlJobExecutionFailed | Register-Gemini
```

## PARAMETERS

### -InputObject
Informaci ³n del job a reportar.

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

## INPUTS

## OUTPUTS

### System.Void

## NOTES
Autor: Carlos Franco

## RELATED LINKS

[[Get-MonitoredServer](Get-MonitoredServer.md)]()

[[Get-SqlJobExecutionFailed](Get-SqlJobExecutionFailed.md)]()

[[Register-Gemini](Register-Gemini.md)]()

