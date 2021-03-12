---
title: Organisationshierarchien einrichten
description: In diesem Thema wird beschrieben, wie man in Microsoft Dynamics 365 Commerce Organisationshierarchien aufbaut.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b887616ef29396ba99ca0c7428ab89df01b3008c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997774"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="5b635-103">Organisationshierarchien einrichten</span><span class="sxs-lookup"><span data-stu-id="5b635-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5b635-104">In diesem Thema wird beschrieben, wie man in Microsoft Dynamics 365 Commerce Organisationshierarchien aufbaut.</span><span class="sxs-lookup"><span data-stu-id="5b635-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5b635-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="5b635-105">Overview</span></span>

<span data-ttu-id="5b635-106">Bevor Sie Kanäle erstellen, müssen Sie sicherstellen, dass Ihre Organisationshierarchien eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="5b635-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="5b635-107">Organisationshierarchien können verwendet werden, um unterschiedliche Perspektiven des Unternehmens anzuzeigen und entsprechende Berichte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b635-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="5b635-108">So können Sie z. B. eine Hierarchie für Steuererklärungen sowie für rechtlich relevante oder für gesetzlich vorgeschriebene Berichte einrichten.</span><span class="sxs-lookup"><span data-stu-id="5b635-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="5b635-109">Anschließend können Sie eine weitere Hierarchie einrichten, um anhand von Finanzdaten Berichte zu erstellen, die zwar gesetzlich nicht erforderlich sind, aber zur internen Berichterstattung dienen.</span><span class="sxs-lookup"><span data-stu-id="5b635-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="5b635-110">Bevor Sie eine Organisationshierarchie erstellen, müssen Sie Organisationen erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b635-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="5b635-111">Weitere Informationen finden Sie unter [Juristische Personen erstellen](channels-legal-entities.md) oder [Organisationseinheiten erstellen](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="5b635-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="5b635-112">Weitere Informationen finden Sie unter folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="5b635-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="5b635-113">Organisationen und Organisationshierarchien – Übersicht</span><span class="sxs-lookup"><span data-stu-id="5b635-113">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="5b635-114">Ihre Organisationshierarchie planen</span><span class="sxs-lookup"><span data-stu-id="5b635-114">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="5b635-115">Erstellen einer Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="5b635-115">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="5b635-116">Erstellen einer Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="5b635-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="5b635-117">Führen Sie die folgenden Schritte aus, um eine Organisationshierarchie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b635-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="5b635-118">Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Organisationshierarchien**.</span><span class="sxs-lookup"><span data-stu-id="5b635-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="5b635-119">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5b635-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5b635-120">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5b635-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="5b635-121">Wählen Sie im Abschnitt **Zweck** die Option **Zweck zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="5b635-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="5b635-122">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5b635-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="5b635-123">Wählen Sie einen Zweck aus, der Ihrer Organisationshierarchie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b635-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="5b635-124">Wählen Sie im Abschnitt **Zugewiesene Hierarchien** die Option **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="5b635-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="5b635-125">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5b635-125">In the list, mark the selected row.</span></span> <span data-ttu-id="5b635-126">Suchen Sie die Hierarchie, die Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5b635-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="5b635-127">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b635-127">Select **OK**.</span></span>

<span data-ttu-id="5b635-128">Die folgende Abbildung zeigt eine beispielhafte Organisationshierarchie, die für eine fiktive Gruppe von „Adventure Works”-Läden erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5b635-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Beispiel einer Organisationshierarchie](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="5b635-130">Hinzufügen von Organisationen zu einer Hierarchie</span><span class="sxs-lookup"><span data-stu-id="5b635-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="5b635-131">Gehen Sie folgendermaßen vor, um Organisationen zu einer Hierarchie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b635-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="5b635-132">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5b635-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="5b635-133">Wählen Sie Ihre Hierarchie aus.</span><span class="sxs-lookup"><span data-stu-id="5b635-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="5b635-134">Wählen Sie im Aktionsbereich **Anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="5b635-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="5b635-135">Fügen Sie Organisationen nach Bedarf hinzu.</span><span class="sxs-lookup"><span data-stu-id="5b635-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="5b635-136">Um eine Organisation hinzuzufügen, wählen Sie **Bearbeiten** und dann **Einfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5b635-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="5b635-137">Wenn Sie mit den Änderungen fertig sind, können Sie einen Entwurf speichern und die Änderungen veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="5b635-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="5b635-138">Die folgende Abbildung zeigt eine juristische Person, die im Hierarchie-Stammverzeichnis hinzugefügt wurde. Für die Kanäle „Mall“, „Outlet“, „Online“ und „Callcenter“ wurden vier Kostenstellen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5b635-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="5b635-139">Anschließend können jeweils verschiedene Einzelhandels-, Callcenter- und Online-Kanäle hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5b635-139">Various retail, call center and online channels can then be added to each.</span></span>

![Beispiel eines Hierarchiedesigners](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="5b635-141">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5b635-141">Additional resources</span></span>

[<span data-ttu-id="5b635-142">Organisationen und Organisationshierarchien – Übersicht</span><span class="sxs-lookup"><span data-stu-id="5b635-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="5b635-143">Planen Ihrer Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="5b635-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="5b635-144">Erstellen juristischer Personen</span><span class="sxs-lookup"><span data-stu-id="5b635-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="5b635-145">Erstellen von Organisationseinheiten</span><span class="sxs-lookup"><span data-stu-id="5b635-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="5b635-146">Kanalübersicht</span><span class="sxs-lookup"><span data-stu-id="5b635-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="5b635-147">Voraussetzungen der Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="5b635-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
