---
title: "Qualitätsprüfungsaufträge einrichten"
description: "Diese Prozedur zeigt Ihnen an, wie ein Qualitätsmanagementprozess aktiviert wird, in dem eingehender Lagerbestand direkt nach der Eingangsregistrierung geprüft werden muss."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 73981313fc662094ee4f8bb15a88271e16d41193
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-quality-orders"></a><span data-ttu-id="25a65-103">Qualitätsprüfungsaufträge einrichten</span><span class="sxs-lookup"><span data-stu-id="25a65-103">Set up quality orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25a65-104">Diese Prozedur zeigt Ihnen an, wie ein Qualitätsmanagementprozess aktiviert wird, in dem eingehender Lagerbestand direkt nach der Eingangsregistrierung geprüft werden muss.</span><span class="sxs-lookup"><span data-stu-id="25a65-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="25a65-105">Die Prozedur wird normalerweise von einem Qualitätsmanager ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25a65-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="25a65-106">Der Prozess umfasst die Erstellung einer Qualitätsgruppe, um die Artikel zu definieren, bei denen Stichproben durchgeführt werden, und eine Testgruppe, um die Tests zu gruppieren, die an Artikeln in der Qualitätsgruppe ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="25a65-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="25a65-107">Sie können diesen Leitfaden im Demodatunternehmen USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="25a65-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="25a65-108">Qualitätsmanagement aktivieren</span><span class="sxs-lookup"><span data-stu-id="25a65-108">Enable quality management</span></span>
1. <span data-ttu-id="25a65-109">Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Lager- und Lagerortverwaltungsparameter".</span><span class="sxs-lookup"><span data-stu-id="25a65-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="25a65-110">Klicken Sie auf die Registerkarte "Qualitätsmanagement".</span><span class="sxs-lookup"><span data-stu-id="25a65-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="25a65-111">Setzen Sie die Option Qualitätsmanagement verwenden auf Ja.</span><span class="sxs-lookup"><span data-stu-id="25a65-111">Set the Use quality management option to Yes.</span></span>
4. <span data-ttu-id="25a65-112">Klicken Sie auf "Berichtseinstellungen".</span><span class="sxs-lookup"><span data-stu-id="25a65-112">Click Report setup.</span></span>
    * <span data-ttu-id="25a65-113">In USMF sind die Berichtseinstellungen für das Qualitätsmanagement bereits definiert.</span><span class="sxs-lookup"><span data-stu-id="25a65-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="25a65-114">Wenn dieses nicht getan wäre, würden Sie hier neue Positionen für die verschiedenen Berichtstypen hinzufügen und den Dokumenttyp auswählen, der für jeden Bericht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="25a65-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="25a65-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="25a65-115">Close the page.</span></span>
6. <span data-ttu-id="25a65-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="25a65-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="25a65-117">Einen Test erstellen</span><span class="sxs-lookup"><span data-stu-id="25a65-117">Create a test</span></span>
1. <span data-ttu-id="25a65-118">Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätskontrolle" > "Tests".</span><span class="sxs-lookup"><span data-stu-id="25a65-118">Go to Inventory management > Setup > Quality control > Tests.</span></span>
2. <span data-ttu-id="25a65-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="25a65-119">Click New.</span></span>
3. <span data-ttu-id="25a65-120">Geben Sie im Feld "Test" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-120">In the Test field, type a value.</span></span>
4. <span data-ttu-id="25a65-121">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="25a65-122">Wählen Sie im Feld "Typ" die Option "Option" aus.</span><span class="sxs-lookup"><span data-stu-id="25a65-122">In the Type field, select 'Option'.</span></span>
    * <span data-ttu-id="25a65-123">In diesem Beispiel wählen wir "Option" aus, damit können wir die Testergebnisse basierend auf vordefinierten Werten zuweisen.</span><span class="sxs-lookup"><span data-stu-id="25a65-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="25a65-124">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="25a65-124">Click Save.</span></span>
