---
title: Regression Suite Automation Tool-Tutorial
description: Dieses Thema zeigt, wie das Regression Suite Automation Tool (RSAT) verwendet wird. Es beschreibt die verschiedenen Funktionen und enthält Beispiele, die erweiterte Skripterstellung verwenden.
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 5a9f19168093f24a7f152b2b5b23b3728ca80222
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745164"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="356ae-104">Regression Suite Automation Tool-Tutorial</span><span class="sxs-lookup"><span data-stu-id="356ae-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="356ae-105">Verwenden Sie das Internet-Browsertool, um die Seite in pdf-Format herunterzuladen und zu speichern.</span><span class="sxs-lookup"><span data-stu-id="356ae-105">Use your internet browser tools to download and save this page in pdf format.</span></span>

<span data-ttu-id="356ae-106">Dies Tutorial führt Sie durch mehrere der erweiterten Funktionen des Regression Suite Automation Tool (RSAT), enthält eine Demozuweisung und beschreibt Strategie und wichtige Lernpunkte.</span><span class="sxs-lookup"><span data-stu-id="356ae-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="356ae-107">Bemerkenswerte Funktionen von RSAT und Aufgabenaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="356ae-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="356ae-108">Einen Feldwert überprüfen</span><span class="sxs-lookup"><span data-stu-id="356ae-108">Validate a field value</span></span>

<span data-ttu-id="356ae-109">Mit RSAT können Sie Validierungsschritte in Ihren Testfall aufnehmen, um die erwarteten Werte zu validieren.</span><span class="sxs-lookup"><span data-stu-id="356ae-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="356ae-110">Informationen zu dieser Funktion finden Sie im Artikel [Überprüfen Sie die erwarteten Werte](rsat-validate-expected.md).</span><span class="sxs-lookup"><span data-stu-id="356ae-110">For information about this feature, see the article [Validate expected values](rsat-validate-expected.md).</span></span>

