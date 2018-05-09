---
title: "Einzelhandelskanäle definieren und verwalten"
description: "Dieser Artikel gibt einen Überblick über den Prozess für das Einrichten von physischen Shops, die in Microsoft Dynamics 365 for Retail als Einzelhandelsshops bezeichnet werden. Er umfasst Informationen über die Aufgaben, die Sie durchführen müssen, bevor und nachdem Sie ein Einzelhandelsgeschäft einrichten."
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 321673a4294e705587bbd5c1afcaab67de50bad5
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="4d980-104">Einzelhandelskanäle definieren und verwalten</span><span class="sxs-lookup"><span data-stu-id="4d980-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4d980-105">Dieser Artikel gibt einen Überblick über den Prozess für das Einrichten von physischen Shops, die in Microsoft Dynamics 365 for Retail als Einzelhandelsshops bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="4d980-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="4d980-106">Er umfasst Informationen über die Aufgaben, die Sie durchführen müssen, bevor und nachdem Sie ein Einzelhandelsgeschäft einrichten.</span><span class="sxs-lookup"><span data-stu-id="4d980-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="4d980-107">Dynamics 365 for Retail unterstützt mehrere Einzelhandelskanäle, wie Onlineshops, Call-Center und physische Läden.</span><span class="sxs-lookup"><span data-stu-id="4d980-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="4d980-108">Ein physischer Laden wird Einzelhandelsshop genannt.</span><span class="sxs-lookup"><span data-stu-id="4d980-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="4d980-109">Jeder Einzelhandelsshop kann seine eigenen Zahlungsmethoden, Preisgruppen, POS-Register, Ein- und Ausgabenkonten und Mitarbeiter einrichten.</span><span class="sxs-lookup"><span data-stu-id="4d980-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="4d980-110">Sie müssen alle Elemente für einen Shop einrichten, bevor Sie ihn erstellen.</span><span class="sxs-lookup"><span data-stu-id="4d980-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="4d980-111">Nachdem Sie einen Einzelhandelsshop erstellt haben, weisen Sie die Produkte zu, die der Shop umfassen soll.</span><span class="sxs-lookup"><span data-stu-id="4d980-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="4d980-112">Sie ordnen außerdem Mitarbeiter, Register und Debitoren der Filiale zu.</span><span class="sxs-lookup"><span data-stu-id="4d980-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="4d980-113">Fügen Sie den neuen Shop schließlich zu einer Organisationshierarchie hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d980-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="4d980-114">Einrichten von Einzelhandelsgeschäften</span><span class="sxs-lookup"><span data-stu-id="4d980-114">Setting up retail stores</span></span>
<span data-ttu-id="4d980-115">Bevor Sie einen Einzelhandelsshop in Microsoft Dynamics 365 for Retail einrichten können, müssen Sie mehrere erforderliche Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d980-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="4d980-116">Sie können dann den Shop erstellen und Details hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4d980-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4d980-117">Erforderliche Komponenten</span><span class="sxs-lookup"><span data-stu-id="4d980-117">Prerequisites</span></span>

<span data-ttu-id="4d980-118">Bevor Sie einen Einzelhandelsshop einrichten können, müssen Sie die folgenden erforderlichen Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="4d980-118">You must complete the following tasks before you can set up a retail store:</span></span>

