---
title: Richtlinien zur Lieferungskonsolidierung konfigurieren
description: In diesem Artikel wird erläutert, wie Sie Standard- und benutzerdefinierte Versandkonsolidierungsrichtlinien einrichten.
author: Mirzaab
ms.date: 09/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0312d425d2ebc5311e894030423a916b90f1881a
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427981"
---
# <a name="configure-shipment-consolidation-policies"></a>Richtlinien zur Lieferungskonsolidierung konfigurieren

[!include [banner](../includes/banner.md)]

Der Lieferungskonsolidierungsprozess, der Richtlinien zur Lieferungskonsolidierung verwendet, ermöglicht eine automatisierte Lieferungskonsolidierung während der automatisierten und manuellen Freigabe an das Lager. Nachdem Sie diese Funktion aktiviert haben, müssen Sie Ihre anfänglichen Richtlinien konfigurieren. Wenn keine Richtlinien konfiguriert sind, generiert jede Verkaufslinie eine separate Lieferung mit einer einzelnen Ladelinie.

Die in diesem Artikel vorgestellten Szenarien zeigen, wie Standard- und benutzerdefinierte Versandkonsolidierungsrichtlinien eingerichtet werden.

> [!WARNING]
> Wenn Sie ein Microsoft Dynamics 365 Supply Chain Management-System aktualisieren, in dem Sie die Legacy-Sendungskonsolidierungsfunktion verwendet haben, funktioniert die Konsolidierung möglicherweise nicht mehr wie erwartet, es sei denn, Sie befolgen die hier gegebenen Ratschläge.
>
> Bei Supply Chain Management-Installationen, bei denen die *Lieferungskonsolidierungsrichtlinien* deaktiviert ist, aktivieren Sie die Sendungskonsolidierung mithilfe der **Lieferung bei Freigabe für Lagerort konsolidieren**-Einstellung für jedes einzelne Lager. Diese Funktion ist ab Version 10.0.29 obligatorisch. Wenn sie eingeschaltet ist, wird die **Lieferung bei Freigabe für Lagerort konsolidieren**-Einstellung ausgeblendet und die Funktionalität wird durch *Richtlinien zur Lieferungskonsolidierung* die ersetzt, die in diesem Artikel beschrieben werden. Jede Richtlinie legt Konsolidierungsregeln fest und enthält eine Abfrage, um zu steuern, wo die Richtlinie angewendet wird. Wenn Sie die Funktion zum ersten Mal aktivieren, werden keine Richtlinien zur Lieferungskonsolidierung auf der **Lieferungskonsolidierungsrichtlinien**-Seite definiert. Wenn keine Richtlinien definiert sind, verwendet das System das Legacy-Verhalten. Daher respektiert jedes bestehende Lager weiterhin seine **Lieferung bei Freigabe für Lagerort konsolidieren**-Einstellung, obwohl diese Einstellung jetzt ausgeblendet ist. Nachdem Sie jedoch mindestens eine Lieferungskonsolidierungsrichtlinie erstellt haben, wird die **Lieferung bei Freigabe für Lagerort konsolidieren**-Einstellung keine Auswirkungen mehr haben und die Konsolidierungsfunktion wird vollständig von den Richtlinien gesteuert.
>
> Nachdem Sie mindestens eine Lieferungskonsolidierungsrichtlinie definiert haben, überprüft das System die Konsolidierungsrichtlinien jedes Mal, wenn eine Bestellung an das Lager freigegeben wird. Das System verarbeitet die Richtlinien unter Verwendung der Rangordnung, die durch jeden **Richtliniensequenz**-Wert der Richtlinie definiert ist. Es wendet die erste Richtlinie an, bei der die Abfrage mit der neuen Reihenfolge übereinstimmt. Wenn keine Abfragen mit dem Auftrag übereinstimmen, erzeugt jede Auftragszeile eine separate Sendung, die eine einzelne Ladelinie hat. Als Ausweichlösung empfehlen wir Ihnen daher, eine Standardrichtlinie zu erstellen, die für alle Warenlager und Gruppen nach Bestellnummer gilt. Geben Sie dieser Fallback-Richtlinie den höchsten **Richtliniensequenz**-Wert, damit er zuletzt verarbeitet wird.
>
> Um das alte Verhalten zu reproduzieren, müssen Sie eine Richtlinie erstellen, die nicht nach Bestellnummer gruppiert und die Abfragekriterien enthält, die alle relevanten Warenlager umfassen.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Richtlinienfunktion zur Lieferungskonsolidierung aktivieren

