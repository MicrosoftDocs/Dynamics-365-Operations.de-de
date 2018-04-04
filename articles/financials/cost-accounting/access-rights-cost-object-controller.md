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
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6403aabb6b029807b42ab1ccb11756dcb0dda5dc
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="85d30-103">Zugriffsrechte eines Kostenobjekt-Controllers</span><span class="sxs-lookup"><span data-stu-id="85d30-103">Access rights of a cost object controller</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="85d30-104">Der Arbeitsbereich **Kostensteuerung** ist ein zentraler Punkt, in dem Manager die Leistung der Kostenobjekte anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="85d30-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="85d30-105">In diesem Arbeitsbereich können Manager Kostenrechnungsdaten nutzen, auch wenn sie keine Kostenbuchhalter sind.</span><span class="sxs-lookup"><span data-stu-id="85d30-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="85d30-106">Aus Sicherheitsgründen solle Managern ermöglicht werden, nur die Kostenrechnungsdaten anzuzeigen, die den bestimmten Kostenobjekten zugeordnet sind, für die sie zuständig sind.</span><span class="sxs-lookup"><span data-stu-id="85d30-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="85d30-107">Es gibt vier eindeutige Rollen in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="85d30-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="85d30-108">Rollenname</span><span class="sxs-lookup"><span data-stu-id="85d30-108">Role name</span></span>               | <span data-ttu-id="85d30-109">Lizenz</span><span class="sxs-lookup"><span data-stu-id="85d30-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="85d30-110">Kostenrechnungs-Manager</span><span class="sxs-lookup"><span data-stu-id="85d30-110">Cost accounting manager</span></span> | <span data-ttu-id="85d30-111">Aktivität</span><span class="sxs-lookup"><span data-stu-id="85d30-111">Activity</span></span>     |
| <span data-ttu-id="85d30-112">Kostenbuchhalter</span><span class="sxs-lookup"><span data-stu-id="85d30-112">Cost accountant</span></span>         | <span data-ttu-id="85d30-113">Operations</span><span class="sxs-lookup"><span data-stu-id="85d30-113">Operations</span></span>   |
| <span data-ttu-id="85d30-114">Sachbearbeiter Kostenbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="85d30-114">Cost accountant clerk</span></span>   | <span data-ttu-id="85d30-115">Operations</span><span class="sxs-lookup"><span data-stu-id="85d30-115">Operations</span></span>   |
| <span data-ttu-id="85d30-116">Kostenobjekt-Controller</span><span class="sxs-lookup"><span data-stu-id="85d30-116">Cost object controller</span></span>  | <span data-ttu-id="85d30-117">Teammitglieder</span><span class="sxs-lookup"><span data-stu-id="85d30-117">Team members</span></span> |

<span data-ttu-id="85d30-118">In diesem Thema wird erläutert, wie einem Manager die Rolle **Kostenobjekt-Controller** zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="85d30-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="85d30-119">Wenn einem Manager die Rolle **Kostenobjekt-Controller** zugewiesen wird, kann der Manager die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="85d30-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="85d30-120">Zugriff auf den Arbeitsbereich **Kostensteuerung** (im Client).</span><span class="sxs-lookup"><span data-stu-id="85d30-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="85d30-121">Detailinformationen zu den und Ansichtszugriff auf die Seiten, die die Drillthrough-Erfahrung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="85d30-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="85d30-122">Zugriff auf den Arbeitsbereich **Kostensteuerung** (im der Mobilanwendung).</span><span class="sxs-lookup"><span data-stu-id="85d30-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="85d30-123">Die Rolle **Kostenobjekt-Controller** steuert nicht, auf welche Kostenobjekte der Benutzer zugreifen und Daten dazu anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="85d30-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="85d30-124">Sicherheit auf Positionsebene wird über Dimensionshierarchien und die Zugriffslistenhierarchie bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="85d30-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="85d30-125">Zugriffsrechte gewähren</span><span class="sxs-lookup"><span data-stu-id="85d30-125">Grant access rights</span></span>
<span data-ttu-id="85d30-126">Das folgende Beispiel zeigt, wie eine Dimensionshierarchie aussehen kann.</span><span class="sxs-lookup"><span data-stu-id="85d30-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="85d30-127">**Dimensionshierarchiedetails**</span><span class="sxs-lookup"><span data-stu-id="85d30-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="85d30-128">Dimensionshierarchiename</span><span class="sxs-lookup"><span data-stu-id="85d30-128">Dimension hierarchy name</span></span> | <span data-ttu-id="85d30-129">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="85d30-129">Dimension</span></span>    | <span data-ttu-id="85d30-130">Dimensionshierarchie-Typname</span><span class="sxs-lookup"><span data-stu-id="85d30-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="85d30-131">Zugriffslistenhierarchie</span><span class="sxs-lookup"><span data-stu-id="85d30-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="85d30-132">Organisation</span><span class="sxs-lookup"><span data-stu-id="85d30-132">Organization</span></span>             | <span data-ttu-id="85d30-133">Kostenstellen</span><span class="sxs-lookup"><span data-stu-id="85d30-133">Cost centers</span></span> | <span data-ttu-id="85d30-134">Dimensionsklassifizierungshierarchie</span><span class="sxs-lookup"><span data-stu-id="85d30-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="85d30-135">**Ja**</span><span class="sxs-lookup"><span data-stu-id="85d30-135">**Yes**</span></span>               |

