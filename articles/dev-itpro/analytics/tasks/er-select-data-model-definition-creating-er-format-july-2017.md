--- 
title: "Auswählen einer Datenmodelldefinition beim Erstellen eines Formats für elektronische Berichterstellung (ER)"
description: "Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter \"Konfigurationsanbieter erstellen und als aktiv markieren\" abschließen."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e560daa19b30c3f12e2b7a414580f89c93dfc31a
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="select-data-model-definition-while-creating-format-for-electronic-reporting-er"></a><span data-ttu-id="2556e-103">Auswählen einer Datenmodelldefinition beim Erstellen eines Formats für elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="2556e-103">Select data model definition while creating format for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2556e-104">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="2556e-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="2556e-105">Dieses Verfahren zeigt, wie Stammartikel eines Modells als Datenmodelldefinition zum Einfügen einer elektronischen meldenden (ER)- Formatkonfiguration ausgewählt werden kann, die dazu da ist, um elektronische Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="2556e-105">This procedure shows how a model’s root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="2556e-106">In dieser Prozedur fügen Sie eine neue ER-Formatkonfigurartion für das Beispielunternehmen „Litware, Inc.” hinzu.</span><span class="sxs-lookup"><span data-stu-id="2556e-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="2556e-107">Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="2556e-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="2556e-108">Die Schritte können abgeschlossen werden, indem Sie einen Datensatz verwenden.</span><span class="sxs-lookup"><span data-stu-id="2556e-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="2556e-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="2556e-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="2556e-110">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist.</span><span class="sxs-lookup"><span data-stu-id="2556e-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="2556e-111">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren” abschließen. </span><span class="sxs-lookup"><span data-stu-id="2556e-111">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="2556e-112">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="2556e-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="2556e-113">Neue ER-Daten-Modellkonfiguration hinzufügen</span><span class="sxs-lookup"><span data-stu-id="2556e-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="2556e-114">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2556e-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="2556e-115">Wir fügen eine neue ER-Modellkonfiguration hinzu, die das Datenmodell enthält, das entwickelt wurde, die als Datenquelle für das Generieren des Intrastat-Berichts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2556e-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="2556e-116">Geben Sie im Feld "Name" "Zahlungsmodell (fiktiv) ein.</span><span class="sxs-lookup"><span data-stu-id="2556e-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="2556e-117">Zahlungsmodell (fiktiv)</span><span class="sxs-lookup"><span data-stu-id="2556e-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="2556e-118">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="2556e-118">Click Create configuration.</span></span>
4. <span data-ttu-id="2556e-119">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="2556e-119">Click Designer.</span></span>
    * <span data-ttu-id="2556e-120">Öffnen Sie den ER-Designer, um die Struktur des Datenmodells dieser Variante angeben.</span><span class="sxs-lookup"><span data-stu-id="2556e-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="2556e-121">Angenommen, dass wir das Datenmodell für Zahlungen entwerfen, um damit die 2-Zahlungsgeschäftsdomänen-Methoden - Kreditübertragungen und Direktbelastungen.</span><span class="sxs-lookup"><span data-stu-id="2556e-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="2556e-122">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2556e-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="2556e-123">Geben Sie im Feld "Name" Typ Zahlung - Kreditübertragung ein.</span><span class="sxs-lookup"><span data-stu-id="2556e-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="2556e-124">Zahlungen - Überweisungszahlung</span><span class="sxs-lookup"><span data-stu-id="2556e-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="2556e-125">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2556e-125">Click Add.</span></span>
8. <span data-ttu-id="2556e-126">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2556e-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="2556e-127">Geben Sie im Feld „Neuer Knoten als ein Feld” die Bezeichnung „Modellwurzel” ein.</span><span class="sxs-lookup"><span data-stu-id="2556e-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="2556e-128">Geben Sie im Feld "Name" Typ Zahlung - Direktbelastung ein.</span><span class="sxs-lookup"><span data-stu-id="2556e-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="2556e-129">Zahlungen - Direkteinzugszahlungen</span><span class="sxs-lookup"><span data-stu-id="2556e-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="2556e-130">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2556e-130">Click Add.</span></span>
12. <span data-ttu-id="2556e-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="2556e-131">Click Save.</span></span>
13. <span data-ttu-id="2556e-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2556e-132">Close the page.</span></span>
14. <span data-ttu-id="2556e-133">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="2556e-133">Click Change status.</span></span>
    * <span data-ttu-id="2556e-134">Schließt die Entwurfsversion des Modells ab, um die neuen Zuordnungsmodelle und Formate verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="2556e-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="2556e-135">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="2556e-135">Click Complete.</span></span>
