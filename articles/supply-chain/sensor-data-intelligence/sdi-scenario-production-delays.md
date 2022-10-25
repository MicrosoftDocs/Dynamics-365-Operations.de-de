---
title: Das Szenario Produktionsverzögerungen
description: Dieser Artikel beschreibt das Szenario „Produktionsverzögerungen“, das eine Meldung erzeugt, wenn der Produktionsdurchsatz unter einen bestimmten Schwellenwert fällt.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 25ccbda1628544f14dc32d9bea3f2162ad47d79e
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690020"
---
# <a name="the-production-delays-scenario"></a>Das Szenario Produktionsverzögerungen

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Das Szenario *Produktionsverzögerungen* generiert eine Benachrichtigung, wenn der Produktionsdurchsatz einen spezifischen Schwellenwert unterschreitet. In diesem Szenario wird ein *part-out*-Signal für jeden produzierten Artikel an Microsoft Azure IoT-Hub gesendet. In Dynamics 365 Supply Chain Management wird die Auftragsverzögerung basierend auf der geplanten Ausführungszeit des Produktionsauftrags, der Anzahl der zu produzierenden Artikel, der Ausführungszeit des Auftrags und der Anzahl der empfangenen *part-out*-Signale berechnet. Eine Verzögerungsbenachrichtigung wird generiert, wenn die Zahl der *part-out*-Signale für den Einzelvorgang den Schwellenwert unterschreitet.

## <a name="scenario-dependencies"></a>Szenarioabhängigkeiten

Das Szenario *Produktionsverzögerungen* weist die Folgenden Abhängigkeiten auf:

- Eine Warnung kann nur ausgelöst werden, wenn ein Produktionsauftrag auf einer zugeordneten Maschine ausgeführt wird.
- Ein Signal, das das *part-out*-Signal einer zugeordneten Maschine darstellt, muss mit einem eindeutigen IoT-Hub und einem eindeutigen Eigenschaftsnamen enthalten sein.
- Eine UNIX-Zeitstempel-Eigenschaft, bei der der Wert in Millisekunden (ms) angegeben wird, muss in der Azure IoT Hub-Nachricht vorhanden sein.

## <a name="prepare-demo-data-for-the-product-delays-scenario"></a>Vorbereitung von Demodaten für das Szenario der Produktverzögerungen

