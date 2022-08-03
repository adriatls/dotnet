# dotnet

<p align=center>🚀 Projeto DDD desenvolvido em C# e .NET 6 para fins de estudo da linguagem e framework 🚀</p>

## 👷‍♀️ Passos para a construção do projeto

No terminal, usar os seguintes comandos:

**1 -** Para criar a API Web do ASP.NET Core:
~~~
dotnet new webapi -o NomeDaAPI
~~~

**2 -** Para criar o projeto de cada camada:
~~~
dotnet new classlib -o NomeDaCamada
~~~

As camadas, de acordo com o que está recomendado na Meta S.M.A.R.T, seguindo uma arquitetura com DDD:
  * Application
  * AutoMapper
  * Domain
  * Infra.Data
  * Infra.Data.Dapper
  * Infrastructure.IoC
  * Utility
  
**3 -** Para criar o arquivo de solução:
~~~
dotnet new sln --name NomeDaSolucao
~~~

**4 -** Para adicionar cada camada (projeto) na solução:
~~~
dotnet sln NomeDaSolucao.sln add ./NomeDaCamada/NomeDaCamada.csproj
~~~

Obs: Para remover um projeto do arquivo de solução:
~~~
dotnet sln NomeDaSolucao.sln remove ./NomeDaCamada/NomeDaCamada.csproj
~~~

Obs:  Para adicionar vários projetos no arquivo de solução recursivamente:
~~~
dotnet sln NomeDaSolucao.sln add (ls -r **/*.csproj)
~~~

