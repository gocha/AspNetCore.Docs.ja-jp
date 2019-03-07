---
title: ASP.NET Core でのポリシー設定
author: rick-anderson
description: ポリシーの認証スキーム容易に 1 つの論理認証方式を使用して
ms.author: riande
ms.date: 2/28/2019
uid: security/authentication/policyschemes
ms.openlocfilehash: c310b61e14df2b7846e32a602bb75914a5850aff
ms.sourcegitcommit: 036d4b03fd86ca5bb378198e29ecf2704257f7b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57346779"
---
# <a name="policy-schemes-in-aspnet-core"></a><span data-ttu-id="dfd8e-103">ASP.NET Core でのポリシー設定</span><span class="sxs-lookup"><span data-stu-id="dfd8e-103">Policy schemes in ASP.NET Core</span></span>

<span data-ttu-id="dfd8e-104">ポリシーの認証スキームでは、複数のアプローチを使用して、可能性のある 1 つの論理認証方式を使用してやすいようにします。</span><span class="sxs-lookup"><span data-stu-id="dfd8e-104">Authentication policy schemes make it easier to have a single logical authentication scheme potentially use multiple approaches.</span></span> <span data-ttu-id="dfd8e-105">たとえば、ポリシー スキーム可能性がありますの課題、Google の認証と認証を使用 cookie 以外のすべての。</span><span class="sxs-lookup"><span data-stu-id="dfd8e-105">For example, a policy scheme might use Google authentication for challenges, and cookie authentication for everything else.</span></span> <span data-ttu-id="dfd8e-106">ポリシーの認証スキームを使用すると、そのように。</span><span class="sxs-lookup"><span data-stu-id="dfd8e-106">Authentication policy schemes make it:</span></span>

* <span data-ttu-id="dfd8e-107">簡単に認証操作を別の構成を転送します。</span><span class="sxs-lookup"><span data-stu-id="dfd8e-107">Easy to forward any authentication action to another scheme.</span></span>
* <span data-ttu-id="dfd8e-108">要求に基づいて動的に転送します。</span><span class="sxs-lookup"><span data-stu-id="dfd8e-108">Forward dynamically based on the request.</span></span>

<span data-ttu-id="dfd8e-109">使用して派生したすべての認証スキーム<xref:Microsoft.AspNetCore.Authentication.AuthenticationSchemeOptions>および関連付けられた[ `AuthenticationHandler<TOptions>` ](/dotnet/api/microsoft.aspnetcore.authentication.authenticationhandler-1):</span><span class="sxs-lookup"><span data-stu-id="dfd8e-109">All authentication schemes that use derived <xref:Microsoft.AspNetCore.Authentication.AuthenticationSchemeOptions> and the associated [`AuthenticationHandler<TOptions>`](/dotnet/api/microsoft.aspnetcore.authentication.authenticationhandler-1):</span></span>

* <span data-ttu-id="dfd8e-110">ASP.NET Core 2.1 以降のポリシー設定は自動的に。</span><span class="sxs-lookup"><span data-stu-id="dfd8e-110">Are automatically policy schemes in ASP.NET Core 2.1 and later.</span></span>
* <span data-ttu-id="dfd8e-111">スキームのオプションの構成を使用して有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="dfd8e-111">Can be enabled via configuring the scheme's options.</span></span>

[!code-csharp[sample](policyschemes/samples/AuthenticationSchemeOptions.cs?name=snippet)]

## <a name="examples"></a><span data-ttu-id="dfd8e-112">使用例</span><span class="sxs-lookup"><span data-stu-id="dfd8e-112">Examples</span></span>

<span data-ttu-id="dfd8e-113">次の例では、下位レベルのスキームを組み合わせてより高いレベルの体系を示します。</span><span class="sxs-lookup"><span data-stu-id="dfd8e-113">The following example shows a higher level scheme that combines lower level schemes.</span></span> <span data-ttu-id="dfd8e-114">課題、Google 認証を使用して、他のすべての cookie 認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="dfd8e-114">Google authentication is used for challenges, and cookie authentication is used for everything else:</span></span>

[!code-csharp[sample](policyschemes/samples/Startup.cs?name=snippet1)]

<span data-ttu-id="dfd8e-115">次の例で、要求ごとにパターンを動的に選択します。</span><span class="sxs-lookup"><span data-stu-id="dfd8e-115">The following example enables dynamic selection of schemes on a per request basis.</span></span> <span data-ttu-id="dfd8e-116">つまり、cookie、および API の認証を混在させる方法。</span><span class="sxs-lookup"><span data-stu-id="dfd8e-116">That is, how to mix cookies and API authentication.</span></span>

 <!-- REVIEW, missing If set in public Func<HttpContext, string> ForwardDefaultSelector -->

[!code-csharp[sample](policyschemes/samples/Startup.cs?name=snippet2)]