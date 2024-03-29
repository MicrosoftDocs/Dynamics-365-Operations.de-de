---
title: Erstellen einer Debitorenrechnung
description: Bei einer Debitorenrechnung für einen Auftrag handelt es sich um eine Rechnung, die sich auf einen Auftrag bezieht, und die ein Debitor von einer Organisation erhält.
author: ShivamPandey-msft
ms.date: 03/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0d1221e07f6dc4a5a99aa205c4a7f6fb367f000
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780506"
---
# <a name="create-a-customer-invoice"></a>Erstellen einer Debitorenrechnung

[!include [banner](../includes/banner.md)]

Bei einer **Debitorenrechnung für einen Auftrag** handelt es sich um eine Rechnung, die sich auf einen Auftrag bezieht, und die ein Debitor von einer Organisation erhält. Diese Art von Debitorenrechnung wird auf Basis eines Auftrags, der die einzelnen Auftragspositionen und Artikelnummern enthält, erstellt. Die Artikelnummern werden im Sachkonto angegeben und gebucht. Journaleinträge in untergeordnetem Sachkonto sind bei einer Debitorenrechnung für einen Auftrag nicht verfügbar. Weitere Informationen finden Sie unter [Auftragserechnung erstellen](tasks/create-sales-order-invoices.md).

Eine **Freitextrechnung** ist nicht mit einem Auftrag verknüpft. Sie enthalten Auftragspositionen mit Sachkonten, Freitextbeschreibungen und benutzerdefinierten Verkaufsbeträgen. Bei dieser Art von Rechnung kann keine Artikelnummer eingegeben werden. Geben Sie die geeigneten Mehrwertsteuerinformationen ein. Für jede Rechnungsposition wird ein Hauptkonto für den Verkauf angegeben, das auf mehrere Sachkonten verteilt werden kann, indem Sie auf **Beträge verteilen** auf der Seite **Freitextrechnung** klicken. Der Debitorensaldo wird außerdem auf das Summenkonto aus dem Buchungsprofil gebucht, das für die Freitextrechnung verwendet wird.

Weitere Informationen finden Sie hier:
 - [Freitextrechnungen erstellen](../accounts-receivable/create-free-text-invoice-new.md)
 - [Vorlage für Freitextrechnungen erstellen](../accounts-receivable/create-free-text-invoice-template-new.md)
 - [Einem Debitor eine Freitextrechnungsvorlage zuweisen](tasks/assign-free-text-invoice-template-customer.md)
 - [Freitextserienrechnungen generieren und buchen](tasks/post-recurring-free-text-invoices.md)


Bei einer **Proforma-Rechnung** handelt es sich um eine Rechnung, die vor dem Buchen der Rechnung als Vorkalkulation der tatsächlichen Rechnungsbeträge vorbereitet wird. **Proforma-Rechnungen** können sowohl für eine Debitorenrechnung für einen Auftrag als auch für eine Freitextrechnung gedruckt werden. 

>[!NOTE]
> Im Falle einer Systemunterbrechung während des Umsatz-Pro-forma-Rechnungsprozesses kann eine Pro-forma-Rechnung verwaist sein. Eine verwaiste Proforma-Rechnung kann durch Ausführen des periodischen Einzelvorgangs **Proforma-Rechnungen manuell löschen** gelöscht werden. Gehen Sie zu **Vertrieb und Marketing > Periodische Aufgaben > Bereinigen > Proforma-Rechnungen manuell löschen**.

## <a name="using-sales-order-customer-invoice-data-entities"></a>Verwendung von Entitäten für Verkaufsaufträge und Debitor-Rechnungen
Sie können Entitäten verwenden, um Informationen zu einer Verkaufsrechnung für einen Verkaufsauftrag zu importieren und zu exportieren. Es gibt verschiedene Entitäten für die Informationen auf dem Kopf der Verkaufsrechnung und den Zeilen der Verkaufsrechnung.

Die folgenden Entitäten stehen für die Informationen zum Kopf der Verkaufsrechnungen zur Verfügung:

- **Verkaufsrechnungen Journal Kopf** Entität (SalesInvoiceJournalHeaderEntity)
- **Verkaufsrechnungsköpfe V2** Entität (SalesInvoiceHeaderV2Entity)

Wir empfehlen Ihnen, die Entität **Erfassung von Verkaufsrechnungen** zu verwenden, da sie für den Import und Export von Verkaufsrechnungen eine höhere Leistung bietet. Diese Entität enthält nicht die Spalte **Umsatzsteuerbetrag** (INVOICEHEADERTAXAMOUNT), die den Wert der Mehrwertsteuer im Kopf der Verkaufsrechnung darstellt. Wenn Ihr Geschäftsszenario diese Informationen erfordert, verwenden Sie die Entität **Verkaufsrechnungskopfdaten V2**, um die Kopfdaten der Verkaufsrechnungen zu importieren und zu exportieren.

