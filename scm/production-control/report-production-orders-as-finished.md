---
title: "Fertigmeldung für Produktionsaufträge"
description: "Einen Produktionsauftrag als abgeschlossen melden. In dieser Phase wird ein Produkt aus dem Produktionsauftrag für Bestand gemeldet und verschoben."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 52607d645c6eaf4ff97d2c4bf8abc6ec1374fd7e
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="report-production-orders-as-finished"></a>Fertigmeldung für Produktionsaufträge

[!include[banner](../includes/banner.md)]


Einen Produktionsauftrag als abgeschlossen melden. In dieser Phase wird ein Produkt aus dem Produktionsauftrag für Bestand gemeldet und verschoben.

Wenn eine Menge der fertiggestellten Güter auf einem Produktionsauftrag als fertig gemeldet wurde, wird sie im Bestand als verfügbar aktualisiert. Teilmengen der ursprünglichen geplanten Bestellmenge können als fertig gemeldet werden. Es ist auch möglich, Ausschussmengen mit einem zugeordneten Fehlergrund zu melden, wenn Mengen als fertig gemeldet werden. Wenn der Produktionsauftrag die Phase „Als fertig gemeldet“ erreicht, bedeutet das, dass keine weitere Menge am Produktionsauftrag fertig gemeldet werden wird.
Die folgenden Merkmale werden auch dem Vorgang **Fertigmeldung** zugeordnet:
-   Es ist möglich, den Verbrauch des Rohmaterials und der Zeit einzurichten, die proportional zur gemeldeten Menge sind (Zurückströmen)
-   Einlagerungsarbeit kann für Artikel generiert werden, die für Lagerortprozesse aktiviert werden.
-   Geplanter oder Standardkostenwert der Fertigerzeugnisse kann so eingerichtet werden, dass er in die Sachkonten angegeben werden muss.
-   Ein Qualitätsprüfungsauftrag kann für die gemeldete Menge auf Grundlage der Einstellungen einer Qualitätszuordnung erstellt werden.

Die Menge wird für den Ausgangslagerplatz gemeldet. Lagerarbeit wird dann generiert, um die Menge vom Ausgangslagerplatz zum endgültigen Bestimmungsort zu verschieben, die durch die Lagerplatzdirektive für die Einlagerungsarbeit definiert wurde.

-   Ein Qualitätsprüfungsauftrag kann erstellt werden, wenn ein Produktionsauftrag als fertig gemeldet wird, wenn eine Qualitätszuordnung eingerichtet wurde.

## <a name="set-a-production-order-to-reporting-as-finished"></a>Produktionsauftrag als Fertigmeldung einrichten
Sie können einen Produktionsauftrag auf **Fertigmeldung** setzen, über die standardmäßige Aktualisierungsfunktion des Produktionsauftrags, oder durch die Übersichtserfassungen für Arbeitspläne und Einzelvorgänge, oder über die Erfassung **Fertigmeldung**. Sie können die Phase auch auf **Fertigmeldung** über die Einzelvorgangslistenterminal- und Einzelvorgangslistengerätenseiten aktualisieren, wenn Sie zum letzten Einzelvorgang des Produktionsauftrags melden. Abschließend können Sie die Option **Fertigmeldung** als Prozess für die Handheld-Lösung am Lagerort aktivieren.  




