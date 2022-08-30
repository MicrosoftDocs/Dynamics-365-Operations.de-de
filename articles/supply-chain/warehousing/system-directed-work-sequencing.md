---
title: Systemgeleitete Arbeitsabfolgen
description: Dieser Artikel enthält Informationen zu systemgeleiteten Arbeitsabfolgen. Mit dieser Funktion können Sie die Arbeitsaufträge sortieren und filtern, die das System den Benutzern zur Ausführung vorlegt. Dies ist hilfreich in Szenarien, in denen zusätzliche Kriterien erforderlich sind, um den Lagerkommissioniervorgang voranzutreiben.
author: Mirzaab
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 1dab8d8bdace046f0f061713600fd1eab69e7c12
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335464"
---
# <a name="system-directed-work-sequencing"></a>Systemgeleitete Arbeitsabfolgen

[!include [banner](../includes/banner.md)]

Mit systemgeleiteten Arbeitsabfolgen können Sie die Arbeitsaufträge sortieren und filtern, die das System den Benutzern zur Ausführung vorlegt. Dies ist hilfreich in Szenarien, in denen zusätzliche Kriterien (z. B. Versandzeitpunkt, Kommissionierzone, Lagerplatzprofil oder eine Kombination verschiedener Kriterien) erforderlich sind, um den Lagerkommissioniervorgang voranzutreiben.

Diese Funktionalität erweitert die aktuelle systemgeleitete Kommissionierfunktion um eine systemgeleitete Abfragereihenfolge, in der Benutzer eine Sequenz und eine oder mehrere Abfragen einrichten können, die alle erstellten Arbeitsaufträge auswerten. Es werden nur Arbeitsaufträge erfasst und angezeigt, die die Kriterien erfüllen, die im Setup des Menüpunkts für mobile Geräte angegeben sind.

Daher ermöglicht diese Funktionalität eine weitere Optimierung der Lagerkommissioniervorgänge, indem Arbeitsaufträge identifiziert werden, die den angegebenen Kriterien entsprechen, sie dem richtigen Menüpunkt für mobile Geräte zugewiesen und sie dann einem Mitarbeiter basierend auf bestimmten Fähigkeiten, Kommissioniergeräten oder einer anderen Anforderung präsentiert werden.

> [!NOTE]
> Wenn unterschiedliche Kriterien erforderlich sind, müssen mehrere Menüpunkte für Mobilgeräte verwendet werden.

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a>Funktion für organisationsweite systemgeleitete Arbeitsabfolgen aktivieren

Bevor Sie die Funktion für systemgeleitete Arbeitsabfolgen verwenden können, muss sie für Ihr System aktiviert sein. Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Organisationsweite systemgeleitete Arbeitsabfolgen*

## <a name="setup"></a>Einstellung

### <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Um das Szenario mithilfe der in diesem Artikel dargestellten Werte zu bearbeiten, müssen Sie auf einem System arbeiten, auf dem die [Standarddemodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen. Das Szenario verwendet Lagerort *51* aus den Demodaten.

> [!IMPORTANT]
> Bevor Sie die Aufträge für den Lagerort freigeben, stellen Sie sicher, dass die Kommissionierstellen über genügend Lagerbestand für alle Artikel in den Aufträgen verfügen.
>
> Standard-USMF-Daten sollten dieses Szenario unterstützen. Wenn Sie keine Demodaten verwenden, überprüfen Sie die Einstellung **Lagerplatzrichtlinie**, um zu erfahren, welche Kommissionierorte für die Auftragskommissionierung verwendet werden. Wenn Sie den Lagerbestand anpassen müssen, können Sie manuelle Bewegungen erstellen, Wiederbeschaffung verwenden oder einen anderen Flow verwenden.

