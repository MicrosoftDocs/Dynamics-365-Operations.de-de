---
title: Erstellen einer Umgebung im Power Apps Admin Center nicht möglich
description: In diesem Thema wird erklärt, was zu tun ist, wenn der Administrator keine Umgebung im Microsoft Power Apps Admin Center erstellen kann.
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
ms.openlocfilehash: 7a66b7624655aaf976aaa63b2626f65c54d0ea38
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898812"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="05b8d-103">Erstellen einer Umgebung im Power Apps Admin Center nicht möglich</span><span class="sxs-lookup"><span data-stu-id="05b8d-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="05b8d-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="05b8d-104">**Issue**</span></span>

- <span data-ttu-id="05b8d-105">Der Mandanten-/Umgebungsadministrator kann keine Umgebung im Microsoft Power Apps Admin Center erstellen.</span><span class="sxs-lookup"><span data-stu-id="05b8d-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="05b8d-106">Eine Lizenz, die Benutzern das Recht zum Ausführen des Umgebungserstellungsschritts gibt, ist dem Benutzer, der diesen Schritt ausführt, nicht direkt zugewiesen worden.</span><span class="sxs-lookup"><span data-stu-id="05b8d-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="05b8d-107">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="05b8d-107">**Solution**</span></span>

<span data-ttu-id="05b8d-108">Stellen Sie sicher, dass der Mandantenadministrator eine gültige Power Apps P2-Lizenz direkt dem Benutzer zugewiesen hat, der den Umgebungserstellungsschritt ausführt.</span><span class="sxs-lookup"><span data-stu-id="05b8d-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="05b8d-109">Hier sind die Microsoft Dynamics-Servicepläne, die dieses Recht gewähren.</span><span class="sxs-lookup"><span data-stu-id="05b8d-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="05b8d-110">Gesamtprodukt-Lagermengeneinheit (SKU)</span><span class="sxs-lookup"><span data-stu-id="05b8d-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="05b8d-111">Power Apps P2-Serviceplan</span><span class="sxs-lookup"><span data-stu-id="05b8d-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="05b8d-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="05b8d-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="05b8d-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="05b8d-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="05b8d-114">Microsoft Dynamics 365-Plan – Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="05b8d-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="05b8d-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="05b8d-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="05b8d-116">Beachten Sie, dass verschiedene Microsoft Office-SKUs auch das Recht bereitstellen, zusammen mit den eigenständigen Power Apps Plan 2 SKUs.</span><span class="sxs-lookup"><span data-stu-id="05b8d-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="05b8d-117">Der wichtige Aspekt ist, dass einer dieser SKUs vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="05b8d-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="05b8d-118">Gehe zu [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="05b8d-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="05b8d-119">Erstellen Sie die Umgebungen, indem Sie in die Anweisungen befolgen in [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="05b8d-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
