---
title: Estrutura do diretório do ASP.NET Core
author: guardrex
description: Saiba mais sobre a estrutura do diretório de aplicativos publicados do ASP.NET Core.
monikerRange: '>= aspnetcore-2.2'
ms.author: riande
ms.custom: mvc
ms.date: 12/11/2018
uid: host-and-deploy/directory-structure
ms.openlocfilehash: ee0bebb8b5c688f8471d6420d1641b87ac271f6c
ms.sourcegitcommit: b34b25da2ab68e6495b2460ff570468f16a9bf0d
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2018
ms.locfileid: "53284559"
---
# <a name="aspnet-core-directory-structure"></a>Estrutura do diretório do ASP.NET Core

Por [Luke Latham](https://github.com/guardrex)

O diretório *publish* contém os ativos implantáveis do aplicativo produzidos pelo comando [dotnet publish](/dotnet/core/tools/dotnet-publish). O diretório contém:

* Arquivos de aplicativo
* Arquivos de configuração
* Ativos estáticos
* Pacotes
* Um tempo de execução ([somente implantação autocontida](/dotnet/core/deploying/#self-contained-deployments-scd))

| Tipo de aplicativo | Estrutura de diretórios |
| -------- | ------------------- |
| [Implantação dependente de estrutura](/dotnet/core/deploying/#framework-dependent-deployments-fdd) | <ul><li>publish&dagger;<ul><li>Logs&dagger; (opcional, a menos que necessário para receber logs de stdout)</li><li>Exibições&dagger; (aplicativos MVC; se as exibições não são pré-compiladas)</li><li>Páginas&dagger; (aplicativos de Páginas do Razor ou MVC, se as páginas não são pré-compiladas)</li><li>wwwroot&dagger;</li><li>arquivos *\.dll</li><li>{NOME DO ASSEMBLY}.deps.json</li><li>{NOME DO ASSEMBLY}.dll</li><li>{NOME DO ASSEMBLY}.pdb</li><li>{NOME DO ASSEMBLY}.Views.dll</li><li>{NOME DO ASSEMBLY}.Views.pdb</li><li>{NOME DO ASSEMBLY}.runtimeconfig.json</li><li>web.config (implantações do IIS)</li></ul></li></ul> |
| [Implantação autossuficiente](/dotnet/core/deploying/#self-contained-deployments-scd) | <ul><li>publish&dagger;<ul><li>Logs&dagger; (opcional, a menos que necessário para receber logs de stdout)</li><li>Exibições&dagger; (aplicativos MVC; se as exibições não são pré-compiladas)</li><li>Páginas&dagger; (aplicativos de Páginas do Razor ou MVC, se as páginas não são pré-compiladas)</li><li>wwwroot&dagger;</li><li>arquivos \*.dll</li><li>{NOME DO ASSEMBLY}.deps.json</li><li>{NOME DO ASSEMBLY}.dll</li><li>{NOME DO ASSEMBLY}.exe</li><li>{NOME DO ASSEMBLY}.pdb</li><li>{NOME DO ASSEMBLY}.Views.dll</li><li>{NOME DO ASSEMBLY}.Views.pdb</li><li>{NOME DO ASSEMBLY}.runtimeconfig.json</li><li>web.config (implantações do IIS)</li></ul></li></ul> |

&dagger;Indica um diretório

O diretório *publish* representa o *caminho raiz de conteúdo* (também chamado de *caminho base do aplicativo*) da implantação. Qualquer que seja o nome fornecido para o diretório *publish* do aplicativo implantado no servidor, o local dele serve como o caminho físico do servidor para o aplicativo hospedado.

O diretório *wwwroot*, se presente, contém somente ativos estáticos.

O diretório *Logs* de stdout pode ser criado para a implantação usando uma das duas abordagens a seguir:

* Adicione o seguinte elemento `<Target>` ao arquivo de projeto:

   ```xml
   <Target Name="CreateLogsFolder" AfterTargets="Publish">
     <MakeDir Directories="$(PublishDir)Logs" 
              Condition="!Exists('$(PublishDir)Logs')" />
     <WriteLinesToFile File="$(PublishDir)Logs\.log" 
                       Lines="Generated file" 
                       Overwrite="True" 
                       Condition="!Exists('$(PublishDir)Logs\.log')" />
   </Target>
   ```

   O elemento `<MakeDir>` cria uma pasta *Logs* vazia na saída publicada. O elemento usa a propriedade `PublishDir` para determinar o local de destino no qual criar a pasta. Vários métodos de implantação, como a Implantação da Web, ignoram pastas vazias durante a implantação. O elemento `<WriteLinesToFile>` gera um arquivo na pasta *Logs*, o que garante a implantação da pasta no servidor. A criação de pasta usando essa abordagem poderá falhar se o processo de trabalho não tiver acesso de gravação para a pasta de destino.

* Crie fisicamente o diretório *Logs* no servidor na implantação.

O diretório de implantação requer permissões de leitura/execução. O diretório *Logs* requer permissões de leitura/gravação. Diretórios adicionais em que os arquivos são gravados exigem permissões de leitura/gravação.

## <a name="additional-resources"></a>Recursos adicionais

* [dotnet publish](/dotnet/core/tools/dotnet-publish)
* [Implantação de aplicativos do .NET Core](/dotnet/core/deploying/)
* [Estruturas de destino](/dotnet/standard/frameworks)
* [Catálogo de RIDs do .NET Core](/dotnet/core/rid-catalog)
