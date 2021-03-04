---
title: Kostenanalyse für Produktionsauftrag
description: Dieser Artikel bietet Informationen zur Kostenanalyse, die Sie für abgeschlossene und aktuelle Produktionsaufträge ausführen können. Sie können die vorkalkulierten Kosten und tatsächlichen Kosten analysieren, indem Sie die Seite "Preiskalkulation" oder den Bericht "Vor- und Nachkalkulation" verwenden. Sie können für jeden Komponentenartikel, jeden Arbeitsplan-Arbeitsgang sowie für alle indirekten Kosten Informationen zu den vorkalkulierten Kosten sowie zu den Istkosten (und zur entsprechenden Menge) anzeigen.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage, ProdSetupHistoricalCost
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dcc155a7fe5ca16e7543bf5917dbedadef987b62
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428789"
---
# <a name="production-order-cost-analysis"></a>Kostenanalyse für Produktionsauftrag

[!include [banner](../includes/banner.md)]

Dieser Artikel bietet Informationen zur Kostenanalyse, die Sie für abgeschlossene und aktuelle Produktionsaufträge ausführen können. Sie können die vorkalkulierten Kosten und tatsächlichen Kosten analysieren, indem Sie die Seite "Preiskalkulation" oder den Bericht "Vor- und Nachkalkulation" verwenden. Sie können für jeden Komponentenartikel, jeden Arbeitsplan-Arbeitsgang sowie für alle indirekten Kosten Informationen zu den vorkalkulierten Kosten sowie zu den Istkosten (und zur entsprechenden Menge) anzeigen.

Die Istkosten für einen Produktionsauftrag basieren auf dem gemeldeten Verbrauch von Material sowie auf den Arbeitsgängen des Arbeitsplans. Sie können auf die Detailbuchungen zum gemeldeten Materialverbrauch, zu den Arbeitsplan-Arbeitsgängen sowie zu indirekten Kosten für einen Produktionsauftrag über die Seite **Produktionsbuchungen** zugreifen.

## <a name="variance-analysis-for-a-completed-production-order"></a>Abweichungsanalyse bei einem abgeschlossenen Produktionsauftrag
Bei den Produktionsabweichungen handelt es sich um das Ergebnis des Vergleichs zwischen den gemeldeten Produktionsaktivitäten und der Berechnung der Standardkosten für den Produktionsartikel. Die Abweichungen enthalten keinen Vergleich mit den vorkalkulierten Kosten des Produktionsauftrags. Zu den gemeldeten Produktionsaktivitäten zählen der Verbrauch von Material und Arbeitsgängen des Arbeitsplans (inklusive der zugehörigen indirekten Kosten) sowie die als fertig gemeldete Menge. Die folgenden vier Arten von Abweichungen werden berechnet:

-   Losgrößenabweichung
-   Abweichung bei Produktionsmenge
-   Produktionspreisabweichung
-   Abweichung bei Produktionsersetzung

Das folgende Diagramm zeigt die vier Abweichungen zur Erfassung der Differenz zwischen den tatsächlichen Kosten eines Produktionsauftrags und den berechneten Kosten aus dem Kostendatensatz des Artikels am Ende des Produktionsauftrags: 

![Abweichungen, die Unterschiede bei einem abgeschlossenen Produktionsauftrag berücksichtigen](./media/control.jpg) 

Sie können Produktionsabweichungen analysieren, indem Sie die Seite **Abweichung** oder den Bericht **Produktionsabweichung** verwenden. Verwenden Sie die Anzeigeoptionen, um ausführliche Abweichungen nach Artikel und betrieblichen Ressourcen oder nach Kostengruppe anzuzeigen. Die Richtlinie für die Kostenaufschlüsselung in den Lagerparametern bestimmt, ob die Abweichungen nach Kostengruppe verfolgt werden. Sie können auch die Anzeigeoptionen **Einzeln**, **Mehrere** und **Summe** verwenden, um zusammengefasste Abweichungen anzuzeigen. Die Informationen zu detaillierten Abweichungen können helfen, die Quelle der einzelnen Abweichungen zu erkennen. Um Abweichungen vor dem Ende eines Produktionsauftrags vorhersagen zu können, analysieren Sie die ausführlichen Informationen des Berichts **Vor- und Nachkalkulation**.

## <a name="cost-analysis-for-current-production-orders"></a>Kostenanalyse für aktuelle Produktionsaufträge
Separate Berichte enthalten Informationen zu den einzelnen Buchungstypen. Diese Berichte dienen zum Analysieren der Kosten für gemeldete Produktionsaktivitäten. Die Informationen werden ausschließlich für aktuelle Produktionsaufträge mit dem Status **Gestartet** oder  **Als fertig gemeldet** angezeigt.

-   **Material in Bearbeitung** − In diesem Bericht sind die Kommissionierlistenbuchungen aufgeführt, die für die aktuellen Produktionsaufträge ab dem angegebenen Buchungsdatum gemeldet wurden. Der Bericht gibt Aufschluss über die ausgegebene Menge der Komponente sowie über den Einstandsbetrag für die einzelnen Buchungen. Verwenden Sie die Auswahlkriterien für einen einzelnen Komponentenartikel. Sie können beispielsweise Informationen zur Ausgabemenge der Komponente für entsprechende Produktionsaufträge ausdrucken. Die Ausgabemenge wird nicht anhand der fertig gemeldeten Mengen des übergeordneten Artikels aktualisiert. Dadurch kann sich eine Überbewertung der Istmenge von Rohmaterialien ergeben.
-   **Arbeit in Verarbeitung** − In diesem Bericht sind Arbeitsplanbuchungen (oder Einzelvorgangsbuchungen) aufgeführt, die für die aktuellen Produktionsaufträge ab dem angegebenen Buchungsdatum gemeldet wurden. Im Bericht werden die Stunden, der Betrag und die Menge angegeben (sowohl Gutmenge als auch Ausschussmenge) die für jede Buchung gemeldet werden. Er umfasst auch Informationen wie Vorgangsnummer, die Vorgangskennung und die betriebliche Ressource. In diesem Bericht werden auch Gesamtzeit und -betrag für alle Buchungen des Produktionsauftrags und die fertig gemeldete Menge angezeigt.
-   **Indirekte Kosten in Bearbeitung** − In diesem Bericht sind die indirekten Kosten der Produktionsaufträge aufgeführt. Die Werte basieren auf dem gemeldeten Verbrauch durch die Arbeitsgänge des Arbeitsplans und der Komponenten ab dem angegebenen Buchungsdatum. Der Bericht gibt die Art der indirekten Kosten (Zuschlag oder Satz), den Nachkalkulationsbogen-Code für die indirekten Kosten und den Kostenbetrag für jede Buchung an. Der Bericht enthält keine Informationen zur Arbeitsplanlisten- oder Kommissionierlistenbuchung, durch die die indirekten Kosten generiert wurden.
-   **Nachkalkulation für Produktion in Bearbeitung** − In diesem Bericht ist der kombinierte Verbrauch von Material, Arbeitsplanvorgänge sowie indirekte Kosten der Produktionsaufträge ab dem angegebenen Buchungsdatum aufgeführt.
-   **Fertigartikel in Bearbeitung** − In diesem Bericht sind die derzeitigen Produktionsaufträge sowie die fertig gemeldeten Buchungen ab dem angegebenen Buchungsdatum aufgeführt.


<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Allgemeine Ursachen für Produktionsabweichungen](common-sources-of-production-variances.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]