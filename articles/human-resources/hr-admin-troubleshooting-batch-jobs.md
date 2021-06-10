---
title: Optimieren der Leistung durch Planung von Batch-Jobs außerhalb der Geschäftszeiten
description: In diesem Thema wird erläutert, wie einige Leistungsprobleme mit Microsoft Dynamics 365 Human Resources behoben werden, indem Sie Batch-Jobs mit langer Laufzeit außerhalb der Geschäftszeiten planen.
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a5aeaeb7311d87a154882b7058b6da430900bd56
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053466"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Optimieren der Leistung durch Planung von Batch-Jobs außerhalb der Geschäftszeiten

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

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

   ![Wiederholung festlegen](media/talent-batch-history-cleanup-recurrence.png)

4. Legen Sie unter **Wiederholung definieren** das **Startdatum** und die **Startzeit** für die Wiederholungen außerhalb der Geschäftszeiten oder an Wochenenden fest. Wählen Sie **Kein Enddatum** aus. 

   ![Startdatum und -zeit der Wiederholung definieren](media/talent-batch-history-cleanup-define-recurrence.png)

5. Wählen Sie **OK**.

6. Ändern Sie gegebenenfalls weitere Parameter unter **Im Hintergrund ausführen** und wählen Sie dann **OK** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Leistung mit automatischen Bereinigungsaufgaben optimieren](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]