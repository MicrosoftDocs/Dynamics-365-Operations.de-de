---
title: Fremdarbeit
description: Dieses Thema können Sie eine, einschließlich Zulieferung exemplarischen Vorgehensweise der bei der Herstellung in Dynamics 365 Supply Chain Managementerstellen.
author: christophernread
manager: tfehr
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3e282e0676e53200b0993dd9cb2b52e08fe97dca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981455"
---
# <a name="subcontracting"></a><span data-ttu-id="1a208-103">Fremdarbeit</span><span class="sxs-lookup"><span data-stu-id="1a208-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a208-104">Dieses Thema können Sie eine, einschließlich Zulieferung exemplarischen Vorgehensweise der bei der Herstellung in Microsoft Dynamics 365 Supply Chain Management erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a208-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1a208-105">Der erste Teil dieses Themas beschreibt die Einstellungen der Daten.</span><span class="sxs-lookup"><span data-stu-id="1a208-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="1a208-106">Der zweite Teil führt Sie durch die Schritte der exemplarischen Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="1a208-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="1a208-107">Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="1a208-107">Target audience</span></span>

<span data-ttu-id="1a208-108">In diesem Thema erfahren Sie, wie Fremdarbeit der Herstellung eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="1a208-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="1a208-109">Sie können vorhandene Daten in der HQUS-juristischen Person nutzen, um die Basiseinstellungen eines Fremdarbeitsaktivitätsflusses einzurichten.</span><span class="sxs-lookup"><span data-stu-id="1a208-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="1a208-110">Die Demodaten in der HQUS-juristischen Person enthält Einstellungsparameter, die vorab eingerichtet wurden, um die Schritte in der exemplarischen Vorgehensweise zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1a208-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="1a208-111">Obwohl die exemplarische Vorgehensweise zentrale Probleme und Herausforderungen für verschiedene Rollen adressiert, kann dies vom Systemadministrator ausgeführt werden. können.</span><span class="sxs-lookup"><span data-stu-id="1a208-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="1a208-112">Vorführungsszenario</span><span class="sxs-lookup"><span data-stu-id="1a208-112">Demo scenario</span></span>

