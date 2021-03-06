---
ms.openlocfilehash: a3ac1ac389892681e8c122d569e6325353ed6e88
ms.sourcegitcommit: 42a8164b8aba21f322ffefacb92301bdfb4d3c2d
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54341674"
---
# [Documentação do ASP.NET Core](/aspnet/#pivot=core)

# Visão geral
## [Sobre o ASP.NET Core](xref:index)
## [Comparar o ASP.NET Core e o ASP.NET](xref:fundamentals/choose-between-aspnet-and-aspnetcore)
## [Comparar o .NET Core e o .NET Framework](/dotnet/articles/standard/choosing-core-framework-server)

# [Introdução](xref:getting-started)

# O que há de novo
## [Novidades no 2.2](xref:aspnetcore-2.2)
## [Novidades no 2.1](xref:aspnetcore-2.1)
## [Novidades no 2.0](xref:aspnetcore-2.0)
## [Novidades no 1.1](xref:aspnetcore-1.1)

# Tutoriais
## Aplicativos API Web
### [Criar uma API Web](xref:tutorials/first-web-api)
### [API Web com o MongoDB](xref:tutorials/first-mongo-app)
## Aplicativos Web
### [Páginas do Razor](xref:tutorials/razor-pages/index)
### [MVC](xref:tutorials/first-mvc-app/index)

## Aplicativos Web em tempo real
### [SignalR com JavaScript](xref:tutorials/signalr)
### [SignalR com TypeScript](xref:tutorials/signalr-typescript-webpack)
## [Criar serviços de back-end para aplicativos móveis nativos](xref:mobile/native-mobile-backend)

## Acesso aos dados
### [EF Core com Razor Pages](xref:data/ef-rp/index)
### [EF Core com MVC, BD existente](/ef/core/get-started/aspnetcore/existing-db)
### [EF Core com MVC, BD novo](/ef/core/get-started/aspnetcore/new-db)
### [EF Core com MVC, tutorial longo](xref:data/ef-mvc/index)

# Princípios básicos
## [Visão geral](xref:fundamentals/index)
## [Inicialização do aplicativo](xref:fundamentals/startup)
## [Injeção de dependência (serviços)](xref:fundamentals/dependency-injection)
## [Roteamento](xref:fundamentals/routing)
## [Ambientes (desenvolvimento, preparação, produção)](xref:fundamentals/environments)
## [Configuração](xref:fundamentals/configuration/index)
## [Opções](xref:fundamentals/configuration/options)
## [Registro em log](xref:fundamentals/logging/index)
## [Tratar erros](xref:fundamentals/error-handling)
## Middleware
### [Visão geral](xref:fundamentals/middleware/index)
### [Middleware de fábrica](xref:fundamentals/middleware/extensibility)
### [Middleware baseado em fábrica com contêiner de terceiros](xref:fundamentals/middleware/extensibility-third-party-container)
## Host
### [Visão geral](xref:fundamentals/host/index)
### [Host da Web](xref:fundamentals/host/web-host)
### [Host Genérico](xref:fundamentals/host/generic-host)
## [Servidores](xref:fundamentals/servers/index)
## [Iniciar solicitações HTTP](xref:fundamentals/http-requests)

# Aplicativos Web
## Páginas do Razor
### [Visão geral](xref:razor-pages/index)
### [Tutorial do Razor Pages](xref:tutorials/razor-pages/index)
#### [Introdução](xref:tutorials/razor-pages/razor-pages-start)
#### [Adicionar um modelo](xref:tutorials/razor-pages/model)
#### [Scaffolding](xref:tutorials/razor-pages/page)
#### [Trabalhar com um BD](xref:tutorials/razor-pages/sql)
#### [Atualizar as páginas](xref:tutorials/razor-pages/da1)
#### [Adicionar pesquisa](xref:tutorials/razor-pages/search)
#### [Adicionar um novo campo](xref:tutorials/razor-pages/new-field)
#### [Adicionar validação](xref:tutorials/razor-pages/validation)

