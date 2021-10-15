---
title: Intercompany-Produktprogrammplanungslauf
description: In diesem Thema wird der Intercompany-Produktprogrammplanungslauf erläutert.
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e28051097905503e291e0c15a50e9363b39b2daa
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548286"
---
# <a name="intercompany-master-scheduling"></a>Intercompany-Produktprogrammplanungslauf

[!include [banner](../../includes/banner.md)]

Mit dem Intercompany-Produktprogrammplanungslauf wird der Bedarf berechnet und werden geplante Intercompany-Aufträge über mehrere Konzerntöchter generiert. Beim Intercompany-Produktprogrammplanungslauf wird eine von Ihnen festgelegte Anzahl von Iterationen ausgeführt. Damit Microsoft Dynamics 365 Supply Chain Management den Intercompany-Produktprogrammplanungslauf ausführen kann, müssen Sie diesen in jedem Intercompany-Unternehmen einrichten. Dies umfasst mehrere Iterationen, in deren Rahmen Microsoft Dynamics 365 Supply Chain Management automatisch eine Intercompany-Bestellung anlegt, was wiederum zur automatischen Erstellung eines Intercompany-Auftrags führt, mit dem dann neuer Bedarf generiert wird.

Der Intercompany-Masterplan und die Intercompany-Planungsreihenfolge werden in den Parametern der **Produktprogrammplanung** in jedem Intercompany-Unternehmen eingerichtet.

Damit der Bedarf in der gesamten Intercompany-Kette weitergegeben werden kann, müssen Parameter festgelegt werden, um sicherzustellen, dass geplante Einkaufsbestellungen automatisch umgewandelt werden, d. h. Aufträge können im Hinblick auf Zeit oder Menge nicht geändert werden. Richten Sie den **Sofortanlagezeitraum** in der Gruppe „Abdeckung“ oder den **Sofortanlagezeitraum** im Masterplan ein. Wird kein **Sofortanlagezeitraum** eingerichtet ist, werden Intercompany-Bestellungen nicht automatisch generiert. Nur die erste Ausführung des Produktprogrammplanungslauf führt zu geplanten Aufträgen. Da jedoch keine Intercompany-Bestellung erstellt wird, wird kein Intercompany-Auftrag erstellt, und daher werden keine weiteren Intercompany-Bestellungen erstellt usw.

Beim Start des Intercompany-Produktprogrammplanungslaufs führt Microsoft Dynamics 365 Supply Chain Management in jedem Intercompany-Unternehmen einen Produktprogrammplanungslauf und anschließend einen weiteren Lauf aus usw., bis die angegebene Anzahl von Iterationen erreicht ist. Maximal sind 30 Iterationen möglich; allerdings dauert der Planungslauf je nach Anzahl der Iterationen entsprechend länger.

Da die Produktprogrammplanung in den Unternehmen von der Intercompany-Planungsreihenfolge abhängig ist, d. h. von der Reihenfolge, in der das Programm die Produktprogrammpläne in den einzelnen Intercompany-Unternehmen priorisiert, können Sie die Intercompany-Produktprogrammplanung von jedem beliebigen Intercompany-Unternehmen aus starten. Da die Intercompany-Planungsreihenfolge die Sequenz festlegt, in der die Produktprogrammplanung in den Unternehmen ausgeführt wird, ist es unerheblich, wo mit der Intercompany-Produktprogrammplanung begonnen wird. Bei jeder Iteration wird das aktuelle Unternehmen zuletzt berücksichtigt.

> [!NOTE]
> Die optimale Methode besteht darin, die Intercompany-Produktprogrammplanung von einem Microsoft Dynamics 365 Supply Chain Management-Unternehmen aus zu initiieren.

Auf der Seite **Intercompany-Produktprogrammplanungslauf** können Sie eine Abfolge der Produktprogrammplanungsläufe starten, wodurch ein erster Produktprogrammplanungslauf mit dem Prinzip ausgeführt wird, die Bedarfsberechnung zu aktualisieren, die Sie für die erste Iteration für alle Intercompany-Unternehmen ausgewählt haben. Bei nachfolgenden Iterationen wird das Sekundärprinzip verwendet, das Sie für die nächste Iteration ausgewählt haben, und dieses Prinzip bleibt gültig, bis die Anzahl der von Ihnen angegebenen Iterationen erreicht ist.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
