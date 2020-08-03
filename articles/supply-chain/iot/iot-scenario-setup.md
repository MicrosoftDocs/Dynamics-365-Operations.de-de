---
title: Szenarioeinrichtung für IoT-Intelligenz
description: In diesem Thema wird beschrieben, wie Sie ein Szenario in Supply Chain Management für IoT-Intelligenz konfigurieren.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597167"
---
# <a name="scenario-setup-for-iot-intelligence"></a>Szenarioeinrichtung für IoT-Intelligenz

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie ein Szenario in Supply Chain Management für IoT-Intelligenz konfigurieren. Bevor Sie die Szenarien einrichten können, müssen Sie [LCS einrichten](iot-lcs-setup.md).

In diesem Thema konfigurieren Sie das Szenario **Ausfallzeiten der Geräte** zum Generieren einer Benachrichtigung in Supply Chain Management, wenn eine Maschine ausfällt.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Szenario **Ausfallzeiten der Geräte** im Supply Chain Management konfigurieren

Das Szenario **Ausfallzeiten der Geräte** ordnet ein Teilausgangssignal einem Maschinenalarmschwellenwert zu. Die Maschine wird nur überwacht, wenn sie für das Szenario ausgewählt und in Supply Chain Management ausgeführt wird. Wenn die Zeit seit dem letzten Empfang des Teilausgangssignals der Maschine den Alarmschwellenwert übersteigt, wird die Benachrichtigung **Maschine aus** ausgelöst. Wenn die Maschine noch läuft, wenn das nächste **PartOut**-Signal empfangen wird, wird eine **Maschine aus**-Benachrichtigung ausgelöst. Wenn eine Maschine 30 Minuten lang außer Betrieb bleibt, wird eine neue **Maschine aus**-Benachrichtigung ausgelöst.

Das Szenario **Ausfallzeiten der Geräte** weist diese Abhängigkeiten auf:

+ Ein Fertigungsauftrag muss auf einer zugeordneten Maschine ausgeführt werden, damit eine Warnung ausgelöst wird.
+ Ein Signal, das das Teilausgangssignal einer zugeordneten Maschine darstellt, muss mit einem eindeutigen Eigenschaftsnamen an den IoT-Hub gesendet werden.
+ In der IoT-Hub-Nachricht muss eine Unix-Millisekunden-Zeitstempeleigenschaft vorhanden sein.

Gehen Sie folgendermaßen vor, um das Szenario zu konfigurieren:

