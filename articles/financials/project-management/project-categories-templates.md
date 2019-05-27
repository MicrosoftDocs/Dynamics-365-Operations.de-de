---
title: Synchronisieren Sie Projektausgabenkategorien zwischen Finance and Operations and Project Service Automation
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projektausgabenkategorien zwischen Microsoft Dynamics 365 for Finance and Operations und Microsoft Dynamics 365 for Project Service Automation zu synchronisieren.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558241"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="b30ee-103">Synchronisieren Sie Projektausgabenkategorien zwischen Finance and Operations and Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b30ee-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b30ee-104">Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projektausgabenkategorien zwischen Microsoft Dynamics 365 for Finance and Operations und Microsoft Dynamics 365 for Project Service Automation zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b30ee-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="b30ee-105">Projektaufgaben-Integration, Ausgabenbuchungskategorien, Stundenschätzungen, Ausgabenenschätzungen und Funktionenssperre sind in Microsoft Dynamics 365 for Finance and Operations, Version 8.0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b30ee-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="b30ee-106">Integration von Ist-Werten ist in Microsoft Dynamics 365 for Finance and Operations, Version 8.0.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b30ee-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="b30ee-107">Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 verwenden und KB 4132657 und 4132660 KB einrichten, sind Sie in der Lage, die Vorlagen zu verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, geschätzte Stunden, geschätzte Ausgaben und aktuelle Kosten zu integrieren und die Funktionalitätssperre zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b30ee-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="b30ee-108">Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, wird empfohlen, dass Sie auch 4131710 KB einrichten.</span><span class="sxs-lookup"><span data-stu-id="b30ee-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="b30ee-109">Datenfluss für Project Service Automation und Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b30ee-109">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="b30ee-110">Die Project Service Automation und Finance and Operations Integrationslösung nutzen die Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b30ee-110">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="b30ee-111">Die Integrationsvorlagen, die in der Datenintegrationsfunktion verfügbar sind, ermöglichen den Datenfluss zu Projektausgaben-Transaktionskategorien zwischen Finance and Operations und Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b30ee-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="b30ee-112">Wenn die Projektausgabenkategorien in Finance and Operations erfolgreich gehandhabt werden, erfolgt der Integrationsfluss zuerst von Finance and Operations nach Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b30ee-112">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation.</span></span> <span data-ttu-id="b30ee-113">Die Integrationskennungen aus den Projektausgabenkategorien werden dann über Synchronisierung von Project Service Automation nach Finance and Operations synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="b30ee-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="b30ee-114">Wenn die Projektausgabenkategorien in der Project Service Automation erfolgt, ist der Integrationsfluss zuerst von Project Service Automation zu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b30ee-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="b30ee-115">Die Projektkategorien müssen in Finance and Operations bereits vor der Synchronisierung von Project Service Automation konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="b30ee-115">The project categories must already be configured in Finance and Operations before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="b30ee-116">Dann synchronisieren Sie von Finance and Operations zurück zu Project Service Automation und dann von Project Service Automation zu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b30ee-116">Then synchronize from Finance and Operations back to Project Service Automation, and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="b30ee-117">Auf diese Weise können Sie sicherstellen, dass die Kategorien verknüpft sind und dass keine Duplikate erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b30ee-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="b30ee-118">Normalerweise werden die Projektausgabenkategorien in Finance and Operations abgewickelt.</span><span class="sxs-lookup"><span data-stu-id="b30ee-118">Typically, the project expense categories are mastered in Finance and Operations.</span></span> <span data-ttu-id="b30ee-119">Wenn sie jedoch nicht in Finance and Operations erfolgreich gehandhabt werden, oder wenn Ausgabenkategorien bereits in Project Service Automation erstellt wurden, müssen Sie zuerst mithilfe der Vorlage für Projektausgaben-Transaktionskategorien (PSA zu Fin and Ops) synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b30ee-119">However, if they aren't mastered in Finance and Operations, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="b30ee-120">Synchronisieren Sie dann mithilfe der Vorlage für Projektausgaben-Transaktionskategorien (Fin and Ops zu PSA).</span><span class="sxs-lookup"><span data-stu-id="b30ee-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="b30ee-121">Sie sollten dann die Synchronisierung von Project Service Automation nach Finance and Operations noch einmal ausführen.</span><span class="sxs-lookup"><span data-stu-id="b30ee-121">You should then run the synchronization from Project Service Automation to Finance and Operations one more time.</span></span>
>
> <span data-ttu-id="b30ee-122">Wenn Sie zuerst von Project Service Automation synchronisieren, müssen die folgenden Anforderungen in Finance and Operations erfüllt sein, bevor die Synchronisierung ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="b30ee-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance and Operations before the synchronization is run:</span></span>
>
> - <span data-ttu-id="b30ee-123">Die freigegebene Kategorie, die mit der Projektkategorie übereinstimmt, die in Project Service Automation eingerichtet ist, muss vorhanden sein, und sie muss sowohl für **Projekt** als auch **Ausgaben** aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="b30ee-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="b30ee-124">Für jede juristische Finance and Operations-Person, mit der eine Integration hergestellt werden muss, müssen die folgenden Projektkategorien vorhanden sein:</span><span class="sxs-lookup"><span data-stu-id="b30ee-124">For each Finance and Operations legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="b30ee-125">**Projektkategorie** ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b30ee-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="b30ee-126">**In Ausgaben verwenden** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b30ee-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="b30ee-127">**Aktiv in der Erfassung** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b30ee-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="b30ee-128">**Transaktionstyp** ist auf **Ausgaben** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b30ee-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="b30ee-129">Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b30ee-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="b30ee-130">[![Datenfluss für Project Service Automation Integration mit Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="b30ee-130">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a><span data-ttu-id="b30ee-131">Projektausgabenkategorie-Synchronisierung von Finance and Operations nach Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b30ee-131">Project expense category synchronization from Finance and Operations to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="b30ee-132">Vorlage und Aufgabe</span><span class="sxs-lookup"><span data-stu-id="b30ee-132">Template and task</span></span>

