---
title: IoT-Intelligenz – Startseite
description: Dieses Thema enthält Links zu Informationen zu IoT-Intelligenz.
author: tonyafehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b6c179052cdb9d1ca808d9cba089163bde0d5d5
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782680"
---
# <a name="iot-intelligence-home-page"></a>IoT-Intelligenz – Startseite

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

+ **Produktionsverzögerungen** – Dieses Szenario vergleicht die tatsächliche Zykluszeit mit der geplanten Zykluszeit. Supply Chain Management benachrichtigt Sie, wenn die Produktion nicht im Zeitplan ist, damit Sie eingreifen können, um die Betriebseffizienz zu maximieren und Auftragsverzögerungen zu vermeiden.
+ **Ausfallzeiten der Geräte** – Dieses Szenario vergleicht die gemessene Betriebszeit mit benutzerdefinierten Parametern. Supply Chain Management benachrichtigt Sie, wenn eine Ausfallschwelle überschritten wird, damit Sie Aktionen wie die Neuplanung eines Produktionsarbeitsauftrags oder das Anlegen eines Instandhaltungsarbeitsauftrags durchführen können.
+ **Produktqualität** – Dieses Szenario vergleicht Sensormesswerte wie Feuchtigkeit und Temperatur mit benutzerdefinierten Qualitätsmetriken. Das Supply Chain Management benachrichtigt Sie, wenn eine Abweichung auftritt, damit Sie eingreifen können, um Qualitätsstandards einzuhalten und Verschwendung zu minimieren.

Die folgende Abbildung zeigt das Zusammenspiel von Azure IoT Hub, IoT-Intelligenz und Supply Chain Management.

![IoT Hub, IoT-Intelligenz und Supply Chain Management.](media/iot_intelligence.png)

## <a name="setup"></a>Einrichtung

Sie können IoT-Intelligenz einrichten und konfigurieren, ohne Code schreiben zu müssen. Hier sind die grundlegenden Schritte:

1. [Einrichten von Azure-Ressourcen](iot-azure-setup.md) – Erstellen Sie einen IoT-Hub, einen Redis Cache und einen Schlüsseltresor, auf den über Supply Chain Management zugegriffen werden kann.
2. [Nachrichtenschemaformate für IoT Hub](iot-schema-format.md) – Konfigurieren Sie Ihre Geräte zum Senden von Nachrichten an IoT Hub und definieren Sie das Nachrichtenformat JavaScript Object Notation (JSON).
3. Aktivieren Sie in der Funktionsverwaltung das IoT-Intelligenz-Funktions-Flag. 
4. [Das IoT-Intelligenz-Add-In in Microsoft Dynamics Lifecycle Services (LCS) installieren](iot-lcs-setup.md) – Installieren Sie das Add-In in LCS und konfigurieren Sie die Azure-Geheimnisse.
5. [Metriken einrichten](iot-metrics-setup.md) – Richten Sie Metriken im Supply Chain Management ein.
6. [Szenario-Einrichtung](iot-scenario-setup.md) – Richten Sie die Szenarien im Supply Chain Management ein.

## <a name="tracking-and-maintenance"></a>Verfolgung und Wartung

+ [Szenarien in Dynamics 365 Supply Chain Management überwachen](iot-management.md#monitor-scenarios)
+ [Deaktivieren eines Szenarios](iot-scenario-setup.md#disable-a-scenario)
+ [Add-In deinstallieren](iot-lcs-setup.md#uninstall-addin)
+ [Ausgeführtes IoT-Intelligenz-Szenario ändern](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [Simulationsoptionen](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]