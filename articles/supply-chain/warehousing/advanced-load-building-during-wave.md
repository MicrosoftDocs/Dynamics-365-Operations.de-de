---
title: Erweiterte Ladungserstellung während einer Welle
description: Dieses Thema enthält Informationen zur erweiterten Ladungserstellung während einer Welle, bei der Sendungen während der Wellenausführung automatisch vorhandenen Wellen zugewiesen werden. Daher können Sie aussagekräftige Ladungen erstellen, die LKWs darstellen, ohne die Ladungsplanungs-Workbench verwenden zu müssen.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod,WHSWaveTemplateTable,WHSLoadMixGroup,WHSLoadBuildTemplate, WHSWaveTableListPage, TMSLoadBuildTemplateApply, TMSLoadBuildTemplates, TMSLoadBuildTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 1b75d5cec991b2863e7e0213257ac63d5ab566a6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233198"
---
# <a name="advanced-load-building-during-wave"></a>Erweiterte Ladungserstellung während einer Welle

[!include [banner](../includes/banner.md)]

Die erweiterte Ladungserstellung während Wellen weist Lieferungen während der Wellenausführung automatisch vorhandenen Wellen zu. Daher können Sie aussagekräftige Ladungen erstellen, die LKWs darstellen, ohne die Ladungsplanungs-Workbench verwenden zu müssen. Diese Funktion ist nützlich für Unternehmen, die das Konzept von Ladungen verwenden möchten, um die Lieferung von Waren in einem LKW/Anhänger zu verfolgen und zu planen, wobei sie diese Ladungen jedoch nicht täglich manuell erstellen möchten.

Während der Wellenverarbeitung erstellt das System normalerweise eine neue Ladung für jede Lieferung, der keine Ladung zugewiesen ist. Wenn jedoch die erweiterte Ladungserstellung während Wellen aktiviert ist, weist das System jede nicht zugewiesene Lieferung einer vorhandenen Ladung zu (sofern eine geeignete Ladung vorhanden ist) und neue Ladungen werden nur erstellt, wenn es erforderlich ist. Bei der erweiterten Ladungserstellung während Wellen werden die neuen Ladungen automatisch basierend auf den von Ihnen definierten Kriterien erstellt.

Um diese Funktion zu verwenden, müssen Sie das System folgendermaßen einrichten:

- Erstellen Sie *Wellenvorlagen* inklusive der neuen Methode **buildLoads**. Diese Methode sorgt für die Verfügbarkeit der erweiterten Ladungserstellung während Wellen, die diese Vorlagen verwenden.
- Richten Sie *Ladungserstellungsvorlagen* ein, von denen jede mit einer bestimmten Wellenvorlage und -methode verknüpft ist. Ladungserstellungsvorlagen legen fest, zu welcher Ladung (vorhanden oder neu) die gewellten Ladungspositionen hinzugefügt werden. Sie können Lieferungen basierend auf Kriterien wie der Ladungsvorlage, der Ausrüstung und anderen Feldwerten in der Ladungsposition kombinieren oder trennen.
- Definieren Sie *Ladungsmischgruppen*, um zu steuern, welche Artikel in einer einzigen Ladung kombiniert werden sollen und welche nicht. Sie geben außerdem an, ob die Einschränkung eine Warnung oder einen Fehler erzeugen soll und ob die volumetrische Einschränkung der Ladungsvorlage ausgewertet werden soll.

## <a name="turn-on-advanced-wave-load-building-in-your-system"></a>Aktivieren der erweiterten Ladungserstellung während Wellen in Ihrem System

Bevor Sie die erweiterte Ladungserstellung während Wellen verwenden können, müssen in Ihrem System zwei Funktionen aktiviert sein. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status dieser Funktionen überprüfen und sie gegebenenfalls aktivieren. Im Arbeitsbereich **Funktionsverwaltung** sind die Funktionen wie folgt aufgeführt:

- Funktion zur Ladungserstellung während Wellen:

    - **Module:** *Lagerortverwaltung*
    - **Funktionsname:** *Funktion zur Ladungserstellung während Wellen*

- Organisationsweiter Wellenschrittcode:

    - **Module:** *Lagerortverwaltung*
    - **Funktionsname:** *Organisationsweiter Wellenschrittcode*

