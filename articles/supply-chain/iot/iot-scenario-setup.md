---
title: Szenarioeinrichtung für IoT-Intelligenz
description: In diesem Thema wird erläutert, wie Sie Szenarien für IoT-Intelligenz in Microsoft Dynamics 365 Supply Chain Management konfigurieren.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a45ed57f1fb5e4d508c30b2f3a83dafacfb7dd870701a8f519bbc1e807ed982
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736792"
---
# <a name="scenario-setup-for-iot-intelligence"></a>Szenarioeinrichtung für IoT-Intelligenz

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Szenarien für IoT-Intelligenz in Microsoft Dynamics 365 Supply Chain Management konfigurieren. Bevor Sie die Szenarien einrichten können, müssen Sie [Microsoft Dynamics Lifecycle Services (LCS) einrichten](iot-lcs-setup.md).

In diesem Thema konfigurieren Sie das Szenario **Ausfallzeiten der Geräte** , sodass eine Benachrichtigung in Supply Chain Management generiert wird, wenn eine Maschine ausfällt. Das Thema zeigt auch, wie Sie das **Produktqualität**-Szenario konfigurieren, in dem eine Benachrichtigung generiert wird, wenn das Attribut eines Elements außerhalb eines angegebenen Bereichs liegt, und wie das **Produktionsverzögerungen**-Szenario konfiguriert wird, sodass eine Benachrichtigung generiert wird, wenn der Produktionsdurchsatz einen Schwellenwert unterschreitet.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Szenario Ausfallzeiten der Geräte im Supply Chain Management konfigurieren

Das Szenario **Ausfallzeiten der Geräte** ordnet ein **PartOut**-Signal einem Maschinenalarmschwellenwert zu. Die Maschine wird nur überwacht, wenn sie für das Szenario ausgewählt und in Supply Chain Management auf **Ausgeführt** festgelegt wird. Wenn die Zeit seit dem letzten Empfang eines **PartOut**-Signals der Maschine den Alarmschwellenwert übersteigt, wird eine Benachrichtigung **Maschine ausgefallen** ausgelöst. Wenn die Maschine noch läuft, wird eine **Maschine ein** ausgelöst, wenn das nächste **PartOut**-Signal empfangen wird. Wenn eine Maschine 30 Minuten lang außer Betrieb bleibt, wird eine neue **Maschine aus**-Benachrichtigung ausgelöst.

Das Szenario **Ausfallzeiten der Geräte** weist die Folgenden Abhängigkeiten auf:

+ Eine Warnung kann nur ausgelöst werden, wenn ein Produktionsauftrag auf einer zugeordneten Maschine ausgeführt wird.
+ Ein Signal, das das **PartOut**-Signal einer zugeordneten Maschine darstellt, muss mit einem eindeutigen IoT-Hub und einem eindeutigen Eigenschaftsnamen enthalten sein.
+ Eine UNIX-**Zeitstempel**-Eigenschaft, bei der der Wert in Millisekunden (ms) angegeben wird, muss in der Azure IoT Hub-Nachricht vorhanden sein.

Gehen Sie folgendermaßen vor, um das Szenario zu konfigurieren.

