---
title: Erstellen einer Umgebung im Power Apps Admin Center nicht möglich
description: In diesem Artikel wird erklärt, was zu tun ist, wenn der Administrator keine Umgebung im Microsoft Power Apps Admin Center erstellen kann.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418653"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="521e0-103">Erstellen einer Umgebung im Power Apps Admin Center nicht möglich</span><span class="sxs-lookup"><span data-stu-id="521e0-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="521e0-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="521e0-104">**Issue**</span></span>

- <span data-ttu-id="521e0-105">Der Mandanten-/Umgebungsadministrator kann keine Umgebung im Microsoft Power Apps Admin Center erstellen.</span><span class="sxs-lookup"><span data-stu-id="521e0-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="521e0-106">Eine Lizenz, die Benutzern das Recht zum Ausführen des Umgebungserstellungsschritts gibt, ist dem Benutzer, der diesen Schritt ausführt, nicht direkt zugewiesen worden.</span><span class="sxs-lookup"><span data-stu-id="521e0-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="521e0-107">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="521e0-107">**Solution**</span></span>

<span data-ttu-id="521e0-108">Stellen Sie sicher, dass der Mandantenadministrator eine gültige Power Apps P2-Lizenz direkt dem Benutzer zugewiesen hat, der den Umgebungserstellungsschritt ausführt.</span><span class="sxs-lookup"><span data-stu-id="521e0-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="521e0-109">Hier sind die Microsoft Dynamics-Servicepläne, die dieses Recht gewähren.</span><span class="sxs-lookup"><span data-stu-id="521e0-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="521e0-110">Gesamtprodukt-Lagermengeneinheit (SKU)</span><span class="sxs-lookup"><span data-stu-id="521e0-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="521e0-111">Power Apps P2-Serviceplan</span><span class="sxs-lookup"><span data-stu-id="521e0-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="521e0-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="521e0-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="521e0-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="521e0-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="521e0-114">Microsoft Dynamics 365-Plan – Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="521e0-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="521e0-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="521e0-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="521e0-116">Beachten Sie, dass verschiedene Microsoft Office-SKUs auch das Recht bereitstellen, zusammen mit den eigenständigen Power Apps Plan 2 SKUs.</span><span class="sxs-lookup"><span data-stu-id="521e0-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="521e0-117">Der wichtige Aspekt ist, dass einer dieser SKUs vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="521e0-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="521e0-118">Gehe zu [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="521e0-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="521e0-119">Erstellen Sie die Umgebungen, indem Sie in die Anweisungen befolgen in [Human Resources bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="521e0-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
