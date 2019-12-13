---
title: Kreditorenzusammenarbeit mit externen Kreditoren
description: In diesem Thema wird erklärt, wie Einkaufsvertreter mit externen Keditoren kooperieren können, um Informationen über Bestellungen und Lieferbestand auszutauschen.
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, VendVendorPortalInvoicePart
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 733ecc7cfb4fee325560f5a6fe11612bb8ba57ef
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815294"
---
# <a name="vendor-collaboration-with-external-vendors"></a>Kreditorenzusammenarbeit mit externen Kreditoren

[!include [banner](../includes/banner.md)]

Das **Kreditorenzusammenarbeit** Modul richtet sich an Kreditoren, die keine elektronische Datenaustausch-Integration (EDI) mit Microsoft Dynamics 365 Supply Chain Management haben. Es erlaubt es Kreditoren, mit Bestellungen, Rechnungen, Lieferbestandsinformationen und Angebotsanforderungen zu arbeiten, und es ermöglicht ihnen auch den Zugriff auf Teile ihrer Kreditorenmasterdaten. In diesem Thema wird erklärt, wie Sie mit externen Kreditoren zusammenarbeiten können, die die Kreditorenzusammenarbeitsschnittstelle verwenden, um mit Bestellungen, Angebotsanforderungen und Lieferbestand zu arbeiten. Außerdem wird erklärt, wie ein bestimmter Kreditor aktiviert wird, um Kreditorenzusammenarbeit zu verwenden, und wie die Anzeige der Informationen definiert wird, die alle Kreditoren sehen, wenn Sie auf eine Bestellung antworten.

Weitere Informationen dazu, was externe Kreditoren in der Kreditorenzusammenarbeitschnittstelle tun können, finden Sie unter [Kreditorenzusammenarbeit mit Debitoren](vendor-collaboration-work-customers-dynamics-365-operations.md)

> [!NOTE]
> Die Informationen zur Kreditorenzusammenarbeit in diesem Thema gelten nur für die aktuelle Version von Supply Chain Management. In Microsoft Dynamics AX 7.0 (Februar 2016) und Microsoft Dynamics AX-Anwendungsversion 7.0.1 (Mai 2016) arbeiten Sie mit Kreditoren zusammen, indem Sie das Modul **Kreditorenportal** verwenden. Informationen zum Modul **Kreditorenportal** finden Sie unter [Zusammenarbeiten mit Kreditoren mithilfe des Kreditorenportals](collaborate-vendors-vendor-portal.md).

Weitere Informationen dazu, wie Kreditoren die Kreditorenzusammenarbeit in Rechnungsstellungsprozessen verwenden können, finden Sie unter [Kreditorenzusammenarbeit-Rechnungsstellungsarbeitsbereich](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md) Informationen darüber, wie neue Nutzer der Kreditorezusammenarbeit bereitgestellt werden, finden Sie unter [Kreditorenzusammenarbeitbenutzer verwalten](manage-vendor-collaboration-users.md).

## <a name="defining-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Definieren der Informationen, die den Kreditoren angezeigt werden, wenn sie auf Bestellungen antworten

Wenn Kreditoren auf eine Bestellung antworten, die Sie ihnen übermitteln, finden sie eines von drei Nachrichtenfeldern, in dem sie bestätigen müssen, dass sie die Bestellung annehmen, ablehnen oder mit Änderungen annehmen möchten. Da die Informationen, die dem Kreditor an diesem Punkt angezeigt werden, möglicherweise spezifisch für Ihr Unternehmen sind, können Sie den Text festlegen, der in jeder einzelnen Bestätigungsnachricht angezeigt wird. Beispielsweise kann der Text den Kreditor über den nächsten Schritte im Prozess oder die Bedingungen informieren.

Um den Text zu definieren, der in der Bestellungsantwort angezeigt wird, befolgen Sie diese Schritte

