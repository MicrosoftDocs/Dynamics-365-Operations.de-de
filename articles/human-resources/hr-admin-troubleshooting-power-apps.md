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
ms.openlocfilehash: f4c75706183a3d6c961852395e464d46ba3ec1f2
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009114"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="dcc25-103">Erstellen einer Umgebung im Power Apps Admin Center nicht möglich</span><span class="sxs-lookup"><span data-stu-id="dcc25-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="dcc25-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="dcc25-104">**Issue**</span></span>

- <span data-ttu-id="dcc25-105">Der Mandanten-/Umgebungsadministrator kann keine Umgebung im Microsoft Power Apps Admin Center erstellen.</span><span class="sxs-lookup"><span data-stu-id="dcc25-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="dcc25-106">Eine Lizenz, die Benutzern das Recht zum Ausführen des Umgebungserstellungsschritts gibt, ist dem Benutzer, der diesen Schritt ausführt, nicht direkt zugewiesen worden.</span><span class="sxs-lookup"><span data-stu-id="dcc25-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="dcc25-107">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="dcc25-107">**Solution**</span></span>

<span data-ttu-id="dcc25-108">Stellen Sie sicher, dass der Mandantenadministrator eine gültige Power Apps P2-Lizenz direkt dem Benutzer zugewiesen hat, der den Umgebungserstellungsschritt ausführt.</span><span class="sxs-lookup"><span data-stu-id="dcc25-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="dcc25-109">Hier sind die Microsoft Dynamics-Servicepläne, die dieses Recht gewähren.</span><span class="sxs-lookup"><span data-stu-id="dcc25-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="dcc25-110">Gesamtprodukt-Lagermengeneinheit (SKU)</span><span class="sxs-lookup"><span data-stu-id="dcc25-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="dcc25-111">Power Apps P2-Serviceplan</span><span class="sxs-lookup"><span data-stu-id="dcc25-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="dcc25-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="dcc25-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="dcc25-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="dcc25-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="dcc25-114">Microsoft Dynamics 365-Plan – Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="dcc25-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="dcc25-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="dcc25-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="dcc25-116">Beachten Sie, dass verschiedene Microsoft Office-SKUs auch das Recht bereitstellen, zusammen mit den eigenständigen Power Apps Plan 2 SKUs.</span><span class="sxs-lookup"><span data-stu-id="dcc25-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="dcc25-117">Der wichtige Aspekt ist, dass einer dieser SKUs vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="dcc25-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="dcc25-118">Gehe zu [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="dcc25-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="dcc25-119">Erstellen Sie die Umgebungen, indem Sie in die Anweisungen befolgen in [Human Resources bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="dcc25-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
