# Create a Microservice with Powershell

- Save the following as a Powershell script

```powershell
param ($namespace)

$frameworkVersion = "netcoreapp2.2"
$originalPath = $PSScriptRoot

dotnet new sln -o $namespace

cd $namespace

dotnet new webapi -o $namespace'.WebApi'

dotnet new classlib -o $namespace'.Infrastructure' --framework $frameworkVersion

dotnet new classlib -o $namespace'.Domain' --framework $frameworkVersion

dotnet new mstest -o $namespace'.Tests'

dotnet sln $namespace'.sln' add `
    .\$namespace'.WebApi\'$namespace'.WebApi.csproj' `
    .\$namespace'.Infrastructure\'$namespace'.Infrastructure.csproj' `
    .\$namespace'.Domain\'$namespace'.Domain.csproj' `
    .\$namespace'.Tests\'$namespace'.Tests.csproj'

dotnet add $(".\" + $namespace + ".Infrastructure\" + $namespace + '.Infrastructure.csproj') reference $(".\" + $namespace + ".Domain\" + $namespace + ".Domain.csproj")

dotnet add $(".\" + $namespace + ".WebApi\" + $namespace + '.WebApi.csproj') reference $(".\" + $namespace + ".Domain\" + $namespace + ".Domain.csproj")
dotnet add $(".\" + $namespace + ".WebApi\" + $namespace + '.WebApi.csproj') reference $(".\" + $namespace + ".Infrastructure\" + $namespace + ".Infrastructure.csproj")

dotnet add $(".\" + $namespace + ".Tests\" + $namespace + '.Tests.csproj') reference $(".\" + $namespace + ".Domain\" + $namespace + ".Domain.csproj")
dotnet add $(".\" + $namespace + ".Tests\" + $namespace + '.Tests.csproj') reference $(".\" + $namespace + ".Infrastructure\" + $namespace + ".Infrastructure.csproj")

cd $originalPath
```

- Execute the script in a command prompt and supply a namespace:

    `./create-service.ps1 -namespace pubapi.services`
