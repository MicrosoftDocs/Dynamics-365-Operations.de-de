---
title: MwSt Berichterstattung Europa.
description: "Dieses Thema enthält allgemeine Informationen zum Einrichten und Generierung Mehrwertsteuer des Auszugs europäische (VAT)- für einige Länder verfügbar."
author: ShylaThompson
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266844
ms.assetid: 06798e29-6140-489e-9b4e-66b45b26be2b
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 84a639b25c64821e00ca4397f42f69298953e599
ms.lasthandoff: 03/31/2017


---

# <a name="vat-reporting-for-europe"></a>MwSt Berichterstattung Europa.

Dieses Thema enthält allgemeine Informationen zum Einrichten und Generierung Mehrwertsteuer des Auszugs europäische (VAT)- für einige Länder verfügbar.

Dieses Thema bietet einen allgemeinen Ansatz zum Einrichten und zum Generieren der Mehrwertsteuererklärung. -Auszugs. Durch diesen Ansatz ist für Benutzer in juristischen Personen in den folgenden Land/Region wird:

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

## <a name="vat-statement-overview"></a>MwSt.-Auszugsüberblick
Der Mehrwertsteuertyp. im basiert auf die Beträge der Steuerbuchungen. Die Generierung eines MwSt. -Auszugs ist Teil des Mehrwertsteuerzahlungsprozesses, der durch die Bank- und Beitragsmehrwertsteuerfunktion implementiert ist. Diese Funktion wird die Mehrwertsteuer, die für eine Periode fällige ist. Die Ausgleichsberechnung enthält die gebuchte Mehrwertsteuer für die ausgewählte Ausgleichsperiode für Steuerbuchungen. Der Prozess zum Berechnen von Daten für ein MwSt. im ist auf Basis der Beziehung zwischen Mehrwertsteuercodes und Mehrwertsteuer-Erklärungscodes, in denen Mehrwertsteuer-Erklärungscodes die MwSt. -Auszugsfelder übereinstimmen (oder die Markierungen in XML). Für jeden Mehrwertsteuercode sollen Mehrwertsteuer-Erklärungscodes für jede Buchungsart, z steuerpflichtigen Verkäufe eingerichtet werden, steuerpflichtigen Einkäufe, steuerpflichtiger Import. Hiermit werden Buchungsarten im Feld [Mehrwertsteuercodes für Mehrwertsteuer. Berichte in Bezug]( #Sales Steuercodes für Mehrwertsteuer. Berichte in Bezug,) beschrieben, Abschnitt weiter unten in diesem Thema.

Für jeden Mehrwertsteuer-Erklärungscode soll ein bestimmtes Berichtslayout bestimmt werden. Gleichzeitig werden Mehrwertsteuercodes auf eine bestimmte Mehrwertsteuerbehörde von Mehrwertsteuer-Ausgleichsperioden verknüpft. Für jede Mehrwertsteuerbehörde soll ein Berichtslayout bestimmt werden. Auf diese Weise können nur mit Mehrwertsteuer-Erklärungscodes demselben Berichtslayout, das für die Mehrwertsteuerbehörde in Mehrwertsteuer-Abrechnungszeiträume für den Mehrwertsteuercode wird festgelegt, in der Berichtseinstellung des Mehrwertsteuercodes ausgewählt werden. Eine Mehrwertsteuerbuchung generierte nach dem Buchen eines Auftrags, oder eine Erfassung, enthält einen Mehrwertsteuercode, eine quelle Mehrwertsteuer, eine und Mehrwertsteuerart Buchungsbeträge (und -Steuerbetrag Steuergrundlagenbetrag in der Buchhaltungswährung, in der Mehrwertsteuerwährung und in der Buchungswährung). Durch die Kombination aus Steuerbuchungsattributen, verfassen Buchungsbeträge Gesamtbeträge für die Mehrwertsteuer-Erklärungscodes, die für Mehrwertsteuercodes angegeben werden. Die folgende Abbildung zeigt die Datenenbeziehung angezeigt.

![Diagramm](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>MwSt.-Auszugseinstellung
Um einer Mehrwertsteuererklärung. im zu generieren müssen Sie Folgendes einrichten.

### <a name="sales-tax-authorities-for-vat-reporting"></a>Mehrwertsteuerbehörden für Mehrwertsteuer. Berichte in Bezug

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-authorities/). -->
Bevor Sie Mehrwertsteuer-Erklärungscodes einrichten können, müssen Sie das gewünschte Berichtslayout für die Mehrwertsteuerbehörde auswählen. Auf der Mehrwertsteuerbehörden ** ** Seite im ** Allgemein ** Abschnitt, wählen Sie eine aus ** Berichtslayout **. Dieses Layout wird verwendet, wenn Sie Mehrwertsteuer-Erklärungscodes einrichten.

### <a name="sales-tax-reporting-codes"></a>Mehrwertsteuer-Erklärungscodes

Mehrwertsteuer-Erklärungscodes werden im Feldcodes MwSt. im oder markiert Namen im XML-Format. Diese Codes werden verwendet, um Beträge für den Bericht zu aggregieren und vorbereitet. Wenn Sie das elektronische Berichterstellungsformat des MwSt.-Auszugs konfigurieren, werden die Namen der Ergebnisbeträge verwendet. Sie können auf der Mehrwertsteuer-Erklärungscodes ** Mehrwertsteuer-Erklärungscodes ** Seite erstellen und verwalten. Sie müssen jeden Code ein Berichtslayout zuweisen. Nachdem Sie die Mehrwertsteuer-Erklärungscodes erstellt haben, können Sie die Codes im ** der Bericht eingerichtet ** Abschnitt auf der Mehrwertsteuercodes ** ** Seite auswählen. <!---For more information, see [Set up sales tax reporting codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-reporting-codes/) and [Sales tax reporting codes page (Field descriptions)](http://ax.help.dynamics.com/en/wiki/sales-tax-reporting-codes-page-field-descriptions/).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>Mehrwertsteuercodes für Mehrwertsteuer. Berichte in Bezug

 Und Grundbeträge Steuerbeträge Mehrwertsteuerbuchungen können auf Erklärungscodes im MwSt. im zusammengefasst werden (XML-Markierungen oder Meldungsfelder). Sie können dieses einrichten, indem von Mehrwertsteuer-Erklärungscodes für verschiedene Buchungsarten für Mehrwertsteuercodes auf der Seite ** ** Mehrwertsteuercodes zugeordnet. Die folgende Tabelle beschreibt die Buchungsarten im Bericht, der für Mehrwertsteuercodes eingerichtet ist. Die Berechnung umfasst Buchungen für alle Typen Quellen außer Mehrwertsteuer.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Transaction type</strong></td>
<td><strong>Beschreibung von den auf der Buchungsart zu zählenden Buchungen und Beträgen,</strong></td>
</tr>
<tr class="even">
<td><strong>Steuerpflichtiger Umsatz</strong></td>
<td>Summe <strong>Steuergrundlagebeträge</strong> Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist im ausgewählten Zeitraum</li>
<li>Der Verkauf erfolgt inländisch (ist)<strong>Steuerart</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; das 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Steuerfreier Verkauf</strong></td>
<td>Summe <strong>Steuergrundlagebeträge</strong> Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li>Der Verkauf erfolgt (<strong>Steuerart</strong> Export).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; das 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax payable</strong></td>
<td>Summe <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li>Der Verkauf erfolgt inländisch (ist)<strong>Steuerart</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; das 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable sales credit note</strong></td>
<td>Summe <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li>Der Verkauf erfolgt inländisch (ist)<strong>Steuerart</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; das 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Ausgenommene des Faxes Verkaufsgutschrift</strong></td>
<td>Summe <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li>Der Verkauf erfolgt (<strong>Steuerart</strong> Export).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; das 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on sales credit note</strong></td>
<td>Summe <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li>Der Verkauf erfolgt inländisch (ist)<strong>Steuerart</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; das 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable purchases</strong></td>
<td>Summe <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li>Der Kauf ist inländisch (ist)<strong>Steuerart</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; das 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Tax-free purchase</strong></td>
<td>Summe <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li>Der Import ist Einkauf (is)<strong>Steuerart</strong>  <strong>Steuerfreier Einkauf</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; das 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax receivable</strong></td>
<td>Summe <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li>Der Kauf ist inländisch (ist)<strong>Steuerart</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; das 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable purchase credit note</strong></td>
<td>Summe <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li>Der Kauf ist inländisch (ist)<strong>Steuerart</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; das 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Tax exempt purchase credit note</strong></td>
<td>Summe <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li>Der Import ist Einkauf (is)<strong>Steuerart</strong>  <strong>Steuerfreier Einkauf</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; das 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on purchase credit note</strong></td>
<td>Summe <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li>Der Kauf ist inländisch (ist)<strong>Steuerart</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; das 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import</strong></td>
<td>Summe <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li><strong>Steuerart</strong> ist <strong>Verbrauchssteuer (USA)</strong></li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; das 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import</strong></td>
<td>Stornierte Summe <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li><strong>Steuerart</strong> ist <strong>Verbrauchssteuer (USA)</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; das 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import credit note</strong></td>
<td>Summe <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
e<li><strong>Steuerart</strong> ist <strong>Verbrauchssteuer (USA)</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; das 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import credit note</strong></td>
<td>Stornierte Summe <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li>Ist Steuerart. <strong>Verbrauchssteuer (USA)</strong></li>
d<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; das 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Use tax</strong></td>
<td>Summe <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li><strong>Steuerart</strong> ist <strong>Verbrauchssteuer (USA)</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; das 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset use tax</strong></td>
<td>Stornierte Summe <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Buchungsdatum ist in der ausgewählten Periode.</li>
<li><strong>Steuerart</strong> ist <strong>Verbrauchssteuer (USA)</strong>.</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; das 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Für die Tabelle), wird angenommen, dass die folgenden Kriterien erfüllt sein: 
> -   Der Steuergrundbetrag ist ein vom ** Ursprung Buchungsbetrag in der Buchhaltungswährung ** Feld.
> -   Der Steuerbetrag ist ein vom Übergangsbetrag ** tatsächlicher Mehrwertsteuerbetrag in der Buchhaltungswährung ** Feld.

### <a name="configure-the-er-model-and-format-for-the-report"></a>Konfigurieren Sie das ER-Modell und -Format für den Bericht

Sie können meldendes elektronisches (ER) verwenden, um Auszüge und Bericht konfiguriert, und verschiedene Formate elektronische der Daten exportiert, ohne X++-Code zu ändern. Weitere Informationen:

-   [Überblick über die elektronische Berichterstellung](/dynamics365/operations/dev-itpro/dev-itpro/analytics/general-electronic-reporting)
-   [Laden Sie die elektronische Berichtskonfigurationen der Lifecycle Services herunter](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
-   [Lokalisierungsanforderungen - Erstellen Sie eine GER-Konfiguration]( /dynamics365/operations/dev-itpro/analytics/electronic-reporting-configuration)

## <a name="countryspecific-resources-for-vat-statements"></a>Countryspecific Ressourcen für Mehrwertsteuer. -Auszüge
Der Mehrwertsteuertyp. im für jedes Land muss den Bedingungen der Gesetzgeber des Lands erfüllen. Es gibt vordefinierten allgemeine Modelle und Formate der der MwSt. -Auszügen für die Länder, die in der weiter unten dargestellten Tabelle.


| Land        | Weitere Informationen                                                          |
|----------------|---------------------------------------------------------------------------------|
| Österreich        |  [MwSt.-Auszugsdetails für Österreich] (emea-aut-vat-statement-details.md)         |
| Belgien        |                                                                                 |
| Tschechische Republik |  [MwSt.-Auszugsdetails für Tschechische Republik] (emea-cze-vat-statement-details.md)   |
| Estland        |  [MwSt.-Auszugsdetails für Estland] (emea-est-vat-statement-details.md) |
| Finnland        |                                                                                 |
| Deutschland        |                                                                                 |
| Italien          | [MwSt. -Auszugsdetails für Italien (emea-ita-vat-statements-details.md )]            |
| Lettland         | [MwSt.-Auszugsdetails für Lettland] (emea-lva-vat-statement-details.md)           |
| Litauen      | [MwSt.-Auszugsdetails für Litauen] (emea-ltu-vat-statement-details.md)         |
| Niederlande    |                                                                                 |
| Schweden         |                                                                                 |




