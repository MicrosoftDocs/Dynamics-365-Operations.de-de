---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management
description: In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen in Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a7a06b5476302e43d107c448c139c235ea57b05b
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947543"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Dieses Thema wird aktualisiert, sobald neue entfernte oder veraltete Funktionen dokumentiert werden Dynamics 365 Supply Chain Management.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen.

> [!NOTE]
> Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](/dynamics/s-e/). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.


## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>Entfernte oder veraltete Funktionen in Supply Chain Management 10.0.19

### <a name="job-card-device"></a>Einzelvorgangslistengerät

|   |   |
|---|---|
| **Grund für veralteten Zustand/Entfernung** | Das [Jobkartengerät](../production-control/config-job-card-device.md) wird durch die neue [Produktionsausführungsoberfläche](../production-control/production-floor-execution-configure.md) ersetzt. |
| **Ersetzt durch eine andere Funktion?**   | Ja, das [Jobkartengerät](../production-control/config-job-card-device.md) soll durch die neue [Produktionsausführungsoberfläche](../production-control/production-floor-execution-configure.md) ersetzt werden. |
| **Betroffene Produktbereiche** | Supply Chain Management – Steuerelement für die Produktion |
| **Bereitstellungsoption** | Cloud und lokal |
| **Status** | Veraltet. Das Jobkartengerät wird mit Fehler- und Sicherheitskorrekturen unterstützt, aber Funktionserweiterungen werden nicht mehr zur Verfügung gestellt. Nach April 2022 wird das Jobkarten-Gerät nicht mehr unterstützt und die Kunden werden aufgefordert, auf die neue Produktionsausführungsoberfläche umzusteigen. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Entfernte oder veraltete Funktionen in Supply Chain Management 10.0.18

