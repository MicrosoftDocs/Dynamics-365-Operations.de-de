---
title: Richten Sie einen simulierten Sensor zum Testen ein
description: In diesem Artikel wird beschrieben, wie Sie einen Simulator einrichten, mit dem Sie Sensor Data Intelligence testen können, ohne physische Sensoren zu installieren.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: f12d6e1d417a260477b1eb4e027b850d1862f51f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689803"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>Richten Sie einen simulierten Sensor zum Testen ein

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Wenn Sie Sensor Data Intelligence testen möchten, ohne physische Sensoren zu installieren, können Sie den *Raspberry PI Azure IoT Online Simulator*-Service verwenden, um Sensorsignale zu emulieren und sie an Ihre Internet of Things (IoT)-Lösung in Microsoft Azure zu senden. Weitere Informationen zum Simulator finden Sie unter [Den Raspberry Pi-Onlinesimulator mit Azure IoT Hub (Node.js) verbinden](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started).

## <a name="video-instructions"></a>Videoanleitungen

Das folgende Video zeigt, wie Sie einen simulierten Sensor zum Testen einrichten. Die verbleibenden Abschnitte in diesem Artikel bieten dieselben Anweisungen in einem textbasierten Format.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE588g6]

## <a name="create-a-device-in-azure-iot-hub"></a>Ein Gerät in Azure IoT Hub erstellen

Sie müssen zuerst ein Gerät einrichten, um die Sensorsignale beim Azure IoT Hub zu authentifizieren.

1. Wechseln Sie in Azure zur Liste der Ressourcen für die Ressourcengruppe, die Sie für die Verwendung mit Sensor Data Intelligence erstellt haben. (Weitere Informationen finden Sie unter [Eine IoT-Lösung in Azure bereitstellen](sdi-deploy-iot-solution-on-azure.md) .)
1. Suchen Sie in der Ressourcenliste den Datensatz, in dem das **Typ**-Feld auf *IoT Hub* eingestellt ist. Wählen Sie in der Spalte **Name** den Namen, um die Detailseite für die Ressource zu öffnen.
1. Wählen Sie im linken Navigationsbereich **Geräte**.
1. Wählen Sie auf der Seite **Geräte** die Option **Gerät hinzufügen**.
1. Auf der Seite **Ein Gerät erstellen** setzen Sie die folgenden Felder fest:

    - **Geräte-ID** – Geben Sie einen Namen für das neue Gerät ein (z. B. *Mein-IoT-Gerät*).
    - **Authentifizierungsart** – Wählen Sie *Symmetrische Schlüssel*.
    - **Schlüssel automatisch generieren** – Aktivieren Sie dieses Kontrollkästchen.
    - **Dieses Gerät mit einem IoT-Hub verbinden** – Wählen Sie *Aktivieren*.

1. Wählen Sie **Speichern** aus, um zur Seite **Geräte** zurückzukehren.
1. Suchen Sie das neue Gerät in der Liste. Wählen Sie in der Spalte **Geräte-ID** den Namen, um die Detailseite für das Gerät zu öffnen. Wenn Sie das neue Gerät nicht in der Liste sehen, aktualisieren Sie die Seite.
1. Kopieren Sie den Wert **Primäre Verbindungszeichenfolge** (z. B. durch Auswahl der Schaltfläche **In die Zwischenablage kopieren**). Sie benötigen diesen Wert später, wenn Sie den Raspberry Pi IoT-Simulator einrichten, um Sensorsignale zu emulieren. Erwägen Sie daher vorerst, es in eine Textdatei einzufügen.

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>Fügen Sie die Azure-Verbindungszeichenfolge zum Raspberry Pi IoT-Simulator hinzu

Führen Sie diese Schritte aus, um die Verbindungszeichenfolge vom Gerät in Azure IoT Hub zum Skript im Raspberry-Dienst hinzuzufügen.

1. Öffnen Sie den [Raspberry Pi IoT-Simulator](https://azure-samples.github.io/raspberry-pi-web-simulator/).
1. Suchen Sie im Code-Editor-Bereich die Zeile, die den folgenden Befehl enthält.

    `const connectionString = '[Your IoT hub device connection string]';`

1. Ersetzen Sie den Hilfetext einschließlich der Klammern durch den **Primäre Verbindungszeichenfolge**-Wert, den Sie im vorherigen Abschnitt kopiert haben. Das Ergebnis sollte dem folgenden Beispiel ähneln.

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>Fügen Sie der Nutzlast im Raspberry Pi IoT-Simulator Sensor-IDs und Werte hinzu

Sie müssen nun den Raspberry Pi IoT-Simulator mit simulierten Sensoren und den Werten, die sie als Nutzdaten senden, einrichten.

- Suchen Sie im Code-Editor des Raspberry Pi IoT-Simulators die `getMessage`-Funktion, und bearbeiten Sie sie so, dass sie mit dem folgenden Code übereinstimmt. (Die Sensoren werden in den `cb()`-Positionen eingerichtet.)

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > Die Sensor-IDs, die im Code-Editor für den Raspberry Pi IoT-Simulator definiert werden, müssen mit den Sensor-IDs identisch sein, die Sie später für die Szenarien im Supply Chain Management angeben. Der vorangehende Beispielcode verwendet für Menschen lesbare Sensor-IDs. In einem tatsächlichen Szenario sind die Sensor-IDs jedoch global eindeutige Kennungs-(GUID-)Werte, die vom Sensorhersteller bereitgestellt werden. Die von Menschen lesbaren Sensor-IDs, die in diesem Beispielcode verwendet werden, werden auch in den Beispielen im [Produktqualitätsszenario](sdi-scenario-product-quality.md), [Anlagenwartungsszenario](sdi-scenario-asset-maintenance.md), [Szenario Produktionsverzögerungen](sdi-scenario-production-delays.md) und [Maschinenstatus-Szenario](sdi-scenario-equipment-downtime.md)) verwendet. Verwenden Sie daher diesen Code, wenn Sie diese Szenarien durcharbeiten.

## <a name="edit-the-interval-for-sending-sensor-signals"></a>Bearbeiten Sie das Intervall für das Senden von Sensorsignalen

Sie müssen nun das Intervall einstellen, in dem der Raspberry Pi IoT-Simulator die emulierten Sensorsignale senden soll.

1. Suchen Sie im Code-Editor des Raspberry Pi IoT-Simulators den folgenden Funktionsaufruf.

    `setInterval(sendMessage, 2000);`

2. Standardmäßig sendet der Raspberry Pi IoT-Simulator alle 2.000 Millisekunden (zwei Sekunden) ein Sensorsignal. Sie den Wert in diesem Feld nach Bedarf ändern.

## <a name="run-the-raspberry-pi-iot-simulator"></a>Führen Sie den Raspberry Pi IoT-Simulator aus.

- Wählen Sie **Ausführen** aus, um den Simulator zu starten und mit dem Senden simulierter Sensordaten zu beginnen.
