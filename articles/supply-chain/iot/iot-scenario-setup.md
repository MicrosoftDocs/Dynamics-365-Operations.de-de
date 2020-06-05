---
title: Szenarioeinrichtung für IoT-Intelligenz
description: In diesem Thema wird beschrieben, wie Sie ein Szenario in Supply Chain Management für IoT-Intelligenz konfigurieren.
author: robinarh
manager: AnnBe
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
ms.openlocfilehash: b87a9b73f49e73fe13b98fb11da939c9b30e0f6e
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386518"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="36a9f-103">Szenarioeinrichtung für IoT-Intelligenz</span><span class="sxs-lookup"><span data-stu-id="36a9f-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="36a9f-104">In diesem Thema wird beschrieben, wie Sie ein Szenario in Supply Chain Management für IoT-Intelligenz konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="36a9f-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="36a9f-105">Bevor Sie die Szenarien einrichten können, müssen Sie [LCS einrichten](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="36a9f-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="36a9f-106">In diesem Thema konfigurieren Sie das Szenario **Ausfallzeiten der Geräte** zum Generieren einer Benachrichtigung in Supply Chain Management, wenn eine Maschine ausfällt.</span><span class="sxs-lookup"><span data-stu-id="36a9f-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="36a9f-107">Szenario **Ausfallzeiten der Geräte** im Supply Chain Management konfigurieren</span><span class="sxs-lookup"><span data-stu-id="36a9f-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="36a9f-108">Das Szenario **Ausfallzeiten der Geräte** ordnet ein Teilausgangssignal einem Maschinenalarmschwellenwert zu.</span><span class="sxs-lookup"><span data-stu-id="36a9f-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="36a9f-109">Die Maschine wird nur überwacht, wenn sie für das Szenario ausgewählt und in Supply Chain Management ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36a9f-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="36a9f-110">Wenn die Zeit seit dem letzten Empfang des Teilausgangssignals der Maschine den Alarmschwellenwert übersteigt, wird die Benachrichtigung **Maschine aus** ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="36a9f-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="36a9f-111">Wenn die Maschine noch läuft, wenn das nächste **PartOut**-Signal empfangen wird, wird eine **Maschine aus**-Benachrichtigung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="36a9f-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="36a9f-112">Wenn eine Maschine 30 Minuten lang außer Betrieb bleibt, wird eine neue **Maschine aus**-Benachrichtigung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="36a9f-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="36a9f-113">Das Szenario **Ausfallzeiten der Geräte** weist diese Abhängigkeiten auf:</span><span class="sxs-lookup"><span data-stu-id="36a9f-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="36a9f-114">Ein Fertigungsauftrag muss auf einer zugeordneten Maschine ausgeführt werden, damit eine Warnung ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="36a9f-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="36a9f-115">Ein Signal, das das Teilausgangssignal einer zugeordneten Maschine darstellt, muss mit einem eindeutigen Eigenschaftsnamen an den IoT-Hub gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="36a9f-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="36a9f-116">In der IoT-Hub-Nachricht muss eine Unix-Millisekunden-Zeitstempeleigenschaft vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="36a9f-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="36a9f-117">Gehen Sie folgendermaßen vor, um das Szenario zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="36a9f-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="36a9f-118">Melden Sie sich in Supply Chain Management an.</span><span class="sxs-lookup"><span data-stu-id="36a9f-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="36a9f-119">Aktivieren Sie das IoT-Intelligenz-Funktionsflag.</span><span class="sxs-lookup"><span data-stu-id="36a9f-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="36a9f-120">Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="36a9f-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="36a9f-121">Konfigurieren Sie die Kennzahlen.</span><span class="sxs-lookup"><span data-stu-id="36a9f-121">Configure the metrics.</span></span> <span data-ttu-id="36a9f-122">Weitere Informationen finden Sie unter [So konfigurieren Sie Kennzahlen](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="36a9f-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="36a9f-123">Navigieren Sie zu **Produktionskontrolle**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="36a9f-124">Navigieren Sie zu **Installieren \> IoT-Intelligenz \> Szenariovewaltung**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="36a9f-125">Klicken Sie auf **Konfigurieren** auf der Kachel**Ausfallzeiten der Geräte**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="36a9f-126">Der Konfigurationsassistent startet mit der Seite **Definition des Gerätesensorschemas**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="36a9f-127">Ziel ist es, das Schema in Supply Chain Management so einzurichten, dass es dem JSON-Format der IoT-Nachrichten entspricht.</span><span class="sxs-lookup"><span data-stu-id="36a9f-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="36a9f-128">Es können mehrere Nachrichtenschemata definiert werden.</span><span class="sxs-lookup"><span data-stu-id="36a9f-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="36a9f-129">Weitere Informationen finden Sie unter [Nachrichtenschemaformate für IoT-Hub](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="36a9f-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="36a9f-130">In diesem Beispiel enthält die Nachrichtennutzlast einen Stapel von Nachrichten in diesem Format:</span><span class="sxs-lookup"><span data-stu-id="36a9f-130">In this example, the message payload contains a batch of messages with this format:</span></span>

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

7. <span data-ttu-id="36a9f-131">Fügen Sie der Tabelle eine Zeile hinzu.</span><span class="sxs-lookup"><span data-stu-id="36a9f-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="36a9f-132">Setzen Sie **Schemaname** auf **ID**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="36a9f-133">Setzen Sie **Schemapfad** auf **/payload[\*]/id**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="36a9f-134">Setzen Sie **Beschreibung** auf **Nachrichten-ID**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="36a9f-135">Fügen Sie der Tabelle eine Zeile hinzu.</span><span class="sxs-lookup"><span data-stu-id="36a9f-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="36a9f-136">Setzen Sie **Schemaname** auf **Zeitstempel**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="36a9f-137">Setzen Sie **Schemapfad** auf **/payload[\*]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="36a9f-138">Setzen Sie **Beschreibung** auf **Nachrichtenzeitstempel**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="36a9f-139">Fügen Sie der Tabelle eine Zeile hinzu.</span><span class="sxs-lookup"><span data-stu-id="36a9f-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="36a9f-140">Setzen Sie **Schemaname** auf **Wert**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="36a9f-141">Setzen Sie **Schemapfad** auf **/payload[\*]/value**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="36a9f-142">Setzen Sie **Beschreibung** auf **Nachrichtenwert**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="36a9f-143">Sie müssen nicht alle Eigenschaften in der Nachricht definieren, sondern nur die, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="36a9f-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="36a9f-144">In diesem Beispiel haben Sie keine Zeile für **Root-Zeitstempel** erstellt.</span><span class="sxs-lookup"><span data-stu-id="36a9f-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="36a9f-145">Der Pfad für **Root-Zeitstempel** wäre **/Zeitstempel**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="36a9f-146">Klicken Sie auf **Weiter**, um zur Seite **Gerätesensorschemazuordnung** zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="36a9f-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="36a9f-147">In der Zeile für **Geräteressourcen-ID** setzen Sie **Schemaname** auf **ID**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="36a9f-148">Die gültigen Werte werden in einer Dropdowntabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="36a9f-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="36a9f-149">In der Zeile für **UTC-Zeit** setzen Sie **Schemaname** auf **Zeitstempel**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="36a9f-150">Die gültigen Werte werden in einer Dropdowntabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="36a9f-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="36a9f-151">In der Zeile für **Teilsignal** setzen Sie **Schemaname** auf **Wert**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="36a9f-152">Die gültigen Werte werden in einer Dropdowntabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="36a9f-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="36a9f-153">Klicken Sie auf **Weiter** für die Seite **Konfiguration der Geräteressourcen-ID**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="36a9f-154">In diesem Schritt ordnen Sie die IoT Hub-Nachrichtenwerte den Supply Chain Management-Ressourcen zu.</span><span class="sxs-lookup"><span data-stu-id="36a9f-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="36a9f-155">Fügen Sie in der Tabelle **Signaldatenwerte** eine neue Zeile hinzu, und geben Sie **IoTInt.Machine1225.PartOut** in der Spalte **Wert** ein.</span><span class="sxs-lookup"><span data-stu-id="36a9f-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="36a9f-156">Der Wert **IoTInt.Machine1225.PartOut** kommt von der JSON-Eigenschaft **ID** in der IoT-Hub-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="36a9f-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="36a9f-157">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-157">Click **Save**.</span></span>
    3. <span data-ttu-id="36a9f-158">Klicken Sie in der Tabelle **Geschäftsdatensatzzuordnung** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="36a9f-159">Der Standardwert für **Geschäftsdatensatztyp** wird automatisch aufgefüllt und muss nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="36a9f-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="36a9f-160">Wählen Sie in der Spalte **Geschäftsdatensatz** die Supple Chain Management-Maschinenressource aus, von der dieser Signalwert gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="36a9f-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="36a9f-161">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-161">Click **Save**.</span></span>
    6. <span data-ttu-id="36a9f-162">Wiederholen Sie diese Schritte, und fügen Sie eine neue Geschäftsdatensatzzuordnung für **Machine1226** hinzu.</span><span class="sxs-lookup"><span data-stu-id="36a9f-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="36a9f-163">In Supply Chain Management können Sie einem einzelnen Datensatz mehrere Signaldatenwerte zuordnen.</span><span class="sxs-lookup"><span data-stu-id="36a9f-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="36a9f-164">Verwenden Sie die Spalte **Ausgewählt**, um zu wählen, welche Maschinen Sie verarbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="36a9f-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="36a9f-165">Sie müssen nicht alle Signalwerte definieren und nicht alle Maschinen auswählen.</span><span class="sxs-lookup"><span data-stu-id="36a9f-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="36a9f-166">Klicken Sie auf **Weiter**, um zur Seite **Teilsignalkonfiguration** zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="36a9f-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="36a9f-167">Fügen Sie in der Tabelle **Signaldatenwerte** eine Zeile hinzu, und setzen Sie **Wert** auf **Wahr**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="36a9f-168">Der Wert **Wahr** kommt von der JSON-Eigenschaft **Wert** in der IoT-Hub-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="36a9f-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="36a9f-169">Sie können so viele Werte hinzufügen, wie Sie für Ihr Szenario benötigen.</span><span class="sxs-lookup"><span data-stu-id="36a9f-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="36a9f-170">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-170">Click **Save**.</span></span>
20. <span data-ttu-id="36a9f-171">Klicken Sie auf **Weiter**, um zur Seite **Schwellenwert für Geräteausfallzeiten** zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="36a9f-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="36a9f-172">Die aufgelisteten Maschinen sind die Maschinen, die zuvor Signalwerten zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="36a9f-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="36a9f-173">In diesem Schritt definieren Sie einen Schwellenwert, um festzustellen, ob eine Maschine ausgefallen ist.</span><span class="sxs-lookup"><span data-stu-id="36a9f-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="36a9f-174">Wenn Sie beispielsweise den Schwellenwert auf 10 festlegen, generiert Supply Chain Management eine Benachrichtigung, wenn 10 Minuten lang keine Teilausgangsnachricht von einer Maschine vorliegt.</span><span class="sxs-lookup"><span data-stu-id="36a9f-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="36a9f-175">Klicken Sie auf **Weiter**, um zur Seite **Szenario aktivieren** zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="36a9f-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="36a9f-176">Schalten Sie den Schieberegler um, um das Szenario zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="36a9f-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="36a9f-177">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-177">Click **Finish**.</span></span>

<span data-ttu-id="36a9f-178">Die Szenarioeinrichtung ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="36a9f-178">The scenario setup is complete.</span></span> <span data-ttu-id="36a9f-179">IoT-Intelligenz beginnt automatisch mit der Verarbeitung der IoT-Hub-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="36a9f-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="36a9f-180">Szenario **Produktqualität** im Supply Chain Management konfigurieren</span><span class="sxs-lookup"><span data-stu-id="36a9f-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="36a9f-181">Das Szenario **Produktqualität** generiert eine Benachrichtigung, wenn ein Attribut eines Elements außerhalb eines angegebenen Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="36a9f-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="36a9f-182">Beispielsweise könnte ein Sensor das Gewicht jedes Elements an den IoT-Hub senden.</span><span class="sxs-lookup"><span data-stu-id="36a9f-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="36a9f-183">In Supply Chain Management wird eine Benachrichtigung generiert, wenn der Artikel zu schwer oder zu leicht ist.</span><span class="sxs-lookup"><span data-stu-id="36a9f-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="36a9f-184">Das Szenario hat folgende Abhängigkeiten:</span><span class="sxs-lookup"><span data-stu-id="36a9f-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="36a9f-185">Ein Fertigungsauftrag muss auf einer zugeordneten Maschine ausgeführt werden und ein Produkt mit einem zugeordneten Chargenattribut produzieren, damit eine Warnung ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="36a9f-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="36a9f-186">Ein Signal, das das Chargenattribut darstellt, muss mit einem eindeutigen Eigenschaftsnamen an den IoT-Hub gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="36a9f-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="36a9f-187">In der IoT-Hub-Nachricht muss eine Unix-Millisekunden-Zeitstempeleigenschaft vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="36a9f-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="36a9f-188">Szenario **Produktionsverzögerungen** im Supply Chain Management konfigurieren</span><span class="sxs-lookup"><span data-stu-id="36a9f-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="36a9f-189">Das Szenario **Produktionsverzögerungen** generiert eine Benachrichtigung, wenn der Produktionsdurchsatz einen Schwellenwert unterschreitet.</span><span class="sxs-lookup"><span data-stu-id="36a9f-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="36a9f-190">In diesem Szenario wird ein **PartOut**-Signal für jeden produzierten Artikel an IoT-Hub gesendet.</span><span class="sxs-lookup"><span data-stu-id="36a9f-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="36a9f-191">In Supply Chain Management wird die Auftragsverzögerung basierend darauf berechnet, wie lange der Fertigungsauftrag ausgeführt werden soll, wie viele Artikel produziert werden sollen, wie lange der Auftrag ausgeführt wurde und wie viele **PartOut**-Signale empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="36a9f-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="36a9f-192">Eine Verzögerungsbenachrichtigung würde generiert, wenn die Zahl der **PartOut**-Signale für den Einzelvorgang den Schwellenwert des erwarteten Wertes unterschreitet.</span><span class="sxs-lookup"><span data-stu-id="36a9f-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="36a9f-193">Das Szenario hat folgende Abhängigkeiten:</span><span class="sxs-lookup"><span data-stu-id="36a9f-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="36a9f-194">Ein Fertigungsauftrag muss auf einer zugeordneten Maschine ausgeführt werden, damit eine Warnung ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="36a9f-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="36a9f-195">Ein Signal, das das Teilausgangssignal einer zugeordneten Maschine darstellt, muss mit einem eindeutigen Eigenschaftsnamen an den IoT-Hub gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="36a9f-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="36a9f-196">In der IoT-Hub-Nachricht muss eine Unix-Millisekunden-Zeitstempeleigenschaft vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="36a9f-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="36a9f-197">So deaktivieren Sie ein Szenario</span><span class="sxs-lookup"><span data-stu-id="36a9f-197">How to disable a scenario</span></span>

<span data-ttu-id="36a9f-198">Um ein Szenario zu deaktivieren, führen Sie folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="36a9f-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="36a9f-199">Navigieren Sie in Supply Chain Management zu **Produktionskontrolle \> Einrichtung \> IoT-Intelligenz \>Szenarioverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="36a9f-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="36a9f-200">Klicken Sie auf **Konfigurieren** im Szenario.</span><span class="sxs-lookup"><span data-stu-id="36a9f-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="36a9f-201">Klicken Sie auf **Weiter**, um zur letzten Registerkarte des Assistenten zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="36a9f-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="36a9f-202">Schalten Sie den Schieberegler um, um das Szenario zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="36a9f-202">Toggle the slider to disable the scenario.</span></span>