7. <span data-ttu-id="25a65-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="25a65-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="25a65-126">Erstellen von Testvariablen zum Definieren des Verfahrens zur Erfassung von Testergebnissen</span><span class="sxs-lookup"><span data-stu-id="25a65-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="25a65-127">Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätskontrolle" > "Testvariablen".</span><span class="sxs-lookup"><span data-stu-id="25a65-127">Go to Inventory management > Setup > Quality control > Test variables.</span></span>
2. <span data-ttu-id="25a65-128">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="25a65-128">Click New.</span></span>
3. <span data-ttu-id="25a65-129">Geben Sie im Feld "Variable" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-129">In the Variable field, type a value.</span></span>
4. <span data-ttu-id="25a65-130">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="25a65-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="25a65-131">Click Save.</span></span>
6. <span data-ttu-id="25a65-132">Klicken Sie auf "Ergebnisse".</span><span class="sxs-lookup"><span data-stu-id="25a65-132">Click Outcomes.</span></span>
7. <span data-ttu-id="25a65-133">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="25a65-133">Click New.</span></span>
8. <span data-ttu-id="25a65-134">Geben Sie im Feld "Ergebnis" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-134">In the Outcome field, type a value.</span></span>
9. <span data-ttu-id="25a65-135">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-135">In the Description field, type a value.</span></span>
10. <span data-ttu-id="25a65-136">Wählen Sie im Feld "Ergebnisstatus" die Option "Erfolgreich" aus.</span><span class="sxs-lookup"><span data-stu-id="25a65-136">In the Outcome status field, select 'Pass'.</span></span>
11. <span data-ttu-id="25a65-137">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="25a65-137">Click Save.</span></span>
12. <span data-ttu-id="25a65-138">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="25a65-138">Click New.</span></span>
13. <span data-ttu-id="25a65-139">Geben Sie im Feld "Ergebnis" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-139">In the Outcome field, type a value.</span></span>
14. <span data-ttu-id="25a65-140">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-140">In the Description field, type a value.</span></span>
15. <span data-ttu-id="25a65-141">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="25a65-141">Click Save.</span></span>
16. <span data-ttu-id="25a65-142">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="25a65-142">Close the page.</span></span>
17. <span data-ttu-id="25a65-143">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="25a65-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="25a65-144">"Artikelmusteraufnahme" einrichten</span><span class="sxs-lookup"><span data-stu-id="25a65-144">Set up item sampling</span></span>
1. <span data-ttu-id="25a65-145">Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätskontrolle" > "Artikelmusteraufnahme".</span><span class="sxs-lookup"><span data-stu-id="25a65-145">Go to Inventory management > Setup > Quality control > Item sampling.</span></span>
2. <span data-ttu-id="25a65-146">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="25a65-146">Click New.</span></span>
3. <span data-ttu-id="25a65-147">Geben Sie im Feld "Artikelmusteraufnahme" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-147">In the Item sampling field, type a value.</span></span>
4. <span data-ttu-id="25a65-148">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-148">In the Description field, type a value.</span></span>
5. <span data-ttu-id="25a65-149">Geben Sie im Feld "Wert" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-149">In the Value field, enter a number.</span></span>
    * <span data-ttu-id="25a65-150">Dieser Wert bezieht sich auf die "Mengenspezifikation", die im angrenzenden Feld ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="25a65-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="25a65-151">Erweitern oder reduzieren Sie den Abschnitt 'Prozess'.</span><span class="sxs-lookup"><span data-stu-id="25a65-151">Expand or collapse the Process section.</span></span>
7. <span data-ttu-id="25a65-152">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Vollständige Sperrung".</span><span class="sxs-lookup"><span data-stu-id="25a65-152">Select or clear the Full blocking check box.</span></span>
    * <span data-ttu-id="25a65-153">Wenn Sie diese Option auswählen, wird alles oder die Auftragspositionsmenge gesperrt, wenn ein Test fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="25a65-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="25a65-154">Wenn Sie sie nicht auswählen, werden nur die Artikel in der Testbestellung gesperrt.</span><span class="sxs-lookup"><span data-stu-id="25a65-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="25a65-155">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="25a65-155">Click Save.</span></span>
9. <span data-ttu-id="25a65-156">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="25a65-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="25a65-157">Eine Qualitätsgruppe erstellen</span><span class="sxs-lookup"><span data-stu-id="25a65-157">Create a quality group</span></span>
1. <span data-ttu-id="25a65-158">Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätskontrolle" > "Qualitätsgruppen".</span><span class="sxs-lookup"><span data-stu-id="25a65-158">Go to Inventory management > Setup > Quality control > Quality groups.</span></span>
2. <span data-ttu-id="25a65-159">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="25a65-159">Click New.</span></span>
3. <span data-ttu-id="25a65-160">Geben Sie im Feld "Qualitätsgruppe" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-160">In the Quality group field, type a value.</span></span>
    * <span data-ttu-id="25a65-161">Verwenden Sie einen beschreibenden Namen, damit Sie identifizieren können, welche Art von Artikeln die Gruppe enthalten wird (Ihre Sampling-Kriterien).</span><span class="sxs-lookup"><span data-stu-id="25a65-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="25a65-162">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="25a65-163">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="25a65-163">Click Save.</span></span>
