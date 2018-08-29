--- 
title: EB-Modellzuordnung in getrennten EB-Konfigurationen verwalten
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle \"Entwickler für elektronische Berichterstellung\" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann."
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 24ca4124d190df94e7ca9ac31c2ea757fe9ff242
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="8a9da-103">EB-Modellzuordnung in getrennten EB-Konfigurationen verwalten</span><span class="sxs-lookup"><span data-stu-id="8a9da-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a9da-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="8a9da-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="8a9da-105">In diesem Aufgabenleitfaden erstellen Sie erforderliche ER-Konfigurationen für das Beispielunternehmen, Litware, Inc., um diesen Aufgabenleitfaden abzuschließen, müssen Sie die Schritte im Aufgabenleitfaden erst abschließen, "ER bieten einen Konfigurationsanbieter" erstellen und als aktiv markieren, ihn.</span><span class="sxs-lookup"><span data-stu-id="8a9da-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, “ER Create a configuration provider” and mark it as active.</span></span> 

<span data-ttu-id="8a9da-106">Da ER-Konfigurationen unter Unternehmen freigegeben werden, können Sie diese Aufgabenleitfaden mithilfe der Unternehmensdaten aus, die von Ihrer Auswahl werden gefestgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8a9da-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="8a9da-107">Die Funktionen für diesen Aufgabenleitfaden sind nur verfügbar, wenn Sie einen der folgenden Hotfixes installiert haben: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 für die Version Dynamics AX 7.0 oder https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 für die Version Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="8a9da-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="8a9da-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="8a9da-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="8a9da-109">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist.</span><span class="sxs-lookup"><span data-stu-id="8a9da-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="8a9da-110">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren” abschließen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-110">If you don’t see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="8a9da-111">Neue ER-Modellkonfiguration hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8a9da-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="8a9da-112">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="8a9da-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="8a9da-113">Neue ER-Modellkonfiguration hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-113">Add a new model configuration.</span></span> <span data-ttu-id="8a9da-114">Der Name des Profils muss in der Konfigurationsstruktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="8a9da-115">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="8a9da-116">Geben Sie im Feld "Name" Datenmodellkonfiguration" ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="8a9da-117">Muster-Datenmodell</span><span class="sxs-lookup"><span data-stu-id="8a9da-117">Sample data model</span></span>  
4. <span data-ttu-id="8a9da-118">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-118">Click Create configuration.</span></span>
5. <span data-ttu-id="8a9da-119">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8a9da-119">Click Designer.</span></span>
6. <span data-ttu-id="8a9da-120">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="8a9da-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="8a9da-121">Geben Sie im Feld Name "Root" ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="8a9da-122">Stamm</span><span class="sxs-lookup"><span data-stu-id="8a9da-122">Root</span></span>  
8. <span data-ttu-id="8a9da-123">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-123">Click Add.</span></span>
9. <span data-ttu-id="8a9da-124">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="8a9da-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="8a9da-125">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="8a9da-126">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="8a9da-126">Company</span></span>  
11. <span data-ttu-id="8a9da-127">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-127">Click Add.</span></span>
12. <span data-ttu-id="8a9da-128">Im Feld Beschreibung geben Sie den Text, die Beschreibung der juristischen Personen oder des Unternehmen, in denen ein Benutzer zur Laufzeit protokollierte ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="8a9da-129">Beschreibung der juristischen Person oder des Unternehmens, bei denen Benutzer zur Laufzeit protokollierte.</span><span class="sxs-lookup"><span data-stu-id="8a9da-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="8a9da-130">Stammreferenz anklicken.</span><span class="sxs-lookup"><span data-stu-id="8a9da-130">Click Root reference.</span></span>
14. <span data-ttu-id="8a9da-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a9da-131">Click OK.</span></span>
15. <span data-ttu-id="8a9da-132">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8a9da-132">Click Save.</span></span>
16. <span data-ttu-id="8a9da-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a9da-133">Close the page.</span></span>
17. <span data-ttu-id="8a9da-134">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="8a9da-134">Click Change status.</span></span>
18. <span data-ttu-id="8a9da-135">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="8a9da-135">Click Complete.</span></span>
19. <span data-ttu-id="8a9da-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a9da-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="8a9da-137">Neue ER-Daten-Modellkonfigurationszuordnung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8a9da-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="8a9da-138">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="8a9da-139">Geben Sie im Feld "Neu" 'Modellzuordnung basierend auf Datenmodell-Beispielsdatenmodell ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="8a9da-140">Geben Sie im Feld "Typ" Musterzuordnung ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="8a9da-141">Musterzuordnung</span><span class="sxs-lookup"><span data-stu-id="8a9da-141">Sample mapping</span></span>  
4. <span data-ttu-id="8a9da-142">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-142">Click Create configuration.</span></span>
5. <span data-ttu-id="8a9da-143">Erweitern des Abschnitts Voraussetzungen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="8a9da-144">Beachten Sie, dass die Implementierungs-Voraussetzungsgruppe automatisch hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="8a9da-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="8a9da-145">Diese Gruppe beinhaltet die erforderliche Komponente, die die Datenmodellkonfiguration bezieht und die Implementierungsmarkierung hat, die aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8a9da-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="8a9da-146">Diese Markierung gibt an, dass die Zuordnungskonfiguration als "Beispielzuordnungs" für die Implementierung des " Beispieldatmodell" Datenmodells gilt.</span><span class="sxs-lookup"><span data-stu-id="8a9da-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="8a9da-147">Diese Komponente zwingt ER, die Beispielzuordnungs-Zuordnungskonfiguration von einem ER-Repository herunterzuladen, sobald die Beispieldatmodell-Modellkonfiguration heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="8a9da-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="8a9da-148">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8a9da-148">Click Designer.</span></span>
    * <span data-ttu-id="8a9da-149">Beachten Sie, dass die vorbildliche erstellte Zuordnungskonfiguration eine neue leere Zuordnung mit demselben Namen wie die erstellte Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="8a9da-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="8a9da-150">Beachten Sie, dass, wenn eine ausgewählte Elternteilmodellkonfiguration vorbildliche Zuordnungen, enthält sie in eine Zuordnungskonfiguration des neuen Modells kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="8a9da-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="8a9da-151">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8a9da-151">Click Designer.</span></span>
