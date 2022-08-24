---
title: Schemaformate für IoT-Hub-Nachrichten
description: In diesem Artikel wird erläutert, wie Sie ein Nachrichtenschema entwerfen sollten, das Sie in IoT-Intelligenz verwenden können.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6d133d520ce0a1dccb2575e352f63e6ceb2bd3f
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228631"
---
# <a name="schema-formats-for-iot-hub-messages"></a>Schemaformate für IoT-Hub-Nachrichten

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

In diesem Artikel wird erläutert, wie Sie ein Nachrichtenschema entwerfen sollten, das Sie in IoT-Intelligenz verwenden können.

## <a name="message-requirements"></a>Nachrichtenanforderungen

Für die Überwachung von Nachrichten in IoT-Intelligenz gelten folgende Regeln:

+ Nachrichtenschemas müssen im Format JavaScript Object Notation (JSON) vorliegen.
+ Eine UNIX-**Zeitstempel**-Eigenschaft, bei der der Wert in Millisekunden (ms) angegeben wird, muss in der Microsoft Azure IoT Hub-Nachricht vorhanden sein.
+ Eine Nachricht wird nur verfolgt, wenn sie alle Eigenschaften enthält, die in der Szenarioeinrichtung definiert sind. Wenn Sie beispielsweise **ID**, **Zeitstempel** und **Wert**-Eigenschaften definieren, wird die folgende Meldung überwacht.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    Diese Nachricht wird nicht überwacht, da die **Wert**-Eigenschaft fehlt.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ IoT-Intelligenz ignoriert Eigenschaften in der Nachricht, die nicht in der Szenariokonfiguration definiert sind. Wenn Sie beispielsweise **ID**, **Zeitstempel** und **Wert**-Eigenschaften definieren, überwacht IoT-Intelligenz die folgende Nachrichten.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ IoT-Intelligenz ignoriert stillschweigend Nachrichten, die nicht den Szenariokonfigurationskriterien entsprechen.
+ Sie können mehrere Arten von Nachrichtenschemas definieren und verwenden.
+ Nicht jeder Nachrichtenschematyp muss definiert werden. Es müssen nur Schemas definiert werden, die für die IoT-Intelligenz-Szenarien verwendet werden.

## <a name="id-value-pair-schema"></a>ID-Wert-Paar-Schema

Ein ID-Wert-Paar ist ein gängiges Muster für IoT-Intelligenz-Nachrichtenschemas. Durch die Verwendung eines ID-Wert-Paares stellen Sie sicher, dass Ihr Nachrichtenschema in allen Szenarien gleich ist. Hier ist zum Beispiel eine Nachricht für das Szenario **Ausfallzeiten der Geräte** oder **Produktionsverzögerungen**.

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

Hier ist eine Nachricht für das Szenario **Produktqualität**.

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

Beide vorhergehenden Nachrichten enthalten **ID**- und **Wert**-Eigenschaften. Die **ID**-Werte können während der Szenarioeinrichtung in der **Signaldatenwerte**-Tabelle abgebildet werden. Für das Szenario **Ausfallzeiten der Geräte** ordnen Sie den Wert **IoTINt.Machine1225.PartOut** zu. Für das Szenario **Produktqualität** ordnen Sie den Wert **IoTInt.Machine1225.Temperature** zu.

Weitere Informationen finden Sie in der [Azure IoT Hub-Dokumentation](/azure/iot-hub/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]