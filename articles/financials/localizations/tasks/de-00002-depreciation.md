--- 
title: "Abschreibungsregulierungen für zusätzliche Anschaffungen im zweiten Jahr (Deutschland)"
description: "Dieses Handbuch veranschaulicht, wie die Berechnung der Abschreibung für zusätzliche Anschaffungen eingerichtet."
author: mrolecki
manager: AnnBe
ms.date: 05/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Germany
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 10ac903342d5dd5e2bd207665beb8170c53bff7c
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="depreciation-adjustments-for-additional-acquisitions-in-the-second-year-germany"></a><span data-ttu-id="433d3-103">Abschreibungsregulierungen für zusätzliche Anschaffungen im zweiten Jahr (Deutschland)</span><span class="sxs-lookup"><span data-stu-id="433d3-103">Depreciation adjustments for additional acquisitions in the second year (Germany)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="433d3-104">Dieses Handbuch veranschaulicht, wie die Berechnung der Abschreibung für zusätzliche Anschaffungen eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="433d3-104">This guide demonstrates how to set up the calculation of depreciation for additional acquisitions.</span></span> <span data-ttu-id="433d3-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DEMF.</span><span class="sxs-lookup"><span data-stu-id="433d3-105">The demo data company used to create this procedure is DEMF.</span></span>


## <a name="allow-multiple-acquisitions"></a><span data-ttu-id="433d3-106">Mehrere Anschaffungen zulassen</span><span class="sxs-lookup"><span data-stu-id="433d3-106">Allow multiple acquisitions</span></span>
1. <span data-ttu-id="433d3-107">Wechseln Sie zu "Anlagen" > "Einstellungen" > "Anlagenparameter".</span><span class="sxs-lookup"><span data-stu-id="433d3-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="433d3-108">Prüfen Sie das mehrere Anschaffungskontrollkästchen des Zulässiger.</span><span class="sxs-lookup"><span data-stu-id="433d3-108">Check the Allow multiple acquisitions checkbox.</span></span>
3. <span data-ttu-id="433d3-109">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="433d3-109">Click Save.</span></span>

## <a name="set-up-depreciation-profile"></a><span data-ttu-id="433d3-110">Einrichten von Abschreibungsprofilen</span><span class="sxs-lookup"><span data-stu-id="433d3-110">Set up depreciation profile</span></span>
1. <span data-ttu-id="433d3-111">Wechseln Sie zu Anlagen > Einstellungen > Abschreibungsprofile.</span><span class="sxs-lookup"><span data-stu-id="433d3-111">Go to Fixed assets > Setup > Depreciation profiles.</span></span>
2. <span data-ttu-id="433d3-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="433d3-112">Click New.</span></span>
3. <span data-ttu-id="433d3-113">Geben Sie im Feld "Abschreibungsprofil" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="433d3-113">In the Depreciation profile field, type a value.</span></span>
4. <span data-ttu-id="433d3-114">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="433d3-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="433d3-115">Abschreibungsmethode "Lineare verbleibende Nutzungsdauer"</span><span class="sxs-lookup"><span data-stu-id="433d3-115">In the Method field, select 'Straight line life remaining'.</span></span>
6. <span data-ttu-id="433d3-116">Wählen Sie im Feld "Berichtszeitraum" "Monatlich" aus.</span><span class="sxs-lookup"><span data-stu-id="433d3-116">In the Period frequency field, select 'Monthly'.</span></span>
7. <span data-ttu-id="433d3-117">Ganzjährliche Abschreibung sonstiger Anschaffungen</span><span class="sxs-lookup"><span data-stu-id="433d3-117">Check the Full year depreciation on additional acquisitions checkbox.</span></span>
8. <span data-ttu-id="433d3-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="433d3-118">Click Save.</span></span>


