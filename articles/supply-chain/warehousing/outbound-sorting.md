---
title: Ausgangssortierung
description: Dieser Artikel enthält Informationen über ausgehende Sortierung. Diese Funktion erleichtert die Handhabung kleiner Container und hilft Lagerarbeitern, die Palettenkapazität im LKW besser zu planen und zu organisieren.
author: Mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: ec7bc573329a0f8a37b2fd17dcb998ec161b04e8
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336334"
---
# <a name="outbound-sorting"></a>Ausgangssortierung

[!include [banner](../includes/banner.md)]

Diese Funktion erleichtert die Handhabung kleiner Container und hilft Lagerarbeitern, die Palettenkapazität im LKW besser zu planen und zu organisieren. Wenn Sie die Ausgangssortierung verwenden, können Sie verpackte Container auf der richtigen Palette sortieren, nachdem sie an einer Verpackungsstation waren. Sie können auch eine Packungshierarchie erstellen.

Mit dieser Funktion können Sie Paletten aus Containern erstellen, die über die Verpackungsfunktion verpackt sind. Der Container wird nicht an den endgültigen Versandort gesendet, da er sich im ursprünglichen Verpackungsflow befindet. Stattdessen können Mitarbeiter den Container schließen und an einen Lagerplatz für Sortiertypen verschieben. Sie können dann Container nach Positionen sortieren, von denen jede ein Kennzeichen (LP) hat. Nachdem die Container sortiert wurden, kann eine Arbeit erstellt werden, um das gesamte LP basierend auf den Standortanweisungen oder Ihren eigenen Anforderungen an das endgültige Versanddock oder die endgültigen Bühnenstandorte zu senden. Darüber hinaus kann durch das Schließen der Sortierposition den Bestand sofort an den endgültigen Versandort verschoben und in die Bestellung aufgenommen werden.

## <a name="turn-on-the-outbound-sorting-feature"></a>Aktivieren der Funktion „Ausgangssortierung“

Bevor Sie die Funktion nutzen können, muss sie für Ihr System aktiviert werden. Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Ausgangssortierung*

## <a name="setup"></a>Einstellung

Für dieses Szenario müssen Sie standardmäßige **USMF**-Demodaten und Lager *62* verwenden. Sie müssen auch die in den folgenden Unterabschnitten beschriebenen Einstellungen durchführen.

### <a name="set-up-a-wave-template"></a>Richten Sie eine Wellenvorlage ein

Durch diese Einstellungen wird die Welle automatisch verarbeitet und Arbeit erstellt, wenn eine Position an den Lagerort freigegeben wird.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.
1. Wählen Sie in der Vorlagenliste **Lagerort 62**.
1. Stellen Sie im Inforegister **Allgemein** sicher, dass die Option **Welle bei Freigabe für Lagerort verarbeiten** auf *Ja* eingestellt ist.

### <a name="set-up-a-worker"></a>Einrichten einer Arbeitskraft

Die Verpackungsstation gilt als Lagerplatz. Lagerarbeiter, die sich an der Verpackungsstation anmelden, sehen und bearbeiten nur Sendungen und Container, die an diesem bestimmten Verpackungsort geplant sind. Ein Benutzer, der sich bei Microsoft Dynamics 365 anmeldet, muss als Arbeitskraft in der Lagerortverwaltung eingerichtet sein. Wenn der Name des Benutzers nicht in der Liste der Arbeitsbenutzer angezeigt wird, fügen Sie ihn wie folgt hinzu.

> [!NOTE]
> Diese Schritte setzen voraus, dass der Benutzer bereits im System vorhanden ist und als Mitarbeiter oder Arbeitskraft im Modul **Personalverwaltung** zugeordnet wurde.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeitskraft**.
1. Wählen Sie **Neu** aus.
1. Wählen Sie im Feld **Arbeitskraft** den Zielbenutzer in der Liste der Mitarbeiter aus.
1. Wählen Sie **Auswählen**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Inforegister **Benutzer** **Neu** aus, um ein Konto für mobile Geräte zu erstellen und die folgenden Werte dafür festzulegen:

    - **Benutzer-ID:** Geben Sie eine eindeutige ID ein.
    - **Benutzername:** Geben Sie einen Namen für die ID ein.
    - **Standardlagerort:** *62*
    - **Menüname:** *Hauptseite*

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Das Dialogfeld **Passwort festlegen** wird angezeigt, in dem Sie ein einfaches Kennwort erstellen können, mit dem sich der Benutzer bei der mobilen App anmelden kann. Legen Sie die folgenden Werte fest:

    - **Passwort:** Geben Sie ein einfaches Passwort ein.
    - **Passwort bestätigen:** Geben Sie das gleiche Passwort erneut ein.

1. **Kennwortzurücksetzung** auswählen.

    Eine Benachrichtigung im Aktionszentrum informiert Sie darüber, dass das Kennwort für den von Ihnen erstellten Benutzer festgelegt wurde.

### <a name="create-a-location-type"></a>Erstellen eines Lagerplatztyps

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplatztypen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Lagerplatztyp zu erstellen und die folgenden Werte dafür festzulegen:

    - **Lagerplatztyp:** *SORT*
    - **Beschreibung:** *Sortieren*

1. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="set-up-warehouse-management-parameters"></a>Parameter für Lagerortverwaltung einrichten

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.
1. Legen Sie im Registerkarte **Allgemein** im Inforegister **Lagerplatztypen** das Feld **Lagerplatztyp für Sortierung** auf *SORT* fest.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="set-up-a-location-profile"></a>Lagerplatzprofil einrichten

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Header die folgenden Werte fest:

    - **Lagerortprofilkennung:** *Sortierung*
    - **Name:** *Sortierung*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Lagerplatzformat:** *ASRB* (Gang-Regal-Regalboden-Lagerfach)
    - **Lagerplatztyp:** *SORT*
    - **Kennzeichenverfolgung verwenden:** *Ja*
    - **Gemischte Artikel zulassen:** *Ja* (Wenn Sie diese Option auf *Ja* setzen, wird die Option **Gemischte Bestandchargenoption zulassen** automatisch auf *Ja* gesetzt und kann nicht unabhängig geändert werden.)

1. Wählen Sie **Speichern** aus.

### <a name="set-up-a-location"></a>Lagerplatz einrichten

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplätze**.
1. Löschen Sie in der Kopfzeile das Kontrollkästchen **Prüfziffern für den Lagerplatz erstellen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Lagerplatz zu erstellen und die folgenden Werte dafür festzulegen:

    - **Lagerort:** *62*
    - **Lagerplatz:** *SORT*
    - **Lagerortprofilkennung:** *SORTING*

1. Wählen Sie **Speichern** aus.

### <a name="set-up-an-outbound-sorting-template"></a>Einrichten einer Vorlage für die Ausgangssortierung

Die Vorlage für die Ausgangssortierung bestimmt, ob die Arbeit außerhalb des Sortierorts erstellt wird und ob die Sortierung manuell oder automatisch erfolgt.

In diesem Szenario erstellen Sie eine Vorlage für die Ausgangssortierung, um Paletten nach der Verpackungsstation zu erstellen.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Verpackung \> Vorlage für die Ausgangssortierung**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie in der Kopfzeile der neuen Vorlage die folgenden Werte fest:

    - **ID der Vorlage für die Ausgangssortierung:** *AutoWork*
    - **Beschreibung:** *Automatische Arbeitserstellung*
    - **Vorlagentyp für Ausgangssortierung:** *Container*
    - **Lagerort:** *62*
    - **Lagerplatz:** *SORT*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Sortierbestätigung:** *Positionsscan*
    - **Arbeit bei Schließen der Position erstellen:** *Ja*

        Wenn diese Option auf *Ja* eingestellt ist, wird Arbeit erstellt, wenn die Position geschlossen wird, um den Bestand zum endgültigen Versandlagerplatz umzulagern. Ist sie auf *Nein* festgelegt, wird Lagerbestand sofort für den Auftrag entnommen, wenn die Position geschlossen wird.

    - **Positionszuweisung:** *Automatisch*

        Ist dieses Feld auf *Manuell* eingestellt, muss der Benutzer immer angeben, in welche Position der Bestand sortiert werden soll. Ist es auf *Automatisch* eingestellt, leitet das System automatisch den Bestand an eine Position, sofern möglich, basierend auf den Sortiervorlagenunterbrechungen.

1. Wählen Sie **Speichern** aus, um die Schaltfläche **Abfrage bearbeiten** im Aktivitätsbereich verfügbar zu machen.
1. Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** aus
1. Fügen Sie im Abfrage-Editor auf der Registerkarte **Sortieren** eine Position mit den folgenden Werten ein:

    - **Tabelle:** *Lieferungen*
    - **Abgeleitete Tabelle:** *Lieferungen*
    - **Feld:** *Spediteur*

        Wenn Sie diesen Wert ausgewählt haben, wird möglicherweise die folgende Meldung angezeigt: „Das Spediteur-Feld ist kein Indexfeld. Möchten Sie eine Sortierung hinzufügen?“ Wählen Sie **Ja** aus.

    - **Suchrichtigung:** *Aufsteigend*

1. Wählen Sie **OK**.
1. Möglicherweise erhalten Sie die folgende Meldung: „Gruppierung wird zurückgesetzt, fortfahren?“ Wählen Sie **Ja** aus.

    Die Schaltfläche **Vorlagenunterbrechungen für Ausgangssortierung** im Aktivitätsbereich wird verfügbar.

1. Wählen Sie im Aktivitätsbereich **Vorlagenunterbrechungen für Ausgangssortierung**.
1. Legen Sie im Dialogfeld **Ausgehende Sortierkriterien** die folgenden Werte fest:

    - **Name der Referenztabelle:** *Lieferungen*
    - **Name des Referenzfelds:** *Spediteur*
    - **Gruppieren nach Feld:** Aktivieren Sie dieses Kontrollkästchen, um Sendungen nach Spedition zu gruppieren.

1. Wählen Sie **OK**, um Ihre Einstellungen zu speichern und das Dialogfeld zu schließen.

### <a name="set-up-container-packing-policies"></a>Einrichten von Containerverpackungsrichtlinien

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Container \> Containerverpackungsrichtlinien**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie in der Kopfzeile der neuen Richtlinie die folgenden Werte fest:

    - **Containerverpackungsrichtlinien:** *Sortieren*
    - **Beschreibung:** *Sortieren*

1. Legen Sie im Inforegister **Übersicht** die folgenden Werte fest:

    - **Lagerort:** *62*
    - **Standardlagerplatz für die Sortierung:** *SORT*
    - **Gewichtseinheit:** *kg*
    - **Richtlinie zum Containerabschluss:** *Automatische Freigabe*
    - **Richtlinie zur Containerfreigabe:** *Container der ausgehenden Sortierposition zuweisen*

