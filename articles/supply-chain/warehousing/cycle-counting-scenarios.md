---
title: Beispielszenarien zur Zykluszählung
description: Dieses Thema bietet eine Sammlung von Szenarien, die die Funktionen der Zykluszählung von Microsoft Dynamics 365 Supply Chain Management untersuchen.
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 09ca57d6a3654e56e12240af73d6793002eb1794e4b41d25e182b9b1d3b66df5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746794"
---
# <a name="cycle-counting-example-scenarios"></a>Beispielszenarien zur Zykluszählung

[!include [banner](../includes/banner.md)]

Dieses Thema bietet eine Sammlung von Szenarien, die die Funktionen der Zykluszählung von Microsoft Dynamics 365 Supply Chain Management untersuchen. Es beschreibt zunächst die Anforderungen an Ihre bestehende Supply Chain Management Umgebung. Anschließend wird erklärt, wie Sie die Zykluszählung konfigurieren, und es werden alle Phasen der Zykluszählung beschrieben. Wenn Sie fertig sind, sollten Sie ein gutes Verständnis der Zykluszählung haben, einschließlich der geführten Zykluszählung, der blinden Zykluszählung, der Spot-Zykluszählung, der Zykluszählungsschwellenwerte und der Zykluszählungspläne.

## <a name="prerequisites"></a>Voraussetzungen

### <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Jedes Szenario in diesem Thema verweist auf Werte und Datensätze, die in den Standard-Demodaten enthalten sind, die für Supply Chain Management bereitgestellt werden. Wenn Sie die hier bereitgestellten Werte beim Durcharbeiten der Szenarien verwenden möchten, stellen Sie sicher, dass Sie in einer Umgebung arbeiten, in der die Demo-Daten installiert sind, und legen Sie die juristische Entität (Firma) auf **USMF** fest, bevor Sie beginnen.

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a>Schalten Sie die Unterstützung für die Warehouse Management Mobile-App ein

Bevor Sie die neue Warehouse Management Mobile-App verwenden können, müssen Sie die Unterstützung dafür in Ihrem System einschalten. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Benutzereinstellungen, Symbole und Schritttitel für die neue Lagerort-App*

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a>Bereiten Sie Demo-Daten für die Szenarien vor

Führen Sie die folgenden Schritte aus, um sicherzustellen, dass alle für die Szenarien erforderlichen Demodaten in der Firma USMF in Ihrem System vorhanden sind. Erstellen Sie alle Datensätze oder Werte, die fehlen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeitskraft**.
1. Wählen Sie im Listenbereich **Julia Funderburk**.
1. Wählen Sie im Inforegister **Benutzer** die Zeile aus, die die folgenden Werte enthält. Wenn keine Zeile mit diesen Werten vorhanden ist, erstellen Sie sie.

    - **Benutzer-ID:** *61*
    - **Benutzername:** *WH61*
    - **Standardlagerort:** *61*
    - **Menüname:** *Hauptseite*

1. Legen Sie auf dem Inforegister **Arbeit** die folgenden Werte für den Benutzer *61* fest, wenn sie nicht bereits festgelegt sind:

    - **Ist eine Zykluszählung Supervisor:** *Nein*
    - **Maximale Prozentgrenze:** *0*
    - **Maximale Mengenbegrenzung:** *0*
    - **Maximale Wertgrenze:** *0*

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitspools**.
1. Arbeitspools werden verwendet, um Lagerortarbeit zu trennen, basierend auf der Art der Arbeit (in diesem Fall Zykluszählungsarbeit). Stellen Sie sicher, dass ein Datensatz mit den folgenden Einstellungen vorhanden ist:

    - **Arbeitspool-ID:** *CycleCount*
    - **Beschreibung:** *Zykluszählung*

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Listenbereich den Datensatz aus, der den Namen *Zykluszählung* trägt. Wenn kein Datensatz mit diesem Namen vorhanden ist, erstellen Sie ihn. Bestätigen Sie oder legen Sie die folgenden Werte für den Datensatz fest:

    - **Name des Menüelements:** *Zykluszählung*
    - **Titel:** *Zykluszählung angeleitet*
    - **Modus:** *Arbeit*
    - **Vorhandene Arbeit verwenden:** *Ja*
    - **Geführt von:** *Systemgeführt* (Dieser Wert zeigt an, dass Supply Chain Management der Arbeitskraft eine ID für Zykluszählungsarbeiten zuweist.)
    - **Status des Bestands anzeigen:** *Ja*

