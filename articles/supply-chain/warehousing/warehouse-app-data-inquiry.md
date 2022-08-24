---
title: Daten mit den Umleitungen der mobilen Warehouse Management-App abfragen
description: In diesem Artikel wird beschrieben, wie Sie die Menüelemente für die Datenabfrage auf Mobilgeräten konfigurieren und als Teil von Umwegen verwenden.
author: perlynne
ms.date: 08/01/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c3ea53379badb3cb2ed71b7f102956d71c3f047a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220539"
---
# <a name="query-data-using-warehouse-management-mobile-app-detours"></a>Daten mit den Umleitungen der mobilen Warehouse Management-App abfragen

[!include [banner](../includes/banner.md)]

## <a name="feature-introduction"></a>Funktionseinführung

Durch die Bereitstellung von Barcode-Scanfunktionen bietet Ihnen die mobile Warehouse Management-App eine einfache und genaue Möglichkeit, Daten im Rahmen Ihrer Lagerprozesse zu erfassen. Strichcodes werden jedoch manchmal beschädigt und unlesbar, oder die erforderlichen Dateninformationen sind möglicherweise nicht als Strichcode in Ihren Geschäftsprozessflüssen vorhanden. In diesen Fällen kann die manuelle Eingabe der Daten lange dauern und sogar dazu führen, dass falsche Daten erfasst werden. Die Folgen können eine verringerte Effektivität und ein niedrigeres Serviceniveau sein.

Durch die Verwendung eines flexiblen Datenabfrageprozesses können Mitarbeiter die erforderlichen Informationen als Teil der eingebetteten mobilen App-Flows für die Lagerverwaltung leicht nachschlagen und Filteroptionen anwenden, sodass nur die relevanten Daten angezeigt werden. Daher ist die manuelle Auswahl schneller und genauer.

Beispielsweise ist im Bestelleingangsablauf eine Bestellnummer erforderlich, um den eingehenden Bestand abzugleichen. Als Teil dieses Prozesses können Sie Menüpunkte einfach konfigurieren, um eine Kartenlistenansicht der relevanten Bestellnummern bereitzustellen. Auf diese Weise können Sie den Empfangsfluss fortsetzen, indem Sie einen schnellen Point-to-Select-Ansatz verwenden. Dieser Artikel enthält Beispielszenarien, aber die Funktionalität kann auch in beliebigen oder allen Flows Ihrer mobilen Warehouse Management-App verwendet werden.

## <a name="turn-on-the-data-inquiry-flow-feature-and-its-prerequisites"></a>Aktivieren Sie die Datenabfrageflow-Funktion und ihre Voraussetzungen

Bevor Sie die in diesem Artikel beschriebene Funktionalität verwenden können, müssen Sie das folgende Verfahren ausführen, um die erforderlichen Features zu aktivieren.