1. Melden Sie sich im Supply Chain Management an.
2. Aktivieren Sie das IoT-Intelligenz-Funktionsflag. Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Konfigurieren Sie die Kennzahlen. Weitere Informationen finden Sie unter [So konfigurieren Sie Kennzahlen](iot-metrics-setup.md#configure-metrics).
4. Wechseln Sie zu **Produktionssteuerung \> Einrichtung \> IoT-Intelligenz \> Szenariovewaltung**.
6. Wählen Sie auf der **Ausfallzeiten der Geräte**-Kachel **Konfigurieren** aus, um den Konfigurationsassistenten zu öffnen.

   Die erste Seite im Assistenten ist die Seite **Definition des Gerätesensorschemas**. Das Ziel auf dieser Seite ist es, das Schema in Supply Chain Management so einzurichten, dass es mit dem JSON-Format (JavaScript Object Notation) der IoT Hub-Nachrichten übereinstimmt. Es können mehrere Nachrichtenschemata definiert werden. Weitere Informationen finden Sie unter [Schemaformate für IoT-Hub-Nachrichten](iot-schema-format.md). In diesem Beispiel enthält die Nachrichtennutzlast einen Stapel von Nachrichten, der das folgende Format aufweist.

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

7. Fügen Sie einer Tabelle eine Zeile hinzu und legen Sie die folgenden Werte fest:

    1. Setzen Sie das Feld **Schemaname** auf **ID**.
    2. Setzen Sie das Feld **Schemapfad** auf **/payload\[\*\]/id**.
    3. Setzen Sie das Feld **Beschreibung** auf **Nachrichten-ID**.

8. Fügen Sie einer Tabelle eine andere Zeile hinzu und legen Sie die folgenden Werte fest:

    1. Setzen Sie das Feld **Schemaname** auf **Zeitstempel**.
    2. Setzen Sie das Feld **Schemapfad** auf **/payload\[\*\]/timestamp**.
    3. Setzen Sie das Feld **Beschreibung** auf **Nachrichtenzeitstempel**.

9. Fügen Sie einer Tabelle eine andere Zeile hinzu und legen Sie die folgenden Werte fest:

    1. Setzen Sie das Feld **Schemaname** auf **Wert**.
    2. Setzen Sie das Feld **Schemapfad** auf **/payload\[\*\]/value**.
    3. Setzen Sie das Feld **Beschreibung** auf **Nachrichtenwert**.

    > [!NOTE]
    > Sie müssen nicht alle Eigenschaften in der Nachricht definieren. Definieren Sie nur die Eigenschaften, die Sie benötigen. In den vorhergehenden Schritten haben Sie keine Zeile für **Root-Zeitstempel** erstellt. Der Pfad von **Root-Zeitstempel** wäre **/timestamp**.

10. Wählen Sie **Weiter**, um zur Seite **Gerätesensorschemazuordnung** zu wechseln.
11. In der Zeile für **Geräteressourcen-ID** wählen Sie im Feld **Schemaname** **ID** aus.
12. In der Zeile für **UTC-Zeit** wählen Sie im Feld **Schemaname** **Zeitstempel** aus.
13. In der Zeile für **Teilsignal** wählen Sie im Feld **Schemaname** **Wert** aus.
14. Wählen Sie **Weiter**, um zur Seite **Konfiguration der Geräteressourcen-ID** zu wechseln.
15. Führen Sie diese Schritte aus, um die Werte in der IoT Hub-Nachricht den Supply Chain Management-Ressourcen zuzuordnen:

    1. Fügen Sie in der Tabelle **Signaldatenwerte** eine neue Zeile hinzu. Geben Sie im **Wert**-Feld **IoTInt.Machine1225.PartOut** ein. Dieser Wert kommt von der JSON-**id**-Eigenschaft in der IoT-Hub-Nachricht.
    2. Wählen Sie **Speichern** aus.
    3. Wählen Sie in der Tabelle **Geschäftsdatensatzzuordnung** **Neu** aus. Ein Standardwert für das Feld **Geschäftsdatensatztyp** wird automatisch aufgefüllt und muss nicht geändert werden.
    4. Wählen Sie im Feld **Geschäftsdatensatz** die Supply Chain Management-Maschinenressource aus, von der dieser Signalwert gesendet wird.
    5. Wählen Sie **Speichern** aus.
    6. Wiederholen Sie diese Schritte, um eine neue Geschäftsdatensatzzuordnung für **Machine1226** hinzuzufügen. In Supply Chain Management können Sie einem einzelnen Datensatz mehrere Signaldatenwerte zuordnen.

16. Verwenden Sie die Spalte **Ausgewählt**, um die Maschinen auszuwählen, die Sie verarbeiten möchten. Sie müssen nicht alle Signalwerte definieren und nicht alle Maschinen auswählen.
17. Wählen Sie **Weiter**, um zur Seite **Teilsignalkonfiguration** zu wechseln.
18. Fügen Sie in der Tabelle **Signaldatenwerte** eine Zeile hinzu, und setzen Sie das Feld **Wert** auf **Wahr**. Dieser Wert kommt von der JSON-**value**-Eigenschaft in der IoT-Hub-Nachricht. Sie können so viele Werte hinzufügen, wie Sie für Ihr Szenario benötigen.
19. Wählen Sie **Speichern** aus.
20. Wählen Sie **Weiter**, um zur Seite **Schwellenwert für Geräteausfallzeiten** zu wechseln. Die aufgelisteten Maschinen sind die Maschinen, die zuvor Signalwerten zugeordnet wurden. Auf dieser Seite definieren Sie einen Schwellenwert, um festzustellen, ob eine Maschine ausgefallen ist. Wenn Sie beispielsweise den Schwellenwert auf **10** festlegen, generiert Supply Chain Management eine Benachrichtigung, wenn 10 Minuten lang kein **PartOut**-Signal von einer Maschine empfangen wird.
21. Wählen Sie **Weiter**, um zur Seite **Szenario aktivieren** zu wechseln. Legen Sie die Option fest, um das Szenario zu aktivieren.
22. Wählen Sie **Fertig stellen** aus.

Die Szenarioeinrichtung ist jetzt abgeschlossen. IoT-Intelligenz beginnt automatisch mit der Verarbeitung der IoT-Hub-Nachrichten.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Szenario Produktqualität im Supply Chain Management konfigurieren

Das Szenario **Produktqualität** generiert eine Benachrichtigung, wenn ein Attribut eines Elements außerhalb eines angegebenen Bereichs liegt. Beispielsweise sendet ein Sensor das Gewicht jedes Elements an den IoT-Hub. Wenn ein Artikel zu schwer oder zu leicht ist, wird in Supply Chain Management eine Benachrichtigung generiert.

Das Szenario **Produktmenge** weist die Folgenden Abhängigkeiten auf:

+ Eine Warnung kann nur ausgelöst werden, wenn ein Produktionsauftrag auf einer zugeordneten Maschine ausgeführt wird und ein Produkt mit einem zugeordneten Chargenattribut produziert wird.
+ Ein Signal, das das Chargenattribut darstellt, muss an den IoT-Hub gesendet werden und ein eindeutiger Eigenschaftsname muss enthalten sein.
+ Eine UNIX-**Zeitstempel**-Eigenschaft, bei der der Wert in ms angegeben wird, muss in der IoT Hub-Nachricht vorhanden sein.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Szenario Produktionsverzögerungen im Supply Chain Management konfigurieren

Das Szenario **Produktionsverzögerungen** generiert eine Benachrichtigung, wenn der Produktionsdurchsatz einen Schwellenwert unterschreitet. In diesem Szenario wird ein **PartOut**-Signal für jeden produzierten Artikel an IoT-Hub gesendet. In Supply Chain Management wird die Auftragsverzögerung basierend auf der geplanten Ausführungszeit des Produktionsauftrags, der Anzahl der zu produzierenden Artikel, der Ausführungszeit des Auftrags und der Anzahl der empfangenen **PartOut**-Signale berechnet. Eine Verzögerungsbenachrichtigung wird generiert, wenn die Zahl der **PartOut**-Signale für den Einzelvorgang den Schwellenwert unterschreitet.

Das Szenario **Produktionsverzögerungen** weist die Folgenden Abhängigkeiten auf:

+ Eine Warnung kann nur ausgelöst werden, wenn ein Produktionsauftrag auf einer zugeordneten Maschine ausgeführt wird.
+ Ein Signal, das das **PartOut**-Signal einer zugeordneten Maschine darstellt, muss mit einem eindeutigen Azure IoT-Hub und einem eindeutigen Eigenschaftsnamen enthalten sein.
+ Eine UNIX-**Zeitstempel**-Eigenschaft, bei der der Wert in ms angegeben wird, muss in der IoT Hub-Nachricht vorhanden sein.

## <a name="disable-a-scenario"></a>Deaktivieren eines Szenarios

Um ein Szenario zu deaktivieren, führen Sie folgende Schritte aus.

1. Wechseln Sie in Supply Chain Management zu **Produktionskontrolle \> Einrichtung \> IoT-Intelligenz \> Szenarioverwaltung**.
2. Wählen Sie auf der Kachel für das Szenario **Konfigurieren** aus.
3. Wählen Sie **Weiter**, um zur letzten Assistentenseite zu wechseln.
4. Legen Sie die Option fest, um das Szenario zu deaktivieren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]