---
title: 新機能 リリース ノート - Azure Active Directory | Microsoft Docs
description: 最新のリリース ノート、既知の問題、バグの修正、非推奨の機能、予定されている変更点など、Azure Active Directory の新着情報について説明します。
services: active-directory
author: eross-msft
manager: daveba
featureFlags:
- clicktale
ms.assetid: 06a149f7-4aa1-4fb9-a8ec-ac2633b031fb
ms.service: active-directory
ms.subservice: fundamentals
ms.workload: identity
ms.topic: conceptual
ms.date: 05/23/2019
ms.author: lizross
ms.reviewer: dhanyahk
ms.custom: it-pro
ms.collection: M365-identity-device-management
ms.openlocfilehash: e6a66aefec69a0551f85b11a380c90d1915bd776
ms.sourcegitcommit: cababb51721f6ab6b61dda6d18345514f074fb2e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2019
ms.locfileid: "66474192"
---
# <a name="whats-new-in-azure-active-directory"></a>Azure Active Directory の新着情報

>URL `https://docs.microsoft.com/api/search/rss?search=%22release+notes+for+azure+AD%22&locale=en-us` をコピーして、お使いの ![RSS フィード リーダー アイコン](./media/whats-new/feed-icon-16x16.png) フィード リーダーに貼り付け、更新内容を確認するためにこのページに再度アクセスするタイミングに関する通知を受け取るようにしてください。

Azure AD は随時改善されています。 常に最新の開発情報を把握していただけるよう、この記事では以下に関する情報を提供します。

- 最新のリリース
- 既知の問題
- バグの修正
- 非推奨の機能
- 変更の計画

このページは毎月更新されるため、定期的にアクセスしてご確認ください。 6 か月以上前の項目を探す場合は、「[新着情報のアーカイブ - Azure Active Directory](whats-new-archive.md)」をご覧ください。

---

## <a name="may-2019"></a>2019 年 5 月

### <a name="service-change-future-support-for-only-tls-12-protocols-on-the-application-proxy-service"></a>サービスの変更:アプリケーション プロキシ サービスでの TLS 1.2 プロトコルのみの今後のサポート

**種類:** 変更の計画  
**サービス カテゴリ:** アプリ プロキシ  
**製品の機能:** Access Control

お客様にクラス最高の暗号化を提供するために、Application Proxy サービスでは TLS 1.2 プロトコルのみにアクセスを制限しています。 この変更は、TLS 1.2 プロトコルのみを既に使用しているお客様に徐々に適用されているため、変更を意識することはありません。

