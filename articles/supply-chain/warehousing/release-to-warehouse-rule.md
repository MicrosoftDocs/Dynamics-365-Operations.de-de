---
title: Lagerortfreigaberegel
description: Dieses Thema enthält Informationen zur Lagerortfreigaberegel-Funktion, die Flexibilität bei der Freigabe an den Lagerort bietet. Es wird eine Konfigurationsoption hinzugefügt, die steuert, ob das System die Freigabe teilweise reservierter Auftragspositionen zulässt.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 8c4775ca3f44486fd3cd557df49acd229048d186
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996172"
---
# <a name="release-to-warehouse-rule"></a>Lagerortfreigaberegel

[!include [banner](../includes/banner.md)]

Die Funktion *Lagerortfreigaberegel* bietet Flexibilität bei der Freigabe an den Lagerort. Es wird eine Konfigurationsoption für jeden Lagerort hinzugefügt. Mit dieser Option können Sie angeben, ob teilweise reservierte Bestellpositionen für diesen Lagerort freigegeben werden können. Die Funktion arbeitet mit erweiterten Crossdocking-Funktionen zusammen, wobei ein Teil einer Bestellpositionsmenge gegen eine Bezugsquelle gekennzeichnet ist, der verbleibende Teil jedoch im Lagerort verarbeitet werden kann. Daher kann die Position freigegeben werden, damit die Lagerortverarbeitung der verfügbaren Lagerbestandsmenge fortgesetzt werden kann.

## <a name="turn-on-and-initialize-the-release-to-warehouse-rule-feature"></a>Lagerortfreigaberegel-Funktion aktivieren und initialisieren

### <a name="turn-on-the-feature"></a>Aktivieren Sie die Funktion

Bevor Sie die Funktion *Lagerortfreigaberegel* verwenden können, muss sie in Ihrem System aktiviert sein. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Lagerortfreigaberegel*

### <a name="initialize-the-feature"></a>Funktion initialisieren

Nachdem die Funktion in Ihrem System aktiviert wurde, müssen Sie sie initialisieren, um die Regel für alle Lagerorte auf den richtigen Anfangsstatus zu setzen.

- Für Lagerorte, die nicht für die Lagerortverwaltung aktiviert sind, wird die Regel zunächst auf **Nicht zutreffend** festgelegt.
- Für Lagerorte, die für die Lagerortverwaltung aktiviert sind, wird die Regel zunächst auf **Teilweise Reservierung zulassen** festgelegt.

Führen Sie die folgenden Schritte aus, um die Funktion zu initialisieren und die Lagerortfreigaberegel für alle Lagerorte festzulegen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.
1. Wählen Sie auf der Seite **Lagerortverwaltungsparameter** auf der Registerkarte **Allgemein** im Abschnitt **Unternehmensdaten** den Link für die Regel **Lagerortfreigabe initialisieren** aus. (Wenn dieser Link nicht angezeigt wird, ist die Funktion entweder nicht aktiviert oder wurde bereits initialisiert.)
1. Wenn Sie aufgefordert werden, die Aktivität zu bestätigen, wählen Sie **Ja** aus, um die Funktion zu initialisieren.

## <a name="set-the-release-to-warehouse-rule-for-each-warehouse"></a><a name="set-option-warehouse"></a>Lagerortfreigaberegel für jeden Lagerort festlegen

Nachdem die Funktion aktiviert und initialisiert wurde, haben alle Ihre Lagerorte eine Grundeinstellung, wie im vorherigen Abschnitt beschrieben. Sie können diese Einstellung für einzelne Lagerorte ändern, indem Sie die folgenden Schritte ausführen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerorte**.
1. Wählen Sie den zu konfigurierenden Lagerort aus.
1. Klicken Sie auf **Bearbeiten**, um die Seite in den Bearbeitungsmodus zu versetzen.
1. Im Inforegister **Lagerort** im Abschnitt **Reservierungen** steuert das Feld **Anforderung für Lagerbestandsreservierung**, ob eine teilweise Freigabe von Aufträgen zulässig ist. Wählen Sie einen der folgenden Werte aus:

    - **Nicht zutreffend** – Wenn die Funktion zum ersten Mal aktiviert und initialisiert wird, wird dieser Wert automatisch allen Lagerorten zugewiesen, die nicht für die Lagerortverwaltung aktiviert sind. Er kann nicht geändert werden. Dieser Wert ist nicht für Lagerorte verfügbar, die für die Lagerortverwaltung aktiviert sind.
    - **Teilweise Reservierung zulassen** – Aufträge können freigegeben werden, wenn eine beliebige Menge reserviert ist. Das System bewertet, ob die nicht reservierte Menge für ein erweitertes Crossdocking markiert werden soll, und markiert diese Menge nach Bedarf. Wenn keine Markierung vorhanden ist, erstellt das System nur Arbeiten für die reservierte Menge. Wenn die Funktion zum ersten Mal aktiviert und initialisiert wird, wird dieser Wert automatisch allen Lagerorten zugewiesen, die für die Lagerortverwaltung aktiviert sind. Dieser Wert ist nicht für Lagerorte verfügbar, die nicht für die Lagerortverwaltung aktiviert sind.
    - **Vollständige Reservierung erforderlich** – Aufträge können nur freigegeben werden, wenn die gesamte Menge reserviert ist. Sie können nicht freigegeben werden, wenn die Gesamtmenge weder physisch reserviert noch für das Crossdocking geplant ist. Dieser Wert ist nicht für Lagerorte verfügbar, die nicht für die Lagerortverwaltung aktiviert sind.

