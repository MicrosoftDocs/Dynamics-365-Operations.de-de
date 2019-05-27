---
title: Projektaufträge
description: In diesem Thema wird erläutert, wie Projekt basierte Auträge für Zeit- und Materialprojekte erstellt werden.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1529901"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="2379a-103">Projekt-Aufträge für Zeit- und Materialprojekte</span><span class="sxs-lookup"><span data-stu-id="2379a-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="2379a-104">In diesem Thema wird beschrieben, wie ein Auftrag für ein Projekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2379a-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="2379a-105">Aufträge können ausschließlich für Projekte vom Typ **Zeit oder 'Material** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2379a-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="2379a-106">Wenn ein Zeit- und Materialprojekt mehrere Finanzierungsquellen im Projektvertrag hat, müssen Sie die Parameter **Aufträge für Projekte mit mehreren Finanzierungsquellen zulassen** auf der Seite **Projektmanagement und Buchhaltungsparameter** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2379a-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="2379a-107">Unterstützung für Projektaufträge mit mehreren Finanzierungsquellen ist verfügbar beginnend mit Anwendung 10.0.2 und höher.</span><span class="sxs-lookup"><span data-stu-id="2379a-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="2379a-108">Der Parameter, um den Support für Projektaufträge mit mehreren Finanzierungsquellen zu aktivieren wird in der im April 2020 geplanten Aktualisierung entfernt und die Funktion wird danach immer aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="2379a-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="2379a-109">Sie können Projekt basierte Aufträge auf zwei Arten erstellen:</span><span class="sxs-lookup"><span data-stu-id="2379a-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="2379a-110">Gehen Sie zum Projekt selber.</span><span class="sxs-lookup"><span data-stu-id="2379a-110">Go to the project itself.</span></span> <span data-ttu-id="2379a-111">Klicken Sie im Aktivitätsbereich auf **Verwalten > Artikelaufgaben > Auftrag**.</span><span class="sxs-lookup"><span data-stu-id="2379a-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="2379a-112">Die Projektinformationen werden standardmäßig dem Auftrag aus dem Projekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2379a-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="2379a-113">Hat der Projektvertrag mehrere Finanzierungsquellen, müssen Sie die Finanzierungsquelle auswählen, um den Debitor für den Auftrag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2379a-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="2379a-114">Wenn es nur eine Finanzierungsquelle für das Projekt gibt, wird der Debitor automatisch festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2379a-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="2379a-115">Gehen Sie zur Listenseite **alle Aufträge** und erstellen Sie einen neuen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="2379a-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="2379a-116">Sie müssen das Projekt für den Auftrag auswählen.</span><span class="sxs-lookup"><span data-stu-id="2379a-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="2379a-117">Nachdem das Projekt ausgewählt ist, wird der Debitor von der Finanzierungsquelle festgelegt, oder Sie müssen die Finanzierungsquelle auswählen, wenn der Projektvertrag mehrere Finanzierungsquellen aufweist.</span><span class="sxs-lookup"><span data-stu-id="2379a-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

