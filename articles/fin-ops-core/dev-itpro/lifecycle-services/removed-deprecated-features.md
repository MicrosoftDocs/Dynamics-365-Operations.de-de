---
title: Entfernte oder veraltete Funktionen in Lifecycle Services (LCS)
description: In diesem Thema werden die Funktionen beschrieben, die aus Microsoft Dynamics Lifecycle Services (LCS) entfernt wurden oder entfernt werden sollen.
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b49a6f26b4c2fa895fe0e49f716ce423c3c0057
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559084"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="0e20a-103">Entfernte oder veraltete Funktionen in Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="0e20a-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0e20a-104">In diesem Thema werden die Funktionen beschrieben, die für Microsoft Dynamics Lifecycle Services (LCS) entfernt wurden oder veraltet sind.</span><span class="sxs-lookup"><span data-stu-id="0e20a-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="0e20a-105">Eine Funktion *entfernt* ist nicht mehr im Dienst verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e20a-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="0e20a-106">Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="0e20a-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="0e20a-107">Diese Liste soll Ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="0e20a-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="0e20a-108">Oktober 2019 Ankündigungen</span><span class="sxs-lookup"><span data-stu-id="0e20a-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="0e20a-109">Flussdiagramme im Geschäftsprozessmodellierer</span><span class="sxs-lookup"><span data-stu-id="0e20a-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="0e20a-110"><strong>Grund für veralteten Zustand/Entfernung</strong></span><span class="sxs-lookup"><span data-stu-id="0e20a-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="0e20a-111">Die Flowchart-Diagrammkomponente im Geschäftsprozessmodellierer (BPM) wird nicht mehr empfohlen, da das Legacy-Design zu einer geringen Nutzung geführt hat.</span><span class="sxs-lookup"><span data-stu-id="0e20a-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e20a-112"><strong>Ersetzt durch eine andere Funktion?</strong></span><span class="sxs-lookup"><span data-stu-id="0e20a-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="0e20a-113">Nein</span><span class="sxs-lookup"><span data-stu-id="0e20a-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e20a-114"><strong>Betroffene Bereiche</strong></span><span class="sxs-lookup"><span data-stu-id="0e20a-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="0e20a-115">Geschäftsprozessmodellierer</span><span class="sxs-lookup"><span data-stu-id="0e20a-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e20a-116"><strong>Status</strong></span><span class="sxs-lookup"><span data-stu-id="0e20a-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="0e20a-117">Veraltet: Die Flussdiagrammkomponente in BPM wird voraussichtlich im Jahr 2020 entfernt.</span><span class="sxs-lookup"><span data-stu-id="0e20a-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="0e20a-118">Folgende Funktion wird nicht mehr verfügbar sein:</span><span class="sxs-lookup"><span data-stu-id="0e20a-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="0e20a-119">Alle Flussdiagramme sind schreibgeschützt und können nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="0e20a-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="0e20a-120">Die Formeigenschaften, die Flussdiagrammaktivitäten zugeordnet sind, sind ebenfalls nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e20a-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="0e20a-121">Diese Flussdiagramme umfassen sowohl automatisch generierte Standardflussdiagramme als auch benutzerdefinierte Flussdiagramme, die auf der Grundlage dieser Standardflussdiagramme geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0e20a-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="0e20a-122">Die Prozessschritte sind schreibgeschützt und können nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="0e20a-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="0e20a-123">Die Funktion zur Analyse älterer Anpassungen/Lücken ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e20a-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="0e20a-124">Daher wird keine Lückenliste automatisch erstellt oder steht für den Export zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="0e20a-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="0e20a-125"><strong>Hinweis:</strong> Diese Funktion war zuvor veraltet und wurde durch Microsoft Azure DevOps-Integrationen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="0e20a-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="0e20a-126">Der Versionsverlauf des Flussdiagramms ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e20a-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]