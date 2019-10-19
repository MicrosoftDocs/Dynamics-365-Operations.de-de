---
title: EB-Modellzuordnung in getrennten EB-Konfigurationen verwalten
description: In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dcf322973ea5e4afd9c828c3cbd1ebbd9972a964
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182254"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="65045-103">EB-Modellzuordnung in getrennten EB-Konfigurationen verwalten</span><span class="sxs-lookup"><span data-stu-id="65045-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="65045-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="65045-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="65045-105">In diesem Aufgabenleitfaden erstellen Sie erforderliche ER-Konfigurationen für das Beispielunternehmen, Litware, Inc., um diesen Aufgabenleitfaden abzuschließen, müssen Sie die Schritte im Aufgabenleitfaden erst abschließen, "ER bieten einen Konfigurationsanbieter" erstellen und als aktiv markieren, ihn.</span><span class="sxs-lookup"><span data-stu-id="65045-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, “ER Create a configuration provider” and mark it as active.</span></span> 

<span data-ttu-id="65045-106">Da ER-Konfigurationen unter Unternehmen freigegeben werden, können Sie diese Aufgabenleitfaden mithilfe der Unternehmensdaten aus, die von Ihrer Auswahl werden gefestgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="65045-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="65045-107">Die Funktionen für diesen Aufgabenleitfaden sind nur verfügbar, wenn Sie einen der folgenden Hotfixes installiert haben: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 für die Dynamics AX 7.0 Version oder https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 für die Dynamics 365 for Operations Version.</span><span class="sxs-lookup"><span data-stu-id="65045-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="65045-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="65045-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="65045-109">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist.</span><span class="sxs-lookup"><span data-stu-id="65045-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="65045-110">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren” abschließen.</span><span class="sxs-lookup"><span data-stu-id="65045-110">If you don’t see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="65045-111">Neue ER-Modellkonfiguration hinzufügen</span><span class="sxs-lookup"><span data-stu-id="65045-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="65045-112">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="65045-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="65045-113">Neue ER-Modellkonfiguration hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="65045-113">Add a new model configuration.</span></span> <span data-ttu-id="65045-114">Der Name des Profils muss in der Konfigurationsstruktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="65045-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="65045-115">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="65045-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="65045-116">Geben Sie im Feld "Name" Datenmodellkonfiguration" ein.</span><span class="sxs-lookup"><span data-stu-id="65045-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="65045-117">Muster-Datenmodell</span><span class="sxs-lookup"><span data-stu-id="65045-117">Sample data model</span></span>  
4. <span data-ttu-id="65045-118">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="65045-118">Click Create configuration.</span></span>
5. <span data-ttu-id="65045-119">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="65045-119">Click Designer.</span></span>
6. <span data-ttu-id="65045-120">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="65045-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="65045-121">Geben Sie im Feld Name "Root" ein.</span><span class="sxs-lookup"><span data-stu-id="65045-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="65045-122">Stamm</span><span class="sxs-lookup"><span data-stu-id="65045-122">Root</span></span>  
8. <span data-ttu-id="65045-123">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="65045-123">Click Add.</span></span>
9. <span data-ttu-id="65045-124">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="65045-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="65045-125">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="65045-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="65045-126">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="65045-126">Company</span></span>  
11. <span data-ttu-id="65045-127">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="65045-127">Click Add.</span></span>
12. <span data-ttu-id="65045-128">Im Feld Beschreibung geben Sie den Text, die Beschreibung der juristischen Personen oder des Unternehmen, in denen ein Benutzer zur Laufzeit protokollierte ein.</span><span class="sxs-lookup"><span data-stu-id="65045-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="65045-129">Beschreibung der juristischen Person oder des Unternehmens, bei denen Benutzer zur Laufzeit protokollierte.</span><span class="sxs-lookup"><span data-stu-id="65045-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="65045-130">Stammreferenz anklicken.</span><span class="sxs-lookup"><span data-stu-id="65045-130">Click Root reference.</span></span>
14. <span data-ttu-id="65045-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="65045-131">Click OK.</span></span>
15. <span data-ttu-id="65045-132">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="65045-132">Click Save.</span></span>
16. <span data-ttu-id="65045-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="65045-133">Close the page.</span></span>
17. <span data-ttu-id="65045-134">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="65045-134">Click Change status.</span></span>
18. <span data-ttu-id="65045-135">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="65045-135">Click Complete.</span></span>
19. <span data-ttu-id="65045-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="65045-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="65045-137">Neue ER-Daten-Modellkonfigurationszuordnung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="65045-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="65045-138">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="65045-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="65045-139">Geben Sie im Feld "Neu" 'Modellzuordnung basierend auf Datenmodell-Beispielsdatenmodell ein.</span><span class="sxs-lookup"><span data-stu-id="65045-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="65045-140">Geben Sie im Feld "Typ" Musterzuordnung ein.</span><span class="sxs-lookup"><span data-stu-id="65045-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="65045-141">Musterzuordnung</span><span class="sxs-lookup"><span data-stu-id="65045-141">Sample mapping</span></span>  
4. <span data-ttu-id="65045-142">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="65045-142">Click Create configuration.</span></span>
5. <span data-ttu-id="65045-143">Erweitern des Abschnitts Voraussetzungen.</span><span class="sxs-lookup"><span data-stu-id="65045-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="65045-144">Beachten Sie, dass die Implementierungs-Voraussetzungsgruppe automatisch hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="65045-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="65045-145">Diese Gruppe beinhaltet die erforderliche Komponente, die die Datenmodellkonfiguration bezieht und die Implementierungsmarkierung hat, die aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="65045-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="65045-146">Diese Markierung gibt an, dass die Zuordnungskonfiguration als "Beispielzuordnungs" für die Implementierung des " Beispieldatmodell" Datenmodells gilt.</span><span class="sxs-lookup"><span data-stu-id="65045-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="65045-147">Diese Komponente zwingt ER, die Beispielzuordnungs-Zuordnungskonfiguration von einem ER-Repository herunterzuladen, sobald die Beispieldatmodell-Modellkonfiguration heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="65045-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="65045-148">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="65045-148">Click Designer.</span></span>
    * <span data-ttu-id="65045-149">Beachten Sie, dass die vorbildliche erstellte Zuordnungskonfiguration eine neue leere Zuordnung mit demselben Namen wie die erstellte Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="65045-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="65045-150">Beachten Sie, dass, wenn eine ausgewählte Elternteilmodellkonfiguration vorbildliche Zuordnungen, enthält sie in eine Zuordnungskonfiguration des neuen Modells kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="65045-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="65045-151">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="65045-151">Click Designer.</span></span>
