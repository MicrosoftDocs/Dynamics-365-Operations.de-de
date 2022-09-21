---
title: Sensor Data Intelligence-Startseite
description: In diesem Artikel wird eine Übersicht der Sensor Data Intelligence angezeigt. Organisationen können diese Funktion verwenden, um Geschäftsprozesse in Microsoft Dynamics 365 Supply Chain Management voranzutreiben, basierend auf Internet of Things (IoT)-Signalen von Maschinen und Anlagen in der Produktionshalle.
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
ms.openlocfilehash: 2e4cd8d4d4ffcd10d02fbf26615f12cdd6ccca9e
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428369"
---
# <a name="sensor-data-intelligence-home-page"></a>Sensor Data Intelligence-Startseite

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Sensor Data Intelligence für Microsoft Dynamics 365 Supply Chain Management ermöglicht es Unternehmen, Geschäftsprozesse im Supply Chain Management auf der Grundlage von Internet of Things (IoT)-Signalen von Maschinen und Anlagen in der Produktion zu steuern. Es ist eine aktualisierte, umbenannte Version der *IoT-Intelligenz*-Funktion, die zuvor für das Supply Chain Management verfügbar war.

Mit Sensor Data Intelligence können folgende Aufgaben ausgeführt werden:

- Sammeln Sie Details von Maschinen und Anlagen, um Zählerwerte für Wartungsanlagen im Supply Chain Management zu aktualisieren und die vorausschauende Wartung voranzutreiben.
- Richten Sie die Lösung mithilfe eines einfachen Onboarding-Assistenten ein, anstatt Komponenten manuell in Microsoft Dynamics Lifecycle Services (LCS) zu installieren und zu konfigurieren.
- Stellen Sie Komponenten in Ihrem eigenen Abonnement bereit, damit Sie mehr Flexibilität bei der Verwaltung von Azure-Komponenten haben.
- Konfigurieren, skalieren und erweitern Sie die Lösung als Geschäftslogik, die auf Azure-Komponenten ausgeführt wird. Diese Komponenten werden jetzt in Ihrem eigenen Abonnement verwaltet. Daher können Sie sie nach Bedarf anpassen, um Ihre individuellen Geschäftsanforderungen zu erfüllen.

## <a name="business-scenarios"></a>Geschäftsszenarien

Sensor Data Intelligence ermöglicht mehrere Arten von Funktionen, von denen jede durch ein spezifisches *Szenario* im System repräsentiert wird. Jedes Szenario bietet einen speziellen Satz von Konfigurationsoptionen im System, wie in der folgenden Tabelle aufgeführt.

| Szenario | Description |
|---|---|
| [Anlagenausfall](sdi-scenario-asset-downtime.md) | Verfolgen Sie die Effizienz von Maschinenanlagen genau nach, indem Sie Sensordaten verwenden, um Maschinenausfallzeiten zu verfolgen. |
| [Anlagenwartung](sdi-scenario-asset-maintenance.md) | Minimieren Sie die Wartungskosten und verlängern Sie die Lebensdauer der Anlagen, indem Sie die Wartungspläne auf der Grundlage von Sensormesswerten kritischer Kontrollpunkte für Maschinenanlagen verbessern. |
| [Maschinenstatus](sdi-scenario-equipment-downtime.md) | Stellen Sie die Betriebseffizienz sicher, indem Sie Sensormesswerte verwenden, um Planer über Maschinenausfälle zu informieren und Optionen zur Minderung potenzieller Verzögerungen bereitzustellen. |
| [Produktqualität](sdi-scenario-product-quality.md) | Stellen Sie die Qualität von Produktchargen sicher, indem Sie Sensormesswerte mit tatsächlichen Eigenschaften jeder Produktcharge wie Feuchtigkeit, Temperatur oder benutzerdefinierten Qualitätsmetriken vergleichen. Das System benachrichtigt Benutzer, wenn Abweichungen auftreten. |
| [Produktionsverzögerungen](sdi-scenario-production-delays.md) | Verwenden Sie Sensormesswerte, um die tatsächliche Zykluszeit mit der geplanten Zykluszeit zu vergleichen, und benachrichtigen Sie Vorgesetzte, wenn die Produktion nicht im Zeitplan liegt. Vorgesetzte können dann nach Bedarf eingreifen, um eine maximale Betriebseffizienz zu gewährleisten. |

## <a name="architecture"></a>Architektur

Das folgende Architekturdiagramm gibt einen Überblick über die Lösung und ihre Komponenten.

![Architekturdiagramm für Sensordatenintelligenz.](media/sdi-architecture.png "Architekturdiagramm für Sensor Data Intelligence")
