---
title: Wellenvorlagengruppierung
description: Die Gruppierung von Wellenvorlagen ermöglicht es dem System, mithilfe von Wellenvorlagen-Setups anhand der von Ihnen definierten Kriterien zu bestimmen, wie freigegebene Positionen aufgeteilt und neuen oder vorhandenen Wellen zugewiesen werden sollen. Diese Funktion kann in Lagerorten nützlich sein, in denen Wellen nach bestimmten Kriterien erstellt werden, Manager jedoch Wellen lieber automatisch als manuell erstellen.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: a48e6a81299badf4b811e1cf905beb06099e5a24
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335974"
---
# <a name="wave-template-grouping"></a>Wellenvorlagengruppierung

[!include [banner](../includes/banner.md)]

Die Gruppierung von Wellenvorlagen ermöglicht es dem System, mithilfe von [Wellenvorlagen](tasks/configure-wave-processing.md)-Setups anhand der von Ihnen definierten Kriterien zu bestimmen, wie freigegebene Positionen aufgeteilt und neuen oder vorhandenen Wellen zugewiesen werden sollen. Diese Funktion kann in Lagerorten nützlich sein, in denen Wellen nach bestimmten Kriterien erstellt werden, Manager jedoch Wellen lieber automatisch als manuell erstellen. Es ermöglicht dem System, jede neu freigegebene Lieferung der ersten Welle hinzuzufügen, die übereinstimmende Gruppierungsfeldwerte aufweist. Wird keine Übereinstimmung gefunden, erstellt das System eine neue Welle für die neue Lieferung.

> [!IMPORTANT]
> Die Wellenvorlagengruppierung wird für die Arbeitstypen *Produktionsrohmaterialentnahme* oder *Kanban-Entnahme* nicht unterstützt. Dies liegt daran, dass die Wellengruppierung auf Lieferungen basiert und diese Arbeitstypen keine Lieferungen verwenden.

## <a name="turn-on-the-wave-template-grouping-feature"></a>Funktion für Wellenvorlagengruppierung aktivieren

Bevor Sie die Funktion *Wellenvorlagengruppierung* verwenden können, muss sie für Ihr System aktiviert sein. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Wellenvorlagengruppierung*

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a>Wellenvorlage für Wellenvorlagengruppierung festlegen

Um die Wellenvorlagengruppierung verfügbar zu machen, führen Sie die folgenden Schritte aus, um die [Wellenvorlage](tasks/configure-wave-processing.md) einzurichten.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.
1. Wählen Sie im linken Bereich die einzurichtende Wellenvorlage aus. Wenn Sie sich darauf vorbereiten, das Szenario später in diesem Artikel mithilfe von Demodaten zu bearbeiten, wählen Sie die Vorlage **62 Versandstandard** aus.
1. Klicken Sie auf **Bearbeiten**, um die Seite in den Bearbeitungsmodus zu versetzen.
1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Wellenerstellung automatisieren:** *Ja*
    - **Offenen Wellen zuweisen:** *Ja*
    - **Welle bei Freigabe für Lagerort verarbeiten:** *Nein*

1. Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** aus, um das Abfragedialogfeld zu öffnen.
1. Überprüfen Sie im Abfragedialogfeld auf der Registerkarte **Sortierung** die Sortierkriterien, und stellen Sie sicher, dass es eine Regel gibt, die das Feld enthält, mit dem Sie Ihre Wellen gruppieren möchten.

    Wenn Sie sich darauf vorbereiten, das Szenario mithilfe von Demodaten zu bearbeiten, fügen Sie eine Zeile mit den folgenden Werten hinzu:

    - **Tabelle:** *Lieferungen*
    - **Abgeleitete Tabelle:** *Lieferungen*
    - **Feld:** *Spediteur*

        > [!NOTE]
        > Nachdem Sie diesen Wert ausgewählt haben, wird möglicherweise die folgende Meldung angezeigt: „Das Spediteur-Feld ist kein Indexfeld. Möchten Sie eine Sortierung hinzufügen?“ Wählen Sie **Ja** aus, um eine Sortierung hinzuzufügen.

    - **Suchrichtung:** *Aufsteigend*