### <a name="make-sample-data-available"></a>Beispieldaten zur Verfügung stellen

Um diese Demo mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

Sie können diese Demo auch als Anleitung zur Verwendung dieser Funktion nutzen, wenn Sie an einem Produktionssystem arbeiten. In diesem Fall müssen Sie jedoch Ihre eigenen Werte ersetzen, und es fehlen möglicherweise einige Typen von erforderlichen Datensätzen, die in den Standarddemodaten enthalten sind.

### <a name="make-sure-that-the-scenario-setup-includes-enough-available-inventory"></a>Sicherstellen, dass die Szenarioeinrichtung genügend verfügbaren Bestand umfasst

Wenn Sie mit den **USMF**-Demodaten arbeiten, müssen Sie zunächst sicherstellen, dass Ihr System so eingerichtet ist, dass an jedem relevanten Lagerplatz genügend Bestand vorhanden ist. Für diese Demo wird erwartet, dass am Lagerort folgender Bestand verfügbar ist *62*:

- **Artikel A0001:** 10 Stk.
- **Artikel A0002:** 10 Stk.
- **Artikel M9200:** 10 EA

Artikel **M9200** muss dem Lagerort hinzugefügt werden. Gehen Sie wie in den folgenden Unterabschnitten beschrieben vor, um den Artikelbestand hinzuzufügen.

#### <a name="create-a-new-license-plate-id"></a>Erstellen einer neue Kennzeichen-ID

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Lagerort** \> **Kennzeichen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie in der neuen Zeile im Feld **Kennzeichen** den Wert *LP6203* ein.
1. Wählen Sie **Speichern** aus.

#### <a name="create-a-standard-cost-for-item-m9200-in-site-6"></a>Erstellen von Standardkosten für Artikel M9200 an Standort 6

1. Wechseln Sie zu **Produktinformationsverwaltung** \> **Produkte** \> **Freigegebene Produkte**.
1. Suchen Sie nach **M9200**.
1. Wählen Sie die Zeile für den Artikel aus und klicken Sie dann im Aktivitätsbereich auf der Registerkarte **Kosten verwalten** in der Gruppe **Einrichtung** auf **Artikelpreis**.
1. Wählen Sie auf der Seite **Artikelpreis** die Registerkarte **Ausstehende Preise** aus.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Nachkalkulationstyp:** *Geplante Kosten*
    - **Preistyp:** *Kosten*
    - **Version:** *10*
    - **Standort:** *6*
    - **Preis:** *1,60*

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktivitätsbereich **Ausstehende(n) Preis(e) aktivieren** aus.
1. Wählen Sie die Registerkarte **Aktive Preise** aus, um zu überprüfen, ob der neue Einstandspreis für Standort *6* hinzugefügt wurde.

#### <a name="create-inventory-in-warehouse-62"></a>Erstellen von Bestand für Lagerort 62

1. Wechseln Sie zu **Lagerverwaltung** \> **Journaleinträge** \> **Artikel** \> **Lagerregulierung**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Dialogfeld **Bestandserfassung erstellen** auf dem Inforegister **Überblick** in das Feld **Lagerort** den Wert *62* ein. Übernehmen Sie in allen anderen Feldern die Standardwerte.
1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.
1. Die Seite **Bestandsregulierung** wird geöffnet. Wählen Sie auf dem Inforegister **Erfassungspositionen** die Option **Neu** aus, um eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest. Übernehmen Sie in allen anderen Feldern die Standardwerte.

    - **Artikelnummer:** *M9200*
    - **Lagerplatz:** *bulk-003*
    - **Menge:** Ändern Sie den Wert zu *10*.

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktivitätsbereich **Überprüfen** aus, um auf Fehler zu prüfen.
1. Klicken Sie im Dialogfeld **Erfassung prüfen** auf **OK**, um die Überprüfung zu starten. Sie erhalten eine Nachricht, wenn die Überprüfung abgeschlossen ist.
1. Wählen Sie im Aktivitätsbereich **Buchen** aus, um die Bestandsregulierung zu bestätigen.
1. Klicken Sie im Dialogfeld **Erfassung buchen** auf **OK**, um den Buchungsprozess zu starten. Sie erhalten eine Nachricht, wenn der Buchungsprozess abgeschlossen ist.

