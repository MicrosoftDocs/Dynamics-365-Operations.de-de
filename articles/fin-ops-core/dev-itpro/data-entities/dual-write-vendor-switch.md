---
title: Zwischen Lieferantendesigns wechseln
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772363"
---
# <a name="switch-between-vendor-designs"></a>Zwischen Lieferantendesigns wechseln

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Kreditorendatenfluss 

Wenn Sie andere Dynamics 365-Apps für das Lieferanten-Mastering verwenden und die Lieferanteninformationen von Kunden isolieren möchten, verwenden Sie dieses Basislieferantendesign.  

![Grundlegender Lieferantenfluss](media/dual-write-switch-1.png)
 
Wenn Sie andere Dynamics 365-Apps für das Lieferanten-Mastering verwenden und weiterhin die **Kontoentität** zum Speichern der Lieferanteninformationen verwenden möchten, verwenden Sie dieses erweiterte Lieferantendesign. In diesem Entwurf werden erweiterte Lieferanteninformationen wie der Gesperrt-Status des Lieferanten und das Lieferantenprofil in der Entität **Lieferanten** in Common Data Service gespeichert. 

![Erweiterter Lieferantenfluss](media/dual-write-switch-2.png)
 
Führen Sie die unten stehenden Schritte aus, um das erweiterte Lieferantendesign zu verwenden: 
 
1. Das **SupplyChainCommon**-Lösungspaket enthält die Workflowprozessvorlagen wie auf dem folgenden Bild gezeigt.
    > [!div class="mx-imgBorder"]
    > ![Workflowprozessvorlagen](media/dual-write-switch-3.png)
2. Erstellen Sie neue Workflowprozesse mithilfe der Workflowprozessvorlagen: 
    1. Erstellen Sie einen neuen Workflowprozess für die Entität **Lieferant** mithilfe der Workflowprozessvorlage **Lieferanten in der Kontoentität erstellen** und klicken Sie auf **OK**. Dieser Workflow verarbeitet das Lieferantenerstellungsszenario für die Entität **Konto**.
        > [!div class="mx-imgBorder"]
        > ![Lieferanten in der Kontoentität erstellen](media/dual-write-switch-4.png)
    2. Erstellen Sie einen neuen Workflowprozess für die Entität **Lieferant** mithilfe der Workflowprozessvorlage **Kontoentität aktualisieren** und klicken Sie auf **OK**. Dieser Workflow verarbeitet das Lieferantenaktualisierungsszenario für die Entität **Konto**. 
        > [!div class="mx-imgBorder"]
        > ![Kontoentität aktualisieren](media/dual-write-switch-5.png)
    3. Erstellen Sie neue Workflowprozesse aus den Vorlagen, die in der Entität **Konten** erstellt wurden. 
        > [!div class="mx-imgBorder"]
        > ![Lieferanten in der Kontoentität erstellen](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![Lieferantenentität aktualisieren](media/dual-write-switch-7.png)
    4. Sie können die Workflow als Echtzeit- oder Hintergrundworkflows je nach Ihren Anforderungen konfigurieren. 
        > [!div class="mx-imgBorder"]
        > ![In einen Hintergrundworkflow konvertieren](media/dual-write-switch-8.png)
    5. Aktivieren Sie die Workflows, die Sie in den Entitäten **Konto** und **Lieferant** erstellt haben, um mit der Verwendung der Customer Engagement-Entität **Konto** für das Speichern von Lieferanteninformationen zu starten. 
 
