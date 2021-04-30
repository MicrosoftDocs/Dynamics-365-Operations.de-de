---
title: Zugriffsrechte für Kostenobjekt-Controller
description: Dieses Thema bietet Informationen über Zugriffsrechte für Kostenobjekt-Controller.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fa8faf0f0f45f901151b3b20a1792b3d8f264fa6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897623"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="05f0f-103">Zugriffsrechte für Kostenobjekt-Controller</span><span class="sxs-lookup"><span data-stu-id="05f0f-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05f0f-104">Der Arbeitsbereich **Kostensteuerung** ist ein zentraler Punkt, in dem Manager die Leistung der Kostenobjekte anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="05f0f-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="05f0f-105">In diesem Arbeitsbereich können Manager Kostenrechnungsdaten nutzen, auch wenn sie keine Kostenbuchhalter sind.</span><span class="sxs-lookup"><span data-stu-id="05f0f-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="05f0f-106">Aus Sicherheitsgründen solle Managern ermöglicht werden, nur die Kostenrechnungsdaten anzuzeigen, die den bestimmten Kostenobjekten zugeordnet sind, für die sie zuständig sind.</span><span class="sxs-lookup"><span data-stu-id="05f0f-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="05f0f-107">Es gibt vier eindeutige Rollen in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="05f0f-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="05f0f-108">Rollenname</span><span class="sxs-lookup"><span data-stu-id="05f0f-108">Role name</span></span>               | <span data-ttu-id="05f0f-109">Lizenz</span><span class="sxs-lookup"><span data-stu-id="05f0f-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="05f0f-110">Kostenrechnungs-Manager</span><span class="sxs-lookup"><span data-stu-id="05f0f-110">Cost accounting manager</span></span> | <span data-ttu-id="05f0f-111">Aktivität</span><span class="sxs-lookup"><span data-stu-id="05f0f-111">Activity</span></span>     |
| <span data-ttu-id="05f0f-112">Kostenbuchhalter</span><span class="sxs-lookup"><span data-stu-id="05f0f-112">Cost accountant</span></span>         | <span data-ttu-id="05f0f-113">Operations</span><span class="sxs-lookup"><span data-stu-id="05f0f-113">Operations</span></span>   |
| <span data-ttu-id="05f0f-114">Sachbearbeiter Kostenbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="05f0f-114">Cost accountant clerk</span></span>   | <span data-ttu-id="05f0f-115">Operations</span><span class="sxs-lookup"><span data-stu-id="05f0f-115">Operations</span></span>   |
| <span data-ttu-id="05f0f-116">Kostenobjekt-Controller</span><span class="sxs-lookup"><span data-stu-id="05f0f-116">Cost object controller</span></span>  | <span data-ttu-id="05f0f-117">Teammitglieder</span><span class="sxs-lookup"><span data-stu-id="05f0f-117">Team members</span></span> |

<span data-ttu-id="05f0f-118">In diesem Thema wird erläutert, wie einem Manager die Rolle **Kostenobjekt-Controller** zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="05f0f-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="05f0f-119">Wenn einem Manager die Rolle **Kostenobjekt-Controller** zugewiesen wird, kann der Manager die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="05f0f-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="05f0f-120">Zugriff auf den Arbeitsbereich **Kostensteuerung** (im Client).</span><span class="sxs-lookup"><span data-stu-id="05f0f-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="05f0f-121">Detailinformationen zu den und Ansichtszugriff auf die Seiten, die die Drillthrough-Erfahrung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="05f0f-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="05f0f-122">Zugriff auf den Arbeitsbereich **Kostensteuerung** (im der Mobilanwendung).</span><span class="sxs-lookup"><span data-stu-id="05f0f-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="05f0f-123">Die Rolle **Kostenobjekt-Controller** steuert nicht, auf welche Kostenobjekte der Benutzer zugreifen und Daten dazu anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="05f0f-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="05f0f-124">Sicherheit auf Positionsebene wird über Dimensionshierarchien und die Zugriffslistenhierarchie bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="05f0f-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="05f0f-125">Zugriffsrechte gewähren</span><span class="sxs-lookup"><span data-stu-id="05f0f-125">Grant access rights</span></span>
<span data-ttu-id="05f0f-126">Das folgende Beispiel zeigt, wie eine Dimensionshierarchie aussehen kann.</span><span class="sxs-lookup"><span data-stu-id="05f0f-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="05f0f-127">**Dimensionshierarchiedetails**</span><span class="sxs-lookup"><span data-stu-id="05f0f-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="05f0f-128">Dimensionshierarchiename</span><span class="sxs-lookup"><span data-stu-id="05f0f-128">Dimension hierarchy name</span></span> | <span data-ttu-id="05f0f-129">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="05f0f-129">Dimension</span></span>    | <span data-ttu-id="05f0f-130">Dimensionshierarchie-Typname</span><span class="sxs-lookup"><span data-stu-id="05f0f-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="05f0f-131">Zugriffslistenhierarchie</span><span class="sxs-lookup"><span data-stu-id="05f0f-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="05f0f-132">Organisation</span><span class="sxs-lookup"><span data-stu-id="05f0f-132">Organization</span></span>             | <span data-ttu-id="05f0f-133">Kostenstellen</span><span class="sxs-lookup"><span data-stu-id="05f0f-133">Cost centers</span></span> | <span data-ttu-id="05f0f-134">Dimensionsklassifizierungshierarchie</span><span class="sxs-lookup"><span data-stu-id="05f0f-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="05f0f-135">**Ja**</span><span class="sxs-lookup"><span data-stu-id="05f0f-135">**Yes**</span></span>               |

