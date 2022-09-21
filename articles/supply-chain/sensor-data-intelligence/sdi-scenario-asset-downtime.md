---
title: Das Szenario der Anlagendowntime
description: In diesem Artikel wird das Szenario der Anlagenausfallzeiten beschrieben, mit dem Sie die Verfügbarkeit Ihrer Anlagen mithilfe von Sensordaten überwachen können.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetObjectProductionStop
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 944818557deebed06c02c00fd69de6e8f08bda83
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428375"
---
# <a name="the-asset-downtime-scenario"></a>Das Szenario der Anlagendowntime

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Das Anlagendowntime-Szenario generiert einen Wartungs-Downtime-Datensatz, wenn innerhalb eines definierten Zeitschwellenwerts seit dem Empfang des letzten Signals kein Signal von einer Maschine empfangen wird. Das Szenario erfordert, dass Sie Ihre Maschine mit einem Sensor ausstatten, der regelmäßig ein Signal an Ihren Azure IoT Hub sendet, während die Maschine in Betrieb ist, aber kein Signal sendet, wenn die Maschine nicht in Betrieb ist.

## <a name="set-up-the-asset-downtime-scenario"></a>Richten Sie das Szenario der Anlagendowntime ein

Gehen Sie folgendermaßen vor, um das Szenario *Anlagendowntime* in Supply Chain Management einzurichten.

1. Wechseln Sie zu **Anlagenverwaltung \> Einrichtung \> Sensor Data Intelligence \> Szenarien**, um die Seite **Szenarien** zu öffnen.
2. Wählen Sie im Szenariofeld **Anlagendowntime** die Option **Konfigurieren**, um den Einrichtungsassistenten für dieses Szenario zu öffnen.
3. Wählen Sie auf der Seite **Sensoren** die Option **Neu** aus, um dem Raster einen Sensor hinzuzufügen. Legen Sie dann die folgenden Felder fest:

    - **Sensor-ID** – Geben Sie die ID des verwendeten Sensors ein. (Wenn Sie den Raspberry PI Azure IoT Online Simulator verwenden und ihn wie in [Einrichten eines simulierten Sensors für Tests](sdi-set-up-simulated-sensor.md) beschrieben eingerichtet haben, geben Sie *AssetDownTime* ein.)
    - **Sensorbeschreibung** – Geben Sie eine detaillierte Beschreibung des Sensors ein.

4. Wiederholen Sie den vorherigen Schritt für jeden weiteren Sensor, den Sie jetzt hinzufügen möchten. Sie können jederzeit zurückkehren und weitere Sensoren hinzufügen.
5. Wählen Sie **Weiter** aus.
6. Wählen Sie auf der Seite **Geschäftsdatensatzzuordnung** im Abschnitt **Sensoren** den Datensatz für einen der Sensoren aus, den Sie gerade hinzugefügt haben.
7. Öffnen Sie im Abschnitt **Geschäftsdatensatzzuordnung** und wählen Sie **Neu** aus, um dem Raster eine Zeile hinzuzufügen.
8. Legen Sie in der neuen Zeile das Feld **Geschäftsdatensatz** auf die Ressource fest, die Sie mit dem ausgewählten Sensor überwachen. (Wenn Sie die Demodaten verwenden, wählen Sie *AK-101, Luftmesser für Zeile 1*.)
9. Wählen Sie **Weiter** aus.
10. Auf der Seite **Schwellenwert für Anlagenausfall** definieren Sie, wie lange nach dem letzten Signal das System warten soll, bevor es eine Benachrichtigung über Anlagenausfall sendet. Es gibt zwei Möglichkeiten, den Schwellenwert zu definieren:

    - **Standardschwellenwert (Minuten)** – Legen Sie dieses Feld fest, um den Standardschwellenwert zu definieren. Dieser Wert gilt für alle Ressourcen, bei denen das **Benachrichtigungsschwellenwert (Minuten)**-Feld auf zwei Minuten oder weniger eingestellt ist. Der Mindestwert ist *2* (Minuten).
    - **Schwellenwert zur Bestimmung der nicht reagierenden Maschine (Minuten)** – Geben Sie für jede Ressource im Raster, für die Sie den Standardschwellenwert nicht verwenden möchten, einen Überschreibungswert in dieses Feld ein. Ressourcen, die auf einen Schwellenwert von zwei Minuten oder weniger eingestellt sind, verwenden die **Standardschwellenwert (Minuten)**-Einstellung stattdessen.
11. Wählen Sie **Weiter** aus.
12. Wählen Sie auf der Seite **Sensoren aktivieren** im Raster den Sensor aus, den Sie eingerichtet haben, und wählen Sie dann **Aktivieren**. Für jeden aktivierten Sensor im Raster erscheint ein Häkchen in der **Aktiv**-Spalte.
13. Wählen Sie **Fertig stellen** aus.

## <a name="work-with-the-asset-downtime-scenario"></a>Arbeiten mit dem Szenario der Anlagendowntime

Wenn innerhalb des in der Szenariokonfiguration definierten Schwellenwerts kein Sensorsignal von einer Anlage empfangen wird, erstellt das System einen Wartungsausfallzeit-Datensatz für diese Anlage. Manager sollten die Ausfallzeitaufzeichnungen regelmäßig überprüfen (z. B. einmal während jeder Arbeitsschicht) und für jede Ausfallzeitregistrierung geeignete Ursachencodes und Endzeiten anwenden. Befolgen Sie diese Schritte, um die Aufzeichnungen zu Wartungsausfallzeiten für eine Anlage anzuzeigen:

1. Wechseln Sie zu **Anlagenverwaltung > Anlagen > Alle Anlagen**.
2. Suchen Sie die Anlage, die Sie überprüfen möchten, und wählen Sie sie aus. (Wenn Sie mit den Demodaten arbeiten, wählen Sie *AK-101* aus.)
3. Öffnen Sie im Aktivitätsbereich die **Anlage**-Registerkarte und wählen Sie in der **Arbeitsauftrag**-Gruppe **Wartungsausfallzeit**, um die Seite für Aufzeichnungen zu Wartungsausfallzeiten für die ausgewählte Anlage zu öffnen.
