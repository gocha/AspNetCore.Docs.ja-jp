---
title: ASP.NET Core での Google 外部ログインのセットアップ
author: rick-anderson
description: このチュートリアルでは、既存の ASP.NET Core アプリに Google アカウントユーザー認証を統合する方法について説明します。
ms.author: riande
ms.custom: mvc, seodec18
ms.date: 03/19/2020
no-loc:
- appsettings.json
- ASP.NET Core Identity
- cookie
- Cookie
- Blazor
- Blazor Server
- Blazor WebAssembly
- Identity
- Let's Encrypt
- Razor
- SignalR
uid: security/authentication/google-logins
ms.openlocfilehash: 111ea7c972778dfd5296d0401c16563aeaa36a63
ms.sourcegitcommit: ca34c1ac578e7d3daa0febf1810ba5fc74f60bbf
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2020
ms.locfileid: "93060314"
---
# <a name="google-external-login-setup-in-aspnet-core"></a>ASP.NET Core での Google 外部ログインのセットアップ

作成者: [Valeriy Novytskyy](https://github.com/01binary)、[Rick Anderson](https://twitter.com/RickAndMSFT)

このチュートリアルでは、 [前のページ](xref:security/authentication/social/index)で作成した ASP.NET Core 3.0 プロジェクトを使用して、ユーザーが自分の Google アカウントでサインインできるようにする方法について説明します。

## <a name="create-a-google-api-console-project-and-client-id"></a>Google API コンソールプロジェクトとクライアント ID を作成する

* [AspNetCore](https://www.nuget.org/packages/Microsoft.AspNetCore.Authentication.Google)をインストールします。
* [Google Sign-In と web アプリの統合](https://developers.google.com/identity/sign-in/web/sign-in)に移動し、[ **プロジェクトの構成** ] を選択します。
* [ **OAuth クライアントの構成** ] ダイアログで、[ **Web サーバー** ] を選択します。
* [承認された **リダイレクト uri** のテキスト入力] ボックスで、リダイレクト uri を設定します。 たとえば、`https://localhost:44312/signin-google` のように指定します。
* **クライアント ID** と **クライアントシークレット** を保存します。
* サイトをデプロイするときに、新しいパブリック url を **Google コンソール** から登録します。

## <a name="store-the-google-client-id-and-secret"></a>Google クライアント ID とシークレットを保存する

Google クライアント ID やシークレット値などの機微な設定を [Secret Manager](xref:security/app-secrets)に保存します。 このサンプルでは、次の手順を使用します。

1. 「 [シークレットストレージを有効にする](xref:security/app-secrets#enable-secret-storage)」の手順に従って、シークレットストレージのプロジェクトを初期化します。
1. 秘密キーとシークレットキーを使用して、機密設定をローカルシークレットストアに保存 `Authentication:Google:ClientId` し `Authentication:Google:ClientSecret` ます。

    ```dotnetcli
    dotnet user-secrets set "Authentication:Google:ClientId" "<client-id>"
    dotnet user-secrets set "Authentication:Google:ClientSecret" "<client-secret>"
    ```

[!INCLUDE[](~/includes/environmentVarableColon.md)]

Api [コンソール](https://console.developers.google.com/apis/dashboard)で api の資格情報と使用状況を管理できます。

## <a name="configure-google-authentication"></a>Google 認証を構成する

Google サービスをに追加し `Startup.ConfigureServices` ます。

[!code-csharp[](~/security/authentication/social/social-code/3.x/StartupGoogle3x.cs?highlight=11-19)]

[!INCLUDE [default settings configuration](includes/default-settings2-2.md)]

## <a name="sign-in-with-google"></a>Google でサインイン

* アプリを実行し、[ **ログイン** ] をクリックします。 Google でサインインするためのオプションが表示されます。
* [ **Google** ] ボタンをクリックします。これにより、認証のために google にリダイレクトされます。
* Google の資格情報を入力すると、web サイトにリダイレクトされます。

[!INCLUDE[Forward request information when behind a proxy or load balancer section](includes/forwarded-headers-middleware.md)]

[!INCLUDE[](includes/chain-auth-providers.md)]

<xref:Microsoft.AspNetCore.Authentication.Google.GoogleOptions>Google 認証でサポートされる構成オプションの詳細については、「API リファレンス」を参照してください。 これは、ユーザーに関するさまざまな情報を要求するために使用できます。

## <a name="change-the-default-callback-uri"></a>既定のコールバック URI を変更する

URI セグメント `/signin-google` は、Google 認証プロバイダーの既定のコールバックとして設定されます。 [GoogleOptions](/dotnet/api/microsoft.aspnetcore.authentication.google.googleoptions)クラスの [継承された[remoteauthenticationoptions]](/dotnet/api/microsoft.aspnetcore.authentication.remoteauthenticationoptions.callbackpath)プロパティを使用して Google 認証ミドルウェアを構成するときに、既定のコールバック URI を変更できます。

## <a name="troubleshooting"></a>トラブルシューティング

* サインインが機能せず、エラーが発生しない場合は、開発モードに切り替えて、問題を簡単にデバッグできるようにします。
* Identityでを呼び出すことによってが構成されていない場合 `services.AddIdentity` 、ArgumentException で結果を認証しようとしています。 `ConfigureServices` *' SignInScheme ' オプションを指定する必要があり* ます。 このチュートリアルで使用するプロジェクトテンプレートによって、この処理が確実に行われます。
* 初期移行を適用してサイトデータベースが作成されていない場合は、 *要求エラーの処理中にデータベース操作が失敗* します。 [ **移行の適用** ] を選択してデータベースを作成し、ページを更新してエラーを解消します。

## <a name="next-steps"></a>次のステップ

* この記事では、Google で認証する方法について説明しました。 同様のアプローチに従って、 [前のページ](xref:security/authentication/social/index)に一覧表示されている他のプロバイダーとの認証を行うことができます。
* アプリを Azure に発行したら、 `ClientSecret` GOOGLE API コンソールでをリセットします。
* とを `Authentication:Google:ClientId` 、 `Authentication:Google:ClientSecret` Azure portal のアプリケーション設定として設定します。 構成システムは、環境変数からキーを読み取るように設定されています。