## <a name="set-up-advanced-wave-load-building"></a>Einrichten der erweiterten Ladungserstellung während Wellen

### <a name="regenerate-wave-process-methods"></a>Erneutes Generieren von Wellenprozessmethoden

Möglicherweise müssen Sie Ihre Wellenprozessmethoden erneut generieren, um die Ladungserstellungsmethode (**buildLoads**) verfügbar zu machen.

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Wellen** \> **Wellenprozessmethoden**.
2. Überprüfen Sie, ob **buildLoads** in der Liste enthalten ist. Wenn die Methode nicht in der Liste enthalten ist, wählen Sie im Aktivitätsbereich **Methoden erneut generieren** aus, um sie hinzuzufügen.

### <a name="set-up-wave-templates"></a>Einrichten von Wellenvorlagen

Um die erweiterte Ladungserstellung während Wellen nutzen zu können, müssen Sie die Methode **buildLoads** in jede relevante [Wellenvorlage](tasks/configure-wave-processing.md) aufnehmen.

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Wellen** \> **Wellenvorlagen**.
1. Wählen Sie eine Wellenvorlage aus.

    Wenn Sie mit den **USMF**-Demodaten arbeiten, wählen Sie die Vorlage **Standard-62-Lieferung** aus.

1. Klicken Sie im Aktivitätsbereich auf **Bearbeiten**, um die Seite in den Bearbeitungsmodus zu versetzen.
1. Wählen Sie auf dem Inforegister **Methoden** im Raster **Verbleibende Methoden** die Methode **buildLoads** aus.
1. Wählen Sie die Schaltfläche mit dem Pfeil nach rechts aus, um die Methode **buildLoads** in das Raster **Ausgewählte Methoden** zu verschieben.
1. Um einen **Wellenschrittcode** für die Methode **buildLoads** zuzuweisen, müssen Sie zuerst auf der Seite **Wellenschrittcodes** einen Code erstellen. Sie können einen beliebigen Wert verwenden. Sie sollten sich diesen Wert jedoch unbedingt notieren, da Sie ihn später benötigen werden. Gehen Sie folgendermaßen vor, um den Code **WSC2112** zu erstellen.

    1. In der Zeile für die Methode **buildLoads** klicken Sie mit der rechten Maustaste auf den Abwärtspfeil im Feld **Wellenschrittcode** und wählen Sie dann **Details anzeigen** aus.
    1. Wählen Sie auf der Seite **Wellenschrittcodes** im Aktivitätsbereich **Neu** aus.
    1. Geben Sie im Feld **Wellenschrittcode** den Wert *WSC2112* ein.
    1. Geben Sie im Feld **Wellenschrittbeschreibung** den Wert *WSC2112* ein.
    1. Wählen Sie im Feld **Wellenschritttyp** die Option *Ladungserstellung* aus.

1. Klicken Sie auf **Speichern** und schließen Sie die Seite.
1. Wählen Sie in der Zeile für die Methode **buildLoads** im Feld **Wellenschrittcode** den Code aus, den Sie soeben erstellt haben (**WSC2112**).
1. Wählen Sie im Aktionsbereich **Speichern** aus.

> [!NOTE]
> Wellenschrittcodes sind Codes, die Benutzer einrichten und verwenden können, um bestimmte Instanzen von Wellenmethoden mit entsprechenden Vorlagen zu verknüpfen. Die Vorlagen enthalten Vorlagen für die Auffüllung, Containerisierung, Etikettendruck, Auslastungsgebäude und Sortieren.
>
> Wenn keine Wellenschrittcodes verwendet werden, müssen Benutzer Freitext eingeben, um auf eine bestimmte Vorlage aus der Wellenmethodeninstanz zu verweisen. Freier Text ist fehleranfällig, da Benutzer sicherstellen müssen, dass der Wellenschritttext, den sie für eine bestimmte Wellenschrittmethode in einer Wellenvorlage hinzufügen, genau mit dem Wellenschritttext in der Zielvorlage übereinstimmt.
>
> Wellenschrittcodes für einen bestimmten Wellenschritttyp werden auf einer separaten Seite eingerichtet. Für jede Instanz einer Wellenschrittmethode in einer Wellenvorlage, die einen Wellenschrittcode erfordert, muss der Wellenschrittcode in einer Dropdownliste ausgewählt werden. Die Auswahl in einer Dropdownliste ersetzt den freien Texteintrag und hilft, das Risiko und die Auswirkungen des menschlichen Versagens zu verringern. Einstellungscodes werden verwendet, um eine Wellenschrittmethode in einer Wellenvorlage zu einer Zielvorlage für die Methode zu verknüpfen.

