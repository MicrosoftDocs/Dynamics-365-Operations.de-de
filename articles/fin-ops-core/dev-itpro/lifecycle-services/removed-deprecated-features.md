---
title: Entfernte oder veraltete Funktionen in Lifecycle Services (LCS)
description: In diesem Thema werden die Funktionen beschrieben, die aus Microsoft Dynamics Lifecycle Services (LCS) entfernt wurden oder entfernt werden sollen.
author: AngelMarshall
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5c5c525b403715ba8dfd3c1bc2dfac4dd69f4a3d
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367267"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="e0a8f-103">Entfernte oder veraltete Funktionen in Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="e0a8f-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e0a8f-104">In diesem Thema werden die Funktionen beschrieben, die für Microsoft Dynamics Lifecycle Services (LCS) entfernt wurden oder veraltet sind.</span><span class="sxs-lookup"><span data-stu-id="e0a8f-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="e0a8f-105">Eine Funktion *entfernt* ist nicht mehr im Dienst verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e0a8f-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="e0a8f-106">Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e0a8f-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="e0a8f-107">Diese Liste soll Ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="e0a8f-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="e0a8f-108">Oktober 2019 Ankündigungen</span><span class="sxs-lookup"><span data-stu-id="e0a8f-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="e0a8f-109">Flussdiagramme im Geschäftsprozessmodellierer</span><span class="sxs-lookup"><span data-stu-id="e0a8f-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="e0a8f-110"><strong>Grund für veralteten Zustand/Entfernung</strong></span><span class="sxs-lookup"><span data-stu-id="e0a8f-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="e0a8f-111">Die Flowchart-Diagrammkomponente im Geschäftsprozessmodellierer (BPM) wird nicht mehr empfohlen, da das Legacy-Design zu einer geringen Nutzung geführt hat.</span><span class="sxs-lookup"><span data-stu-id="e0a8f-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e0a8f-112"><strong>Ersetzt durch eine andere Funktion?</strong></span><span class="sxs-lookup"><span data-stu-id="e0a8f-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="e0a8f-113">Nein</span><span class="sxs-lookup"><span data-stu-id="e0a8f-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e0a8f-114"><strong>Betroffene Bereiche</strong></span><span class="sxs-lookup"><span data-stu-id="e0a8f-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="e0a8f-115">Geschäftsprozessmodellierer</span><span class="sxs-lookup"><span data-stu-id="e0a8f-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e0a8f-116"><strong>Status</strong></span><span class="sxs-lookup"><span data-stu-id="e0a8f-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="e0a8f-117">Veraltet: Die Flussdiagrammkomponente in BPM wird voraussichtlich im Jahr 2020 entfernt.</span><span class="sxs-lookup"><span data-stu-id="e0a8f-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="e0a8f-118">Folgende Funktion wird nicht mehr verfügbar sein:</span><span class="sxs-lookup"><span data-stu-id="e0a8f-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="e0a8f-119">Alle Flussdiagramme sind schreibgeschützt und können nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="e0a8f-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="e0a8f-120">Die Formeigenschaften, die Flussdiagrammaktivitäten zugeordnet sind, sind ebenfalls nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e0a8f-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="e0a8f-121">Diese Flussdiagramme umfassen sowohl automatisch generierte Standardflussdiagramme als auch benutzerdefinierte Flussdiagramme, die auf der Grundlage dieser Standardflussdiagramme geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e0a8f-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="e0a8f-122">Die Funktion zur Analyse älterer Anpassungen/Lücken ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e0a8f-122">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="e0a8f-123">Daher wird keine Lückenliste automatisch erstellt oder steht für den Export zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e0a8f-123">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="e0a8f-124"><strong>Hinweis:</strong> Diese Funktion war zuvor veraltet und wurde durch Microsoft Azure DevOps-Integrationen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e0a8f-124"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="e0a8f-125">Der Versionsverlauf des Flussdiagramms ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e0a8f-125">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
