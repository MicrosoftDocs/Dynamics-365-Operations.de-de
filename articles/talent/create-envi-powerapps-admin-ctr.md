---
title: "Erstellen einer Umgebung im PowerApps Admin Center nicht möglich"
description: "In diesem Thema wird erklärt, was zu tun ist, wenn der Administrator keine Umgebung im Microsoft PowerApps Admin Center erstellen kann."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: de-de
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="1dadc-103">Erstellen einer Umgebung im PowerApps Admin Center nicht möglich</span><span class="sxs-lookup"><span data-stu-id="1dadc-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1dadc-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="1dadc-104">**Issue**</span></span>

- <span data-ttu-id="1dadc-105">Der Mandanten-/Umgebungsadministrator kann keine Umgebung im Microsoft PowerApps Admin Center erstellen.</span><span class="sxs-lookup"><span data-stu-id="1dadc-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="1dadc-106">Eine Lizenz, die Benutzern das Recht zum Ausführen des Umgebungserstellungsschritts gibt, ist dem Benutzer, der diesen Schritt ausführt, nicht direkt zugewiesen worden.</span><span class="sxs-lookup"><span data-stu-id="1dadc-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="1dadc-107">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="1dadc-107">**Solution**</span></span>

<span data-ttu-id="1dadc-108">Stellen Sie sicher, dass der Mandantenadministrator eine gültige PowerApps P2-Lizenz direkt dem Benutzer zugewiesen hat, der den Umgebungserstellungsschritt ausführt.</span><span class="sxs-lookup"><span data-stu-id="1dadc-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="1dadc-109">Hier sind die Microsoft Dynamics-Servicepläne, die Ihnen dieses Recht gewähren.</span><span class="sxs-lookup"><span data-stu-id="1dadc-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="1dadc-110">Gesamtprodukt-Lagermengeneinheit (SKU)</span><span class="sxs-lookup"><span data-stu-id="1dadc-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="1dadc-111">PowerApps P2-Serviceplan</span><span class="sxs-lookup"><span data-stu-id="1dadc-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="1dadc-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="1dadc-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="1dadc-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="1dadc-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="1dadc-114">Microsoft Dynamics 365-Plan – Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="1dadc-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="1dadc-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="1dadc-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="1dadc-116">Beachten Sie, dass verschiedene Microsoft Office-SKUs auch das Recht bereitstellen, zusammen mit den eigenständigen PowerApps Plan 2-SKUs.</span><span class="sxs-lookup"><span data-stu-id="1dadc-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="1dadc-117">Der wichtige Aspekt ist, dass einer dieser SKUs vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="1dadc-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="1dadc-118">Gehe zu [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="1dadc-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="1dadc-119">Erstellen Sie die Umgebungen, indem Sie in die Anweisungen befolgen in [Talent bereitstellen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="1dadc-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

