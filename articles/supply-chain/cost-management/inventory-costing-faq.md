---
title: Nachkalkulation von Beständen FAQ
description: Dieses Thema beantwortet einige häufig gestellte Fragen zur Nachkalkulation von Beständen in Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 05/03/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-03
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 45f65bd4a5cfb9bd0c4eb03ceb56eca452f6ec95
ms.sourcegitcommit: cbe9493d479f96f271d94599ec1b85131b26169f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809287"
---
# <a name="inventory-costing-faq"></a>Nachkalkulation von Beständen FAQ

[!include [banner](../includes/banner.md)]

Dieses Thema beantwortet einige häufig gestellte Fragen zur Nachkalkulation von Beständen in Microsoft Dynamics 365 Supply Chain Management.

## <a name="inventory-close-adjustments-and-recalculation"></a>Bestandsabschluss, Anpassungen und Neuberechnung

### <a name="is-the-inventory-close-required"></a>Ist der Abschluss des Bestands erforderlich?

Wenn Sie die Funktion Bestandsarchivierung verwenden möchten, ist der Bestandsabschluss erforderlich. Wenn Sie die Funktion zur Archivierung von Beständen nicht nutzen möchten, empfehlen wir Ihnen dringend, unabhängig von den von Ihnen verwendeten Nachkalkulationsmodellen, den Bestandsabschluss auszuführen.

### <a name="how-often-should-the-inventory-close-be-run"></a>Wie oft sollte der Bestandsabschluss ausgeführt werden?

Der Bestandsabschluss sollte mindestens einmal pro Sachkontoperiode ausgeführt werden. Wenn Ihr Sachkonto zum Beispiel auf einen kalendermonatsbasierten Fiskalkalender festgelegt ist, sollten Sie den Bestandsabschluss einmal pro Monat ausführen.

### <a name="is-the-inventory-recalculation-required"></a>Ist die Neuberechnung des Bestandes erforderlich?

Nein, die Neuberechnung des Bestandes ist nicht erforderlich. Wenn Sie ein periodisches Nachkalkulationsmodell wie first in, first out (FIFO), last in, first out (LIFO) oder gewichteter Durchschnitt verwenden, sollten Sie sich genau überlegen, ob Sie die Nachkalkulation des Bestands ausführen wollen. Es kann eine genauere Nachkalkulation in den von Ihnen gewählten heuristischen Modellen liefern.

### <a name="how-often-should-the-inventory-recalculation-be-run"></a>Wie oft sollte die Neuberechnung des Bestands ausgeführt werden?

Wenn Sie die Neuberechnung des Bestands planen, empfehlen wir Ihnen, diese täglich als Batch-Prozess auszuführen. Wenn Ihr Unternehmen keine häufigen Berichte über die Bestandswerte für periodische Nachkalkulationsmodelle benötigt, können Sie in Erwägung ziehen, die Bestandsberechnung weniger häufig auszuführen.

### <a name="when-should-i-use-the-on-hand-inventory-adjustment-on-the-closing-and-adjustments-page"></a>Wann sollte ich die Anpassung des Lagerbestands auf der Seite Abschluss und Anpassungen verwenden?

Die Anpassung des Lagerbestands kann erst nach Abschluss eines Bestandsabschlusses ausgeführt werden. Sie wird normalerweise für das Datum nach dem letzten Abschluss ausgeführt. Mit der Bestandsanpassung können nur Bestände angepasst werden, die zu dem Zeitpunkt, an dem Sie die Anpassung ausführen, noch vorhanden sind.

### <a name="when-should-i-use-the-inventory-transaction-adjustment-on-the-closing-and-adjustments-page"></a>Wann sollte ich die Anpassung der Transaktion für den Bestand auf der Seite Abschluss und Anpassungen verwenden?

Sie sollten die Anpassung von Transaktionen im Bestand verwenden, bevor Sie einen Bestandsabschluss ausführen. Sie wird in der Regel verwendet, um einen falschen Beleg zu korrigieren. Sie können die Anpassung der Bestandstransaktion nicht buchen, nachdem ein Bestandsabschluss ausgeführt und die Transaktion abgerechnet wurde.

### <a name="are-purchase-order-returns-treated-like-other-issues-during-the-inventory-close"></a>Werden Rücklieferungen von Bestellungen während des Bestandsabschlusses wie andere Ausgaben behandelt?

Ja. Ein Bestellungseingang ist eine Ausgabe, die in dem heuristischen Modell, das Sie für den Artikel auswählen, mit einem Eingang verrechnet wird. Wenn Sie eine periodische Nachkalkulation verwenden, können Sie die heuristischen Kosten durch Markierung außer Kraft setzen.

### <a name="what-happens-to-sales-order-returns-during-the-inventory-close"></a>Was geschieht mit Verkaufsaufträgen, die während des Bestandsabschlusses zurückgegeben werden?

Wenn Sie den Bestandsabschluss ausführen, wird die Rücklieferung eines Verkaufsauftrags wie ein Eingang in den Bestand behandelt. Ausgaben werden gegen den Bestand abgerechnet, basierend auf dem heuristischen Modell, das Sie für den Artikel auswählen.

### <a name="what-cost-price-is-used-on-a-sales-order-return"></a>Welcher Einstandspreis wird bei der Rücklieferung eines Verkaufsauftrags verwendet?

Wenn Sie eine Rücklieferung erstellen, die sich auf einen Verkaufsauftrag bezieht, wird der Wert des Feldes **Einheitspreis** aus dem ursprünglichen Verkaufsauftrag kopiert und das Feld **Rücklieferungseinstandspreis** in der Rücklieferung wird auf den angepassten Einstandspreis aus der ursprünglichen Bestandstransaktion für die Auftragsposition festgelegt, die zurückgeliefert wird. Wenn die Option **Wert offen** für die zugehörige Transaktion im Bestand auf *Ja* festgelegt ist, kann die Nachkalkulation im Bestand zu Aktualisierungen der Ausgabekosten im ursprünglichen Verkaufsauftrag führen. Das Feld **Rückgabe Einstandspreis** wird in diesem Szenario nicht aktualisiert. Wenn Sie jedoch einen Lieferschein für eine Rücklieferung buchen, prüft das System den Einstandspreis und verwendet die aktualisierten Kosten für die Transaktion zur Nachkalkulation des Bestands.

Bei einer Rücklieferung eines Artikels mit Standardkosten, der sich auf einen Verkaufsauftrag bezieht, verwendet das System die Standardkosten aus der Zeit des ursprünglichen Verkaufsauftrags, auch wenn für den Artikel eine neue Standardkostenrechnung aktiv ist.

Wenn Sie eine Rücklieferung erstellen, die sich nicht auf einen Verkaufsauftrag bezieht, wird das Feld **Rücklieferungseinstandspreis** auf den aktiven Artikelpreis festgelegt, den Sie für den Artikel in der Website haben, für den Sie die Rücklieferung erstellen. Wenn Sie keinen aktiven Einstandspreis in einer Nachkalkulation für den Artikel haben, wird der Wert 0 (Null) angezeigt. Wenn Sie den Wert auf 0 (Null) belassen, erhalten Sie eine Warnung, die besagt, dass die Rückgabe-Los-ID oder die Nachkalkulation nicht angegeben ist.

### <a name="what-is-the-expected-performance-of-the-inventory-close"></a>Was ist die erwartete Leistung des Bestandsabschlusses?

Viele Faktoren können die Leistung des Bestandsabschlusses beeinflussen. Zu diesen Faktoren gehören die Gesamtzahl der Artikel, die Gesamtzahl der Transaktionen in der Periode, die Bestandsmodelle, die Sie verwenden, und die Anzahl der Batch-Helfer, die Sie in den Parametern für die Bestands- und Lagerverwaltung konfigurieren. Sie können damit rechnen, dass der Abschluss nur wenige Minuten oder mehrere Stunden dauern kann. Es gibt keine spezifischen Vorgaben für die Zeit, die der Abschluss zum Ausführen benötigen sollte. Sie sollten Ihre nichtfunktionalen Geschäftsanforderungen für die Durchführung des Bestandsabschlusses definieren und eng mit Ihrem Partner zusammenarbeiten, um den Zeitplan für das Ausführen des Bestandsabschlusses festzulegen. Wenn die Leistung des Bestandsabschlusses unerwartet niedrig ist, sollten Sie ein Support-Ticket eröffnen.

## <a name="costing-sheet-and-indirect-costs"></a>Nachkalkulationsbogen und indirekte Kosten

### <a name="which-costing-models-support-the-costing-sheet"></a>Welche Kalkulationsmodelle unterstützen den Nachkalkulationsbogen?

Obwohl der Nachkalkulationsbogen in der Regel in Unternehmen verwendet wird, die mit der Standardkalkulation arbeiten, können Sie ihn mit jedem Kalkulationsmodell verwenden, das im Supply Chain Management verfügbar ist.

### <a name="can-i-have-multiple-costing-sheets-for-various-parts-of-my-organization"></a>Kann ich mehrere Nachkalkulationsbögen für verschiedene Teile meines Unternehmens haben?

Nein Sie können nur einen Nachkalkulationsbogen pro juristischer Entität haben.

### <a name="can-i-have-different-costing-sheets-for-each-site"></a>Kann ich für jeden Standort unterschiedliche Nachkalkulationsbögen haben?

Nein, Sie können nicht für jeden Standort einen eigenen Nachkalkulationsbogen haben. Sie können für jede juristische Entität nur einen Nachkalkulationsbogen erstellen. Sie können jedoch Gesamtknoten, Kostengruppen oder Knoten für indirekte Kosten pro Betrieb konfigurieren. Diese Konfiguration ist ein manueller Prozess, und Sie müssen die Hierarchie und die Artikelzuordnungen auf dem Nachkalkulationsbogen pflegen, wenn sich organisatorische oder betriebliche Änderungen ergeben. Wenn ein einzelner Artikel an mehreren Standorten produziert oder gekauft wird, gibt es keinen Mechanismus, mit dem Sie den Artikel auf dem Nachkalkulationsbogen für jeden Standort unterschiedlich behandeln können. Beachten Sie außerdem, dass alle indirekten Kostencodes einen Satz oder Zuschlag haben, der in Ihrer Nachkalkulation definiert ist. Die Nachkalkulationen, die Sie definieren, sind immer standortspezifisch.

### <a name="can-i-deactivate-and-activate-versions-of-the-costing-sheet"></a>Kann ich Versionen des Nachkalkulationsbogens deaktivieren und aktivieren?