<span data-ttu-id="85d30-136">Sie können das Inforegister **Benutzer** im Hierarchie-Designer verwenden, um mindestens eine Benutzerkennungen auf jedem Knoten einzufügen.</span><span class="sxs-lookup"><span data-stu-id="85d30-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="85d30-137">Benutzer</span><span class="sxs-lookup"><span data-stu-id="85d30-137">Users</span></span>            | <span data-ttu-id="85d30-138">Dimensionsmitgliedsbereiche</span><span class="sxs-lookup"><span data-stu-id="85d30-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="85d30-139">**Knoten**</span><span class="sxs-lookup"><span data-stu-id="85d30-139">**Nodes**</span></span>                         | <span data-ttu-id="85d30-140">**Benutzerkennung**</span><span class="sxs-lookup"><span data-stu-id="85d30-140">**User ID**</span></span>      | <span data-ttu-id="85d30-141">**Ausgangsdimensionsmitglied**</span><span class="sxs-lookup"><span data-stu-id="85d30-141">**From dimension member**</span></span> | <span data-ttu-id="85d30-142">**Zieldimensionsmitglied**</span><span class="sxs-lookup"><span data-stu-id="85d30-142">**To dimension member**</span></span> |
| <span data-ttu-id="85d30-143">Organisation</span><span class="sxs-lookup"><span data-stu-id="85d30-143">Organization</span></span>                      | <span data-ttu-id="85d30-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="85d30-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="85d30-145">&nbsp;&nbsp;Verwaltung</span><span class="sxs-lookup"><span data-stu-id="85d30-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="85d30-146">April</span><span class="sxs-lookup"><span data-stu-id="85d30-146">April</span></span>            |                           |                         |
| <span data-ttu-id="85d30-147">&nbsp;&nbsp;&nbsp;&nbsp;Finanzen</span><span class="sxs-lookup"><span data-stu-id="85d30-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="85d30-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="85d30-148">Alicia</span></span>           | <span data-ttu-id="85d30-149">CC002</span><span class="sxs-lookup"><span data-stu-id="85d30-149">CC002</span></span>                     | <span data-ttu-id="85d30-150">CC003</span><span class="sxs-lookup"><span data-stu-id="85d30-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="85d30-151">CC007</span><span class="sxs-lookup"><span data-stu-id="85d30-151">CC007</span></span>                     | <span data-ttu-id="85d30-152">CC007</span><span class="sxs-lookup"><span data-stu-id="85d30-152">CC007</span></span>                   |
| <span data-ttu-id="85d30-153">&nbsp;&nbsp;&nbsp;&nbsp;Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="85d30-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="85d30-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="85d30-154">Arnie</span></span>            | <span data-ttu-id="85d30-155">CC001</span><span class="sxs-lookup"><span data-stu-id="85d30-155">CC001</span></span>                     | <span data-ttu-id="85d30-156">CC001</span><span class="sxs-lookup"><span data-stu-id="85d30-156">CC001</span></span>                   |
| <span data-ttu-id="85d30-157">&nbsp;&nbsp;Produktion</span><span class="sxs-lookup"><span data-stu-id="85d30-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="85d30-158">David</span><span class="sxs-lookup"><span data-stu-id="85d30-158">David</span></span>            |                           |                         |
| <span data-ttu-id="85d30-159">&nbsp;&nbsp;&nbsp;&nbsp;Verpackung</span><span class="sxs-lookup"><span data-stu-id="85d30-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="85d30-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="85d30-160">Ellen</span></span>            | <span data-ttu-id="85d30-161">CC005</span><span class="sxs-lookup"><span data-stu-id="85d30-161">CC005</span></span>                     | <span data-ttu-id="85d30-162">CC005</span><span class="sxs-lookup"><span data-stu-id="85d30-162">CC005</span></span>                   |
| <span data-ttu-id="85d30-163">&nbsp;&nbsp;&nbsp;&nbsp;Montage</span><span class="sxs-lookup"><span data-stu-id="85d30-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="85d30-164">Chris</span><span class="sxs-lookup"><span data-stu-id="85d30-164">Chris</span></span>            | <span data-ttu-id="85d30-165">CC006</span><span class="sxs-lookup"><span data-stu-id="85d30-165">CC006</span></span>                     | <span data-ttu-id="85d30-166">CC006</span><span class="sxs-lookup"><span data-stu-id="85d30-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="85d30-167">Kostenbuchhalter sollten der höchsten Ebene der Hierarchie zugewiesen werden, damit sie alle Einträge in der Kostenrechnung anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="85d30-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="85d30-168">Bevor die Zugriffslistenhierarchie und deren Sicherheitseinstellungen angewendet werden können, muss die Option **Anzeigezugriff für Kostenobjektdimensionsmitglieder zulassen** auf **Ja** in der Registerkarte **Allgemein** der Seite **Kostenrechnungsparameter** (**Kostenrechnung** > **Einstellungen** > **Parameter**) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="85d30-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="85d30-169">Die Einstellungen für die Zugriffslistenhierarchie werden verwendet, um die Daten zu steuern, die in den folgenden Bereichen angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="85d30-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="85d30-170">Arbeitsbereich **Kostensteuerung** (im Client)</span><span class="sxs-lookup"><span data-stu-id="85d30-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="85d30-171">Daten auf den Seiten, die für den Drillthrough verwendet werden</span><span class="sxs-lookup"><span data-stu-id="85d30-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="85d30-172">Arbeitsbereich **Kostensteuerung** (in der Mobilanwendung):</span><span class="sxs-lookup"><span data-stu-id="85d30-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="85d30-173">Salden in Karten</span><span class="sxs-lookup"><span data-stu-id="85d30-173">Balances in cards</span></span>