## MVC
### [Visão geral do MVC](xref:mvc/overview)
### [Tutorial do MVC](xref:tutorials/first-mvc-app/index)
#### [Introdução](xref:tutorials/first-mvc-app/start-mvc)
#### [Adicionar um controlador](xref:tutorials/first-mvc-app/adding-controller)
#### [Adicionar uma exibição](xref:tutorials/first-mvc-app/adding-view)
#### [Adicionar um modelo](xref:tutorials/first-mvc-app/adding-model)
#### [Trabalhar com um BD](xref:tutorials/first-mvc-app/working-with-sql)
#### [Exibições e ações do controlador](xref:tutorials/first-mvc-app/controller-methods-views)
#### [Adicionar pesquisa](xref:tutorials/first-mvc-app/search)
#### [Adicionar um novo campo](xref:tutorials/first-mvc-app/new-field)
#### [Adicionar validação](xref:tutorials/first-mvc-app/validation)
#### [Examinar os métodos Details e Delete](xref:tutorials/first-mvc-app/details)

### [Filtros](xref:razor-pages/filter)
### [Bibliotecas de classes Razor](xref:razor-pages/ui-class)
### [Convenções de aplicativo e roteamento](xref:razor-pages/razor-pages-conventions)
### [Carregar arquivos](xref:razor-pages/upload-files)
### [SDK do Razor](xref:razor-pages/sdk)

### [Exibições](xref:mvc/views/overview)
### [Exibições parciais](xref:mvc/views/partial)
### [Controladores](xref:mvc/controllers/actions)
### [Roteamento](xref:mvc/controllers/routing)
### [Uploads de arquivo](xref:mvc/models/file-uploads)
### [Injeção de dependência – controladores](xref:mvc/controllers/dependency-injection)
### [Injeção de dependência – exibições](xref:mvc/views/dependency-injection)
### [Teste de unidade](xref:mvc/controllers/testing)
## [Estado de sessão e de aplicativo](xref:fundamentals/app-state)
## Auxiliares de Marca
### [Visão geral](xref:mvc/views/tag-helpers/intro)
### [Criar auxiliares de marcação](xref:mvc/views/tag-helpers/authoring)
### [Usar auxiliares de marcação em formulários](xref:mvc/views/working-with-forms)
### [Componentes do Auxiliar de Marca](xref:mvc/views/tag-helpers/th-components)
### Auxiliares de marcação internos
#### [Âncora](xref:mvc/views/tag-helpers/builtin-th/anchor-tag-helper)
#### [Cache](xref:mvc/views/tag-helpers/builtin-th/cache-tag-helper)
#### [Cache distribuído](xref:mvc/views/tag-helpers/builtin-th/distributed-cache-tag-helper)
#### [Ambiente](xref:mvc/views/tag-helpers/builtin-th/environment-tag-helper)
#### [Formulário](mvc/views/working-with-forms.md#the-form-tag-helper)
#### [Image](xref:mvc/views/tag-helpers/builtin-th/image-tag-helper)
#### [Entrada](mvc/views/working-with-forms.md#the-input-tag-helper)
#### [Rótulo](mvc/views/working-with-forms.md#the-label-tag-helper)
#### [Parcial](xref:mvc/views/tag-helpers/builtin-th/partial-tag-helper)
#### [Selecionar](mvc/views/working-with-forms.md#the-select-tag-helper)
#### [Área de texto](mvc/views/working-with-forms.md#the-textarea-tag-helper)
#### [Mensagem de validação](mvc/views/working-with-forms.md#the-validation-message-tag-helper)
#### [Resumo de validação](mvc/views/working-with-forms.md#the-validation-summary-tag-helper)
## [Layout](xref:mvc/views/layout)
## [Arquivos estáticos](xref:fundamentals/static-files)
## [Model binding](xref:mvc/models/model-binding)
## [Validação de modelo](xref:mvc/models/validation)
## [Sintaxe Razor](xref:mvc/views/razor)
## Avançado
### [Exibir componentes](xref:mvc/views/view-components)
### [Exibir compilação](xref:mvc/views/view-compilation)
### [Modelo de aplicativo](xref:mvc/controllers/application-model)
### [Filtros](xref:mvc/controllers/filters)
### [Áreas](xref:mvc/controllers/areas)
### [Partes do aplicativo](xref:mvc/extensibility/app-parts)
### [Model binding personalizado](xref:mvc/advanced/custom-model-binding)
### [Compatibilidade de versões](xref:mvc/compatibility-version)