Obwohl für den Nachkalkulationsbogen keine detaillierte Versionsverwaltung geführt wird, können Sie Änderungen an dem Nachkalkulationsbogen vornehmen und ihn dann, wenn Sie bereit sind, speichern und validieren. Es gibt keinen Mechanismus, der es Ihnen ermöglicht, zu einer älteren Version des Nachkalkulationsbogens zurückzukehren oder die an dem Nachkalkulationsbogen vorgenommenen Änderungen anzuzeigen. Wenn Sie Änderungen beginnen und nicht möchten, dass diese wirksam werden, können Sie die Seite schließen, ohne die Änderungen zu speichern und zu validieren. Sie werden dann aufgefordert, die Änderungen zu verwerfen.

### <a name="can-i-create-indirect-costs-for-each-item"></a>Kann ich indirekte Kosten für jeden Artikel erstellen?

Auf Ihrem Nachkalkulationsbogen können Sie Codes für indirekte Kosten erstellen, bei denen das Feld **Knotentyp** auf *Zuschlag*, *Satz* oder *Ausgabeeinheit basiert* festgelegt ist. Sie können dann den Satz oder den Aufschlag so definieren, dass er spezifisch für eine Artikelnummer ist. Auf der Seite **Satz** oder **Zuschlag** Inforegister, fügen Sie eine Zeile zum Raster hinzu. Legen Sie das Feld **Gültig für** auf *Tabelle* und das Feld **Beziehung** auf die spezifische Artikelnummer fest.

### <a name="can-i-create-an-indirect-cost-that-isnt-related-to-a-specific-item"></a>Kann ich indirekte Kosten erstellen, die sich nicht auf einen bestimmten Artikel beziehen?

Ja. Sie können eine Nachkalkulation erstellen, bei der das Feld **Knotentyp** auf *Output-Einheit basiert* festgelegt ist. Sie können dann das Feld **Untertyp** auf *Menge*, *Gewicht* oder *Volumen* festlegen, um die Menge, das Gewicht oder das Volumen des von Ihnen produzierten Artikels anzugeben. Der Satz, den Sie auf dem Inforegister **Satz** angeben, wird auf den von Ihnen ausgewählten Untertyp angewendet. Sie legen zum Beispiel das Feld **Untertyp** auf *Menge* und das Feld **Satz** auf *1,00 USD* fest und erstellen dann einen Produktions- oder Batch-Auftrag für eine Menge von 10. In diesem Fall betragen die indirekten Kosten, die auf die fertige Ware aufgeschlagen werden, 10,00 USD.

### <a name="can-i-use-the-costing-sheet-to-split-my-production-costs-by-hours-and-materials"></a>Kann ich den Nachkalkulationsbogen verwenden, um meine Produktionskosten nach Stunden und Materialien aufzuteilen?

Ja. Sie können auf Ihrem Nachkalkulationsbogen **Gesamt**-Knoten erstellen, um die Kosten nach einer von Ihnen gewählten Gruppierung zu trennen. Sie können z.B. einen **Gesamt**-Knoten erstellen, der *Stunden* heißt, und einen anderen, der *Materialien* heißt. Fügen Sie unter dem Knoten **Stunden** jede Codegruppe hinzu, die mit Ihren Stunden zusammenhängt. Fügen Sie unter dem Knoten **Materialien** jede Kostengruppe hinzu, die mit Ihren Materialien zusammenhängt.

## <a name="dimension-groups"></a>Dimensionsgruppen

### <a name="can-i-manage-cost-at-the-batch-or-serial-number-level"></a>Kann ich die Kosten auf der Ebene der Batches oder Seriennummern verwalten?

Ja, wenn Sie ein periodisches Kalkulationsmodell wie FIFO, LIFO, LIFO-Datum, gewichteter Durchschnitt oder gewichtetes Durchschnittsdatum verwenden, können Sie die Option **Wertmäßiger Bestand** für die Dimension **Batch** oder **Seriennummer** in der Dimensionsgruppe Nachkalkulation aktivieren, um die Kosten auf einer detaillierten Ebene zu verfolgen.

### <a name="can-i-manage-costs-at-the-location-level"></a>Kann ich die Kosten auf der Ebene des Standorts verwalten?

Nein, Sie können die Option **Wertmäßiger Bestand** nicht für die Dimension **Standort** in der Dimensionsgruppe Lagerung aktivieren. Wenn Ihr Unternehmen die Kosten auf einer detaillierteren Ebene nachverfolgen muss, überlegen Sie, ob Sie virtuelle Lager erstellen können, und wählen Sie dann die Option **Wertmäßiger Bestand** für die Dimension **Lager** in Ihrer Lagerdimensionsgruppe.

### <a name="should-i-enable-the-use-warehouse-management-processes-option-for-the-storage-dimension-group"></a>Soll ich die Option Lagerverwaltungsprozesse verwenden für die Dimensionengruppe Lager aktivieren?

Wenn Sie glauben, dass Sie die erweiterten Funktionen der Lagerverwaltung in Zukunft nutzen möchten, sollten Sie die Option **Prozesse der Lagerverwaltung nutzen** aktivieren. Nachdem Sie eine Gruppe von Dimensionen gespeichert haben, können Sie die Einstellung der Option **Prozesse der Lagerverwaltung verwenden** für diese nicht mehr ändern. Wenn Sie sich später für Lagerverwaltungsprozesse entscheiden, müssen Sie ein neues Lager erstellen, in dem diese Option aktiviert ist. Es gibt keinen automatisierten Prozess, mit dem Sie den gesamten Bestand von einem Lager in ein anderes Lager verschieben oder die zugehörigen Konfigurationen in ein neues Lager kopieren können.

### <a name="can-i-enable-the-use-warehouse-management-processes-for-the-storage-dimension-group-even-if-im-not-planning-to-use-advanced-warehousing"></a>Kann ich die Option Lagerverwaltungsprozesse für die Dimensionengruppe Lagerung verwenden auch dann aktivieren, wenn ich keine erweiterte Lagerverwaltung verwenden möchte?

Ja, auch wenn Sie nicht vorhaben, die erweiterten Funktionen der Lagerverwaltung zu verwenden, können Sie die Option **Prozesse der Lagerverwaltung verwenden** für die Gruppe der Dimensionen des Lagers aktivieren. Um Transaktionen zu erstellen und zu verarbeiten, müssen Sie die Mindestkonfiguration vornehmen, z. B. Reservierungshierarchien und Sequenzgruppen für Einheiten. Die Einstellungen für die erweiterte Lagerhaltung werden jedoch allgemein ignoriert, wenn Sie Kommissionierlisten, Lieferscheine und Produktzugänge (z.B. auf den Seiten für Verkaufsaufträge und Bestellungen) manuell bearbeiten.

### <a name="when-should-i-enable-the-physical-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Wann sollte ich die Option Physischer Bestand für eine Lager- oder Tracking-Dimensionengruppe aktivieren?

Sie sollten die Option **Physischer Bestand** für Lager- und Nachverfolgungsdimensionsgruppen aktivieren, wenn Sie detaillierte Datensätze zu dieser Dimension aufbewahren müssen. In der Regel wird jede Dimension, die aktiv ist, auch physisch nachverfolgt. Daher wird jeder Zugang, jeder Abgang und jede Bewegung des Bestands anhand der gewählten Dimension verfolgt. Wenn eine Dimension nicht obligatorisch ist (z.B. das Ladungsträger-Kennzeichen), können Sie die Optionen **Blanko-Empfang zugelassen** und **Blanko-Ausgabe zugelassen** aktivieren, damit Benutzer auch dann Bestand empfangen, ausgeben oder verschieben können, wenn die Dimension nicht angegeben ist.

### <a name="when-should-i-enable-the-financial-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Wann sollte ich die Option Wertmäßiger Bestand für eine Lager- oder Tracking-Dimensionsgruppe aktivieren?

Sie sollten die Option **Wertmäßiger Bestand** für Lager- und Nachverfolgungsdimensionsgruppen aktivieren, wenn Sie auf der Grundlage dieser Dimension detaillierte finanzielle Datensätze führen müssen. Die **Standort** Dimensionen werden immer finanziell verfolgt, während andere Dimensionen für die finanzielle Verfolgung optional sind. Wenn Sie ein periodisches Nachkalkulationsmodell wie FIFO, LIFO oder gewichteter Durchschnitt verwenden, bedeutet die Aktivierung der Option **Finanzieller Bestand** für eine Dimension, dass Sie Abrechnungen nur in den Fällen vornehmen, in denen Zugang und Abgang dieselben Dimensionswerte haben. Wenn Sie z.B. die Option **Wertmäßiger Bestand** für die Dimension **Lager** aktivieren, haben Sie in jedem Lager unterschiedliche Kosten, und Zu- und Abgänge aus verschiedenen Lagern können nicht abgerechnet werden.

### <a name="can-i-make-changes-to-a-product-storage-or-tracking-dimension-group-after-transactions-exist"></a>Kann ich Änderungen an einer Produkt-, Lager- oder Tracking-Dimensionsgruppe vornehmen, nachdem Transaktionen vorhanden sind?

Nachdem Sie eine Artikelmodellgruppe erstellt haben, können Sie die Einstellung der Felder **Deckungsplan nach Dimension**, **Für Einkaufspreise** und **Für Verkaufspreise** ändern, wenn das Kontrollkästchen **Aktiv** für eine Dimension in der Artikelmodellgruppe aktiviert ist. Andere Änderungen sind nicht zugelassen. Sie können zum Beispiel die Optionen **Aktiv**, **Rohlingsausgabe zugelassen**, **Rohlingsbon zugelassen**, **Physischer Bestand** und **Finanzieller Bestand** nicht aktivieren oder deaktivieren.

### <a name="can-i-change-the-product-storage-or-tracking-dimension-group-for-a-released-product"></a>Kann ich die Produkt-, Lager- oder Tracking-Dimensionsgruppe für ein freigegebenes Produkt ändern?

Wenn der Lagerbestand für ein Produkt 0 (Null) ist und die Option **Wert offen** für alle Bestandstransaktionen auf *Nein* festgelegt ist, können Sie die Lager- und Nachverfolgungsdimensionsgruppen auf der Seite für freigegebene Produktion ändern. Sie können die Gruppe der Produktdimensionen nicht mehr ändern, nachdem der Datensatz erstellt wurde.

## <a name="item-model-groups"></a>Lagersteuerungsgruppen

### <a name="when-should-i-enable-the-stocked-product-option"></a>Wann sollte ich die Option Vorrätiges Produkt aktivieren?