### <a name="set-up-load-mix-groups"></a>Einrichten von Ladungsmischgruppen

Ladungsmischgruppen legen Regeln für die Artikeltypen fest, die in einer einzelnen Ladung kombiniert werden können. Sie können so viele Ladungsmischgruppen einrichten, wie Sie benötigen. Um jedoch die erweiterte Ladungserstellung während Wellen verwenden zu können, benötigen Sie mindestens eine. Gehen Sie folgendermaßen vor, um eine Ladungsmischgruppe zu erstellen.

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Ladung** \> **Ladungsmischgruppen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Ladungsgruppe zu erstellen.
1. Geben Sie in das Feld **Ladungsmischgruppen-ID** einen Namen für die neue Gruppe ein.

    Wenn Sie mit den **USMF**-Demodaten arbeiten, legen Sie die folgenden Werte fest:

    - **Ladungsmischgruppen-ID:** *TV*
    - **Beschreibung:** *TV*

1. Wählen Sie im Aktivitätsbereich **Speichern** aus, um das Inforegister **Kriterien für Ladungsmischgruppen** verfügbar zu machen.
1. Wählen Sie auf dem Inforegister **Kriterien für Ladungsmischgruppen** die Option **Neu** aus, um dem Raster eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile in jedem Feld die gewünschten Werte fest. Diese Werte bestimmen die Artikelgruppen, die für die Ladungsmischung berücksichtigt werden.

    Wenn Sie mit den **USMF**-Demodaten arbeiten, wählen Sie *TV & Video* im Feled **Artikelgruppe** aus.

1. Wählen Sie im Aktivitätsbereich **Speichern** aus, um das Inforegister **Einschränkungen für Ladungsmischgruppen** verfügbar zu machen.
1. Wählen Sie auf dem Inforegister **Einschränkungen für Ladungsmischgruppen** die Option **Neu** aus, um dem Raster eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile in jedem Feld die gewünschten Werte fest.

    Wenn Sie mit den **USMF**-Demodaten arbeiten, legen Sie die folgenden Werte fest:

    - **Artikelgruppe:** *CarAudio*
    - **Ladungserstellungsaktion:** *Einschränken* (Dieser Wert verhindert, dass sich Artikel aus der Artikelgruppe **CarAudio** in derselben Ladung befinden wie Artikel aus der Artikelgruppe **TV & Video**.)

1. Arbeiten Sie weiter mit den Regeln, bis Sie alle Kriterien und Einschränkungen hinzugefügt haben, die Sie für die Ladungsmischgruppe benötigen.

Wenn Sie mit den **USMF**-Demodaten arbeiten, sind Sie mit dem Einrichten jetzt fertig.

### <a name="set-up-load-build-templates"></a>Einrichten von Ladungserstellungsvorlagen

