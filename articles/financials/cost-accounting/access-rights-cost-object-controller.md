---
title: Zugriffsrechte für Kostenobjekt-Controller definieren
description: Dieses Thema bietet Informationen über Zugriffsrechte für Kostenobjekt-Controller.
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 290b16eeb99ac7ddb9b552b289215c99a0451660
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "355540"
---
# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="6a935-103">Zugriffsrechte eines Kostenobjekt-Controllers</span><span class="sxs-lookup"><span data-stu-id="6a935-103">Access rights of a cost object controller</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a935-104">Der Arbeitsbereich **Kostensteuerung** ist ein zentraler Punkt, in dem Manager die Leistung der Kostenobjekte anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="6a935-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="6a935-105">In diesem Arbeitsbereich können Manager Kostenrechnungsdaten nutzen, auch wenn sie keine Kostenbuchhalter sind.</span><span class="sxs-lookup"><span data-stu-id="6a935-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="6a935-106">Aus Sicherheitsgründen solle Managern ermöglicht werden, nur die Kostenrechnungsdaten anzuzeigen, die den bestimmten Kostenobjekten zugeordnet sind, für die sie zuständig sind.</span><span class="sxs-lookup"><span data-stu-id="6a935-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="6a935-107">Es gibt vier eindeutige Rollen in der Kostenrechnung.</span><span class="sxs-lookup"><span data-stu-id="6a935-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="6a935-108">Rollenname</span><span class="sxs-lookup"><span data-stu-id="6a935-108">Role name</span></span>               | <span data-ttu-id="6a935-109">Lizenz</span><span class="sxs-lookup"><span data-stu-id="6a935-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="6a935-110">Kostenrechnungs-Manager</span><span class="sxs-lookup"><span data-stu-id="6a935-110">Cost accounting manager</span></span> | <span data-ttu-id="6a935-111">Aktivität</span><span class="sxs-lookup"><span data-stu-id="6a935-111">Activity</span></span>     |
| <span data-ttu-id="6a935-112">Kostenbuchhalter</span><span class="sxs-lookup"><span data-stu-id="6a935-112">Cost accountant</span></span>         | <span data-ttu-id="6a935-113">Operations</span><span class="sxs-lookup"><span data-stu-id="6a935-113">Operations</span></span>   |
| <span data-ttu-id="6a935-114">Sachbearbeiter Kostenbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="6a935-114">Cost accountant clerk</span></span>   | <span data-ttu-id="6a935-115">Operations</span><span class="sxs-lookup"><span data-stu-id="6a935-115">Operations</span></span>   |
| <span data-ttu-id="6a935-116">Kostenobjekt-Controller</span><span class="sxs-lookup"><span data-stu-id="6a935-116">Cost object controller</span></span>  | <span data-ttu-id="6a935-117">Teammitglieder</span><span class="sxs-lookup"><span data-stu-id="6a935-117">Team members</span></span> |

