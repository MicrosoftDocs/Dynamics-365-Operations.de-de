---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management
description: In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen in Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
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
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597115"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Dieses Thema wird aktualisiert, sobald neue entfernte oder veraltete Funktionen dokumentiert werden Dynamics 365 Supply Chain Management.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen.

> [!NOTE]
> Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Entfernte oder veraltete Funktionen in Supply Chain Management 10.0.11

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Verwenden des integrierten Supply Chain Management-Masterplanungsmoduls für Verteilungszenarien

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Um die Leistung zu verbessern und die SQL-Datenbanklast während der Ausführung der Masterplanung zu minimieren, wird das integrierte Supply Chain Management-Masterplanungsmodul durch die Planungsoptimierung ersetzt. Die Planungsoptimierung ermöglicht schnelle Planungsausführungen, die auch während der Geschäftszeiten durchgeführt werden können. Dadurch können Planer sofort auf Änderungen in der Nachfrage oder bei den Planungsparametern reagieren. |
| **Ersetzt durch eine andere Funktion?**   | Ja, die Planungsoptimierung wird das bestehende integrierte Supply Chain Management-Masterplanungsmodul ersetzen. |
| **Betroffene Produktbereiche**         | Supply Chain Management – Masterplanung |
| **Bereitstellungsoption**              | Nur Cloud. Planungsoptimierung wird bei lokalen Bereitstellungen nicht unterstützt. |
| **Status**                         | Veraltet. Im April 2021 werden Verteilungsszenarien mit dem integrierten Dynamics 365 Supply Chain Management-Masterplanungsmodul nicht mehr unterstützt. Für Verteilungsszenarien müssen Kunden die Planungsoptimierung für Masterplanungsberechnungen verwenden. Weitere Informationen finden Sie unter [Planungsoptimierungsdokumentation](https://go.microsoft.com/fwlink/?linkid=2105830). Kunden mit lokalen Bereitstellungen von Dynamics 365 Supply Chain Management verwenden möglicherweise weiterhin das Supply Chain Management-Masterplanungsmodul für Verteilungsszenarien nach April 2021. Es werden jedoch keine weiteren Funktionserweiterungen bereitgestellt. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Frühere Ankündigungen über entfernte oder veraltete Funktionen

Um mehr über Funktionen zu erfahren, die in früheren Versionen entfernt oder veraltet sind, siehe [Entfernte oder veraltete Funktionen in früheren Versionen](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
