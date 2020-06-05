---
title: IoT-Intelligenz überwachen und verwalten
description: In diesem Thema wird erläutert, wie Sie IoT-Intelligenz überwachen und verwalten.
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
ms.openlocfilehash: 97a87b78a0178424f00e464262bb7f69e8a5b4a0
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386516"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="23a8e-103">IoT-Intelligenz überwachen und verwalten</span><span class="sxs-lookup"><span data-stu-id="23a8e-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23a8e-104">In diesem Thema wird erläutert, wie Sie IoT-Intelligenz überwachen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="23a8e-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="23a8e-105">Szenarien in Microsoft Dynamics 365 Supply Chain Management überwachen</span><span class="sxs-lookup"><span data-stu-id="23a8e-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="23a8e-106">Sie können die IoT-Intelligenz-Verarbeitung von mehreren Orten aus überwachen:</span><span class="sxs-lookup"><span data-stu-id="23a8e-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="23a8e-107">**Module \> Produktionssteuerung \> Abfragen und Berichte \> IoT-Intelligenz \> Benachrichtigungen** – Liste der ungelösten Benachrichtigungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="23a8e-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="23a8e-108">**Module \> Produktionssteuerung \> Abfragen und Berichte \> IoT-Intelligenz \> Geschlossene Benachrichtigungen** – Liste der Benachrichtigungen anzeigen, die gelöst oder verworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="23a8e-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="23a8e-109">**Module \> Produktionssteuerung \> Abfragen und Berichte \> IoT-Intelligenz \> Metrische Schlüssel** – Metrikschlüssel für die Zeitreihendiagramme des **Ressourcenstatus** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="23a8e-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="23a8e-110">**Module \> Produktionssteuerung \> Fertigungssteuerung \> Ressourcenstatus** – Bestimmte Metriken über das Dialogfeld **Konfigurieren** verfolgen.</span><span class="sxs-lookup"><span data-stu-id="23a8e-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="23a8e-111">Wenn ein Szenario eine Ausnahme erkennt, zeigt eine Benachrichtigung die Details der Ausnahme an.</span><span class="sxs-lookup"><span data-stu-id="23a8e-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="23a8e-112">**Arbeitsbereiche \> Produktionsverwaltung \> Benachrichtigungen** – Liste der nicht aufgelösten Benachrichtigungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="23a8e-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="23a8e-113">Ausgeführtes IoT-Intelligenz-Szenario ändern</span><span class="sxs-lookup"><span data-stu-id="23a8e-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="23a8e-114">Wenn ein Szenario ausgeführt wird, können Sie folgende Änderungen vornehmen:</span><span class="sxs-lookup"><span data-stu-id="23a8e-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="23a8e-115">Neue Definitionen für Sensorschemas hinzufügen</span><span class="sxs-lookup"><span data-stu-id="23a8e-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="23a8e-116">Neue Signaldatenwerte auswählen</span><span class="sxs-lookup"><span data-stu-id="23a8e-116">Select new signal data values.</span></span>
+ <span data-ttu-id="23a8e-117">Die Auswahl vorhandener Signaldatenwerte abbrechen</span><span class="sxs-lookup"><span data-stu-id="23a8e-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="23a8e-118">Neue Signaldatenwerte hinzufügen und zuordnen</span><span class="sxs-lookup"><span data-stu-id="23a8e-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="23a8e-119">Schwellenwerte aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="23a8e-119">Update threshold values.</span></span>

<span data-ttu-id="23a8e-120">Wenn ein Szenario ausgeführt wird, können dürfen die folgende Änderungen nicht vorgenommen werden:</span><span class="sxs-lookup"><span data-stu-id="23a8e-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="23a8e-121">Schemadefinitionen, die derzeit von einem aktivierten Szenario verwendet werden löschen oder ändern</span><span class="sxs-lookup"><span data-stu-id="23a8e-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="23a8e-122">Die ausgewählten Schemapfade des aktivierten Szenarios ändern</span><span class="sxs-lookup"><span data-stu-id="23a8e-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="23a8e-123">Simulationsoptionen</span><span class="sxs-lookup"><span data-stu-id="23a8e-123">Simulation options</span></span>

<span data-ttu-id="23a8e-124">Sie können werkseitige Maschinensignale simulieren.</span><span class="sxs-lookup"><span data-stu-id="23a8e-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="23a8e-125">Weitere Informationen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="23a8e-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="23a8e-126">IoT DevKit AZ3166 mit Azure IoT Hub verbinden</span><span class="sxs-lookup"><span data-stu-id="23a8e-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="23a8e-127">Raspberry Pi-Onlinesimulator mit Azure IoT Hub (Node.js) verbinden</span><span class="sxs-lookup"><span data-stu-id="23a8e-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="23a8e-128">Übersicht über den Solution Accelerator für die Gerätesimulation</span><span class="sxs-lookup"><span data-stu-id="23a8e-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
