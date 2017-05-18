---
title: Flexibler Durchschnitt
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: da743efaf03b7a087d797cedb9bb6f4e3d4510ca
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="moving-average"></a>Flexibler Durchschnitt

[!include[banner](../includes/banner.md)]


Die folgenden Voraussetzungen gelten, wenn Sie flexible Durchschnittskosten als Nachkalkulationsmethode verwenden.
1.  Richten Sie auf der Seite **Artikelmodellgruppen** eine Artikelmodellgruppe ein, bei der im Feld **Lagermodell** die Option "Gleitender Durchschnitt" ausgewählt ist. **Hinweis:** Standardmäßig, wenn "Gleitender Durchschnitt" ausgewählt ist, sind die Felder **Physischen Bestand buchen** und **Wertmäßigen Bestand buchen** ebenfalls ausgewählt. 

2.  Weisen Sie auf der Seite **Buchung** Konten zu den Konten **Preisdifferenz für gleitenden Durchschnitt** sowie **Kostenneubewertung für gleitenden Durchschnitt** auf der Registerkarte **Bestand** aus. Sie verwenden das Konto **Preisdifferenz für gleitenden Durchschnitt**, wenn Kosten proportional gebucht werden müssen. Dies geschieht aufgrund eines Kostenunterschieds zwischen einem Einkaufsdokument und der Einkaufsrechnung und aufgrund eines Unterschieds zwischen der ursprünglichen Lagermenge und der aktuell verfügbaren Menge. Verwenden Sie das Konto **Kostenneubewertung für gleitenden Durchschnitt**, wenn Sie die gleitenden Durchschnittskosten für ein Produkt auf einen neuen Preis je Einheit anpassen möchten.
3.  Weisen Sie auf der Seite **Freigegebene Produkte** die gleitende Durchschnitts-Artikelmodellgruppe dem Produkt zu. **Hinweis** Der Lagerabschlussprozess enthält nur die Buchungsperiode. Er hat keinerlei Auswirkungen auf Produkte, denen der flexible Durchschnitt als Artikelmodellgruppe zugeordnet ist.

## <a name="convert-to-the-moving-average-costing-method"></a>Umrechnen zur Nachkalkulationsmethode des gleitenden Durchschnitts
Produkte können umgewandelt werden, um die Lagerbewertungsmethode des flexiblen Durchschnitts zu verwenden. Diese Art der Umrechnung geschieht normalerweise am Jahresende, nachdem der letzte Monat des aktuellen Jahres abgeschlossen ist. Sie wird umgesetzt, indem das aktuelle Nachkalkulationsmodell des Produkts verwendet wird. Sie können Ihre Lagernachkalkulationsmethode von einer Nachkalkulationsmethode, die auf dem durchschnittlichen Einstandspreis oder den Standardkosten basiert, zu einer Methode ändern, die auf dem flexiblen Durchschnitt basiert. 

Wenn Sie die Nachkalkulationsmethode von einer standardmäßigen Nachkalkulationsmethode zu einer Methode mit flexiblem Durchschnitt ändern, müssen Sie die folgenden Aufgaben ausführen:

1.  Nehmen Sie Anpassungen vor, um Lagermengen und Werte auf 0 (Null) zu setzen.
2.  Wenn Lagerwert und Menge 0 (Null) sind, ändern die Artikelmodellgruppe auf flexiblen Durchschnitt.
3.  Nehmen Sie Anpassungen vor, um Lagermengen und Werte auf 0 (Null) zu setzen.

Sie können die Bestandsnachkalkulationsmethode nicht von einer Methode mit gleitendem Durchschnitt zu einer FIFO-Methode, einer LIFO-Methode oder einer Methode für den gewichteten Durchschnitt ändern.

**Hinweis** Das Konvertieren von den Standardkosten zum flexiblen gewichteten Durchschnitt ist ein manueller Prozess.

