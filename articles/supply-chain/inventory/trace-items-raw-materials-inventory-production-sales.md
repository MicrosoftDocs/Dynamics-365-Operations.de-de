---
title: Verfolgen von Artikeln und Rohmaterialien im Bestand, in der Produktion und im Verkauf
description: "In diesem Thema wird beschrieben, wie Sie Artikelverfolgung verwenden können, um erkennen zu können, wo Artikel oder Rohmaterial verwendet wurden, verwendet werden oder zukünftig in der Produktion und in den Verkaufsprozessen verwendet werden."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30191
ms.assetid: fdd0939a-855c-430f-a684-94f3baea1df4
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5c901dfa448a320d447b43dd5ab80417229f388b
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017

---

# <a name="item-and-raw-material-tracing-in-inventory-production-and-sales"></a>Verfolgen von Artikeln und Rohmaterialien im Bestand, in der Produktion und im Verkauf

[!include[banner](../includes/banner.md)]


In diesem Thema wird beschrieben, wie Sie Artikelverfolgung verwenden können, um erkennen zu können, wo Artikel oder Rohmaterial verwendet wurden, verwendet werden oder zukünftig in der Produktion und in den Verkaufsprozessen verwendet werden.

Artikelverfolgungsfunktionen sind auf der Seite **Artikelverfolgung** verfügbar. Die folgenden Abschnitte beschreiben, wie Sie die Artikelverfolgung verwenden können und welche Optionen und Einschränkungen es gibt.

## <a name="what-is-item-tracing"></a>Was ist Artikelverfolgung?
Die Artikelverfolgung ist ein Business Intelligence-Tool (BI), das Einblick in die Quelle und in das Ziel von Artikeln und Rohmaterial in der Lieferkette bereitstellt. Hersteller können Artikel, Rohmaterial oder Inhaltsstoffe bis zu dem Kreditor nachverfolgen, sowie für die Produktion und Verkauf des Produkts weitergeleitet werden. Artikelverfolgung hilft den Herstellern die gesetzlichen Vorgaben einzuhalten und hilft Qualitätsverantwortlichen und Produktionsleitern, Abweichungen in der Qualität von Produkten und Material zu analysieren und Maßnahmen zu ergreifen, um diese zu beheben. Hier finden Sie einige Beispiele der Methoden, wie Hersteller die Artikelverfolgung verwenden können:

-   Erkennen der Menge eines Artikels oder des Rohmaterials, das aktuell auf Lager ist und wo es gelagert wird.
-   Festlegen, wie viel des Artikels oder des Rohmaterials versendet wurde und an welche Kunden.
-   Kennzeichnen Sie alle geplanten Lieferungen, die den Artikel oder das Rohmaterial enthalten.
-   Suchen Sie Produktionsaufträge, die den Artikel oder das Rohmaterial verwenden und geplant sind, in Bearbeitung sind oder die als abgeschlossen gemeldet wurden.
-   Herausfinden, wo der Artikel oder das Rohmaterial gekauft wurden.
-   Untersuchen, wo ein Artikel oder ein Rohmaterial für die Produktion eines anderen Artikels verbraucht wurde.

## <a name="what-can-i-trace-and-are-there-any-limitations"></a>Was kann ich verfolgen und gibt es Einschränkungen?
Sie können historische Lagerbuchungen für Artikel und Rohmaterial auf Basis einer Artikelnummer und einer Rückverfolgungsangabe, wie einer Seriennummer, einer Chargennummer oder einer Kreditorenchargennummer verfolgen. Sie können einen Artikel oder ein Rohmaterial nur nachverfolgen, wenn diesem eine Rückverfolgungsangabe zugeordnet ist. Da die Verfolgung auf Lagerbuchungen basiert, gibt es einige Einschränkungen, wenn man Artikel nachverfolgt. Es gibt beispielsweise Einschränkungen, die Transaktionen für Projekte, den Anlagen und dem Einzelhandel zugeordnet sind. Außerdem werden Kuppelprodukte in den Verfolgungsdetails angezeigt, aber Nebenprodukte sind nicht enthalten. Die Verfolgung umfasst alle Lagerortbuchungen von einem Lagerplatz zu einem anderen. Daher kann die Menge der Informationen für den Benutzer überwältigend sein. Die Verfolgung wird für jeweils eine juristische Person zur Zeit angezeigt. Es gibt keine unternehmensübergreifenden Funktionen in einem Intercompany-Kontext. Sie müssen eine neue Verfolgung für jedes Unternehmen beginnen, das einen Artikel empfängt oder ausgibt.