Sie können so viele Ladungserstellungsvorlagen einrichten, wie Sie benötigen. Um jedoch die erweiterte Ladungserstellung während Wellen verwenden zu können, benötigen Sie mindestens eine. Gehen Sie folgendermaßen vor, um eine Ladungserstellungsvorlage zu erstellen.

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Ladung** \> **Ladungserstellungsvorlagen für Wellen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest.

    | Feld | Beschreibung | Wert in den USMF-Demodaten |
    |---|---|---|
    | Laufende Nummer | Die Reihenfolge, in der die Vorlage ausgewertet wird. | *1* |
    | Name der Ladungserstellungsvorlage | Geben Sie den eindeutigen Bezeichner der Ladungserstellungsvorlage ein. Sie sollten den Namen der Vorlage eingeben, die Sie zuvor in dieser Einrichtung erstellt oder aktualisiert haben. | *Standard-62-Lieferung* |
    | Wellenschrittcode | Geben Sie den Wellenschrittcode ein, mit dem die Vorlage mit einer Wellenmethode verknüpft wird. Sie sollten den Code eingeben, den Sie für die Methode **buildLoads** ausgewählt haben, als Sie die Wellenvorlage zuvor eingerichtet haben. | *WSC2112* |
    | Ladungsvorlagenkennung | Wählen Sie die Ladungsvorlage aus, die zur Erstellung neuer Ladungen sowie für den Abgleich bei der Zuweisung zu vorhandenen Ladungen verwendet werden soll. Die Ladungsvorlage definiert die maximalen Kennzahlen für Gewicht und Volumen, die für die gesamte Ladung zulässig sind. | *Standardladungsvorlage* |
    | Gerät | Das Arbeitsgerät, das bei der Zuweisung zu vorhandenen Ladungen und zum Auffüllen neu erstellter Ladungen verwendet wird. | Lassen Sie dieses Feld leer. |
    | Ladungsmischgruppen-Kennung | Wählen Sie die Ladungsmischgruppe aus, die verwendet werden soll, wenn der Artikel für die Ladung zugelassen ist. Die Mischgruppe legt Regeln für die Artikeltypen fest, die in einer einzelnen Ladung kombiniert werden können. Sie sollten eine der MIschgruppen auswählen, die Sie zuvor in dieser Einrichtung erstellt haben. | *TV* |
    | Offene Ladungen verwenden | Wählen Sie, ob vorhandene offene Ladungen hinzugefügt werden sollen. Die folgenden Optionen stehen zur Verfügung:<ul><li>**Keine** – Fügen Sie keine offenen Ladungen zu vorhandenen Ladungen hinzu.</li><li>**Beliebige** – Fügen Sie offene Ladungen zu jeglichen vorhandenen Ladungen hinz, die für die Position gültig sind.</li><li>**Zugewiesen** – Fügen Sie der Ladung, die der Welle zugeordnet ist, offene Ladungen hinzu.</li></ul> | *Beliebige* |
    | Ladungen erstellen | Geben Sie an, ob neue Ladungen erstellt werden sollen, wenn keine vorhandenen Ladungen den Kriterien entsprechen. | Ausgewählt (= *Ja*) |
    | Teilen von Lieferungspositionen zulassen | Legen Sie fest, ob eine einzelne Ladungsposition auf mehrere Ladungen aufgeteilt werden kann, wenn die vollständige Position die Höchstkapazität der Ladungsvorlage überschreitet. | Deaktiviert (= *Nein*) |
    | Volumenmetriken überprüfen | Legen Sie fest, ob die Ladungserstellung das Gewicht und Volumen überprüfen soll, während jede Position hinzugefügt wird, um sicherzustellen, dass die volumetrischen Grenzwerte der Ladungsvorlage eingehalten werden. | Deaktiviert (= *Nein*) |

1. Wählen Sie im Aktivitätsbereich **Speichern** aus, um die Option **Abfrage bearbeiten** verfügbar zu machen.
1. Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** aus, um ein Dialogfeld zur Bearbeitung der Abfrage zu öffnen.
1. Wählen Sie im Dialogfeld auf der Registerkarte **Sortierung** die Option **Hinzufügen** aus, um dem Raster eine Zeile hinzuzufügen.
1. Definieren Sie in der neuen Zeile die Sortierregeln, die Sie verwenden möchten. Legen Sie beispielsweise die folgenden Werte fest, um die Suchergebnisse in aufsteigender Reihenfolge nach Bestellnummer zu sortieren:

    - **Tabelle:** *Ladungsdetails*
    - **Abgeleitete Tabelle:** *Ladungsdetails*
    - **Feld:** *Bestellnummer*
    - **Suchrichtigung:** *Aufsteigend*

1. Wählen Sie **OK** aus, um Ihre Änderungen zu speichern und das Dialogfeld zu schließen.
1. Legen Sie auf dem Inforegister **Aufteilen nach** Regeln fest, um zu steuern, wie Ihre Ladungen aufgeteilt werden. In der Regel erfolgt die Aufteilung nach benutzerdefinierten Feldern, die auf die Ladungsposition erweitert wurden, z. B. **Route**, **Tour** oder **Lauf**. Um beispielsweise eine Ladung pro Bestellnummer zu erstellen, aktivieren Sie das Kontrollkästchen **Aufteilen nach** für die Zeile mit den folgenden Werten:

    - **Name der Referenztabelle:** *Ladungsdetails*
    - **Name des Referenzfelds:** *Bestellnummer*

