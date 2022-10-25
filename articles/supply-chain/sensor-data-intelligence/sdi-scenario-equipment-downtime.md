---
title: Das Szenario des Maschinenstatus
description: Dieser Artikel beschreibt das Maschinenstatus-Szenario, mit dem Sie Sensordaten verwenden können, um die Verfügbarkeit Ihrer Ausrüstung zu überwachen.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 30fdfb898384aea4c1f8cb2f36f9e104cd316f90
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689638"
---
# <a name="the-machine-status-scenario"></a>Das Szenario des Maschinenstatus

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Mit dem *Maschinenstatus*-Szenario können Sie Sensordaten verwenden, um die Verfügbarkeit Ihrer Ausrüstung zu überwachen. Wenn Sie einen Sensor einrichten, der ein Signal sendet, wenn ein Produktionsjob auf einer Maschinenressource eine Ausgabe erzeugt, aber innerhalb eines bestimmten Intervalls kein Sensorsignal empfangen wird, wird eine Benachrichtigung auf dem Dashboard des Supervisors angezeigt.

## <a name="scenario-dependencies"></a>Szenarioabhängigkeiten

Das Szenario *Maschinenstatus* weist die Folgenden Abhängigkeiten auf:

- Eine Benachrichtigung kann nur ausgelöst werden, wenn ein Produktionsauftrag auf einer zugeordneten Maschine läuft.
- Ein Signal, das ein *part-out*-Signal darstellt, muss an den IoT-Hub gesendet werden.

## <a name="prepare-demo-data-for-the-machine-status-scenario"></a>Demo-Daten für das Szenario Maschinenstatus vorbereiten

