---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Commerce
description: In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 06/10/2020
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
ms.openlocfilehash: 64241ef1c25359c7b3b305c4e8f2b24de7e8f5e4
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443917"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Entfernte oder veraltete Funktionen in Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Commerce.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen. 

> [!NOTE]
> Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Entfernte oder veraltete Funktionen in Commerce Version 10.0.11
### <a name="data-action-hooks"></a>Datenaktivitätshooks
|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Funktion für Datenaktions-Hooks wird aufgrund von Leistungsproblemen nicht mehr unterstützt. |
| **Ersetzt durch eine andere Funktion?**   | Es wird empfohlen, stattdessen [Datenaktion überschreibt](../e-commerce-extensibility/data-action-overrides.md) zu verwenden, um die Geschäftslogik in der Datenaktionsschicht zu ändern.|
| **Betroffene Produktbereiche**         | E-Commerce-Erweiterbarkeit Datenaktionen |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: ab Frühjahr 10.0.11 Version |

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