# Aplicativos API Web
## [Visão geral](xref:web-api/index)

## Tutoriais
### [Criar uma API Web](xref:tutorials/first-web-api)
### [API Web com o MongoDB](xref:tutorials/first-mongo-app)

## Swagger/OpenAPI
### [Visão geral](xref:tutorials/web-api-help-pages-using-swagger)
### [Introdução ao Swashbuckle](xref:tutorials/get-started-with-swashbuckle)
### [Introdução ao NSwag](xref:tutorials/get-started-with-nswag)
## [Tipos de retorno de ação](xref:web-api/action-return-types)
## [Formatar dados de resposta](xref:web-api/advanced/formatting)
## [Formatadores personalizados](xref:web-api/advanced/custom-formatters)

## [Analisadores](xref:web-api/advanced/analyzers)
## [Convenções](xref:web-api/advanced/conventions)

# Aplicativos em tempo real
## [Visão geral do SignalR](xref:signalr/introduction)
## [Plataformas compatíveis](xref:signalr/supported-platforms)
## Tutoriais
### [SignalR com JavaScript](xref:tutorials/signalr)
### [SignalR com TypeScript](xref:tutorials/signalr-typescript-webpack)
## [Amostras](https://github.com/aspnet/SignalR-samples)
## Conceitos de servidor
### [Hubs](xref:signalr/hubs)
### [HubContext](xref:signalr/hubcontext)
### [Usuários e Grupos](xref:signalr/groups)
### [Publicar no Azure](xref:signalr/publish-to-azure-web-app)
### [Considerações sobre o design da API](xref:signalr/api-design)
## Clientes
### [Cliente .NET](xref:signalr/dotnet-client)
### [Referência da API REST](/dotnet/api/microsoft.aspnetcore.signalr.client)
### [Cliente Java](xref:signalr/java-client)
### [Referência de API Java](/java/api/com.microsoft.signalr?view=aspnet-signalr-java)
### [Cliente JavaScript](xref:signalr/javascript-client)
### [Referência de API JavaScript](/javascript/api/?view=signalr-js-latest)
## Hospedagem e dimensionamento
### [Visão geral](xref:signalr/scale)
### [Serviço Azure SignalR](/azure/azure-signalr/signalr-overview)
### [Backplane de Redis](xref:signalr/redis-backplane)
## [Configuração](xref:signalr/configuration)
## [Autenticação e autorização](xref:signalr/authn-and-authz)
## [Considerações sobre segurança](xref:signalr/security)
## [Protocolo de Hub do MessagePack](xref:signalr/messagepackhubprotocol)
## [Streaming](xref:signalr/streaming)
## [Comparar o SignalR e o SignalR Core](xref:signalr/version-differences)
## [WebSockets sem SignalR](xref:fundamentals/websockets)

# Testar, depurar e solucionar problemas
## [Teste de unidade](/dotnet/articles/core/testing/unit-testing-with-dotnet-test)
## [Testes de unidades de páginas Razor](xref:test/razor-pages-tests)
## [Controladores de teste](xref:mvc/controllers/testing)
## [Depuração remota](/visualstudio/debugger/remote-debugging-azure)
## [Depuração de instantâneo](/azure/application-insights/app-insights-snapshot-debugger)
## [Depurando de instantâneo no Visual Studio](/visualstudio/debugger/debug-live-azure-applications)
## [Testes de integração](xref:test/integration-tests)
## [Testes de estresse e carga](xref:test/loadtests)
## [Solução de problemas](xref:test/troubleshoot)
## [Registro em log](xref:fundamentals/logging/index)