<span data-ttu-id="b30ee-133">Wenn Sie auf die Vorlage im Microsoft PowerApps-Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b30ee-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b30ee-134">Die folgende Vorlage und zugrunde liegende Aufgabe werden verwendet, um Projektausgabenkategorien von Finance and Operations mit Project Service Automation zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="b30ee-134">The following template and underlying task are used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="b30ee-135">**Name der Vorlage in der Datenintegration:** Projekctausgabentransaktionskategorien (Fin and Ops zu PSA)</span><span class="sxs-lookup"><span data-stu-id="b30ee-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="b30ee-136">**Name der Aufgabe im Projekt:** Synchronisierungskategorien zu PSA</span><span class="sxs-lookup"><span data-stu-id="b30ee-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="b30ee-137">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="b30ee-137">Entity set</span></span>

| <span data-ttu-id="b30ee-138">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b30ee-138">Finance and Operations</span></span>            | <span data-ttu-id="b30ee-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b30ee-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="b30ee-140">Integrationsentität für Kategorien</span><span class="sxs-lookup"><span data-stu-id="b30ee-140">Integration entity for categories</span></span> | <span data-ttu-id="b30ee-141">Transaktionskategorien</span><span class="sxs-lookup"><span data-stu-id="b30ee-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="b30ee-142">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="b30ee-142">Entity flow</span></span>

<span data-ttu-id="b30ee-143">Projektausgaben werden in Finance and Operations verwaltet und dann zu Project Service Automation als Transaktionskategorien synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="b30ee-143">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="b30ee-144">Powerabfrage</span><span class="sxs-lookup"><span data-stu-id="b30ee-144">Power Query</span></span>

<span data-ttu-id="b30ee-145">Wenn Sie mit Project Service Automation synchronisieren, müssen Sie Microsoft Power Query für Excel nutzen, um den Fakturierungstyps für die Transaktionskategorie festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b30ee-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="b30ee-146">Die Vorlage für Projektausgaben-Transaktionskategorien (Fin and Ops zu PSA) bietet eine Standardspalte und -zuordnung.</span><span class="sxs-lookup"><span data-stu-id="b30ee-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="b30ee-147">Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie eine bedingte Spalte in der Power-Abfrage hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b30ee-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="b30ee-148">Führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="b30ee-148">Follow these steps.</span></span>