<span data-ttu-id="1a208-113">In der HQUS-juristischen Person sind Spitzenlautsprecher hergestellt.</span><span class="sxs-lookup"><span data-stu-id="1a208-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="1a208-114">Während des Fertigungsprozesses durchlaufen die Lautsprecher die drei folgenden Arbeitsgänge.</span><span class="sxs-lookup"><span data-stu-id="1a208-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="1a208-115">**Vormontage** – Das Lautsprechergehäuse wird zusammengestellt.</span><span class="sxs-lookup"><span data-stu-id="1a208-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="1a208-116">Das Material für das Gehäuse wird dem Formular Lagerort entnommen, bevor der Arbeitsgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1a208-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="1a208-117">**Beschichten** – Wenn das Lautsprechergehäuse zusammengestellt wurde, muss es überzogen sein.</span><span class="sxs-lookup"><span data-stu-id="1a208-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="1a208-118">Dieser Arbeitsgang wird von einem Lieferanten (Zulieferer) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a208-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="1a208-119">Das vormontierte Lautsprechergehäuse wird zusammen mit dem Beschichtungszulieferer mit zwei Materialien geliefert.</span><span class="sxs-lookup"><span data-stu-id="1a208-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="1a208-120">**Fertig stellen** – Wenn das vormontierte Lautsprechergehäuse durch den Zulieferer beschichtet wurde, wird es an die HQUS-juristische Person zurückgegeben, sodass die Endmontage des Lautsprechers abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1a208-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="1a208-121">Die folgende Abbildung zeigt die drei Arbeitsgängen und das Material an, das sie brauchen.</span><span class="sxs-lookup"><span data-stu-id="1a208-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![Vormontage-, Beschichtungs- und Endarbeitsgänge und das Material, das sie verbrauchen](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="1a208-123">Einrichten</span><span class="sxs-lookup"><span data-stu-id="1a208-123">Setup</span></span>

<span data-ttu-id="1a208-124">Damit Sie die exemplarischen Vorgehensweise beginnen können, müssen Sie die Daten einrichten.</span><span class="sxs-lookup"><span data-stu-id="1a208-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="1a208-125">Fertiges Produkt einrichten</span><span class="sxs-lookup"><span data-stu-id="1a208-125">Set up the finished product</span></span>

<span data-ttu-id="1a208-126">Diese Verfahren führt Sie durch das Einrichten des freigegebenen Produkts D8100, "beschichtetes Gehäuse."</span><span class="sxs-lookup"><span data-stu-id="1a208-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="1a208-127">Wählen Sie **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**, um die Seite **Details für freigegebene Produkte** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="1a208-128">Im Schnellfilterfeld geben Sie **D8100** ein, um das vorhandene freigegebene Produkt zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1a208-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![Filter für D8100 freigegebenes Produkt auf der Seite der Details für freigegebene Produkte](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="1a208-130">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Entwickler**, wählen Sie **Arbeitsplan**, um die Seite **Arbeitsplan** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="1a208-131">Die Seite **Arbeitsplan** enthält die acht Arbeitsplanversionen für D8100 freigegebenes Produkt.</span><span class="sxs-lookup"><span data-stu-id="1a208-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="1a208-132">Die acht Arbeitsplanversionen werden auf vier Arbeitsplänen auf Standort 1 und 5. Standort aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="1a208-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="1a208-133">Arbeitsplan 000400 wird für die Nachkalkulation verwendet, Arbeitsplan 00041 wird verwendet, wenn der Beschichtungsarbeitsgang ein interner Arbeitsgang und Arbeitsplan 00042 wird verwendet, wenn der Beschichtungsarbeitsgang eine externe Verarbeitung ist.</span><span class="sxs-lookup"><span data-stu-id="1a208-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![Acht Arbeitsplanversionen auf der Arbeitsplanseite](./media/subcontract03_route-page.png)

4. <span data-ttu-id="1a208-135">Im oberen Bereich im Raster **Versionen**, wählen Sie **00042** Arbeitsplanversion für Standort **5** aus.</span><span class="sxs-lookup"><span data-stu-id="1a208-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="1a208-136">Im unteren Bereich auf der Registerkarte **Überblick**, Auswahloperation **20** (**Cbnt CtSc**) im Raster.</span><span class="sxs-lookup"><span data-stu-id="1a208-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![Arbeitsgang 20 für Arbeitsplanversion 00042 für den Standort 5 ausgewählt.](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="1a208-138">Wählen Sie die Registerkarte **Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="1a208-138">Select the **General** tab.</span></span>

    <span data-ttu-id="1a208-139">Beachten Sie, dass das Feld Feld **Arbeitsplantyp** auf **Lieferant** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1a208-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="1a208-140">Dieser Wert gibt an, dass Arbeitsgang 20 (Cbnt CtSc) ein geregelter Arbeitsgang ist.</span><span class="sxs-lookup"><span data-stu-id="1a208-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![Führen Sie den Feldtyp auf den Lieferant in der Registerkarte "Allgemeines"](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="1a208-142">Wählen Sie die Registerkarte **Ressourcenanforderung**.</span><span class="sxs-lookup"><span data-stu-id="1a208-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="1a208-143">Funktionen werden verwendet, um eine zutreffender Ressource bei der Produktionsplanung zu finden.</span><span class="sxs-lookup"><span data-stu-id="1a208-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="1a208-144">Für Arbeitsgang 20 (Cbnt CtSc) beachten Sie, dass eine Ressource zwei Funktionen erfordert, nämlich **Beschichten** und **Überzogene Gehäuse**.</span><span class="sxs-lookup"><span data-stu-id="1a208-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![Beschichten und überzogene Gehäusefunktionen auf der Ressourcenanforderungsregisterkarte](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="1a208-146">Wählen Sie **Anwendbare Ressourcen**, um das Dialogfeld **Anwendbare Ressourcen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="1a208-147">Drei Ressourcen werden gesucht, die mit den Ressourcenanforderungen für den Arbeitsgang übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="1a208-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="1a208-148">Beachten Sie, dass Ressource 8851 und 8852 vom Typ **Kreditor** sind.</span><span class="sxs-lookup"><span data-stu-id="1a208-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![Drei entsprechende Ressourcen im Dialogfeld Anwendbare Ressourcen](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="1a208-150">Wählen Sie **OK**, um das Dialogfeld **Anwendbare Ressourcen** zu schließen und zur Seite **Arbeitsplan** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="1a208-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="1a208-151">Schließen Sie die Seite **Arbeitsplan**, um zur Seite **Details für freigegebene Produkte** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="1a208-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![Seite für freigegebene Produkte](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="1a208-153">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Entwickler**, wählen Sie **Stücklisten-Versionen**, um die Seite **Stücklisten-Versionen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="1a208-154">Die Seite **Stücklistenversionen** zeigt vier Stücklistenpositionen (BOM)- Versionen für freigegebenes Produkt D8100 an.</span><span class="sxs-lookup"><span data-stu-id="1a208-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="1a208-155">Stückliste 000040 wird zur Nachkalkulation und Planung verwendet, Stückliste 000041 wird verwendet, wenn der Beschichtungsarbeitsgang intern erfolgt ist und Stücklisten 000042 und 000043 werden verwendet, wenn der Beschichtungsarbeitsgang abgezogen wird.</span><span class="sxs-lookup"><span data-stu-id="1a208-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="1a208-156">Beachten Sie, dass Artikel S8050 ein Produkt vom Artikeltyp **Dienstleistung** ist.</span><span class="sxs-lookup"><span data-stu-id="1a208-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="1a208-157">Dieser Artikel stellt die Fremdarbeit dar.</span><span class="sxs-lookup"><span data-stu-id="1a208-157">This item represents the subcontracted work.</span></span>

    ![Vier Stücklistenversionen auf der Stücklistenversionsseite](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="1a208-159">Auf dem Inforegister **Stücklistenpositionen** aktivieren Sie **Bearbeiten**, um das Dialogfeld **Stücklistenposition bearbeiten** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="1a208-160">Wenn ein Produktionsauftrag für das freigegebene Produkt D8100 erstellt und vorkalkuliert wird, wird automatisch eine Bestellung für Artikel S8050 generiert.</span><span class="sxs-lookup"><span data-stu-id="1a208-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="1a208-161">Diese Bestellung wird mit dem Produktionsauftrag verknüpft.</span><span class="sxs-lookup"><span data-stu-id="1a208-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="1a208-162">Damit Bestellungen automatisch generiert werden können, müssen Sie das Feld **Positionstyp** auf **Lieferant** festlegen und der Kreditor für den Zulieferer ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="1a208-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="1a208-163">In diesem Fall ist das Kreditorenkonto US-801.</span><span class="sxs-lookup"><span data-stu-id="1a208-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="1a208-164">Beachten Sie, ob die Stücklistenposition mit dem Beschichtungsarbeitsgang durch die Arbeitsgangnummer verbunden ist (in diesem Fall 20).</span><span class="sxs-lookup"><span data-stu-id="1a208-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![Bearbeiten Sie das Stücklistenpositionsdialogfeld](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="1a208-166">Erstellen Sie ein Kennwort für Lagerarbeiter</span><span class="sxs-lookup"><span data-stu-id="1a208-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="1a208-167">Sie müssen ein Kennwort für die Lagerarbeiter definieren, die das tragbare Gerät verwenden.</span><span class="sxs-lookup"><span data-stu-id="1a208-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="1a208-168">Wählen Sie **Lagerortverwaltung \> Einstellungen \> Arbeitskraft**, um die Seite **Arbeitsbenutzer** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="1a208-169">Auf dem Inforegister **Benutzer** aktivieren Sie die Zeile für Benutzer **51** aus.</span><span class="sxs-lookup"><span data-stu-id="1a208-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![Arbeitsbenutzer-Seite](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="1a208-171">**Kennwortzurücksetzung** auswählen.</span><span class="sxs-lookup"><span data-stu-id="1a208-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="1a208-172">Wählen Sie in den Feldern **Kennwort** und **Kennwort bestätigen** und geben Sie **1** ein.</span><span class="sxs-lookup"><span data-stu-id="1a208-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="1a208-173">**Kennwortzurücksetzung** auswählen.</span><span class="sxs-lookup"><span data-stu-id="1a208-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="1a208-174">Schrittweise Vorgehensweise</span><span class="sxs-lookup"><span data-stu-id="1a208-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="1a208-175">**Szenario und Hintergrund**</span><span class="sxs-lookup"><span data-stu-id="1a208-175">**Scenario and background**</span></span>

<span data-ttu-id="1a208-176">Ein Produktionsauftrag von 10 Stück wird erstellt für Produkt D8100, "Beschichtetes Gehäuse."</span><span class="sxs-lookup"><span data-stu-id="1a208-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="1a208-177">Die Beschichtung der Gehäuse ist ein geregelter Arbeitsgang, der beim Lieferant US-801 Kreditor geleistet wird, perfekte Beschichtungs-Lösungen.</span><span class="sxs-lookup"><span data-stu-id="1a208-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="1a208-178">Der Produktionsauftrag besteht aus drei Arbeitsgängen.</span><span class="sxs-lookup"><span data-stu-id="1a208-178">The production order consists of three operations.</span></span> <span data-ttu-id="1a208-179">Im ersten Arbeitsgang wird das Gehäuse als interner Arbeitsgang vormontiert.</span><span class="sxs-lookup"><span data-stu-id="1a208-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="1a208-180">Das Material für die Vormontage ist für Entnahme im Rohmateriallagerort freigegeben.</span><span class="sxs-lookup"><span data-stu-id="1a208-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="1a208-181">Nachdem die Vormontage abgeschlossen wurde, wird das vormontierte Gehäuse zu den perfekten Beschichtungs-Lösungen zusammen mit zwei Materialien gesendet, die für den Beschichtungsarbeitsgang erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1a208-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="1a208-182">Wenn das beschichtete Gehäuse vom Lieferant zurückkommt, geht es abschließenden zur internen Assemblierung, bevor es als fertig gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="1a208-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="1a208-183">Wählen Sie **Produktionssteuerung \> Produktionsaufträge \> Alle Produktionsaufträge**, um die Seite **Alle Produktionsaufträge** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="1a208-184">Klicken Sie im Aktivitätsbereich und wählen Sie **Neuer Produktionsauftrag**, um das Dialogfeld **Produktionsauftrag erstellen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![Dialogfeld "Geplanten Produktionsauftrag erstellen".](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="1a208-186">Wählen Sie im Feld **Artikelnummer** die Option **D8100** aus.</span><span class="sxs-lookup"><span data-stu-id="1a208-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="1a208-187">Das Feld "Lagerungsdimensionen" wird angezeigt, wenn Sie die Artikelnummer auswählen.</span><span class="sxs-lookup"><span data-stu-id="1a208-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="1a208-188">Im Feld **Farbe** wählen Sie **Chrome** aus.</span><span class="sxs-lookup"><span data-stu-id="1a208-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="1a208-189">Ein Meldungsfeld angezeigt wird, die fragt, ob die aktive Versionen für die Stückliste und den Arbeitsplan eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1a208-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![Meldungsfeld](./media/subcontract13_message-box.png)

5. <span data-ttu-id="1a208-191">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="1a208-191">Select **Yes**.</span></span> 

    <span data-ttu-id="1a208-192">Im Dialogfeld **Produktionsauftrag erstellen** werden die aktiven Versionen der Stückliste und der Arbeitsplan für Produkt D8100 automatisch in den Feldern **Stücklistennummer** und **Arbeitsplannummer** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="1a208-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="1a208-193">In diesem Fall werden Stückliste **000040** und Arbeitsplan **000040** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="1a208-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="1a208-194">Für die Stückliste und Arbeitsplan wird Version 000040 zur Nachkalkulation und Planung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a208-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="1a208-195">Im Feld **Standort** wählen Sei **5** aus.</span><span class="sxs-lookup"><span data-stu-id="1a208-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="1a208-196">Im Feld **Lagerort** wählen Sie **51** aus.</span><span class="sxs-lookup"><span data-stu-id="1a208-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="1a208-197">In den Feldern **Stücklistennummer** und **Arbeitsplannummer** ändern Sie den Wert, der automatisch für **000042** ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="1a208-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a208-198">Für die Stückliste und den Arbeitsplan wird Version 000042 verwendet, um die Beschichtung des Gehäuses für Lieferant US-801 zu regeln.</span><span class="sxs-lookup"><span data-stu-id="1a208-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![Werte festgelegt im Dialogfeld Produktionsauftrag](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="1a208-200">Wählen Sie **Erstellen**, um den Produktionsauftrag zu erstellen und zur Seite **Alle Produktionsaufträge** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="1a208-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![Neuer Produktionsauftrag auf der Seite alle Produktionsaufträge](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="1a208-202">Klicken Sie im Aktivitätsbereich auf die Registerkarte **Produktionsauftrag** und wählen **Schätzung**, um das Dialogfeld **Schätzung** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![Dialogfeld Vorkalkulation](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="1a208-204">Wählen Sie **Ok**, um die Vorkalkulation zu bestätigen und kehren Sie zur Seite **Alle Produktionsaufträge** zurück.</span><span class="sxs-lookup"><span data-stu-id="1a208-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a208-205">Wenn der Produktionsauftrag vorkalkuliert wird, ist die Bestellung für Dienstleistungsartikel S8050 für Kreditor US-801 generiert.</span><span class="sxs-lookup"><span data-stu-id="1a208-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="1a208-206">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produktionsauftrag**, wählen Sie **Stückliste**, um die Seite **Stückliste** zu öffnen, in der die Stücklistenpositionen für den Produktionsauftrag angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="1a208-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="1a208-207">Für Dienstleistungsartikel S8050 beachten Suem, dass es eine Referenz zur Bestellung gibt, die erstellt wurde, als der Produktionsauftrag vorkalkuliert wurde.</span><span class="sxs-lookup"><span data-stu-id="1a208-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![Produktionsauftrags-Stücklistenposition auf der Seite Stückliste](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="1a208-209">Schließen Sie die Seite **Stückliste**, um zur Seite **Alle Produktionsaufträge** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="1a208-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="1a208-210">Klicken Sie im Aktivitätsbereich auf die Registerkarte **Zeitplan** und wählen **Aufträge planen**, um das Dialogfeld **Auftragsplanung** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="1a208-211">Füllen Sie die folgenden Werte aus:</span><span class="sxs-lookup"><span data-stu-id="1a208-211">Specify the following values:</span></span>

    - <span data-ttu-id="1a208-212">Wählen Sie im Feld **Planungsrichtung** **Vorwärts ab Lieferdatum** aus.</span><span class="sxs-lookup"><span data-stu-id="1a208-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="1a208-213">Hier können Sie die Option **Begrenzte Kapazität** auf **Ja** festlegen.</span><span class="sxs-lookup"><span data-stu-id="1a208-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![Dialogfeld Feinterinierung](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="1a208-215">Wählen Sie **OK**, um das Dialogfeld **Feinterminierung** zu schließen und zur Seite **Alle Produktionsaufträge** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="1a208-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="1a208-216">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Planung**, wählen Sie **Gantt**, um die Seite **Gantt-Diagramm - Ressourcenansicht** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="1a208-217">Im Gantt-Diagramm wird eine visuelle Übersicht bereitgestellt, die zeigt, wie Produktions-Einzelvorgänge für die Ressourcen geplant werden.</span><span class="sxs-lookup"><span data-stu-id="1a208-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="1a208-218">Beachten Sie, dass der externe Beschichtungsarbeitsgang aus drei Einzelvorgängen besteht: Ein Bearbeitungseinzelvorgänge, ein Abschluss und ein Wartezeiteinzelvorgang.</span><span class="sxs-lookup"><span data-stu-id="1a208-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![Gantt-Diagramm auf der Gantt-Diagramm-Ressourcenansichtsseite](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="1a208-220">Schließen Sie die Seite **Gantt-Diagramm - Ressourcenansicht**, um zur Seite **Alle Produktionsaufträge** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="1a208-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="1a208-221">Klicken Sie im Aktivitätsbereich auf die Registerkarte **Produktionsauftrag** und wählen **Freigabe**, um das Dialogfeld **Freigabe** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![Dialogfeld Freigabe](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="1a208-223">Klicken Sie auf **OK**, um das Dialogfeld **Freigabe** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="1a208-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="1a208-224">Wählen Sie **Produktionssteuerung \> Periodische Aufgaben \> Freigabe Lagerort \> Automatische Version der Stückliste und der Formelpositionen**, um das Dialogfeld **Automatische Version der Stückliste und der Formelpositionen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![Dialogfeld automatische Freigabe von Stücklisten- und Formelpositionen](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="1a208-226">Wählen Sie **OK** aus, um die automatische Freigabe des Stücklisten- und Formelpositionseinzelvorgangs auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1a208-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="1a208-227">Dieser Einzelvorgang gibt Entnahmearbeit für Rohmaterialen an den Lagerort frei.</span><span class="sxs-lookup"><span data-stu-id="1a208-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="1a208-228">Wählen Sie **Produktionssteuerung \> Produktionsaufträge \> Alle Produktionsaufträge**, um die Seite **Alle Produktionsaufträge** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="1a208-229">Verwenden Sie d die Schnellfilterung, um den Produktionsauftrag auszuwählen, an dem Sie gearbeitet haben.</span><span class="sxs-lookup"><span data-stu-id="1a208-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="1a208-230">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerhaus**, wählen Sie **Arbeitsdetails**, um die Seite **Arbeit** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="1a208-231">Beachten Sie, dass die Seite zwei Sätze Arbeit für Rohmaterialentnahmen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1a208-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="1a208-232">Die erste Arbeit ist für Material M8100 und M8101.</span><span class="sxs-lookup"><span data-stu-id="1a208-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="1a208-233">Deise Materialien werden auch vom Vorgang 10 verbraucht.</span><span class="sxs-lookup"><span data-stu-id="1a208-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="1a208-234">Die zweite Arbeit ist für Material M8202 und M8250.</span><span class="sxs-lookup"><span data-stu-id="1a208-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="1a208-235">Diese Materialien werden von Arbeitsgang 20 verbraucht, welcher ein geregelter Arbeitsgang ist.</span><span class="sxs-lookup"><span data-stu-id="1a208-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![Zwei Sätze Arbeit für Rohmaterialentnahmen auf der Seite Arbeit](./media/subcontract22_work-page.png)

26. <span data-ttu-id="1a208-237">Starten Sie die Lagerort-App, um die Lagerortarbeit für Arbeitsgang 10 zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1a208-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="1a208-238">Wählen Sie **Produktionssteuerung \> Produktionsaufträge \> Alle Produktionsaufträge**, um die Seite **Alle Produktionsaufträge** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="1a208-239">Verwenden Sie d die Schnellfilterung, um den Produktionsauftrag auszuwählen, an dem Sie gearbeitet haben.</span><span class="sxs-lookup"><span data-stu-id="1a208-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="1a208-240">Klicken Sie im Aktivitätsbereich auf die Registerkarte **Produktionsauftrag** und wählen **Start**, um das Dialogfeld **Start** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="1a208-241">Definieren Sie auf der Registerkarte **Allgemeines** die folgenden Werte</span><span class="sxs-lookup"><span data-stu-id="1a208-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="1a208-242">Im **Von Arbeitsgangnr.**</span><span class="sxs-lookup"><span data-stu-id="1a208-242">In the **From Oper. No.**</span></span> <span data-ttu-id="1a208-243">Feld wählen Sie **10**.</span><span class="sxs-lookup"><span data-stu-id="1a208-243">field, select **10**.</span></span>
    - <span data-ttu-id="1a208-244">Im **Zu Arbeitsgangnr.**</span><span class="sxs-lookup"><span data-stu-id="1a208-244">In the **To Oper. No.**</span></span> <span data-ttu-id="1a208-245">Feld wählen Sie **10**.</span><span class="sxs-lookup"><span data-stu-id="1a208-245">field, select **10**.</span></span>

    ![Werte festgelegt auf der Registerkarte "Allgemeines"](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="1a208-247">Wählen Sie **OK**, um das Dialogfeld **Start** zu schließen und zur Seite **Alle Produktionsaufträge** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="1a208-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="1a208-248">Beachten Sie, dass der Status des Produktionsauftrags nun **Gestartet** ist.</span><span class="sxs-lookup"><span data-stu-id="1a208-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="1a208-249">Die Materialien für Arbeitsgang 10 werden durch eine automatische Buchung der Kommissionierlistenerfassung verbraucht.</span><span class="sxs-lookup"><span data-stu-id="1a208-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="1a208-250">Der Zeitverbrauch für Arbeitsgang 10 wird durch eine automatische Buchung einer Arbeitsplanlisten-Erfassung angegeben.</span><span class="sxs-lookup"><span data-stu-id="1a208-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="1a208-251">Starten Sie die Lagerort-App, um die Lagerortarbeit für Arbeitsgang 20 zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1a208-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="1a208-252">Klicken Sie im Aktivitätsbereich auf die Registerkarte **Produktionsauftrag** und wählen **Start**, um das Dialogfeld **Start** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="1a208-253">Definieren Sie auf der Registerkarte **Allgemeines** die folgenden Werte</span><span class="sxs-lookup"><span data-stu-id="1a208-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="1a208-254">Im **Von Arbeitsgangnr.**</span><span class="sxs-lookup"><span data-stu-id="1a208-254">In the **From Oper. No.**</span></span> <span data-ttu-id="1a208-255">Feld wählen Sie **20**.</span><span class="sxs-lookup"><span data-stu-id="1a208-255">field, select **20**.</span></span>
    - <span data-ttu-id="1a208-256">Im **Zu Arbeitsgangnr.**</span><span class="sxs-lookup"><span data-stu-id="1a208-256">In the **To Oper. No.**</span></span> <span data-ttu-id="1a208-257">Feld wählen Sie **20**.</span><span class="sxs-lookup"><span data-stu-id="1a208-257">field, select **20**.</span></span>
    - <span data-ttu-id="1a208-258">Geben Sie im Feld **Menge** den Wert **10** ein.</span><span class="sxs-lookup"><span data-stu-id="1a208-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="1a208-259">Wählen Sie im Feld **Kommissionierliste jetzt buchen** die Antwort **Nein** aus.</span><span class="sxs-lookup"><span data-stu-id="1a208-259">Set the **Post picking list now** option to **No**.</span></span>

    ![Werte festgelegt auf der Registerkarte "Allgemeines"](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="1a208-261">Wählen Sie **OK**, um das Dialogfeld **Start** zu schließen und zur Seite **Alle Produktionsaufträge** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="1a208-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="1a208-262">Eine Kommissionierliste wird für die Materialien, die für den Beschichtungsarbeitsgang verwendet werden und für Dienstleistungsartikel erstellt.</span><span class="sxs-lookup"><span data-stu-id="1a208-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="1a208-263">Der Dienstleistungsartikel stellt die Kosten des geregelten Arbeitsgangs dar.</span><span class="sxs-lookup"><span data-stu-id="1a208-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="1a208-264">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Ansicht**, wählen Sie **Kommissionierliste**, um die Seite **Kommissionierliste** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="1a208-265">Wählen Sie die Kommissionierliste, die nicht gebucht wurde, und wählen Sie dann die Erfassungsnummer aus, um die Erfassungspositionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1a208-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![Erfassungsposition auf der Seite Kommissionierliste](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="1a208-267">Klicken Sie im Aktivitätsbereich **Drucken** \> wählen Sie **Kommissionierlistenbericht**, um das Dialogfeld **Kommissionierlistenbericht** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="1a208-268">Hier können Sie die Option **Lieferscheinlayout verwenden** auf **Ja** festlegen.</span><span class="sxs-lookup"><span data-stu-id="1a208-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![Dialogfeld Kommissionierlistenbericht](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="1a208-270">Wählen Sie **OK**, um den **Kommissionierlisten**-Bericht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a208-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="1a208-271">In diesem Fall wird ein Lieferschein des Kreditors aus der Produktionskommissionierlistenerfassung gedruckt.</span><span class="sxs-lookup"><span data-stu-id="1a208-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="1a208-272">Der Lieferschein zeigt die Materialien an, die an den Kreditor gesendet werden, der den Beschichtungsarbeitsgang durchführt.</span><span class="sxs-lookup"><span data-stu-id="1a208-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![Bericht 'Kommissionierliste'](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="1a208-274">Beenden Sie den Bericht **Kommissionierliste**, um zur Seite **Kommissionierliste** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="1a208-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="1a208-275">Im Aktivitätsbereich wählen Sie **Buchen**, um das Dialogfeld **Erfassung buchen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![Dialogfeld Erfassung buchen](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="1a208-277">Klicken Sie auf **OK**, um das Dialogfeld **Erfassung buchen** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="1a208-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="1a208-278">Bestellpositionen öffnen.</span><span class="sxs-lookup"><span data-stu-id="1a208-278">Open the purchase order.</span></span>

    ![Seite Bestellungen](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="1a208-280">Klicken Sie im Aktivitätsbereich auf der Registerkarte auf **Einkauf** und wählen Sie **Bestätigen**.</span><span class="sxs-lookup"><span data-stu-id="1a208-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="1a208-281">Klicken Sie auf **Buchen**, um das Dialogfeld **Erfassung buchen** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="1a208-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="1a208-282">Wählen Sie **OK**, um das Dialogfeld **Erfassung buchen** zu schließen und zur Seite **Alle Bestellungen** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="1a208-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="1a208-283">Ändern Sie den Preis je Einheit von **33** in **40**.</span><span class="sxs-lookup"><span data-stu-id="1a208-283">Change the unit price from **33** to **40**.</span></span>

    ![Preis je Einheit auf der Bestellungsseite geändert](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="1a208-285">Dient zur erneuten Bestätigung der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="1a208-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="1a208-286">Produktzugang.</span><span class="sxs-lookup"><span data-stu-id="1a208-286">Product receipt.</span></span>

    ![Dialogfeld Buchen des Produktzugangs](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="1a208-288">Rechnung Bestellung</span><span class="sxs-lookup"><span data-stu-id="1a208-288">Purchase invoice.</span></span>
52. <span data-ttu-id="1a208-289">Status des Abgleichs aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1a208-289">Update the match status.</span></span>

    ![Seite Kreditorenrechnung](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="1a208-291">Fertigmeldung.</span><span class="sxs-lookup"><span data-stu-id="1a208-291">Report as finished.</span></span>

    ![Dialogfeld Fertigmeldung](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="1a208-293">Beenden.</span><span class="sxs-lookup"><span data-stu-id="1a208-293">End.</span></span>

    ![Dialogfeld beenden](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="1a208-295">Kostenvergleich.</span><span class="sxs-lookup"><span data-stu-id="1a208-295">Cost comparison.</span></span>

    ![Diagramme Kostenvergleich](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="1a208-297">Fehlende Daten in Unternehmensdaten.</span><span class="sxs-lookup"><span data-stu-id="1a208-297">Missing setup in data.</span></span>