Wenn Sie ein Demosystem verwenden möchten, um das Szenario *Produktionsverzögerungen* zu testen, verwenden Sie ein System, auf dem die Datei [Demodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert ist, wählen Sie die *USMF* juristische Person (Firma) aus und bereiten Sie die zusätzlichen Demodaten wie in diesem Abschnitt beschrieben vor. Wenn Sie Ihre eigenen Sensoren und Daten verwenden, können Sie diesen Abschnitt überspringen.

### <a name="set-up-sensor-simulator"></a>Sensorsimulator einrichten

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

### <a name="configure-the-production-floor-execution-interface"></a>Produktionsausführungsschnittstelle konfigurieren

Falls noch nicht geschehen, konfigurieren Sie die Ausführungsschnittstelle für die Produktion so, dass Aufträge angezeigt werden, die der Ressource *3118* (*Schaumstoffschneidemaschine*) zugewiesen sind. Anweisungen finden Sie in den folgenden Abschnitten.

- [Produktionsausführungsoberfläche konfigurieren](sdi-scenario-equipment-downtime.md#config-pfe)
- [Aktivieren Sie die Suchoption auf der Ausführungsoberfläche der Produktionsstätte](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Starten Sie den ersten Einzelvorgang in der Chargenreihenfolge

Gehen Sie folgendermaßen vor, um den ersten Auftrag in der Chargenreihenfolge zu starten.

1. Gehen Sie zu **Produktionskontrolle \> Fertigungsausführung \> Ausführung in der Produktion**.
1. Geben Sie im Feld **Badge-ID** den Wert *123* ein. Wählen Sie dann **Anmelden** aus.
1. Wenn Sie nach einem Abwesenheitsgrund gefragt werden, wählen Sie eine der Abwesenheitskarten aus und wählen Sie dann **OK**.
1. Geben Sie in das Feld **Suche** die Chargenauftragsnummer ein, die Sie sich zuvor notiert haben. Wählen Sie dann die **Eingabetaste**.
1. Wählen Sie den Auftrag und anschließend **Einzelvorgang starten** aus.
1. Wählen Sie im **Einzelvorgang starten**-Dialogfeld **Starten** aus.

## <a name="set-up-the-production-delays-scenario"></a>Das Szenario der Produktionsverzögerungen einrichten

Gehen Sie folgendermaßen vor, um das Szenario *Produktionsverzögerungen* in Supply Chain Management einzurichten.

1. Wechseln Sie zu **Produktionssteuerung \> Einrichtung \> Sensor Data Intelligence \> Szenarien**.
1. Wählen Sie im Szenariofeld **Produktionsverzögerungen** die Option **Konfigurieren**, um den Einrichtungsassistenten für dieses Szenario zu öffnen.
1. Wählen Sie auf der Seite **Sensoren** die Option **Neu** aus, um dem Raster einen Sensor hinzuzufügen. Legen Sie dann die folgenden Felder fest:

    - **Sensor-ID** – Geben Sie die ID des verwendeten Sensors ein. (Wenn Sie den Raspberry PI Azure IoT Online Simulator verwenden und ihn wie in [Einrichten eines simulierten Sensors für Tests](sdi-set-up-simulated-sensor.md) beschrieben eingerichtet haben, geben Sie *ProductionDelay* ein.)
    - **Sensorbeschreibung** – Geben Sie eine detaillierte Beschreibung des Sensors ein.

1. Wiederholen Sie den vorherigen Schritt für jeden weiteren Sensor, den Sie jetzt hinzufügen möchten. Sie können jederzeit zurückkehren und weitere Sensoren hinzufügen.
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Geschäftsdatensatzzuordnung** im Abschnitt **Sensoren** den Datensatz für einen der Sensoren aus, den Sie gerade hinzugefügt haben.
1. Öffnen Sie im Abschnitt **Geschäftsdatensatzzuordnung** und wählen Sie **Neu** aus, um dem Raster eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile **Geschäftsdatensatz** die Ressource fest, die Sie mit dem ausgewählten Sensor überwachen. (Wenn Sie die Demodaten verwenden, die Sie zuvor in diesem Artikel erstellt haben, setzen Sie sie auf *3118, Schaumschneidemaschine*.)
1. Wählen Sie **Weiter** aus.
1. Führen Sie auf der Seite **Schwellenwert für Produktionsverzögerungsabweichung** die folgenden Schritte aus, wenn Sie die zuvor in diesem Artikel erstellten Demodaten verwenden:

    1. Wählen Sie die **Artikelbeziehung**-Spaltenüberschrift, um ein Dropdown-Dialogfeld zu öffnen, das Suchfilter für die Spalte enthält. Geben Sie *P0111* in das Suchfeld ein und wählen Sie dann **Anwenden**.
    2. Wählen Sie die Position aus, in der das Feld **Vorgang** auf *Trimmen/Schneiden* festgelegt ist. Setzen Sie das Feld **Benachrichtigungsschwelle für Verzögerung (%)** auf den Schwellenwert (in Prozent), bei dem eine Benachrichtigung gesendet werden soll.

1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Sensoren aktivieren** im Raster den Sensor aus, den Sie hinzugefügt haben, und wählen Sie dann **Aktivieren**. Für jeden aktivierten Sensor im Raster erscheint ein Häkchen in der **Aktiv**-Spalte.
1. Wählen Sie **Fertig stellen** aus.

## <a name="work-with-the-production-delays-scenario"></a>Arbeit mit dem Szenario der Produktionsverzögerungen

### <a name="view-production-delay-data-on-the-resource-status-page"></a>Zeigen Sie Produktionsverzögerungsdaten auf der Seite „Ressourcenstatus“ an

Auf der **Ressourcenstatus**-Seite können Supervisoren eine Zeitleiste von Signalen überwachen, die von den Sensoren empfangen werden, die jeder Maschinenressource zugeordnet sind. Gehen Sie folgendermaßen vor, um die Zeitleiste zu konfigurieren.

1. Gehen Sie zu **Produktionssteuerung \> Fertigungssteuerung \> Ressourcenstatus**.
1. Im angezeigten Dialogfeld **Konfigurieren** legen Sie die folgenden Felder fest:

    - **Ressource** – Wählen Sie die Ressourcen, die Sie überwachen möchten. (Wenn Sie mit den Demodaten arbeiten, wählen Sie *3118* aus.)
    - **Zeitreihe 1** – Wählen Sie den Datensatz (Metrikschlüssel) aus, dessen Name das folgende Format hat: *ProductionJobDelayed:ActualQuantity:&lt;JobId&gt;*
    - **Anzeigename** – Geben Sie *Parts out-Signal* ein.