Um die Funktion *Richtlinien zur Lieferungskonsolidierung* verwenden zu können, muss sie für ihr System aktiviert sein. Ab Supply Chain Management Version 10.0.29 ist die Funktion obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.29 ausführen, können Administratoren diese Funktionalität ein- oder ausschalten, indem sie nach der Funktion *Richtlinien zur Lieferungskonsolidierung* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

## <a name="set-up-your-initial-consolidation-policies"></a><a name="initial-policies"></a>Richtlinien für erste Sendungskonsolidierung festlegen

Wenn Sie mit einem neuen System arbeiten oder mit einem System, bei dem Sie gerade erst die Funktion *Lieferungskonsolidierungsrichtlinien* zum ersten Mal verwenden, befolgen Sie diese Schritte, um Ihre Erstkonsolidierungsrichtlinien für Sendungen einzurichten.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Für Lagerort freigeben \> Richtlinien zur Lieferungskonsolidierung**.
1. Wählen Sie im Aktionsbereich **Standardeinstellungen erstellen** aus, um die folgenden Richtlinien zu erstellen:

    - Eine Richtlinie namens *Standard* für den Richtlinientyp *Aufträge*.
    - Eine Richtlinie namens *Standard* für den Richtlinientyp *Umlagerungsproblem*.
    - Eine Richtlinie namens *CrossOrder* für den Richtlinientyp *Umlagerungsproblem*. (Diese Richtlinie wird nur erstellt, wenn Sie mindestens ein Lager hatten, in dem die Legacy-Einstellung **Lieferung bei Freigabe für Lagerort konsolidieren** aktiviert war.)
    - Eine Richtlinie namens *CrossOrder* für den Richtlinientyp *Aufträge*. (Diese Richtlinie wird nur erstellt, wenn Sie mindestens ein Lager hatten, in dem die Legacy-Einstellung **Lieferung bei Freigabe für Lagerort konsolidieren** aktiviert war.)

    > [!NOTE]
    > - Beide *CrossOrder*-Richtlinien berücksichtigen denselben Satz von Feldern wie die frühere Logik. Sie berücksichtigen jedoch auch das Bestellnummernfeld. (In diesem Feld werden Linien zu Lieferungen zusammengefasst, basierend auf Faktoren wie Lager, Transportart und Adresse.)
    > - Beide *Standard*-Richtlinien berücksichtigen denselben Satz von Feldern wie die frühere Logik. Sie berücksichtigen jedoch auch das Bestellnummernfeld. (In diesem Feld werden Linien zu Lieferungen zusammengefasst, basierend auf Faktoren wie Auftragsnummer, Lager, Transportart und Adresse.)

1. Wählen Sie ggf. die vom System erstellte *CrossOrder*-Richtlinie für den Richtlinientyp *Aufträge*, und wählen Sie dann im Aktionsbereich **Abfrage bearbeiten** aus. Im Abfrageeditor können Sie sehen, für welches Ihrer Lager die **Lieferung bei Freigabe für Lagerort konsolidieren**-Einstellung zuvor aktiviert war. Daher reproduziert diese Richtlinie Ihre vorherigen Einstellungen für diese Warenlager.
1. Passen Sie die neuen Standardrichtlinien nach Bedarf an, indem Sie Felder hinzufügen oder entfernen und/oder die Abfragen bearbeiten. Sie können auch so viele neue Richtlinien hinzufügen, wie Sie benötigen. Beispiele, die zeigen, wie Sie Ihre Richtlinien anpassen und konfigurieren, finden Sie im Beispielszenario weiter unten in diesem Artikel.