Sie sollten die Option **Lagerware** für jeden Artikel aktivieren, der in Ihrem Bestand verfolgt wird. Wenn diese Option aktiviert ist, werden detaillierte Bestandstransaktionen aufbewahrt, die den Eingang und die Ausgabe des Artikels verfolgen. Diese Option wird in der Regel für alle greifbaren Artikel aktiviert, die Sie z.B. in Ihrem Lager aufbewahren. Sie sollten diese Option auch aktivieren, wenn Sie planen, einen nicht-materiellen Artikel, wie z.B. einen Serviceartikel, zu Ihren Stücklisten oder Formeln hinzuzufügen. Wenn Sie die Option **Lagerware** nicht aktivieren, werden im untergeordneten Sachkonto keine Bestandstransaktionen nachverfolgt und die Kosten der Artikel werden in der Regel in Ihrem Hauptbuch verbucht. Diese Option wird z.B. häufig für Vorräte oder Dienstleistungen verwendet, die nicht in Ihren Stücklisten oder Formeln enthalten sind.

### <a name="when-should-i-enable-the-post-physical-inventory-option"></a>Wann sollte ich die Option Physischen Bestand buchen aktivieren?

Die Option **Physikalischen Bestand buchen** wird in der Regel aktiviert, wenn die Option **Bestandsartikel** aktiviert ist. Wenn Sie diese Option aktivieren, verfolgt das System die physische Aktualisierung des Artikels in der Transaktion für den Bestand. Diese Option wird in Verbindung mit Parametern in den Steuerelementen Kreditoren, Debitoren und Produktion verwendet, die angeben, dass die physische Aktualisierung einen Beleg erstellen soll. Sie werden diese Option in der Regel aktivieren, wenn Sie möchten, dass das Sachkonto immer dann aktualisiert wird, wenn Sie den Bestand physisch aktualisieren. Wenn Supply Chain Management nicht der Datensatz ist, den Sie für Ihre Finanzdaten verwenden, sollten Sie diese Option deaktivieren.

### <a name="when-should-i-enable-the-post-financial-inventory-option"></a>Wann sollte ich die Option Finanziellen Bestand buchen aktivieren?

Die Option **Wertmäßigen Bestand buchen** ist in der Regel aktiviert, wenn die Option **Bestandsartikel** aktiviert ist. Diese Option wird in Koordination mit Parametern in Kreditoren, Debitoren und Steuerelementen für die Produktion verwendet, die festlegen, dass die Finanzaktualisierung einen Beleg erstellen soll. Sie werden diese Option in der Regel aktivieren, wenn Sie möchten, dass das Sachkonto immer dann aktualisiert wird, wenn Sie den Bestand finanziell aktualisieren (z.B. durch die Fakturierung von Verkaufsaufträgen und Bestellungen oder das Beenden eines Produktionsauftrags). Wenn Supply Chain Management nicht der Datensatz ist, den Sie für Ihre Finanzdaten verwenden, sollten Sie diese Option deaktivieren.

### <a name="when-should-i-enable-the-post-to-deferred-revenue-account-on-sales-delivery-option"></a>Wann sollte ich die Option Auf abgegrenztes Umsatzkonto bei Verkaufslieferung buchen aktivieren?

Mit der Option **Buchen auf abgegrenztes Erlöskonto bei Verkaufslieferung** geben Sie an, ob Sie den Umsatz im Hauptbuch erfassen möchten, wenn Sie einen Lieferschein für einen Verkaufsauftrag buchen. Diese Option wird in der Regel verwendet, wenn zwischen Lieferschein und Rechnung eines Verkaufsauftrags eine lange Zeitspanne liegt oder wenn es nicht möglich ist, alle Verkaufsaufträge in der Periode zu fakturieren. In der Regel deaktivieren Sie diese Option, wenn Sie Ihre Verkaufsrechnungen unmittelbar nach der Buchung des Lieferscheins buchen. Auf diese Weise vermeiden Sie zusätzliche Buchungen im Hauptbuch, die sofort wieder storniert werden, wenn Sie einen Verkaufsauftrag fakturieren.

### <a name="when-should-i-enable-the-accrue-liability-on-product-receipt-option"></a>Wann sollte ich die Option Verbindlichkeit bei Produktzugang abgrenzen aktivieren?

In den meisten Unternehmen werden Sie die Option **Haftung bei Produktzugang** für alle Artikelmodellgruppen aktivieren wollen, unabhängig davon, ob es sich um ein gelagertes oder ein nicht gelagertes Produkt handelt. Diese Option wird verwendet, um eine Abgrenzung im Hauptbuch zu buchen, die auf dem Preis des Produktzugangs basiert. Da zwischen der Buchung des Produktzugangs für eine Bestellung und der Buchung der Rechnung in der Regel eine Verzögerung eintritt, müssen die meisten Unternehmen die Verbindlichkeit in der Bilanz ausweisen, um den lokalen Vorschriften wie den Generally Accepted Accounting Practices (GAAP) zu entsprechen. Wenn Supply Chain Management nicht der Datensatz ist, den Sie für Ihre Finanzdaten verwenden, sollten Sie diese Option deaktivieren. Wenn Ihr Unternehmen Beschaffungskategorien auf Bestellungen verwendet, können Sie das Erfordernis der Abgrenzung steuern, indem Sie die Option **Einkaufsaufwand bei Eingang abgrenzen** für die Kategorie-Richtlinienregel auf der Seite **Einkaufsrichtlinien** aktivieren.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-product-receipt-if-a-receipt-registration-isnt-yet-posted"></a>Wie kann ich einen Benutzer daran hindern, einen Produktzugang zu einer Bestellung zu buchen, wenn eine Zugangserfassung noch nicht gebucht wurde?

Sie können einen Benutzer daran hindern, einen Produktzugang für eine Bestellung zu buchen, wenn noch keine Bestellungsregistrierung stattgefunden hat, indem Sie die Option **Registrierungsanforderungen** für die Artikelmodellgruppe aktivieren. Diese Option wird typischerweise in Unternehmen verwendet, die einen zweistufigen Wareneingangsprozess verwenden, oder in Szenarien, in denen Sie z.B. eine Batch- oder Seriennummer auf den Artikeln, die Sie empfangen, registrieren müssen. Die Option **Registrierungspflicht** gilt für *alle* Lagerzugänge für einen Artikel, nicht nur für Bestellungen. Sie gilt beispielsweise für ein Lagererfassungs-Journal, das eine positive Menge und einen Produktionsauftragsbericht als fertiges Journal enthält.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-invoice-if-a-product-receipt-isnt-yet-posted"></a>Wie kann ich einen Benutzer daran hindern, eine Einkaufsrechnung zu buchen, wenn ein Produktzugang noch nicht gebucht wurde?

Sie können einen Benutzer daran hindern, eine Einkaufsrechnung zu buchen, wenn noch kein Produktzugang stattgefunden hat, indem Sie die Option **Empfangsanforderungen** für die Artikelmodellgruppe aktivieren. Diese Option wird in der Regel in Unternehmen verwendet, die verlangen, dass Eingänge im Hauptbuch für Abgrenzungen physisch erfasst werden. Die Option **Empfangsvoraussetzung** gilt für *alle* Bestandseingänge für einen Artikel, nicht nur für Bestellungen. Sie gilt beispielsweise für ein Lagererfassungs-Journal, das eine positive Menge und einen Produktionsauftragsbericht als fertiges Journal enthält. Wenn Ihr Unternehmen Beschaffungskategorien für Bestellungen verwendet, können Sie das Erfordernis einer Quittung steuern, indem Sie auf der Seite **Einkaufsrichtlinien** die Option **Empfangsanforderungen** für die Kategorie-Richtlinie aktivieren.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-packing-slip-if-a-sales-order-picking-list-isnt-yet-posted"></a>Wie kann ich verhindern, dass ein Benutzer einen Lieferschein für einen Verkaufsauftrag bucht, wenn eine Kommissionierliste für einen Verkaufsauftrag noch nicht gebucht wurde?

Sie können einen Benutzer daran hindern, einen Lieferschein oder eine Rechnung zu buchen, wenn noch keine Kommissionierliste vorliegt, indem Sie die Option **Kommissionieranforderungen** für die Artikelmodellgruppe aktivieren. Diese Option wird in der Regel in Unternehmen verwendet, die eine physische Kommissionierung im Lager durchführen (z.B. indem sie das mobile Gerät der Lagerverwaltung für die Kommissionierung verwenden). Die Option **Kommissionierpflicht** gilt für *alle* Bestandsausgaben für einen Artikel, nicht nur für Verkaufsaufträge. Dies gilt zum Beispiel für eine Lagererfassung mit einer negativen Menge und einem Journal mit einer Kommissionierliste für Produktionsaufträge.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-invoice-if-the-sales-order-packing-slip-isnt-yet-posted"></a>Wie kann ich einen Benutzer daran hindern, eine Verkaufsrechnung zu buchen, wenn der Lieferschein für den Verkaufsauftrag noch nicht gebucht wurde?

Sie können einen Benutzer daran hindern, eine Verkaufsrechnung zu buchen, wenn noch kein Lieferschein vorliegt, indem Sie die Option **Abzugsvoraussetzungen** für die Artikelmodellgruppe aktivieren. Diese Option wird in der Regel in Unternehmen verwendet, die einen physischen Verpackungsprozess im Lager durchführen (z.B. indem sie die Mobile-App der Lagerverwaltung zum Verpacken verwenden oder indem sie einen Beleg erstellen, der den versendeten Artikeln beigefügt wird). Die Option **Abzugspflicht** gilt für *alle* Bestandsausgaben für einen Artikel, nicht nur für Verkaufsaufträge. Dies gilt zum Beispiel für eine Lagererfassung mit einer negativen Menge und einem Journal mit einer Kommissionierliste für Produktionsaufträge.

### <a name="can-i-prevent-items-that-are-registered-from-being-sold"></a>Kann ich verhindern, dass Artikel, die registriert sind, verkauft werden?

Wenn ein Artikel in Ihrem Bestand im Supply Chain Management registriert wird, ist die Menge physisch verfügbar, um im System ausgegeben zu werden. Wenn Artikel, die zwar registriert, aber noch nicht eingegangen sind, *nicht* für die Ausgabe an Kundenaufträge oder Produktionsaufträge zur Verfügung stehen sollen, sollten Sie die Funktionen Bestandsstatus, Bestandssperre, Qualitätsaufträge, Quarantäneaufträge oder Reservierungen verwenden, um den Geschäftsprozess zu verwalten.

## <a name="production-costing"></a>Nachkalkulation für Produktion

### <a name="can-i-use-one-costing-model-for-raw-materials-and-a-different-costing-model-for-finished-goods"></a>Kann ich ein Kalkulationsmodell für Rohstoffe und ein anderes Kalkulationsmodell für fertige Waren verwenden?