2019 年 8 月 31日で TLS 1.0 と TLS 1.1 が廃止されますが、改めて事前通知を行いますので、この変更に備える時間が与えられます。 この変更に備えるために、Application Proxy を通じて発行されたアプリへのアクセスにユーザーが使用するすべてのクライアントを含む、クライアントとサーバーおよびブラウザーとサーバーの組み合わせが、TLS 1.2 プロトコルを使用して Application Proxy サービスへの接続を維持するように更新されていることを確認してください。 詳しくは、「[Azure Active Directory のアプリケーション プロキシを使用してリモート アクセスするためのオンプレミス アプリケーションを追加する](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-add-on-premises-application#before-you-begin)」を参照してください。

---

### <a name="use-the-usage-and-insights-report-to-view-your-app-related-sign-in-data"></a>使用状況および分析情報レポートを使用して、アプリに関連するサインイン データを表示する

**種類:** 新機能  
**サービス カテゴリ:** エンタープライズ アプリケーション  
**製品の機能:** 監視とレポート

これで、Azure portal の **[エンタープライズ アプリケーション]** 領域にある使用状況および分析情報レポートを使用して、以下に関する情報を含んだサインイン データをアプリケーションを中心にして表示できます。

- 組織内で最もよく使われるアプリ

- サインインの失敗が最も多いアプリ

- アプリごとの上位のサインイン エラー

この機能の詳細については、「[Azure Active Directory ポータルの使用状況と分析情報のレポート](https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-usage-insights-report)」を参照してください

---

### <a name="automate-your-user-provisioning-to-cloud-apps-using-azure-ad"></a>Azure AD を使用してクラウド アプリへのユーザー プロビジョニングを自動化する

**種類:** 新機能  
**サービス カテゴリ:** エンタープライズ アプリケーション  
**製品の機能:** 監視とレポート

これらの新しいチュートリアルに従って、Azure AD プロビジョニング サービスを使用して、次のクラウド ベース アプリのユーザー アカウントの作成、削除、および更新を自動化します。

- [Comeet](https://docs.microsoft.com/azure/active-directory/saas-apps/comeet-recruiting-software-provisioning-tutorial)

- [DynamicSignal](https://docs.microsoft.com/azure/active-directory/saas-apps/dynamic-signal-provisioning-tutorial)

- [KeeperSecurity](https://docs.microsoft.com/azure/active-directory/saas-apps/keeper-password-manager-digitalvault-provisioning-tutorial)

グループ オブジェクトのプロビジョニング方法に関する情報が記載されている、この新しい [Dropbox チュートリアル](https://docs.microsoft.com/azure/active-directory/saas-apps/dropboxforbusiness-provisioning-tutorial)に従うこともできます。

自動化されたユーザー アカウント プロビジョニングを使用して組織をより適切にセキュリティ保護する方法の詳細については、[Azure AD での SaaS アプリケーションへのユーザー プロビジョニングの自動化](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning)に関するページを参照してください。

---

### <a name="identity-secure-score-is-now-available-in-azure-ad-general-availability"></a>Azure AD で ID セキュリティ スコアが利用可能 (一般提供)

**種類:** 新機能  
**サービス カテゴリ:** 該当なし  
**製品の機能:** ID のセキュリティ & 保護

これで、Azure AD で ID セキュリティ スコア機能を使用することにより、ID セキュリティ体制を監視し改善できます。 ID セキュリティ スコア機能では、次の操作に役立つ単一のダッシュボードを使用します。

- 1 から 223 のスコアに基づいて ID セキュリティ体制を客観的に測定する。

- ID セキュリティの強化を計画する

- セキュリティの強化の成功を確認する

ID セキュリティ スコア機能の詳細については、「[Azure Active Directory の ID セキュリティ スコアとは](https://docs.microsoft.com/azure/active-directory/fundamentals/identity-secure-score)」を参照してください。

---

### <a name="new-app-registrations-experience-is-now-available-general-availability"></a>新しいアプリの登録エクスペリエンスが利用可能 (一般提供)

**種類:** 新機能  
**サービス カテゴリ:** 認証 (ログイン)  
**製品の機能:** 開発者エクスペリエンス

新しい[アプリの登録](https://aka.ms/appregistrations)エクスペリエンスが一般提供され利用可能になりました。 この新しいエクスペリエンスには、Azure portal とアプリケーション登録ポータルの使い慣れているすべての主要機能が含まれ、これらの機能は以下を通じて向上しています。

- **アプリの管理の向上。** さまざまなポータルにわたってアプリを表示する代わりに、1 か所ですべてのアプリを表示できるようになりました。

- **アプリの登録の簡略化。** 改善されたナビゲーション エクスペリエンスから、刷新されたアクセス許可選択エクスペリエンスまで、アプリの登録および管理が簡単になりました。

- **詳細情報。** クイック スタート ガイドなど、アプリに関する詳細が表示されます。

詳細については、[Microsoft ID プラットフォーム](https://docs.microsoft.com/azure/active-directory/develop/)と[新しいアプリの登録エクスペリエンスが一般に利用可能になった](https://developer.microsoft.com/identity/blogs/new-app-registrations-experience-is-now-generally-available/)ことに関するページを参照してください。 ブログでのお知らせ。

---

### <a name="new-capabilities-available-in-the-risky-users-api-for-identity-protection"></a>Identity Protection の Risky Users API で使用できる新機能

**種類:** 新機能  
**サービス カテゴリ:** Identity Protection  
**製品の機能:** ID のセキュリティ & 保護

Risky Users API を使用して、ユーザーのリスク履歴を取得し、危険なユーザーを無視し、ユーザーを侵害対象として確認できるようになったことをお知らせします。 この変更により、より効率的にユーザーのリスク状態を更新し、リスク履歴を理解できるようになりました。

詳細については、[Risky Users API のリファレンス ドキュメント](https://docs.microsoft.com/graph/api/resources/riskyuser?view=graph-rest-beta)を参照してください。

---

### <a name="new-federated-apps-available-in-azure-ad-app-gallery---may-2019"></a>Azure AD アプリ ギャラリーで入手できる新しいフェデレーション アプリ - 2019 年 5 月

**種類:** 新機能  
**サービス カテゴリ:** エンタープライズ アプリケーション  
**製品の機能:** サード パーティ統合

2019年 5 月に、フェデレーションを使用した以下の 21 の新規アプリのサポートが、アプリ ギャラリーに追加されました。

[Freedcamp](https://docs.microsoft.com/azure/active-directory/saas-apps/freedcamp-tutorial)、[Real Links](https://docs.microsoft.com/azure/active-directory/saas-apps/real-links-tutorial)、[Kianda](https://app.kianda.com/sso/OpenID/AzureAD/)、[Simple Sign](https://docs.microsoft.com/azure/active-directory/saas-apps/simple-sign-tutorial)、[Braze](https://docs.microsoft.com/azure/active-directory/saas-apps/braze-tutorial)、[Displayr](https://docs.microsoft.com/azure/active-directory/saas-apps/displayr-tutorial)、[Templafy](https://docs.microsoft.com/azure/active-directory/saas-apps/templafy-tutorial)、[Marketo Sales Engage](https://toutapp.com/login)、[ACLP](https://docs.microsoft.com/azure/active-directory/saas-apps/aclp-tutorial)、[OutSystems](https://docs.microsoft.com/azure/active-directory/saas-apps/outsystems-tutorial)、[Meta4 Global HR](https://docs.microsoft.com/azure/active-directory/saas-apps/meta4-global-hr-tutorial)、[Quantum Workplace](https://docs.microsoft.com/azure/active-directory/saas-apps/quantum-workplace-tutorial)、[Cobalt](https://docs.microsoft.com/azure/active-directory/saas-apps/cobalt-tutorial)、[webMethods API Cloud](https://docs.microsoft.com/azure/active-directory/saas-apps/webmethods-integration-cloud-tutorial)、[RedFlag](https://pocketstop.com/redflag/)、[Whatfix](https://docs.microsoft.com/azure/active-directory/saas-apps/whatfix-tutorial)、[Control](https://docs.microsoft.com/azure/active-directory/saas-apps/control-tutorial)、[JOBHUB](https://docs.microsoft.com/azure/active-directory/saas-apps/jobhub-tutorial)、[NEOGOV](https://docs.microsoft.com/azure/active-directory/saas-apps/neogov-tutorial)、[Foodee](https://docs.microsoft.com/azure/active-directory/saas-apps/foodee-tutorial)、[MyVR](https://docs.microsoft.com/azure/active-directory/saas-apps/myvr-tutorial)

アプリに関する詳細については、「[SaaS アプリケーションと Azure Active Directory の統合](https://aka.ms/appstutorial)」を参照してください。 アプリケーションの Azure AD アプリ ギャラリーでの公開に関する詳細については、「[アプリケーションを Azure Active Directory アプリケーション ギャラリーで公開する](https://aka.ms/azureadapprequest)」を参照してください。

---

### <a name="improved-groups-creation-and-management-experiences-in-the-azure-ad-portal"></a>Azure AD ポータルの強化されたグループ作成および管理エクスペリエンス

**種類:** 新機能  
**サービス カテゴリ:** グループ管理  
**製品の機能:** コラボレーション

Azure AD ポータルでグループに関連するエクスペリエンスの機能強化を行いました。 これらの機能強化により、管理者は、グループの一覧やメンバーの一覧をより適切に管理し、追加の作成オプションを提供できます。

機能強化は次のとおりです。

- メンバーシップの種類およびグループの種類による基本フィルター処理。

- ソースやメール アドレスなどの新しい列の追加。

- 簡単に選択解除するためのグループ、メンバー、および所有者の一覧を複数選択する機能。

- グループの作成中にメール アドレスを選択し、所有者を追加する機能。

詳細については、「[Azure Active Directory を使用して基本グループを作成してメンバーを追加する](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)」を参照してください。

---

### <a name="configure-a-naming-policy-for-office-365-groups-in-azure-ad-portal-general-availability"></a>Azure AD ポータルで Office 365 グループの名前付けポリシーを構成する (一般提供)

**種類:** 変更された機能  
**サービス カテゴリ:** グループ管理  
**製品の機能:** コラボレーション

管理者は、Azure AD ポータルを使用して、Office 365 グループの名前付けポリシーを構成できるようになりました。 この変更は、組織内のユーザーによって作成または編集される Office 365 グループに対して一貫性のある名前付け規則を適用するのに役立ちます。

Office 365 グループの名前付けポリシーは、次の 2 通りの方法で構成できます。

- グループ名に自動的に追加されるプレフィックスまたはサフィックスを定義します。

- グループ名で許可されない、組織の禁止されている単語のカスタマイズ セットをアップロードします (たとえば、“CEO、Payroll、HR”)。

詳細情報については、「[Azure Active Directory での Office 365 グループの名前付けポリシーの強制](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-naming-policy)」をご覧ください。

---

### <a name="microsoft-graph-api-endpoints-are-now-available-for-azure-ad-activity-logs-general-availability"></a>Microsoft Graph API エンドポイントが Azure AD アクティビティ ログで利用可能(一般提供)

**種類:** 変更された機能  
**サービス カテゴリ:** レポート  
**製品の機能:** 監視とレポート

Azure AD アクティビティ ログで Microsoft Graph API エンドポイントのサポートが一般的に利用できるようになったことをお知らせします。 このリリースでは、バージョン 1.0 の Azure AD 監査ログとサインイン ログ API を使用できるようになりました。

詳細については、[Azure AD 監査ログ API の概要](https://docs.microsoft.com/graph/api/resources/azure-ad-auditlog-overview?view=graph-rest-1.0)に関するページを参照してください。

---

### <a name="administrators-can-now-use-conditional-access-for-the-combined-registration-process-public-preview"></a>管理者が統合登録プロセスに条件付きアクセスを使用可能 (パブリック プレビュー)

**種類:** 新機能  
**サービス カテゴリ:** 条件付きアクセス  
**製品の機能:** ID のセキュリティ & 保護  

管理者は、統合登録ページで使用する条件付きアクセス ポリシーを作成できるようになりました。 これには、次の場合に登録を許可するポリシーの適用が含まれます。

- ユーザーが信頼できるネットワーク上にいる場合。

- ユーザーのサインイン リスクが低い場合。

- ユーザーがマネージド デバイス上にある場合。

- ユーザーが組織の利用規約 (TOU) に同意した場合。

条件付きアクセスとパスワードのリセットの詳細については、[Azure AD の MFA とパスワードのリセットの統合登録エクスペリエンスの条件付きアクセスに関するブログの投稿](https://techcommunity.microsoft.com/t5/Azure-Active-Directory-Identity/Conditional-access-for-the-Azure-AD-combined-MFA-and-password/ba-p/566348)を参照してください。 統合登録プロセスの条件付きアクセス ポリシーの詳細については、「[統合登録の条件付きアクセス ポリシー](https://docs.microsoft.com/azure/active-directory/authentication/howto-registration-mfa-sspr-combined#conditional-access-policies-for-combined-registration)」を参照してください。 Azure AD Terms of Use 機能の詳細については、「[Azure Active Directory Terms of Use 機能](https://docs.microsoft.com/azure/active-directory/conditional-access/terms-of-use)」を参照してください。

---

## <a name="april-2019"></a>2019 年 4 月

### <a name="new-azure-ad-threat-intelligence-detection-is-now-available-in-refreshed-azure-ad-identity-protection"></a>新しい Azure AD 脅威インテリジェンス検出が、更新後の Azure AD Identity Protection で利用可能

**種類:** 新機能  
**サービス カテゴリ:** Azure AD Identity Protection  
**製品の機能:** ID のセキュリティ & 保護

Azure AD 脅威インテリジェンス検出が、更新後の Azure AD Identity Protection で利用可能になりました。 この新しい機能は、Microsoft の内部および外部の脅威インテリジェンスに基づいて、特定のユーザーにとって異常であったり、既知の攻撃パターンに一致したりするユーザー アクティビティを示す場合に役立ちます。

更新されたバージョンの Azure AD Identity Protection の詳細については、[Azure AD Identity Protection の 4 つの主要な機能強化がパブリック ビューに示されるようになった](https://techcommunity.microsoft.com/t5/Azure-Active-Directory-Identity/Four-major-Azure-AD-Identity-Protection-enhancements-are-now-in/ba-p/326935)ことに関するブログと「[Azure Active Directory Identity Protection (更新版) とは](https://docs.microsoft.com/azure/active-directory/identity-protection/overview-v2)」の記事を参照してください。 article. Azure AD 脅威インテリジェンス検出の詳細については、[Azure Active Directory Identity Protection のリスク イベント](https://docs.microsoft.com/azure/active-directory/identity-protection/risk-events-reference#azure-ad-threat-intelligence)に関する記事を参照してください。

---

### <a name="azure-ad-entitlement-management-is-now-available-public-preview"></a>Azure AD エンタイトルメント管理が利用可能 (パブリック プレビュー)

**種類:** 新機能  
**サービス カテゴリ:** Identity Governance  
**製品の機能:** Identity Governance

Azure AD エンタイトルメント管理 (現在パブリック プレビュー段階) は、従業員とビジネス パートナーがアクセスを要求する方法、承認を行うユーザー、アクセスできる時間を定義するアクセス パッケージの管理をお客様が委任できるようにします。 アクセス パッケージは、Azure AD と Office 365 の各グループでのメンバーシップ、エンタープライズ アプリケーションでのロールの割り当て、および SharePoint Online サイトのロールの割り当てを管理できます。 エンタイトルメント管理の詳細情報については、[Azure AD エンタイトルメント管理の概要](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-overview)に関する記事をご覧ください。 Privileged Identity Management、アクセス レビュー、および利用規約などの Azure AD Identity Governance 機能の広がりについて詳しくは、「[Azure AD Identity Governance とは](../governance/identity-governance-overview.md)」をご覧ください。

---

### <a name="configure-a-naming-policy-for-office-365-groups-in-azure-ad-portal-public-preview"></a>Azure AD ポータルで Office 365 グループの名前付けポリシーを構成する (パブリック プレビュー)

**種類:** 新機能  
**サービス カテゴリ:** グループ管理  
**製品の機能:** コラボレーション

管理者は、Azure AD ポータルを使用して、Office 365 グループの名前付けポリシーを構成できるようになりました。 この変更は、組織内のユーザーによって作成または編集される Office 365 グループに対して一貫性のある名前付け規則を適用するのに役立ちます。

Office 365 グループの名前付けポリシーは、次の 2 通りの方法で構成できます。

- グループ名に自動的に追加されるプレフィックスまたはサフィックスを定義します。

- グループ名で許可されない、組織の禁止されている単語のカスタマイズ セットをアップロードします (たとえば、“CEO、Payroll、HR”)。

詳細情報については、「[Azure Active Directory での Office 365 グループの名前付けポリシーの強制](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-naming-policy)」をご覧ください。

---

### <a name="azure-ad-activity-logs-are-now-available-in-azure-monitor-general-availability"></a>Azure AD アクティビティ ログを Azure Monitor で使用できるようになりました (一般提供)。

**種類:** 新機能  
**サービス カテゴリ:** レポート  
**製品の機能:** 監視とレポート

Azure AD アクティビティ ログの視覚化に関するフィードバックに対応するために、Log Analytics に新しい分析情報機能を導入します。 この機能により、Workbooks という対話型テンプレートを使用して Azure AD リソースに関する分析情報を得ることができます。 これらの既製の Workbooks は、アプリまたはユーザーの詳細情報を提供することができます。これには以下が含まれます。

- **サインイン。** サインインの場所、使用中のオペレーティング システムまたはブラウザーのクライアントとバージョン、成功または失敗したサインインの回数などのアプリおよびユーザーの詳細情報を提供します。

- **レガシ認証と条件付きアクセス。** 条件付きアクセス ポリシーによってトリガーされる Multi-Factor Authentication の使用、条件付きアクセス ポリシーを使用するアプリなど、レガシ認証を使用するアプリおよびユーザーの詳細情報を提供します。

- **サインイン エラー分析。** サインイン エラーの発生原因がユーザー アクションか、ポリシーの問題か、またはインフラストラクチャかを判別するのを支援します。

- **カスタム レポート。** 新規の Workbooks を作成したり、既存の Workbooks を編集したりして、組織の Insights 機能のカスタマイズに役立てることができます。

詳細情報については、「[Azure Active Directory レポートに Azure Monitor ブックを使用する方法](https://docs.microsoft.com/azure/active-directory/reports-monitoring/howto-use-azure-monitor-workbooks)」を参照してください。

---

### <a name="new-federated-apps-available-in-azure-ad-app-gallery---april-2019"></a>Azure AD アプリ ギャラリーで入手できる新しいフェデレーション アプリ - 2019 年 4 月

**種類:** 新機能  
**サービス カテゴリ:** エンタープライズ アプリケーション  
**製品の機能:** サード パーティ統合

2019 年 4 月に、フェデレーションを使用した以下の 21 の新規アプリのサポートが、アプリ ギャラリーに追加されました。

[SAP Fiori](https://docs.microsoft.com/azure/active-directory/saas-apps/sap-fiori-tutorial)、[HRworks Single Sign-On](https://docs.microsoft.com/azure/active-directory/saas-apps/hrworks-single-sign-on-tutorial)、[Percolate](https://docs.microsoft.com/azure/active-directory/saas-apps/percolate-tutorial)、[MobiControl](https://docs.microsoft.com/azure/active-directory/saas-apps/mobicontrol-tutorial)、[Citrix NetScaler](https://docs.microsoft.com/azure/active-directory/saas-apps/citrix-netscaler-tutorial)、[Shibumi](https://docs.microsoft.com/azure/active-directory/saas-apps/shibumi-tutorial)、[Benchling](https://docs.microsoft.com/azure/active-directory/saas-apps/benchling-tutorial)、[MileIQ](https://mileiq.onelink.me/991934284/7e980085)、[PageDNA](https://docs.microsoft.com/azure/active-directory/saas-apps/pagedna-tutorial)、[EduBrite LMS](https://docs.microsoft.com/azure/active-directory/saas-apps/edubrite-lms-tutorial)、[RStudio Connect](https://docs.microsoft.com/azure/active-directory/saas-apps/rstudio-connect-tutorial)、[AMMS](https://docs.microsoft.com/azure/active-directory/saas-apps/amms-tutorial)、[Mitel Connect](https://docs.microsoft.com/azure/active-directory/saas-apps/mitel-connect-tutorial)、[Alibaba Cloud (ロールベースの SSO)](https://docs.microsoft.com/azure/active-directory/saas-apps/alibaba-cloud-service-role-based-sso-tutorial)、[Certent Equity Management](https://docs.microsoft.com/azure/active-directory/saas-apps/certent-equity-management-tutorial)、[Sectigo Certificate Manager](https://docs.microsoft.com/azure/active-directory/saas-apps/sectigo-certificate-manager-tutorial)、[GreenOrbit](https://docs.microsoft.com/azure/active-directory/saas-apps/greenorbit-tutorial)、[Workgrid](https://docs.microsoft.com/azure/active-directory/saas-apps/workgrid-tutorial)、[monday.com](https://docs.microsoft.com/azure/active-directory/saas-apps/mondaycom-tutorial)、[SurveyMonkey Enterprise](https://docs.microsoft.com/azure/active-directory/saas-apps/surveymonkey-enterprise-tutorial)、[Indiggo](https://indiggolead.com/)

アプリに関する詳細については、「[SaaS アプリケーションと Azure Active Directory の統合](https://aka.ms/appstutorial)」を参照してください。 アプリケーションの Azure AD アプリ ギャラリーでの公開に関する詳細については、「[アプリケーションを Azure Active Directory アプリケーション ギャラリーで公開する](https://aka.ms/azureadapprequest)」を参照してください。

---

### <a name="new-access-reviews-frequency-option-and-multiple-role-selection"></a>新規アクセス レビューの頻度オプションと複数のロールの選択

**種類:** 新機能  
**サービス カテゴリ:** アクセス レビュー  
**製品の機能:** Identity Governance

Azure AD アクセス レビューの新しい更新プログラムにより、次のことが可能になります。

- アクセス レビューの頻度を、以前からある、週に 1 度、月に 1 度、4 半期に 1 度、および 1 年に 1 度のオプションに加え、「**半年に 1 度**」に変更します。

- 1 つのアクセス レビューを作成するときに、複数の Azure AD と Azure リソースのロールを選択します。 この場合は、すべてのロールが同じ設定値で設定され、すべてのレビュー担当者に同時に通知が送られます。

アクセス レビューを作成する方法の詳細については、[Azure AD アクセス レビューでのグループまたはアプリケーションのアクセス レビューの作成](https://docs.microsoft.com/azure/active-directory/governance/create-access-review)に関するページを参照してください

---

### <a name="azure-ad-connect-email-alert-systems-are-transitioning-sending-new-email-sender-information-for-some-customers"></a>Azure AD Connect の電子メール アラート システムの切り替えが行われており、一部のお客様に対して新規電子メール送信者情報が送信される

**種類:** 変更された機能  
**サービス カテゴリ:** AD 同期  
**製品の機能:** プラットフォーム

Azure AD Connect で電子メール アラート システムの切り替えが行われており、一部のお客様に新規電子メール送信者が表示される可能性があります。 これに対処するには、`azure-noreply@microsoft.com` を組織の許可リストに追加する必要があります。さもないと、Office 365、Azure、またはお使いの同期サービスから重要なアラートを引き続き受信できなくなります。

---

### <a name="upn-suffix-changes-are-now-successful-between-federated-domains-in-azure-ad-connect"></a>Azure AD Connect でフェデレーション ドメイン間の UPN サフィックスの変更が正常に行われるようになりました

**種類:** 固定  
**サービス カテゴリ:** AD 同期  
**製品の機能:** プラットフォーム

Azure AD Connect で、あるフェデレーション ドメインから別のフェデレーション ドメインに、ユーザーの UPN サフィックスを正しく変更できるようになりました。 この修正により、同期サイクル中に FederatedDomainChangeError エラー メッセージを受け取ったり、「Azure Active Directory でこのオブジェクトを更新できません。属性 [FederatedUser.UserPrincipalName] が無効です。 ローカル ディレクトリ サービスの値を更新してください」という通知メールを受け取ったりすることがなくなります。

詳しくは、[同期中のエラーのトラブルシューティング](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#federateddomainchangeerror)に関するページをご覧ください。

---

### <a name="increased-security-using-the-app-protection-based-conditional-access-policy-in-azure-ad-public-preview"></a>Azure AD (パブリック プレビュー) でアプリ保護ベースの条件付きアクセス ポリシーを使用してセキュリティを強化

**種類:** 新機能  
**サービス カテゴリ:** 条件付きアクセス  
**製品の機能:** ID のセキュリティ & 保護

アプリ保護ベースの条件付きアクセスが、 **[アプリの保護ポリシーが必要]** を使用することで使用できるようになりました。 この新しいポリシーは、次のことを防止することで組織のセキュリティ向上を支援します。

- ユーザーが Microsoft Intune ライセンスなしでアプリにアクセスできるようにすること。

- ユーザーが Microsoft Intune アプリ保護ポリシーを取得できないようにすること。

- ユーザーが Microsoft Intune アプリ保護ポリシーなしでアプリにアクセスできるようにすること。

詳細については、[条件付きアクセスを使用してクラウド アプリへのアクセスにアプリ保護ポリシーを要求する方法](https://docs.microsoft.com/azure/active-directory/conditional-access/app-protection-based-conditional-access)に関するページを参照してください。

---

### <a name="new-support-for-azure-ad-single-sign-on-and-conditional-access-in-microsoft-edge-public-preview"></a>Microsoft Edge での Azure AD シングル サインオンと条件付きアクセスの新しいサポート (パブリック プレビュー)

**種類:** 新機能  
**サービス カテゴリ:** 条件付きアクセス  
**製品の機能:** ID のセキュリティ & 保護

Microsoft Edge に対する Azure AD のサポートが強化されました。これには、Azure AD シングル サインオンと条件付きアクセスの新しいサポートの提供が含まれます。 以前に Microsoft Intune Managed Browser を使用していた場合は、代わりに Microsoft Edge を使用できるようになりました。

条件付きアクセスを使用したデバイスとアプリの設定と管理の詳細については、「[条件付きアクセスを使用してクラウド アプリへのアクセスにマネージド デバイスを要求する](https://docs.microsoft.com/azure/active-directory/conditional-access/require-managed-devices)」および「[条件付きアクセスを使用してクラウド アプリへのアクセスに承認されたクライアント アプリを要求する](https://docs.microsoft.com/azure/active-directory/conditional-access/app-based-conditional-access)」を参照してください。 Microsoft Intune ポリシーと Microsoft Edge を使用してアクセスを管理する方法の詳細については、「[Microsoft Intune のポリシーで保護されたブラウザーを使用してインターネット アクセスを管理する](https://docs.microsoft.com/intune/app-configuration-managed-browser)」を参照してください。

---

## <a name="march-2019"></a>2019 年 3 月

### <a name="identity-experience-framework-and-custom-policy-support-in-azure-active-directory-b2c-is-now-available-ga"></a>Azure Active Directory B2C での Identity Experience Framework とカスタム ポリシーのサポートが使用可能になりました (GA)

**種類:** 新機能  
**サービス カテゴリ:** B2C - コンシューマー ID 管理  
**製品の機能:** B2B/B2C

Azure AD B2C でカスタム ポリシーを作成できるようになりました。これには、Azure SLA のもとで大規模にサポートされる次のタスクが含まれます。

- カスタム ポリシーを使用して、カスタム認証のユーザー体験を作成およびアップロードする。

- 要求プロバイダー間のやり取りとしてユーザー体験を順を追って記述する。

- ユーザー体験の条件分岐を定義する。

- リアルタイムの意思決定および通信で使用するために、要求を変換およびマップする。

- カスタム認証のユーザー体験で REST API 対応サービスを使用する。 たとえば、電子メール プロバイダー、CRM、および独自の承認システムで。

- OpenIDConnect プロトコルに準拠している ID プロバイダーとフェデレーションする。 たとえば、マルチテナント Azure AD、ソーシャル アカウント プロバイダー、または 2 要素検証プロバイダーと。

カスタム ポリシーの作成の詳細については、[Azure Active Directory B2C でのカスタム ポリシーの開発者向けメモ](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-developer-notes-custom)に関するページ、および [Alex Simon のブログ記事 (ケース スタディを含む)](https://techcommunity.microsoft.com/t5/Azure-Active-Directory-Identity/Azure-AD-B2C-custom-policies-to-build-your-own-identity-journeys/ba-p/382791) を参照してください。

---

### <a name="new-federated-apps-available-in-azure-ad-app-gallery---march-2019"></a>Azure AD アプリ ギャラリーで入手できる新しいフェデレーション アプリ - 2019 年 3 月

**種類:** 新機能  
**サービス カテゴリ:** エンタープライズ アプリケーション  
**製品の機能:** サード パーティ統合

2019 年 3 月に、フェデレーションがサポートされる次の 14 の新しいアプリがアプリ ギャラリーに追加されました。

[ISEC7 Mobile Exchange Delegate](https://www.isec7.com/english/)、[MediusFlow](https://office365.cloudapp.mediusflow.com/)、[ePlatform](https://docs.microsoft.com/azure/active-directory/saas-apps/eplatform-tutorial)、[Fulcrum](https://docs.microsoft.com/azure/active-directory/saas-apps/fulcrum-tutorial)、[ExcelityGlobal](https://docs.microsoft.com/azure/active-directory/saas-apps/excelityglobal-tutorial)、[Explanation-Based Auditing System](https://docs.microsoft.com/azure/active-directory/saas-apps/explanation-based-auditing-system-tutorial)、[Lean](https://docs.microsoft.com/azure/active-directory/saas-apps/lean-tutorial)、[Powerschool Performance Matters](https://docs.microsoft.com/azure/active-directory/saas-apps/powerschool-performance-matters-tutorial)、[Cinode](https://cinode.com/)、[Iris Intranet](https://docs.microsoft.com/azure/active-directory/saas-apps/iris-intranet-tutorial)、[Empactis](https://docs.microsoft.com/azure/active-directory/saas-apps/empactis-tutorial)、[SmartDraw](https://docs.microsoft.com/azure/active-directory/saas-apps/smartdraw-tutorial)、[Confirmit Horizons](https://docs.microsoft.com/azure/active-directory/saas-apps/confirmit-horizons-tutorial)、[TAS](https://docs.microsoft.com/azure/active-directory/saas-apps/tas-tutorial)

アプリに関する詳細については、「[SaaS アプリケーションと Azure Active Directory の統合](https://aka.ms/appstutorial)」を参照してください。 アプリケーションの Azure AD アプリ ギャラリーでの公開に関する詳細については、「[アプリケーションを Azure Active Directory アプリケーション ギャラリーで公開する](https://aka.ms/azureadapprequest)」を参照してください。

---

### <a name="new-zscaler-and-atlassian-provisioning-connectors-in-the-azure-ad-gallery---march-2019"></a>Azure AD ギャラリー内の新しい Zscaler および Atlassian プロビジョニング コネクタ - 2019 年 3 月

**種類:** 新機能  
**サービス カテゴリ:** アプリ プロビジョニング  
**製品の機能:** サード パーティ統合

次のアプリでのユーザー アカウントの作成、更新、および削除を自動化します。

[Zscaler](https://aka.ms/ZscalerProvisioning)、[Zscaler Beta](https://aka.ms/ZscalerBetaProvisioning)、[Zscaler One](https://aka.ms/ZscalerOneProvisioning)、[Zscaler 2](https://aka.ms/ZscalerTwoProvisioning)、[Zscaler 3](https://aka.ms/ZscalerThreeProvisioning)、[Zscaler ZSCloud](https://aka.ms/ZscalerZSCloudProvisioning)、[Atlassian Cloud](https://aka.ms/atlassianCloudProvisioning)

自動化されたユーザー アカウント プロビジョニングを使用して組織をより適切にセキュリティ保護する方法の詳細については、[Azure AD での SaaS アプリケーションへのユーザー プロビジョニングの自動化](https://aka.ms/ProvisioningDocumentation)に関するページを参照してください。

---

### <a name="restore-and-manage-your-deleted-office-365-groups-in-the-azure-ad-portal"></a>Azure AD ポータルで削除された Office 365 グループの復元および管理

**種類:** 新機能  
**サービス カテゴリ:** グループ管理  
**製品の機能:** コラボレーション

Azure AD ポータルから削除された Office 365 グループを表示および管理できるようになりました。 この変更により、どのグループが復元できるかを確認したり、組織で必要がなくなったすべてのグループを完全に削除したりできるようになります。

詳細については、[有効期限が切れたグループや削除されたグループの復元](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-restore-deleted#view-and-manage-the-deleted-office-365-groups-that-are-available-to-restore)に関するページを参照してください。

---

### <a name="single-sign-on-is-now-available-for-azure-ad-saml-secured-on-premises-apps-through-application-proxy-public-preview"></a>Azure AD SAML で保護されたオンプレミス アプリで、アプリケーション プロキシ経由でシングル サインオンを使用できるようになりました (パブリック プレビュー)

**種類:** 新機能  
**サービス カテゴリ:** アプリ プロキシ  
**製品の機能:** Access Control

SAML で認証されたオンプレミス アプリで、これらのアプリへのリモート アクセスと共に、アプリケーション プロキシ経由でシングル サインオン (SSO) エクスペリエンスを使用できるようになりました。 オンプレミス アプリで SAML SSO を設定する方法の詳細については、「[アプリケーション プロキシ (プレビュー) を使用したオンプレミスのアプリケーションに対する SAML シングル サインオン](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-configure-single-sign-on-on-premises-apps)」を参照してください。

---

### <a name="client-apps-in-request-loops-will-be-interrupted-to-improve-reliability-and-user-experience"></a>信頼性とユーザー エクスペリエンスを向上させるために要求ループ内のクライアント アプリが中断されます

**種類:** 新機能  
**サービス カテゴリ:** 認証 (ログイン)  
**製品の機能:** ユーザー認証

クライアント アプリが、短期間に数百の同じログイン要求を誤って発行する場合があります。 これらの要求は、成功するかどうかにかかわらず、そのすべてがユーザー エクスペリエンスの低下や IDP のワークロードの増加につながるため、すべてのユーザーの待ち時間が長くなり、IDP の可用性が低下します。

この更新プログラムは、通常の動作の範囲を超えて、重複した要求を短期間に複数回発行するクライアント アプリに `invalid_grant` エラー: `AADSTS50196: The server terminated an operation because it encountered a loop while processing a request` を送信します。 この問題が発生したクライアント アプリは対話型プロンプトを表示し、ユーザーに再度サインインすることを要求する必要があります。 この変更や、このエラーが発生した場合にアプリを修正する方法の詳細については、「[認証の新機能](https://docs.microsoft.com/azure/active-directory/develop/reference-breaking-changes#looping-clients-will-be-interrupted)」を参照してください。

---

### <a name="new-audit-logs-user-experience-now-available"></a>[監査ログ] の新しいユーザー エクスペリエンスが使用可能になりました

**種類:** 変更された機能  
**サービス カテゴリ:** レポート  
**製品の機能:** 監視とレポート

読みやすさと情報の検索方法の両方を向上させるのに役立つ新しい Azure AD **[監査ログ]** ページが作成されました。 新しい **[監査ログ]** ページを表示するには、Azure AD の **[アクティビティ]** セクションで **[監査ログ]** を選択します。

![サンプル情報を含む新しい [監査ログ] ページ](media/whats-new/audit-logs-page.png)

新しい **[監査ログ]** ページの詳細については、「[Azure Active Directory ポータルの監査アクティビティ レポート](https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-audit-logs#audit-logs)」を参照してください。

---

### <a name="new-warnings-and-guidance-to-help-prevent-accidental-administrator-lockout-from-misconfigured-conditional-access-policies"></a>正しく構成されていない条件付きアクセス ポリシーからの誤った管理者ロックアウトの防止に役立つ新しい警告およびガイダンス

**種類:** 変更された機能  
**サービス カテゴリ:** 条件付きアクセス  
**製品の機能:** ID のセキュリティ & 保護

管理者が、正しく構成されていない条件付きアクセス ポリシーにより自分のテナントから誤って自身をロックすることを防止するのに役立つように、Azure Portal に新しい警告および更新されたガイダンスが作成されました。 新しいガイダンスの詳細については、「[Azure Active Directory 条件付きアクセスのサービス依存関係の概要](https://docs.microsoft.com/azure/active-directory/conditional-access/service-dependencies)」を参照してください。

---

### <a name="improved-end-user-terms-of-use-experiences-on-mobile-devices"></a>モバイル デバイスでのエンドユーザーの利用規約エクスペリエンスの改善

**種類:** 変更された機能  
**サービス カテゴリ:** 使用条件  
**製品の機能:** ガバナンス

モバイル デバイスで利用規約を確認して同意する方法の改善に役立つように、既存の利用規約エクスペリエンスが更新されました。 情報のズームイン/ズームアウト、前の画面への戻り、ダウンロード、およびハイパーリンクの選択が可能になりました。 更新された利用規約の詳細については、[Azure Active Directory Terms of Use 機能](https://docs.microsoft.com/azure/active-directory/conditional-access/terms-of-use#what-terms-of-use-looks-like-for-users)に関するページを参照してください。

---

### <a name="new-azure-ad-activity-logs-download-experience-available"></a>新しい Azure AD アクティビティ ログのダウンロード エクスペリエンスが使用可能になりました

**種類:** 変更された機能  
**サービス カテゴリ:** レポート  
**製品の機能:** 監視とレポート

大量のアクティビティ ログを Azure Portal から直接ダウンロードできるようになりました。 この更新プログラムでは、次のことが可能になります。

- 最大 250,000 行をダウンロードする。

- ダウンロードが完了したら通知を受け取る。

- ファイル名をカスタマイズする。

- 出力形式 (JSON または CSV のどちらか) を決定する。

この機能の詳細については、「[クイック スタート: Azure portal を使用して監査レポートをダウンロードする](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-download-audit-report)」を参照してください。

---

### <a name="breaking-change-updates-to-condition-evaluation-by-exchange-activesync-eas"></a>重大な変更:Exchange ActiveSync (EAS) による条件評価の更新

**種類:** 変更の計画  
**サービス カテゴリ:** 条件付きアクセス  
**製品の機能:** Access Control

現在、Exchange ActiveSync (EAS) が次の条件を評価する方法を更新しているところです。

- 国、地域、または IP アドレスに基づいたユーザーの場所

- サインイン リスク

- デバイスのプラットフォーム

以前に条件付きアクセス ポリシーでこれらの条件を使用している場合は、条件動作が変更される可能性があることに注意してください。 たとえば、以前にあるポリシーでユーザーの場所の条件を使用している場合は、そのポリシーが、ユーザーの場所に基づいて省略されるようになったことに気付く可能性があります。

---

## <a name="february-2019"></a>2019 年 2 月

### <a name="configurable-azure-ad-saml-token-encryption-public-preview"></a>構成可能な Azure AD SAML トークン暗号化 (パブリック プレビュー) 

**種類:** 新機能  
**サービス カテゴリ:** エンタープライズ アプリケーション  
**製品の機能:** SSO

サポートされている SAML アプリを、暗号化された SAML トークンを受信するように構成できるようになりました。 アプリで構成および使用する場合、Azure AD は、Azure AD に格納されている証明書から取得した公開キーを使用して、出力された SAML アサーションを暗号化します。

SAML トークン暗号化を構成する方法の詳細については、「[Azure AD SAML トークン暗号化の構成](https://docs.microsoft.com/azure/active-directory/manage-apps/howto-saml-token-encryption)」を参照してください。

---

### <a name="create-an-access-review-for-groups-or-apps-using-azure-ad-access-reviews"></a>Azure AD アクセス レビューを使用してグループやアプリのアクセス レビューを作成する

**種類:** 新機能  
**サービス カテゴリ:** アクセス レビュー  
**製品の機能:** ガバナンス

グループのメンバーシップまたはアプリの割り当てについて、1 つの Azure AD アクセス レビューに複数のグループまたはアプリを含められるようになりました。 複数のグループまたはアプリを含むアクセス レビューは同じ設定を使用して設定され、含められたすべてのレビュー担当者に同時に通知されます。

Azure AD アクセス レビューを使用してアクセス レビューを作成する方法の詳細については、[Azure AD アクセス レビューでのグループまたはアプリケーションのアクセス レビューの作成](https://docs.microsoft.com/azure/active-directory/governance/create-access-review)に関するページを参照してください

---

### <a name="new-federated-apps-available-in-azure-ad-app-gallery---february-2019"></a>Azure AD アプリ ギャラリーで入手できる新しいフェデレーション アプリ - 2019 年 2 月

**種類:** 新機能  
**サービス カテゴリ:** エンタープライズ アプリケーション  
**製品の機能:** サード パーティ統合
 
2019 年 2 月に、フェデレーションがサポートされる次の 27 の新しいアプリがアプリ ギャラリーに追加されました。

[Euromonitor Passport](https://docs.microsoft.com/azure/active-directory/saas-apps/euromonitor-passport-tutorial)、[MindTickle](https://docs.microsoft.com/azure/active-directory/saas-apps/mindtickle-tutorial)、[FAT FINGER](https://seeforgetest-exxon.azurewebsites.net/Account/create?Length=7)、[AirStack](https://docs.microsoft.com/azure/active-directory/saas-apps/airstack-tutorial)、[Oracle Fusion ERP](https://docs.microsoft.com/azure/active-directory/saas-apps/oracle-fusion-erp-tutorial)、[IDrive](https://docs.microsoft.com/azure/active-directory/saas-apps/idrive-tutorial)、[Skyward Qmlativ](https://docs.microsoft.com/azure/active-directory/saas-apps/skyward-qmlativ-tutorial)、[Brightidea](https://docs.microsoft.com/azure/active-directory/saas-apps/brightidea-tutorial)、[AlertOps](https://docs.microsoft.com/azure/active-directory/saas-apps/alertops-tutorial)、[Soloinsight-CloudGate SSO](https://docs.microsoft.com/azure/active-directory/saas-apps/soloinsight-cloudgate-sso-tutorial)、Permission Click、[Brandfolder](https://docs.microsoft.com/azure/active-directory/saas-apps/brandfolder-tutorial)、[StoregateSmartFile](https://docs.microsoft.com/azure/active-directory/saas-apps/smartfile-tutorial)、[Pexip](https://docs.microsoft.com/azure/active-directory/saas-apps/pexip-tutorial)、[Stormboard](https://docs.microsoft.com/azure/active-directory/saas-apps/stormboard-tutorial)、[Seismic](https://docs.microsoft.com/azure/active-directory/saas-apps/seismic-tutorial)、[Share A Dream](https://www.shareadream.org/how-it-works)、[Bugsnag](https://docs.microsoft.com/azure/active-directory/saas-apps/bugsnag-tutorial)、[webMethods Integration Cloud](https://docs.microsoft.com/azure/active-directory/saas-apps/webmethods-integration-cloud-tutorial)、[Knowledge Anywhere LMS](https://docs.microsoft.com/azure/active-directory/saas-apps/knowledge-anywhere-lms-tutorial)、[OU Campus](https://docs.microsoft.com/azure/active-directory/saas-apps/ou-campus-tutorial)、[Periscope Data](https://docs.microsoft.com/azure/active-directory/saas-apps/periscope-data-tutorial)、[Netop Portal](https://docs.microsoft.com/azure/active-directory/saas-apps/netop-portal-tutorial)、[smartvid.io](https://docs.microsoft.com/azure/active-directory/saas-apps/smartvid.io-tutorial)、[PureCloud by Genesys](https://docs.microsoft.com/azure/active-directory/saas-apps/purecloud-by-genesys-tutorial)、[ClickUp Productivity Platform](https://docs.microsoft.com/azure/active-directory/saas-apps/clickup-productivity-platform-tutorial)

アプリに関する詳細については、「[SaaS アプリケーションと Azure Active Directory の統合](https://aka.ms/appstutorial)」を参照してください。 アプリケーションの Azure AD アプリ ギャラリーでの公開に関する詳細については、「[アプリケーションを Azure Active Directory アプリケーション ギャラリーで公開する](https://aka.ms/azureadapprequest)」を参照してください。

---

### <a name="enhanced-combined-mfasspr-registration"></a>拡張された MFA と SSPR の統合登録

**種類:** 変更された機能  
**サービス カテゴリ:** セルフサービスによるパスワードのリセット  
**製品の機能:** ユーザー認証

お客様からのフィードバックに基づき、MFA と SSPR の統合登録のプレビュー版の機能を強化して、ユーザーが MFA と SSPR の両方のセキュリティ情報をより迅速に登録できるようにしました。 

**ユーザーがこの強化された機能を今すぐ利用できるようにするには、以下の手順を実行してください。**

1. グローバル管理者またはユーザー管理者として Azure portal にサインインし、 **[Azure Active Directory] > [ユーザー設定] > [アクセス パネル プレビュー機能の設定を管理]** の順に移動します。 

2. **[ユーザーはセキュリティ情報の登録と管理のためにプレビュー機能を使用できます – 更新]** オプションで、この機能を有効にする対象として **[選択したユーザー グループ]** または **[すべてのユーザー]** を選択します。

今後数週間のうちに、現時点で有効にされていない MFA/SSPR の古い統合登録 のプレビュー版の機能を有効にできないようにする予定です。

**ご使用のテナントで対象コントロールが削除されるかどうかを確認するには、次の手順を実行します。**

1. グローバル管理者またはユーザー管理者として Azure portal にサインインし、 **[Azure Active Directory] > [ユーザー設定] > [アクセス パネル プレビュー機能の設定を管理]** の順に移動します。  

2. **[ユーザーはセキュリティ情報の登録と管理のためにプレビュー機能を使用できます]** オプションを **[なし]** に設定すると、このオプションがテナントから削除されます。

以前に MFA/SSPR の古い統合登録のプレビュー版の機能をユーザーに対して有効にしたかどうかに関係なく、古い機能は今後無効になる予定です。 そのため、可能なかぎり早急に、強化された新しい機能に移行することをお勧めします。

強化された登録機能の詳細については、[Azure AD の MFA とパスワードのリセットの統合登録エクスペリエンスに関する優れた拡張内容](https://techcommunity.microsoft.com/t5/Azure-Active-Directory-Identity/Cool-enhancements-to-the-Azure-AD-combined-MFA-and-password/ba-p/354271)に関するページを参照してください。

---

### <a name="updated-policy-management-experience-for-user-flows"></a>ユーザー フローのポリシー管理エクスペリエンスが更新されました

**種類:** 変更された機能  
**サービス カテゴリ:** B2C - コンシューマー ID 管理  
**製品の機能:** B2B/B2C

ユーザー フローに対するポリシーの作成と管理のプロセス (従来の組み込みポリシー) が簡単になるように更新しました。 この新しいエクスペリエンスがすべての Azure AD テナントに関する新しい既定になりました。

ポータル画面上部にある **[フィードバックの送信]** 領域にあるお気に入りや問題点、改善点のためのアイコンを使用して、フィードバックや提案をお送りください。

新しいポリシー管理エクスペリエンスについて詳しくは、関連するブログ記事「[Azure AD B2C に JavaScript のカスタマイズおよび多数の新機能が追加されました](https://techcommunity.microsoft.com/t5/Azure-Active-Directory-Identity/Azure-AD-B2C-now-has-JavaScript-customization-and-many-more-new/ba-p/353595)」をご覧ください。

---

### <a name="choose-specific-page-element-versions-provided-by-azure-ad-b2c"></a>Azure AD B2C によって提供される特定のページ要素のバージョンを選択する

**種類:** 新機能  
**サービス カテゴリ:** B2C - コンシューマー ID 管理  
**製品の機能:** B2B/B2C

Azure AD B2C が提供する特定のバージョンのページ要素を選択できるようになりました。 特定のバージョンを選択することで、ページに表示される前に更新をテストし、動作を予測できるようになります。 さらに、JavaScript のカスタマイズを可能にするために特定のページ バージョンを強制するように選択できるようになりました。 この機能を有効にするには、ユーザー フローの **[プロパティ]** ページにアクセスします。

特定のバージョンのページ要素を選択する方法の詳細については、関連するブログ記事「[Azure AD B2C に JavaScript のカスタマイズおよび多数の新機能が追加されました](https://techcommunity.microsoft.com/t5/Azure-Active-Directory-Identity/Azure-AD-B2C-now-has-JavaScript-customization-and-many-more-new/ba-p/353595)」をご覧ください。

---

### <a name="configurable-end-user-password-requirements-for-b2c-ga"></a>B2C の構成可能なエンドユーザーのパスワード要件 (GA)

**種類:** 新機能  
**サービス カテゴリ:** B2C - コンシューマー ID 管理  
**製品の機能:** B2B/B2C

ネイティブな Azure AD パスワード ポリシーを使用しなくても、エンド ユーザー向けの組織のパスワードの複雑さを設定できるようになりました。 ユーザー フローの **[プロパティ]** ブレード (以前の組み込みポリシー) から、パスワードの複雑度を **[簡易]** または **[強い]** のいずれかに選択できます。または、 **[カスタム]** の要件セットを作成することもできます。

パスワードの複雑度の要件構成については、「[Azure Active Directory B2C でパスワードの複雑度要件を構成する](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-password-complexity)」をご覧ください。

---

### <a name="new-default-templates-for-custom-branded-authentication-experiences"></a>カスタムのブランド化された認証エクスペリエンスの新しい既定のテンプレート

**種類:** 新機能  
**サービス カテゴリ:** B2C - コンシューマー ID 管理  
**製品の機能:** B2B/B2C

ユーザー フローの **[ページ レイアウト]** ブレードにある新しい既定のテンプレート (以前の組み込みポリシー) を使用して、ユーザー用にカスタムのブランド化された認証エクスペリエンスを作成できます。

テンプレートの使用方法については、「[Azure AD B2C に JavaScript のカスタマイズと多くの新機能が追加されました](https://techcommunity.microsoft.com/t5/Azure-Active-Directory-Identity/Azure-AD-B2C-now-has-JavaScript-customization-and-many-more-new/ba-p/353595)」をご覧ください。

---

## <a name="january-2019"></a>2019 年 1 月

### <a name="active-directory-b2b-collaboration-using-one-time-passcode-authentication-public-preview"></a>ワンタイム パスコード認証を使用した Active Directory B2B コラボレーション (パブリック プレビュー)

**種類:** 新機能  
**サービス カテゴリ:** B2B  
**製品の機能:** B2B/B2C

Azure AD、Microsoft アカウント (MSA)、Google フェデレーションなどの他の手段を使用して認証できない B2B ゲスト ユーザーのために、ワンタイム パスコード認証 (OTP) が導入されました。 この新しい認証方法により、ゲスト ユーザーは新しい Microsoft アカウントを作成せずに済みます。 代わりに、ゲスト ユーザーは、招待の利用時、または共有リソースへのアクセス時に、メール アドレスに一時コードを送信するように要求できます。 ゲスト ユーザーは、この一時コードを使用してサインインを続行できます。

詳細については、[メールによるワンタイム パスコード認証 (プレビュー)](https://docs.microsoft.com/azure/active-directory/b2b/one-time-passcode) に関するページ、および [Azure AD でアカウントを持つユーザーがシームレスに共有およびコラボレーションを行う方法](https://techcommunity.microsoft.com/t5/Azure-Active-Directory-Identity/Azure-AD-makes-sharing-and-collaboration-seamless-for-any-user/ba-p/325949)に関するブログを参照してください。

### <a name="new-azure-ad-application-proxy-cookie-settings"></a>新しい Azure AD アプリケーション プロキシの Cookie の設定

**種類:** 新機能  
**サービス カテゴリ:** アプリ プロキシ  
**製品の機能:** Access Control

アプリケーション プロキシを使用して発行されたアプリで使用可能な、次の 3 つの新しい Cookie の設定を導入しました。

- **HTTP 専用 Cookie を使用する。** アプリケーション プロキシのアクセスとセッションの Cookie に **HTTPOnly** フラグを設定します。 この設定をオンにすると、クライアント側のスクリプトによる Cookie のコピーや変更の防止に役立つといった、セキュリティに関する追加の利点が提供されます。 追加の利点を得るために、このフラグをオンにする ( **[はい]** を選択する) ことをお勧めします。

- **セキュリティで保護された Cookie を使用する。** アプリケーション プロキシのアクセスとセッションの Cookie に **Secure** フラグを設定します。 この設定をオンにすると、Cookie が HTTPS などの TLS セキュア チャネル経由でのみ送信されるようにすることで、セキュリティに関する追加の利点が提供されます。 追加の利点を得るために、このフラグをオンにする ( **[はい]** を選択する) ことをお勧めします。

- **永続的な Cookie を使用する。** Web ブラウザーが閉じているときにアクセスの Cookie が期限切れにならないようにします。 これらの Cookie は、アクセス トークンの有効期間の間、持続します。 ただし、有効期限に達した場合、またはユーザーが手動で Cookie を削除した場合、これらの Cookie はリセットされます。 既定の設定 **[いいえ]** のままにして、プロセス間で Cookie を共有しない古いアプリの設定だけをオンにすることをお勧めします。

新しい Cookie の詳細については、「[Azure Active Directory でオンプレミスのアプリケーションにアクセスするための Cookie 設定](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-configure-cookie-settings)」を参照してください。

---

### <a name="new-federated-apps-available-in-azure-ad-app-gallery---january-2019"></a>Azure AD アプリ ギャラリーで入手できる新しいフェデレーション アプリ - 2019 年 1 月

**種類:** 新機能  
**サービス カテゴリ:** エンタープライズ アプリケーション  
**製品の機能:** サード パーティ統合
 
2019 年 1 月に、フェデレーションを使用した以下の 35 の新規アプリのサポートが、アプリ ギャラリーに追加されました。

[Firstbird](https://docs.microsoft.com/azure/active-directory/saas-apps/firstbird-tutorial)、[Folloze](https://docs.microsoft.com/azure/active-directory/saas-apps/folloze-tutorial)、[Talent Palette](https://docs.microsoft.com/azure/active-directory/saas-apps/talent-palette-tutorial)、[Infor CloudSuite](https://docs.microsoft.com/azure/active-directory/saas-apps/infor-cloud-suite-tutorial)、[Cisco Umbrella](https://docs.microsoft.com/azure/active-directory/saas-apps/cisco-umbrella-tutorial)、[Zscaler Internet Access Administrator](https://docs.microsoft.com/azure/active-directory/saas-apps/zscaler-internet-access-administrator-tutorial)、[Expiration Reminder](https://docs.microsoft.com/azure/active-directory/saas-apps/expiration-reminder-tutorial)、[InstaVR Viewer](https://docs.microsoft.com/azure/active-directory/saas-apps/instavr-viewer-tutorial)、[CorpTax](https://docs.microsoft.com/azure/active-directory/saas-apps/corptax-tutorial)、[Verb](https://app.verb.net/login)、[OpenLattice](https://openlattice.com/agora)、[TheOrgWiki](https://www.theorgwiki.com/signup)、[Pavaso Digital Close](https://docs.microsoft.com/azure/active-directory/saas-apps/pavaso-digital-close-tutorial)、[GoodPractice Toolkit](https://docs.microsoft.com/azure/active-directory/saas-apps/goodpractice-toolkit-tutorial)、[Cloud Service PICCO](https://docs.microsoft.com/azure/active-directory/saas-apps/cloud-service-picco-tutorial)、[AuditBoard](https://docs.microsoft.com/azure/active-directory/saas-apps/auditboard-tutorial)、[iProva](https://docs.microsoft.com/azure/active-directory/saas-apps/iprova-tutorial)、[Workable](https://docs.microsoft.com/azure/active-directory/saas-apps/workable-tutorial)、[CallPlease](https://webapp.callplease.com/create-account/create-account.html)、[GTNexus SSO System](https://docs.microsoft.com/azure/active-directory/saas-apps/gtnexus-sso-module-tutorial)、[CBRE ServiceInsight](https://docs.microsoft.com/azure/active-directory/saas-apps/cbre-serviceinsight-tutorial)、[Deskradar](https://docs.microsoft.com/azure/active-directory/saas-apps/deskradar-tutorial)、[Coralogixv](https://docs.microsoft.com/azure/active-directory/saas-apps/coralogix-tutorial)、[Signagelive](https://docs.microsoft.com/azure/active-directory/saas-apps/signagelive-tutorial)、[ARES for Enterprise](https://docs.microsoft.com/azure/active-directory/saas-apps/ares-for-enterprise-tutorial)、[K2 for Office 365](https://www.k2.com/O365)、[Xledger](https://www.xledger.net/)、[iDiD Manager](https://docs.microsoft.com/azure/active-directory/saas-apps/idid-manager-tutorial)、[HighGear](https://docs.microsoft.com/azure/active-directory/saas-apps/highgear-tutorial)、[Visitly](https://docs.microsoft.com/azure/active-directory/saas-apps/visitly-tutorial)、[Korn Ferry ALP](https://docs.microsoft.com/azure/active-directory/saas-apps/korn-ferry-alp-tutorial)、[Acadia](https://docs.microsoft.com/azure/active-directory/saas-apps/acadia-tutorial)、[Adoddle cSaas Platform](https://docs.microsoft.com/azure/active-directory/saas-apps/adoddle-csaas-platform-tutorial)<!-- , [CaféX Portal (Meetings)](https://docs.microsoft.com/azure/active-directory/saas-apps/cafexportal-meetings-tutorial), [MazeMap Link](https://docs.microsoft.com/azure/active-directory/saas-apps/mazemaplink-tutorial)-->  

アプリに関する詳細については、「[SaaS アプリケーションと Azure Active Directory の統合](https://aka.ms/appstutorial)」を参照してください。 アプリケーションの Azure AD アプリ ギャラリーでの公開に関する詳細については、「[アプリケーションを Azure Active Directory アプリケーション ギャラリーで公開する](https://aka.ms/azureadapprequest)」を参照してください。

---

### <a name="new-azure-ad-identity-protection-enhancements-public-preview"></a>新しい Azure AD Identity Protection の機能強化 (パブリック プレビュー)

**種類:** 変更された機能  
**サービス カテゴリ:** Identity Protection  
**製品の機能:** ID のセキュリティ & 保護

Azure AD Identity Protection のパブリック プレビュー オファリングに、以下の機能強化が追加されたことを発表いたします。

- ユーザー インターフェイスが更新され、さらに統合されました

- 追加の API

- 機械学習によるリスク評価が強化されました

- リスクの高いユーザーとリスクの高いサインインの間での製品全体の配置

機能強化の詳細については、[Azure Active Directory Identity Protection (更新済み) の概要](https://aka.ms/IdentityProtectionDocs)に関するページを参照してください。 製品内のプロンプトを介して、詳しく学習することや自分の考えを共有することができます。

---

### <a name="new-app-lock-feature-for-the-microsoft-authenticator-app-on-ios-and-android-devices"></a>iOS および Android デバイスの Microsoft Authenticator アプリのアプリ ロックの新機能

**種類:** 新機能  
**サービス カテゴリ:** Microsoft Authenticator アプリ  
**製品の機能:** ID のセキュリティ & 保護

ワンタイム パスコード、アプリの情報、アプリの設定のセキュリティを強化するには、Microsoft Authenticator アプリのアプリ ロック機能をオンにします。 アプリ ロック機能をオンにすることは、Microsoft Authenticator アプリを開くたびに、PIN または生体認証を使用した認証を求められることを意味します。

詳細については、「[Microsoft Authenticator アプリに関する FAQ](https://docs.microsoft.com/azure/active-directory/user-help/microsoft-authenticator-app-faq)」を参照してください。

---

### <a name="enhanced-azure-ad-privileged-identity-management-pim-export-capabilities"></a>Azure AD Privileged Identity Management (PIM) のエクスポート機能の強化

**種類:** 新機能  
**サービス カテゴリ:** Privileged Identity Management  
**製品の機能:** Privileged Identity Management

Privileged Identity Management (PIM) の管理者が、すべての子リソースのロールの割り当てを含む、特定のリソースのすべてのアクティブで適格なロールの割り当てをエクスポートできるようになりました。 以前は、管理者がサブスクリプションに対するロールの割り当ての完全な一覧を取得するは困難で、特定のリソースごとにロールの割り当てをエクスポートする必要がありました。

詳細については、[PIM での Azure リソース ロールのアクティビティおよび監査履歴の表示](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/azure-pim-resource-rbac)に関するページを参照してください。

---

## <a name="novemberdecember-2018"></a>2018 年 11 月/12 月

### <a name="users-removed-from-synchronization-scope-no-longer-switch-to-cloud-only-accounts"></a>同期範囲から削除されたユーザーがクラウド専用アカウントに切り替わらない

**種類:** 固定  
**サービス カテゴリ:** [ユーザー管理]  
**製品の機能:** Directory

>[!Important]
>この修正についてご意見をいただき、ご迷惑をおかけしていることをよく理解しております。 このため、お客様の組織に変更を簡単に導入できるようになるまで、この変更は元に戻しました。

Active Directory Domain Services (AD DS) オブジェクトが同期範囲から除外され、後続の同期周期で Azure AD のごみ箱に移動されると、ユーザーの DirSyncEnabled フラグが間違って **False** に切り替わるバグを修正しました。 この修正の結果、ユーザーが同期範囲から除外され、その後、Azure AD のごみ箱から復元された場合、予想どおり、ユーザー アカウントはオンプレミス AD との同期を維持します。また、その権限ソース (SoA) がオンプレミス AD のままなので、クラウドで管理できません。

この修正の前は、DirSyncEnabled フラグが False に切り替わるという問題がありました。 これらのアカウントがクラウド専用オブジェクトに変換された、アカウントをクラウドで管理できるという間違った印象を与えました。 しかしながら、アカウントの SoA はオンプレミスのままであり、同期されるプロパティ (シャドウ属性) はすべてオンプレミス AD から届きます。 この状態は Azure AD とその他のクラウド ワークロードでさまざまな問題を引き起こしました。これらのアカウントは AD と同期しているものとして処理されるはずですが、クラウド専用アカウントのように動作しました。

現時点では、AD 同期アカウントをクラウド専用アカウントに実際に変換する唯一の方法はテナント レベルで DirSync を無効にし、SoA を転送するバックエンド操作をトリガーすることです。 この種の SoA 変更では、オンプレミス関連の属性 (LastDirSyncTime やシャドウ属性など) をすべて消去する必要があり、また、他のクラウド ワークロードに信号を送り、個々のオブジェクトもクラウド専用アカウントに変換させる必要があります (ただし、これらに限定されません)。

結果的に、今回の修正によって、一部のシナリオでは過去に必須でしたが、AD と同期しているユーザーの ImmutableID 属性を直接更新することが回避されます。 仕様では、Azure AD のオブジェクトの ImmutableID はその名前が示すように不変であることを意図しています。 Azure AD Connect Health と Azure AD Connect Synchronization クライアントで導入された新機能で次のようなシナリオに対処できます。

- **多数のユーザーを対象に大規模な ImmutableID 更新を段階的に行う**
  
  たとえば、時間のかかる AD DS フォレスト間移行を行う必要があります。 解決方法:Azure AD Connect を使用し、**ソース アンカーを構成**します。また、ユーザーが移行するとき、Azure AD からローカル AD DS ユーザーの新しいフォレストの ms-DS-Consistency-Guid 属性に既存の ImmutableID 値をコピーします。 詳細については、「[sourceAnchor としての ms-DS-ConsistencyGuid の使用](/azure/active-directory/hybrid/plan-connect-design-concepts#using-ms-ds-consistencyguid-as-sourceanchor)」を参照してください。

- **多数のユーザーを対象に大規模な ImmutableID 更新を一度に行う**

  たとえば、Azure AD Connect の導入中、設定を間違え、SourceAnchor 属性を変更しなければなりません。 解決方法:テナント レベルで DirSync を無効にし、無効な ImmutableID 値をすべて消去します。 詳しくは、「[Office 365 のディレクトリ同期を無効にする](/office365/enterprise/turn-off-directory-synchronization)」をご覧ください。

- **オンプレミス ユーザーと Azure AD の既存ユーザーを再度組み合わせる** たとえば、AD DS でユーザーが再作成された場合、Azure AD の既存アカウントと再度組み合わされず、重複する Azure AD アカウントが生成されます (孤立オブジェクト)。 解決方法:Azure portal の Azure AD Connect Health を使用し、ソース アンカー/ImmutableID のマッピングをやり直します。 詳細については、「[孤立したオブジェクトのシナリオ](/azure/active-directory/hybrid/how-to-connect-health-diagnose-sync-errors#orphaned-object-scenario)」を参照してください。

### <a name="breaking-change-updates-to-the-audit-and-sign-in-logs-schema-through-azure-monitor"></a>重大な変更:Azure Monitor を通じた監査およびサインイン ログ スキーマの更新

**種類:** 変更された機能  
**サービス カテゴリ:** レポート  
**製品の機能:** 監視とレポート

現在、監査とサインインのログ ストリームはどちらも Azure Monitor を通じて公開していますので、お使いの SIEM ツールや Log Analytics とログ ファイルをシームレスに統合できます。 お客様のフィードバックに基づき、またこの機能の一般提供の発表に備えて、次の変更がスキーマに加えられます。 これらのスキーマ変更と関連ドキュメントの更新は 1 月の第 1 週までに行われる予定です。

#### <a name="new-fields-in-the-audit-schema"></a>監査スキーマの新しいフィールド
リソースに対して実行される操作の種類を提供するために、新しい **[操作の種類]** フィールドが追加されます。 たとえば、 **[追加]** 、 **[更新]** 、 **[削除]** などです。

#### <a name="changed-fields-in-the-audit-schema"></a>監査スキーマの変更されるフィールド
監査スキーマの次のフィールドが変更されます:

|フィールド名|変更箇所|古い値|新しい値|
|----------|------------|----------|----------|
|Category|以前は **[サービス名]** フィールドでした。 現在は **[監査カテゴリ]** フィールドです。 **[サービス名]** は **loggedByService** フィールドに名前が変更されました。|<ul><li>アカウント プロビジョニング</li><li>Core Directory (コア ディレクトリ)</li><li>セルフサービスのパスワード リセット</li></ul>|<ul><li>[ユーザー管理]</li><li>グループ管理</li><li>アプリの管理</li></ul>|
|targetResources|**TargetResourceType** を最上位レベルに含みます。|&nbsp;|<ul><li>ポリシー</li><li>アプリ</li><li>User</li><li>Group</li></ul>|
|loggedByService|監査ログを生成したサービスの名前を提供します。|Null|<ul><li>アカウント プロビジョニング</li><li>Core Directory (コア ディレクトリ)</li><li>セルフサービスのパスワード リセット</li></ul>|
|結果|監査ログの結果を提供します。 以前は、これは列挙されていましたが、実際の値を示すようになります。|<ul><li>0</li><li>1</li></ul>|<ul><li>Success</li><li>失敗</li></ul>|

#### <a name="changed-fields-in-the-sign-in-schema"></a>サインイン スキーマの変更されるフィールド
サインイン スキーマの次のフィールドが変更されます:

|フィールド名|変更箇所|古い値|新しい値|
|----------|------------|----------|----------|
|appliedConditionalAccessPolicies|これは **conditionalaccessPolicies** フィールドでした。 現在は **appliedConditionalAccessPolicies** フィールドです。|変更なし|変更なし|
|conditionalAccessStatus|サインイン時点の条件付きアクセス ポリシー ステータスの結果を提供します。 以前は、これは列挙されていましたが、実際の値を示すようになります。|<ul><li>0</li><li>1</li><li>2</li><li>3</li></ul>|<ul><li>Success</li><li>失敗</li><li>未適用</li><li>Disabled</li></ul>|
|appliedConditionalAccessPolicies: 結果|サインイン時点の個別の条件付きアクセス ポリシー ステータスの結果を提供します。 以前は、これは列挙されていましたが、実際の値を示すようになります。|<ul><li>0</li><li>1</li><li>2</li><li>3</li></ul>|<ul><li>Success</li><li>失敗</li><li>未適用</li><li>Disabled</li></ul>|

スキーマの詳細については、「[Azure Monitor の Azure AD 監査ログ スキーマを解釈する (プレビュー)](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-azure-monitor-audit-log-schema)」を参照してください。

---

### <a name="identity-protection-improvements-to-the-supervised-machine-learning-model-and-the-risk-score-engine"></a>Identity Protection の教師あり機械学習モデルとリスク スコア エンジンの機能強化

**種類:** 変更された機能  
**サービス カテゴリ:** Identity Protection  
**製品の機能:** リスク スコア

Identity Protection に関連した、ユーザーおよびサインインのリスク評価エンジンの機能強化により、ユーザー リスクの精度とカバレッジを向上させることができます。 管理者にとっての注目点は、ユーザーのリスク レベルが特定の検出のリスク レベルに直接リンクされなくなったことと、リスクの高いサインイン イベントの数とレベルが増加していることです。

ユーザーのサインインと検出のパターンの追加機能を使用してユーザーのリスクを計算する、教師ありの機械学習モデルによってリスクの検出が評価されるようになりました。 ユーザーに関連付けられた検出のリスクが低または中の場合でも、このモデルに基づいて、管理者はリスク スコアの高いユーザーを見つけることができます。 

---

### <a name="administrators-can-reset-their-own-password-using-the-microsoft-authenticator-app-public-preview"></a>管理者が Microsoft Authenticator アプリ (パブリック プレビュー) を使用して自分自身のパスワードをリセット可能

**種類:** 変更された機能  
**サービス カテゴリ:** セルフサービスによるパスワードのリセット  
**製品の機能:** ユーザー認証

Azure AD 管理者は、Microsoft Authenticator アプリの通知や、任意のモバイル認証アプリまたはハードウェア トークンのコードを使用して、自分自身のパスワードをリセットできるようになりました。 自分自身のパスワードをリセットするために、管理者は次の方法のうちの 2 つを使用できるようになります:

- Microsoft Authenticator アプリの通知

- その他のモバイル認証アプリ/ハードウェア トークンのコード

- Email

- 音声通話

- テキスト メッセージ

Microsoft Authenticator アプリを使用したパスワードのリセットの詳細については、[Azure AD のセルフサービスでのパスワード リセット - モバイル アプリと SSPR (プレビュー)](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-howitworks#mobile-app-and-sspr-preview) に関するページを参照してください。

---

### <a name="new-azure-ad-cloud-device-administrator-role-public-preview"></a>新しい Azure AD Cloud Device Administrator ロール (パブリック プレビュー)

**種類:** 新機能  
**サービス カテゴリ:** デバイスの登録と管理  
**製品の機能:** アクセス制御

クラウド デバイス管理タスクを実行するために、管理者はユーザーを新しい Cloud Device Administrator ロールに割り当てることができます。 Cloud Device Administrators ロールを割り当てられたユーザーは、Azure AD でデバイスを有効化、無効化、削除できることに加えて、Azure portal で Windows 10 の BitLocker キー (ある場合) を読み取ることができます。

ロールとアクセス許可の詳細については、「[Azure Active Directory の管理者ロールの割り当て](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)」を参照してください

---

### <a name="manage-your-devices-using-the-new-activity-timestamp-in-azure-ad-public-preview"></a>Azure AD で新しいアクティビティ タイムスタンプを使用してデバイスを管理する (パブリック プレビュー)

**種類:** 新機能  
**サービス カテゴリ:** デバイスの登録と管理  
**製品の機能:** デバイスのライフサイクル管理

Azure AD では、古くなったデバイスを環境から排除するために、定期的に組織のデバイスを更新したり、インベントリから削除したりする必要があります。 このプロセスを支援するために、Azure AD では、新しいアクティビティ タイムスタンプによってデバイスが更新されることで、デバイスのライフサイクルが管理しやすくなりました。

このタイムスタンプを取得および使用する方法については、「[方法:Azure AD で古いデバイスを管理する](https://docs.microsoft.com/azure/active-directory/devices/manage-stale-devices)」を参照してください

---

### <a name="administrators-can-require-users-to-accept-a-terms-of-use-on-each-device"></a>管理者が各デバイスで利用規約の承諾をユーザーに要求可能

**種類:** 新機能  
**サービス カテゴリ:** 使用条件  
**製品の機能:** ガバナンス
 
管理者は **[各デバイスでユーザーによる同意が必要]** オプションを有効にすることで、テナントでユーザーが使用しているすべてのデバイスで利用規約の承諾をユーザーに要求できるようになりました。

詳細については、[Azure Active Directory Terms of Use 機能の、デバイスごとの利用規約に関するセクション](https://docs.microsoft.com/azure/active-directory/conditional-access/terms-of-use#per-device-terms-of-use)を参照してください。

---

### <a name="administrators-can-configure-a-terms-of-use-to-expire-based-on-a-recurring-schedule"></a>管理者が定期的なスケジュールに基づいて利用規約の有効期限を設定可能

**種類:** 新機能  
**サービス カテゴリ:** 使用条件  
**製品の機能:** ガバナンス
 

管理者は **[期限切れの同意]** オプションを有効にすることで、すべてのユーザーを対象に、利用規約の有効期限を指定の定期スケジュールに基づいて設定できるようになりました。 年に 1 回、半年に 1 回、3 か月に 1 回、または月に 1 回のスケジュールを指定できます。 利用規約が期限切れになったら、ユーザーは再度受け入れる必要があります。

詳細については、[Azure Active Directory Terms of Use 機能の、利用規約の追加に関するセクション](https://docs.microsoft.com/azure/active-directory/conditional-access/terms-of-use#add-terms-of-use)を参照してください。

---

### <a name="administrators-can-configure-a-terms-of-use-to-expire-based-on-each-users-schedule"></a>管理者が各ユーザーのスケジュールに基づいて利用規約の有効期限を設定可能

**種類:** 新機能  
**サービス カテゴリ:** 使用条件  
**製品の機能:** ガバナンス

管理者は、ユーザーが利用規約を再承諾しなければならない期間を指定できるようになりました。 たとえば、管理者は、ユーザーが 90 日おきに利用規約を再承諾しなければならないことを指定できます。

詳細については、[Azure Active Directory Terms of Use 機能の、利用規約の追加に関するセクション](https://docs.microsoft.com/azure/active-directory/conditional-access/terms-of-use#add-terms-of-use)を参照してください。
 
---

### <a name="new-azure-ad-privileged-identity-management-pim-emails-for-azure-active-directory-roles"></a>Azure Active Directory のロールに関する新しい Azure AD Privileged Identity Management (PIM) の電子メール

**種類:** 新機能  
**サービス カテゴリ:** Privileged Identity Management  
**製品の機能:** Privileged Identity Management
 
Azure AD Privileged Identity Management (PIM) を使用しているお客様は、過去 7 日間の次の情報を含むダイジェスト電子メールを毎週受信できるようになりました:

- 最上位の有資格かつ永続的なロール割り当ての概要

- ロールをアクティブ化しているユーザー数

- PIM でロールに割り当てられたユーザー数

- PIM 外でロールに割り当てられたユーザー数

- PIM で "永続化" されたユーザー数

PIM と利用可能な電子メール通知の詳細については、「[PIM での電子メール通知](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-email-notifications)」を参照してください。

---

### <a name="group-based-licensing-is-now-generally-available"></a>グループベースのライセンスの一般提供開始

**種類:** 変更された機能  
**サービス カテゴリ:** その他  
**製品の機能:** Directory

グループベースのライセンスのパブリック プレビューが終了し、一般提供が開始されました。 この一般向けリリースの一環として、この機能のスケーラビリティの向上に加えて、単一ユーザーへのグループベースのライセンス割り当てを再処理できるようになり、Office 365 E3/A3 ライセンスでグループベースのライセンスが使用できるようになりました。

グループベースのライセンスの詳細については、「[Azure Active Directory のグループベースのライセンスとは](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal)」を参照してください。

---

### <a name="new-federated-apps-available-in-azure-ad-app-gallery---november-2018"></a>Azure AD アプリ ギャラリーで入手できる新しいフェデレーション アプリ - 2018 年 11 月

**種類:** 新機能  
**サービス カテゴリ:** エンタープライズ アプリケーション  
**製品の機能:** サード パーティ統合
 
2018 年 11 月に、フェデレーションを使用した以下の 26 の新規アプリのサポートが、アプリ ギャラリーに追加されました:

[CoreStack](https://cloud.corestack.io/site/login)、[HubSpot](https://docs.microsoft.com/azure/active-directory/saas-apps/HubSpot-tutorial)、[GetThere](https://docs.microsoft.com/azure/active-directory/saas-apps/getthere-tutorial)、[Gra-Pe](https://docs.microsoft.com/azure/active-directory/saas-apps/grape-tutorial)、[eHour](https://getehour.com/try-now)、[Consent2Go](https://docs.microsoft.com/azure/active-directory/saas-apps/Consent2Go-tutorial)、[Appinux](https://docs.microsoft.com/azure/active-directory/saas-apps/appinux-tutorial)、[DriveDollar](https://azuremarketplace.microsoft.com/marketplace/apps/savitas.drivedollar-azuread?tab=Overview)、[Useall](https://docs.microsoft.com/azure/active-directory/saas-apps/useall-tutorial)、[Infinite Campus](https://docs.microsoft.com/azure/active-directory/saas-apps/infinitecampus-tutorial)、[Alaya](https://alayagood.com/en/demo/)、[HeyBuddy](https://docs.microsoft.com/azure/active-directory/saas-apps/heybuddy-tutorial)、[Wrike SAML](https://docs.microsoft.com/azure/active-directory/saas-apps/wrike-tutorial)、[Drift](https://docs.microsoft.com/azure/active-directory/saas-apps/drift-tutorial)、[Zenegy for Business Central 365](https://accounting.zenegy.com/)、[Everbridge Member Portal](https://docs.microsoft.com/azure/active-directory/saas-apps/everbridge-tutorial)、[IDEO](https://profile.ideo.com/users/sign_up)、[Ivanti Service Manager (ISM)](https://docs.microsoft.com/azure/active-directory/saas-apps/ivanti-service-manager-tutorial)、[Peakon](https://docs.microsoft.com/azure/active-directory/saas-apps/peakon-tutorial)、[Allbound SSO](https://docs.microsoft.com/azure/active-directory/saas-apps/allbound-sso-tutorial)、[Plex Apps - Classic Test](https://test.plexonline.com/signon)、[Plex Apps – Classic](https://www.plexonline.com/signon)、[Plex Apps - UX Test](https://test.cloud.plex.com/sso)、[Plex Apps – UX](https://cloud.plex.com/sso)、[Plex Apps – IAM](https://accounts.plex.com/)、[CRAFTS - Childcare Records, Attendance, & Financial Tracking System](https://getcrafts.ca/craftsregistration) 

アプリに関する詳細については、「[SaaS アプリケーションと Azure Active Directory の統合](https://aka.ms/appstutorial)」を参照してください。 アプリケーションの Azure AD アプリ ギャラリーでの公開に関する詳細については、「[アプリケーションを Azure Active Directory アプリケーション ギャラリーで公開する](https://aka.ms/azureadapprequest)」を参照してください。

---