<span data-ttu-id="6a935-118">In diesem Thema wird erläutert, wie einem Manager die Rolle **Kostenobjekt-Controller** zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6a935-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="6a935-119">Wenn einem Manager die Rolle **Kostenobjekt-Controller** zugewiesen wird, kann der Manager die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="6a935-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="6a935-120">Zugriff auf den Arbeitsbereich **Kostensteuerung** (im Client).</span><span class="sxs-lookup"><span data-stu-id="6a935-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="6a935-121">Detailinformationen zu den und Ansichtszugriff auf die Seiten, die die Drillthrough-Erfahrung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6a935-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="6a935-122">Zugriff auf den Arbeitsbereich **Kostensteuerung** (im der Mobilanwendung).</span><span class="sxs-lookup"><span data-stu-id="6a935-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="6a935-123">Die Rolle **Kostenobjekt-Controller** steuert nicht, auf welche Kostenobjekte der Benutzer zugreifen und Daten dazu anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="6a935-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="6a935-124">Sicherheit auf Positionsebene wird über Dimensionshierarchien und die Zugriffslistenhierarchie bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6a935-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="6a935-125">Zugriffsrechte gewähren</span><span class="sxs-lookup"><span data-stu-id="6a935-125">Grant access rights</span></span>
<span data-ttu-id="6a935-126">Das folgende Beispiel zeigt, wie eine Dimensionshierarchie aussehen kann.</span><span class="sxs-lookup"><span data-stu-id="6a935-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="6a935-127">**Dimensionshierarchiedetails**</span><span class="sxs-lookup"><span data-stu-id="6a935-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="6a935-128">Dimensionshierarchiename</span><span class="sxs-lookup"><span data-stu-id="6a935-128">Dimension hierarchy name</span></span> | <span data-ttu-id="6a935-129">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="6a935-129">Dimension</span></span>    | <span data-ttu-id="6a935-130">Dimensionshierarchie-Typname</span><span class="sxs-lookup"><span data-stu-id="6a935-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="6a935-131">Zugriffslistenhierarchie</span><span class="sxs-lookup"><span data-stu-id="6a935-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="6a935-132">Organisation</span><span class="sxs-lookup"><span data-stu-id="6a935-132">Organization</span></span>             | <span data-ttu-id="6a935-133">Kostenstellen</span><span class="sxs-lookup"><span data-stu-id="6a935-133">Cost centers</span></span> | <span data-ttu-id="6a935-134">Dimensionsklassifizierungshierarchie</span><span class="sxs-lookup"><span data-stu-id="6a935-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="6a935-135">**Ja**</span><span class="sxs-lookup"><span data-stu-id="6a935-135">**Yes**</span></span>               |

<span data-ttu-id="6a935-136">Sie können das Inforegister **Benutzer** im Hierarchie-Designer verwenden, um mindestens eine Benutzerkennungen auf jedem Knoten einzufügen.</span><span class="sxs-lookup"><span data-stu-id="6a935-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="6a935-137">Benutzer</span><span class="sxs-lookup"><span data-stu-id="6a935-137">Users</span></span>            | <span data-ttu-id="6a935-138">Dimensionsmitgliedsbereiche</span><span class="sxs-lookup"><span data-stu-id="6a935-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="6a935-139">**Knoten**</span><span class="sxs-lookup"><span data-stu-id="6a935-139">**Nodes**</span></span>                         | <span data-ttu-id="6a935-140">**Benutzerkennung**</span><span class="sxs-lookup"><span data-stu-id="6a935-140">**User ID**</span></span>      | <span data-ttu-id="6a935-141">**Ausgangsdimensionsmitglied**</span><span class="sxs-lookup"><span data-stu-id="6a935-141">**From dimension member**</span></span> | <span data-ttu-id="6a935-142">**Zieldimensionsmitglied**</span><span class="sxs-lookup"><span data-stu-id="6a935-142">**To dimension member**</span></span> |
| <span data-ttu-id="6a935-143">Organisation</span><span class="sxs-lookup"><span data-stu-id="6a935-143">Organization</span></span>                      | <span data-ttu-id="6a935-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="6a935-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="6a935-145">&nbsp;&nbsp;Verwaltung</span><span class="sxs-lookup"><span data-stu-id="6a935-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="6a935-146">April</span><span class="sxs-lookup"><span data-stu-id="6a935-146">April</span></span>            |                           |                         |
| <span data-ttu-id="6a935-147">&nbsp;&nbsp;&nbsp;&nbsp;Finanzen</span><span class="sxs-lookup"><span data-stu-id="6a935-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="6a935-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="6a935-148">Alicia</span></span>           | <span data-ttu-id="6a935-149">CC002</span><span class="sxs-lookup"><span data-stu-id="6a935-149">CC002</span></span>                     | <span data-ttu-id="6a935-150">CC003</span><span class="sxs-lookup"><span data-stu-id="6a935-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="6a935-151">CC007</span><span class="sxs-lookup"><span data-stu-id="6a935-151">CC007</span></span>                     | <span data-ttu-id="6a935-152">CC007</span><span class="sxs-lookup"><span data-stu-id="6a935-152">CC007</span></span>                   |
| <span data-ttu-id="6a935-153">&nbsp;&nbsp;&nbsp;&nbsp;Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="6a935-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="6a935-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="6a935-154">Arnie</span></span>            | <span data-ttu-id="6a935-155">CC001</span><span class="sxs-lookup"><span data-stu-id="6a935-155">CC001</span></span>                     | <span data-ttu-id="6a935-156">CC001</span><span class="sxs-lookup"><span data-stu-id="6a935-156">CC001</span></span>                   |
| <span data-ttu-id="6a935-157">&nbsp;&nbsp;Produktion</span><span class="sxs-lookup"><span data-stu-id="6a935-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="6a935-158">David</span><span class="sxs-lookup"><span data-stu-id="6a935-158">David</span></span>            |                           |                         |
| <span data-ttu-id="6a935-159">&nbsp;&nbsp;&nbsp;&nbsp;Verpackung</span><span class="sxs-lookup"><span data-stu-id="6a935-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="6a935-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="6a935-160">Ellen</span></span>            | <span data-ttu-id="6a935-161">CC005</span><span class="sxs-lookup"><span data-stu-id="6a935-161">CC005</span></span>                     | <span data-ttu-id="6a935-162">CC005</span><span class="sxs-lookup"><span data-stu-id="6a935-162">CC005</span></span>                   |
| <span data-ttu-id="6a935-163">&nbsp;&nbsp;&nbsp;&nbsp;Montage</span><span class="sxs-lookup"><span data-stu-id="6a935-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="6a935-164">Chris</span><span class="sxs-lookup"><span data-stu-id="6a935-164">Chris</span></span>            | <span data-ttu-id="6a935-165">CC006</span><span class="sxs-lookup"><span data-stu-id="6a935-165">CC006</span></span>                     | <span data-ttu-id="6a935-166">CC006</span><span class="sxs-lookup"><span data-stu-id="6a935-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="6a935-167">Kostenbuchhalter sollten der höchsten Ebene der Hierarchie zugewiesen werden, damit sie alle Einträge in der Kostenrechnung anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="6a935-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="6a935-168">Bevor die Zugriffslistenhierarchie und deren Sicherheitseinstellungen angewendet werden können, muss die Option **Anzeigezugriff für Kostenobjektdimensionsmitglieder zulassen** auf **Ja** in der Registerkarte **Allgemein** der Seite **Kostenrechnungsparameter** (**Kostenrechnung** > **Einstellungen** > **Parameter**) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6a935-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="6a935-169">Die Einstellungen für die Zugriffslistenhierarchie werden verwendet, um die Daten zu steuern, die in den folgenden Bereichen angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="6a935-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="6a935-170">Arbeitsbereich **Kostensteuerung** (im Client)</span><span class="sxs-lookup"><span data-stu-id="6a935-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="6a935-171">Daten auf den Seiten, die für den Drillthrough verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6a935-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="6a935-172">Arbeitsbereich **Kostensteuerung** (in der Mobilanwendung):</span><span class="sxs-lookup"><span data-stu-id="6a935-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="6a935-173">Salden in Karten</span><span class="sxs-lookup"><span data-stu-id="6a935-173">Balances in cards</span></span>