Ja, Sie können für jeden Artikel verschiedene Nachkalkulationsmodelle verwenden. Es ist nicht ungewöhnlich, dass Hersteller eine periodische Nachkalkulation für Rohmaterialien und Standardkosten für halbfertige und fertige Waren verwenden.

### <a name="how-can-i-drive-overhead-off-machine-costs"></a>Wie kann ich die Gemeinkosten von den Maschinenkosten abziehen?

Um Ihre Maschinenkosten zu senken, müssen Sie für jede Maschine Ressourcen und Ressourcengruppen erstellen, die Ihren Geschäftsanforderungen entsprechen. Jede Ressource oder Ressourcengruppe kann Kostenkategorien zugewiesen werden, um die Kosten der Maschine zu steuern. Jede Kostenkategorie kann mit einer Kostengruppe verknüpft werden, und jede Kostengruppe kann als Grundlage für die Berechnung der indirekten Kosten auf dem Nachkalkulationsbogen verwendet werden.

### <a name="how-do-i-recognize-cost-that-is-related-to-energy-consumption-for-example-water-energy-or-gas-consumption-on-the-costing-sheet"></a>Wie erkenne ich Kosten, die mit dem Energieverbrauch zusammenhängen (z.B. Wasser-, Energie- oder Gasverbrauch) auf dem Nachkalkulationsbogen?

Allgemein können Sie Nachkalkulationen, die mit dem Energieverbrauch zusammenhängen, auf eine von zwei Arten erkennen:

- Erstellen Sie eine Zeile in Ihrer Stückliste oder Formel. In der Regel wird diese Zeile als Artikel erstellt, und Sie können die Maßeinheit angeben, die Sie im Verhältnis zu der von Ihnen produzierten Menge verbrauchen. Auf diese Weise kann der Benutzer während des Produktionsprozesses einen anderen Betrag verbrauchen. Sie können die Artikel automatisch auf der Grundlage des Wertes verbrauchen, den Sie im Feld **Bezugsprinzip** auswählen.
- Erzeugen Sie indirekte Kosten in Ihrem Nachkalkulationsbogen. In der Regel wird dieser Ansatz verwendet, um die Gesamtkosten Ihres Energieverbrauchs auf Ihren Produktionsprozess umzulegen. Sie können die Kostengruppe und die Absorptionsbasis verwenden, um den Verbrauch z.B. nach Material oder Arbeit in Ihrer Route zu skalieren.

Sie sollten die beste Option auf der Grundlage Ihrer Berichts-, Abstimmungs- und Vorgangsanforderungen auswählen.

### <a name="can-i-capture-resource-details-in-the-bom-or-formula"></a>Kann ich Ressourcendetails in der Stückliste oder Formel erfassen?

Ressourcendetails können nur in einem Vorgang der Route erfasst werden. Obwohl Sie einen Artikel erstellen können, um eine Ressource darzustellen, und ihm Kosten zuweisen können, um die Nachkalkulation für eine fertige Ware zu erhöhen, empfehlen wir diese Vorgehensweise normalerweise nicht. Wir empfehlen Ihnen stattdessen, eine einfache Route zu erstellen, die eine Zeile zur Verfolgung der Ressourcenkosten enthält, und den Vorgang so zu konfigurieren, dass er entweder am Anfang oder am Ende des Produktionsauftrags automatisch verbraucht wird.

### <a name="can-i-view-the-calculation-details-if-the-cost-is-manually-entered"></a>Kann ich die Berechnungsdetails einsehen, wenn die Kosten manuell eingegeben werden?

Nein Wenn Sie den Preis manuell auf der Seite **Artikelpreis** eingeben, sind die Schaltflächen **Kalkulationsdetails anzeigen** und **Kalkulationsdetails melden** nicht verfügbar. Wenn Sie die Schaltfläche **Kosten hochrechnen nach Kostengruppe** für einen manuell eingegebenen Selbstkostenpreis wählen, wird eine zusammengefasste Zeile angezeigt, und alle Kosten werden auf den Artikel der fertigen Ware hochgerechnet.

### <a name="does-the-system-calculate-variances-on-a-production-order-when-i-manually-enter-the-cost"></a>Berechnet das System Abweichungen bei einem Produktionsauftrag, wenn ich die Kosten manuell eingebe?

Ja, das System berechnet Abweichungen, wenn Sie einen Standardpreis manuell eingeben. Wenn Sie jedoch Standardkosten manuell eingeben, anstatt sie zu berechnen, werden alle Material-, Routen- und indirekten Kostenverbräuche im Produktionsauftrag als Substitutionsabweichung betrachtet. Wenn es zusätzliche Abweichungen gibt, wie z.B. der Verbrauch von zusätzlichen Materialien oder Arbeitskräften, werden diese ebenfalls als Abweichungen von der Fertigungsstückliste erfasst. Wir empfehlen Ihnen daher dringend, immer eine Nachkalkulation für Artikel auszuführen, die eine Stückliste, eine Route oder indirekte Kosten haben.

### <a name="how-can-i-carry-the-variances-from-a-subproduction-order-to-the-parent-production-order"></a>Wie kann ich die Abweichungen von einem Unterproduktionsauftrag auf den übergeordneten Produktionsauftrag übertragen?

Wenn Sie ein periodisches Nachkalkulationsmodell wie FIFO, LIFO oder gewichteter Durchschnitt verwenden, werden die Kosten aus einer Unterproduktion in dem heuristischen Modell berücksichtigt, das Sie für die Artikel ausgewählt haben. Wenn Sie eine Nachkalkulation benötigen, sollten Sie das Markierungsprinzip verwenden, um anzugeben, welche Unterproduktion für einen übergeordneten Produktionsauftrag ausgegeben wird. Alternativ können Sie z.B. die Option **Wertmäßiger Bestand** für die Dimension **Batch** oder **Seriennummer** in der Dimensionsgruppe Nachverfolgung verwenden.

### <a name="how-does-the-flushing-principle-affect-consumption"></a>Wie wirkt sich das Bezugsprinzip auf den Verbrauch aus?

Das Bezugsprinzip einer Stückliste, Formel oder Zeile steuert das Timing und die Technik, mit der der Artikel oder die Arbeit verbraucht wird. Wenn Sie *Start* wählen, wird der Artikel oder die Arbeitskraft automatisch verbraucht, wenn Sie den Produktionsauftrag starten. Wenn Sie *Fertig* wählen, wird der Artikel oder die Arbeitskraft automatisch verbraucht, wenn Sie den Produktionsauftrag als fertiggestellt melden. Wenn Sie *Manuell* wählen, muss ein Benutzer die Materialien manuell kommissionieren oder die Zeit in einem Auftrags- oder Routenkarten-Journal erfassen. Stücklisten und Formeln haben auch eine *Verfügbar am Standort* Option. Wenn Sie diese Option wählen, werden die Artikel automatisch verbraucht, nachdem sie an den Standort der Produktionsstätte übertragen wurden.

### <a name="how-should-i-run-cost-calculations-if-i-have-multi-level-boms-or-formulas"></a>Wie sollte ich Nachkalkulationen ausführen, wenn ich mehrstufige Stücklisten oder Formeln habe?

Allgemein empfehlen wir, dass Sie bei der Berechnung auf der untersten Ebene Ihrer Stücklisten oder Formeln beginnen. Um die Filterung zu erleichtern, wenn Sie Nachkalkulationen in großem Umfang ausführen, können Sie Berechnungsgruppen verwenden, um Produkte zu trennen. Wir empfehlen Ihnen außerdem, den periodischen Auftrag *Neuberechnung der Stücklisten* auszuführen, bevor Sie mit der Nachkalkulation beginnen. Jedes Unternehmen sollte den Produktmix berücksichtigen und eine Strategie festlegen, die den spezifischen Anforderungen Ihrer Produkt- und Stücklisten- oder Formelstrukturen entspricht.

## <a name="transfer-order-costing"></a>Nachkalkulation von Umlagerungsaufträgen

### <a name="is-there-a-way-to-allocate-freight-to-a-transfer-order-cost"></a>Gibt es eine Möglichkeit, die Frachtkosten einem Umlagerungsauftrag zuzuordnen?

Sie können einem Umlagerungsauftrag Belastungen hinzufügen, um Nachkalkulationen zu erstellen. Der Code für Belastungen definiert die Soll- und Habenbeträge für die von Ihnen hinzugefügte Belastung. Sie müssen zunächst im Modul **Bestandsverwaltung** Gebührencodes erstellen. Um einem Umlagerungsauftrag eine Belastung hinzuzufügen, wählen Sie **Belastungen** in der Zeile des Umlagerungsauftrags, dem Sie eine Belastung hinzufügen möchten.

## <a name="variances"></a>Abweichungen

### <a name="can-i-treat-variances-differently-based-on-the-site-or-warehouse"></a>Kann ich Abweichungen je nach Standort oder Lager unterschiedlich behandeln?

Es gibt keine Option zur Konfiguration von Abweichungskonten nach Standort. Wenn Sie die Nachkalkulation für ein freigegebenes Produkt verwenden, können Sie auf der Seite **Buchung** das Hauptkonto auswählen, das für Standardkostenabweichungsbuchungen verwendet wird. Sie können wählen, ob Sie die Konten für einen Artikel, eine Gruppe von Artikeln oder alle Artikel konfigurieren möchten. Sie können auch eine Kostengruppe, eine Gruppe von Kostengruppen oder alle Kostengruppen konfigurieren.

### <a name="can-i-separate-variances-that-are-the-result-of-currency-exchange-rates-from-other-types-of-variances"></a>Kann ich Abweichungen, die sich aus den Exchange Sätzen ergeben, von anderen Arten von Abweichungen trennen?

Wenn eine Abweichung das Ergebnis einer Wechselkursdifferenz zwischen dem Preis einer Bestellung und den Standardkosten für einen Artikel ist, gibt es keine Möglichkeit, die Wechselkursdifferenz von anderen Abweichungen zu trennen.

## <a name="reporting"></a>Berichterstellung

### <a name="how-many-inventory-value-report-configurations-can-i-create-and-use"></a>Wie viele Konfigurationen des Bestandswertberichts kann ich erstellen und verwenden?

Es gibt keine Begrenzung für die Anzahl der Konfigurationen für Bestandswertberichte, die Sie erstellen können. Sie sollten Ihre spezifischen Berichtsanforderungen bewerten und die Anzahl der Konfigurationen erstellen, die Sie benötigen, um diese Anforderungen zu erfüllen. Sie benötigen mindestens eine Bestandswertberichtskonfiguration, um den Bericht oder die Berichtsspeicheroption ausführen zu können.