- <span data-ttu-id="85d30-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="85d30-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="85d30-175">Daten, die in den BI-Visualisierungen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="85d30-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="85d30-176">Data Power BI Visualisierungen, die im Microsoft Dynamics 365 for Finance and Operations Client eingebettet werden</span><span class="sxs-lookup"><span data-stu-id="85d30-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="85d30-177">Bevor sich die Zugriffslistenhierarchie auf Daten in Power BI auswirken kann, müssen die Zugriffslistenhierarchie und Sicherheit auf Positionsebene in Power BI zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="85d30-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="85d30-178">Weitere Informationen finden Sie unter [Sicherheit für das Kostenrechnungs-Inhaltspack einrichten](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="85d30-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="85d30-179">In diesem Thema werden die Voraussetzungen behandelt, die erfüllt sein müssen, bevor Sie den Arbeitsbereich **Kostensteuerung** verwenden können.</span><span class="sxs-lookup"><span data-stu-id="85d30-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="85d30-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85d30-180">See also</span></span>

- [<span data-ttu-id="85d30-181">Kostensteuerungs-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="85d30-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="85d30-182">Dimensionshierarchie</span><span class="sxs-lookup"><span data-stu-id="85d30-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="85d30-183">Sicherheit für Kostensteuerungs-Inhaltspack einrichten</span><span class="sxs-lookup"><span data-stu-id="85d30-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

