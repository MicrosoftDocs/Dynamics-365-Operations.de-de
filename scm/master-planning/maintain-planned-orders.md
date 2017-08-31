---
title: "Bestellvorschläge verwalten"
description: "Dieser Artikel bietet Informationen dazu, wie Bestellvorschläge verwaltet werden. Es wird beschrieben, wie Sie den Status von Bestellvorschlägen aktualisieren, umwandeln und Bestellvorschläge filtern können, die den gleichen Status wie ein ausgewählter Bestellvorschlag haben."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 94f6f28ec4b255930f84a27eb5394503ff59e4c0
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017

---

# <a name="maintain-planned-orders"></a>Bestellvorschläge verwalten

[!include[banner](../includes/banner.md)]


Dieser Artikel bietet Informationen dazu, wie Bestellvorschläge verwaltet werden. Es wird beschrieben, wie Sie den Status von Bestellvorschlägen aktualisieren, umwandeln und Bestellvorschläge filtern können, die den gleichen Status wie ein ausgewählter Bestellvorschlag haben.

Sie können Bestellvorschläge aus dem Arbeitsbereich **Produktprogrammplanung**, aus der Liste **Bestellvorschlag**, oder aus den Listen **Geplante Produktionsaufträge**, **Geplante Einkaufsbestellungen** und **Geplante Umlagerung** verwalten. Sie können das Feld **Status** verwenden, um Ihren Fortschritt zu verfolgen. Folgende Werte werden verwendet:

-   Wenn vom Produktprogrammplanungslauf Bestellvorschläge generiert wurden, weisen die Bestellvorschläge den Status **Offen** auf.
-   Wenn ein Bestellvorschlag nicht umgewandelt werden soll, können Sie ihm den Status **Abgeschlossen** zuweisen.
-   Wenn ein Bestellvorschlag nicht umgewandelt werden soll, können Sie diesem den Status **Genehmigt** zuweisen. Mit diesem Status geben Sie an, dass Sie die Umwandlung des Bestellvorschlags genehmigen, was jedoch nicht bedeutet, dass er bereits umgewandelt ist.

**Hinweis:** Ein genehmigter Bestellvorschlag wird mit dem aktuellen Status in die nächste Produktprogrammplanungs-Berechnung übertragen. Bestellvorschläge können umgewandelt werden, indem Sie auf **Vorschlagsumwandlung** klicken. Die folgenden Bestellvorschläge können umgewandelt werden:

-   Der Bestellvorschlag, der ausgewählt wurde.
-   Mehrere Bestellvorschläge.
-   Bestellvorschläge, die mithilfe einer Stücklistenauflösung auf der Seite **Stücklistenauflösung** generiert wurden. Klicken Sie auf **Bestellvorschläge**, wählen Sie den Bestellvorschlag aus, und klicken Sie dann auf **Vorschlagsumwandlung**.

Nachdem ein Bestellvorschlag umgewandelt wurde, wird er in den Abschnitt "Aufträge" des jeweiligen Moduls verschoben. **Hinweis:** Sie können mit der rechten Maustaste auf einen Bestellvorschlag mit einem bestimmten Status klicken und so andere Bestellvorschläge herausfiltern, die den gleichen Status aufweisen. Diese Funktion ist beispielsweise nützlich zum Filtern nach allen Bestellvorschlägen mit dem Status **Genehmigt**, um sie dann umzuwandeln.

<a name="see-also"></a>Siehe auch
--------

[Produktprogrammpläne](master-plans.md)




