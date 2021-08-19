---
title: Verwaltung für technische Änderungen FAQ
description: In diesem Thema finden Sie Antworten auf häufig gestellte Fragen zur Funktion Verwaltung für technische Änderungen.
author: t-benebo
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-25
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ba489358ef2d74e816186f29956aea5538a2432825c7d949e7c9cc23d947b997
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714377"
---
# <a name="engineering-change-management-faq"></a>Verwaltung für technische Änderungen FAQ

[!include [banner](../includes/banner.md)]

In diesem Thema finden Sie Antworten auf häufig gestellte Fragen zur Funktion Verwaltung für technische Änderungen.

## <a name="should-i-track-the-version-in-transactions"></a>Soll ich die Version in Transaktionen verfolgen?

Wenn Sie eine technische Änderungskategorie erstellen, bietet die Seite **Details der technischen Änderungskategorie** eine Option mit dem Namen **Version in Transaktionen verfolgen**. Was ist diese Einstellung, und was bewirkt sie?

- Wenn Sie die Option **Version in Transaktionen verfolgen** auf *Ja* festgelegt haben, wird das Feld **Dimensionsgruppe** so gefiltert, dass es nur Dimensionsgruppen anzeigt, in denen Version eine aktive Dimension ist.
- Wenn Sie die Option **Version in Transaktionen verfolgen** auf *Nein* festlegen, wird das Feld **Dimensionsgruppe** so gefiltert, dass es nur Dimensionsgruppen anzeigt, bei denen die Versionsdimension **keine aktive Dimension** ist.

### <a name="if-you-track-the-version-in-transactions"></a>Wenn Sie die Version in Transaktionen verfolgen

Für technische Kategorien, in denen Sie eine Dimensionsgruppe ausgewählt haben, in der Version eine aktive Dimension ist, werden Sie Versionen in Transaktionen für Produkte in dieser Kategorie verfolgen. In diesem Fall ist das technische Produkt ein Produktstamm, und jede Version des Produkts ist eine Produktvariante, die die Dimension Version verwendet. Andere Dimensionen können zusammen mit der Dimension Versionsverwaltung verwendet werden.

In diesem Fall wird jede technische Version in allen Prozessen als eine Variante behandelt. Wenn Sie also eine bestimmte Variante in einer Transaktion haben (damit Sie feststellen können, welche Variante verkauft oder gekauft wurde), müssen Sie den Bestand für jede Version verwalten, die Produktprogrammplanung wird die Versorgung für jede Version planen, und so weiter. Wenn Sie eine Version aus dem Verkehr ziehen, müssen Sie deren Gültig-ab- und Gültig-bis-Datum manuell anpassen, damit sie die Änderung widerspiegeln. Sie müssen auch Ihren Bestand verwalten, um sicherzustellen, dass Sie keine unbenutzten Versionen von Artikeln in Ihren Lagerorten haben.

Obwohl diese Option mehr Verwaltungsaufwand erfordert, empfehlen wir sie, wenn Sie eine hohe Nachvollziehbarkeit der spezifischen Versionen benötigen, die in jeder Transaktion verwendet werden.

### <a name="if-you-dont-track-the-version-in-transactions"></a>Wenn Sie die Versionsverwaltung in Transaktionen nicht nachverfolgen

Für technische Kategorien, in denen Sie eine Dimensionsgruppe ausgewählt haben, in der Version **nicht** eine aktive Dimension ist, werden **nicht** Versionen in Transaktionen für Produkte in dieser Kategorie verfolgt. Wenn Sie in diesem Fall keine andere Dimension verwenden, ist das technische Produkt ein eigenständiges Produkt. Das Produkt wird immer noch versioniert und Sie können Informationen über bestimmte Versionen (z. B. ihre Stückliste \[Stückliste] und Arbeitsplan) verwalten, aber Sie können nicht mehr nachvollziehen, welche spezifische Version in jeder Transaktion verwendet wurde. Die Gültig-ab- und Gültig-bis-Daten geben die Gültigkeit der jeweiligen Version an.

Diese Option ist viel einfacher zu verwalten, denn wenn Sie von einer Version zu einer anderen wechseln wollen, müssen Sie nur die erforderlichen Änderungen in einem Änderungsauftrag vornehmen und dann die Gültig-ab- und Gültig-bis-Daten in der technischen Version aktualisieren. Die Produktionsprozesse entnehmen dann die erforderliche Stückliste und den Arbeitsplan für das Produkt (und seine spezifische Version).

Die meisten Unternehmen entscheiden sich für diese Option, weil sie Versions- und Änderungsverwaltung bietet, aber nicht den zusätzlichen Aufwand für die Verfolgung der Version in jeder Transaktion, im Bestand und bei der Produktprogrammplanung mit sich bringt.

## <a name="which-fields-are-copied-from-the-released-item-template"></a>Welche Felder werden aus der Vorlage für zugelassene Artikel kopiert?