1. Wählen Sie **OK** aus, um Ihre Änderungen zu speichern und das Abfragedialogfeld zu schließen.
1. Wählen Sie im Aktivitätsbereich **Wellenvorlagengruppierung** aus.
1. Aktivieren Sie auf der Seite **Wellenvorlagengruppierung** das Kontrollkästchen **Gruppieren nach** für jede Zeile, mit der Sie Ihre Bestellpositionen nach Bedarf in Wellen gruppieren möchten. Wenn Sie sich darauf vorbereiten, das Szenario mithilfe von Demodaten zu bearbeiten, aktivieren Sie das Kontrollkästchen **Gruppieren nach** für die Zeile *Spediteur*.
1. Wählen Sie **Speichern** aus.
1. Schließen Sie die Seite **Wellenvorlagengruppierung**.
1. Wählen Sie **Speichern** aus, um die Vorlage zu speichern.

## <a name="scenario"></a>Szenario

Dieser Abschnitt enthält ein Skript, mit dem Sie lernen können, was diese Funktion tut und wie Sie damit arbeiten.

### <a name="make-sample-data-available"></a>Beispieldaten zur Verfügung stellen

Um dieses Szenario mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

Sie können dieses Szenario auch als Anleitung zur Verwendung dieser Funktion nutzen, wenn Sie an einem Produktionssystem arbeiten. In diesem Fall müssen Sie jedoch Ihre eigenen Werte ersetzen, und es fehlen möglicherweise einige Typen von erforderlichen Datensätzen, die in den Standarddemodaten enthalten sind.

### <a name="scenario-wave-template-grouping"></a>Szenario: Wellenvorlagengruppierung

Dieses Szenario zeigt, wie mithilfe der Wellenvorlagengruppierung automatisch mehrere Wellen erstellt werden, basierend auf Gruppierungskriterien, die in einer Wellenvorlage definiert sind. In diesem Szenario wird die Wellenvorlage im System so eingerichtet, dass eine Welle pro Spediteur erstellt wird.

