---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management
description: In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen in Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d4d2805e36f132660152370cbeee856862ad6faa
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689524"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Dieses Thema wird aktualisiert, sobald neue entfernte oder veraltete Funktionen dokumentiert werden Dynamics 365 Supply Chain Management.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen.

> [!NOTE]
> Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Entfernte oder veraltete Funktionen in Supply Chain Management 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 Unterstützung für Dynamics 365 wird außer Betrieb genommen

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Gültig bis Dezember 2020 wird der Internet Explorer 11-Support von Microsoft für alle Dynamics 365-Produkte außer Betrieb genommen, und Internet Explorer 11 wird ab August 2021 nicht mehr unterstützt werden.<br><br>Dies wird sich auf Kunden auswirken, die Dynamics 365-Produkte verwenden, die für die Verwendung über eine Internet Explorer 11-Schnittstelle konzipiert sind. Nach August 2021 wird Internet Explorer 11 für solche Dynamics 365-Produkte nicht mehr unterstützt werden. |
| **Ersetzt durch eine andere Funktion?**   | Wir empfehlen Kunden, auf Microsoft Edge umzusteigen.|
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
| **Status**                         | Veraltet. Ab dem 1. Oktober 2021 werden Fertigungsszenarien nicht mehr mit der eingebauten Dynamics 365 Supply Chain Management-Masterprogrammplanung unterstützt. Für Fertigungsszenarien müssen Kunden die Planungsoptimierung für die Produktprogrammplanung verwenden. Weitere Informationen finden Sie unter [Planungsoptimierungsdokumentation](https://go.microsoft.com/fwlink/?linkid=2105830). Kunden, die Dynamics 365 Supply Chain Management lokal bereitstellen, können nach Oktober 2021 weiterhin die Supply Chain Management Masterplanungs-Engine für Fertigungsszenarien verwenden. Es werden jedoch keine weiteren Funktionserweiterungen bereitgestellt. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Entfernte oder veraltete Funktionen in Supply Chain Management 10.0.11

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Verwenden des integrierten Supply Chain Management-Masterplanungsmoduls für Verteilungszenarien

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Um die Leistung zu verbessern und die SQL-Datenbanklast während der Ausführung der Masterplanung zu minimieren, wird das integrierte Supply Chain Management-Masterplanungsmodul durch die Planungsoptimierung ersetzt. Die Planungsoptimierung ermöglicht schnelle Planungsausführungen, die auch während der Geschäftszeiten durchgeführt werden können. Dadurch können Planer sofort auf Änderungen in der Nachfrage oder bei den Planungsparametern reagieren. |
| **Ersetzt durch eine andere Funktion?**   | Ja, die Planungsoptimierung wird das bestehende integrierte Supply Chain Management-Masterplanungsmodul ersetzen. |
| **Betroffene Produktbereiche**         | Supply Chain Management – Masterplanung |
| **Bereitstellungsoption**              | Nur Cloud. Planungsoptimierung wird bei lokalen Bereitstellungen nicht unterstützt. |
| **Status**                         | Veraltet. Ab dem 1. April 2021 werden Vertriebsszenarien nicht mehr mit der eingebauten Dynamics 365 Supply Chain Management-Masterprogrammplanung unterstützt. Für Verteilungsszenarien müssen Kunden die Planungsoptimierung für Masterplanungsberechnungen verwenden. Weitere Informationen finden Sie unter [Planungsoptimierungsdokumentation](https://go.microsoft.com/fwlink/?linkid=2105830). Kunden mit lokalen Bereitstellungen von Dynamics 365 Supply Chain Management verwenden möglicherweise weiterhin das Supply Chain Management-Masterplanungsmodul für Verteilungsszenarien nach April 2021. Es werden jedoch keine weiteren Funktionserweiterungen bereitgestellt. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Frühere Ankündigungen über entfernte oder veraltete Funktionen

Um mehr über Funktionen zu erfahren, die in früheren Versionen entfernt oder veraltet sind, siehe [Entfernte oder veraltete Funktionen in früheren Versionen](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