1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Funktionsverwaltung**. (Weitere Informationen zum Arbeitsbereich **Funkionsverwaltung** finden Sie unter [Funktionsverwaltung Übersicht](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Aktivieren Sie die Funktion, die folgendermaßen aufgelistet ist:

    - **Module:** *Lagerortverwaltung*
    - **Name der Funktion:** *Schrittanweisungen für die App "Lager"*

    Diese Funktion ist Voraussetzung für die Funktion *Datenabfrage-Flow in der Warehouse Management-App*. Für weitere Informationen über die Funktion *Schrittanleitung für die Warehouse-App* siehe [Passen Sie Schritttitel und Anweisungen für die mobile Warehouse Management-App an](mobile-app-titles-instructions.md).

1. Aktivieren Sie die Funktion, die folgendermaßen aufgelistet ist:

    - **Module:** *Lagerortverwaltung*
    - **Funktionsname:** *Umwege über die Warehouse Management-App*

    Diese Funktion ist Voraussetzung für die Funktion *Datenabfrage-Flow in der Warehouse Management-App*. Für weitere Informationen über die Funktion *Umleitung für Warehouse Management-App*, siehe [Umleitungen für Schritte in den Menüpunkten des Mobilgeräts konfigurieren](warehouse-app-detours.md).

1. Wie die Funktion *Umleitung für Warehouse Management-App* nicht bereits aktiviert ist, aktualisieren Sie die Feldnamen in der mobilen App für Warehouse Management, indem Sie zu **Lagerverwaltung\> Einstellungen \> Mobiles Gerät \> Feldnamen der Warehouse-App** und wählen **Standard-Setup** erstellen. Wiederholen Sie diesen Schritt für jede juristische Person (Firma), in der Sie die mobile App Warehouse Management verwenden. Weitere Informationen finden Sie unter [Felder für die Warehouse Management Mobile App konfigurieren](configure-app-field-names-priorities-warehouse.md).
1. Aktivieren Sie die Funktion, die folgendermaßen aufgelistet ist:

    - **Module:** *Lagerortverwaltung*
    - **Funktionsname** *Datenabfrage-Flow in der Warehouse Management-App*

    Diese Funktion wird in diesem Artikel beschrieben.

## <a name="example-scenarios"></a>Beispielszenarien

In diesem Artikel wird anhand von Beispielszenarien gezeigt, wie Sie *Datenabfrage-Flow in der Warehouse Management-App* Funktion zur Verbesserung des Kaufbelegflows verwenden können. Die Szenarien verwenden die standardmäßigen Beispieldaten, die den Flow *Einkauf empfangen* enthalten. Dieser Flow beginnt damit, dass die Mitarbeiter aufgefordert werden, eine Bestellnummer zu identifizieren, gegen die sie eine Bestellung erhalten. Um den Mitarbeitern zu helfen, die Bestellung leichter zu identifizieren, erweitern Sie die erste Seite des Flows, indem Sie die folgenden neuen Abfrageoptionen als [Umleitungen](warehouse-app-detours.md) hinzufügen:

- **Suchen Sie Bestellungen nach Kreditor** – Öffnen Sie eine Seite, auf der Mitarbeiter aufgefordert werden, einen Kreditorennamen oder einen Teil eines Kreditorennamens einzugeben. Sie können Platzhalterzeichen verwenden. Wenn beispielsweise eine Arbeitskraft heute eine eingehende Lieferung von einem Kreditor erwartet, der *Tailspin* in seinem Namen enthält, können sie **Tail\*** eingeben, um einen Kartensatz für offene Bestellungen anzuzeigen, die diesen Text enthalten. Jede Karte hat mehrere Felder, die Informationen zu jeder Bestellung liefern. Neben dem Namen des Kreditors können Sie die Karten so gestalten, dass sie die Kontonummer des Kreditors, das Lieferdatum und den Dokumentenstatus anzeigen.
- **Suchen Sie nach POs für heute** – Öffnen Sie eine Seite, die die Mitarbeiter nicht zur Eingabe von Daten auffordert, sondern stattdessen vorkonfigurierte Filter anzeigt (z. B. das heutige Datum). Die Seite zeigt dann eine Reihe von Karten an, die dem Filter entsprechen. Arbeiter fahren fort, indem sie eine Karte für die Bestellung auswählen, für die sie Bestandsartikel registrieren möchten.
- **Suchen Sie Bestellungen nach Artikel** – Öffnen Sie eine Seite, auf der die Mitarbeiter aufgefordert werden, den Strichcode eines beliebigen Artikels im eingetroffenen Bestand zu scannen. Der Flow listet dann alle offenen Bestellungen auf, die Positionen für die gescannte Artikelnummer enthalten. Um Situationen abzudecken, in denen ein Strichcode nicht gelesen werden kann, können Sie dieser Seite eine weitere Umleitungssuche hinzufügen, mit der Mitarbeiter in einer bestimmten Bestellung nach Artikelnummern suchen können.

In jedem Fall identifiziert der Arbeiter eine Bestellung, indem er eine Karte auswählt, und kehrt dann zur ersten Seite zurück, die die ausgewählte Bestellnummer zeigt. Die Arbeitskraft kann dann mit dem Registrierungsablauf für eingehende Bestandsartikel fortfahren.

## <a name="enable-sample-data"></a>Beispieldaten aktivieren

Um das Beispielszenario mithilfe der in diesem Artikel dargestellten Werte zu bearbeiten, müssen Sie auf einem System arbeiten, auf dem die [Standarddemodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind. Außerdem müssen Sie die *USMF* juristische Person (Unternehmen) auswählen, bevor Sie beginnen.

## <a name="configure-the-mobile-device-menu-items"></a>Menüelemente des mobilen Geräts konfigurieren

Um jede der neuen Abfrageoptionen zu erstellen, die Sie der ersten Seite des Flows hinzufügen müssen, müssen Sie sie als Menüelement für mobile Geräte einrichten. Später stellen Sie die Abfragemöglichkeiten als Umwege für den Flow *Einkauf empfangen* zur Verfügung.

### <a name="create-the-look-up-pos-by-vendor-menu-item"></a>Erstellen Sie den Menüpunkt „Bestellungen nach Kreditor suchen“.

Erstellen Sie **Suchen Sie Bestellungen nach Kreditor**, indem Sie diesen Schritten folgen.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Menüpunkt des mobilen Geräts zu erstellen.
1. Legen Sie für das neue Menüelement die folgenden Werte fest:

    - **Menüpunktname** *Bestellungen nach Kreditor suchen*
    - **Titel:** *Suchen Sie Bestellungen nach Kreditor*
    - **Modus:** *Indirekt*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Aktivitätscode:** *Datenabfrage*
    - **Prozessanleitung verwenden:** *Ja* (Dieser Wert wird automatisch ausgewählt.)
    - **Tabellenname:** *PurchTable* (Sie möchten Bestellnummern aus dieser Tabelle nachschlagen.)

1. Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten**, um eine Abfrage zu definieren, die auf der ausgewählten Basistabelle basiert (in diesem Fall die Tabelle mit Bestellungen).
1. Fügen Sie im Abfrage-Editor auf der Registerkarte **Bereich** folgende Positionen dem Raster hinzu:

    | Tabelle | Abgeleitete Tabelle | Feld | Kriterien |
    |---|---|---|---|
    | Bestellungen | Bestellungen | Bestellungsstatus | Offener Auftrag |
    | Bestellungen | Bestellungen | Lieferdatum | (dayRange(-10,10)) |
    | Bestellungen | Bestellungen | Lieferantenname | |

1. Wählen Sie **OK** aus.

    In diesem Beispiel ist das neue Menüelement so konfiguriert, dass offene Bestellungen gefunden werden, die voraussichtlich zwischen 10 Tagen in der Vergangenheit und 10 Tagen in der Zukunft eintreffen.

    In der Abfrage wurde die Spalte **Kriterien** für *Herstellername* leer gelassen. Daher können Arbeiter diesen Wert angeben, während sie die mobile App für Warehouse Management verwenden.

    Wenn Sie festlegen möchten, wie die Liste sortiert werden soll, können Sie die Sortierung auf der Registerkarte **Sortierung** einrichten.

1. Zusätzlich zum Definieren der Abfrage müssen Sie auswählen, welche Felder auf den Karten auf der Abfragelistenseite angezeigt werden. Wählen Sie im Aktionsbereich **Feldliste** aus.
1. Legen Sie auf der Seite **Feldliste** die folgenden Werte fest:

    - **Anzeigefeld 1:** *PurchId* (Dieses Feld wird als Kopfzeile für jede Karte angezeigt.)
    - **Anzeigefeld 2:** *PurchStatus*
    - **Anzeigefeld 3:** *PurchName*
    - **Anzeigefeld 4:** *OrderAccount*
    - **Anzeigefeld 5:** *DeliveryDate*
    - **Anzeigefeld 6:** *displayDocumentStatus()* (Dieser Wert ist eine Anzeigemethode, wie das „()“ am Ende anzeigt.)

1. Wählen Sie im Aktionsbereich **Speichern** aus. Schließen Sie nun die Seite.

### <a name="create-the-look-up-pos-for-today-menu-item"></a>Erstellen Sie den Menüpunkt „Bestellungen für heute suchen“.

Erstellen Sie **Suchen Sie Bestellungen für heute**, indem Sie diesen Schritten folgen.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Menüpunkt des mobilen Geräts zu erstellen.
1. Legen Sie die folgenden Werte für das neue Element fest:

    - **Menüpunktname** *Bestellungen für heute suchen*
    - **Titel:** *Suchen Sie nach POs für heute*
    - **Modus:** *Indirekt*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Aktivitätscode:** *Datenabfrage*
    - **Prozessanleitung verwenden:** *Ja* (Dieser Wert wird automatisch ausgewählt.)
    - **Tabellenname:** *PurchTable* (Sie möchten Bestellnummern aus dieser Tabelle nachschlagen.)

1. Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten**, um eine Abfrage zu definieren, die auf der ausgewählten Basistabelle basiert (in diesem Fall die Tabelle mit Bestellungen).
1. Fügen Sie im Abfrage-Editor auf der Registerkarte **Bereich** folgende Positionen dem Raster hinzu:

    | Tabelle | Abgeleitete Tabelle | Feld | Kriterien |
    |---|---|---|---|
    | Bestellung | Bestellung | Bestellungsstatus | Offener Auftrag |
    | Bestellung | Bestellung | Lieferdatum | (Day(0)) |

1. Wählen Sie **OK** aus.

    In diesem Beispiel ist der neue Menüpunkt so konfiguriert, dass offene Bestellungen gefunden werden, die voraussichtlich heute eintreffen.

    Wenn Sie festlegen möchten, wie die Liste sortiert werden soll, können Sie die Sortierung auf der Registerkarte **Sortierung** einrichten.

1. Zusätzlich zum Definieren der Abfrage müssen Sie auswählen, welche Felder auf den Karten auf der Abfragelistenseite angezeigt werden. Wählen Sie im Aktionsbereich **Feldliste** aus.
1. Legen Sie auf der Seite **Feldliste** die folgenden Werte fest:

    - **Anzeigefeld 1:** *PurchName* (Dieses Feld wird als Kopfzeile für jede Karte angezeigt.)
    - **Anzeigefeld 2:** *PurchId*
    - **Anzeigefeld 3:** *PurchStatus*
    - **Anzeigefeld 4:** *DlvMode*
    - **Anzeigefeld 5:** *DlvTerm*
    - **Anzeigefeld 6:** *OrderAccount*
    - **Anzeigefeld 7:** *VendorName()* (Dieser Wert ist eine Anzeigemethode, wie das "()" am Ende anzeigt.)

1. Wählen Sie im Aktionsbereich **Speichern** aus. Schließen Sie nun die Seite.

### <a name="create-the-look-up-pos-by-item-menu-item"></a>Erstellen Sie den Menüpunkt „Bestellungen nach Artikel suchen“.

Erstellen Sie **Suchen Sie Bestellungen nach Artikel**, indem Sie diesen Schritten folgen.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Menüpunkt des mobilen Geräts zu erstellen.
1. Legen Sie die folgenden Werte für das neue Element fest:

    - **Menüpunktname** *Bestellungen nach Artikel suchen*
    - **Titel:** *Suchen Sie Bestellungen nach Artikel*
    - **Modus:** *Indirekt*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Aktivitätscode:** *Datenabfrage*
    - **Prozessanleitung verwenden:** *Ja* (Dieser Wert wird automatisch ausgewählt.)
    - **Tabellenname:** *PurchLine* (Sie möchten Bestellnummern basierend auf der Artikelnummer über die Positionsdaten nachschlagen.)

1. Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** um eine Abfrage zu definieren, die auf der ausgewählten Basistabelle basiert (in diesem Fall die Bestellpositionstabelle, aber Sie können jeden der Werte verwenden, die sich auf die Kopfzeile beziehen, indem Sie mit der verknüpfen *Einkaufstabelle*).
1. Fügen Sie im Abfrage-Editor auf der Registerkarte **Bereich** folgende Positionen dem Raster hinzu:

    | Tabelle | Abgeleitete Tabelle | Feld | Kriterien |
    |---|---|---|---|
    | Bestellpositionen | Bestellpositionen | Positionsstatus | Offener Auftrag |
    | Bestellpositionen | Bestellpositionen | Lieferdatum | (dayRange(-10,10)) |
    | Bestellpositionen | Bestellpositionen | Artikelnummer | |

1. Wählen Sie **OK** aus.

    In diesem Beispiel ist das neue Menüelement so konfiguriert, dass offene Bestellungspositionen gefunden werden, die voraussichtlich zwischen 10 Tagen in der Vergangenheit und 10 Tagen in der Zukunft eintreffen.

    In der Abfrage wurde die Spalte **Kriterien** für *Artikelnummer* leer gelassen. Daher können Arbeiter diesen Wert angeben, während sie die mobile App für Warehouse Management verwenden.

    Wenn Sie festlegen möchten, wie die Liste sortiert werden soll, können Sie die Sortierung auf der Registerkarte **Sortierung** einrichten.

1. Zusätzlich zum Definieren der Abfrage müssen Sie auswählen, welche Felder auf den Karten auf der Abfragelistenseite angezeigt werden. Wählen Sie im Aktionsbereich **Feldliste** aus.
1. Legen Sie auf der Seite **Feldliste** die folgenden Werte fest:

    - **Anzeigefeld 1:** *PurchId* (Dieser Feldwert wird als Kopfzeile für jede Karte verwendet.)
    - **Anzeigefeld 2:** *VendAccount*
    - **Anzeigefeld 3:** *PurchQty*
    - **Anzeigefeld 4:** *PurchUnit*
    - **Anzeigefeld 5:** *PurchStatus*

1. Wählen Sie im Aktionsbereich **Speichern** aus. Schließen Sie nun die Seite.

## <a name="add-the-new-mobile-device-menu-items-to-a-menu"></a>Hinzufügen der neuen Menüoptionen des mobilen Geräts zu einem Menü

Ihre drei neuen Menüelemente für mobile Geräte können jetzt zum Menü für mobile Geräte hinzugefügt werden. Diese Aufgabe muss abgeschlossen sein, bevor die Menüpunkte im Rahmen eines Umleitungsprozesses verwendet werden können. In diesem Beispiel erstellen Sie ein neues Untermenü und fügen ihm die neuen Menüelemente hinzu.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie in der Kopfzeile des neuen Datensatzes die folgenden Werte fest:

    - **Name:** *Anfragen*
    - **Beschreibung:** *Anfragen*

1. Suchen und wählen Sie im Raster **Verfügbare Menüs und Menüpunkte** den ersten mobilen Menüpunkt aus, den Sie gerade erstellt haben. Wählen Sie die rechte Pfeil-Schaltfläche, um das Element in die Liste **Menüstruktur** zu verschieben.
1. Wiederholen Sie den vorherigen Schritt für die beiden anderen neuen Menüpunkte.
1. Wählen Sie im Listenbereich links das **Hauptmenü**.
1. Scrollen Sie in der Liste **Verfügbare Menüs und Menüpunkte** nach unten zum Abschnitt **Menüs** und wählen Sie Ihr neues Menü **Anfragen** aus. Wählen Sie die rechte Pfeil-Schaltfläche, um das Element in die Liste **Menüstruktur** zu verschieben.

## <a name="configure-detours-in-your-mobile-device-steps"></a>Umleitungen für Ihre Schritte des Mobilgeräts konfigurieren

Um die Einrichtung abzuschließen, müssen Sie nun die Umleitungskonfiguration auf der Seite **Schritte für Mobilgeräte** verwenden, um die drei neuen Menüpunkte für mobile Geräte zum bestehenden Bestellidentifizierungsschritt dem Flow *Einkauf empfangen* hinzuzufügen.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichtung > Mobiles Gerät \> Mobiles Gerät Schritte**.
1. Geben Sie im Feld **Filter** *PONum* ein. Wählen Sie dann *Schritt-ID: "PONum"* in der Dropdown-Liste.
1. Während der gefundene Datensatz im Raster ausgewählt ist, wählen Sie **Schrittkonfiguration hinzufügen** im Aktionsbereich. Verwenden Sie im Dropdown-Dialogfeld das Feld **Menüpunkt** zum Suchen und Auswählen von *Einkauf empfangen*. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.
1. Auf der Detailseite für die neue Schrittkonfiguration (**Einkauf empfangen: PONum**), auf dem Inforegister **Verfügbare Umleitungen (Menüpunkte)** wählen Sie **Hinzufügen** auf der Symbolleiste.
1. Suchen Sie im Dialogfeld **Umleitung hinzufügen** den Menüpunkt **Suchen Sie Bestellungen nach Kreditor** und wählen Sie ihn aus.
1. Wählen Sie **OK**, um das Dialogfeld zu schließen und den ausgewählten Menüpunkt zur Umleitungsliste hinzuzufügen.
1. Wählen Sie die neue Umleitung aus und wählen Sie dann **Wählen Sie die zu sendenden Felder aus** auf der Symbolleiste.
1. Fügen Sie im Dialog **Wählen Sie die zu sendenden Felder aus** nichts dem Abschnitt **Senden von Kauf erhalten** hinzu, da Sie dem Umweg-Menüpunkt keine Werte übergeben möchten. Setzen Sie aber im Abschnitt **Von der Suche nach Bestellungen nach Kreditor zurückbringen** für die dort bereits hinzugefügte leere Zeile folgenden Wert:

    - **Kopieren von Bestellungen nach Kreditor suchen:** *Bestellung*
    - **Einfügen in Einkauf empfangen:** *Bestellung*

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.
1. Wiederholen Sie die Schritte 4 bis 9 für die anderen beiden neuen Menüpunkte (**Suchen Sie nach POs für heute** und **Suchen Sie Bestellungen nach Artikel**). Wie für **Suchen Sie Bestellungen nach Anbieter** möchten Sie auf diesen Umwegen keine Daten senden, sondern eine Bestellnummer zurückgeben.
1. Schließen Sie die Seite.

## <a name="try-a-purchase-receiving-flow-that-has-a-data-inquiry-as-part-of-a-detour"></a>Probieren Sie einen Kaufempfangsflow aus, der eine Datenabfrage als Teil eines Umwegs enthält

Befolgen Sie diese Schritte, um die Einrichtung Ihrer neuen mobilen App zu testen.

1. Erstellen Sie mehrere Bestellungen mit Positionen für Lager 51.
1. Wechseln Sie zu einem mobilen Gerät oder Emulator, auf dem die Warehouse Management Mobile App ausgeführt wird, und melden Sie sich mit der Benutzer-ID *51* und dem Kennwort *1* am Lagerort 51 an.
1. Wählen Sie im Menü der mobilen App **Eingehende** und dann **Einkauf empfangen**.

    Sie sollten die folgende Seite sehen, die die drei neuen Menüpunkte enthält.

    ![Kaufeingang unter Verwendung der Bestellnummer.](media/wma-purchase-receive-po-num-with-detours.png "Kaufeingang unter Verwendung der Bestellnummer")

1. Probieren Sie die verschiedenen Funktionen aus und beachten Sie, dass Sie eine Bestellnummer zurücksenden können, indem Sie eine der Karten in der Liste auswählen.

    ![Kaufeingang mit Bestellsuche nach Lieferant, Beispiel 1.](media/wma-purchase-receive-lookup-po-vendor-keyin-detours.png "Kaufeingang mit Bestellsuche nach Lieferant, Beispiel 1")

    ![Kaufeingang mit Bestellsuche nach Lieferant, Beispiel 2.](media/wma-purchase-receive-lookup-po-vendor-detours.png "Kaufeingang mit Bestellsuche nach Lieferant, Beispiel 2")

> [!TIP]
> Anstatt den empfangenden Flow auszuführen, indem Sie eine Suche in **Kaufeingang** können Sie von einem Abfrageflow aus starten (**Hauptmenü \> Anfragen \> Suchen Sie Bestellungen nach Anbieter**) und rufen Sie einen Umweg auf, um den gewünschten Flow auszuführen, indem Sie eine der Karten in der Liste auswählen. Um diesen Ansatz zu nutzen, können Sie eine Umleitung auf der Seite **Schritte für Mobilgeräte** für den Schritt definieren, der eine **Schritt-ID** von *GenericDataInquiryList* hat. Da es sich bei diesem Flow um einen Umleitungsflow handelt, können Sie keine weiteren Umleitungen daraus aufrufen. Wenn Sie also beispielsweise zur Artikelnummerneingabe gelangen, ist die Suche dort nicht verfügbar, da das System derzeit nur eine Umleitungsebene unterstützt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
