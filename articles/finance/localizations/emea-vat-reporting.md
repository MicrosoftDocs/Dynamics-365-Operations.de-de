---
title: MwSt-Berichterstattung für Europa
description: Dieser Artikel enthält allgemeine Informationen zum Einrichten und Generieren der MwSt.-Abrechnung für einige europäische Länder.
author: mrolecki
ms.date: 03/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 266844
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
ms.openlocfilehash: 54be8844fadf744cc5527001737ab470fcec46d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283415"
---
# <a name="vat-reporting-for-europe"></a>MwSt-Berichterstattung für Europa

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält allgemeine Informationen zum Einrichten und Generieren der MwSt.-Abrechnung für einige europäische Länder.

Dieser Artikel bietet einen allgemeinen Ansatz zum Einrichten und zum Generieren der Mehrwertsteuerabrechnung. Dieser Ansatz ist für Benutzer in juristischen Personen in den folgenden Ländern/Regionen üblich:

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

> [!IMPORTANT]
> Die in diesem Artikel beschriebenen Funktionen für Österreich, die Tschechische Republik, Deutschland, die Niederlande und Schweden sind veraltet. Weitere Informationen finden Sie unter [Entfernte und außer Betrieb genommene Funktionen](../get-started/removed-deprecated-features-finance.md).
> Verwenden Sie die Links in der folgenden Tabelle, um mehr über das neue Design der Mehrwertsteuererklärungen in den entsprechenden Ländern zu erfahren.
> 
>
> | Land        | Zusätzliche Informationen                                                          |
> |----------------|---------------------------------------------------------------------------------|
> | Österreich        | [Mehrwertsteuererklärung (Österreich)](emea-aut-vat-declaration-austria.md)       |                                                                           
> | Tschechische Republik | [Mehrwertsteuererklärung (Tschechische Republik](emea-cze-vat-declaration-tax-declaration-model.md) |
> | Dänemark        | [MwSt.-Erklärung (Dänemark)](emea-dnk-vat-declaration-denmark.md)         |
> | Frankreich         | [Mehrwertsteuererklärung (Frankreich)](emea-fra-vat-declaration-preview-france.md)       |
> | Deutschland        | [Umsatzsteuererklärung (Deutschland)](emea-deu-vat-declaration-germany.md)           |
> | Niederlande    | [MwSt.-Erklärung (Niederlande)](emea-nl-vat-declaration-netherlands.md)    |
> | Norwegen         | [MwSt.-Erklärung mit direkter Übermittlung an Altinn](emea-nor-vat-return.md) |
> | Spanien          | [Mehrwertsteuererklärung (Spanien)](emea-esp-vat-declaration-spain.md)              |
> | Schweden         | [Mehrwertsteuererklärung (Schweden)](emea-swe-vat-declaration-sweden.md)          |
> | Schweiz    | [Mehrwertsteuererklärung (Schweiz)](emea-che-vat-declaration-switzerland.md) |
> | Vereinigtes Königreich             | [Vorbereitung für die Integration mit MRD für die Mehrwertsteuer](emea-gbr-mtd-vat-integration.md) |

## <a name="vat-statement-overview"></a>MwSt.-Auszugs, Überblick
Der MwSt-Auszug basiert auf dem Steuerbuchungsbeträgen. Die Generierung eines MwSt. -Auszugs ist Teil des Mehrwertsteuerzahlungsprozesses, der durch die Bank- und Beitragsmehrwertsteuerfunktion implementiert ist. Mithilfe dieses Funkltion können Sie die für eine Periode fällige Mehrwertsteuer berechnen. Die Ausgleichsberechnung enthält die gebuchte Mehrwertsteuer für den ausgewählten Abrechnungszeitraum für die Steuerbuchungen im Formular . Der Prozess zum Berechnen von Daten für einen MwSt.-Auszug basiert auf der Beziehung zwischen Mehrwertsteuercodes und Mehrwertsteuer-Erklärungscodes, in denen Mehrwertsteuer-Erklärungscodes mit den MwSt.-Auszugsfelder übereinstimmen (oder die Markierungen in XML). Für jeden Mehrwertsteuercode sollen Mehrwertsteuer-Erklärungscodes für jede Buchungsart, zum Beispiel steuerpflichtige Verkäufe, steuerpflichtige Einkäufe, steuerpflichtiger Import eingerichtet werden. Diese Buchungsarten werden im Abschnitt „Mehrwertsteuercodes für MwSt-Berichterstattung“ weiter unten in diesem Artikel beschrieben.

Für jeden Mehrwertsteuer-Erklärungscode soll ein bestimmtes Berichtslayout bestimmt werden. Gleichzeitig werden Mehrwertsteuercodes auf eine bestimmte Mehrwertsteuerbehörde von Mehrwertsteuer-Ausgleichsperioden verknüpft. Für jede Mehrwertsteuer-Behörde sollte ein bestimmtes Berichtslayout bestimmt werden. Auf diese Weise können nur mit Mehrwertsteuer-Erklärungscodes demselben Berichtslayout, das für die Mehrwertsteuerbehörde in Mehrwertsteuer-Abrechnungszeiträume für den Mehrwertsteuercode errichtet wird, in der Berichtseinstellung des Mehrwertsteuercodes ausgewählt werden. Eine Mehrwertsteuerbuchung, die nach dem Buchen eines Auftrags oder eine Erfassung erstellt wurde, enthält einen Mehrwertsteuercode, eine Mehrwertsteuerquelle, Mehrwertsteuerart und Buchungsbeträge (Steuergrundbetrag und Steuerbetrag in der Buchhaltungswährung, in der Mehrwertsteuerwährung und in der Buchungswährung). Durch die Kombination aus Steuerbuchungsattributen, verfassen Buchungsbeträge Gesamtbeträge für die Mehrwertsteuer-Erklärungscodes, die für Mehrwertsteuercodes angegeben werden. Die folgende Abbildung zeigt diese Datenbeziehung.

![Diagramm.](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>MwST-Bericht, Einrichtung
Um einen MwSt-Bericht zu zu Erstellen, müssen Sie Folgendes erstellen:

### <a name="sales-tax-authorities-for-vat-reporting"></a>MwST-Behörde für MwST-Beichterstattung

Bevor Sie Mehrwertsteuer-Erklärungscodes einrichten können, müssen Sie das gewünschte Berichtslayout für die Mehrwertsteuerbehörde auswählen. Sie müssen auch das Feld **Berichtslayout** im Bereich **Allgemein** auf der Seite **Mehrwertsteuer-Behörden** auswählen. Dieses Layout wird verwendet, wenn Sie Mehrwertsteuer-Erklärungscodes einrichten.

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a>Mehrwertsteuer-Erklärungscodes

Mehrwertsteuer-Erklärungscodes werden im Feldcodes MwSt. oder markierter Namen im XML-Format eingegeben. Diese Codes werden verwendet, um Beträge für den Bericht zu aggregieren und vorzubereiten. Wenn Sie das elektronische Berichterstellungsformat des MwSt.-Auszugs konfigurieren, werden die Namen der Ergebnisbeträge verwendet. Sie können auf der Seite "Mehrwertsteuer-Erklärungscodes" **Mehrwertsteuer-Erklärungscodes** erstellen und verwalten. Sie müssen jedem Code ein Berichtslayout zuweisen. Nachdem Sie die Mehrwertsteuer-Erklärungscodes erstellt haben, können Sie auf dem Inforegister **Berichtseinstellungen** auf der Seite **Mehrwertsteuercode** auf sie verweisen. <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>Mehrwertsteuercodes für MwSt-Berichterstattung

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Grundbeträge und Steuerbeträge von Mehrwertsteuerbuchungen können auf Erklärungscodes im MwSt.-Bericht (XML-Markierungen oder Meldungsfelder) zusammengefasst werden. Sie können dieses einrichten, indem Sie Mehrwertsteuer-Erklärungscodes für verschiedene Buchungsarten für Mehrwertsteuercodes auf der Seite <strong>Mehrwertsteuercodes</strong> zuordnen. Die folgende Tabelle beschreibt die Buchungsarten im Bericht, der für Mehrwertsteuercodes eingerichtet ist. Die Berechnung umfasst Buchungen für alle Quellenarten außer Mehrwertsteuer.

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
<li>Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Steuerfreier Verkauf</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt im Ausland (<strong>Steuerart</strong> ist <strong>steuerfreier Umsatz</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Mehrwertsteuer</strong></td>
<td>Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Steuerpflichtige Verkaufsgutschrift</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Steuerbefreite Verkaufsgutschrift</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt im Ausland (<strong>Steuerart</strong> ist <strong>steuerfreier Umsatz</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Mehrwertsteuer auf Verkaufsgutschrift</strong></td>
<td>Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Steuerpflichtige Einkäufe</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Steuerfreier Einkauf</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Kauf erfolgt im Ausland (<strong>Steuerart</strong> ist <strong>steuerfreier Einkauf</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Vorsteuer</strong></td>
<td>Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Steuerpflichtige Einkaufsgutschrift</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Steuerbefreite Einkaufsgutschrift</strong></td>
<td>Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Kauf erfolgt im Ausland (<strong>Steuerart</strong> ist <strong>steuerfreier Einkauf</strong>).</li>
<li>Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Mehrwertsteuer auf Einkaufsgutschrift</strong></td>
<td>Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:
<ul>
<li>Das Fälligkeitsdatum für die ausgewählte Periode.</li>
<li>Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</li>
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
> -   Der Steuerbetrag ist ein Transaktionsbetrag aus dem Feld **Aktueller Mehrwertsteuerbetrag in der Buchungswährung**.

### <a name="configure-the-er-model-and-format-for-the-report"></a>Konfigurieren Sie das ER-Modell und -Format für den Bericht

Sie können Elektronische Berichterstattung (ER) verwenden, um Auszüge und Berichte zu konfigurieren und verschiedene elektronische Datenformate zu exportieren, ohne den X++-Code zu ändern. Zusätzliche Informationen:

-   [Überblick über die elektronische Berichterstellung](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)
-   [Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [Lokalisierungsanforderungen - Erstellen Sie eine GER-Konfiguration](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a>Länderspezifische Ressourcen für Mehrwertsteuer-Auszüge
Der Mehrwertsteuertyp für jedes Land muss den Bedingungen der Gesetzgeber des Lands erfüllen. Es gibt vordefinierte allgemeine Modelle und Formate der MwSt.-Auszüge für die Länder, die in der weiter unten dargestellten Tabelle aufgeführt sind.


| Land        | Weitere Informationen                                                          |
|----------------|---------------------------------------------------------------------------------|
| Österreich        | [MwSt-Berichtdetails für Österreich](emea-aut-vat-statement-details.md)         |
| Belgien        |                                                                                 |
| Tschechische Republik | [MwSt.-Abrechnung für die Tschechische Republik](emea-cze-vat-statement-details.md)   |
| Estland        | [MwSt-Berichtadetails für Estland](emea-est-vat-statement-details.md) |
| Finnland        | [Mehrwertsteuererklärung für Finnland](emea-fin-sales-tax-payment-report-finland.md)          |
| Deutschland        | [Umsatzsteuererklärung für Deutschland](emea-de-vat-declaration.md)                       |
| Italien          | [MwSt-Abrechnungsdetails für Italien](emea-ita-vat-statements-details.md)            |
| Lettland         | [MwSt-Berichtdetail für Lettland](emea-lva-vat-statement-details.md)           |
| Litauen      | [MwSt-Berichtdetail für Litauen](emea-ltu-vat-statement-details.md)         |
| Niederlande    | [Mehrwertsteuererklärung für die Niederlande](emea-nl-vat-declaration.md)           |
| Schweden         | [Mehrwertsteuererklärung für Schweden](emea-swe-sales-tax-payment-report-sweden.md)          |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
