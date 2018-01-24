---
title: Adicionando um modelo a um aplicativo ASP.NET Core MVC.
author: rick-anderson
description: Adicione um modelo a um aplicativo ASP.NET Core simples.
ms.author: riande
ms.date: 09/18/2017
ms.topic: get-started-article
ms.technology: aspnet
ms.prod: asp.net-core
manager: wpickett
uid: tutorials/first-mvc-app-xplat/adding-model
ms.openlocfilehash: 4c09225c925c326da7e815b39f176325a04fc17b
ms.sourcegitcommit: 3e303620a125325bb9abd4b2d315c106fb8c47fd
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/19/2018
---
[!INCLUDE[adding-model1](../../includes/mvc-intro/adding-model1.md)]

* <span data-ttu-id="d9d96-103">Adicionar uma classe denominada *Movie.cs* à pasta *Modelos*.</span><span class="sxs-lookup"><span data-stu-id="d9d96-103">Add a class to the *Models* folder named *Movie.cs*.</span></span>
* <span data-ttu-id="d9d96-104">Adicione o código a seguir ao arquivo *Models/Movie.cs*:</span><span class="sxs-lookup"><span data-stu-id="d9d96-104">Add the following code to the *Models/Movie.cs* file:</span></span>

[!code-csharp[Main](../../tutorials/first-mvc-app/start-mvc/sample/MvcMovie/Models/MovieNoEF.cs?name=snippet_1)]

<span data-ttu-id="d9d96-105">O campo `ID` é necessário para o banco de dados para a chave primária.</span><span class="sxs-lookup"><span data-stu-id="d9d96-105">The `ID` field is required by the database for the primary key.</span></span> 

<span data-ttu-id="d9d96-106">Compile o aplicativo para verificar se você não tem nenhum erro e, por fim, você adicionou um **M**odelo ao seu aplicativo **M**VC.</span><span class="sxs-lookup"><span data-stu-id="d9d96-106">Build the app to verify you don't have any errors, and you've finally added a **M**odel to your **M**VC app.</span></span>

## <a name="prepare-the-project-for-scaffolding"></a><span data-ttu-id="d9d96-107">Preparar o projeto para scaffolding</span><span class="sxs-lookup"><span data-stu-id="d9d96-107">Prepare the project for scaffolding</span></span>

- <span data-ttu-id="d9d96-108">Adicione os pacotes NuGet realçados a seguir ao arquivo *MvcMovie.csproj*:</span><span class="sxs-lookup"><span data-stu-id="d9d96-108">Add the following highlighted NuGet packages to the *MvcMovie.csproj* file:</span></span>
             
   [!code-csharp[Main](start-mvc/sample/MvcMovie/MvcMovie.csproj?highlight=7,10)]

- <span data-ttu-id="d9d96-109">Salve o arquivo e selecione **Restaurar** para a mensagem **Informativa** "Há dependências não resolvidas".</span><span class="sxs-lookup"><span data-stu-id="d9d96-109">Save the file and select **Restore** to the **Info** message "There are unresolved dependencies".</span></span>
- <span data-ttu-id="d9d96-110">Crie um arquivo *Models/MvcMovieContext.cs* e adicione a seguinte classe `MvcMovieContext`:</span><span class="sxs-lookup"><span data-stu-id="d9d96-110">Create a *Models/MvcMovieContext.cs* file and add the following `MvcMovieContext` class:</span></span>

   [!code-csharp[Main](start-mvc/sample/MvcMovie/Models/MvcMovieContext.cs)]
   
- <span data-ttu-id="d9d96-111">Abra o arquivo *Startup.cs* e adicione dois usings:</span><span class="sxs-lookup"><span data-stu-id="d9d96-111">Open the *Startup.cs* file and add two usings:</span></span>

   [!code-csharp[Main](start-mvc/sample/MvcMovie/Startup.cs?name=snippet1&highlight=1,2)]

- <span data-ttu-id="d9d96-112">Adicione o contexto do banco de dados para o arquivo *Startup.cs*:</span><span class="sxs-lookup"><span data-stu-id="d9d96-112">Add the database context to the *Startup.cs* file:</span></span>

   [!code-csharp[Main](start-mvc/sample/MvcMovie/Startup.cs?name=snippet2&highlight=6-7)]

  <span data-ttu-id="d9d96-113">Isso informa ao Entity Framework quais classes de modelo estão incluídas no modelo de dados.</span><span class="sxs-lookup"><span data-stu-id="d9d96-113">This tells Entity Framework which model classes are included in the data model.</span></span> <span data-ttu-id="d9d96-114">Você está definindo um *conjunto de entidades* de objetos Movie, que serão representados no banco de dados como uma tabela Movie.</span><span class="sxs-lookup"><span data-stu-id="d9d96-114">You're defining one *entity set* of Movie objects, which will be represented in the database as a Movie table.</span></span>