Wenn Sie ein Demosystem verwenden möchten, um das Szenario *Maschinenstatus* zu testen, verwenden Sie ein System, auf dem die Datei [Demodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert ist, wählen Sie die *USMF* juristische Person (Firma) aus und bereiten Sie die zusätzlichen Demodaten wie in diesem Abschnitt beschrieben vor. Wenn Sie Ihre eigenen Sensoren und Daten verwenden, können Sie diesen Abschnitt überspringen.

### <a name="set-up-a-sensor-simulator"></a>Einen Sensorsimulator einrichten

Wenn Sie dieses Szenario ohne Verwendung eines physischen Sensors ausprobieren möchten, können Sie einen Simulator einrichten, um die erforderlichen Signale zu erzeugen. Weitere Informationen finden Sie unter [Einrichten eines simulierten Sensors für Tests](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Stellen Sie sicher, dass Ressource 3118 für Produkt P0111 verwendet wird

Ein Fertigungsauftrag wird eingeplant und freigegeben. Daher wird ein Produktionsauftrag an die Ressource *3118* (*Schaumschneidemaschine*) freigegeben. Führen Sie diese Schritte aus, um zu überprüfen, dass die Ressource *3118* für Produkt *P0111* in Ihren Demodaten verwendet wird.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Suchen und wählen Sie das Produkt, bei dem das Feld **Artikelnummer** auf *P0111* festgelegt ist.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Techniker** in der Gruppe **Ansicht** die Option **Route** aus.
1. Auf der **Route**-Seite wählen Sie auf der **Überblick**-Registerkarte unten auf der Seite die Zeile aus, in der das Feld **Arbeitsgangnummer** auf *30* festgelegt ist.
1. Vergewissern Sie sich auf der Registerkarte **Ressourcenanforderungen** unten auf der Seite, dass die Ressource *3118* (*Schaumstoffschneidemaschine*) mit dem Vorgang verknüpft ist.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Anlegen und Freigeben eines Fertigungsauftrags für das Produkt P0111

Befolgen Sie diese Schritte, um einen Produktionsauftrag für das Produkt *P0111* zu erstellen und freizugeben.

1. Wechseln Sie zu **Produktionssteuerung \> Produktionsaufträge \> Alle Produktionsaufträge**.
1. Wählen Sie auf der Seite **Alle Produktionsaufträge** im Aktivitätsbereich **Neuer Chargenauftrag**.
1. Legen Sie im Dialogfeld **Charge erstellen** die folgenden Werte fest:

    - **Artikelnummer:** *P0111*
    - **Menge** *10*

1. Wählen Sie **Erstellen**, um den Auftrag zu erstellen und zur Seite **Alle Produktionsaufträge** zurückzukehren.
1. Verwenden Sie das **Filter**-Feld für die Suche nach Fertigungsaufträgen, bei denen das **Artikelnummer**-Feld auf *P0111* eingestellt ist. Suchen Sie dann den soeben erstellten Produktionsauftrag und wählen Sie ihn aus.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produktionsauftrag** in der Gruppe **Prozess** auf **Kalkulieren**.
1. Wählen Sie im Dialogfeld **Schätzen** die Option **OK**, um die Schätzung durchzuführen.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produktionsauftrag** in der Gruppe **Prozess** auf **Freigabe**.
1. Notieren Sie sich im Dialogfeld **Freigabe** die Nummer des soeben erstellten Chargenauftrags.
1. Wählen Sie **OK** aus, um den Auftrag freizugeben.

### <a name="configure-the-production-floor-execution-interface"></a><a name="config-pfe"></a>Produktionsausführungsschnittstelle konfigurieren

Sie verwenden die Ausführungsschnittstelle für die Produktionsebene, um den Job zu starten, der für die Artikelnummer *P0111* im vorherigen Abschnitt geplant und freigegeben wurde. Führen Sie die folgenden Schritte aus, um die Ausführungsschnittstelle für den Produktionsbereich zu konfigurieren.

1. Gehen Sie zu **Produktionskontrolle \> Fertigungsausführung \> Ausführung in der Produktion**.
1. Wenn Sie die Benutzeroberfläche noch nicht eingerichtet haben, wird eine Anmeldeseite angezeigt. Geben Sie Ihre Anmeldeinformationen ein.
1. Wählen Sie auf der Willkommensseite **Konfigurieren** aus, um den Assistenten **Gerät konfigurieren** zu öffnen.
1. Auf der **Gerät konfigurieren – Schritt 1 – Konfiguration auswählen**-Seite wählen Sie die *Standard*-Konfiguration.
1. Wählen Sie **Weiter** aus.
1. Auf der **Gerät konfigurieren – Schritt 2 – Produktionsfläche definieren**-Seite stellen Sie das **Ressource**-Feld auf *3118* ein.
1. Wählen Sie **OK** aus.

### <a name="enable-the-search-option-in-the-production-floor-execution-interface"></a><a name="enable-pfe-search"></a>Aktivieren Sie die Suchoption auf der Ausführungsoberfläche der Produktionsstätte

Um das Auffinden des Produktionsauftrags für den zuvor freigegebenen Produktionsauftrag zu erleichtern, befolgen Sie diese Schritte, um die Suchoption in der Ausführungsschnittstelle für die Produktionsebene zu aktivieren.

1. Gehen Sie zu **Produktionskontrolle \> Einrichtung \> Fertigungsausführung \> Ausführung in der Produktion**.
1. Wählen Sie die Konfiguration *Standard*.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Auf dem Inforegister **Allgemein** legen Sie die Option **Suche aktivieren** auf *Ja* fest.
1. Schließen Sie die Seite.

### <a name="start-the-first-job-in-the-batch-order"></a>Starten Sie den ersten Einzelvorgang in der Chargenreihenfolge

Führen Sie diese Schritte aus, um den für die Ressource *3118* geplanten Job zu starten.

1. Gehen Sie zu **Produktionskontrolle \> Fertigungsausführung \> Ausführung in der Produktion**.
1. Geben Sie im Feld **Badge-ID** den Wert *123* ein. Wählen Sie dann **Anmelden** aus.
1. Wenn Sie nach einem Abwesenheitsgrund gefragt werden, wählen Sie eine der Abwesenheitskarten aus und wählen Sie dann **OK**.
1. Geben Sie in das Feld **Suche** die Chargenauftragsnummer ein, die Sie sich zuvor notiert haben. Wählen Sie dann die **Eingabetaste**.
1. Wählen Sie den Auftrag und anschließend **Einzelvorgang starten** aus.
1. Wählen Sie im **Einzelvorgang starten**-Dialogfeld **Starten** aus.

## <a name="set-up-the-machine-status-scenario"></a>Das Szenario des Maschinenstatus einrichten

Gehen Sie folgendermaßen vor, um das Szenario *Maschinenstatus* in Supply Chain Management einzurichten.

1. Wechseln Sie zu **Produktionssteuerung \> Einrichtung \> Sensor Data Intelligence \> Szenarien**.
1. Wählen Sie im Szenariofeld **Maschinenstatus** die Option **Konfigurieren**, um den Einrichtungsassistenten für dieses Szenario zu öffnen.
1. Wählen Sie auf der Seite **Sensoren** die Option **Neu** aus, um dem Raster einen Sensor hinzuzufügen. Legen Sie dann die folgenden Felder fest:

    - **Sensor-ID** – Geben Sie die ID des verwendeten Sensors ein. (Wenn Sie den Raspberry PI Azure IoT Online Simulator verwenden und ihn wie in [Einrichten eines simulierten Sensors für Tests](sdi-set-up-simulated-sensor.md) beschrieben eingerichtet haben, geben Sie *MachineStatus* ein.)
    - **Sensorbeschreibung** – Geben Sie eine detaillierte Beschreibung des Sensors ein.

1. Wiederholen Sie den vorherigen Schritt für jeden weiteren Sensor, den Sie jetzt hinzufügen möchten. Sie können jederzeit zurückkehren und weitere Sensoren hinzufügen.
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Geschäftsdatensatzzuordnung** im Abschnitt **Sensoren** den Datensatz für einen der Sensoren aus, den Sie gerade hinzugefügt haben.
1. Öffnen Sie im Abschnitt **Geschäftsdatensatzzuordnung** und wählen Sie **Neu** aus, um dem Raster eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile das Feld **Geschäftsdatensatz** auf die Ressource fest, die Sie mit dem ausgewählten Sensor überwachen. (Wenn Sie die Demodaten verwenden, die Sie zuvor in diesem Artikel erstellt haben, setzen Sie das Feld auf *3118, Schaumschneidemaschine*.)
1. Wählen Sie **Weiter** aus.
1. Auf der **Schwellenwert für den Maschinenstatus**-Seite legen Sie fest, wie lange nach dem letzten *part-out*-Signal das System eine Maschinenstatusbenachrichtigung senden soll. Es gibt zwei Möglichkeiten, den Schwellenwert zu definieren:

    - **Standardschwellenwert (Minuten)** – Legen Sie dieses Feld fest, um den Standardschwellenwert zu definieren. Der Wert gilt dann für alle Ressourcen, bei denen das **Schwellenwert zur Bestimmung der nicht reagierenden Maschine (Minuten)**-Feld auf zwei Minuten oder weniger eingestellt ist. Der Mindestwert ist *2* (Minuten).
    - **Schwellenwert zur Bestimmung der nicht reagierenden Maschine (Minuten)** – Geben Sie für jede Ressource im Raster, für die Sie den Standardschwellenwert nicht verwenden möchten, einen Überschreibungswert in dieses Feld ein. Ressourcen, die auf einen Schwellenwert von zwei Minuten oder weniger eingestellt sind, verwenden die **Standardschwellenwert (Minuten)**-Einstellung stattdessen.

    > [!NOTE]
    > Normalerweise verwenden Sie ein *part-out*-Signal zur Überwachung des Maschinenstatus. Daher sollten Sie sicherstellen, dass der Schwellenwert für jede Maschinenressource länger ist als die Maschine benötigt, um jedes Teil zu produzieren.

1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Sensoren aktivieren** im Raster den Sensor aus, den Sie hinzugefügt haben, und wählen Sie dann **Aktivieren**. Für jeden aktivierten Sensor im Raster erscheint ein Häkchen in der **Aktiv**-Spalte.
1. Wählen Sie **Fertig stellen** aus.

## <a name="work-with-the-machine-status-scenario"></a>Arbeiten mit dem Szenario des Maschinenstatus

Nachdem Sie Ihre Sensoren installiert und das Szenario konfiguriert haben, können Sie Maschinenstatusereignisse in Supply Chain Management anzeigen. In diesem Abschnitt wird beschrieben, wo und wie Sie diese Informationen anzeigen können.

### <a name="view-machine-status-data-on-the-resource-status-page"></a>Zeigen Sie Maschinenstatusdaten auf der Seite „Ressourcenstatus“ an

Auf der **Ressourcenstatus**-Seite können Supervisoren eine Zeitleiste von *part-out*-Signal überwachen, die von den Sensoren empfangen werden, die jeder Maschinenressource zugeordnet sind. Gehen Sie folgendermaßen vor, um die Zeitleiste zu konfigurieren.

1. Gehen Sie zu **Produktionssteuerung \> Fertigungssteuerung \> Ressourcenstatus**.
1. Im angezeigten Dialogfeld **Konfigurieren** legen Sie die folgenden Felder fest:

    - **Ressource** – Wählen Sie die Ressourcen, die Sie überwachen möchten. (Wenn Sie mit den Demodaten arbeiten, wählen Sie *3118* aus.)
    - **Zeitreihe 1** – Wählen Sie den Datensatz (Metrikschlüssel) aus, dessen Name das folgende Format hat: *MachineReportingStatus:&lt;Sensor&gt;*
    - **Anzeigename** – Geben Sie *Parts out-Signal* ein.

Die folgende Abbildung zeigt ein Beispiel für Maschinenstatusdaten auf der **Ressourcenstatus**-Seite im Normalbetrieb.

![Maschinenstatusdaten auf der Seite Ressourcenstatus im Standardbetrieb.](media/sdi-resource-status-downtime-up.png "Maschinenstatusdaten auf der Seite Ressourcenstatus im Standardbetrieb")

Die folgende Abbildung zeigt ein Beispiel für Maschinenstatusdaten, wenn eine Ausfallzeit erkannt wird.

![Maschinenstatusdaten auf der Ressourcenstatusseite, wenn eine Ausfallzeit erkannt wird.](media/sdi-resource-status-downtime-down.png "Maschinenstatusdaten auf der Ressourcenstatusseite, wenn eine Ausfallzeit erkannt wird")

### <a name="view-machine-status-on-the-notifications-page"></a>Zeigen Sie den Maschinenstatus auf der Seite „Benachrichtigungen“ an

Auf der **Benachrichtigungen**-Seite können Vorgesetzte die Benachrichtigungen anzeigen, die generiert werden, wenn zu viel Zeit vergangen ist, seit der Sensor zuletzt ein *part-out*-Signal geliefert hat. Jede Benachrichtigung bietet einen Überblick über den Produktionsauftrag, der von dem Ausfall betroffen ist, und bietet die Möglichkeit, den betroffenen Auftrag einer anderen Ressource zuzuweisen.

Um die Seite **Benachrichtigung** zu öffnen, gehen Sie zu **Produktionssteuerung \> Abfragen und Berichte \> Sensor Data Intelligence \> Benachrichtigungen**.

Die folgende Abbildung zeigt das Beispiel einer Maschinenstatusbenachrichtigung.

![Beispiel für eine Meldung über den Maschinenstatus.](media/sdi-resource-status-downtime-notification.png "Beispiel für eine Meldung über den Maschinenstatus")
