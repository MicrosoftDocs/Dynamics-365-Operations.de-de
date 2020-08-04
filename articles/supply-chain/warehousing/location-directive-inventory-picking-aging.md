---
title: Fälligkeit für Lagerplatzrichtlinie-Bestandsentnahme
description: In diesem Thema wird erläutert, wie Sie während der Kommissionierung die Lagerplatzrichtlinienstrategien FIFO (First In, First Out) und LIFO (Last In, First Out) verwenden.
author: mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 56a3a838374bb1cd0f4b839124ada7114205c1e7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597287"
---
# <a name="location-directive-inventory-picking-aging"></a>Fälligkeit für Lagerplatzrichtlinie-Bestandsentnahme

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie während der Kommissionierung die Lagerplatzrichtlinienstrategien FIFO (First In, First Out) und LIFO (Last In, First Out) verwenden. Diese Strategien arbeiten mit den Fälligkeitsdaten zusammen, die für Lagerplätze aufgezeichnet werden, um zu verfolgen, wann der Bestand zum ersten Mal in das Lager gelangt ist. Die Funktion *Fälligkeit für Standortrichtlinie-Bestandsentnahme* verwendet das Datum am Lagerplatz, um die Fälligkeit zu bestimmen. Die Funktion *Status des Lagerplatzes an einem Lagerort* aktualisiert das Datum am Lagerplatz basierend auf dem Datum auf dem Kennzeichen.

Sie können FIFO- und LIFO-Strategien verwenden, um Artikel mit und ohne Chargenverfolgung zu versenden, basierend auf dem Datum, an dem der Bestand in das Lager gelangt ist. Diese Funktion kann besonders nützlich sein für Bestände ohne Chargenverfolgung, bei denen kein Ablaufdatum für die Sortierung verfügbar ist.

Wenn der Bestand zum ersten Mal im Lager eingeht oder erstellt wird, aktualisiert das System das entsprechende Kennzeichen, sodass das aktuelle Datum als Fälligkeitsdatum angezeigt wird. Dieses Datum wird dann von den Lagerplatzrichtlinienstrategien verwendet, um den ältesten oder neuesten Bestand im Lager zu identifizieren. Wenn der Bestand an einen Ort verschoben wird, der nicht vom Kennzeichen erfasst wird, wird der Ort selbst mit Fälligkeitsinformationen aktualisiert, und diese Informationen werden dann von den Strategien verwendet.

## <a name="turn-on-the-feature"></a>Aktivieren Sie die Funktion

Um diese Funktion verfügbar zu machen, aktivieren Sie die folgenden Funktionen in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) in dieser Reihenfolge:

1. Status des Lagerplatzes an einem Lagerort
1. Fälligkeit für Lagerplatzrichtlinie-Bestandsentnahme

## <a name="feature-requirements"></a>Funktionsanforderungen

Um diese Funktion nutzen zu können, müssen Sie die Option **Lagerplatzstatus aktivieren** für jedes verwendete [Lagerplatzprofil](tasks/create-location-profile.md) auf *Ja* einstellen, um den Bestand zu speichern. Um diese Option für ein Lagerplatzprofil festzulegen, gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplatzprofile** und wählen Sie das Lagerplatzprofil aus. Die Option finden Sie auf dem Inforegister **Allgemein**.

## <a name="feature-scenarios"></a>Funktionsszenarien

Dieser Abschnitt enthält Beispiele zum Einrichten und Verwenden von FIFO- und LIFO-Strategien.

> [!TIP]
> Dieser Abschnitt enthält zwei Szenarien, eines für FIFO und eines für LIFO. Bei den bereitgestellten Verfahren wird davon ausgegangen, dass Sie beide Szenarien der Reihe nach ausführen. Wir empfehlen, dass Sie beide Szenarien ausführen, damit Sie die Unterschiede zwischen den beiden Strategien feststellen können.

### <a name="make-sample-data-available"></a>Beispieldaten zur Verfügung stellen

Um diese Szenarien mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

Sie können diese Szenarien auch als Anleitung für die Verwendung der Funktion für ein Produktionssystem verwenden. In diesem Fall müssen Sie jedoch für jede hier beschriebene Einstellung Ihre eigenen Werte einsetzen.

### <a name="set-up-the-scenarios"></a><a name="demo-set-up"></a>Szenarien einrichten

Die Demodaten erfordern Einstellungs- und Bestandsapassungen, um die Szenarien zu unterstützen. Befolgen Sie diese Schritte, um die Bestandsdaten zu erstellen, die zum Durcharbeiten der FIFO- und LIFO-Szenarien erforderlich sind.