In den folgenden Beispielen werden die Auswirkungen der Verwendung der Nachkalkulationsmethode mit flexiblem Durchschnitt dargestellt. Es gibt vier Arten von Varianten:
-   Bestellung und proportional in Aufwand gebuchte Kostendifferenz
-   Produkt und Lagerregulierung des flexiblen Durchschnitts
-   Flexibler Durchschnitt mit Produktion
-   Flexibler Durchschnitt mit einer rückdatierten Transaktion

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Bestellung und proportional in Aufwand gebuchte Kostendifferenz
Bei flexiblem Durchschnitt werden die Kosten des Produkts mit dem Einkaufszugang bestimmt. Wenn die Einkaufsrechnung gebucht wird und es eine Abweichung zwischen der Kosten auf dem Einkaufsdokument und auf der Einkaufsrechnung gibt, wird der Unterschied proportional auf die aktuellen Produkte im Bestand verteilt, und der Restbetrag in Aufwand gebucht. 

In diesem Beispiel wird eine Bestellung zu einem Preis erstellt und erhalten, und die Einkaufsrechnung wird mit anderen Kosten gebucht.

1.  Erstellen Sie eine Bestellung mit der Menge 2 und einem Preis je Einheit von 10,00.
2.  Erstellen Sie ein Einkaufsdokument des Produkts.
3.  Erstellen Sie einen Auftrag mit der Menge 1 und einem Preis je Einheit von 10,00.
4.  Erstellen Sie eine Einkaufsrechnung mit der Menge 2 und einem Preis je Einheit von 12,00.

Der Unterschied des Preises je Einheit, 2,00, wird zum Konto "Preisdifferenz für gleitenden Durchschnitt" gebucht, wenn die Einkaufsrechnung gebucht wird. Der Grund ist, dass zwei Produkte für einen Einstandspreis von 20,00 gekauft wurden. Eines der Produkte wurde für einen Einheitenpreis von 10,00 verkauft. Die Einkaufsrechnung wurde zu einem Einheitenpreis von 12,00 mit einer Menge von 2 gebucht. Der Preis je Einheit des Produkts kann nicht mit 14,00 gebucht werden.

## <a name="moving-average-product-and-inventory-adjustment"></a>Produkt und Lagerregulierung des flexiblen Durchschnitts
Wenn Sie die flexiblen Durchschnittskosten eines Produkts anpassen müssen, werden Lagerregulierungen ab dem aktuellen Datum zulässig. Sie können eine Lagerregulierung nicht zurückdatieren, um die flexiblen Durchschnittskosten eines Produkts zu korrigieren. Sie können die Kosten nicht durch die folgenden Buchungen fließen lassen. 

In diesem Beispiel werden die flexiblen Durchschnittskosten für ein Produkt angepasst.

1.  Wählen Sie das Produkt aus, für das Sie die gleitenden Durchschnittskosten anpassen möchten. **Hinweis:** Auf der Seite **Neubewertung für gleitenden Durchschnitt** wird der für ein Produkt verfügbare Lagerbestand überprüft. Das Produkt, das aktiviert ist, hat eine gebuchte Menge von 1, einen gebuchten Wert von 12,00, gebuchte Einheitenkosten von 12,00 und Einheitenkosten von 12,00.
2.  Aktualisieren Sie das Feld **Einheitenkosten** auf 16,00. Das System berechnet die verbleibenden Felder.
3.  Die Anpassung wird gebucht.

**Hinweis:** Sie können die flexiblen Durchschnittskosten erst ab dem aktuellen Datum anpassen.

Auf der Seite **Ausgleiche für Beleg** können Sie eine Regulierung von 4,00 sehen, die zum Konto "Kostenneubewertung für gleitenden Durchschnitt" gebucht wird.

## <a name="moving-average-with-production"></a>Flexibler Durchschnitt mit Produktion
Der flexible Durchschnitt unterstützt produzierte Artikel. Wenn Sie planen, den gleitenden Durchschnitt in einer Produktionsumgebung zu verwenden, sollte der Schieberegler **Vorkalkulierten Einstandspreis verwenden** auf der Seite **Produktionssteuerungsparameter**ausgewählt werden. Dies bedeutet, dass der Einstandspreis, der bei der Vorkalkulation berechnet wird, anstelle des tatsächlichen Herstellkostenkalkulationspreises verwendet wird.

