---
external help file: PSJobMonitor-help.xml
Module Name: PSJobMonitor
online version: 
schema: 2.0.0
---

# Get-JobIssueId

## SYNOPSIS
Obtiene el número de Gemini asociado a un Job en la base de datos.

## SYNTAX

```powershell
Get-JobIssueId [[-JobID] <Guid>] [[-ConnectionString] <String>]
```

## DESCRIPTION
Obtiene el número de Gemini asociado a un Job en la base de datos. 
Este devuelve cero en los siguientes casos: 
- Si el Job no existe.
- Si el Job no tiene un Gemini asociado.
- Si el Job tiene asociado un Gemini pero, este está en estado Cerrado.
> De lo contrario se devuelve el número de Gemini.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```powershell
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
Cadena de conexión a la base de datos de Monitor.

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

System.Boolean

## NOTES
Autor: Carlos Franco

## RELATED LINKS