1. Auf der Seite **Informationen für Kreditoren, die auf Bestellungen antworten** wählen Sie den Antworttyp aus, und klicken Sie dann auf **Bearbeiten**.
2. Im Feld **Informationensnachricht** geben Sie die Informationen ein, die Kreditoren im Nachrichtenfeld angezeigt werden soll.

Wenn Sie Nachrichten in mehr als einer Sprache hinzufügen müssen, erstellen Sie separate Meldungen, und geben Sie für jede von ihnen den entsprechenden Sprachcode an. Der Nachricht, die jedem Kreditor angezeigt wird, wird in der Sprache sein, die der Kreditor verwendet.

## <a name="setting-the-vendor-collaboration-options-for-a-specific-vendor"></a>Festlegen der Kreditorenzusammenarbeitsoptionen für einen bestimmten Kreditor

Ein Administrator konfiguriert die allgemeinen Einstellungen für Kreditorenzusammenarbeit, wie die Sicherheitsrollen, die für alle Kreditoren verfügbar sind, mit denen Sie zusammenarbeiten. Es gibt jedoch auch Einstellungen, die für jedes Kreditorenkonto anders sein können. Sie sollten diese Einstellungen konfigurieren.

- Kreditorenzusammenarbeit aktivieren.
- Geben Sie an, ob der Kreditor Preisinformationen sehen soll.

### <a name="enabling-vendor-collaboration"></a>Kreditorenzusammenarbeit aktivieren

Bevor Benutzerkonten für einen externen Lieferanten erstellt werden können, müssen Sie das Kreditorenkonto konfigurieren, sodass der Kreditor die Kreditorenzusammenarbeit nutzen kann. Legen Sie auf der Seite **Kreditoren** auf der Registerkarte **Allgemein** das Feld **Zusammenarbeitsaktivierung** fest. Die folgenden Optionen sind verfügbar:

- **Aktiv (Bestellung wird automatisch bestätigt)** – Bestellungen werden automatisch bestätigt, wenn der Kreditor diese akzeptiert ohne Änderungen.
- **Aktiv (Bestellung wird nicht automatisch bestätigt)** – Ihre Organisation muss Bestellungen manuell bestätigen, nachdem der Kreditor diese akzeptiert hat.

### <a name="specifying-whether-the-vendor-should-see-price-information"></a>Angeben, ob der Kreditor Preisinformationen sehen soll

Um Preisinformationen für Bestellungen über die Kreditorenzusammenarbeitschnittstelle freizugeben, müssen Sie die Option **Bestellungspreise bzw. -betrag** auf der Registerkarte **Standardwerte für Bestellungen** für das Kreditorenkonto auf **Ja** festlegen. Diese Preisinformationen umfassen den Preis je Einheit, Rabatte und Gebühren.

## <a name="working-with-pos-when-vendor-collaboration-is-used"></a>Arbeiten mit Bestellungen, wenn die Kreditorenzusammenarbeit verwendet wird

### <a name="sending-a-po-to-a-vendor"></a>Eine Bestellung an einen Kreditor senden

Bestellungen werden in Supply Chain Management werden vorbereitet. Wenn eine Bestellung den Status **Genehmigt** hat, senden Sie sie an den Kreditor, indem Sie **Zur Bestätigung senden** auf der Seite **Bestellung** auswählen. Der Status der Bestellung wird dann auf **In externer Prüfung** geändert. Nachdem die Bestellung versendet wurde, kann der Kreditor diese auf der Seite **Bestellungen zur Prüfung** in der Kreditorenzusammenarbeitschnittstelle finden. Der Kreditor kann dann die Bestellung akzeptieren, ablehnen oder Änderungen vorschlagen. Der Kreditor kann auch Kommentare hinzufügen, um Informationen wie Änderungen an der Bestellung mitzuteilen. Wenn Sie die Aufmerksamkeit des Kreditors auf eine neue Bestellung lenken möchten, können Sie die Bestellung auch per E-Mail senden, indem Sie das Druckverwaltungssystem verwenden.

