---
title: Rechnungsabgangsfrist
description: "In diesem Artikel wird erläutert, wie Parameter eingerichtet werden, um die Fälligkeitsdaten für die Erstellung von Debitorenrechnungen und Kreditorenrechnungen in der Europäischen Union zu berechnen."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters, LedgerInvoiceIssueDueDateSetup_W
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10923
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Iceland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 34dac634e09a8daa8a22b9f1efbc18ca44444e21
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="invoice-issue-deadline"></a>Rechnungsabgangsfrist

[!include[banner](../includes/banner.md)]


In diesem Artikel wird erläutert, wie Parameter eingerichtet werden, um die Fälligkeitsdaten für die Erstellung von Debitorenrechnungen und Kreditorenrechnungen in der Europäischen Union zu berechnen.

Die Direktive 45/2010 der Europäischen Union (EU) und andere Richtlinien erfordern, dass Lieferungen innerhalb der EU (innergemeinschaftliche Lieferungen) am oder vor dem fünfzehnten Tag des Monats im Anschluss an die erfolgte Lieferung fakturiert werden müssen. Gleichzeitig kann jedes EU-Land verschiedene Rechnungsstellungsfristen für inländische Lieferungen aufweisen. Über das Fälligkeitsdatum für die Ausstellung von Rechnungen können Sie das Datumsintervall an die Länder-/Regionsart anpassen. Dann wird das Fälligkeitsdatum für die Ausstellung von Rechnungen für alle Lieferungen in Länder/Regionen eines bestimmten Typs oder aus diesen Ländern/Regionen unter Verwendung von Regeln berechnet, die für das angegebene Datumsintervall festgelegt wurden. Darüber hinaus können Sie alle Lieferscheine abrufen, die ein bestimmtes Fälligkeitsdatum für die Ausstellung von Rechnungen enthalten, nach dem Fälligkeitsdatum für die Ausstellung von Rechnungen während der periodischen Vertriebsrechnungsstellung filtern und das Fälligkeitsdatum für die Ausstellung von Rechnungen bei der Rechnungsbuchung steuern. Sie können einen Datumsintervallcode und dann eine Berechnungsregel für das Rechnungsausgabedatum einrichten, indem Sie den Datumsintervallcode einem Länder-/Regionstyp zuweisen. Die Berechnungsregel wird verwendet, um das Fälligkeitsdatum für die Erstellung von Rechnungen für die folgenden Transaktionen zu berechnen:

-   Lieferungen innerhalb der EU
-   Inlandsversände innerhalb eines EU-Mitgliedsstaats

Sie können auch Datumskontrollen einrichten, um sicherzustellen, dass Debitorenrechnungen und Gutschriften für Debitorentransaktionen innerhalb des angegebenen Zeitraums generiert werden, nachdem die Lieferung erfolgt ist.

## <a name="prerequisites"></a>Erforderliche Komponenten
In der folgenden Tabelle werden die Voraussetzungen angezeigt, die erfüllt sein müssen, bevor Sie die Funktion für das Fälligkeitsdatum für die Ausstellung von Rechnungen verwenden können.

| Kategorie            | Voraussetzung                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Land/Region      | Die primäre Adresse der juristischen Person muss in einem EU-Mitgliedsstaat sein.                                                                                                                                                                                                                                                                                                                    |
| Zugehörige Einrichtungsaufgaben | Richten Sie auf der Seite **Datumsintervalle** ein Datumsintervall ein, das verwendet wird, um das Fälligkeitsdatum der Rechnungsausstellung zu berechnen. (Klicken Sie auf **Hauptbuch** &gt; **Sachkonto-Einstellungen** &gt; **Datumsintervalle**.) Auf der Seite **Außenhandeleigenschaften** setzen Sie die Außenhandelsparameter für verschiedene Länder/Regionen fest. (Klicken Sie  **Steuer** &gt; **Einrichten** &gt; **Außenhandel** &gt; **Außenhandelsparameter**.) |

## <a name="invoice-issue-due-date-calculation-rule"></a>Berechnungsregel für Fälligkeitsdaten für die Ausstellung von Rechnungen
Verwenden Sie die Seite **Berechnung für Fälligkeitsdatum der Rechnungsausstellung einrichten**, um eine Berechnungsregel für Fälligkeitsdaten für die Ausstellung von Rechnungen einzurichten, indem Sie einem Länder-/Regionstyp einen Datumsintervallcode zuweisen.

## <a name="date-control-parameters-for-customer-invoices-and-credit-notes"></a>Datumskontrollenparameter für Debitorenrechnungen und Gutschriften
Sie können auch Datumskontrollenparameter einrichten, um sicherzustellen, dass Debitorenrechnungen und Gutschriften für Debitorentransaktionen innerhalb des angegebenen Zeitraums generiert werden, nachdem die Lieferung erfolgt ist. Sie finden diese Parameter im Bereich **Rechnungsdatenkontrolle** auf der Seite **Debitorenkontenparameter**.

## <a name="example"></a>Beispiel
Um Microsoft Dynamics 365 for Finance and Operations einzurichten, um die Fälligkeitsdaten für die Ausstellung von Rechnungen für Lieferungen innerhalb der EU am 15. Tag des Folgemonats, nachdem die Lieferung zugestellt wurde, zu berechnen, erstellen Sie einen Datumsintervallcode und eine Berechnungsregel, die die folgenden Einstellungen besitzen:

### <a name="date-interval-code"></a>Datumsintervallcode

