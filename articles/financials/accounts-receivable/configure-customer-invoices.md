---
title: Erstellen einer Debitorenrechnung
description: Bei einer **Debitorenrechnung für einen Auftrag** handelt es sich um eine Rechnung, die sich auf einen Auftrag bezieht, und die ein Debitor von einer Organisation erhält.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa49b70b07ac3dc6cbc5989b11981098f22be89c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835213"
---
# <a name="create-a-customer-invoice"></a>Erstellen einer Debitorenrechnung

[!include [banner](../includes/banner.md)]

Bei einer **Debitorenrechnung für einen Auftrag** handelt es sich um eine Rechnung, die sich auf einen Auftrag bezieht, und die ein Debitor von einer Organisation erhält. Diese Art von Debitorenrechnung wird auf Basis eines Auftrags, der die einzelnen Auftragspositionen und Artikelnummern enthält, erstellt. Die Artikelnummern werden im Sachkonto angegeben und gebucht. Journaleinträge in untergeordnetem Sachkonto sind bei einer Debitorenrechnung für einen Auftrag nicht verfügbar. Weitere Informationen finden Sie unter [Auftragserechnung erstellen](tasks/create-sales-order-invoices.md).

**Freitextrechnungen** sind nicht mit einem Auftrag verknüpft. Sie enthalten Auftragspositionen mit Sachkonten, Freitextbeschreibungen und benutzerdefinierten Verkaufsbeträgen. Bei dieser Art von Rechnung kann keine Artikelnummer eingegeben werden. Geben Sie die geeigneten Mehrwertsteuerinformationen ein. Für jede Rechnungsposition wird ein Hauptkonto für den Verkauf angegeben, das auf mehrere Sachkonten verteilt werden kann, indem Sie auf **Beträge verteilen** auf der Seite **Freitextrechnung** klicken. Der Debitorensaldo wird außerdem auf das Summenkonto aus dem Buchungsprofil gebucht, das für die Freitextrechnung verwendet wird.

Weitere Informationen finden Sie unter ''.

[Freitextrechnung erstellen](../accounts-receivable/create-free-text-invoice-new.md)

[Erstellt eine Vorlage für Freitextrechnungen.](../accounts-receivable/create-free-text-invoice-template-new.md)

[Einem Debitor eine Freitext-Rechnungsvorlage zuweisen](tasks/assign-free-text-invoice-template-customer.md)

[Freitext-Serienrechnungen generieren und buchen](tasks/post-recurring-free-text-invoices.md)


Bei einer **Proforma-Rechnung** handelt es sich um eine Rechnung, die vor dem Buchen der Rechnung als Vorkalkulation der tatsächlichen Rechnungsbeträge vorbereitet wird. Proforma-Rechnungen können sowohl für eine Debitorenrechnung für einen Auftrag als auch für Freitextrechnungen gedruckt werden.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Buchen und Drucken einzelner Debitorenrechnungen anhand von Aufträgen
Erstellen Sie mit diesem Prozess eine Rechnung, die auf einem Auftrag basiert. Das kann z. B. der Fall sein, wenn Sie dem Kunden vor Lieferung der Waren oder Dienstleistungen eine Rechnung senden möchten. 

Durch Buchen der Rechnung wird die Menge für den **Rechnungsrestbetrag** mit der Summe der fakturierten Mengen aus dem ausgewählten Auftrag aktualisiert. Wenn sowohl die Menge für den **Rechnungsrestbetrag** als auch die Menge **Rest liefern** für alle Artikel des Auftrags gleich Null ist, wird der Status des Auftrags zu **In Rechnung gestellt** geändert. Ist die **Rechnungsrestbetrag** nicht 0 (Null), bleibt der Status der Bestellung unverändert, und es können weitere Rechnungen für den Auftrag erstellt werden.

Auf der Listenseite **Alle Aufträge** können Sie den Status des Auftrags anzeigen. Zeigen Sie die gebuchten Rechnungen auf der Listenseite **Offene Debitorenrechnungen** an.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Buchen und Drucken einzelner Debitorenrechnungen anhand von Lieferscheinen und dem Datum
Verwenden Sie diesen Prozess, wenn für den Auftrag ein oder mehr als ein Lieferschein gebucht wurde. Die Debitorenrechnung basiert auf diesen Lieferscheinen und enthält die auf den Lieferscheinen angegebenen Mengen. Die Finanzinformationen für die Rechnung basieren auf den beim Buchen der Rechnung eingegebenen Informationen. 

Sie können basierend auf den bisher versendeten Artikeln der Lieferscheinpositionen eine Debitorenrechnung erstellen, auch wenn noch nicht alle Artikel eines bestimmten Auftrags versendet wurden. Das kann der Fall sein, wenn Ihre juristische Person monatlich eine Rechnung pro Debitor für alle Lieferungen ausstellt, die während des Monats versendet wurden. Jeder Lieferschein stellt eine teilweise oder vollständig abgeschlossene Artikellieferung für einen Auftrag dar. 