1. Wählen Sie **Speichern** aus.

### <a name="set-up-packing-profiles"></a>Richten Sie Verpackungsprofile ein

Erstellen Sie ein neues Verpackungsprofil, das zusammen mit der Sortierfunktion verwendet wird.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Verpackung \> Verpackungsprofile**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Position zu erstellen und die folgenden Werte dafür festzulegen:

    - **Verpackungsprofilkennung:** *Sortieren*
    - **Beschreibung:** *Sortieren*
    - **Containerverpackungsrichtlinien:** *Sortieren*
    - **Containerkennungsmodus:** *Auto*
    - **Containertyp:** *Box-Groß*
    - **Container beim Schließen des Containers automatisch erstellen:** Gelöscht (= *Nein*)

1. Wählen Sie **Speichern** aus.

### <a name="set-up-work-classes"></a>Arbeitsklassen einrichten

Richten Sie eine Arbeitsklasse ein, die zusammen mit dem Sortieren verwendet wird.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsklassen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Arbeitsklasse zum Sortieren zu erstellen und die folgenden Werte dafür festzulegen:

    - **Arbeitsklassen-ID:** *Sortieren*
    - **Beschreibung:** *Sortieren*
    - **Arbeitsauftragstyp:** *Sortierte Bestandsentnahme*

1. Wählen Sie **Speichern** aus.

### <a name="set-up-mobile-device-menu-items"></a>Menüpunkte für mobiles Gerät einrichten

#### <a name="set-up-a-new-pallet-menu-item"></a>Menüpunkt für neue Palette einrichten

Erstellen Sie einen Menüpunkt für mobile Geräte, um Paletten während des Sortierens zu erstellen.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Header die folgenden Werte fest:

    - **Name des Menüelements:** *Palettenerstellung*
    - **Titel:** *Palettenerstellung*
    - **Modus:** *Indirekt*
    - **Vorhandene Arbeit verwenden:** *Nein*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Aktivitätscode:** *Ausgangssortierung*

        Wenn dieses Feld auf *Ausgangssortierung* eingestellt ist, wird das Feld **ID der Vorlage für die Ausgangssortierung** angezeigt.

    - **Prozessleitfaden verwenden:** *Ja*

        Wenn das Feld **Aktivitätscode** auf *Ausgangssortierung* festgelegt ist, wird diese Option automatisch auf *Ja* gesetzt.

    - **ID der Vorlage für die Ausgangssortierung:** *AutoWork*

1. Wählen Sie **Speichern** aus.

#### <a name="set-up-a-new-loading-menu-item"></a>Menüpunkt für neue Ladung einrichten

Erstellen Sie als Nächstes ein Menüelement, mit dem Benutzer die sortierten Bestandselemente an den Versandort verschieben können.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Header die folgenden Werte fest:

    - **Name des Menüelements:** *Aus Sortierung laden*
    - **Titel:** *Aus Sortierung laden*
    - **Modus:** *Arbeit*
    - **Vorhandene Arbeit verwenden:** *Ja*

1. Legen Sie im Inforegister **Allgemein** das Feld **Geleitet von** auf *Benutzergeleitet* fest.
1. Legen Sie im Inforegister **Arbeitsklassen** die Option **Neu** aus und stellen Sie dann die folgenden Werte ein:

    - **Arbeitsklassenkennung:** *SORT*
    - **Arbeitsauftragstyp:** *Sortierte Bestandsentnahme*

1. Wählen Sie **Speichern** aus.

### <a name="set-up-the-mobile-device-menu"></a>Menü für mobiles Gerät einrichten

Sie müssen jetzt die neuen Menüelemente zum Menü des Mobilgeräts hinzufügen.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.
1. Wählen Sie das Menü **Ausgehend**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Suchen Sie in der Spalte **Verfügbare Menüs und Menüpunkte** und wählen Sie **Palettenerstellung** aus.
1. Wählen Sie die rechte Pfeiltaste, um **Palettenerstellung** zur Spalte **Menüstruktur** zu verschieben.
1. Verwenden Sie die Aufwärtspfeil- und Abwärtspfeiltasten, um die Menüoption **Palettenerstellung** an die gewünschte Position im Menü des Mobilgeräts zu verschieben.
1. Wählen Sie **Speichern** aus.
1. Wiederholen Sie diesen Vorgang, um die Menüoption **Aus Sortierung laden** zum Menü **Ausgehend** hinzuzufügen.

### <a name="set-up-location-directives"></a>Lagerplatzrichtlinien einrichten

*Lagerplatzrichtlinien* sind Regeln, die dabei helfen, Entnahme- und Einlagerungslagerorte für die Lagerumlagerung zu identifizieren. Sie müssen jetzt eine Regel erstellen, um die Sortierarbeit zu verwalten.

#### <a name="set-up-a-single-sku-directive"></a>Einrichten einer Richtlinie für eine einzelne SKU

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Ändern Sie im linken Bereich den Wert des Felds **Arbeitsauftragstyp** zu *Sortierte Bestandsentnahme*.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Header die folgenden Werte fest:

    - **Sequenz:** *1*
    - **Name:** *Ladebereichstor*

1. Legen Sie im Inforegister **Lagerplatzrichtlinien** die folgenden Werte fest:

    - **Arbeitstyp:** *Einlagern*
    - **Standort:** *6*
    - **Lagerort:** *62*
    - **Mehrfach-SKU:** *Nein*

