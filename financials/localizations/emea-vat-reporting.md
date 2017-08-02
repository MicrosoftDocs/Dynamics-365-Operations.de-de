---
title: "MwSt-Berichterstattung für Europa"
description: "Dieses Thema enthält allgemeine Informationen zum Einrichten und Generierung  des Mehrwertsteuer-Auszugs für einige europäische Länder."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: f76e431320414b508728cbe9fe20456f107cbe40
ms.openlocfilehash: 7dc6a32a9babc95cfa4ad031534404cae6fa37ea
ms.contentlocale: de-de
ms.lasthandoff: 06/09/2017

---

# <a name="vat-reporting-for-europe"></a>MwSt-Berichterstattung für Europa

[!include[banner](../includes/banner.md)]


Dieses Thema enthält allgemeine Informationen zum Einrichten und Generierung  des Mehrwertsteuer-Auszugs für einige europäische Länder.

Dieses Thema bietet einen allgemeinen Ansatz zum Einrichten und zum Generieren der Mehrwertsteuererklärung. Dieser Ansatz ist für Benutzer in juristischen Personen in den folgenden Ländern/Regionen üblich:

-   Österreich
-   Belgien
-   Tschechische Republik
-   Estland
-   Finnland
-   Deutschland
-   Lettland
-   Litauen
-   Niederlande
-   Schweden

## <a name="vat-statement-overview"></a>MwSt.-Auszugs, Überblick
Der MwSt-Auszug basiert auf dem Steuerbuchungsbeträgen. Die Generierung eines MwSt. -Auszugs ist Teil des Mehrwertsteuerzahlungsprozesses, der durch die Bank- und Beitragsmehrwertsteuerfunktion implementiert ist. Mithilfe dieses Funkltion können Sie die für eine Periode fällige Mehrwertsteuer berechnen. Die Ausgleichsberechnung enthält die gebuchte Mehrwertsteuer für den ausgewählten Abrechnungszeitraum für die Steuerbuchungen im Formular . Der Prozess zum Berechnen von Daten für einen MwSt.-Auszug basiert auf der Beziehung zwischen  Mehrwertsteuercodes und Mehrwertsteuer-Erklärungscodes, in denen Mehrwertsteuer-Erklärungscodes mit den MwSt.-Auszugsfelder übereinstimmen (oder die Markierungen in XML). Für jeden Mehrwertsteuercode sollen Mehrwertsteuer-Erklärungscodes für jede Buchungsart, zum Beispiel steuerpflichtige Verkäufe, steuerpflichtige Einkäufe, steuerpflichtiger Import eingerichtet werden. Hiermit werden Buchungsarten im Feld Mehrwertsteuercodes für Mehrwertsteuer-Berichte im Abschnitt weiter unten in diesem Thema.

Für jeden Mehrwertsteuer-Erklärungscode soll ein bestimmtes Berichtslayout bestimmt werden. Gleichzeitig werden Mehrwertsteuercodes auf eine bestimmte Mehrwertsteuerbehörde von Mehrwertsteuer-Ausgleichsperioden verknüpft. Für jede Mehrwertsteuer-Behörde sollte ein bestimmtes Berichtslayout bestimmt werden. Auf diese Weise können nur mit Mehrwertsteuer-Erklärungscodes demselben Berichtslayout, das für die Mehrwertsteuerbehörde in Mehrwertsteuer-Abrechnungszeiträume für den Mehrwertsteuercode errichtet wird, in der Berichtseinstellung des Mehrwertsteuercodes ausgewählt werden. Eine Mehrwertsteuerbuchung, die nach dem Buchen eines Auftrags oder eine Erfassung erstellt wurde, enthält einen Mehrwertsteuercode, eine Mehrwertsteuerquelle, Mehrwertsteuerart und Buchungsbeträge (Steuergrundbetrag und Steuerbetrag in der Buchhaltungswährung, in der Mehrwertsteuerwährung und in der Buchungswährung). Durch die Kombination aus Steuerbuchungsattributen, verfassen Buchungsbeträge Gesamtbeträge für die Mehrwertsteuer-Erklärungscodes, die für Mehrwertsteuercodes angegeben werden. Die folgende Abbildung zeigt diese Datenbeziehung.

![Diagramm](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>MwST-Bericht, Einrichtung
Um einen MwSt-Bericht zu zu Erstellen, müssen Sie Folgendes erstellen:

### <a name="sales-tax-authorities-for-vat-reporting"></a>MwST-Behörde für MwST-Beichterstattung

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](/dynamics365/unified-operations/financials/general-ledger/tasks/set-up-sales-tax-authorities). -->
Bevor Sie Mehrwertsteuer-Erklärungscodes einrichten können, müssen Sie das gewünschte Berichtslayout für die Mehrwertsteuerbehörde auswählen. Sie müssen auch das Feld **Berichtslayout** im Bereich **Allgemein** auf der Seite **Mehrwertsteuer-Behörden** auswählen. Dieses Layout wird verwendet, wenn Sie Mehrwertsteuer-Erklärungscodes einrichten.

### <a name="sales-tax-reporting-codes"></a>Mehrwertsteuer-Erklärungscodes

