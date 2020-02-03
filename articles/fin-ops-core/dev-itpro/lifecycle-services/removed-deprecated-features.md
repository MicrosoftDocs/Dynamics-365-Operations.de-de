---
title: Entfernte oder veraltete Funktionen in Lifecycle Services (LCS)
description: In diesem Thema werden die Funktionen beschrieben, die aus Microsoft Dynamics Lifecycle Services (LCS) entfernt wurden oder entfernt werden sollen.
author: sericks007
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c792d06e9b0aa42919de924bdcc9118358779b72
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885454"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="44bdd-103">Entfernte oder veraltete Funktionen in Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="44bdd-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="44bdd-104">In diesem Thema werden die Funktionen beschrieben, die für Microsoft Dynamics Lifecycle Services (LCS) entfernt wurden oder veraltet sind.</span><span class="sxs-lookup"><span data-stu-id="44bdd-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="44bdd-105">Eine Funktion *entfernt* ist nicht mehr im Dienst verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44bdd-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="44bdd-106">Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="44bdd-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="44bdd-107">Diese Liste soll Ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="44bdd-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="44bdd-108">Oktober 2019 Ankündigungen</span><span class="sxs-lookup"><span data-stu-id="44bdd-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="44bdd-109">Flussdiagramme im Geschäftsprozessmodellierer</span><span class="sxs-lookup"><span data-stu-id="44bdd-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="44bdd-110"><strong>Grund für veralteten Zustand/Entfernung</strong></span><span class="sxs-lookup"><span data-stu-id="44bdd-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="44bdd-111">Die Flowchart-Diagrammkomponente im Geschäftsprozessmodellierer (BPM) wird nicht mehr empfohlen, da das Legacy-Design zu einer geringen Nutzung geführt hat.</span><span class="sxs-lookup"><span data-stu-id="44bdd-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44bdd-112"><strong>Ersetzt durch eine andere Funktion?</strong></span><span class="sxs-lookup"><span data-stu-id="44bdd-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="44bdd-113">Nein</span><span class="sxs-lookup"><span data-stu-id="44bdd-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44bdd-114"><strong>Betroffene Bereiche</strong></span><span class="sxs-lookup"><span data-stu-id="44bdd-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="44bdd-115">Geschäftsprozessmodellierer</span><span class="sxs-lookup"><span data-stu-id="44bdd-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="44bdd-116"><strong>Status</strong></span><span class="sxs-lookup"><span data-stu-id="44bdd-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="44bdd-117">Veraltet: Die Flussdiagrammkomponente in BPM wird voraussichtlich Anfang Februar 2020 entfernt.</span><span class="sxs-lookup"><span data-stu-id="44bdd-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed by early February 2020.</span></span> <span data-ttu-id="44bdd-118">Folgende Funktion wird entfernt:</span><span class="sxs-lookup"><span data-stu-id="44bdd-118">The following functionality will be removed:</span></span>
<ul>
<li><span data-ttu-id="44bdd-119">Vorhandene Flussdiagramme können nicht angezeigt oder bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="44bdd-119">Existing flowcharts will be unavailable for viewing or editing.</span></span> <span data-ttu-id="44bdd-120">Die Formeigenschaften, die mit Flussdiagrammaktivitäten verknüpft sind, sind ebenfalls nicht verfügbar, da die gesamte Registerkarte <strong>Flussdiagramm</strong> entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="44bdd-120">The shape properties that are associated with flowchart activities will also be unavailable, because the whole <strong>Flowchart</strong> tab will be removed.</span></span> <span data-ttu-id="44bdd-121">Diese Flussdiagramme umfassen sowohl automatisch generierte Standardflussdiagramme als auch benutzerdefinierte Flussdiagramme, die auf der Grundlage dieser Standardflussdiagramme geändert werden.</span><span class="sxs-lookup"><span data-stu-id="44bdd-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="44bdd-122">Die Funktion zur Analyse älterer Anpassungen/Lücken ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44bdd-122">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="44bdd-123">Daher wird keine Lückenliste automatisch erstellt oder steht für den Export zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="44bdd-123">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="44bdd-124"><strong>Hinweis:</strong> Diese Funktion war zuvor veraltet und wurde durch Microsoft Azure DevOps-Integrationen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="44bdd-124"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="44bdd-125">Der Versionsverlauf des Flussdiagramms ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44bdd-125">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>