16. <span data-ttu-id="2556e-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2556e-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="2556e-137">Start, um eine neue ER-Formatkonfiguration einzugeben</span><span class="sxs-lookup"><span data-stu-id="2556e-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="2556e-138">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2556e-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="2556e-139">Geben Sie im Feld "Neu" 'Format basierend auf Modell Zahlungsmodell (fiktiv) ein.</span><span class="sxs-lookup"><span data-stu-id="2556e-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="2556e-140">Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2556e-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="2556e-141">Beachten Sie, dass alle Stammartikel des Datenmodells für die ausgewählten Auswahl als Datenmodelldefinition im Zeitpunkt vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="2556e-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="2556e-142">Sie können fortfahren, um das Format zu entwerfen, indem Sie eines der erforderlichen Stammartikel des - Datenmodells verwenden.</span><span class="sxs-lookup"><span data-stu-id="2556e-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="2556e-143">Eine fehlende Modellzuordnung für den ausgewählten Stammartikel hindert Sie nicht am Fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="2556e-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="2556e-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2556e-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="2556e-145">Neue ER-Daten-Modellkonfigurationszuordnung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="2556e-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="2556e-146">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2556e-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="2556e-147">Geben Sie im Feld "Neu" 'Modellzuordnung basierend auf Datenmodell-Zahlungsmodell (fiktiv) ein.</span><span class="sxs-lookup"><span data-stu-id="2556e-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="2556e-148">Geben Sie im Feld "Name" "Zahlungsmodellzuordnung (fiktiv) ein.</span><span class="sxs-lookup"><span data-stu-id="2556e-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="2556e-149">Zahlungsmodell-Zuordnungen (fiktiv)</span><span class="sxs-lookup"><span data-stu-id="2556e-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="2556e-150">Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2556e-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="2556e-151">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="2556e-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="2556e-152">Modellzuordnungsdesigner</span><span class="sxs-lookup"><span data-stu-id="2556e-152">Design ER model mappings</span></span>
1. <span data-ttu-id="2556e-153">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="2556e-153">Click Designer.</span></span>
    * <span data-ttu-id="2556e-154">Verwenden Sie den ER-Designer, um das Lagermodell der Zuordnungen für die erforderlichen Stammartikel anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2556e-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="2556e-155">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="2556e-155">Click Designer.</span></span>
    * <span data-ttu-id="2556e-156">Einrichtung ausgewälter Modellzuordnungen für den ausgewählten Stammartikel des Modells simulieren.</span><span class="sxs-lookup"><span data-stu-id="2556e-156">Simulate setting of selected model mapping for the selected model’s root item.</span></span>  
3. <span data-ttu-id="2556e-157">Wählen Sie in der Strukturdarstellung "Dynamics 365 for Operations \Tabellendatensätze" aus.</span><span class="sxs-lookup"><span data-stu-id="2556e-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="2556e-158">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="2556e-158">Click Add root.</span></span>
5. <span data-ttu-id="2556e-159">Geben Sie im Feld Name den Typ Sachkonto ein.</span><span class="sxs-lookup"><span data-stu-id="2556e-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="2556e-160">Im Tabellenfeld geben Sie "LedgerJournalTrans" ein.</span><span class="sxs-lookup"><span data-stu-id="2556e-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="2556e-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="2556e-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="2556e-162">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2556e-162">Click OK.</span></span>
8. <span data-ttu-id="2556e-163">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="2556e-163">Click Save.</span></span>
9. <span data-ttu-id="2556e-164">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2556e-164">Close the page.</span></span>
10. <span data-ttu-id="2556e-165">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2556e-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="2556e-166">Start, um eine andere ER-Formatkonfiguration einzugeben</span><span class="sxs-lookup"><span data-stu-id="2556e-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="2556e-167">Wählen Sie in der Struktur die Option "Zahlungsmodell" (fiktiv) aus.</span><span class="sxs-lookup"><span data-stu-id="2556e-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="2556e-168">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2556e-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="2556e-169">Geben Sie im Feld "Neu" 'Format basierend auf Modell Zahlungsmodell (fiktiv) ein.</span><span class="sxs-lookup"><span data-stu-id="2556e-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="2556e-170">Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2556e-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="2556e-171">Beachten Sie, dass ein Stammartikel nun verfügbar ist, um diesen den Bewerbungsdatenquellen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="2556e-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="2556e-172">Wenn mindestens eine vorbildliche Zuordnung eingegeben wird, werden nur die Stammartikel des Modells, die den Bewerbungsdatenquellen zugeordnet werden, als vorbildliche Definition ausgewählt werden können, für die das ER-Format hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2556e-172">When at least one model mapping is introduced, only the model’s root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="2556e-173">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2556e-173">Close the page.</span></span>