8. <span data-ttu-id="65045-152">Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabelle' aus.</span><span class="sxs-lookup"><span data-stu-id="65045-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="65045-153">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="65045-153">Click Add root.</span></span>
10. <span data-ttu-id="65045-154">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="65045-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="65045-155">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="65045-155">Company</span></span>  
11. <span data-ttu-id="65045-156">Im Tabellenfeld geben Sie "CompanyInfo" ein.</span><span class="sxs-lookup"><span data-stu-id="65045-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="65045-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="65045-157">CompanyInfo</span></span>  
12. <span data-ttu-id="65045-158">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="65045-158">Click OK.</span></span>
13. <span data-ttu-id="65045-159">Erweitern Sie in der Struktur Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="65045-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="65045-160">In der Struktur erweitern Sie das Feld Unternehmen\Suchen ().</span><span class="sxs-lookup"><span data-stu-id="65045-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="65045-161">Wählen Sie in der Struktur 'Unternehmen\Namen\finden'.</span><span class="sxs-lookup"><span data-stu-id="65045-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="65045-162">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="65045-162">Click Bind.</span></span>
17. <span data-ttu-id="65045-163">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="65045-163">Click Save.</span></span>
18. <span data-ttu-id="65045-164">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="65045-164">Close the page.</span></span>
19. <span data-ttu-id="65045-165">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="65045-165">Close the page.</span></span>
20. <span data-ttu-id="65045-166">Klicken Sie im Aktivitätsbereich auf Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="65045-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="65045-167">Klicken Sie auf Benutzerparameter.</span><span class="sxs-lookup"><span data-stu-id="65045-167">Click User parameters.</span></span>
22. <span data-ttu-id="65045-168">Wählen Sie "Ja" im Feld "Testlaufeinstellungen".</span><span class="sxs-lookup"><span data-stu-id="65045-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="65045-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="65045-169">Click OK.</span></span>
24. <span data-ttu-id="65045-170">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="65045-170">Click Edit.</span></span>
25. <span data-ttu-id="65045-171">Wählen Sie "Ja" im Feld "Testentwurf".</span><span class="sxs-lookup"><span data-stu-id="65045-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="65045-172">Neues ER-Modellformat hinzufügen</span><span class="sxs-lookup"><span data-stu-id="65045-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="65045-173">Wählen Sie in der Struktur 'Muster Datenmodell'.</span><span class="sxs-lookup"><span data-stu-id="65045-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="65045-174">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="65045-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="65045-175">Geben Sie im Feld "Neu" 'Format basierend auf Modell Musterdatenmodell' ein.</span><span class="sxs-lookup"><span data-stu-id="65045-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="65045-176">Geben Sie im Feld "Typ" Musterformat ein.</span><span class="sxs-lookup"><span data-stu-id="65045-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="65045-177">Beispielformat</span><span class="sxs-lookup"><span data-stu-id="65045-177">Sample format</span></span>  
5. <span data-ttu-id="65045-178">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="65045-178">Click Create configuration.</span></span>
6. <span data-ttu-id="65045-179">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="65045-179">Click Designer.</span></span>
7. <span data-ttu-id="65045-180">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="65045-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="65045-181">Wählen Sie in der Struktur 'Text\String' aus.</span><span class="sxs-lookup"><span data-stu-id="65045-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="65045-182">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="65045-182">Click OK.</span></span>
10. <span data-ttu-id="65045-183">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="65045-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="65045-184">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="65045-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="65045-185">Wählen Sie in der Struktur Modell\Unternehmen aus.</span><span class="sxs-lookup"><span data-stu-id="65045-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="65045-186">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="65045-186">Click Bind.</span></span>
14. <span data-ttu-id="65045-187">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="65045-187">Click Save.</span></span>
15. <span data-ttu-id="65045-188">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="65045-188">Close the page.</span></span>
    * <span data-ttu-id="65045-189">Führt die Entwurfsversion des erstellten Formats für Testzwecke aus.</span><span class="sxs-lookup"><span data-stu-id="65045-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="65045-190">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="65045-190">Click Run.</span></span>
    * <span data-ttu-id="65045-191">Wählen Sie in der Version Inforegister ausführen.</span><span class="sxs-lookup"><span data-stu-id="65045-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="65045-192">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="65045-192">Click OK.</span></span>
    * <span data-ttu-id="65045-193">Wiederholen Sie die Ausgabe, die den Namen des Unternehmens enthält, in dem der Benutzer, der ausgeführt wird, diese Formatkonfiguration angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="65045-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="65045-194">Beachten Sie, dass die vorbildliche erstellte Zuordnungskonfiguration von dieser Formatkonfiguration verwendet wird, da es nur eine verfügbare Variante gibt, die erforderliche vorbildliche Zuordnungen enthält.</span><span class="sxs-lookup"><span data-stu-id="65045-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="65045-195">Fügen Sie alternaitve ER-Modellzuordnungskonfiguration hinzu</span><span class="sxs-lookup"><span data-stu-id="65045-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="65045-196">Wählen Sie in der Struktur 'Muster Datenmodell'.</span><span class="sxs-lookup"><span data-stu-id="65045-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="65045-197">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="65045-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="65045-198">Geben Sie im Feld "Neu" 'Modellzuordnung basierend auf Datenmodell-Beispielsdatenmodell ein.</span><span class="sxs-lookup"><span data-stu-id="65045-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="65045-199">Geben Sie im Feld "Typ" Musterzurodnung (alternativ) ein.</span><span class="sxs-lookup"><span data-stu-id="65045-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="65045-200">Beispielzuordnung (Alternative)</span><span class="sxs-lookup"><span data-stu-id="65045-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="65045-201">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="65045-201">Click Create configuration.</span></span>
