---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Commerce
description: In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335275"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Entfernte oder veraltete Funktionen in Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Commerce.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen. 

> [!NOTE]
> Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Entfernte oder veraltete Funktionen in Commerce Version 10.0.10
### <a name="pos-operation-803---picking-and-receiving"></a>POS-Vorgang 803 – Entnahme und Empfang
|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Entnahme- und Empfangsvorgänge werden veraltet, aufgrund der Neugestaltung des neuen Vorgangs. |
| **Ersetzt durch eine andere Funktion?**   | Ja. Er wird durch zwei neue POS-Vorgänge ersetzt: Eingangsvorgang (804) und Ausgangsvorgang (805).|
| **Betroffene Produktbereiche**         | Verkaufsstellen-(POS)-Anwendung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Ab Version 10.0.10 erhält der Entnahme- und Empfangsvorgang keine neuen Funktionsupdates mehr. Nur kritische Fehlerbehebungen werden für diesen Vorgang in zukünftigen Versionen durchgeführt. Alle Kunden werden aufgefordert, auf die neuen [Eingehenden Vorgänge](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) und [Ausgehenden Vorgänge](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) zu wechseln, die weiterhin Teil unserer langfristigen Produkt-Roadmap sein werden. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Entfernte oder veraltete Funktionen in Commerce Version 10.0.7
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities und GetAvailableInventoryNearby-APIs
|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Neue optimierte APIs sind erstellt worden, um die GetProductAvailabilities und GetAvailableInventoryNearby-APIs zu ersetzen. |
| **Ersetzt durch eine andere Funktion?**   | Ja: Es wird durch GetEstimatedAvailability- und GetEstimatedProductWarehouseAvailability-APIs ersetzt. |
| **Betroffene Produktbereiche**         | E-Commerce-Anwendung SDK |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Ab Version 10.0.7 werden keine technischen Investitionen mehr für GetProductAvailabilities und GetAvailableInventoryNearby getätigt. Organisationen, die diese APIs in ihren E-Commerce-Bereitstellungen verwenden, sollten zu den neuen GetEstimatedAvailability- und GetEstimatedProductWarehouseAvailability-APIs wechseln und die [Optimierte Funktion zur Berechnung der Produktverfügbarkeit](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels) aktivieren.  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Frühere Ankündigungen über entfernte oder veraltete Funktionen
Um mehr über Funktionen zu erfahren, die in früheren Versionen entfernt oder veraltet sind, siehe [Entfernte oder veraltete Funktionen in früheren Versionen](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).
