---
title: Einzelhandelskanäle definieren und verwalten
description: Dieses Thema bietet einen Überblick über den Prozess für das Einrichten von physischen Shops, die in Dynamics 365 Commerce als Geschäfte bezeichnet werden. Er umfasst Informationen über die Aufgaben, die Sie durchführen müssen, bevor und nachdem Sie ein Geschäft einrichten.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 51524ad6918d962d70a8a700f135f96e236f7d34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000874"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="7d387-104">Definieren und Verwalten von Retail-Kanälen</span><span class="sxs-lookup"><span data-stu-id="7d387-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7d387-105">Dieses Thema bietet einen Überblick über den Prozess für das Einrichten von physischen Shops, die in Dynamics 365 Commerce als Geschäfte bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="7d387-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="7d387-106">Er umfasst Informationen über die Aufgaben, die Sie durchführen müssen, bevor und nachdem Sie ein Geschäft einrichten.</span><span class="sxs-lookup"><span data-stu-id="7d387-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="7d387-107">Commerce unterstützt mehrere Einzelhandelskanäle wie Onlineshops, Callcenter und physische Shops.</span><span class="sxs-lookup"><span data-stu-id="7d387-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="7d387-108">Ein physischer Laden wird Geschäft genannt.</span><span class="sxs-lookup"><span data-stu-id="7d387-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="7d387-109">Jeder Shop kann seine eigenen Zahlungsmethoden, Preisgruppen, POS-Register, Ein- und Ausgabenkonten und Mitarbeiter einrichten.</span><span class="sxs-lookup"><span data-stu-id="7d387-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="7d387-110">Sie müssen alle Elemente für ein Geschäft einrichten, bevor Sie ihn erstellen.</span><span class="sxs-lookup"><span data-stu-id="7d387-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="7d387-111">Nachdem Sie ein Geschäft erstellt haben, weisen Sie die Produkte zu, die der Shop umfassen soll.</span><span class="sxs-lookup"><span data-stu-id="7d387-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="7d387-112">Sie ordnen außerdem Mitarbeiter, Register und Debitoren der Filiale zu.</span><span class="sxs-lookup"><span data-stu-id="7d387-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="7d387-113">Fügen Sie den neuen Shop schließlich zu einer Organisationshierarchie hinzu.</span><span class="sxs-lookup"><span data-stu-id="7d387-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="7d387-114">Einrichten von Shops</span><span class="sxs-lookup"><span data-stu-id="7d387-114">Setting up stores</span></span>

<span data-ttu-id="7d387-115">Bevor Sie einen Einzelhandelsshop in Commerce einrichten können, müssen Sie mehrere erforderliche Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d387-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="7d387-116">Sie können dann das Geschäft erstellen und Details hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7d387-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7d387-117">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="7d387-117">Prerequisites</span></span>

<span data-ttu-id="7d387-118">Bevor Sie ein Geschäft einrichten können, müssen Sie die folgenden erforderlichen Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="7d387-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="7d387-119">Konfigurieren Sie Ihre Organisationsstruktur und Einstellungsorganisationshierarchien für Einzelhandelssortimente, Auffüllung und Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="7d387-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="7d387-120">Einrichten eines Lagerorts, der das Geschäft abbildet.</span><span class="sxs-lookup"><span data-stu-id="7d387-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="7d387-121">Richten Sie Nummernkreise für Geschäfte, Lageraufstellungen und Auszugsbelege ein.</span><span class="sxs-lookup"><span data-stu-id="7d387-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="7d387-122">Parameter für Commerce konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7d387-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="7d387-123">Richten Sie die Zahlungsmethoden ein, die im Shop akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="7d387-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="7d387-124">Für die Verarbeitung von Kreditkartentransaktionen an POS-Kassen können Sie auch Zahlungsdienste einrichten.</span><span class="sxs-lookup"><span data-stu-id="7d387-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="7d387-125">Mehrwertsteuergruppen einrichten.</span><span class="sxs-lookup"><span data-stu-id="7d387-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="7d387-126">Produkte einrichten.</span><span class="sxs-lookup"><span data-stu-id="7d387-126">Set up products.</span></span> <span data-ttu-id="7d387-127">Als Teil dieser Aufgabe richten Sie auch Produkthierarchien, Produktvarianten und Sortimente ein.</span><span class="sxs-lookup"><span data-stu-id="7d387-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="7d387-128">Einrichten von Produktpreisgruppen.</span><span class="sxs-lookup"><span data-stu-id="7d387-128">Set up product price groups.</span></span>
10. <span data-ttu-id="7d387-129">Produktpreise einrichten.</span><span class="sxs-lookup"><span data-stu-id="7d387-129">Set up product pricing.</span></span> <span data-ttu-id="7d387-130">Als Teil dieser Aufgabe richten Sie auch Preisregulierungen, Rabatte und Rabattzeiträume ein.</span><span class="sxs-lookup"><span data-stu-id="7d387-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="7d387-131">Einrichten von Mitarbeitern.</span><span class="sxs-lookup"><span data-stu-id="7d387-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d387-132">Sie müssen die entsprechenden Berechtigungen den Arbeitskräften zuweisen, sodass diese sich anmelden und Aufgaben mit dem POS-System ausführen können.</span><span class="sxs-lookup"><span data-stu-id="7d387-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="7d387-133">Konfigurieren der POS-Profile, um sie dem Geschäft zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="7d387-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="7d387-134">Diese Aufgabe beinhaltet zahlreiche weitere Aufgaben, wie das Einrichten von Registern, Einrichten von Offlineprofilen, und das Einrichten von Bonformaten und Profilen.</span><span class="sxs-lookup"><span data-stu-id="7d387-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="7d387-135">Prüfen Sie alle Aufgaben, die Voraussetzung sind, und führen Sie nur die Aufgaben aus, die für Sie gelten.</span><span class="sxs-lookup"><span data-stu-id="7d387-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="7d387-136">Ein Geschäft einrichten</span><span class="sxs-lookup"><span data-stu-id="7d387-136">Set up a store</span></span>

