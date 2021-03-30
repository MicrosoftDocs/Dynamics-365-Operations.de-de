---
title: Standortkennzeichenpositionierung
description: Durch die Standortkennzeichenpositionierung können Sie sehen, wo sich ein Kennzeichen an einem Ort mit mehreren Paletten befindet, z. B. an einem Ort, an dem doppelt tiefe Palettenregale verwendet werden.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cfab8c36adb08f799305a153589926bfc1ae31fe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217100"
---
# <a name="location-license-plate-positioning"></a>Standortkennzeichenpositionierung

[!include [banner](../includes/banner.md)]

Durch die Standortkennzeichenpositionierung können Sie sehen, wo sich ein Kennzeichen an einem Ort mit mehreren Paletten befindet, z. B. an einem Ort, an dem doppelt tiefe Palettenregale verwendet werden.

Die Funktion fügt jedem Kennzeichen, das an einem Lagerort abgelegt wird, eine Sequenznummer hinzu. Diese Sequenznummer wird verwendet, um die Kennzeichen am Lagerort zu bestellen. Daher unterstützt die Funktion auf intelligente Weise Szenarien, in denen Kunden ein Schwerkraft-Regalsystem verwenden und zu Kommissionierzwecken wissen müssen, welches Kennzeichen nach vorne zeigt.

In diesem Thema wird ein Szenario vorgestellt, in dem gezeigt wird, wie die Funktion eingerichtet und verwendet wird.

## <a name="turn-on-the-location-license-plate-positioning-feature"></a>Funktion für Standortkennzeichenpositionierung aktivieren

Bevor Sie die Standortkennzeichenpositionierung verwenden können, muss die Funktion in Ihrem System aktiviert sein. Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Standortkennzeichenpositionierung*

## <a name="example-scenario"></a>Beispielszenario

### <a name="make-sample-data-available"></a>Beispieldaten zur Verfügung stellen

Um dieses Szenario mit den hier vorgeschlagenen Werten zu bearbeiten, müssen Sie auf einem System arbeiten, auf dem Beispieldaten installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

### <a name="set-up-the-feature-for-this-scenario"></a>Funktion für dieses Szenario einrichten

Führen Sie die folgenden Schritte aus, um die Funktion *Standortkennzeichenpositionierung* für das in diesem Thema vorgestellte Szenario einzurichten.

#### <a name="location-profiles"></a>Lagerplatzprofile

Die Funktion muss im Lagerplatzprofil für jeden Lagerplatz aktiviert sein, an dem sie verwendet wird.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.
1. Wählen Sie in der Liste der Lagerplatzprofile im linken Bereich **BULK-06** aus.
1. Im Inforegister **Allgemein** wurden zwei neue Optionen durch die Funktion hinzugefügt. Legen Sie die folgenden Werte fest:

    - **Kennzeichenposition aktivieren:** *Ja*

        Wenn diese Option auf *Ja* eingestellt ist, wird die Kennzeichenposition für Kennzeichen am Lagerplatz beibehalten.

    - **LP-Position des Mobilgeräts anzeigen:** *Ja*

        Wenn diese Option auf *Ja* eingestellt ist, wir die Kennzeichenposition den Benutzern mobiler Geräte während der Einstellung und Zählung angezeigt. Sie können die Einstellung dieser Option nur ändern, wenn die Funktion aktiviert ist.

1. Wählen Sie **Speichern** aus.

#### <a name="location-directives"></a>Lagerplatzrichtlinien

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Stellen Sie im linken Bereich sicher, dass das Feld **Arbeitsauftragstyp** auf *Aufträge* eingestellt ist.
1. Wählen Sie in der Liste der Lagerplatzrichtlinien **61 SO Kommissionierreihenfolge** aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie im Inforegister **Positionen** die Position mit einer **Sequenznummer** im Wert von *2* aus.
1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** die Position mit einem **Namen** im Wert von *Entnahme für weniger als Palette* (es sollte die einzige Position sein) aus, und ändern Sie den Wert ihrer **Sequenznummer** auf *2*.
1. Wählen Sie **Neu** oberhalb des Rasters aus, um eine Position für eine neue Lagerplatzrichtlinienaktivität hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Sequenznummer:** *1*
    - **Name:** *Entnahmeposition 1*

