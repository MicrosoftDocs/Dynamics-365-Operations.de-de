---
title: Kreditorenzusammenarbeit mit externen Kreditoren
description: "In diesem Artikel wird beschrieben, wie Einkaufsvertreter das Kreditorenportal nutzen können, um Informationen über die Bestellungen und den Lieferbestand auszutauschen."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: cbd099403f48b502ca74bcb38ae12decedb8f2da
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="vendor-collaboration-with-external-vendors"></a>Kreditorenzusammenarbeit mit externen Kreditoren

[!include[banner](../includes/banner.md)]


In diesem Artikel wird beschrieben, wie Einkaufsvertreter das Kreditorenportal nutzen können, um Informationen über die Bestellungen und den Lieferbestand auszutauschen.

Das **Kreditorenzusammenarbeit** Modul richtet sich an Kreditoren, die keine elektronische Datenaustausch-Integration (EDI) mit Microsoft Dynamics 365 for Finance and Operations haben. Es ermöglicht Kreditoren die Arbeit mit Bestellung, Rechnung und Lieferungsbestandsinformationen. In diesem Thema wird beschrieben, wie Sie mit externen Kreditoren zusammenarbeiten können, die die Kreditorenzusammenarbeitschnittstelle verwenden, um mit PO und Lieferungsbestand zu arbeiten. Außerdem wird beschrieben, wie ein bestimmter Kreditor aktiviert wird, um Kreditorenzusammenarbeit zu verwenden und wie die Anzeige der Informationen definiert wird, die alle Kreditoren sehen, wenn Sie auf eine Bestellung antworten. Weitere Informationen dazu, was externe Kreditoren in der Kreditorenzusammenarbeitschnittstelle tun können, finden Sie unter [Kreditorenzusammenarbeit mit Debitoren](vendor-collaboration-work-customers-dynamics-365-operations.md)  

Weitere Informationen dazu, wie Kreditoren die Kreditorenzusammenarbeit in Rechnungsstellungsprozessen verwenden können, finden Sie unter [Kreditorenzusammenarbeit-Rechnungsstellungsarbeitsbereich](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace) Informationen darüber, wie neue Nutzer der Kreditorezusammenarbeit bereitgestellt werden, finden Sie unter [Kreditorenzusammenarbeitbenutzer verwalten](manage-vendor-collaboration-users.md).

Weitere Informationen dazu, wie Kreditoren die Kreditorenzusammenarbeit in Rechnungsstellungsprozessen verwenden können, finden Sie unter [Kreditorenzusammenarbeit-Rechnungsstellungsarbeitsbereich](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace) 

Informationen darüber, wie neue Nutzer der Kreditorezusammenarbeit bereitgestellt werden, finden Sie unter [Kreditorenzusammenarbeitbenutzer verwalten](manage-vendor-collaboration-users.md).