1. Wählen Sie im Aktionsbereich **Zykluszählung**.
1. Bestätigen oder legen Sie im Dialogfeld **Zykluszählung für mobile Geräte** die folgenden Werte fest:

    - **Elementnummer anzeigen:** *Ja*
    - **Kennzeichen anzeigen:** *Ja*
    - **Anzahl der Versuche:** *1*

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.
1. Wählen Sie im Listenbereich den Datensatz mit der Bezeichnung *Zykluszählung blind*. Wenn kein Datensatz mit diesem Namen vorhanden ist, erstellen Sie ihn. Bestätigen Sie oder legen Sie die folgenden Werte für den Datensatz fest:

    - **Name des Menüelements:** *Zykluszählung Blind*
    - **Titel:** *Zykluszählung Blind*
    - **Modus:** *Arbeit*
    - **Vorhandene Arbeit verwenden:** *Ja*
    - **Geführt von:** *Zykluszählung gruppieren* (Dieser Wert gibt an, dass die Arbeitskraft Zykuszählungsarbeiten gruppieren kann, die für einen Lagerplatz, eine Zone oder einen Arbeitspool spezifisch sind.)

1. Wählen Sie im Aktionsbereich **Zykluszählung**.
1. Bestätigen oder legen Sie im Dialogfeld **Zykluszählung für mobile Geräte** die folgenden Werte fest:

    - **Elementnummer anzeigen:** *Nein*
    - **Ladungsträger anzeigen:** *Nein*
    - **Anzahl der Versuche:** *0*

1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.
1. Wählen Sie im Listenbereich den Datensatz mit der Bezeichnung *Versuchszählung*. Wenn kein Datensatz mit diesem Namen vorhanden ist, erstellen Sie ihn. Bestätigen Sie oder legen Sie die folgenden Werte für den Datensatz fest:

    - **Name des Menüelements:** *Punktzählung*
    - **Titel:** *Punktzählung*
    - **Modus:** *Arbeit*
    - **Vorhandene Arbeit verwenden:** *Nein*
    - **Arbeitserstellungsprozess:** *Spot-Zykluszählung* (Dieser Wert gibt an, dass die Arbeitskraft jederzeit Artikel an einem Lagerplatz zählen kann, ohne Zykluszählungsarbeit zu erstellen. Um eine Spot-Zykluszählung an einem Lagerplatz durchzuführen, gibt die Arbeitskraft die Lagerplatz-ID ein.)

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.
1. Wählen Sie im Listenbereich den Datensatz mit dem Namen *Bestand*. Wenn kein Datensatz mit diesem Namen vorhanden ist, erstellen Sie ihn. Bestätigen Sie, dass die folgenden Elemente des Menüs Zykluszählung in der Spalte **Menüstruktur** erscheinen:

    - Inventurzählung
    - Zykluszählung blind
    - Spot-Zählung

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.
1. Legen Sie auf der Registerkarte **Zykluszählung** die folgenden Werte fest:

    - **Standardtyp für die Zykluszählung:** *Zykluszählung* (Dieses Feld gibt den Journaltyp an, der bei der Zykluszählung gebucht wird.)
    - **Standard-ID der Zykuszählungsarbeitsklasse:** *CCount* (Dieses Feld gibt die Arbeitsklasse an, die für die Zykluszählung verwendet wird.)
    - **Standardpriorität der Zykuszählungsarbeit:** *50* (Dieses Feld legt die Priorität fest, die Zykuszählungsarbeit im Verhältnis zu anderen Arten von Arbeit im Lagerort hat. Indem Sie eine Zahl eingeben, die niedriger ist als die Zahl, die für andere Arbeitsarten eingegeben wird, erhöhen Sie die Priorität der Zykuszählungsarbeit).

1. Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Bestand \> Anpassungsarten**.
1. Auf der Seite **Anpassungstypen** können Sie Codes für die verschiedenen Ein- und Auslagerungen erstellen, die auftreten können. Vergewissern Sie sich, dass ein Datensatz vorhanden ist, der die folgenden Einstellungen hat:

    - **Bestandskorrektur-Typ:** *Zykluszählung*
    - **Beschreibung:** *Zykluszählung*
    - **Name:** *ICnt*

1. Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Lagerort einrichten \> Lagerorte**.
1. Wählen Sie im Listenbereich den Lagerort *61*. Wenn kein Datensatz mit diesem Namen vorhanden ist, erstellen Sie ihn.
1. Legen Sie auf dem Inforegister **Lagerort** die folgenden Werte fest:

    - **Prozess der Lagerortverwaltung verwenden:** *Ja* (Dieser Wert aktiviert den Lagerort für Prozesse der Lagerortverwaltung.)
    - **Bewegungen von Ladungsträgern während der Zykluszählung zulassen:** *Ja* (Dieser Wert ermöglicht den Arbeitskräften, Ladungsträger während einer Zykluszählung zu bewegen.)

## <a name="scenario-1-guided-cycle-counting"></a>Szenario 1: Geführte Zykluszählung

Bevor eine geführte Zykluszählung stattfinden kann, müssen Sie eine Arbeit erstellen. Diese Arbeit wird die zugewiesene Person durch das Lager führen, von Lagerplatz zu Lagerplatz, um die Zählungen durchzuführen, die in der Arbeit festgelegt sind.

### <a name="create-cycle-counting-work-for-scenario-1"></a>Zykluszählungsarbeit für Szenario 1 erstellen

Führen Sie die folgenden Schritte aus, um Zykluszählungsarbeit für den Elementplatz *01A02R2S2B* (BULK-06) im Lagerort *61* zu erstellen.

1. Gehen Sie zu **Lagerortverwaltung \> Zykluszählung \> Zykluszählungsarbeit nach Lagerort**.
1. Legen Sie in der Dialogbox **Zykluszählungsarbeit nach Lagerplatz erstellen** das Feld **Arbeitspool-ID** auf *CycleCount* fest.
1. Wählen Sie auf der Seite **Einschließende Datensätze** Inforegister die Option **Filter**.
1. Führen Sie im Dialogfeld Abfrage-Editor auf der Registerkarte **Bereich** die folgenden Schritte aus:

    - Für die Zeile, in der das Feld **Feld** auf *Lagerort* festgelegt ist, legen Sie das Feld **Kriterien** auf *61* fest.
    - Für die Zeile, in der das Feld **Feld** auf *Lagerplatz* festgelegt ist, setzen Sie das Feld **Kriterien** auf *01A02R2S2B*.

1. Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.
1. Wählen Sie **OK**, um das Dialogfeld **Zykuszählungsarbeit nach Lagerplatz erstellen** zu schließen.

    Wenn der Prozess der Arbeitserstellung abgeschlossen ist, erscheint eine Nachricht im Aktionscenter.

1. Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.
1. Finden Sie die neu erstellte Arbeit, indem Sie einen Filter auf die Spalte **Arbeitspool ID** setzen, um Datensätze zu finden, die einen Wert von *CycleCount* haben.

### <a name="do-cycle-counting-work-for-scenario-1"></a>Zykluszählungsarbeit für Szenario 1 durchführen

Nachdem Sie die Zykluszählungsarbeit erstellt haben, führen Sie die Arbeit durch, indem Sie die Artikel an einem Lagerplatz zählen und dann ein mobiles Gerät verwenden, um die Ergebnisse in die Supply Chain Management einzugeben. Folgen Sie diesen Schritten, um die Zykluszählungsarbeit in der Warehouse Management Mobile-App durchzuführen.