Durch Buchen der Rechnung wird die Menge des **Rechnungsrestbetrags** für jeden Artikel mit der Summe der gelieferten Mengen aus den ausgewählten Lieferscheinen aktualisiert. Wenn sowohl die Menge für den **Rechnungsrestbetrag** als auch die Menge **Rest liefern** für alle Artikel des Aufrags gleich 0 (Null) ist, wird der Status des Auftrags zu **In Rechnung gestellt** geändert. Ist die **Rechnungsrestbetrag** nicht 0 (Null), bleibt der Status der Bestellung unverändert, und es können weitere Rechnungen für den Auftrag erstellt werden. 

Die Lagerbuchungen werden mit der Rechnungsnummer aktualisiert, und der Status im Feld **Positionsstatus** des Auftrags wird zu **In Rechnung gestellt** geändert. 

Auf der Listenseite **Alle Aufträge** können Sie den Status des Auftrags anzeigen.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Konsolidieren von Aufträgen oder Lieferscheinen für das Buchen
Verwenden Sie diesen Prozess, wenn eine oder mehrere Aufträge fakturierungsbereit sind, und Sie möchten sie in einer einzelnen Rechnung konsolidieren. 

Sie können mehrere Rechnungen auf der Listenseite **Auftrag** auswählen und dann **Generieren von Rechnungen** verwenden, um sie zu konsolidieren. Auf der Seite **Rechnung buchen** können Sie die **Einstellungen Sammelaufträge** ändern, um nach Auftragsnummern (wenn es mehrere Lieferscheine für einen einzelnen Auftrag gibt) oder nach Rechnungskonto (wenn es mehrere Aufträge für ein einzelnes Rechnungskonto gibt) zusammenzufassen. Verwenden Sie die Anordnen Schaltfläche, um Aufträge als einzelne Rechnungen, basierend auf den Einstellungen für Sammelaufträge zu konsolidieren. Nutzen Sie die **Ordnet an** Schaltfläche, um Aufträge in einzelne Rechnungen, die auf Grundlage der Einstellungen **Zusammenfassender Auftrag** basieren.