### <a name="can-i-use-the-inventory-value-report-to-analyze-the-cost-of-an-item-in-each-warehouse"></a>Kann ich den Bestandswertbericht verwenden, um die Kosten eines Artikels in jedem Lager zu analysieren?

Ja. Sie können die Option **Ansicht** oder **Gesamt** für jede **Lager** Dimension in der Konfiguration des Bestandswertberichts aktivieren. Der Bericht zeigt jedoch nur Werte für Dimensionen an, bei denen die Option **Wertmäßiger Bestand** für die Lagerdimensionsgruppe aktiviert ist. Bei anderen Dimensionen zeigt es leere Spalten an. Weitere Informationen finden Sie unter [Beispiele für Bestandswertberichte und Logik](inventory-value-report-examples.md).

### <a name="how-can-i-view-the-inventory-quantity-as-of-a-specific-date-with-the-weighted-average"></a>Wie kann ich die Bestandsmenge zu einem bestimmten Datum mit dem gewichteten Durchschnitt anzeigen?

Sie können den Bericht **Bestandsalterung** verwenden, der eine Spalte **Durchschnittskosten pro Einheit** enthält, die den Wert des Bestands zu einem bestimmten Datum anzeigt. Weitere Informationen finden Sie unter [Beispiele für Bestandsalterungsberichte und Logik](inventory-aging-report.md).

### <a name="how-can-i-view-which-receipt-transactions-are-settled-against-an-issue-transaction"></a>Wie kann ich sehen, welche Zugangstransaktionen mit einer Ausgangstransaktion verrechnet werden?

Sie können die Nachkalkulationen für eine Bestandstransaktion einsehen, indem Sie auf der Seite **Bestandstransaktion** oder **Details zur Bestandstransaktion** im Aktionsbereich auf der Registerkarte **Bestand** die Option **Nachkalkulationen** oder **Kostenexplorer** wählen. Wenn Sie einen Bon auswählen, um die Ausgaben zu sehen, die mit der Transaktion verbunden sind, zeigt der Kosten-Explorer die Details nicht an. Die Details werden nur angezeigt, wenn Sie eine Ausgabe-Transaktion auswählen.

### <a name="how-does-the-inventory-value-report-show-items-that-have-a-positive-physical-quantity-and-a-negative-financial-value"></a>Wie zeigt der Bestandswertbericht Artikel an, die eine positive physische Menge und einen negativen finanziellen Wert haben?

Der Bestandswertbericht trennt die physischen und finanziellen Beträge und Mengen in eigene Spalten auf. Die im Bericht angezeigten Werte beziehen sich auf den Datumsbereich, den Sie beim Ausführen des Berichts ausgewählt haben. Die angezeigte Verdichtungsebene hängt von den Einstellungen ab, die Sie festgelegt haben. Wenn ein Artikel Transaktionen hat, die physisch empfangen und finanziell ausgegeben wurden, werden die Mengen und Werte unabhängig voneinander summiert. Wenn Sie die Detailebene als Transaktionen anzeigen lassen, werden die Zeilen für jeden Zugang und jeden Abgang separat angezeigt und die physischen und finanziellen Mengen bzw. Beträge werden angezeigt. Weitere Informationen finden Sie unter [Beispiele für Bestandswertberichte und Logik](inventory-value-report-examples.md).

### <a name="what-is-the-impact-of-storage-and-tracking-dimension-groups-on-the-inventory-value-report"></a>Wie wirken sich die Dimensionsgruppen für Lagerung und Nachverfolgung auf den Bestandswertbericht aus?

Wenn Sie die Option **Finanzwert** für eine Dimension in einer Lagerungs- oder Nachverfolgungsdimensionsgruppe aktivieren, können Sie die Option **Ansicht** oder **Gesamt** für die Dimension in der Konfiguration des Bestandswertberichts auswählen. Wenn Sie die Option **Ansicht** oder **Gesamt** für eine Dimension wählen, bei der die Option **Finanzwert** nicht ausgewählt ist, wird die Spalte in der Berichtsausgabe leer bleiben. Wenn Sie die Option **Finanzieller Wert** für eine Dimension in einer Lager- oder Verfolgungsdimensionsgruppe aktiviert haben und in der Konfiguration des Bestandswertberichts nicht die Option **Ansicht** oder **Gesamt** auswählen, werden die Werte für die ausgewählten Dimensionen, in denen sie finanziell verfolgt werden, zusammengefasst.

### <a name="can-i-customize-the-power-bi-embedded-reports-for-costing"></a>Kann ich die Power BI Embedded-Berichte für die Nachkalkulation anpassen?

Ja, Benutzer mit den richtigen Berechtigungen können das Design Canvas für jeden Power BI Embedded-Bericht im Supply Chain Management aktualisieren. Weitere Informationen finden Sie unter [Eingebettete Berichte in analytischen Arbeitsbereichen anpassen](../../fin-ops-core/dev-itpro/analytics/customize-analytical-workspace.md).

### <a name="where-can-i-view-the-variance-analysis-statement"></a>Wo kann ich die Abweichungsanalyse einsehen?

Sie können auf die Nachkalkulation zugreifen, indem Sie auf **Kostenverwaltung \> Abfragen und Berichte \> Bestandsbuchhaltung - Analyseberichte** oder **Kostenverwaltung \> Abfragen und Berichte \> Fertigungsbuchhaltung - Analyseberichte** gehen. Beide Optionen öffnen denselben Bericht, und der Bericht verhält sich auch genauso.

## <a name="item-prices-and-default-costs"></a>Artikelpreise und Standardkosten

### <a name="can-i-maintain-the-cost-for-each-product-variant"></a>Kann ich die Kosten für jede Produktvariante pflegen?

Ja. Sie können die Option **Einkaufspreis nach Variante verwenden** auf dem Inforegister **Kosten verwalten** der Seite **Freigegebene Produkte** aktivieren, um die Nachkalkulation nach Produktvarianten zu ermöglichen. (Diese Option steht nur für Produktstämme zur Verfügung.) Auf der Seite **Preis des Artikels** (die Sie entweder von der Seite **Kalkulationsversion** oder der Seite **Zugelassenes Produkt** aus öffnen können) können Sie dann **Anzeige der Dimensionen** wählen, um anzugeben, ob Sie die Dimension **Konfiguration**, **Größe**, **Farbe** oder **Stil** anzeigen möchten. Um die Einrichtung zu speichern und die ausgewählten Dimensionen jedes Mal zu verwenden, wenn Sie die Seite öffnen, aktivieren Sie die Option **Einrichtung speichern** und wählen dann **OK**. Sie können die Dimensionen nur für Artikel eingeben, bei denen die Dimensionen in der Produktdimensionsgruppe aktiv sind.

### <a name="can-i-maintain-the-cost-for-each-warehouse"></a>Kann ich die Nachkalkulation für jedes Lager pflegen?

Nein, Sie können den Artikelpreis nicht nach Lager pflegen. Sie können jedoch Handelsvereinbarungen für Einkaufspreise oder Verkaufspreise pro Lager pflegen. Wählen Sie zunächst die Option **Für Einkaufspreise** oder **Für Verkaufspreise** für die Dimension auf der Seite **Lagerdimensionsgruppe**. Wenn Sie dann die Handelsvereinbarung erstellen und die Zeilen für die Dimensionen öffnen, wählen Sie **Bestand \> Dimensionen anzeigen**, um auszuwählen, welche Dimension im Raster angezeigt werden soll. Um die Einrichtung zu speichern und die ausgewählten Dimensionen jedes Mal zu verwenden, wenn Sie die Seite öffnen, aktivieren Sie die Option **Einrichtung speichern** und wählen dann **OK**. Sie können die Dimensionen nur für Artikel eingeben, bei denen die Dimensionen in der Produktdimensionsgruppe aktiv sind.

### <a name="what-are-price-charges"></a>Was sind Preisbelastungen?

Preisbelastungen bieten eine Möglichkeit, einen festen Betrag auf den Einheitspreis des Artikels oder der Handelsvereinbarung aufzuschlagen. Wenn Sie einen Betrag in das Feld **Preis Belastungen** eingeben, können Sie auch einen Wert in das Feld **Belastungen Menge** eingeben. Die Preisbelastungen werden über die von Ihnen angegebene Belastungsmenge abgeschrieben. Aktivieren Sie die Option **Inkl. im Einheitspreis**, wenn Sie die Preisbelastungen in den Einheitspreis für den Artikel einbeziehen möchten. Diese Option ist für eine Standardkalkulation immer aktiviert.

### <a name="how-should-i-configure-prices-for-items-that-are-procured-in-multiple-currencies"></a>Wie sollte ich die Preise für Artikel konfigurieren, die in mehreren Währungen beschafft werden?

Wenn Sie auf der Seite **Freigegebenes Produkt** einen Standardpreis in das Feld **Einkaufspreis** eingeben, wird davon ausgegangen, dass dieser in der Buchhaltungswährung des Sachkontos der juristischen Entität angegeben ist, in der Sie sich befinden. Wenn Sie einen Kaufpreis in einer Nachkalkulation eingeben, bei der das Feld **Preistyp** auf *Kauf* festgelegt ist, wird angenommen, dass der Preis in der Buchhaltungswährung Ihrer juristischen Entität angegeben ist. Wenn Sie eine Bestellung für einen Kreditor erstellen, der eine andere Währung hat, rechnet das System automatisch den Betrag von der Buchhaltungswährung in die Transaktionswährung um, indem es den Satz verwendet, den Sie im Feld **Buchhaltungswährungswechselkurstyp** in Ihrem Sachkonto angeben.

Wenn Sie ein Journal für Handelsvereinbarungen erstellen, können Sie in jeder Zeile die Währung angeben, in der Sie den Preis ausdrücken möchten. Sie können Handelsvereinbarungen für mehrere Währungen, bestimmte Kreditor und viele andere Kombinationen von Faktoren erstellen. Wenn Sie eine Bestellung erstellen, für die eine Handelsvereinbarung für die von Ihnen gewählte Währung existiert, verwendet das System die Handelsvereinbarung mit der passenden Währung. Wenn Sie Transaktionen wie Produktzugänge oder Rechnungen buchen, wird der Betrag in die Buchhaltungswährung des Sachkontos umgerechnet, indem der von Ihnen im Sachkonto angegebene Satz verwendet wird.

### <a name="how-should-i-configure-costs-for-items-that-are-procured-in-multiple-currencies"></a>Wie sollte ich die Nachkalkulation für Artikel konfigurieren, die in mehreren Währungen beschafft werden?