## <a name="scenario"></a>Szenario

Dieses Szenario zeigt, wie sich die zuvor in diesem Thema beschriebenen Einstellungen auf den Lagerortbetrieb auswirken, während ein Auftrag verarbeitet wird. Dieses Szenario verwendet die **USMF**-Demodaten zusammen mit anderen Demowerten, die in diesen Anweisungen zur Einrichtung enthalten sind.

### <a name="create-sales-orders"></a>Aufträge erstellen

1. Wechseln Sie zu **Vertrieb und Marketing** \> **Aufträge** \> **Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um das Dialogfeld **Auftrag erstellen** zu öffnen.
1. Legen Sie im Dialogfeld die folgenden Werte fest:

    - Legen Sie im Inforegister **Kunde** das Feld **Kundenkonto** auf *US-007* fest.
    - Legen Sie im Inforegister **Allgemein** das Feld **Lagerort** auf *62* fest.

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.
1. Ihr neuer Auftrag wird geöffnet. Es sollte eine neue, leere Position im Raster auf dem Inforegister **Auftragspositionen** enthalten. Legen Sie für diese neue Position das Feld **Artikelnummer** auf *A0001* und das Feld **Menge** auf *1* fest.
1. Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** im Aktivitätsbereich **Los reservieren** aus.
1. Klicken Sie auf die Schaltfläche **Schließen** (**X**) in der rechten oberen Ecke der Seite, um zum Auftrag zurückzukehren.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus. Das System erstellt eine Lieferung und fügt sie einer neuen Ladung hinzu, da keine vorhandene Ladung Positionen mit dieser Bestellnummer enthält.

    Sie erhalten Informationsmeldungen zu Arbeit, Welle und Lieferung, die für diesen Auftrag erstellt wurden.

1. Um die Ladungs-, Lieferungs- und Arbeitsdetails in der Verkaufsposition zu bestätigen, wählen Sie zunächst die Position aus. Wählen Sie dann im Menü **Lagerort** über dem Raster die Option **Ladungsdetails**, **Lieferungsdetails** oder **Arbeitsdetails** aus.
1. Wählen Sie im soeben erstellten Auftrag auf dem Inforegister **Auftragspositionen** die Option **Position hinzufügen** aus, um eine weitere Position hinzuzufügen.
1. Legen Sie für die neue Position das Feld **Artikelnummer** auf *A0002* und das Feld **Menge** auf *1* fest.
1. Wiederholen Sie die Positionen 6 bis 9, um die Position zu reservieren und für den Lagerort freizugeben. Das System erstellt eine **neue** Lieferung für die Position, die Sie hinzugefügt haben. Da Sie jedoch die erweiterte Ladungserstellung während Wellen verwenden, fügt das System diese Lieferungs- und Ladungsposition der vorhandenen Welle hinzu. Wenn Sie die erweiterte Ladungserstellung während Wellen nicht verwenden würden, würde das System für die Lieferung eine neue Ladung erstellen.
1. Wählen Sie im soeben erstellten Auftrag auf dem Inforegister **Auftragspositionen** die Option **Position hinzufügen** aus, um eine weitere Position hinzuzufügen.
1. Legen Sie für die neue Position das Feld **Artikelnummer** auf *M9200* und das Feld **Menge** auf *1* fest.
1. Wiederholen Sie die Positionen 6 bis 9, um die Position zu reservieren und für den Lagerort freizugeben. Wie zuvor erstellt das System eine **neue** Lieferung für die Position, die Sie hinzugefügt haben. Da der Artikel jedoch zur Artikelgruppe **CarAudio** gehört, können **die Einschränkungen, die Sie für die Ladungsmischgruppe eingerichtet haben, nicht weitergegeben werden**. Daher wird der Artikel **einer neuen Ladung hinzugefügt**. Wenn Sie in der Ladungserstellungsvorlage keine Ladungsmischgruppe angegeben hätten, wäre diese Lieferung zur ersten Ladung hinzugefügt worden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]