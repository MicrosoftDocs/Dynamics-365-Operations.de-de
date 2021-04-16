---
title: Wareneingangsübersicht
description: Dieses Thema enthält Informationen zu den Wareneingangsübersichtfunktion. Die Wareneingangsübersichtseite ist Teil dieser Funktionen und bietet eine Übersicht aller Artikel, von denen erwarten wird, dass sie als eingehende Artikel eintreffen.
author: perlynne
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 734fbdd6f62c192580029a24844fff78fda8b919
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809589"
---
# <a name="arrival-overview"></a>Wareneingangsübersicht

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zu den Wareneingangsübersichtfunktion. Die Wareneingangsübersichtseite ist Teil dieser Funktionen und bietet eine Übersicht aller Artikel, von denen erwarten wird, dass sie als eingehende Artikel eintreffen.

Die Seite **Wareneingangsübersicht** enthält eine Übersicht aller eingehenden erwarteten Artikel. Sie zeigt auch Eingänge an, die basierend auf der Übersicht initialisiert werden können. Dieses Thema bezieht sich auf den empfangenden Prozess.

## <a name="business-scenario"></a>Geschäftsszenario
Beachten Sie das folgende Szenario im Eingangsprozess.

[![Geschäftsszenario](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)

Thomas, ein empfangender Arbeiter, möchte wissen, was am aktuellen Tag erwartet wird. Auf der Seite **Wareneingangsübersicht** kann Thomas eine Übersicht der aktuellen Aufgaben, eine grobe Schätzung von Mengen, Volumen, Gewicht, unterschiedliche Auftragstypen usw. abrufen. Später kommt eine Lieferung an einer Eingangsrampen und Thomas erhält eine Liste der Lieferung. Auf der Seite **Eingangsübersicht** kann Thomas folgende Aufgaben ausführen:

-   Geben Sie den entsprechenden Zugangsauftrag, und erfassen Sie den Zugang als **In Bearbeitung** Die Positionen, für die eine Erfassung erforderlich sind, werden automatisch erstellt und der Empfang kann überwacht werden, obwohl die Transaktionen noch nicht als **Erfasst** gebucht wurden.
-   Greifen Sie auf die entsprechende Wareneingangserfassungsreferenz zu (das heißt, die Erfassung **Wareneingang** oder die Erfassung **Produktionseingang**) und kennzeichnen Sie die Erfassungen, die für eine Produktzugangsaktualisierung bereit sind.

## <a name="arrival-overview-page"></a>Wareneingangsübersicht anzeigen
Um die Seite **Wareneingangsübersicht** zu öffnen, klicken Sie auf **Lagerverwaltung** &gt; **Eingehende Aufträge** &gt; **Wareneingangsübersicht**. Sie können eine Liste der Aufträge anzeigen, die voraussichtlich empfangen werden. Der Überblick ist in eine Überschrift und in Positionen aufgeteilt. Die Überschriftsinformationen werden nach Bestellungstyp, erwartetes Datum und Lieferort gruppiert. Wenn eine Überschrift für den Zugang aktiviert ist, werden alle Positionen, die der Zugangsreferenz zugeordnet sind, für den Eingang im Positionsdetailteil der Seite ausgewählt. Wenn alle diesbezüglichen Erfassungspositionen gebucht wurden, werden diese Informationen nicht angezeigt.

### <a name="arrival-overview-profiles"></a>Übersichtsprofile für Wareneingänge

Die Seite **Wareneingangsübersicht** enthält einen Überblick über Artikel, von denen zu erwarten ist, dass Sie am erwarteten Eingangsdatum eintreffen. Im Rahmen des Eingangsprozesses können verschiedene persönlichen Einstellungen verwendet werden. Einzelne Benutzer können ihre eigenen Einstellungen auf der Seite **Wareneingangsübersichtprofile** festlegen.

### <a name="set-up-item-arrival"></a>Artikeleingang einrichten

In Beispiel möchte Thomas einen neuen Computer an einem Standort einrichten, der verwendet wird, um fertige Artikel zu empfangen, die von der Produktion am Standort 1 kommen. Auf der Seite **Wareneingangsübersichtprofile** erstellt Thomas ein neues Profil mit Namen **Produktion des Standorts 1** und definiert die folgenden Einstellungen angezeigt.

1.  Im Inforegister **Eingangsoptionen** in der Feldgruppe **Bereich** geben Sie Informationen zu einem Tagintervall und die Lagerorte ein, die in Übersicht angezeigt werden sollen.
2.  Im Inforegister **Eingangsoptionen** in der Feldgruppe **Erfassung**, geben Sie einen empfangenden Lagerort, einen Speicherort und einen Journalnamen ein (Artikel Eingang/Produktionseingang).
3.  Im Inforegister **Eingangsabfragendetails** in der Feldgruppe **Standort**, im Feld **Auf Standort beschränken**, geben Sie einen Standort ein, um die Anzeige im Bereich Überblick einzuschränken.
4.  Im Inforegister **Eingangsabfragendetails** in der Feldgruppe **Angezeigte Buchungsarten**, setzen Sie **Produktionsaufträge** auf **Ja**.
5.  Im Inforegister **Eingangsabfragendetails** in der Gruppe **Sonstiges**, setzen Sie die Option **Beim Start aktualisieren** auf **Ja**, wenn die Ansicht automatisch beim Start aktualisiert wird. Setzen Sie die Option **Bei Bereichsänderung aktualisieren** auf **Ja** nachdem die Ansicht automatisch aktualisiert wird, wenn Bereichswerte geändert werden.

Bei diesem Beispiel wird das Feld **Wareneingangsübersichtprofilname** auf dem Inforegister **Eingangsoptionen** der Seite **Wareneingangsübersicht** auf **Produktion des Standorts 1** festgelegt.

### <a name="prerequisites-for-arrival-journals"></a>Voraussetzungen für Wareneingangserfassungen

Um automatisch Wareneingangserfassungen von der Seite **Wareneingangsübersicht** zu erstellen, müssen Sie die entsprechenden Informationen in der Feldgruppe **Erfassung** auf dem Inforegister **Eingangsoptionen** definieren.

-   Wählen Sie beim Erstellen eines neuen Journals einen Namen für das Journal aus.

[![So definieren Sie einen Journalnamen](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   Wenn Sie die Werte in den Feldern **Lagerort** und **Lagerplatz** angegeben, werden diese Werte in den Erfassungspositionen übernommen. Wenn Sie keine Werte festlegen, verwendet das System die Werte aus der Dimension, die in den Lagerbuchungen angegeben wird.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>Artikel, die von einem Auftrag des erwarteten Zugangs empfangen werden

Im Inforegister **Zugänge** wählt Thomas eine Position aus und klickt anschließend **Wareneingang starten**. Alle zugehörigen Positionen, die im angegebenen Bereich sind und eine Menge zu erfassen haben, werden automatisch ausgewählt. Eine Wareneingangserfassung wird generiert, die eine Übereinstimmung zwischen dem erwarteten Auftrag und der Erfassung hat. Die Menge wird automatisch in allen Positionen initialisiert, die erstellt werden.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>Artikel, die von mehr als einem erwarteten Zugangs empfangen werden

Im Inforegister **Zugänge** wählt Thomas eine oder mehrere Position aus und klickt anschließend **Wareneingang starten**. Eine Wareneingangserfassung wird generiert, die eine Übereinstimmung zwischen allen erwarteten Aufträgen und der Erfassung hat. Alle Positionen werden auf einem Wareneingangserfassungskopf erstellt, und die Menge wird automatisch initialisiert.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>Artikel, die von mehr als einem erwarteten Zugangs empfangen werden

#### <a name="view-information"></a>Informationen anzeigen

Um einen Überblick der erwarteter Zugänge in einem Datumsintervall abrufen zu können, gibt Thomas die folgenden Informationen in den Feldern auf dem Inforegister **Eingangsoptionen** auf der Seite **Wareneingangsübersicht** ein und klickt anschließend **Aktualisieren** um die Ansicht zu aktualisieren:

-   Wareneingangsübersichtprofilname: **Abfrage**
-   **Alle** Auszugspositionen anzeigen
-   Tage zurück (Leer)
-   Tage vorwärts: **0**
-   Lagerorte: **GW, MW**

Thomas kann die folgenden Informationen anzeigen:

-   Alle zugehörigen Zugangsaufträge für das Systemdatum und eine unbegrenzte Anzahl von Tagen nach der Kombination (das Intervall **InventTrans.StatusDate**) und der Empfang an den Lagerorten GW und MW unabhängig vom Status.
-   Ausführliche Positionsinformationen für mehr als einen Auftrag. Thomas kann mehrere Überschriftzeilen im Überblick auswählen und **Alle ausgewählten Elemente anzeigen** klicken, um alle übereinstimmenden Positionsdetailinformationen für alle ausgewählten Aufträge anzuzeigen..
-   Zeigt Informationen über eine spezifische Bestellung an. Um nur Informationen anzuzeigen, die einer bestimmten Referenznummer im Überblick zugeordnet sind, kann Thomas eine Kontonummer im Feld **Kontonummer** und die Auftragsnummer im Feld **Referenznummer** eingeben.
-   Ein Überblick der erfassten Aufgaben, die für alle Auftragspositionen fällig sind, die für eine Wareneingangserfassung erstellt aber noch nicht gebucht wurden. Um diese Informationen anzuzeigen, kann Thomas im Feld **Positionen anzeigen** **In Bearbeitung** auswählen.

### <a name="update-journals"></a>Erfassungen aktualisieren

Um eine oder mehrere Auftragspositionen zu erfassen, die verarbeitet werden müssen, kann Thomas die Positionen im Übersichtsraster oder im Positionsraster auswählen und dann auf **Erfassungen** &gt; **Wareneingänge aus Zugängen anzeigen** klicken. Die Wareneingangsüberschriften, die den Positionen entsprechen, werden angezeigt. Um den Produktzug der erfassten Artikel zu aktualisieren, kann Thomas auf die Überschriften der Wareneingangserfassung zugreifen, die zur Aktualisierung bereit sind. Um auf diese Wareneingangserfassungsüberschriften zuzugreifen, klickt der **Erfassungen** &gt; **Für Produktzugang vorbereitete Erfassungen**. Alle Überschriftzeilen, die für die Aktualisierung des Produktzugangs im angegebenen Lagerortbereich bereit sind, werden angezeigt. (Die Überschriftzeilen, die angezeigt werden, werden nicht in Tagintervall zugeordnet).

### <a name="start-an-arrival-registration"></a>Hiermit starten Sie eine Eingangserfassung

Wenn Sie mehrere Positionen auf der Seite **Wareneingangsübersicht** aktivieren, kann Thomas einen Zugang in mehreren Zugangsreferenz starten. Wenn er eine Position aus dem Zugangsüberblick auswählt, werden die entsprechenden Positionsdetails ausgewählt. Wenn eine Menge für die Erfassung vorhanden ist, ist die Schaltfläche **Wareneingang starten** verfügbar. Thomas kann zwei Methoden verwenden, um die Eingangserfassung zu starten:

-   Um die Seite zu filtern, so dass nur Datensätze angezeigt werden, die den bestimmte Kriterien entsprechen, erfassen Sie im Feld **Kreditorenreferenz**, eine Referenznummer aus einem Kreditor, wie der Barcode für einen Lieferschein.
-   Im Überblicksteil oder auf im Detailteil der Seite **Wareneingangsübersicht** wählen Sie manuell die Auswahl von Datensätzen für die Eingangserfassung oder deaktivieren Sie diese. Thomas wird anschließend auf **Wareneingang starten** klicken, und die ausgewählten Datensätze werden automatisch in einer Wareneingangserfassung erstellt. Die Datensätze enthalten alle eindeutigen Positionsinformationen und die Feldinformationen werden zugewiesen.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>Aktualisieren Sie Eingangsinformationen und verarbeiten Sie einen Produktzugang
Nachdem alle Waren erfasst wurden, aktualisiert der Lagerortleiter oder der Einkaufsleiter die eingegangenen Artikel mit einem Lieferschein, um so den physischen Einstandsbetrag hinzuzufügen. Um Eingangsinformationen zu aktualisieren und einen Produktzugang zu buchen, führen Sie die folgenden Schritte aus.

1.  Klciken Sie auf **Lagerverwaltung** &gt; **Eingehende Aufträge** &gt; **Wareneingangsübersicht**.
2.  Auf der Seite **Wareneingangsübersicht** klicken Sie auf **Erfassungen** &gt; **Für Produktzugang vorbereitete Erfassungen**, um eine Liste der Erfassungen anzeigen, die die für den Produktzugang vorbereitete Erfassungen aktualisiert.
3.  Wählen Sie die Journale, die aktualisiert werden müssen und klicken sie **Funktionen** &gt; **Produktzugang**.
4.  Auf der Seite **Buchung** geben Sie die Produktzugangsnummer ein, wenn sie nicht für die Erfassung bereits verfügbar ist, und klicken Sie dann **OK** um den Produktzugang zu verarbeiten.

## <a name="summary"></a>Summe
Die Seite **Wareneingangsübersicht** kann der Lagerortverwaltung und den Lagerarbeitern dabei helfen, sich einen Überblick über die erwarteten Arbeit zu verschaffen, der als Teil eines eingehenden Prozesses ausgeführt werden muss. Die Seite kann auch verwendet werden, um den Wareneingangprozess zu starten, um zu gewährleisten, dass die Artikel an der ersten Position am Lagerort verfolgt werden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]