---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Commerce
description: In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: dd982ae60da1c2958d6d759bb5dd256a71fabf6c
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154200"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Entfernte oder veraltete Funktionen in Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Commerce.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen. 

> [!NOTE]
> Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](https://docs.microsoft.com/dynamics/s-e/). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Entfernte oder veraltete Funktionen in Commerce Version 10.0.17

> [!Important]
> Version 10.0.17 ist als Teil einer Vorschauversion verfügbar. Inhalt und Funktionsweise unterliegen Änderungen. Weitere Informationen zu Vorschauversionen finden Sie in den [FAQ zu Dienstupdates für One Version](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).

### <a name="full-dataset-generation-interval-is-deprecated"></a>Das vollständige Intervall für die Datensatzgenerierung ist veraltet

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ab dieser Version in wird das **Commerce-Scheduler-Parameter**-Formular in der Dynamics 365-Zentralverwaltung das Feld **Vollständiges Intervall für die Datensatzgenerierung in Tagen** veraltet sein. Ab dieser Version wird das Feld auch visuell entfernt, sodass der Wert nicht bearbeitet werden kann. Dies bleibt als Wert **0** erhalten. |
| **Ersetzt durch eine andere Funktion?**   | Nr. |
| **Betroffene Produktbereiche**         | Dynamics 365 Commerce |
| **Bereitstellungsoption**              | Alle|
| **Status**                         | Veraltet. Verwenden Sie dieses Feld nicht und ändern Sie den Wert darin nicht.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Entfernte oder veraltete Funktionen in Commerce Version 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-Unterstützung für Dynamics 365 ist veraltet

|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ab Dezember 2020 wird die Unterstützung von Microsoft Internet Explorer 11 für alle Dynamics 365-Produkte veraltet sein und Internet Explorer 11 wird nach August 2021 nicht mehr unterstützt werden.<br><br>Dies wirkt sich auf Kunden aus, die Dynamics 365-Produkte verwenden, die für die Verwendung über eine Internet Explorer 11-Schnittstelle entworfen wurden. Nach August 2021 wird Internet Explorer 11 für solche Dynamics 365-Produkte nicht mehr unterstützt. |
| **Ersetzt durch eine andere Funktion?**   | Wir empfehlen den Kunden den Übergang zu Microsoft Edge.|
| **Betroffene Produktbereiche**         | Alle Dynamics 365-Produkte |
| **Bereitstellungsoption**              | Alle|
| **Status**                         | Veraltet. Internet Explorer 11 wird nach August 2021 nicht mehr unterstützt.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Entfernte oder veraltete Funktionen in Commerce Version 10.0.11
### <a name="data-action-hooks"></a>Datenaktivitätshooks
|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Funktion für Datenaktions-Hooks wird aufgrund von Leistungsproblemen nicht mehr unterstützt. |
| **Ersetzt durch eine andere Funktion?**   | Es wird empfohlen, [Datenaktion überschreibt](../e-commerce-extensibility/data-action-overrides.md) zu verwenden, um die Geschäftslogik in der Datenaktionsschicht zu ändern.|
| **Betroffene Produktbereiche**         | E-Commerce-Erweiterbarkeit Datenaktionen |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: ab Frühjahr 10.0.11 Version |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Retail SDK Unterstützung für Visual Studio 2015, msbuild 14.0 und Retail SDK\Referencebibliotheken und Tools
|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Retail SDK-Unterstützung für Visual Studio 2015 wurde veraltet und aktualisiert, um VS 2017, msbuild 15.0 und alle Referenzbibliotheken und Commerce-Proxy-Generator-Tools im Ordner RetailSDK\Referenzen zu unterstützen, die in verschoben wurden NuGet-Pakete zur Vereinfachung des Erweiterungsmodells und des SDK-Aktualisierungsprozesses.|
| **Ersetzt durch eine andere Funktion?**   | Wir empfehlen Ihnen, den Informationen in [Migrieren von Retail SDK von Visual Studio 2015 bis Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md) zu folgen, um Ihr System zu aktualisieren. |
| **Betroffene Produktbereiche**         | Retail SDK-Erweiterungen |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: ab Frühjahr 10.0.11 Version |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Retail Server-Erweiterung mit IEdmModelExtender und CommerceController
|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Retail Server -Erweiterung mit IEdmModelExtender und CommerceController wurde eingestellt, um ein vereinfachtes Erweiterungsmodell bereitzustellen. Die neue Implementierung enthält nur die Controller-Klasse ohne zusätzliche Implementierung der IEdmModelExtender-Klasse. Dadurch wird auch die Abhängigkeit von einer bestimmten OData-Version vermieden (wenn die OData-Version aktualisiert wird, können Erweiterungen beschädigt werden.) |
| **Ersetzt durch eine andere Funktion?**   |  Wir empfehlen, dass Sie das IController-Klassenerweiterungsmodell verwenden, indem Sie das NuGet-Paket importieren(Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Betroffene Produktbereiche**         | Retail Server-Erweiterungen |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: ab Frühjahr 10.0.11 Version |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Hardware-Stationserweiterung mit IHardwareStationController
|   |  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Erweiterung der Hardwarestation mit IHardwareStationController wird eingestellt, um ein vereinfachtes Erweiterungsmodell bereitzustellen. Die neue Implementierung wird nur die IController-Klasse ohne zusätzliche Klassenimplementierung haben. Um die Abhängigkeit von den wichtigsten Hardware-Stationsbibliotheken zu vermeiden, muss die vorherige Erweiterung auf mehrere Bibliotheken verweisen.) |
| **Ersetzt durch eine andere Funktion?**   | Es wird empfohlen, dass Sie das IController-Klassenerweiterungsmodell verwenden, indem Sie das NuGet-Paket importieren(Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Betroffene Produktbereiche**         | Hardwar-Stationserweiterungen |
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]