1. Melden Sie sich bei einem System an, bei dem Demodaten installiert sind, und wählen Sie die juristische Person **USMF** aus.
1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie in der Liste der Lagerplatzprofile **BODEN-05** aus.
1. Auf dem Inforegister **Allgemein** legen Sie die Option **Lagerplatzstatus aktivieren** auf *Ja* fest.
1. Wählen Sie **Speichern** aus.
1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Wählen Sie in der Liste der Lagerplatzrichtlinien **63 Verpacken in Container entnehmen** aus.
1. Klicken Sie auf **Bearbeiten**, um die Seite in den Bearbeitungsmodus zu versetzen.
1. Suchen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Zeile, in der das Feld **Sequenznummer** auf *1* gesetzt ist und befolgen Sie einen dieser Schritte:

    - Wenn Sie ein FIFO-Szenario einrichten, ändern Sie den Wert des Felds **Strategie** zu *Lagerplatzfälligkeit FIFO*.
    - Wenn Sie ein LIFO-Szenario einrichten, ändern Sie den Wert des Felds **Strategie** zu *Lagerplatzfälligkeit LIFO*.

1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** **Abfrage bearbeiten** aus.
1. Wählen Sie im Abfragedialogfeld auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um eine Position hinzuzufügen und legen Sie die folgenden Werte fest:

    - **Tabelle:** *Lagerorte*
    - **Abgeleitete Tabelle:** *Lagerorte*
    - **Feld:** *Zonen-ID*
    - **Kriterien:** *Boden*

1. Wählen Sie **OK**, um Ihre Einstellungen zu übernehmen und das Abfragedialogfeld zu schließen.
1. Wählen Sie **Speichern** aus, um Ihre Änderungen an der Lagerplatzrichtlinie zu speichern.
1. Führen Sie auf einem mobilen Gerät oder in der App *Dynamics 365 for Finance and Operations – Lagerung* die folgenden Schritte aus, um vorhandenen Bestand aus dem Lagerort zu entfernen und die Szenarien zu unterstützen:

    1. Melden Sie sich mit der passenden Benutzer-ID und einem Kennwort für den Lagerort *63* an.
    1. Auf dem Hauptmenü wählen Sie **Qualität**.
    1. Im Menü **Qualitätsmanagement** wählen Sie **Ausschuss**.
    1. Auf der Seite **Ausschuss** wählen Sie das Feld **LOC/LP** und geben dann *63\_1* ein.
    1. Wählen Sie **Eingeben** oder **OK** aus.
    1. Bestätigen Sie die Details **Ausschuss** für **Anpassung aus**, indem Sie **Eingeben** oder **OK** auswählen.

    Wenn der Kennzeichenbestand angepasst wird, erhalten Sie die Meldung „Arbeit abgeschlossen“.

    Diese Schritte belassen das Inventar an zwei Stellen in den Demodaten. Jeder Standort hat ein anderes Fälligkeitsdatum. Lagerplatz *FL-001* hat ein Fälligkeitsdatum vom 15. April 2017 und Lagerplatz *FL-002* hat ein Fälligkeitsdatum vom 29. Januar 2017. Beide Lagerplätze enthalten Artikel *A0001*.

    Um diese Daten anzuzeigen, gehen Sie zu **Bestandsverwaltung \> Anfragen und Berichte \> Bestandsliste** und filtern dann nach Lager *63* und Artikel *A0001*. In den Zeilen, in denen das Feld **Lagerplatz** auf *FL-001* oder *FL-002*festgelegt ist, wählen Sie eine Position mit einem positiven Wert für **Physischer Bestand** aus und wählen dann im Aktionsbereich **Transaktionen** aus. Das Feld **Physisches Datum** zeigt ein Datum an, das einem der zuvor genannten Fälligkeitsdaten entspricht.

### <a name="scenario-1-set-up-and-use-fifo-location-aging"></a><a name="fifo-demo"></a>Szenario 1: Einrichten und Verwenden der FIFO-Lagerplatzfälligkeit

Die FIFO-Strategie ermittelt den Lagerplatz, der das älteste Fälligkeitsdatum enthält, und weist die Kommissionierung basierend auf diesem Fälligkeitsdatum zu.

