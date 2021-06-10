---
title: Erstellen einer Umgebung im Power Apps Admin Center nicht möglich
description: In diesem Artikel wird erklärt, was zu tun ist, wenn der Administrator keine Umgebung im Microsoft Power Apps Admin Center erstellen kann.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73c8910900ba6486a8e60a547b07ea0c82a6cb10
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053346"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="6e650-103">Erstellen einer Umgebung im Power Apps Admin Center nicht möglich</span><span class="sxs-lookup"><span data-stu-id="6e650-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6e650-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="6e650-104">**Issue**</span></span>

- <span data-ttu-id="6e650-105">Der Mandanten-/Umgebungsadministrator kann keine Umgebung im Microsoft Power Apps Admin Center erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e650-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="6e650-106">Der Benutzer verfügt nicht über eine Lizenz, die das Recht zum Erstellen von Umgebungen einräumt.</span><span class="sxs-lookup"><span data-stu-id="6e650-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="6e650-107">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="6e650-107">**Solution**</span></span>

<span data-ttu-id="6e650-108">Stellen Sie sicher, dass der Mandantenadministrator dem Benutzer, der die Umgebung erstellt, eine gültige Power Apps-P2-Lizenz zugewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="6e650-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="6e650-109">Folgende Microsoft Dynamics-Servicepläne bieten Berechtigungen zum Erstellen von Umgebungen:</span><span class="sxs-lookup"><span data-stu-id="6e650-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="6e650-110">Gesamtprodukt-Lagermengeneinheit (SKU)</span><span class="sxs-lookup"><span data-stu-id="6e650-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="6e650-111">Power Apps P2-Serviceplan</span><span class="sxs-lookup"><span data-stu-id="6e650-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="6e650-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="6e650-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="6e650-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6e650-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="6e650-114">Microsoft Dynamics 365-Plan – Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="6e650-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="6e650-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6e650-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="6e650-116">Beachten Sie, dass verschiedene Microsoft Office-SKUs auch das Recht bereitstellen, zusammen mit den eigenständigen Power Apps Plan 2 SKUs.</span><span class="sxs-lookup"><span data-stu-id="6e650-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="6e650-117">Der wichtige Aspekt ist, dass einer dieser SKUs vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="6e650-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="6e650-118">Gehe zu [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="6e650-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="6e650-119">Erstellen Sie die Umgebungen, indem Sie in die Anweisungen befolgen in [Human Resources bereitstellen](/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="6e650-119">Create the environments by following the instructions in [Provision Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]