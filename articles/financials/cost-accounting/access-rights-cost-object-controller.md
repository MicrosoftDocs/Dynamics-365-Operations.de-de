---
title: "Zugriffsrechte für Kostenobjekt-Controller definieren"
description: "Dieses Thema bietet Informationen über Zugriffsrechte für Kostenobjekt-Controller."
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2ba38ddc5c717df29462e4316dc5045d0eef8c1a
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="8db89-103">Zugriffsrechte eines Kostenobjekt-Controllers</span><span class="sxs-lookup"><span data-stu-id="8db89-103">Access rights of a cost object controller</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8db89-104">Der Arbeitsbereich **Kostensteuerung** ist ein zentraler Punkt, in dem Manager die Leistung der Kostenobjekte anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="8db89-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="8db89-105">In diesem Arbeitsbereich können Manager Kostenrechnungsdaten nutzen, auch wenn sie keine Kostenbuchhalter sind.</span><span class="sxs-lookup"><span data-stu-id="8db89-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="8db89-106">Aus Sicherheitsgründen solle Managern ermöglicht werden, nur die Kostenrechnungsdaten anzuzeigen, die den bestimmten Kostenobjekten zugeordnet sind, für die sie zuständig sind.</span><span class="sxs-lookup"><span data-stu-id="8db89-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="8db89-107">Es gibt vier eindeutige Rollen in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="8db89-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="8db89-108">Rollenname</span><span class="sxs-lookup"><span data-stu-id="8db89-108">Role name</span></span>               | <span data-ttu-id="8db89-109">Lizenz</span><span class="sxs-lookup"><span data-stu-id="8db89-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="8db89-110">Kostenrechnungs-Manager</span><span class="sxs-lookup"><span data-stu-id="8db89-110">Cost accounting manager</span></span> | <span data-ttu-id="8db89-111">Aktivität</span><span class="sxs-lookup"><span data-stu-id="8db89-111">Activity</span></span>     |
| <span data-ttu-id="8db89-112">Kostenbuchhalter</span><span class="sxs-lookup"><span data-stu-id="8db89-112">Cost accountant</span></span>         | <span data-ttu-id="8db89-113">Operations</span><span class="sxs-lookup"><span data-stu-id="8db89-113">Operations</span></span>   |
| <span data-ttu-id="8db89-114">Sachbearbeiter Kostenbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="8db89-114">Cost accountant clerk</span></span>   | <span data-ttu-id="8db89-115">Operations</span><span class="sxs-lookup"><span data-stu-id="8db89-115">Operations</span></span>   |
| <span data-ttu-id="8db89-116">Kostenobjekt-Controller</span><span class="sxs-lookup"><span data-stu-id="8db89-116">Cost object controller</span></span>  | <span data-ttu-id="8db89-117">Teammitglieder</span><span class="sxs-lookup"><span data-stu-id="8db89-117">Team members</span></span> |