### <a name="confirmation-and-acceptance-of-a-po-by-a-vendor"></a>Bestätigung und Akzeptieren einer Bestellung durch einen Kreditor

Nachdem ein Kreditor eine Bestellung annimmt, kann die Bestellung automatisch bestätigt werden, oder sie muss möglicherweise manuell bestätigt werden. Das Verhalten ist abhängig davon, ob das Feld **Zusammenarbeitsaktivierung** für den Kreditor auf **Aktiv (Bestellung wird automatisch bestätigt)** oder auf **Aktiv (Bestellung wird nicht automatisch bestätigt)** festgelegt ist.

Die folgende Tabelle zeigt den üblichen Informationsaustausch, abhängig von der Antwort des Kreditors, wenn Sie eine Bestellung zur Bestätigung senden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr>
<th>Kreditorenantwort</th>
<th>Ergebnis</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td>Der Kreditor <strong>akzeptiert</strong> den Auftrag, und Supply Chain Management wird so konfiguriert, dass Bestellungen, die der Kreditor akzeptiert, automatisch bestätigt werden.</td>
<td>Der Status einer Bestellstatus wird auf <strong>Bestätigt</strong> aktualisiert. Wenn der Auftrag aus einem bestimmten Grund nicht aktualisiert werden kann, wird die Antwort des Kreditors trotzdem als <strong>Akzeptiert</strong> erfasst, die Bestellung bleibt aber im Status <strong>In externer Prüfung</strong>. 

Die Bestellung, die an den Kreditor gesendet wurde und die den Status <strong>In externer Prüfung</strong> hat, wird mit bestätigtem Lieferdatum für die Positionen aktualisiert. Diese Aktualisierung initiiert eine neue Version, die automatisch auf den Status <strong>Bestätigt</strong> festgelegt wird. Wenn die Bestellung bestätigt wird, wird sie in der Zusammenarbeitschnittstelle des Kreditors angezeigt.</td>
</tr>
<tr class="odd">
<td>Der Kreditor <strong>akzeptiert</strong> den Auftrag, aber Supply Chain Management wird so konfiguriert, dass Bestellungen, die der Kreditor akzeptiert, automatisch bestätigt werden.</td>
<td>Die Antwort des Kreditors wird als <strong>Bestätigt</strong> erfasst, die Bestellung bleibt jedoch im Status <strong>Externe Prüfung</strong>.

Die Bestellung, die an den Kreditor gesendet wurde und die den Status <strong>In externer Prüfung</strong> hat, wird mit bestätigtem Lieferdatum für die Positionen aktualisiert. Diese Aktualisierung initiiert eine neue Version, die automatisch auf den Status <strong>In externer Überprüfung</strong> festgelegt wird. Sie können anschließend die Bestellung manuell bestätigen.</td>
</tr>
<tr class="even">
<td>Der Kreditor <strong>lehnt</strong> die Bestellung ab.</td>
<td>Die Antwort des Kreditors wird als <strong>Abgelehnt</strong> erfasst, die Bestellung bliebt jedoch im Status <strong>Externe Prüfung</strong>. Die Ablehnung wird zusammen mit dem Kreditoren-Hinweis empfangen</td>
</tr>
<tr class="odd">
<td>Der Kreditor <strong>akzeptiert</strong> den Auftrag <strong>mit Änderungen</strong>. Änderungen werden auf Positionsebene vorgeschlagen. Der Kreditor kann einzelne Positionen annehmen oder ablehnen. Hier sind einige andere Änderungen, die der Kreditor vorschlagen kann:
<ul>
<li>Ändern von Mengen oder Datumsangaben.</li>
<li>Teilen Sie Positionen für verschiedene Lieferdaten und Mengen auf.</li>
<li>Einen Artikel ersetzen.</li>
</ul>
Der Kreditor kann keine Preisinformationen und Gebühren ändern. Allerdings kann der Kreditor diese Änderungen vorschlagen, indem er Hinweise verwendet.</td>
<td>Die Antwort des Kreditors wir als <strong>Mit Änderungen akzeptiert</strong>, erfasst und der Status der Bestellung bleibt <strong>In externer Prüfung</strong> Die Statusangaben zeigen die Arten von Änderungen, die der Kreditor vorgeschlagen hat. Weitere Informationen zum automatischen Verbrauch der Änderungen lesen Sie im Abschnitt &quot;Die Bestellung aktualisieren, wenn ein Kreditor Änderungen vorschlägt&quot;, später in diesem Thema. </td>
</tr>
</tbody>
</table>

