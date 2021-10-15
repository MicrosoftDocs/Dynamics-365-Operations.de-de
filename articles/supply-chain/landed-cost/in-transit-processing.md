---
title: Waren in Zustellung bearbeiten
description: Dieses Thema beschreibt, wie Sie mit Waren in Zustellung arbeiten. Wenn ein Auftrag oder eine Fahrt so festgelegt ist, dass die Waren in Zustellung verarbeitet werden, können die Waren in Rechnung gestellt werden, bevor sie im Lagerort zum Verbrauch eingegangen sind.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DeliveryTerms, InventLocation, InventPosting, ITMGoodsInTransitOrder, ITMTableListPage, ITMTable, ITMContainersListPage, ITMContainers, ITMFolioTableListPage, ITMFolioTable, ITMGoodsInTransitOrderEditLines, SysOperationTemplateForm, WHSRFMenuItem, WHSLocDirTable, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e85e3ba92b61e0208e1cf95d3f361d38772d83cb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571040"
---
# <a name="goods-in-transit-processing"></a>Waren in Zustellung

[!include [banner](../../includes/banner.md)]

Dieses Thema beschreibt, wie Sie mit Waren in Zustellung arbeiten. Diese Art von Auftrag wird nur vom Modul **Gesamttransportkosten** verwendet. Wenn ein Auftrag oder eine Fahrt für die Verwendung der Waren in Zustellung festgelegt ist, müssen Sie nicht warten, bis die Waren im Lagerort eingegangen sind, bevor Sie sie in Rechnung stellen können. Stattdessen werden die Waren fakturiert, wenn sie den Lagerort oder den Hafen des Lieferanten verlassen, und die finanziellen Kosten werden bei Beginn der Fahrt erfasst. Mit dieser Funktionalität können Sie den Bestand korrekt in Besitz nehmen, da Waren oft in das Eigentum Ihres Unternehmens übergehen, wenn sie den Lieferhafen verlassen.

Bei Waren in Zustellung werden die finanziell fortgeschriebenen Artikel in einem Zwischenlager empfangen, das als Lagerort in Zustellung bezeichnet wird. Die Waren verbleiben dann in diesem Lagerort, bis sie im endgültigen Ziellager (d.h. in dem Lagerort, der auf der Zeile des Kaufs definiert ist) empfangen werden können. Sie können nicht manuell entnommen werden.

Solange sich die Artikel in Zustellung befinden, sind sie nicht im Bestand verfügbar und können nicht aus dem Bestand für eine Lieferung entnommen werden. Sie können jedoch den Bestand der Waren in Zustellung einsehen. Sie können die Waren auch für die Produktprogrammplanung verwenden. In diesem Fall verwenden Sie das bestätigte Lieferdatum in der Zeile der Einkaufsbestellung als voraussichtliches Datum, an dem der Bestand für den Verbrauch zur Verfügung steht.

Die folgenden Abschnitte beschreiben die Einrichtung, die erforderlich ist, um Bestände und Fahrten unter Verwendung des Konzepts und der Funktionalität von Waren in Zustellung zu verarbeiten.

## <a name="terms-of-delivery"></a>Lieferbedingungen

Wenn Sie das Modul **Gesamttransportkosten** aktivieren, wird die Standard-Entität *Lieferbedingungen* erweitert, um die Funktion Waren in Zustellung zu unterstützen.

Wenn die Option **Waren in Zustellung** für den entsprechenden Lieferbedingungen-Datensatz auf *Ja* festgelegt ist, werden die Waren in den Lagerort für Waren in Zustellung eingelagert. Diese Aktion wird nur ausgelöst, wenn der Bestandseingang nicht vor der Bearbeitung einer Rechnung verarbeitet wird. Wenn die Lieferbedingungen für eine Bestellung auf Waren in Zustellung festgelegt sind, können Benutzer keinen Wareneingang mehr für die Einkaufsbestellung buchen. Wenn sie es versuchen, tritt ein Fehler auf. Die Fehlermeldung besagt, dass sie die Waren in Zustellung verwenden müssen, um fortzufahren.

