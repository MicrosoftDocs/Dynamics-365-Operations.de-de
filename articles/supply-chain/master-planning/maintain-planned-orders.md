---
title: Bestellvorschläge verwalten
description: Dieser Artikel bietet Informationen dazu, wie Bestellvorschläge verwaltet werden. Es wird beschrieben, wie Sie den Status von Bestellvorschlägen aktualisieren, umwandeln und Bestellvorschläge filtern können, die den gleichen Status wie ein ausgewählter Bestellvorschlag haben.
author: t-benebo
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2bf3efec234ea4d22c01e1b48b3548dad7577a2b
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468579"
---
# <a name="maintain-planned-orders"></a>Bestellvorschläge verwalten

[!include [banner](../includes/banner.md)]

Dieser Artikel bietet Informationen dazu, wie Bestellvorschläge verwaltet werden. Es wird beschrieben, wie Sie den Status von Bestellvorschlägen aktualisieren, umwandeln und Bestellvorschläge filtern können, die den gleichen Status wie ein ausgewählter Bestellvorschlag haben.

Sie können Bestellvorschläge aus dem Arbeitsbereich **Produktprogrammplanung**, aus der Liste **Bestellvorschlag**, oder aus den Listen **Geplante Produktionsaufträge**, **Geplante Einkaufsbestellungen** und **Geplante Umlagerung** verwalten. 

## <a name="planned-order-status"></a>Status der Bestellvorschläge
Sie können das Feld **Status** verwenden, um Ihren Fortschritt zu verfolgen. Folgende Werte werden verwendet:

-   Wenn vom Produktprogrammplanungslauf Bestellvorschläge generiert wurden, weisen die Bestellvorschläge den Status **Offen** auf.
-   Wenn ein Bestellvorschlag nicht umgewandelt werden soll, können Sie ihm den Status **Abgeschlossen** zuweisen.
-   Wenn Sie ein Bestellvorschlag umgewandelt werden soll, können Sie den Status in **Genehmigt** ändern. Planaufträge mit dem Status **Genehmigt** werden von der Masterplanung berücksichtigt, so dass sie bei einem späteren Masterplanungslauf nicht geändert oder gelöscht werden. Um dies zu erreichen, kopiert die Planungslogik während der Produktplanung die **genehmigten** Planaufträge aus der alten Planversion in die neue Planversion.

## <a name="firming-planned-orders"></a>Umwandeln von Bestellvorschlägen 
Durch die Umwandlung von Bestellvorschlägen werden tatsächliche Aufträge erstellt. Diese sind auch als *freigegebene* oder *offene Aufträge* bekannt. Nachdem ein Bestellvorschlag umgewandelt wurde, wird er in den Abschnitt "Aufträge" des jeweiligen Moduls verschoben.

Sie können auf der Seite **Bestellvorschläge** zwei Umwandlungsoptionen auswählen:

-   **Umwandlung** – Dies wandelt ein oder mehrere Bestellvorschläge um.
-   **Alle umwandeln** – Dies wandelt alle Bestellvorschläge im Filter um. Wenn Sie **Alle umwandeln** verwenden, müssen Sie den Bestellvorschlag nicht auswählen, alle Bestellvorschläge innerhalb des Filters werden umgewandelt. Diese Option ist hilfreich, falls Sie eine hohe Anzahl von Bestellvorschlägen umwandeln.

> [!NOTE]
> Sie können einen Bestellvorschlag nachverfolgen, der aus der **Umwandlungshistorie** unter **Bestellvorschlagsformular > Ansicht > Umwandlungshistorie** umgewandelt wurde.

## <a name="parallelize-firming"></a>Umwandlung parallelisieren
Wenn Sie viele Aufträge gleichzeitig umwandeln möchten, kann das Parallelisieren des Durchlaufs die Laufzeit oder die Leistung verbessern. Diese Option ist nur verfügbar, wenn mehrere Bestellvorschläge entweder mit **Umwandeln** oder **Alle umwandeln** umgewandelt werden. Folgende Parameter sind verfügbar:

-   **Umwandlung parallelisieren** – Bei **Ja** wird der Umwandlungsvorgang mit der Anzahl der Threads parallelisiert, die in **Anzahl der Threads** definiert werden.
-   **Anzahl der Threads** – Steuert die Anzahl der Threads, die verwendet werden, um den Umwandlungsvorgang zu parallelisieren. Der Parameter wird nur angezeigt, wenn **Umwandlung parallelisieren** auf **Ja** festgelegt ist.

> [!NOTE]
> Die Option für **Umwandlung parallelisieren** wird nur angezeigt, wenn Sie mehr als einen Planauftrag zum Fixieren ausgewählt haben.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht zu Produktprogrammplänen](master-plans.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]