## <a name="what-criteria-can-i-specify-for-an-item-trace"></a>Welche Kriterien kann ich für eine Artikelverfolgung angeben?
Die Kriterien, die für eine Artikelverfolgung erforderlich sind, sind die Artikelnummer, eine Rückverfolgungsangabe (wie eine Chargennummer oder Seriennummer) und die Richtung. In der folgenden Tabelle werden die Kriterien, die Sie in einer Artikelverfolgung verwenden können, beschrieben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Feldgruppe</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Artikelnummer</td>
<td>Geben Sie die Kennung für den Artikel oder das Rohmaterial ein, dass Sie erfassen.</td>
</tr>
<tr class="even">
<td>Produktdimensionen</td>
<td>Optional: Verfolgen Sie bestimmte Aspekte der Produktdefinition, wie eine Konfiguration, Größe, Farbe oder einen Stil nach.</td>
</tr>
<tr class="odd">
<td>Rückverfolgungsangaben</td>
<td>Geben Sie eine Chargennummer, die Kreditorenchargennummer oder Seriennummern als Rückverfolgungsangabe ein. Wenn Sie eine Chargennummer als Kriterium verwenden, wird die Kreditorenchargennummer angezeigt, wenn diese Informationen erfasst wurde.</td>
</tr>
<tr class="even">
<td>Lagerdimensionen</td>
<td>Optional: Verfolgt die Artikel nach, die in einem bestimmten Ort gespeichert wurden.</td>
</tr>
<tr class="odd">
<td>Zeitraum</td>
<td>Optional: Geben Sie Daten ein, um die Verfolgung auf eine bestimmte Periode zu begrenzen. Die Verfolgungsdetails werden nur Dokumente und Transaktionen anzeigen, die zwischen diesen Daten erstellt wurden.</td>
</tr>
<tr class="even">
<td>Vorwärts oder rückwärts</td>
<td>Wählen Sie die Richtung für die Verfolgung aus. Sie können vorwärts oder rückwärts verfolgen:
<ul>
<li><strong>Rückwärts</strong> – Nachverfolgen des Downstreams, um die Quelle, die am Lager verbleibende Menge und alle Produktionsaufträge zu erkennen, die mindestens teilweise als fertig gemeldet wurden.</li>
<li><strong>Vorwärts</strong> – Nachverfolgen des Upstreams, um das Ziel zu ermitteln. Sie können die Aufträge und die Kunden finden, zu denen der verfolgte Artikel oder das Rohmaterial mindestens teilweise geliefert wurde.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="what-information-is-included-in-the-trace-details"></a>Welche Informationen sind in die Verfolgungsdetails einbezogen?
Die Ergebnisse einer Verfolgung werden in chronologischer Reihenfolge in der Struktur des Inforegisters **Details** auf der Seite **Artikelverfolgung** angezeigt. Der Auftrag variiert, abhängig von der Ablaufverfolgungsrichtung. Die Details enthalten alle Transaktionen, vom Einkauf des Artikels vom Lieferanten bis hin zum Verkauf an den Kunden. Verfolgungsergebnisse enthalten außerdem Zwischenprodukte, die dem aktuellen Artikel oder den Rückverfolgungsangaben zugeordnet werden, die in den Verfolgungskriterien angegeben wurden. Der Knoten der obersten Ebene zeigt die Menge des Artikels in der Lagereinheit, die entsprechend den Lagerdimensionen am Lager verbleibt, die in den Verfolgungskriterien angegeben wurden. **Hinweis:** Die Verfolgungsdetails sind eine Momentaufnahme der Informationen, die verfügbar waren, als die Verfolgung ausgeführt wurde. Die Verfolgungsdetails werden nicht aktualisiert, wenn die Informationen geändert wurden, nachdem die Verfolgung ausgeführt wurde.

