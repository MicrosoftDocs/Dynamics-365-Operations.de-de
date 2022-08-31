---
title: Clusterposition voll
description: Dieser Artikel enthält Informationen zur Funktion Clusterposition voll. Diese Funktion bietet eine Alternative zur strengeren Durchsetzung von Arbeitsunterbrechungsregeln, wenn die Clusterkommissionierung verwendet wird, da sie eine größere Fehlerquote bei den volumetrischen Einschränkungen von Containern oder Behältern ermöglicht.
author: Mirzaab
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 9361448ba7993ba7cc126d6dd60a45fe497b2e84
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218769"
---
# <a name="cluster-position-full"></a>Clusterposition voll

[!include [banner](../includes/banner.md)]

Die Funktion *Clusterposition voll* bietet eine Alternative zur strengeren Durchsetzung von Arbeitsunterbrechungsregeln, wenn die Clusterkommissionierung verwendet wird, da sie eine größere Fehlerquote bei den volumetrischen Einschränkungen von Containern oder Behältern ermöglicht. In einem allgemeinen Szenario passen nicht alle Elemente eines Arbeitsauftrags in einen ausgewählten Container. Lagerarbeiter, die Cluster auswählen, haben in diesem Szenario nur wenige Optionen: Sie müssen entweder zu einem größeren Container wechseln oder mit ihrem Vorgesetzten zusammenarbeiten, um eine andere Lösung zu finden.

Diese Funktion bietet die Möglichkeit, die Schaltfläche **Voll** auf einer der Arbeitseinheiten in einem Cluster auszuführen. In älteren Versionen war diese Option nur für die reguläre Kommissionierung verfügbar, nicht für die Clusterkommissionierung. Diese Funktion unterscheidet sich jedoch von der Standard **Voll**-Schaltfläche, da die verbleibende Arbeit abgebrochen wird. Es wird nicht vorgeschlagen, dass der Benutzer dem gleichen Cluster ein weiteres Lagerfach hinzufügt, und es wird nicht automatisch eine neue Arbeit erstellt.

## <a name="turn-the-cluster-position-full-feature-on-or-off"></a>Funktion „Clusterposition voll“ ein- oder ausschalten

Um die Funktionalität zu verwenden, die in diesem Artikel beschrieben wird, muss die Funktion *Clusterposition voll* für Ihr System eingeschaltet werden. Ab Supply Chain Management 10.0.25 ist diese Funktion obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.25 ausführen, können Administratoren diese Funktionalität ein- oder ausschalten, indem sie nach der Funktion *Clusterposition voll* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="setup"></a>Einrichtung

Dieser Abschnitt enthält Richtlinien und ein Beispiel, das zeigt, wie Sie die *Clusterposition voll*-Funktion einrichten und verwenden.

### <a name="make-sample-data-available"></a>Beispieldaten zur Verfügung stellen