## <a name="define-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Hier können Sie die Informationen definieren, die den Kreditoren angezeigt werden, wenn sie auf Bestellungen antworten
Wenn Kreditoren auf eine Bestellung antworten, die Sie ihnen übermitteln, finden sie ein Di""""alogfeld, in dem sie bestätigen müssen, dass sie die Bestellung mit Änderungen annehmen, ablehnen oder akzeptieren möchten. Die Informationen, die dem Kreditor an diesem Punkt angezeigt werden, sind möglicherweise spezifisch für Ihr Unternehmen, und Sie können den Text definieren, der auf jeder der drei Bestätigungsnachrichten angezeigt wird. Beispielsweise kann der Text den Kreditor über den nächsten Schritte im Prozess oder die Bedingungen informieren.  

Wenn Sie den Text angeben, der in der Bestellung angezeigt wird:

1.  Öffnen Sie die Seite **Informationen für Kreditoren, die auf Bestellungen antworten**.
2.  Wählen Sie eine der folgenden Optionen aus:
3.  Klicken Sie auf **Bearbeiten**.
4.  Hier können Sie die Informationen eingeben, die Kreditoren im Feld **Informationensnachricht** angezeigt werden soll.

Wenn Sie Nachrichten in mehr als einer Sprache hinzufügen möchten, erstellen Sie separate Meldungen mit den entsprechenden Sprachcodes. Der Kreditor erhält die Nachricht in der Sprache angezeigt, die dieser Kreditor verwendet.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Legen Sie die Kreditorenzusammenarbeitoptionen für einen bestimmten Kreditor fest
Die allgemeinen Einstellungen für Kreditorenzusammenarbeit in Finance and Operations werden von einem Administrator konfiguriert. Beispielsweise bestimmen ein Administrator, welche Sicherheitsrollen für alle Kreditoren verfügbar sind, mit denen Sie zusammenarbeiten. Es gibt auch einige Einstellungen, die für jedes Kreditorenkonto variieren kann, und Sie sollten diese festlegen:
-   Kreditorenzusammenarbeit aktivieren.
-   Legen Sie fest, ob Sie möchten, dass dem Kreditor Preisinformationen angezeigt werden.

### <a name="enable-vendor-collaboration"></a>Kreditorenzusammenarbeit aktivieren

Bevor Benutzerkonten erstellt werden können für einen externen Lieferanten, müssen Sie das Kreditorenkonto konfigurieren, um die Nutzung der Kreditorenzusammenarbeit zu ermöglichen. Um dies zu bewerkstelligen, legen Sie das Feld **Zusammenarbeitaktivierung** in der Registerkarte **Allgemein** auf der Seite **Kreditor** fest. Es gibt zwei Möglichkeiten, die Sie auswählen können:

-   **Aktiv (Bestellung wird automatisch bestätigt)**- Bestellungen werden automatisch bestätigt, wenn der Kreditor diese akzeptiert ohne Änderungen.
-   **Aktiv (Bestellung wird nicht automatisch bestätigt)**- Bestellungen müssen manuell von der Organisation bestätigt werden, nachdem der Kreditor diese akzeptiert hat.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Legen Sie fest, ob Sie möchten, dass dem Kreditor Preisinformationen angezeigt werden.

Wenn Sie Preisangaben wie Einheitenpreise, Rabatte und Belastungen über die Zusammenarbeitsschnittstelle freigeben möchten, müssen Sie die Option **Bestellungspreise bzw. -betrag** im Kreditorenkonto auf **Ja** setzen. Diese Option befindet sich auf der Registerkarte **Standardwerte für Bestellungen**.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Arbeiten mit Bestellungen, wenn Sie Kreditorenzusammenarbeit verwenden
### <a name="sending-a-po-to-the-vendor"></a>Eine Bestellung an den Kreditor senden

Bestellungen werden in Finance and Operations vorbereitet. Wenn die Bestellung den Status **Genehmigt** hat, senden Sie ihn mithilfe der Aktion **Zur Bestätigung senden** auf der Seite **Bestellung** an den Kreditor. Der Status der Bestellung ändert auf **externe Prüfung**. Nachdem die Bestellung versendet wurde, kann der Kreditor diese auf der Seite **Bestellungen zur Prüfung** in der Kreditorenzusammenarbeitschnittstelle finden. Der Kreditor kann den Auftrag dann akzeptieren, ablehnen oder Änderungen vorschlagen. Der Kreditor kann auch Kommentare hinzufügen, um Informationen wie Änderungen an der Bestellung mitzuteilen. Wenn Sie die Aufmerksamkeit des Kreditors auf die neue Bestellung lenken möchten, können Sie die Bestellung auch per E-Mail senden, indem Sie das Druckverwaltungssystem verwenden.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Bestätigung und Akzeptieren der Bestellung durch den Kreditor

Wenn ein Lieferant eine Bestellung angenommen hat, wird die Bestellung automatisch bestätigt werden, oder sie muss möglicherweise manuell bestätigt werden. Dies ist davon abhängig, ob das Feld **Kreditorenaktivierung** für den Kreditor auf **Aktiv (Bestellung wird automatisch bestätigt)** oder auf **Aktiv (Bestellung wird nicht automatisch bestätigt)** festgelegt. wird.  

Die folgende Tabelle zeigt den üblichen Nachrichtenaustausch, abhängig davon, wie der Kreditor antwortet, wenn Sie ihm eine Bestellung zur Bestätigung senden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Kreditorenantwort</strong></td>
<td><strong>Ergebnis</strong></td>
</tr>
<tr class="even">
<td>Der Kreditor <strong>bestätigt</strong> die Bestellung. Finance and Operations ist konfiguriert, um Bestellungen automatisch zu bestätigen, wenn der Kreditor bestätigt.</td>

<td>Der Status einer Bestellstatus wird auf <strong>Bestätigt</strong> aktualisiert. Wenn der Auftrag aus einem bestimmten Grund nicht aktualisiert werden kann, wird die Antwort des Kreditors trotzdem als <strong>Bestätigt</strong> erfasst, die Bestellung bleibt aber im Status <strong>Externe Prüfung</strong>. 

Die Bestellung, die an den Kreditor gesendet wurden und der Status **In der externen Prüfung** wird mit bestätigtem Lieferdatum für die Positionen aktualisiert. Die Aktualisierung initiiert eine neue Version, die automatisch auf den Status **Bestätigt** aktualisiert wird. Wenn die Bestellung bestätigt wird, wird sie in der Zusammenarbeitschnittstelle des Kreditors angezeigt.</td>
</tr>
<tr class="odd">
<td>Der Kreditor <strong>bestätigt</strong> die Bestellung. Finance and Operations ist nicht konfiguriert, um Bestellungen automatisch zu bestätigen, wenn der Kreditor bestätigt.</td>
<td>Die Antwort des Kreditors wird als <strong>Bestätigt</strong> erfasst, die Bestellung bleibt jedoch im Status <strong>Externe Prüfung</strong>.

Die Bestellung, die an den Kreditor gesendet wurden und der Status **In der externen Prüfung** wird mit bestätigtem Lieferdatum für die Positionen aktualisiert. Die Aktualisierung initiiert eine neue Version, die automatisch auf den Status **In externer Überprüfung** aktualisiert wird. Sie werden dann in der Lage sein, die Bestellung manuell zu bestätigen.</td>

</tr>
<tr class="even">
<td>Der Kreditor <strong>lehnt</strong> die Bestellung ab.</td>
<td>Die Antwort des Kreditors wird als <strong>Abgelehnt</strong> erfasst, die Bestellung bliebt jedoch im Status <strong>Externe Prüfung</strong>. Die Ablehnung wird zusammen mit dem Kreditoren-Hinweis empfangen</td>
</tr>
<tr class="odd">
<td>Der Kreditor <strong>akzeptiert den Auftrag mit Änderungen</strong>. Änderungen werden auf Positionsebene vorgeschlagen. Es ist möglich, eine einzelne Positionen anzunehmen oder abzulehnen. Andere mögliche Änderungen sind:
<ul>
<li>Ändern von Mengen oder Datumsangaben.</li>
<li>Aufteilen von Positionen für sonstige Lieferdaten und Mengen.</li>
<li>Artikelersatz.</li>
</ul>
Preisangaben und Zuschläge können vom Kreditor nicht geändert werden. Vorschläge bei Änderungen dazu können mithilfe von Hinweisen vorgenommen werden.</td>
<td>Die Antwort des Kreditors wir als <strong>Mit Änderungen akzeptiert</strong>, erfasst und der Status der Bestellung bleibt <strong>In externer Prüfung</strong> Der Status zeigt, welche Änderungen der Kreditor vorgeschlagen hat. Weitere Informationen zum automatischen Verbrauch der Änderungen lesen Sie im Abschnitt zum Aktualisierungen von Bestellungen, wenn ein Kreditor Änderungen vorschlägt. </td>
</tr>
</tbody>
</table>

Mit dem Arbeitsbereich **Bestellung** **Vorbereitung** können Sie überwachen, auf welche Bestellungen der Kreditor geantwortet hat. Der Arbeitsbereich enthält zwei Listen mit Bestellungen mit dem Status **Externe Prüfung**:

-   Externe Prüfung erfordert Aktivität.
-   In externer Überprüfung Lieferantenantwort erwartet.

### <a name="changing-a-po"></a>Ändern einer Bestellung

Wenn Sie eine Bestellung ändern müssen, die bereits bestätigt wurde, können Sie eine neue Version der Bestellung über das Portal an den Kreditor senden. Die neue Bestellung weist einen Versionssuffix auf, der anzeigt, dass es sich um eine geänderte Version einer Bestellung handelt, die zuvor mitgeteilt wurde. Die Seite **Bestellungskreditoren-Bestätigungsverlauf** ermöglicht es Ihnen und Ihren Lieferanten, den Verlauf jedes Auftrags zu verfolgen. Die zuvor bestätigte Version der Bestellung bleibt in der Liste bestätigter POs, bis die neue Bestellung bestätigt wurde.

### <a name="cancelling-a-po"></a>Abbrechen einer Bestellung

Wenn Sie eine Bestellung stornieren, wird der Status wieder zu **Genehmigt** geändert. Sie müssen sie über das Kreditorportal zurück an den Kreditor senden, sodass der Kreditor die Stornierung bestätigen oder ablehnen kann. Nachdem die Stornierung bestätigt wurde, wird die Bestellung in der Liste bestätigter Bestellungen des Kreditors als **Storniert** angezeigt.

### <a name="adding-attachments-to-a-po"></a>Hinzufügen von Anhängen in eine Bestellung

Sie können Zuordnungen wie Dateien, Bilder und Hinweise für die Bestellung unter Verwendung des Dokumentverwaltungssystems hinzufügen. Die Anlagen des Typs **Extern** werden für den Kreditor angezeigt, wenn Sie die Bestellung an den Debitor senden.

## <a name="update-the-po-when-a-vendor-suggests-changes"></a>Aktualisieren Sie die Bestellung, wenn ein Kreditor Änderungen vorschlägt.
Wenn ein Kreditor auf den Auftrag die vorgeschlagene Änderung reagiert hat, besteht der nächste Schritt darin, die Antwort zu verarbeiten.
In **Bestellungsvorbereitungsarbeitsbereich** unter "Externen Überprüfung erfordert Aktivitätsliste" Sie können eine Bestellung identifizieren, auf die Kreditor mit Änderungen reagiert hat. In der "unter externer Prüfung erfordert Aktivitätsliste" können Sie auch zur Antwort des Kreditors navigieren. In einer Antwort kann ein Kreditor die folgenden Informationen im Kopf ändern.
 
-   Zeilendokumentreferenz
-   Lieferart
-   Lieferbedingungen
-   Bestätigtes Lieferdatum

Der Kreditor kann auch eine Notiz oder eine Anlage hinzufügen

In den Positionen kann der Kreditor die Menge und das Lieferdatum ändern, Hinweise und Anhänge hinzufügen, eine Position zurückweisen, eine Position mit einem Produkt ersetzen, das als Text eingegeben wird und eine Position in mehrere Lieferungen teilen. Abhängig davon, welche Änderungen vom Kreditor gemacht werden, erhält der Status einen unterschiedlichen Positionsstatus.
    
-   **Mit Änderungen akzeptiert**
-   **Abgelehnt**
-   **Ersetzt** In diesem Fall ist eine weitere Position hinzugefügt worden, die den Status **Stellvertreter** aufweist.
-   **Bestätigt** In Positionen des Zeitplans teilen. in diesem Fall werden Zeilen hinzugefügt, die den Status **Zeitplanpositionen** haben.

Wenn eine Position keine Änderungen hat, erhält sie den Positionsstatus **Angenommen**.

Auf der Antwort können Sie den zuvor genannten Positionsstatus anzeigen, aus denen der Typ der Änderungen hervorgeht, die der Kreditor gemacht hat. Darüber hinaus werden alle geänderten Felder in Fettschrift angezeigt, damit Sie die Änderungen besser ermitteln können.

Sie können eine Bestellung aktualisieren, indem Sie einmal auf **Prozess-Bestellungsaktualisierunga** aktion auf der Antwort auf einer Position klicken. Mithilfe einem Indikator, **Für Bestellaktualisierung verarbeitet?**, auf dem Kopf und der Positionen können Sie erkennen, ob das System den Kopf oder die Positionen verarbeitet hat, um die Bestellung mit allen möglichen Änderungen zu aktualisieren, die aus der Antwort stammen. Sie können den Prozess **Prozess-Bestellungsaktualisierung** jeweils nur einmal pro Kopf oder Position durchführen.

Nicht alle diese Änderung können auf einer Bestellung aktualisiert werden. Nur Aktualisierungen für den Kopf und Aktualisierungen von Datumsangaben und Mengen auf Positionen können in der Bestellung automatisch aktualisiert werden. Für andere Änderungen muss die Bestellung manuell aktualisiert werden. In diesem Fall enthält der Indikator **Für Bestellaktualisierung konfigurieren verarbeitet?** den Vermerk **Manuelle Aktualisierung**. Ein Beispiel für eine Änderung, die manuell genehmigt werden muss, würde sein, wenn ein Kreditor vorgeschlagen hat, eine Position in einem Zeitplan aufzuteilen.

Eine Position, die den Status **Angenommen** besitzt, hat ein bestätigtes Lieferdatum, das in der Bestellung aktualisiert wird, wenn der **Prozess Bestellungsaktualisierung** ausgeführt wird. Hinweise und Anhänge werden nicht automatisch auf die aktuelle Bestellung übertragen. Beachten Sie, dass, wenn die aktuelle Bestellung über die Aktivität **Prozess-Bestellungsaktualisierung** aktualisiert wird, Handelsvereinbarungen auf der Bestellungspositionen nicht neu abgeschätzt werden.


## <a name="po-statuses-and-versions"></a>PO-Status- und versionen
In diesem Abschnitt werden die verschiedenen Statuswerte, die eine Bestellung bis zum Zeitpunkt der Bestätigung haben kann, beschrieben. Es wird zudem beschrieben, an welchem Punkt neuen Versionen der Bestellung für den Kreditor angezeigt werden. Das Verhalten variiert, abhängig davon, ob Sie das Änderungsmanagement für PO verwenden. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versionen und Status, wenn Sie das Änderungsmanagement nicht verwenden

Die folgende Tabelle enthält ein Beispiel der Änderungen des Status und der Version, die eine Bestellung durchlaufen kann.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vorgang**                                                               | **Status und Version**                                                                                                                                       |
| Die ursprüngliche Version der Bestellung wird in Finance and Operations erstellt. | Der Status ist **Genehmigt**.                                                                                                                                  |
| Die Bestellung wird an den Kreditor gesendet.                                            | Eine Version wird in der Kreditorenportalschnittstelle erfasst und der Status wird in **Externe Prüfung** geändert.                                          |
| Der Kreditor übermittelt eine Antwort **Angenommen mit Änderungen**.                  | Der Status ist weiterhin **In externer Prüfung**.                                                                                                                  |
| Sie nehmen einige Änderungen vor, die vom Kreditor gefordert werden.                  | Der Status wird zurückgeändert in **Genehmigt**.                                                                                                                        |
| Sie senden die neue Version der Bestellung an den Kreditor.                        | Eine neue Version wird in der Kreditorenportalschnittstelle erfasst und der Status wird in **Externe Prüfung** geändert.                                      |
| Der Kreditor genehmigt die neue Version der Bestellung.                            | Der Status ist weiterhin **In externer Prüfung,**, es sei denn, das Kreditorenkonto ist so konfiguriert, dass die Bestellung automatisch den Status **Bestätigt** erhält, wenn er akzeptiert wird. |


Kreditoren müssen die Bestellung in der Kreditorenzusammenarbeitsschnittstelle nicht bestätigen. Sie können auch eine E-Mail-Nachricht senden oder ihrer Zustimmung zu einer Bestellung über andere Kanäle vermitteln. Sie können den Auftrag dann manuell in Finance and Operations bestätigen. In diesem Fall erhalten Sie eine Warnung, dass der Auftrag bestätigt wird, obwohl keine Antwort vom Kreditor vorhanden ist. Die Bestellung wird dann in der Bestätigungshistorie im Kreditorenportal als offener, bestätigter Auftrag ohne Antworten aufgeführt. Der Kreditor hat zusätzlich nicht mehr die Möglichkeit, die Bestellung zu bestätigen oder abzulehnen.  


>[!NOTE]
>Die Version der Bestellung, die anderen Prozessen in Dynamics 365 for Finance and Operations zur Verfügung steht, ist immer die neueste Version, auch wenn diese Version noch nicht erfasst wurde.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versionen und Status, wenn Sie das Änderungsmanagement verwenden

Wenn Sie das Änderungsmanagement für eine Bestellung aktiviert haben, durchläuft die Bestellung einen Genehmigungsworkflow bis zum Status **Genehmigt**. Dieser Prozess wird dem Kreditor nicht angezeigt.  

Die folgende Tabelle enthält ein Beispiel der Änderungen des Status und der Version, die eine Bestellung durchlaufen kann, wenn das Änderungsmanagement aktiviert ist: Die Version wird registriert, wenn die Bestellung aktiviert ist, nicht wenn die Bestellung an den Kreditor geschickt oder bestätigt wird.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vorgang**                                                               | **Status und Version**                                                                                                                                       |
| Die ursprüngliche Version der Bestellung wird in Finance and Operations erstellt.      | Der Kopfstatus ist **Entwurf**.  |
| Die Bestellung wird zum Genehmigungsprozess übermittelt. (Der Genehmigungsprozess ist ein interner Prozess, an dem der Kreditor nicht beteiligt ist.)                                                           | Der Status wird von in **Entwurf** auf **Wird überprüft** und **Genehmigung** geändert, wenn die Bestellung nicht während dem Genehmigungsprozess abgelehnt wird. Die genehmigte Bestellung wird als eine Version erfasst.           | 
| Die Bestellung wird an den Kreditor gesendet                                                            | Die Version wird in der Kreditorenportalschnittstelle erfasst und der Status wird in **Externe Prüfung** geändert.      |
| Sie nehmen einige Änderungen vor, die der Kreditor verlangt hat, entweder manuell oder mithilfe der Aktivität auf der Antwort, um die Bestellung zu aktualisieren.                                                            | Der Status wird zurückgeändert in **Entwurf**.     |
|Die Bestellung wird erneut zum Genehmigungsprozess übermittelt.                                                |  Der Status wird von in **Entwurf** auf **Wird überprüft** und **Genehmigung** geändert, wenn die Bestellung nicht während dem Genehmigungsprozess abgelehnt wird. Alternativ kann das System so konfiguriert werden, dass bestimmte Feldänderungen keine erneute Genehmigung erfordern. In diesem Fall wird der Status zuerst in **Entwurf** geändert und wird dann automatisch auf **Genehmigt** aktualisiert. Die genehmigte Bestellung wird als eine neue Version erfasst.                                         |
|Sie senden die neue Version der Bestellung an den Kreditor.                                                |  Die neue Version wird in der Kreditorenportalschnittstelle erfasst und der Status wird in **Externe Prüfung** geändert.                                         |
|Der Kreditor genehmigt die neue Version der PO.                                                |  Der Status wird entweder automatisch in **Bestätigt** geändert oder wenn Sie die Antwort vom Kreditor erhalten und die Bestellung dann bestätigen. |

## <a name="share-information-about-consignment-inventory"></a>Informationen zum Lieferbestand teilen
Wenn Sie Lieferungsbestand verwenden, können Kreditoren die Kreditorenzusammenarbeitschnittstelle verwenden, um Informationen zu den folgenden Seiten anzeigen:

-   **Bestellungen, die Lieferungsbestand verbrauchen -** Bestellungen für Lieferungsbestand werden erzeugt, wenn das Eigentum vom Bestand vom Lieferant an Ihr Unternehmen übergeht. Eine Produktquittung wird gleichzeitig gebucht. Diese Lieferungsbestellungen werden nur auf der Seite **Bestellungen, die Lieferungsbestands verbrauchen** angezeigt. Sie werden nicht auf der Seite **Alle bestätigen Bestellungen** im Modul **Kreditorenzusammenarbeit** angezeigt.
-   **Produkte erhalten vom Lieferungsbestand** - Diese Seite enthält alle Buchunge, in denen der Besitz der Prdukte vom Kreditor an das Unternehmen übertragen wurde. Verkäufer können diese Informationen verwenden, für die Rechnungsstellung.
-   **Verfügbarer Lieferungsbestand** - Diese Seite zeigt den Lieferungsbestand des Lieferanten, der an unserem Lagerort eingetroffen ist.