8. <span data-ttu-id="8a9da-152">Wählen Sie in der Strukturdarstellung "Dynamics 365 for Operations \Tabelle" aus.</span><span class="sxs-lookup"><span data-stu-id="8a9da-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="8a9da-153">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8a9da-153">Click Add root.</span></span>
10. <span data-ttu-id="8a9da-154">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="8a9da-155">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="8a9da-155">Company</span></span>  
11. <span data-ttu-id="8a9da-156">Im Tabellenfeld geben Sie "CompanyInfo" ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="8a9da-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="8a9da-157">CompanyInfo</span></span>  
12. <span data-ttu-id="8a9da-158">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a9da-158">Click OK.</span></span>
13. <span data-ttu-id="8a9da-159">Erweitern Sie in der Struktur Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="8a9da-160">In der Struktur erweitern Sie das Feld Unternehmen\Suchen ().</span><span class="sxs-lookup"><span data-stu-id="8a9da-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="8a9da-161">Wählen Sie in der Struktur 'Unternehmen\Namen\finden'.</span><span class="sxs-lookup"><span data-stu-id="8a9da-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="8a9da-162">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8a9da-162">Click Bind.</span></span>
17. <span data-ttu-id="8a9da-163">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8a9da-163">Click Save.</span></span>
18. <span data-ttu-id="8a9da-164">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a9da-164">Close the page.</span></span>
19. <span data-ttu-id="8a9da-165">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a9da-165">Close the page.</span></span>
20. <span data-ttu-id="8a9da-166">Klicken Sie im Aktivitätsbereich auf Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="8a9da-167">Klicken Sie auf Benutzerparameter.</span><span class="sxs-lookup"><span data-stu-id="8a9da-167">Click User parameters.</span></span>
22. <span data-ttu-id="8a9da-168">Wählen Sie "Ja" im Feld "Testlaufeinstellungen".</span><span class="sxs-lookup"><span data-stu-id="8a9da-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="8a9da-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a9da-169">Click OK.</span></span>
24. <span data-ttu-id="8a9da-170">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8a9da-170">Click Edit.</span></span>
25. <span data-ttu-id="8a9da-171">Wählen Sie "Ja" im Feld "Testentwurf".</span><span class="sxs-lookup"><span data-stu-id="8a9da-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="8a9da-172">Neues ER-Modellformat hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8a9da-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="8a9da-173">Wählen Sie in der Struktur 'Muster Datenmodell'.</span><span class="sxs-lookup"><span data-stu-id="8a9da-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="8a9da-174">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="8a9da-175">Geben Sie im Feld "Neu" 'Format basierend auf Modell Musterdatenmodell' ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="8a9da-176">Geben Sie im Feld "Typ" Musterformat ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="8a9da-177">Beispielformat</span><span class="sxs-lookup"><span data-stu-id="8a9da-177">Sample format</span></span>  
5. <span data-ttu-id="8a9da-178">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-178">Click Create configuration.</span></span>
6. <span data-ttu-id="8a9da-179">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8a9da-179">Click Designer.</span></span>
7. <span data-ttu-id="8a9da-180">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="8a9da-181">Wählen Sie in der Struktur 'Text\String' aus.</span><span class="sxs-lookup"><span data-stu-id="8a9da-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="8a9da-182">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a9da-182">Click OK.</span></span>
10. <span data-ttu-id="8a9da-183">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="8a9da-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="8a9da-184">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="8a9da-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="8a9da-185">Wählen Sie in der Struktur Modell\Unternehmen aus.</span><span class="sxs-lookup"><span data-stu-id="8a9da-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="8a9da-186">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8a9da-186">Click Bind.</span></span>
14. <span data-ttu-id="8a9da-187">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8a9da-187">Click Save.</span></span>
15. <span data-ttu-id="8a9da-188">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a9da-188">Close the page.</span></span>
    * <span data-ttu-id="8a9da-189">Führt die Entwurfsversion des erstellten Formats für Testzwecke aus.</span><span class="sxs-lookup"><span data-stu-id="8a9da-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="8a9da-190">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="8a9da-190">Click Run.</span></span>
    * <span data-ttu-id="8a9da-191">Wählen Sie in der Version Inforegister ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="8a9da-192">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a9da-192">Click OK.</span></span>
    * <span data-ttu-id="8a9da-193">Wiederholen Sie die Ausgabe, die den Namen des Unternehmens enthält, in dem der Benutzer, der ausgeführt wird, diese Formatkonfiguration angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="8a9da-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="8a9da-194">Beachten Sie, dass die vorbildliche erstellte Zuordnungskonfiguration von dieser Formatkonfiguration verwendet wird, da es nur eine verfügbare Variante gibt, die erforderliche vorbildliche Zuordnungen enthält.</span><span class="sxs-lookup"><span data-stu-id="8a9da-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="8a9da-195">Fügen Sie alternaitve ER-Modellzuordnungskonfiguration hinzu</span><span class="sxs-lookup"><span data-stu-id="8a9da-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="8a9da-196">Wählen Sie in der Struktur 'Muster Datenmodell'.</span><span class="sxs-lookup"><span data-stu-id="8a9da-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="8a9da-197">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="8a9da-198">Geben Sie im Feld "Neu" 'Modellzuordnung basierend auf Datenmodell-Beispielsdatenmodell ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="8a9da-199">Geben Sie im Feld "Typ" Musterzurodnung (alternativ) ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="8a9da-200">Beispielzuordnung (Alternative)</span><span class="sxs-lookup"><span data-stu-id="8a9da-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="8a9da-201">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-201">Click Create configuration.</span></span>
