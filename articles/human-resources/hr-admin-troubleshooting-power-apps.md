---
title: Erstellen einer Umgebung im Power Apps Admin Center nicht möglich
description: In diesem Artikel wird erklärt, was zu tun ist, wenn der Administrator keine Umgebung im Microsoft Power Apps Admin Center erstellen kann.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 26a228229a09e74809a048675a3ff90025f2a26c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892226"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="ac9af-103">Erstellen einer Umgebung im Power Apps Admin Center nicht möglich</span><span class="sxs-lookup"><span data-stu-id="ac9af-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ac9af-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="ac9af-104">**Issue**</span></span>

- <span data-ttu-id="ac9af-105">Der Mandanten-/Umgebungsadministrator kann keine Umgebung im Microsoft Power Apps Admin Center erstellen.</span><span class="sxs-lookup"><span data-stu-id="ac9af-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="ac9af-106">Der Benutzer verfügt nicht über eine Lizenz, die das Recht zum Erstellen von Umgebungen einräumt.</span><span class="sxs-lookup"><span data-stu-id="ac9af-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="ac9af-107">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="ac9af-107">**Solution**</span></span>

<span data-ttu-id="ac9af-108">Stellen Sie sicher, dass der Mandantenadministrator dem Benutzer, der die Umgebung erstellt, eine gültige Power Apps-P2-Lizenz zugewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="ac9af-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="ac9af-109">Folgende Microsoft Dynamics-Servicepläne bieten Berechtigungen zum Erstellen von Umgebungen:</span><span class="sxs-lookup"><span data-stu-id="ac9af-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="ac9af-110">Gesamtprodukt-Lagermengeneinheit (SKU)</span><span class="sxs-lookup"><span data-stu-id="ac9af-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="ac9af-111">Power Apps P2-Serviceplan</span><span class="sxs-lookup"><span data-stu-id="ac9af-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="ac9af-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="ac9af-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="ac9af-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ac9af-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="ac9af-114">Microsoft Dynamics 365-Plan – Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="ac9af-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="ac9af-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ac9af-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="ac9af-116">Beachten Sie, dass verschiedene Microsoft Office-SKUs auch das Recht bereitstellen, zusammen mit den eigenständigen Power Apps Plan 2 SKUs.</span><span class="sxs-lookup"><span data-stu-id="ac9af-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="ac9af-117">Der wichtige Aspekt ist, dass einer dieser SKUs vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="ac9af-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="ac9af-118">Gehe zu [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="ac9af-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="ac9af-119">Erstellen Sie die Umgebungen, indem Sie in die Anweisungen befolgen in [Human Resources bereitstellen](/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="ac9af-119">Create the environments by following the instructions in [Provision Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]