Die folgenden Entitäten sind für die Informationen zu Verkaufsrechnungszeilen verfügbar:

- **Kundenrechnungszeilen** - Entität (BusinessDocumentSalesInvoiceLineItemEntity)
- **Verkaufsrechnung Zeilen V3** Entität (SalesInvoiceLineV3Entity)

Wenn Sie festlegen, welche Entität für den Export verwendet werden soll, überlegen Sie, ob ein vollständiger Push oder ein inkrementeller Push verwendet werden soll. Beachten Sie außerdem die Zusammensetzung der Daten. Die Entität **Zeilen der Verkaufsrechnungen V3** unterstützt komplexere Szenarien (z.B. die Zuordnung zu den Bestandsfeldern). Es unterstützt auch Full-Push-Export-Szenarien. Für inkrementelle Pushs empfehlen wir Ihnen, die Entität **Kundenrechnungszeilen** zu verwenden. Diese Entität enthält eine viel einfachere Datenzusammensetzung als die Entität **Verkaufsrechnungen V3** und wird bevorzugt, insbesondere wenn die Integration von Bestandsfeldern nicht erforderlich ist. Aufgrund von Unterschieden in der Zuordnung zwischen den Zeilen-Entitäten ist die Entität **Kundenrechnung Zeilen** in der Regel schneller als die Entität **Verkaufsrechnungen Zeilen V3**.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Buchen und Drucken einzelner Debitorenrechnungen anhand von Aufträgen
Erstellen Sie mit diesem Prozess eine Rechnung, die auf einem Auftrag basiert. Das kann z. B. der Fall sein, wenn Sie dem Kunden vor Lieferung der Waren oder Dienstleistungen eine Rechnung senden möchten. 

Durch Buchen der Rechnung wird die Menge für den **Rechnungsrestbetrag** mit der Summe der fakturierten Mengen aus dem ausgewählten Auftrag aktualisiert. Wenn sowohl die Menge für den **Rechnungsrestbetrag** als auch die Menge **Rest liefern** für alle Artikel des Auftrags gleich Null ist, wird der Status des Auftrags zu **In Rechnung gestellt** geändert. Ist die **Rechnungsrestbetrag** nicht 0 (Null), bleibt der Status der Bestellung unverändert, und es können weitere Rechnungen für den Auftrag erstellt werden.

Auf der Listenseite **Alle Aufträge** können Sie den Status des Auftrags anzeigen. Zeigen Sie die gebuchten Rechnungen auf der Listenseite **Offene Debitorenrechnungen** an.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Buchen und Drucken einzelner Debitorenrechnungen anhand von Lieferscheinen und dem Datum
Verwenden Sie diesen Prozess, wenn für den Auftrag ein oder mehr als ein Lieferschein gebucht wurde. Die Debitorenrechnung basiert auf diesen Lieferscheinen und enthält die auf den Lieferscheinen angegebenen Mengen. Die Finanzinformationen für die Rechnung basieren auf den beim Buchen der Rechnung eingegebenen Informationen. 

Sie können basierend auf den bisher versendeten Artikeln der Lieferscheinpositionen eine Debitorenrechnung erstellen, auch wenn nicht alle Artikel eines bestimmten Auftrags versendet wurden. Das kann der Fall sein, wenn Ihre juristische Person monatlich eine Rechnung pro Debitor für alle Lieferungen ausstellt, die während des Monats versendet wurden. Jeder Lieferschein stellt eine teilweise oder vollständig abgeschlossene Artikellieferung für einen Auftrag dar. 

Durch Buchen der Rechnung wird die Menge des **Rechnungsrestbetrags** für jeden Artikel mit der Summe der gelieferten Mengen aus den ausgewählten Lieferscheinen aktualisiert. Wenn sowohl die Menge für den **Rechnungsrestbetrag** als auch die Menge **Rest liefern** für alle Artikel des Aufrags gleich 0 (Null) ist, wird der Status des Auftrags zu **In Rechnung gestellt** geändert. Ist die **Rechnungsrestbetrag** nicht 0 (Null), bleibt der Status der Bestellung unverändert, und es können weitere Rechnungen für den Auftrag erstellt werden. 

Die Lagerbuchungen werden mit der Rechnungsnummer aktualisiert, und der Status im Feld **Positionsstatus** des Auftrags wird zu **In Rechnung gestellt** geändert. 

Sehen Sie sich den Status der Verkaufsaufträge auf der **Alle Verkaufsaufträge** Listenseite an.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Konsolidieren von Aufträgen oder Lieferscheinen für das Buchen
Verwenden Sie diesen Prozess, wenn eine oder mehrere Aufträge fakturierungsbereit sind, und Sie möchten sie in einer einzelnen Rechnung konsolidieren. 

