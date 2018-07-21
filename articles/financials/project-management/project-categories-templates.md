---
title: Synchronisieren Sie Ausgabenkategorien von Project Service Automation
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Projektausgabenkategorien zwischen Microsoft Dynamics 365 for Finance and Operations und Dynamics 365 for Project Service Automation zu synchronisieren."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: de-de
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="4ba60-103">Synchronisieren Sie Projektausgabenkategorien zwischen Finance and Operations and Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4ba60-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="4ba60-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Projektausgabenkategorien zwischen Microsoft Dynamics 365 for Finance and Operations und Dynamics 365 for Project Service Automation zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="4ba60-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="4ba60-105">Projektaufgaben-Integration, Ausgabenbuchungskategorien, StundensDynamics 365 for Finance and Operations version 8.0.chätzungen, Ausgabenenschätzungen und Funktionenssperre sind in Dynamics 365 for Finance and Operations Version 8.0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4ba60-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="4ba60-106">Datenfluss für Project Service Automation und Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4ba60-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="4ba60-107">Die Project Service Automation und Finance and Operations Integrationslösung nutzen die  Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="4ba60-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="4ba60-108">Die Integrationsvorlagen, die in der Datenenintegrationsfunktion verfügbar sind, ermöglichen den Datenfluss zu Projektaufgaben zwischen Finance and Operations and Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="4ba60-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="4ba60-109">Wenn die Projektausgabenkategorien im Bereich Finance and Operations verwaltet werden, erfolgt der Integrationsfluss zuerst von Finance and Operations zu Project Service Automation und aktualisiert dann Projektausgabenkategorien-Integrations-IDs durch Synchronisierung von Project Service Automation zu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4ba60-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="4ba60-110">Wenn die Projektausgabenkategorien in der Project Service Automation erfolgt, ist der Integrationsfluss zuerst von Project Service Automation zu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4ba60-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="4ba60-111">Die Projektkategorien müssen im Bereich Finance and Operations vor der Synchronisierung mit Project Service Automation konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="4ba60-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="4ba60-112">Dann synchronisieren Sie von Finance and Operations zurück zur Project Service Automation und dann von Project Service Automation zu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4ba60-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="4ba60-113">Dadurch wird sichergestellt, dass die Kategorien verknüpft werden und keine Duplikate erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4ba60-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="4ba60-114">Normalerweise werden die Projektausgabenkategorien in Finance and Operations abgewickelt.</span><span class="sxs-lookup"><span data-stu-id="4ba60-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="4ba60-115">Wenn das nicht Ihrer Situation entspricht oder Sie bereits Ausgabenkategorien in Project Service Automation erstellt haben, müssen Sie zuerst die Projektausgabenbuchungskategorien (PSA zu Fin und Ops) synchronisieren und dann Projektausgabentransaktions-Kategorien (Fin und Ops zu PSA) synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="4ba60-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="4ba60-116">Sie sollten dann die Synchronisierung von PSA zu Fin und Ops noch einmal ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ba60-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="4ba60-117">Wenn Sie zuerst von Project Service Automation synchronisieren, müssen die Projektkategorien zuerst in Finance and Operations eingerichtet werden und sämtliche Projektkategorien, die mit Project Service Automation Transaktionskategorien synchronisiert werden müssen, müssen eingerichtet werden, um **Aktiv in Erfassungen** zu sein.</span><span class="sxs-lookup"><span data-stu-id="4ba60-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="4ba60-118">Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4ba60-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="4ba60-119">[![Datenfluss für Project Service Automation Integration mit Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="4ba60-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="4ba60-120">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="4ba60-120">Templates and tasks</span></span>

<span data-ttu-id="4ba60-121">Wenn Sie auf die Vorlage im Microsoft PowerApps Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4ba60-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="4ba60-122">Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Projektausgabenkategorien von Finance and Operations zu Project Service Automation zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="4ba60-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="4ba60-123">**Name der Vorlage in der Datenintegration:** Projekctausgabentransaktionskategorien (Fin and Ops zu PSA)</span><span class="sxs-lookup"><span data-stu-id="4ba60-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="4ba60-124">**Name der Aufgabe im Projekt:** Synchronisierungskategorien zu PSA</span><span class="sxs-lookup"><span data-stu-id="4ba60-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="4ba60-125">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="4ba60-125">Entity set</span></span>

| <span data-ttu-id="4ba60-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4ba60-126">Finance and Operations</span></span>               | <span data-ttu-id="4ba60-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4ba60-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="4ba60-128">Integrationsentität für Kategorien</span><span class="sxs-lookup"><span data-stu-id="4ba60-128">Integration entity for categories</span></span>    | <span data-ttu-id="4ba60-129">Transaktionskategorien</span><span class="sxs-lookup"><span data-stu-id="4ba60-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="4ba60-130">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="4ba60-130">Entity flow</span></span>

<span data-ttu-id="4ba60-131">Projektausgaben werden in Finance and Operations verwaltet und dann zu Project Service Automation als Transaktionskategorien synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="4ba60-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="4ba60-132">Powerabfrage</span><span class="sxs-lookup"><span data-stu-id="4ba60-132">Power Query</span></span>

<span data-ttu-id="4ba60-133">Sie müssen icrosoft Power Query nutzen, um den Fakturierungstyps auf der Transaktionskategorie festzulegen, wenn Sie mit Project Service Automation synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="4ba60-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="4ba60-134">Die Project Ausgabentransaktionskategorie (Fin und Ops zu PSA) Vorlage hat eine Standardspalte und die Zuordnung ist bereits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4ba60-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="4ba60-135">Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie eine bedingte Spalte in der Power-Abfrage hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4ba60-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="4ba60-136">Öffnen Sie die Vorabfragen- und Filterungsformulare in der Zuordnung der Projektausgabenkategorieaufgabe.</span><span class="sxs-lookup"><span data-stu-id="4ba60-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="4ba60-137">Wählen Sie **Hinzufügen von bedingten Spalten** aus.</span><span class="sxs-lookup"><span data-stu-id="4ba60-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="4ba60-138">Geben Sie der neuen Spalte einen Namen, wie BillingType.</span><span class="sxs-lookup"><span data-stu-id="4ba60-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="4ba60-139">Geben Sie die folgende Bedingung ein: wenn **CATEGORYID Ungleich null dann 19235001, ansonsten NULL**.</span><span class="sxs-lookup"><span data-stu-id="4ba60-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="4ba60-140">Klicken Sie **OK** in der Spalte.</span><span class="sxs-lookup"><span data-stu-id="4ba60-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="4ba60-141">Stellen Sie sicher, dass Sie diese neue Spalte der Zuordnungsseite zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="4ba60-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="4ba60-142">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="4ba60-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="4ba60-143">Die Zuordnung zeigt, welche Feldinformationen von Finance and Operations zu Project Service Automation synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4ba60-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="4ba60-144">[![Vorlagenzuordnung](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="4ba60-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="4ba60-145">Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Projektausgabenkategorien von Project Service Automation zu Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="4ba60-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="4ba60-146">-**Bezeichnung der Vorlage in der Datenintegration:** Projektausgabentransaktion (PSA zu Fin and Ops) - **Name der Aufgabe im Projekt** Synchronisation der Kategorien zu Fin Ops</span><span class="sxs-lookup"><span data-stu-id="4ba60-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="4ba60-147">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="4ba60-147">Entity set</span></span>

| <span data-ttu-id="4ba60-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4ba60-148">Project Service Automation</span></span>      | <span data-ttu-id="4ba60-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4ba60-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="4ba60-150">Transaktionskategorien</span><span class="sxs-lookup"><span data-stu-id="4ba60-150">Transaction categories</span></span>          | <span data-ttu-id="4ba60-151">Integrationsentität für Kategorien</span><span class="sxs-lookup"><span data-stu-id="4ba60-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="4ba60-152">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="4ba60-152">Entity flow</span></span>

<span data-ttu-id="4ba60-153">Projektausgaben werden in Finance and Operations verwaltet und dann zu Project Service Automation als Transaktionskategorien synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="4ba60-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="4ba60-154">Die Rücksynchronisierung zu Finance and Operations aktualisiert die Integrations-ID von Project Service Automation auf der Finance and Operations Projektkategorie.</span><span class="sxs-lookup"><span data-stu-id="4ba60-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="4ba60-155">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="4ba60-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="4ba60-156">Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4ba60-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="4ba60-157">[![Vorlagenzuordnung](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="4ba60-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