1. Wählen Sie **Abfrage bearbeiten** über dem Gitter aus, während die neue Position noch ausgewählt ist.
1. Wählen Sie im Abfrageeditor die Registerkarte **Verknüpfungen** aus.
1. Erweitern Sie die Tabellenverknüpfung **Lagerplätze**, um die Verknüpfung zur Tabelle **Lagerungsdimensionen** anzuzeigen.
1. Erweitern Sie die Tabellenverknüpfung **Lagerungsdimensionen**, um die Verknüpfung zur Tabelle **Verfügbarer Lagerbestand** anzuzeigen.
1. Wählen Sie **Lagerungsdimensionen** und dann **Tabellenverknüpfung hinzufügen** aus.
1. Wählen Sie in der Liste der angezeigten Tabellen in der Spalte **Beziehung** die Option **Kennzeichen (Kennzeichen)** aus. Wählen Sie dann **Auswählen** aus, um **Kennzeichen** zur Tabellenverknüpfung **Lagerungsdimensionen** hinzuzufügen.
1. Während **Kennzeichen** noch ausgewählt ist, wählen Sie **Tabellenverknüpfung hinzufügen** aus.
1. Wählen Sie in der Liste der angezeigten Tabellen in der Spalte **Beziehung** die Option **Standortkennzeichenpositionierung (Kennzeichen)** aus. Wählen Sie dann **Auswählen** aus, um **Standortkennzeichenpositionierung** zur Tabellenverknüpfung **Lagerungsdimensionen** hinzuzufügen.

    ![Tabellenverknüpfungen](media/LpTableJoin.png "Tabellenverknüpfungen")

1. Wählen Sie **OK** aus, um die aktualisierten verknüpften Tabellen zu bestätigen und den Abfrageeditor zu schließen.
1. Wählen Sie im Inforegister **Lagerplatzrichtlinienaktivitäten** erneut die Option **Abfrage bearbeiten** aus, um den Abfrageeditor erneut zu öffnen.
1. Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen** aus, um dem Raster eine Position hinzuzufügen.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **Tabelle:** *Standortkennzeichenpositionierung*
    - **Abgeleitete Tabelle:** *Standortkennzeichenpositionierung*
    - **Feld:** *LP-Position*
    - **Kriterien:** *1*

    ![Neuer Bereich](media/LpPositionCriteria.png "Neuer Bereich")

1. Wählen Sie **OK** aus, um Ihre Änderungen zu bestätigen und den Abfrageeditor zu schließen.

### <a name="set-up-sample-data-for-this-scenario"></a>Beispieldaten für dieses Szenario einrichten

In diesem Szenario muss sich der Benutzer bei der Warehouse Mobile App anmelden, indem er einen Mitarbeiter verwendet, der für Warehouse *61* eingerichtet ist, um die Arbeit durchzuführen. Der Benutzer muss auch Transaktionen abschließen.

Weil mit der Funktion *Standortkennzeichenpositionierung* ein neuer Bezeichner für Kennzeichenpositionen an einem Lagerplatz hinzugefügt wird, müssen Sie zuerst einige Daten erstellen, um das Szenario zu unterstützen.

#### <a name="spot-count-the-first-location"></a>Erste Lagerplatzinventur

1. Öffnen Sie die Warehouse Mobile App, und melden Sie sich bei Warehouse *61* an.
1. Gehen Sie zu **Lagerbestand \> Lagerplatzinventur**.
1. Legen Sie auf der Seite **Lagerplatzinventur** das Feld **Lagerplatz** auf *01A01R1S1B* fest.
1. Wählen Sie **OK**.

    Die Seite zeigt den Lagerplatz, den Sie eingegeben haben. Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“

1. Wählen Sie **Aktualisieren** aus, um eine Zählung am Lagerplatz hinzuzufügen.
1. Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **Artikel** aus, und geben Sie dann den Wert *A0001* ein.
1. Wählen Sie **OK**.
1. Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **LP** aus, und geben Sie dann den Wert *LP1001* (oder eine andere Kennzeichennummer Ihrer Wahl) ein.

    Die Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** zeigt **Kennzeichenposition 1** an.

1. Wählen Sie **OK**.

    Sie müssen nun die Menge des Artikels angeben, die auf dem Kennzeichen gezählt wird.

1. Legen Sie das Feld **Menge** auf *10* fest.
1. Wählen Sie **OK**.

    Die Seite zeigt den Lagerplatz, den Sie eingegeben haben. Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“

1. Wählen Sie **Aktualisieren** aus, um eine weitere Zählung am Lagerplatz hinzuzufügen.
1. Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **Artikel** aus, und geben Sie dann den Wert *A0002* ein.
1. Wählen Sie **OK**.
1. Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **LP** aus, und geben Sie dann den Wert *LP1002* (oder eine andere Kennzeichennummer Ihrer Wahl, sofern sie von der zuvor angegebenen Kennzeichennummer abweicht) ein.
1. Ändern Sie die Kennzeichenposition durch Einstellen des Felds **LP-Position** auf *2*.
1. Wählen Sie **OK**.
1. Geben Sie die Menge des Artikels an, die auf dem Kennzeichen gezählt wird, indem Sie das Feld **Menge** auf *10* festlegen.
1. Wählen Sie **OK**.

    Die Seite zeigt den Lagerplatz, den Sie eingegeben haben. Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“

