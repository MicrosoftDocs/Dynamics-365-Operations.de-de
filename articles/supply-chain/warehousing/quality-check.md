---
title: Qualitätsprüfung
description: Dieses Thema enthält Informationen zur Qualitätsprüf+ungsfunktion. Mit dieser Funktion können Lagerarbeiter schnelle Stichproben der Qualität durchführen, während sie Artikel an der Eingangsrampe in Empfang nehmen.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 31afcfcb9d8dbb91f4ea4e3e7a7282c2a87328d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228464"
---
# <a name="quality-check"></a>Qualitätsprüfung

[!include [banner](../includes/banner.md)]

Mit der Funktion *Qualitätsprüfung* können Lagerarbeiter schnelle Stichproben der Qualität durchführen, während sie Artikel an der Eingangsrampe in Empfang nehmen. Diese Stichproben sind hilfreich, wenn Arbeiter Verpackungen oder andere leicht erkennbare Teile eines Artikels inspizieren. Die Funktion hilft den Mitarbeitern, schnell zu überprüfen, ob etwas offensichtlich fehlerhaft oder beschädigt ist, bevor sie die Bestände an ihren Einlagerungslagerplatz lagern.

Diese Funktion ist eine Alternative zum Standardverfahren zur Qualitätsprüfung. Sie bietet mehr Flexibilität und eine schnellere Verarbeitung.

Wenn Sie diese Funktion verwenden, erfolgt die Wareneingangs- und Qualitätsprüfung wie folgt:

1. Wenn eine Lieferung eintrifft, zeichnet ein Lagerarbeiter den Wareneingang auf. Der Arbeiter scannt auch einen Ladungsträger, um den Standort aufzuzeichnen.
1. Der Mitarbeiter führt eine schnelle Qualitätsprüfung durch und zeichnet das Ergebnis (bestanden oder nicht bestanden) für diesen Ladungsträger auf.
1. Eine der folgenden Aktionen erfolgt:

    - Wenn die Qualitätsprüfung bestanden ist, wird der Ladungsträger angenommen und wie gewohnt zu einem Empfangsort weitergeleitet.
    - Wenn die Qualitätsprüfung nicht bestanden wird, wird der Ladungsträger abgelehnt und laufende Einlagerungsarbeiten werden zur weiteren Überprüfung an einen anderen Ort umgeleitet. Ein neuer Qualitätsprüfungsauftrag wird erstellt. Um den Qualitätsprüfungsauftrag anzusehen, der aus der fehlgeschlagenen Qualitätsprüfung erstellt wurde, gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsauftrag**.

Dieser Vorgang kann auch so eingerichtet werden, dass alle gescannten Ladungsträger sofort an den Ort der Qualitätsprüfung umgeleitet werden.

## <a name="turn-on-the-quality-check-feature"></a>Die Qualitätsprüfungsfunktion aktivieren

Bevor Sie die Funktion *Qualitätsprüfung* nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Qualitätsprüfung*

## <a name="set-up-the-feature-for-the-example-scenario"></a>Funktion für das Beispielszenario einrichten

Dieser Abschnitt enthält Richtlinien und ein Beispiel, das zeigt, wie Sie die Funktion *Qualitätsprüfung* einrichten und Beispieldaten für das Beispielszenario vorbereiten, das später in diesem Thema bereitgestellt wird.

### <a name="make-sample-data-available"></a>Beispieldaten zur Verfügung stellen