1.  <span data-ttu-id="4d980-119">Konfigurieren Sie Ihre Organisationsstruktur und Einstellungsorganisationshierarchien für Einzelhandelssortimente, Auffüllung und Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="4d980-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2.  <span data-ttu-id="4d980-120">Einrichten eines Lagerorts, der den Einzelhandelsshop abbildet.</span><span class="sxs-lookup"><span data-stu-id="4d980-120">Set up a warehouse that represents the retail store.</span></span>
3.  <span data-ttu-id="4d980-121">Richten Sie Nummernkreise für Einzelhandelsshops, Lageraufstellungen und Auszugsbelege ein.</span><span class="sxs-lookup"><span data-stu-id="4d980-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4.  <span data-ttu-id="4d980-122">Parameter für Einzelhandel konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4d980-122">Configure parameters for Retail.</span></span>
5.  <span data-ttu-id="4d980-123">Richten Sie die Zahlungsmethoden ein, die im Shop akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="4d980-123">Set up the methods of payment that the store accepts.</span></span>
6.  <span data-ttu-id="4d980-124">Um Kreditkartenbuchungen an POS-Kassen zu verarbeiten, können Sie Zahlungsdienste einrichten.</span><span class="sxs-lookup"><span data-stu-id="4d980-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7.  <span data-ttu-id="4d980-125">Mehrwertsteuergruppen einrichten.</span><span class="sxs-lookup"><span data-stu-id="4d980-125">Set up sales tax groups.</span></span>
8.  <span data-ttu-id="4d980-126">Einrichten von Einzelhandelsprodukten.</span><span class="sxs-lookup"><span data-stu-id="4d980-126">Set up retail products.</span></span> <span data-ttu-id="4d980-127">Als Teil dieser Aufgabe richten Sie auch Produkthierarchien, Produktvarianten und Sortimente ein.</span><span class="sxs-lookup"><span data-stu-id="4d980-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9.  <span data-ttu-id="4d980-128">Einrichten von Produktpreisgruppen.</span><span class="sxs-lookup"><span data-stu-id="4d980-128">Set up product price groups.</span></span>
10. <span data-ttu-id="4d980-129">Einrichten von Einzelhandelsproduktpreiskalkulation.</span><span class="sxs-lookup"><span data-stu-id="4d980-129">Set up retail product pricing.</span></span> <span data-ttu-id="4d980-130">Als Teil dieser Aufgabe richten Sie auch Preisregulierungen, Rabatte und Rabattzeiträume ein.</span><span class="sxs-lookup"><span data-stu-id="4d980-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="4d980-131">Einrichten von Mitarbeitern.</span><span class="sxs-lookup"><span data-stu-id="4d980-131">Set up staff members.</span></span> <span data-ttu-id="4d980-132">**Hinweis:** Sie müssen den Arbeitskräften die entsprechenden Berechtigungen zuweisen, sodass diese sich anmelden und Aufgaben mit dem Microsoft Dynamics 365 for Retail für Retail POS-System ausführen können.</span><span class="sxs-lookup"><span data-stu-id="4d980-132">**Note:** You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>
12. <span data-ttu-id="4d980-133">Konfigurieren der Retail POS-Profile, um sie dem Shop zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="4d980-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="4d980-134">Diese Aufgabe beinhaltet zahlreiche weitere Aufgaben, wie das Einrichten von Registern, Einrichten von Offlineprofilen, und das Einrichten von Bonformaten und Profilen.</span><span class="sxs-lookup"><span data-stu-id="4d980-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="4d980-135">Prüfen Sie alle Aufgaben, die Voraussetzung sind, und führen Sie nur die Aufgaben aus, die für Sie gelten.</span><span class="sxs-lookup"><span data-stu-id="4d980-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="4d980-136">Einrichten eines Einzelhandelsgeschäfts</span><span class="sxs-lookup"><span data-stu-id="4d980-136">Set up a retail store</span></span>