6. <span data-ttu-id="8a9da-202">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8a9da-202">Click Designer.</span></span>
7. <span data-ttu-id="8a9da-203">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8a9da-203">Click Designer.</span></span>
8. <span data-ttu-id="8a9da-204">Wählen Sie in der Strukturdarstellung "Dynamics 365 for Operations \Tabelle" aus.</span><span class="sxs-lookup"><span data-stu-id="8a9da-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="8a9da-205">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8a9da-205">Click Add root.</span></span>
10. <span data-ttu-id="8a9da-206">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="8a9da-207">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="8a9da-207">Company</span></span>  
11. <span data-ttu-id="8a9da-208">Im Tabellenfeld geben Sie "CompanyInfo" ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="8a9da-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="8a9da-209">CompanyInfo</span></span>  
12. <span data-ttu-id="8a9da-210">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a9da-210">Click OK.</span></span>
13. <span data-ttu-id="8a9da-211">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8a9da-211">Click Edit.</span></span>
14. <span data-ttu-id="8a9da-212">Wählen Sie in der Struktur 'String\CONCATENATE' aus.</span><span class="sxs-lookup"><span data-stu-id="8a9da-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="8a9da-213">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-213">Click Add function.</span></span>
16. <span data-ttu-id="8a9da-214">Erweitern Sie in der Struktur Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="8a9da-215">In der Struktur erweitern Sie das Feld Unternehmen\Suchen ().</span><span class="sxs-lookup"><span data-stu-id="8a9da-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="8a9da-216">Wählen Sie in der Struktur 'Unternehmen\Namen\finden'.</span><span class="sxs-lookup"><span data-stu-id="8a9da-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="8a9da-217">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-217">Click Add data source.</span></span>
20. <span data-ttu-id="8a9da-218">Geben Sie im Feld "Formel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="8a9da-219">e Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="8a9da-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="8a9da-220">Wählen Sie in der Struktur 'Unternehmen\finden()\Unternehmen(DataArea).</span><span class="sxs-lookup"><span data-stu-id="8a9da-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="8a9da-221">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a9da-221">Click Add data source.</span></span>
23. <span data-ttu-id="8a9da-222">Geben Sie im Feld "Formel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8a9da-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="8a9da-223">CONCATENATE(Company.'find()Adressbüchern. Name, "; ", Company.'find()' .DataArea)</span><span class="sxs-lookup"><span data-stu-id="8a9da-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="8a9da-224">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8a9da-224">Click Save.</span></span>
25. <span data-ttu-id="8a9da-225">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a9da-225">Close the page.</span></span>
26. <span data-ttu-id="8a9da-226">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8a9da-226">Click Save.</span></span>
27. <span data-ttu-id="8a9da-227">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a9da-227">Close the page.</span></span>
28. <span data-ttu-id="8a9da-228">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a9da-228">Close the page.</span></span>
29. <span data-ttu-id="8a9da-229">Wählen Sie "Ja" im Feld "Testentwurf".</span><span class="sxs-lookup"><span data-stu-id="8a9da-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="8a9da-230">Verwenden Sie eine vorhandene ER-Modellzuordnungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="8a9da-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="8a9da-231">Wählen Sie in der Struktur 'Muster\Datenmodell'.</span><span class="sxs-lookup"><span data-stu-id="8a9da-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="8a9da-232">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="8a9da-232">Click Run.</span></span>
    * <span data-ttu-id="8a9da-233">Beachten Sie, dass die ausgewählte ER-Formatkonfiguration der Entwurfsversion nicht ausgeführt werden, weil es mehr als eine vorbildliche Zuordnungskonfiguration gibt, die für das definierten Datenmodell nicht verfügbar ist, das als Datenquelle des Ausführungsbeginns ER-Formats ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="8a9da-233">Note that the selected draft version of the ER format configuration can’t be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="8a9da-234">Definieren Sie als Nächstes die Zuordnungskonfiguration des alternativen Modells da, die von der als vorbildliche Zuordnungen Datenquellen für die Ausführung von ER-Format verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a9da-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="8a9da-235">Wählen Sie in der Struktur Musterdatenmodell\Musterzuordnung (alternativ).</span><span class="sxs-lookup"><span data-stu-id="8a9da-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="8a9da-236">Wählen Sie die Option „Ja” im Feld „Standard für Modellzuordnung” aus.</span><span class="sxs-lookup"><span data-stu-id="8a9da-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="8a9da-237">Wählen Sie in der Struktur 'Muster\Datenmodell'.</span><span class="sxs-lookup"><span data-stu-id="8a9da-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="8a9da-238">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="8a9da-238">Click Run.</span></span>
7. <span data-ttu-id="8a9da-239">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a9da-239">Click OK.</span></span>
    * <span data-ttu-id="8a9da-240">Beachten Sie, dass die Standardmodellzuordnungskonfiguration von dieser Formatkonfiguration für die Generierung elektronischer Dokumente verwendet wird (die erstellten Ausgaben enthält den Unternehmenscode).</span><span class="sxs-lookup"><span data-stu-id="8a9da-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  


