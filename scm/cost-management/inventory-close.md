---
title: Lagerabschluss
description: "Im Rahmen des Prozesses, um Abgangstransaktionen mit Zugangstransaktionen auszugleichen, können Sie wählen, dass das Hauptbuch ausgeglichen wird, um die Regulierungen widerzuspiegeln, die vorgenommen wurden."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventClosing
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9ff992be8a2a4f1cc0cd3146f138d12267bb74ee
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017

---

# <a name="inventory-close"></a>Lagerabschluss

[!include[banner](../includes/banner.md)]


Im Rahmen des Prozesses, um Abgangstransaktionen mit Zugangstransaktionen auszugleichen, können Sie wählen, dass das Hauptbuch ausgeglichen wird, um die Regulierungen widerzuspiegeln, die vorgenommen wurden.

Durch den Lagerabschluss werden Abgangsbuchungen mit Zugangsbuchungen ausgeglichen. Grundlage hierfür bildet die Lagerbewertungsmethode, die in der Artikelmodellgruppe des Artikels ausgewählt ist. Als Teil des Ausgleichsprozesses können Sie angeben, dass das Hauptbuch mit dem vorgenommenen Regulierungen aktualisiert werden soll. Bis zur Ausführung des Lagerabschlusses oder einer Neuberechnung werden Abgangsbuchungen jedoch zum laufenden Durchschnittseinstandspreis gebucht. 

Nach dem Lagerabschluss sind keine Buchungen in Perioden mehr möglich, die vor dem festgelegten Lagerabschlussdatum liegen, sofern nicht ein abgeschlossener Lagerabschlussprozess storniert wird. Wenn der Lagerabschluss für die Periode ausgeführt wird, die am 31. Januar beendet, können Sie Buchungen nicht buchen, die ein Datum aufweisen, das vor dem am 31. Januar ist. 

Artikel im Lager werden einem der folgenden beiden Lagertypen zugewiesen: Artikel oder Service. Beim Lagerabschluss werden für beide Typen die gleichen Schritte ausgeführt. Jedoch für Dienstleistungsartikel werden nach wie vor Abgänge mit den Zugängen ausgeglichen. 

Wie häufig der Lagerabschlussprozess ausgeführt wird, variiert nach Unternehmen. Jedoch das Buchungsvolumen gibt in der Regel darüber Aufschluss, wie oft ein Lagerabschluss erstellt werden sollte. In den meisten Unternehmen wird der Lagerabschluss zum Monatsende im Rahmen der Abschluss- und Abstimmungsverfahren vorgenommen.

## <a name="inventory-recalculation-and-the-general-ledger"></a>Lagerneuberechnung und Hauptbuch
Sind im Laufe eines Monats oder einer anderen Lagerperiode Regulierungen für das Lager und das Hauptbuch notwendig, kann anstelle eines Lagerabschlusses eine Lagerneuberechnung ausgeführt werden. Durch eine Lagerneuberechnung werden Lagerbuchungen nicht ausgeglichen, sondern reguliert. 

Während der Lagerneuberechnung werden der verfügbare Lagerbestand und Lagerbuchungen reguliert, sowie Lagerneuberechnungen und Lagerabschlüsse ausgeführt. Diese Aufgaben betreffen alle Sachkonten, die mit der ursprünglichen Lagerbuchung verknüpft sind. 

**Beispiel** 

Wenn Sie eine Bestellung aus einem Auftrag erstellen, werden die für den ursprünglichen Auftrag verwendeten Hauptbuchkonten entsprechend aktualisiert. Auch wenn das Sachkonto die Artikelgruppe, die dem Artikel zugewiesen ist, geändert wird, nachdem der Auftrag gebucht wurde und eine Lagerneuberechnung einen Ausgleichsbetrag erstellte, wird der Ausgleichsbetrag auf die ursprünglichen Sachkonten gebucht. Der regulierte Betrag wird nicht in den neuen Sachkonten gebucht, die dem Artikel zugewiesen sind. 

Nach Abschluss der Aktualisierung kann der erstellte Sachkontobeleg überprüft werden, der aufgrund einer dieser Aufgaben gebucht wurde.

1.  Wählen Sie auf der Seite **Abschluss und Regulierung** die Registerkarte **Überblick**  und die Aktualisierung aus, die überprüft werden soll.
2.  Klicken Sie auf **Details**und wählen Sie dann **Beleg**aus.

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a>Auswirkungen des Lagerabschlusses auf das Hauptbuch
Viele der Aufgaben, die Sie auf der Seite **Abschluss und Regulierung** ausführen können, führen zu einer Aktualisierung des Hauptbuchs. Das Hauptbuch wird beispielsweise aktualisiert, wenn Sie Regulierungen des vorhandenen Bestands, Regulierungen bei Lagerbuchungen, Lagerneuberechnungen sowie Lagerabschlüsse durchführen. 

