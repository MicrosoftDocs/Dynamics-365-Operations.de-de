---
title: Erstellen und Verarbeiten von Qualitätsmängeln
description: Dieses Thema beschreibt, wie Sie das Management von Qualitätsmängeln auf der Basis eines bestehenden Qualitätsprüfungsauftrags durchführen können.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956205"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="6fcd4-103">Erstellen und Verarbeiten von Qualitätsmängeln</span><span class="sxs-lookup"><span data-stu-id="6fcd4-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6fcd4-104">Dieses Thema beschreibt, wie Sie das Management von Qualitätsmängeln auf der Basis eines bestehenden Qualitätsprüfungsauftrags durchführen können.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="6fcd4-105">Typischerweise wird das Qualitätsmangel-Management von einem Qualitätssachbearbeiter durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="6fcd4-106">Als Voraussetzung müssen Sie einen Qualitätsprüfungsauftrag zur Verfügung haben.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="6fcd4-107">(Informationen zum Erstellen eines Qualitätsprüfungsauftrags finden Sie unter [Prüfen der Qualität von Waren](inspect-quality-goods.md).)</span><span class="sxs-lookup"><span data-stu-id="6fcd4-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="6fcd4-108">Bevor ein Benutzer die Genehmigung eines Qualitätsmangels verarbeiten kann, muss ihm ein worker im Feld **Person** auf der Seite **Benutzer** zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="6fcd4-109">Zusätzlich muss in den Benutzeroptionen die Option **Dokumentenbearbeitung aktivieren** auf *Ja* festgelegt werden, bevor der Benutzer die Dokumentennotizen verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="6fcd4-110">Erstellen einer Nichtübereinstimmung</span><span class="sxs-lookup"><span data-stu-id="6fcd4-110">Create a nonconformance</span></span>

<span data-ttu-id="6fcd4-111">Um einen Qualitätsmangel zu erstellen, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="6fcd4-112">Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="6fcd4-113">Wählen Sie im Aktivitätsbereich **Neu**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="6fcd4-114">Wählen Sie im Dialogfeld **Nichtkonformität erstellen** im Feld **Problemtyp** die Art des Problems, das während des Inspektionsprozesses gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="6fcd4-115">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="6fcd4-116">Einen Qualitätsmangel genehmigen oder ablehnen</span><span class="sxs-lookup"><span data-stu-id="6fcd4-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="6fcd4-117">Um einen Qualitätsmangel zu genehmigen oder abzulehnen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="6fcd4-118">Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="6fcd4-119">Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fcd4-120">Sie können eine Korrektur nur zu Qualitätsmängeln hinzufügen, die genehmigt sind.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="6fcd4-121">Wählen Sie im Aktivitätsbereich **Funktionen \> Qualitätsmangel genehmigen**, um den Qualitätsmangel zu genehmigen oder **Funktionen \> Qualitätsmangel ablehnen**, um ihn abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="6fcd4-122">Sie können genehmigte Qualitätsmängel mit [verwandten Vorgängen](../quality-operations.md) verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="6fcd4-123">Auf diese Weise können Sie die Arbeit, die im Rahmen der Behandlung von Qualitätsmängeln und der Verarbeitung von Korrekturen geleistet wird, in Datensätzen festhalten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="6fcd4-124">Sie werden aufgefordert, Ihre Auswahl zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="6fcd4-125">Wählen Sie **Ja** aus, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="6fcd4-126">Hinzufügen von Vorgängen und anderen Details zu Qualitätsmängeln</span><span class="sxs-lookup"><span data-stu-id="6fcd4-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="6fcd4-127">Nachdem Sie einen Qualitätsmangel erstellt haben, können Sie beginnen, verwandte Vorgänge hinzuzufügen und zusätzliche Informationen zu diesen Vorgängen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="6fcd4-128">Sie können verwandte Vorgänge nur für Qualitätsmängel hinzufügen, die genehmigt sind.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="6fcd4-129">Neben den Basisinformationen können Sie einem Vorgang die folgenden Details hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="6fcd4-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="6fcd4-130">**Elemente** – Sie können eine Liste von Elementen erstellen, die verbraucht werden, um die Korrektur durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="6fcd4-131">Bei den Elementen kann es sich z. B. um Produkte handeln, die zur Reparatur von Geräten benötigt werden, oder um Zutaten, die zur Nachbearbeitung eines Fertigprodukts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="6fcd4-132">**Qualitätsbelastungen** – Sie können eine Liste von Belastungen erstellen, die angefallen sind oder nach außen abgerechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="6fcd4-133">**Arbeitszeitnachweis** – Sie können ein Protokoll über die Zeit erstellen, die jeder worker mit dem Vorgang verbringt.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="6fcd4-134">Die übrigen Einstellungen sind optional.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-134">The remaining settings are optional.</span></span> <span data-ttu-id="6fcd4-135">Die Kosten für jedes Element, die Qualitätsbelastungen und die Zeittabelle werden summiert und auf dem Vorgang angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="6fcd4-136">Sie können das Feld **Kalkulation** im Vorgang nicht direkt bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="6fcd4-137">Erzeugen eines Vorgangs für einen Qualitätsmangel</span><span class="sxs-lookup"><span data-stu-id="6fcd4-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="6fcd4-138">Um einen Vorgang für einen Qualitätsmangel zu erstellen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="6fcd4-139">Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="6fcd4-140">Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fcd4-141">Sie können Vorgänge nur für Qualitätsmängel, die genehmigt sind, hinzufügen oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="6fcd4-142">Wählen Sie im Aktivitätsbereich **Bezogene Vorgänge**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="6fcd4-143">Wählen Sie auf der Seite **Bezogene Vorgänge** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="6fcd4-144">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="6fcd4-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="6fcd4-145">**Vorgang** – Wählen Sie den Code des Vorgangs, der für den Qualitätsmangel durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="6fcd4-146">**Grund** – Geben Sie eine detaillierte Beschreibung ein, die erklärt, warum der Vorgang erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="6fcd4-147">**Verkaufsauftrag** – Wenn sich der gewählte Vorgangscode auf die Art des Verkaufsauftrags bezieht, wählen Sie den Verkaufsauftrag, mit dem Sie den Vorgang verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="6fcd4-148">**Einkaufsbestellung** – Wenn der gewählte Vorgangscode mit der Art der Bestellung zusammenhängt, wählen Sie die Einkaufsbestellung, mit der Sie den Vorgang verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="6fcd4-149">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="6fcd4-150">Hinzufügen von Elementen zu einem Vorgang</span><span class="sxs-lookup"><span data-stu-id="6fcd4-150">Add items to an operation</span></span>