| Feld                                                           | Wert                           |
|-----------------------------------------------------------------|---------------------------------|
| Datumsintervallcode                                              | 15-NM                           |
| Beschreibung                                                     | Fünfzehnter Tag des Folgemonats |
| Vor (in der Feldgruppe **Bis Datum**)                         | Monat                           |
| Anf./Ende (in der Feldgruppe **Bis Datum**)                      | Beenden                             |
| +/- (in der Feldgruppe **Bis Datum**)                            | 15                              |
| Tage, Monate, Jahre oder Perioden (in der Feldgruppe **Bis Datum**) | Tage                            |

### <a name="invoice-issue-due-date-calculation-rule"></a>Berechnungsregel für Fälligkeitsdaten für die Ausstellung von Rechnungen

| Feld               | Wert                                                     |
|---------------------|-----------------------------------------------------------|
| Länder-/Regionsart | **EU**                                                    |
| Startdatum          | Geben Sie das Datum ein, ab dem die aktuelle Einstellungsposition gültig ist. |
| Datumsintervallcode  | **15-NM**                                                 |

## <a name="next-steps"></a>Nächste Schritte
Nachdem Sie die Parameter eingerichtet haben, die zur Berechnung von Fälligkeitsdaten für die Ausstellung von Rechnungen verwendet werden, können Sie die folgenden Transaktionen erstellen und buchen, um die Fälligkeitsdaten für die Ausstellung von Rechnungen automatisch zu berechnen und zu aktualisieren:

-   **Aufträge** – Wenn Sie einen Auftrag erstellen und einen Lieferschein buchen, wird das Fälligkeitsdatum für die Ausstellung der Rechnung berechnet und auf dem Lieferschein aktualisiert. Das Fälligkeitsdatum wird anhand des Datumsintervalls berechnet, das dem Land/der Region zugewiesen ist, das in der Lieferadresse des Auftrags angegeben ist. Nachdem Sie den Lieferschein gebucht haben, können Sie das Fälligkeitsdatum der Rechnungsausstellung im Feld **Fälligkeitsdatum für Rechnungserstellung** auf der Seite **Lieferscheinerfassung** überprüfen. (Klicken Sie auf **Vertrieb und Marketing** &gt; **Auftrag** &gt; **Auftragsversand** &gt; **Lieferschein**.) Sie können alle Lieferscheine, die nicht fakturiert werden, und das Rechnungsausgabefälligkeitsdatum auf der Seite **Lieferscheine nicht fakturiert** anzeigen. (Klicken Sie auf **Vertrieb und Marketing** &gt; **Auftrag** &gt; **Versandgebühr** &gt; **Nicht in Rechnung gestellte Lieferscheine**.)
-   **Bestellungen** – Wenn Sie eine Bestellung erstellen und einen Produktzugang buchen, wird das Fälligkeitsdatum für die Ausstellung der Rechnung berechnet und auf dem Produktzugang aktualisiert. Das Fälligkeitsdatum wird anhand des Datumsintervalls berechnet, das dem Land bzw. der Region zugewiesen ist, das bzw. die in der primären Adresse des Kreditors angegeben ist. Nachdem Sie den Produktzugang gebucht haben, können Sie das Fälligkeitsdatum der Rechnungsausstellung im Feld **Fälligkeitsdatum für Rechnungserstellung** auf der Seite **Produktzugangserfassung** überprüfen. (Klicken Sie auf **Beschaffung** &gt; **Bestellungen** &gt; **Produkte Empfangen** &gt;  **Produktzugang**.) Sie können alle Produktzugänge, die nicht fakturiert werden, und ihr Rechnungsausgabefälligkeitsdatum, auf der Seite **Produktzugänge nicht fakturiert** anzeigen. (Klicken Sie auf **Beschaffung** &gt; **Bestellungen** &gt; **Empfangene Produkte** &gt; **Nicht fakturierte Produktzugänge**.)

## <a name="technical-information-for-system-administrators"></a>Technische Informationen für Systemadministratoren
Wenn Sie keinen Zugriff auf die Seiten für die Durchführung der in diesem Artikel beschriebenen Aufgaben haben, wenden Sie sich mit den Informationen aus der folgenden Tabelle an Ihren Systemadministrator.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorie</th>
<th>Voraussetzung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Konfigurationsschlüssel</td>
<td>Klicken Sie auf <strong>Systemverwaltung</strong> &gt; <strong>Einstellungen</strong> &gt; <strong>Lizenzierung</strong> &gt; <strong>Lizenzkonfiguration.</strong>. Klicken Sie auf den Konfigurationsschlüssel <strong>Hauptbuch</strong>.</td>
</tr>
<tr class="even">
<td>Sicherheitsrollen und Aufgaben</td>
<td>Zum Ausführen dieser Aufgabe müssen Sie Mitglied einer Sicherheitsrolle sein, die folgende Aufgaben umfasst:
<ul>
<li><strong>CustInvoiceInvoiceAndCashProcessEnable</strong> (Aktivieren von Rechnungs- und Barverkaufsprozessen)</li>
<li><strong>VendInvoiceInvoicePaymentProcessEnable</strong> (Aktivieren von Rechnungs- und Zahlungsprozessen)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sicherheitsrollen und -rechte</td>
<td>Zum Ausführen dieser Aufgabe müssen Sie Mitglied einer Sicherheitsrolle sein, die folgende Rechte umfasst:
<ul>
<li><strong>CustPackingSlipJournalView</strong> (Anzeigen von Verkaufslieferscheinen)</li>
<li><strong>VendPackingSlipJournalView</strong> (Anzeigen der Produktzugangserfassung aus der Bestellung)</li>
<li><strong>LedgerInvoiceIssueDueDateSetupMaintain_W</strong> (Berechnen von Fälligkeitsdaten für die Ausstellung von Rechnungen)</li>
</ul></td>
</tr>
</tbody>
</table>






