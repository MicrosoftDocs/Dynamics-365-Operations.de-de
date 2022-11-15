---
title: Einen Einzelvorgang abbrechen, der mit dem veralteten Produktprogrammplanungsmodul erstellt wurde
description: In diesem Artikel wird erläutert, wie ein aktiver Planungsauftrag, der das veraltete Produktprogrammplanungsmodul verwendet, abgebrochen werden kann.
author: t-benebo
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7b71a43f407050dccb7550db7c4b6a98a596d589
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740876"
---
# <a name="cancel-a-job-that-was-created-using-the-deprecated-master-planning-engine"></a>Einen Einzelvorgang abbrechen, der mit dem veralteten Produktprogrammplanungsmodul erstellt wurde

[!include [banner](../includes/banner.md)]

Es gibt mehrere Optionen, einen Einzelvorgang abzubrechen, der mit dem veralteten Produktprogrammplanungsmodul erstellt wurde. Beispielsweise möchten Sie vielleicht einen Masterplanungsauftrag abbrechen, wenn er versehentlich gestartet wurde oder länger als erwartet ausgeführt wird, und Sie möchten ihn beenden.

Am besten brechen Sie einen Planungsauftrag über die Seite **Nicht abgeschlossene Planungsprozesse** ab. Alternative Optionen auf den Seiten **Batchaufträge** und **Erweiterte Batchaufträge** sollten nur verwendet werden, wenn das Abbrechen des Masterplanungsauftrags über die Seite **Nicht abgeschlossene Prozesse** nicht innerhalb weniger Minuten abgeschlossen wurde.

## <a name="preferred-cancel-option"></a>Bevorzugte Option zum Abbrechen

### <a name="cancel-master-planning-job-from-the-unfinished-planning-processes-page"></a>Masterplanungsauftrag über die Seite Nicht abgeschlossene Prozesse abbrechen

1. Gehen Sie zu **Produktprogrammplanung > Abfragen und Berichte > Produktprogrammplanung > Nicht abgeschlossene Prozesse**.
2. Wählen Sie die Position mit dem abzubrechenden Planungsprozess aus.
3. Wählen Sie **Abbrechen** aus.

## <a name="additional-cancel-options"></a>Weitere Optionen zum Abbrechen

Diese sollten nur dann verwendet werden, wenn der Abbruch des Generalplanungsjobs von der Seite **Unerledigte Planungsprozesse** nicht innerhalb weniger Minuten abgeschlossen wurde.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Masterplanungsauftrag über die Seite **Batchaufträge** löschen

1. Wechseln Sie zu **Systemverwaltung > Anfragen > Batchaufträge**.
2. Wählen Sie die Position mit dem zu löschenden Planungsauftrag aus.
3. Wählen Sei **Löschen**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Aufgabe des Masterplanungsauftrags über die Seite **Erweiterte Batchaufträge** abbrechen

1. Wechseln Sie zu **Systemverwaltung > Anfragen > Batchaufträge**.
2. Wenn die Auftrags-ID nicht in der Liste angezeigt wird, klicken Sie auf **Zum erweiterten Formular wechseln**. Fahren Sie andernfalls mit dem nächsten Schritt fort.
3. Öffnen Sie den Batchauftrag. Wählen Sie **Auftrags-ID** für den Batchauftrag, der Aufgaben enthält, die Sie beenden möchten.
4. Wählen Sie in **Batchaufgaben** die zu beendenden Aufgaben aus.
5. Wählen Sie **Status ändern**, wählen Sie **Abbrechen**, und klicken Sie auf **OK**.
6. Klicken Sie auf dem Inforegister **Batchaufgaben** auf **Abbrechen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]