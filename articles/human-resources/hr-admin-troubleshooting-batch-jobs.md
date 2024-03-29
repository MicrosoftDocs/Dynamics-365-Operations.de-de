---
title: Optimieren der Leistung durch Planung von Batch-Jobs außerhalb der Geschäftszeiten
description: In diesem Artikel wird erläutert, wie einige Leistungsprobleme mit Microsoft Dynamics 365 Human Resources behoben werden, indem Sie Batchaufträge mit langer Laufzeit außerhalb der Geschäftszeiten planen.
author: twheeloc
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 6efb0a906bb948a47f03665dd6e7a8dd43434083
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896075"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Optimieren der Leistung durch Planung von Batch-Jobs außerhalb der Geschäftszeiten


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>Abgang

In Microsoft Dynamics 365 Human Resources können Leistungsprobleme auftreten, wenn Batch-Jobs mit langer Laufzeit während der üblichen Geschäftszeiten ausgeführt werden.

## <a name="resolution"></a>Lösung

Planen Sie die folgenden Batch-Jobs außerhalb der Geschäftszeiten. Wir empfehlen außerdem, die Frequenz von häufig ausgeführten Batch-Jobs zu überprüfen. Reduzieren Sie nach Möglichkeit die Wiederholung des Batch-Jobs. In vielen Fällen ist die Standardfrequenz ausreichend.

Die folgenden Batch-Jobs sollten nachts oder nach Geschäftsschluss ausgeführt werden. Überprüfen Sie unbedingt die Zeitzone für diese sich wiederholenden Batch-Jobs. Einige Batch-Jobs verwenden möglicherweise Pacific Standard Time (PST).

| Stapelverarbeitungsauftrag | Standardhäufigkeit |
| --- | --- |
| Bereinigung des Batch-Jobs | 1 Mal pro Monat |
| Stagingbereinigung exportieren | 1 Mal pro Tag |
| Fehlende Anforderungssynchronisierung bei der Common Data Service-Integration | 1 Mal pro Tag |
| Job zur Datenbankkomprimierung, der außerhalb der Geschäftszeiten regelmäßig ausgeführt werden muss | 1 Mal pro Tag |
| Job zur erneuten Erstellung des Datenbankindex, der außerhalb der Geschäftszeiten regelmäßig ausgeführt werden muss | 1 Mal pro Tag |

1. Wählen Sie in Human Resources **Systemverwaltung** aus.

2. Verwenden Sie die Leiste **Suchen**, um nach einem der oben genannten Batch-Jobs zu suchen.

3. Wählen Sie **Im Hintergrund ausführen** aus und wählen Sie dann **Wiederholung** aus.

   ![Wiederholung festlegen.](media/talent-batch-history-cleanup-recurrence.png)

4. Legen Sie unter **Wiederholung definieren** das **Startdatum** und die **Startzeit** für die Wiederholungen außerhalb der Geschäftszeiten oder an Wochenenden fest. Wählen Sie **Kein Enddatum** aus. 

   ![Startdatum und -zeit der Wiederholung definieren.](media/talent-batch-history-cleanup-define-recurrence.png)

5. Wählen Sie **OK** aus.

6. Ändern Sie gegebenenfalls weitere Parameter unter **Im Hintergrund ausführen** und wählen Sie dann **OK** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Leistung mit automatischen Bereinigungsaufgaben optimieren](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