## <a name="scenario-configure-custom-shipment-consolidation-policies"></a>Szenario: Benutzerdefinierte Richtlinien zur Lieferungskonsolidierung konfigurieren

Dieses Szenario enthält ein Beispiel, das zeigt, wie Sie benutzerdefinierte Lieferungskonsolidierungsrichtlinien einrichten und diese dann mithilfe von Demodaten testen. Benutzerdefinierte Richtlinien können komplexe Geschäftsanforderungen unterstützen, bei denen die Lieferungskonsolidierung von mehreren Bedingungen abhängt. Für jede Beispielrichtlinie später in diesem Szenario ist eine kurze Beschreibung des Geschäftsfalls enthalten. Diese Beispielrichtlinien sollten in einer Reihenfolge eingerichtet werden, die eine pyramidenartige Auswertung der Abfragen gewährleistet. (Mit anderen Worten, die Richtlinien mit den meisten Bedingungen sollten als mit der höchsten Priorität bewertet werden.)

### <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Dieses Szenario verweist auf Werte und Datensätze, die in den für das Supply Chain Management bereitgestellten [Standarddemodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) enthalten sind. Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf *USMF* festlegen, bevor Sie beginnen.

### <a name="prepare-master-data-for-this-scenario"></a>Masterdaten für dieses Szenario vorbereiten