Nachkalkulationen können nicht in mehr als einer Währung konfiguriert werden. Die Kosten, die Sie für den Artikelpreis oder die Standardkosten, die Sie im Feld **Preis** auf dem Inforegister **Kosten verwalten** der Seite **Freigegebenes Produkt** eingeben, werden immer in der Buchhaltungswährung des Sachkontos der von Ihnen ausgewählten juristischen Entität angegeben.

Wenn Ihr Unternehmen eine Nachkalkulation verwendet, sollten Sie eine Strategie für die Definition der Kosten bei mehreren Währungen festlegen. Sie sollten auch einen Prozess für die regelmäßige Nachkalkulation definieren, um die Anzahl der gebuchten Abweichungen zu reduzieren.

### <a name="can-i-use-the-profit-setting-on-the-cost-group-page-to-calculate-sales-prices"></a>Kann ich die Einstellung Gewinn auf der Seite Kostengruppe verwenden, um Verkaufspreise zu berechnen?

Ja, Sie können die Einstellung **Gewinn** auf der Seite **Kostengruppe** verwenden, um einen Prozentsatz hinzuzufügen, wenn die Verkaufspreise mit Hilfe einer Nachkalkulation berechnet werden. Weitere Informationen finden Sie unter [Stücklistenberechnungen](bom-calculations.md).

## <a name="marking"></a>Markierung

### <a name="how-does-marking-affect-periodic-costing-models"></a>Wie wirkt sich die Vormerkung auf periodische Nachkalkulationsmodelle aus?

Wenn Sie ein periodisches Nachkalkulationsmodell wie FIFO, LIFO oder gewichteter Durchschnitt verwenden und eine Zugangstransaktion gegen eine Abgangstransaktion markiert haben, wird das heuristische Modell des Artikels während des Bestandsabschlusses ignoriert. Stattdessen wird das System die tatsächlichen Kosten des Eingangs für die Nachkalkulation verwenden.

### <a name="what-happens-during-the-inventory-close-when-i-use-marking"></a>Was geschieht während des Bestandsabschlusses, wenn ich die Markierung verwende?

Wenn Sie Bons und Ausgaben markieren, wird der Bestandsabschluss die gemeinsam markierten Transaktionen abrechnen. Wenn zum Erstellen der Abrechnung die Markierung verwendet wird, wird das Feld **Prinzip** auf der Seite **Abrechnung** auf *Markierung* festgelegt. Wenn eine Transaktion markiert wird, bevor sie physisch oder finanziell aktualisiert wird, verwendet die Ausgabe die Kosten des markierten Belegs anstelle der laufenden Durchschnittskosten. Wenn die Transaktionen nach der Finanzaktualisierung markiert werden, wird der Bestandsabschluss- und Anpassungsprozess die Ausgabekosten so anpassen, dass sie mit den Eingangskosten übereinstimmen.

### <a name="can-i-manually-mark-transactions-when-i-use-standard-costing-or-moving-average"></a>Kann ich Transaktionen manuell markieren, wenn ich die Standardnachkalkulation oder den gleitenden Durchschnitt verwende?

Nein, Sie können Eingänge oder Ausgaben nicht manuell markieren, wenn Sie eine Nachkalkulation oder einen gleitenden Durchschnitt verwenden. Wenn Transaktionen (z.B. Direktlieferungen oder Intercompany-Bestellungen) automatisch vorgemerkt werden, bleibt der Datensatz für die Vormerkung erhalten und dient als feste Reservierung. Wenn Sie jedoch die Nachkalkulation oder den gleitenden Durchschnitt verwenden, hat die Markierung der Datensätze keinen Einfluss auf die Kosten der Artikel.

### <a name="how-does-marking-affect-the-profit-and-loss-statement"></a>Wie wirkt sich die Markierung auf die Gewinn- und Verlustrechnung aus?

Wenn Sie eine Ausgabetransaktion gegen einen Bon markieren, stimmen die Kosten für die Ausgabe mit dem ausgewählten Bon überein. Wenn Sie die Ausgabe physisch und finanziell buchen, wirkt sich die Buchung auf die Konten **Verkaufskosten der Waren, geliefert** und **Verkaufskosten der Waren, berechnet** aus, die Sie im Bestandsbuchungsprofil angeben. Wenn eine Transaktion nach der physischen oder finanziellen Aktualisierung markiert wird, erstellt der Prozess *Bestandsabschluss und -anpassung* eine Anpassung mit einem passenden Beleg, der das Konto **Kosten der verkauften Waren, kalkuliert** anpasst und mit dem Konto verrechnet, das Sie für **Kosten der Einheiten, kalkuliert** (Bestand) angeben.

### <a name="how-does-marking-affect-master-planning"></a>Wie wirkt sich die Markierung auf die Produktprogrammplanung aus?

Die Registerkarte **Standardaktualisierung** auf der Seite **Parameter der Produktprogrammplanung** enthält ein Feld mit der Bezeichnung **Aktualisierungskennzeichnung**. Die Option, die Sie dort auswählen, wird verwendet, wenn Sie einen geplanter Auftrag fixieren, der durch die Produktprogrammplanung erzeugt wurde. Die folgenden Optionen stehen zur Verfügung:

- *Nein* - Das System führt keine Markierung durch.
- *Standard* - Das System kennzeichnet Eingänge gegen Ausgaben gemäß dem Bedarfsverursacher. Ein Bedarfsauftrag wird mit einem Erfüllungsauftrag verrechnet. Wenn bei der Erfüllung eine gewisse Menge übrig bleibt, wird der Erfüllungsauftrag nicht markiert.
- *Erweitert* - Das System markiert sowohl die Bedarfsaufträge als auch die Erfüllungsaufträge, unabhängig davon, ob für den Erfüllungsauftrag noch eine Menge offen ist.

## <a name="negative-inventory"></a><a name="negative-inventory"></a>Negativer Bestand

### <a name="when-should-i-allow-physical-negative-inventory"></a>Wann sollte ich physische negative Bestände zulassen?

Allgemein empfehlen wir Ihnen nicht, einen physischen negativen Bestand zuzulassen, da es nicht möglich ist, weniger als 0 (Null) eines materiellen Artikels in Ihrem Lager zu haben. Die Geschäftsprozesse einiger Branchen und Geschäftsszenarien können jedoch Vorgänge einschränken, die es erfordern, dass der Bestand physisch negativ werden darf. Einzelhändler möchten z.B. den Verkauf eines Artikels, der zur Kasse gebracht wird, nicht verhindern, auch wenn das System anzeigt, dass keine Artikel verfügbar sind. Prozesshersteller liefern ein weiteres Beispiel. Für diese Hersteller kann der verbrauchte Betrag den in der Formel empfohlenen Wert übersteigen. Alternativ kann der Verbrauch auch geschätzt statt genau sein, so dass der Verbrauch die Menge an einem bestimmten Ort, z.B. einem Tank, übersteigt.

Wann immer möglich, sollten Sie Ihren Geschäftsprozess evaluieren und versuchen, ihn zu verbessern, um sicherzustellen, dass der Bestand nicht negativ sein kann. Wenn Sie negative Bestände zulassen müssen, sollten Sie über einen klaren Geschäftsprozess zur Korrektur der negativen Bestände verfügen, da diese die Nachkalkulation beeinträchtigen können.

### <a name="when-should-i-allow-financial-negative-inventory"></a>Wann sollte ich einen wertmäßigen Bestand zulassen?

Allgemein empfehlen wir den meisten Unternehmen, einen wertmäßigen negativen Bestand zuzulassen. (In den meisten Fällen werden Einkaufsrechnungen nicht verarbeitet, bevor Sie die Artikel versenden können.) Sie sollten diese Option aktivieren, wenn Sie bestimmte Geschäftsprozesse haben, die erfordern, dass der Verkaufspreis die endgültigen Kosten einer Bestellung widerspiegelt. Diese Anforderung könnte beispielsweise in einer Branche mit Einzelfertigung oder in bestimmten Regionen gelten, in denen dies gesetzlich vorgeschrieben ist.

### <a name="what-happens-to-the-cost-of-my-issues-when-the-inventory-is-negative"></a>Was passiert mit den Kosten für meine Ausgaben, wenn der Bestand negativ ist?

Wenn der Bestand für Ihren Artikel negativ ist und Sie mehr Artikel ausgeben, als Sie physisch besitzen, verwendet das System den Standardartikelpreis, um den laufenden Durchschnitt zu berechnen, wenn Sie ein periodisches Nachkalkulationsmodell wie FIFO, LIFO oder den gewichteten Durchschnitt verwenden. Wird für den Artikel kein Standardpreis angegeben, gibt das System den Bestand mit einem Wert von 0 (Null) aus. Dieses Verhalten kann dazu führen, dass zukünftige Berechnungen Ihres laufenden Durchschnitts oder gleitenden Durchschnitts ungenau sind.

### <a name="can-i-prevent-items-from-being-picked-packed-or-sold-on-sales-orders-and-production-orders-if-there-isnt-enough-on-hand-inventory"></a>Kann ich verhindern, dass Artikel auf Verkaufsaufträgen und Produktionsaufträgen kommissioniert, verpackt oder verkauft werden, wenn nicht genügend Lagerbestand vorhanden ist?

Ja. Wir empfehlen Ihnen, die Option **Physikalisch negativ** für die Artikelmodellgruppe zu deaktivieren, um zu verhindern, dass Artikel auf Verkaufsaufträgen und Produktionsaufträgen kommissioniert, verpackt oder verkauft werden.

### <a name="can-i-prevent-items-from-being-invoiced-on-a-sales-order-if-no-purchase-orders-have-been-invoiced-for-the-same-item"></a>Kann ich verhindern, dass Artikel auf einem Verkaufsauftrag in Rechnung gestellt werden, wenn für denselben Artikel noch keine Einkaufsrechnungen vorliegen?

Ja. Wir empfehlen Ihnen, die Option **Finanziell negativ** für die Artikelmodellgruppe zu deaktivieren, um zu verhindern, dass Artikel auf einem Verkaufsauftrag in Rechnung gestellt werden, wenn für denselben Artikel noch keine Einkaufsrechnungen vorliegen.

### <a name="how-does-negative-inventory-affect-financial-ratios-such-as-gross-profit-margin"></a>Wie wirkt sich ein negativer Bestand auf Finanzkennzahlen wie die Gewinnspanne aus?

