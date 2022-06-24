---
title: IoT Intelligence – Startseite
description: Dieser Artikel enthält Links zu Informationen zu IoT-Intelligenz.
author: johanhoffmann
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b43681b036379a6f95103d4bb17cbde018724552
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877623"
---
# <a name="iot-intelligence-home-page"></a>IoT Intelligence – Startseite

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> Diese Funktion ist aktuell nur in den folgenden Ländern/Regionen verfügbar:
>
> - USA (Vereinigte Staaten von Amerika)
> - EU (Europäische Union)
> - AU (Australien)
> - CA (Kanada)
> - UK (Vereinigtes Königreich)

IoT-Intelligenz ist ein Add-In für Microsoft Dynamics 365 Supply Chain Management. Es integriert Internet of Things (IoT)-Signale mit Daten im Supply Chain Management, um umsetzbare Erkenntnisse zu gewinnen.

IoT-Intelligenz unterstützt die folgenden Szenarien:

- **Produktionsverzögerungen** – Dieses Szenario vergleicht die tatsächliche Zykluszeit mit der geplanten Zykluszeit. Supply Chain Management benachrichtigt Sie, wenn die Produktion nicht im Zeitplan ist, damit Sie eingreifen können, um die Betriebseffizienz zu maximieren und Auftragsverzögerungen zu vermeiden.
- **Ausfallzeiten der Geräte** – Dieses Szenario vergleicht die gemessene Betriebszeit mit benutzerdefinierten Parametern. Supply Chain Management benachrichtigt Sie, wenn eine Ausfallschwelle überschritten wird, damit Sie Aktionen wie die Neuplanung eines Produktionsarbeitsauftrags oder das Anlegen eines Instandhaltungsarbeitsauftrags durchführen können.
- **Produktqualität** – Dieses Szenario vergleicht Sensormesswerte wie Feuchtigkeit und Temperatur mit benutzerdefinierten Qualitätsmetriken. Das Supply Chain Management benachrichtigt Sie, wenn eine Abweichung auftritt, damit Sie eingreifen können, um Qualitätsstandards einzuhalten und Verschwendung zu minimieren.

Die folgende Abbildung zeigt das Zusammenspiel von Azure IoT Hub, IoT-Intelligenz und Supply Chain Management.

![IoT Hub, IoT-Intelligenz und Supply Chain Management.](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>Verfolgung und Wartung

- [Szenarien in Dynamics 365 Supply Chain Management überwachen](iot-management.md#monitor-scenarios)
- [Deaktivieren eines Szenarios](iot-scenario-setup.md#disable-a-scenario)
- [Ausgeführtes IoT-Intelligenz-Szenario ändern](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [Simulationsoptionen](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]