<span data-ttu-id="6fcd4-151">Um Elemente zu einem Vorgang hinzuzufügen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="6fcd4-152">Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="6fcd4-153">Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fcd4-154">Sie können Vorgänge nur für Qualitätsmängel, die genehmigt sind, hinzufügen oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="6fcd4-155">Wählen Sie im Aktivitätsbereich **Bezogene Vorgänge**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="6fcd4-156">Wählen Sie auf der Seite **Verknüpfte Vorgänge** den Vorgang aus, dem Sie Elemente hinzufügen wollen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="6fcd4-157">Klicken Sie im Aktivitätsbereich auf **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="6fcd4-158">Wählen Sie auf der Seite **Bezogene Vorgänge** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="6fcd4-159">Legen Sie dann die folgenden Felder für die neue Zeile fest:</span><span class="sxs-lookup"><span data-stu-id="6fcd4-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="6fcd4-160">**Elementnummer** – Wählen Sie das Produkt, das als Teil des gewählten Vorgangs verbraucht wird.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="6fcd4-161">**Menge** – Geben Sie die Anzahl der Elemente an, die verbraucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fcd4-162">Sie können die Kosten für das Element im Feld **Kosten** auf der Registerkarte **Allgemein** anzeigen. Die Kosten, die dort angezeigt werden, stammen von der Kalkulation, die auf der Seite **Freigegebenes Produkt** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="6fcd4-163">Die Kalkulation kann nicht direkt auf der Seite **Bezogener Vorgang Element** aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="6fcd4-164">Die Kosten aller Elemente, die auf der Seite **Bezogene Vorgangselemente** hinzugefügt werden, werden automatisch zum Feld **Kosten** auf der Seite **Bezogene Vorgänge** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="6fcd4-165">Wiederholen Sie den vorherigen Schritt für jedes zusätzliche Element, das Sie hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="6fcd4-166">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="6fcd4-167">Hinzufügen von Qualitätsbelastungen zu einem Vorgang</span><span class="sxs-lookup"><span data-stu-id="6fcd4-167">Add quality charges to an operation</span></span>

