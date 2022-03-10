---
title: Container-Packstrategien
description: Dieses Thema beschreibt die Unterschiede zwischen den Container-Packstrategien und gibt Beispiele.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4e5faf8e4544b2bcb58f3c578789b2bd379a27b0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572360"
---
# <a name="container-packing-strategies"></a>Container-Packstrategien

[!include [banner](../includes/banner.md)]

Eine *Behälter-Packstrategie* ist eine Strategie, die Sie verwenden können, um Element-Zuordnungen über Container hinweg zu definieren. In diesem Thema werden die Unterschiede zwischen den Strategien *Packen in alle offenen Container* und *Nur in den aktuellen Container packen* erläutert.

- **In alle offenen Container packen** – Das System muss alle offenen Container prüfen, die während des Containerisierungszyklus bereits erstellt wurden, um sicherzustellen, dass das Element in einen von ihnen passt. Während des Packens prüft das System jedes Element, um festzustellen, ob es in einen der zuvor erstellten Container passen wird. Wenn das Element nicht in einen vorhandenen Container passt, erstellt das System einen neuen Container und fährt fort, bis es den gesamten Auftrag gepackt hat.

    Zum Beispiel erfordern *n* bestellte Elemente eine Containerisierung. Im schlimmsten Fall führt das System jedes Mal, wenn es ein Element verarbeitet, das in keinen vorhandenen Container passt, insgesamt (\[(*n* – 1) × (*n* + 1)\] ÷ 2) Überprüfungen durch, um festzustellen, ob das Element in die vorhandenen Container passt.

- **Nur in aktuellen Container packen** – Das System muss nur den zuletzt erstellten Container prüfen, um sicherzustellen, dass das Element in diesen passt. Während des Packens prüft das System jedes Element, um festzustellen, ob es in den zuletzt erstellten Container passt. Wenn das Element nicht in diesen Container passt, erstellt das System einen neuen Container und fährt fort, bis es den gesamten Auftrag gepackt hat.

    Zum Beispiel erfordern *n* bestellte Elemente eine Containerisierung. Im schlimmsten Fall führt das System insgesamt (*n* – 1) Überprüfungen durch, um festzustellen, ob das Element in die Container passt.

## <a name="example-of-the-flow-for-container-packing-strategies"></a>Beispiel für den Flow für Container-Packstrategien

Sie legen die folgenden Elemente für die Containerisierung fest.

| Artikel | Physikalische Dimensionen (Breite × Tiefe × Höhe) | Gewicht |
|---|---|---|
| HDMI-Kabel 6' | 1 × 1 × 1 | 1 |
| HDMI-Kabel 12' | 2 × 1 × 1 | 1 |
| HDMI-Kabel 18' | 3 × 1 × 1 | 2 |

Sie legen auch den folgenden Karton fest, der für die Verpackung verwendet wird.

| Container | Physikalische Dimensionen (Länge × Breite × Höhe) | Gewicht | Volumen |
|---|---|---|---|
| Medium-Box | 6 × 3 × 2 | 10 | 100 |

Schließlich legen Sie eine Bestellung mit den folgenden Produkten und Mengen fest.

| Auftragsposition | Menge |
|---|---|
| HDMI-Kabel 12' | 9 |
| HDMI-Kabel 18' | 8 |
| HDMI-Kabel 6' | 13 |

Die folgende Tabelle fasst zusammen, wie die Containerisierung funktioniert, wenn Sie die Strategie *In alle offenen Container packen* und wenn Sie die Strategie *Nur in den aktuellen Container packen* verwenden.