1. Wählen Sie **Speichern** aus, um die Symbolleiste im Inforegister **Positionen** verfügbar zu machen.
1. Legen Sie im Inforegister **Positionen** die Option **Neu** aus und stellen Sie dann die folgenden Werte auf die neue Position ein: Übernehmen Sie für alle anderen Felder die Standardwerte.

    - **Sequenz:** *1*
    - **Von:** *0*
    - **An:** *1.000.000*

1. Wählen Sie **Speichern** aus, um die Symbolleiste im Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.
1. Legen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus und stellen Sie dann die folgenden Werte auf die neue Position ein: Übernehmen Sie für alle anderen Felder die Standardwerte.

    - **Sequenz:** *1*
    - **Name:** *Ladebereichstor*

1. Wählen Sie **Speichern** aus.
1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** **Abfrage bearbeiten** aus.
1. Suchen Sie im Abfrageeditor auf der Registerkarte **Bereich** die Zeile, in der das Feld **Feld** auf *Lagerplatz* festgelegt ist. Legen Sie das Feld **Kriterien** für diese Zeile auf *Baydoor* fest.
1. Wählen Sie **OK** aus, um Ihre Einstellungen zu speichern und den Abfrageeditor zu schließen.

#### <a name="set-up-a-multiple-sku-directive"></a>Einrichten einer Richtlinie für eine Mehrfach-SKU

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Ändern Sie im linken Bereich den Wert des Felds **Arbeitsauftragstyp** zu *Sortierte Bestandsentnahme*.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Header die folgenden Werte fest:

    - **Sequenz:** *2*
    - **Name:** *Baydoor Multi*

1. Legen Sie im Inforegister **Lagerplatzrichtlinien** die folgenden Werte fest:

    - **Arbeitstyp:** *Einlagern*
    - **Standort:** *6*
    - **Lagerort:** *62*
    - **Mehrfach-SKU:** *Ja*

1. Wählen Sie **Speichern** aus, um die Symbolleiste im Inforegister **Positionen** verfügbar zu machen.
1. Legen Sie im Inforegister **Positionen** die Option **Neu** aus und stellen Sie dann die folgenden Werte auf die neue Position ein: Übernehmen Sie für alle anderen Felder die Standardwerte.

    - **Sequenz:** *1*
    - **Von:** *0*
    - **An:** *1.000.000*

1. Wählen Sie **Speichern** aus, um die Symbolleiste im Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.
1. Legen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Option **Neu** aus und stellen Sie dann die folgenden Werte auf die neue Position ein: Übernehmen Sie für alle anderen Felder die Standardwerte.

    - **Sequenz:** *1*
    - **Name:** *Baydoor Multi*

1. Wählen Sie **Speichern** aus.
1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** **Abfrage bearbeiten** aus.
1. Suchen Sie im Abfrageeditor auf der Registerkarte **Bereich** die Zeile, in der das Feld **Feld** auf *Lagerplatz* festgelegt ist. Legen Sie das Feld **Kriterien** für diese Zeile auf *Baydoor* fest.
1. Wählen Sie **OK** aus, um Ihre Einstellungen zu speichern und den Abfrageeditor zu schließen.

### <a name="set-up-work-templates"></a>Arbeitsvorlagen einrichten

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Ändern Sie den Wert des Felds **Arbeitsauftragstyp** zu *Sortierte Bestandsentnahme*.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Arbeitsvorlage zu erstellen.
1. Legen Sie auf der Registerkarte **Überblick** die folgenden Werte fest:

    - **Sequenz:** *1*
    - **Arbeitsvorlage:** *Sortieren*
    - **Arbeitsvorlagenbeschreibung:** *Sortieren*

1. Wählen Sie **Speichern** aus, um das Inforegister **Arbeitsvorlagendetails** verfügbar zu machen.
1. Wählen Sie im Inforegister **Arbeitsvorlagendetails** die Option **Neu** aus, um eine Zeile hinzuzufügen und dann die folgenden Werte dafür festzulegen:

    - **Arbeitstyp:** *Entnahme*
    - **Arbeitsklassenkennung:** *SORT*

1. Wählen Sie erneut **Neu** aus, um eine zweite Position hinzuzufügen, und legen Sie dann die folgenden Werte dafür fest:

    - **Arbeitstyp:** *Einlagern*
    - **Arbeitsklassenkennung:** *SORT*

1. Wählen Sie **Speichern** aus.

## <a name="scenario"></a>Szenario

Dieses Szenario simuliert eine Situation, in der verpackte Container je nach Spedition automatisch nach verschiedenen Positionen (Paletten) nach der Verpackungsstation sortiert werden sollten. Nachdem alle Artikel aus der Ladung verpackt und nach Adresse sortiert wurden, werden die Paletten zur Frachttür gebracht.

### <a name="create-sales-orders-and-picking-work"></a>Aufträge und Kommissionierarbeit erstellen

#### <a name="create-sales-order-1"></a>Auftrag 1 erstellen

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-005*
    - **Lagerort:** *62*

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.

    Der neue Auftrag wird geöffnet.

1. Wechseln Sie zur Ansicht **Kopfzeile**.
1. Legen Sie im Inforegister **Lieferung** im Abschnitt **Transport** die folgenden Werte fest:

    - **Spediteur:** *Luftfracht*
    - **Spediteur:** *Air*