<span data-ttu-id="7d387-137">Nach Abschluss der erforderlichen Aufgaben, führen Sie diese Aufgaben aus, um die Details für das Geschäft einzurichten:</span><span class="sxs-lookup"><span data-stu-id="7d387-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="7d387-138">Erstellen Sie einen Shop.</span><span class="sxs-lookup"><span data-stu-id="7d387-138">Create a store.</span></span>
2. <span data-ttu-id="7d387-139">Eine Mehrwertsteuergruppe dem Shop zuweisen.</span><span class="sxs-lookup"><span data-stu-id="7d387-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="7d387-140">Die angenommenen Zahlungsmethoden dem Shop zuweisen.</span><span class="sxs-lookup"><span data-stu-id="7d387-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="7d387-141">Fügen Sie Details zu den Produktbeschreibungen für Produkte hinzu, die Sie in den Geschäften anbieten.</span><span class="sxs-lookup"><span data-stu-id="7d387-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="7d387-142">Sie können beispielsweise Rich-Text und Bilder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7d387-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="7d387-143">Diese Produktdetails werden in verschiedenen Kontexten, wie auf der POS-Kasse oder auf gedruckten Beschriftungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d387-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="7d387-144">Fügen Sie den Shop zu einer Organisationshierarchie hinzu, die für ein **Sales-Sortiment**, eine **Sales-Auffüllung** oder die **Berichterstellung in Sales** zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7d387-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="7d387-145">Nachdem Sie ein Geschäft einrichten</span><span class="sxs-lookup"><span data-stu-id="7d387-145">After you set up a store</span></span>

<span data-ttu-id="7d387-146">Nachdem Sie die Details für das Geschäft eingeben, schließen Sie diese Aufgaben ab, um die neuen Geschäftdaten an POS zu senden.</span><span class="sxs-lookup"><span data-stu-id="7d387-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="7d387-147">Konfigurieren der POS-Kassen für den Shop.</span><span class="sxs-lookup"><span data-stu-id="7d387-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="7d387-148">Weisen Sie dem Shop Produktsortimente zu.</span><span class="sxs-lookup"><span data-stu-id="7d387-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="7d387-149">Sortimente verarbeiten, um die Liste der Produkte zu generieren, die im Sortiment berücksichtigt werden, und um die Produkte im Geschäft verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="7d387-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="7d387-150">Senden Sie Daten wie Nummernkreise, Hardwareprofile, POS-Bildschirmlayouts, usw. zu den POS-Kassen.</span><span class="sxs-lookup"><span data-stu-id="7d387-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="7d387-151">Veröffentlichen Sie das Geschäft, um Ladendaten an POS zu senden.</span><span class="sxs-lookup"><span data-stu-id="7d387-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="7d387-152">Führen Sie die Jobs aus, um die Speicherdaten an POS zu senden.</span><span class="sxs-lookup"><span data-stu-id="7d387-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="7d387-153">Organisationshierarchien</span><span class="sxs-lookup"><span data-stu-id="7d387-153">Organization hierarchies</span></span>

<span data-ttu-id="7d387-154">Commerce verwendet Organisationshierarchien, um Kanäle zu strukturieren.</span><span class="sxs-lookup"><span data-stu-id="7d387-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="7d387-155">Organisationshierarchien stellen die Beziehungen zwischen den Organisationen dar, aus denen das Unternehmen besteht.</span><span class="sxs-lookup"><span data-stu-id="7d387-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="7d387-156">Wenn Sie Filialen einrichten, können Sie diese einer Organisationshierarchie hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7d387-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="7d387-157">Die Filialen teilen dann Daten, die für Sortimente, Auffüllung und Berichterstellung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d387-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="7d387-158">Um die Commerce-Verkaufsfunktionalität zu nutzen, muss der Konfigurationsschlüssel für **Mehrfache Wareneingänge** aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="7d387-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="7d387-159">Diesen Konfigurationsschlüssel finden Sie in den Konfigurationsschlüsseln **Handel** unter **Systemverwaltung**\> **Einstellungen** \> **Lizenzkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="7d387-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="7d387-160">Dies ist aufgrund verschiedener Validierungen auf der Grundlage der auf der Ebene der Kundenauftragszeile konfigurierten Lieferadresse erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7d387-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>