## <a name="why-dont-some-nodes-contain-any-details"></a>Warum beinhalten mehrere Knoten nicht alle Details?
Um die Menge von Informationen in den Verfolgungsdetails zu reduzieren, umfasst nur der Knoten für die erste Instanz des Artikels oder des Rohmaterials Details. Wenn ein ausgewählter Knoten keine Details enthält, können Sie den Knoten anzeigen, der die Informationen enthält, indem Sie auf **Zur verfolgten Position** klicken. Sie können dann zu dem Knoten zurückkehren, den Sie verlassen haben, indem Sie auf **Zurück** klicken.

## <a name="can-i-view-only-a-particular-type-of-document-for-example-can-i-view-only-production-orders-customers-or-vendors"></a>Kann ich nur einen bestimmten Dokumenttyp sehen? So kann ich nur Produktionsaufträge, Debitoren oder Kreditoren sehen?
Ja, Sie können Listenseiten, die nur einen bestimmten Dokumenttyp oder eine Transaktion enthalten, aus den Verfolgungsdetails öffnen. Sie können auf diese Seiten mithilfe des Menüelements **Verfolgen** im Aktivitätsbereich der Gruppen **Artikel**, **Vertrieb**, **Einkauf**, **Produktion** und **Qualität** zugreifen. Um beispielsweise eine Liste der Lieferanten in den Verfolgungsdetails anzuzeigen, klicken Sie auf **Verfolgung** &gt; **Einkauf** &gt; **Lieferanten**. Die Listenseiten fassen die Dokumente oder die Transaktionen der Verfolgungsdetails zusammen. Auf den Listenseiten **Ausstehende Buchungen**, **Ausstehende Aufträge** und **Nicht gelieferte Aufträge** werden auch die Informationen angezeigt, die nicht in den Verfolgungsdetails enthalten sind. Darüber hinaus zeigen sie immer Ergebnisse an, die auf dem aktuellen Datum basieren, auch wenn ein Datumsbereich angegeben wurde. In der folgenden Tabelle werden die zusätzlichen Details beschrieben, die diese Seiten enthalten können.

| Listen                    | Beschreibung                                                                                                                                                                                                                                                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nicht gelieferte Aufträge | Hier werden Auftragspositionen angezeigt, die nicht entnommen wurden und daher nicht in den Verfolgungsdetails angezeigt werden.                                                                                                                                                                                                                        |
| Ausstehende Aufträge           | Hier werden alle ausstehenden Produktionsaufträge für den verfolgten Artikel, unabhängig von den Rückverfolgungsangaben, angezeigt, die in den Verfolgungskriterien verwendet wurden. Sie können auch ausstehende Produktionsaufträge anzeigen, in denen der verfolgte Artikel eine Substanz ist, bei dem keine Erfassungen erfolgt ist und keine Transaktionen für den Auftrag als beendet gemeldet sind. |
| Ausstehende Buchungen     | Ansicht der schwebenden Lagerbuchungen für den verfolgten Artikel, der die angegebenen Rückverfolgungsangaben oder eine leere Rückverfolgungsangabe umfasst. Sie können auch ausstehende Lagerbuchungen für Artikel und Rückverfolgungsangabekombinationen oder einen leeren Wert in den Verfolgungsdetails anzeigen.                                                |

## <a name="how-many-levels-can-i-trace-up-or-down-in-a-bom-or-formula"></a>Wie viele Ebenen kann ich in einer Stückliste oder in einer Formel hoch und runter verfolgen?
Sie können eine Ebene in einer Stückliste oder in einer Formel hoch und runter verfolgen. Wenn Sie beispielsweise eine Verfolgung auf Rohmaterial ausführen, können Sie die fertigen Produkte und alle Kuppelprodukte finden. Wenn Sie jedoch ein Kuppelprodukt verfolgen, enthalten die Verfolgungsdetails nicht das fertige Produkt.

