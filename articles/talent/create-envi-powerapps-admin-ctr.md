---
title: Erstellen einer Umgebung im PowerApps Admin Center nicht möglich
description: In diesem Thema wird erklärt, was zu tun ist, wenn der Administrator keine Umgebung im Microsoft PowerApps Admin Center erstellen kann.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 96119ca869cbbb15ed8d8d5d0fe3b0f94b5f36cc
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742841"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="18da7-103">Eine Umgebung im PowerApps Admin Center kann nicht erstellt werden</span><span class="sxs-lookup"><span data-stu-id="18da7-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="18da7-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="18da7-104">**Issue**</span></span>

- <span data-ttu-id="18da7-105">Der Mandanten-/Umgebungsadministrator kann keine Umgebung im Microsoft PowerApps Admin Center erstellen.</span><span class="sxs-lookup"><span data-stu-id="18da7-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="18da7-106">Eine Lizenz, die Benutzern das Recht zum Ausführen des Umgebungserstellungsschritts gibt, ist dem Benutzer, der diesen Schritt ausführt, nicht direkt zugewiesen worden.</span><span class="sxs-lookup"><span data-stu-id="18da7-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="18da7-107">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="18da7-107">**Solution**</span></span>

<span data-ttu-id="18da7-108">Stellen Sie sicher, dass der Mandantenadministrator eine gültige PowerApps P2-Lizenz direkt dem Benutzer zugewiesen hat, der den Umgebungserstellungsschritt ausführt.</span><span class="sxs-lookup"><span data-stu-id="18da7-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="18da7-109">Hier sind die Microsoft Dynamics-Servicepläne, die dieses Recht gewähren.</span><span class="sxs-lookup"><span data-stu-id="18da7-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="18da7-110">Gesamtprodukt-Lagermengeneinheit (SKU)</span><span class="sxs-lookup"><span data-stu-id="18da7-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="18da7-111">PowerApps P2-Serviceplan</span><span class="sxs-lookup"><span data-stu-id="18da7-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="18da7-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="18da7-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="18da7-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="18da7-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="18da7-114">Microsoft Dynamics 365-Plan – Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="18da7-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="18da7-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="18da7-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="18da7-116">Beachten Sie, dass verschiedene Microsoft Office-SKUs auch das Recht bereitstellen, zusammen mit den eigenständigen PowerApps Plan 2-SKUs.</span><span class="sxs-lookup"><span data-stu-id="18da7-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="18da7-117">Der wichtige Aspekt ist, dass einer dieser SKUs vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="18da7-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="18da7-118">Gehe zu [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="18da7-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="18da7-119">Erstellen Sie die Umgebungen, indem Sie in die Anweisungen befolgen in [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="18da7-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