## <a name="moving-average-with-a-backdated-transaction"></a>Flexibler Durchschnitt mit einer rückdatierten Transaktion
Rückdatierten Transaktionen werden die aktuellen flexiblen Durchschnittskosten zugeordnet, und die physische Menge des Produkts wird aktualisiert, die flexiblen Durchschnittskosten des Produkts sind jedoch nicht betroffen. In diesem Beispiel für flexiblen Durchschnitt wird eine rückdatierte Transaktion für ein Produkt flexiblen Durchschnitts gebucht.

1.  Erstellen Sie eine Lagerregulierung für das Produkt flexiblen Durchschnitts für eine Menge von 1 und Kosten von 20,00.
2.  Die Lagerbuchungshistorie für das Produkt wird wie folgt aussehen:
    -   Eine Lagerbuchung von 1, Kosten von 16,00, ein Buchungsdatum vom 15. Januar und ein Buchungsdatum vom 15. Januar.
    -   Eine Lagerregulierung von 1, Kosten von 20,00, ein Buchungsdatum vom 1. Januar und ein Buchungsdatum vom 15. Januar.
3.  Buchen Sie die Regulierung.

Auf der Seite **Lagerbuchungen** können Sie sehen, dass 4,00 in Aufwand gebucht wurde, da der aktuelle gleitende Durchschnitt für das Produkt 16,00 ist. Sie können in der Vergangenheit buchen, aber der Unterschied der Kosten wird in Aufwand gebucht, sodass die flexiblen Durchschnittskosten nicht betroffen sind.

## <a name="inventory-value-report"></a>Lagerwertbericht
In diesem Beispiel für flexiblen Durchschnitt wird der Lagerwertbericht gedruckt, um die aktuelle Berechnung des flexiblen Durchschnitts für ein Produkt zu unterstützen. Der Bericht "Lagerwert" kann die Buchungen sowie die Kosten in chronologischer Reihenfolge drucken, um die Berechnung der gleitenden Durchschnittskosten eines Produkts zu unterstützen. Im Bericht werden die flexiblen Durchschnittskosten für das Produkt angezeigt. Im Dialgofeld **Lagerwertberichte** ermöglicht Ihnen ein "Datumsintervall", die **Transaktionsuhrzeit** oder das **Buchungsdatum** auszuwählen, nach denen der Bericht zu sortieren ist. Die Option **Buchungsdatum** legt fest, wie der Bericht üblicherweise gedruckt wird. Die Option **Transaktionsuhrzeit** ist das tatsächliche Datum, an dem die Buchung gemeldet ist und die gleitenden Durchschnittskosten für das Produkt aktualisiert werden. Sie können den Bericht "Lagerwert" drucken, indem Sie die Option**Transaktionsuhrzeit-Sortierung** verwenden, wenn die Berechnung der gleitenden Durchschnittskosten im Laufe der Zeit angezeigt werden sollen. In der folgenden Tabelle werden die Transaktionen für das Produkt angezeigt, für das der Bericht gedruckt wird, wenn die Option **Transaktionsuhrzeit-Sortierung** verwendet wird.

| Transaktionsuhrzeit | Datum         | Transaktionstyp           | Menge | Betrag | Durchschnittliche Einheitenkosten |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1. Oktober    | Anfangssaldo          | 0        | 0,00   | 0,00              |
| 8. Oktober        | 28. September | Zurückdatierte Zugang          | 1        | 16,00  | 16,00             |
| 3. Oktober        | 3. Oktober    | Einkaufslieferung           | 2        | 20,00  | 12,00             |
| 5. Oktober        | 5. Oktober    | Auftrag                | -1       | -10,00 | 13,00             |
| 7. Oktober        | 7. Oktober    | Einkaufsrechnung           |          | 2,00   | 14,00             |
| 8. Oktober        | 8. Oktober    | Neubewertung für flexiblen Durchschnitt |          | 4,00   | 16,00             |
|                  | 31. Oktober   | Gesamt                      | 2        | 32,00  | 16,00             |

 **Hinweis:** Sie können das Hauptbuch nicht mit dem Lagerbestand abstimmen, indem Sie die Option **Transaktionsuhrzeit-Sortierung** verwenden. Der Bericht muss gedruckt werden, indem die Option **Buchungsdatum** verwendet wird.






