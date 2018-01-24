---
title: Criar uma API Web com o ASP.NET Core e o Visual Studio para Windows
author: rick-anderson
description: Compilar uma API Web com o ASP.NET Core MVC e o Visual Studio para Windows
ms.author: riande
manager: wpickett
ms.date: 08/15/2017
ms.topic: get-started-article
ms.technology: aspnet
ms.prod: asp.net-core
uid: tutorials/first-web-api
ms.openlocfilehash: 234dbf73f9751ad4f995d6e7471d94f060fb15bf
ms.sourcegitcommit: 3e303620a125325bb9abd4b2d315c106fb8c47fd
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/19/2018
---
#<a name="create-a-web-api-with-aspnet-core-and-visual-studio-for-windows"></a><span data-ttu-id="b9316-103">Criar uma API Web com o ASP.NET Core e o Visual Studio para Windows</span><span class="sxs-lookup"><span data-stu-id="b9316-103">Create a web API with ASP.NET Core and Visual Studio for Windows</span></span>

<span data-ttu-id="b9316-104">Por [Rick Anderson](https://twitter.com/RickAndMSFT) e [Mike Wasson](https://github.com/mikewasson)</span><span class="sxs-lookup"><span data-stu-id="b9316-104">By [Rick Anderson](https://twitter.com/RickAndMSFT) and [Mike Wasson](https://github.com/mikewasson)</span></span>

<span data-ttu-id="b9316-105">Este tutorial compilará uma API Web para gerenciar uma lista de itens de “tarefas pendentes”.</span><span class="sxs-lookup"><span data-stu-id="b9316-105">This tutorial builds a web API for managing a list of "to-do" items.</span></span> <span data-ttu-id="b9316-106">Uma interface de usuário (UI) não é criada.</span><span class="sxs-lookup"><span data-stu-id="b9316-106">A user interface (UI) is not created.</span></span>

<span data-ttu-id="b9316-107">Há três versões deste tutorial:</span><span class="sxs-lookup"><span data-stu-id="b9316-107">There are 3 versions of this tutorial:</span></span>

* <span data-ttu-id="b9316-108">Windows: API Web com o Visual Studio para Windows (este tutorial)</span><span class="sxs-lookup"><span data-stu-id="b9316-108">Windows: Web API with Visual Studio for Windows (This tutorial)</span></span>
* <span data-ttu-id="b9316-109">macOS: [API Web com o Visual Studio para Mac](xref:tutorials/first-web-api-mac)</span><span class="sxs-lookup"><span data-stu-id="b9316-109">macOS: [Web API with Visual Studio for Mac](xref:tutorials/first-web-api-mac)</span></span>
* <span data-ttu-id="b9316-110">macOS, Linux, Windows: [API Web com o Visual Studio Code](xref:tutorials/web-api-vsc)</span><span class="sxs-lookup"><span data-stu-id="b9316-110">macOS, Linux, Windows: [Web API with Visual Studio Code](xref:tutorials/web-api-vsc)</span></span>

<!-- WARNING: The code AND images in this doc are used by uid: tutorials/web-api-vsc, tutorials/first-web-api-mac and tutorials/first-web-api. If you change any code/images in this tutorial, update uid: tutorials/web-api-vsc -->

[!INCLUDE[intro to web API](../includes/webApi/intro.md)]

## <a name="prerequisites"></a><span data-ttu-id="b9316-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="b9316-111">Prerequisites</span></span>

[!INCLUDE[install 2.0](../includes/install2.0.md)]

<span data-ttu-id="b9316-112">Consulte [este PDF](https://github.com/aspnet/Docs/blob/master/aspnetcore/tutorials/first-web-api/_static/_webAPI.pdf) para o ASP.NET Core versão 1.1.</span><span class="sxs-lookup"><span data-stu-id="b9316-112">See [this PDF](https://github.com/aspnet/Docs/blob/master/aspnetcore/tutorials/first-web-api/_static/_webAPI.pdf) for the ASP.NET Core 1.1 version.</span></span>

## <a name="create-the-project"></a><span data-ttu-id="b9316-113">Criar o projeto</span><span class="sxs-lookup"><span data-stu-id="b9316-113">Create the project</span></span>

<span data-ttu-id="b9316-114">No Visual Studio, selecione o menu **Arquivo**, > **Novo** > **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="b9316-114">From Visual Studio, select **File** menu, > **New** > **Project**.</span></span>

<span data-ttu-id="b9316-115">Selecione o modelo de projeto **Aplicativo Web ASP.NET Core (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="b9316-115">Select the **ASP.NET Core Web Application (.NET Core)** project template.</span></span> <span data-ttu-id="b9316-116">Nomeie o projeto `TodoApi` e selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9316-116">Name the project `TodoApi` and select **OK**.</span></span>

![Caixa de diálogo Novo projeto](first-web-api/_static/new-project.png)

<span data-ttu-id="b9316-118">Na caixa de diálogo **Novo aplicativo Web ASP.NET Core – TodoApi**, selecione o modelo **API Web**.</span><span class="sxs-lookup"><span data-stu-id="b9316-118">In the **New ASP.NET Core Web Application - TodoApi** dialog, select the **Web API** template.</span></span> <span data-ttu-id="b9316-119">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9316-119">Select **OK**.</span></span> <span data-ttu-id="b9316-120">**Não** selecione **Habilitar Suporte ao Docker**.</span><span class="sxs-lookup"><span data-stu-id="b9316-120">Do **not** select **Enable Docker Support**.</span></span>

![Caixa de diálogo Novo Aplicativo Web ASP.NET com modelo de projeto de API Web selecionado de Modelos do ASP.NET Core](first-web-api/_static/web-api-project.png)

### <a name="launch-the-app"></a><span data-ttu-id="b9316-122">Iniciar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="b9316-122">Launch the app</span></span>

<span data-ttu-id="b9316-123">No Visual Studio, pressione CTRL + F5 para iniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b9316-123">In Visual Studio, press CTRL+F5 to launch the app.</span></span> <span data-ttu-id="b9316-124">O Visual Studio inicia um navegador e navega para `http://localhost:port/api/values`, em que *porta* é um número da porta escolhido aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="b9316-124">Visual Studio launches a browser and navigates to `http://localhost:port/api/values`, where *port* is a randomly chosen port number.</span></span> <span data-ttu-id="b9316-125">O Chrome, Microsoft Edge e Firefox exibem a seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="b9316-125">Chrome, Microsoft Edge, and Firefox display the following output:</span></span>

```
["value1","value2"]
```

### <a name="add-a-model-class"></a><span data-ttu-id="b9316-126">Adicionar uma classe de modelo</span><span class="sxs-lookup"><span data-stu-id="b9316-126">Add a model class</span></span>

<span data-ttu-id="b9316-127">Um modelo é um objeto que representa os dados no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b9316-127">A model is an object that represents the data in the app.</span></span> <span data-ttu-id="b9316-128">Nesse caso, o único modelo é um item de tarefas pendentes.</span><span class="sxs-lookup"><span data-stu-id="b9316-128">In this case, the only model is a to-do item.</span></span>

<span data-ttu-id="b9316-129">Adicione uma pasta denominada "Modelos".</span><span class="sxs-lookup"><span data-stu-id="b9316-129">Add a folder named "Models".</span></span> <span data-ttu-id="b9316-130">No Gerenciador de Soluções, clique com o botão direito do mouse no projeto.</span><span class="sxs-lookup"><span data-stu-id="b9316-130">In Solution Explorer, right-click the project.</span></span> <span data-ttu-id="b9316-131">Selecione **Adicionar** > **Nova Pasta**.</span><span class="sxs-lookup"><span data-stu-id="b9316-131">Select **Add** > **New Folder**.</span></span> <span data-ttu-id="b9316-132">Nomeie a pasta *Models*.</span><span class="sxs-lookup"><span data-stu-id="b9316-132">Name the folder *Models*.</span></span>

<span data-ttu-id="b9316-133">Observação: as classes de modelo entram em qualquer lugar no projeto.</span><span class="sxs-lookup"><span data-stu-id="b9316-133">Note: The model classes go anywhere in the project.</span></span> <span data-ttu-id="b9316-134">A pasta *Modelos* é usada por convenção para as classes de modelo.</span><span class="sxs-lookup"><span data-stu-id="b9316-134">The *Models* folder is used by convention for model classes.</span></span>

<span data-ttu-id="b9316-135">Adicione uma classe `TodoItem`.</span><span class="sxs-lookup"><span data-stu-id="b9316-135">Add a `TodoItem` class.</span></span> <span data-ttu-id="b9316-136">Clique com o botão direito do mouse na pasta *Modelos* e selecione **Adicionar** > **Classe**.</span><span class="sxs-lookup"><span data-stu-id="b9316-136">Right-click the *Models* folder and select **Add** > **Class**.</span></span> <span data-ttu-id="b9316-137">Nomeie a classe `TodoItem` e, em seguida, selecione **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="b9316-137">Name the class `TodoItem` and select **Add**.</span></span>

<span data-ttu-id="b9316-138">Atualize a classe `TodoItem` com o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="b9316-138">Update the `TodoItem` class with the following code:</span></span>

[!code-csharp[Main](first-web-api/sample/TodoApi/Models/TodoItem.cs)]

<span data-ttu-id="b9316-139">O banco de dados gera o `Id` quando um `TodoItem` é criado.</span><span class="sxs-lookup"><span data-stu-id="b9316-139">The database generates the `Id` when a `TodoItem` is created.</span></span>

### <a name="create-the-database-context"></a><span data-ttu-id="b9316-140">Criar o contexto de banco de dados</span><span class="sxs-lookup"><span data-stu-id="b9316-140">Create the database context</span></span>

<span data-ttu-id="b9316-141">O *contexto de banco de dados* é a classe principal que coordena a funcionalidade do Entity Framework para um determinado modelo de dados.</span><span class="sxs-lookup"><span data-stu-id="b9316-141">The *database context* is the main class that coordinates Entity Framework functionality for a given data model.</span></span> <span data-ttu-id="b9316-142">Essa classe é criada derivando-a da classe `Microsoft.EntityFrameworkCore.DbContext`.</span><span class="sxs-lookup"><span data-stu-id="b9316-142">This class is created by deriving from the `Microsoft.EntityFrameworkCore.DbContext` class.</span></span>

<span data-ttu-id="b9316-143">Adicione uma classe `TodoContext`.</span><span class="sxs-lookup"><span data-stu-id="b9316-143">Add a `TodoContext` class.</span></span> <span data-ttu-id="b9316-144">Clique com o botão direito do mouse na pasta *Modelos* e selecione **Adicionar** > **Classe**.</span><span class="sxs-lookup"><span data-stu-id="b9316-144">Right-click the *Models* folder and select **Add** > **Class**.</span></span> <span data-ttu-id="b9316-145">Nomeie a classe `TodoContext` e, em seguida, selecione **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="b9316-145">Name the class `TodoContext` and select **Add**.</span></span>

<span data-ttu-id="b9316-146">Substitua a classe pelo código a seguir:</span><span class="sxs-lookup"><span data-stu-id="b9316-146">Replace the class with the following code:</span></span>

[!code-csharp[Main](first-web-api/sample/TodoApi/Models/TodoContext.cs)]

[!INCLUDE[Register the database context](../includes/webApi/register_dbContext.md)]

### <a name="add-a-controller"></a><span data-ttu-id="b9316-147">Adicionar um controlador</span><span class="sxs-lookup"><span data-stu-id="b9316-147">Add a controller</span></span>

<span data-ttu-id="b9316-148">No Gerenciador de Soluções, clique com o botão direito do mouse na pasta *Controladores*.</span><span class="sxs-lookup"><span data-stu-id="b9316-148">In Solution Explorer, right-click the *Controllers* folder.</span></span> <span data-ttu-id="b9316-149">Selecione **Adicionar** > **Novo Item**.</span><span class="sxs-lookup"><span data-stu-id="b9316-149">Select **Add** > **New Item**.</span></span> <span data-ttu-id="b9316-150">Na caixa de diálogo **Adicionar Novo Item**, selecione o modelo **Classe do Controlador de API Web**.</span><span class="sxs-lookup"><span data-stu-id="b9316-150">In the **Add New Item** dialog, select the **Web API Controller Class** template.</span></span> <span data-ttu-id="b9316-151">Nomeie a classe `TodoController`.</span><span class="sxs-lookup"><span data-stu-id="b9316-151">Name the class `TodoController`.</span></span>

![Caixa de diálogo Adicionar Novo Item com o controlador na caixa de pesquisa e o controlador da API Web selecionados](first-web-api/_static/new_controller.png)

<span data-ttu-id="b9316-153">Substitua a classe pelo código a seguir:</span><span class="sxs-lookup"><span data-stu-id="b9316-153">Replace the class with the following code:</span></span>

[!INCLUDE[code and get todo items](../includes/webApi/getTodoItems.md)]

### <a name="launch-the-app"></a><span data-ttu-id="b9316-154">Iniciar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="b9316-154">Launch the app</span></span>

<span data-ttu-id="b9316-155">No Visual Studio, pressione CTRL + F5 para iniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b9316-155">In Visual Studio, press CTRL+F5 to launch the app.</span></span> <span data-ttu-id="b9316-156">O Visual Studio inicia um navegador e navega para `http://localhost:port/api/values`, em que *porta* é um número da porta escolhido aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="b9316-156">Visual Studio launches a browser and navigates to `http://localhost:port/api/values`, where *port* is a randomly chosen port number.</span></span> <span data-ttu-id="b9316-157">Navegue até o controlador `Todo` no `http://localhost:port/api/todo`.</span><span class="sxs-lookup"><span data-stu-id="b9316-157">Navigate to the `Todo` controller at `http://localhost:port/api/todo`.</span></span>

[!INCLUDE[last part of web API](../includes/webApi/end.md)]

[!INCLUDE[next steps](../includes/webApi/next.md)]