1. Wählen Sie **Speichern** aus.

## <a name="scenarios"></a>Szenarien

Dieser Abschnitt enthält zwei Szenarien, in denen Sie lernen können, was die Funktion tut und wie sie verwendet wird.

### <a name="make-sample-data-available"></a>Beispieldaten zur Verfügung stellen

Um diese Szenarien mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

Sie können diese Szenarien auch als Anleitung für die Funktion verwenden, wenn Sie an einem Produktionssystem arbeiten. In diesem Fall müssen Sie jedoch Ihre eigenen Werte ersetzen, und es fehlen möglicherweise einige Typen von erforderlichen Datensätzen, die in den Standarddemodaten enthalten sind.

### <a name="scenario-1-require-full-release-no-planned-cross-docking"></a><a name="scenario1"></a>Szenario 1: Vollständige Freigabe erforderlich (kein geplantes Crossdocking)

Dieses Szenario zeigt, wie die Funktion für Lagerorte funktioniert, die auf **Vollständige Reservierung erforderlich** festgelegt sind.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerorte**.
1. Legen Sie für Lagerort _62_ das Feld **Anforderung für Lagerbestandsreservierung** auf **Vollständige Reservierung erforderlich** fest, wie im Abschnitt [Lagerortfreigaberegel für jeden Lagerort festlegen](#set-option-warehouse) weiter oben in diesem Thema beschrieben.
1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus, um einen Auftrag zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - Legen Sie im Inforegister **Kunde** das Feld **Kundenkonto** auf _US-004_ fest.
    - Legen Sie im Inforegister **Allgemein** das Feld **Lagerort** auf _62_ fest.

1. Wählen Sie **OK** aus, um den neuen Auftrag zu erstellen und das Dialogfeld zu schließen.
1. Ihr neuer Auftrag wird geöffnet. Es enthält eine leere Position im Raster im Abschnitt **Auftragspositionen**. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikelnummer** *A001*
    - **Menge** *2*

1. Wählen Sie **Position hinzufügen** aus, um eine neue Position hinzuzufügen, und legen Sie die folgenden Werte fest:

    - **Artikelnummer:** *A0002*
    - **Menge** *2*

1. Wählen Sie die erste Bestellposition aus, und klicken Sie dann im Menü **Lagerbestand** über dem Raster auf **Reservierung**.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.
1. Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.
1. Reservieren Sie nicht die zweite Bestellposition.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.
1. Beachten Sie, dass Sie die folgende Fehlermeldung erhalten: „Die volle Menge muss physisch reserviert werden.“ Daher erstellt das System keine Arbeit, Lieferung oder Ladung für den Auftrag.

    > [!NOTE]
    > Sie erhalten dieselbe Fehlermeldung, wenn Sie die zweite Position teilweise reservieren.

### <a name="scenario-2-allow-partial-release"></a>Szenario 2: Teilweise Freigabe zulassen

Dieses Szenario zeigt, wie die Funktion für Lagerorte funktioniert, die auf **Teilweise Freigabe zulassen** festgelegt sind.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerorte**.
1. Legen Sie für Lagerort _62_ das Feld **Anforderung für Lagerbestandsreservierung** auf **Teilweise Reservierung zulassen** fest, wie im Abschnitt [Lagerortfreigaberegel für jeden Lagerort festlegen](#set-option-warehouse) weiter oben in diesem Thema beschrieben.
1. Wie im [vorherigen Szenario](#scenario1), gehen Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**, und erstellen Sie einen Auftrag für das Kundenkonto _US-004_ vom Lagerort _62_. Fügen Sie die folgenden zwei Bestellpositionen hinzu:

    - **Position 1:** Legen Sie das Feld **Artikelnummer** auf _A0001_, das Feld **Menge** auf _2_ und das Feld **Einheit** auf _Stck_ fest.
    - **Position 2:** Legen Sie das Feld **Artikelnummer** auf _A0002_, das Feld **Menge** auf _2_ und das Feld **Einheit** auf _Stck_ fest.

1. Wie im [vorherigen Szenario](#scenario1), reservieren Sie die volle Menge für Bestellposition 1, aber reservieren Sie nicht Bestellposition 2.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.
1. Beachten Sie, dass Sie diesmal keine Fehlermeldung erhalten. Stattdessen erstellt das System nach Bedarf Arbeit, Lieferungen und Ladungen und zeigt die Ergebnisse an.
1. Um die Liefer-, Ladungs- und Arbeitsinformationen anzuzeigen, verwenden Sie die Optionen im Menü **Lagerort** über dem Raster:

    - **Position 1:** Drei Optionen stehen zur Verfügung: **Lieferdetails**, **Ladungsdetails** und **Arbeitsdetails**. Wählen Sie jede Option aus, um die Details der Lieferung, Ladung und Arbeit anzuzeigen, die erstellt wurden, als der Auftrag für den Lagerort freigegeben wurde.
    - **Position 2:** Nur die Option **Arbeitsdetails** ist verfügbar. Wählen Sie es aus und beachten Sie, dass keine Arbeit erstellt wurde, da kein Lagerbestand reserviert wurde. Daher wurde auch keine Lieferung oder Ladung erstellt.

> [!NOTE]
> Das gleiche Ergebnis wird erwartet, wenn die zweite Position teilweise reserviert ist. In diesem Fall wird Arbeit für die reservierte Positionsmenge erstellt, nicht jedoch für die nicht reservierte Menge.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]