| In alle offenen Container packen | In den aktuellen Container packen |
|---|---|
| <p>HDMI-Kabel 12':</p><ol><li>Erzeugen Sie einen neuen Container, CONT0001.</li><li>Legen Sie 9 ea in den Container CONT0001.</li></ol> | <p>HDMI-Kabel 12':</p><ol><li>Erzeugen Sie einen neuen Container, CONT0001.</li><li>Legen Sie 9 ea in den Container CONT0001.</li></ol> |
| <p>HDMI-Kabel 18':</p><ol><li>Prüfen Sie, ob das Element in den Container CONT0001 passen kann.</li><li>Erzeugen Sie einen neuen Container, CONT0002.</li><li>Legen Sie 5 Stk. in den Container CONT0002.</li><li>Erstellen Sie einen neuen Container, CONT0003.</li><li>Legen Sie 3 Stk. in den Container CONT0003.</li></ol> | <p>HDMI-Kabel 18':</p><ol><li>Prüfen Sie, ob das Element in den Container CONT0001 passen kann.</li><li>Erzeugen Sie einen neuen Container, CONT0002.</li><li>Legen Sie 5 Stk. in den Container CONT0002.</li><li>Erstellen Sie einen neuen Container, CONT0003.</li><li>Legen Sie 3 Stk. in den Container CONT0003.</li></ol> |
| <p>HDMI-Kabel 6':</p><ol><li>Prüfen Sie, ob das Element in den Container CONT0001 passen kann.</li><li>Legen Sie 1 ea in den Container CONT0001.</li><li>Prüfen Sie, ob das Element in den Container CONT0002 passen kann.</li><li>Prüfen Sie, ob das Element in den Container CONT0003 passt.</li><li>Legen Sie 4 ea in den Container CONT0003.</li><li>Erzeugen Sie einen neuen Container, CONT0004.</li><li>Legen Sie 8 Stk. in den Container CONT0004.</li></ol> | <p>HDMI-Kabel 6':</p><ol><li>Prüfen Sie, ob das Element in den Container CONT0003 passt.</li><li>Legen Sie 4 ea in den Container CONT0003.</li><li>Erzeugen Sie einen neuen Container, CONT0004.</li><li>Legen Sie 9 ea in den Container CONT0004.</li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a>Beispielszenario: Einzelne Aufträge pro Container verpacken

In diesem Abschnitt wird ein Szenario vorgestellt, bei dem das System so festgelegt ist, dass mehrere Bestellungen in einer Sendung zusammengefasst werden. Daher wird die Containerisierung vom Verkaufsauftrag aus durchgeführt, um sicherzustellen, dass jeder Auftrag, der mehrere Produkte enthält, in einen eigenen Container gepackt wird.

Mit dieser Funktionalität können Sie Szenarien handhaben, in denen Sie nur einen Verkaufsauftrag in jeden Container packen müssen, damit das Distributionszentrum volle Container zwischen den Einzelhandelsgeschäften cross-docken kann. Zusätzlich zu den Einzelhandelsszenarien (Auftrag pro Einzelhandelsgeschäft und Versand an ein Distributionszentrum für Cross-Docking) wird diese Technik auch allgemein in schlanken Vorratsketten (Verkaufsauftrag pro Just-in-Time-Produktionslinie) verwendet.

Dieses Szenario zeigt, wie Sie die Anzahl der Container, die beim Packen ausgewertet werden, verringern können, indem Sie die Strategie *Nur in aktuellen Container packen* für die Containerisierung verwenden.

### <a name="prerequisites"></a>Voraussetzungen

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a>Aktivieren Sie die Funktion „Sendungen konsolidieren“ in Ihrem System

Dieses Szenario verwendet die Funktion *Sendungen konsolidieren*. Wenn diese Funktion in Ihrem System noch nicht vorhanden ist, müssen Sie sie mit [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) einschalten.

#### <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Dieses Szenario referenziert Werte und Datensätze, die in den Standard-Demodaten enthalten sind, die für Microsoft Dynamics 365 Supply Chain Management zur Verfügung gestellt werden. Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf **USMF** festlegen, bevor Sie beginnen.

### <a name="inspect-or-create-container-types"></a>Containertypen inspizieren oder erstellen

Um Ihre Containertypen zu inspizieren oder bei Bedarf neue Containertypen zu erstellen, gehen Sie folgendermaßen vor.

1. Gehen Sie zu **Lagerortverwaltung** \> **Einrichten** \> **Behälter** \> **Behältertypen**.
1. Stellen Sie sicher, dass jeder der folgenden Container-Typen in Ihren Demo-Daten vorhanden ist. Bearbeiten oder erstellen Sie die Containertypen nach Bedarf.

    - Container-Typ 1:

        - **Containertyp-Code:** *Box-Large*
        - **Beschreibung:** *Große Box*
        - **Maximales Nettogewicht:** *100*
        - **Volumen:** *400*
        - **Länge:** *4*
        - **Breite:** *10*
        - **Höhe:** *10*

    - Container Typ 2:

        - **Container-Typ-Code:** *Box-Medium*
        - **Beschreibung:** *Medium Box*
        - **Maximales Nettogewicht:** *50*
        - **Volumen:** *200*
        - **Länge:** *2*
        - **Breite:** *10*
        - **Höhe:** *10*

    - Container-Typ 3:

        - **Containertyp-Code:** *Box-Small*
        - **Beschreibung:** *Kleine Box*
        - **Maximales Nettogewicht:** *20*
        - **Volumen:** *100*
        - **Länge:** *1*
        - **Breite:** *10*
        - **Höhe:** *10*