Mehrwertsteuer-Erklärungscodes werden im Feldcodes MwSt. oder markierter Namen im XML-Format eingegeben. Diese Codes werden verwendet, um Beträge für den Bericht zu aggregieren und vorzubereiten. Wenn Sie das elektronische Berichterstellungsformat des MwSt.-Auszugs konfigurieren, werden die Namen der Ergebnisbeträge verwendet. Sie können auf der Seite "Mehrwertsteuer-Erklärungscodes" **Mehrwertsteuer-Erklärungscodes** erstellen und verwalten. Sie müssen jedem Code ein Berichtslayout zuweisen. Nachdem Sie die Mehrwertsteuer-Erklärungscodes erstellt haben, können Sie auf dem Inforegister **Berichtseinstellungen** auf der Seite **Mehrwertsteuercode** auf sie verweisen. <!---For more information, see [Set up sales tax reporting codes](/dynamics365/unified-operations/financials/general-ledger/tasks/set-up-sales-tax-reporting-codes).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>Mehrwertsteuercodes für MwSt-Berichterstattung

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](/dynamics365/unified-operations/financials/general-ledger/tasks/set-up-sales-tax-codes).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the **Sales tax codes** page. The following table describes the transaction types in the report setup for sales tax codes. The calculation includes transactions for all types of sources except sales tax.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Buchungstyp</strong></td>
<td><strong>Die Buchungsart sowie eine Beschreibung der Buchungsart auf dem Buchungstyp</strong></td>
</tr>
<tr class="even">
<td><strong>Steuerpflichtiger Umsatz</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode/</li>
<li>Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>)..</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Steuerfreier Verkauf</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt im Ausland <strong>Steuerart</strong> ist <strong>steuerfreier Umsatz</strong>)..</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Mehrwertsteuer</strong></td>
<td>Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>)..</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Steuerpflichtige Verkaufsgutschrift</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>)..</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Steuerbefreite Verkaufsgutschrift</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt im Ausland <strong>Steuerart</strong> ist <strong>steuerfreier Umsatz</strong>)..</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Mehrwertsteuer auf Verkaufsgutschrift</strong></td>
<td>Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>)..</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Steuerpflichtige Einkäufe</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Steuerfreier Einkauf</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Kauf erfolgt im Ausland <strong>Steuerart</strong> ist <strong>steuerfreier Einkauf</strong>)..</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Vorsteuer</strong></td>
<td>Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Steuerpflichtige Einkaufsgutschrift</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Steuerbefreite Einkaufsgutschrift</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Kauf erfolgt im Ausland <strong>Steuerart</strong> ist <strong>steuerfreier Einkauf</strong>)..</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Mehrwertsteuer auf Einkaufsgutschrift</strong></td>
<td>Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Steuerpflichtiger Import</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Gegenkonto zum steuerpflichtigen Import</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Steuerpflichtige Importgutschrift</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
e<li><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Gegenkonto zur steuerpflichtigen Import-Gutschrift</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Steuerart ist <strong>Steuernutzung</strong>.</li>
d<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Verbrauchssteuer</strong></td>
<td>Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Gegenkonto Verbrauchssteuer</strong></td>
<td>Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Für die Tabelle oben wird angenommen, dass die folgenden Kriterien erfüllt sein: 
> -   Der Steuergrundbetrag ist ein Transaktionsbetrag aus dem Feld **Ursprung in der Buchungswährung**.
> -   Der Steuerbetrag ist ein Transaktionsbetrag aus dem Feld **Aktueller Mehrwertsteuerbetrag in der  Buchungswährung**.

### <a name="configure-the-er-model-and-format-for-the-report"></a>Konfigurieren Sie das ER-Modell und -Format für den Bericht

Sie können Elektronische Berichterstattung (ER) verwenden, um Auszüge und Berichte zu konfigurieren und verschiedene elektronische Datenformate zu exportieren, ohne den X++-Code zu ändern. Zusätzliche Informationen:

-   [Überblick über die elektronische Berichterstellung](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting)
-   [Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
-   [[Lokalisierungsanforderungen - Erstellen Sie eine GER-Konfiguration](/dynamics365/unified-operations/dev-itpro/analytics/electronic-reporting-configuration)

## <a name="countryspecific-resources-for-vat-statements"></a>Länderspezifische Ressourcen für Mehrwertsteuer-Auszüge
Der Mehrwertsteuertyp. im für jedes Land muss den Bedingungen der Gesetzgeber des Lands erfüllen. Es gibt vordefinierten allgemeine Modelle und Formate der MwSt.-Auszügen für die Länder, die in der weiter unten dargestellten Tabelle aufgeführt sind.


| Land        | Weitere Informationen                                                          |
|----------------|---------------------------------------------------------------------------------|
| Österreich        |  [MwSt-Berichtdetails für Österreich](emea-aut-vat-statement-details.md)         |
| Belgien        |                                                                                 |
| Tschechische Republik |  [MwSt.-Berichtsdetails für die Tschechische Republik](emea-cze-vat-statement-details.md)   |
| Estland        |  [MwSt-Berichtadetails für Estland](emea-est-vat-statement-details.md) |
| Finnland        |                                                                                 |
| Deutschland        |                                                                                 |
| Italien          | [MwSt-Berichtdetail für Italien](emea-ita-vat-statements-details.md)            |
| Lettland         | [MwSt-Berichtdetail für Lettland](emea-lva-vat-statement-details.md)           |
| Litauen      | [MwSt-Berichtdetail für Litauen](emea-ltu-vat-statement-details.md)         |
| Niederlande    |                                                                                 |
| Schweden         |                                                                                 |