## <a name="additional-settings-that-change-the-posting-behavior"></a>Zusätzliche Einstellungen, die das Buchungsverhalten ändern
Die folgenden Felder ändern das Verhalten des Buchungsprozesses.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Feld</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Menge</td>
<td>Wählen Sie die Mengen aus, auf denen die Buchung des Dokuments basieren soll. Die verfügbaren Optionen varieren, abhängig von Dokumenttyp, den Sie buchen, z. B. Lieferschein oder Rechnung.
<ul>
<li><strong>Jetzt liefern</strong> - Hiermit werden alle Mengen ausgewählt, die im Feld <strong>Jetzt liefern</strong> eingegeben wurden. Verwenden Sie diese Option, um einen Teilauftrag zu bestätigen oder zu liefern.</li>
<li><strong>Entnommen</strong> – Wählt alle Mengen aus, die entnommen wurden.</li>
<li><strong>Alle</strong> – Wählt alle Mengen im Auftrag aus, die noch nicht durch den aktuellen Dokumenttyp aktualisiert wurden.</li>
<li><strong>Lieferschein</strong>– Hiermit werden alle Mengen ausgewählt, die durch einen Lieferschein aktualisiert wurden.</li>
<li><strong>Entnommene Menge und nicht gelagerte Produkte</strong> – Wählen Sie alle Mengen aus, die entnommen wurden, und alle Produktmengen, die nicht gelagert werden.</li>
</ul></td>
</tr>
<tr class="even">
<td>Buchung</td>
<td><ul>
<li>Wählen Sie diese Option, um den Auftrag journalisieren.</li>
<li>Deaktivieren Sie diese Option, um einen Proformaauftrag zu drucken. <strong>Hinweis:</strong> Falls Sie eine Vereinbarung über einen Zahlungszeitplan getroffen haben, wird dieser auf dem Proforma-Auftrag nicht angezeigt. Der Zahlungsplan wird nur auf dem tatsächlichen Auftrag angezeigt.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Späte Auswahl</td>
<td>Aktivieren Sie diese Option, um die ausgewählte Abfrage später anzuwenden. Diese Option wird für Stapelverarbeitungsaufträge genutzt. Die Anfrage läuft, wenn der Batchauftrag ausgeführt wrid.</td>
</tr>
<tr class="even">
<td>Menge verringern</td>
<td>Wählen Sie diese Option aus, um die gelieferte Menge automatisch zu reduzieren, wenn das Dokument gebucht wird, sodass die gelieferte Menge dem verfügbaren Bestand entspricht.</td>
</tr>
<tr class="odd">
<td>Drucken</td>
<td>Wählen Sie aus, wann Dokumente gedruckt werden sollen:
<ul>
<li><strong>Aktuell</strong> – Dokumente drucken, nachdem eine Rechnung aktualisiert wurde.</li>
<li><strong>Später</strong> – Dokumente drucken, nachdem alle Rechnungen aktualisiert wurden.</li>
</ul>
<strong>Hinweis:</strong> Das Feld <strong>Drucken</strong> ist nur verfügbar, wenn Sie die Option <strong>Rechnung drucken</strong>, <strong>Angebot drucken</strong>, <strong>Kommissionierliste drucken</strong> oder <strong>Lieferschein drucken</strong> aktivieren. Sie haben beispielsweise das System so eingerichtet, dass Daten im Formular <strong>Formularsortierung</strong> nach Rechnungskonto sortiert werden. Sie können dann <strong>Später</strong> auswählen, um die Dokumente in einer Charge zu drucken, die nach Rechnungskonto sortiert wird. Andernfalls werden die Dokumente gedruckt, bevor die Verarbeitung abgeschlossen ist, und die Dokumente werden nicht in der Reihenfolge sortiert, die auf der Seite <strong>Formularsortierung</strong> angegeben ist.</td>
</tr>
<tr class="even">
<td>Rechnung drucken</td>
<td>Aktivieren Sie diese Option, um die Rechnung zu drucken. Wenn diese Option deaktiviert ist, können Sie eine Rechnung buchen, ohne sie zu drucken.</td>
</tr>
<tr class="odd">
<td>E-Mail senden</td>
<td>Aktivieren Sie diese Option, um die Rechnung für einen Auftrag nach dem Buchen der Rechnung als E-Mail-Anhäng an einen Debitor zu senden. Anlagen werden als PDF- und XML-Dateien übermittelt. Diese Option ist nur verfügbar, wenn Sie die Option <strong>CFD (elektronische Rechnungen) aktivieren</strong> auf der Seite <strong>Parameter für elektronische Rechnungen</strong> auswählen. <strong>Hinweis:</strong> (MEX) Dieses Steuerelement ist nur für juristische Personen verfügbar, deren primäre Adresse sich in Mexiko befindet.</td>
</tr>
<tr class="even">
<td>Druckverwaltungsziel verwenden</td>
<td>Wählen Sie diese Option aus, um die Druckeinstellungen zu verwenden, die für die Transaktion, das Dokument oder das Modul auf der Seite <strong>Druckverwaltungseinstellungen</strong> angegeben werden.</td>
</tr>
<tr class="odd">
<td>Kreditlimit prüfen</td>
<td>Hier legen Sie die Daten fest, die bei einer Kreditlimitprüfung analysiert werden sollen.
<ul>
<li><strong>Kein</strong> – Es gelten keine Anforderungen für die Kreditlimitprüfung.</li>
<li><strong>Saldo</strong> – Der Debitorensaldo wird durch Vergleich mit dem Kreditlimit überprüft.</li>
<li><strong>Saldo + Lieferschein oder Produktzugang</strong> – Das Kreditlimit wird durch Vergleich mit Debitorensaldo und Lieferungen überprüft.</li>
<li><strong>Saldo+Alles</strong> – Das Kreditlimit wird durch Vergleich mit Debitorensaldo, Lieferungen und offenen Aufträgen überprüft.</li>
</ul></td>
</tr>
<tr class="even">
<td>Habenkorrektur</td>
<td>Wählen Sie diese Option, um eine Gutschrift in den Belegbuchungen als Verrechnung anzuzeigen.</td>
</tr>
<tr class="odd">
<td>Haben-Restmenge</td>
<td>Wenn Sie eine Gutschrift buchen, aktivieren Sie diese Option, damit die Restmenge im Auftrag bleibt. Wenn dieses Kontrollkästchen deaktiviert ist, wird die Restmenge auf 0 (Null) festgelegt.</td>
</tr>
<tr class="even">
<td>Sammelaktualisierung für</td>
<td>Wählen Sie aus, wie mehrere Aufträge zusammengefasst werden sollen.
<ul>
<li><strong>Kein</strong> – Aufträge werden nicht summiert. Für jeden Auftrag wird z. B. eine separate Rechnung erstellt.</li>
<li><strong>Rechnungskonto</strong> – Fassen Sie alle ausgewählten Aufträge, basierend auf der im Formular <strong>Sammelaktualisierungsparameter</strong> festgelegten Kriterien, zusammen.</li>
<li><strong>Auftrag</strong> – Ein ausgewählter Bereich von Aufträgen wird in einem angegebenen Auftrag summiert. Die Aufträge werden entsprechend der im Formular <strong>Sammelaktualisierungsparameter</strong> festgelegten Kriterien zusammengefasst. Wenn Sie diese Option auswählen, muss auch ein Wert im Feld <strong>Auftrag</strong> ausgewählt werden.</li>
<li><strong>Automatische Zusammenfassung</strong> – Wenn Sammelaktualisierungen auf der Seite <strong>Sammelaktualisierung</strong> angegeben wurden, können Sie alle ausgewählten Aufträge, basierend auf den Kriterien der Seite <strong>Sammelaktualisierungsparameter</strong>, zusammenfassen. Wenn Sammelaktualisierungen nicht angegeben wurden, wird der Auftrag separat gebucht.</li>
<li><strong>Lieferschein</strong> – Ein ausgewählter Bereich von Aufträgen wird in einer Rechnung pro Lieferschein zusammengefasst. Diese Option steht nur zur Verfügung, wenn <strong>Lieferschein</strong> im Feld <strong>Menge</strong> ausgewählt wurde.</li>
</ul></td>
</tr>
</tbody>
</table>