### <a name="inspect-or-create-container-groups"></a>Containergruppen inspizieren oder erstellen

Führen Sie die folgenden Schritte aus, um Ihre Container-Gruppen zu inspizieren oder neue Container-Gruppen zu erstellen, falls diese benötigt werden.

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Container** \> **Containergruppen**.
1. Stellen Sie sicher, dass die folgende Containergruppe in Ihren Demodaten vorhanden ist. Wenn sie nicht vorhanden ist, wählen Sie **Neu**, um sie zu erstellen.

    - **Containergruppen-ID:** *Boxen*
    - **Beschreibung:** *Boxengrößen*

1. Stellen Sie im Inforegister **Details** für die Container-Gruppe *Boxen* sicher, dass die folgenden Zeilen vorhanden sind. Wenn sie nicht vorhanden sind, wählen Sie **Neu**, um sie hinzuzufügen.

    - Position 1:

        - **Sequenznummer:** *1*
        - **Containertyp:** *Box-Groß*
        - **Container-Auslastung in Prozent:** *100*

    - Position 2:

        - **Sequenznummer:** *2*
        - **Container-Typ:** *Box-Medium*
        - **Container-Auslastung in Prozent:** *100*

    - Position 3:

        - **Sequenznummer:** *3*
        - **Container-Typ:** *Box-Small*
        - **Container-Auslastung in Prozent:** *100*

### <a name="create-a-new-container-build-template"></a>Erstellen einer neuen Container-Bauvorlage

Um eine neue Container-Bauvorlage zu erstellen, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Container** \> **Containererstellungsvorlage**.
1. Wählen Sie **Neu**, um eine Container-Vorlage zu erstellen, die die folgenden Einstellungen hat:

    - **Sequenznummer:** *1*
    - **Container-Vorlagen-ID:** *Box*
    - **Containergruppen-ID:** *Boxen*
    - **Basisabfragetypen:** *Verkaufszuordnung Zeile*
    - **Wellenschritt-Code:** *234*
    - **Geteiltes Kommissionieren zulassen:** *Ja*
    - **Packstrategie für Container:** *Nur in den aktuellen Container packen*
    - **Packen nach Einheit der Richtlinie:** *Nein*

1. Während die Zeile für die neue Vorlage noch ausgewählt ist, wählen Sie im Aktionsbereich **Abfrage bearbeiten**.
1. Ein Standard-Dialogfeld für den Abfrage-Editor wird angezeigt. Wählen Sie auf der Registerkarte **Sortierung** die Option **Hinzufügen**, um eine Zeile hinzuzufügen, die die folgenden Einstellungen hat:

    - **Tabelle:** *Temporäre Arbeitstransaktionen*
    - **Abgeleitete Tabelle:** *Temporäre Arbeitstransaktionen*
    - **Feld:** *Bestellnummer*
    - **Suchrichtigung:** *Aufsteigend*

    > [!IMPORTANT]
    > Um zu vermeiden, dass alle anderen geöffneten Container durchlaufen werden, und um den Vorgang zu beschleunigen, indem jeweils nur ein Container geprüft wird, verwenden Sie zusätzlich zur Sortierung nach Auftragsnummer die Strategie *Nur in aktuellen Container packen*. Diese Kombination funktioniert wie eine Arbeitspause bei einer Arbeitsvorlage.

1. Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.
1. Während die Zeile für die neue Vorlage noch ausgewählt ist, wählen Sie **Container-Mischbedingungen** im Aktionsbereich.

    Sie fügen nun eine Beschränkung hinzu, die Elemente aus einem einzigen Auftrag in einen einzigen Container legt. Elemente aus allen anderen Aufträgen werden in einen separaten Container gelegt.

1. Wählen Sie **Neu**, um eine Mischungsbeschränkung zu erstellen, die die folgenden Einstellungen hat:

    - **Tabelle:** *Aufträge*
    - **Feldauswahl:** *VerkaufsId* (Das Feld wird als *Verkaufsauftrag* im Raster angezeigt.)

1. Wählen Sie **OK**, um die Einschränkung hinzuzufügen.
1. Schließen Sie die Seite.

### <a name="set-up-a-wave-template-for-containerization"></a>Eine Wellenvorlage für die Containerisierung festlegen