Mit dem Arbeitsbereich **Bestellungsvorbereitung** können Sie überwachen, auf welche Bestellungen der Kreditor geantwortet hat. Dieser Arbeitsbereich enthält zwei Listen mit Bestellungen, die den Status **In externer Prüfung** haben:

- Externe Prüfung erfordert Aktivität
- In externer Überprüfung Lieferantenantwort erwartet

### <a name="changing-a-po"></a>Ändern einer Bestellung

Um eine Bestellung zu ändern, auf die ein Kreditor bereits geantwortet hat, müssen Sie dem Kreditor eine neue Version der Bestellung senden. Die neue Bestellung weist einen Versionssuffix auf, der anzeigt, dass es sich um eine geänderte Version einer Bestellung handelt, die zuvor gesendet wurde. Die Seite **Bestellungskreditoren-Bestätigungsverlauf** ermöglicht es Ihnen und Ihren Lieferanten, den Verlauf jedes Auftrags zu verfolgen. Die zuvor bestätigte Version der Bestellung bleibt in der Liste bestätigter POs, bis die neue Bestellung bestätigt wurde.

### <a name="canceling-a-po"></a>Eine Bestellung stornieren

Wenn Sie eine Bestellung stornieren, wird der Status wieder zu **Genehmigt** geändert. Sie müssen die Bestellung zurück an den Kreditor senden, sodass der Kreditor die Stornierung bestätigen oder ablehnen kann. Nachdem die Stornierung bestätigt wurde, wird die Bestellung in der Liste bestätigter PO des Kreditors als **Storniert** angezeigt.

### <a name="adding-attachments-to-a-po"></a>Hinzufügen von Anhängen in eine Bestellung

Sie können Zuordnungen wie Dateien, Bilder und Hinweise für die Bestellung unter Verwendung des Dokumentverwaltungssystems hinzufügen. Die Anlagen des Typs **Extern** werden für den Kreditor angezeigt, wenn Sie die Bestellung an den Debitor senden.

## <a name="updating-a-po-when-a-vendor-suggests-changes"></a>Eine Bestellung aktualisieren, wenn ein Kreditor Änderungen vorschlägt

Wenn ein Kreditor auf eine Bestellung geantwortet hat und Änderungen vorgeschlagen hat, besteht der nächste Schritt darin, die Antwort zu verarbeiten.

Im Arbeitsbereich **Bestellungsvorbereitung** in der Liste **In externer Überprüfung ist Aktivität erforderlich** können Sie Bestellungen identifizieren, die ein Kreditor mit Änderungen akzeptiert hat. Von dieser Liste aus können Sie auch zur Antwort des Kreditors navigieren.

In einer Antwort kann ein Kreditor die folgenden Informationen im Kopf ändern:
 
- Zeilendokumentreferenz
- Lieferart
- Lieferbedingungen
- Bestätigtes Lieferdatum

Der Kreditor kann auch eine Notiz oder eine Anlage hinzufügen.

Bei den Positionen kann der Kreditor die Menge und das Lieferdatum ändern, Hinweise und Anhänge hinzufügen, eine Position zurückweisen, eine Position mit einem Produkt ersetzen, das als Text eingegeben wird und eine Position in mehrere Lieferungen teilen. Der Status einer Position variiert, abhängig von den Änderungen, die der Kreditor vorgeschlagen hat:
    
