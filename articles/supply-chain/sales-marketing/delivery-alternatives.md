---
title: Alternative Lieferung
description: Auftragsabnehmer können die Lieferungsalternativenseite verwenden, um alternative Auftragserfüllungsoptionen zu ermitteln.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 1fbf8f08322c954a482777abcf041ff0b9d8fb77
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555861"
---
# <a name="delivery-alternatives"></a>Alternative Lieferung

[!include [banner](../includes/banner.md)]

Auftragsabnehmer können die **Lieferungsalternativenseite** verwenden, um alternative Auftragserfüllungsoptionen zu ermitteln.

Die neute Seite **Alternative Lieferung** gibt ein besserer Überblick über alle alternativen Optionen. Die Personen, die den Auftrag entgegennehmen können auch hinter das aktuelle Unternehmen blicken, um mehr über die Erfüllungsverkaufschancen zu erfahren. Sie können nun Intercompany-Verkaufschancen und Verkaufschancen von externen Kreditoren anzeigen. Mithilfe der Funktion nach Lieferdatum sortieren, können Auftragsabnehmer eine intelligente Liste der Lieferalternativen anzeigen. Außerdem helfen Parameter, die vorgeschlagenen Lieferungen zu verwalten. Da die Transportzeit die Lieferdaten beeinflussen kann, können Auftragsabnehmer die verschiedenen Transportmöglichkeiten ansehen, die Spediteure anbieten. Da Detailinformationen zu jedem Vorschlag angezeigt werden, können Auftragsannehmer informierte Entscheidungen direkt über die Seite **Lieferalternativen durch Anzeigen** machen.

## <a name="open-the-delivery-alternatives-page"></a>Öffnen Sie die Lieferungsalternativeseite
Sie können die Seite **Alternative Lieferung** aus der Auftragsposition öffnen.

1.  Klicken Sie auf **Produkte und Lieferung** &gt; **Lieferalternativen**.
2.  Klicken Sie auf &gt; **Positionsdetails** **Lieferung** &gt; **Lieferalternativen.**

Sie können auch die Seite **Lieferalternativen** über den Arbeitsbereich **Abfrage Auftragsverarbeitung und -abfrage**. Klicken Sie dann auf **Bestellungen und Favoriten** &gt; **Verzögerte Auftragspositionen** &gt; **Lieferalternativen** **Hinweis:** Sie können die Seite **Lieferalternativen** nur öffnen, wenn beide Bedingungen erfüllt sind:

-   Alle zwingenden Verkaufspositionsinformationen sind ausgefüllt.
-   Das Feld **Lieferdatumskontrolle** ist auf einen anderen Wert als **None** festgelegt.