1. <span data-ttu-id="b30ee-149">Klicken Sie auf den Pfeil, um die Zuordnung der Projektausgaben-Kategorieaufgabe in der Vorlage für Projektausgaben-Transaktionskategorien (Fin and Ops zu PSA) zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b30ee-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="b30ee-150">Klicken Sie auf den Link **Erweiterte Abfrage und Filterung**, um Power Query zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b30ee-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="b30ee-151">Wählen Sie **Hinzufügen von bedingten Spalten** aus.</span><span class="sxs-lookup"><span data-stu-id="b30ee-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="b30ee-152">Geben Sie einen Namen für die neue Spalte ein, wie beispielsweise **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="b30ee-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="b30ee-153">Geben Sie die folgende Bedingung ein: **wenn CATEGORYID ungleich null dann 19235001, ansonsten null**.</span><span class="sxs-lookup"><span data-stu-id="b30ee-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="b30ee-154">Klicken Sie **OK** in der Spalte.</span><span class="sxs-lookup"><span data-stu-id="b30ee-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="b30ee-155">Stellen Sie sicher, dass Sie diese neue Spalte auf der Zuordnungsseite zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="b30ee-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="b30ee-156">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="b30ee-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="b30ee-157">Die Zuordnung zeigt, welche Feldinformationen von Finance and Operations zu Project Service Automation synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b30ee-157">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="b30ee-158">[![Vorlagenzuordnung](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b30ee-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="b30ee-159">Projektausgabenkategorie-Synchronisierung von Project Service Automation nach Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b30ee-159">Project expense category synchronization from Project Service Automation to Finance and Operations</span></span>

### <a name="template-and-task"></a><span data-ttu-id="b30ee-160">Vorlage und Aufgabe</span><span class="sxs-lookup"><span data-stu-id="b30ee-160">Template and task</span></span>

<span data-ttu-id="b30ee-161">Die folgende Vorlage und zugrunde liegende Aufgabe werden verwendet, um Projektausgabenkategorien von Project Service Automation mit Finance and Operations zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="b30ee-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="b30ee-162">**Name der Vorlage in der Datenintegration:** Projektausgaben-Transaktionskategorien (Fin and Ops zu PSA)</span><span class="sxs-lookup"><span data-stu-id="b30ee-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="b30ee-163">**Name der Aufgabe im Projekt:** Synchronisierungskategorien nach Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b30ee-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="b30ee-164">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="b30ee-164">Entity set</span></span>

| <span data-ttu-id="b30ee-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b30ee-165">Project Service Automation</span></span> | <span data-ttu-id="b30ee-166">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b30ee-166">Finance and Operations</span></span>            |
|----------------------------|-----------------------------------|
| <span data-ttu-id="b30ee-167">Transaktionskategorien</span><span class="sxs-lookup"><span data-stu-id="b30ee-167">Transaction categories</span></span>     | <span data-ttu-id="b30ee-168">Integrationsentität für Kategorien</span><span class="sxs-lookup"><span data-stu-id="b30ee-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="b30ee-169">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="b30ee-169">Entity flow</span></span>

<span data-ttu-id="b30ee-170">Projektausgaben werden in Finance and Operations verwaltet und dann zu Project Service Automation als Transaktionskategorien synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="b30ee-170">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="b30ee-171">Die Rücksynchronisierung mit Finance and Operations aktualisiert die Projektkategorie in Finance and Operations mit der Integrationskennung aus Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b30ee-171">The synchronization back to Finance and Operations updates the project category in Finance and Operations with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b30ee-172">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="b30ee-172">Template mapping in Data integration</span></span>

<span data-ttu-id="b30ee-173">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="b30ee-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="b30ee-174">Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b30ee-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="b30ee-175">[![Vorlagenzuordnung](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b30ee-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