### <a name="set-up-a-mobile-device-menu-item"></a>Menüpunkt für mobiles Gerät einrichten

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie in der Liste der Menüpunkte für mobile Geräte die Option **Verkaufsauswahl – System** aus. Der gewünschte Menüpunkt sollte bereits vorhanden sein. 
1. Überprüfen Sie die folgenden Einstellungen:

    - Im Inforegister **Allgemein** sollte das Feld **Geleitet von** auf *Systemgeleitet* festgelegt sein.
    - Das Inforegister **Arbeitsklassen** sollte die folgenden Einstellungen anzeigen.

        | Arbeitsklassenkennung | Arbeitsauftragstyp |
        |---|---|
        | Verk. | Aufträge |
        | SO-Entnahme | Aufträge |

1. Wählen Sie im Aktivitätsbereich **Systemgeleitete Arbeitsabfolgeabfragen** aus.
1. Wählen Sie **Bearbeiten** aus.
1. Löschen Sie die vorhandene Position, und bestätigen Sie die Aktivität durch Auswahl von **Ja**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Position zu erstellen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Sequenznummer:** *1*
    - **Beschreibungsfeld:** *Arbeitsmenge unter 20 und absteigend*

1. Wählen Sie **Speichern** aus.
1. Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** aus
1. Erweitern Sie auf der Registerkarte **Verknüpfungen** die Verknüpfungshierarchie, um die Tabelle **Arbeitspositionen** anzuzeigen.
1. Wählen Sie die Tabellenverknüpfung **Arbeitspositionen** aus.
1. **Tabellen-Join hinzufügen** auswählen.
1. Suchen Sie in der angezeigten Liste die Zeile mit den folgenden Einstellungen, und wählen Sie sie aus:

    - **Verknüpfungsmodus:** *n:1*
    - **Beziehung:** *Lagerplätze (Lagerplatz)*

1. Wählen Sie **Auswählen**.

    Lagerplätze werden der Tabellenverknüpfung hinzugefügt.

1. Wählen Sie auf der Registerkarte **Sortieren** die Option **Hinzufügen** aus, um eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Tabelle:** *Arbeitspositionen*
    - **Abgeleitete Tabelle:** *Arbeitspositionen*
    - **Feld:** *Arbeitsmenge* (Wählen Sie im angezeigten Meldungsfeld die Option **Ja** aus, um diesem Feld eine Sortierung hinzuzufügen.)
    - **Suchrichtung:** *Absteigend*

1. Wählen Sie die Registerkarte **Bereich**.

    Wenn nur bestimmte Arbeitskriterien in die Abfolge einbezogen werden sollen, können Sie diese auf der Registerkarte **Bereich** angeben. In diesem Beispiel möchten Sie nur Arbeiten einbeziehen, bei denen die Menge weniger als 20 EA beträgt (die niedrigste Maßeinheit).

    Beachten Sie, dass einige Positionen bereits enthalten sind. Diese Positionen sollten nicht entfernt werden.

1. Wählen Sie **Hinzufügen** aus, um eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Tabelle:** *Arbeitspositionen*
    - **Abgeleitete Tabelle:** *Arbeitspositionen*
    - **Feld:** *Bestandsarbeitsmenge*
    - **Kriterien:** *\<20* (weniger als 20)

1. Wählen Sie **Hinzufügen** aus, um eine weitere Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Tabelle:** *Arbeitspositionen*
    - **Abgeleitete Tabelle:** *Arbeitspositionen*
    - **Feld:** *Arbeitstyp*
    - **Kriterien:** *Entnahme*

1. Wählen Sie **Hinzufügen** aus, um eine weitere Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Tabelle:** *Lagerorte*
    - **Abgeleitete Tabelle:** *Lagerorte*
    - **Feld:** *Lagerortprofilkennung*
    - **Kriterien:** *!STAGE*

        > [!IMPORTANT]
        > Stellen Sie sicher, dass das Ausrufezeichen (*!*) vor *STAGE* steht.

1. Wählen Sie **OK** aus, um die Abfrage zu speichern und zu schließen.
1. Wählen Sie **Speichern** aus.
1. Schließen Sie die Seite, um zur Seite **Menüpunkte für mobile Geräte** zurückzukehren.