Um eine Wellenvorlage festzulegen, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.
1. Legen Sie im Listenbereich das Feld **Wellenvorlagentyp** auf *Versand* fest.
1. Wählen Sie die Vorlage **63 Containerisierung** in der Liste aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Suchen Sie im Inforegister **Methoden** in der Spalte **Ausgewählte Methoden** die folgende Position:

    - **Methodenname:** *Containerisierung*
    - **Name:** *Kontainerisierung*

1. Legen Sie das Feld **Wellenschrittcode** für die Zeile auf *234* fest.

### <a name="set-up-a-work-template"></a>Eine Arbeitsvorlage einrichten

Um eine Arbeitsvorlage festzulegen, gehen Sie wie folgt vor.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Legen Sie das Feld **Arbeitsauftragstyp** auf *Verkaufsaufträge* fest.
1. Suchen Sie im Raster **Übersicht** die Arbeitsvorlage, die für das Verpacken einzelner Aufträge pro Container verwendet werden soll, und wählen Sie sie aus. Wählen Sie für dieses Szenario die Vorlage **63 In Container kommissionieren**.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Ein Standard-Dialogfeld für den Abfrage-Editor wird angezeigt. Fügen Sie auf der Registerkarte **Sortierung** die folgenden Zeilen ein:

    - Position 1:

        - **Tabelle:** *Temporäre Arbeitstransaktionen*
        - **Abgeleitete Tabelle:** *Temporäre Arbeitstransaktionen*
        - **Feld:** *Lieferungs-ID*
        - **Suchrichtigung:** *Aufsteigend*

    - Position 2:

        - **Tabelle:** *Temporäre Arbeitstransaktionen*
        - **Abgeleitete Tabelle:** *Temporäre Arbeitstransaktionen*
        - **Feld:** *Bestellnummer*
        - **Suchrichtigung:** *Aufsteigend*

    - Position 3:

        - **Tabelle:** *Temporäre Arbeitstransaktionen*
        - **Abgeleitete Tabelle:** *Temporäre Arbeitstransaktionen*
        - **Feld:** *Container-ID*
        - **Suchrichtigung:** *Aufsteigend*

1. Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.
1. Die folgende Meldung wird angezeigt: „Gruppierung wird zurückgesetzt, fortfahren?“ Wählen Sie **Ja** aus, um fortzufahren.
1. Während die Vorlage **63 Entnahme in Container** noch immer kommissioniert ist, wählen Sie im Aktionsbereich **Arbeitskopfunterbrechungen**.

    Sie werden nun Einstellungen anwenden, um die Arbeit so zu unterbrechen, dass jeder Container im Auftrag mit einem Arbeitsauftrag verknüpft ist.

1. Aktivieren Sie das Kontrollkästchen **Nach diesem Feld gruppieren** für jede Zeile auf der Seite **Arbeitskopf-Unterbrechungen** (**Sendungs-ID**, **Auftragsnummer** und **Container-ID**).
1. Schließen Sie die Seite.

### <a name="set-up-shipment-consolidation-policies"></a>Richtlinien für die Sendungskonsolidierung festlegen

Um eine Richtlinie zur Sendungskonsolidierung festzulegen, gehen Sie folgendermaßen vor.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Für Lagerort freigeben \> Richtlinien zur Lieferungskonsolidierung**.
1. Legen Sie im Listenbereich das Feld **Richtlinientyp** auf *Verkaufsaufträge* fest.
1. Wählen Sie die Richtlinie **Standard** in der Liste aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie im Inforegister **Konsolidierungsfelder** in der Liste **Ausgewählte Felder** die Zeile, in der das Feld **Feldname** auf *Auftragsnummer* festgelegt ist.
1. Wählen Sie die Schaltfläche **Entfernen** aus, ![Links-Pfeil](media/backward-button.png), um das Feld in die Liste **Verbleibende Felder** zu verschieben.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="set-up-physical-dimensions-for-the-product"></a>Festlegen der physikalischen Dimensionen für das Produkt

Um die physikalischen Dimensionen für die Produkte festzulegen, die in diesem Szenario verwendet werden, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie das Produkt, bei dem das Feld **Artikelnummer** auf *A0001* festgelegt ist.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Lagerort** **Physische Dimensionen** aus.
1. Auf der Seite **Physikalische Dimensionen** sollten Sie die folgende Zeile im Raster sehen:

    - **Einheit:** *Stk*
    - **Bruttogewicht:** *3,00*
    - **Breite:** *2,00*
    - **Tiefe:** *2,00*
    - **Höhe:** *4,00*
    - **Volumen:** *16,00*

