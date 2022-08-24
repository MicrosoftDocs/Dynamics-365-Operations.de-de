---
title: Fehlerbehebung bei Einrichtungs- und Installationsproblemen von Store Commerce
description: In diesem Artikel wird erläutert, wie Sie Einrichtungs‑ und Installationsprobleme in der Microsoft Dynamics 365 Commerce Store Commerce-App beheben.
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: e3d115e84af1aaf5266eff6588ca6996a333e51a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286329"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>Fehlerbehebung bei Einrichtungs- und Installationsproblemen von Store Commerce

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie Einrichtungs‑ und Installationsprobleme in der Microsoft Dynamics 365 Commerce Store Commerce-App beheben.

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>Ich kann die App nicht aktivieren und erhalte eine Verbindungsfehlermeldung

Nachdem Sie die gültige Cloud Point of Sale (CPOS)-URL eingegeben haben, erhalten Sie möglicherweise eine Verbindungsfehlermeldung, die dem folgenden Beispiel ähnelt:

> Es ist ein Verbindungsfehler aufgetreten und Ihr Gerät kann keine Verbindung zum CPOS herstellen. Die eingegebene CPOS-URL kann einige Probleme aufweisen.

Überprüfen Sie in diesem Fall die URL auf Tippfehler oder stellen Sie fest, ob CPOS nicht erreichbar ist, weil es offline ist.

Stellen Sie außerdem sicher, dass die Version der Cloud Scale Unit (CSU) 10.0.25 (9.35 ist.\*.\*) oder später. CPOS-Version 10.0.25 oder höher ist erforderlich, um die Store Commerce-App zu verwenden.

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>Ich kann die App nicht installieren, weil Modern POS bereits installiert ist

Während der Installation erhalten Sie möglicherweise eine Fehlermeldung, wie im folgenden Beispiel:

> Eine Version (9.\*.\*.\*) dieses Produkts (Modern POS) wurde zuvor über das Legacy-Installationsprogramm installiert.

Um den Fehler zu beheben, müssen Sie die Modern Point of Sale (MPOS)-App für alle Benutzer auf dem Computer deinstallieren und es dann erneut versuchen. Sie können bestätigen, ob MPOS für alle Benutzer entfernt wurde, indem Sie den folgenden PowerShell-Befehl ausführen.

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>Ich kann die App aufgrund einer ungültigen URL oder eines Fehlerstatus nicht aktivieren

Wenn die von Ihnen eingegebene CPOS-URL nicht gültig ist und Sie sie ändern möchten oder wenn sich die Store Commerce-App während der Aktivierung in einem Fehlerzustand befindet, können Sie den Vorgang neu starten, indem Sie die App zurücksetzen. Die Store Commerce-App speichert nur eine gültige CPOS-URL.

Führen Sie die folgenden Schritte aus, um die Store Commerce-App zurückzusetzen.

1. Auf dem Fenstermenü **Start** halten Sie die App gedrückt (oder klicken Sie mit der rechten Maustaste darauf) und wählen Sie dann **Mehr \> App Einstellungen** aus.
2. Scrollen Sie auf der Seite mit den App-Einstellungen nach unten, bis Sie die Schaltfläche **Zurücksetzen** finden.
3. Wählen Sie **Zurücksetzen** aus. Wenn Sie dann aufgefordert werden, bestätigen Sie, dass Sie die App zurücksetzen möchten.
