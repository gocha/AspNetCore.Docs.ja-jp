---
title: ASP.NET Core 3.0 の新機能
author: rick-anderson
description: ASP.NET Core 3.0 の新機能について説明します。
ms.author: riande
ms.custom: mvc
ms.date: 09/23/2019
uid: aspnetcore-3.0
ms.openlocfilehash: 490d00da7282e2efe28fcc52e593dd71d7324d3f
ms.sourcegitcommit: 0365af91518004c4a44a30dc3a8ac324558a399b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2019
ms.locfileid: "71198995"
---
# <a name="whats-new-in-aspnet-core-30"></a><span data-ttu-id="435be-103">ASP.NET Core 3.0 の新機能</span><span class="sxs-lookup"><span data-stu-id="435be-103">What's new in ASP.NET Core 3.0</span></span>

<span data-ttu-id="435be-104">この記事では、ASP.NET Core 3.0 の最も大きな変更点について説明します。また、その変更点のドキュメントへのリンクも示します。</span><span class="sxs-lookup"><span data-stu-id="435be-104">This article highlights the most significant changes in ASP.NET Core 3.0 with links to relevant documentation.</span></span>

## <a name="blazor"></a><span data-ttu-id="435be-105">Blazor</span><span class="sxs-lookup"><span data-stu-id="435be-105">Blazor</span></span>

<span data-ttu-id="435be-106">Blazor は、.NET を使って対話型のクライアント側 Web UI を構築するための ASP.NET Core の新しいフレームワークです。</span><span class="sxs-lookup"><span data-stu-id="435be-106">Blazor is a new framework in ASP.NET Core for building interactive client-side web UI with .NET:</span></span>

* <span data-ttu-id="435be-107">JavaScript の代わりに C# を使って、優れた対話型 UI を作成します。</span><span class="sxs-lookup"><span data-stu-id="435be-107">Create rich interactive UIs using C# instead of JavaScript.</span></span>
* <span data-ttu-id="435be-108">.NET で記述された、サーバー側とクライアント側のアプリのロジックを共有します。</span><span class="sxs-lookup"><span data-stu-id="435be-108">Share server-side and client-side app logic written in .NET.</span></span>
* <span data-ttu-id="435be-109">モバイル ブラウザーを含めた広範なブラウザーのサポートのために、HTML および CSS として UI をレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="435be-109">Render the UI as HTML and CSS for wide browser support, including mobile browsers.</span></span>

<span data-ttu-id="435be-110">Blazor フレームワークでサポートされるシナリオ:</span><span class="sxs-lookup"><span data-stu-id="435be-110">Blazor framework supported scenarios:</span></span>

* <span data-ttu-id="435be-111">再利用可能な UI コンポーネント (Razor コンポーネント)</span><span class="sxs-lookup"><span data-stu-id="435be-111">Reusable UI components (Razor components)</span></span>
* <span data-ttu-id="435be-112">クライアント側のルーティング</span><span class="sxs-lookup"><span data-stu-id="435be-112">Client-side routing</span></span>
* <span data-ttu-id="435be-113">コンポーネントのレイアウト</span><span class="sxs-lookup"><span data-stu-id="435be-113">Component layouts</span></span>
* <span data-ttu-id="435be-114">依存関係の挿入のサポート</span><span class="sxs-lookup"><span data-stu-id="435be-114">Support for dependency injection</span></span>
* <span data-ttu-id="435be-115">フォームと検証</span><span class="sxs-lookup"><span data-stu-id="435be-115">Forms and validation</span></span>
* <span data-ttu-id="435be-116">Razor クラス ライブラリを使用したコンポーネント ライブラリの構築</span><span class="sxs-lookup"><span data-stu-id="435be-116">Build component libraries with Razor class libraries</span></span>
* <span data-ttu-id="435be-117">JavaScript 相互運用</span><span class="sxs-lookup"><span data-stu-id="435be-117">JavaScript interop</span></span>

<span data-ttu-id="435be-118">詳細については、<xref:blazor/index> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-118">For more information, see <xref:blazor/index>.</span></span>

### <a name="blazor-server"></a><span data-ttu-id="435be-119">Blazor サーバー</span><span class="sxs-lookup"><span data-stu-id="435be-119">Blazor Server</span></span>

<span data-ttu-id="435be-120">Blazor では、UI の更新プログラムを適用する方法からコンポーネントのレンダリング ロジックが分離されます。</span><span class="sxs-lookup"><span data-stu-id="435be-120">Blazor decouples component rendering logic from how UI updates are applied.</span></span> <span data-ttu-id="435be-121">Blazor サーバーでは、ASP.NET Core アプリでサーバー上の Razor コンポーネントをホストするためのサポートが提供されます。</span><span class="sxs-lookup"><span data-stu-id="435be-121">Blazor Server provides support for hosting Razor components on the server in an ASP.NET Core app.</span></span> <span data-ttu-id="435be-122">UI の更新は SignalR 接続を介して処理されます。</span><span class="sxs-lookup"><span data-stu-id="435be-122">UI updates are handled over a SignalR connection.</span></span> <span data-ttu-id="435be-123">Blazor サーバーは ASP.NET Core 3.0 でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="435be-123">Blazor Server is supported in ASP.NET Core 3.0.</span></span>

### <a name="blazor-webassembly-preview"></a><span data-ttu-id="435be-124">Blazor WebAssembly (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="435be-124">Blazor WebAssembly (Preview)</span></span>

<span data-ttu-id="435be-125">Blazor アプリは、WebAssembly ベースの .NET ランタイムを使用してブラウザーで直接実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="435be-125">Blazor apps can also be run directly in the browser using a WebAssembly-based .NET runtime.</span></span> <span data-ttu-id="435be-126">Blazor WebAssembly はプレビュー段階であり、ASP.NET Core 3.0 ではサポートされて "*いません*"。</span><span class="sxs-lookup"><span data-stu-id="435be-126">Blazor WebAssembly is in preview and *not* supported in ASP.NET Core 3.0.</span></span> <span data-ttu-id="435be-127">Blazor WebAssembly は、ASP.NET Core の今後のリリースでサポートされる予定です。</span><span class="sxs-lookup"><span data-stu-id="435be-127">Blazor WebAssembly will be supported in a future release of ASP.NET Core.</span></span>

### <a name="razor-components"></a><span data-ttu-id="435be-128">Razor のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="435be-128">Razor components</span></span>

<span data-ttu-id="435be-129">Blazor アプリはコンポーネントから構築されています。</span><span class="sxs-lookup"><span data-stu-id="435be-129">Blazor apps are built from components.</span></span> <span data-ttu-id="435be-130">コンポーネントは、ページ、ダイアログ、フォームなどのユーザー インターフェイス (UI) の自己完結型チャンクです。</span><span class="sxs-lookup"><span data-stu-id="435be-130">Components are self-contained chunks of user interface (UI), such as a page, dialog, or form.</span></span> <span data-ttu-id="435be-131">コンポーネントは、UI レンダリング ロジックとクライアント側のイベント ハンドラーを定義する通常の .NET クラスです。</span><span class="sxs-lookup"><span data-stu-id="435be-131">Components are normal .NET classes that define UI rendering logic and client-side event handlers.</span></span> <span data-ttu-id="435be-132">JavaScript を使用せずに、機能豊富な対話型 Web アプリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="435be-132">You can create rich interactive web apps without JavaScript.</span></span>

<span data-ttu-id="435be-133">通常、Blazor のコンポーネントは、HTML と C# が自然に融合している Razor 構文を使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="435be-133">Components in Blazor are typically authored using Razor syntax, a natural blend of HTML and C#.</span></span> <span data-ttu-id="435be-134">Razor コンポーネントは、両方とも Razor を使用するという点で Razor Pages および MVC ビューに似ています。</span><span class="sxs-lookup"><span data-stu-id="435be-134">Razor components are similar to Razor Pages and MVC views in that they both use Razor.</span></span> <span data-ttu-id="435be-135">要求 - 応答モデルに基づくページやビューとは異なり、コンポーネントは特に UI コンポジションを処理するために使われます。</span><span class="sxs-lookup"><span data-stu-id="435be-135">Unlike pages and views, which are based on a request-response model, components are used specifically for handling UI composition.</span></span>

## <a name="grpc"></a><span data-ttu-id="435be-136">gRPC</span><span class="sxs-lookup"><span data-stu-id="435be-136">gRPC</span></span>