1. Schließen Sie die Seite.
1. Wählen Sie das Produkt, bei dem das Feld **Artikelnummer** auf *A0002* festgelegt ist.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Lagerort** **Physische Dimensionen** aus.
1. Auf der Seite **Physikalische Dimensionen** sollten Sie die folgende Zeile im Raster sehen:

    - **Einheit:** *Stück*
    - **Bruttogewicht:** *4,00*
    - **Breite:** *3,00*
    - **Tiefe:** *1,00*
    - **Höhe:** *3,00*
    - **Volumen:** *9,00*

### <a name="create-sales-order-1"></a>Auftrag 1 erstellen

Gehen Sie folgendermaßen vor, um einen Auftrag zu erstellen.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Es erscheint ein Dialogfenster zum Erstellen eines neuen Verkaufsauftrags. Legen Sie die folgenden Werte fest:

    - **Debitorenkonto:** *US-001*
    - **Lagerort:** *63*

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.
1. Der neue Auftrag wird geöffnet. Fügen Sie auf dem Inforegister **Verkaufsauftragszeilen** die folgenden Verkaufszeilen hinzu:

    - Position 1:

        - **Artikelnummer** *A001*
        - **Menge** *2*

    - Position 2:

        - **Artikelnummer:** *A0002*
        - **Menge** *2*

1. Markieren Sie die erste Zeile und wählen Sie dann **Bestand \> Reservierung**.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus. Schließen Sie nun die Seite.
1. Wiederholen Sie die beiden vorherigen Schritte für die zweite Zeile.
1. Schließen Sie die Seite.

### <a name="create-sales-order-2"></a>Auftrag 2 erstellen

Um einen zweiten Verkaufsauftrag zu erstellen, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Es erscheint ein Dialogfenster zum Erstellen eines neuen Verkaufsauftrags. Legen Sie die folgenden Werte fest:

    - **Debitorenkonto:** *US-001*
    - **Lagerort:** *63*

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.
1. Der neue Auftrag wird geöffnet. Fügen Sie auf dem Inforegister **Verkaufsauftragszeilen** die folgenden Verkaufszeilen hinzu:

    - Position 1:

        - **Artikelnummer** *A001*
        - **Menge** *4*

    - Position 2:

        - **Artikelnummer:** *A0002*
        - **Menge** *4*

1. Markieren Sie die erste Zeile und wählen Sie dann **Bestand \> Reservierung**.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus. Schließen Sie nun die Seite.
1. Wiederholen Sie die beiden vorherigen Schritte für die zweite Zeile.
1. Schließen Sie die Seite.

### <a name="create-the-load"></a>Erstellen Sie die Ladung

Um für jeden Auftrag, den Sie für dieses Szenario erstellt haben, eine Ladung zu erstellen und diese dann an den Lagerort freizugeben, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Transportverwaltung \> Planung \> Ladungsplanungsworkbench**.
1. Suchen Sie auf der Registerkarte **Verkaufszeilen** alle Verkaufsauftragszeilen aus den Kundenaufträgen, die Sie für dieses Szenario erstellt haben, und wählen Sie sie aus.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Angebot und Nachfrage** in der Gruppe **Hinzufügen** die Option **Zu neuer Ladung** aus. Die ausgewählten Auftragszeilen werden zu einer neuen Ladung hinzugefügt.
1. Wählen Sie im Dialogfeld **Ladungsvorlagenzuordnung** im Feld **Ladungsvorlagen-ID** eine Ladungsvorlage, z. B. *40' Container*.
1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.
1. Suchen Sie im Abschnitt **Ladungen** die Ladung, die Sie gerade erstellt haben, und wählen Sie sie aus.
1. Wählen Sie **Freigabe \> Freigabe an Lagerort**.
1. Wählen Sie im Dialogfeld **Freigeben an Lager** die Option **OK**, um die ausgewählte Ladung an das Lagerort freizugeben.

### <a name="verify-the-shipments-and-containers"></a>Überprüfen der Sendungen und Container

Mit dem folgenden Verfahren können Sie die erstellten Sendungen verifizieren. Verwenden Sie es, um den Auftrag zu überprüfen, den Sie für dieses Szenario erstellt haben, um sicherzustellen, dass Sie die erwarteten Ergebnisse erhalten haben.

1. Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.
1. Suchen Sie die Sendung, die für die Ladung erstellt wurde, die Sie gerade freigegeben haben, und wählen Sie sie aus.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Transportieren** die Option **Container anzeigen**.
1. Bestätigen Sie, dass die Elemente aus den Verkaufsaufträgen in zwei verschiedene Container verpackt wurden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Containerisierung](wave-containerization.md)