1. Melden Sie sich in Supply Chain Management an.
2. Aktivieren Sie das IoT-Intelligenz-Funktionsflag. Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Konfigurieren Sie die Kennzahlen. Weitere Informationen finden Sie unter [So konfigurieren Sie Kennzahlen](iot-metrics-setup.md#configure-metrics).
4. Navigieren Sie zu **Produktionskontrolle**.
5. Navigieren Sie zu **Installieren \> IoT-Intelligenz \> Szenariovewaltung**.
6. Klicken Sie auf **Konfigurieren** auf der Kachel**Ausfallzeiten der Geräte**. Der Konfigurationsassistent startet mit der Seite **Definition des Gerätesensorschemas**. Ziel ist es, das Schema in Supply Chain Management so einzurichten, dass es dem JSON-Format der IoT-Nachrichten entspricht. Es können mehrere Nachrichtenschemata definiert werden. Weitere Informationen finden Sie unter [Nachrichtenschemaformate für IoT-Hub](iot-schema-format.md). In diesem Beispiel enthält die Nachrichtennutzlast einen Stapel von Nachrichten in diesem Format:

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. Fügen Sie der Tabelle eine Zeile hinzu.

    1. Setzen Sie **Schemaname** auf **ID**.
    2. Setzen Sie **Schemapfad** auf **/payload[\*]/id**.
    3. Setzen Sie **Beschreibung** auf **Nachrichten-ID**.

8. Fügen Sie der Tabelle eine Zeile hinzu.

    1. Setzen Sie **Schemaname** auf **Zeitstempel**.
    2. Setzen Sie **Schemapfad** auf **/payload[\*]/timestamp**.
    3. Setzen Sie **Beschreibung** auf **Nachrichtenzeitstempel**.

9. Fügen Sie der Tabelle eine Zeile hinzu.

    1. Setzen Sie **Schemaname** auf **Wert**.
    2. Setzen Sie **Schemapfad** auf **/payload[\*]/value**.
    3. Setzen Sie **Beschreibung** auf **Nachrichtenwert**.

    Sie müssen nicht alle Eigenschaften in der Nachricht definieren, sondern nur die, die Sie benötigen. In diesem Beispiel haben Sie keine Zeile für **Root-Zeitstempel** erstellt. Der Pfad für **Root-Zeitstempel** wäre **/Zeitstempel**.
  
10. Klicken Sie auf **Weiter**, um zur Seite **Gerätesensorschemazuordnung** zu wechseln.
11. In der Zeile für **Geräteressourcen-ID** setzen Sie **Schemaname** auf **ID**. Die gültigen Werte werden in einer Dropdowntabelle angezeigt.
12. In der Zeile für **UTC-Zeit** setzen Sie **Schemaname** auf **Zeitstempel**. Die gültigen Werte werden in einer Dropdowntabelle angezeigt.
13. In der Zeile für **Teilsignal** setzen Sie **Schemaname** auf **Wert**. Die gültigen Werte werden in einer Dropdowntabelle angezeigt.
14. Klicken Sie auf **Weiter** für die Seite **Konfiguration der Geräteressourcen-ID**.
15. In diesem Schritt ordnen Sie die IoT Hub-Nachrichtenwerte den Supply Chain Management-Ressourcen zu.

    1. Fügen Sie in der Tabelle **Signaldatenwerte** eine neue Zeile hinzu, und geben Sie **IoTInt.Machine1225.PartOut** in der Spalte **Wert** ein. Der Wert **IoTInt.Machine1225.PartOut** kommt von der JSON-Eigenschaft **ID** in der IoT-Hub-Nachricht.
    2. Klicken Sie auf **Speichern**.
    3. Klicken Sie in der Tabelle **Geschäftsdatensatzzuordnung** auf **Neu**. Der Standardwert für **Geschäftsdatensatztyp** wird automatisch aufgefüllt und muss nicht geändert werden.
    4. Wählen Sie in der Spalte **Geschäftsdatensatz** die Supple Chain Management-Maschinenressource aus, von der dieser Signalwert gesendet wird.
    5. Klicken Sie auf **Speichern**.
    6. Wiederholen Sie diese Schritte, und fügen Sie eine neue Geschäftsdatensatzzuordnung für **Machine1226** hinzu. In Supply Chain Management können Sie einem einzelnen Datensatz mehrere Signaldatenwerte zuordnen.

16. Verwenden Sie die Spalte **Ausgewählt**, um zu wählen, welche Maschinen Sie verarbeiten möchten. Sie müssen nicht alle Signalwerte definieren und nicht alle Maschinen auswählen.
17. Klicken Sie auf **Weiter**, um zur Seite **Teilsignalkonfiguration** zu wechseln.
18. Fügen Sie in der Tabelle **Signaldatenwerte** eine Zeile hinzu, und setzen Sie **Wert** auf **Wahr**. Der Wert **Wahr** kommt von der JSON-Eigenschaft **Wert** in der IoT-Hub-Nachricht. Sie können so viele Werte hinzufügen, wie Sie für Ihr Szenario benötigen.
19. Klicken Sie auf **Speichern**.
20. Klicken Sie auf **Weiter**, um zur Seite **Schwellenwert für Geräteausfallzeiten** zu wechseln. Die aufgelisteten Maschinen sind die Maschinen, die zuvor Signalwerten zugeordnet wurden. In diesem Schritt definieren Sie einen Schwellenwert, um festzustellen, ob eine Maschine ausgefallen ist. Wenn Sie beispielsweise den Schwellenwert auf 10 festlegen, generiert Supply Chain Management eine Benachrichtigung, wenn 10 Minuten lang keine Teilausgangsnachricht von einer Maschine vorliegt.
21. Klicken Sie auf **Weiter**, um zur Seite **Szenario aktivieren** zu wechseln. Schalten Sie den Schieberegler um, um das Szenario zu aktivieren.
22. Klicken Sie auf **Fertig stellen**.

Die Szenarioeinrichtung ist abgeschlossen. IoT-Intelligenz beginnt automatisch mit der Verarbeitung der IoT-Hub-Nachrichten.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Szenario **Produktqualität** im Supply Chain Management konfigurieren

Das Szenario **Produktqualität** generiert eine Benachrichtigung, wenn ein Attribut eines Elements außerhalb eines angegebenen Bereichs liegt. Beispielsweise könnte ein Sensor das Gewicht jedes Elements an den IoT-Hub senden. In Supply Chain Management wird eine Benachrichtigung generiert, wenn der Artikel zu schwer oder zu leicht ist.

Das Szenario hat folgende Abhängigkeiten:

+ Ein Fertigungsauftrag muss auf einer zugeordneten Maschine ausgeführt werden und ein Produkt mit einem zugeordneten Chargenattribut produzieren, damit eine Warnung ausgelöst wird.
+ Ein Signal, das das Chargenattribut darstellt, muss mit einem eindeutigen Eigenschaftsnamen an den IoT-Hub gesendet werden.
+ In der IoT-Hub-Nachricht muss eine Unix-Millisekunden-Zeitstempeleigenschaft vorhanden sein.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Szenario **Produktionsverzögerungen** im Supply Chain Management konfigurieren

Das Szenario **Produktionsverzögerungen** generiert eine Benachrichtigung, wenn der Produktionsdurchsatz einen Schwellenwert unterschreitet. In diesem Szenario wird ein **PartOut**-Signal für jeden produzierten Artikel an IoT-Hub gesendet. In Supply Chain Management wird die Auftragsverzögerung basierend darauf berechnet, wie lange der Fertigungsauftrag ausgeführt werden soll, wie viele Artikel produziert werden sollen, wie lange der Auftrag ausgeführt wurde und wie viele **PartOut**-Signale empfangen werden. Eine Verzögerungsbenachrichtigung würde generiert, wenn die Zahl der **PartOut**-Signale für den Einzelvorgang den Schwellenwert des erwarteten Wertes unterschreitet.

Das Szenario hat folgende Abhängigkeiten:

+ Ein Fertigungsauftrag muss auf einer zugeordneten Maschine ausgeführt werden, damit eine Warnung ausgelöst wird.
+ Ein Signal, das das Teilausgangssignal einer zugeordneten Maschine darstellt, muss mit einem eindeutigen Eigenschaftsnamen an den IoT-Hub gesendet werden.
+ In der IoT-Hub-Nachricht muss eine Unix-Millisekunden-Zeitstempeleigenschaft vorhanden sein.

## <a name="how-to-disable-a-scenario"></a>So deaktivieren Sie ein Szenario

Um ein Szenario zu deaktivieren, führen Sie folgende Schritte aus:

1. Navigieren Sie in Supply Chain Management zu **Produktionskontrolle \> Einrichtung \> IoT-Intelligenz \>Szenarioverwaltung**.
2. Klicken Sie auf **Konfigurieren** im Szenario.
3. Klicken Sie auf **Weiter**, um zur letzten Registerkarte des Assistenten zu gelangen.
4. Schalten Sie den Schieberegler um, um das Szenario zu deaktivieren.
