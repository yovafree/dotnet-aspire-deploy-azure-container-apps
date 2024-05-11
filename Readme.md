# Despliegue de una aplicación .NET Aspire en Azure Container Apps

## DEMOS

## **Conocimientos previos**  
* C#
* Desarrollo de APIs Rest
* Conocimientos básicos de Docker

## **Demos**  
* [01 - Aspire Starter](demo1)

## Instrucciones para .NET Aspire
### Instalar .NET Aspire

```
dotnet workload update
dotnet workload install aspire
```

### Crear un proyecto de inicio de .NET Aspire
```
dotnet new aspire-starter --use-redis-cache --output demo1
```

### Ejecutar el proyecto de .NET Aspire
```
dotnet run --project demo1/demo1.AppHost
```

## Instrucciones para Desplegar la aplicación de .NET Aspire en Azure Container Apps

### Instalar Azure Developer CLI (AZD) en Windows

```
winget install microsoft.azd
```

### Inicializar el proyecto:

```
cd demo1/demo1.AppHost
azd init
```
### Desplegar el proyecto en Azure:
```
azd up
```

### Si realiza cambios y desea subirlos, puede utilizar:
```
azd deploy
```

### Habilitar Dashboard de .NET Aspire para desplegarlo en Azure:
```
azd config set alpha.aspire.dashboard on
```

### Habilitar Dashboard de .NET Aspire para desplegarlo en Local:
```
azd monitor

```
### Eliminar recursos de Azure
```
az group delete --name rg-demo1
```



