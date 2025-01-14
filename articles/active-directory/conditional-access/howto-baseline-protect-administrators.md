---
title: 'ベースライン ポリシー: 管理者に MFA を要求する - Azure Active Directory'
description: 管理者の多要素認証を要求する条件付きアクセス ポリシー
services: active-directory
ms.service: active-directory
ms.subservice: conditional-access
ms.topic: conceptual
ms.date: 05/16/2019
ms.author: joflore
author: MicrosoftGuyJFlo
manager: daveba
ms.reviewer: calebb, rogoya
ms.collection: M365-identity-device-management
ms.openlocfilehash: a1ce48126c3e8867ac7f2696d8cf7db992a9a60a
ms.sourcegitcommit: 13cba995d4538e099f7e670ddbe1d8b3a64a36fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "66003547"
---
# <a name="baseline-policy-require-mfa-for-admins"></a>ベースライン ポリシー:Require MFA for admins \(管理者に MFA を要求する\)

特権アカウントにアクセスできるユーザーは、環境に無制限にアクセスできます。 これらのアカウントには権限があるので、特別な注意を払って対処する必要があります。 特権アカウントの保護を向上するための一般的な方法の 1 つは、特権アカウントがサインインに使用されるときに、強力な形式のアカウント検証を必須にすることです。 Azure Active Directory では、多要素認証 (MFA) を必須にすることで、アカウント検証を強力にすることができます。

**管理者の MFA を要求する** は、次のいずれかの特権管理者ロールがサインインするたびに MFA を必要とする[ベースライン ポリシー](concept-baseline-protection.md)です。

* 全体管理者
* SharePoint 管理者
* Exchange 管理者
* 条件付きアクセス管理者
* セキュリティ管理者
* ヘルプデスク管理者/パスワード管理者
* 課金管理者
* ユーザー管理者

管理者に MFA を要求するポリシーを有効にすると、上記の 9 つの管理者ロールは Authenticator アプリを使用して、MFA を登録する必要があります。 MFA の登録が完了すると、管理者はサインインするたびに MFA を実行する必要があります。

![管理者に MFA を要求するベースライン ポリシー](./media/howto-baseline-protect-administrators/baseline-policy-require-mfa-for-admins.png)

## <a name="deployment-considerations"></a>デプロイに関する考慮事項

**管理者に MFA を要求する**ポリシーは、すべての重要な管理者に適用されます。したがって、デプロイが確実かつスムーズに行われるようにするための考慮事項がいくつかあります。 たとえば、MFA を実行できない、または実行すべきではないユーザーやサービス プリンシパルを Azure AD で特定する、ご自身の組織で使用されている先進認証に対応していないアプリケーションやクライアントを特定する、といった考慮事項です。

### <a name="legacy-protocols"></a>レガシ プロトコル

レガシ認証プロトコル (IMAP、SMTP、POP3 など) は、認証要求を行うためにメール クライアントによって使用されます。 これらのプロトコルは、MFA をサポートしていません。 Microsoft によって確認されているアカウントのセキュリティ侵害のほとんどでは、攻撃者がレガシ プロトコルを攻撃することによって MFA のバイパスを試みています。 管理アカウントにログインするときに確実に MFA を要求し、攻撃者が MFA をバイパスできないようにするために、このポリシーは、レガシ プロトコルから管理者アカウントに対して行われるすべての認証要求をブロックします。

> [!WARNING]
> このポリシーを有効にする前に、管理者がレガシ認証プロトコルを使用していないことを確認してください。 詳しくは、[条件付きアクセスを利用して Azure AD へのレガシ認証をブロックする方法](howto-baseline-protect-legacy-auth.md#identify-legacy-authentication-use)に関する記事を参照してください。

### <a name="user-exclusions"></a>ユーザーの除外

このベースライン ポリシーには、ユーザーを対象外とするオプションが用意されています。 ご自身のテナントのポリシーを有効にする前に、次のアカウントを対象外とすることをお勧めします。

* **緊急アクセス用**アカウントまたは**非常用**アカウント。テナント全体でアカウントがロックアウトされるのを防ぎます。 発生する可能性は低いシナリオですが、すべての管理者がテナントからロックアウトされた場合に、ご自身の緊急アクセス用管理アカウントを使用してテナントにログインし、アクセスを復旧する手順を実行できます。
   * 詳細については、「[Azure AD で緊急アクセス用アカウントを管理する](../users-groups-roles/directory-emergency-access.md)」を参照してください。
* **サービス アカウント**と**サービス プリンシパル** (Azure AD Connect 同期アカウントなど)。 サービス アカウントは、特定のユーザーに関連付けられていない非対話型のアカウントです。 通常、バックエンド サービスで使用され、アプリケーションへのプログラムによるアクセスが許可されます。 プログラムでは MFA を完了できないため、サービス アカウントは対象外とする必要があります。
   * これらのアカウントがスクリプトまたはコードで使用されている組織の場合は、 [マネージド ID](../managed-identities-azure-resources/overview.md) に置き換えることを検討してください。 これらの特定のアカウントは、一時的な回避策として、ベースライン ポリシーの対象外にすることができます。
* スマートフォンを持っていない、または使用できないユーザー。
   * このポリシーでは、管理者が Microsoft Authenticator アプリを使用して MFA 登録を行う必要があります。

## <a name="enable-the-baseline-policy"></a>ベースライン ポリシーを有効にする

ポリシー **[Baseline policy: Require MFA for admins]\(ベースライン ポリシー: 管理者に MFA を要求する\)** ポリシーは事前構成され、Azure portal の [条件付きアクセス] ブレードに移動すると上部に表示されます。

このポリシーを有効にして管理者を保護するには:

1.  **Azure portal**  にグローバル管理者、セキュリティ管理者、または条件付きアクセス管理者としてサインインします。
1. **[Azure Active Directory]**  >  **[条件付きアクセス]** の順に移動します。
1. ポリシーの一覧で、 **[Baseline policy: Require MFA for admins]\(ベースライン ポリシー: 管理者に MFA を要求する\)** をクリックします。
1. **[ポリシーを有効にする]** を **[ポリシーをすぐに使用する]** に設定します。
1. **[ユーザー]**  >  **[対象外とするユーザーの選択]** の順にクリックし、対象外とする必要があるユーザーを選択して、ユーザーの除外すべてを追加します。 **[選択]** 、 **[完了]** の順にクリックします。
1.  **[保存]** をクリックします。

## <a name="next-steps"></a>次の手順

詳細については、次を参照してください。

* [条件付きアクセス ベースライン保護ポリシー](concept-baseline-protection.md)
* [ID インフラストラクチャをセキュリティ保護する 5 つのステップ](../../security/azure-ad-secure-steps.md)
* [Azure Active Directory の条件付きアクセスとは](overview.md)