> [!NOTE]
> Dieses Setup definiert die Kriterien, anhand derer berechtigte Arbeiten dem Menüpunkt für mobile Geräte zugeführt werden. Wenn Sie der Abfrage weitere Kriterienpositionen hinzufügen, verwendet das System zuerst die Abfrageposition mit der niedrigsten Sequenznummer. Mit anderen Worten, alle berechtigten Arbeiten für Sequenznummer 1 werden dem Benutzer zuerst präsentiert, und dann alle Arbeiten für Sequenznummer 2. Wenn ein bestimmter Bereich und eine bestimmte Sortierung zusammen verwendet werden müssen, sollten sie daher in derselben systemgeleiteten Arbeitsabfolgeabfrage angegeben werden.
>
> Dieses Setup erfasst alle Arbeiten mit mindestens einer Position, in der die Menge weniger als 20 EA beträgt. Wenn die Arbeit eine Position hat, in der die Menge genau 20 EA oder mehr als 20 EA beträgt, ist sie gültig, vorausgesetzt, sie hat auch mindestens eine Position, in der die Menge weniger als 20 EA beträgt.

### <a name="location-directives"></a>Lagerplatzrichtlinien

Wenn Sie Standard-Contoso-Daten verwenden, sind für die Abfrage der Lagerplatzrichtlinienaktivität keine Änderungen erforderlich. Erstellen Sie jedoch eine neue Lagerplatzrichtlinie, um sicherzustellen, dass die Lagerplatzrichtlinien die Artikel in den Aufträgen erfassen, wenn Sie die Funktion in einer Nicht-Contoso-Umgebung anwenden. Führen Sie die folgenden Schritte aus, um die Einstellungen in der Demoumgebung zu überprüfen.

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Lagerplatzrichtlinien**.
1. Wählen Sie im Feld **Arbeitsauftragsart** *Arbeitsaufträge* aus.
1. Wählen Sie die Lagerplatzrichtlinie namens *51 Entnahme* aus.
1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Position für die Aktivität **Entnahme** aus.
1. Wählen Sie **Abfrage bearbeiten** über dem Raster aus.
1. Überprüfen Sie die Abfrage **Bereich**.

    1. Suchen Sie die Position, in der das Feld **Feld** auf *Lagerplatz* festgelegt ist.
    2. Stellen Sie sicher, dass das Feld **Kriterien** leer ist (d. h., es gibt keine Einschränkungen).

## <a name="scenario"></a>Szenario

### <a name="create-sales-order-picking-work"></a>Auftragskommissionierarbeit erstellen

Bevor eine systemgeleitete Kommissionierung ausgeführt wird, sollten einige ausgehende Arbeiten erstellt werden. In diesem Szenario erstellen Sie vier Aufträge, die auf den angegebenen systemgeleiteten Arbeitsabfolgeabfragen basieren.

Sie reservieren Lagerbestandsmengen für jeden Auftrag. Deshalb kann reservierter Lagerbestand nicht für andere Aufträge aus dem Lagerort entnommen werden, es sei denn, die gesamte Lagerreservierung oder ein Teil davon wird storniert.

Anschließend geben Sie jeden Auftrag für den Lagerort frei, um die ausgehende Arbeit zu erstellen.

#### <a name="sales-order-1"></a>Auftrag 1

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um Auftrag 1 zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - Legen Sie im Abschnitt **Kunde** das Feld **Kundenkonto** auf *US-004* fest.
    - Legen Sie im Abschnitt **Allgemein** das Feld **Lagerort** auf *51* fest.

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen. Notieren Sie sich die Auftragsnummer.
1. Fügen Sie dem neuen Auftrag eine Position hinzu, und legen Sie die folgenden Werte fest:

    - **Artikelnummer:** *M9200*
    - **Menge** *20*

1. Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um den Bestand zu reservieren.
1. Schließen Sie die Seite **Reservierung**.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**, um Arbeit für den Lagerort zu erstellen.

    Sie erhalten Informationsnachrichten mit der Wellen-ID und den Lieferungs-IDs, die für den Auftrag erstellt wurden.

#### <a name="sales-order-2"></a>Auftrag 2

1. Wählen Sie im Aktivitätsbereich **Neu** aus, um Auftrag 2 zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-007*
    - **Lagerort:** *51*

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen. Notieren Sie sich die Auftragsnummer.
1. Fügen Sie dem neuen Auftrag eine Position hinzu, und legen Sie die folgenden Werte fest:

    - **Artikelnummer:** *M9200*
    - **Menge** *5*

1. Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen, und legen Sie die folgenden Werte fest:

    - **Artikelnummer:** *M9201*
    - **Menge** *1*

1. Reservieren Sie Lagerbestand für beide Positionen.
1. Geben Sie den Auftrag für den Lagerort frei.

#### <a name="sales-order-3"></a>Auftrag 3

1. Wählen Sie im Aktivitätsbereich **Neu** aus, um Auftrag 3 zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-009*
    - **Lagerort:** *51*

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen. Notieren Sie sich die Auftragsnummer.
1. Fügen Sie dem neuen Auftrag eine Position hinzu, und legen Sie die folgenden Werte fest:

    - **Artikelnummer:** *M9200*
    - **Menge** *7*

1. Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen, und legen Sie die folgenden Werte fest:

    - **Artikelnummer:** *M9202*
    - **Menge** *8*

1. Reservieren Sie Lagerbestand für beide Positionen.
1. Geben Sie den Auftrag für den Lagerort frei.

#### <a name="sales-order-4"></a>Auftrag 4

1. Wählen Sie im Aktivitätsbereich **Neu** aus, um Auftrag 4 zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-010*
    - **Lagerort:** *51*

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen. Notieren Sie sich die Auftragsnummer.
1. Fügen Sie dem neuen Auftrag eine Position hinzu, und legen Sie die folgenden Werte fest:

    - **Artikelnummer:** *M9200*
    - **Menge** *25*

1. Wählen Sie **Position hinzufügen** aus, um eine zweite Position hinzuzufügen, und legen Sie die folgenden Werte fest:

    - **Artikelnummer:** *M9202*
    - **Menge** *10*

1. Reservieren Sie Lagerbestand für beide Positionen.
1. Geben Sie den Auftrag für den Lagerort frei.

### <a name="get-work-ids-for-the-work-that-was-created"></a>Arbeits-IDs für die erstellte Arbeit abrufen

1. Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.
1. Filtern Sie das Feld **Lagerort**, sodass nur Arbeit für den Lagerort *51* gezeigt wird.
1. Es sollten vier Arbeits-IDs erstellt worden sein. Notieren Sie sich die Arbeits-ID für jeden Auftrag.

    | Auftragskennung | Arbeitskennung | Arbeitsmenge |
    |---|---|---|
    | Auftrag 1 | Arbeits-ID 1 | 20 EA |
    | Auftrag 2 | Arbeits-ID 2 | 6 EA (Summe beider Positionen) |
    | Auftrag 3 | Arbeits-ID 3 | 15 EA (Summe beider Positionen) |
    | Auftrag 4 | Arbeits-ID 4 | 35 EA (Summe beider Positionen) |

Stellen Sie vor dem Ausführen des Flows auf dem mobilen Gerät sicher, dass sich nur die gerade erstellte Arbeit im Status *Öffnen* für Lagerort *51* und den Arbeitsauftragstyp *Auftrag* befindet. Andernfalls können die Testergebnisse variieren, da die systemgeleitete Kommissionierung alle berechtigten Arbeiten umfasst.

1. Gehen Sie zu **Lagerortverwaltung \> Arbeit \> Ausgehend \> Offene Verkaufsarbeit**.
1. Filtern Sie im Raster **Offene Verkaufsarbeit** das Feld **Lagerort**, sodass nur Arbeit für den Lagerort *51* gezeigt wird.
1. Stellen Sie sicher, dass nur die vier zuvor erstellten Arbeits-IDs angezeigt werden.
1. Schließen Sie die Seite **Arbeit**.