### <a name="dynamics-365-for-finance-and-operations---warehousing-the-warehouse-app"></a>Dynamics 365 for Finance and Operations – Lagerhaltung (die Lagerort-App)

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Gültig ab April 2021, *Dynamics 365 for Finance and Operations – Lagerhaltung* (die Lagerort-App) ist veraltet und wird nach April 2022 nicht mehr unterstützt. Es wird jetzt durch die *Warehouse Management Mobile App* ersetzt, die mit Version 10.0.17 von Supply Chain Management veröffentlicht wurde. Die neue App ist ein vollständiger Ersatz, verwendet jedoch dasselbe zugrunde liegende Framework, was die Migration vereinfacht. Bei Bedarf können die beiden Apps nebeneinander verwendet werden, damit Benutzer sich schrittweise anpassen können, während sie lernen, die neue App zu verwenden.<br><br>Weitere Informationen über die neue Warehouse Management Mobile App finden Sie unter [Mobile Warehouse Management-Anwendung](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) und unter [Warehouse Management Mobile App installieren und Verbindung herstellen](../warehousing/install-configure-warehouse-management-app.md). |
| **Ersetzt durch eine andere Funktion?**   | Ja, wird durch die neue Warehouse Management Mobile App ersetzt. |
| **Betroffene Produktbereiche**         | Supply Chain Management – Lagerort-App |
| **Bereitstellungsoption**              | Cloud und lokal |
| **Status**                         | Veraltet. Die Lagerort-App wird mit Fehler- und Sicherheitskorrekturen unterstützt, es werden jedoch keine Funktionserweiterungen mehr bereitgestellt. Nach April 2022 wird die alte Lagerort-App nicht mehr unterstützt und Kunden werden aufgefordert, auf die neue Warehouse Management Mobile App umzusteigen. Die alte Lagerort-App wird dann aus dem Microsoft Store und dem Google Play Store entfernt.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Entfernte oder veraltete Funktionen in Supply Chain Management 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 Unterstützung für Dynamics 365 wird außer Betrieb genommen

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ab Dezember 2020 wird die Unterstützung von Microsoft Internet Explorer 11 für alle Dynamics 365-Produkte veraltet sein und Internet Explorer 11 wird nach August 2021 nicht mehr unterstützt werden.<br><br>Dies wirkt sich auf Kunden aus, die Dynamics 365-Produkte verwenden, die für die Verwendung über eine Internet Explorer 11-Schnittstelle entworfen wurden. Nach August 2021 wird Internet Explorer 11 für solche Dynamics 365-Produkte nicht mehr unterstützt. |
| **Ersetzt durch eine andere Funktion?**   | Wir empfehlen den Kunden den Übergang zu Microsoft Edge.|
| **Betroffene Produktbereiche**         | Alle Dynamics 365-Produkte |
| **Bereitstellungsoption**              | Alle|
| **Status**                         | Veraltet. Internet Explorer 11 wird nach August 2021 nicht mehr unterstützt.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Verwendung der integrierten Supply Chain Management-Masterprogrammplanung für Fertigungsszenarien

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Um die Leistung zu verbessern und die SQL-Datenbanklast während der Ausführung der Masterplanung zu minimieren, wird das integrierte Supply Chain Management-Masterplanungsmodul durch die Planungsoptimierung ersetzt. Die Planungsoptimierung ermöglicht schnelle Planungsausführungen, die auch während der Geschäftszeiten durchgeführt werden können. Dadurch können Planer sofort auf Änderungen in der Nachfrage oder bei den Planungsparametern reagieren. |
| **Ersetzt durch eine andere Funktion?**   | Ja, die Planungsoptimierung wird das bestehende integrierte Supply Chain Management-Masterplanungsmodul ersetzen. |
| **Betroffene Produktbereiche**         | Supply Chain Management – Masterplanung |
| **Bereitstellungsoption**              | Nur Cloud. Planungsoptimierung wird bei lokalen Bereitstellungen nicht unterstützt. |
| **Status**                         | Veraltet. Ab dem 1. April 2022 werden Fertigungsszenarien nicht mehr mit der eingebauten Dynamics 365 Supply Chain Management-Masterprogrammplanung unterstützt. Für Fertigungsszenarien müssen Kunden die Planungsoptimierung für die Produktprogrammplanung verwenden. Weitere Informationen finden Sie unter [Planungsoptimierungsdokumentation](../master-planning/planning-optimization/planning-optimization-overview.md). Kunden, die Dynamics 365 Supply Chain Management lokal bereitstellen, können nach April 2022 weiterhin die Supply Chain Management Masterplanungs-Engine für Fertigungsszenarien verwenden. Es werden jedoch keine weiteren Funktionserweiterungen bereitgestellt. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Entfernte oder veraltete Funktionen in Supply Chain Management 10.0.11

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Verwenden des integrierten Supply Chain Management-Masterplanungsmoduls für Verteilungszenarien

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Um die Leistung zu verbessern und die SQL-Datenbanklast während der Ausführung der Masterplanung zu minimieren, wird das integrierte Supply Chain Management-Masterplanungsmodul durch die Planungsoptimierung ersetzt. Die Planungsoptimierung ermöglicht schnelle Planungsausführungen, die auch während der Geschäftszeiten durchgeführt werden können. Dadurch können Planer sofort auf Änderungen in der Nachfrage oder bei den Planungsparametern reagieren. |
| **Ersetzt durch eine andere Funktion?**   | Ja, die Planungsoptimierung wird das bestehende integrierte Supply Chain Management-Masterplanungsmodul ersetzen. |
| **Betroffene Produktbereiche**         | Supply Chain Management – Masterplanung |
| **Bereitstellungsoption**              | Nur Cloud. Planungsoptimierung wird bei lokalen Bereitstellungen nicht unterstützt. |
| **Status**                         | Veraltet. Ab dem 1. April 2021 werden Vertriebsszenarien nicht mehr mit der eingebauten Dynamics 365 Supply Chain Management-Masterprogrammplanung unterstützt. Für Verteilungsszenarien müssen Kunden die Planungsoptimierung für Masterplanungsberechnungen verwenden. Weitere Informationen finden Sie unter [Planungsoptimierungsdokumentation](../master-planning/planning-optimization/planning-optimization-overview.md). Kunden mit lokalen Bereitstellungen von Dynamics 365 Supply Chain Management verwenden möglicherweise weiterhin das Supply Chain Management-Masterplanungsmodul für Verteilungsszenarien nach April 2021. Es werden jedoch keine weiteren Funktionserweiterungen bereitgestellt. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Frühere Ankündigungen über entfernte oder veraltete Funktionen

Um mehr über Funktionen zu erfahren, die in früheren Versionen entfernt oder veraltet sind, siehe [Entfernte oder veraltete Funktionen in früheren Versionen](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
