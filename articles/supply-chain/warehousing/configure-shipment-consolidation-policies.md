---
title: Richtlinien zur Lieferungskonsolidierung konfigurieren
description: In diesem Thema wird erläutert, wie Sie Standard- und benutzerdefinierte Versandkonsolidierungsrichtlinien einrichten.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 4df62d7b2c8b0463ca6e9564e167f9060e811a24
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975415"
---
# <a name="configure-shipment-consolidation-policies"></a>Richtlinien zur Lieferungskonsolidierung konfigurieren

[!include [banner](../includes/banner.md)]

Der Lieferungskonsolidierungsprozess, der Richtlinien zur Lieferungskonsolidierung verwendet, ermöglicht eine automatisierte Lieferungskonsolidierung während der automatisierten und manuellen Freigabe an das Lager. Nachdem Sie diese Funktion aktiviert haben, müssen Sie Ihre anfänglichen Richtlinien konfigurieren. Wenn keine Richtlinien konfiguriert sind, generiert jede Verkaufslinie eine separate Lieferung mit einer einzelnen Ladelinie.

Die in diesem Thema vorgestellten Szenarien zeigen, wie Standard- und benutzerdefinierte Versandkonsolidierungsrichtlinien eingerichtet werden.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Richtlinienfunktion zur Lieferungskonsolidierung aktivieren

