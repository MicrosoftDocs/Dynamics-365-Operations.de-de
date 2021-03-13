---
title: ER-Modellzuordnungen in separaten EB-Konfigurationen verwalten
description: In diesem Thema wird beschrieben, wie Sie EB-Modellzuordnungen (elektronische Berichterstellung) in separaten EB-Konfigurationen verwalten.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f1013cfc9f421525fb0661cd5ace5eeaa157f9a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093797"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="8a778-103">EB-Modellzuordnung in getrennten EB-Konfigurationen verwalten</span><span class="sxs-lookup"><span data-stu-id="8a778-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a778-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, einen Konfigurationsanbieter für elektronische Berichterstellung (ER) erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="8a778-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="8a778-105">In diesem Aufgabenleitfaden erstellen Sie erforderliche ER-Konfigurationen für das Beispielunternehmen, Litware, Inc., um diesen Aufgabenleitfaden abzuschließen, müssen Sie die Schritte im Aufgabenleitfaden erst abschließen, „ER bieten einen Konfigurationsanbieter“ erstellen und als aktiv markieren, ihn.</span><span class="sxs-lookup"><span data-stu-id="8a778-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="8a778-106">Da ER-Konfigurationen unter Unternehmen freigegeben werden, können Sie diese Aufgabenleitfaden mithilfe der Unternehmensdaten aus, die von Ihrer Auswahl werden gefestgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8a778-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="8a778-107">Die Funktionen für diesen Aufgabenleitfaden sind nur verfügbar, wenn Sie einen der folgenden Hotfixes installiert haben: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 für die Dynamics AX 7.0 Version oder https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 für die Dynamics 365 for Operations Version.</span><span class="sxs-lookup"><span data-stu-id="8a778-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="8a778-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="8a778-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="8a778-109">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist.</span><span class="sxs-lookup"><span data-stu-id="8a778-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="8a778-110">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="8a778-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider, and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="8a778-111">Neue ER-Modellkonfiguration hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8a778-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="8a778-112">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="8a778-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="8a778-113">Neue ER-Modellkonfiguration hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a778-113">Add a new model configuration.</span></span> <span data-ttu-id="8a778-114">Der Name des Profils muss in der Konfigurationsstruktur eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="8a778-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="8a778-115">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a778-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="8a778-116">Geben Sie im Feld "Name" Datenmodellkonfiguration" ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="8a778-117">Muster-Datenmodell</span><span class="sxs-lookup"><span data-stu-id="8a778-117">Sample data model</span></span>  
4. <span data-ttu-id="8a778-118">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a778-118">Click Create configuration.</span></span>
5. <span data-ttu-id="8a778-119">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8a778-119">Click Designer.</span></span>
6. <span data-ttu-id="8a778-120">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="8a778-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="8a778-121">Geben Sie im Feld Name "Root" ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="8a778-122">Stamm</span><span class="sxs-lookup"><span data-stu-id="8a778-122">Root</span></span>  
8. <span data-ttu-id="8a778-123">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a778-123">Click Add.</span></span>
9. <span data-ttu-id="8a778-124">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="8a778-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="8a778-125">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="8a778-126">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="8a778-126">Company</span></span>  
11. <span data-ttu-id="8a778-127">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a778-127">Click Add.</span></span>
12. <span data-ttu-id="8a778-128">Im Feld Beschreibung geben Sie den Text, die Beschreibung der juristischen Personen oder des Unternehmen, in denen ein Benutzer zur Laufzeit protokollierte ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="8a778-129">Beschreibung der juristischen Person oder des Unternehmens, bei denen Benutzer zur Laufzeit protokollierte.</span><span class="sxs-lookup"><span data-stu-id="8a778-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="8a778-130">Stammreferenz anklicken.</span><span class="sxs-lookup"><span data-stu-id="8a778-130">Click Root reference.</span></span>
14. <span data-ttu-id="8a778-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a778-131">Click OK.</span></span>
15. <span data-ttu-id="8a778-132">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8a778-132">Click Save.</span></span>
16. <span data-ttu-id="8a778-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a778-133">Close the page.</span></span>
17. <span data-ttu-id="8a778-134">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="8a778-134">Click Change status.</span></span>
18. <span data-ttu-id="8a778-135">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="8a778-135">Click Complete.</span></span>
19. <span data-ttu-id="8a778-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a778-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="8a778-137">Neue EB-Modellzuordnungskonfiguration hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8a778-137">Add a new ER model-mapping configuration</span></span>
1. <span data-ttu-id="8a778-138">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a778-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="8a778-139">Geben Sie im Feld "Neu" 'Modellzuordnung basierend auf Datenmodell-Beispielsdatenmodell ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="8a778-140">Geben Sie im Feld "Typ" Musterzuordnung ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="8a778-141">Musterzuordnung</span><span class="sxs-lookup"><span data-stu-id="8a778-141">Sample mapping</span></span>  
4. <span data-ttu-id="8a778-142">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a778-142">Click Create configuration.</span></span>
5. <span data-ttu-id="8a778-143">Erweitern des Abschnitts Voraussetzungen.</span><span class="sxs-lookup"><span data-stu-id="8a778-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="8a778-144">Die Implementierungs-Voraussetzungsgruppe wurde automatisch hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8a778-144">The Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="8a778-145">Diese Gruppe beinhaltet die erforderliche Komponente, die die Datenmodellkonfiguration bezieht und die Implementierungsmarkierung hat, die aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8a778-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="8a778-146">Diese Markierung gibt an, dass diese Modellzuordnungskonfiguration als „Beispielzuordnung“ zur Implementierung des „Beispieldatenmodells“ gilt.</span><span class="sxs-lookup"><span data-stu-id="8a778-146">This means that this Sample-mapping model-mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="8a778-147">Diese Komponente zwingt die EB, die Modellzuordnungskonfiguration für die Beispielzuordnung von einem EB-Repository herunterzuladen, sobald die Modellkonfiguration für das Beispieldatenmodell heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="8a778-147">Therefore, this component will force ER to download the model-mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="8a778-148">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8a778-148">Click Designer.</span></span>
    * <span data-ttu-id="8a778-149">Die erstellte Modellzuordnungskonfiguration enthält eine neue leere Zuordnung mit demselben Namen wie die erstellte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8a778-149">The created model-mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="8a778-150">Wenn eine ausgewählte übergeordnete Modellkonfiguration Modellzuordnungen enthält, werden diese in eine neue Modellzuordnungskonfiguration kopiert.</span><span class="sxs-lookup"><span data-stu-id="8a778-150">When a selected parent model configuration contains model mappings, they will be copied to a new model-mapping configuration.</span></span>   
