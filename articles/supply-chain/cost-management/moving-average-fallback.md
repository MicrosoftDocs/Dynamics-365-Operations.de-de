---
title: Flexible durchschnittliche Fallback-Kostensequenz
description: Dieses Thema enthält Informationen zu Fallback-Kostensequenzen für Berechnungen des flexiblen Durchschnitts in Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0538701588b9c71dff4c538711606913a359de6a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428890"
---
# <a name="moving-average-fallback-cost-sequence"></a>Flexible durchschnittliche Fallback-Kostensequenz

Eine Möglichkeit, die Kosten Ihres Inventars zu berechnen, ist die Verwendung von einem _flexiblens Durschnitt_. Jedem Inventargegenstand können bis zu drei Kostenwerte zugeordnet werden:

- **Letztes Problem** – Die letzten Ausgabekosten, die zugewiesen wurden, bevor der Lagerbestand negativ wurde
- **Aktive Kosten** – Die letzten Kosten, die in einer Kalkulationsversion aktiviert wurden
- **Stückpreis** – Die Kosten, die für das freigegebene Produkt angegeben sind

Um zu bestimmen, welcher dieser Kostenwerte für Berechnungen des flexiblen Durchschnitts verwendet werden soll, verwendet das System eine _Fallback-Kostenfolge_, um die Präferenzreihenfolge für die Werte festzulegen. Wenn der bevorzugte Kostenwert nicht verfügbar ist, verwendet das System den nächstvorzugten Wert usw.

In früheren Versionen von Microsoft Dynamics 365 Supply Chain Management verwendete das System eine feste Fallback-Kostensequenz (_Letzte Ausgabe – Aktive Kosten – Artikelpreis_). In Version 10.0.11 ist diese Sequenz immer noch die Standardsequenz. Sie können jedoch auch eine Funktion aktivieren, mit der Sie zwischen drei verfügbare Fallback-Kostensequenzen auswählen können. Diese Funktion kann besonders nützlich sein für Organisationen, die regelmäßig negative Inventarwerte verwenden.

Um den Selektor für die Fallback-Kostensequenz verfügbar zu machen, müssen Sie (oder ein Administrator) [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um die benannte Funktion _Gleitende durchschnittliche Fallback-Kostenfolge_ zu aktivieren.

Führen Sie die folgenden Schritte aus, um die Fallback-Kostenfolge für Berechnungen des flexiblen Durchschnitts auszuwählen.

1. Öffnen der Seite **Parameter**:
2. Auf der Registerkarte **Bestandsbuchhaltung** im Abschnitt **Gleitender Durchschnitt** stellen Sie legen Sie das Feld **Fallback-Kostenfolge** auf einen der folgenden Werte fest:

    - **Letzte Ausgabe – Aktive Kosten – Artikelpreis** – Diese Sequenz ist die Standardsequenz. Es ist die gleiche Sequenz, die verwendet wird, wenn die _Gleitende durchschnittliche Fallback-Kostenfolge_ Funktion nicht aktiviert ist.
    - **Aktive Kosten – Letztes Problem**
    - **Aktive Kosten – Artikelpreis** – Organisationen können Leistungsprobleme haben, wenn sie Geschäftsprozesse verwenden, bei denen der Lagerbestand regelmäßig negativ wird und gleichzeitig das Transaktionsvolumen hoch ist. Diese Einstellung kann dazu beitragen, diese Leistungsprobleme zu verringern.

![Bestandsbuchhaltungsparameter](media/inventory-accounting-parameters.png "Bestandsbuchhaltungsparameter")