# Acesso aos dados
## Tutoriais
### EF Core com Razor Pages
#### [Visão geral](xref:data/ef-rp/index)
#### [Introdução](xref:data/ef-rp/intro)
#### [Criar, ler, atualizar e excluir](xref:data/ef-rp/crud)
#### [Classificar, filtrar, paginar e agrupar](xref:data/ef-rp/sort-filter-page)
#### [Migrações](xref:data/ef-rp/migrations)
#### [Criar um modelo de dados complexo](xref:data/ef-rp/complex-data-model)
#### [Ler dados relacionados](xref:data/ef-rp/read-related-data)
#### [Atualizar dados relacionados](xref:data/ef-rp/update-related-data)
#### [Tratar conflitos de simultaneidade](xref:data/ef-rp/concurrency)
### [EF Core com MVC, BD novo](/ef/core/get-started/aspnetcore/new-db)
### [EF Core com MVC, BD existente](/ef/core/get-started/aspnetcore/existing-db)
### EF Core com MVC, tutorial longo
#### [Visão geral](xref:data/ef-mvc/index)
#### [Introdução](xref:data/ef-mvc/intro)
#### [Criar, ler, atualizar e excluir](xref:data/ef-mvc/crud)
#### [Classificar, filtrar, paginar e agrupar](xref:data/ef-mvc/sort-filter-page)
#### [Migrações](xref:data/ef-mvc/migrations)
#### [Criar um modelo de dados complexo](xref:data/ef-mvc/complex-data-model)
#### [Ler dados relacionados](xref:data/ef-mvc/read-related-data)
#### [Atualizar dados relacionados](xref:data/ef-mvc/update-related-data)
#### [Tratar conflitos de simultaneidade](xref:data/ef-mvc/concurrency)
#### [Herança](xref:data/ef-mvc/inheritance)
#### [Tópicos avançados](xref:data/ef-mvc/advanced)
## [EF 6 com ASP.NET Core](xref:data/entity-framework-6)
## Armazenamento do Azure com o Visual Studio
### [Serviços conectados](/azure/vs-azure-tools-connected-services-storage)
### [Armazenamento de Blobs](/azure/vs-storage-aspnet5-getting-started-blobs/)
### [Armazenamento de filas](/azure/vs-storage-aspnet5-getting-started-queues/)
### [Armazenamento de tabelas](/azure/vs-storage-aspnet5-getting-started-tables/)

# Desenvolvimento do lado do cliente
## [Visão geral](xref:client-side/index)
## [Gulp](xref:client-side/using-gulp)
## [Grunt](xref:client-side/using-grunt)
## LibMan
### [Visão geral](xref:client-side/libman/index)
### [CLI](xref:client-side/libman/libman-cli)
### [Visual Studio](xref:client-side/libman/libman-vs)
## [Bower](xref:client-side/bower)
## [LESS, Sass e Font Awesome](xref:client-side/less-sass-fa)
## [Agrupar e minificar](xref:client-side/bundling-and-minification)
## [Link do navegador](xref:client-side/using-browserlink)
## Aplicativos de página única
### [Visão geral](xref:spa/index)
### [Angular](xref:spa/angular)
### [React](xref:spa/react)
### [React com Redux](xref:spa/react-with-redux)
### [JavaScriptServices](xref:client-side/spa-services)

