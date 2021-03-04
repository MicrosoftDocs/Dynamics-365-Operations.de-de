---
title: Masterplanungsauftrag abbrechen
description: In diesem Thema wird erläutert, wie Sie einen aktiven Planungsauftrag abbrechen, der die Funktion „Integrierte Planung“ verwendet.
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6f5ce460cc2915d1d4d9b5699723a62ed7f94599
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428952"
---
# <a name="cancel-a-master-planning-job"></a>Masterplanungsauftrag abbrechen

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics 365 Supply Chain Management gibt es mehrere Möglichkeiten, einen Masterplanungsauftrag abzubrechen. Beispielsweise möchten Sie vielleicht einen Masterplanungsauftrag abbrechen, wenn er versehentlich gestartet wurde oder länger als erwartet ausgeführt wird, und Sie möchten ihn beenden. Am besten brechen Sie einen Planungsauftrag über die Seite **Nicht abgeschlossene Planungsprozesse** ab. Alternative Optionen auf den Seiten **Batchaufträge** und **Erweiterte Batchaufträge** sollten nur verwendet werden, wenn das Abbrechen des Masterplanungsauftrags über die Seite **Nicht abgeschlossene Prozesse** nicht innerhalb weniger Minuten abgeschlossen wurde.

## <a name="preferred-cancel-option"></a>Bevorzugte Option zum Abbrechen
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>Masterplanungsauftrag über die Seite **Nicht abgeschlossene Prozesse** abbrechen
1. Gehen Sie zu **Produktprogrammplanung > Abfragen und Berichte > Produktprogrammplanung > Nicht abgeschlossene Prozesse**.
2. Wählen Sie die Position mit dem abzubrechenden Planungsprozess aus.
3. Klicken Sie auf **Abbrechen**.

## <a name="additional-cancel-options"></a>Weitere Optionen zum Abbrechen
Diese sollten nur dann verwendet werden, wenn der Abbruch des Generalplanungsjobs von der Seite **Unerledigte Planungsprozesse** nicht innerhalb weniger Minuten abgeschlossen wurde.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Masterplanungsauftrag über die Seite **Batchaufträge** löschen
1. Wechseln Sie zu **Systemverwaltung > Anfragen > Batchaufträge**.
2. Wählen Sie die Position mit dem zu löschenden Planungsauftrag aus.
3. Klicken Sie auf **Löschen**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Aufgabe des Masterplanungsauftrags über die Seite **Erweiterte Batchaufträge** abbrechen
1. Wechseln Sie zu **Systemverwaltung > Anfragen > Batchaufträge**.
2. Wenn die Auftrags-ID nicht in der Liste angezeigt wird, klicken Sie auf **Zum erweiterten Formular wechseln**. Fahren Sie andernfalls mit dem nächsten Schritt fort.
3. Öffnen Sie den Batchauftrag. Klicken Sie auf die **Auftrags-ID** für den Batchauftrag, der Aufgaben enthält, die Sie beenden möchten.
4. Wählen Sie in **Batchaufgaben** die zu beendenden Aufgaben aus.
5. Klicken Sie auf **Status ändern**, wählen Sie **Abbrechen**, und klicken Sie auf **OK**.
6. Klicken Sie auf dem Inforegister **Batchaufgaben** auf **Abbrechen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]