> [!IMPORTANT]
> Im [ersten Szenario](#scenario-1) dieses Themas wird zunächst ein Lager eingerichtet, sodass die frühere Funktion zur Lieferungskonsolidierung verwendet wird. Anschließend stellen Sie Richtlinien zur Lieferungskonsolidierung zur Verfügung. Auf diese Weise können Sie erfahren, wie das Upgradeszenario funktioniert. Wenn Sie vorhaben, eine Demodatenumgebung zu verwenden, um das erste Szenario zu durchlaufen, aktivieren Sie die Funktion nicht, bevor Sie das Szenario ausführen.

Bevor Sie die Funktion *Richtlinien zur Lieferungskonsolidierung* verwenden können, müssen Sie sie in Ihrem System aktivieren. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Lieferung konsolidieren*

## <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Jedes Szenario in diesem Thema verweist auf Werte und Datensätze, die in den für Microsoft Dynamics 365 Supply Chain Management bereitgestellten Standarddemodaten enthalten sind. Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf **USMF** festlegen, bevor Sie beginnen.

## <a name="scenario-1-configure-default-shipment-consolidation-policies"></a><a name="scenario-1"></a>Szenario 1: Standardrichtlinien zur Lieferungskonsolidierung konfigurieren

Es gibt zwei Situationen, in denen Sie die Mindestanzahl von Standardrichtlinien konfigurieren müssen, nachdem Sie die Funktion *Richtlinien zur Lieferungskonsolidierung* aktiviert haben:

- Sie aktualisieren eine Umgebung, die bereits Daten enthält.
- Sie richten eine völlig neue Umgebung ein.

### <a name="upgrade-an-environment-where-warehouses-are-already-configured-for-cross-order-consolidation"></a>Aktualisieren Sie eine Umgebung, in der Lager bereits für die auftragsübergreifende Konsolidierung konfiguriert sind

Wenn Sie diesen Vorgang starten, sollte die Funktion *Richtlinien zur Lieferungskonsolidierung* deaktiviert werden, um eine Umgebung zu simulieren, in der die grundlegende Funktion zur konsolidierungsübergreifenden Konsolidierung bereits verwendet wurde. Anschließend aktivieren Sie die Funktion mithilfe der Funktionsverwaltung, um zu erfahren, wie Sie nach dem Upgrade Richtlinien für die Lieferungskonsolidierung einrichten.

Befolgen Sie diese Schritte, um Standardrichtlinien für die Lieferungskonsolidierung in einer Umgebung einzurichten, in der Lager bereits für die auftragsübergreifende Konsolidierung konfiguriert wurden.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerorte**.
1. Suchen und öffnen Sie in der Liste den gewünschten Lagerdatensatz (z. B. Lager *24* in den **USMF**-Demodaten).
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Legen Sie auf dem Inforegister **Lagerort** die Option **Lieferung bei Freigabe an Lagerort konsolidieren** auf *Ja* fest.
1. Wiederholen Sie die Schritte 2 bis 4 für alle anderen Lager, in denen eine Konsolidierung erforderlich ist.
1. Schließen Sie die Seite.
1. Verwenden Sie die [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um *Richtlinien zur Lieferungskonsolidierung* zu aktivieren. Im Arbeitsbereich **Funktionsverwaltung** heißt die Funktion *Lieferung konsolidieren*.
1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Für Lagerort freigeben \> Richtlinien zur Lieferungskonsolidierung**. Möglicherweise müssen Sie Ihren Browser aktualisieren, um den neuen Menüpunkt **Richtlinien zur Lieferungskonsolidierung** nach dem Einschalten der Funktion zu sehen.
1. Wählen Sie im Aktionsbereich **Standardeinstellungen erstellen** aus, um die folgenden Richtlinien zu erstellen:

    - Eine **CrossOrder**-Richtlinie für den Richtlinientyp *Aufträge* (vorausgesetzt, Sie haben mindestens einen Lagerort, der für die Verwendung der früheren Konsolidierungsfunktion eingerichtet ist)
    - Eine **Standard**-Richtlinie für den Richtlinientyp *Aufträge*
    - Eine **Standard**-Richtlinie für den Richtlinientyp *Umlagerungsabgang*
    - Eine **CrossOrder**-Richtlinie für den Richtlinientyp *Umlagerungsabgang* (vorausgesetzt, Sie haben mindestens einen Lagerort, der für die Verwendung der früheren Konsolidierungsfunktion eingerichtet ist)

    > [!NOTE]
    > - Beide **CrossOrder**-Richtlinien berücksichtigen denselben Satz von Feldern wie die frühere Logik, mit Ausnahme des Felds für die Bestellnummer. (In diesem Feld werden Linien zu Lieferungen zusammengefasst, basierend auf Faktoren wie Lager, Transportart und Adresse.)
    > - Beide **Standard**-Richtlinien berücksichtigen denselben Satz von Feldern wie die frühere Logik, einschließlich des Felds für die Bestellnummer. (In diesem Feld werden Linien zu Lieferungen zusammengefasst, basierend auf Faktoren wie Auftragsnummer, Lager, Transportart und Adresse.)

1. Wählen Sie die **CrossOrder**-Richtlinie für den Richtlinientyp *Aufträge*, und wählen Sie dann im Aktionsbereich **Abfrage bearbeiten** aus.
1. Beachten Sie im Dialogfeld des Abfrage-Editors, dass Lager, bei denen die Option **Lieferung bei Freigabe an Lagerort konsolidieren** auf *Ja* gesetzt ist, aufgelistet sind. Daher sind sie in der Abfrage enthalten.

### <a name="create-default-policies-for-a-new-environment"></a>Erstellen Sie Standardrichtlinien für eine neue Umgebung

Befolgen Sie diese Schritte, um Standardrichtlinien für die Lieferungskonsolidierung in einer brandneuen Umgebung einzurichten.

1. Verwenden Sie die [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um *Richtlinien zur Lieferungskonsolidierung* zu aktivieren, wenn es noch nicht aktiviert wurde. Im Arbeitsbereich **Funktionsverwaltung** heißt die Funktion *Lieferung konsolidieren*.
1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Für Lagerort freigeben \> Richtlinien zur Lieferungskonsolidierung**.
1. Wählen Sie im Aktionsbereich **Standardeinstellungen erstellen** aus, um die folgenden Richtlinien zu erstellen:

    - Eine **Standard**-Richtlinie für den Richtlinientyp *Aufträge*
    - Eine **Standard**-Richtlinie für den Richtlinientyp *Umlagerungsabgang*

    > [!NOTE]
    > Beide **Standard**-Richtlinien berücksichtigen denselben Satz von Feldern wie die frühere Logik, einschließlich des Felds für die Bestellnummer. (In diesem Feld werden Linien zu Lieferungen zusammengefasst, basierend auf Faktoren wie Auftragsnummer, Lager, Transportart und Adresse.)

## <a name="scenario-2-configure-custom-shipment-consolidation-policies"></a>Szenario 2: Benutzerdefinierte Richtlinien zur Lieferungskonsolidierung konfigurieren

In diesem Szenario wird gezeigt, wie benutzerdefinierte Lieferungskonsolidierungsrichtlinien eingerichtet werden. Benutzerdefinierte Richtlinien können komplexe Geschäftsanforderungen unterstützen, bei denen die Lieferungskonsolidierung von mehreren Bedingungen abhängt. Für jede Beispielrichtlinie später in diesem Szenario ist eine kurze Beschreibung des Geschäftsfalls enthalten. Diese Beispielrichtlinien sollten in einer Reihenfolge eingerichtet werden, die eine pyramidenartige Auswertung der Abfragen gewährleistet. (Mit anderen Worten, die Richtlinien mit den meisten Bedingungen sollten als mit der höchsten Priorität bewertet werden.)

### <a name="turn-on-the-feature-and-prepare-master-data-for-this-scenario"></a>Aktivieren Sie die Funktion und bereiten Sie Stammdaten für dieses Szenario vor

Bevor Sie die Übungen in diesem Szenario ausführen können, müssen Sie die Funktion aktivieren und die Stammdaten vorbereiten, die für die Filterung erforderlich sind, wie in den folgenden Unterabschnitten beschrieben. (Diese Voraussetzungen gelten auch für die in [Beispielszenarien für die Verwendung von Richtlinien zur Lieferungskonsolidierung](#example-scenarios) aufgeführten Szenarien.)

#### <a name="turn-on-the-feature-and-create-the-default-policies"></a>Aktivieren Sie die Funktion und erstellen Sie die Standardrichtlinien

Verwenden Sie die Funktionsverwaltung, um die Funktion zu aktivieren, falls Sie sie noch nicht aktiviert haben, und erstellen Sie die Standardkonsolidierungsrichtlinien, die in [Szenario 1](#scenario-1) beschrieben sind.

#### <a name="create-two-new-product-filter-codes"></a>Erstellen Sie zwei neue Produktfiltercodes

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \>Produktfilter \> Produktfilter** und fügen Sie zwei Produktfilter hinzu:

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
1. Schaltfläche **Hinzufügen** auswählen ![Pfeil nach rechts](media/forward-button.png), um das Feld in die Liste **Ausgewählte Felder** zu verschieben.
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
1. Schaltfläche **Hinzufügen** auswählen ![Pfeil nach rechts](media/forward-button.png), um das Feld in die Liste **Ausgewählte Felder** zu verschieben.
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
1. Schaltfläche **Hinzufügen** auswählen ![Pfeil nach rechts](media/forward-button.png), um das Feld in die Liste **Ausgewählte Felder** zu verschieben.
1. Wählen Sie in der Liste **Verbleibende Felder** die Zeile aus, in der das Feld **Feldname** auf *Lieferart* gesetzt ist.
1. Schaltfläche **Hinzufügen** auswählen ![Pfeil nach rechts](media/forward-button.png), um das Feld in die Liste **Ausgewählte Felder** zu verschieben.
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
1. Schaltfläche **Hinzufügen** auswählen ![Pfeil nach rechts](media/forward-button.png), um das Feld in die Liste **Ausgewählte Felder** zu verschieben.
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

In der Regel kann dieser Geschäftsfall mithilfe der von Ihnen erstellten Standardrichtlinie aus [Szenario 1](#scenario-1) behoben werden. Sie können ähnliche Richtlinien jedoch auch manuell erstellen, indem Sie die folgenden Schritte ausführen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Für Lagerort freigeben \> Richtlinien zur Lieferungskonsolidierung**.
1. Stellen Sie das Feld **Richtlinientyp** auf *Aufträge* ein.
1. Wählen Sie im Aktionsbereich **Neu** aus, um eine Richtlinie mit den folgenden Einstellungen zu erstellen:

    - **Richtlinienname:** *Auftragsübergreifend*
    - **Richtlinienbeschreibung:** *Auftragsübergreifende Konsolidierung für bestimmte Lagerorte*

1. Lassen Sie die **Konsolidierung mit offenen Lieferungen**-Option auf *Nein* gesetzt.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie auf dem Inforegister **Konsolidierungsfelder** im Feld **Verbleibende Felder** die Zeile aus, in der das Feld **Feldname** auf *Lieferart* gesetzt ist.
1. Schaltfläche **Hinzufügen** auswählen ![Pfeil nach rechts](media/forward-button.png), um das Feld in die Liste **Ausgewählte Felder** zu verschieben.
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

Die folgenden Szenarien veranschaulichen, wie Sie die Versandkonsolidierungsrichtlinien verwenden können, die Sie beim Lesen dieses Themas erstellt haben. Jedes Szenarion führt Sie durch einen Lieferungskonsolidierungsprozess, der Lieferungskonsolidierungsrichtlinien bei automatisierter oder manueller Freigabe an das Lager verwendet:

- Szenario 1: [Lieferungen mithilfe der automatischen Auftragsfreigabe konsolidieren, wenn sie im Lager freigegeben werden](../warehousing/consolidate-shipments-automatic.md)
- Szenario 2: [Lieferungen konsolidieren, wenn die Richtlinie zur Lieferungskonsolidierung auf der Seite „Freigabe an Lager“ überschrieben wird](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- Szenario 3: [Lieferungen mithilfe von „An Lager freigeben“ von der Ladungsplanungs-Workbench aus konsolidieren](../warehousing/consolidate-shipments-load-planning-workbench.md)
- Szenario 4: [Lieferungen mithilfe der Workbench zur Lieferungskonsolidierung konsolidieren](../warehousing/consolidate-shipments-manual-workbench.md)
- Szenario 5: [Lieferungen manuell auf der Seite zur Lieferungskonsolidierung konsolidieren](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Lieferungskonsolidierungsrichtlinien](about-shipment-consolidation-policies.md)
