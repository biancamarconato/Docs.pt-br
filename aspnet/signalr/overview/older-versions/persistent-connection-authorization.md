---
uid: signalr/overview/older-versions/persistent-connection-authorization
title: "Autenticação e autorização para conexões persistentes SignalR (SignalR 1. x) | Microsoft Docs"
author: pfletcher
description: "Este tópico descreve como implantar a autorização em uma conexão persistente. Para obter informações gerais sobre como integrar a segurança em um aplicativo de SignalR,..."
ms.author: aspnetcontent
manager: wpickett
ms.date: 10/21/2013
ms.topic: article
ms.assetid: c34bc627-41af-4c21-a817-e97a19a7f252
ms.technology: dotnet-signalr
ms.prod: .net-framework
msc.legacyurl: /signalr/overview/older-versions/persistent-connection-authorization
msc.type: authoredcontent
ms.openlocfilehash: 2e97dfd03c61b110325c41a992b4af490fcd17de
ms.sourcegitcommit: 060879fcf3f73d2366b5c811986f8695fff65db8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/24/2018
---
<a name="authentication-and-authorization-for-signalr-persistent-connections-signalr-1x"></a><span data-ttu-id="e9bff-104">Autenticação e autorização para conexões persistentes SignalR (SignalR 1. x)</span><span class="sxs-lookup"><span data-stu-id="e9bff-104">Authentication and Authorization for SignalR Persistent Connections (SignalR 1.x)</span></span>
====================
<span data-ttu-id="e9bff-105">por [Patrick Fletcher](https://github.com/pfletcher), [Tom FitzMacken](https://github.com/tfitzmac)</span><span class="sxs-lookup"><span data-stu-id="e9bff-105">by [Patrick Fletcher](https://github.com/pfletcher), [Tom FitzMacken](https://github.com/tfitzmac)</span></span>

> <span data-ttu-id="e9bff-106">Este tópico descreve como implantar a autorização em uma conexão persistente.</span><span class="sxs-lookup"><span data-stu-id="e9bff-106">This topic describes how to enforce authorization on a persistent connection.</span></span> <span data-ttu-id="e9bff-107">Para obter informações gerais sobre como integrar a segurança em um aplicativo SignalR, consulte [Introdução à segurança](index.md).</span><span class="sxs-lookup"><span data-stu-id="e9bff-107">For general information about integrating security into a SignalR application, see [Introduction to Security](index.md).</span></span>


## <a name="enforce-authorization"></a><span data-ttu-id="e9bff-108">Implantar a autorização</span><span class="sxs-lookup"><span data-stu-id="e9bff-108">Enforce authorization</span></span>

<span data-ttu-id="e9bff-109">Para impor regras de autorização ao usar um [PersistentConnection](https://msdn.microsoft.com/library/microsoft.aspnet.signalr.persistentconnection(v=vs.111).aspx) você deve substituir o `AuthorizeRequest` método.</span><span class="sxs-lookup"><span data-stu-id="e9bff-109">To enforce authorization rules when using a [PersistentConnection](https://msdn.microsoft.com/library/microsoft.aspnet.signalr.persistentconnection(v=vs.111).aspx) you must override the `AuthorizeRequest` method.</span></span> <span data-ttu-id="e9bff-110">Não é possível usar o `Authorize` atributo com conexões persistentes.</span><span class="sxs-lookup"><span data-stu-id="e9bff-110">You cannot use the `Authorize` attribute with persistent connections.</span></span> <span data-ttu-id="e9bff-111">O `AuthorizeRequest` método é chamado pelo SignalR Framework antes de cada solicitação para verificar se o usuário está autorizado a executar a ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="e9bff-111">The `AuthorizeRequest` method is called by the SignalR Framework before every request to verify that the user is authorized to perform the requested action.</span></span> <span data-ttu-id="e9bff-112">O `AuthorizeRequest` método não é chamado do cliente; em vez disso, autenticar o usuário por meio do mecanismo de autenticação padrão do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e9bff-112">The `AuthorizeRequest` method is not called from the client; instead, you authenticate the user through your application's standard authentication mechanism.</span></span>

<span data-ttu-id="e9bff-113">O exemplo a seguir mostra como limitar solicitações para usuários autenticados.</span><span class="sxs-lookup"><span data-stu-id="e9bff-113">The example below shows how to limit requests to authenticated users.</span></span>

[!code-csharp[Main](persistent-connection-authorization/samples/sample1.cs)]

<span data-ttu-id="e9bff-114">Você pode adicionar qualquer lógica de autorização personalizado no método AuthorizeRequest; como verificar se um usuário pertencer a uma função específica.</span><span class="sxs-lookup"><span data-stu-id="e9bff-114">You can add any customized authorization logic in the AuthorizeRequest method; such as, checking whether a user belongs to a particular role.</span></span>