- **Mit Änderungen akzeptiert**
- **Abgelehnt**
- **Ersetzt** – In diesem Fall ist eine weitere Position hinzugefügt worden, die den Status **Ersatz** aufweist.
- **Bestätigt**
- **In Zeitplan aufgeteilt** – In diesem Fall werden zusätzliche Zeilen hinzugefügt, die den Status **Zeitplanpositionen** haben.

Wenn eine Position keine Änderungen hat, erhält sie den Positionsstatus **Angenommen**.

In der Antwort vermitteln Ihnen die Positionsstatusangaben die Arten von Änderungen, die der Kreditor gemacht hat. Darüber hinaus werden alle Felder, die geändert wurden, in Fettschrift angezeigt, damit Sie die Änderungen besser ermitteln können.

Sie können eine Bestellung aktualisieren, indem Sie **Bestellungsaktualisierung verarbeiten** in jeweils der Antwort oder in einer Position auf einmal auswählen. Ein Feld **Wurde die Bestellungsaktualisierung verarbeitet?** im Kopf und den Positionen gibt an, ob das System den Kopf oder die Positionen verarbeitet hat, um die Bestellung mit Änderungen zu aktualisieren, die aus der Antwort stammen. Sie können die Aktivität **Bestellungsaktualisierung verarbeiten** jeweils nur einmal pro Kopf oder Position durchführen.

Nicht alle diese Änderung können auf einer Bestellung aktualisiert werden. Nur Aktualisierungen für den Kopf und Aktualisierungen von Datumsangaben und Mengen zu Positionen können in der Bestellung automatisch aktualisiert werden. Für andere Änderungen muss die Bestellung manuell aktualisiert werden. In diesem Fall hat das Feld **Wurde Bestellungsaktualisierung verarbeitet?** den Wert **Manuelle Aktualisierung**. Wenn beispielsweise ein Kreditor vorschlägt, dass eine Position in einen Zeitplan aufgeteilt wird, muss diese Änderung manuell vorgenommen werden.

Jede Position, die den Status **Akzeptiert** besitzt, hat ein bestätigtes Lieferdatum. Wenn Sie die Aktivität **Bestellungsaktualisierung verarbeiten** ausführen, wird dieses Datum in der Bestellung aktualisiert. Hinweise und Anhänge werden nicht automatisch auf die aktuelle Bestellung übertragen. Darüber hinaus werden Handelsvereinbarungen in den Bestellpositionen nicht neu beurteilt, wenn Sie die aktuelle Bestellung über die Aktivität **Bestellungsaktualisierung verarbeiten** aktualisieren.

## <a name="po-statuses-and-versions"></a>PO-Status- und versionen

In diesem Abschnitt werden die verschiedenen Statuswerte, die eine Bestellung bis zum Zeitpunkt der Bestätigung haben kann, beschrieben. Es wird zudem beschrieben, wann neue Versionen einer Bestellung für den Kreditor verfügbar werden. Das Verhalten variiert, abhängig davon, ob Sie das Änderungsmanagement für PO verwenden. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versionen und Status, wenn Sie das Änderungsmanagement nicht verwenden

Die folgende Tabelle enthält ein Beispiel der Änderungen des Status und der Version, die eine Bestellung durchlaufen kann.

| Aktion | Status und Version |
|--------|--------------------|
| Die ursprüngliche Version der Bestellung wird in Supply Chain Management erstellt. | Der Status ist **Genehmigt**. |
| Die Bestellung wird an den Kreditor gesendet. | Eine Version wird in der Kreditorenportalschnittstelle erfasst und der Status wird in **Externe Prüfung** geändert. |
| Der Kreditor übermittelt eine Antwort **Angenommen mit Änderungen**. | Der Status ist weiterhin **In externer Prüfung**. |
| Sie nehmen einige Änderungen vor, die vom Kreditor gefordert wurden. | Der Status wird zurückgeändert in **Genehmigt**. |
| Sie senden die neue Version der Bestellung an den Kreditor. | Eine neue Version wird in der Kreditorenportalschnittstelle erfasst und der Status wird in **Externe Prüfung** geändert. |
| Der Kreditor genehmigt die neue Version der Bestellung. | Der Status ist weiterhin **In externer Prüfung,**, es sei denn, das Kreditorenkonto ist so konfiguriert, dass Bestellungen automatisch den Status **Bestätigt** erhalten, wenn der Keditor sie akzeptiert. |