1. Wenn Sie dies noch nicht getan haben, [bereiten Sie die Beispieldaten vor](#demo-set-up), die für dieses Szenario erforderlich sind.
1. Gehen Sie zu **Vertrieb und Marketing \> Auftrag \> Alle Aufträge**.
1. Wählen Sie **Neu** aus.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - Legen Sie im Inforegister **Kunde** das Feld **Kundenkonto** auf *US-001* fest.
    - Legen Sie im Inforegister **Allgemein** das Feld **Lagerort** auf *63* fest.

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.
1. Der neue Auftrag wird geöffnet. Es enthält eine neue, leere Zeile im Raster auf dem Inforegister **Auftragspositionen**. Legen Sie für diese Auftragsposition das Feld **Artikelnummer** auf *A0001* und das Feld **Menge** auf *1* fest.
1. Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** die Option **Los reservieren** aus, um die bestellte Menge dieses Artikels aus dem Bestand im Lagerort zu reservieren.
1. Schließen Sie die Seite **Reservierung**.
1. Klicken Sie auf der Seite **Auftrag** im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten** **Für Lagerort freigeben**. Es werden Informationsnachrichten angezeigt. Das System erstellt eine Sendung, fügt sie einer neuen Ladung hinzu und erstellt die erforderliche Arbeit.
1. Wählen Sie im Inforegister **Auftragspositionen** im Menü **Lagerort** die Option **Arbeitsdetails** aus, um die Arbeit zu öffnen, die für diesen Auftrag erstellt wurde. Beachten Sie, dass die Position, in der der Wert **Arbeitstyp** *Entnehmen* lautet, für **Lagerplatz** den Wert *FL-002* anzeigt. Dieser Lagerplatz enthält das Kennzeichen mit dem ältesten Fälligkeitsdatum (FIFO).
1. Wählen Sie **Lagerort \> Lieferdetails**.
1. Notieren Sie sich im Inforegister ***Allgemein** die Wellen-ID, damit Sie sie in Szenario 2 verwenden können.

### <a name="scenario-2-set-up-and-use-lifo-location-aging"></a>Szenario 2: Einrichten und Verwenden der LIFO-Lagerplatzfälligkeit

Die LIFO-Strategie ermittelt den Lagerplatz, der das neueste Fälligkeitsdatum enthält, und weist die Kommissionierung basierend auf diesem Fälligkeitsdatum zu. In Szenario 2 bearbeiten Sie die Einstellungen für Szenario 1 (FIFO) und verwenden den Kundenauftrag und die Welle, die in diesem Szenario erstellt wurden, erneut.

1. Bevor Sie dieses Szenario starten, richten Sie das vollständige FIFO-Szenario ein und schließen Sie es ab, wie im [vorherigen Abschnitt](#fifo-demo) beschrieben. In diesem Szenario werden Sie die Welle und den größten Teil der für dieses Szenario erstellten Einstellungen wiederverwenden.
1. Bearbeiten Sie die Lagerplatzrichtlinie **63 Verpacken in Container entnehmen**, damit die Strategie *Lagerplatzfälligkeit LIFO* verwendet wird, wie im ersten Teil des Verfahrens [Szenarien einrichten](#demo-set-up) beschrieben.

    Als Nächstes ändern Sie die Welle, die in Szenario 1 für den Auftrag erstellt wurde, sodass die Strategie *Lagerplatzfälligkeit LIFO* verwendet wird.

1. Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.
1. Wählen Sie die Welle aus und öffnen Sie sie, die die Reihenfolge enthält, die Sie für das FIFO-Szenario erstellt haben.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeit** die Option **Abbrechen**, um die Arbeit abzubrechen, die Sie für das FIFO-Szenario erstellt haben.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Welle** in der Gruppe **Welle** auf **Verarbeiten**.
1. Wenn die Verarbeitung abgeschlossen ist, klicken Sie im Aktivitätsbereich auf der Registerkarte **Welle** in der Gruppe **Zugehörige Informationen** auf **Arbeit**, um die Arbeit zu öffnen, die für diese Welle erstellt wurde.
1. Auf der Seite **Arbeit** auf der Registerkarte **Übersicht** sollte es zwei Positionen geben. Wählen Sie die Position aus, in der das Feld **Arbeitsstatus** auf *Offen* festgelegt ist.
1. Beachten Sie, dass die Position, in der der Wert **Arbeitstyp** *Entnehmen* lautet, für **Lagerplatz** den Wert *FL-001* anzeigt. Dieser Lagerplatz enthält das Kennzeichen mit dem neuesten Fälligkeitsdatum (LIFO).

In diesen Szenarien haben Sie gesehen, wie die Lagerortfälligkeitsstrategie die Arbeit an den Lagerort-Standort lenkt, der je nach ausgewählter Strategie entweder den ältesten oder neuesten Bestand enthält.
