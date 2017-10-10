---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-JobIssueId

## SYNOPSIS
Obtiene el n ºmero de Gemini asociado a un Job en la base de datos.

## SYNTAX

```
Get-JobIssueId [[-JobID] <Guid>] [[-ConnectionString] <String>]
```

## DESCRIPTION
Obtiene el n ºmero de Gemini asociado a un Job en la base de datos. 
Si el Job no existe  ³, no tiene un Gemini  ³, si tiene asociado un Gemini y  ©ste tiene estado Cerrado, 
se devuelve 0, de lo contrario se devuelve el n ºmero de Gemini.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-JobIssueId
```

## PARAMETERS

### -JobID
Identificador univoco del job.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: [System.Guid]::Empty
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Cadena de conexi ³n a la base de datos de Monitor.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

### System.Boolean

## NOTES
Autor: Carlos Franco

## RELATED LINKS