6. <span data-ttu-id="65045-202">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="65045-202">Click Designer.</span></span>
7. <span data-ttu-id="65045-203">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="65045-203">Click Designer.</span></span>
8. <span data-ttu-id="65045-204">Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabelle' aus.</span><span class="sxs-lookup"><span data-stu-id="65045-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="65045-205">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="65045-205">Click Add root.</span></span>
10. <span data-ttu-id="65045-206">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="65045-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="65045-207">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="65045-207">Company</span></span>  
11. <span data-ttu-id="65045-208">Im Tabellenfeld geben Sie "CompanyInfo" ein.</span><span class="sxs-lookup"><span data-stu-id="65045-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="65045-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="65045-209">CompanyInfo</span></span>  
12. <span data-ttu-id="65045-210">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="65045-210">Click OK.</span></span>
13. <span data-ttu-id="65045-211">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="65045-211">Click Edit.</span></span>
14. <span data-ttu-id="65045-212">Wählen Sie in der Struktur 'String\CONCATENATE' aus.</span><span class="sxs-lookup"><span data-stu-id="65045-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="65045-213">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="65045-213">Click Add function.</span></span>
16. <span data-ttu-id="65045-214">Erweitern Sie in der Struktur Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="65045-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="65045-215">In der Struktur erweitern Sie das Feld Unternehmen\Suchen ().</span><span class="sxs-lookup"><span data-stu-id="65045-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="65045-216">Wählen Sie in der Struktur 'Unternehmen\Namen\finden'.</span><span class="sxs-lookup"><span data-stu-id="65045-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="65045-217">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="65045-217">Click Add data source.</span></span>
20. <span data-ttu-id="65045-218">Geben Sie im Feld "Formel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="65045-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="65045-219">e Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="65045-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="65045-220">Wählen Sie in der Struktur 'Unternehmen\finden()\Unternehmen(DataArea).</span><span class="sxs-lookup"><span data-stu-id="65045-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="65045-221">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="65045-221">Click Add data source.</span></span>
23. <span data-ttu-id="65045-222">Geben Sie im Feld "Formel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="65045-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="65045-223">CONCATENATE(Company.'find()Adressbüchern. Name, "; ", Company.'find()' .DataArea)</span><span class="sxs-lookup"><span data-stu-id="65045-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="65045-224">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="65045-224">Click Save.</span></span>
25. <span data-ttu-id="65045-225">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="65045-225">Close the page.</span></span>
26. <span data-ttu-id="65045-226">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="65045-226">Click Save.</span></span>
27. <span data-ttu-id="65045-227">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="65045-227">Close the page.</span></span>
28. <span data-ttu-id="65045-228">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="65045-228">Close the page.</span></span>
29. <span data-ttu-id="65045-229">Wählen Sie "Ja" im Feld "Testentwurf".</span><span class="sxs-lookup"><span data-stu-id="65045-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="65045-230">Verwenden Sie eine vorhandene ER-Modellzuordnungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="65045-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="65045-231">Wählen Sie in der Struktur 'Muster\Datenmodell'.</span><span class="sxs-lookup"><span data-stu-id="65045-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="65045-232">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="65045-232">Click Run.</span></span>
    * <span data-ttu-id="65045-233">Beachten Sie, dass die ausgewählte ER-Formatkonfiguration der Entwurfsversion nicht ausgeführt werden, weil es mehr als eine vorbildliche Zuordnungskonfiguration gibt, die für das definierten Datenmodell nicht verfügbar ist, das als Datenquelle des Ausführungsbeginns ER-Formats ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="65045-233">Note that the selected draft version of the ER format configuration can’t be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="65045-234">Definieren Sie als Nächstes die Zuordnungskonfiguration des alternativen Modells da, die von der als vorbildliche Zuordnungen Datenquellen für die Ausführung von ER-Format verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="65045-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="65045-235">Wählen Sie in der Struktur Musterdatenmodell\Musterzuordnung (alternativ).</span><span class="sxs-lookup"><span data-stu-id="65045-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="65045-236">Wählen Sie die Option „Ja” im Feld „Standard für Modellzuordnung” aus.</span><span class="sxs-lookup"><span data-stu-id="65045-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="65045-237">Wählen Sie in der Struktur 'Muster\Datenmodell'.</span><span class="sxs-lookup"><span data-stu-id="65045-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="65045-238">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="65045-238">Click Run.</span></span>
7. <span data-ttu-id="65045-239">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="65045-239">Click OK.</span></span>
    * <span data-ttu-id="65045-240">Beachten Sie, dass die Standardmodellzuordnungskonfiguration von dieser Formatkonfiguration für die Generierung elektronischer Dokumente verwendet wird (die erstellten Ausgaben enthält den Unternehmenscode).</span><span class="sxs-lookup"><span data-stu-id="65045-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  