1. Wechseln Sie zur Ansicht **Positionen**.
1. Auf dem Inforegister **Kundenauftragspositionen** wählen Sie **Zeile hinzufügen**, wenn eine neue Zeile nicht automatisch zum Raster hinzugefügt wird, geben Sie Folgendes ein:
1. Stellen Sie die folgenden Werte für die neue Bestellposition ein:

    - **Artikelnummer** *A001*
    - **Menge** *2*

1. Während die neue Auftragsposition weiterhin im Inforegister **Auftragspositionen** ausgewählt ist, wählen Sie im Menü **Bestand** über dem Raster **Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.
1. Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.
1. Sie erhalten eine Informationsnachricht, die die Lieferung und die Welle für diese Bestellung anzeigt. Notieren Sie sich die Wellen-ID- und Lieferungs-ID-Nummern.

#### <a name="sales-order-2"></a>Auftrag 2

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-006*
    - **Lagerort:** *62*

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.
1. Der neue Auftrag wird geöffnet. Es sollte eine neue, leere Position im Raster auf dem Inforegister **Auftragspositionen** enthalten. Stellen Sie die folgenden Werte für diese Bestellposition ein:

    - **Artikel:** *A0001*
    - **Menge** *1*

1. Im Inforegister **Zeilendetails** auf der Registerkarte **Lieferung** legen Sie das Feld **Lieferart** auf *Flowe-STD* fest.
1. Legen Sie im Inforegister **Auftragspositionen** die Option **Position hinzufügen** aus und stellen Sie dann die folgenden Werte auf die zweite Auftragsposition ein:

    - **Artikel:** *A0002*
    - **Menge** *1*

1. Im Inforegister **Zeilendetails** auf der Registerkarte **Lieferung** ändern Sie den Wert des Felds **Lieferart** auf *Air C-Air* fest.
1. Wählen Sie im Inforegister **Auftragspositionen** die erste Auftragsposition aus. Wählen Siedann im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.
1. Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.
1. Wählen Sie im Inforegister **Auftragspositionen** die zweite Auftragsposition aus. Wählen Siedann im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.
1. Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.
1. Sie erhalten eine Informationsnachricht, die die Lieferung und die Welle für diese Bestellung anzeigt. Beachten Sie, dass zwei Wellen-ID-Nummern und zwei Lieferungs-ID-Nummern erstellt wurden, eine für jede Lieferart für die Auftragspositionen.

#### <a name="get-the-work-ids-from-the-work-details"></a>Arbeits-IDs aus den Arbeitsdetails abrufen

1. Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.
1. Die Seite zeigt die Arbeits-IDs, die aus Aufträgen erstellt wurden. Verwenden Sie die Wellen-IDs und Lieferungs-IDs aus den von Ihnen erstellten Aufträgen, um die Arbeits-ID für jede Welle und Lieferung zu ermitteln. Notieren Sie sich diese Arbeits-IDs, da Sie sie in den nächsten Schritten benötigen. Beachten Sie, dass für den zweiten Auftrag zwei Arbeits-IDs erstellt wurden. Wenn verschiedene Artikel an verschiedenen Orten entnommen werden, werden separate Wort-IDs generiert.

### <a name="pick-items-for-the-sales-orders"></a>Artikel für die Aufträge entnehmen

Schließen Sie die erstellte Arbeit ab, indem Sie die Artikel mit dem mobilen Gerät zur Verpackungsstation verschieben.

1. Melden Sie sich auf dem mobilen Gerät im Lagerort *62* an, indem Sie die Benutzer-ID verwenden, die Sie für dieses Szenario erstellt haben (oder die Benutzer-ID eines vorhandenen Demodatenbenutzers).
1. Auf dem Hauptmenü wählen Sie **Ausgehend**.
1. Auf dem Menü **Ausgehend** wählen Sie **Verkaufsauswahl**.
1. Geben Sie im Feld **ID** die Arbeits-ID ein, die für den Auftrag 1 erstellt wurde.
1. Wählen Sie **OK**.
1. Geben Sie auf dieser Seite **Aufträge – Entnehmen** eine Ziel-LP ein, die für Auftrag 1 erstellt wurde. Beachten Sie, dass Entnahmeort (*Bulk-001*), Artikel (*A0001*) und Menge (*2 Stk*) gezeigt werden.
1. Wählen Sie **OK**.
1. Prüfen Sie die Informationen auf der Seite **Aufträge – Einlagern**. Das Feld **Loc** sollte anzeigen, dass die ausgewählten Artikel an den Ort *Verpackung* gehen.
1. Wählen Sie **OK**.

    Auf der Seite **Arbeits-/Kennzeichen-ID scannen** erhalten Sie eine Meldung „Arbeit abgeschlossen“ message, die angibt, dass die Arbeits-ID aus Auftrag 1 abgeschlossen wurde.

    Sie wählen nun Auftrag 2.

1. Geben Sie im Feld **ID** die Arbeits-ID ein, die für den Auftrag 2 erstellt wurde, bei der Position 1 den Artikel *A0001* aufweist.
1. Wählen Sie **OK**.
1. Geben Sie auf der Seite **Aufträge – Entnehmen** eine Ziel-LP ein. Beachten Sie, dass Entnahmeort (*Bulk-001*), Artikel (*A0001*) und Menge (*1 Stk*) gezeigt werden.
1. Wählen Sie **OK**.
1. Prüfen Sie die Informationen auf der Seite **Aufträge – Einlagern**. Das Feld **Loc** sollte anzeigen, dass die ausgewählten Artikel an den Ort *Verpackung* gehen.
1. Wählen Sie **OK**.

    Auf der Seite **Arbeits-/Kennzeichen-ID scannen** erhalten Sie eine Meldung „Arbeit abgeschlossen“. Diese Nachricht zeigt an, dass die Arbeits-ID aus Position 1 von Auftrag 2 abgeschlossen wurde.