<span data-ttu-id="435be-137">[gRPC](https://grpc.io/):</span><span class="sxs-lookup"><span data-stu-id="435be-137">[gRPC](https://grpc.io/):</span></span>

* <span data-ttu-id="435be-138">広く普及している高パフォーマンス RPC (リモート プロシージャ コール) フレームワークです。</span><span class="sxs-lookup"><span data-stu-id="435be-138">Is a popular, high-performance RPC (remote procedure call) framework.</span></span>
* <span data-ttu-id="435be-139">API 開発に対して独特のコントラクト優先のアプローチを提供します。</span><span class="sxs-lookup"><span data-stu-id="435be-139">Offers an opinionated contract-first approach to API development.</span></span>
* <span data-ttu-id="435be-140">次のような最新テクノロジを使用します。</span><span class="sxs-lookup"><span data-stu-id="435be-140">Uses modern technologies such as:</span></span>

  * <span data-ttu-id="435be-141">HTTP/2 (転送用)。</span><span class="sxs-lookup"><span data-stu-id="435be-141">HTTP/2 for transport.</span></span>
  * <span data-ttu-id="435be-142">プロトコル バッファー (インターフェイス記述言語として)。</span><span class="sxs-lookup"><span data-stu-id="435be-142">Protocol Buffers as the interface description language.</span></span>
  * <span data-ttu-id="435be-143">バイナリ シリアル化形式。</span><span class="sxs-lookup"><span data-stu-id="435be-143">Binary serialization format.</span></span>
* <span data-ttu-id="435be-144">次のような機能があります。</span><span class="sxs-lookup"><span data-stu-id="435be-144">Provides features such as:</span></span>

  * <span data-ttu-id="435be-145">認証</span><span class="sxs-lookup"><span data-stu-id="435be-145">Authentication</span></span>
  * <span data-ttu-id="435be-146">双方向のストリーミングおよびフロー制御。</span><span class="sxs-lookup"><span data-stu-id="435be-146">Bidirectional streaming and flow control.</span></span>
  * <span data-ttu-id="435be-147">キャンセルおよびタイムアウト。</span><span class="sxs-lookup"><span data-stu-id="435be-147">Cancellation and timeouts.</span></span>

<span data-ttu-id="435be-148">ASP.NET Core 3.0 の gRPC 機能には次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="435be-148">gRPC functionality in ASP.NET Core 3.0 includes:</span></span>

* <span data-ttu-id="435be-149">[Grpc AspNetCore](https://www.nuget.org/packages/Grpc.AspNetCore) &ndash;grpc サービスをホストするための ASP.NET Core フレームワーク。</span><span class="sxs-lookup"><span data-stu-id="435be-149">[Grpc.AspNetCore](https://www.nuget.org/packages/Grpc.AspNetCore) &ndash; An ASP.NET Core framework for hosting gRPC services.</span></span> <span data-ttu-id="435be-150">ASP.NET Core 上の gRPC は、ログ記録、依存関係の挿入 (DI)、認証、承認など、標準の ASP.NET Core 機能と完全に統合されています。</span><span class="sxs-lookup"><span data-stu-id="435be-150">gRPC on ASP.NET Core integrates with standard ASP.NET Core features like logging, dependency injection (DI), authentication and authorization.</span></span>
* <span data-ttu-id="435be-151">[Grpc.Net.Client](https://www.nuget.org/packages/Grpc.Net.Client) &ndash; 使い慣れた `HttpClient` に基づいて構築される .NET Core 用の gRPC クライアント。</span><span class="sxs-lookup"><span data-stu-id="435be-151">[Grpc.Net.Client](https://www.nuget.org/packages/Grpc.Net.Client) &ndash; A gRPC client for .NET Core that builds upon the familiar `HttpClient`.</span></span>
* <span data-ttu-id="435be-152">[Grpc.Net.ClientFactory](https://www.nuget.org/packages/Grpc.Net.ClientFactory) &ndash; `HttpClientFactory` と gRPC クライアントの統合。</span><span class="sxs-lookup"><span data-stu-id="435be-152">[Grpc.Net.ClientFactory](https://www.nuget.org/packages/Grpc.Net.ClientFactory) &ndash; gRPC client integration with `HttpClientFactory`.</span></span>

<span data-ttu-id="435be-153">詳細については、<xref:grpc/index> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-153">For more information, see <xref:grpc/index>.</span></span>

## <a name="signalr"></a><span data-ttu-id="435be-154">SignalR</span><span class="sxs-lookup"><span data-stu-id="435be-154">SignalR</span></span>

<span data-ttu-id="435be-155">移行の手順については、「[SignalR コードの更新](xref:migration/22-to-30#signalr)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-155">See [Update SignalR code](xref:migration/22-to-30#signalr) for migration instructions.</span></span> <span data-ttu-id="435be-156">現在、SignalR は `System.Text.Json` を使用して JSON メッセージのシリアル化および逆シリアル化を行います。</span><span class="sxs-lookup"><span data-stu-id="435be-156">SignalR now uses `System.Text.Json` to serialize/deserialize JSON messages.</span></span> <span data-ttu-id="435be-157">`Newtonsoft.Json` ベースのシリアライザーを復元する手順については、「[Newtonsoft.Json に切り替える](xref:migration/22-to-30#switch-to-newtonsoftjson)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-157">See [Switch to Newtonsoft.Json](xref:migration/22-to-30#switch-to-newtonsoftjson) for instructions to restore the `Newtonsoft.Json`-based serializer.</span></span>

<span data-ttu-id="435be-158">SignalR 対応の JavaScript および .NET クライアント には、自動再接続のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="435be-158">In the JavaScript and .NET Clients for SignalR, support was added for automatic reconnection.</span></span> <span data-ttu-id="435be-159">既定では、クライアントはすぐに再接続を試行し、必要に応じて 2 秒後、10 秒後、30 秒後に再試行します。</span><span class="sxs-lookup"><span data-stu-id="435be-159">By default, the client tries to reconnect immediately and retry after 2, 10, and 30 seconds if necessary.</span></span> <span data-ttu-id="435be-160">クライアントが正常に再接続すると、新しい接続 ID を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="435be-160">If the client successfully reconnects, it receives a new connection ID.</span></span> <span data-ttu-id="435be-161">自動再接続はオプトインです。</span><span class="sxs-lookup"><span data-stu-id="435be-161">Automatic reconnect is opt-in:</span></span>

```javascript
const connection = new signalR.HubConnectionBuilder()
    .withUrl("/chatHub")
    .withAutomaticReconnect()
    .build();
```

<span data-ttu-id="435be-162">再接続の間隔は、ミリ秒単位の間隔を配列で渡すことによって指定できます。</span><span class="sxs-lookup"><span data-stu-id="435be-162">The reconnection intervals can be specified by passing an array of millisecond-based durations:</span></span>

```javascript
.withAutomaticReconnect([0, 3000, 5000, 10000, 15000, 30000])
//.withAutomaticReconnect([0, 2000, 10000, 30000]) The default intervals.
```

<span data-ttu-id="435be-163">カスタム実装を渡すと、再接続間隔を完全に制御することができます。</span><span class="sxs-lookup"><span data-stu-id="435be-163">A custom implementation can be passed in for full control of the reconnection intervals.</span></span>

<span data-ttu-id="435be-164">最後の再接続間隔の後で再接続に失敗した場合:</span><span class="sxs-lookup"><span data-stu-id="435be-164">If the reconnection fails after the last reconnect interval:</span></span>

* <span data-ttu-id="435be-165">クライアントは接続がオフラインであると見なします。</span><span class="sxs-lookup"><span data-stu-id="435be-165">The client considers the connection is offline.</span></span>
* <span data-ttu-id="435be-166">クライアントは再接続の試行を停止します。</span><span class="sxs-lookup"><span data-stu-id="435be-166">The client stops trying to reconnect.</span></span>

<span data-ttu-id="435be-167">再接続の試行中に、再接続が試行されていることをユーザーに通知するようにアプリ UI を更新します。</span><span class="sxs-lookup"><span data-stu-id="435be-167">During reconnection attempts, update the app UI to notify the user that the reconnection is being attempted.</span></span>

<span data-ttu-id="435be-168">接続が中断されたときに UI にフィードバックを提供するため、次のイベント ハンドラーを含むように SignalR クライアント API が拡張されました。</span><span class="sxs-lookup"><span data-stu-id="435be-168">To provide UI feedback when the connection is interrupted, the SignalR client API has been expanded to include the following event handlers:</span></span>

* <span data-ttu-id="435be-169">`onreconnecting`:これによって、開発者が UI を無効にしたり、アプリがオフラインであることをユーザーに知らせたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="435be-169">`onreconnecting`:  Gives developers an opportunity to disable UI or to let users know the app is offline.</span></span>
* <span data-ttu-id="435be-170">`onreconnected`:これによって、接続が再確立したときに開発者が UI を更新できます。</span><span class="sxs-lookup"><span data-stu-id="435be-170">`onreconnected`: Gives developers an opportunity to update the UI once the connection is reestablished.</span></span>

<span data-ttu-id="435be-171">次のコードでは `onreconnecting` を使用して、接続の試行中に UI を更新します。</span><span class="sxs-lookup"><span data-stu-id="435be-171">The following code uses `onreconnecting` to update the UI while trying to connect:</span></span>

```javascript
connection.onreconnecting((error) => {
    const status = `Connection lost due to error "${error}". Reconnecting.`;
    document.getElementById("messageInput").disabled = true;
    document.getElementById("sendButton").disabled = true;
    document.getElementById("connectionStatus").innerText = status;
});
```

<span data-ttu-id="435be-172">次のコードでは `onreconnected` を使用して、接続時に UI を更新します。</span><span class="sxs-lookup"><span data-stu-id="435be-172">The following code uses `onreconnected` to update the UI on connection:</span></span>

```javascript
connection.onreconnected((connectionId) => {
    const status = `Connection reestablished. Connected.`;
    document.getElementById("messageInput").disabled = false;
    document.getElementById("sendButton").disabled = false;
    document.getElementById("connectionStatus").innerText = status;
});
```

<span data-ttu-id="435be-173">SignalR 3.0 以降では、ハブ メソッドが承認を必要とする場合に、承認ハンドラーにカスタム リソースが提供されます。</span><span class="sxs-lookup"><span data-stu-id="435be-173">SignalR 3.0 and later provides a custom resource to authorization handlers when a hub method requires authorization.</span></span> <span data-ttu-id="435be-174">リソースは `HubInvocationContext` のインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="435be-174">The resource is an instance of `HubInvocationContext`.</span></span> <span data-ttu-id="435be-175">`HubInvocationContext` には次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="435be-175">The `HubInvocationContext` includes the:</span></span>

* `HubCallerContext`
* <span data-ttu-id="435be-176">呼び出されているハブ メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="435be-176">Name of the hub method being invoked.</span></span>
* <span data-ttu-id="435be-177">ハブ メソッドに対する引数。</span><span class="sxs-lookup"><span data-stu-id="435be-177">Arguments to the hub method.</span></span>

<span data-ttu-id="435be-178">複数の組織が Azure Active Directory を使用してサインインできるチャット ルーム アプリの例について考えてみます。</span><span class="sxs-lookup"><span data-stu-id="435be-178">Consider the following example of a chat room app allowing multiple organization sign-in via Azure Active Directory.</span></span> <span data-ttu-id="435be-179">Microsoft アカウントを持つユーザーは誰でもサインインしてチャットできますが、ユーザーを利用禁止にしたりユーザーのチャット履歴を表示したりできるのは所有している組織のメンバーのみです。</span><span class="sxs-lookup"><span data-stu-id="435be-179">Anyone with a Microsoft account can sign in to chat, but only members of the owning organization can ban users or view users’ chat histories.</span></span> <span data-ttu-id="435be-180">アプリを使用すると、特定のユーザーに対して特定の機能を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="435be-180">The app could restrict certain functionality from specific users.</span></span>

```csharp
public class DomainRestrictedRequirement :
    AuthorizationHandler<DomainRestrictedRequirement, HubInvocationContext>,
    IAuthorizationRequirement
{
    protected override Task HandleRequirementAsync(AuthorizationHandlerContext context,
        DomainRestrictedRequirement requirement,
        HubInvocationContext resource)
    {
        if (context.User?.Identity?.Name == null)
        {
            return Task.CompletedTask;
        }

        if (IsUserAllowedToDoThis(resource.HubMethodName, context.User.Identity.Name))
        {
            context.Succeed(requirement);
        }

        return Task.CompletedTask;
    }

    private bool IsUserAllowedToDoThis(string hubMethodName, string currentUsername)
    {
        if (hubMethodName.Equals("banUser", StringComparison.OrdinalIgnoreCase))
        {
            return currentUsername.Equals("bob42@jabbr.net", StringComparison.OrdinalIgnoreCase);
        }

        return currentUsername.EndsWith("@jabbr.net", StringComparison.OrdinalIgnoreCase));
    }
}
```

<span data-ttu-id="435be-181">上記のコードでは、`DomainRestrictedRequirement` がカスタムの `IAuthorizationRequirement` として機能します。</span><span class="sxs-lookup"><span data-stu-id="435be-181">In the preceding code, `DomainRestrictedRequirement` serves as a custom `IAuthorizationRequirement`.</span></span> <span data-ttu-id="435be-182">`HubInvocationContext` リソース パラメーターが渡されているため、内部ロジックで以下を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="435be-182">Because the `HubInvocationContext` resource parameter is being passed in, the internal logic can:</span></span>

* <span data-ttu-id="435be-183">ハブが呼び出されているコンテキストを調べます。</span><span class="sxs-lookup"><span data-stu-id="435be-183">Inspect the context in which the Hub is being called.</span></span>
* <span data-ttu-id="435be-184">個々のハブ メソッドの実行をユーザーに許可するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="435be-184">Make decisions on allowing the user to execute individual Hub methods.</span></span>

<span data-ttu-id="435be-185">個々のハブ メソッドは、コードが実行時にチェックするポリシーの名前で修飾できます。</span><span class="sxs-lookup"><span data-stu-id="435be-185">Individual Hub methods can be decorated with the name of the policy the code checks at run-time.</span></span> <span data-ttu-id="435be-186">クライアントが個々のハブ メソッドを呼び出そうとすると、`DomainRestrictedRequirement` ハンドラーが実行され、メソッドへのアクセスを制御します。</span><span class="sxs-lookup"><span data-stu-id="435be-186">As clients attempt to call individual Hub methods, the `DomainRestrictedRequirement` handler runs and controls access to the methods.</span></span> <span data-ttu-id="435be-187">この方法に基づいて、`DomainRestrictedRequirement` が次のようにアクセスを制御します。</span><span class="sxs-lookup"><span data-stu-id="435be-187">Based on the way the `DomainRestrictedRequirement` controls access:</span></span>

* <span data-ttu-id="435be-188">ログインしているすべてのユーザーが `SendMessage` メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="435be-188">All logged-in users can call the `SendMessage` method.</span></span>
* <span data-ttu-id="435be-189">`@jabbr.net` 電子メール アドレスを使用してログインしたユーザーのみが、ユーザーの履歴を表示できます。</span><span class="sxs-lookup"><span data-stu-id="435be-189">Only users who have logged in with a `@jabbr.net` email address can view users’ histories.</span></span>
* <span data-ttu-id="435be-190">`bob42@jabbr.net` のみが、ユーザーをチャット ルーム利用禁止にすることができます。</span><span class="sxs-lookup"><span data-stu-id="435be-190">Only `bob42@jabbr.net` can ban users from the chat room.</span></span>

```csharp
[Authorize]
public class ChatHub : Hub
{
    public void SendMessage(string message)
    {
    }

    [Authorize("DomainRestricted")]
    public void BanUser(string username)
    {
    }

    [Authorize("DomainRestricted")]
    public void ViewUserHistory(string username)
    {
    }
}
```

<span data-ttu-id="435be-191">`DomainRestricted` ポリシーの作成には以下が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="435be-191">Creating the `DomainRestricted` policy might involve:</span></span>

* <span data-ttu-id="435be-192">*Startup.cs* に新しいポリシーを追加します。</span><span class="sxs-lookup"><span data-stu-id="435be-192">In *Startup.cs*, adding the new policy.</span></span>
* <span data-ttu-id="435be-193">カスタムの `DomainRestrictedRequirement` 要件をパラメーターとして指定します。</span><span class="sxs-lookup"><span data-stu-id="435be-193">Provide the custom `DomainRestrictedRequirement` requirement as a parameter.</span></span>
* <span data-ttu-id="435be-194">承認ミドルウェアを使用して `DomainRestricted` を登録します。</span><span class="sxs-lookup"><span data-stu-id="435be-194">Registering `DomainRestricted` with the authorization middleware.</span></span>

```csharp
services
    .AddAuthorization(options =>
    {
        options.AddPolicy("DomainRestricted", policy =>
        {
            policy.Requirements.Add(new DomainRestrictedRequirement());
        });
    });
```

<span data-ttu-id="435be-195">SignalR ハブは[エンドポイント ルーティング](xref:fundamentals/routing)を使用します。</span><span class="sxs-lookup"><span data-stu-id="435be-195">SignalR hubs use [Endpoint Routing](xref:fundamentals/routing).</span></span> <span data-ttu-id="435be-196">SignalR ハブ接続は以前は明示的に実行されました。</span><span class="sxs-lookup"><span data-stu-id="435be-196">SignalR hub connection was previously done explicitly:</span></span>

```csharp
app.UseSignalR(routes =>
{
    routes.MapHub<ChatHub>("hubs/chat");
});
```

<span data-ttu-id="435be-197">以前のバージョンでは、開発者はさまざまな場所でコントローラー、Razor ページ、およびハブを接続する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="435be-197">In the previous version, developers needed to wire up controllers, Razor pages, and hubs in a variety of different places.</span></span> <span data-ttu-id="435be-198">明示的な接続によって、ほぼ同一のルーティング セグメントがいくつも生成されます。</span><span class="sxs-lookup"><span data-stu-id="435be-198">Explicit connection results in a series of nearly-identical routing segments:</span></span>

```csharp
app.UseSignalR(routes =>
{
    routes.MapHub<ChatHub>("hubs/chat");
});

app.UseRouting(routes =>
{
    routes.MapRazorPages();
});
```

<span data-ttu-id="435be-199">SignalR 3.0 ハブは、エンドポイント ルーティングを介してルーティングできます。</span><span class="sxs-lookup"><span data-stu-id="435be-199">SignalR 3.0 hubs can be routed via endpoint routing.</span></span> <span data-ttu-id="435be-200">エンドポイント ルーティングでは、通常、すべてのルーティングを `UseRouting` に構成できます。</span><span class="sxs-lookup"><span data-stu-id="435be-200">With endpoint routing, typically all routing can be configured in `UseRouting`:</span></span>

```csharp
app.UseRouting(routes =>
{
    routes.MapRazorPages();
    routes.MapHub<ChatHub>("hubs/chat");
});
```

<span data-ttu-id="435be-201">ASP.NET Core 3.0 SignalR によって以下が追加されました。</span><span class="sxs-lookup"><span data-stu-id="435be-201">ASP.NET Core 3.0 SignalR added:</span></span>

<span data-ttu-id="435be-202">クライアントとサーバー間のストリーミング。</span><span class="sxs-lookup"><span data-stu-id="435be-202">Client-to-server streaming.</span></span> <span data-ttu-id="435be-203">クライアントとサーバー間のストリーミングでは、サーバー側メソッドが `IAsyncEnumerable<T>` または `ChannelReader<T>` のインスタンスを受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="435be-203">With client-to-server streaming, server-side methods can take instances of either an `IAsyncEnumerable<T>` or `ChannelReader<T>`.</span></span> <span data-ttu-id="435be-204">次 C# の例では、ハブの `UploadStream` メソッドがクライアントから文字列のストリームを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="435be-204">In the following C# sample, the `UploadStream` method on the Hub will receive a stream of strings from the client:</span></span>

```csharp
public async Task UploadStream(IAsyncEnumerable<string> stream)
{
    await foreach (var item in stream)
    {
        // process content
    }
}
```

<span data-ttu-id="435be-205">.NET クライアント アプリは、`IAsyncEnumerable<T>` または `ChannelReader<T>` インスタンスを、上記の `UploadStream` Hub メソッドの `stream` 引数として渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="435be-205">.NET client apps can pass either an `IAsyncEnumerable<T>` or `ChannelReader<T>` instance as the `stream` argument of the `UploadStream` Hub method above.</span></span>

<span data-ttu-id="435be-206">`for` ループが完了し、ローカル関数が終了した後で、ストリームの完了が送信されます。</span><span class="sxs-lookup"><span data-stu-id="435be-206">After the `for` loop has completed and the local function exits, the stream completion is sent:</span></span>

```csharp
async IAsyncEnumerable<string> clientStreamData()
{
    for (var i = 0; i < 5; i++)
    {
        var data = await FetchSomeData();
        yield return data;
    }
}

await connection.SendAsync("UploadStream", clientStreamData());
```

<span data-ttu-id="435be-207">JavaScript クライアント アプリは、上記の `UploadStream` ハブの `stream`引数のために SignalR `Subject` (または [RxJS Subject](https://rxjs.dev/api/index/class/Subject)) を使用します。</span><span class="sxs-lookup"><span data-stu-id="435be-207">JavaScript client apps use the SignalR `Subject` (or an [RxJS Subject](https://rxjs.dev/api/index/class/Subject)) for the `stream` argument of the `UploadStream` Hub method above.</span></span>

```javascript
let subject = new signalR.Subject();
await connection.send("StartStream", "MyAsciiArtStream", subject);
```

<span data-ttu-id="435be-208">JavaScript コードで `subject.next` メソッドを使用すると、文字列がキャプチャされてからサーバーへの送信準備が整うように文字列を処理できます。</span><span class="sxs-lookup"><span data-stu-id="435be-208">The JavaScript code could use the `subject.next` method to handle strings as they are captured and ready to be sent to the server.</span></span>

```javascript
subject.next("example");
subject.complete();
```

<span data-ttu-id="435be-209">直前の 2 つのスニペットのようなコードを使用して、リアルタイム ストリーミング エクスペリエンスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="435be-209">Using code like the two preceding snippets, real-time streaming experiences can be created.</span></span>

### <a name="new-json-serialization"></a><span data-ttu-id="435be-210">新しい JSON シリアル化</span><span class="sxs-lookup"><span data-stu-id="435be-210">New JSON serialization</span></span>

<span data-ttu-id="435be-211">現在、ASP.NET Core 3.0 では、JSON シリアル化のために既定で <xref:System.Text.Json> が使用されます。</span><span class="sxs-lookup"><span data-stu-id="435be-211">ASP.NET Core 3.0 now uses <xref:System.Text.Json> by default for JSON serialization:</span></span>

* <span data-ttu-id="435be-212">非同期で JSON の読み取りと書き込みを行います。</span><span class="sxs-lookup"><span data-stu-id="435be-212">Reads and writes JSON asynchronously.</span></span>
* <span data-ttu-id="435be-213">UTF-8 テキスト用に最適化されています。</span><span class="sxs-lookup"><span data-stu-id="435be-213">Is optimized for UTF-8 text.</span></span>
* <span data-ttu-id="435be-214">通常、`Newtonsoft.Json` よりパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="435be-214">Typically higher performance than `Newtonsoft.Json`.</span></span>

<span data-ttu-id="435be-215">Json.NET を ASP.NET Core 3.0 に追加するには、「[Newtonsoft.Json ベースの JSON 形式のサポートを追加する](xref:web-api/advanced/formatting#add-newtonsoftjson-based-json-format-support)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-215">To add Json.NET to ASP.NET Core 3.0, see [Add Newtonsoft.Json-based JSON format support](xref:web-api/advanced/formatting#add-newtonsoftjson-based-json-format-support).</span></span>

## <a name="new-razor-directives"></a><span data-ttu-id="435be-216">新しい Razor ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="435be-216">New Razor directives</span></span>

<span data-ttu-id="435be-217">次の一覧には、新しい Razor ディレクティブが含まれます。</span><span class="sxs-lookup"><span data-stu-id="435be-217">The following list contains new Razor directives:</span></span>

* <span data-ttu-id="435be-218">[@attribute](xref:mvc/views/razor#attribute) &ndash; `@attribute` ディレクティブでは、指定された属性が生成されたページまたはビューのクラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="435be-218">[@attribute](xref:mvc/views/razor#attribute) &ndash; The `@attribute` directive applies the given attribute to the class of the generated page or view.</span></span> <span data-ttu-id="435be-219">たとえば、`@attribute [Authorize]` のようにします。</span><span class="sxs-lookup"><span data-stu-id="435be-219">For example, `@attribute [Authorize]`.</span></span>
* <span data-ttu-id="435be-220">[@implements](xref:mvc/views/razor#implements) &ndash; `@implements` ディレクティブでは、生成されたクラスのインターフェイスが実装されます。</span><span class="sxs-lookup"><span data-stu-id="435be-220">[@implements](xref:mvc/views/razor#implements) &ndash; The `@implements` directive implements an interface for the generated class.</span></span> <span data-ttu-id="435be-221">たとえば、`@implements IDisposable` のようにします。</span><span class="sxs-lookup"><span data-stu-id="435be-221">For example, `@implements IDisposable`.</span></span>

## <a name="certificate-and-kerberos-authentication"></a><span data-ttu-id="435be-222">証明書および Kerberos 認証</span><span class="sxs-lookup"><span data-stu-id="435be-222">Certificate and Kerberos authentication</span></span>

<span data-ttu-id="435be-223">証明書認証には以下が必要です。</span><span class="sxs-lookup"><span data-stu-id="435be-223">Certificate authentication requires:</span></span>

* <span data-ttu-id="435be-224">証明書を受け入れるようにサーバーを構成します。</span><span class="sxs-lookup"><span data-stu-id="435be-224">Configuring the server to accept certificates.</span></span>
* <span data-ttu-id="435be-225">`Startup.Configure` に認証ミドルウェアを追加します。</span><span class="sxs-lookup"><span data-stu-id="435be-225">Adding the authentication middleware in `Startup.Configure`.</span></span>
* <span data-ttu-id="435be-226">`Startup.ConfigureServices` に証明書認証サービスを追加します。</span><span class="sxs-lookup"><span data-stu-id="435be-226">Adding the certificate authentication service in `Startup.ConfigureServices`.</span></span>

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddAuthentication(
        CertificateAuthenticationDefaults.AuthenticationScheme)
            .AddCertificate();
    // Other service configuration removed.
}

public void Configure(IApplicationBuilder app, IHostingEnvironment env)
{
    app.UseAuthentication();
    // Other app configuration removed.
}
```

<span data-ttu-id="435be-227">証明書認証のオプションには次の機能が含まれます。</span><span class="sxs-lookup"><span data-stu-id="435be-227">Options for certificate authentication include the ability to:</span></span>

* <span data-ttu-id="435be-228">自己署名された証明書を受け入れる。</span><span class="sxs-lookup"><span data-stu-id="435be-228">Accept self-signed certificates.</span></span>
* <span data-ttu-id="435be-229">証明書の失効を確認する。</span><span class="sxs-lookup"><span data-stu-id="435be-229">Check for certificate revocation.</span></span>
* <span data-ttu-id="435be-230">提供された証明書に適切な使用フラグが含まれていることを確認する。</span><span class="sxs-lookup"><span data-stu-id="435be-230">Check that the proffered certificate has the right usage flags in it.</span></span>

<span data-ttu-id="435be-231">既定のユーザー プリンシパルは、証明書のプロパティで構成されます。</span><span class="sxs-lookup"><span data-stu-id="435be-231">A default user principal is constructed from the certificate properties.</span></span> <span data-ttu-id="435be-232">ユーザー プリンシパルには、プリンシパルの補完または置換を可能にするイベントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="435be-232">The user principal contains an event that enables supplementing or replacing the principal.</span></span> <span data-ttu-id="435be-233">詳細については、<xref:security/authentication/certauth> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-233">For more information, see <xref:security/authentication/certauth>.</span></span>

<span data-ttu-id="435be-234">[Windows 認証](/windows-server/security/windows-authentication/windows-authentication-overview)は、Linux および macOS に拡張されています。</span><span class="sxs-lookup"><span data-stu-id="435be-234">[Windows Authentication](/windows-server/security/windows-authentication/windows-authentication-overview) has been extended onto Linux and macOS.</span></span> <span data-ttu-id="435be-235">以前のバージョンでは、Windows 認証は [IIS](xref:host-and-deploy/iis/index) と [HttpSys](xref:fundamentals/servers/httpsys) に限定されていました。</span><span class="sxs-lookup"><span data-stu-id="435be-235">In previous versions, Windows Authentication was limited to [IIS](xref:host-and-deploy/iis/index) and [HttpSys](xref:fundamentals/servers/httpsys).</span></span> <span data-ttu-id="435be-236">ASP.NET Core 3.0 では、[Kestrel](xref:fundamentals/servers/kestrel) は、Windows、Linux、および macOS 上で、Windows ドメインに参加しているホストに対して Negotiate、[Kerberos](/windows-server/security/kerberos/kerberos-authentication-overview)、および [NTLM](/windows-server/security/kerberos/ntlm-overview) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="435be-236">In ASP.NET Core 3.0, [Kestrel](xref:fundamentals/servers/kestrel) has the ability to use Negotiate, [Kerberos](/windows-server/security/kerberos/kerberos-authentication-overview), and [NTLM on Windows](/windows-server/security/kerberos/ntlm-overview), Linux, and macOS for Windows domain-joined hosts.</span></span> <span data-ttu-id="435be-237">これらの認証スキームの Kestrel サポートは、[Microsoft.AspNetCore.Authentication.Negotiate NuGet](https://www.nuget.org/packages/Microsoft.AspNetCore.Authentication.Negotiate) パッケージによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="435be-237">Kestrel support of these authentication schemes is provided by the [Microsoft.AspNetCore.Authentication.Negotiate NuGet](https://www.nuget.org/packages/Microsoft.AspNetCore.Authentication.Negotiate) package.</span></span> <span data-ttu-id="435be-238">他の認証サービスと同様に、認証アプリ全体を構成してからサービスを構成します。</span><span class="sxs-lookup"><span data-stu-id="435be-238">As with the other authentication services, configure authentication app wide, then configure the service:</span></span>

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddAuthentication(NegotiateDefaults.AuthenticationScheme)
        .AddNegotiate();
    // Other service configuration removed.
}

public void Configure(IApplicationBuilder app, IHostingEnvironment env)
{
    app.UseAuthentication();
    // Other app configuration removed.
}
```

<span data-ttu-id="435be-239">ホストの要件:</span><span class="sxs-lookup"><span data-stu-id="435be-239">Host requirements:</span></span>

* <span data-ttu-id="435be-240">Windows ホストでは、アプリをホストするユーザー アカウントに[サービス プリンシパル名](/windows/win32/ad/service-principal-names) (SPN) を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="435be-240">Windows hosts must have [Service Principal Names](/windows/win32/ad/service-principal-names) (SPNs) added to the user account hosting the app.</span></span>
* <span data-ttu-id="435be-241">Linux および macOS マシンは、ドメインに参加している必要があります。</span><span class="sxs-lookup"><span data-stu-id="435be-241">Linux and macOS machines must be joined to the domain.</span></span>
  * <span data-ttu-id="435be-242">Web プロセス用に SPN を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="435be-242">SPNs must be created for the web process.</span></span>
  * <span data-ttu-id="435be-243">[キータブ ファイル](https://blogs.technet.microsoft.com/pie/2018/01/03/all-you-need-to-know-about-keytab-files/)をホスト マシン上で生成して構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="435be-243">[Keytab files](https://blogs.technet.microsoft.com/pie/2018/01/03/all-you-need-to-know-about-keytab-files/) must be generated and configured on the host machine.</span></span>

<span data-ttu-id="435be-244">詳細については、<xref:security/authentication/windowsauth> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-244">For more information, see <xref:security/authentication/windowsauth>.</span></span>

## <a name="template-changes"></a><span data-ttu-id="435be-245">テンプレートの変更</span><span class="sxs-lookup"><span data-stu-id="435be-245">Template changes</span></span>

<span data-ttu-id="435be-246">Web UI テンプレート (Razor Pages、コントローラーとビューを含む MVC) では、以下が削除されています。</span><span class="sxs-lookup"><span data-stu-id="435be-246">The web UI templates (Razor Pages, MVC with controller and views) have the following removed:</span></span>

* <span data-ttu-id="435be-247">Cookie 同意 UI は含まれなくなりました。</span><span class="sxs-lookup"><span data-stu-id="435be-247">The cookie consent UI is no longer included.</span></span> <span data-ttu-id="435be-248">ASP.NET Core 3.0 テンプレートで生成されるアプリで Cookie 同意機能を有効にするには、<xref:security/gdpr> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-248">To enable the cookie consent feature in an ASP.NET Core 3.0 template generated app, see <xref:security/gdpr>.</span></span>
* <span data-ttu-id="435be-249">スクリプトと関連する静的アセットは、CDN を使用する代わりに、ローカル ファイルとして参照されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="435be-249">Scripts and related static assets are now referenced as local files instead of using CDNs.</span></span> <span data-ttu-id="435be-250">詳細については、「[現在、スクリプトと関連する静的アセットは、現在の環境に基づいた CDN を使用する代わりに、ローカル ファイルとして参照される (aspnet/AspNetCore.Docs #14350)](https://github.com/aspnet/AspNetCore.Docs/issues/14350)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-250">For more information, see [Scripts and related static assets are now referenced as local files instead of using CDNs based on the current environment (aspnet/AspNetCore.Docs #14350)](https://github.com/aspnet/AspNetCore.Docs/issues/14350).</span></span>

<span data-ttu-id="435be-251">Angular テンプレートは、Angular 8 を使用するように更新されました。</span><span class="sxs-lookup"><span data-stu-id="435be-251">The Angular template updated to use Angular 8.</span></span>

<span data-ttu-id="435be-252">Razor クラス ライブラリ (RCL) テンプレートは Razor コンポーネント開発での既定です。</span><span class="sxs-lookup"><span data-stu-id="435be-252">The Razor class library (RCL) template defaults to Razor component development by default.</span></span> <span data-ttu-id="435be-253">Visual Studio の新しいテンプレート オプションによって、ページとビューのテンプレート サポートが提供されます。</span><span class="sxs-lookup"><span data-stu-id="435be-253">A new template option in Visual Studio provides template support for pages and views.</span></span> <span data-ttu-id="435be-254">コマンド シェルでテンプレートから RCL を作成するときは、`-support-pages-and-views` オプション (`dotnet new razorclasslib -support-pages-and-views`) を渡します。</span><span class="sxs-lookup"><span data-stu-id="435be-254">When creating an RCL from the template in a command shell, pass the `-support-pages-and-views` option (`dotnet new razorclasslib -support-pages-and-views`).</span></span>

## <a name="generic-host"></a><span data-ttu-id="435be-255">汎用ホスト</span><span class="sxs-lookup"><span data-stu-id="435be-255">Generic Host</span></span>

<span data-ttu-id="435be-256">ASP.NET Core 3.0 テンプレートでは <xref:fundamentals/host/generic-host> が使用されます。</span><span class="sxs-lookup"><span data-stu-id="435be-256">The ASP.NET Core 3.0 templates use <xref:fundamentals/host/generic-host>.</span></span> <span data-ttu-id="435be-257">以前のバージョンでは <xref:Microsoft.AspNetCore.Hosting.WebHostBuilder> が使用されていました。</span><span class="sxs-lookup"><span data-stu-id="435be-257">Previous versions used <xref:Microsoft.AspNetCore.Hosting.WebHostBuilder>.</span></span> <span data-ttu-id="435be-258">.NET Core 汎用ホスト (<xref:Microsoft.Extensions.Hosting.HostBuilder>) を使用すると、ASP.NET Core アプリと、Web 固有ではない他のサーバー シナリオの統合が強化されます。</span><span class="sxs-lookup"><span data-stu-id="435be-258">Using the .NET Core Generic Host (<xref:Microsoft.Extensions.Hosting.HostBuilder>) provides better integration of ASP.NET Core apps with other server scenarios that are not web specific.</span></span> <span data-ttu-id="435be-259">詳細については、「[HostBuilder による WebHostBuilder の置き換え](xref:migration/22-to-30?view=aspnetcore-2.2#hostbuilder-replaces-webhostbuilder)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-259">For more information, see [HostBuilder replaces WebHostBuilder](xref:migration/22-to-30?view=aspnetcore-2.2#hostbuilder-replaces-webhostbuilder).</span></span>

### <a name="host-configuration"></a><span data-ttu-id="435be-260">ホストの構成</span><span class="sxs-lookup"><span data-stu-id="435be-260">Host configuration</span></span>

<span data-ttu-id="435be-261">ASP.NET Core 3.0 リリースよりも前には、`ASPNETCORE_` というプレフィックスが付いた環境変数が Web ホストのホスト構成用に読み込まれました。</span><span class="sxs-lookup"><span data-stu-id="435be-261">Prior to the release of ASP.NET Core 3.0, environment variables prefixed with `ASPNETCORE_` were loaded for host configuration of the Web Host.</span></span> <span data-ttu-id="435be-262">3\.0 では、`AddEnvironmentVariables` が使用され、`DOTNET_` というプレフィックスが付いた環境変数が `CreateDefaultBuilder` でのホスト構成用に読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="435be-262">In 3.0, `AddEnvironmentVariables` is used to load environment variables prefixed with `DOTNET_` for host configuration with `CreateDefaultBuilder`.</span></span>

### <a name="changes-to-startup-contructor-injection"></a><span data-ttu-id="435be-263">Startup コンストラクター挿入の変更</span><span class="sxs-lookup"><span data-stu-id="435be-263">Changes to Startup contructor injection</span></span>

<span data-ttu-id="435be-264">汎用ホストでは、`Startup` コンストラクター挿入で次の型しかサポートされません。</span><span class="sxs-lookup"><span data-stu-id="435be-264">The Generic Host only supports the following types for `Startup` constructor injection:</span></span>

* <xref:Microsoft.Extensions.Hosting.IHostEnvironment>
* `IWebHostEnvironment`
* <xref:Microsoft.Extensions.Configuration.IConfiguration>

<span data-ttu-id="435be-265">すべてのサービスを `Startup.Configure` メソッドへの引数として直接挿入することは引き続きできます。</span><span class="sxs-lookup"><span data-stu-id="435be-265">All services can still be injected directly as arguments to the `Startup.Configure` method.</span></span> <span data-ttu-id="435be-266">詳細については、「[汎用ホストによる Startup コンストラクター挿入の制限 (aspnet/Announcements #353)](https://github.com/aspnet/Announcements/issues/353)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-266">For more information, see [Generic Host restricts Startup constructor injection (aspnet/Announcements #353)](https://github.com/aspnet/Announcements/issues/353).</span></span>

## <a name="kestrel"></a><span data-ttu-id="435be-267">Kestrel</span><span class="sxs-lookup"><span data-stu-id="435be-267">Kestrel</span></span>

* <span data-ttu-id="435be-268">Kestrel 構成は、汎用ホストへの移行に対応するように更新されました。</span><span class="sxs-lookup"><span data-stu-id="435be-268">Kestrel configuration has been updated for the migration to the Generic Host.</span></span> <span data-ttu-id="435be-269">3\.0 では、Kestrel は `ConfigureWebHostDefaults` によって提供される Web ホスト ビルダー上で構成されます。</span><span class="sxs-lookup"><span data-stu-id="435be-269">In 3.0, Kestrel is configured on the web host builder provided by `ConfigureWebHostDefaults`.</span></span>
* <span data-ttu-id="435be-270">接続アダプターは Kestrel から削除され、接続ミドルウェアで置き換えられました。これは ASP.NET Core パイプラインの HTTP ミドルウェアに似ていますが下位レベルの接続用です。</span><span class="sxs-lookup"><span data-stu-id="435be-270">Connection Adapters have been removed from Kestrel and replaced with Connection Middleware, which is similar to HTTP Middleware in the ASP.NET Core pipeline but for lower-level connections.</span></span>
* <span data-ttu-id="435be-271">Kestrel トランスポート層は、`Connections.Abstractions` のパブリック インターフェイスとして公開されています。</span><span class="sxs-lookup"><span data-stu-id="435be-271">The Kestrel transport layer has been exposed as a public interface in `Connections.Abstractions`.</span></span>
* <span data-ttu-id="435be-272">ヘッダーとトレーラーのあいまいさは、末尾のヘッダーを新しいコレクションに移動することによって解決されました。</span><span class="sxs-lookup"><span data-stu-id="435be-272">Ambiguity between headers and trailers has been resolved by moving trailing headers to a new collection.</span></span>
* <span data-ttu-id="435be-273">同期 IO の API (`HttpReqeuest.Body.Read` など) は、アプリのクラッシュにつながるスレッド スタベーションの一般的な原因です。</span><span class="sxs-lookup"><span data-stu-id="435be-273">Synchronous IO APIs, such as `HttpReqeuest.Body.Read`, are a common source of thread starvation leading to app crashes.</span></span> <span data-ttu-id="435be-274">3\.0 では、`AllowSynchronousIO` は既定で無効になっています。</span><span class="sxs-lookup"><span data-stu-id="435be-274">In 3.0, `AllowSynchronousIO` is disabled by default.</span></span>

<span data-ttu-id="435be-275">詳細については、<xref:migration/22-to-30#kestrel> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-275">For more information, see <xref:migration/22-to-30#kestrel>.</span></span>

## <a name="http2-enabled-by-default"></a><span data-ttu-id="435be-276">既定で有効な HTTP/2</span><span class="sxs-lookup"><span data-stu-id="435be-276">HTTP/2 enabled by default</span></span>

<span data-ttu-id="435be-277">HTTP/2 は、Kestrel では HTTPS エンドポイントに対して既定で有効です。</span><span class="sxs-lookup"><span data-stu-id="435be-277">HTTP/2 is enabled by default in Kestrel for HTTPS endpoints.</span></span> <span data-ttu-id="435be-278">IIS または HTTP.sys での HTTP/2 サポートは、オペレーティング システムでサポートされる場合に有効です。</span><span class="sxs-lookup"><span data-stu-id="435be-278">HTTP/2 support for IIS or HTTP.sys is enabled when supported by the operating system.</span></span>

## <a name="request-counters"></a><span data-ttu-id="435be-279">要求カウンター</span><span class="sxs-lookup"><span data-stu-id="435be-279">Request counters</span></span>

<span data-ttu-id="435be-280">ホスティング EventSource (Microsoft.AspNetCore.Hosting) は、受信要求に関連する次の EventCounter を出力します。</span><span class="sxs-lookup"><span data-stu-id="435be-280">The Hosting EventSource (Microsoft.AspNetCore.Hosting) emits the following EventCounters related to incoming requests:</span></span>

* `requests-per-second`
* `total-requests`
* `current-requests`
* `failed-requests`

## <a name="endpoint-routing"></a><span data-ttu-id="435be-281">エンドポイント ルーティング</span><span class="sxs-lookup"><span data-stu-id="435be-281">Endpoint routing</span></span>

<span data-ttu-id="435be-282">エンドポイント ルーティングによってフレームワーク (MVC など) がミドルウェアとうまく連携できるようになりますが、これが次のように強化されています。</span><span class="sxs-lookup"><span data-stu-id="435be-282">Endpoint Routing, which allows frameworks (for example, MVC) to work well with middleware, is enhanced:</span></span>

* <span data-ttu-id="435be-283">ミドルウェアとエンドポイントの順序を `Startup.Configure` の要求処理パイプラインで構成できます。</span><span class="sxs-lookup"><span data-stu-id="435be-283">The order of middleware and endpoints is configurable in the request processing pipeline of `Startup.Configure`.</span></span>
* <span data-ttu-id="435be-284">エンドポイントとミドルウェアは、正常性チェックなどの他の ASP.NET Core ベースのテクノロジに対して適切に構成できます。</span><span class="sxs-lookup"><span data-stu-id="435be-284">Endpoints and middleware compose well with other ASP.NET Core-based technologies, such as Health Checks.</span></span>
* <span data-ttu-id="435be-285">エンドポイントは、ミドルウェアと MVC の両方に、CORS や承認などのポリシーを実装できます。</span><span class="sxs-lookup"><span data-stu-id="435be-285">Endpoints can implement a policy, such as CORS or authorization, in both middleware and MVC.</span></span>
* <span data-ttu-id="435be-286">フィルターおよび属性をコントローラーのメソッドに設定できます。</span><span class="sxs-lookup"><span data-stu-id="435be-286">Filters and attributes can be placed on methods in controllers.</span></span>

<span data-ttu-id="435be-287">詳細については、<xref:fundamentals/routing#routing-basics> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-287">For more information, see <xref:fundamentals/routing#routing-basics>.</span></span>

## <a name="health-checks"></a><span data-ttu-id="435be-288">正常性チェック</span><span class="sxs-lookup"><span data-stu-id="435be-288">Health Checks</span></span>

<span data-ttu-id="435be-289">正常性チェックでは、汎用ホストとのエンドポイント ルーティングを使用します。</span><span class="sxs-lookup"><span data-stu-id="435be-289">Health Checks use endpoint routing with the Generic Host.</span></span> <span data-ttu-id="435be-290">`Startup.Configure` で、エンドポイントの URL または相対パスを使用して、エンドポイント ビルダーで `MapHealthChecks` を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="435be-290">In `Startup.Configure`, call `MapHealthChecks` on the endpoint builder with the endpoint URL or relative path:</span></span>

```csharp
app.UseEndpoints(endpoints =>
{
    endpoints.MapHealthChecks("/health");
});
```

<span data-ttu-id="435be-291">正常性チェックのエンドポイントは以下を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="435be-291">Health Checks endpoints can:</span></span>

* <span data-ttu-id="435be-292">1 つまたは複数の許可されたホスト/ポートを指定する。</span><span class="sxs-lookup"><span data-stu-id="435be-292">Specify one or more permitted hosts/ports.</span></span>
* <span data-ttu-id="435be-293">承認を必要とする。</span><span class="sxs-lookup"><span data-stu-id="435be-293">Require authorization.</span></span>
* <span data-ttu-id="435be-294">CORS を必要とする。</span><span class="sxs-lookup"><span data-stu-id="435be-294">Require CORS.</span></span>

<span data-ttu-id="435be-295">詳細については、次の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-295">For more information, see the following articles:</span></span>

* <xref:migration/22-to-30#health-checks>
* <xref:host-and-deploy/health-checks>

## <a name="pipes-on-httpcontext"></a><span data-ttu-id="435be-296">HttpContext のパイプ</span><span class="sxs-lookup"><span data-stu-id="435be-296">Pipes on HttpContext</span></span>

<span data-ttu-id="435be-297">現在、<xref:System.IO.Pipelines> API を使用して、要求本文の読み取りと応答本文の書き込みを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="435be-297">It's now possible to read the request body and write the response body using the <xref:System.IO.Pipelines> API.</span></span> <span data-ttu-id="435be-298">次に、</span><span class="sxs-lookup"><span data-stu-id="435be-298">The</span></span> <!-- <xref:Microsoft.AspNetCore.Http.HttpRequest.BodyReader> --> <span data-ttu-id="435be-299">`HttpRequest.BodyReader` プロパティは、要求本文を読み取るために使用できる <xref:System.IO.Pipelines.PipeReader> を提供します。</span><span class="sxs-lookup"><span data-stu-id="435be-299">`HttpRequest.BodyReader` property provides a <xref:System.IO.Pipelines.PipeReader> that can be used to read the request body.</span></span> <span data-ttu-id="435be-300">次に、</span><span class="sxs-lookup"><span data-stu-id="435be-300">The</span></span> <!-- <xref:Microsoft.AspNetCore.Http.> --> <span data-ttu-id="435be-301">`HttpResponse.BodyWriter` プロパティは、応答本文を書き込むために使用できる <xref:System.IO.Pipelines.PipeWriter> を提供します。</span><span class="sxs-lookup"><span data-stu-id="435be-301">`HttpResponse.BodyWriter` property provides a <xref:System.IO.Pipelines.PipeWriter> that can be used to write the response body.</span></span> <span data-ttu-id="435be-302">`HttpRequest.BodyReader` は、`HttpRequest.Body` ストリームに類似しています。</span><span class="sxs-lookup"><span data-stu-id="435be-302">`HttpRequest.BodyReader` is an analogue of the `HttpRequest.Body` stream.</span></span> <span data-ttu-id="435be-303">`HttpResponse.BodyWriter` は `HttpResponse.Body` ストリームに類似しています。</span><span class="sxs-lookup"><span data-stu-id="435be-303">`HttpResponse.BodyWriter` is an analogue of the `HttpResponse.Body` stream.</span></span>

<!-- indirectly related, https://github.com/dotnet/docs/pull/14414 won't be published by 9/23  -->

## <a name="improved-error-reporting-in-iis"></a><span data-ttu-id="435be-304">IIS でのエラー報告の向上</span><span class="sxs-lookup"><span data-stu-id="435be-304">Improved error reporting in IIS</span></span>

<span data-ttu-id="435be-305">IIS で ASP.NET Core アプリをホストする際の起動エラーで生成される診断データが豊富になりました。</span><span class="sxs-lookup"><span data-stu-id="435be-305">Startup errors when hosting ASP.NET Core apps in IIS now produce richer diagnostic data.</span></span> <span data-ttu-id="435be-306">これらのエラーは、該当する場合は常にスタック トレースと共に Windows イベント ログに報告されます。</span><span class="sxs-lookup"><span data-stu-id="435be-306">These errors are reported to the Windows Event Log with stack traces wherever applicable.</span></span> <span data-ttu-id="435be-307">さらに、すべての警告、エラー、および未処理の例外が、Windows イベント ログに記録されます。</span><span class="sxs-lookup"><span data-stu-id="435be-307">In addition, all warnings, errors, and unhandled exceptions are logged to the Windows Event Log.</span></span>

## <a name="worker-service-and-worker-sdk"></a><span data-ttu-id="435be-308">ワーカー サービスとワーカー SDK</span><span class="sxs-lookup"><span data-stu-id="435be-308">Worker Service and Worker SDK</span></span>

<span data-ttu-id="435be-309">.NET Core 3.0 では、新しいワーカー サービス アプリ テンプレートが導入されました。</span><span class="sxs-lookup"><span data-stu-id="435be-309">.NET Core 3.0 introduces the new Worker Service app template.</span></span> <span data-ttu-id="435be-310">このテンプレートは、.NET Core で長期サービスを作成する場合の出発点として利用できます。</span><span class="sxs-lookup"><span data-stu-id="435be-310">This template is provides a starting point for writing long running services in .NET Core.</span></span>

<span data-ttu-id="435be-311">詳細については次を参照してください:</span><span class="sxs-lookup"><span data-stu-id="435be-311">For more information, see:</span></span>

* [<span data-ttu-id="435be-312">Windows サービスとしての .NET Core ワーカー</span><span class="sxs-lookup"><span data-stu-id="435be-312">.NET Core Workers as Windows Services</span></span>](https://devblogs.microsoft.com/aspnet/net-core-workers-as-windows-services/)
* <xref:fundamentals/host/hosted-services>
* <xref:host-and-deploy/windows-service>

## <a name="forwarded-headers-middleware-improvements"></a><span data-ttu-id="435be-313">Forwarded Headers Middleware の機能強化</span><span class="sxs-lookup"><span data-stu-id="435be-313">Forwarded Headers Middleware improvements</span></span>

<span data-ttu-id="435be-314">ASP.NET Core の以前のバージョンでは、Azure Linux にデプロイした場合、または IIS 以外のリバース プロキシの背後にデプロイした場合に、<xref:Microsoft.AspNetCore.Builder.HstsBuilderExtensions.UseHsts*> と <xref:Microsoft.AspNetCore.Builder.HttpsPolicyBuilderExtensions.UseHttpsRedirection*> の呼び出しで問題が発生していました。</span><span class="sxs-lookup"><span data-stu-id="435be-314">In previous versions of ASP.NET Core, calling <xref:Microsoft.AspNetCore.Builder.HstsBuilderExtensions.UseHsts*> and  <xref:Microsoft.AspNetCore.Builder.HttpsPolicyBuilderExtensions.UseHttpsRedirection*> were problematic when deployed to an Azure Linux or behind any reverse proxy other than IIS.</span></span> <span data-ttu-id="435be-315">以前のバージョンの修正方法は、「[Linux および非 IIS のリバース プロキシのスキームを転送する](xref:host-and-deploy/proxy-load-balancer#forward-the-scheme-for-linux-and-non-iis-reverse-proxies)」に記載されてます。</span><span class="sxs-lookup"><span data-stu-id="435be-315">The fix for previous versions is documented in [Forward the scheme for Linux and non-IIS reverse proxies](xref:host-and-deploy/proxy-load-balancer#forward-the-scheme-for-linux-and-non-iis-reverse-proxies).</span></span>

<span data-ttu-id="435be-316">このシナリオは ASP.NET Core 3.0 では修正されています。</span><span class="sxs-lookup"><span data-stu-id="435be-316">This scenario is fixed in ASP.NET Core 3.0.</span></span> <span data-ttu-id="435be-317">ホストによって [Forwarded Headers Middleware](xref:host-and-deploy/proxy-load-balancer#forwarded-headers-middleware-options) が有効化されるのは、`ASPNETCORE_FORWARDEDHEADERS_ENABLED` 環境変数が `true` に設定されているときです。</span><span class="sxs-lookup"><span data-stu-id="435be-317">The host enables the [Forwarded Headers Middleware](xref:host-and-deploy/proxy-load-balancer#forwarded-headers-middleware-options) when the `ASPNETCORE_FORWARDEDHEADERS_ENABLED` environment variable is set to `true`.</span></span> <span data-ttu-id="435be-318">`ASPNETCORE_FORWARDEDHEADERS_ENABLED` はコンテナー イメージで `true` に設定されています。</span><span class="sxs-lookup"><span data-stu-id="435be-318">`ASPNETCORE_FORWARDEDHEADERS_ENABLED` is set to `true` in our container images.</span></span>

## <a name="performance-improvements"></a><span data-ttu-id="435be-319">パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="435be-319">Performance improvements</span></span>

<span data-ttu-id="435be-320">ASP.NET Core 3.0 には、メモリ使用量を減らしてスループットを向上させる多くの機能強化が含まれています。</span><span class="sxs-lookup"><span data-stu-id="435be-320">ASP.NET Core 3.0 includes many improvements that reduce memory usage and improve throughput:</span></span>

* <span data-ttu-id="435be-321">スコープ サービスで組み込み依存関係挿入コンテナーを使用する場合のメモリ使用量の削減。</span><span class="sxs-lookup"><span data-stu-id="435be-321">Reduction in memory usage when using the built-in dependency injection container for scoped services.</span></span>
* <span data-ttu-id="435be-322">ミドルウェアのシナリオやルーティングを含む、フレームワーク全体での割り当ての削減。</span><span class="sxs-lookup"><span data-stu-id="435be-322">Reduction in allocations across the framework, including middleware scenarios and routing.</span></span>
* <span data-ttu-id="435be-323">WebSocket 接続のメモリ使用量の削減。</span><span class="sxs-lookup"><span data-stu-id="435be-323">Reduction in memory usage for WebSocket connections.</span></span>
* <span data-ttu-id="435be-324">HTTPS 接続でのメモリの削減とスループットの向上。</span><span class="sxs-lookup"><span data-stu-id="435be-324">Memory reduction and throughput improvements for HTTPS connections.</span></span>
* <span data-ttu-id="435be-325">最適化された完全非同期の新 JSON シリアライザー。</span><span class="sxs-lookup"><span data-stu-id="435be-325">New optimized and fully asynchronous JSON serializer.</span></span>
* <span data-ttu-id="435be-326">フォーム解析でのメモリ使用量の削減とスループットの向上。</span><span class="sxs-lookup"><span data-stu-id="435be-326">Reduction in memory usage and throughput improvements in form parsing.</span></span>

## <a name="aspnet-core-30-only-runs-on-net-core-30"></a><span data-ttu-id="435be-327">.NET Core 3.0 のみで実行する ASP.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="435be-327">ASP.NET Core 3.0 only runs on .NET Core 3.0</span></span>

<span data-ttu-id="435be-328">ASP.NET Core 3.0 以降、.NET Framework はサポートされるターゲット フレームワークではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="435be-328">As of ASP.NET Core 3.0, .NET Framework is no longer a supported target framework.</span></span> <span data-ttu-id="435be-329">.NET Framework をターゲットとするプロジェクトは、[.NET Core 2.1 LTS リリース](https://www.microsoft.com/net/download/dotnet-core/2.1)を使用して完全にサポートされた状態で続行できます。</span><span class="sxs-lookup"><span data-stu-id="435be-329">Projects targeting .NET Framework can continue in a fully supported fashion using the [.NET Core 2.1 LTS release](https://www.microsoft.com/net/download/dotnet-core/2.1).</span></span> <span data-ttu-id="435be-330">ほとんどの ASP.NET Core 2.1.x 関連パッケージは、.NET Core 2.1 の 3 年の LTS 期間が終わっても無期限にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="435be-330">Most ASP.NET Core 2.1.x related packages will be supported indefinitely, beyond the 3 year LTS period for .NET Core 2.1.</span></span>

<span data-ttu-id="435be-331">移行の詳細については、「[.NET Framework から .NET Core にコードを移植する](/dotnet/core/porting/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-331">For migration information, see [Port your code from .NET Framework to .NET Core](/dotnet/core/porting/).</span></span>

## <a name="use-the-aspnet-core-shared-framework"></a><span data-ttu-id="435be-332">ASP.NET Core 共有フレームワークの使用</span><span class="sxs-lookup"><span data-stu-id="435be-332">Use the ASP.NET Core shared framework</span></span>

<span data-ttu-id="435be-333">[Microsoft.AspNetCore.App メタパッケージ](xref:fundamentals/metapackage-app)に含まれる ASP.NET Core 3.0 共有フレームワークでは、プロジェクト ファイル内の明示的な `<PackageReference />` 要素を必要としなくなりました。</span><span class="sxs-lookup"><span data-stu-id="435be-333">The ASP.NET Core 3.0 shared framework, contained in the [Microsoft.AspNetCore.App metapackage](xref:fundamentals/metapackage-app), no longer requires an explicit `<PackageReference />` element in the project file.</span></span> <span data-ttu-id="435be-334">プロジェクト ファイル内で `Microsoft.NET.Sdk.Web` SDK を使用すると、共有フレームワークが自動的に参照されます。</span><span class="sxs-lookup"><span data-stu-id="435be-334">The shared framework is automatically referenced when using the `Microsoft.NET.Sdk.Web` SDK in the project file:</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk.Web">
```

## <a name="assemblies-removed-from-the-aspnet-core-shared-framework"></a><span data-ttu-id="435be-335">ASP.NET Core 共有フレームワークから削除されたアセンブリ</span><span class="sxs-lookup"><span data-stu-id="435be-335">Assemblies removed from the ASP.NET Core shared framework</span></span>

<span data-ttu-id="435be-336">ASP.NET Core 3.0 共有フレームワークから削除された重要なアセンブリは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="435be-336">The most notable assemblies removed from the ASP.NET Core 3.0 shared framework are:</span></span>

* <span data-ttu-id="435be-337">[Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json/) (Json.NET)。</span><span class="sxs-lookup"><span data-stu-id="435be-337">[Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json/) (Json.NET).</span></span> <span data-ttu-id="435be-338">Json.NET を ASP.NET Core 3.0 に追加するには、「[Newtonsoft.Json ベースの JSON 形式のサポートを追加する](xref:web-api/advanced/formatting#add-newtonsoftjson-based-json-format-support)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-338">To add Json.NET to ASP.NET Core 3.0, see [Add Newtonsoft.Json-based JSON format support](xref:web-api/advanced/formatting#add-newtonsoftjson-based-json-format-support).</span></span> <span data-ttu-id="435be-339">ASP.NET Core 3.0 では JSON の読み取りと書き込みのために `System.Text.Json` が導入されています。</span><span class="sxs-lookup"><span data-stu-id="435be-339">ASP.NET Core 3.0 introduces `System.Text.Json` for reading and writing JSON.</span></span> <span data-ttu-id="435be-340">詳細については、このドキュメントの「[新しい JSON シリアル化](#new-json-serialization)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-340">For more information, see [New JSON serialization](#new-json-serialization) in this document.</span></span>
* [<span data-ttu-id="435be-341">Entity Framework Core</span><span class="sxs-lookup"><span data-stu-id="435be-341">Entity Framework Core</span></span>](/ef/core/)

<span data-ttu-id="435be-342">共有フレームワークから削除されたすべてのアセンブリの一覧については、「[Microsoft.AspNetCore.App 3.0 から削除されるアセンブリ](https://github.com/aspnet/AspNetCore/issues/3755)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-342">For a complete list of assemblies removed from the shared framework, see [Assemblies being removed from Microsoft.AspNetCore.App 3.0](https://github.com/aspnet/AspNetCore/issues/3755).</span></span> <span data-ttu-id="435be-343">この変更の動機については、「[Microsoft.AspNetCore.App 3.0 に対する重大な変更](https://github.com/aspnet/Announcements/issues/325)」および「[ASP.NET Core 3.0 の変更点を初めて見て](https://devblogs.microsoft.com/aspnet/a-first-look-at-changes-coming-in-asp-net-core-3-0/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="435be-343">For more information on the motivation for this change, see [Breaking changes to Microsoft.AspNetCore.App in 3.0](https://github.com/aspnet/Announcements/issues/325) and [A first look at changes coming in ASP.NET Core 3.0](https://devblogs.microsoft.com/aspnet/a-first-look-at-changes-coming-in-asp-net-core-3-0/).</span></span>

<!-- 
## Additional information
For the complete list of changes, see the [ASP.NET Core 3.0 Release Notes](WHERE IS THIS????).
-->