Kreditoren müssen eine Bestellung in der Kreditorenzusammenarbeitsschnittstelle nicht bestätigen. Sie können auch eine E-Mail senden oder ihre Zustimmung zu einer Bestellung über andere Kanäle vermitteln. Sie können anschließend den Auftrag manuell bestätigen. In diesem Fall erhalten Sie eine Warnung, die aussagt, dass der Auftrag gerade bestätigt wird, obwohl keine Antwort vom Kreditor vorhanden ist. Die Bestellung wird dann in der Bestätigungshistorie als offener, bestätigter Auftrag ohne Antworten aufgeführt. Zu diesem Zeitpunkt hat der Kreditor nicht mehr die Möglichkeit, die Bestellung zu bestätigen oder abzulehnen.

> [!NOTE]
> Die Version der Bestellung, die anderen Prozessen in Supply Chain Management zur Verfügung steht, ist immer die neueste Version, auch wenn diese Version noch nicht in der Kreditorenzusammenarbeitsschnittstelle erfasst wurde.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versionen und Status, wenn Sie das Änderungsmanagement verwenden

Wenn Sie das Änderungsmanagement für Bestellungen aktiviert haben, durchlaufen die Bestellungen einen Genehmigungsworkflow bis zum Status **Genehmigt**. Dieser Prozess wird dem Kreditor nicht angezeigt.

Die folgende Tabelle enthält ein Beispiel der Änderungen des Status und der Version, die eine Bestellung durchlaufen kann, wenn das Änderungsmanagement aktiviert ist: Eine Version wird registriert, wenn die Bestellung genehmigt ist, nicht wenn die Bestellung an den Kreditor geschickt oder bestätigt wird.

| Vorgang | Status und Version |
|--------|--------------------|
| Die ursprüngliche Version der Bestellung wird in Supply Chain Management erstellt. | Der Kopfstatus ist **Entwurf**. |
| Die Bestellung wird zum Genehmigungsprozess übermittelt. (Der Genehmigungsprozess ist ein interner Prozess, an dem der Kreditor nicht beteiligt ist.) | Der Status wird von in **Entwurf** auf **Wird überprüft** und **Genehmigung** geändert, wenn die Bestellung nicht bei der Genehmigungsprozedur abgelehnt wird. Die genehmigte Bestellung wird als eine Version erfasst. | 
| Die Bestellung wird an den Kreditor gesendet. | Die Version wird in der Kreditorenportalschnittstelle erfasst und der Status wird in **Externe Prüfung** geändert. |
| Sie nehmen einige Änderungen vor, die der Kreditor verlangt hat, entweder manuell oder mithilfe der Aktivität **Bestellungsaktualisierung verarbeiten** auf der Antwort, um die Bestellung zu aktualisieren. | Der Status wird zurückgeändert in **Entwurf**. |
| Die Bestellung wird erneut zum Genehmigungsprozess übermittelt. | Der Status wird von in **Entwurf** auf **Wird überprüft** und **Genehmigung** geändert, wenn die Bestellung nicht bei der Genehmigungsprozedur abgelehnt wird. Alternativ kann das System so konfiguriert werden, dass bestimmte Feldänderungen keine erneute Genehmigung erfordern. In diesem Fall wird der Status zuerst in **Entwurf** geändert und wird dann automatisch auf **Genehmigt** aktualisiert. Die genehmigte Bestellung wird als eine neue Version erfasst. |
| Sie senden die neue Version der Bestellung an den Kreditor. | Die neue Version wird in der Kreditorenportalschnittstelle erfasst und der Status wird in **Externe Prüfung** geändert. |
| Der Kreditor genehmigt die neue Version der PO. | Der Status wird entweder automatisch in **Bestätigt** geändert oder wenn Sie die Antwort vom Kreditor erhalten und die Bestellung dann bestätigen. |

