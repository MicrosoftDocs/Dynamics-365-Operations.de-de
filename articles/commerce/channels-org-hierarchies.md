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
ms.openlocfilehash: 490d466c10cfe0640f8fbcf8fe2298536e499d9b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477995"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="897f0-103">Organisationshierarchien einrichten</span><span class="sxs-lookup"><span data-stu-id="897f0-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="897f0-104">In diesem Thema wird beschrieben, wie man in Microsoft Dynamics 365 Commerce Organisationshierarchien aufbaut.</span><span class="sxs-lookup"><span data-stu-id="897f0-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="897f0-105">Bevor Sie Kanäle erstellen, müssen Sie sicherstellen, dass Ihre Organisationshierarchien eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="897f0-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="897f0-106">Organisationshierarchien können verwendet werden, um unterschiedliche Perspektiven des Unternehmens anzuzeigen und entsprechende Berichte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="897f0-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="897f0-107">So können Sie z. B. eine Hierarchie für Steuererklärungen sowie für rechtlich relevante oder für gesetzlich vorgeschriebene Berichte einrichten.</span><span class="sxs-lookup"><span data-stu-id="897f0-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="897f0-108">Anschließend können Sie eine weitere Hierarchie einrichten, um anhand von Finanzdaten Berichte zu erstellen, die zwar gesetzlich nicht erforderlich sind, aber zur internen Berichterstattung dienen.</span><span class="sxs-lookup"><span data-stu-id="897f0-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="897f0-109">Bevor Sie eine Organisationshierarchie erstellen, müssen Sie Organisationen erstellen.</span><span class="sxs-lookup"><span data-stu-id="897f0-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="897f0-110">Weitere Informationen finden Sie unter [Juristische Personen erstellen](channels-legal-entities.md) oder [Organisationseinheiten erstellen](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="897f0-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="897f0-111">Weitere Informationen finden Sie unter folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="897f0-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="897f0-112">Organisationen und Organisationshierarchien – Übersicht</span><span class="sxs-lookup"><span data-stu-id="897f0-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="897f0-113">Ihre Organisationshierarchie planen</span><span class="sxs-lookup"><span data-stu-id="897f0-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="897f0-114">Erstellen einer Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="897f0-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="897f0-115">Erstellen einer Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="897f0-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="897f0-116">Führen Sie die folgenden Schritte aus, um eine Organisationshierarchie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="897f0-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="897f0-117">Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Organisationshierarchien**.</span><span class="sxs-lookup"><span data-stu-id="897f0-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="897f0-118">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="897f0-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="897f0-119">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="897f0-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="897f0-120">Wählen Sie im Abschnitt **Zweck** die Option **Zweck zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="897f0-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="897f0-121">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="897f0-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="897f0-122">Wählen Sie einen Zweck aus, der Ihrer Organisationshierarchie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="897f0-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="897f0-123">Wählen Sie im Abschnitt **Zugewiesene Hierarchien** die Option **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="897f0-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="897f0-124">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="897f0-124">In the list, mark the selected row.</span></span> <span data-ttu-id="897f0-125">Suchen Sie die Hierarchie, die Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="897f0-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="897f0-126">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="897f0-126">Select **OK**.</span></span>

<span data-ttu-id="897f0-127">Die folgende Abbildung zeigt eine beispielhafte Organisationshierarchie, die für eine fiktive Gruppe von „Adventure Works”-Läden erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="897f0-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Beispiel einer Organisationshierarchie](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="897f0-129">Hinzufügen von Organisationen zu einer Hierarchie</span><span class="sxs-lookup"><span data-stu-id="897f0-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="897f0-130">Gehen Sie folgendermaßen vor, um Organisationen zu einer Hierarchie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="897f0-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="897f0-131">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="897f0-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="897f0-132">Wählen Sie Ihre Hierarchie aus.</span><span class="sxs-lookup"><span data-stu-id="897f0-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="897f0-133">Wählen Sie im Aktionsbereich **Anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="897f0-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="897f0-134">Fügen Sie Organisationen nach Bedarf hinzu.</span><span class="sxs-lookup"><span data-stu-id="897f0-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="897f0-135">Um eine Organisation hinzuzufügen, wählen Sie **Bearbeiten** und dann **Einfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="897f0-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="897f0-136">Wenn Sie mit den Änderungen fertig sind, können Sie einen Entwurf speichern und die Änderungen veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="897f0-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="897f0-137">Die folgende Abbildung zeigt eine juristische Person, die im Hierarchie-Stammverzeichnis hinzugefügt wurde. Für die Kanäle „Mall“, „Outlet“, „Online“ und „Callcenter“ wurden vier Kostenstellen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897f0-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="897f0-138">Anschließend können jeweils verschiedene Einzelhandels-, Callcenter- und Online-Kanäle hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="897f0-138">Various retail, call center and online channels can then be added to each.</span></span>

![Beispiel eines Hierarchiedesigners](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="897f0-140">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="897f0-140">Additional resources</span></span>

[<span data-ttu-id="897f0-141">Organisationen und Organisationshierarchien – Übersicht</span><span class="sxs-lookup"><span data-stu-id="897f0-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="897f0-142">Planen Ihrer Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="897f0-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="897f0-143">Erstellen juristischer Personen</span><span class="sxs-lookup"><span data-stu-id="897f0-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="897f0-144">Erstellen von Organisationseinheiten</span><span class="sxs-lookup"><span data-stu-id="897f0-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="897f0-145">Kanalübersicht</span><span class="sxs-lookup"><span data-stu-id="897f0-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="897f0-146">Voraussetzungen der Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="897f0-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