Wenn Sie zulassen, dass Ihr Bestand negativ wird, können der Bestandswert in Ihrer Bilanz und die Kosten der verkauften Waren in Ihrer Gewinn- und Verlustrechnung zu niedrig ausgewiesen werden, insbesondere wenn für Ihre Artikel kein Standardpreis konfiguriert ist. Daher können Finanzberichte und Kennzahlen wie die Bruttogewinnspanne zu hoch angesetzt sein, weil die Kosten nicht korrekt sind. Wenn Sie ein Modell der periodischen Nachkalkulation wie FIFO, LIFO oder gewichteter Durchschnitt verwenden, kann der Wert der Abgänge angepasst werden, wenn Sie den Bestandsabschluss und die Bestandsanpassung ausführen, nachdem die negativen Bestandsmengen korrigiert wurden. Wenn Sie jedoch den gleitenden Durchschnitt verwenden, gibt es keine Möglichkeit, die einzelnen Transaktionen neu zu bewerten.

### <a name="how-should-i-correct-negative-inventory"></a>Wie sollte ich negative Bestände korrigieren?

Wir empfehlen Ihnen, negative Bestände häufig zu überwachen und zu korrigieren, wenn Ihr Unternehmen oder Ihre geschäftlichen Anforderungen es erfordern, dass Sie negative Bestände zulassen. Sie können die Werte des Bestands korrigieren, indem Sie eine Zykuszählung durchführen, eine Korrektur buchen oder ein Bewegungsjournal buchen. Wenn Sie unerwartete Zuwächse im Bestand auf einem bestimmten Hauptbuch-Sachkonto erfassen müssen, sollten Sie ein Bewegungsjournal verwenden. Andernfalls bucht das System, wenn Sie die Zykluszählung oder die Bestandsanpassung verwenden, die Bestandsanpassung auf das Konto **Bestandseingang** und den Ausgleich auf die Konten **Bestandsaufwand, Gewinn**, die Sie im Bestandsbuchungsprofil angeben.

### <a name="do-i-have-to-create-a-new-item-if-my-inventory-has-gone-negative-and-i-use-moving-average"></a>Muss ich einen neuen Artikel erstellen, wenn mein Bestand negativ geworden ist und ich den gleitenden Durchschnitt verwende?