6. <span data-ttu-id="25a65-164">Klicken Sie auf Artikel hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="25a65-164">Click Add items.</span></span>
7. <span data-ttu-id="25a65-165">Die Zeile "Artikelnummer" auswählen</span><span class="sxs-lookup"><span data-stu-id="25a65-165">Select the Item number row</span></span>
    * <span data-ttu-id="25a65-166">In diesem Beispiel wird der Filter auf Grundlage der Artikelnummer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25a65-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="25a65-167">Geben Sie im Feld "Kriterien" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-167">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="25a65-168">Beispielsweise Typ T*, um nach den Artikelnummern zu filtern, die mit T starten.</span><span class="sxs-lookup"><span data-stu-id="25a65-168">For example, type T* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="25a65-169">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="25a65-169">Click OK.</span></span>
10. <span data-ttu-id="25a65-170">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="25a65-170">Click OK.</span></span>
11. <span data-ttu-id="25a65-171">Klicken Sie auf "Artikelqualitätsgruppen".</span><span class="sxs-lookup"><span data-stu-id="25a65-171">Click Item quality groups.</span></span>
12. <span data-ttu-id="25a65-172">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="25a65-172">Close the page.</span></span>
13. <span data-ttu-id="25a65-173">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="25a65-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="25a65-174">Erstellen einer Testgruppe</span><span class="sxs-lookup"><span data-stu-id="25a65-174">Create a test group</span></span>
1. <span data-ttu-id="25a65-175">Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätskontrolle" > "Testgruppen".</span><span class="sxs-lookup"><span data-stu-id="25a65-175">Go to Inventory management > Setup > Quality control > Test groups.</span></span>
2. <span data-ttu-id="25a65-176">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="25a65-176">Click New.</span></span>
3. <span data-ttu-id="25a65-177">Geben Sie im Feld "Testgruppe" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-177">In the Test group field, type a value.</span></span>
    * <span data-ttu-id="25a65-178">Geben Sie der Testgruppe einen Namen, womit Sie sich merken können, welche Arten von Tests ausgeführt werden und welcher Qualitätsgruppe sie zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="25a65-178">Give the Test group a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="25a65-179">Beispielsweise, wenn sie mit einer Qualitätsgruppe verwendet wird, die Artikel auswählt, die mit "T" anfangen, könnten Sie sie "T-Artikel-Tests" nennen.</span><span class="sxs-lookup"><span data-stu-id="25a65-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="25a65-180">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-180">In the Description field, type a value.</span></span>