Bei den durch diese Aufgaben aktualisierten Sachkonten handelt es sich um die Sachkonten, die mit der ursprünglichen Lagerbuchung verknüpft sind. Wird beispielsweise ein Auftrag mit einer Bestellung ausgeglichen, werden die für den ursprünglichen Auftrag verwendeten Hauptbuchkonten entsprechend reguliert. Dies gilt auch, wenn sich die Sachkonten der Artikelgruppe, die dem Artikel zugewiesen sind, seit der Buchung des Auftrags geändert haben. Nachdem durch einen Lagerabschluss ein Ausgleichsbetrag erstellt wurde, wird der Ausgleichsbetrag auf die ursprünglichen Sachkonten gebucht, nicht auf die neuen, dem Artikel zugeordneten Sachkonten. Sie können das Hauptbuch auch aktualisieren, indem Sie einen Lagerabschluss stornieren. 

**Hinweise:**

-   Ein Lagerabschluss ist für die Bewertungsmethode "Standardkosten" nicht erforderlich.
-   Bevor Sie die Abschlussprozedur ausführen, können Sie eine Liste der Artikel anzeigen, die während der Aktualisierung nicht ausgeglichen werden können.
-   Es empfiehlt sich, den Lagerabschluss nicht zu Spitzenzeiten auszuführen, um eine gleichmäßigere Verteilung der Berechnungsressourcen zu gewährleisten.

## <a name="the-inventory-close-log"></a> Das Lagerabschlussprotokoll
Nach Fertigstellung des Lagerabschlussprozesses meldet eine Nachricht im Nachrichtencenter möglicherweise, dass ein Einstandspreis pro Einheit falsch ist, da eine Buchung nicht vollständig ausgeglichen werden konnte. 

Vor dieser Meldung wird vom System auf die Artikelnummer sowie auf die betroffene Buchung hingewiesen. In dieser Meldung werden Sie davon in Kenntnis gesetzt, dass der für diese Buchung verwendete Einstandspreis aufgrund des Lagerabschlusses nicht aktualisiert wurde. Die Meldung wird angezeigt, wenn eine Abgangsbuchung nicht ausgeglichen werden kann. 

Im Rahmen des Lagerabschlusses wird jede Finanzdimension durch das System geprüft, um zu ermitteln, ob bis zum angegebenen Abschlusstag mehr Abgänge als Zugänge vorhanden sind. Dieses Ungleichgewicht kann auf die Lagerbuchung einer Bestellung zurückzuführen sein, die wertmäßig noch nicht vollständig gebucht wurde, da die Kreditorenrechnung noch nicht eingegangen ist, oder es kann auf Stücklistenkomponenten zurückzuführen sein, die in der Produktion auf einer höheren Ebene eingesetzt werden und noch nicht wertmäßig gebucht wurden. (Die Unterproduktion ist nicht kostenkalkutiert.) In diesem Fall werden durch den nachfolgenden Abschluss nicht alle Abgänge auf den korrekten Einstandspreis reguliert, da nicht genügend Beleginformationen verfügbar sind. 

Für jedes Abschlussverfahren gibt das System an, ob ein Protokoll mit Warnungen gespeichert wird und angezeigt werden kann. 

Wenn Sie viele Warnungen in der Nachricht erhalten, empfehlen wir, dass Sie folgende Aktionen ausführen:

-   Nehmen Sie eine wertmäßige Aktualisierung der Zugänge vor.
-   Verlegen Sie das Abschlussdatum auf einen späteren Termin.
-   Nehmen Sie eine Neubewertung der Geschäftsabläufe vor.

Unter bestimmten Voraussetzungen lassen sich Warnungen unter Umständen nicht vermeiden. Wird beispielsweise mit Markierungen gearbeitet, und das Finanzdatum der markierten Bestellung liegt nach dem Abschlussdatum, kann das Abschlussdatum nicht geändert werden.

## <a name="reversing-a-completed-inventory-close"></a>Stornieren eines abgeschlossenen Lagerabschlusses
Gelegentlich muss ein bereits abgeschlossener Lagerabschluss storniert werden, um die Ausgleiche wieder in den Zustand zu versetzen, der vor der Ausführung der Regulierungen vorlag. Durch die Stornierung eines abgeschlossenen Lagerabschlusses wird auch das Lager wieder geöffnet, um Buchungen für die entsprechende Periode zu ermöglichen. Auch im Hauptbuch können dann entsprechende Änderungen vorgenommen werden. Nach Abschluss der Anpassungen können Sie den Lagerabschluss für die bearbeitete Periode erneut ausführen. 

**Hinweis:** Es kann jeweils nur die letzte abgeschlossene Lagerbuchungsperiode erneut geöffnet werden. Um einen älteren Lagerabschluss zu stornieren, müssen Sie jeden nachfolgenden Lagerabschluss, beginnend dem letzten Abschluss einzeln stornieren.