## <a name="sharing-information-about-consignment-inventory"></a>Informationen zum Lieferbestand teilen

Wenn Sie Lieferungsbestand verwenden, können Lieferanten, bzw. Kreditoren die Kreditorenzusammenarbeitschnittstelle verwenden, um Informationen auf den folgenden Seiten anzeigen:

- **Bestellungen, die Lieferungsbestand verbrauchen -** – Bestellungen für Lieferungsbestand werden erzeugt, wenn das Eigentum vom Bestand vom Lieferant an Ihr Unternehmen übergeht. Eine Produktquittung wird gleichzeitig gebucht. Diese Lieferungsbestellungen werden nur auf der Seite **Bestellungen, die Lieferungsbestand verbrauchen** angezeigt. Sie sind nicht auf der Seite **Alle bestätigen Bestellungen** im Modul **Kreditorenzusammenarbeit** enthalten.
- **Produkte erhalten vom Lieferungsbestand** – Auf dieser Seite sind alle Buchungen aufgelistet, bei denen der Besitz der Produkte vom Kreditor an Ihr Unternehmen übertragen wurde. Verkäufer können diese Informationen verwenden, für die Rechnungsstellung.
- **Verfügbarer Lieferungsbestand** – Diese Seite zeigt den verfügbaren, im Besitz des Kreditoren befindlichen Lieferungsbestand an, der an Ihrem Lagerort eingetroffen ist.

## <a name="working-with-rfqs-when-you-use-vendor-collaboration"></a>Arbeiten mit Angebotsanforderungen, wenn Sie die Kreditorenzusammenarbeit verwenden

Dieser Abschnitt beschreibt die Interaktionen zwischen Debitoren und Kreditoren während des Angebotsanforderungsprozesses. Es wird auch erklärt, wie Kreditoren Informationen mitgeteilt werden. Einen grundlegenden Überblick über die Unterstützung des Ausschreibungsprozesses finden Sie unter [Anfrage zu Angeboten (RFQs) Übersicht](request-quotations.md).

### <a name="alternates-attachments-amendments-and-returns"></a>Alternativen, Anhänge, Ergänzungen und Rückgaben

- **Alternativen** – Im Kopf einer Angebotsanforderungsanfrage können Sie angeben, dass Alternativen für nicht im Katalog enthaltene Artikelpositionen zulässig sind. Wenn Alternativen aktiviert sind, können Kreditoren eine alternative Position für jede angeforderte Position hinzufügen.
- **Anhänge** – Anhänge können sowohl auf der Kopfebene als auch auf Positionsebene einer Angebotsanforderungsanfrage hinzugefügt werden. Anhänge können als entweder intern oder extern klassifiziert sein. Interne Anhänge können nur auf der Debitorenseite angezeigt werden, wohingegen Kreditoren externe Anhänge anzeigen können, nachdem sie versendet werden.

    Kreditoren können auch Anhänge in ihrer Angebotsantwort hinzufügen. Diese Anhänge können auf der Debitorenseite angezeigt werden, nachdem ein Kreditor die Angebotsantwort übermittelt. Anhänge, die Kreditoren hinzufügen, werden immer als extern klassifiziert. Um auf einen Anhang zuzugreifen, den ein Kreditor zusammen mit einem Angebot übermittelt hat, wählen Sie **Angebotsanhänge** oder **Angebotspositionsanhänge** aus.
    
    Um Anhänge zu öffnen, die zusammen mit einer Angebotsanforderungsanfrage übermittelt wurden, verwenden Sie das Büroklammernsymbol für die Dokumentbehandlung in der Antwort.