1. Geben Sie im Feld **ID** die Arbeits-ID ein, die für den Auftrag 2 erstellt wurde, bei der Position 2 den Artikel *A0002* aufweist.
1. Wählen Sie **OK**.
1. Geben Sie auf der Seite **Aufträge – Entnehmen** eine Ziel-LP ein. Beachten Sie, dass Entnahmeort (*Bulk-002*), Artikel (*A0001*) und Menge (*1 Stk*) gezeigt werden.
1. Wählen Sie **OK**.
1. Prüfen Sie die Informationen auf der Seite **Aufträge – Einlagern**. Das Feld **Loc** sollte anzeigen, dass die ausgewählten Artikel an den Ort *Verpackung* gehen.
1. Wählen Sie **OK**.

    Auf der Seite **Arbeits-/Kennzeichen-ID scannen** erhalten Sie eine Meldung „Arbeit abgeschlossen“. Diese Nachricht zeigt an, dass die Arbeits-ID aus Position 2 von Auftrag 2 abgeschlossen wurde.

### <a name="pack-sales-orders-into-containers"></a>Aufträge in Container verpacken

#### <a name="pack-sales-order-1-into-containers"></a>Auftrag 1 in Container verpacken

1. Gehen Sie zu **Lagerortverwaltung \> Verpackung und Containerisierung \> Verpackung**.

    Das Dialogfeld **Verpackungsstation auswählen** wird angezeigt. Standardmäßig sollte das Feld **Arbeitskraft** auf den Namen der Arbeitskraft gesetzt werden, die Sie zuvor eingerichtet haben.

1. Legen Sie die folgenden Werte fest, um Lieferungen und Container anzuzeigen und zu bearbeiten, die am jeweiligen Verpackungsort geplant sind:

    - **Standort:** *6*
    - **Lagerort:** *62*
    - **Lagerplatz:** *Verpackung*
    - **Verpackungsprofilkennung:** *Sortieren*

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.
1. Geben Sie auf der Seite **Verpackung** im Feld **Kennzeichen oder Lieferung** die Ziel-LP für Auftrag 1 ein. Drücken Sie dann die Taste **Tab** oder **Eingabe** auf Ihrer Tastatur, um das Feld zu verlassen.
1. Wählen Sie im Aktivitätsbereich **Neuer Container** aus.
1. Übernehmen Sie alle Standardeinstellungen und wählen Sie **OK**. Notieren Sie die Container-ID.
1. Legen Sie im Inforegister **Artikelverpackung** die folgenden Werte fest:

    - **Menge** *1*
    - **Bezeichner:** Artikel *A0001*

1. Wählen Sie im Aktivitätsbereich **Container schließen** aus.
1. Wählen Sie im Dialogfeld **Container schließen** die Option **Systemgewicht abrufen**, damit das System das Feld **Bruttogewicht** aktualisiert.
1. Wählen Sie **OK**. Der Container wird zum Lagerplatz *SORT* verschoben und ist bereit zum Sortieren.
1. Erstellen Sie einen zweiten Container, um den zweiten Artikel aus der LP für Auftrag 1 einem neuen Container hinzuzufügen.
1. Wählen Sie im Aktivitätsbereich **Neuer Container** aus.
1. Übernehmen Sie alle Standardeinstellungen und wählen Sie **OK**. Notieren Sie die Container-ID.
1. Legen Sie im Inforegister **Artikelverpackung** die folgenden Werte fest:

    - **Menge** *1*
    - **Bezeichner:** Artikel *A0001*

1. Wählen Sie im Aktivitätsbereich **Container schließen** aus.
1. Wählen Sie im Dialogfeld **Container schließen** die Option **Systemgewicht abrufen**, damit das System das Feld **Bruttogewicht** aktualisiert.
1. Wählen Sie **OK**. Der Container wird zum Lagerplatz *SORT* verschoben und ist bereit zum Sortieren.

#### <a name="pack-sales-order-2-into-containers"></a>Auftrag 2 in Container verpacken

1. Geben Sie auf der Seite **Verpackung** im Feld **Kennzeichen oder Lieferung** die Ziel-LP für Position 1 von Auftrag 1 ein. Drücken Sie dann die Taste **Tab** oder **Eingabe** auf Ihrer Tastatur, um das Feld zu verlassen.
1. Wählen Sie im Aktivitätsbereich **Neuer Container** aus.
1. Übernehmen Sie alle Standardeinstellungen und wählen Sie **OK**. Notieren Sie die Container-ID.
1. Legen Sie im Inforegister **Artikelverpackung** die folgenden Werte fest:

    - **Menge** *1*
    - **Bezeichner:** Artikel *A0001*

1. Wählen Sie im Aktivitätsbereich **Container schließen** aus.
1. Wählen Sie im Dialogfeld **Container schließen** die Option **Systemgewicht abrufen**, damit das System das Feld **Bruttogewicht** aktualisiert.
1. Wählen Sie **OK**. Der Container wird zum Lagerplatz *SORT* verschoben und ist bereit zum Sortieren.
1. Geben Sie im Feld **Kennzeichen oder Lieferung** die Ziel-LP für Position 2 von Auftrag 2 ein. Drücken Sie dann die Taste **Tab** oder **Eingabe** auf Ihrer Tastatur, um das Feld zu verlassen.
1. Wählen Sie im Aktivitätsbereich **Neuer Container** aus.
1. Übernehmen Sie alle Standardeinstellungen und wählen Sie **OK**. Notieren Sie die Container-ID.
1. Legen Sie im Inforegister **Artikelverpackung** die folgenden Werte fest:

    - **Menge** *1*
    - **Bezeichnerfeld:** Artikel *A0002*

