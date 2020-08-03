---
title: IoT-Intelligenz überwachen und verwalten
description: In diesem Thema wird erläutert, wie Sie IoT-Intelligenz überwachen und verwalten.
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
ms.openlocfilehash: 05aee9865dc90c97e026d5c05fa2032fc0625f7a
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597407"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT-Intelligenz überwachen und verwalten

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie IoT-Intelligenz überwachen und verwalten.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>Szenarien in Microsoft Dynamics 365 Supply Chain Management überwachen

Sie können die IoT-Intelligenz-Verarbeitung von mehreren Orten aus überwachen:

+ **Module \> Produktionssteuerung \> Abfragen und Berichte \> IoT-Intelligenz \> Benachrichtigungen** – Liste der ungelösten Benachrichtigungen anzeigen.
+ **Module \> Produktionssteuerung \> Abfragen und Berichte \> IoT-Intelligenz \> Geschlossene Benachrichtigungen** – Liste der Benachrichtigungen anzeigen, die gelöst oder verworfen wurden.
+ **Module \> Produktionssteuerung \> Abfragen und Berichte \> IoT-Intelligenz \> Metrische Schlüssel** – Metrikschlüssel für die Zeitreihendiagramme des **Ressourcenstatus** anzeigen.
+ **Module \> Produktionssteuerung \> Fertigungssteuerung \> Ressourcenstatus** – Bestimmte Metriken über das Dialogfeld **Konfigurieren** verfolgen. Wenn ein Szenario eine Ausnahme erkennt, zeigt eine Benachrichtigung die Details der Ausnahme an.
+ **Arbeitsbereiche \> Produktionsverwaltung \> Benachrichtigungen** – Liste der nicht aufgelösten Benachrichtigungen anzeigen.

## <a name="modify-a-running-iot-intelligence-scenario"></a>Ausgeführtes IoT-Intelligenz-Szenario ändern

Wenn ein Szenario ausgeführt wird, können Sie folgende Änderungen vornehmen:

+ Neue Definitionen für Sensorschemas hinzufügen
+ Neue Signaldatenwerte auswählen
+ Die Auswahl vorhandener Signaldatenwerte abbrechen
+ Neue Signaldatenwerte hinzufügen und zuordnen
+ Schwellenwerte aktualisieren.

Wenn ein Szenario ausgeführt wird, können dürfen die folgende Änderungen nicht vorgenommen werden:

+ Schemadefinitionen, die derzeit von einem aktivierten Szenario verwendet werden löschen oder ändern
+ Die ausgewählten Schemapfade des aktivierten Szenarios ändern

## <a name="simulation-options"></a>Simulationsoptionen

Sie können werkseitige Maschinensignale simulieren. Weitere Informationen finden Sie in den folgenden Themen:

+ [IoT DevKit AZ3166 mit Azure IoT Hub verbinden](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Raspberry Pi-Onlinesimulator mit Azure IoT Hub (Node.js) verbinden](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [Übersicht über den Solution Accelerator für die Gerätesimulation](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