- <span data-ttu-id="d9d96-115">Crie o projeto para verificar se não existem erros.</span><span class="sxs-lookup"><span data-stu-id="d9d96-115">Build the project to verify there are no errors.</span></span>

## <a name="scaffold-the-moviecontroller"></a><span data-ttu-id="d9d96-116">Faça o scaffolding do MovieController</span><span class="sxs-lookup"><span data-stu-id="d9d96-116">Scaffold the MovieController</span></span>

<span data-ttu-id="d9d96-117">Abra uma janela de terminal na pasta do projeto e execute os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="d9d96-117">Open a terminal window in the project folder and run the following commands:</span></span>

```
dotnet restore
dotnet aspnet-codegenerator controller -name MoviesController -m Movie -dc MvcMovieContext --relativeFolderPath Controllers --useDefaultLayout --referenceScriptLibraries 
```

> [!NOTE]
> <span data-ttu-id="d9d96-118">Se você receber um erro quando executar o comando de scaffolding, consulte [problema 444 no repositório de scaffolding](https://github.com/aspnet/scaffolding/issues/444) para uma solução alternativa.</span><span class="sxs-lookup"><span data-stu-id="d9d96-118">If you get an error when the scaffolding command runs, see [issue 444 in the scaffolding repository](https://github.com/aspnet/scaffolding/issues/444) for a workaround.</span></span>

<span data-ttu-id="d9d96-119">O mecanismo de scaffolding cria o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d9d96-119">The scaffolding engine creates the following:</span></span>

* <span data-ttu-id="d9d96-120">Um controlador de filmes (*Controllers/MoviesController.cs*)</span><span class="sxs-lookup"><span data-stu-id="d9d96-120">A movies controller (*Controllers/MoviesController.cs*)</span></span>
* <span data-ttu-id="d9d96-121">Arquivos de exibição do Razor para as páginas Criar, Excluir, Detalhes, Editar e Índice (*Views/Movies/\*.cshtml*)</span><span class="sxs-lookup"><span data-stu-id="d9d96-121">Razor view files for Create, Delete, Details, Edit and Index pages (*Views/Movies/\*.cshtml*)</span></span>

<span data-ttu-id="d9d96-122">A criação automática das exibições e métodos de ação [CRUD](https://wikipedia.org/wiki/Create,_read,_update_and_delete) (criar, ler, atualizar e excluir) é conhecida como *scaffolding*.</span><span class="sxs-lookup"><span data-stu-id="d9d96-122">The automatic creation of [CRUD](https://wikipedia.org/wiki/Create,_read,_update_and_delete) (create, read, update, and delete) action methods and views is known as *scaffolding*.</span></span> <span data-ttu-id="d9d96-123">Logo você terá um aplicativo Web totalmente funcional que permitirá que você gerencie um banco de dados de filmes.</span><span class="sxs-lookup"><span data-stu-id="d9d96-123">You'll soon have a fully functional web application that lets you manage a movie database.</span></span>

[!INCLUDE[adding-model 2x](../../includes/mvc-intro/adding-model2xp.md)]

[!INCLUDE[adding-model](../../includes/mvc-intro/adding-model3.md)]

<span data-ttu-id="d9d96-124">Agora você tem um banco de dados e páginas para exibir, editar, atualizar e excluir dados.</span><span class="sxs-lookup"><span data-stu-id="d9d96-124">You now have a database and pages to display, edit, update and delete data.</span></span> <span data-ttu-id="d9d96-125">No próximo tutorial, trabalharemos com o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d9d96-125">In the next tutorial, we'll work with the database.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="d9d96-126">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="d9d96-126">Additional resources</span></span>

* [<span data-ttu-id="d9d96-127">Auxiliares de marcação</span><span class="sxs-lookup"><span data-stu-id="d9d96-127">Tag Helpers</span></span>](xref:mvc/views/tag-helpers/intro)
* [<span data-ttu-id="d9d96-128">Globalização e localização</span><span class="sxs-lookup"><span data-stu-id="d9d96-128">Globalization and localization</span></span>](xref:fundamentals/localization)

>[!div class="step-by-step"]
<span data-ttu-id="d9d96-129">[Anterior – adicionar uma exibição](adding-view.md)
[Próximo – trabalhando com SQLite](working-with-sql.md)</span><span class="sxs-lookup"><span data-stu-id="d9d96-129">[Previous - Add a view](adding-view.md)
[Next - Working with SQLite](working-with-sql.md)</span></span>