# ¿Qué hace cada una de las funciones?

Ejecute el comando:

```
Get-PSPCommand
```

También puede utilizar el comando [Get-Help](https://msdn.microsoft.com/en-us/powershell/reference/5.1/microsoft.powershell.core/get-help) de PowerShell para observar la ayuda de una función. La sintaxis es Get-Help seguido del nombre de la función. Supongamos que desea observar la ayuda del comando Add-MonitoredServer del módulo.

```
Get-Help Add-MonitoredServer
```

Get-Help inicialmente muestra un resumen de la ayuda. Si desea observar toda la ayuda, ejecute:

```
Get-Help Add-MonitoredServer -Full
```

Observar los ejemplos:

```
Get-Help Add-MonitoredServer -Examples
```

Observar la ayuda de un parámetro (en este caso ConnectionString):

```
Get-Help Add-MonitoredServer -Parameter ConnectionString
```

Observar la ayuda en una ventana de Windows (en lugar de en la consola)

```
Get-Help Add-MonitoredServer -ShowWindow
```

Observar la ayuda en línea (a través del Browser)

```
Get-Help Add-MonitoredServer -Online
```