- **Ergänzungen** – Wenn eine Ergänzung abgeschlossen ist, werden die vorhandenen Angebotsantworten entfernt, sodass sie durch aktualisierte Werte ersetzt werden können. Informationen wie der Positionspreis und -menge aus früheren Angebotsantworten können über die Erfassungen in der Angebotsanforderungsanfrage angezeigt werden.

    Um die Verarbeitung von Ergänzungen zu erzwingen, legen Sie auf der Seite **Beschaffungsparameter** im Inforegister **Angebotsanforderungen** die Option **Angebotsanforderungen sperren, wenn diese gesendet werden** auf **Ja** fest. (Diese Option wird für öffentlichen Sektor festgelegt und ist für diesen erforderlich.)

- **Rückgabe** – Wenn ein Kreditor ein Angebot gesendet hat, aber weitere oder geänderte Informationen für die Angebotsanforderungsanfrage erforderlich sind, kann der Kunde das Angebot an den Kreditor zurückgeben. Die Daten aus dem Angebot, die zuvor übermittelt wurden, werden vermerkt, und der Kreditor kann die erforderlichen Änderungen vornehmen, ohne den Angebotsprozess erneut zu starten.

## <a name="public-sector-extensions"></a>Erweiterungen für den öffentlichen Sektor

Für den öffentlichen Sektor ermöglicht die erweiterte Funktionalität, dass eine Angebotsanforderungsanfrage an Kreditoren gesendet und veröffentlicht wird. Wenn Sie eine Angebotsanforderung veröffentlichen, kann jeder, der die Informationen anfordert, die Arbeit anzeigen, die mit den meisten Bestimmungen des öffentlichen Sektors übereinstimmt. Alle verfügbare Arbeit wird auf der Listenseite **Offene veröffentlichte Angebotsanforderungen** angezeigt, und die stornierten, ausstehenden oder bewilligten Angebotsanforderungen können auf der Listenseite **Geschlossene veröffentlichtes Angebotsanforderungen** angezeigt werden. Diese Dokumente können auf einer Website außerhalb von Supply Chain Management durch Integrationen mit den folgenden Datenentitäten ebenfalls angezeigt werden:

- Veröffentlichte Angebotsanforderungen
- Eintrag veröffentlichter Angebotsanforderungen
- Kopfzeilenanlagen veröffentlichter Angebotsanforderungen

Diese Entitäten ermöglichen es Personen, die keine bereitgestellten Benutzer in Supply Chain Management sind, aber die anonymen Zugriff auf die externe Website haben, die verfügbare und geschlossene Arbeit anzuzeigen. Darüber hinaus ermöglicht es die erweiterte Funktionalität in **Übermitteln und veröffentlichen** dem Benutzer, der Parameter für den Angebotsanforderungsprozess festlegt, eine E-Mail-Vorlage zu definieren. Wenn der Prokurist dann die Angebotsanforderungsanfrage erstellt, muss er oder sie die E-Mail-Vorlage auswählen, um die erforderlichen Informationen an die Kreditoren zur Angebotsanforderungsanfrage zu senden. 

Der Benutzer, der Parameter für den Angebotsanforderungsprozess einrichtet, kann mehrere E-Mail-Vorlagen erstellen. Diese E-Mail-Vorlagen können sowohl statischen Text als auch die folgenden Ersetzungstoken enthalten. Die Token werden durch kontextabhängige Werte ersetzt, wenn eine E-Mail erstellt wird.

- %RFQCase%
- %RFQCaseName%
- %bidType%
- %inviteOnly%
- %expiryDateTime%
- %anfordernde Person%
- %requestingDepartment%
- %Kontonummer%
- %heutiges Datum%
- %Erstellungsdatum%

Wenn eine Ergänzung erforderlich ist und übermittelt wird, nachdem die Angebotsanforderung gesendet wurde, wird die Angebotsanforderung an alle eingeladenen Kreditoren erneut übermittelt. Das veröffentlichte Dokument wird auch auf der Seite **Offene veröffentlichte Angebotsanforderungen** aktualisiert.