Bevor Sie die Übungen in diesem Szenario ausführen können, müssen Sie die Masterdaten vorbereiten, die für die Filterung erforderlich sind, wie in den folgenden Unterabschnitten beschrieben. (Diese Voraussetzungen gelten auch für die im Abschnitt [Beispielszenarien für die Verwendung von Richtlinien zur Lieferungskonsolidierung](#example-scenarios) aufgeführten Szenarien.)

#### <a name="create-two-new-product-filter-codes"></a>Erstellen Sie zwei neue Produktfiltercodes

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Produktfilter \> Produktfilter** und fügen Sie zwei Produktfilter hinzu:

    - Produktfilter 1:

        - **Filtercode:** *Brennbar*
        - **Filtertitel:** *Code 4*

    - Produktfilter 2:

        - **Filtercode:** *Explosiv*
        - **Filtertitel:** *Code 4*

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Öffnen Sie das Produkt mit Artikelnummer *M9200*. (Das von Ihnen ausgewählte Produkt muss für erweiterte \[WMS\]-Lagerortprozesse aktiviert sein, und dieses Produkt ist für WMS-Prozesse in den **USMF**-Demodaten voraktiviert.)
1. Auf dem Inforegister **Lagerort** legen Sie das Feld **Code 4** auf *Brennbar* fest.
1. Schließen Sie die Seite.
1. Öffnen Sie das Produkt mit Artikelnummer *M9201*. (Dieses Produkt ist auch für WMS-Prozesse in den **USMF**-Demodaten voraktiviert.)
1. Auf dem Inforegister **Lagerort** legen Sie das Feld **Code 4** auf *Explosiv* fest.
1. Schließen Sie die Seite.

#### <a name="create-a-new-transportation-mode-of-delivery"></a>Neuen Transportmodus zur Lieferung erstellen

1. Wechseln Sie zu **Transportverwaltung \> Einstellungen \> Spediteure \> Modus**.
1. Erstellen Sie einen Transportmodus, der in Konsolidierungsabfragen verwendet wird, und benennen Sie ihn *Airways*.
1. Wechseln Sie zu **Transportverwaltung \> Einstellungen \> Spediteure \> Spediteure**.
1. Erstellen Sie einen Spediteur mit den folgenden Einstellungen:

    - **Spediteur:** *Airways*
    - **Name:** *Airways*
    - **Modus:** *Airways*

1. Fügen Sie auf dem Inforegister **Services** für den neuen Spediteur eine Zeile mit den folgenden Einstellungen hinzu:

    - **Spediteur:** *Air*
    - **Transportmethode:** *Air*

1. Wählen Sie im Aktionsbereich **Speichern** aus.

    > [!NOTE]
    > Wenn Sie den neuen Spediteur speichern, wird das Feld **Lieferart** für die neue Position im Raster **Services** automatisch auf *Airwa-Air* gesetzt. Wenn Sie die Lieferart *Airwa-Air* für einen Kundenauftrag verwenden, wird der Transportmodus *Airways* für verwandte Lieferungen verwendet.

#### <a name="create-an-order-pool"></a>Arbeitsauftragspool anlegen

1. Wechseln Sie zu **Vertrieb und Marketing \> Einstellungen \> Aufträge \> Auftragspools**.
1. Erstellen Sie einen Auftragspool, der für die Konsolidierungsabfrage verwendet wird. Dieser Auftragspool sollte folgende Einstellungen haben:

    - **Pool:** Geben Sie eine Ganzzahl ein, die noch von keinem anderen Pool verwendet wird.
    - **Name:** *ShipCons*

1. Wechseln Sie zu **Vertrieb und Marketing \> Debitoren \> Alle Debitoren**.
1. Öffnen Sie den Kunden mit der Kontonummer *US-003*.
1. Auf dem Inforegister **Auftragsstandardabschnitt** stellen Sie das Feld **Auftragspool** auf den soeben erstellten Auftragspool ein.
1. Schließen Sie die Seite und wiederholen Sie die Schritte 4 und 5 für den Kunden mit der Kontonummer *US-004*.

### <a name="create-example-policy-1"></a>Beispielrichtlinie 1 erstellen

In diesem Beispiel erstellen Sie eine *Kunde+Modus*-Richtlinie, die für den folgenden Geschäftsfall verwendet werden kann:

- Die Richtlinie fragt ein bestimmtes Kundenkonto (*US-001*) und eine bestimmte Lieferart (*Airwa-Air*) ab.
- Die Konsolidierung mit offenen Lieferungen ist deaktiviert.
- Die Konsolidierung erfolgt pro Auftrags-ID. (Mit anderen Worten, es werden separate Lieferungen pro Bestellung, Lager usw. gesendet.)

Führen Sie die folgenden Schritte aus, um die Versandkonsolidierungsrichtlinie für diesen Geschäftsfall zu erstellen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Für Lagerort freigeben \> Richtlinien zur Lieferungskonsolidierung**.
1. Stellen Sie das Feld **Richtlinientyp** auf *Aufträge* ein.
1. Wählen Sie im Aktionsbereich **Neu** aus, um eine Richtlinie mit den folgenden Einstellungen zu erstellen:

    - **Richtlinienname:** *CustomerMode*
    - **Richtlinienbeschreibung:** *Kundenkonto und Lieferart*

1. Lassen Sie die **Konsolidierung mit offenen Lieferungen**-Option auf *Nein* gesetzt.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie auf dem Inforegister **Konsolidierungsfelder** in der Liste **Verbleibende Felder** die Zeile aus, in der das Feld **Feldname** auf *Lieferart* gesetzt ist.
1. Wählen Sie die Schaltfläche **Hinzufügen** ![rechter Pfeil](media/forward-button.png) aus, um das Feld in die Liste **Ausgewählte Felder** zu verschieben.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Suchen Sie im Abfrageeditor-Dialogfeld auf der Registerkarte **Bereich** im Raster die Zeile, in der das Feld **Feld** auf *Kundenkonto* gesetzt ist, und stellen Sie das Feld **Kriterien** für diese Zeile auf *US-001* ein.
1. Wählen Sie **Hinzufügen** aus, um eine Zeile mit den folgenden Einstellungen zum Raster hinzuzufügen:

    - **Tabelle:** *Auftragspositionen*
    - **Abgeleitete Tabelle:** *Auftragspositionen*
    - **Feld:** *Lieferart*
    - **Kriterien:** *Airwa-Air*

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.

> [!NOTE]
> Für diesen Business Case sind Bestellpositionen für den Kunden *US-001*, die die Lieferart *Airwa-Air* verwenden, nicht über Bestellungen hinweg konsolidiert. Diese Richtlinie soll zuerst in einer Sequenz verwendet werden, wenn Lieferungen für alle anderen Lieferarten für diesen Kunden konsolidiert werden.

### <a name="create-example-policy-2"></a>Beispielrichtlinie 2 erstellen

In diesem Beispiel erstellen Sie eine *Gefahrengut*-Richtlinie, die für den folgenden Geschäftsfall verwendet werden kann:

- Die Richtlinie fragt einen bestimmten Filtercode (*Gefahrengut*) und eine bestimmte Lieferart (*Airwa-Air*) ab.
- Die Konsolidierung mit offenen Lieferungen ist aktiviert.
- Die Konsolidierung erfolgt auftragsübergreifend. (Mit anderen Worten: es werden separate Lieferungen pro Konto, Lager usw. ausgeführt, jedoch nur innerhalb der in der Abfrage angegebenen Artikelgruppe.)

Führen Sie die folgenden Schritte aus, um die Versandkonsolidierungsrichtlinie für diesen Geschäftsfall zu erstellen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Für Lagerort freigeben \> Richtlinien zur Lieferungskonsolidierung**.
1. Stellen Sie das Feld **Richtlinientyp** auf *Aufträge* ein.
1. Wählen Sie im Aktionsbereich **Neu** aus, um eine Richtlinie mit den folgenden Einstellungen zu erstellen:

    - **Richtlinienname:** *Artikeltyp*
    - **Richtlinienbeschreibung:** *Konsolidieren Sie den gleichen Artikeltyp über Bestellungen hinweg*

1. Legen Sie die **Konsolidierung mit offenen Lieferungen**-Option auf *Ja* fest.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie auf dem Inforegister **Konsolidierungsfelder** in der Liste **Verbleibende Felder** die Zeile aus, in der das Feld **Feldname** auf *Lieferart* gesetzt ist.
1. Wählen Sie die Schaltfläche **Hinzufügen** ![rechter Pfeil](media/forward-button.png) aus, um das Feld in die Liste **Ausgewählte Felder** zu verschieben.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Erweitern Sie im Abfrageeditor-Dialogfeld auf der **Verknüpfungen**-Registerkarte in der Baumstruktur **Tabellen \> Ladungsdetails**.
1. **Tabellen-Join hinzufügen** auswählen.
1. Suchen Sie im angezeigten Beziehungsraster die Zeile, in der das Feld **Beziehung** auf *Lagerartikelnummer (Artikelnummer)* gesetzt ist und wählen Sie dann **Auswählen** aus. 
1. Wählen Sie auf der Registerkarte **Bereich** **Hinzufügen** aus, um eine Zeile mit den folgenden Einstellungen zum Raster hinzuzufügen:

    - **Tabelle:** *Lagerartikelnummer*
    - **Abgeleitete Tabelle:** *Lagerartikelnummer*
    - **Feld:** *Code 4*
    - **Kriterien:** *Brennbar*

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.

> [!NOTE]
> Für diesen Geschäftsfall werden alle Auftragspositionen, in denen Artikel einen bestimmten Filtercode haben (d. h., den Filtercode, in dem das **Code 4**-Feld auf *Brennbar* gesetzt ist), über Aufträge hinweg mit anderen Artikeln des gleichen Typs konsolidiert. Wenn für dasselbe Konto, dasselbe Lager und dieselbe Artikelgruppe eine offene Lieferung vorhanden ist, werden die neuen Zeilen daran angehängt.

### <a name="create-example-policy-3"></a>Beispielrichtlinie 3 erstellen

In diesem Beispiel erstellen Sie eine *Kundenanforderungen*-Richtlinie, die für den folgenden Geschäftsfall verwendet werden kann:

- Die Richtlinie fragt nach einem bestimmten Kundenkonto.
- Die Konsolidierung mit offenen Lieferungen ist aktiviert.
- Die Konsolidierung erfolgt auftragsübergreifend, basiert jedoch auf Kundenanforderungen. (Mit anderen Worten: mehrere Bestellungen werden basierend auf derselben Kundenanforderungsnummer und demselben Lager in Lieferungen zusammengefasst.)

Führen Sie die folgenden Schritte aus, um die Versandkonsolidierungsrichtlinie für diesen Geschäftsfall zu erstellen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Für Lagerort freigeben \> Richtlinien zur Lieferungskonsolidierung**.
1. Stellen Sie das Feld **Richtlinientyp** auf *Aufträge* ein.
1. Wählen Sie im Aktionsbereich **Neu** aus, um eine Richtlinie mit den folgenden Einstellungen zu erstellen:

    - **Richtlinienname:** *CustomerOrderNo*
    - **Richtlinienbeschreibung:** *Konsolidieren Sie die Positionen basierend auf der Kundenbestellung*

1. Legen Sie die **Konsolidierung mit offenen Lieferungen**-Option auf *Ja* fest.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie auf dem Inforegister **Konsolidierungsfelder** in der Liste **Verbleibende Felder** die Zeile aus, in der das Feld **Feldname** auf *Debitorenmaterialanforderung* gesetzt ist.
1. Wählen Sie die Schaltfläche **Hinzufügen** ![rechter Pfeil](media/forward-button.png) aus, um das Feld in die Liste **Ausgewählte Felder** zu verschieben.
1. Wählen Sie in der Liste **Verbleibende Felder** die Zeile aus, in der das Feld **Feldname** auf *Lieferart* gesetzt ist.
1. Wählen Sie die Schaltfläche **Hinzufügen** ![rechter Pfeil](media/forward-button.png) aus, um das Feld in die Liste **Ausgewählte Felder** zu verschieben.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Suchen Sie im Abfrageeditor-Dialogfeld auf der Registerkarte **Bereich** die Zeile, in der das Feld **Feld** auf *Kundenkonto* gesetzt ist, und stellen Sie das Feld **Kriterien** für diese Zeile auf *US-001* ein.
1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.

> [!NOTE]
> In diesem Geschäftsfall werden alle Auftragspositionen, in denen Kundenaufträge dieselbe Kundenanforderungsnummer haben, unabhängig von der Kundenauftragsnummer zu einer Lieferung zusammengefasst. (Die Kundenanforderungsnummer wird als Bestellungsnummer, \[PO\]-Nummer, des Kunden verwendet.) Wenn für dasselbe Konto, dasselbe Lager und dieselbe Kundenanforderung eine offene Lieferung vorhanden ist, werden die neuen Zeilen daran angehängt. Diese Richtlinie kann verwendet werden, wenn der Kunde mehrmals am Tag zusätzliche Bestellpositionen mit derselben Bestellnummer sendet und möchte, dass alle Positionen in einer Lieferung zusammengefasst werden. (Mit anderen Worten, es gibt einen Frachtbrief und einen Packzettel.)

### <a name="create-example-policy-4"></a>Beispielrichtlinie 4 erstellen

In diesem Beispiel erstellen Sie eine *Kunden, die Konsolidierung zulassen*-Richtlinie, die für den folgenden Geschäftsfall verwendet werden kann:

- Die Richtlinie fragt nach einem bestimmten Auftragspool, um Kunden zu identifizieren, die konsolidierte Lieferungen annehmen.
- Die Konsolidierung mit offenen Lieferungen ist deaktiviert.
- Die Konsolidierung erfolgt über Aufträge hinweg unter Verwendung der Felder, die in der Standard-CrossOrder-Richtlinie ausgewählt sind (um das frühere Kontrollkästchen **Lieferung bei Freigabe am Lagerort konsolidieren** zu replizieren).

- Sie können die Regel für einen Kundenauftrag überschreiben, indem Sie einen anderen Auftragspool auswählen.

Führen Sie die folgenden Schritte aus, um die Versandkonsolidierungsrichtlinie für diesen Geschäftsfall zu erstellen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Für Lagerort freigeben \> Richtlinien zur Lieferungskonsolidierung**.
1. Stellen Sie das Feld **Richtlinientyp** auf *Aufträge* ein.
1. Wählen Sie im Aktionsbereich **Neu** aus, um eine Richtlinie mit den folgenden Einstellungen zu erstellen:

    - **Richtlinienname:** *Auftragspool*
    - **Richtlinienbeschreibung:** *Konsolidierung über Aufträge hinweg basierend auf dem Auftragspool*

1. Lassen Sie die **Konsolidierung mit offenen Lieferungen**-Option auf *Nein* gesetzt.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie auf dem Inforegister **Konsolidierungsfelder** in der Liste **Verbleibende Felder** die Zeile aus, in der das Feld **Feldname** auf *Lieferart* gesetzt ist.
1. Wählen Sie die Schaltfläche **Hinzufügen** ![rechter Pfeil](media/forward-button.png) aus, um das Feld in die Liste **Ausgewählte Felder** zu verschieben.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Wählen Sie im Abfrageeditor-Dialogfeld auf der Registerkarte **Bereich** **Hinzufügen** aus, um eine Zeile mit den folgenden Einstellungen zum Raster hinzuzufügen:

    - **Tabelle:** *Aufträge*
    - **Abgeleitete Tabelle:** *Aufträge*
    - **Feld:** *Pool*
    - **Kriterien:** *ShipCons*

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.

> [!NOTE]
> In diesem Geschäftsfall werden alle Auftragspositionen, in denen Kundenaufträge zum selben Auftragspool gehören, zu einer Lieferung über Kundenaufträge hinweg für dasselbe Konto, dasselbe Lager und dieselbe Transportart zusammengefasst. Anstelle des Auftragspools können Sie ein beliebiges anderes Feld verwenden, um eine Kundengruppe zu unterscheiden und standardmäßig den Kundenauftragskopf zu verwenden. Sie können diesen Ansatz verwenden, wenn der Kunde und nicht das Lager den Konsolidierungsbedarf erhöht. (In der früheren Konsolidierungslogik hat das Lager den Konsolidierungsbedarf erhöht.)

### <a name="create-example-policy-5"></a>Beispielrichtlinie 5 erstellen

In diesem Beispiel erstellen Sie eine *Lagerorte, die Konsolidierung zulassen*-Richtlinie, die für den folgenden Geschäftsfall verwendet werden kann:

- Die Richtlinie fragt nach einem bestimmten Auftragspool, um Lagerorte zu identifizieren, die Lieferungen konsolidieren.
- Die Konsolidierung mit offenen Lieferungen ist deaktiviert.
- Die Konsolidierung erfolgt über Aufträge hinweg unter Verwendung der Felder, die in der Standard-CrossOrder-Richtlinie ausgewählt sind (um das frühere Kontrollkästchen **Lieferung bei Freigabe am Lagerort konsolidieren** zu replizieren).

In der Regel kann dieser Geschäftsfall mithilfe der von Ihnen erstellten Standardrichtlinie aus [Richtlinien für erste Sendungskonsolidierung festlegen](#initial-policies) behoben werden. Sie können ähnliche Richtlinien jedoch auch manuell erstellen, indem Sie die folgenden Schritte ausführen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Für Lagerort freigeben \> Richtlinien zur Lieferungskonsolidierung**.
1. Stellen Sie das Feld **Richtlinientyp** auf *Aufträge* ein.
1. Wählen Sie im Aktionsbereich **Neu** aus, um eine Richtlinie mit den folgenden Einstellungen zu erstellen:

    - **Richtlinienname:** *Auftragsübergreifend*
    - **Richtlinienbeschreibung:** *Auftragsübergreifende Konsolidierung für bestimmte Lagerorte*

1. Lassen Sie die **Konsolidierung mit offenen Lieferungen**-Option auf *Nein* gesetzt.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie auf dem Inforegister **Konsolidierungsfelder** im Feld **Verbleibende Felder** die Zeile aus, in der das Feld **Feldname** auf *Lieferart* gesetzt ist.
1. Wählen Sie die Schaltfläche **Hinzufügen** ![rechter Pfeil](media/forward-button.png) aus, um das Feld in die Liste **Ausgewählte Felder** zu verschieben.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Suchen Sie im Abfrageeditor-Dialogfeld auf der Registerkarte **Bereich** die Zeile, in der das Feld **Feld** auf *Lagerorte* gesetzt ist, und stellen Sie das Feld **Kriterien** für diese Zeile auf *61, 63* ein.
1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.

### <a name="set-the-order"></a>Legen Sie die Reihenfolge fest

Nachdem Sie alle Ihre Richtlinien erstellt haben, müssen Sie die Reihenfolge festlegen, in der sie angewendet werden. Befolgen Sie diese Schritte, um einen pyramidenähnlichen Ansatz zu verwenden, bei dem die Richtlinien mit den meisten Bedingungen als mit der höchsten Priorität bewertet werden.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Für Lagerort freigeben \> Richtlinien zur Lieferungskonsolidierung**.
1. Stellen Sie das Feld **Richtlinientyp** auf *Aufträge* ein.
1. Wählen Sie jede Richtlinie aus, die in der linken Spalte aufgeführt ist, und verwenden Sie dann die **Nach oben**- und **Nach unten**-Schaltflächen im Aktionsbereich, um die Richtlinien in der folgenden Reihenfolge anzuordnen:

    1. CustomerMode
    1. Artikeltyp
    1. CustomerOrderNo
    1. Auftragspool
    1. Auftragsübergreifend
    1. Standard

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a> Beispielszenarien für die Verwendung von Richtlinien zur Lieferungskonsolidierung

Die folgenden Szenarien veranschaulichen, wie Sie die Versandkonsolidierungsrichtlinien verwenden können, die Sie beim Lesen dieses Artikels erstellt haben. Jedes Szenarion führt Sie durch einen Lieferungskonsolidierungsprozess, der Lieferungskonsolidierungsrichtlinien bei automatisierter oder manueller Freigabe an das Lager verwendet:

- Szenario 1: [Lieferungen mithilfe der automatischen Auftragsfreigabe konsolidieren, wenn sie im Lager freigegeben werden](../warehousing/consolidate-shipments-automatic.md)
- Szenario 2: [Lieferungen konsolidieren, wenn die Richtlinie zur Lieferungskonsolidierung auf der Seite „Freigabe an Lager“ überschrieben wird](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- Szenario 3: [Lieferungen mithilfe von „An Lager freigeben“ von der Ladungsplanungs-Workbench aus konsolidieren](../warehousing/consolidate-shipments-load-planning-workbench.md)
- Szenario 4: [Lieferungen mithilfe der Workbench zur Lieferungskonsolidierung konsolidieren](../warehousing/consolidate-shipments-manual-workbench.md)
- Szenario 5: [Lieferungen manuell auf der Seite zur Lieferungskonsolidierung konsolidieren](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Übersicht über Richtlinien für die Lieferungskonsolidierung](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