1. Wählen Sie im Aktivitätsbereich **Container schließen** aus.
1. Wählen Sie im Dialogfeld **Container schließen** die Option **Systemgewicht abrufen**, damit das System das Feld **Bruttogewicht** aktualisiert.
1. Wählen Sie **OK**. Der Container wird zum Lagerplatz *SORT* verschoben und ist bereit zum Sortieren.

Um die Containerdetails anzuzeigen, gehen Sie zu **Lagerortverwaltung \> Verpackung und Containerisierung \> Container** und suchen Sie nach den Container-IDs, die beim Packen erstellt wurden.

### <a name="sort-the-containers"></a>Container sortieren

> [!IMPORTANT]
> Wenn Sie auf der mobilen App auf die Menüoption **Palettenerstellung** für die Ausgangssortierung zugreifen, wird eine Schaltfläche mit der Bezeichnung **Voll** angezeigt. *Verwenden Sie die Schaltfläche **Voll** nicht zum Sortieren oder Schließen der Position.*
>
> Die Schaltfläche **Voll** ist standardmäßig verfügbar und kann nicht deaktiviert oder von der Seite entfernt werden. Sie wird nicht für die Funktion *Ausgangssortierung* verwendet.

#### <a name="sort-the-first-container"></a>Sortieren des ersten Containers

1. Melden Sie sich auf dem mobilen Gerät im Lagerort *62* an, indem Sie die Benutzer-ID verwenden, die Sie für dieses Szenario erstellt haben (oder die Benutzer-ID eines vorhandenen Demodatenbenutzers).
1. Auf dem Hauptmenü wählen Sie **Ausgehend**.
1. Auf dem Menü **Ausgehend** wählen Sie **Palettenerstellung**.
1. Geben Sie im Feld **LP/Con** die erste Container-ID ein, die dem Auftrag 1 zugeordnet ist.
1. Wählen Sie **OK**.
1. Da derzeit keine Sortierpositionen vorhanden sind, müssen Sie eine angeben. Geben Sie im Feld **Sortierposition-ID** *SP01* ein.
1. Weil derzeit keine LP mit der Sortierposition *SP01* verknüpft ist, müssen Sie eine angeben. Im Feld **LP** geben Sie *PLP01* ein.
1. Wählen Sie **OK**.
1. Da die Überprüfung der Sortierposition aktiviert ist, müssen Sie die ID der Sortierposition erneut eingeben. Geben Sie im Feld **Sortierposition-ID** *SP01* ein.
1. Wählen Sie **OK**.

    Sie erhalten die Nachricht „Arbeit abgeschlossen“.

> [!TIP]
> Um die Sortierposition und die darin enthaltene LP anzuzeigen, gehen Sie zu **Lagerortverwaltung \> Verpackung und Containerisierung \> Zuweisungen von Ausgangssortierpositionen**.
>
> Die Seite **Zuweisungen von Ausgangssortierpositionen** zeigt alle aktuell aktiven Sortierpositionen an. Das Feld **Sortierpositionstransaktionen** zeigt die LP, die jeder Sortierposition zugeordnet ist, und die Container, die sich an der Sortierposition befinden. Beachten Sie, dass derzeit eine Sortierposition vorhanden ist und dass das Inforegister **Sortierpositionskriterien** ein Kriterium von **Lieferung – Spedition – Luft**.

#### <a name="sort-the-remaining-containers"></a>Übrige Container sortieren

1. Melden Sie sich auf dem mobilen Gerät im Lagerort *62* an, indem Sie die Benutzer-ID verwenden, die Sie für dieses Szenario erstellt haben (oder die Benutzer-ID eines vorhandenen Demodatenbenutzers).
1. Auf dem Hauptmenü wählen Sie **Ausgehend**.
1. Auf dem Menü **Ausgehend** wählen Sie **Palettenerstellung**.
1. Geben Sie im Feld **LP/Con** die zweite Container-ID ein, die dem Auftrag 1 zugeordnet ist.
1. Wählen Sie **OK**. Da die Sortiervorlage so eingerichtet ist, dass sie automatisch sortiert wird und bereits eine Sortierposition mit übereinstimmenden Kriterien vorhanden ist, werden Sie automatisch zur richtigen Sortierposition weitergeleitet.
1. Wählen Sie **OK**.
1. Bestätigen Sie die ID der Sortierposition, um anzuzeigen, dass sich der Bestand an der richtigen Stelle befindet. Geben Sie im Feld **Sortierposition-ID** *SP01* ein.
1. Wählen Sie **OK**.

    Die Arbeiten am zweiten Container aus Auftrag 1 sind abgeschlossen. Sie sortieren nun die verbleibenden Container aus Auftrag 2.

1. Geben Sie im Feld **LP/Con** die Container-ID des Containers aus Auftrag 2 ein, der den Artikel *A0001* enthält. Da sich die Spedition unterscheidet, werden Sie aufgefordert, eine neue Sortierposition einzugeben und dieser Position eine LP zuzuweisen. Verwenden Sie Sortierposition *SP02* und LP *PLP02*.
1. Wählen Sie **OK**.
1. Bestätigen Sie die Sortierposition durch Eingabe von *SP02* im Feld **Sortierposition-ID**.
1. Wählen Sie **OK**.

    Die Arbeiten am Container sind abgeschlossen.