## <a name="delivery-date-control-methods"></a>Methoden für die Lieferdatumskontrolle
Die Lieferdatumsteuermethode bestimmt, wie das System Versanddatum einrichtet, wie Lieferalternativen berechnet und welche Informationen angezeigt werden. Beachten Sie, dass die Lieferdatumskontrolle Kalender in Erwägung ziehen. Daher können die folgenden Kalender das vorgeschlagene Empfangsdatum betreffen: Kalender, der dem Lagerort zugeordnet ist, Transportkalender, Kreditorenkalender und Kundenkalender. Die folgende Tabelle beschreibt jede Methode zur Lieferdatumskontrolle.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Methode</strong></td>
<td><strong>Beschreibung</strong></td>
</tr>
<tr class="even">
<td><strong>Keines</strong></td>
<td><ul>
<li>Lieferalternativen für Verkaufspositionen werden nicht unterstützt. Diese Option deaktiviert die Lieferdatensteuerung.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Verkaufslieferzeit</strong></td>
<td><ul>
<li>Lieferalternativen werden basierend auf vordefinierten die Verkaufslieferzeit berechnet. Die Transporttage werden aufgrund der Lieferart berechnet.</li>
<li>Lieferalternativen umfassen Lagerorte, die verfügbaren Lagerbestand haben und Angebots-/Nachfrageaufträge.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>VfZ</strong></td>
<td><ul>
<li>Lieferalternativen werden auf Basis der Logik der verfügbaren Zusagen (VfZ) berechnet. Die aktuelle Verfügbarkeit und die erwartete zukünftige Verfügbarkeit werden berücksichtigt. Die Transporttage werden aufgrund der Lieferart berechnet.</li>
<li>Lieferalternativen umfassen Lagerorte, die verfügbaren Lagerbestand haben und Angebots-/Nachfrageaufträge.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>VfZ + Sicherheitszuschlag</strong></td>
<td><ul>
<li>Lieferalternativen werden wie bei der VfZ-Methode berechnet aber der Sicherheitszuschlag ist in der Berechnung berücksichtigt.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>CTP</strong></td>
<td><ul>
<li>Lieferalternativen werden auf Basis der Logik der verfügbaren Zusagen (CTP) berechnet. Mrp-Auflösung wird verwendet, um die Verfügbarkeit festzulegen. Beachten Sie, dass mindestens das CTP Lieferdatum die Verkaufslieferzeit ausgleicht. Die Transporttage werden aufgrund der Lieferart berechnet.</li>
<li>Lieferalternativen umfassen auch für die folgenden Lagerorte:
<ul>
<li>Aktueller Lagerort</li>
<li>Standardlagerort</li>
<li>Alle Lagerorte, die verfügbaren Lagerbestand haben</li>
<li>Alle Lagerorte, die Lieferaufträge haben</li>
<li>Alle Lagerorte, die eine aktive Stücklisten (BOM)- Versionen haben</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a>Hier werden Informationen zu Lieferalternativen angezeigt
Dieser Abschnitt beschreibt die Informationen zu den Lieferalternativen, die auf jeder Registerkarte auf der Seite **Lieferalternativen** verfügbar ist.

### <a name="products"></a>Produkte

Diese Registerkarte zeigt eine Zusammenfassung des Produkts und Details der aktuellen Auftragsposition.

### <a name="delivery-alternatives"></a>Alternative Lieferung

Diese Registerkarte ist eine Liste von Lieferalternativen , die nach Empfangsdatum sortiert sind. Über der Liste können Sie auswählen, welche Optionen basierend auf den Vorschlägen, ausgewählt wird. Sie können auch die Lieferart auswählen, die die Transporttage bestimmt. Die folgenden Optionen sind verfügbar:

-   **Schließen Sie andere Produktvarianten ein** - Diese Option ist auch für Produkte verfügbar, die Produktvarianten haben. Er umfasst Lieferalternativen für weitere Varianten des Produkts. Diese Option ist nicht für CTP verfügbar.
-   **Schließen Sie Teilmenge ein** -, Standardmäßig sind nur Vorschläge verfügbar, die die gesamte Menge der Verkaufsposition einschließen. Wählen Sie diese Option, um Vorschläge einzubeziehen, die der Auftragsposition nur teilweise entsprechen. Diese Option ist hilfreich, wenn der Debitor ein früheres Lieferdatum anfordert und Teillieferung akzeptiert.
-   **Schließen Sie ein späteres Datum** -, Standardmäßig werden nur Anforderungen berücksichtigt, die besser sind (früher) als das aktuelle Datum in der Verkaufsposition. Wählen Sie diese Option aus, um spätere Daten einzuschließen. Diese Option kann in den folgenden Situationen hilfreich sein, in dem Parameter nicht das Datum Priorität haben. So werden beispielsweise ein Kreditor oder ein bestimmter Lagerort bevorzugt werden.
-   **Lieferart** - Wählen den bevorzugten Liefermodus, um Kosten und Transportzeiten zu optimieren. Sie finden die Auswirkungen sofort in den vorgeschlagenen Lieferalternativen. Daher ist es einfach, die Alternativen zu vergleichen.
-   **Beschaffung einschließen** Wenn Beschaffung aktiviert ist, schließen die vorgeschlagenen Lieferalternativen Optionen ein, die sowohl Optionen für externe Kreditoren und andere Unternehmen in der Unternehmensgruppe (Intercompany) ein. Die Option **Beschaffung einschließen** wird für die VfZ-Kalkulation und die Lieferdatumssteuerung VfZ + Sicherheitszuschlag unterstützt. Beschaffungsoptionen vom Standardlieferanten für das Produkt und alle genehmigten Lieferanten für das Produkt sind eingeschlossen.
-   Bei externen Kreditoren basiert die Berechnung auf Grundlage der Lieferzeit.
-   Für Intercompany berücksichtigt die Berechung, was vom Beschaffungsunternehmen verfügbar ist, basierend auf der Lieferdatumskontrolle im Beschaffungsunternehmen.
-   **Liefertyp** (Nur relevant für Beschaffung)
    -   **Bestand** - Produkte werden vom Beschaffungslagerort zum Standort/Lagerort in der Verkaufsposition versendet. Sie werden dann von diesem Lagerort an den Kunden versendet.
    -   **Direktlieferung** - Produkte werden direkt vom Beschaffungslagerort an den Kunden versendet.

