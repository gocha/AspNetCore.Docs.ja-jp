---
title: ASP.NET Core のリンク タグ ヘルパー
author: rick-anderson
ms.author: riande
description: ASP.NET Core リンク タグ ヘルパーの属性と、HTML リンク タグの動作拡張時の各属性の役割を示します。
ms.custom: mvc
ms.date: 09/24/2019
uid: mvc/views/tag-helpers/builtin-th/link-tag-helper
ms.openlocfilehash: e1e2e58b4ab9087e1f9de5b5c03b587feb88f1b9
ms.sourcegitcommit: fae6f0e253f9d62d8f39de5884d2ba2b4b2a6050
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2019
ms.locfileid: "71256484"
---
# <a name="link-tag-helper-in-aspnet-core"></a><span data-ttu-id="60426-103">ASP.NET Core のリンク タグ ヘルパー</span><span class="sxs-lookup"><span data-stu-id="60426-103">Link Tag Helper in ASP.NET Core</span></span>

<span data-ttu-id="60426-104">作成者: [Rick Anderson](https://twitter.com/RickAndMSFT)</span><span class="sxs-lookup"><span data-stu-id="60426-104">By [Rick Anderson](https://twitter.com/RickAndMSFT)</span></span>

<span data-ttu-id="60426-105">[リンク タグ ヘルパー](xref:Microsoft.AspNetCore.Mvc.TagHelpers.LinkTagHelper)によって、プライマリまたはフォール バック CSS ファイルへのリンクが生成されます。</span><span class="sxs-lookup"><span data-stu-id="60426-105">The [Link Tag Helper](xref:Microsoft.AspNetCore.Mvc.TagHelpers.LinkTagHelper) generates a link to a primary or fall back CSS file.</span></span> <span data-ttu-id="60426-106">通常、プライマリ CSS ファイルは [Content Delivery Network](/office365/enterprise/content-delivery-networks#what-exactly-is-a-cdn) (CDN) 上にあります。</span><span class="sxs-lookup"><span data-stu-id="60426-106">Typically the primary CSS file is on a [Content Delivery Network](/office365/enterprise/content-delivery-networks#what-exactly-is-a-cdn) (CDN).</span></span>

[!INCLUDE[](~/includes/cdn.md)]

<span data-ttu-id="60426-107">リンク タグ ヘルパーを使用すると、CSS ファイルの CDN と、CDN が使用できない場合のフォールバックを指定できます。</span><span class="sxs-lookup"><span data-stu-id="60426-107">The Link Tag Helper allows you to specify a CDN for the CSS file and a fallback when the CDN is not available.</span></span> <span data-ttu-id="60426-108">リンク タグ ヘルパーによって、ローカル ホスティングの堅牢性が CDN のパフォーマンスの利点にもたらされます。</span><span class="sxs-lookup"><span data-stu-id="60426-108">The Link Tag Helper provides the performance advantage of a CDN with the robustness of local hosting.</span></span>

<span data-ttu-id="60426-109">次の Razor マークアップでは、ASP.NET Core Web アプリ テンプレートを使用して作成されたレイアウト ファイルの `head` 要素を示します。</span><span class="sxs-lookup"><span data-stu-id="60426-109">The following Razor markup shows the `head` element of a layout file created with the ASP.NET Core web app template:</span></span>

[!code-html[](link-tag-helper/sample/_Layout.cshtml?name=snippet)]

<span data-ttu-id="60426-110">次に示すのは、前のコードからレンダリングされた HTML です (非開発環境)。</span><span class="sxs-lookup"><span data-stu-id="60426-110">The following is rendered HTML from the preceding code (in a non-Development environment):</span></span>

[!code-csharp[](link-tag-helper/sample/HtmlPage1.html)]

<span data-ttu-id="60426-111">前のコードでは、リンク タグ ヘルパーによって `<meta name="x-stylesheet-fallback-test" content="" class="sr-only" />` 要素が生成され、要求された *bootstrap.min.css* ファイルが CDN 上にあることを確認するために使用される次の JavaScript も生成されました。</span><span class="sxs-lookup"><span data-stu-id="60426-111">In the preceding code, the Link Tag Helper generated the `<meta name="x-stylesheet-fallback-test" content="" class="sr-only" />` element and the following JavaScript which is used to verify the requested *bootstrap.min.css* file is available on the CDN.</span></span> <span data-ttu-id="60426-112">このケースでは、CSS ファイルは存在しており、タグ ヘルパーによって CDN CSS ファイルを含む `<link />` 要素が生成されました。</span><span class="sxs-lookup"><span data-stu-id="60426-112">In this case, the CSS file was available so the Tag Helper generated the `<link />` element with the CDN CSS file.</span></span>

## <a name="commonly-used-link-tag-helper-attributes"></a><span data-ttu-id="60426-113">一般的に使用されるリンク タグ ヘルパー属性</span><span class="sxs-lookup"><span data-stu-id="60426-113">Commonly used Link Tag Helper attributes</span></span>

<span data-ttu-id="60426-114">リンク タグ ヘルパーのすべての属性、プロパティ、メソッドについては、[リンク タグ ヘルパー](xref:Microsoft.AspNetCore.Mvc.TagHelpers.LinkTagHelper)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="60426-114">See [Link Tag Helper](xref:Microsoft.AspNetCore.Mvc.TagHelpers.LinkTagHelper)  for all the Link Tag Helper attributes, properties, and methods.</span></span>

### <a name="href"></a><span data-ttu-id="60426-115">href</span><span class="sxs-lookup"><span data-stu-id="60426-115">href</span></span>

<span data-ttu-id="60426-116">リンクされたリソースの優先アドレス。</span><span class="sxs-lookup"><span data-stu-id="60426-116">Preferred address of the linked resource.</span></span> <span data-ttu-id="60426-117">このアドレスは、生成された HTML に常に渡されます。</span><span class="sxs-lookup"><span data-stu-id="60426-117">The address is passed thought to the generated HTML in all cases.</span></span>

### <a name="asp-fallback-href"></a><span data-ttu-id="60426-118">asp-fallback-href</span><span class="sxs-lookup"><span data-stu-id="60426-118">asp-fallback-href</span></span>

<span data-ttu-id="60426-119">プライマリ URL が失敗した場合にフォールバックする CSS スタイルシートの URL。</span><span class="sxs-lookup"><span data-stu-id="60426-119">The URL of a CSS stylesheet to fallback to in the case the primary URL fails.</span></span>

### <a name="asp-fallback-test-class"></a><span data-ttu-id="60426-120">asp-fallback-test-class</span><span class="sxs-lookup"><span data-stu-id="60426-120">asp-fallback-test-class</span></span>

<span data-ttu-id="60426-121">フォールバック テストで使用するためにスタイルシートに定義されているクラス名。</span><span class="sxs-lookup"><span data-stu-id="60426-121">The class name defined in the stylesheet to use for the fallback test.</span></span> <span data-ttu-id="60426-122">詳細については、<xref:Microsoft.AspNetCore.Mvc.TagHelpers.LinkTagHelper.FallbackTestClass> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60426-122">For more information, see <xref:Microsoft.AspNetCore.Mvc.TagHelpers.LinkTagHelper.FallbackTestClass>.</span></span>

### <a name="asp-fallback-test-property"></a><span data-ttu-id="60426-123">asp-fallback-test-property</span><span class="sxs-lookup"><span data-stu-id="60426-123">asp-fallback-test-property</span></span>

<span data-ttu-id="60426-124">フォールバック テストで使用する CSS プロパティ名。</span><span class="sxs-lookup"><span data-stu-id="60426-124">The CSS property name to use for the fallback test.</span></span> <span data-ttu-id="60426-125">詳細については、<xref:Microsoft.AspNetCore.Mvc.TagHelpers.LinkTagHelper.FallbackTestProperty> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60426-125">For more information, see <xref:Microsoft.AspNetCore.Mvc.TagHelpers.LinkTagHelper.FallbackTestProperty>.</span></span>

### <a name="asp-fallback-test-value"></a><span data-ttu-id="60426-126">asp-fallback-test-value</span><span class="sxs-lookup"><span data-stu-id="60426-126">asp-fallback-test-value</span></span>

<span data-ttu-id="60426-127">フォールバック テストで使用する CSS プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="60426-127">The CSS property value to use for the fallback test.</span></span> <span data-ttu-id="60426-128">詳細については、<xref:Microsoft.AspNetCore.Mvc.TagHelpers.LinkTagHelper.FallbackTestValue> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60426-128">For more information, see <xref:Microsoft.AspNetCore.Mvc.TagHelpers.LinkTagHelper.FallbackTestValue>.</span></span>

### <a name="asp-fallback-test-value"></a><span data-ttu-id="60426-129">asp-fallback-test-value</span><span class="sxs-lookup"><span data-stu-id="60426-129">asp-fallback-test-value</span></span>

<span data-ttu-id="60426-130">フォールバック テストで使用する CSS プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="60426-130">The CSS property value to use for the fallback test.</span></span> <span data-ttu-id="60426-131">詳細については、「<xref:Microsoft.AspNetCore.Mvc.TagHelpers.LinkTagHelper.FallbackTestValue>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60426-131">For more information, see <xref:Microsoft.AspNetCore.Mvc.TagHelpers.LinkTagHelper.FallbackTestValue></span></span>

## <a name="additional-resources"></a><span data-ttu-id="60426-132">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="60426-132">Additional resources</span></span>

* <xref:mvc/views/tag-helpers/intro>
* <xref:mvc/controllers/areas>
* <xref:razor-pages/index>
* <xref:mvc/compatibility-version>