<span data-ttu-id="356ae-111">Das folgende Beispiel veranschaulicht, wie Sie diese Funktion verwenden können, um zu prüfen, ob der Lagerbestand mehr als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="356ae-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="356ae-112">In den Demodaten im **USMF**-Unternehmen erstellen Sie eine Aufgabenaufzeichnung, die die folgenden Schritte ausführt:</span><span class="sxs-lookup"><span data-stu-id="356ae-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="356ae-113">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="356ae-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="356ae-114">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="356ae-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="356ae-115">Filtern Sie beispielsweise auf einen Wert von **1000** für das Feld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="356ae-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="356ae-116">Wählen Sie **Verfügbarer Lagerbestand** aus</span><span class="sxs-lookup"><span data-stu-id="356ae-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="356ae-117">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="356ae-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="356ae-118">Filtern Sie beispielsweise auf einen Wert von **1** für das Feld **Website**.</span><span class="sxs-lookup"><span data-stu-id="356ae-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="356ae-119">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="356ae-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="356ae-120">Überprüfen Sie, dass der Wert des Feldes **Verfügbare Summe** **411,0000000000000000** ist.</span><span class="sxs-lookup"><span data-stu-id="356ae-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="356ae-121">Speichern Sie die Aufgabenaufzeichnung als eine **Entwickleraufzeichnung** und hängen Sie sie in Azure DevOps an Ihren Testfall an.</span><span class="sxs-lookup"><span data-stu-id="356ae-121">Save the task recording as a **developer recording** and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="356ae-122">Fügen Sie den Testfall dem Testplan hinzu, und laden Sie den Testfall in RSAT.</span><span class="sxs-lookup"><span data-stu-id="356ae-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="356ae-123">Öffnen Sie die Excel-Parameterdatei und wechseln Sie zum Register **TestCaseSteps**.</span><span class="sxs-lookup"><span data-stu-id="356ae-123">Open the Excel parameter file and go to the **TestCaseSteps** tab.</span></span>
5. <span data-ttu-id="356ae-124">Um zu überprüfen, ob der verfügbare Bestand immer größer ist als **0**, wechseln Sie zum Schritt **Gesamtverfügbarkeit prüfen** und ändern Sie seinen Wert von **411** zu **0**.</span><span class="sxs-lookup"><span data-stu-id="356ae-124">To validate whether the inventory on-hand will always be more than **0**, go to the **Validate Total Available** step and change its value from **411** to **0**.</span></span> <span data-ttu-id="356ae-125">Ändern Sie den Wert im Feld **Operator** von einem Gleichheitszeichen (**=**) in ein Größer-als-Zeichen (**\>**).</span><span class="sxs-lookup"><span data-stu-id="356ae-125">Change the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>
6. <span data-ttu-id="356ae-126">Speichern und schließen Sie die Excel-Parameterdatei.</span><span class="sxs-lookup"><span data-stu-id="356ae-126">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="356ae-127">Wählen Sie **Hochladen** aus, um die Änderungen zu speichern, die Sie an der Excel-Parameterdatei vorgenommen haben Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="356ae-127">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="356ae-128">Wenn der Wert des Feldes **Verfügbare Summe** jetzt für den angegebenen Artikel im Bestand größer als 0 (null) ist, sind Tests unabhängig vom tatsächlichen Wert des verfügbaren Bestands erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="356ae-128">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="356ae-129">Gespeicherte Variablen und Verkettung von Testfällen</span><span class="sxs-lookup"><span data-stu-id="356ae-129">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="356ae-130">Eine wichtige zentrale Funktion von RSAT ist das Verketten von Testfällen, das heißt, die Fähigkeit eines Tests, Variablen an andere Tests zu übergebe.</span><span class="sxs-lookup"><span data-stu-id="356ae-130">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="356ae-131">Weitere Informationen finden Sie im Artikel [Kopieren Sie Variablen in Kettentestfälle](rsat-chain-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="356ae-131">For more information, see the article [Copy variables to chain test cases](rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="356ae-132">Abgeleitete Testfälle</span><span class="sxs-lookup"><span data-stu-id="356ae-132">Derived test case</span></span>

<span data-ttu-id="356ae-133">Mit RSAT können Sie dieselbe Aufgabenaufzeichnung mit mehreren Testfällen verwenden, sodass eine Aufgabe mit unterschiedlichen Datenkonfigurationen ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="356ae-133">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="356ae-134">Siehe Artikel [Abgeleitete Testfälle](rsat-derived-test-cases.md) für mehr Informationen.</span><span class="sxs-lookup"><span data-stu-id="356ae-134">See the article [Derived test cases](rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="356ae-135">Überprüfen Sie Benachrichtigungen und Nachrichten</span><span class="sxs-lookup"><span data-stu-id="356ae-135">Validate notifications and messages</span></span>

<span data-ttu-id="356ae-136">Diese Funktion kann verwendet werden, um zu überprüfen, ob eine Aktivität stattfand.</span><span class="sxs-lookup"><span data-stu-id="356ae-136">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="356ae-137">Wenn ein Produktionsauftrag beispielsweise erstellt, vorkalkuliert und dann gestartet wird, zeigt die App eine „Produktion – Start“-Nachricht, die Sie darüber zu informieren, dass der Produktionsauftrag gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="356ae-137">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Produktion – Start-Benachrichtigung](./media/use_rsa_tool_05.png)

<span data-ttu-id="356ae-139">Sie können diese Meldung über RSAT überprüfen, indem Sie den Nachrichtentext auf der Registerkarte **MessageValidation** der Excel-Parameterdatei für die entsprechende Erfassung eingeben.</span><span class="sxs-lookup"><span data-stu-id="356ae-139">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Registerkarte Nachrichtenvalidierung](./media/use_rsa_tool_06.png)

<span data-ttu-id="356ae-141">Nachdem der Testfall ausgeführt wurde, wird die Nachricht in der Excel-Parameterdatei mit der Nachricht verglichen, die angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="356ae-141">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="356ae-142">Wenn die Nachrichten nicht übereinstimmen, schlägt der Testfall fehl.</span><span class="sxs-lookup"><span data-stu-id="356ae-142">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="356ae-143">Sie können mehrere Nachrichten auf der Registerkarte **MessageValidation** in der Excel-Parameterdatei eingeben.</span><span class="sxs-lookup"><span data-stu-id="356ae-143">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="356ae-144">Die Nachrichten können auch Fehler- oder Warnmeldungen anstelle der Informationsmeldungen sein.</span><span class="sxs-lookup"><span data-stu-id="356ae-144">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="356ae-145">Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="356ae-145">Snapshot</span></span>

<span data-ttu-id="356ae-146">Diese Funktion nimmt Screenshots der Schritte auf, die während der Aufgabenaufzeichnung ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="356ae-146">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="356ae-147">Es ist nützlich für Prüf- oder Debugging-Zwecke.</span><span class="sxs-lookup"><span data-stu-id="356ae-147">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="356ae-148">Um diese Funktion zu verwenden, öffnen Sie die Datei **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** im RSAT-Installationsordner (beispielsweise **C:\\Programme (x86)\\Regression Suite Automation Tool**), und ändern Sie den Wert des folgenden Elements von **false** auf **true**.</span><span class="sxs-lookup"><span data-stu-id="356ae-148">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="356ae-149">Wenn Sie den Testfall ausführen, generiert RSAT Snapshots (Bilder) der Schritte im Wiedergabeordner der Testfälle im Arbeitsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="356ae-149">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="356ae-150">Wenn Sie eine ältere Version von RSAT verwenden, werden die Bilder in **C\\Benutzer\\\<Username\>\\AppData\\Roaming\\regressionTool\\Playback** gespeichert und für jeden Testfall, der ausgeführt wird, wird ein separater Ordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="356ae-150">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="356ae-151">Zuweisung</span><span class="sxs-lookup"><span data-stu-id="356ae-151">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="356ae-152">Szenario</span><span class="sxs-lookup"><span data-stu-id="356ae-152">Scenario</span></span>

1. <span data-ttu-id="356ae-153">Der Produktdesigner erstellt ein neues veröffentlichtes Produkt.</span><span class="sxs-lookup"><span data-stu-id="356ae-153">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="356ae-154">Der Produktions-Manager initiiert einen Produktionsauftrag, um den Lagerbestand auf zwei Stück aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="356ae-154">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="356ae-155">Die Fertigung startet und beendet den Produktionsauftrag und überprüft, ob die verfügbare Menge zwei Stück beträgt.</span><span class="sxs-lookup"><span data-stu-id="356ae-155">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="356ae-156">Das Vertriebsteam erhält einen Auftrag für vier Stück des neuen Produkts.</span><span class="sxs-lookup"><span data-stu-id="356ae-156">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="356ae-157">Daher aktualisiert das Vertriebsteam den Nettobedarf anhand des dynamischen Plans.</span><span class="sxs-lookup"><span data-stu-id="356ae-157">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="356ae-158">Da keine Mehrkapazität verfügbar ist, wird die Standardauftragsrichtlinie aus „kaufen statt herstellen“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="356ae-158">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="356ae-159">Daher wird eine geplante Einkaufsbestellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="356ae-159">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="356ae-160">Der Käufer fügt einen Lieferanten hinzu, wandelt die geplante Einkaufsbestellung um und bestätigt die Bestellung anschließend.</span><span class="sxs-lookup"><span data-stu-id="356ae-160">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="356ae-161">Nachdem die gekauften Waren in Laden eingehen, sucht der Ladeninhaber die zugehörige Bestellung erhält die Waren.</span><span class="sxs-lookup"><span data-stu-id="356ae-161">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="356ae-162">Da die Bestellung nun abgeschlossen ist, können Waren für den Auftrag entnommen und verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="356ae-162">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="356ae-163">Finance bucht die Einkaufsrechnung und die Verkaufsrechnung.</span><span class="sxs-lookup"><span data-stu-id="356ae-163">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="356ae-164">Die folgende Abbildung zeigt den Ablauf für dieses Szenario.</span><span class="sxs-lookup"><span data-stu-id="356ae-164">The following illustration shows the flow for this scenario.</span></span>

![Ablauf für das Demoszenario](./media/use_rsa_tool_14.png)

<span data-ttu-id="356ae-166">Die folgende Abbildung zeigt die Geschäftsprozesshierarchie für dieses Szenario im LCS Business Process Modeler.</span><span class="sxs-lookup"><span data-stu-id="356ae-166">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Geschäftsprozesse für das Demoszenario](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="356ae-168">Strategie – Wichtige Lernpunkte</span><span class="sxs-lookup"><span data-stu-id="356ae-168">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="356ae-169">Daten</span><span class="sxs-lookup"><span data-stu-id="356ae-169">Data</span></span>

- <span data-ttu-id="356ae-170">Stellen Sie sicher, dass Sie repräsentative Datenmengen haben (eine Kopie der Produktion bzw. der goldenen Konfigurationsdaten und migrierte Daten).</span><span class="sxs-lookup"><span data-stu-id="356ae-170">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="356ae-171">Wenn Sie neue Daten über die Aufgabenaufzeichnung generieren, erstellen Sie Testnamen, die nicht mit vorhandenen Namen kollidieren, (verwenden Sie beispielsweise das Präfix **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="356ae-171">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="356ae-172">Verwenden Sie Point-In-Time-Wiederherstellung von Azure, um Tests in der nicht-Ebene-1-Umgebung zu wiederholen.</span><span class="sxs-lookup"><span data-stu-id="356ae-172">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="356ae-173">Zwar können Sie die Excel-Funktionen **ZUFÄLLIG** und **JETZT** verwenden, um eine eindeutige Kombination zu generieren, der Aufwand ist ausgesprochen hoch.</span><span class="sxs-lookup"><span data-stu-id="356ae-173">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="356ae-174">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="356ae-174">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="356ae-175">Aufgabenaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="356ae-175">Task recorder</span></span>

- <span data-ttu-id="356ae-176">Definieren Sie Szenarien, bevor Sie mit der Aufzeichnung beginnen.</span><span class="sxs-lookup"><span data-stu-id="356ae-176">Define scenarios before you start recording.</span></span> <span data-ttu-id="356ae-177">Ein in gut verwaltetes Projekt hat vordefinierte Testszenarien.</span><span class="sxs-lookup"><span data-stu-id="356ae-177">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="356ae-178">Um einen Testfall zu erstellen, berücksichtigen Sie, wie vorhersagbar das Ergebnis dieser Testszenarien ist.</span><span class="sxs-lookup"><span data-stu-id="356ae-178">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="356ae-179">Teilen Sie Aufzeichnungen, wenn Sie durch verschiedene Rollen ausgeführt werden oder wenn es Wartezeit gibt oder ein externes Ereignis vor dem nächsten Schritt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="356ae-179">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="356ae-180">Vermeiden Sie es, Werte in Listen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="356ae-180">Avoid selecting values in lists.</span></span> <span data-ttu-id="356ae-181">Verwenden Sie stattdessen Textformate, wie **FIFO**, **AudioRM** und **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="356ae-181">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="356ae-182">Wenn Sie in einer Liste auswählen, wird die Position des Werts in der Liste aufgenommen, nicht der Wert selbst.</span><span class="sxs-lookup"><span data-stu-id="356ae-182">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="356ae-183">Wenn dieser Liste Artikel hinzugefügt werden, kann sich die Position des Werts ändern.</span><span class="sxs-lookup"><span data-stu-id="356ae-183">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="356ae-184">Daher verwendet Ihre Aufzeichnung einen anderen Parameter, und der Rest des Szenarios wird möglicherweise davon beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="356ae-184">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="356ae-185">Denken Sie an ein Verhalten bei mehreren Benutzern.</span><span class="sxs-lookup"><span data-stu-id="356ae-185">Think about multi-user behavior.</span></span> <span data-ttu-id="356ae-186">Nehmen Sie beispielsweise nicht an, dass Ihr neu erstellter Auftrag automatisch immer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="356ae-186">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="356ae-187">Verwenden Sie stattdessen immer den Filter, um die korrekte Reihenfolge zu suchen.</span><span class="sxs-lookup"><span data-stu-id="356ae-187">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="356ae-188">Verwenden Sie die Kopierfunktion in der Aufgabenaufzeichnung, um den Namen eines neu erstellten Produkts zu speichern, damit sie in verketteten Testfällen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="356ae-188">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="356ae-189">Verwenden Sie die Validierungsfunktion in der Aufgabenaufzeichnung, um Prüfpunkte festzulegen, die sicherstellen, dass Schritte ordnungsgemäß ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="356ae-189">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="356ae-190">RSAT</span><span class="sxs-lookup"><span data-stu-id="356ae-190">RSAT</span></span>

- <span data-ttu-id="356ae-191">Um den Test in einem anderen Unternehmen auszuführen, können Sie das Unternehmen auf der Registerkarte **Allgemein** der Excel-Parameterdatei ändern.</span><span class="sxs-lookup"><span data-stu-id="356ae-191">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="356ae-192">Stellen Sie sicher, dass die Einstellungen und Daten im derzeit ausgewählten Unternehmen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="356ae-192">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="356ae-193">Sie können den Testbenutzer auf der Registerkarte **Allgemein** der Excel-Parameterdatei ändern.</span><span class="sxs-lookup"><span data-stu-id="356ae-193">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="356ae-194">Geben Sie die E-Mail-Kennung des Benutzers ein, der den Testfall ausführt.</span><span class="sxs-lookup"><span data-stu-id="356ae-194">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="356ae-195">Auf diese Weise kann der Testfall durchgeführt werden, indem die Sicherheitsberechtigungen des angegebenen Benutzers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="356ae-195">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="356ae-196">Um zu warten, bis der Test begonnen wird, können Sie auf der Registerkarte **Allgemein** der Excel-Parameterdatei eine Pause definieren.</span><span class="sxs-lookup"><span data-stu-id="356ae-196">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="356ae-197">Diese Pause kann in einem Batchauftrag verwendet werden (beispielsweise, wenn ein Workflow ausgeführt werden muss, bevor der nächste Schritt ausgeführt werden kann).</span><span class="sxs-lookup"><span data-stu-id="356ae-197">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="356ae-198">Erweiterte Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="356ae-198">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="356ae-199">CLI</span><span class="sxs-lookup"><span data-stu-id="356ae-199">CLI</span></span>

<span data-ttu-id="356ae-200">RSAT kann von einem Fenster **Befehlseingabeaufforderung** oder **PowerShell** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="356ae-200">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="356ae-201">Überprüfen Sie, dass die Umgebungsvariable **TestRoot** auf den RSAT-Installationspfad festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="356ae-201">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="356ae-202">(Öffnen Sie Microsoft Windows in der **Systemsteuerung**, wählen Sie **System und Sicherheit \> System \> Erweiterte Systemeinstellungen** und **Umgebungsvariablen** aus.)</span><span class="sxs-lookup"><span data-stu-id="356ae-202">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="356ae-203">Öffnen Sie als Administrator ein Fenster **Kommandozeile** oder **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="356ae-203">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="356ae-204">Navigieren Sie zum RSAT-Installationsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="356ae-204">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="356ae-205">Alle Befehle auflisten.</span><span class="sxs-lookup"><span data-stu-id="356ae-205">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a><span data-ttu-id="356ae-206">?</span><span class="sxs-lookup"><span data-stu-id="356ae-206">?</span></span>

<span data-ttu-id="356ae-207">Zeigt die Hilfe zu allen verfügbaren Befehlen und ihren Parametern an.</span><span class="sxs-lookup"><span data-stu-id="356ae-207">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a><span data-ttu-id="356ae-208">?: Optionale Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-208">?: Optional parameters</span></span>

<span data-ttu-id="356ae-209">`command`: Hierbei ist ``[command]`` einer der unten angegebenen Befehle.</span><span class="sxs-lookup"><span data-stu-id="356ae-209">`command`: Where ``[command]`` is one of the commands specified below.</span></span>

#### <a name="about"></a><span data-ttu-id="356ae-210">Info</span><span class="sxs-lookup"><span data-stu-id="356ae-210">about</span></span>

<span data-ttu-id="356ae-211">Zeigt die aktuelle Version an.</span><span class="sxs-lookup"><span data-stu-id="356ae-211">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="356ae-212">cls</span><span class="sxs-lookup"><span data-stu-id="356ae-212">cls</span></span>

<span data-ttu-id="356ae-213">Löscht den Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="356ae-213">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a><span data-ttu-id="356ae-214">herunterladen</span><span class="sxs-lookup"><span data-stu-id="356ae-214">download</span></span>

<span data-ttu-id="356ae-215">Lädt Anhänge für den angegebenen Testfall in das Ausgabeverzeichnis herunter.</span><span class="sxs-lookup"><span data-stu-id="356ae-215">Downloads attachments for the specified test case to the output directory.</span></span>
<span data-ttu-id="356ae-216">Sie können den Befehl ``list`` verwenden, um alle verfügbaren Testfälle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="356ae-216">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="356ae-217">Verwenden Sie einen beliebigen Wert aus der ersten Spalte als Parameter **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="356ae-217">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a><span data-ttu-id="356ae-218">download: erforderliche Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-218">download: required parameters</span></span>

+ <span data-ttu-id="356ae-219">`test_case_id`: Steht für die Kennung des Testfalls.</span><span class="sxs-lookup"><span data-stu-id="356ae-219">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="356ae-220">`output_dir`: Steht für das Ausgabeverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="356ae-220">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="356ae-221">Das Verzeichnis muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="356ae-221">The directory must exist.</span></span>

##### <a name="download-examples"></a><span data-ttu-id="356ae-222">download: Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-222">download: examples</span></span>

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a><span data-ttu-id="356ae-223">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="356ae-223">edit</span></span>

<span data-ttu-id="356ae-224">Erlaubt Ihnen, die Parameterdatei im Programm Excel zu öffnen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="356ae-224">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a><span data-ttu-id="356ae-225">edit: erforderliche Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-225">edit: required parameters</span></span>

+ <span data-ttu-id="356ae-226">`excel_file`: Muss einen vollständigen Pfad zu einer vorhandenen Excel-Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="356ae-226">`excel_file`: Must contain a full path to an existing Excel file.</span></span>

##### <a name="edit-examples"></a><span data-ttu-id="356ae-227">edit: Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-227">edit: examples</span></span>

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a><span data-ttu-id="356ae-228">erzeugen.</span><span class="sxs-lookup"><span data-stu-id="356ae-228">generate</span></span>

<span data-ttu-id="356ae-229">Erzeugt im Ausgabeverzeichnis Testausführungs- und Parameterdateien für den angegebenen Testfall.</span><span class="sxs-lookup"><span data-stu-id="356ae-229">Generates test execution and parameter files for the specified test case in the output directory.</span></span> <span data-ttu-id="356ae-230">Sie können den Befehl ``list`` verwenden, um alle verfügbaren Testfälle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="356ae-230">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="356ae-231">Verwenden Sie einen beliebigen Wert aus der ersten Spalte als Parameter **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="356ae-231">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a><span data-ttu-id="356ae-232">generate: erforderliche Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-232">generate: required parameters</span></span>

+ <span data-ttu-id="356ae-233">`test_case_id`: Steht für die Kennung des Testfalls.</span><span class="sxs-lookup"><span data-stu-id="356ae-233">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="356ae-234">`output_dir`: Steht für das Ausgabeverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="356ae-234">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="356ae-235">Das Verzeichnis muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="356ae-235">The directory must exist.</span></span>

##### <a name="generate-examples"></a><span data-ttu-id="356ae-236">generate: Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-236">generate: examples</span></span>

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a><span data-ttu-id="356ae-237">erzeugt</span><span class="sxs-lookup"><span data-stu-id="356ae-237">generatederived</span></span>

<span data-ttu-id="356ae-238">Erzeugt einen neuen Testfall, der aus dem bereitgestellten Testfall abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="356ae-238">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="356ae-239">Sie können den Befehl ``list`` verwenden, um alle verfügbaren Testfälle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="356ae-239">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="356ae-240">Verwenden Sie einen beliebigen Wert aus der ersten Spalte als Parameter **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="356ae-240">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a><span data-ttu-id="356ae-241">generatederived: erforderliche Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-241">generatederived: required parameters</span></span>

+ <span data-ttu-id="356ae-242">`parent_test_case_id`: Steht für die Kennung des übergeordneten Testfalls.</span><span class="sxs-lookup"><span data-stu-id="356ae-242">`parent_test_case_id`: Represents the parent test case ID.</span></span>
+ <span data-ttu-id="356ae-243">`test_plan_id`: Steht für die Kennung des Testplans.</span><span class="sxs-lookup"><span data-stu-id="356ae-243">`test_plan_id`: Represents the test plan ID.</span></span>
+ <span data-ttu-id="356ae-244">`test_suite_id` Steht für die Kennung der Testsuite.</span><span class="sxs-lookup"><span data-stu-id="356ae-244">`test_suite_id`: Represents the test suite ID.</span></span>

##### <a name="generatederived-examples"></a><span data-ttu-id="356ae-245">generatederived: Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-245">generatederived: examples</span></span>

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a><span data-ttu-id="356ae-246">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="356ae-246">generatetestonly</span></span>

<span data-ttu-id="356ae-247">Erzeugt nur die Testausführungsdatei für den angegebenen Testfall im Ausgabeverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="356ae-247">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="356ae-248">Sie können den Befehl ``list`` verwenden, um alle verfügbaren Testfälle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="356ae-248">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="356ae-249">Verwenden Sie einen beliebigen Wert aus der ersten Spalte als Parameter **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="356ae-249">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a><span data-ttu-id="356ae-250">generatetestonly: erforderliche Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-250">generatetestonly: required parameters</span></span>

+ <span data-ttu-id="356ae-251">`test_case_id`: Steht für die Kennung des Testfalls.</span><span class="sxs-lookup"><span data-stu-id="356ae-251">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="356ae-252">`output_dir`: Steht für das Ausgabeverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="356ae-252">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="356ae-253">Das Verzeichnis muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="356ae-253">The directory must exist.</span></span>

##### <a name="generatetestonly-examples"></a><span data-ttu-id="356ae-254">generatetestonly: Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-254">generatetestonly: examples</span></span>

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a><span data-ttu-id="356ae-255">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="356ae-255">generatetestsuite</span></span>

<span data-ttu-id="356ae-256">Erzeugt alle Testfälle für die angegebene Suite im Ausgabeverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="356ae-256">Generates all test cases for the specified suite in the output directory.</span></span> <span data-ttu-id="356ae-257">Sie können den Befehl ``listtestsuitenames`` verwenden, um alle verfügbaren Testanzüge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="356ae-257">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="356ae-258">Verwenden Sie einen beliebigen Wert aus der Spalte als **Test_suite_name** Parameter.</span><span class="sxs-lookup"><span data-stu-id="356ae-258">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a><span data-ttu-id="356ae-259">generatetestsuite: erforderliche Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-259">generatetestsuite: required parameters</span></span>

+ <span data-ttu-id="356ae-260">`test_suite_name` Steht für den Namen der Testsuite.</span><span class="sxs-lookup"><span data-stu-id="356ae-260">`test_suite_name`: Represents the test suite name.</span></span>
+ <span data-ttu-id="356ae-261">`output_dir`: Steht für das Ausgabeverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="356ae-261">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="356ae-262">Das Verzeichnis muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="356ae-262">The directory must exist.</span></span>

##### <a name="generatetestsuite-examples"></a><span data-ttu-id="356ae-263">generatetestsuite: Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-263">generatetestsuite: examples</span></span>

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a><span data-ttu-id="356ae-264">help</span><span class="sxs-lookup"><span data-stu-id="356ae-264">help</span></span>

<span data-ttu-id="356ae-265">Identisch mit dem [?](#section)</span><span class="sxs-lookup"><span data-stu-id="356ae-265">Identical to the [?](#section)</span></span> <span data-ttu-id="356ae-266">Befehl.</span><span class="sxs-lookup"><span data-stu-id="356ae-266">command.</span></span>

#### <a name="list"></a><span data-ttu-id="356ae-267">Liste</span><span class="sxs-lookup"><span data-stu-id="356ae-267">list</span></span>

<span data-ttu-id="356ae-268">Listet alle verfügbaren Testfälle auf.</span><span class="sxs-lookup"><span data-stu-id="356ae-268">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a><span data-ttu-id="356ae-269">listtestplans</span><span class="sxs-lookup"><span data-stu-id="356ae-269">listtestplans</span></span>

<span data-ttu-id="356ae-270">Listet alle verfügbaren Testpläne auf.</span><span class="sxs-lookup"><span data-stu-id="356ae-270">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a><span data-ttu-id="356ae-271">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="356ae-271">listtestsuite</span></span>

<span data-ttu-id="356ae-272">Listet Testfälle für die angegebene Testsuite auf.</span><span class="sxs-lookup"><span data-stu-id="356ae-272">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="356ae-273">Sie können den Befehl ``listtestsuitenames`` verwenden, um alle verfügbaren Testsuiten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="356ae-273">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="356ae-274">Verwenden Sie einen beliebigen Wert aus der ersten Spalte als **Suitename** Parameter.</span><span class="sxs-lookup"><span data-stu-id="356ae-274">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a><span data-ttu-id="356ae-275">listtestsuite: erforderliche Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-275">listtestsuite: required parameters</span></span>

+ <span data-ttu-id="356ae-276">`suite_name`: Der Name der gewünschten Testsuite.</span><span class="sxs-lookup"><span data-stu-id="356ae-276">`suite_name`: Name of the desired suite.</span></span>

##### <a name="listtestsuite-examples"></a><span data-ttu-id="356ae-277">listtestsuite: Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-277">listtestsuite: examples</span></span>

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a><span data-ttu-id="356ae-278">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="356ae-278">listtestsuitenames</span></span>

<span data-ttu-id="356ae-279">Listet alle verfügbaren Testsuiten auf.</span><span class="sxs-lookup"><span data-stu-id="356ae-279">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a><span data-ttu-id="356ae-280">playback</span><span class="sxs-lookup"><span data-stu-id="356ae-280">playback</span></span>

<span data-ttu-id="356ae-281">Spielt einen Testfall mit Hilfe einer Excel-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="356ae-281">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a><span data-ttu-id="356ae-282">playback: erforderliche Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-282">playback: required parameters</span></span>

+ <span data-ttu-id="356ae-283">`excel_file`: Ein vollständiger Pfad zur Excel-Datei.</span><span class="sxs-lookup"><span data-stu-id="356ae-283">`excel_file`: A full path to the Excel file.</span></span> <span data-ttu-id="356ae-284">Die Datei muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="356ae-284">File must exist.</span></span>

##### <a name="playback-examples"></a><span data-ttu-id="356ae-285">playback: Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-285">playback: examples</span></span>

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a><span data-ttu-id="356ae-286">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="356ae-286">playbackbyid</span></span>

<span data-ttu-id="356ae-287">Spielt mehrere Testfälle gleichzeitig ab.</span><span class="sxs-lookup"><span data-stu-id="356ae-287">Plays back multiple test cases at once.</span></span> <span data-ttu-id="356ae-288">Sie können den Befehl ``list`` verwenden, um alle verfügbaren Testfälle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="356ae-288">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="356ae-289">Verwenden Sie einen beliebigen Wert aus der ersten Spalte als Parameter **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="356ae-289">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a><span data-ttu-id="356ae-290">playbackbyid: erforderliche Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-290">playbackbyid: required parameters</span></span>

+ <span data-ttu-id="356ae-291">`test_case_id1`: Die Kennung des vorhandenen Testfalls.</span><span class="sxs-lookup"><span data-stu-id="356ae-291">`test_case_id1`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="356ae-292">`test_case_id2`: Die Kennung des vorhandenen Testfalls.</span><span class="sxs-lookup"><span data-stu-id="356ae-292">`test_case_id2`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="356ae-293">`test_case_idN`: Die Kennung des vorhandenen Testfalls.</span><span class="sxs-lookup"><span data-stu-id="356ae-293">`test_case_idN`: ID of exisiting test case.</span></span>

##### <a name="playbackbyid-examples"></a><span data-ttu-id="356ae-294">playbackbyid: Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-294">playbackbyid: examples</span></span>

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a><span data-ttu-id="356ae-295">playbackmany</span><span class="sxs-lookup"><span data-stu-id="356ae-295">playbackmany</span></span>

<span data-ttu-id="356ae-296">Spielt viele Testfälle auf einmal ab, wobei Excel-Dateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="356ae-296">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a><span data-ttu-id="356ae-297">playbackmany: erforderliche Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-297">playbackmany: required parameters</span></span>

+ <span data-ttu-id="356ae-298">`excel_file1`: Vollständiger Pfad zur Excel-Datei.</span><span class="sxs-lookup"><span data-stu-id="356ae-298">`excel_file1`: Full path to the Excel file.</span></span> <span data-ttu-id="356ae-299">Die Datei muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="356ae-299">File must exist.</span></span>
+ <span data-ttu-id="356ae-300">`excel_file2`: Vollständiger Pfad zur Excel-Datei.</span><span class="sxs-lookup"><span data-stu-id="356ae-300">`excel_file2`: Full path to the Excel file.</span></span> <span data-ttu-id="356ae-301">Die Datei muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="356ae-301">File must exist.</span></span>
+ <span data-ttu-id="356ae-302">`excel_fileN`: Vollständiger Pfad zur Excel-Datei.</span><span class="sxs-lookup"><span data-stu-id="356ae-302">`excel_fileN`: Full path to the Excel file.</span></span> <span data-ttu-id="356ae-303">Die Datei muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="356ae-303">File must exist.</span></span>

##### <a name="playbackmany-examples"></a><span data-ttu-id="356ae-304">playbackmany: Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-304">playbackmany: examples</span></span>

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a><span data-ttu-id="356ae-305">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="356ae-305">playbacksuite</span></span>

<span data-ttu-id="356ae-306">Spielt alle Testfälle aus der angegebenen Testsuite ab.</span><span class="sxs-lookup"><span data-stu-id="356ae-306">Plays back all test cases from the specified test suite.</span></span>
<span data-ttu-id="356ae-307">Sie können den Befehl ``listtestsuitenames`` verwenden, um alle verfügbaren Testsuiten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="356ae-307">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="356ae-308">Verwenden Sie einen beliebigen Wert aus der ersten Spalte als **Suitename** Parameter.</span><span class="sxs-lookup"><span data-stu-id="356ae-308">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a><span data-ttu-id="356ae-309">playbacksuite: erforderliche Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-309">playbacksuite: required parameters</span></span>

+ <span data-ttu-id="356ae-310">`suite_name`: Der Name der gewünschten Testsuite.</span><span class="sxs-lookup"><span data-stu-id="356ae-310">`suite_name`: Name of the desired suite.</span></span>

##### <a name="playbacksuite-examples"></a><span data-ttu-id="356ae-311">playbacksuite: Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-311">playbacksuite: examples</span></span>

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a><span data-ttu-id="356ae-312">quit</span><span class="sxs-lookup"><span data-stu-id="356ae-312">quit</span></span>

<span data-ttu-id="356ae-313">Schließt die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="356ae-313">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a><span data-ttu-id="356ae-314">upload</span><span class="sxs-lookup"><span data-stu-id="356ae-314">upload</span></span>

<span data-ttu-id="356ae-315">Lädt alle Dateien hoch, die zu der angegebenen Testsuite oder den angegebenen Testfällen gehören.</span><span class="sxs-lookup"><span data-stu-id="356ae-315">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a><span data-ttu-id="356ae-316">upload: erforderliche Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-316">upload: required parameters</span></span>

+ <span data-ttu-id="356ae-317">`suite_name`: Alle Dateien, die zu der angegebenen Testsuite gehören, werden hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="356ae-317">`suite_name`: All files belonging to the specified test suite will be uploaded.</span></span>
+ <span data-ttu-id="356ae-318">`testcase_id`: Alle Dateien, die zu den angegebenen Testfällen gehören, werden hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="356ae-318">`testcase_id`: All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="upload-examples"></a><span data-ttu-id="356ae-319">upload: Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-319">upload: examples</span></span>

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a><span data-ttu-id="356ae-320">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="356ae-320">uploadrecording</span></span>

<span data-ttu-id="356ae-321">Lädt nur die Aufzeichnungsdatei hoch, die zu den angegebenen Testfällen gehört.</span><span class="sxs-lookup"><span data-stu-id="356ae-321">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a><span data-ttu-id="356ae-322">uploadrecording: erforderliche Parameter</span><span class="sxs-lookup"><span data-stu-id="356ae-322">uploadrecording: required parameters</span></span>

+ <span data-ttu-id="356ae-323">`testcase_id`: Die Aufzeichnungsdatei, die zu den angegebenen Testfällen gehört, wird hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="356ae-323">`testcase_id`: Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="uploadrecording-examples"></a><span data-ttu-id="356ae-324">uploadrecording: Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-324">uploadrecording: examples</span></span>

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a><span data-ttu-id="356ae-325">Verwendung</span><span class="sxs-lookup"><span data-stu-id="356ae-325">usage</span></span>

<span data-ttu-id="356ae-326">Zeigt zwei Möglichkeiten, diese Anwendung aufzurufen: eine mit einer Standardeinstellungsdatei, eine andere mit einer Einstellungsdatei.</span><span class="sxs-lookup"><span data-stu-id="356ae-326">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a><span data-ttu-id="356ae-327">Windows PowerShell-Beispiele</span><span class="sxs-lookup"><span data-stu-id="356ae-327">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="356ae-328">Ausführen eines Testfalls in einer Schleife</span><span class="sxs-lookup"><span data-stu-id="356ae-328">Run a test case in a loop</span></span>

<span data-ttu-id="356ae-329">Sie haben ein Testskript, das einen neuen Debitor erstellt.</span><span class="sxs-lookup"><span data-stu-id="356ae-329">You have a test script that creates a new customer.</span></span> <span data-ttu-id="356ae-330">Über Skripterstellung kann dieser Testfall in einer Schleife ausgeführt werden, indem Sie die folgenden Daten zufällig generieren, bevor jede Iteration ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="356ae-330">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="356ae-331">Debitorkennung</span><span class="sxs-lookup"><span data-stu-id="356ae-331">Customer ID</span></span>
- <span data-ttu-id="356ae-332">Name des Debitors</span><span class="sxs-lookup"><span data-stu-id="356ae-332">Customer name</span></span>
- <span data-ttu-id="356ae-333">Adresse des Debitors</span><span class="sxs-lookup"><span data-stu-id="356ae-333">Customer address</span></span>

<span data-ttu-id="356ae-334">Die Debitorenkennung hat das Format *ATCUS\<number\>*, wobei \<number\> ein Wert zwischen **000000001** und **999999999** ist.</span><span class="sxs-lookup"><span data-stu-id="356ae-334">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="356ae-335">Das folgende Beispiel verwendet den Parameter **Start**, um die erste Nummer zu definieren, die verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="356ae-335">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="356ae-336">Es wird ein zweiter Parameter **nr** verwendet, um die Anzahl der Debitoren zu definieren, die erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="356ae-336">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="356ae-337">Für jede Iteration werden die Parameter in der Excel-Parameterdatei geändert, indem eine UpdateCustomer-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="356ae-337">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="356ae-338">Danach wird die RSAT-Befehlszeile in einer RunTestCase-Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="356ae-338">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="356ae-339">Öffnet Sie die Microsoft Windows integrierte Skiptumgebung (ISE) von PowerShell im Administratormodus, und fügen Sie den folgenden Code im Fenster mit dem Namen **Untitled1.ps1** ein.</span><span class="sxs-lookup"><span data-stu-id="356ae-339">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="356ae-340">Führen Sie ein Skript aus, das von den Daten in Microsoft Dynamics 365 abhängt</span><span class="sxs-lookup"><span data-stu-id="356ae-340">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="356ae-341">Das folgende Beispiel verwendet einen Aufruf des Open Data Protocol (OData), um den Status einer Bestellung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="356ae-341">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="356ae-342">Wenn der Status nicht **fakturiert** ist, können Sie beispielsweise einen RSAT-Testfall anrufen, der die Rechnung bucht.</span><span class="sxs-lookup"><span data-stu-id="356ae-342">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]