### <a name="mobile-device-flow-execution"></a>Flowausführung für mobile Geräte

Basierend auf dem Setup versorgt das System die Benutzerarbeit, die von der höchsten Arbeitspositionsmenge zur niedrigsten sortiert ist. Die Menge in jeder Position beträgt weniger als 20 EA.

Denken Sie daran, dass dieses Setup alle Arbeiten mit mindestens einer Position erfasst, in der die Menge weniger als 20 EA beträgt. Wenn die Arbeit eine andere Position hat, in der die Menge genau 20 EA oder mehr als 20 EA beträgt, ist sie daher auch gültig.

#### <a name="mobile-app"></a>Mobile App

1. Melden Sie sich bei der Warehouse-App als ein Benutzer im Lagerort *51* an.
1. Gehen Sie zu **Ausgehend \> Verkaufsauswahl – System**.

    Der Auswahlschritt für die Arbeits-ID *4* wird vorgestellt. Diese Arbeits-ID wird aufgrund des Setups der systemgeleiteten Abfragereihenfolge zuerst angezeigt, in der Sie angegeben haben, dass die Arbeit basierend auf der absteigenden Arbeitspositionsmenge sequenziert werden soll.

1. Vervollständigen Sie die erforderliche Entnahme und Einlagerung, um die Arbeits-ID zu schließen.

    Als Nächstes wird Arbeits-ID *3* vorgestellt. Eine der Arbeitspositionen befindet sich als Nächstes in der Sequenz, basierend auf der Arbeitspositionsmenge.

1. Vervollständigen Sie die Entnahme und Einlagerung, um die Arbeits-ID zu schließen.

    Als Nächstes wird Arbeits-ID *2* vorgestellt. Die Auswahlposition dieser Arbeit folgt als Nächstes in der Sequenz.

1. Vervollständigen Sie die Entnahme und Einlagerung, um die Arbeits-ID zu schließen.

    Es sollten Ihnen keine weiteren Arbeiten vorgelegt werden. Arbeits-ID *1* ist für diesen Menüpunkt für mobile Geräte nicht berechtigt, da in der Abfrage angegeben wird, dass Arbeitskopfzeilen nur berücksichtigt werden, wenn die Menge in den Arbeitspositionen weniger als 20 EA beträgt.

## <a name="tips"></a>Tipps

Die systemgeleiteten Arbeitsabfolgeabfragen sind *inklusive*. Es ist wichtig, dass Sie sich bei einigen Setups an diese Tatsache erinnern. Sie möchten beispielsweise, dass ein bestimmter Menüpunkt Arbeit nur dort verarbeitet, wo sich die Arbeitseinheit *EA* befindet, und Sie geben diese Einschränkung auf der Registerkarte **Bereich** der Abfrage an. In diesem Fall werden alle Arbeiten, bei denen für mindestens eine Arbeitsposition die Arbeitseinheit auf *EA* festgelegt ist, dem Arbeiter zugeführt. Daher kann diese Arbeit auch Arbeiten umfassen, bei denen Arbeitspositionen eine andere Arbeitseinheit als *EA* haben (wie *Kiste* oder *Palette*). Die Abfrage schließt nur Arbeiten aus, bei denen für keine Arbeitsposition die Arbeitseinheit auf *EA* festgelegt ist.

Daher wurde im Beispiel aus diesem Szenario die Arbeits-ID *4* auch von der Abfrage erfasst. Bei der Erstellung wurden zwei Positionen hinzugefügt: eine für 25 EA und eine für 10 EA. Die Arbeit wurde dem Benutzer weiterhin präsentiert, da mindestens eine Arbeitsposition eine Menge von weniger als 20 EA aufweist.

Je nach Szenario können Sie dieses Verhalten mithilfe von Arbeitspausen verhindern.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]