# Hospedagem e implantação
## [Visão geral](xref:host-and-deploy/index)
## Hospedar no Serviço de Aplicativo do Azure
### [Visão geral](xref:host-and-deploy/azure-apps/index)
### [Publicar com o Visual Studio](xref:tutorials/publish-to-azure-webapp-using-vs)
### [Publicar com as ferramentas da CLI](/azure/app-service/app-service-web-tutorial-dotnetcore-sqldb)
### [Publicar com Visual Studio e Git](xref:host-and-deploy/azure-apps/azure-continuous-deployment)
### [Implantação contínua com o Azure Pipelines](/azure/devops/pipelines/get-started-yaml)
### [Módulo do ASP.NET Core](xref:host-and-deploy/aspnet-core-module)
### [Solução de problemas](xref:host-and-deploy/azure-apps/troubleshoot)
### [Referência de erros](xref:host-and-deploy/azure-iis-errors-reference)
## DevOps 
### [Visão geral](xref:azure/devops/index)
### [Ferramentas e downloads](xref:azure/devops/tools-and-downloads)
### [Implantar no Serviço de Aplicativo](xref:azure/devops/deploy-to-app-service)
### [Integração contínua e implantação](xref:azure/devops/cicd)
### [Monitorar e solucionar problemas](xref:azure/devops/monitor)
### [Próximas etapas](xref:azure/devops/next-steps)
## Hospedar no Windows com o IIS
### [Visão geral](xref:host-and-deploy/iis/index)
### [Módulo do ASP.NET Core](xref:host-and-deploy/aspnet-core-module)
### [Suporte ao IIS no Visual Studio](xref:host-and-deploy/iis/development-time-iis-support)
### [Módulos do IIS](xref:host-and-deploy/iis/modules)
### [Solução de problemas](xref:host-and-deploy/iis/troubleshoot)
### [Referência de erros](xref:host-and-deploy/azure-iis-errors-reference)
## [Kestrel](xref:fundamentals/servers/kestrel)
## [HTTP.sys](xref:fundamentals/servers/httpsys)
## [Hospedar em um serviço Windows](xref:host-and-deploy/windows-service)
## [Hospedar em Linux com o Nginx](xref:host-and-deploy/linux-nginx)
## [Hospedar em Linux com o Apache](xref:host-and-deploy/linux-apache)
## Hospedar no Docker
### [Visão geral](xref:host-and-deploy/docker/index)
### [Compilar imagens do Docker](/dotnet/articles/core/docker/building-net-docker-images)
### [Ferramentas do Visual Studio](xref:host-and-deploy/docker/visual-studio-tools-for-docker)
### [Publicar em uma imagem do Docker](/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)
## [Configuração de balanceador de carga e de proxy](xref:host-and-deploy/proxy-load-balancer)
## [Hospedar em uma web farm](xref:host-and-deploy/web-farm)
## [Perfis de publicação do Visual Studio](xref:host-and-deploy/visual-studio-publish-profiles)
## [Estrutura de diretórios](xref:host-and-deploy/directory-structure)
## [Verificações de integridade](xref:host-and-deploy/health-checks)