### <a name="availability-information"></a>Verfügbarkeitsinformationen

Informationen in dieser Registerkarte beziehen sich auf die Lieferung alternativer ausgewählter Positionen. Die folgenden Informationen werden, je nach spezifischer Lieferdatumskontrolle für die Auftragsposition angezeigt:

-   **Verkaufslieferzeit**
    -   **Verfügbar heute** - Zeigt den aktuellen physischen, physisch reservierten und physisch verfügbaren Bestand an.
    -   **Parameter** - Zeigt die Bestandeinheit und die Verkaufslieferzeit.

-   **VfZ und VfZ + Sicherheitszuschlag für Warenabgang**
    -   **Verfügbar heute** - Zeigt den aktuellen physischen, physisch reservierten und physisch verfügbaren Bestand an.
    -   **Parameter** - Zeigt die Bestandeinheit und die Verkaufslieferzeit.
    -   **Künftige Verfügbarkeit** - Zeigt eine grafische Darstellung der aktuellen und künftigen Verfügbarkeit für den ausgewählten Standort und den Lagerort unter **Lieferalternativen**. Sie können auf die Diagrammspalten klicken, um ausführliche Informationen zur künftigen Verfügbarkeit des Produkts anzuzeigen. Der Schieberegler wird eine Liste relevanter Bedarfs- und Angebotaufträge innerhalb des VfZ-Planungszeitraums anzeigen.

-   **CTP**
    -   **Verfügbar heute** - Zeigt den aktuellen physischen, physisch reservierten und physisch verfügbaren Bestand an.
    -   **Parameter** - Zeigt die Bestandeinheit und die Verkaufslieferzeit.
    -   **Auflösung** - Zeigt eine Lieferauflösung der ausgewählten Lieferalternative. Sie können **Einstellungen** verwenden, um die Felder und die Bestanddimensionen zu ändern, die bei der Auflösung angezeigt werden.

### <a name="impact-of-selected-alternative"></a>Auswirkungen der gewählten Alternative

Diese Registerkarte zeigt die Auswirkungen auf die ausgewählte Lieferungsalternative. Wenn Sie **OK** klicken, wird die Auftragsposition mit den markierten Werte in den Spalten AUSGEWÄHLT aktualisiert. Beachten Sie, dass, wenn die Menge in der ausgewählten Lieferalternative kleiner als die Menge in der Auftragsposition ist, und die Auftragsposition in zwei Positionen aufgeteilt wird: eine Position für die ausgewählte Menge und eine Zeile für die Restmenge. Sie können den Handelszweig auch aktualisieren, damit die Zeitplanpositionen übereinstimmt und die Preiskalkulation beeinflussen.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Lieferterminzusage](delivery-dates-available-promise-calculations.md)




