---
title: Regression Suite Automation Tool-Tutorial anweden
description: Dieses Thema zeigt, wie das Regression Suite Automation Tool (RSAT) verwendet wird. Es beschreibt die verschiedenen Funktionen und enthält Beispiele, die erweiterte Skripterstellung verwenden.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 8f3cd6a27ba0e09e48c0562aff46791228bb46b5
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703851"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="bb294-104">Das Regression Suite Automation Tool-Tutorial anweden</span><span class="sxs-lookup"><span data-stu-id="bb294-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="bb294-105">Verwenden Sie das Internet-Browsertool, um die Seite in pdf-Format herunterzuladen und zu speichern.</span><span class="sxs-lookup"><span data-stu-id="bb294-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="bb294-106">Dies Tutorial führt Sie durch mehrere der erweiterten Funktionen des Regression Suite Automation Tool (RSAT), enthält eine Demozuweisung und beschreibt Strategie und wichtige Lernpunkte.</span><span class="sxs-lookup"><span data-stu-id="bb294-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="bb294-107">Funktionen von RSAT/Aufgabenaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="bb294-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="bb294-108">Einen Feldwert überprüfen</span><span class="sxs-lookup"><span data-stu-id="bb294-108">Validate a field value</span></span>

<span data-ttu-id="bb294-109">Informationen zu dieser Funktion finden Sie unter [Erstellen einer neuen Aufgabenaufzeichnung mit einer Validierungsfunktion](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function) Sie unter.</span><span class="sxs-lookup"><span data-stu-id="bb294-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="bb294-110">Variable gespeichert</span><span class="sxs-lookup"><span data-stu-id="bb294-110">Saved variable</span></span>

