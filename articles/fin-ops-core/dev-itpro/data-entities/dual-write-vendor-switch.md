---
title: Wechsel zwischen Kreditorendesigns
description: In diesem Thema wird der Wechsel von Kreditorendaten zwischen Finance and Operations-Apps und Common Data Service beschrieben.
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
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902724"
---
# <a name="switch-between-vendor-designs"></a>Wechsel zwischen Kreditorendesigns

[!include [banner](../includes/banner.md)]

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
 
