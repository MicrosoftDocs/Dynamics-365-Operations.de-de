---
title: Einrichtung von dualem Schreiben aus Lifecycle Services
description: In diesem Thema wird erläutert, wie Sie eine Verbindung für duales Schreiben über Microsoft Dynamics Lifecycle Services (LCS) einrichten.
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 825d6a4b3462077d0f4b3f4275792ea0fe5152df
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063671"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Einrichtung von dualem Schreiben aus Lifecycle Services

[!include [banner](../../includes/banner.md)]



In diesem Thema wird erläutert, wie Sie eine Verbindung für duales Schreiben über Microsoft Dynamics Lifecycle Services (LCS) aktivieren.

## <a name="prerequisites"></a>Voraussetzungen

Sie müssen die Power Platform Integration wie in den folgenden Themen beschrieben ausfüllen:

+ [Power Platform Integration – Aktivieren Sie diese Option während der Bereitstellung der Umgebung](../../power-platform/enable-power-platform-integration.md#enable-during-deploy)
+ [Power Platform-Integration – Aktivieren Sie diese Option nach der Bereitstellung der Umgebung](../../power-platform/enable-power-platform-integration.md#enable-after-deploy)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Richten Sie duales Schreiben für neue Dataverse Umgebungen ein

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

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Richten Sie duales Schreiben für eine bestehende Dataverse Umgebung ein

Um duales Schreiben für eine vorhandene Dataverse Umgebung einzurichten, müssen Sie ein Microsoft [Supportticket](../../lifecycle-services/lcs-support.md) erstellen. Das Ticket muss enthalten:

+ Ihre Finance und Operations Umgebungs-ID.
+ Ihr Umgebungsname von Lifecycle Services.
+ Die Dataverse Organisations-ID oder Power Platform Umgebungs-ID vom Power Platform Admin Center. Fordern Sie in Ihrem Ticket an, dass die ID die Instanz ist, die für die Power Platform Integration verwendet wird.

> [!NOTE]
> Sie können die Verknüpfung von Umgebungen mit LCS nicht aufheben. Um eine Umgebung zu entkoppeln, öffnen Sie den Arbeitsbereich **Datenintegration** in der Finance und Operations Umgebung und wählen Sie dann **Entkoppeln**.

## <a name="linking-mismatch"></a>Verknüpfungskonflikt

Es ist möglich, dass Ihre LCS-Umgebung mit einer Dataverse-Instanz verknüpft ist, während Ihre Umgebung für duales Schreiben mit einer anderen Dataverse-Instanz verknüpft ist. Dieser Verknüpfungskonflikt kann zu unerwartetem Verhalten und dazu führen, dass Daten an die falsche Umgebung gesendet werden. Es wird empfohlen, die Umgebung zu verwenden, die im Rahmen der Power Platform-Integration erstellt wurde. Langfristig wird dies die einzige Möglichkeit sein, eine Verknüpfung zwischen den Umgebungen herzustellen.

Wenn Ihre Umgebung einen Verknüpfungskonflikt aufweist, zeigt LCS auf Ihrer Umgebungsdetailseite eine Warnung an wie: „Microsoft hat festgestellt, dass Ihre Umgebung über duales Schreiben mit einem anderen Ziel verknüpft ist als in der Power Platform-Integration angeben. Dies wird nicht empfohlen“:

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform-Integrationslink stimmt nicht überein.":::

Wenn dieser Fehler auftritt, gibt es je nach Bedarf zwei Möglichkeiten:

+ Sie können [Umgebungen für duales Schreiben trennen und erneut verknüpfen (Verknüpfung zurücksetzen oder ändern)](relink-environments.md#scenario-reset-or-change-linking), wie auf der Detailseite Ihrer LCS-Umgebung angegeben. Dies ist die ideale Option, da Sie sie ohne den Microsoft-Support ausführen können.  
+ Wenn Sie Ihre Verknüpfung bei Dual-Write beibehalten möchten, können Sie den Microsoft Support um Hilfe bitten, um die Power Platform-Integration zu ändern, damit Ihre bestehende Dataverse-Umgebung verwendet wird, wie im vorherigen Abschnitt belegt.  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