Um mit Informationen zu den Lieferbedingungen für Waren in Zustellung zu arbeiten, gehen Sie zu **Beschaffung und Sourcing \> Einrichten \> Verteilung \> Lieferbedingungen**. Die folgende Tabelle beschreibt die Felder, die das Modul **Gesamttransportkosten** auf der Seite **Lieferbedingungen** hinzufügt, um die Funktionalität für Waren in Zustellung zu unterstützen. Beide Felder befinden sich auf dem Inforegister **Allgemein**. Weitere Informationen über die anderen Felder auf dieser Seite finden Sie unter [Lieferbedingungen (Formular)](/dynamicsax-2012//terms-of-delivery-form).

| Feld | Beschreibung |
|---|---|
| Obligatorischer Versandport | Legen Sie diese Option auf *Ja* fest, wenn ein Lieferhafen zwingend erforderlich ist, wenn die Lieferbedingungen gelten. |
| Waren in Zustellung – Verwaltung | Legen Sie diese Option auf *Ja* fest, um die Verwaltung von Waren in Zustellung zu verwenden, wenn die Lieferbedingungen gelten. |

## <a name="warehouses-for-goods-in-transit-and-under-delivery"></a>Lagerorte für Waren in Zustellung und Unterlieferungen

Wenn Sie das Modul **Gesamttransportkosten** aktivieren, wird die Standard-Entität *Lagerhäuser* erweitert, damit Einkäufe fakturiert werden können, während sich die Waren in einem Lagerort in Zustellung befinden.

Gesamttransportkosten fügt zwei neue Arten von Lagerorten hinzu: *Waren in Zustellung* und *unter Zustellung*. Lagerorte beider Typen können als Standard-Lagerorte ausgewählt werden. Für eine erfolgreiche Verarbeitung von Waren in Zustellung ist es erforderlich, dass sowohl das Waren in Zustellung-Lager als auch das Unterlieferungs-Lager auf der Seite **Lager** konfiguriert werden. Dann müssen für jedes Standardlager, das mit Gesamttransportkosten und Waren in Zustellung verwendet werden soll, das Waren in Zustellung-Lager und das Unterlieferungs-Lager für die verfügbaren Lagerorte jedes Typs ausgewählt werden.

Der Lagertyp *Transitware* wird mit Ihrem Lagerort für Waren in Zustellung verknüpft, und dieser Lagerort wird verwendet, um die Waren von Aufträgen für Waren in Zustellung zu verarbeiten, bevor sie im endgültigen Ziellager ankommen. Allgemein gilt, dass ein Waren in Zustellung pro Standort ausreicht, wenn Standort und Lagerort die einzigen Bestandsdimensionen sind, die für die Lagerortverwaltung verwendet werden. Wenn auch die Bestandsdimension Standort verwendet wird, muss für jede Kombination aus einem Betrieb und einem Lagerort ein Waren in Zustellung festgelegt werden, damit auch der Standardlagerort angegeben werden kann.

Um mit den Einstellungen für Waren in Zustellung für Ihre Lagerorte zu arbeiten, gehen Sie zu **Bestandsverwaltung \> Einrichten \> Bestandsaufteilung \> Lagerorte**. Die folgende Tabelle beschreibt die Felder, die das Modul **Gesamttransportkosten** auf der Seite **Lagerorte** hinzufügt, um die Funktion Waren in Zustellung zu unterstützen. Beide Felder erscheinen auf dem Inforegister **Allgemein**. Informationen über die anderen Felder auf der Seite finden Sie unter [Lagerorte (Formular)](/dynamicsax-2012//warehouses-form).

| Feld | Beschreibung |
|---|---|
| Waren in Zustellung – Lagerort | Identifizieren Sie den Waren in Zustellung Lagerort, der mit dem Hauptlager verbunden ist. |
| Unterlieferungslagerort | Identifizieren Sie das Unterlieferungslager, das mit dem Hauptlager verbunden ist. |

## <a name="posting-rules-for-landed-cost"></a>Buchungsregeln für landed cost

Gesamttransportkosten fügt zwei neue Buchungsregeln hinzu, die Sie konfigurieren können. Diese Buchungsregeln werden verwendet, um die Rechnungsbeträge der direkten Einkaufsbestellung finanziell zu buchen, um das Eigentum an den Waren zu identifizieren, wenn sie den Ursprungsort verlassen. Dieser Prozess ersetzt das Konzept *Wareneingang nicht fakturiert*, da die Waren fakturiert werden, bevor sie empfangen werden. <!-- KFM: Add a link to the related scenario when available. -->

Um mit Buchungsprofilen zu arbeiten, gehen Sie zu **Bestandsverwaltung \> Einrichten \> Buchen \> Buchen**. Auf der Registerkarte **Einkaufsbestellung** sind die folgenden neuen Buchungsregeln verfügbar:

- **Gesamttransportkosten, Waren in Zustellung** - Geben Sie die Buchungsregeln für die Verwaltung von Waren in Zustellung an.
- **Gesamttransportkosten, Kalkulation** - Legen Sie die Buchungsregeln für die Kalkulation fest.

## <a name="goods-in-transit-orders"></a>Waren in Zustellung

Sie können Waren in Zustellung direkt im Modul **Gesamttransportkosten** überprüfen und verwalten. Sie können Waren in Zustellung direkt auf der Seite **Waren in Zustellung** bearbeiten. Alternativ können Sie zu der Fahrt gehen, die mit den Waren in Zustellung-Aufträgen verbunden ist, und die gesamte Fahrt, den Transportcontainer oder die Palette bearbeiten. Wenn Sie eine Fahrt fakturieren und Waren in Zustellung erstellen, wird für jede Kombination von Bestand und Bestandsdimensionen, die mit der Zeile der Einkaufsbestellung verknüpft ist, eine neue Waren in Zustellung erstellt.

Um Waren in Zustellung zu verwalten, verwendet Gesamttransportkosten ein zweistufiges Verfahren:

1. Ein Artikel wird bei der Bearbeitung einer Lagerrechnung empfangen und erhält den Status *In Zustellung*.
1. Die Waren in Zustellung werden auf der Seite **Waren in Zustellung** bearbeitet und gehen dann in dem Lagerort ein, der auf der Einkaufsbestellung angegeben ist. Zu diesem Zeitpunkt wird der Status auf *Eingegangen* geändert.

Um mit Waren in Zustellung zu arbeiten, gehen Sie auf die Seite **Gesamttransportkosten \> Periodische Aufgaben \> Waren in Zustellung**.

## <a name="receiving-stock-from-the-goods-in-transit-warehouse"></a>Empfangen von Waren aus dem Lagerort in Zustellung

Sie können Waren aus einer Waren in Zustellung auf verschiedene Weise empfangen, je nachdem, wie Ihr System eingerichtet ist.

### <a name="in-transit-receiving"></a>In-transit-Empfang

Sie können den Wareneingang in Zustellung von jeder der folgenden Seiten aus durchführen:

- Wählen Sie auf der Seite **Waren in Zustellung** die Zeile aus und wählen Sie dann im Aktivitätsbereich **Empfang**.
- Wählen Sie auf der Seite **Alle Fahrten** eine Fahrt aus oder öffnen Sie sie. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Verwalten** in der Gruppe **Waren in Zustellung** die Option **Waren in Zustellung empfangen**.
- Wählen Sie auf der Seite **Alle Transportcontainer** einen Transportcontainer aus oder öffnen Sie ihn. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Verwalten** in der Gruppe **Waren in Zustellung** die Option **Waren in Zustellung empfangen**.
- Wählen Sie auf der Seite **Alle Paletten** eine Palette aus oder öffnen Sie sie. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Verwalten** in der Gruppe **Waren in Zustellung** die Option **Waren in Zustellung empfangen**.

> [!NOTE]
> Der Empfang in Zustellung wird allgemein in Situationen verwendet, in denen Lagerplätze und Chargen-/Serienverfolgung nicht verwendet werden.

### <a name="arrival-journal"></a>Eingangserfassung

Sie können Waren auch empfangen, indem Sie eine Wareneingangserfassung erstellen. Sie können eine Wareneingangserfassung direkt von der Seite „Fahrt“ aus erstellen. Die bewährten Verfahren, die Ihr Unternehmen festgelegt hat, bestimmen, ob das Wareneingangsprotokoll für den Empfang von Waren verwendet wird.

1. Öffnen Sie die Fahrt, den Container oder die Palette.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Verwalten** in der Gruppe **Funktionen** die Option **Ankunftserfassung erstellen**.
1. Legen Sie in der Dialogbox **Wareneingangserfassung erstellen** die folgenden Werte fest:

    - **Menge initialisieren** - Setzen Sie diese Option auf *Ja*, um die Menge aus der in Zustellung befindlichen Menge festzulegen. Wenn diese Option auf *Nein* gesetzt ist, wird keine Standardmenge aus den Waren in Zustellung festgelegt.
    - **Erstellen aus Waren in Zustellung** - Legen Sie diese Option auf *Ja* fest, um Mengen aus den ausgewählten Zeilen in Zustellung für die ausgewählte Fahrt, den ausgewählten Container oder die ausgewählte Palette zu nehmen.
    - **Erstellen aus Bestellzeilen** - Setzen Sie diese Option auf *Ja*, um die Standardmenge in der Wareneingangserfassung aus den Zeilen der Einkaufsbestellung festzulegen. Die Standardmenge in der Wareneingangserfassung kann auf diese Weise nur festgelegt werden, wenn die Menge in der Zeile der Einkaufsbestellung mit der Menge in der Waren in Zustellung übereinstimmt.

1. Verarbeiten Sie das Wareneingangsprotokoll wie in [Artikel-Eingänge mit einer Wareneingangserfassung erfassen](/dynamicsax-2012/appuser-itpro/register-item-receipts-with-an-item-arrival-journal) beschrieben.

> [!NOTE]
> Die Wareneingangserfassung wird allgemein in Situationen verwendet, in denen Lagerorte und Chargen-/Serienverfolgung verwendet werden, aber keine Lagerortverwaltung.
>
> Standard-Eingangsplätze sollten nicht in den Auftragszeilen angegeben werden, wenn ein Lagerplatz für die Einlagerung in der Wareneingangserfassung angegeben wird.

## <a name="warehouse-management"></a>Lagerortverwaltung

Wenn Sie das Modul **Gesamttransportkosten** aktivieren, werden mehrere Seiten im Modul **Lagerortverwaltung** so geändert, dass die Auftragsverarbeitung (speziell die Verarbeitung von Waren in Zustellung) über das Modul **Gesamttransportkosten** erfolgen kann. In diesem Abschnitt werden die Felder und Prozesse beschrieben, die im Modul **Lagerortverwaltung** hinzugefügt werden.

### <a name="mobile-device-menu-items"></a>Menüelemente des mobilen Geräts

Waren können über ein mobiles Gerät empfangen werden, vorausgesetzt, das Menü für mobile Geräte und das Modul **Lagerverwaltung** wurden für den Empfang von Waren in Zustellung festgelegt. Dieser Abschnitt beschreibt die Einrichtung, die mit dem Empfang von Waren in Zustellung verbunden ist.

Um mobile Geräte für die Bearbeitung von Waren in Zustellung festzulegen, gehen Sie zu **Lagerortverwaltung \> Einrichtung \> Mobiles Gerät \> Menüpunkte für mobile Geräte**.

Gesamttransportkosten fügt die folgenden Arbeitserstellungsprozesse zu den Menüpunkten für mobile Geräte hinzu, um die Bearbeitung von Waren in Zustellung zu unterstützen:

- Waren in Zustellung – Artikelempfang
- Waren in Zustellung Artikel-Eingang und Einlagerung

Die Konfigurationseinstellungen für diese Prozesse ähneln den Einstellungen für die [Arbeitserstellungsprozesse Einkaufsbestellung empfangen und einlagern](/dynamicsax-2012/appuser-itpro/configure-mobile-devices-for-warehouse-work). Allerdings fügt der Prozess *Waren in Zustellung Artikel empfangen und einlagern* zusätzlich das folgende Feld hinzu.

- **Transportcontainer abschließen** - Wenn diese Option auf *Ja* festgelegt ist, bietet die Warehouse Management Mobile App nach Abschluss der Einlagerungsarbeiten eine zusätzliche Option an, die **Transportcontainer abschließen** heißt. Wenn diese Option ausgewählt wird, wird die Arbeitskraft aufgefordert, zu bestätigen, dass der Container vollständig ist. Zu diesem Zeitpunkt werden alle Kurzbelege als eine untere Transaktion verarbeitet.

### <a name="location-directives"></a>Lagerplatzrichtlinien

Gesamttransportkosten fügt eine neue Arbeitsauftragsart mit dem Namen *Waren in Zustellung* auf der Seite **Lagerplatzrichtlinien** hinzu. Diese Arbeitsauftragsart sollte auf die gleiche Weise konfiguriert werden wie die [Arbeitsauftragsarten für Kaufsbestellungen](/dynamicsax-2012/appuser-itpro/create-a-work-template).

### <a name="work-templates"></a>Arbeitsvorlagen

In diesem Abschnitt werden Funktionen beschrieben, die das Modul **Gesamttransportkosten** Arbeitsvorlagen hinzufügt.

#### <a name="goods-in-transit-work-order-type"></a>Arbeitsauftragstyp „Waren in Zustellung“

Gesamttransportkosten fügt einen neuen Arbeitsauftragstyp mit dem Namen *Waren in Zustellung* auf der Seite **Arbeitsvorlagen** hinzu. Dieser Arbeitsauftragstyp sollte auf die gleiche Weise konfiguriert werden wie die [Arbeitsvorlagen für Einkaufsbestellungen](/dynamicsax-2012/appuser-itpro/create-a-work-template).

#### <a name="work-header-breaks"></a>Arbeitskopfzeilenumbrüche

Arbeitsvorlagen mit dem Arbeitsauftragstyp *Waren in Zustellung* können so konfiguriert werden, dass Arbeitkopfzeilen geteilt werden. Führen Sie auf der Seite **Arbeitsvorlagen** die folgenden Schritte aus:

- Legen Sie auf der Registerkarte **Allgemein** die Höchstwerte für die Arbeitskopfzeile fest. Diese Höchstwerte funktionieren auf die gleiche Weise wie bei Arbeitsvorlagen für Bestellungen. (Weitere Informationen finden Sie in [Arbeitsvorlagen für Einkaufsbestellungen](/dynamicsax-2012/appuser-itpro/create-a-work-template).)
- Verwenden Sie die Schaltfläche **Arbeitskopfzeilenumbrüche**, um festzulegen, wann das System neue Arbeitskopfzeilen basierend auf den zum Sortieren verwendeten Feldern erstellen soll. Um z.B. für jede Container-ID eine Arbeitskopfzeile zu erstellen, wählen Sie **Abfrage bearbeiten** im Aktivitätsbereich und fügen dann das Feld **Container-ID** auf der Registerkarte **Sortierung** des Abfrage-Editors hinzu. Felder, die der Registerkarte **Sortierung** hinzugefügt werden, stehen als *Gruppierungsfelder* zur Auswahl. Um Gruppierungsfelder festzulegen, wählen Sie **Arbeitskopfzeilenumbrüche** im Aktivitätsbereich und aktivieren dann für jedes Feld, das Sie als Gruppierungsfeld verwenden wollen, das Kontrollkästchen in der Spalte **Nach diesem Feld gruppieren**.

Gesamttransportkosten [erzeugt eine Überbuchung](over-under-transactions.md), wenn die registrierte Menge die ursprüngliche Auftragsmenge überschreitet. Wenn eine Arbeitskopfzeile abgeschlossen ist, aktualisiert das System den Status der Bestandsbuchungen für die Hauptauftragsmenge. Es aktualisiert jedoch erst die Menge, die mit der Überbuchung verknüpft ist, nachdem der Hauptauftrag vollständig gekauft wurde.

Wenn Sie eine Arbeitskopfzeile für einen bereits registrierten Überbuchung stornieren, wird die Überbuchung zunächst um die stornierte Menge reduziert. Nachdem die Überbuchung auf eine Menge von 0 (Null) reduziert wurde, wird der Datensatz entfernt und alle zusätzlichen Mengen werden gegenüber der Hauptauftragsmenge abgebucht.
