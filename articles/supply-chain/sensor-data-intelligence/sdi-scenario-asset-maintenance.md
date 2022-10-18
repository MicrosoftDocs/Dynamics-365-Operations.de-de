---
title: Das Szenario der Anlagenwartung
description: Dieser Artikel beschreibt das Asset-Wartungsszenario, mit dem Sie Sensordaten verwenden können, um Zählerdatensätze zu erstellen, die die Nutzung eines Maschinen-Assets nachverfolgen.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: fcd16d09b4293046c457b602857ef8950e8259c6
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644056"
---
# <a name="the-asset-maintenance-scenario"></a>Das Szenario der Anlagenwartung

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Mit dem *Anlagenwartung*-Szenario können Sie Sensordaten verwenden, um Zählerdatensätze zu erstellen. Zähleraufzeichnungen verfolgen die Nutzung eines Maschinenanlagen und werden als Eingabe verwendet, um den Wartungsplan für Maschinenanlagen zu erstellen.

## <a name="video-instructions"></a>Videoanleitungen

Das folgende Video zeigt, wie Sie das Asset Maintenance-Szenario mit standardmäßigen [Demodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) einrichten und ausprobieren. Die verbleibenden Abschnitte in diesem Artikel bieten dieselben Anweisungen in einem textbasierten Format.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58aRW]

## <a name="prepare-demo-data-for-the-asset-maintenance-scenario"></a>Demodaten für das Szenario der Anlagenwartung vorbereite