# Segurança e identidade
## [Visão geral](xref:security/index)
## Autenticação
### [Introdução ao Identity](xref:security/authentication/identity)
### [Identidade Scaffold](xref:security/authentication/scaffold-identity)
### [Adicionar dados de usuário personalizados à Identidade](xref:security/authentication/add-user-data)
### [Personalizar Identidade](xref:security/authentication/customize_identity_model)
### [Opções de autenticação de OSS da comunidade](xref:security/authentication/community)
### [Configurar o Identity](xref:security/authentication/identity-configuration)
### [Configurar a Autenticação do Windows](xref:security/authentication/windowsauth)
### [Provedores de armazenamento personalizados para o Identity](xref:security/authentication/identity-custom-storage-providers)
### Provedores externos
#### [Visão geral](xref:security/authentication/social/index)
#### [Autenticação do Facebook](xref:security/authentication/facebook-logins)
#### [Autenticação do Twitter](xref:security/authentication/twitter-logins)
#### [Autenticação do Google](xref:security/authentication/google-logins)
#### [Autenticação da Microsoft](xref:security/authentication/microsoft-logins)
#### [Provedores de autenticação externos](xref:security/authentication/otherlogins)
#### [Declarações adicionais](xref:security/authentication/social/additional-claims)
### [Autenticação de Web Services Federation](xref:security/authentication/ws-federation)
### [Confirmação de conta e recuperação de senha](xref:security/authentication/accconfirm)
### [Habilitar a geração de código QR no Identity](xref:security/authentication/identity-enable-qrcodes)
### [Autenticação de dois fatores com SMS](xref:security/authentication/2fa)
### [Usar a autenticação de cookie sem o Identity](xref:security/authentication/cookie)
### Azure Active Directory
#### [Visão geral](xref:security/authentication/azure-active-directory/index)
#### [Integrar o Azure AD em um aplicativo Web](https://azure.microsoft.com/documentation/samples/active-directory-dotnet-webapp-openidconnect-aspnetcore/)
#### [Integrar o Azure AD B2C em um aplicativo Web](xref:security/authentication/azure-ad-b2c)
#### [Integrar o Azure AD B2C em uma API Web](xref:security/authentication/azure-ad-b2c-webapi)
#### [Chamar uma API Web do WPF](https://azure.microsoft.com/documentation/samples/active-directory-dotnet-native-aspnetcore/)
#### [Chamar uma API Web em um aplicativo Web usando o Azure AD](https://azure.microsoft.com/documentation/samples/active-directory-dotnet-webapp-webapi-openidconnect-aspnetcore/)
### [Proteger aplicativos ASP.NET Core com o IdentityServer4](https://identityserver4.readthedocs.io/)
### [Proteger aplicativos ASP.NET Core com a Autenticação do Serviço de Aplicativo do Azure (autenticação fácil)](/azure/app-service/app-service-authentication-overview)
### [Contas de usuários individuais](xref:security/authentication/individual)
## Autorização
### [Visão geral](xref:security/authorization/introduction)
### [Criar um aplicativo Web com autorização](xref:security/authorization/secure-data)
### [Convenções de autorização de Páginas Razor](xref:security/authorization/razor-pages-authorization)
### [Autorização simples](xref:security/authorization/simple)
### [Autorização baseada em função](xref:security/authorization/roles)
### [Autorização baseada em declarações](xref:security/authorization/claims)
### [Autorização baseada em política](xref:security/authorization/policies)
### [Provedores da política de autorização](xref:security/authorization/iauthorizationpolicyprovider)
### [Injeção de dependência em manipuladores de requisitos](xref:security/authorization/dependencyinjection)
### [Autorização baseada em recursos](xref:security/authorization/resourcebased)
### [Autorização baseada em exibição](xref:security/authorization/views)
### [Limitar a identidade por esquema](xref:security/authorization/limitingidentitybyscheme)
## Proteção de dados
### [Visão geral](xref:security/data-protection/introduction)
### [APIs de Proteção de Dados](xref:security/data-protection/using-data-protection)
### APIs de consumidor
#### [Visão geral](xref:security/data-protection/consumer-apis/overview)
#### [Cadeias de caracteres de finalidade](xref:security/data-protection/consumer-apis/purpose-strings)
#### [Multilocação e hierarquia de finalidade](xref:security/data-protection/consumer-apis/purpose-strings-multitenancy)
#### [Senhas hash](xref:security/data-protection/consumer-apis/password-hashing)
#### [Limitar o tempo de vida de cargas protegidas](xref:security/data-protection/consumer-apis/limited-lifetime-payloads)
#### [Desproteger cargas cujas chaves foram revogadas](xref:security/data-protection/consumer-apis/dangerous-unprotect)
### Configuração
#### [Visão geral](xref:security/data-protection/configuration/index)
#### [Configurar a proteção de dados](xref:security/data-protection/configuration/overview)
#### [Configurações padrão](xref:security/data-protection/configuration/default-settings)
#### [Política ampla de computador](xref:security/data-protection/configuration/machine-wide-policy)
#### [Cenários sem reconhecimento de DI](xref:security/data-protection/configuration/non-di-scenarios)
### APIs de extensibilidade
#### [Visão geral](xref:security/data-protection/extensibility/index)
#### [Extensibilidade da criptografia básica](xref:security/data-protection/extensibility/core-crypto)
#### [Extensibilidade de gerenciamento de chaves](xref:security/data-protection/extensibility/key-management)
#### [APIs diversas](xref:security/data-protection/extensibility/misc-apis)
### Implementação
#### [Visão geral](xref:security/data-protection/implementation/index)
#### [Detalhes de criptografia autenticada](xref:security/data-protection/implementation/authenticated-encryption-details)
#### [Derivação de subchaves e criptografia autenticada](xref:security/data-protection/implementation/subkeyderivation)
#### [Cabeçalhos de contexto](xref:security/data-protection/implementation/context-headers)
#### [Gerenciamento de chaves](xref:security/data-protection/implementation/key-management)
#### [Provedores de armazenamento de chaves](xref:security/data-protection/implementation/key-storage-providers)
#### [Criptografia de chave em repouso](xref:security/data-protection/implementation/key-encryption-at-rest)
#### [Imutabilidade de chave e configurações](xref:security/data-protection/implementation/key-immutability)
#### [Formato do armazenamento de chaves](xref:security/data-protection/implementation/key-storage-format)
#### [Provedores de proteção de dados efêmeros](xref:security/data-protection/implementation/key-storage-ephemeral)
### Compatibilidade
#### [Visão geral](xref:security/data-protection/compatibility/index)
#### [Substitua <machineKey> no ASP.NET](xref:security/data-protection/compatibility/replacing-machinekey)
## [Proteger segredos no desenvolvimento](xref:security/app-secrets)
## [Impor o HTTPS](xref:security/enforcing-ssl)
## [Compatível com o RGPD (Regulamento Geral sobre a Proteção de Dados) da UE](xref:security/gdpr)
## [Provedor de configuração do Azure Key Vault](xref:security/key-vault-configuration)
## [Falsificação antissolicitação](xref:security/anti-request-forgery)
## [Prevenir ataques de redirecionamento abertos](xref:security/preventing-open-redirects)
## [Evitar scripts entre sites](xref:security/cross-site-scripting)
## [Habilitar o CORS (Solicitações Entre Origens)](xref:security/cors)
## [Compartilhar cookies entre aplicativos](xref:security/cookie-sharing)
## [Lista segura de IP](xref:security/ip-safelist)

