---
title: Artikelkonsolidierung – Auslastung von Lagerplatz
description: Dieses Thema enthält Informationen zu Funktionen, mit denen Lagerverwalter die volumetrische Auslastung von Standorten im gesamten Lager problemlos anzeigen und filtern können. Manager können direkt auf der Seite „Positionskonsolidierung“ Standorte auswählen und Lagerumlagerungsarbeiten erstellen, um Artikel zu konsolidieren und so den Lagerraum besser zu nutzen.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a328b20c1cfb2fc376ab4656c64cf585a5aa015
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429028"
---
# <a name="item-consolidation---location-utilization"></a>Artikelkonsolidierung – Auslastung von Lagerplatz

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zu Funktionen, mit denen Lagerverwalter die volumetrische Auslastung von Standorten im gesamten Lager problemlos anzeigen und filtern können. Manager können direkt auf der Seite **Positionskonsolidierung** Standorte auswählen und Lagerumlagerungsarbeiten erstellen, um Artikel zu konsolidieren und so den Lagerraum besser zu nutzen.

## <a name="turn-on-the-features"></a>Aktivieren der Funktionen

Bevor Sie die in diesem Thema beschriebenen Funktionen verwenden können, müssen Sie sie in Ihrem System aktivieren. Administratoren können im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktionen überprüfen und sie gegebenenfalls aktivieren. Aktivieren Sie beide folgenden Funktionen in der Reihenfolge, in der sie aufgeführt sind. (Beide Funktionen sind für das Modul **Lagerortverwaltung** vorgesehen.)

1. Status des Lagerplatzes an einem Lagerort
2. Nutzung von Lagerplatz für Positionskonsolidierung

## <a name="warehouse-location-status"></a>Status des Lagerplatzes an einem Lagerort

Mit der Funktion *Status des Lagerplatzes an einem Lagerort* werden der Seite **Lagerplätze** vier neue Felder hinzugefügt, um zusätzliche Informationen zum aktuellen Status des Standorts zu verfolgen:

- **Artikelnummer** – Der Artikel, der sich derzeit am Lagerplatz befindet. Wenn der Lagerplatz mehrere Artikel enthält, ist dieses Feld leer.
- **Datum und Uhrzeit der letzten Aktivität** – Der Zeitstempel der letzten Lagertransaktion, die für den Lagerplatz ausgeführt wurde.
- **Fälligkeitsdatum** – Das Datum, an dem der Bestand am Lagerplatz in den Lagerort gebracht wurde. Dieses Datum wird anhand des Fälligkeitsdatums des Kennzeichens berechnet. Obwohl dieses Datum für Lagerplätze, die mit einem Kennzeichen versehen sind, genau ist, gilt dies möglicherweise nicht für Lagerplätze, die nicht mit einem Kennzeichen versehen sind.
- **Lagerplatzstatus** – Der Status des Lagerplatzes. Vier Werte sind verfügbar:

    - **Unbestimmt** – Das Lagerplatzprofil verfolgt den Status nicht nach. Daher ist der aktuelle Status unbekannt.
    - **Leer** – Derzeit befindet sich kein Bestand am Lagerplatz.
    - **Kommissionierung** – Ausgehende Transaktionen wurden für den Lagerplatz ausgeführt, nachdem er zuletzt leer war.
    - **Lager** – Nur eingehende Transaktionen wurden ausgeführt, da der Lagerplatz zuletzt leer war.

In diesen Feldern erhalten Lagerverwalter einen besseren Überblick über den Status der Lagerplätze am Lagerort. Sie ermöglichen auch erweiterte Berichterstellung und Filterung.

## <a name="set-up-item-consolidation-and-location-utilization"></a>Einrichten von Artikelkonsolidierung und Auslastung von Lagerplatz

In diesem Abschnitt wird beschrieben, wie Sie Ihr System auf die Verwendung der Artikelkonsolidierung und Auslastung von Lagerplatz vorbereiten. Die Verfahren verwenden Beispielwerte aus den Standarddemodaten. Wenn Sie das Beispielszenario durcharbeiten möchten, das später in diesem Thema bereitgestellt wird, wählen Sie die juristische Person **USMF** aus (die die Standarddemodaten enthält) und erstellen Sie jeden Datensatz, der in diesem Abschnitt beschrieben wird. Wenn Sie das Beispielszenario nicht durcharbeiten möchten, können die hier angegebenen Werte als Beispiele für die Einrichtungstypen betrachtet werden, die Sie zur Verwendung der Funktionen ausführen müssen.

### <a name="released-product"></a>Freigegebenes Produkt

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie im Feld **Artikelnummer** die Option *M9201* aus und öffnen Sie die Detailseite.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Lagerort** **Physische Dimensionen** aus.
1. Wählen Sie auf der Seite **Physische Dimensionen** im Aktivitätsbereich **Neu** aus.

    Dem Raster wird eine neue Zeile hinzugefügt. Das Feld **Artikelnummer** ist voreingestellt.

