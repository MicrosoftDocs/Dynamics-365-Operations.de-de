---
title: Kostenobjekte
description: Dieser Artikel enthält Informationen zu den Kostenobjekten und beschreibt, wie Kosten und Mengen kumuliert werden. Ein Kostenträger ist eine Entität, für die Kosten und Mengen kumuliert werden. Eine Kostenträgerentität kann entweder ein Produkt oder Produktvarianten, wie Varianten für Format und Farbe sein.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85e590322c75cfb2ad21236af56656061037a4b7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428844"
---
# <a name="cost-objects"></a>Kostenobjekte

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu den Kostenobjekten und beschreibt, wie Kosten und Mengen kumuliert werden. Ein Kostenträger ist eine Entität, für die Kosten und Mengen kumuliert werden. Eine Kostenträgerentität kann entweder ein Produkt oder Produktvarianten, wie Varianten für Format und Farbe sein.  

## <a name="cost-objects"></a>Kostenobjekte

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

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Produktdimensionsgruppe](https://technet.microsoft.com/library/aa499382.aspx)

[Lagerdimensionsgruppe](https://technet.microsoft.com/library/hh209317.aspx)

[Rückverfolgungsangabengruppe](https://technet.microsoft.com/library/hh209465.aspx)

[Neuheiten und Änderungen](../../fin-and-ops/get-started/whats-new-changed.md)

[Kosteneinträge](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]