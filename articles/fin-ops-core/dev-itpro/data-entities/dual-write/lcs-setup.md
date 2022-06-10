---
title: Einrichtung von dualem Schreiben aus Lifecycle Services
description: In diesem Thema wird erläutert, wie Sie eine Verbindung für duales Schreiben über Microsoft Dynamics Lifecycle Services (LCS) einrichten.
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 53e82fbf8cff834c9eb0d14a0597561158b85fa1
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783200"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Einrichtung von dualem Schreiben aus Lifecycle Services

[!include [banner](../../includes/banner.md)]



In diesem Thema wird erläutert, wie Sie eine Verbindung für duales Schreiben über Microsoft Dynamics Lifecycle Services (LCS) aktivieren.

## <a name="prerequisites"></a>Voraussetzungen

Der Debitor muss die Power Platform-Integration wie in den folgenden Themen beschrieben durchführen:

- Wenn Sie Microsoft Power Platform noch nicht verwenden und Ihre Finanz- und Betriebs-Umgebungen um Funktionalitäten der Plattform erweitern möchten, lesen Sie [Power Platform Integration - Während der Bereitstellung der Umgebung aktivieren](../../power-platform/enable-power-platform-integration.md#enable-during-deploy).
- Wenn Sie bereits Dataverse- und Power Platform-Umgebungen haben und diese mit Finanz- und Betriebs-Umgebungen verbinden möchten, lesen Sie [Power Platform-Integration - Aktivieren nach Bereitstellen der Umgebung](../../power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>Dual-write für neue oder bestehende Dataverse-Umgebungen festlegen

Befolgen Sie diese Schritte, um duales Schreiben von der LCS -Seite **Umgebungsdetails** einzurichten:

1. Auf der Seite **Umgebungsdetails** erweitern Sie den Abschnitt **Power Platform Integration**.

2. Wählen Sie die Schaltfläche **Duale Schreibanwendung** aus.

    ![Power Platform-Integration.](media/powerplat_integration_step2.png)

3. Lesen Sie die allgemeinen Geschäftsbedingungen und wählen Sie **Konfigurieren** aus.

4. Wählen Sie **OK**, um fortzufahren.

5. Sie können den Fortschritt überwachen, indem Sie die Seite mit den Umgebungsdetails regelmäßig aktualisieren. Die Einrichtung dauert normalerweise 30 Minuten oder weniger.  

6. Nach Abschluss der Einrichtung werden Sie in einer Meldung darüber informiert, ob der Vorgang erfolgreich war oder ob ein Fehler aufgetreten ist. Wenn die Einrichtung fehlgeschlagen ist, wird eine entsprechende Fehlermeldung angezeigt. Sie müssen alle Fehler beheben, bevor Sie mit dem nächsten Schritt fortfahren können.

7. Wählen Sie **Link zur Power Platform Umgebung**, um eine Verbindung zwischen Dataverse und der aktuellen Umgebung der Datenbank zu erstellen. Diese Einrichtung dauert normalerweise 5 Minuten oder weniger.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Link zur Power Platform-Umgebung.":::

8. Wenn die Verknüpfung abgeschlossen ist, wird ein Hyperlink angezeigt. Verwenden Sie den Link, um sich beim duales Schreiben Administrationsbereich in der Finance und Operations Umgebung anzumelden. Von dort aus können Sie Entitätszuordnungen einrichten.

## <a name="linking-mismatch"></a>Verknüpfungskonflikt

Es ist möglich, dass Ihre Dual-write Umgebung mit einer Dataverse-Instanz verknüpft ist, während LCS nicht für die Power Platform-Integration festgelegt ist. Diese nicht übereinstimmende Verknüpfung kann zu unerwartetem Verhalten führen. Es wird empfohlen, dass die Details der LCS Umgebung mit denen übereinstimmen, mit denen Sie in Dual-write verbunden sind, damit dieselbe Verbindung von Ereignissen, virtuellen Tabellen und Add-Ins verwendet werden kann.

Wenn in Ihrer Umgebung eine Verknüpfungsinkongruenz besteht, zeigt LCS auf der Seite mit den Umgebungsdetails eine Warnung an, die dem folgenden Beispiel ähnelt: „Microsoft hat festgestellt, dass Ihre Umgebung über Dual-write mit einem anderen Ziel verknüpft ist als in Power Platform Integration angegeben, was nicht empfehlenswert ist.“

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform-Integrationslink stimmt nicht überein.":::

Wenn Sie diese Warnung erhalten, versuchen Sie eine der folgenden Lösungen:

- Wenn Ihre LCS Umgebung nie für die Power Platform-Integration festgelegt wurde, können Sie sich mit der Dataverse-Instanz verbinden, die in Dual-write konfiguriert ist, indem Sie die Anweisungen in diesem Artikel befolgen.
- Wenn Ihre LCS Umgebung bereits für die Power Platform-Integration festgelegt ist, sollten Sie die Verknüpfung von Dual-write aufheben und die Verbindung zu der von LCS festgelegten Instanz erneut herstellen, indem Sie das [Szenario verwenden: Verknüpfung zurücksetzen oder ändern](relink-environments.md#scenario-reset-or-change-linking).

In der Vergangenheit war eine manuelle Support-Ticket-Option verfügbar, aber das war, bevor es die obige Option 1 gab.  Microsoft unterstützt keine manuellen Relinking-Anfragen über Support-Tickets mehr.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
