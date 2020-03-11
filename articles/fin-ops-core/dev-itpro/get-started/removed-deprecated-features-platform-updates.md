---
title: Entfernte oder veraltete Plattformfunktionen
description: Dieses Thema beschreibt Funktionen, die in den Plattform-Updates von Finance and Operations-Anwendungen entfernt wurden oder deren Entfernung geplant ist.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087882"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="c25a7-103">Entfernte oder veraltete Plattformfunktionen</span><span class="sxs-lookup"><span data-stu-id="c25a7-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c25a7-104">Dieses Thema beschreibt Funktionen, die in den Plattform-Updates von Finance and Operations-Anwendungen entfernt wurden oder deren Entfernung geplant ist.</span><span class="sxs-lookup"><span data-stu-id="c25a7-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="c25a7-105">Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c25a7-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="c25a7-106">Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c25a7-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="c25a7-107">Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="c25a7-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="c25a7-108">Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="c25a7-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="c25a7-109">Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="c25a7-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="c25a7-110">Plattformupdate 32</span><span class="sxs-lookup"><span data-stu-id="c25a7-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="c25a7-111">Das Dialogfeld für die Änderung von Workflow-Anforderungen enthält nicht mehr die Dropdown-Liste für die Benutzerauswahl.</span><span class="sxs-lookup"><span data-stu-id="c25a7-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="c25a7-112">**Grund für veralteten Zustand/Entfernung**</span><span class="sxs-lookup"><span data-stu-id="c25a7-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="c25a7-113">Dies war ein Sicherheitsproblem, da die Änderungsanfrage an einen unbeabsichtigten Benutzer gesendet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="c25a7-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="c25a7-114">Dies war auch eine Frage der Benutzerfreundlichkeit, da der Benutzer gezwungen war, den Urheber des Workflows zu bestimmen und manuell auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c25a7-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="c25a7-115">**Ersetzt durch eine andere Funktion?**</span><span class="sxs-lookup"><span data-stu-id="c25a7-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="c25a7-116">Nein</span><span class="sxs-lookup"><span data-stu-id="c25a7-116">No</span></span> |
| <span data-ttu-id="c25a7-117">**Betroffene Produktbereiche**</span><span class="sxs-lookup"><span data-stu-id="c25a7-117">**Product areas affected**</span></span>         | <span data-ttu-id="c25a7-118">Workflow</span><span class="sxs-lookup"><span data-stu-id="c25a7-118">Workflow</span></span> |
| <span data-ttu-id="c25a7-119">**Bereitstellungsoption**</span><span class="sxs-lookup"><span data-stu-id="c25a7-119">**Deployment option**</span></span>              | <span data-ttu-id="c25a7-120">Alle</span><span class="sxs-lookup"><span data-stu-id="c25a7-120">All</span></span> |
| <span data-ttu-id="c25a7-121">**Status**</span><span class="sxs-lookup"><span data-stu-id="c25a7-121">**Status**</span></span>                         | <span data-ttu-id="c25a7-122">Die Benutzerauswahl-Dropdown-Liste wurde aus dem Dialogfeld zur Änderung der Anforderung in Plattform-Update 32 entfernt.</span><span class="sxs-lookup"><span data-stu-id="c25a7-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="c25a7-123">Änderungsanfragen werden automatisch wie vorgesehen an den Absender gesendet.</span><span class="sxs-lookup"><span data-stu-id="c25a7-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="c25a7-124">Weitere Informationen über diese Funktionalität finden Sie unter [Aktionen in Workflow-Genehmigungsprozessen](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span><span class="sxs-lookup"><span data-stu-id="c25a7-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="c25a7-125">Frühere Ankündigungen über entfernte oder veraltete Funktionen</span><span class="sxs-lookup"><span data-stu-id="c25a7-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="c25a7-126">Um mehr über Funktionen zu erfahren, die in früheren Versionen entfernt oder veraltet sind, siehe [Entfernte oder veraltete Funktionen in früheren Versionen](../migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="c25a7-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