1. Wählen Sie **OK**.

Die Arbeit ist jetzt abgeschlossen.

#### <a name="spot-count-the-second-location"></a>Zweite Lagerplatzinventur

1. Legen Sie auf der Seite **Lagerplatzinventur** das Feld **Lagerplatz** auf *01A01R1S2B* fest.
1. Wählen Sie **OK**.

    Die Seite zeigt den Lagerplatz, den Sie eingegeben haben. Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“

1. Wählen Sie **Aktualisieren** aus, um eine Zählung am Lagerplatz hinzuzufügen.
1. Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **Artikel** aus, und geben Sie dann den Wert *A0002* ein.
1. Wählen Sie **OK**.
1. Wählen Sie auf der Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** das Feld **LP** aus, und geben Sie dann den Wert *LP1003* (oder eine andere Kennzeichennummer Ihrer Wahl, sofern sie von den beiden im vorherigen Verfahren angegebenen Kennzeichennummern abweicht) ein.

    Die Seite **Inventurzählung: Neue LP oder Artikel hinzufügen** zeigt **Kennzeichenposition 1** an.

1. Wählen Sie **OK**.
1. Geben Sie die Menge des Artikels an, die auf dem Kennzeichen gezählt wird, indem Sie das Feld **Menge** auf *10* festlegen.
1. Wählen Sie **OK**.

    Die Seite zeigt den Lagerplatz, den Sie eingegeben haben. Außerdem wird die folgende Meldung angezeigt: „Lagerplatz abgeschlossen, neue LP oder Artikel hinzufügen?“

1. Wählen Sie **OK**.

Die Arbeit ist jetzt abgeschlossen.

#### <a name="work-details"></a>Arbeitsdetails

> [!NOTE]
> Lagerplatzinventuren aus der mobilen App erstellen Zykluszählarbeit in Microsoft Dynamics 365. Die Arbeit erfordert, dass die Zählungen akzeptiert werden, bevor sie in den Lagerbestand gebucht werden.

1. Melden Sie sich bei Dynamics 365 Supply Chain Management an.
1. Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.
1. Suchen Sie auf der Registerkarte **Überblick** nach Positionen mit den folgenden Werten:

    - **Arbeitsauftragstyp:** *Zykluszählung*
    - **Lagerort:** *61*
    - **Arbeitsstatus:** *Überprüfung ausstehend*

    Für diese Positionen sollten zwei Arbeits-IDs erstellt worden sein. Die Zählungen für diese beiden Arbeits-IDs müssen akzeptiert werden.

1. Wählen Sie im Raster die erste Arbeits-ID für den Arbeitsauftragstyp *Zykluszählung* aus.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeit** in der Gruppe **Arbeit** die Option **Zykluszählung** aus.

    Es werden zwei Positionen angezeigt, eine für jeden Artikel und jedes Kennzeichen. Die Werte in den Feldern **Gezählte Menge**, **Lagerplatz**, **Kennzeichen** und **Artikel** sollten mit den Zähleinträgen übereinstimmen, die Sie auf dem mobilen Gerät erstellt haben. Wenn eines dieser Felder nicht sichtbar ist, wählen Sie im Aktivitätsbereich **Dimensionen anzeigen** aus, um sie dem Raster hinzuzufügen.

1. Wählen Sie beide Positionen aus.
1. Klicken Sie im Aktivitätsbereich auf **Zählung akzeptieren**.
1. Sie erhalten eine Nachricht „Buchung – Erfassung“. Wählen Sie **Nachrichtendetails** aus, um die gebuchte Erfassungsnummer anzuzeigen.
1. Schließen Sie die Nachrichtendetails.
1. Aktualisieren Sie die Seite **Arbeit**.

    Die erste Arbeits-ID wurde geschlossen und wird nicht mehr angezeigt.

    > [!TIP]
    > Um geschlossene Arbeiten anzuzeigen, aktivieren Sie das Kontrollkästchen **Geschlossene anzeigen** über dem Raster.

    Sie akzeptieren nun die Arbeit für das Kennzeichen im Lagerplatz *01A01R1S2B*.

