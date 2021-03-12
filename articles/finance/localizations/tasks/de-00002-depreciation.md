---
title: DE-00002 Abschreibungsregulierungen für zusätzliche Anschaffungen im zweiten Jahr
description: Dieses Handbuch veranschaulicht, wie die Berechnung der Abschreibung für zusätzliche Anschaffungen eingerichtet.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.search.region: Germany
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9479f5935b7eda81408986fc1aa2d31e107aba2b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964503"
---
# <a name="de-00002-depreciation-adjustments-for-additional-acquisitions-in-the-second-year"></a><span data-ttu-id="6fa09-103">DE-00002 Abschreibungsregulierungen für zusätzliche Anschaffungen im zweiten Jahr</span><span class="sxs-lookup"><span data-stu-id="6fa09-103">DE-00002 Depreciation adjustments for additional acquisitions in the second year</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6fa09-104">Dieses Handbuch veranschaulicht, wie die Berechnung der Abschreibung für zusätzliche Anschaffungen eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6fa09-104">This guide demonstrates how to set up the calculation of depreciation for additional acquisitions.</span></span> <span data-ttu-id="6fa09-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DEMF.</span><span class="sxs-lookup"><span data-stu-id="6fa09-105">The demo data company used to create this procedure is DEMF.</span></span>


## <a name="allow-multiple-acquisitions"></a><span data-ttu-id="6fa09-106">Mehrere Anschaffungen zulassen</span><span class="sxs-lookup"><span data-stu-id="6fa09-106">Allow multiple acquisitions</span></span>
1. <span data-ttu-id="6fa09-107">Wechseln Sie zu "Anlagen" > "Einstellungen" > "Anlagenparameter".</span><span class="sxs-lookup"><span data-stu-id="6fa09-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="6fa09-108">Prüfen Sie das mehrere Anschaffungskontrollkästchen des Zulässiger.</span><span class="sxs-lookup"><span data-stu-id="6fa09-108">Check the Allow multiple acquisitions checkbox.</span></span>
3. <span data-ttu-id="6fa09-109">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6fa09-109">Click Save.</span></span>

## <a name="set-up-depreciation-profile"></a><span data-ttu-id="6fa09-110">Einrichten von Abschreibungsprofilen</span><span class="sxs-lookup"><span data-stu-id="6fa09-110">Set up depreciation profile</span></span>
1. <span data-ttu-id="6fa09-111">Wechseln Sie zu Anlagen > Einstellungen > Abschreibungsprofile.</span><span class="sxs-lookup"><span data-stu-id="6fa09-111">Go to Fixed assets > Setup > Depreciation profiles.</span></span>
2. <span data-ttu-id="6fa09-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6fa09-112">Click New.</span></span>
3. <span data-ttu-id="6fa09-113">Geben Sie im Feld "Abschreibungsprofil" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6fa09-113">In the Depreciation profile field, type a value.</span></span>
4. <span data-ttu-id="6fa09-114">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6fa09-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6fa09-115">Abschreibungsmethode "Lineare verbleibende Nutzungsdauer"</span><span class="sxs-lookup"><span data-stu-id="6fa09-115">In the Method field, select 'Straight line life remaining'.</span></span>
6. <span data-ttu-id="6fa09-116">Wählen Sie im Feld "Berichtszeitraum" "Monatlich" aus.</span><span class="sxs-lookup"><span data-stu-id="6fa09-116">In the Period frequency field, select 'Monthly'.</span></span>
7. <span data-ttu-id="6fa09-117">Ganzjährliche Abschreibung sonstiger Anschaffungen</span><span class="sxs-lookup"><span data-stu-id="6fa09-117">Check the Full year depreciation on additional acquisitions checkbox.</span></span>
8. <span data-ttu-id="6fa09-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6fa09-118">Click Save.</span></span>

