---
title: IoT-Intelligenz überwachen und verwalten
description: In diesem Thema wird erläutert, wie Sie IoT-Intelligenz überwachen und verwalten.
author: tonyafehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8fbd750aa4a316f5e04f3c8622d0847ad9318360
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782656"
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

+ [IoT DevKit AZ3166 mit Azure IoT Hub verbinden](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Raspberry Pi-Onlinesimulator mit Azure IoT Hub (Node.js) verbinden](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [Übersicht über den Solution Accelerator für die Gerätesimulation](/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]