1. Wählen Sie im Feld **Einheit** die Option *ea* aus. Die verbleibenden Felder in der Zeile werden automatisch festgelegt.
1. Klicken Sie auf **Speichern** und schließen Sie die Seite.

### <a name="location-profile"></a>Lagerortprofil

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.
1. Wählen Sie in der Liste der Lagerplatzprofile **BODEN-05** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Stellen Sie im Inforegister **Allgemeines** sicher, dass beide folgenden Optionen auf *Ja* eingestellt sind:

    - Artikel am Lagerplatz aktivieren
    - Lagerplatzstatus aktivieren

1. Wählen Sie **Speichern** aus.

    > [!IMPORTANT]
    > Wenn die Optionen **Artikel an Lagerplatz aktivieren** und **Lagerplatzstatus aktivieren** bereits auf *Ja*  eingestellt, fahren Sie mit den Anweisungen zum Einrichten des Inforegisters **Dimensionen** in Schritt 10 fort. Wenn die Optionen nicht bereits auf *Ja* eingestellt waren, müssen Sie eine Konsistenzprüfung für das Modul **Lagerortverwaltung** durchführen, nachdem Sie sie manuell eingestellt haben. Fahren Sie in diesem Fall mit dem nächsten Schritt fort.

1. Um die Konsistenzprüfung durchzuführen, gehen Sie zu **Systemadministration \> Periodische Aufgaben \> Datenbank \> Konsistenzprüfung**.
1. Legen Sie im Dialogfeld **Konsistenzprüfung** die folgenden Werte fest:

    - **Module:** *Lagerortverwaltung*
    - **Überprüfen/Beheben:** *Überprüfen*
    - **Startdatum:** Lassen Sie dieses Feld leer.
    - **Konsistenzprüfung des Status des Lagerplatzes an einem Lagerort:** Aktivieren Sie dieses Kontrollkästchen.

1. Wählen Sie **OK**.

    > [!TIP]
    > Sie erhalten eine Benachrichtigung, wenn die Konsistenzprüfung abgeschlossen ist. Öffnen Sie das [Aktionszentrum](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications), um die Nachricht anzuzeigen. Wählen Sie **Meldungsdetails**, um die Details anzuzeigen.
    >
    > Wenn die Meldung für die Konsistenzprüfung „Falsche Standortstatusinformationen für Standort XXXX in Lagerort XX gefunden“ lautet, müssen Sie die Konsistenzprüfung erneut ausführen. Stellen Sie diesmal das Feld **Überprüfen/Beheben** auf *Fehler beheben* ein. Zeigen Sie die Nachrichten an, um sicherzustellen, dass keine Fehler gefunden wurden.

1. Sie müssen nun die Einrichtung des Lagerplatzprofils abschließen. Gehen Sie zurück zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplatzprofile**, wählen Sie das Lagerplatzprofil **BODEN-05** und dann im Aktionsbereich die Option **Bearbeiten** aus.
1. Legen Sie im Inforegister **Dimensionen** die folgenden Werte fest:

    - **Volumennutzung in Prozent:** *100*
    - **Volumetrische Methode für den Lagerort-Standort:** *Lagerplatzvolumen verwenden*
    - **Tatsächliche Höhe des Lagerplatzes:** *10*
    - **Tatsächliche Breite des Lagerplatzes:** *10*
    - **Tatsächliche Tiefe des Lagerplatzes:** *10*
    - **Höchstgewicht:** *100*

1. Wählen Sie **Speichern** aus.

### <a name="mobile-device-menu-items"></a>Menüelemente des mobilen Geräts

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um einen Menüpunkt zum Sortieren zu erstellen.
1. Legen Sie im Header die folgenden Werte fest:

    - **Name des Menüelements:** *Anpassen in*
    - **Titel:** *Anpassen in*
    - **Modus:** *Arbeit*
    - **Vorhandene Arbeit verwenden:** *Nein*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Arbeitserstellungsprozess:** *Anpassung in*
    - **Lagerregulierungstypen:** *Anpassen in*

1. Wählen Sie **Speichern** aus.

### <a name="mobile-device-menu"></a>Menü für mobiles Gerät

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.
1. Wählen Sie in der Liste der Menüs **Lager** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Suchen und wählen Sie in der Liste **Verfügbare Menüs und Menüpunkte** den Menüpunkt **Anpassen in** aus.
1. Wählen Sie die rechte Pfeiltaste, um **Anpassen in** zur Liste **Menüstruktur** zu verschieben. Auf diese Weise fügen Sie dem ausgewählten Menü den neuen Menüpunkt hinzu.
1. Wählen Sie **Speichern** aus.

### <a name="movement-types"></a>Bewegungstypen

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Bestand \> Bewegungstypen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, und legen Sie dann die folgenden Werte fest:

    - **Bewegungstypcode:** *KONSOLIDIEREN*
    - **Beschreibung:** *Lagerplätze konsolidieren*
    - **Arbeitsklassen-ID:** *InvMov*

1. Wählen Sie **Speichern** aus.

## <a name="example-scenario"></a>Beispielszenario