<span data-ttu-id="6fcd4-168">Um Qualitätsbelastungen zu einem Vorgang hinzuzufügen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="6fcd4-169">Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="6fcd4-170">Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fcd4-171">Sie können Vorgänge nur für Qualitätsmängel, die genehmigt sind, hinzufügen oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="6fcd4-172">Wählen Sie im Aktivitätsbereich **Bezogene Vorgänge**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="6fcd4-173">Wählen Sie auf der Seite **Verbundene Vorgänge** den Vorgang aus, dem Sie Qualitätsbelastungen hinzufügen wollen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="6fcd4-174">Wählen Sie im Aktionsbereich **Qualitätsbelastungen**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="6fcd4-175">Wählen Sie auf der Seite **Bezogene Vorgänge Belastungen** im Aktivitätsbereich die Option **Neu**, um dem Raster eine Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="6fcd4-176">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="6fcd4-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="6fcd4-177">**Gebührencode** – Wählen Sie die Qualitätsgebühr, die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="6fcd4-178">**Beschreibung** – Geben Sie eine detaillierte Beschreibung der Gebühr ein.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="6fcd4-179">**Gebührenwert** – Geben Sie den Betrag der Gebühr ein.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="6fcd4-180">Wiederholen Sie den vorherigen Schritt für jede zusätzliche Gebühr, die Sie hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="6fcd4-181">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="6fcd4-182">Der Betrag im Feld **Gebührenwert** wird automatisch für alle Qualitätsbelastungen summiert und zu allen anderen Beträgen im Feld **Kosten** auf der Seite **Bezogene Vorgänge** addiert.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="6fcd4-183">Erstellen eines Stundenzettels für einen Vorgang</span><span class="sxs-lookup"><span data-stu-id="6fcd4-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="6fcd4-184">Führen Sie diese Schritte aus, um einem Vorgang einen Stundenzettel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="6fcd4-185">Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="6fcd4-186">Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fcd4-187">Sie können Vorgänge nur für Qualitätsmängel, die genehmigt sind, hinzufügen oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="6fcd4-188">Wählen Sie im Aktivitätsbereich **Bezogene Vorgänge**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="6fcd4-189">Wählen Sie auf der Seite **Verknüpfte Vorgänge** den Vorgang aus, zu dem Sie einen Stundenzettel hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="6fcd4-190">Wählen Sie im Aktivitätsbereich **Zeitplan**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="6fcd4-191">Wählen Sie auf der Seite **Zugehörige Vorgänge** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="6fcd4-192">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="6fcd4-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="6fcd4-193">**Datum** – Geben Sie das Datum an, an dem die Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="6fcd4-194">Standardmäßig ist dieses Feld auf das aktuelle Datum festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="6fcd4-195">**Arbeiter** – Wählen Sie den Mitarbeiter aus, der die Arbeit ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="6fcd4-196">Standardmäßig ist dieses Feld auf den worker festgelegt, der dem aktuellen Benutzer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="6fcd4-197">**Vorgangsstunden** – Geben Sie die Anzahl der Stunden ein, die an dem gewählten Vorgang gearbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="6fcd4-198">**Fakturiert** – Aktivieren Sie dieses Kontrollkästchen, wenn die Zeit einem Kunden oder Lieferanten auf einer Rechnung in Rechnung gestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fcd4-199">Sie können die Kalkulation im Feld **Kosten** auf der Registerkarte **Allgemein** sehen. Die Kalkulation erfolgt mit dem Satz, den Sie auf der Seite **Parameter der Bestandsverwaltung** definieren.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="6fcd4-200">Wiederholen Sie den vorigen Schritt für jede zusätzliche Zeile, die Sie hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="6fcd4-201">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="6fcd4-202">Der Betrag im Feld **Kosten** wird für alle Timesheet-Zeilen summiert und zu allen anderen Beträgen im Feld **Kosten** auf der Seite **Bezogene Vorgänge** addiert.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="6fcd4-203">Hinzufügen einer Korrektur zu einem Qualitätsmangel</span><span class="sxs-lookup"><span data-stu-id="6fcd4-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="6fcd4-204">Um eine Korrektur zu einem Qualitätsmangel hinzuzufügen, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="6fcd4-205">Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="6fcd4-206">Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fcd4-207">Sie können eine Korrektur nur zu Qualitätsmängeln hinzufügen, die genehmigt sind.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="6fcd4-208">Wählen Sie im Aktivitätsbereich **Korrekturen**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="6fcd4-209">Wählen Sie auf der Seite **Korrekturen** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="6fcd4-210">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="6fcd4-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="6fcd4-211">**Diagnose** – Wählen Sie den Diagnosetyp, der die Art der Korrektur, die Sie erstellen, identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="6fcd4-212">**Mitarbeiter** – Wählen Sie die Person, die für die Korrektur verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="6fcd4-213">**Korrekturpriorität** – Wählen Sie eine Option, um anzugeben, wie die Korrektur priorisiert werden soll (*Niedrig*, *Normal* oder *Hoch*).</span><span class="sxs-lookup"><span data-stu-id="6fcd4-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="6fcd4-214">**Anforderungsdatum** – Geben Sie das Datum ein, an dem die Korrekturmaßnahme angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="6fcd4-215">**Plan-Datum** – Geben Sie das Datum ein, an dem die Korrektur voraussichtlich abgeschlossen sein wird.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="6fcd4-216">**Kurzfristige Lösung** – Aktivieren Sie dieses Kontrollkästchen, wenn die Korrekturmaßnahme den Qualitätsmangel nur für kurze Zeit korrigiert.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="6fcd4-217">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="6fcd4-218">Markieren Sie eine Korrektur als abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="6fcd4-218">Mark a correction as completed</span></span>