1. Melden Sie sich bei der Warehouse Management Mobile-App als der Arbeitsbenutzer an, den Sie im Abschnitt [Demodaten für die Szenarien vorbereiten](#prepare-demo-data) weiter oben in diesem Thema festgelegt haben. Für das Beispiel in diesem Thema heißt der Benutzer *Julia Funderburk* und ist für den Lagerort *61* festgelegt. (In den USMF-Demodaten sollten Sie sich als dieser Arbeitsbenutzer anmelden können, indem Sie *61* als Benutzer-ID und *1* als Kennwort eingeben.)
1. Wählen Sie im Hauptmenü **Bestand**.
1. Wählen Sie im Menü **Bestand** die Option **Zykluszählung angeleitet**.
1. Wählen Sie das Feld **Anzahl**, geben Sie *9* mit Hilfe des Nummernblocks ein und wählen Sie dann **OK** (die Schaltfläche mit dem Häkchen).
1. Das System hat erwartet, dass Sie eine Anzahl von 10 Stück für dieses Element, den Lagerplatz und den Ladungsträger eingeben. Daher werden Sie aufgefordert, nachzuzählen. Wählen Sie das Feld **Anzahl**, geben Sie *9* erneut über den Nummernblock ein und wählen Sie dann **OK** (die Schaltfläche mit dem Häkchen). Beim zweiten Versuch wird Ihre Zählung akzeptiert.

    > [!NOTE]
    > Als das System eine Differenz zwischen dem erwarteten Lagerbestand und der von Ihnen eingegebenen Menge feststellte, forderte es Sie auf, ein zweites Mal zu zählen, weil das Feld **Anzahl der Versuche** für den Menüpunkt **Zykuszählung geführt** für mobile Geräte auf *1* festgelegt ist. Sie wurden zu einer bestimmten Elementnummer und einem bestimmten Ladungsträger angeleitet, weil sowohl die Option **Elementnummer anzeigen** als auch die Option **Ladungsträger anzeigen** für den Menüpunkt für mobile Geräte auf *Ja* festgelegt sind.

1. Wählen Sie **OK** (die Schaltfläche mit dem Häkchen).

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a>Überprüfen der Unterschiede bei der Zykluszählung für Szenario 1

Führen Sie diese Schritte aus, um die Unterschiede in der Zykluszählung zu überprüfen.

1. Kehren Sie zum Supply Chain Management zurück.
1. Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.
1. Suchen Sie die Zykluszählungsarbeit, die Sie sich zuvor angesehen haben, und wählen Sie sie aus. (Legen Sie z.B. einen Filter auf die Spalte **Arbeitspool ID** fest, um Datensätze zu finden, die einen Wert von *CycleCount* haben.) Beachten Sie, dass das Feld **Arbeitsstatus** für diese Arbeit jetzt auf *Ausstehende Überprüfung* festgelegt ist.

    > [!NOTE]
    > Für das Benutzerkonto der Arbeit, mit dem Sie die Zykluszählungsarbeit durchgeführt haben, ist die Option **Zykluszählungs-Aufsicht** auf *Nein* festgelegt und die Felder **Maximale Prozentgrenze**, **Maximale Mengengrenze** und **Maximale Wertgrenze** sind alle auf *0* (Null) festgelegt. Daher müssen alle Zähldifferenzen, die dieser Benutzer meldet, manuell genehmigt werden, und das Feld **Arbeitsstatus** für die betreffende Arbeit wird auf *Anstehende Überprüfung* festgelegt. Wäre der gezählte Wert innerhalb der Abweichungsgrenzen (wie in den Feldern **Maximale Prozentgrenze** oder **Maximale Mengengrenze** auf der Seite **Arbeitsbenutzer** festgelegt), oder wenn die Option **Zykluszählung Supervisor** für den Benutzer auf *Ja* festgelegt wäre, wäre die Arbeit automatisch geschlossen worden.

1. Wählen Sie im Aktionsbereich auf der Registerkarte **Arbeit** die Option **Zykluszählung**.
1. Klicken Sie im Aktivitätsbereich auf **Zählung akzeptieren**.

    Die Differenz wird mit Hilfe des Standard-Zähljournals gebucht und ein neuer Arbeitsauftrag erstellt.

1. Wählen Sie auf der Seite **Zykluszählungstransaktionen** im Aktionsbereich **Abgeleitete Arbeit**, um die Arbeit zu finden, die für die genehmigte Differenz erstellt wurde.

## <a name="scenario-2-blind-cycle-counting"></a>Szenario 2: Blinde Zykluszählung

Dieses Szenario setzt voraus, dass Szenario 1 in Ihrem System bereits abgeschlossen ist.

### <a name="create-cycle-counting-work-for-scenario-2"></a>Zykluszählungsarbeit für Szenario 2 erstellen

Bevor die blinde Zykluszählung erfolgen kann, müssen Sie Arbeit erstellen. Führen Sie die folgenden Schritte aus, um Zykluszählungsarbeit für den Elementplatz *01A02R2S2B* (BULK-06) im Lagerort *61* zu erstellen.

1. Gehen Sie zu **Lagerortverwaltung \> Zykluszählung \> Zykluszählungsarbeit nach Element**.
1. In der Dialogbox **Zykuszählungsarbeit nach Element erstellen** legen Sie das Feld **Arbeitspool-ID** auf *CycleCount* fest.
1. Wählen Sie auf der Seite **Einschließende Datensätze** Inforegister die Option **Filter**.
1. Fügen Sie im Dialogfeld „Abfrage-Editor“ auf der Registerkarte **Bereich** drei Zeilen hinzu, die die folgenden Einstellungen haben:

    - Zeile 1:

        - **Tabelle:** *Artikel*
        - **Feld:** *Artikelnummer*
        - **Kriterien:** *L0101*

    - Zeile 2:

        - **Tabelle:** *Bestandsdimensionen*
        - **Feld:** *Lagerort*
        - **Kriterien:** *61*

    - Zeile 3:

        - **Tabelle:** *Bestandsdimensionen*
        - **Feld:** *Lagerplatz*
        - **Kriterien:** *01A02R2S2B*

1. Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.
1. Wählen Sie **OK**, um das Dialogfeld **Zykuszählungsarbeit nach Element erstellen** zu schließen.

    Wenn der Arbeitserstellungsprozess abgeschlossen ist, erhalten Sie eine informative Nachricht.

### <a name="do-cycle-counting-work-for-scenario-2"></a>Zykluszählungsarbeit für Szenario 2 durchführen

Nachdem Sie die Zykluszählungsarbeit erstellt haben, folgen Sie diesen Schritten, um die Arbeit in der Warehouse Management Mobile-App auszuführen.

1. Melden Sie sich bei der Warehouse Management Mobile-App als der Arbeitsbenutzer an, den Sie im Abschnitt [Demodaten für die Szenarien vorbereiten](#prepare-demo-data) weiter oben in diesem Thema festgelegt haben. Für das Beispiel in diesem Thema heißt der Benutzer *Julia Funderburk* und ist für den Lagerort *61* festgelegt. (In den USMF-Demodaten sollten Sie sich als dieser Arbeitsbenutzer anmelden können, indem Sie *61* als Benutzer-ID und *1* als Kennwort eingeben.)
1. Wählen Sie im Hauptmenü **Bestand**.
1. Wählen Sie im Menü **Inventar** die Option **Zykluszählung blind**.
1. Wählen Sie das Feld **Zonen-ID**, geben Sie *BULK06* ein und wählen Sie dann **OK** (die Schaltfläche mit dem Häkchen).
1. Wählen Sie das Feld **Element**, geben Sie *L0101* ein, und wählen Sie dann **OK** (die Schaltfläche mit dem Häkchen).
1. Wählen Sie das Feld **Kennzeichen**, geben Sie *LP \_BULK \_06\_01* ein, und wählen Sie dann **OK** (die Schaltfläche mit dem Häkchen).
1. Wählen Sie das Feld **Anzahl**, geben Sie *10* ein, und wählen Sie dann **OK** (die Schaltfläche mit dem Häkchen).

    > [!NOTE]
    > Obwohl das System eine Differenz zwischen dem erwarteten Lagerbestand und der Menge, die Sie gescannt haben, festgestellt hat, hat es Sie nicht aufgefordert, ein zweites Mal zu zählen, weil das Feld **Anzahl der Versuche** für den Menüpunkt **Zykluszählung blind** des mobilen Geräts auf *0* (Null) festgelegt ist. Sie wurden aufgefordert, die Elementnummer und den Ladungsträger zu scannen, weil sowohl die Option **Elementnummer anzeigen** als auch die Option **Ladungsträger anzeigen** für den Menüpunkt des mobilen Geräts auf *Nein* festgelegt sind.

1. Wählen Sie **OK** (die Schaltfläche mit dem Häkchen).

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a>Überprüfen Sie die Unterschiede bei der Zykluszählung für Szenario 2

Führen Sie diese Schritte aus, um die Unterschiede in der Zykluszählung zu überprüfen.

1. Kehren Sie zum Supply Chain Management zurück.
1. Gehen Sie zu **Lagerortverwaltung \> Allgemein \> Arbeit \> Zykuszählungsarbeit zur Überprüfung**.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Arbeit** die Option **Zykluszählung**.
1. Wählen Sie im Aktionsbereich **Zählung zurückweisen**.

    Da die Zähldifferenz abgelehnt wurde, wird die Arbeit geschlossen.

## <a name="scenario-3-spot-cycle-counting"></a>Szenario 3: Spot-Zykluszählung

Der Datensatz zum Lagerbestand besagt, dass sich ein Lagerbestand des Elements *L0101* an Lagerplatz *01A02R2S2B* befindet. Die Arbeitskraft im Lagerort befindet sich an Platz *01A02R2S1B*. Obwohl dieser Lagerplatz leer sein sollte, ist er voll. Daher führt die Arbeitskraft an diesem Lagerort sofort eine Zählung durch.

### <a name="do-cycle-counting-work-for-scenario-3"></a>Führen Sie Zykluszählungsarbeiten für Szenario 3 durch

Folgen Sie diesen Schritten, um die Zykluszählungsarbeit in der Warehouse Management Mobile-App durchzuführen.

1. Melden Sie sich bei der Warehouse Management Mobile-App als der Arbeitsbenutzer an, den Sie im Abschnitt [Demodaten für die Szenarien vorbereiten](#prepare-demo-data) weiter oben in diesem Thema festgelegt haben. Für das Beispiel in diesem Thema heißt der Benutzer *Julia Funderburk* und ist für den Lagerort *61* festgelegt. (In den USMF-Demodaten sollten Sie sich als dieser Arbeitsbenutzer anmelden können, indem Sie *61* als Benutzer-ID und *1* als Kennwort eingeben.)
1. Wählen Sie im Hauptmenü **Bestand**.
1. Wählen Sie im Menü **Bestand** die Option **Stichprobenzählung**.
1. Wählen Sie das Feld **Lagerplatz**, geben Sie *01A02R2S1B* ein und wählen Sie dann **OK** (die Schaltfläche mit dem Häkchen).

    Das System erkennt, dass der Lagerplatz im Supply Chain Management leer ist.

1. Wählen Sie **LP oder Element hinzufügen**.
1. Wählen Sie das Feld **Element**, geben Sie *L0101* ein, und wählen Sie dann **OK** (die Schaltfläche mit dem Häkchen).
1. Wählen Sie das Feld **Kennzeichen**, geben Sie *LP \_BULK \_06\_01* ein, und wählen Sie dann **OK** (die Schaltfläche mit dem Häkchen).
1. Wählen Sie das Feld **Anzahl**, geben Sie *9* ein und wählen Sie dann **OK** (die Schaltfläche mit dem Häkchen).

    Da das System erkennt, dass der angegebene Ladungsträger bereits an einem anderen Lagerplatz im Supply Chain Management vorhanden ist, wird dieser Ladungsträger an den aktuellen Lagerplatz verschoben. Daher fordert das System Sie auf, die Verschiebung zu bestätigen.

1. Wählen Sie **OK** (die Schaltfläche mit dem Häkchen).

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a>Überprüfen der Unterschiede bei der Zykluszählung für Szenario 3

Gehen Sie wie folgt vor, um die Zählergebnisse zu überprüfen.

1. Kehren Sie zum Supply Chain Management zurück.
1. Gehen Sie zu **Lagerortverwaltung \> Allgemein \> Arbeitsdetails**.
1. Aktivieren Sie das Kontrollkästchen **Geschlossene anzeigen** am oberen Rand des Rasters.
1. Legen Sie den Filter für die Spalte **Arbeitsauftragstyp** auf *Bestandsbewegung* fest.

    Das System hat diese Zählung automatisch als eine Bestandsbewegung erkannt. Diese Bewegung ist zulässig, weil die Option **Ladungsträgerbewegungen während der Zykluszählung zulassen** auf der Seite **Lagerorte** für Lagerort *61* auf *Ja* festgelegt ist.

## <a name="scenario-4-define-cycle-count-thresholds"></a>Szenario 4: Schwellenwerte für die Zykluszählung definieren

Eine Möglichkeit, Zykluszählungsarbeiten zu erstellen, ist die Verwendung von Schwellenwerten. Ein Schwellenwert für die Zykluszählung gibt die Mengen- oder Prozentgrenze von Bestandspositionen an. Zykluszählungsarbeiten werden automatisch erstellt, wenn der Schwellenwert erreicht ist.

Beispiel: An einem Lagerplatz mit einem Schwellenwert für die Zykluszählung von 40 befinden sich 60 Elemente. Während einer Auftragsbuchung werden 25 Artikel vom Lagerplatz entnommen und in den Staginglagerplatz gelegt. Da die Menge des neuen Artikels mit 35 geringer ist als die Schwellenmenge, wird automatisch Zykluszählungsarbeit für den Speicherort erstellt.

Gehen Sie wie folgt vor, um Schwellenwerte für die Zykluszählung festzulegen.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Zykluszählung \> Schwellenwerte für Zykluszählung**.
1. Wählen Sie im Aktionsbereich **Neu**, um einen Schwellenwert zu erstellen, und legen Sie die folgenden Werte dafür fest:

    - **Schwellenwert der Zykluszählung ID:** *L0101*
    - **Beschreibung:** *Schwellenwert L0101*
    - **Schwellenwert Menge:** *2*
    - **Einheit:** *ea*
    - **Kapazitätsschwelle basierend auf Prozent:** *0,00*
    - **Typ des Schwellenwerts für die Zykluszählung:** *Menge*
    - **Zykluszählung sofort verarbeiten:** *Ja*
    - **Tage zwischen Zykluszählungen:** *1*
    - **Arbeitspool-ID:** *CycleCount*

1. Wählen Sie im Aktionsbereich **Elemente auswählen**.
1. Suchen Sie im Dialogfeld des Abfrage-Editors auf der Registerkarte **Bereich** die Zeile, in der das Feld **Feld** auf *Elementnummer* festgelegt ist. Legen Sie das Feld **Kriterium** für diese Zeile auf *L0101* fest.
1. Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.

    Sie haben jetzt eine Schwelle für die Zykluszählung für das Element *L0101* definiert.

Die Zykluszählung wird nun für das Element *L0101* an einem beliebigen Lagerplatz erstellt, wenn der Lagerbestand kleiner als 2 ist und wenn das Datum der letzten Zykluszählung für den Lagerplatz nicht heute ist.

## <a name="scenario-5-define-cycle-count-plans"></a>Szenario 5: Definieren von Zykluszählungsplänen

Mit Zykluszählungsplänen können Sie die Erstellung von Zykluszählungsarbeiten automatisieren. Sie können jeden Zykluszählungs-Plan mit spezifischen Element- und Lagerplatz-Abfragen festlegen. Wenn der Batch-Auftrag ausgeführt wird, erstellt er Zykluszählungsarbeiten für alle Lagerplätze, die den Element- und Lagerplatzkriterien entsprechen (bis zu der maximalen Anzahl von Zählungen, die für den Plan angegeben ist). Wenn Zykluszählungsarbeit erstellt wird, enthält die Zählarbeitszeile Informationen über den Lagerplatz, der gezählt werden muss. Der Lagerbestand, der mit diesem Lagerplatz verbunden ist, ist nicht gesperrt. Daher ist er für die Reservierung und ausgehende Verarbeitung verfügbar, auch wenn offene Zählarbeit vorhanden ist.

Gehen Sie wie folgt vor, um einen Plan für die Zykluszählung festzulegen.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Zykluszählung \> Zykluszählungspläne**.
1. Wählen Sie im Aktionsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen, und legen Sie die folgenden Werte dafür fest:

    - **Plan für Zykluszählung ID:** *BULK06*
    - **Beschreibung:** *Zählung des Lagerplatzes für BULK06*
    - **Arbeitspool-ID:** *CycleCount*
    - **Maximale Anzahl von Zykluszählungen:** *10*
    - **Tage zwischen Zykluszählungen:** *10*
    - **Leere Lagerplätze:** *Leere ausschließen*
    - **Arbeitsvorlage:** Lassen Sie dieses Feld leer.

1. Wählen Sie im Aktionsbereich **Lagerplätze auswählen**.
1. Ein Standard-Dialogfeld für den Abfrage-Editor wird angezeigt. Fügen Sie auf der Registerkarte **Bereich** eine Zeile hinzu, und legen Sie die folgenden Werte dafür fest:

    - **Tabelle:** *Lagerorte*
    - **Feld:** *Zonen-ID*
    - **Kriterien:** *BULK06*

1. Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.
1. Wählen Sie im Aktionsbereich **Plan zur Zykluszählung verarbeiten**.
1. Legen Sie im Dialogfeld **Zykluszählung planen** auf dem Inforegister **Im Hintergrund ausführen** die Option **Batch-Verarbeitung** auf *Ja* fest.
1. Wählen Sie **Wiederholung**.
1. Legen Sie im Dialogfeld **Wiederholung definieren** den Batchauftrag so fest, dass er sofort beginnt und einmal pro Minute ausgeführt wird, und dass es kein Enddatum gibt.
1. Wählen Sie **OK**, um das Dialogfeld **Wiederholung definieren** zu schließen.
1. Wählen Sie **OK**, um das Dialogfeld **Zykuszählung planen** zu schließen.

    Eine Nachricht informiert Sie darüber, dass der Auftrag zur Batch-Warteschlange hinzugefügt wurde.

1. Gehen Sie zu **Lagerortverwaltung \> Allgemein \> Zykluszählung planen**. Der Plan beginnt sofort und erstellt Zählarbeit. Da die Zählarbeit noch nicht abgeschlossen ist, wird das Feld **Status** auf *In Bearbeitung* festgelegt. Nach einer Minute ändert sich der Wert in der Spalte **Gesamte Zykluszählungen** auf *1*.

    > [!NOTE]
    > Zykuszählungsarbeit wird nicht erstellt, wenn die Anzahl der Tage seit der letzten Zykluszählung kleiner ist als der Wert, den Sie für das Feld **Tage zwischen Zykluszählungen** für den Zykluszählungsplan festgelegt haben. Wenn zum Beispiel das Feld **Tage zwischen Zykluszählung** auf *5* festgelegt ist, werden Zykuszählungsarbeiten alle fünf Tage erstellt. Wenn jedoch eine Zykluszählungsarbeit an Tag drei verarbeitet wird, wird die nächste Zykluszählungsarbeit fünf Tage nachdem die letzte Zykluszählung verarbeitet wurde, erstellt, am Tag acht.

1. Wählen Sie im Aktionsbereich **Arbeit**, um die erstellte Zählarbeit anzuzeigen.