<span data-ttu-id="05f0f-136">Sie können das Inforegister **Benutzer** im Hierarchie-Designer verwenden, um mindestens eine Benutzerkennungen auf jedem Knoten einzufügen.</span><span class="sxs-lookup"><span data-stu-id="05f0f-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|             <span data-ttu-id="05f0f-137">Knoten</span><span class="sxs-lookup"><span data-stu-id="05f0f-137">Nodes</span></span>                 | <span data-ttu-id="05f0f-138">Benutzer</span><span class="sxs-lookup"><span data-stu-id="05f0f-138">Users</span></span>            | <span data-ttu-id="05f0f-139">Von-Dimensionsmitglied</span><span class="sxs-lookup"><span data-stu-id="05f0f-139">From dimension member</span></span>     |   <span data-ttu-id="05f0f-140">Bis-Dimensionsmitglied</span><span class="sxs-lookup"><span data-stu-id="05f0f-140">To dimension member</span></span>   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="05f0f-141">Organisation</span><span class="sxs-lookup"><span data-stu-id="05f0f-141">Organization</span></span>                      | <span data-ttu-id="05f0f-142">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="05f0f-142">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="05f0f-143">&nbsp;&nbsp;Verwaltung</span><span class="sxs-lookup"><span data-stu-id="05f0f-143">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="05f0f-144">April</span><span class="sxs-lookup"><span data-stu-id="05f0f-144">April</span></span>            |                           |                         |
| <span data-ttu-id="05f0f-145">&nbsp;&nbsp;&nbsp;&nbsp;Finanzen</span><span class="sxs-lookup"><span data-stu-id="05f0f-145">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="05f0f-146">Alicia</span><span class="sxs-lookup"><span data-stu-id="05f0f-146">Alicia</span></span>           | <span data-ttu-id="05f0f-147">CC002</span><span class="sxs-lookup"><span data-stu-id="05f0f-147">CC002</span></span>                     | <span data-ttu-id="05f0f-148">CC003</span><span class="sxs-lookup"><span data-stu-id="05f0f-148">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="05f0f-149">CC007</span><span class="sxs-lookup"><span data-stu-id="05f0f-149">CC007</span></span>                     | <span data-ttu-id="05f0f-150">CC007</span><span class="sxs-lookup"><span data-stu-id="05f0f-150">CC007</span></span>                   |
| <span data-ttu-id="05f0f-151">&nbsp;&nbsp;&nbsp;&nbsp;Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="05f0f-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="05f0f-152">Arnie</span><span class="sxs-lookup"><span data-stu-id="05f0f-152">Arnie</span></span>            | <span data-ttu-id="05f0f-153">CC001</span><span class="sxs-lookup"><span data-stu-id="05f0f-153">CC001</span></span>                     | <span data-ttu-id="05f0f-154">CC001</span><span class="sxs-lookup"><span data-stu-id="05f0f-154">CC001</span></span>                   |
| <span data-ttu-id="05f0f-155">&nbsp;&nbsp;Produktion</span><span class="sxs-lookup"><span data-stu-id="05f0f-155">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="05f0f-156">David</span><span class="sxs-lookup"><span data-stu-id="05f0f-156">David</span></span>            |                           |                         |
| <span data-ttu-id="05f0f-157">&nbsp;&nbsp;&nbsp;&nbsp;Verpackung</span><span class="sxs-lookup"><span data-stu-id="05f0f-157">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="05f0f-158">Ellen</span><span class="sxs-lookup"><span data-stu-id="05f0f-158">Ellen</span></span>            | <span data-ttu-id="05f0f-159">CC005</span><span class="sxs-lookup"><span data-stu-id="05f0f-159">CC005</span></span>                     | <span data-ttu-id="05f0f-160">CC005</span><span class="sxs-lookup"><span data-stu-id="05f0f-160">CC005</span></span>                   |
| <span data-ttu-id="05f0f-161">&nbsp;&nbsp;&nbsp;&nbsp;Montage</span><span class="sxs-lookup"><span data-stu-id="05f0f-161">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="05f0f-162">Chris</span><span class="sxs-lookup"><span data-stu-id="05f0f-162">Chris</span></span>            | <span data-ttu-id="05f0f-163">CC006</span><span class="sxs-lookup"><span data-stu-id="05f0f-163">CC006</span></span>                     | <span data-ttu-id="05f0f-164">CC006</span><span class="sxs-lookup"><span data-stu-id="05f0f-164">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="05f0f-165">Kostenbuchhalter sollten der höchsten Ebene der Hierarchie zugewiesen werden, damit sie alle Einträge in der Kostenrechnung anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="05f0f-165">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="05f0f-166">Bevor die Zugriffslistenhierarchie und deren Sicherheitseinstellungen angewendet werden können, muss die Option **Anzeigezugriff für Kostenobjektdimensionsmitglieder zulassen** auf **Ja** in der Registerkarte **Allgemein** der Seite **Kostenrechnungsparameter** (**Kostenrechnung** > **Einstellungen** > **Parameter**) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="05f0f-166">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="05f0f-167">Die Einstellungen für die Zugriffslistenhierarchie werden verwendet, um die Daten zu steuern, die in den folgenden Bereichen angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="05f0f-167">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="05f0f-168">Arbeitsbereich **Kostensteuerung** (im Client)</span><span class="sxs-lookup"><span data-stu-id="05f0f-168">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="05f0f-169">Daten auf den Seiten, die für den Drillthrough verwendet werden</span><span class="sxs-lookup"><span data-stu-id="05f0f-169">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="05f0f-170">Arbeitsbereich **Kostensteuerung** (in der Mobilanwendung):</span><span class="sxs-lookup"><span data-stu-id="05f0f-170">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="05f0f-171">Salden in Karten</span><span class="sxs-lookup"><span data-stu-id="05f0f-171">Balances in cards</span></span>