## <a name="how-can-i-view-more-details-about-a-document-or-transaction-in-the-trace-details"></a>Wie lassen sich weitere Details zu einem Dokument oder einer Transaktion in den Verfolgungsdetails anzeigen?
Im Inforegister **Details** können Sie auf zwei Arten weitere Informationen zu einem ausgewählten Dokument oder einer Transaktion in den Verfolgungsdetails anzeigen:

-   Wenn Sie einen Knoten in den Verfolgungsdetails auf dem Inforegister **Details** auswählen, zeigen die anderen Inforegister im Formular Informationen zum Dokument oder Transaktion im Knoten an.
-   Sie können für das Dokument in einem ausgewählten Knoten die Detailseite öffnen, indem Sie auf **Details anzeigen** klicken. Wenn Sie beispielsweise einen Knoten auswählen, der einen Produktionsauftrag beschreibt und Sie auf **Details anzeigen** klicken, wird die Seite **Produktionsauftragsdetails** angezeigt.

Einige Inforegister geben Ihnen Zugriff auf zusätzliche Informationen zum ausgewählten Knoten . Sie können im Inforegister **Qualitätsmangel** beispielsweise testen, ob es eine Historie der Qualitätsmängel gibt, indem Sie auf **Abfragen** klicken. Im Inforegister **Charge** können Sie auf **Bestandsliste** klicken, um die Menge des physischen Bestands, der derzeit verfügbar ist, und die Lagertransaktionen zu dieser Charge anzuzeigen.

## <a name="can-i-run-more-than-one-trace-and-then-compare-the-details"></a>Kann ich mehr als eine Verfolgung ausführen und dann die Details vergleichen?
Nachdem Sie die Verfolgung ausgeführt haben, können Sie die folgenden Optionen auf der Schaltfläche **Ausgangsknoten für Verfolgung** verwenden, um eine neue Verfolgung zur Transaktion im ausgewählten Knoten auszuführen.

-   **Rückwärts** oder **Vorwärts** - Starten Sie eine neue Verfolgung für den ausgewählten Knoten, und überschreiben Sie die Details der aktuellen Verfolgung.
-   **Neu (rückwärts)** oder **Neu (vorwärts)** - Starten Sie eine neue Verfolgung in einem neuen Fenster, und behalten Sie die Details der aktuellen Verfolgung.

Wenn Sie die Option **Neu rückwärts** oder **Neu vorwärts** anwenden möchten, müssen Sie die Funktion **In einem neuen Fenster öffnen** verwenden, um eine neue Verfolgung in einem neuen Fenster anzeigen zu können.

## <a name="can-i-save-the-trace-details"></a>Kann ich die Verfolgungsdetails speichern?
Sie können die Informationen auf der Registerkarte **Details**als XML-Datei speichern, indem Sie auf **Exportieren** unterhalb der Aktion ****Verfolgung**** im Aktivitätsbereich klicken. Neben den Verfolgungsdetails beinhaltet die XML-Datei auch die Verfolgungskriterien, übergeordnete Knoten und die verfügbare Menge. Die Möglichkeit, eine Verfolgung zu speichern ist zweckmäßig, wenn Sie die Informationen beispielsweise einem Qualitätsprüfungsauftrag oder einer anderen Kompatibilitätsdokumentation hinzufügen möchten. Sie können angeben, wo die Datei gespeichert wird. Aktivieren Sie zum sofortigen Anzeigen der Datei das Kontrollkästchen **Dokument anzeigen**. **Hinweis:** Die Datei wird immer gespeichert, auch wenn Sie sie nur anzeigen möchten. Die XML-Datei wird standardmäßig in einem Browserfenster geöffnet. Sie können jedoch auch mit der rechten Maustaste auf die Datei klicken, **Öffnen mit** auswählen, und dann das Programm auswählen, mit dem Sie die Inhalte anzeigen möchten.