5. <span data-ttu-id="25a65-181">Wählen Sie im Feld "Artikelmusteraufnahme" die Artikelmusteraufnahmeposition aus, die Sie zuvor erstellten.</span><span class="sxs-lookup"><span data-stu-id="25a65-181">In the Item sampling field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="25a65-182">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="25a65-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="25a65-183">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="25a65-183">Click Add.</span></span>
8. <span data-ttu-id="25a65-184">Geben Sie im Feld "Laufende Nummer" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="25a65-184">In the Sequence number field, enter a number.</span></span>
9. <span data-ttu-id="25a65-185">Wählen Sie im Feld "Test" den Test aus, den Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="25a65-185">In the Test field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="25a65-186">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="25a65-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="25a65-187">Klicken Sie auf die Registerkarte Test.</span><span class="sxs-lookup"><span data-stu-id="25a65-187">Click the Test tab.</span></span>
12. <span data-ttu-id="25a65-188">Wählen Sie im Feld "Variable" die Variable aus, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="25a65-188">In the Variable field, select the test variable that you created before</span></span>
13. <span data-ttu-id="25a65-189">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="25a65-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="25a65-190">Klicken Sie im Feld "Standardergebnis" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="25a65-190">In the Default outcome field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="25a65-191">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="25a65-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="25a65-192">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="25a65-192">Click Save.</span></span>
17. <span data-ttu-id="25a65-193">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="25a65-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="25a65-194">Definieren, wann Testbestellungen erstellt werden</span><span class="sxs-lookup"><span data-stu-id="25a65-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="25a65-195">Wechseln Sie zu "Lagerverwaltung" > "Einstellungen" > "Qualitätskontrolle" > "Qualitätszuordnungen".</span><span class="sxs-lookup"><span data-stu-id="25a65-195">Go to Inventory management > Setup > Quality control > Quality associations.</span></span>
2. <span data-ttu-id="25a65-196">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="25a65-196">Click New.</span></span>
3. <span data-ttu-id="25a65-197">Wählen Sie im Feld "Referenztyp" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="25a65-197">In the Reference type field, select an option.</span></span>
4. <span data-ttu-id="25a65-198">Wählen Sie im Feld "Artikelcode" die Option "Gruppe" aus.</span><span class="sxs-lookup"><span data-stu-id="25a65-198">In the Item code field, select 'Group'.</span></span>
    * <span data-ttu-id="25a65-199">In diesem Beispiel wählen wir" Gruppe" aus und verwenden die Qualitätsgruppe, die wir zuvor erstellt hatten.</span><span class="sxs-lookup"><span data-stu-id="25a65-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="25a65-200">Sie können dies auch als "Tabelle" festlegen, um die Artikel manuell anzugeben, oder Sie können "Alle" auswählen, um alle Artikel der Testbestellung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="25a65-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="25a65-201">Wählen Sie im Feld "Artikel" die Qualitätsgruppe aus, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="25a65-201">In the Item field, select the quality group that you created before.</span></span>
    * <span data-ttu-id="25a65-202">Die Optionen, die im Feld "Artikel" verfügbar sind, hängen davon ab, was Sie im Feld "Artikelcode" festlegen.</span><span class="sxs-lookup"><span data-stu-id="25a65-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="25a65-203">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="25a65-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="25a65-204">Erweitern oder reduzieren Sie den Abschnitt 'Prozess'.</span><span class="sxs-lookup"><span data-stu-id="25a65-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="25a65-205">Wählen Sie im Feld "Ereignistyp" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="25a65-205">In the Event type field, select an option.</span></span>
    * <span data-ttu-id="25a65-206">Dies ist das Ereignis, das den Test auslöst.</span><span class="sxs-lookup"><span data-stu-id="25a65-206">This is the event that triggers the test.</span></span> <span data-ttu-id="25a65-207">Die hier verfügbaren Optionen hängen davon ab, welchen Prozess Sie im Feld "Referenztyp" ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="25a65-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="25a65-208">Wählen Sie im Feld "Ausführung" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="25a65-208">In the Execution field, select an option.</span></span>
10. <span data-ttu-id="25a65-209">Erweitern oder reduzieren Sie den Abschnitt 'Qualitätsauftragsprozess'.</span><span class="sxs-lookup"><span data-stu-id="25a65-209">Expand or collapse the Quality order process section.</span></span>
11. <span data-ttu-id="25a65-210">Klicken Sie im Feld "Ereignissperrung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="25a65-210">In the Event blocking field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25a65-211">Dieses Feld zeigt die Liste der Prozesse an, die gesperrt werden können, wenn die Testbestellung noch offen ist.</span><span class="sxs-lookup"><span data-stu-id="25a65-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="25a65-212">Die Optionen hängen davon ab, was Sie im Feld "Ereignistyp" ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="25a65-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="25a65-213">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="25a65-213">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="25a65-214">Dies hängt von den vorher ausgewählten Werten ab.</span><span class="sxs-lookup"><span data-stu-id="25a65-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="25a65-215">Wählen Sie aus, ob die folgenden Prozesse gesperrt werden müssen, während Sie offene Testbestellungen mit einer Quelldokumentposition verknüpfen lassen.</span><span class="sxs-lookup"><span data-stu-id="25a65-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="25a65-216">Erweitern oder reduzieren Sie den Abschnitt 'Spezifikationen'.</span><span class="sxs-lookup"><span data-stu-id="25a65-216">Expand or collapse the Specifications section.</span></span>
14. <span data-ttu-id="25a65-217">Wählen Sie im Feld "Testgruppe" die Testgruppe aus, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="25a65-217">In the Test group field, select the test group that you created before.</span></span>
15. <span data-ttu-id="25a65-218">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="25a65-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="25a65-219">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="25a65-219">Click Save.</span></span>
17. <span data-ttu-id="25a65-220">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="25a65-220">Close the page.</span></span>