Wenn eine Engineering-Firma ein technisches Produkt erstellt, wird dieses Produkt als freigegebenes Produkt in der Engineering-Firma erstellt. Das erstellte freigegebene Produkt basiert auf der ausgewählten *Vorlage für freigegebene Artikel*. (Die Vorlage für zugelassene Artikel ist selbst ein bestehendes zugelassenes Produkt.) Die Vorlage für zugelassene Artikel wird auch verwendet, wenn das Produkt für eine Betriebsfirma freigegeben wird. In jedem Fall definiert die Vorlage für zugelassene Artikel die meisten Feldwerte für das zugelassene Produkt, und diese Werte stammen von der zugehörigen Seite **Details zu zugelassenen Artikeln**.

Die folgenden Tabellen zeigen die Felder, die bei diesen Prozessen kopiert werden.

| Inforegister | Felder, die bei der Produkterstellung in der Engineering-Firma kopiert werden | Felder, die bei der Freigabe an eine Betriebsfirma kopiert werden |
|---|---|---|
| **Allgemeines** | Alle Felder im Abschnitt **Verwaltung** | Die gleichen Felder, die für die Engineering-Firma kopiert werden |
| **Einkauf** | Alle Felder | Alle Felder außer **Einheit** |
| **Verkaufen** | Alle Felder in den folgenden Abschnitten: **Verkaufsauftrag**, **Verwaltung**, **Besteuerung**, **Preisaktualisierung**, **Basisverkaufspreis**, **Gebühren**, **Rabatte**, und **Alternativprodukt** | Alle gleichen Felder, die für die Engineering-Firma kopiert werden, außer **Einheit** |
| **Außenhandel** | Alle Felder | Alle Felder |
| **Lagerbestand verwalten** | Alle Felder und Abschnitte *außer* **Physikalische Dimensionen** und **Fanggewicht** | Alle gleichen Felder, die für die Engineering-Firma kopiert werden, außer **Einheit** |
| **Entwerfen**, **Planen**, **Kosten verwalten**, **Projekte verwalten**, **Finanzielle Dimensionen** und **Lagerort** | Alle Felder | Alle Felder außer **Stücklisteneinheit** |
| **Produktvarianten** | Alle Felder im Abschnitt **Standard-Produktvariante** | Die gleichen Felder, die für die Engineering-Firma kopiert werden |

Zusätzlich zu den Feldern, die in der vorherigen Tabelle gezeigt werden, werden alle Standardauftragseinstellungen aus der Vorlage für freigegebene Artikel übernommen, sowohl wenn das Produkt in der Engineering-Firma erstellt wird, als auch wenn es für eine Betriebsfirma freigegeben wird. (Um die Standardauftragseinstellungen für eine Vorlage für zugelassene Artikel anzuzeigen, öffnen Sie die entsprechende Seite **Details zu einem freigegebenen Produkt** und wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Lagerbestand verwalten** die Option **Standardauftragseinstellungen**.)

## <a name="should-i-create-a-separate-legal-entity-for-engineering-products-or-use-an-existing-legal-entity"></a>Soll ich eine eigene juristische Entität für technische Produkte erstellen oder eine bestehende juristische Entität verwenden?

Ihre geschäftlichen Anforderungen bestimmen, ob Sie eine neue juristische Entität für technische Produkte erstellen sollen.

Indem Sie eine separate Engineering-Firma erstellen, können Sie die technischen Daten getrennt halten und dann Änderungen hinzufügen, wenn sie für Ihre lokalen Betriebsfirmen erforderlich sind. Auf diese Weise können Sie die folgenden Ziele erreichen:

- Behalten Sie eine separate Entität, in der die technischen Produkte erstellt und verwaltet werden.
- Verhindern Sie, dass technische Produkte zusammen mit dem Rest Ihrer freigegebenen Produkte erscheinen, bis sie fertig und freigegeben sind.
- Trennen Sie klar zwischen Daten, die von technischen und lokalen Daten diktiert werden.

Andererseits sollten Sie wahrscheinlich eine bestehende juristische Entität als Engineering-Firma verwenden, wenn die folgenden Bedingungen auf Sie zutreffen:

- Sie haben nur eine juristische Entität in Ihrem System, und/oder Sie benötigen keine klare Trennung zwischen den technischen Produkten.
- Sie möchten einige Daten nicht duplizieren, z. B. Ressourcengruppen, Ressourcen, Vorgänge und (vielleicht) Standorte.

## <a name="what-is-the-nomenclature-for-engineering-versions-and-variants"></a>Wie lautet die Nomenklatur für technische Versionen und Varianten?

Die Nomenklatur für technische Produkte und Produktvarianten funktioniert folgendermaßen:

- Für das technische Produkt (d. h. das eindeutige Produkt, wenn keine Dimensionen verwendet werden, oder der Produktstamm, wenn eine Dimension verwendet wird) wird die Nomenklatur der Nummernregel in der Kategorie des technischen Produkts definiert. Dort haben Sie die Möglichkeit, eine Sequenz von Nummern, Textkonstanten und Attributnamen und -werten zu verwenden.
- Für jede Variante eines technischen Produkts (wenn Ihr technisches Produkt ein Produktstamm ist, werden Varianten in der Kategorie des technischen Produkts festgelegt, in der Sie die Dimensionsgruppe angeben) wird die Nummernregel-Nomenklatur für jede Variante in der Dimensionsgruppe definiert. In diesem Fall können Sie die Produkt-ID des Masters sowie die Werte und Namen der Dimensionen verwenden.