## <a name="can-i-calculate-a-balance-for-a-particular-item-or-ingredient"></a>Kann ich einen Saldo für einen bestimmten Artikel oder eine Substanz berechnen?
Sie können die Informationen aus den zusammengefassten Seiten in Microsoft Excel exportieren. Öffnen Sie die entsprechende Seite, klicken Sie auf das Symbol **In Microsoft Office öffnen** , und wählen Sie dann **Nach Microsoft Excel exportieren** aus. Diese Funktion ist insbesonders dann hilfreich, wenn Sie einen Massensaldo für einen Artikel oder eine einzelne Substanz von der Seite **Buchungszusammenfassung** berechnen möchten. Auf der Seite **Buchungszusammenfassung** können Sie nach Artikel oder Substanz und wahlweise nach Charge filtern und dann die Informationen in Excel exportieren. In Excel können Sie beispielsweise die verfügbare Menge, die Menge, die verkauft wurde, und den Betrag, der in der Produktion verwendet wurde, isolieren.

## <a name="can-i-investigate-whether-there-is-a-history-of-issues-with-items-or-raw-materials"></a>Kann ich herausfinden, ob es eine Historie der Probleme mit Artikeln oder Rohmaterialien gibt?
Die Verfolgungsdetails enthalten Informationen zu Qualitätsprüfungsaufträgen und Qualitätsmängeln, die den Artikel oder das Rohmaterial einschließen. Sie können eine Zusammenfassung von Qualitätsprüfungsaufträgen und von Qualitätsmängeln anzeigen, indem Sie im Aktivitätsbereich auf **Qualitätsprüfungsaufträge** oder **Qualitätsmangel** klicken. **Hinweis:** Qualitätsprüfungsaufträge mit Zerstörungstests können mehrmals in den Verfolgungsdetails erscheinen. Wenn für ein Dokument, z.B. eine Bestellung, ein Qualitätsprüfungsauftrag mit Zerstörungstest erstellt wird, wird dieser für jede Transaktion dieses Dokuments angezeigt.

## <a name="are-there-any-reporting-capabilities-that-are-related-to-item-tracing"></a>Gibt es Berichtsfunktionen, die der Artikelverfolgung zugeordnet werden?
Sie können den Bericht **Geliefert an Debitoren** generieren, um die Menge des versendeten Artikels oder des Rohmaterials und die Kunden zu identifizieren, an die er oder es geliefert wurde. Bei einer Abfrage, die einer Konformität zugeordnet ist, können Sie den Bericht für alle Kunden generieren. Für eine Abfrage, die dem Kundendienst zugeordnet ist, können Sie den Bericht für einen ausgewählten Kunden generieren. Wenn das Produkt ein Rohmaterial war, das für die Produktion eines Fertigartikels verwendet wurde, ist der Fertigartikel auch enthalten. **Hinweis:** Wenn Sie die Features für das Löschen oder das Archivieren von Aufträgen verwenden, enthalten die Berichtsergebnisse auch alle Aufträge, die gelöscht oder archiviert wurden.

## <a name="can-i-trace-coproducts-and-byproducts"></a>Kann ich Kuppel- und Nebenprodukte verfolgen?
Sie können Kuppelprodukte aber keine Nebenprodukte nachverfolgen, da Rückverfolgungsangaben in der Regel nicht Nebenprodukten zugewiesen werden. Wenn Sie einen Artikel nachverfolgen, beinhalten die Verfolgungsdetails alle zugehörigen Kuppelprodukte. Ein Knoten, der ein Kuppelprodukt enthält, umfasst das Wort "Kuppelprodukt" in den Details. Sie können Details zu einem Kuppelprodukt auch anzeigen, indem Sie den Knoten in den Verfolgungsdetails auswählen, und dann auf das Inforegister **Produktion** klicken.