Nein Wenn Ihr Unternehmen eine Nachkalkulation des physischen Bestands zulässt und Sie als Bestandsmodell den gleitenden Durchschnitt verwenden, verwendet das System die auf der Seite **Parameter der Bestands- und Lagerverwaltung** zugewiesene Nachkalkulation-Sequenz, um zu bestimmen, wie die Kosten Ihren Ausgaben zugewiesen werden. Allgemein empfehlen wir Ihnen, einen physischen negativen Bestand nicht zuzulassen. Weitere Informationen finden Sie unter den anderen Fragen im Abschnitt [Negativer Bestand](#negative-inventory) dieses Themas.

## <a name="not-stocked-products"></a>Nicht gelagerte Produkte

### <a name="can-i-post-sales-order-picking-lists-for-not-stocked-products"></a>Kann ich Verkaufsaufträge mit Kommissionierlisten für nicht vorrätige Produkte kommissionieren?

Wenn Sie eine Kommissionierliste für einen Verkaufsauftrag erstellen, der Artikel enthält, die sich in einer Artikelmodellgruppe befinden, die nicht auf Lager ist, sehen Sie keine Zeilen für diese nicht auf Lager befindlichen Artikel. Sie können die Mobile-App der Lagerverwaltung nicht verwenden, um nicht bestandsgeführte Artikel zu verarbeiten.

Wenn Sie einen Lieferschein für einen Verkaufsauftrag erstellen, der Artikel enthält, die sich in einer Artikelmodellgruppe befinden, die nicht auf Lager ist, legen Sie das Feld **Menge** auf *Kommissionierte Menge und nicht auf Lager befindliche Produkte* fest, um die nicht auf Lager befindlichen Artikel in die Belegerstellung einzubeziehen. Wenn Sie *Alle* wählen, werden nur lagerhaltige Artikel in den Lieferschein aufgenommen.

### <a name="should-i-use-a-not-stocked-product-or-a-category-sales-category-or-procurement-category"></a>Soll ich ein nicht gelagertes Produkt oder eine Kategorie (Verkaufskategorie oder Beschaffungskategorie) verwenden?

Die Wahl zwischen einem nicht gelagerten Produkt und einer Kategorie hängt von Ihren spezifischen Geschäftsanforderungen ab. Nicht gelagerte Produkte bieten allgemein mehr Steuerelemente für Standardwerte, wie z.B. Mengen und Preise in Bestellungen und Verkaufsaufträgen. Daher werden nicht gelagerte Produkte in Szenarien bevorzugt, in denen das gleiche Produkt oder die gleiche Dienstleistung mehr als einmal gekauft oder verkauft wird. Kategorien sind in Szenarien nützlich, in denen der Preis, die Artikel, die Beschreibungen usw. von Transaktion zu Transaktion inkonsistent sind. Kategorien können auch für jedes Produkt verwendet werden, um die Art des Produkts, das verkauft oder gekauft wird, zu klassifizieren.

## <a name="service-items"></a>Serviceelemente

### <a name="what-is-the-difference-between-a-service-item-and-a-not-stocked-product"></a>Was ist der Unterschied zwischen einem Artikel mit Service und einem Produkt ohne Lagerbestand?

Ein Service-Artikel ist eine Produktart. Wenn Sie ein neu zugelassenes Produkt erstellen, können Sie das Feld **Produkttyp** entweder auf *Artikel* oder *Service* festlegen. *Artikel* wird in der Regel ausgewählt, um anzuzeigen, dass es sich um einen materiellen Artikel handelt, während *Service* in der Regel ausgewählt wird, um anzuzeigen, dass es sich um einen immateriellen Artikel handelt.

Jedes zugelassene Produkt, unabhängig davon, ob es sich um einen Artikel oder ein Serviceprodukt handelt, kann gelagert oder nicht gelagert werden. Die Einstellung „auf Lager“ oder „nicht auf Lager“ wird durch die Artikelmodellgruppe festgelegt, die Sie für das zugelassene Produkt auswählen. Wenn Sie eine Artikelgruppe auswählen, die nicht auf Lager ist, erstellt das System z.B. keine Bestandstransaktionen für den zugehörigen Verkaufsauftrag oder Kauf.

### <a name="can-i-include-not-stocked-items-in-a-bom"></a>Kann ich nicht gelagerte Artikel in eine Stückliste aufnehmen?

Nein, Sie können ein zugelassenes Produkt, das mit einer Artikelmodellgruppe verknüpft ist, in der die Option **Lagerbestand** deaktiviert ist, nicht in eine Stückliste oder Formel aufnehmen. Es spielt keine Rolle, ob das Feld **Produkttyp** auf *Artikel* oder *Service* festgelegt ist. Nur Artikel, die auf Lager sind, können in Stücklisten- oder Formelzeilen aufgenommen werden.

## <a name="costing-modelspecific-questions"></a>Nachkalkulation modellspezifische Fragen

### <a name="which-costing-model-should-i-use"></a>Welches Modell der Nachkalkulation sollte ich verwenden?

Die Nachkalkulationsmodelle, die Sie auswählen sollten, hängen von Ihren geschäftlichen Anforderungen ab. Bevor Sie ein Nachkalkulationsmodell zur Verwendung im Supply Chain Management auswählen, sollten Sie überprüfen, ob das Modell von Ihren lokalen Vorschriften zugelassen ist. Wir empfehlen Ihnen, Ihre Auswahl mit einem zugelassenen Buchhalter in Ihrer Region zu überprüfen.

### <a name="can-i-use-more-than-one-costing-model-in-my-organization"></a>Kann ich mehr als ein Nachkalkulationsmodell in meinem Unternehmen verwenden?

Ja. Es gibt keine Begrenzung für die Anzahl der Artikelmodellgruppen oder Nachkalkulationsmodelle, die Sie im Supply Chain Management auswählen können.

### <a name="can-i-use-more-than-one-costing-model-for-each-item"></a>Kann ich für jeden Artikel mehr als ein Nachkalkulationsmodell verwenden?

Nein Sie können für jedes freigegebene Produkt nur ein Nachkalkulationsmodell auswählen. Dieses Verhalten wird durch die Artikelmodellgruppe gesteuert. Wenn Sie mehr als ein Kalkulationsmodell für die Nachkalkulation von Beständen verwenden müssen, sollten Sie das Add-In Globale Bestandsbuchhaltung in Betracht ziehen.

### <a name="when-i-use-manufacturing-execution-which-costing-methodology-should-i-use"></a>Welche Nachkalkulationsmethode sollte ich verwenden, wenn ich die Fertigungsausführung verwende?

Die Nachkalkulationsmodelle, die Sie auswählen sollten, hängen von Ihren geschäftlichen Anforderungen ab. Es gibt keinen spezifischen Vor- oder Nachteil bei der Verwendung eines Nachkalkulationsmodells, wenn Ihr Unternehmen auch die Fertigungsausführung verwendet.

### <a name="when-is-fefo-used"></a>Wann wird FEFO verwendet?

First expired, first out (FEFO) ist keine Nachkalkulationsmethode. Stattdessen handelt es sich um eine Reservierungstechnik, die häufig in Fertigungsunternehmen verwendet wird. Sie können FEFO-Reservierungen für eine Artikelmodellgruppe aktivieren, indem Sie die Option **FEFO datumsgesteuert** aktivieren und dann einen Wert im Feld **Auswahlkriterien** auswählen.

### <a name="are-there-performance-benefits-to-selecting-one-costing-model-over-another"></a>Gibt es Leistungsvorteile bei der Auswahl eines Nachkalkulationsmodells gegenüber einem anderen?

Allgemein gilt, dass das Nachkalkulationsmodell, das Sie für einen Artikel auswählen, nur minimale Auswirkungen auf die Gesamtleistung des Systems hat. Der Zeitaufwand für das Ausführen der Nachkalkulation des Bestands kann jedoch von dem von Ihnen gewählten Modell für die Nachkalkulation des Bestands beeinflusst werden. Wenn Sie z.B. Standardkosten oder gleitenden Durchschnitt verwenden, hat der Bestandsabschluss nur minimale Auswirkungen auf das System, da er nicht jede Transaktion im Bestand aktualisiert und Abrechnungen erstellt. Eine periodische Nachkalkulation wie FIFO, LIFO oder gewichteter Durchschnitt kann jedoch den Zeitaufwand für den Abschluss des Bestands erhöhen. Insbesondere kann der Abschlussprozess länger dauern, wenn Sie für den Prozess *Bestand abschließen* eine hohe Zahl in das Feld **Maximal zulässige Anzahl von Wiederholungen pro Artikel** oder eine niedrige Zahl in das Feld **Mindestbetrag zugelassen** eingeben.

### <a name="when-should-i-use-the-fixed-receipt-price-option"></a>Wann sollte ich die Option Fester Eingangspreis verwenden?

Wenn Sie auf der Seite **Artikelmodellgruppe** für einen Artikel das Kontrollkästchen **Fester Zugangspreis** aktivieren, verwendet das System den Zugangspreis als Standardkalkulation für den Bestandseingang. Wenn es eine Differenz zwischen dem Einkaufspreis und dem für einen Artikel konfigurierten Standardeinkaufspreis gibt, wird die Differenz auf das Konto **Festpreis Gewinn** oder **Festpreis Verlust** gebucht und auf das Konto **Festpreis Ausgleich** verrechnet. (Alle diese Konten werden auf der Seite **Buchung** angegeben).

Sie sollten das Kontrollkästchen **Fester Zugangspreis** aktivieren, wenn Sie ein periodisches Kalkulationsmodell wie FIFO, LIFO oder gewichteter Durchschnitt verwenden und Sie verlangen, dass eine Kaufpreisabweichung im Sachkonto verfolgt wird, wenn der Preis eines Zugangs von den Standardartikelkosten abweicht.

### <a name="moving-average"></a>Gleitender Durchschnitt

### <a name="is-moving-average-the-same-as-a-floating-average"></a>Ist der gleitende Durchschnitt dasselbe wie ein gleitender Durchschnitt?

Die Begriffe gleitender Durchschnitt, gleitender Durchschnitt und laufender Durchschnitt werden oft synonym verwendet. Von diesen Begriffen ist der gleitende Durchschnitt das einzige offizielle Modell für die Nachkalkulation, das im Supply Chain Management zur Verfügung steht. Obwohl der laufende Durchschnitt kein offizielles Kalkulationsmodell ist, ist es die Technik, die verwendet wird, wenn Sie ein periodisches Kalkulationsmodell wie FIFO, LIFO oder den gewichteten Durchschnitt verwenden. Der Begriff gleitender Durchschnitt wird im Supply Chain Management nicht verwendet und kann in anderen Systemen andere Bedeutungen haben.

### <a name="how-can-i-accommodate-the-difference-between-the-product-receipt-price-and-invoice-price-when-i-use-moving-average"></a>Wie kann ich die Differenz zwischen dem Preis beim Produktzugang und dem Rechnungspreis ausgleichen, wenn ich den gleitenden Durchschnitt verwende?

Wenn Sie die gleitende Durchschnittskalkulation verwenden, werden die physischen Kosten (Zugangspreis) zur Berechnung des gleitenden Durchschnitts für alle Transaktionen der Ausgabe verwendet. Wenn es eine Differenz zwischen den physischen Kosten (Zugangspreis) und den finanziellen Kosten (Rechnungspreis) gibt, bucht das System die Differenz automatisch auf das Hauptkonto, das für die Buchungsart **Preisdifferenz für gleitenden Durchschnitt** auf der Registerkarte **Bestand** der Seite **Bestandsbuchungsprofil** angegeben ist.

### <a name="where-is-the-price-difference-for-moving-average-presented-in-the-general-ledger"></a>Wo wird die Preisdifferenz für den gleitenden Durchschnitt im Hauptbuch ausgewiesen?

Wenn es eine Preisdifferenz zwischen der Buchung einer physischen Aktualisierung und einer finanziellen Aktualisierung für einen Zugang gibt, wird die Differenz auf das Hauptkonto gebucht, das für die Buchungsart **Preisdifferenz für gleitenden Durchschnitt** auf der Registerkarte **Bestand** der Seite **Bestandsbuchungsprofil** angegeben ist. Weitere Informationen finden Sie unter [Gleitender Durchschnitt](moving-average.md).

### <a name="when-i-use-moving-average-what-happens-if-there-is-an-issue-before-the-receipt"></a>Wenn ich den gleitenden Durchschnitt verwende, was passiert, wenn es vor dem Wareneingang eine Ausgabe gibt?

Typischerweise kann es vor dem Bon zu einer Ausgabe kommen, entweder weil Sie physischen negativen Bestand für die Artikelmodellgruppe zulassen oder weil die Ausgabe rückdatiert ist. Weitere Informationen finden Sie im Abschnitt [Negative Bestände](#negative-inventory) in diesem Thema.

Wenn Sie Transaktionen rückdatieren, empfehlen wir Ihnen, Ihre Geschäftsprozesse und Vorgänge sorgfältig zu prüfen, um festzustellen, ob es eine Möglichkeit gibt, dieses Szenario zu vermeiden. Wenn Sie eine Transaktion für einen Artikel rückdatieren, der einen gleitenden Durchschnitt verwendet, ordnet das System der Transaktion den aktuellen gleitenden Durchschnitt zu. Spätere Ausgaben werden nicht angepasst. Weitere Informationen zum gleitenden Durchschnitt mit rückwirkenden Transaktionen finden Sie unter [Gleitender Durchschnitt](moving-average.md).

### <a name="standard-costing"></a>Nachkalkulation

### <a name="what-is-the-difference-between-standard-costing-and-fixed-receipt-price"></a>Worin besteht der Unterschied zwischen der Nachkalkulation und dem festen Zugangspreis?

Die Standardkalkulation erfordert, dass Sie einen Artikelpreis definieren und die Kosten in einer Kalkulationsversion aktivieren. Diese Kosten werden für alle Einnahmen und Ausgaben verwendet. Abweichungen für die Zugänge zum Bestand werden im Hauptbuch unter Verwendung der Standardkostenabweichungskonten kalkuliert, die Sie auf der Registerkarte **Standardkosten** der Seite **Bestandsbuchungsprofil** angeben.

Wenn Sie jedoch feste Zugangspreise verwenden, sind nur die Kosten für Zugänge fixiert, und das System verwendet die Kosten, die Sie auf dem Inforegister **Kosten verwalten** der Seite **Freigegebenes Produkt** angeben. Differenzen zwischen den Standardkosten und dem Preis der Bestellung führen dazu, dass die Kaufpreisabweichung auf den Gewinn- und Verlustkonten für den festen Eingangspreis gebucht wird. Ausgaben verwenden keinen festen Eingangspreis. Stattdessen werden die Ausgaben zum Zeitpunkt der Buchung mit dem laufenden Durchschnitt bewertet (es sei denn, Sie verwenden die Markierung), und sie werden nach dem heuristischen Modell neu bewertet, das Sie auswählen, wenn Sie den Bestandsabschluss ausführen.

### <a name="can-i-use-fefo-reservations-with-standard-costing"></a>Kann ich FEFO-Reservierungen mit der Nachkalkulation verwenden?

Ja, Sie können FEFO-Reservierungen für eine Artikelmodellgruppe verwenden, wenn Sie die Nachkalkulation auswählen. FEFO-Reservierungen steuern die Reservierungslogik, die für die physische Handhabung der Artikel verwendet wird, während die Standardkalkulation die physischen und finanziellen Kosten für einen Artikel steuert.

### <a name="can-i-upload-pending-prices"></a>Kann ich ausstehende Preise hochladen?

Ja, Sie können das Excel Add-In oder das Data Management Framework verwenden, um einen ausstehenden Preis hochzuladen. Wir empfehlen Ihnen, die folgenden Entitäten zu verwenden:

- Ausstehende Artikelpreise (V2)
- Einheitskosten für ausstehende Kostenkategorien des Arbeitsplans
- Nachkalkulationsbogen Knoten Berechnungsfaktoren (V2)

### <a name="how-often-can-i-update-the-standard-cost-for-an-item"></a>Wie oft kann ich die Standardkosten für einen Artikel aktualisieren?

Es gibt keine Begrenzung für die Häufigkeit, mit der Sie neue Standardkosten aktivieren können. Wenn Sie eine neue Nachkalkulation für einen Artikel an dem Tag aktivieren, an dem die letzte Nachkalkulation aktiviert wurde, verwendet das System die zuletzt aktivierte Nachkalkulation bei neuen Transaktionen oder Aktualisierungen (z.B. bei Aktualisierungen von bestehenden Transaktionen).

### <a name="can-i-deactivate-or-delete-an-activated-cost"></a>Kann ich eine aktivierte Kalkulation deaktivieren oder löschen?

Nein, Sie können eine aktivierte Nachkalkulation nicht deaktivieren oder löschen. Wenn Sie eine Nachkalkulation fälschlicherweise aktiviert haben, können Sie eine neue Nachkalkulation aktivieren, die die korrekten Kosten enthält.

### <a name="are-calculation-groups-used-with-standard-costing"></a>Werden bei der Nachkalkulation Kalkulationsgruppen verwendet?

Berechnungsgruppen können mit jedem Artikel verwendet werden, unabhängig von der von Ihnen gewählten Artikelmodellgruppe. Die Kalkulationsgruppen werden während des Kosten-Rollups oder der Kostenkalkulation verwendet, um die Einstellungen festzulegen, die für die Artikel verwendet werden sollen, für die Sie die Kalkulation ausführen. Weitere Informationen über Berechnungsgruppen finden Sie unter [Stücklisten-Berechnungsgruppen](bom-calculation-groups.md).

### <a name="when-should-i-use-a-planned-costing-version"></a>Wann sollte ich eine Version der Nachkalkulation verwenden?

Nachkalkulationen können einen Typ von *Standardkosten* oder *Plan-Kosten* haben. Der Typ *Standardkosten* wird für die Kosten verwendet, die im System aktiv sind und in Transaktionen verbucht werden. Der Typ *Plan-Kosten* dient zum Ausführen von Nachkalkulationen und hat keinen Einfluss auf die Kosten von Transaktionen.

### <a name="can-the-total-cost-from-one-entity-be-transferred-to-another-entity-as-the-selling-cost"></a>Können die Gesamtkosten von einer Entität auf eine andere Entität als Verkaufskosten übertragen werden?

Es gibt keine automatisierte Möglichkeit, Nachkalkulationen von einer Firma in eine andere zu kopieren. Außerdem gibt es keine automatische Möglichkeit, Kosten von einem Kauf- in einen Verkaufspreis zu kopieren. Wenn Ihr Unternehmen eine dieser Aufgaben erledigen muss, überlegen Sie, ob Sie das Data Management Framework verwenden können, um die Daten aus Ihrer Nachkalkulation zu exportieren und in eine andere Firma hochzuladen, entweder als Verkaufspreis in der Kalkulationsversion oder als Handelsvereinbarung. Eine manuelle Bearbeitung der Dateien kann erforderlich sein.

### <a name="what-is-the-best-way-to-copy-planned-costs-to-a-standard-costing-version"></a>Wie kopiere ich Plankosten am besten in eine Version der Nachkalkulation?

Sie können die Schaltfläche **Kopieren** auf der Seite **Kalkulationsversionen** verwenden, um Artikelpreise, Kostenkategoriepreise oder indirekte Kosten von einer Nachkalkulation in eine andere zu kopieren.