Im folgenden Szenario wird die Lagerort-App auf einem mobilen Gerät verwendet, um eine Bestandsaufnahme *Anpassung in* an zwei Standorten im Lagerort durchzuführen.

### <a name="add-inventory-to-locations"></a>Lagerbestand zu Lagerplätzen hinzufügen

1. Melden Sie sich beim mobilen Gerät als Benutzer an, der für den Lagerort *51* eingerichtet ist.
1. Gehen Sie zu **Bestand \> Anpassen in**.

    Sie geben nun die erste Lagerplatzanpassung ein.

1. Wählen Sie in der Aufgabe **Anpassung in** den Ort aus, für den die Bestandsanpassung vorgenommen werden soll. Wählen Sie im Feld **LOC** *LP-001*.
1. Bestätigen Sie den Lagerplatz
1. Erstellen Sie eine Kennzeichen-ID für den Artikel, der dem Lagerplatz hinzugefügt wird. Im Feld **LP** geben Sie *LP00101* ein.
1. Bestätigen Sie das Kennzeichen.
1. Geben Sie den Artikel ein, der dem Kennzeichen hinzugefügt werden soll. Im Feld **ITEM** geben Sie *M9201* ein.
1. Bestätigen Sie den Artikel.
1. Geben Sie die Menge des Artikels ein, der dem Kennzeichen hinzugefügt werden soll. Geben Sie im Feld **QTY** den Wert *10* ein.
1. Bestätigen Sie die Menge.

    Sie erhalten die Nachricht „Arbeit abgeschlossen“. Sie geben nun die zweite Lagerplatzanpassung ein.

1. Wählen Sie in der Aufgabe **Anpassung in** den Ort aus, für den die Bestandsanpassung vorgenommen werden soll. Wählen Sie im Feld **LOC** *LP-002*.
1. Bestätigen des Lagerplatzes
1. Erstellen Sie eine Kennzeichen-ID für den Artikel, der dem Lagerplatz hinzugefügt wird. Im Feld **LP** geben Sie *LP00201* ein.
1. Bestätigen Sie das Kennzeichen.
1. Geben Sie den Artikel ein, der dem Kennzeichen hinzugefügt werden soll. Im Feld **ITEM** geben Sie *M9201* ein.
1. Bestätigen Sie den Artikel.
1. Geben Sie die Menge des Artikels ein, der dem Kennzeichen hinzugefügt werden soll. Geben Sie im Feld **QTY** den Wert *15* ein.
1. Bestätigen Sie die Menge.

    Sie erhalten die Nachricht „Arbeit abgeschlossen“.

1. Wählen Sie die Menüschaltfläche (manchmal auch als Hamburger oder Hamburgerschaltfläche bezeichnet) und dann **Abbrechen** aus, um die Aufgabe **Anpassung in** zu beenden.

### <a name="consolidate-locations"></a>Lagerplätze konsolidieren

1. Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Artikelkonsolidierung**.
1. Wählen Sie in der Kopfzeile ein Lager aus, für das die Konsolidierung durchgeführt werden soll. Im Feld **Lagerort** geben Sie *51* ein.

    Für jeden Ort, an dem der Artikel *M9201* angepasst wurde, wird ein Datensatz angezeigt. In der Spalte **Nutzung in Prozent** wird die volumetrische Auslastung jedes Lagerplatzes angezeigt.

1. Um den Bestand zu konsolidieren, wählen Sie alle Lagerplätze aus, die konsolidiert werden müssen, und wählen Sie dann im Aktionsbereich die Option **Bestand konsolidieren**.
1. Geben Sie im Dialogfeld **Bestand konsolidieren** den Lagerplatz und den Bewegungstyp an, die zum Erstellen der Arbeit für die Lagerumlagerung verwendet werden sollen. Legen Sie die folgenden Werte fest:

    - **Lagerplatz:** *LP-001*
    - **Bewegungstypcode:** *KONSOLIDIEREN*

1. Wählen Sie **OK**.
1. Sie erhalten eine Informationsnachricht, die die erstellte Umlagerungsarbeit zeigt. Notieren Sie die Umlagerungsarbeits-ID.

### <a name="view-movement-work"></a>Umlagerungsarbeit anzeigen

1. Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.
1. Zeigen Sie die erstellte Arbeit an. Verwenden Sie die Umlagerungsarbeits-ID aus der Bestandskonsolidierung, um das Arbeitsraster zu filtern oder zu durchsuchen.

    In diesem Szenario wurde ein vorhandener Lagerplatz mit Bestand als Standort für die Bestandskonsolidierung verwendet. Daher wurde nur eine Arbeits-ID erstellt.

    > [!NOTE]
   > Das System erstellt eine Arbeits-ID für jede Bewegung, die abgeschlossen werden muss. Wenn Sie einen Lagerplatz angeben, der bereits Bestand enthält, wird nur eine Arbeits-ID erstellt. Wenn Sie einen neuen Lagerplatz angeben, werden zwei Arbeits-IDs erstellt.
