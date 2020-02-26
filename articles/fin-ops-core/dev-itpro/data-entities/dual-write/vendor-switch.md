---
title: Wechsel zwischen Kreditorendesigns
description: In diesem Thema wird der Wechsel zwischen der Integration von Kreditorendaten zwischen Finance and Operations Apps und Common Data Service beschrieben.
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
ms.openlocfilehash: 587a9b98f28b11e303aff4b59e9726f220d956eb
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019793"
---
# <a name="switch-between-vendor-designs"></a>Wechsel zwischen Kreditorendesigns

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="vendor-data-flow"></a>Kreditorendatenfluss 

Wenn Sie andere Dynamics 365-Apps für das Lieferanten-Mastering verwenden und die Lieferanteninformationen von Kunden isolieren möchten, verwenden Sie dieses Basislieferantendesign.  

![Grundlegender Lieferantenfluss](media/dual-write-vendor-data-flow.png)
 
Wenn Sie andere Dynamics 365-Apps für das Lieferanten-Mastering verwenden und weiterhin die **Kontoentität** zum Speichern der Lieferanteninformationen verwenden möchten, verwenden Sie dieses erweiterte Lieferantendesign. In diesem Entwurf werden erweiterte Lieferanteninformationen wie der Gesperrt-Status des Lieferanten und das Lieferantenprofil in der Entität **Lieferanten** in Common Data Service gespeichert. 

![Erweiterter Lieferantenfluss](media/dual-write-vendor-detail.jpg)
 
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
    5. Aktivieren Sie die Workflows, die Sie in den Entitäten **Konto** und **Kreditor** erstellt haben, um mit der Verwendung der Entität **Konto** für das Speichern von Kreditoreninformationen zu starten. 
 