1. Geben Sie im Feld **LP/Con** die Container-ID für die übrigen Container aus Auftrag 2 ein, der den Artikel *A0002* enthält. Da der Spediteurservice mit dem Spediteurservice für Auftrag 1 identisch ist, zeigt das System die vorhandene Sortierposition mit Übereinstimmungskriterien an.
1. Wählen Sie **OK**.
1. Bestätigen Sie die Sortierposition durch Eingabe von *SP01* im Feld **Sortierposition-ID**.
1. Wählen Sie **OK**.

    Die Arbeiten am Container sind abgeschlossen.

### <a name="close-the-outbound-sorting-positions"></a>Schließen Sie die ausgehenden Sortierpositionen

Wenn der gesamte Bestand sortiert wurde, muss die Position geschlossen werden, bevor Arbeiten erstellt werden können. Es werden sortierte Bestandsentnahmen erstellt, um den Bestand zur Frachttür zu bringen.

#### <a name="close-a-position-from-the-mobile-device"></a>Eine Position vom Mobilgerät aus schließen

1. Melden Sie sich auf dem mobilen Gerät im Lagerort *62* an, indem Sie die Benutzer-ID verwenden, die Sie für dieses Szenario erstellt haben (oder die Benutzer-ID eines vorhandenen Demodatenbenutzers).
1. Auf dem Hauptmenü wählen Sie **Ausgehend**.
1. Auf dem Menü **Ausgehend** wählen Sie **Palettenerstellung**.
1. Geben Sie im Feld **LP/Con** eine Container-ID ein, die nach Sortierposition *SP01* sortiert wurde.
1. Wählen Sie **OK**.
1. Sie erhalten folgende Meldung: „Der Container ist bereits auf Position SP01 sortiert. Diese Position schließen?“ Wählen Sie **Schließen** aus.

    Die Arbeit ist abgeschlossen.

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a>Eine Position aus ausgehenden Sortierpositionszuweisungen schließen

1. Gehen Sie zu **Lagerortverwaltung \> Verpackung und Containerisierung \> Zuweisungen von Ausgangssortierpositionen**.
1. Wählen Sie in der linken Spalte **SP02**. Diese Zeile für die ausgehende Sortierposition wird geschlossen.
1. Wählen Sie im Aktivitätsbereich **Position schließen** aus. Der Sortierpositionsdatensatz ist geschlossen und wird nicht mehr angezeigt.

    > [!TIP]
    > Um alle geschlossenen Positionsdatensätze anzuzeigen, wählen Sie das Kontrollkästchen **Geschlossene anzeigen**.

### <a name="sorted-inventory-picking"></a>Sortierte Bestandsentnahme

Sie müssen die sortierte Bestandsauswahl durchführen. Wenn es fertig ist, wird der Bestand in den Kundenauftrag aufgenommen. Zu diesem Zeitpunkt gelten alle anderen Lagerprozesse.

1. Melden Sie sich auf dem mobilen Gerät im Lagerort *62* an, indem Sie die Benutzer-ID verwenden, die Sie für dieses Szenario erstellt haben (oder die Benutzer-ID eines vorhandenen Demodatenbenutzers).
1. Auf dem Hauptmenü wählen Sie **Ausgehend**.
1. Wählen Sie im Menü **Ausgehend** **Aus Sortierung laden**.
1. Geben Sie die Ziel-LP-ID von der ersten Sortierposition *SP01* aus ein. Legen Sie das Feld **ID** auf *PLP01* fest.
1. Wählen Sie **OK**.
1. Die Seite **Sortierte Bestandentnahme: Entnehmen** zeigt die Entnahmearbeit, die ausgeführt werden müssen. Wählen Sie aus dem Lagerplatz *SORT* und Ziel-LP *PLP01*, die mehrere Artikel und eine Menge von *3* hat.
1. Wählen Sie **OK**.
1. Die Seite **Sortierte Bestandentnahme: Einlagern** zeigt die Einlagerunsarbeit, die ausgeführt werden müssen. Lagern Sie im Lagerplatz *Frachttür* und Ziel-LP *PLP01*, die mehrere Artikel und eine Menge von *3* hat.
1. Wählen Sie **OK**.

    Die Arbeit ist abgeschlossen.

1. Geben Sie das Zielkennzeichen von der zweiten Sortierposition *SP02* aus ein. Legen Sie das Feld **ID** auf *PLP02* fest.
1. Wählen Sie **OK**.
1. Die Seite **Sortierte Bestandentnahme: Entnehmen** zeigt die Entnahmearbeit, die ausgeführt werden müssen. Wählen Sie aus dem Lagerplatz *SORT* und Ziel-LP *PLP02*, die mehrere Artikel und eine Menge von *1* hat.
1. Wählen Sie **OK**.
1. Die Seite **Sortierte Bestandentnahme: Einlagern** zeigt die Einlagerunsarbeit, die ausgeführt werden müssen. Lagern Sie im Lagerplatz *Frachttür* und Ziel-LP *PLP02*, die mehrere Artikel und eine Menge von *1* hat.
1. Wählen Sie **OK**.

    Die Arbeit ist abgeschlossen.

Ab diesem Zeitpunkt gelten alle anderen Lagerprozesse.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]