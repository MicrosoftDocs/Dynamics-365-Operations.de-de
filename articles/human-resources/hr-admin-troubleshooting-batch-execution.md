---
title: Steckengebliebene Batchaufträge zurücksetzen
description: In diesem Thema wird erläutert, wie Sie Probleme mit steckengebliebenen Batchaufträgen beheben können.
author: twheeloc
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 2602bd954daac563cbc50810c6fe0d79dc71a62b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694990"
---
# <a name="reset-stuck-batch-jobs"></a>Steckengebliebene Batchaufträge zurücksetzen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Abgang

In Microsoft Dynamics 365 Human Resources können Probleme mit Batchaufträgen auftreten, die entweder im Zustand **Ausführen** oder **Abbrechen** steckenbleiben und nicht abgeschlossen werden.

## <a name="resolution"></a>Lösung

Wenn ein Batchauftrag im Status **Ausführen** oder **Abbrechen** steckenbleibt, können Sie den Status zurücksetzen, indem Sie die Stornierung des Auftrags erzwingen. Nachdem Sie ihn abgebrochen haben, können Sie den Batchauftrag zurücksetzen, indem Sie ihn auf den Status **Im Wartezustand** setzen. Er wird dann zur Ausführung im nächsten geplanten Batch-Lauf wieder aufgenommen.

1. Wählen Sie im **Systemadministration**-Arbeitsbereich die **Links**-Seite und wählen Sie **Batchaufträge**.

2. Wählen Sie auf der Listenseite **Batchauftrag** den Auftrag aus, der zurückgesetzt werden soll.

3. Wählen Sie in der Aktionsleiste **Abbrechen erzwingen** aus und bestätigen Sie die Aktion.

   > [!NOTE]
   > Die Aktion **Abbrechen erzwingen** ist nur verfügbar, wenn der ausgewählte Batchauftrag den Status **Ausführen** oder **Abbrechen** hat und für den Auftrag keine Batchausführungs- oder -stornierungsprozesse ausgeführt werden.

4. Wählen Sie im Aktionsband **Status ändern** aus.

5. Wählen Sie auf der **Neuen Status auswählen**-Seite **Im Wartezustand** und dann **OK** aus.

   ![Einen neuen Batchauftragsstatus auswählen.](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>Siehe auch

[Leistung durch Einplanung von Batchaufträgen nach Stunden verbessern](hr-admin-troubleshooting-batch-jobs.md)<br>
[Leistung durch automatische Bereinigungsaufgaben verbessern](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