# Desempenho
## [Visão geral](xref:performance/performance-best-practices)
##  Cache de resposta
### [Visão geral](xref:performance/caching/response)
### [Cache na memória](xref:performance/caching/memory)
### [Cache distribuído](xref:performance/caching/distributed)
### [Middleware de cache de resposta](xref:performance/caching/middleware)
## [Compactação de resposta](xref:performance/response-compression)
## [Ferramentas de Diagnóstico](xref:performance/diagnostic-tools)
## [Testes de estresse e carga](xref:test/loadtests)

# Outros tópicos
## [Globalização e localização](xref:fundamentals/localization)
## [Localização do objeto portátil com o Orchard Core](xref:fundamentals/portable-object-localization)
## [Reescrita de URL](xref:fundamentals/url-rewriting)
## [Provedores de arquivo](xref:fundamentals/file-providers)
## [Recursos de solicitação](xref:fundamentals/request-features)
## [Acessar o HttpContext](xref:fundamentals/httpcontext)
## [Alterar tokens](xref:fundamentals/change-tokens)
## [OWIN (Open Web Interface para .NET)](xref:fundamentals/owin)
## [Tarefas em segundo plano com serviços hospedados](xref:fundamentals/host/hosted-services)
## [Hospedando assemblies de inicialização](xref:fundamentals/configuration/platform-specific-configuration)
## [Metapacote Microsoft.AspNetCore.App](xref:fundamentals/metapackage-app)
## [Metapacote Microsoft.AspNetCore.All](xref:fundamentals/metapackage)
## [Fazendo log com o LoggerMessage](xref:fundamentals/logging/loggermessage)
## [Usar um inspetor de arquivo](xref:tutorials/dotnet-watch)

# Migração
## [2.2 a 3.0](xref:migration/22-to-30)
## [2.1 a 2.2](xref:migration/21-to-22)
## [2.0 a 2.1](xref:migration/20_21)
## 1.x a 2.0
### [Visão geral](xref:migration/1x-to-2x/index)
### [Autenticação e identidade](xref:migration/1x-to-2x/identity-2x)
## ASP.NET para ASP.NET Core
### [Visão geral](xref:migration/proper-to-2x/index)
### [MVC](xref:migration/mvc)
### [API Web](xref:migration/webapi)
### [Configuração](xref:migration/configuration)
### [Autenticação e identidade](xref:migration/identity)
### [ClaimsPrincipal.Current](xref:migration/claimsprincipal-current)
### [Associação de identidade](xref:migration/proper-to-2x/membership-to-core-identity)
### [Módulos HTTP para middleware](xref:migration/http-modules)
## [Registro em log (não o ASP.NET Core)](xref:migration/logging-nonaspnetcore)

# [Referência de API](/dotnet/api/?view=aspnetcore-2.1)

# [Contribuir](https://github.com/aspnet/Docs/blob/master/CONTRIBUTING.md)