1. Wählen Sie auf der Registerkarte **Übersicht** die zweite Arbeits-ID für den Arbeitsauftragstyp *Zykluszählung* aus.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeit** in der Gruppe **Arbeit** die Option **Zykluszählung** aus.

    Für den Artikel und das Kennzeichen wird eine Position angezeigt. Die Werte in den Feldern **Gezählte Menge**, **Lagerplatz**, **Kennzeichen** und **Artikel** sollten mit den Zähleinträgen übereinstimmen, die Sie auf dem mobilen Gerät erstellt haben.

1. Wählen Sie die Position aus.
1. Klicken Sie im Aktivitätsbereich auf **Zählung akzeptieren**.
1. Sie erhalten eine Nachricht „Buchung – Erfassung“. Wählen Sie **Nachrichtendetails** aus, um die gebuchte Erfassungsnummer anzuzeigen.
1. Schließen Sie die Nachrichtendetails.
1. Aktualisieren Sie die Seite **Arbeit**.

    Die zweite Arbeits-ID wurde geschlossen und wird nicht mehr angezeigt.

    > [!TIP]
    > Um geschlossene Arbeiten anzuzeigen, aktivieren Sie das Kontrollkästchen **Geschlossene anzeigen** über dem Raster.

#### <a name="on-hand-by-location"></a>Verfügbarer Lagerbestand nach Lagerplatz

1. Wechseln Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Verfügbarer Lagerbestand nach Lagerplatz**.
1. Legen Sie die folgenden Werte fest:

    - **Standort:** *6*
    - **Lagerort:** *61*
    - **Standortübergreifend aktualisieren:** *Ja*

1. Beachten Sie, dass der Lagerplatz *01A01R1S1B* zwei Kennzeichen hat:

    - **A0001**, bei dem das Feld **LP-Position** auf *1* festgelegt ist
    - **A0002**, bei dem das Feld **LP-Position** auf *2* festgelegt ist

1. Beachten Sie, dass der Lagerplatz *01A01R1S2B* ein Kennzeichen hat:

    - **A0002**, bei dem das Feld **LP-Position** auf *1* festgelegt ist

### <a name="sales-order-scenario"></a>Szenario für Aufträge

Nun, da die Funktion *Standortkennzeichenpositionierung* eingerichtet und der Lagerbestand bereitgestellt wurde, müssen Sie einen Auftrag erstellen, um Kommissionierarbeiten zu generieren, die den Lagerarbeiter anweisen, Artikel *A0002* vom Lagerort zu kommissionieren, an dem sich die Paletten-ID an Position *1* befindet.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-004*
    - **Lagerort:** *61*

1. Wählen Sie **OK**.
1. Dem Raster im Inforegister **Auftragspositionen** wird eine neue Position hinzugefügt. Legen Sie die folgenden Werte für diese neue Position fest:

    - **Artikelnummer:** *A0002*
    - **Menge** *1*

1. Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** im Aktivitätsbereich die Option **Los reservieren** aus, um Lagerbestand für die Auftragsposition zu reservieren.
1. Schließen Sie die Seite **Reservierung**.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus.

    Sie erhalten eine Informationsnachricht mit der Wellen-ID und der Lieferungs-ID, die für den Auftrag erstellt wurden.

1. Wählen Sie im Inforegister **Auftragspositionen** im Menü **Lagerort** über dem Raster die Option **Arbeitsdetails** aus.
1. Die Seite **Arbeit** wird angezeigt und zeigt die Arbeit, die für die Verkaufsposition erstellt wurde. Notieren Sie sich die angezeigte Arbeits-ID.

### <a name="sales-picking-scenario"></a>Verkaufsauswahlszenario

1. Öffnen Sie die mobile App, und melden Sie sich bei Warehouse *61* an.
1. Gehen Sie zu **Ausgehend \> Verkaufsauswahl**.
1. Wählen Sie auf der Seite **Arbeits-/Kennzeichen-ID scannen** das Feld **ID** aus, und geben Sie dann die Arbeits-ID aus der Verkaufsposition ein.
1. Beachten Sie, dass Sie bei der Kommissionierung angewiesen werden, den Artikel *A0002* vom Lagerplatz *01A01R1S2B* zu kommissionieren. Sie erhalten diese Anweisung, weil sich Artikel *A0002* auf einem Kennzeichen befindet, das in Position *1* an diesem Lagerplatz ist.

    ![Lagerplatz Position 1](media/LocationLicensePlatePositioning.png "Lagerplatz Position 1")

1. Geben Sie die Kennzeichen-ID ein, die Sie für den Lagerplatz erstellt haben, und befolgen Sie die Anweisungen, um den Auftrag auszuwählen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]