Bevor Sie beginnen, bereiten Sie Ihre Wellenvorlage wie im Abschnitt [Wellenvorlage für Wellenvorlagengruppierung festlegen](#set-up-template) weiter oben in diesem Artikel beschrieben vor. Wenn Sie für dieses Szenario mit Demodaten arbeiten, müssen Sie die in diesem Verfahren vorgeschlagenen Demodatenwerte verwenden. Dieses Setup gruppiert Ihre Wellen nach dem Spediteur, der für jeden Auftrag festgelegt wurde.

#### <a name="create-sales-order-1"></a>Auftrag 1 erstellen

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - Legen Sie im Inforegister **Kunde** das Feld **Kundenkonto** auf *US-004* fest.
    - Legen Sie im Inforegister **Allgemein** das Feld **Lagerort** auf *62* fest.

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen, und schließen Sie das Dialogfeld **Auftrag erstellen**.
1. Der neue Auftrag wird in der Ansicht **Positionen** geöffnet. Notieren Sie sich die Auftragsnummer.
1. Wechseln Sie zur Ansicht **Kopfzeile**.
1. Legen Sie im Inforegister **Lieferung** im Abschnitt **Transport** die folgenden Werte fest:

    - **Spediteur:** *Luftfracht*
    - **Spediteur:** *Air*

1. Wechseln Sie zurück zur Ansicht **Positionen**.
1. Klicken Sie im Abschnitt **Auftragspositionen** auf **Position hinzufügen**, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Artikelnummer:** *A0002*
    - **Menge** *2*

1. Wählen Sie die neue Bestellposition aus, und klicken Sie dann im Menü **Lagerbestand** über dem Raster auf **Reservierung**.
1. Wählen Sie auf der Seite **Reservierung** im Aktivitätsbereich die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.
1. Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.
1. Sie erhalten eine Informationsnachricht, die die Lieferung und die Welle für diese Bestellung anzeigt. Notieren Sie sich die Wellen-ID-Nummer und die Lieferungs-ID-Nummern.

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a>Welle anzeigen, die aus Auftrag 1 erstellt wurde

1. Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.
1. Wählen Sie die Wellen-ID aus, die aus dem Auftrag erstellt wurde.
1. Wählen Sie den Wellen-ID-Link aus, um die Wellendetailseite zu öffnen.
1. Beachten Sie, dass die Lieferung zum Inforegister **Wellenpositionen** hinzugefügt wurde.

#### <a name="create-sales-order-2"></a>Auftrag 2 erstellen

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - Legen Sie im Inforegister **Kunde** das Feld **Kundenkonto** auf *US-005* fest.
    - Legen Sie im Inforegister **Allgemein** das Feld **Lagerort** auf *62* fest.

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen, und schließen Sie das Dialogfeld **Auftrag erstellen**.
1. Der neue Auftrag wird in der Ansicht **Positionen** geöffnet. Notieren Sie sich die Auftragsnummer.
1. Wechseln Sie zur Ansicht **Kopfzeile**.
1. Legen Sie im Inforegister **Lieferung** im Abschnitt **Transport** die folgenden Werte fest:

    - **Spediteur:** *Blume bewegt sich*
    - **Spediteur:** *STD*

1. Wechseln Sie zurück zur Ansicht **Positionen**.
1. Klicken Sie im Abschnitt **Auftragspositionen** auf **Position hinzufügen**, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Artikelnummer** *A001*
    - **Menge** *1*

1. Wählen Sie die neue Bestellposition aus, und klicken Sie dann im Menü **Lagerbestand** über dem Raster auf **Reservierung**.
1. Wählen Sie auf der Seite **Reservierung** im Aktivitätsbereich die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.
1. Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.
1. Sie erhalten eine Informationsnachricht, die die Lieferung und die Welle für diese Bestellung anzeigt. Notieren Sie sich die Wellen-ID-Nummer und die Lieferungs-ID-Nummern. Beachten Sie, dass sich die Wellen-ID von der Wellen-ID des ersten Auftrags unterscheidet.

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a>Welle anzeigen, die aus Auftrag 2 erstellt wurde

1. Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.
1. Wählen Sie die Wellen-ID aus, die aus dem zweiten Auftrag erstellt wurde.
1. Wählen Sie den Wellen-ID-Link aus, um die Wellendetailseite zu öffnen.
1. Beachten Sie, dass die Lieferung zum Inforegister **Wellenpositionen** hinzugefügt wurde.

Für diese Lieferung wurde eine neue Welle erstellt, da sie einen anderen Spediteur als der erste Auftrag verwendet.

#### <a name="create-sales-order-3"></a>Auftrag 3 erstellen

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - Legen Sie im Inforegister **Kunde** das Feld **Kundenkonto** auf *US-006* fest.
    - Legen Sie im Inforegister **Allgemein** das Feld **Lagerort** auf *62* fest.

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen, und schließen Sie das Dialogfeld **Auftrag erstellen**.
1. Der neue Auftrag wird in der Ansicht **Positionen** geöffnet. Notieren Sie sich die Auftragsnummer.
1. Wechseln Sie zur Ansicht **Kopfzeile**.
1. Legen Sie im Inforegister **Lieferung** im Abschnitt **Transport** die folgenden Werte fest:

    - **Spediteur:** *Luftfracht*
    - **Spediteur:** *Air*

1. Wechseln Sie zurück zur Ansicht **Positionen**.
1. Klicken Sie im Abschnitt **Auftragspositionen** auf **Position hinzufügen**, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Artikelnummer** *A001*
    - **Menge** *1*

1. Wählen Sie die neue Bestellposition aus, und klicken Sie dann im Menü **Lagerbestand** über dem Raster auf **Reservierung**.
1. Wählen Sie auf der Seite **Reservierung** im Aktivitätsbereich die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.
1. Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.
1. Sie erhalten eine Informationsnachricht, die die Lieferung und die Welle für diese Bestellung anzeigt. Notieren Sie sich die Wellen-ID-Nummer und die Lieferungs-ID-Nummern. Die Lieferung wurde der bestehenden Welle aus dem ersten Auftrag zugeordnet.

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a>Welle für Aufträge 1 und 3 anzeigen

1. Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.
1. Wählen Sie die Wellen-ID aus, die aus dem dritten Auftrag erstellt wurde.
1. Wählen Sie den Wellen-ID-Link aus, um die Wellendetailseite zu öffnen.
1. Beachten Sie, dass die Lieferung zum Inforegister **Wellenpositionen** hinzugefügt wurde, zusammen mit der Lieferung für den ersten Auftrag.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]