Um das [Beispielszenario](#example-scenario) mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

### <a name="quality-check-template"></a><a name="quality-template"></a>Qualitätsprüfungsvorlage

Die Qualitätsprüfungsvorlage legt die Regeln für die schnelle Stichprobenprüfung der Qualität beim Wareneingang fest.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Qualitätprüfungsvorlage**.
1. Wählen Sie **Neu** aus, um dem Raster eine Vorlage hinzuzufügen.
1. Legen Sie für die neue Vorlage die folgenden Werte fest:

    - **Name der Qualitätsprüfungsvorlage:** *Eingangsrampenprüfung*

        Geben Sie einen Namen ein, der die für diese Vorlage geltenden Richtlinien angibt.

    - **Annahmerichtlinie:** *Benutzer auffordern*

        +Geben Sie an, ob Benutzer aufgefordert werden sollen, die Qualität des Bestands während der Erledigung der Arbeit anzunehmen oder abzulehnen oder ob die Qualität automatisch abgelehnt werden soll. Die verfügbaren Optionen sind *Automatisch ablehnen* und *Benutzer auffordern*.

    - **Qualitätsverarbeitungspolitik:** *Qualitätsprüfungsauftrag erstellen*

        Wählen Sie die Richtlinie aus, die verwendet werden soll, wenn die Bestandsqualität abgelehnt wurde. Die folgenden Optionen stehen zur Verfügung:

        - *Nur Arbeit erstellen*: Erstellen Sie nur die Arbeit, um die Bestandsumlagerung zu ermöglichen.
        - *Qualitätsprüfungsauftrag erstellen*: Erstellen Sie einen Qualitätsprüfungsauftrag, um Qualitätstests zu ermöglichen.

    - **Testgruppe:** *Anlage*

        Geben Sie die Testgruppe an, die in dem erstellten Qualitätsprüfungsauftrag verwendet werden soll. Testgruppen werden im Modul **Bestandsverwaltung** eingerichtet.

        Lassen Sie die Option **Zerstörungstest** für die Testgruppe deaktiviert. Diese Option legt fest, ob das Muster im Rahmen der Tests in der Testgruppe zerstört wird. Wird ein Zerstörungstest verwendet, generiert das System beim Erstellen eines Qualitätsprüfungsauftrags für einen Artikel eine Lagerbuchung. Mit der neuen Lagerbuchung wird die Bestandsverringerung für die Testmenge antizipiert. Die Bestandsverringerung wird durchgeführt, wenn der Qualitätsprüfungsauftrag durch den Überprüfungsschritt abgeschlossen wird. Die Lagerbuchung wird als Qualitätsprüfungsauftrag gekennzeichnet.

### <a name="work-class--quality-check"></a><a name="work-class"></a>Arbeitsklasse – Qualitätsprüfung

Arbeitsklassen werden verwendet, um den Typ der Arbeitsauftragspositionen zuzuweisen und/oder einzuschränken, die Lagerarbeiter auf einem mobilen Gerät verarbeiten können.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsklassen**.
1. Wählen Sie **Neu** aus, um eine Arbeitsklasse zu erstellen.
1. Legen Sie im Header die folgenden Werte fest:

    - **Arbeitsklassen-ID:** *QC-Prüfung*

        Geben Sie den Namen für die Arbeitsklasse ein.

    - **Beschreibung:** *QC-Prüfung*

        Geben Sie eine kurze Beschreibung ein, die angibt, wofür die Arbeitsklasse verwendet wird.

    - **Arbeitsauftragstyp:** *Qualität in der Qualitätsprüfung*

        Wählen Sie den Typ des Arbeitsauftrags aus, der mit der Arbeitsklasse erstellt wird. Wenn Sie Qualitätskontrollarbeiten einrichten, wählen Sie immer *Qualität in der Qualitätsprüfung*.

1. Im Inforegister **Gültige Einlagerungsorttypen** lassen Sie das Feld **Lagerplatztyp** leer.

    Wenn Sie einen Lagerplatztyp auswählen, begrenzen Sie die Lagerorte, an denen Artikel nach der Entnahme abgelegt werden können. Dieses Feld wird verwendet, wenn eine Lagerplatzrichtlinie versucht, den Lagerplatz aufzulösen oder ein Lagerarbeiter manuell den Speicherort für die Menüoption des mobilen Geräts festlegt.

Weitere Informationen zu Arbeitsklassen und deren Erstellung finden Sie unter [Eine Arbeitsklasse erstellen](tasks/create-work-class.md).

### <a name="work-template"></a>Arbeitsvorlage

Mithilfe von Arbeitsvorlagen können Sie die Arbeitsvorgänge definieren, die am Lagerplatz ausgeführt werden müssen. In der Regel bestehen Lagerplatzarbeitsabläufe aus folgenden Aktivitäten: Ein Lagerarbeiter entnimmt verfügbaren Lagerbestand an einem Lagerplatz und legt anschließend den entnommenen Bestand an einem anderen Lagerplatz ab. Eine Arbeitsvorlage für die Qualitätskontrolle legt die Arbeitsabläufe für Qualitätsprüfungen fest.

#### <a name="purchase-orders"></a>Bestellungen

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Wählen Sie in der Kopfzeile **Arbeitsauftragstyp** die Option *Bestellungen* aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie eine Arbeitsvorlage aus, die einen Qualitätsprüfungsschritt enthalten soll. Wählen Sie im Abschnitt **Übersicht** im Feld **Arbeitsvorlage** *51 PO-Eingang* aus.
1. Im Abschnitt **Arbeitsvorlagendetails** hat das im Raster zwei Positionen: eine für *Entnahme* und eine für *Einlagerung*.
1. Wählen Sie im Abschnitt **Arbeitsvorlagendetails** **Neu** aus, um dem Raster einer Zeile zur Qualitätskontrolle hinzuzufügen. Beachten Sie, dass das Feld **Positionsnummer** für die neue Zeile auf *3* gesetzt ist.
1. Legen Sie die folgenden Werte für die neue Position fest. Übernehmen Sie für alle verbleibenden Felder die Standardwerte.

    - **Arbeitstyp:** *Qualitätsprüfung*
    - **Arbeitsklassen-ID:** *Kauf*
    - **Name der Qualitätsprüfungsvorlage:** *Eingangsrampenprüfung*

        Wählen Sie die eindeutige Kennung für die Arbeitsklasse aus. Sie verwenden diesen Wert, um die Menüoptionen im mobilen Gerät und die Typen der Arbeit, die diese Menüoptionen verarbeiten können, zu konfigurieren.

1. Wählen Sie im Aktionsbereich **Speichern**, um Ihre bisherige Arbeit zu speichern.

    Sie erhalten eine Informationsmeldung mit dem Titel „Ungültig – Qualitätsprüfung muss direkt nach einer Entnahme erfolgen“. Daher müssen Sie die **Positionsnummer** für die gerade hinzugefügte Position ändern.

1. Ändern Sie den Wert der **Positionsnummer** für die neue Position wie folgt:

    1. Im Bereich **Arbeitsvorlagendetails** wählen sie die Position aus, in der das Feld **Arbeitstyp** auf *Qualitätsprüfung* gesetzt ist.
    2. Nutzen Sie die Schaltfläche **Nach oben** oder **Nach unten**, um die Position *Qualitätsprüfung* hinter die Position *Entnahme* zu verschieben.

1. Wählen Sie im Aktionsbereich **Speichern** aus.

#### <a name="quality-in-quality-check"></a>Qualität in Qualitätsprüfung

Erstellen Sie als Nächstes eine Arbeitsvorlage für die Qualitätsprüfung.

1. Ändern Sie in der Kopfzeile der Seite **Arbeitsvorlagen** den Wert des Felds **Arbeitsauftragstyp** auf *Qualität in der Qualitätsprüfung*.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster im Bereich **Übersicht** eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Arbeitsvorlage:** *51 Qualitätsprüfung*

        Geben Sie einen Namen für die Vorlage ein.

    - **Arbeitsvorlagenbeschreibung:** *51 Qualitätsprüfung*

1. Wählen Sie im Aktionsbereich **Speichern** aus, um den Abschnitt **Arbeitsvorlagendetails** verfügbar zu machen.
1. Während die neue Vorlage noch im Abschnitt **Übersicht** ausgewählt ist, wählen Sie **Neu** im Abschnitt **Arbeitsvorlagendetails**, um dort eine Zeile zum Raster hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Arbeitstyp:** *Entnahme*
    - **Arbeitsklassen-ID:** *QC-Prüfung*

        Wählen Sie den Namen der [Arbeiterklasse](#work-class) aus, die Sie zuvor für die Qualitätskontrolle erstellt haben.

1. In dem Abschnitt **Arbeitsvorlagendetails** wählen Sie wieder **Neu**, um eine weitere Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Arbeitstyp:** *Einlagern*
    - **Arbeitsklassen-ID:** *QC-Prüfung*

        Wählen Sie den Namen der [Arbeiterklasse](#work-class) aus, die Sie zuvor für die Qualitätskontrolle erstellt haben.

1. Wählen Sie im Aktionsbereich **Speichern** aus.

Weitere Informationen zu Arbeitsvorlagen, finden Sie unter [Steuern von Lagerarbeit mithilfe von Arbeitsvorlagen und Lagerplatzrichtlinien](control-warehouse-location-directives.md)

### <a name="location-directive--quality-failures"></a>Lagerplatzrichtlinie – Qualitätsmängel

Lagerplatzrichtlinien sind Regeln, die dabei helfen, Entnahme- und Einlagerungslagerorte für die Lagerumlagerung zu identifizieren. In einer Auftragsbuchung bestimmt eine Lagerplatzrichtlinie z. B., wo die Artikel entnommen und wo die entnommenen Artikel eingelagert werden. Sie müssen eine Lagerplatzrichtlinienregel konfigurieren, um zu definieren, wie fehlgeschlagene Qualitätsprüfungen behandelt werden.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Stellen Sie im linken Bereich das Feld **Arbeitsauftragstyp** auf *Bestellungen*, um mit Lagerplatzrichtlinien dieses Typs zu arbeiten.
1. Wählen Sie im Aktivitätsbereich die Option **Neu** aus, um eine Lagerplatzrichtlinie für Qualitätsprüfungen zu erstellen.
1. Legen Sie im Header die folgenden Werte fest:

    - **Sequenznummer:** Akzeptieren Sie den Standardwert.
    - **Name:** *51 zu Qualität*

1. Legen Sie im Inforegister **Lagerplatzrichtlinien** die folgenden Werte fest. Übernehmen Sie für alle verbleibenden Felder die Standardwerte.

    - **Arbeitstyp:** *Einlagern*
    - **Standort:** *5*
    - **Lagerort:** *51*

1. Wählen Sie im Aktionsbereich **Speichern** aus, um Ihre Richtlinie zu speichern und das Inforegister **Positionen** verfügbar zu machen.
1. Wählen Sie im Inforegister **Positionen** die Option **Neu** aus, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest. Übernehmen Sie für alle verbleibenden Felder die Standardwerte.

    - **Von Menge:** *1*
    - **Bis Menge:** *1000000*

1. Wählen Sie im Aktionsbereich **Speichern** aus, um die neue Position zu speichern und das Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.
1. Während die neue Position noch im Inforegister **Positionen** ausgewählt ist, gehen Sie auf **Neu** im Inforegister **Lagerplatzrichtlinienaktivitäten**, um dort eine Zeile zum Raster hinzuzufügen, damit Sie eine Aktion für die Position festlegen können.
1. Stellen Sie in der neuen Zeile das Feld **Name** auf *Qualität*. Übernehmen Sie für alle verbleibenden Felder die Standardwerte.
1. Wählen Sie im Aktionsbereich **Speichern** aus, um die Schaltfläche **Abfrage bearbeiten** im Inforegister **Lagerplatzrichtlinienaktivitäten** verfügbar zu machen.
1. Während die gerade hinzugefügte Position im Inforegister **Lagerplatzrichtlinienaktivitäten** noch ausgewählt ist, gehen Sie auf **Abfrage bearbeiten**, um ein Dialogfeld zu öffnen, in dem Sie die Abfrage für die Aktion bearbeiten können.
1. Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Abfrage hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Tabelle:** *Lagerorte*
    - **Abgeleitete Tabelle:** *Lagerorte*
    - **Feld:** *Lagerplatz*
    - **Kriterien:** *QMS*

    Der *QMS*-Lagerplatz ist ein Lagerort für die Qualität.

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.
1. Jetzt müssen Sie die Reihenfolge der vorhandenen Bestellungs-Lagerplatzrichtlinien für Lagerort *51* ändern. Speichern Sie die neue Lagerplatzrichtlinie *51 zu Qualität* aus, aktualisieren Sie die Seite und wählen Sie die Lagerplatzrichtlinie in der Liste aus. Benutzen Sie dann die Schaltflächen **Nach oben** und **Nach unten** im Aktionsbereich, um die Lagerplatzrichtlinie für Lagerort *51* in der folgenden Reihenfolge festzulegen. (Bevor Sie **Nach oben** oder **Nach unten** wählen, müssen Sie eine Lagerplatzrichtlinie in der Liste auswählen.)

    1. 51 zu Qualität
    2. 51 PO direkt
    3. 51 QMS

### <a name="mobile-device-menu-items"></a>Menüelemente des mobilen Geräts

Konfigurieren Sie ein Menüelement, damit mobile Geräte die Funktion **Qualitätsprüfung** ausführen können.

#### <a name="purchase-putaway"></a>Kauf einlagern

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie aus der Liste das Menüelement **Kauf einlagern** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie im Bereich **Arbeitsklassen** die Option **Neu** aus, um dem Raster eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Arbeitsklassen-ID:** *QC-Prüfung*

        Geben Sie den Namen der [Arbeiterklasse](#work-class) ein, die Sie zuvor für die Qualitätskontrolle erstellt haben.

    - **Arbeitsauftragstyp:** *Qualität in der Qualitätsprüfung*

1. Wählen Sie im Aktionsbereich **Speichern** aus.

#### <a name="purchase-order-line-receiving"></a>Bestellposition – Empfang

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Header die folgenden Werte fest:

    - **Name des Menüpunkts:** *PO-Positionsempfang*
    - **Titel:** *PO-Positionsempfang*
    - **Modus:** *Arbeit*
    - **Vorhandene Arbeit verwenden:** *Nein*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest. Übernehmen Sie für alle verbleibenden Felder die Standardwerte.

    - **Arbeitserstellungsprozess:** *Bestellungspositionsempfang und Einlagerung*
    - **Kennzeichen generieren:** *Ja*
    - **Arbeitsvorlage:** *51 PO-Eingang*

1. Wählen Sie im Aktionsbereich **Speichern** aus.

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Hinzufügen der Menüoption zu einem mobilen Gerät

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.
1. Wählen Sie im linken Bereich das Menü **Eingehend** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie in der Liste **Verfügbare Menüs und Menüelemente** das Menüelement **PO-Positionseingang** aus.
1. Wählen Sie die rechte Pfeiltaste, um **PO-Positionseingang** zur Spalte **Menüstruktur** zu verschieben.
1. In der Spalte **Menüstruktur** wählen Sie **PO-Positionseingang** und verschieben das Menüelement dann mit den Nach-oben- und Nach-unten-Tasten an die gewünschte Position im Menü des mobilen Geräts.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

## <a name="example-scenario"></a><a name="example-scenario"></a>Beispielszenario

Nachdem Sie alle zuvor beschriebenen Beispieldaten verfügbar gemacht und eingerichtet haben, können Sie dieses Szenario durcharbeiten, um die Funktion *Qualitätsprüfung* zu testen. Bei den in diesem Szenario angezeigten Werten wird davon ausgegangen, dass Sie mit den Standarddemodaten arbeiten, die juristische Person **USMF** ausgewählt und die Beispieldatensätze vorbereitet haben, die weiter oben in diesem Thema beschrieben wurden. Dieses Szenario dient auch als Beispiel, das zeigt, wie die Funktion in einer Produktionseinstellung verwendet werden kann.

### <a name="create-a-purchase-order"></a>Eine Bestellung erstellen

1. Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Bestellung erstellen** die folgenden Werte fest:

    - **Kreditorenkonto:** *104*
    - **Lagerort:** *51*

1. Wählen Sie **OK** aus, um das Dialogfeld zu schließen und die neue Bestellung zu öffnen.
1. Das Raster im Inforegister **Bestellpositionen** enthält eine neue, leere Position. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikelnummer:** *M9203*
    - **Menge** *3*
    - **Einheit:** *PL*

1. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="process-quality-check-receiving"></a>Eingangsqualitätsprüfung durchführen

Nachdem die Bestellung erstellt wurde, kann sie über das Menüelement **PO-Positionseingang** und die Funktionalität der Funktion *Qualitätsprüfung* empfangen werden.

#### <a name="receive-pallet-1"></a>Palette 1 empfangen

1. Melden Sie sich bei der Warehouse-App als ein Benutzer für Lagerort *51* an. (Geben Sie *51* als Benutzer-ID und *1* als Passwort ein.)
1. Gehen Sie zu **Eingehend \> PO-Positionseingang**.
1. Geben Sie im Feld **PONUM** die Bestellnummer ein.
1. Bestätigen Sie die Bestellnummer.
1. Geben Sie im Feld **POSNUM** die Zahl der eingegangenen Bestellposition ein. Da die Bestellung in diesem Szenario nur eine Position enthält, geben Sie *1* im Feld **POSNUM** bei jedem Eingangsschritt ein.
1. Bestätigen Sie die Positionsnummer.
1. Geben Sie im Feld **MENGE** die eingehende Menge ein. Weil die Bestellung in diesem Szenario drei Paletten (*PL*) umfasst und es drei Eingangsschritte gibt, geben Sie für jeden Schritt *1* im Feld **MENGE** ein.
1. Bestätigen Sie die Menge.

    Eine Seite **Qualitätsprüfung** öffnet sich, die aber keine Eingagefelder enthält. Sie hat nur die Bestätigungstaste (Häkchen) unten und die Menütaste (**≡**) oben. (Die Menütaste wird manchmal als Hamburger- oder Hamburgerschaltfläche bezeichnet.) Um den Qualitätsprüfungsprozess zu beschleunigen, bestätigt der Benutzer nur die Seite **Qualitätsprüfung**, wenn die Palette die Qualitätsprüfung passiert.

    ![Qualitätsprüfungsseite](media/quality-check.png "Qualitätsprüfungsseite")

1. Wählen Sie die Bestätigungsschaltfläche, um die Qualitätsprüfung für Palette 1 aus Position 1 als bestanden zu kennzeichnen.

    Die Seite **Bestellungen: Einlagern**, die sich öffnet, enthält die Details der Einlagerungsarbeit:

    - **LOC:** Das System hat den Lagerplatz ermittelt

        Dieser Lagerplatz ist der vorgesehene Einlagerungsort für die eingehende Bestellung.

    - **LP:** Die vom System generierte Ladungsträger-ID
    - **Artikel:** *M9203*
    - **Menge:** *1 PL: 100 Stück*

    Die Artikelbeschreibung wird ebenfalls angezeigt.

1. Bestätigen Sie die Einlagerungsarbeiten.

    Auf der Seite **Aufgabe** der eingehenden Bestellposition erhalten Sie die Meldung „Arbeit abgeschlossen“. Das Feld **POSNUM** ist verfügbar, damit Sie mit dem Eingang der nächsten Palette beginnen können.

#### <a name="receive-pallet-2"></a>Palette 2 empfangen

In diesem Szenario wird Palette 2 abgelehnt.

1. Geben Sie in dem Feld **POSNUM** *1* ein und bestätigen Sie die Positionsnummer.
1. Das Feld **MENGE** ist jetzt verfügbar. Geben Sie *1* ein und bestätigen Sie die Menge.

    Die Seite **Qualitätsprüfung** wird angezeigt. Für diesen Wareneingang wird die Palette aus Qualitätsgründen abgelehnt und am Qualitätslagerplatz *QMS* eingelagert.

1. Wählen Sie die Menütaste (**≡**) oben auf der Seite und wählen Sie dann im Menü die Option **Ablehnen**.
1. Auf der Seite **Aufgabe**, die angezeigt wird, geben Sie **QMS** als Lagerplatz für das *Einlagern* ein, um die Palette zur weiteren Überprüfung zu senden.

    Die Seite **Qualität in der Qualitätsprüfung: Einlagern**, die sich öffnet, enthält die Details der Einlagerungsarbeit:

    - **LOC:** *QMS*

        Dieser Lagerplatz ist der vorgesehene Einlagerungsort für abgelehnte eingehende Qualität.

    - **LP:** Die vom System generierte Ladungsträger-ID
    - **Artikel:** *M9203*
    - **Menge:** *1 PL: 100 Stück*

    Die Artikelbeschreibung wird ebenfalls angezeigt.

1. Bestätigen Sie die Einlagerungsarbeiten.

    Auf der Seite **Aufgabe** der eingehenden Bestellposition erhalten Sie die Meldung „Arbeit abgeschlossen“. Das Feld **POSNUM** ist verfügbar, damit Sie mit dem Eingang der nächsten Palette beginnen können.

Sie haben nun die Qualitätsprüfung abgeschlossen und einen Qualitätsprüfungsauftrag für die abgelehnte Palette erstellt. Um den erstellten Auftrag anzusehen gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsauftrag**.

Jetzt können Tests zu Qualitätsprüfungsaufträge verarbeitet werden. Qualitätstests werden in diesem Thema nicht behandelt.

Weitere Informationen zum Qualitätsmanagement finden Sie unter [Qualitätsmanagement – Übersicht](../inventory/enable-quality-management.md)

#### <a name="receive-pallet-3"></a>Palette 3 empfangen

In diesem Szenario wird Palette 3 angenommen.

1. Geben Sie in dem Feld **POSNUM** *1* ein und bestätigen Sie die Positionsnummer.
1. Das Feld **MENGE** ist jetzt verfügbar. Geben Sie *1* ein und bestätigen Sie die Menge.

    Die Seite **Qualitätsprüfung** wird angezeigt. Für diesen Wareneingang wird die Palette aus Qualitätsgründen angenommen und am Massenlagerplatz eingelagert.

1. Wählen Sie die Bestätigungsschaltfläche, um die Qualitätsprüfung als bestanden zu kennzeichnen.

    Die Seite **Bestellungen: Einlagern**, die sich öffnet, enthält die Details der Einlagerungsarbeit:

    - **LOC:** Das System hat den Lagerplatz ermittelt

        Dieser Lagerplatz ist der vorgesehene Einlagerungsort für die eingehende Bestellung.

    - **LP:** Die vom System generierte Ladungsträger-ID
    - **Artikel:** *M9203*
    - **Menge:** *1 PL: 100 Stück*

    Die Artikelbeschreibung wird ebenfalls angezeigt.

1. Bestätigen Sie die Einlagerungsarbeiten.

    Auf der Seite **Aufgabe** der eingehenden Bestellposition erhalten Sie die Meldung „Arbeit abgeschlossen“. Das Feld **POSNUM** ist verfügbar, damit Sie mit dem Eingang der nächsten Palette beginnen können.

1. Wählen Sie die Menütaste (**≡**) oben auf der Seite und wählen Sie dann im Menü die Option **Abbrechen**, um zum Menü zurückzukehren.

Sie können jetzt die mobile App schließen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]