- <span data-ttu-id="6a935-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="6a935-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="6a935-175">Daten, die in Power BI-Visualisierungen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="6a935-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="6a935-176">Power BI-Datenvisualisierungen, die im Client von Microsoft Dynamics 365 for Finance and Operations eingebettet werden</span><span class="sxs-lookup"><span data-stu-id="6a935-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="6a935-177">Bevor sich die Zugriffslistenhierarchie auf Daten in Power BI auswirken kann, müssen die Zugriffslistenhierarchie und Sicherheit auf Zeilenebene in Power BI zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="6a935-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="6a935-178">Weitere Informationen finden Sie unter [Sicherheit für das Kostenrechnungs-Inhaltspack einrichten](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="6a935-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="6a935-179">In diesem Thema werden die Voraussetzungen behandelt, die erfüllt sein müssen, bevor Sie den Arbeitsbereich **Kostensteuerung** verwenden können.</span><span class="sxs-lookup"><span data-stu-id="6a935-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="6a935-180">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6a935-180">Additional resources</span></span>

- [<span data-ttu-id="6a935-181">Kostensteuerungs-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="6a935-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="6a935-182">Dimensionshierarchie</span><span class="sxs-lookup"><span data-stu-id="6a935-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="6a935-183">Sicherheit für Kostensteuerungs-Inhaltspack einrichten</span><span class="sxs-lookup"><span data-stu-id="6a935-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)