<span data-ttu-id="bb294-111">Informationen zu dieser Funktion finden Sie unter [Ändern einer vorhandenen Aufgabenaufzeichnung, um eine gespeicherte Variable zu erstellen](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="bb294-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="bb294-112">Abgeleitete Testfälle</span><span class="sxs-lookup"><span data-stu-id="bb294-112">Derived test case</span></span>

1. <span data-ttu-id="bb294-113">Öffnen Sie das Regression Suite Automation Tool (RSAT) und wählen Sie beide Testfälle aus, die Sie in [Einrichten und Installieren des Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md) ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="bb294-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="bb294-114">Wählen Sie **Neu \>Abgeleiteten Testfall berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="bb294-114">Select **New \> Create derived test case**.</span></span>

    ![Abgeleiteten Testfallbefehl im Menü „Neu“ erstellen](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="bb294-116">Sie erhalten eine Meldung, die angibt, dass ein abgeleiteter Testfall für jeden ausgewählten Testfall in der aktuellen Testsuite erstellt wird und dass jeder abgeleitete Testfall eine eigene Kopie der Excel-Parameterdatei hat.</span><span class="sxs-lookup"><span data-stu-id="bb294-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="bb294-117">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb294-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb294-118">Wenn Sie einen abgeleiteten Testfall ausführen, verwendet er die Aufgabenaufzeichnung des übergeordneten Testfalls und die eigene Kopie der Excel-Parameterdatei.</span><span class="sxs-lookup"><span data-stu-id="bb294-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="bb294-119">Auf diese Weise können Sie den gleichen Test mit unterschiedlichen Parametern erstellen, ohne mehr als eine Aufgabenaufzeichnung verwalten zu müssen.</span><span class="sxs-lookup"><span data-stu-id="bb294-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="bb294-120">Ein abgeleiteter Testfall muss kein Teil der gleichen Testsuite wie der übergeordneter Testfall sein.</span><span class="sxs-lookup"><span data-stu-id="bb294-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Meldungsfeld](./media/use_rsa_tool_02.png)

    <span data-ttu-id="bb294-122">Zwei zusätzliche abgeleitete Testfälle werden erstellt, und das Kontrollkästchen **Abgeleitet?** für sie wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bb294-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Abgeleitete Testfälle erstellt](./media/use_rsa_tool_03.png)

    <span data-ttu-id="bb294-124">Ein abgeleiteter Testfall wird automatisch in Azure DevOps erstellt.</span><span class="sxs-lookup"><span data-stu-id="bb294-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="bb294-125">Es ist ein untergeordnetes Element des Testfalls **Neues Produkt erstellen** und es ist mit einem speziellen Schlüsselwort markiert: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="bb294-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="bb294-126">Diese Testfälle werden ebenfalls automatisch dem Testplan in Azure DevOps hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bb294-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![RSAT:DerivedTestSteps-Schlüsselwort](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="bb294-128">Wenn die abgeleiteten Testfälle, die erstellt werden, aus irgendeinem Grund nicht in der richtigen Reihenfolge vorliegen, wechseln Sie zu Azure DevOps und ordnen Sie die Testfälle in der Testsuite neu an, damit RSAT sie in der richtigen Reihenfolge ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="bb294-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="bb294-129">Wählen Sie die abgeleiteten Testfälle aus, und wählen Sie dann **Bearbeiten** aus, um die entsprechenden Excel-Parameterdateien zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bb294-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="bb294-130">Bearbeiten Sie diese Excel-Parameterdateien auf die gleiche Weise, wie Sie die übergeordneten Dateien bearbeitet haben.</span><span class="sxs-lookup"><span data-stu-id="bb294-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="bb294-131">Stellen Sie also sicher, dass die Produktkennung so festgelegt ist, dass sie automatisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="bb294-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="bb294-132">Stellen Sie außerdem sicher, dass die gespeicherte Variable in die relevanten Felder kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="bb294-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="bb294-133">Aktualisieren Sie auf der Registerkarte **Allgemein** beider Excel-Parameterdateien den Wert des Felds **Unternehmen** auf **USSI**, sodass die abgeleiteten Testfälle für eine andere juristische Person als der übergeordnete Testfall ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bb294-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="bb294-134">Um die Testfälle für einen bestimmten Benutzer (oder die Rolle, die einem bestimmten Benutzer zugeordnet ist) auszuführen, können Sie den Wert des Felds **Testbenutzer** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bb294-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="bb294-135">Wählen Sie **Ausführen** aus, und überprüfen Sie, dass das Produkt in der juristischen USMF-Person und in der juristischen USSI-Person erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bb294-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="bb294-136">Benachrichtigungen validieren</span><span class="sxs-lookup"><span data-stu-id="bb294-136">Validate notifications</span></span>

<span data-ttu-id="bb294-137">Diese Funktion kann verwendet werden, um zu überprüfen, ob eine Aktivität stattfand.</span><span class="sxs-lookup"><span data-stu-id="bb294-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="bb294-138">Wenn ein Produktionsauftrag beispielsweise erstellt, vorkalkuliert und dann gestartet wird, zeigt Microsoft Dynamics 365 for Finance and Operations eine „Produktion – Start“-Nachricht, die Sie darüber zu informieren, dass der Produktionsauftrag gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="bb294-138">For example, when a production order is created, estimated, and then started, Microsoft Dynamics 365 for Finance and Operations shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Produktion – Start-Benachrichtigung](./media/use_rsa_tool_05.png)

<span data-ttu-id="bb294-140">Sie können diese Meldung über RSAT überprüfen, indem Sie den Nachrichtentext auf der Registerkarte **MessageValidation** der Excel-Parameterdatei für die entsprechende Erfassung eingeben.</span><span class="sxs-lookup"><span data-stu-id="bb294-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Registerkarte Nachrichtenvalidierung](./media/use_rsa_tool_06.png)

<span data-ttu-id="bb294-142">Nachdem der Testfall ausgeführt wurde, wird die Nachricht in der Excel-Parameterdatei mit der Nachricht verglichen, die in Finance and Operations angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bb294-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown in Finance and Operations.</span></span> <span data-ttu-id="bb294-143">Wenn die Nachrichten nicht übereinstimmen, schlägt der Testfall fehl.</span><span class="sxs-lookup"><span data-stu-id="bb294-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="bb294-144">Sie können mehrere Nachrichten auf der Registerkarte **MessageValidation** in der Excel-Parameterdatei eingeben.</span><span class="sxs-lookup"><span data-stu-id="bb294-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="bb294-145">Die Nachrichten können auch Fehler- oder Warnmeldungen anstelle der Informationsmeldungen sein.</span><span class="sxs-lookup"><span data-stu-id="bb294-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="bb294-146">Überprüfen der Werte mithilfe von Operatoren</span><span class="sxs-lookup"><span data-stu-id="bb294-146">Validate values by using operators</span></span>

<span data-ttu-id="bb294-147">In früheren Versionen von RSAT, konnten Sie Werte nur überprüfen, wenn ein Kontrollwert einem erwarteten Wert entsprach.</span><span class="sxs-lookup"><span data-stu-id="bb294-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="bb294-148">Mit der neuen Funktion können Sie prüfen, dass eine Variable ungleich, kleiner oder größer als ein angegebener Wert ist.</span><span class="sxs-lookup"><span data-stu-id="bb294-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="bb294-149">Um diese Funktion zu verwenden, öffnen Sie die Datei **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** im RSAT-Installationsordner (beispielsweise **C:\\Programme (x86)\\Regression Suite Automation Tool**), und ändern Sie den Wert im folgenden Element von **false** auf **true**.</span><span class="sxs-lookup"><span data-stu-id="bb294-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="bb294-150">In der Excel-Parameterdatei wird das neue Feld **Operator** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb294-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb294-151">Wenn Sie eine ältere Version von RSAT verwendet haben, müssen Sie neue Excel-Parameterdateien generieren.</span><span class="sxs-lookup"><span data-stu-id="bb294-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Feld „Operator“](./media/use_rsa_tool_07.png)

<span data-ttu-id="bb294-153">Das folgende Beispiel veranschaulicht, wie Sie diese Funktion verwenden können, um zu prüfen, ob der Lagerbestand mehr als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="bb294-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="bb294-154">In den Demodaten im **USMF**-Unternehmen erstellen Sie eine Aufgabenaufzeichnung, die die folgenden Schritte ausführt:</span><span class="sxs-lookup"><span data-stu-id="bb294-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="bb294-155">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \>Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="bb294-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="bb294-156">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bb294-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bb294-157">Filtern Sie beispielsweise auf einen Wert von **1000** für das Feld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="bb294-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="bb294-158">Wählen Sie **Verfügbarer Lagerbestand** aus</span><span class="sxs-lookup"><span data-stu-id="bb294-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="bb294-159">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bb294-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bb294-160">Filtern Sie beispielsweise auf einen Wert von **1** für das Feld **Website**.</span><span class="sxs-lookup"><span data-stu-id="bb294-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="bb294-161">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="bb294-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="bb294-162">Überprüfen Sie, dass der Wert des Feldes **Verfügbare Summe** **411,0000000000000000** ist.</span><span class="sxs-lookup"><span data-stu-id="bb294-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="bb294-163">Speichern Sie die Aufgabenaufzeichnung in der die BPM-Bibliothek in LCS und synchronisieren Sie sie mit Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="bb294-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="bb294-164">Fügen Sie den Testfall dem Testplan hinzu, und laden Sie den Testfall in RSAT.</span><span class="sxs-lookup"><span data-stu-id="bb294-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="bb294-165">Öffnen Sie die Excel-Parameterdatei.</span><span class="sxs-lookup"><span data-stu-id="bb294-165">Open the Excel parameter file.</span></span> <span data-ttu-id="bb294-166">Auf der Registerkarte **InventOnhandItem** wird ein Abschnitt **InventOnhandItem validieren** angezeigt, die ein **Operator**-Feld enthält.</span><span class="sxs-lookup"><span data-stu-id="bb294-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Feld „Operator“](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="bb294-168">Um zu Prüfen, ob der verfügbare Bestand immer größer als 0 ist, ändern Sie den Wert des Feldes **Wert** von **411** auf **0** und den Wert des Felds **Operator** von einem Gleichheitszeichen (**=**) zu einem Größer-als-Zeichen (**\>**).</span><span class="sxs-lookup"><span data-stu-id="bb294-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Geänderte Werte der Felder „Wert“ und „Operator“](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="bb294-170">Speichern und schließen Sie die Excel-Parameterdatei.</span><span class="sxs-lookup"><span data-stu-id="bb294-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="bb294-171">Wählen Sie **Hochladen** aus, um die Änderungen zu speichern, die Sie an der Excel-Parameterdatei vorgenommen haben Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="bb294-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="bb294-172">Wenn der Wert des Feldes **Verfügbare Summe** jetzt für den angegebenen Artikel im Bestand größer als 0 (null) ist, sind Tests unabhängig vom tatsächlichen Wert des verfügbaren Bestands erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="bb294-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="bb294-173">Generatorprotokolle</span><span class="sxs-lookup"><span data-stu-id="bb294-173">Generator logs</span></span>

<span data-ttu-id="bb294-174">Diese Funktion erstellt einen Ordner, der die Protokolle der durchgeführten Testfälle enthält.</span><span class="sxs-lookup"><span data-stu-id="bb294-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="bb294-175">Um diese Funktion zu verwenden, öffnen Sie die Datei **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** im RSAT-Installationsordner (beispielsweise **C:\\Programme (x86)\\Regression Suite Automation Tool**), und ändern Sie den Wert im folgenden Element von **false** auf **true**.</span><span class="sxs-lookup"><span data-stu-id="bb294-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="bb294-176">Nachdem die Testfälle ausgeführt werden, finden Sie die Protokolldateien unter **C:\\Benutzer\\\<Benutzername\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="bb294-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![GeneratorLogs-Ordner](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="bb294-178">Wenn Testfälle vorhanden waren, bevor Sie den Wert in der CONFIG-Datei geändert haben, werden keine Protokolle für diese Testfälle generiert, bis Sie neue Testausführungsdateien generieren.</span><span class="sxs-lookup"><span data-stu-id="bb294-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Befehl „Nur Textbewertungsfelder generieren“ im Menü „Neu“](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="bb294-180">Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="bb294-180">Snapshot</span></span>

<span data-ttu-id="bb294-181">Diese Funktion nimmt Screenshots der Schritte auf, die während der Aufgabenaufzeichnung ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="bb294-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="bb294-182">Um diese Funktion zu verwenden, öffnen Sie die Datei **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** im RSAT-Installationsordner (beispielsweise **C:\\Programme (x86)\\Regression Suite Automation Tool**), und ändern Sie den Wert des folgenden Elements von **false** auf **true**.</span><span class="sxs-lookup"><span data-stu-id="bb294-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="bb294-183">Unter **C:\\Benutzer\\\<Benutzername\>\\AppData\\Roaming\\regressionTool\\Playback** wird ein separater Ordner für jeden Testfall erstellt, der ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb294-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Momentaufnahme-Ordner für einen Testfall](./media/use_rsa_tool_12.png)

<span data-ttu-id="bb294-185">In jedem dieser Ordner können Sie Momentaufnahmen der Schritte finden, die ausgeführt wurden, als die Testfälle ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="bb294-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Momentaufnahmedateien](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="bb294-187">Zuweisung</span><span class="sxs-lookup"><span data-stu-id="bb294-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="bb294-188">Szenario</span><span class="sxs-lookup"><span data-stu-id="bb294-188">Scenario</span></span>

1. <span data-ttu-id="bb294-189">Der Produktdesigner erstellt ein neues veröffentlichtes Produkt.</span><span class="sxs-lookup"><span data-stu-id="bb294-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="bb294-190">Der Produktions-Manager initiiert einen Produktionsauftrag, um den Lagerbestand auf zwei Stück aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="bb294-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="bb294-191">Die Fertigung startet und beendet den Produktionsauftrag und überprüft, ob die verfügbare Menge zwei Stück beträgt.</span><span class="sxs-lookup"><span data-stu-id="bb294-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="bb294-192">Das Vertriebsteam erhält einen Auftrag für vier Stück des neuen Produkts.</span><span class="sxs-lookup"><span data-stu-id="bb294-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="bb294-193">Daher aktualisiert das Vertriebsteam den Nettobedarf anhand des dynamischen Plans.</span><span class="sxs-lookup"><span data-stu-id="bb294-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="bb294-194">Da keine Mehrkapazität verfügbar ist, wird die Standardauftragsrichtlinie aus „kaufen statt herstellen“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bb294-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="bb294-195">Daher wird eine geplante Einkaufsbestellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="bb294-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="bb294-196">Der Käufer fügt einen Lieferanten hinzu, wandelt die geplante Einkaufsbestellung um und bestätigt die Bestellung anschließend.</span><span class="sxs-lookup"><span data-stu-id="bb294-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="bb294-197">Nachdem die gekauften Waren in Laden eingehen, sucht der Ladeninhaber die zugehörige Bestellung erhält die Waren.</span><span class="sxs-lookup"><span data-stu-id="bb294-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="bb294-198">Da die Bestellung nun abgeschlossen ist, können Waren für den Auftrag entnommen und verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="bb294-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="bb294-199">Finance bucht die Einkaufsrechnung und die Verkaufsrechnung.</span><span class="sxs-lookup"><span data-stu-id="bb294-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="bb294-200">Die folgende Abbildung zeigt den Ablauf für dieses Szenario.</span><span class="sxs-lookup"><span data-stu-id="bb294-200">The following illustration shows the flow for this scenario.</span></span>

![Ablauf für das Demoszenario](./media/use_rsa_tool_14.png)

<span data-ttu-id="bb294-202">Die folgende Abbildung zeigt den Geschäftsprozess für dieses Szenario in RSAT.</span><span class="sxs-lookup"><span data-stu-id="bb294-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Geschäftsprozesse für das Demoszenario](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="bb294-204">Strategie – Wichtige Lernpunkte</span><span class="sxs-lookup"><span data-stu-id="bb294-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="bb294-205">Daten</span><span class="sxs-lookup"><span data-stu-id="bb294-205">Data</span></span>

- <span data-ttu-id="bb294-206">Stellen Sie sicher, dass Sie repräsentative Datenmengen haben (eine Kopie der Produktion bzw. der goldenen Konfigurationsdaten und migrierte Daten).</span><span class="sxs-lookup"><span data-stu-id="bb294-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="bb294-207">Wenn Sie neue Daten über die Aufgabenaufzeichnung generieren, erstellen Sie Testnamen, die nicht mit vorhandenen Namen kollidieren, (verwenden Sie beispielsweise das Präfix **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="bb294-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="bb294-208">Verwenden Sie Point-In-Time-Wiederherstellung von Azure, um Tests in der nicht-Ebene-1-Umgebung zu wiederholen.</span><span class="sxs-lookup"><span data-stu-id="bb294-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="bb294-209">Zwar können Sie die Excel-Funktionen **ZUFÄLLIG** und **JETZT** verwenden, um eine eindeutige Kombination zu generieren, der Aufwand ist ausgesprochen hoch.</span><span class="sxs-lookup"><span data-stu-id="bb294-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="bb294-210">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="bb294-210">Here is an example.</span></span>

    ```
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="bb294-211">Aufgabenaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="bb294-211">Task recorder</span></span>

- <span data-ttu-id="bb294-212">Definieren Sie Szenarien, bevor Sie mit der Aufzeichnung beginnen.</span><span class="sxs-lookup"><span data-stu-id="bb294-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="bb294-213">Ein in gut verwaltetes Projekt hat vordefinierte Testszenarien.</span><span class="sxs-lookup"><span data-stu-id="bb294-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="bb294-214">Um einen Testfall zu erstellen, berücksichtigen Sie, wie vorhersagbar das Ergebnis dieser Testszenarien ist.</span><span class="sxs-lookup"><span data-stu-id="bb294-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="bb294-215">Teilen Sie Aufzeichnungen, wenn Sie durch verschiedene Rollen ausgeführt werden oder wenn es Wartezeit gibt oder ein externes Ereignis vor dem nächsten Schritt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb294-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="bb294-216">Vermeiden Sie es, Werte in Listen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="bb294-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="bb294-217">Verwenden Sie stattdessen Textformate, wie **FIFO**, **AudioRM** und **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="bb294-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="bb294-218">Wenn Sie in einer Liste auswählen, wird die Position des Werts in der Liste aufgenommen, nicht der Wert selbst.</span><span class="sxs-lookup"><span data-stu-id="bb294-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="bb294-219">Wenn dieser Liste Artikel hinzugefügt werden, kann sich die Position des Werts ändern.</span><span class="sxs-lookup"><span data-stu-id="bb294-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="bb294-220">Daher verwendet Ihre Aufzeichnung einen anderen Parameter, und der Rest des Szenarios wird möglicherweise davon beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="bb294-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="bb294-221">Denken Sie an ein Verhalten bei mehreren Benutzern.</span><span class="sxs-lookup"><span data-stu-id="bb294-221">Think about multi-user behavior.</span></span> <span data-ttu-id="bb294-222">Nehmen Sie beispielsweise nicht an, dass Ihr neu erstellter Auftrag automatisch immer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bb294-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="bb294-223">Verwenden Sie stattdessen immer den Filter, um die korrekte Reihenfolge zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bb294-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="bb294-224">Verwenden Sie die Kopierfunktion in der Aufgabenaufzeichnung, um den Namen eines neu erstellten Produkts zu speichern, damit sie in verketteten Testfällen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bb294-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="bb294-225">Verwenden Sie die Validierungsfunktion in der Aufgabenaufzeichnung, um Prüfpunkte festzulegen, die sicherstellen, dass Schritte ordnungsgemäß ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="bb294-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="bb294-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="bb294-226">RSAT</span></span>

- <span data-ttu-id="bb294-227">Um den Test in einem anderen Unternehmen auszuführen, können Sie das Unternehmen auf der Registerkarte **Allgemein** der Excel-Parameterdatei ändern.</span><span class="sxs-lookup"><span data-stu-id="bb294-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="bb294-228">Stellen Sie sicher, dass die Einstellungen und Daten im derzeit ausgewählten Unternehmen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="bb294-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="bb294-229">Sie können den Testbenutzer auf der Registerkarte **Allgemein** der Excel-Parameterdatei ändern.</span><span class="sxs-lookup"><span data-stu-id="bb294-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="bb294-230">Geben Sie die E-Mail-Kennung des Benutzers ein, der den Testfall ausführt.</span><span class="sxs-lookup"><span data-stu-id="bb294-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="bb294-231">Auf diese Weise kann der Testfall durchgeführt werden, indem die Sicherheitsberechtigungen des angegebenen Benutzers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb294-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="bb294-232">Um zu warten, bis der Test begonnen wird, können Sie auf der Registerkarte **Allgemein** der Excel-Parameterdatei eine Pause definieren.</span><span class="sxs-lookup"><span data-stu-id="bb294-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="bb294-233">Diese Pause kann in einem Batchauftrag verwendet werden (beispielsweise, wenn ein Workflow ausgeführt werden muss, bevor der nächste Schritt ausgeführt werden kann).</span><span class="sxs-lookup"><span data-stu-id="bb294-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="bb294-234">Erweiterte Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="bb294-234">Advanced scripting</span></span>

### <a name="command-line"></a><span data-ttu-id="bb294-235">Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="bb294-235">Command line</span></span>

<span data-ttu-id="bb294-236">RSAT kann von einem Fenster **Eingabeaufforderung** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bb294-236">RSAT can be called from a **Command Prompt** window.</span></span>

> [!NOTE]
> <span data-ttu-id="bb294-237">Überprüfen Sie, dass die Umgebungsvariable **TestRoot** auf den RSAT-Installationspfad festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bb294-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="bb294-238">(Öffnen Sie Microsoft Windows in der **Systemsteuerung**, wählen Sie **System und Sicherheit \> System \> Erweiterte Systemeinstellungen** und **Umgebungsvariablen** aus.)</span><span class="sxs-lookup"><span data-stu-id="bb294-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="bb294-239">Öffnen Sie ein Fenster **Eingabeaufforderung** als Administrator.</span><span class="sxs-lookup"><span data-stu-id="bb294-239">Open a **Command Prompt** window as an admin.</span></span>
2. <span data-ttu-id="bb294-240">Führen Sie das Tool im Installationsverzeichnis aus.</span><span class="sxs-lookup"><span data-stu-id="bb294-240">Run the tool from the installation directory.</span></span>

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="bb294-241">Alle Befehle auflisten.</span><span class="sxs-lookup"><span data-stu-id="bb294-241">List all commands.</span></span>

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a><span data-ttu-id="bb294-242">Windows PowerShell-Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb294-242">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="bb294-243">Ausführen eines Testfalls in einer Schleife</span><span class="sxs-lookup"><span data-stu-id="bb294-243">Run a test case in a loop</span></span>

<span data-ttu-id="bb294-244">Sie haben ein Testskript, das einen neuen Debitor erstellt.</span><span class="sxs-lookup"><span data-stu-id="bb294-244">You have a test script that creates a new customer.</span></span> <span data-ttu-id="bb294-245">Über Skripterstellung kann dieser Testfall in einer Schleife ausgeführt werden, indem Sie die folgenden Daten zufällig generieren, bevor jede Iteration ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="bb294-245">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="bb294-246">Debitorkennung</span><span class="sxs-lookup"><span data-stu-id="bb294-246">Customer ID</span></span>
- <span data-ttu-id="bb294-247">Name des Debitors</span><span class="sxs-lookup"><span data-stu-id="bb294-247">Customer name</span></span>
- <span data-ttu-id="bb294-248">Adresse des Debitors</span><span class="sxs-lookup"><span data-stu-id="bb294-248">Customer address</span></span>

<span data-ttu-id="bb294-249">Die Debitorenkennung hat das Format *ATCUS \<Nummer\>*, wobei \<Nummer\> ein Wert zwischen **000000001** und **999999999** ist.</span><span class="sxs-lookup"><span data-stu-id="bb294-249">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="bb294-250">Das folgende Beispiel verwendet den Parameter **Start**, um die erste Nummer zu definieren, die verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb294-250">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="bb294-251">Es wird ein zweiter Parameter **nr** verwendet, um die Anzahl der Debitoren zu definieren, die erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="bb294-251">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="bb294-252">Für jede Iteration werden die Parameter in der Excel-Parameterdatei geändert, indem eine UpdateCustomer-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb294-252">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="bb294-253">Danach wird die RSAT-Befehlszeile in einer RunTestCase-Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bb294-253">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="bb294-254">Öffnet Sie die Microsoft Windows integrierte Skiptumgebung (ISE) von PowerShell im Administratormodus, und fügen Sie den folgenden Code im Fenster mit dem Namen **Untitled1.ps1** ein.</span><span class="sxs-lookup"><span data-stu-id="bb294-254">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```
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
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="bb294-255">Führen Sie ein Skript aus, das von den Daten in Microsoft Dynamics 365 abhängt</span><span class="sxs-lookup"><span data-stu-id="bb294-255">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="bb294-256">Das folgende Beispiel verwendet einen Aufruf des Open Data Protocol (OData), um den Status einer Bestellung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bb294-256">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="bb294-257">Wenn der Status nicht **fakturiert** ist, können Sie beispielsweise einen RSAT-Testfall anrufen, der die Rechnung bucht.</span><span class="sxs-lookup"><span data-stu-id="bb294-257">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```
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
