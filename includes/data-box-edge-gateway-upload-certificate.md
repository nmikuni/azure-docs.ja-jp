---
author: alkohli
ms.service: databox
ms.topic: include
ms.date: 04/23/2019
ms.author: alkohli
ms.openlocfilehash: d7a9923d5bd9e357bcd75fae6e0a7d1bcd437a53
ms.sourcegitcommit: 3e98da33c41a7bbd724f644ce7dedee169eb5028
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2019
ms.locfileid: "67181632"
---
適切な SSL 証明書により、暗号化された情報が適切なサーバーに確実に送信されます。 暗号化だけでなく、証明書により認証もできます。 デバイスの PowerShell インターフェイス経由で、信頼された独自の SSL 証明書をアップロードすることができます。

1. [PowerShell インターフェイスに接続する](#connect-to-the-powershell-interface)。
2. `Set-HcsCertificate` コマンドレットを使用して証明書をアップロードします。 入力を求められたら、次のパラメーターを指定します。

   - `CertificateFilePath` - *.pfx* 形式の証明書を含む共有へのパス。
   - `CertificatePassword` - 証明書を保護するために使用するパスワード。
   - `Credentials` - 証明書を含む共有にアクセスするためのユーザー名とパスワード。

     このコマンドレットの使用例を次に示します。

     ```
     Set-HcsCertificate -Scope LocalWebUI -CertificateFilePath "\\myfileshare\certificates\mycert.pfx" -CertificatePassword "mypassword" -Credential "Username/Password"
     ```