Um das [Beispielszenario](#example-scenario) mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

Sie können dieses Beispielszenario auch als Anleitung zur Arbeit Sie an einem Produktionssystem mit dieser Funktion nutzen. In diesem Fall müssen Sie jedoch für alle hier beschriebene Einstellungen Ihre eigenen Werte einsetzen.

### <a name="cluster-profiles"></a>Clusterprofile

Sie müssen angeben, ob Cluster-IDs automatisch generiert werden, wie viele Positionen verwendet werden, wann Cluster beschädigt werden und wie die Entnahmearbeit sequenziert und überprüft wird.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Clusterprofile**.
1. Wählen Sie im Listenbereich den Datensatz **Cluster erstellen** aus.
1. Bestätigen Sie im Inforegister **Allgemein** die folgenden Werte.

    - **Cluster-ID generieren:** *Ja*
    - **Positionen aktivieren:** *Ja*
    - **Anzahl der Positionen:** *2*
    - **Positionsname:** *Numerisch*
    - **Cluster unterbrechen bei:** *Einlagern*
    - **Sortierbestätigungstyp:** *Positionsscan*

1. In dem **Clustersortierung**-Inforegister. Das Raster sollte leer sein (d.h. es sollte keine Positionen enthalten).

### <a name="work-templates"></a>Arbeitsvorlagen

Sie müssen definieren, wie die Entnahmearbeit für Clusterkommissionierung erstellt wird.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Stellen Sie oben auf der Seite das Feld **Arbeitsauftragstyp** auf *Aufträge*.
1. Stellen Sie sicher, dass die folgenden Arbeitsvorlagen aus den Demodaten aufgelistet sind. Wenn sie nicht verfügbar sind, können Sie das Szenario nicht abschließen.

    - 61 SO Phase
    - 61 SO Clusterkommissionierung

### <a name="location-directives"></a>Lagerplatzrichtlinien

Sie müssen angeben, woher die Artikel kommissioniert wurden und wo sie platziert werden.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Legen Sie in der Kopfzeile der Liste das Feld **Arbeitsauftragstyp** auf *Aufträge* fest.
1. Stellen Sie sicher, dass die folgenden Auftragsrichtlinien aus den Demodaten aufgelistet sind. Wenn sie nicht verfügbar sind, können Sie das Szenario nicht abschließen.

    - 61 Clusterkommissionierung
    - 61 Kommissionierreihenfolge

### <a name="mobile-device-menu-items"></a>Menüelemente des mobilen Geräts

Sie müssen eine Menüoption des Mobilgeräts konfigurieren, um vorhandene Arbeit zu verwenden, die durch Clusterkommissionierung geleitet wird. Im Menüpunkt des Mobilgeräts für die Clusterkommissionierung muss der **Arbeitsteilung zulassen**-Parameter eingeschaltet sein, und die Arbeiterklasse *SO Kommissionierung* muss hinzugefügt werden.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Listenbereich den Datensatz **Clusterkommissionierung erstellen** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Geleitet von:** *Clusterkommissionierung*
    - **Kennzeichen generieren:** *Ja*
    - **Aufteilung der Arbeit zulassen:** *Ja*
    - **Clusterprofil-ID:** *Cluster erstellen*

    Akzeptieren Sie die Standardwerte für alle anderen Felder.

1. Fügen Sie im Inforegister **Arbeiterklassen** nach Bedarf die folgenden zwei Zeilen hinzu:

    - Zeile 1 (normalerweise in Demodaten vorhanden):

        - **Arbeitsklassenkennung:** *Vertrieb* 
        - **Arbeitsauftragsart:** *Kundenaufträge*

    - Zeile 2 (wahrscheinlich nicht in Demodaten vorhanden):

        - **Arbeitsklassen-ID:** *SO Kommissionierung*
        - **Arbeitsauftragsart:** *Kundenaufträge*

1. Wechseln Sie im Aktionsbereich zu **Einrichtung der Arbeitsbestätigung**.
1. Wählen Sie **Bearbeiten** aus.
1. Geben Sie auf der Position im Raster die folgenden Werte ein:
    - **Arbeitstyp:** - *Kommissionnieren*
    - **Produktbestätigung** - *Aktivieren Sie das Kontrollkästchen*

1. Wählen im Aktionsbereich **Speichern** und schließen Sie die Seite.

## <a name="create-picking-work"></a>Entnahmearbeit erstellen

Bevor Sie mit der Clusterkommissionierung beginnen können, müssen Sie ausgehende Arbeiten erstellen. Das zuvor erstellte Clusterprofil gibt zwei Clusterpositionen an. Daher müssen mindestens zwei Arbeits-IDs für die Auftragskommissionierung erstellt werden. In diesem Szenario werden Transaktionen im Lager *61* ausgeführt und sie werden die Artikel *L0101* und *T0100* verwenden. Die Demodaten sollten über einen ausreichenden Bestand dieser Artikel verfügen. Stellen Sie sicher, dass Sie über genügend Bestand verfügen, um die Transaktionen abzuschließen.

### <a name="create-sales-order-1"></a>Auftrag 1 erstellen

1. Gehen Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus, um Auftrag 1 zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-010*
    - **Lagerort:** *61*

1. Wählen Sie **OK**.
1. Der neue Auftrag wird geöffnet. Fügen Sie im Inforegister **Auftragspositionen** eine Position mit den folgenden Einstellungen hinzu:

    - **Artikelnummer:** *T0100*
    - **Menge** *5*

1. Legen Sie im Feld **Bestätigtes Lieferdatum** auf der Registerkarte **Lieferung** des Inforegisters **Positionsdetails** das heutige Datum fest.
1. Fügen Sie im Inforegister **Auftragspositionen** eine zweite Position mit den folgenden Einstellungen hinzu:

    - **Artikelnummer:** *L0101*
    - **Menge** *20*

1. Legen Sie im Feld **Bestätigtes Lieferdatum** auf der Registerkarte **Lieferung** des Inforegisters **Positionsdetails** das heutige Datum fest.
1. Führen Sie für jede gerade hinzugefügte Position die folgenden Schritte aus, um Bestand zu reservieren:

    1. Wählen Sie die zu reservierende Position aus.
    2. Wählen Sie im Inforegister **Auftragspositionen** die Option **Bestand \> Reservierung** aus.
    3. Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, um den Lagerbestand zu reservieren.
    4. Schließen Sie die Seite **Reservierung**.

1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

    Wenn die Freigabe abgeschlossen ist, erhalten Sie Informationsnachrichten mit der Wellen- und Lade-ID, die erstellt wurden.

### <a name="create-sales-order-2"></a>Auftrag 2 erstellen

1. Gehen Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus, um Auftrag 2 zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-011*
    - **Lagerort:** *61*

1. Wählen Sie **OK**.
1. Der neue Auftrag wird geöffnet. Fügen Sie im Inforegister **Auftragspositionen** eine Position mit den folgenden Einstellungen hinzu:

    - **Artikelnummer:** *L0101*
    - **Menge** *20*

1. Legen Sie im Feld **Bestätigtes Lieferdatum** auf der Registerkarte **Lieferung** des Inforegisters **Positionsdetails** das heutige Datum fest.
1. Fügen Sie im Inforegister **Auftragspositionen** eine zweite Position mit den folgenden Einstellungen hinzu:

    - **Artikelnummer:** *T0100*
    - **Menge** *2*

1. Legen Sie im Feld **Bestätigtes Lieferdatum** auf der Registerkarte **Lieferung** des Inforegisters **Positionsdetails** das heutige Datum fest.
1. Führen Sie für jede gerade hinzugefügte Position die folgenden Schritte aus, um Bestand zu reservieren:

    1. Wählen Sie die zu reservierende Position aus.
    2. Wählen Sie im Inforegister **Auftragspositionen** die Option **Bestand \> Reservierung** aus.
    3. Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, um den Lagerbestand zu reservieren.
    4. Schließen Sie die Seite **Reservierung**.

1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

    Wenn die Freigabe abgeschlossen ist, erhalten Sie Informationsnachrichten mit der Wellen- und Lade-ID, die erstellt wurden.

### <a name="get-work-ids-and-license-plate-numbers"></a>Arbeits-IDs und Kennzeichennummern abrufen

Es sollten zwei Arbeits-IDs erstellt worden sein, von denen jede zwei Kommissionierungspositionen hat. Befolgen Sie diese Schritte, um die Arbeits-IDs und Kennzeichenzuordnungen zu finden.

1. Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.
1. Suchen Sie in dem **Übersicht**-Raster die **Bestellnummer**-Spalte für die beiden Aufträge, die Sie gerade erstellt haben. Notieren Sie sich für jeden Auftrag die entsprechende Arbeits-ID.
1. Wählen Sie die Zeile für jeden Auftrag aus, um relevante Informationen in **Positionen**-Raster anzuzeigen. Notieren Sie sich den Ort, an dem jeder Artikel ausgewählt wird.
1. Wechseln Sie zu **Lagerverwaltung \> Anfragen und Berichte \> Bestandsliste**.
1. Wählen Sie im Aktivitätsbereich **Dimensionen** aus, um das Dialogfeld **Dimensionsanzeige** zu öffnen.
1. Stellen Sie sicher, dass die Kontrollkästchen **Kennzeichen**, **Warenhaus**, und **Artikelnummer** aktiviert sind und wählen Sie anschließend **OK** aus.
1. Legen Sie im **Filter**-Bereich folgende Filter fest:

    - **Artikelnummer** – **ist eine von** – *L0101* und *T100*
    - **Warenhaus** – **beginnt mit** – *61*

1. Notieren Sie sich die angezeigten Werte für **Kennzeichen**.

## <a name="example-scenario"></a><a name="example-scenario"></a>Beispielszenario

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a>Flow-Ausführung für mobile Geräte – Einrichtung der Arbeitsbestätigung für das Produkt

1. Melden Sie sich bei der Warehouse Management Mobile App als ein Benutzer im Lagerort *61* an.
1. Wechseln Sie zu **Ausgehend \> Clusterkommissionierung erstellen**.

    Die **AUFGABE: Arbeit dem Cluster zuweisen**-Seite erscheint.

1. Geben Sie die Arbeits-ID für Auftrag 1 ein, um sie der Clusterposition 1 zuzuweisen.
1. Wählen Sie **OK** (Häkchensymbol).
1. Geben Sie die Arbeits-ID für Auftrag 2 ein, um sie der Clusterposition 2 zuzuweisen.
1. Wählen Sie **OK** (Häkchensymbol).

    Die **AUFGABE: Clusterkommissionierung erstellen: Kommissionieren**-Seite erscheint und zeigt *Artikel L0101 2 PL*.

Da das Clusterprofil die Anzahl der Positionen auf 2 festgelegt hat, leitet das System Sie automatisch zur ersten konsolidierten Auswahl weiter: zwei Paletten (PL) des Artikels *L0101*.

Während der folgenden Schritte können Sie jederzeit die **Details**-Registerkarte auswählen, um zusätzliche Informationen zur Aufgabe anzuzeigen, z. B. den Kommissionierungsort.

1. Legen Sie das Feld **ARTIKEL** auf *L0101* fest. Dies bestätigt die Artikelnummer, die für diesen Menüpunkt erforderlich ist (Sie haben dies zuvor durch Auswahl von **Einrichtung der Arbeitsbestätigung** auf der Seite **Mobilgerät-Menüpunkt** konfiguriert, als Sie diesen Menüpunkt erstellt haben).
1. Geben Sie die Kennzeichennummer ein, die dem Artikel an dem Lagerplatz zugeordnet ist, an dem es ausgewählt wird. Sie werden zwei Paletten kommissionieren.
1. Stellen Sie das **LP**-Feld auf *LP\_PICK\_01*.
1. Wählen Sie **OK** (Häkchensymbol).

    Die **AUFGABE: Sortieren: Clusterkommissionierung erstellen**-Seite erscheint. Hier sortieren Sie die beiden kommissionierten Paletten in eine Kommissionierposition. Diese Position kann ein Behälter oder ein Container sein, mit dem der kommissionierte Bestand nach Auftrag getrennt wird.

1. Zeigen Sie die Details an, die für den Artikel (*L0101*) und die Menge (*20* ea), die in Position 1 sortiert wird (für Auftrag 1), angezeigt werden.
1. Stellen Sie das **POSITION NA**-Feld auf *1*.
1. Wählen Sie **OK** (Häkchensymbol).
1. Zeigen Sie die Details an, die für den Artikel (*L0101*) und die Menge (*20* ea), die in Position 2 sortiert wird (für Auftrag 2), angezeigt werden.
1. Stellen Sie das **POSITION NA**-Feld auf *2*.
1. Wählen Sie **OK** (Häkchensymbol).

    Die **AUFGABE: Clusterkommissionierung erstellen: Kommissionieren**-Seite erscheint und zeigt *Artikel T0100 7 ea*.

In diesem Szenario kann Position 1 nicht die gesamte Menge der Artikel akzeptieren, die zur Erfüllung des Auftrags 1 kommissioniert werden müssen. Eine Position muss als voll markiert sein. In diesem Szenario kommissionieren Sie den zweiten Artikel teilweise. Der zweite Artikel wird für Position 1 teilweise kommissioniert, und es wird neue Arbeit erstellt, um die verbleibende Menge zu kommissionieren, um die Bestellung zu erfüllen.

1. Wählen Sie die Menütaste (manchmal auch als Hamburger oder Hamburgertaste bezeichnet) und dann **Position voll** aus.
1. Identifizieren Sie die Position, die voll ist, und wählen Sie *1*.
1. Wählen Sie **OK** (Häkchensymbol).
1. Geben Sie die Kommissionierungsmenge ein, die noch in Position 1 kommissioniert werden kann. Das System kann bestimmen, welche Artikelnummer kommissioniert wird.
1. Geben Sie *2* ein.
1. Wählen Sie **OK** (Häkchensymbol).
1. Bestätigen Sie die Artikelnummer, um die Auswahl des verbleibenden Artikels in Position 2 abzuschließen.
1. Legen Sie das Feld **ARTIKEL** auf *T0100* fest.
1. Wählen Sie **OK** (Häkchensymbol).
1. Geben Sie das Kennzeichen ein, von dem der Artikel kommissioniert wird, indem Sie das **LP**-Feld auf *LPREPL04* festlegen.
1. Wählen Sie **OK** (Häkchensymbol).
1. Zeigen Sie die Details an, die für den Artikel (*T0100*) und die Menge (*2* ea), die in Position 2 sortiert wird (für Auftrag 2), angezeigt werden.
1. Stellen Sie das **POSITION NA**-Feld auf *2*.
1. Wählen Sie **OK** (Häkchensymbol).
1. Zeigen Sie die Details an, die für den Artikel (*T0100*) und die Menge (*2* ea), die in Position 1 sortiert wird (für Auftrag 1), angezeigt werden.
1. Stellen Sie das **POSITION NA**-Feld auf *1*.
1. Wählen Sie **OK** (Häkchensymbol).

    Die **AUFGABE: Clusterkommissionierung: Einlagern**-Seite erscheint.

In diesem Szenario wurde die Clusterkommissionierung abgeschlossen, und der Benutzer wird angewiesen, die ausgewählten Elemente von Position 1 und Position 2 an den Staging-Lagerplatz zu verschieben *STAGE01*.

1. Prüfen Sie die Informationen auf der Seite. Sie zeigt, dass eine Gesamtmenge von *44* an den Staging-Lagerplatz gebracht wird.
1. Wählen Sie **OK** (Häkchensymbol).

    Sie erhalten die Nachricht „Cluster abgeschlossen“.

Sie können jetzt den **Verkaufsauswahl**-Menüpunkt verwenden, um die verbleibende Menge auszuwählen. Sie können dann das **Verkaufsverladung**-Menüelement verwenden, um Artikel vom Staging-Lagerplatz zum Verladedock zu verschieben.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]