7. <span data-ttu-id="8a778-151">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8a778-151">Click Designer.</span></span>
8. <span data-ttu-id="8a778-152">Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabelle' aus.</span><span class="sxs-lookup"><span data-stu-id="8a778-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="8a778-153">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8a778-153">Click Add root.</span></span>
10. <span data-ttu-id="8a778-154">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="8a778-155">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="8a778-155">Company</span></span>  
11. <span data-ttu-id="8a778-156">Im Tabellenfeld geben Sie "CompanyInfo" ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="8a778-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="8a778-157">CompanyInfo</span></span>  
12. <span data-ttu-id="8a778-158">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a778-158">Click OK.</span></span>
13. <span data-ttu-id="8a778-159">Erweitern Sie in der Struktur Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="8a778-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="8a778-160">In der Struktur erweitern Sie das Feld Unternehmen\Suchen ().</span><span class="sxs-lookup"><span data-stu-id="8a778-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="8a778-161">Wählen Sie in der Struktur 'Unternehmen\Namen\finden'.</span><span class="sxs-lookup"><span data-stu-id="8a778-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="8a778-162">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8a778-162">Click Bind.</span></span>
17. <span data-ttu-id="8a778-163">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8a778-163">Click Save.</span></span>
18. <span data-ttu-id="8a778-164">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a778-164">Close the page.</span></span>
19. <span data-ttu-id="8a778-165">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a778-165">Close the page.</span></span>
20. <span data-ttu-id="8a778-166">Klicken Sie im Aktivitätsbereich auf Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8a778-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="8a778-167">Klicken Sie auf Benutzerparameter.</span><span class="sxs-lookup"><span data-stu-id="8a778-167">Click User parameters.</span></span>
22. <span data-ttu-id="8a778-168">Wählen Sie "Ja" im Feld "Testlaufeinstellungen".</span><span class="sxs-lookup"><span data-stu-id="8a778-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="8a778-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a778-169">Click OK.</span></span>
24. <span data-ttu-id="8a778-170">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8a778-170">Click Edit.</span></span>
25. <span data-ttu-id="8a778-171">Wählen Sie "Ja" im Feld "Testentwurf".</span><span class="sxs-lookup"><span data-stu-id="8a778-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="8a778-172">Neues ER-Modellformat hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8a778-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="8a778-173">Wählen Sie in der Struktur 'Muster Datenmodell'.</span><span class="sxs-lookup"><span data-stu-id="8a778-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="8a778-174">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a778-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="8a778-175">Geben Sie im Feld "Neu" 'Format basierend auf Modell Musterdatenmodell' ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="8a778-176">Geben Sie im Feld "Typ" Musterformat ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="8a778-177">Beispielformat</span><span class="sxs-lookup"><span data-stu-id="8a778-177">Sample format</span></span>  
5. <span data-ttu-id="8a778-178">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a778-178">Click Create configuration.</span></span>
6. <span data-ttu-id="8a778-179">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8a778-179">Click Designer.</span></span>
7. <span data-ttu-id="8a778-180">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a778-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="8a778-181">Wählen Sie in der Struktur 'Text\String' aus.</span><span class="sxs-lookup"><span data-stu-id="8a778-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="8a778-182">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a778-182">Click OK.</span></span>
10. <span data-ttu-id="8a778-183">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="8a778-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="8a778-184">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="8a778-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="8a778-185">Wählen Sie in der Struktur Modell\Unternehmen aus.</span><span class="sxs-lookup"><span data-stu-id="8a778-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="8a778-186">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="8a778-186">Click Bind.</span></span>
14. <span data-ttu-id="8a778-187">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8a778-187">Click Save.</span></span>
15. <span data-ttu-id="8a778-188">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a778-188">Close the page.</span></span>
    * <span data-ttu-id="8a778-189">Führt die Entwurfsversion des erstellten Formats für Testzwecke aus.</span><span class="sxs-lookup"><span data-stu-id="8a778-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="8a778-190">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="8a778-190">Click Run.</span></span>
    * <span data-ttu-id="8a778-191">Wählen Sie in der Version Inforegister ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a778-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="8a778-192">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a778-192">Click OK.</span></span>
    * <span data-ttu-id="8a778-193">Wiederholen Sie die Ausgabe, die den Namen des Unternehmens enthält, in dem der Benutzer, der ausgeführt wird, diese Formatkonfiguration angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="8a778-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="8a778-194">Die erstellte Modellzuordnungskonfiguration wird von dieser Formatkonfiguration verwendet, da es nur eine verfügbare Konfiguration gibt, die erforderliche Modellzuordnungen enthält.</span><span class="sxs-lookup"><span data-stu-id="8a778-194">The created model-mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="8a778-195">Alternative EB-Modellzuordnungskonfiguration hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8a778-195">Add alternative ER model-mapping configuration</span></span>