- <span data-ttu-id="05f0f-172">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="05f0f-172">Microsoft Power BI:</span></span>

    - <span data-ttu-id="05f0f-173">Daten, die in Power BI-Visualisierungen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="05f0f-173">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="05f0f-174">Power BI-Datenvisualisierungen, die im Client der Dynamics 365 Finance eingebettet werden</span><span class="sxs-lookup"><span data-stu-id="05f0f-174">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="05f0f-175">Bevor sich die Zugriffslistenhierarchie auf Daten in Power BI auswirken kann, müssen die Zugriffslistenhierarchie und Sicherheit auf Zeilenebene in Power BI zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="05f0f-175">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="05f0f-176">Weitere Informationen finden Sie unter [Sicherheit für das Kostenrechnungs-Inhaltspack einrichten](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="05f0f-176">For more information, see [Set up security for Cost accounting content pack](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="05f0f-177">In diesem Thema werden die Voraussetzungen behandelt, die erfüllt sein müssen, bevor Sie den Arbeitsbereich **Kostensteuerung** verwenden können.</span><span class="sxs-lookup"><span data-stu-id="05f0f-177">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="05f0f-178">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="05f0f-178">Additional resources</span></span>

- [<span data-ttu-id="05f0f-179">Kostensteuerungs-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="05f0f-179">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="05f0f-180">Dimensionshierarchie</span><span class="sxs-lookup"><span data-stu-id="05f0f-180">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="05f0f-181">Sicherheit für Kostensteuerungs-Inhaltspack einrichten</span><span class="sxs-lookup"><span data-stu-id="05f0f-181">Set up security for Cost accounting content pack</span></span>](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
