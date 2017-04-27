---
title: Kostenobjekte
description: "Dieser Artikel enthält Informationen zu den Kostenobjekten und beschreibt, wie Kosten und Mengen kumuliert werden. Ein Kostenträger ist eine Entität, für die Kosten und Mengen kumuliert werden. Eine Kostenträgerentität kann entweder ein Produkt oder Produktvarianten, wie Varianten für Format und Farbe sein."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8043c81057b5bb79f405642b199f80fc2fbcd8d4
ms.lasthandoff: 03/31/2017


---

# <a name="cost-objects"></a>Kostenobjekte

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen zu den Kostenobjekten und beschreibt, wie Kosten und Mengen kumuliert werden. Ein Kostenträger ist eine Entität, für die Kosten und Mengen kumuliert werden. Eine Kostenträgerentität kann entweder ein Produkt oder Produktvarianten, wie Varianten für Format und Farbe sein.  

<a name="cost-objects"></a>Kostenobjekte
------------

Auf der Seite **Kostenobjekte** werden alle Kostenobjekte aufgeführt, die für ein Produkt erfasst werden. Die Kostenobjekte werden durch Daten aus den folgenden Ressourcen definiert:

-   Produkt
-   Produktdimensionsgruppe
-   Lagerdimensionsgruppe
-   Rückverfolgungsgruppe

**Hinweis:** Ein Kostenobjekte stellt nur ein Kostenelement des Typs **Direktmaterial** dar. Ein Kostenobjekte und ein Bestandsobjekt unterscheiden sich dadurch, dass ein Kostenträger durch die Lagerungsdimensionen definiert wird, die für den wertmäßigen Bestand ausgewählt werden. Ein Artikel hat zum Beispiel die folgende Konfiguration:

-   **Standort:** Physischer Bestand = Ja, wertmäßiger Bestand = Ja
-   **Lagerort:** Physischer Bestand = Ja, wertmäßiger Bestand = Nein
-   **Chargennummer:** Physischer Bestand = Ja, wertmäßiger Bestand = Nein

In der folgenden Tabelle zeigt, was ein Kostenobjekte ist und was ein Bestandsobjekt ist.

| Objekttyp      | Artikelnummer | Standort | Lagerort | Chargennummer |
|------------------|-------------|------|-----------|-----------|
| Kostenobjekt      |  -           |  -    |           |           |
| Bestandsobjekt |  -           |  -    |   -        |  -         |

## <a name="accumulation-of-costs-and-quantities"></a>Ansammlung von Kosten und Mengen
-   Der Wert im Feld **Wert** ist eine Summe der folgenden Werte:
    -   Phys. Einstandsbetrag
    -   Wertmäßiger Einstandsbetrag
    -   Regulierungen
-   Der Wert im Feld **Menge** ist eine Summe der folgenden Werte:
    -   Empfangen
    -   Abgesetzt
    -   Gebuchte Menge
-   Das Feld **Durchschnittlichen Einheitenkosten** ist ein berechnetes Feld. Der Wert wird berechnet, indem der Wert **Wert** durch den Wert **Menge** geteilt wird.

**Hinweis:** Der Parameter **Physischen Wert einbeziehen** hat keinen Einfluss auf die vorhergehenden Berechnungen.

<a name="see-also"></a>Siehe auch
--------

[Produktdimensionsgruppe](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Lagerdimensionsgruppe](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[Rückverfolgungsgruppe](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Neuheiten oder Änderungen in der Architektur von Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)

[Kosteneinträge](cost-entries.md)