<span data-ttu-id="8db89-118">In diesem Thema wird erläutert, wie einem Manager die Rolle **Kostenobjekt-Controller** zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8db89-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="8db89-119">Wenn einem Manager die Rolle **Kostenobjekt-Controller** zugewiesen wird, kann der Manager die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="8db89-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="8db89-120">Zugriff auf den Arbeitsbereich **Kostensteuerung** (im Client).</span><span class="sxs-lookup"><span data-stu-id="8db89-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="8db89-121">Detailinformationen zu den und Ansichtszugriff auf die Seiten, die die Drillthrough-Erfahrung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8db89-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="8db89-122">Zugriff auf den Arbeitsbereich **Kostensteuerung** (im der Mobilanwendung).</span><span class="sxs-lookup"><span data-stu-id="8db89-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="8db89-123">Die Rolle **Kostenobjekt-Controller** steuert nicht, auf welche Kostenobjekte der Benutzer zugreifen und Daten dazu anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="8db89-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="8db89-124">Sicherheit auf Positionsebene wird über Dimensionshierarchien und die Zugriffslistenhierarchie bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8db89-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="8db89-125">Zugriffsrechte gewähren</span><span class="sxs-lookup"><span data-stu-id="8db89-125">Grant access rights</span></span>
<span data-ttu-id="8db89-126">Das folgende Beispiel zeigt, wie eine Dimensionshierarchie aussehen kann.</span><span class="sxs-lookup"><span data-stu-id="8db89-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="8db89-127">**Dimensionshierarchiedetails**</span><span class="sxs-lookup"><span data-stu-id="8db89-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="8db89-128">Dimensionshierarchiename</span><span class="sxs-lookup"><span data-stu-id="8db89-128">Dimension hierarchy name</span></span> | <span data-ttu-id="8db89-129">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="8db89-129">Dimension</span></span>    | <span data-ttu-id="8db89-130">Dimensionshierarchie-Typname</span><span class="sxs-lookup"><span data-stu-id="8db89-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="8db89-131">Zugriffslistenhierarchie</span><span class="sxs-lookup"><span data-stu-id="8db89-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="8db89-132">Organisation</span><span class="sxs-lookup"><span data-stu-id="8db89-132">Organization</span></span>             | <span data-ttu-id="8db89-133">Kostenstellen</span><span class="sxs-lookup"><span data-stu-id="8db89-133">Cost centers</span></span> | <span data-ttu-id="8db89-134">Dimensionsklassifizierungshierarchie</span><span class="sxs-lookup"><span data-stu-id="8db89-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="8db89-135">**Ja**</span><span class="sxs-lookup"><span data-stu-id="8db89-135">**Yes**</span></span>               |

<span data-ttu-id="8db89-136">Sie können das Inforegister **Benutzer** im Hierarchie-Designer verwenden, um mindestens eine Benutzerkennungen auf jedem Knoten einzufügen.</span><span class="sxs-lookup"><span data-stu-id="8db89-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="8db89-137">Benutzer</span><span class="sxs-lookup"><span data-stu-id="8db89-137">Users</span></span>            | <span data-ttu-id="8db89-138">Dimensionsmitgliedsbereiche</span><span class="sxs-lookup"><span data-stu-id="8db89-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="8db89-139">**Knoten**</span><span class="sxs-lookup"><span data-stu-id="8db89-139">**Nodes**</span></span>                         | <span data-ttu-id="8db89-140">**Benutzerkennung**</span><span class="sxs-lookup"><span data-stu-id="8db89-140">**User ID**</span></span>      | <span data-ttu-id="8db89-141">**Ausgangsdimensionsmitglied**</span><span class="sxs-lookup"><span data-stu-id="8db89-141">**From dimension member**</span></span> | <span data-ttu-id="8db89-142">**Zieldimensionsmitglied**</span><span class="sxs-lookup"><span data-stu-id="8db89-142">**To dimension member**</span></span> |
| <span data-ttu-id="8db89-143">Organisation</span><span class="sxs-lookup"><span data-stu-id="8db89-143">Organization</span></span>                      | <span data-ttu-id="8db89-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="8db89-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="8db89-145">&nbsp;&nbsp;Verwaltung</span><span class="sxs-lookup"><span data-stu-id="8db89-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="8db89-146">April</span><span class="sxs-lookup"><span data-stu-id="8db89-146">April</span></span>            |                           |                         |
| <span data-ttu-id="8db89-147">&nbsp;&nbsp;&nbsp;&nbsp;Finanzen</span><span class="sxs-lookup"><span data-stu-id="8db89-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="8db89-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="8db89-148">Alicia</span></span>           | <span data-ttu-id="8db89-149">CC002</span><span class="sxs-lookup"><span data-stu-id="8db89-149">CC002</span></span>                     | <span data-ttu-id="8db89-150">CC003</span><span class="sxs-lookup"><span data-stu-id="8db89-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="8db89-151">CC007</span><span class="sxs-lookup"><span data-stu-id="8db89-151">CC007</span></span>                     | <span data-ttu-id="8db89-152">CC007</span><span class="sxs-lookup"><span data-stu-id="8db89-152">CC007</span></span>                   |
| <span data-ttu-id="8db89-153">&nbsp;&nbsp;&nbsp;&nbsp;Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8db89-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="8db89-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="8db89-154">Arnie</span></span>            | <span data-ttu-id="8db89-155">CC001</span><span class="sxs-lookup"><span data-stu-id="8db89-155">CC001</span></span>                     | <span data-ttu-id="8db89-156">CC001</span><span class="sxs-lookup"><span data-stu-id="8db89-156">CC001</span></span>                   |
| <span data-ttu-id="8db89-157">&nbsp;&nbsp;Produktion</span><span class="sxs-lookup"><span data-stu-id="8db89-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="8db89-158">David</span><span class="sxs-lookup"><span data-stu-id="8db89-158">David</span></span>            |                           |                         |
| <span data-ttu-id="8db89-159">&nbsp;&nbsp;&nbsp;&nbsp;Verpackung</span><span class="sxs-lookup"><span data-stu-id="8db89-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="8db89-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="8db89-160">Ellen</span></span>            | <span data-ttu-id="8db89-161">CC005</span><span class="sxs-lookup"><span data-stu-id="8db89-161">CC005</span></span>                     | <span data-ttu-id="8db89-162">CC005</span><span class="sxs-lookup"><span data-stu-id="8db89-162">CC005</span></span>                   |
| <span data-ttu-id="8db89-163">&nbsp;&nbsp;&nbsp;&nbsp;Montage</span><span class="sxs-lookup"><span data-stu-id="8db89-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="8db89-164">Chris</span><span class="sxs-lookup"><span data-stu-id="8db89-164">Chris</span></span>            | <span data-ttu-id="8db89-165">CC006</span><span class="sxs-lookup"><span data-stu-id="8db89-165">CC006</span></span>                     | <span data-ttu-id="8db89-166">CC006</span><span class="sxs-lookup"><span data-stu-id="8db89-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="8db89-167">Kostenbuchhalter sollten der höchsten Ebene der Hierarchie zugewiesen werden, damit sie alle Einträge in der Kostenrechnung anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="8db89-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="8db89-168">Bevor die Zugriffslistenhierarchie und deren Sicherheitseinstellungen angewendet werden können, muss die Option **Anzeigezugriff für Kostenobjektdimensionsmitglieder zulassen** auf **Ja** in der Registerkarte **Allgemein** der Seite **Kostenrechnungsparameter** (**Kostenrechnung** > **Einstellungen** > **Parameter**) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8db89-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="8db89-169">Die Einstellungen für die Zugriffslistenhierarchie werden verwendet, um die Daten zu steuern, die in den folgenden Bereichen angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="8db89-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="8db89-170">Arbeitsbereich **Kostensteuerung** (im Client)</span><span class="sxs-lookup"><span data-stu-id="8db89-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="8db89-171">Daten auf den Seiten, die für den Drillthrough verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8db89-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="8db89-172">Arbeitsbereich **Kostensteuerung** (in der Mobilanwendung):</span><span class="sxs-lookup"><span data-stu-id="8db89-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="8db89-173">Salden in Karten</span><span class="sxs-lookup"><span data-stu-id="8db89-173">Balances in cards</span></span>

