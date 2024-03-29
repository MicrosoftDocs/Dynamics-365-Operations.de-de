---
title: Erweiterbarkeit der Planungsoptimierung
description: In diesem Artikel werden die Erweiterbarkeitsszenarien beschrieben, die in der Planungsoptimierung unterstützt werden.
author: t-benebo
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7d649110959e6bcfdaeb32dd53c55dbc446ed1be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857543"
---
# <a name="planning-optimization-extensibility"></a>Erweiterbarkeit der Planungsoptimierung

[!include [banner](../../includes/banner.md)]

In diesem Artikel werden die Erweiterbarkeitsszenarien beschrieben, die sich auf die Masterplanung beziehen und in Planning Optimization unterstützt werden. Diese Funktionen sind ab Microsoft Dynamics 365 Supply Chain Management Version 10.0.13 verfügbar.

## <a name="custom-processing-when-master-planning-is-completed"></a>Individuelle Bearbeitung nach Abschluss der Masterplanung

Im gängigsten Erweiterbarkeitsszenario in der Planning Optimization erfolgt die benutzerdefinierte Verarbeitung, nachdem der Plan aktualisiert wurde. Sie können beispielsweise eine Spalte zur Tabelle Auftragsvorbestellungen (`ReqPO`) hinzufügen, oder Sie möchten statistische Informationen aus dem generierten Plan ableiten. Der wichtigste Erweiterbarkeitspunkt, der diese Szenarien ermöglicht, ist die `jobCompletedSuccessfully`-Methode in der `MpsMasterPlanningEvents`-Klasse.

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

Hier ist ein Beispiel für eine Erweiterung, die ein benutzerdefiniertes `CstmOrderPriority`-Feld auf dem Planauftrag festlegt.

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

Berücksichtigen Sie beim Hinzufügen von benutzerdefinierter Logik die folgenden Einschränkungen und bewährten Methoden:

- Die `jobCompletedSuccessfully`-Methode wird außerhalb des Transaktionsbereichs aufgerufen. Daher ist der Plan für den Benutzer bereits sichtbar, wenn die benutzerdefinierte Logik ausgeführt wird. Wenn Ihre Anpassung zusätzliche Felder für geplante Aufträge festlegt, ist es wichtig, dass Sie den Benutzern mitteilen, dass die Werte dieser Felder letztendlich konsistent sind (d. h., sie können unmittelbar nach Abschluss eines Planungsauftrags veraltet sein).
- Ein weiterer Masterplanungsauftrag kann beginnen, wenn die `jobCompletedSuccessfully`-Methode aufgerufen wird. Der neue Einzelvorgang kann sich auf den gesamten Plan oder einen Teil des Plans auswirken. Der neue Einzelvorgang aktualisiert oder löscht möglicherweise dieselben Planaufträge oder Bedarfstransaktionen, die als Teil des Planungseinzelvorgangs erstellt oder aktualisiert wurden, der in `jobCompletedSuccessfully` bearbeitet wurde. Ausnahmen von Aktualisierungskonflikten müssen behandelt werden, wenn dieses Ereignis verlängert wird.
- Vermeiden Sie die Verwendung eines einzelnen Transaktionsbereichs, wenn Sie diese Methode erweitern. Ein einzelner Masterplanungslauf kann Millionen von Bedarfstransaktionen und Hunderttausende von Planaufträgen produzieren. Werden all diese Transaktionen und Planaufträge im Rahmen einer einzigen Transaktion bearbeitet, treten viele SQL-Sperren auf und blockieren andere Planungsprozesse. Wenn die Transaktion über einen längeren Zeitraum gehalten wird, werden außerdem „Ghost Records“ in der SQL-Datenbank erstellt. Ghost Records wirken sich negativ auf jeden Prozess im System aus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]