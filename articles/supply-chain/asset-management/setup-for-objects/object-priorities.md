---
title: Anlagenservicelevel
description: In diesem Thema werden Anlagenservicelevel in Asset Management erläutert.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2730dad0a130dfd3916ae51e9be6d81f97c22b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238085"
---
# <a name="asset-service-levels"></a><span data-ttu-id="aeb50-103">Anlagenservicelevel</span><span class="sxs-lookup"><span data-stu-id="aeb50-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="aeb50-104">In diesem Thema werden Anlagenservicelevel in Asset Management erläutert.</span><span class="sxs-lookup"><span data-stu-id="aeb50-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="aeb50-105">Anlagenservicelevel beziehen sich auf Anlagen und werden auf Wartungsanfragen und Arbeitsaufträge übertragen.</span><span class="sxs-lookup"><span data-stu-id="aeb50-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="aeb50-106">Sie werden verwendet, um die Priorität von Arbeitsaufträgen während der Arbeitsauftragsplanung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="aeb50-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="aeb50-107">Anlagenservicelevel können geändert werden, wenn Änderungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="aeb50-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="aeb50-108">Weitere Informationen zu den Einstellungen, die sich auf die Berechnung von Bewertungsnoten für Arbeitsauftragsplanung beziehen, finden Sie unter [Anlagenverwaltungsparameter](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="aeb50-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="aeb50-109">Sie müssen mindestens einen Standarddatensatz für den Anlagenservicelevel einrichten.</span><span class="sxs-lookup"><span data-stu-id="aeb50-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="aeb50-110">Dieser Standarddatensatz wird verwendet, wenn keine andere Übereinstimmung während der Arbeitsauftragsplanung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="aeb50-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="aeb50-111">**Beispiel 1:** Der Standardservicelevel, der verwendet wird, wenn keine andere Übereinstimmung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="aeb50-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="aeb50-112">In diesem Datensatz wählen Sie nur einen Servicelevel aus.</span><span class="sxs-lookup"><span data-stu-id="aeb50-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="aeb50-113">**Beispiel 2:** Ein hoher Servicelevel, der verwendet wird, um einen Wartungseinzelvorgang für einen Volvo-Lkw-Motor zu planen.</span><span class="sxs-lookup"><span data-stu-id="aeb50-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="aeb50-114">In diesem Datensatz wählen Sie einen entsprechenden Anlagentypen aus, wie z. B. **Lkw-Motor**, einen Hersteller (**Volvo**) und eine Servicelevel.</span><span class="sxs-lookup"><span data-stu-id="aeb50-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="aeb50-115">Anlagenservicelevel einrichten</span><span class="sxs-lookup"><span data-stu-id="aeb50-115">Set up asset service levels</span></span>

1. <span data-ttu-id="aeb50-116">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Anlagenservicelevel**.</span><span class="sxs-lookup"><span data-stu-id="aeb50-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="aeb50-117">Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aeb50-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="aeb50-118">Je nach der Detailebene, die für den Anlagenservicelevel erforderlich ist, nehmen Sie die entsprechende Auswahl in den Feldern **Funktionaler Standort**, **Anlagentyp**, **Hersteller**, **Modell**, **Anlage**, **Arbeitsauftragstyp** und **Servicelevel** vor.</span><span class="sxs-lookup"><span data-stu-id="aeb50-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="aeb50-119">Wenn der Anlagenservicelevel für Wartungsanfragen und Arbeitsaufträge verwendet wird, durchläuft Asset-Management alle Anlagenservicelevel-Datensätze, um nach einer möglichen Übereinstimmung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="aeb50-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="aeb50-120">Die spezifischste Kombination wird immer zuerst geprüft.</span><span class="sxs-lookup"><span data-stu-id="aeb50-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="aeb50-121">Das bedeutet, Asset Management sucht als Erstes nach einer Übereinstimmung für das Feld **Arbeitsauftragstyp**.</span><span class="sxs-lookup"><span data-stu-id="aeb50-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="aeb50-122">Wenn keine Übereinstimmung gefunden wird, sucht es nach einer Übereinstimmung für das Feld **Anlage** usw.</span><span class="sxs-lookup"><span data-stu-id="aeb50-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="aeb50-123">Wie Sie im Layout der Seite **Anlagenservicelevel** sehen können, bedeutet dieses Verhalten, dass Asset Management zum Auffinden der spezifischsten Kombinationen jeden Datensatz von rechts nach links auf Übereinstimmung prüft.</span><span class="sxs-lookup"><span data-stu-id="aeb50-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="aeb50-124">Wenn keine Übereinstimmung gefunden wird, wird der Standarddatensatz, der keine Auswahl in diesen Feldern hat, verwendet.</span><span class="sxs-lookup"><span data-stu-id="aeb50-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="aeb50-125">Wählen Sie im Feld **Servicelevel** eine Zahl aus, die den Servicelevel (die Priorität) angibt.</span><span class="sxs-lookup"><span data-stu-id="aeb50-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="aeb50-126">Wenn Sie einen Anlagenservicelevel-Datensatz auf der Seite ändern **Anlagenservicelevel** ändern, nachdem Sie ihn bereits für einen Arbeitsauftrag verwendet haben, wird der Servicelevel für Wartungsanfragen und Arbeitsaufträge nicht entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="aeb50-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]