- <span data-ttu-id="8db89-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="8db89-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="8db89-175">Daten, die in den BI-Visualisierungen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="8db89-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="8db89-176">Data Power BI-Visualisierungen, die im Client der Enterprise edition von Microsoft Dynamics 365 für Finance and Operations eingebettet werden</span><span class="sxs-lookup"><span data-stu-id="8db89-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="8db89-177">Bevor sich die Zugriffslistenhierarchie auf Daten in Power BI auswirken kann, müssen die Zugriffslistenhierarchie und Sicherheit auf Positionsebene in Power BI zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="8db89-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="8db89-178">Weitere Informationen finden Sie unter [Sicherheit für das Kostenrechnungs-Inhaltspack einrichten](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="8db89-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="8db89-179">In diesem Thema werden die Voraussetzungen behandelt, die erfüllt sein müssen, bevor Sie den Arbeitsbereich **Kostensteuerung** verwenden können.</span><span class="sxs-lookup"><span data-stu-id="8db89-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="8db89-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8db89-180">See also</span></span>

- [<span data-ttu-id="8db89-181">Kostensteuerungs-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="8db89-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="8db89-182">Dimensionshierarchie</span><span class="sxs-lookup"><span data-stu-id="8db89-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="8db89-183">Sicherheit für Kostensteuerungs-Inhaltspack einrichten</span><span class="sxs-lookup"><span data-stu-id="8db89-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