<span data-ttu-id="6fcd4-219">Um eine Korrektur eines Qualitätsmangels als abgeschlossen zu markieren, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="6fcd4-220">Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="6fcd4-221">Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fcd4-222">Sie können eine Korrektur nur zu Qualitätsmängeln hinzufügen, die genehmigt sind.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="6fcd4-223">Wählen Sie im Aktivitätsbereich **Korrekturen**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="6fcd4-224">Wählen Sie auf der Seite **Korrekturen** im Raster die Korrektur aus, die Sie als erledigt markieren wollen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="6fcd4-225">Wählen Sie im Aktivitätsbereich **Erledigt markieren**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="6fcd4-226">Sie werden aufgefordert, Ihre Auswahl zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="6fcd4-227">Wählen Sie **OK**, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-227">Select **OK** to continue.</span></span> <span data-ttu-id="6fcd4-228">Das Feld **Erledigungsdatum und -uhrzeit** ist auf das aktuelle Datum und die aktuelle Uhrzeit festgelegt, und das Kontrollkästchen **Erledigt** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="6fcd4-229">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="6fcd4-230">Erneutes Öffnen einer abgeschlossenen Korrektur</span><span class="sxs-lookup"><span data-stu-id="6fcd4-230">Reopen a completed correction</span></span>

<span data-ttu-id="6fcd4-231">Um eine abgeschlossene Korrektur erneut zu öffnen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="6fcd4-232">Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="6fcd4-233">Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="6fcd4-234">Wählen Sie im Aktivitätsbereich **Korrekturen**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="6fcd4-235">Wählen Sie auf der Seite **Korrekturen** im Raster die Korrektur aus, die Sie wieder öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="6fcd4-236">Wählen Sie im Aktivitätsbereich **Wieder öffnen**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="6fcd4-237">Sie werden aufgefordert, Ihre Auswahl zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="6fcd4-238">Wählen Sie **OK**, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-238">Select **OK** to continue.</span></span> <span data-ttu-id="6fcd4-239">Der Wert im Feld **Erledigungsdatum und -uhrzeit** wird gelöscht, und das Kontrollkästchen **Erledigt** wird deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="6fcd4-240">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-240">Close the page.</span></span>

<span data-ttu-id="6fcd4-241">Sie können jetzt zusätzliche Bearbeitungen oder Aktualisierungen an der Korrektur vornehmen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="6fcd4-242">Wenn Sie fertig sind, können Sie die Korrektur wieder als abgeschlossen markieren.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="6fcd4-243">Qualitätsmangel schließen</span><span class="sxs-lookup"><span data-stu-id="6fcd4-243">Close a nonconformance</span></span>

<span data-ttu-id="6fcd4-244">Um einen Qualitätsmangel zu schließen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="6fcd4-245">Wechseln Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="6fcd4-246">Wählen Sie einen Qualitätsprüfungsauftrag im Raster aus.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="6fcd4-247">Wählen Sie im Aktivitätsbereich **Abfragen \> Nichtkonformitäten**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="6fcd4-248">Wählen Sie auf der Seite **Nichtkonformitäten** die Ziel-Qualitätsmängel im Raster aus.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="6fcd4-249">Wählen Sie im Aktivitätsbereich **Funktionen \> Nichtkonformität schließen**.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="6fcd4-250">Sie werden aufgefordert, Ihre Auswahl zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="6fcd4-251">Wählen Sie **Ja** aus, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="6fcd4-252">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="6fcd4-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6fcd4-253">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6fcd4-253">Additional resources</span></span>

- [<span data-ttu-id="6fcd4-254">Qualitätsmanagement – Übersicht</span><span class="sxs-lookup"><span data-stu-id="6fcd4-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="6fcd4-255">Qualitäts- und Qualitätsmangel-Management aktivieren</span><span class="sxs-lookup"><span data-stu-id="6fcd4-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="6fcd4-256">Mitarbeiter, der für die Genehmigung von Qualitätsmängeln verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="6fcd4-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="6fcd4-257">Quarantänezonen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="6fcd4-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="6fcd4-258">Diagnosetypen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="6fcd4-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="6fcd4-259">Qualitätsbelastungen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="6fcd4-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="6fcd4-260">Vorgänge für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="6fcd4-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="6fcd4-261">Qualitätsmanagement für Lagerortprozesse</span><span class="sxs-lookup"><span data-stu-id="6fcd4-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