Wenn Sie ein Demosystem verwenden möchten, um das Szenario *Anlagenwartung* zu testen, verwenden Sie ein System, auf dem die Datei [Demodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert ist, wählen Sie die *USMF* juristische Person (Firma) aus und bereiten Sie die zusätzlichen Demodaten wie in diesem Abschnitt beschrieben vor. Wenn Sie Ihre eigenen Sensoren und Daten verwenden, können Sie diesen Abschnitt überspringen.

In diesem Abschnitt richten Sie die Anlage *AK-101, Luftmesser* in Demodaten als Beispiel ein. Anschließend sehen Sie, wie anstehende Wartungsarbeiten anhand von Sensorsignalen vorhergesagt werden können, die die Anzahl der Stunden messen, die das Luftmesser gelaufen ist. Sie erstellen auch einen Wartungsplan, in dem das Luftmesser alle 10.000 Stunden gewartet werden muss.

### <a name="set-up-a-sensor-simulator"></a>Einen Sensorsimulator einrichten

Wenn Sie dieses Szenario ohne Verwendung eines physischen Sensors ausprobieren möchten, können Sie einen Simulator einrichten, um die erforderlichen Signale zu erzeugen. Weitere Informationen finden Sie unter [Einrichten eines simulierten Sensors für Tests](sdi-set-up-simulated-sensor.md).

### <a name="create-an-asset-counter-to-track-production-hours"></a>Erstellen Sie einen Anlagenzähler, um die Produktionsstunden zu verfolgen

Gehen Sie wie folgt vor, um einen Anlagenzähler zur Verfolgung der Produktionsstunden zu erstellen.

1. Wechseln Sie zu **Anlagenverwaltung \> Einrichtung \> Anlagentypen \> Zähler**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Zählen zu erstellen.
1. Legen Sie in der Kopfzeile die folgenden Werte fest:

    - **Zähler:** *ProductionHr*
    - **Name:** *Produktionsstunden*

1. Legen Sie im Inforegister **Allgemein** die folgenden Werte fest:

    - **Einheit:** *Std*
    - **Aktualisierung:** *Manuell*
    - **Aggregiert gesamt:** *Summe*

1. Wählen Sie auf dem Inforegister **Anlagentypen** **Zeile hinzufügen**.
1. Stellen Sie in der neuen Zeile das Feld **Anlagentyp** auf *Luftmesser* ein.

### <a name="create-a-maintenance-plan-for-the-asset"></a>Erstellen Sie einen Wartungsplan für die Anlage

Folgen Sie diesen Schritten, um einen Wartungsplan für die Anlage zu erstellen.

1. Wechseln Sie zu **Anlagenverwaltung \> Einrichtung \> Vorbeugende Wartung \> Wartungsplan**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Wartungsplan zu erstellen.
1. Legen Sie in der Kopfzeile die folgenden Werte fest:

    - **Wartungsplan:** *AirKnife*
    - **Name:** *Plan für Luftmesser*

1. Legen Sie auf der Inforegisterkarte **Details** die folgenden Werte fest:

    - **Plandatum:** Geben Sie das heutige Datum ein.
    - **Aktiv:** *Ja*

1. Wählen Sie im Inforegister **Positionen** die Option **Anlagenzählerposition hinzufügen** aus, um dem Raster eine Position hinzuzufügen. Stellen Sie dann die folgenden Werte ein:

    - **Arbeitsauftragsbeschreibung:** *Wartung für Luftmesser*
    - **Wartungsjobtyp:** *Vorbeudgend*
    - **Intervalltyp**: *Wiederholt vom letzten Arbeitsauftrag*
    - **Periodenhäufigkeit** *10000*
    - **Zähler:** *ProductionHr*

## <a name="set-up-the-asset-maintenance-scenario"></a>Richten Sie das Szenario der Anlagenwartung ein

Gehen Sie folgendermaßen vor, um das Szenario *Anlagenwartung* in Supply Chain Management einzurichten.

1. Wechseln Sie zu **Anlagenwartung \> Einrichtung \> Sensor Data Intelligence \> Szenarien**.
1. Wählen Sie im Szenariofeld **Anlagenwartung** die Option **Konfigurieren**, um den Einrichtungsassistenten für dieses Szenario zu öffnen.
1. Wählen Sie auf der Seite **Sensoren** die Option **Neu** aus, um dem Raster einen Sensor hinzuzufügen. Legen Sie dann die folgenden Felder fest:

    - **Sensor-ID** – Geben Sie die ID des verwendeten Sensors ein. (Wenn Sie den Raspberry PI Azure IoT Online Simulator verwenden und ihn wie in [Einrichten eines simulierten Sensors für Tests](sdi-set-up-simulated-sensor.md) beschrieben eingerichtet haben, geben Sie *AssetMaintenance* ein.)
    - **Sensorbeschreibung** – Geben Sie eine detaillierte Beschreibung des Sensors ein.

1. Wiederholen Sie den vorherigen Schritt für jeden weiteren Sensor, den Sie jetzt hinzufügen möchten. Sie können jederzeit zurückkehren und weitere Sensoren hinzufügen.
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Geschäftsdatensatzzuordnung** im Abschnitt **Sensoren** den Datensatz für einen der Sensoren aus, den Sie gerade hinzugefügt haben.
1. Öffnen Sie im Abschnitt **Geschäftsdatensatzzuordnung** und wählen Sie **Neu** aus, um dem Raster eine Zeile hinzuzufügen.
1. In der neuen Zeile sollte das Feld **Geschäftsdatensatztyp** automatisch auf *Assets(EntAssetObjectTable)* gesetzt werden. Legen Sie für das Feld **Geschäftsdatensatz** die Ressource fest, die Sie mit dem ausgewählten Sensor überwachen. (Wenn Sie die Demodaten verwenden, die Sie zuvor in diesem Artikel erstellt haben, setzen Sie sie auf *AK-101, AK-101 Luftmesser für Position 1*.)
1. Unmittelbar nachdem Sie einen Geschäftsdatensatztyp für die Zeile ausgewählt haben, die Sie im vorherigen Schritt hinzugefügt haben, wird dem Raster automatisch eine zweite Zeile hinzugefügt. In dieser Zeile sollte das **Geschäftsdatensatztyp**-Feld auf *Counters(EntAssetCounterType)* gesetzt werden. Stellen Sie das **Geschäftsdatensatz**-Feld auf den Anlagenzähler fest, den Sie basierend auf Signalen vom ausgewählten Sensor aktualisieren. (Wenn Sie die Demodaten verwenden, die Sie zuvor in diesem Artikel erstellt haben, setzen Sie sie auf *ProductionHr, Produktionsstunden*.)
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Sensoren aktivieren** im Raster den Sensor aus, den Sie hinzugefügt haben, und wählen Sie dann **Aktivieren**. Für jeden aktivierten Sensor im Raster erscheint ein Häkchen in der **Aktiv**-Spalte.
1. Wählen Sie **Fertig stellen** aus.

## <a name="work-with-the-asset-maintenance-scenario"></a>Arbeiten mit dem Szenario der Anlagenwartung

### <a name="view-counter-values"></a>Zählerwerte anzeigen

Nachdem die Daten vorbereitet sind und das *Anlagenwartung*-Szenario konfiguriert und aktiviert ist, können Sie sehen, wie Datensätze für einen Anlagenzähler basierend auf Sensordaten eingefügt werden.

1. Wechseln Sie zu **Anlagenverwaltung \> Anlagen \> Alle Anlagen**.
1. Suchen Sie die Anlage, die Sie überprüfen möchten, und wählen Sie sie aus. (Wenn Sie die Demodaten verwenden, die Sie zuvor in diesem Artikel erstellt haben, wählen Sie *AK-101*.)
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Anlage** in der Gruppe **Vorbeugend** die Option **Zähler**, um die Seite mit den Zählereinträgen für die Anlage *AK-101* zu öffnen.

### <a name="generate-maintenance-work-orders"></a>Wartungsarbeitsaufträge erstellen

Nachdem Sie das *Anlagenwartung*-Szenario aktiviert haben und den Wartungsplan eingerichtet haben, können Sie den Wartungsplan ausführen, um Wartungsaufträge zu generieren. Weitere Informationen zum Arbeiten mit vorbeugender Instandhaltung finden Sie unter [Übersicht über die vorbeugende Instandhaltung](../asset-management/preventive-and-reactive-maintenance/preventive-maintenance-overview.md).