1. <span data-ttu-id="8a778-196">Wählen Sie in der Struktur 'Muster Datenmodell'.</span><span class="sxs-lookup"><span data-stu-id="8a778-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="8a778-197">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a778-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="8a778-198">Geben Sie im Feld "Neu" 'Modellzuordnung basierend auf Datenmodell-Beispielsdatenmodell ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="8a778-199">Geben Sie im Feld "Typ" Musterzurodnung (alternativ) ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="8a778-200">Beispielzuordnung (Alternative)</span><span class="sxs-lookup"><span data-stu-id="8a778-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="8a778-201">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a778-201">Click Create configuration.</span></span>
6. <span data-ttu-id="8a778-202">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8a778-202">Click Designer.</span></span>
7. <span data-ttu-id="8a778-203">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8a778-203">Click Designer.</span></span>
8. <span data-ttu-id="8a778-204">Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabelle' aus.</span><span class="sxs-lookup"><span data-stu-id="8a778-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="8a778-205">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="8a778-205">Click Add root.</span></span>
10. <span data-ttu-id="8a778-206">Geben Sie im Feld Name "Firma" ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="8a778-207">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="8a778-207">Company</span></span>  
11. <span data-ttu-id="8a778-208">Im Tabellenfeld geben Sie "CompanyInfo" ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="8a778-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="8a778-209">CompanyInfo</span></span>  
12. <span data-ttu-id="8a778-210">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a778-210">Click OK.</span></span>
13. <span data-ttu-id="8a778-211">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8a778-211">Click Edit.</span></span>
14. <span data-ttu-id="8a778-212">Wählen Sie in der Struktur 'String\CONCATENATE' aus.</span><span class="sxs-lookup"><span data-stu-id="8a778-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="8a778-213">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a778-213">Click Add function.</span></span>
16. <span data-ttu-id="8a778-214">Erweitern Sie in der Struktur Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="8a778-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="8a778-215">In der Struktur erweitern Sie das Feld Unternehmen\Suchen ().</span><span class="sxs-lookup"><span data-stu-id="8a778-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="8a778-216">Wählen Sie in der Struktur 'Unternehmen\Namen\finden'.</span><span class="sxs-lookup"><span data-stu-id="8a778-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="8a778-217">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a778-217">Click Add data source.</span></span>
20. <span data-ttu-id="8a778-218">Geben Sie im Feld "Formel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="8a778-219">e Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="8a778-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="8a778-220">Wählen Sie in der Struktur 'Unternehmen\finden()\Unternehmen(DataArea).</span><span class="sxs-lookup"><span data-stu-id="8a778-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="8a778-221">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8a778-221">Click Add data source.</span></span>
23. <span data-ttu-id="8a778-222">Geben Sie im Feld "Formel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8a778-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="8a778-223">CONCATENATE(Company.'find()Adressbüchern. Name, "; ", Company.'find()' .DataArea)</span><span class="sxs-lookup"><span data-stu-id="8a778-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="8a778-224">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8a778-224">Click Save.</span></span>
25. <span data-ttu-id="8a778-225">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a778-225">Close the page.</span></span>
26. <span data-ttu-id="8a778-226">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8a778-226">Click Save.</span></span>
27. <span data-ttu-id="8a778-227">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a778-227">Close the page.</span></span>
28. <span data-ttu-id="8a778-228">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8a778-228">Close the page.</span></span>
29. <span data-ttu-id="8a778-229">Wählen Sie "Ja" im Feld "Testentwurf".</span><span class="sxs-lookup"><span data-stu-id="8a778-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="8a778-230">Eine vorhandene EB-Modellzuordnungskonfiguration verwenden</span><span class="sxs-lookup"><span data-stu-id="8a778-230">Use an existing ER model-mapping configuration</span></span>
1. <span data-ttu-id="8a778-231">Wählen Sie in der Struktur 'Muster\Datenmodell'.</span><span class="sxs-lookup"><span data-stu-id="8a778-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="8a778-232">Klicken Sie auf Ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a778-232">Click Run.</span></span>
    * <span data-ttu-id="8a778-233">Die ausgewählte Entwurfsversion der EB-Formatkonfiguration kann nicht ausgeführt werden, weil es mehr als eine Modellzuordnungskonfiguration gibt, die für das nicht definierte Datenmodell verfügbar ist, das als Datenquelle für das ausgeführte EB-Format ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="8a778-233">The selected draft version of the ER format configuration can't be executed because there is more than one model-mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="8a778-234">Definieren Sie als Nächstes die alternative Modellzuordnungskonfiguration als diejenige Konfiguration, aus der Modellzuordnungen als Datenquellen für das ausgeführte EB-Format verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a778-234">Next, you will define the alternative model-mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="8a778-235">Wählen Sie in der Struktur Musterdatenmodell\Musterzuordnung (alternativ).</span><span class="sxs-lookup"><span data-stu-id="8a778-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="8a778-236">Wählen Sie die Option „Ja” im Feld „Standard für Modellzuordnung” aus.</span><span class="sxs-lookup"><span data-stu-id="8a778-236">Select Yes in the Default for model-mapping field.</span></span>
5. <span data-ttu-id="8a778-237">Wählen Sie in der Struktur 'Muster\Datenmodell'.</span><span class="sxs-lookup"><span data-stu-id="8a778-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="8a778-238">Klicken Sie auf Ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a778-238">Click Run.</span></span>
7. <span data-ttu-id="8a778-239">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a778-239">Click OK.</span></span>
    * <span data-ttu-id="8a778-240">Die Standardkonfiguration der Modellzuordnung wird von dieser Formatkonfiguration zur Generierung elektronischer Dokumente verwendet (die erstellte Ausgabe enthält den Buchungskreis).</span><span class="sxs-lookup"><span data-stu-id="8a778-240">The default model-mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  

