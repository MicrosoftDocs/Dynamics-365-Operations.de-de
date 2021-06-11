---
title: Einrichtung von dualem Schreiben aus Lifecycle Services
description: In diesem Thema wird erläutert, wie Sie eine Verbindung für duales Schreiben über Microsoft Dynamics Lifecycle Services (LCS) einrichten.
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103568"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Einrichtung von dualem Schreiben aus Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema wird erläutert, wie Sie eine Verbindung für duales Schreiben über Microsoft Dynamics Lifecycle Services (LCS) aktivieren.

## <a name="prerequisites"></a>Voraussetzungen

Sie müssen die Power Platform Integration wie in den folgenden Themen beschrieben ausfüllen:

+ [Power Platform Integration – Aktivieren Sie diese Option während der Bereitstellung der Umgebung](../../power-platform/overview.md#enable-during-environment-deployment)
+ [Power Platform Integration – Richten Sie diese Option nach der Bereitstellung der Umgebung ein](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Richten Sie duales Schreiben für neue Dataverse Umgebungen ein

Befolgen Sie diese Schritte, um duales Schreiben von der LCS -Seite **Umgebungsdetails** einzurichten:

1. Auf der Seite **Umgebungsdetails** erweitern Sie den Abschnitt **Power Platform Integration**.

2. Wählen Sie die Schaltfläche **Duale Schreibanwendung** aus.

    ![Power Platform-Integration](media/powerplat_integration_step2.png)

3. Lesen Sie die allgemeinen Geschäftsbedingungen und wählen Sie **Konfigurieren** aus.

4. Wählen Sie **OK**, um fortzufahren.

5. Sie können den Fortschritt überwachen, indem Sie die Seite mit den Umgebungsdetails regelmäßig aktualisieren. Die Einrichtung dauert normalerweise 30 Minuten oder weniger.  

6. Nach Abschluss der Einrichtung werden Sie in einer Meldung darüber informiert, ob der Vorgang erfolgreich war oder ob ein Fehler aufgetreten ist. Wenn die Einrichtung fehlgeschlagen ist, wird eine entsprechende Fehlermeldung angezeigt. Sie müssen alle Fehler beheben, bevor Sie mit dem nächsten Schritt fortfahren können.

7. Wählen Sie **Link zur Power Platform Umgebung**, um eine Verbindung zwischen Dataverse und der aktuellen Umgebung der Datenbank zu erstellen. Diese Einrichtung dauert normalerweise 5 Minuten oder weniger.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Link zur Power Platform Umgebung":::

8. Wenn die Verknüpfung abgeschlossen ist, wird ein Hyperlink angezeigt. Verwenden Sie den Link, um sich im Verwaltungsbereich mit zwei Schreibvorgängen in der Finance and Operations Umgebung zu registrieren. Von dort aus können Sie Entitätszuordnungen einrichten.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Richten Sie duales Schreiben für eine bestehende Dataverse Umgebung ein

Um duales Schreiben für eine vorhandene Dataverse Umgebung einzurichten, müssen Sie ein Microsoft [Supportticket](../../lifecycle-services/lcs-support.md) erstellen. Das Ticket muss enthalten:

+ Ihre Finance and Operations Umgebungs-ID.
+ Ihr Umgebungsname von Lifecycle Services.
+ Die Dataverse Organisations-ID oder Power Platform Umgebungs-ID vom Power Platform Admin Center. Fordern Sie in Ihrem Ticket an, dass die ID die Instanz ist, die für die Power Platform Integration verwendet wird.

> [!NOTE]
> Sie können die Verknüpfung von Umgebungen mit LCS nicht aufheben. Um die Verknüpfung einer Umgebung aufzuheben, öffnen Sie den **Datenintegration** Arbeitsbereich in der Finance and Operations Umgebung und wählen Sie dann **Verknüpfung aufheben**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