Sie können mehrere Rechnungen auf der Listenseite **Auftrag** auswählen und dann **Generieren von Rechnungen** verwenden, um sie zu konsolidieren. Auf der Seite **Rechnung buchen** können Sie die **Einstellungen Sammelaufträge** ändern, um nach Auftragsnummern (wenn es mehrere Lieferscheine für einen einzelnen Auftrag gibt) oder nach Rechnungskonto (wenn es mehrere Aufträge für ein einzelnes Rechnungskonto gibt) zusammenzufassen. Verwenden Sie die Anordnen Schaltfläche, um Aufträge als einzelne Rechnungen, basierend auf den Einstellungen für Sammelaufträge zu konsolidieren. Nutzen Sie die **Ordnet an** Schaltfläche, um Aufträge in einzelne Rechnungen, die auf Grundlage der Einstellungen **Zusammenfassender Auftrag** basieren.

## <a name="split-sales-order-invoices-by-site-and-delivery-information"></a>Auftragsrechnungen nach Standort und Lieferinformationen aufteilen
Sie können die Aufteilung von Kundenrechnungen für Aufträge nach Standort oder nach Lieferadresse auf der Registerkarte **Sammelaktualisierung** der Seite **Debitorenkontenparameter** konfigurieren. 
 - Aktivieren Sie die Option **Aufteilung basierend auf Rechnungsstandort**, um beim Buchen eine Rechnung pro Standort zu erstellen. 
 - Aktivieren Sie die Option **Aufteilung basierend auf Lieferinformationen der Rechnung**, um beim Buchen eine Rechnung pro Auftragsposition-Lieferadresse zu erstellen. 

## <a name="post-to-revenue-account-for-sales-order-lines-that-have-no-price-and-no-cost"></a>Auf das Umsatzkonto für Auftragspositionen ohne Preise und ohne Kosten buchen
Sie haben die Möglichkeit, das **Umsatzerlös**-Konto im **Hauptbuch** für Auftragspositionen ohne Preis und Kosten zu aktualisieren. 

Um diese Informationen einzurichten oder anzuzeigen:
1. Gehen Sie zum Parameter **Auf das Umsatzkonto für Auftragsrechnungen mit Nullpreisen und Nullkosten buchen** auf der **Hauptbuch und Umsatzsteuer**-Registerkarte der **Debitorenparameter**-Seite. (**Debitoren > Einrichtung > Debitorenparameter**). 
2. Wählen Sie **Ja**, um das **Umsatzerlös**-Konto für Auftragsrechnungspositionen, die keinen Preis und keine Kosten haben, zu aktualisieren. 
 - Wenn diese Option ausgewählt ist, enthält der Beleg 0,00 Einträge für die Buchungstypen **Debitorensaldo** und **Umsatzerlös**. Ein Ertragskonto auf der **Bestandsbuchung** Parameterseite, auf der **Verkaufsauftrag** Registerkarte Kontodefinition definiert. 
 - Wenn diese Option nicht ausgewählt ist, werden Positionen, die keine Preis- oder Kosteninformationen enthalten, nicht an das **Einnahmen** Konto gebucht. Stattdessen enthält der Beleg einen Eintrag von 0,00 für den Buchungstyp **Debitorensaldo**.

## <a name="line-creation-sequence-number-information"></a>Informationen zur Sequenznummer der Zeilenerstellung
Wenn Sie Debitor-Rechnungszeilen buchen, haben Sie die Möglichkeit, Sequenznummern für die Erstellung der Zeilen zu erstellen. Die Sequenznummern für die Erstellung von Zeilen werden während des Buchungsvorgangs zugewiesen. Indem Sie eine nicht fortlaufende Nummerierung zulassen, können Sie die Leistung bei der Buchung von Debitor-Rechnungen verbessern. Die Sequenznummern für die Zeilenerstellung können von Drittanbieter-Integrationen verwendet werden, die eine sequenzielle Reihenfolge erwarten. Wenden Sie sich an Ihre IT-Abteilung, wenn es um Erweiterungen geht, die mit Sequenznummern für die Zeilenerstellung integriert werden können.

Um diese Informationen einzurichten oder anzuzeigen, legen Sie auf der Seite **Parameter für Debitoren** auf der Registerkarte **Aktualisierungen** die Option **Sequenzielle Zeilennummern beim Buchen von Debitor-Rechnungszeilen zuweisen** fest:

- Legen Sie die Option auf **Nein** fest, um eine nicht-sequenzielle Nummerierung für die Sequenznummern der Zeilenerstellung zu verwenden.
- Legen Sie die Option auf **Ja** fest, um eine fortlaufende Nummerierung zu verwenden. Sie müssen die Option auf **Ja** für juristische Entitäten festlegen, die eine Hauptadresse in Italien haben. Sie müssen sie auch auf **Ja** festlegen, wenn der **CustInvoiceTransRandLineCreationSeqNumFlight** Flug deaktiviert ist.

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
<li><strong>Kein</strong> – Es gelten keine Anforderungen für die Kreditlimitüberprüfung.</li>
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







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