<span data-ttu-id="4d980-137">Nach Abschluss der erforderlichen Aufgaben, führen Sie diese Aufgaben aus, um die Details für den Einzelhandelsshop einzurichten:</span><span class="sxs-lookup"><span data-stu-id="4d980-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1.  <span data-ttu-id="4d980-138">Erstellt einen Einzelhandelsshop.</span><span class="sxs-lookup"><span data-stu-id="4d980-138">Create a retail store.</span></span>
2.  <span data-ttu-id="4d980-139">Eine Mehrwertsteuergruppe dem Shop zuweisen.</span><span class="sxs-lookup"><span data-stu-id="4d980-139">Assign a sales tax group to the store.</span></span>
3.  <span data-ttu-id="4d980-140">Die angenommenen Zahlungsmethoden dem Shop zuweisen.</span><span class="sxs-lookup"><span data-stu-id="4d980-140">Assign the accepted payment methods to the store.</span></span>
4.  <span data-ttu-id="4d980-141">Fügen Sie Details zu den Produktbeschreibungen für Produkte hinzu, die Sie in den Einzelhandelsgeschäften anbieten.</span><span class="sxs-lookup"><span data-stu-id="4d980-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="4d980-142">Sie können beispielsweise Rich-Text und Bilder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4d980-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="4d980-143">Diese Produktdetails werden in verschiedenen Kontexten, wie auf der POS-Kasse oder auf gedruckten Beschriftungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4d980-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5.  <span data-ttu-id="4d980-144">Fügen Sie den Shop zu einer Organisationshierarchie hinzu, die für ein **Sales-Sortiment**, eine **Sales-Auffüllung** oder die **Berichterstellung in Sales** zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4d980-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="4d980-145">Nachdem Sie einen Einzelhandelsshop einrichten</span><span class="sxs-lookup"><span data-stu-id="4d980-145">After you set up a retail store</span></span>

<span data-ttu-id="4d980-146">Nachdem Sie die Details für den Einzelhandelsshop eingeben, schließen Sie diese Aufgaben ab, um die neuen Einzelhandelshopdaten an Retail-POS zu senden.</span><span class="sxs-lookup"><span data-stu-id="4d980-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1.  <span data-ttu-id="4d980-147">Konfigurieren der POS-Kassen für den Shop.</span><span class="sxs-lookup"><span data-stu-id="4d980-147">Configure the POS registers for the store.</span></span>
2.  <span data-ttu-id="4d980-148">Weisen Sie dem Shop Produktsortimente zu.</span><span class="sxs-lookup"><span data-stu-id="4d980-148">Assign product assortments to the store.</span></span>
3.  <span data-ttu-id="4d980-149">Sortimente verarbeiten, um die Liste der Produkte zu generieren, die im Sortiment berücksichtigt werden, und um die Produkte im Einzelhandelsshop verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="4d980-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4.  <span data-ttu-id="4d980-150">Senden Sie Daten wie Nummernkreise, Hardwareprofile, POS-Bildschirmlayouts, usw. zu den Retail POS-Kassen.</span><span class="sxs-lookup"><span data-stu-id="4d980-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5.  <span data-ttu-id="4d980-151">Veröffentlichen Sie das Einzelhandelsgeschäft, um Ladendaten an Retail POS zu senden.</span><span class="sxs-lookup"><span data-stu-id="4d980-151">Publish the retail store to send store data to Retail POS.</span></span>
6.  <span data-ttu-id="4d980-152">Führen Sie die Einzelvorgänge aus, um die Speicherdaten zu Retail POS zu senden.</span><span class="sxs-lookup"><span data-stu-id="4d980-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="4d980-153">Organisationshierarchien</span><span class="sxs-lookup"><span data-stu-id="4d980-153">Organization hierarchies</span></span>
<span data-ttu-id="4d980-154">Retail verwendet Organisationshierarchien, um Einzelhandelskanäle zu strukturieren.</span><span class="sxs-lookup"><span data-stu-id="4d980-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="4d980-155">Organisationshierarchien stellen die Beziehungen zwischen den Organisationen dar, aus denen das Unternehmen besteht.</span><span class="sxs-lookup"><span data-stu-id="4d980-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="4d980-156">Wenn Sie Filialen einrichten, können Sie diese einer Organisationshierarchie hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4d980-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="4d980-157">Die Filialen teilen dann Daten, die für Sortimente, Auffüllung und Berichterstellung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d980-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>




