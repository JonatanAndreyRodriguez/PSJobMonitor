# ¿Cómo instalar?

### Prerrequisitos

Se debe tener instalada la última versión de cada uno de los siguientes módulos:

1. PSGemini. Para mayor información, revisar el siguiente enlace: https://github.com/RD-Processa/PSGemini
2. PSProcessa. Para mayor información, revisar el siguiente enlace: https://github.com/RD-Processa/PSProcessa


### Versión Online

1. Abra una ventana de PowerShell como usuario administrador y registre el repositorio de Nuget de Gerencia Técnica (ó, el que aplique).

```powershell
Register-PSRepository -Name 'Processa GT' -SourceLocation 'http://proget:8020/nuget/PowerShell' -InstallationPolicy Trusted
```


2. Instale el módulo desde el Repositorio

```powershell
Install-Module -Name 'PSJobMonitor' -Repository 'Processa GT'
```

# ¿Cómo actualizar?

Si el módulo ya está instalado solo tiene que actualizarlo. 

1. Asegurese de tener registrado el repositorio de Nuget de Gerencia Técnica (ó, el que aplique).

```powershell
Get-PSRepository -Name 'Processa GT'
```

2. Actualice el módulo desde el Repositorio

```powershell
Update-Module -Name 'PSJobMonitor' -Force
```
