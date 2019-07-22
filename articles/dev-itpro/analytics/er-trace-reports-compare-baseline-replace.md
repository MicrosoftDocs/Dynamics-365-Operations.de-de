---
title: Verbesserungen bei der Nachverfolgung erstellter ER-Berichtsergebnisse und Vergleich mit Ausgangswerten
description: Dieses Thema enthält Informationen dazu, wie die ER-Grundlagenfunktion in Microsoft Dynamics 365 for Finance and Operations Version 10.0.3 verbessert wurde (Juni 2019).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 222a415f686c8028fc2a414f97eed0291d850ae7
ms.sourcegitcommit: 9917df8c0c9320955c61186cd922c8df894a4f25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2019
ms.locfileid: "1700681"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="20fd8-103">Verbesserungen bei der Nachverfolgung erstellter ER-Berichtsergebnisse und Vergleich mit Ausgangswerten</span><span class="sxs-lookup"><span data-stu-id="20fd8-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="20fd8-104">In diesem Thema wird der erste Satz an Verbesserungen beschrieben, die an der Grundlagenfunktion des Frameworks der elektronischen Berichterstattung (ER) erfolgt sind.</span><span class="sxs-lookup"><span data-stu-id="20fd8-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="20fd8-105">Diese Verbesserungen sind in Microsoft Dynamics 365 for Finance and Operations Version 10.0.3 (Juni 2019) und später verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20fd8-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="20fd8-106">Automatisieren Sie die Struktur der Grundlagenregeln</span><span class="sxs-lookup"><span data-stu-id="20fd8-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="20fd8-107">Im Thema [Von Trace generierte Berichtergebnisse und deren Vergleich mit Grundwerten](er-trace-reports-compare-baseline.md) wird erläutert, wie das ER-Framework konfiguriert werden muss, um Informationen zu ER-Formatausführungen gesammelt und die Ergebnisse dieser Durchläufe bewertet werden.</span><span class="sxs-lookup"><span data-stu-id="20fd8-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="20fd8-108">Das Beispiel in diesem Thema zeigt die Schritte an, die abgeschlossen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="20fd8-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="20fd8-109">Beispiele für solche Schritte:</span><span class="sxs-lookup"><span data-stu-id="20fd8-109">Here are some of the steps:</span></span>

- <span data-ttu-id="20fd8-110">Führen Sie ein ER-Format aus, um eine ausgehende Datei zu generieren, und speichern Sie die Datei lokal.</span><span class="sxs-lookup"><span data-stu-id="20fd8-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="20fd8-111">Fügen Sie die lokal gespeicherten Datei als Anhang dem Grundwert hinzu, der für ein ER-Format hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="20fd8-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="20fd8-112">Konfigurieren Sie die Grundwertregel für die hinzugefügte Grundregel.</span><span class="sxs-lookup"><span data-stu-id="20fd8-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="20fd8-113">Diese Konfiguration umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="20fd8-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="20fd8-114">Geben Sie ein ER-Formatelement an, das verwendet wird, um eine ausgehende Datei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="20fd8-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="20fd8-115">Wählen Sie die Anlage aus, die auf die generierte ausgehende Datei verweist.</span><span class="sxs-lookup"><span data-stu-id="20fd8-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="20fd8-116">Diese Schritte müssen manuell ausgeführt werden, auch wenn sie durch die neuen ER-Funktionen automatisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="20fd8-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="20fd8-117">Weitere Informationen über diese Funktion erhalten Sie, wenn Sie das folgende Beispiel abschließen.</span><span class="sxs-lookup"><span data-stu-id="20fd8-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="20fd8-118">Beispiel: Automatisieren Sie die Struktur der Grundlagenregeln</span><span class="sxs-lookup"><span data-stu-id="20fd8-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="20fd8-119">Um die Schritte dieses Beispiels abzuschließen, müssen Sie zunächst die Schritte im Beispiel im Thema [Nachverfolgung erstellter Berichtsergebnisse und Vergleich mit Ausgangswerten](er-trace-reports-compare-baseline.md) bis durch den Abschnitt „Fügen Sie eine neue Grundlage für ein entworfenes ER-Format hinzu“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="20fd8-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="20fd8-120">Prüfung des hinzugefügten Grundwerts</span><span class="sxs-lookup"><span data-stu-id="20fd8-120">Review added baseline</span></span>

1. <span data-ttu-id="20fd8-121">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="20fd8-122">Wählen Sie **Grundwerte** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="20fd8-123">Die Schaltfläche **Grundwerte** im Aktivitätsbereich ist nur verfügbar, wenn der ER-Benutzerparameter **Ausführung im Debugmodus** für das aktuelle Unternehmen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="20fd8-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="20fd8-124">Der Grundwert wurde für das ausgewählte Format **Format zum erlernen der ER-Grundwerte** hinzugefügt, aber die Grundwertregeln für diesen Grundwert wurden noch nicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="20fd8-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="20fd8-125">![Seite für die Formatgrundlage für elektronische Berichterstellung](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot der Formatgrundlagen für elektronische Berichterstellung")</span><span class="sxs-lookup"><span data-stu-id="20fd8-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="20fd8-126">Erstellen eines neuen Grundwertregel</span><span class="sxs-lookup"><span data-stu-id="20fd8-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="20fd8-127">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="20fd8-128">Erweitern Sie in der Struktur **Modell zum erlernen der ER-Grundwerte**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="20fd8-129">Wählen Sie in der Struktur das Format **Modell zum erlernen der ER-Grundwerte\\Format zum Erlernen des ER-Grundwerts** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="20fd8-130">Wählen Sie im Inforegister **Versionen** **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="20fd8-131">Geben Sie im Feld **Eingabe-Id** den Wert **1** ein.</span><span class="sxs-lookup"><span data-stu-id="20fd8-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="20fd8-132">Legen Sie die Option **Erstellen von Grundwertdateien** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="20fd8-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="20fd8-133">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-133">Select **OK**.</span></span>

    <span data-ttu-id="20fd8-134">![Dialogfeld für elektronische Berichtsparameter](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Screenshot des Dialogfelds für elektronische Berichtsparameter")</span><span class="sxs-lookup"><span data-stu-id="20fd8-134">![Electronic report parameters dialog box](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Screenshot of the Electronic report parameters dialog box")</span></span>

8. <span data-ttu-id="20fd8-135">Wählen Sie **Grundwerte** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-135">Select **Baselines**.</span></span>

    <span data-ttu-id="20fd8-136">![Seite für die Formatgrundlage für elektronische Berichterstellung](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot der Formatgrundlagen für elektronische Berichterstellung")</span><span class="sxs-lookup"><span data-stu-id="20fd8-136">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="20fd8-137">Die generierte ausgehende Datei wird dem Grundwert des ausgeführten ER-Formats automatisch angefügt.</span><span class="sxs-lookup"><span data-stu-id="20fd8-137">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="20fd8-138">Die Grundwertregel wurde diesem Grundwert automatisch hinzugefügt und enthält auch die Referenz zur zugeordneten Datei.</span><span class="sxs-lookup"><span data-stu-id="20fd8-138">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="20fd8-139">Geben Sie im Feld **Name** **Grundlage 1** ein.</span><span class="sxs-lookup"><span data-stu-id="20fd8-139">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="20fd8-140">Geben Sie im Feld **Dateinamenmaske** **.xml** ein.</span><span class="sxs-lookup"><span data-stu-id="20fd8-140">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="20fd8-141">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-141">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="20fd8-142">Das Format ausführen</span><span class="sxs-lookup"><span data-stu-id="20fd8-142">Run the format</span></span>

<span data-ttu-id="20fd8-143">Sie können nun die verbleibenden Schritte im Beispiel im Thema [Nachverfolgung erstellter Berichtsergebnisse und Vergleich mit Ausgangswerten](er-trace-reports-compare-baseline.md) abschließen. Sie können mit „Führen Sie das entworfene ER-Format aus und prüfen Sie das Protokoll, um die Ergebnisse zu analysieren“ beginnen.</span><span class="sxs-lookup"><span data-stu-id="20fd8-143">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="20fd8-144">Wenn Sie den automatisch auf dem Inforegister**Ausgangswerte** hinzugefügte Ausgangswert löschen, wird die referenzierte Zuordnung nicht automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="20fd8-144">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="20fd8-145">Konfigurieren Sie den Ausgangswert, sodass er sich konstant ändernde Teile der ER-Ausgabe ignoriert.</span><span class="sxs-lookup"><span data-stu-id="20fd8-145">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="20fd8-146">Wenn ein ER-Format konzipiert wurde, um Informationen zu enthalten, die geändert werden, wenn das Format ausgeführt wird, muss das Format obligatorisch die ER-Ausgangswertfunktion verwenden, um die generierten Ergebnisse mit Ausgangswerten zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="20fd8-146">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="20fd8-147">Bei den Informationen kann es sich beispielsweise um das Verarbeitungsdatum und die entsprechende Uhrzeit oder den eindeutigen Bezeichner eines generierten Dokuments in verschiedenen Formaten (globaler eindeutiger Bezeichner \[GUID\], usw.) handeln.</span><span class="sxs-lookup"><span data-stu-id="20fd8-147">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="20fd8-148">Mit den neuen ER-Funktionen können Sie die Ausgangswertregel konfigurieren, sodass sie veränderbare Elemente eines ER-Formats ignoriert, wenn das Format ausgeführt wird. Dies dient dem Zweck eines Vergleichs von Ausgangswerten mit den Ergebnissen der Formatausführung.</span><span class="sxs-lookup"><span data-stu-id="20fd8-148">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="20fd8-149">Weitere Informationen über diese Funktion erhalten Sie, wenn Sie das folgende Beispiel abschließen.</span><span class="sxs-lookup"><span data-stu-id="20fd8-149">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="20fd8-150">Beispiel: Konfigurieren Sie den Ausgangswert, sodass er sich konstant ändernde Teile der ER-Ausgabe ignoriert.</span><span class="sxs-lookup"><span data-stu-id="20fd8-150">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="20fd8-151">Um die Schritte dieses Beispiels abzuschließen, müssen Sie zunächst die Schritte im Beispiel im Thema [Nachverfolgung erstellter Berichtsergebnisse und Vergleich mit Ausgangswerten](er-trace-reports-compare-baseline.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="20fd8-151">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="20fd8-152">Ändern eines konfigurierten ER-Formats</span><span class="sxs-lookup"><span data-stu-id="20fd8-152">Modify a configured ER format</span></span>

1. <span data-ttu-id="20fd8-153">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-153">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="20fd8-154">Erweitern Sie in der Struktur **Modell zum erlernen der ER-Grundwerte**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-154">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="20fd8-155">Wählen Sie in der Struktur das Format **Modell zum erlernen der ER-Grundwerte\\Format zum Erlernen des ER-Grundwerts** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-155">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="20fd8-156">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-156">Select **Designer**.</span></span>
5. <span data-ttu-id="20fd8-157">Wählen Sie in der Struktur **Ausgabe\\Dokument** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-157">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="20fd8-158">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-158">Select **Add**.</span></span>
7. <span data-ttu-id="20fd8-159">Im Drop-Down-Dialogfeld in der Struktur, wählen Sie **XML \\ Attribut** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-159">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="20fd8-160">Geben Sie im Feld **Name** **ProcessingDateTime** ein.</span><span class="sxs-lookup"><span data-stu-id="20fd8-160">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="20fd8-161">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-161">Select **OK**.</span></span>
10. <span data-ttu-id="20fd8-162">Wählen Sie auf der Registerkarte **Zuordnung** in der Struktur **Ausgabe \\Dokument\\ProcessingDateTime** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-162">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="20fd8-163">Wählen Sie **Formel bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-163">Select **Edit formula**.</span></span>
12. <span data-ttu-id="20fd8-164">Geben Sie im Feld **Formel** den folgenden Ausdruck ein: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="20fd8-164">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="20fd8-165">Wählen Sie **Speichern** und dann **Test** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-165">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="20fd8-166">Wählen Sie **Test** erneut aus, um den konfigurierten Ausdruck zu testen.</span><span class="sxs-lookup"><span data-stu-id="20fd8-166">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="20fd8-167">![Formeldesignerseite](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot der Formeldesignerseite")</span><span class="sxs-lookup"><span data-stu-id="20fd8-167">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="20fd8-168">Die Registerkarte **Testergebnis** gibt an, dass der konfigurierte Ausdruck einen unterschiedlichen Datums-und Uhrzeitwert zurückgibt, wenn sie angerufen wird.</span><span class="sxs-lookup"><span data-stu-id="20fd8-168">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="20fd8-169">Schließen Sie die Seite **Formeldesginer** und wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-169">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="20fd8-170">![Formatdesignerseite](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot der Formatdesignerseite")</span><span class="sxs-lookup"><span data-stu-id="20fd8-170">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="20fd8-171">Seite **Format-Designer** schließen.</span><span class="sxs-lookup"><span data-stu-id="20fd8-171">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="20fd8-172">Entfernen Sie eine vorhandene Ausgangaswertregel</span><span class="sxs-lookup"><span data-stu-id="20fd8-172">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="20fd8-173">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-173">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="20fd8-174">Wählen Sie **Ausgangswerte** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-174">Select **Baselines**.</span></span>
3. <span data-ttu-id="20fd8-175">In der Liste der Ausgangswerte wählen Sie den Ausgangswert aus, der für das Format **Format zum erlernen von ER-Ausgangswerten** konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="20fd8-175">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="20fd8-176">Auf dem Inforegister **Ausgangswerte** wählen Sie **Löschen** aus, um die Ausgangswertregel zu entfernen, die Sie zuvor konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="20fd8-176">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="20fd8-177">![Seite für die Formatgrundlage für elektronische Berichterstellung](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot der Formatgrundlagen für elektronische Berichterstellung")</span><span class="sxs-lookup"><span data-stu-id="20fd8-177">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="20fd8-178">Definieren Sie Ersatz für Bindungen eines entworfenen ER-Formats</span><span class="sxs-lookup"><span data-stu-id="20fd8-178">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="20fd8-179">Wählen Sie auf der Seite **Konfigurationen** auf dem Inforegister **Ersatz** die Option **Komponenten auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-179">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="20fd8-180">In der Formatkomponentenstruktur erweitern Sie den Knoten **Ausgabe**, erweitern Sie **Ausgabe \\Dokument** und aktivieren Sie anschließend das Kontrollkästchen für **Ausgabe \\Dokument\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-180">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>

    <span data-ttu-id="20fd8-181">![Dialogfeld „Komponenten auswählen“](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Screenshot des Dialogfelds „Komponenten auswählen“")</span><span class="sxs-lookup"><span data-stu-id="20fd8-181">![Select Components dialog box](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Screenshot of the Select Components dialog box")</span></span>

3. <span data-ttu-id="20fd8-182">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-182">Select **OK**.</span></span>

<span data-ttu-id="20fd8-183">![Seite für die Formatgrundlage für elektronische Berichterstellung](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot der Formatgrundlagen für elektronische Berichterstellung")</span><span class="sxs-lookup"><span data-stu-id="20fd8-183">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="20fd8-184">Die ausgewählte ER-Formatkomponente wurde der Liste der Komponenten auf dem Inforegister **Ersetzungen** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="20fd8-184">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="20fd8-185">Wenn das Basis-ER-Format in Debugmodus ausgeführt wird, wird die Bindung des Formats für jede Komponente durch die Bindung ersetzt, die in der Spalte **Binden** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="20fd8-185">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="20fd8-186">Um die Standardbindung für eine Komponente zu ändern, die im Inforegister **Ersetzungen** angezeigt wird, wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-186">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="20fd8-187">Erstellen eines neuen Grundwertregel</span><span class="sxs-lookup"><span data-stu-id="20fd8-187">Make a new baseline rule</span></span>

<span data-ttu-id="20fd8-188">Führen Sie die Schritte im Abschnitt „Beispiel: Automatisieren Sie die Struktur der Grundlagenregeln“ oben in diesem Thema aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-188">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="20fd8-189">Eine Benachrichtigung warnt Sie, dass die ausgehende Datei mit Ausgangswerteinstellungen erstellt wurde, und dass eine erzwungene Ersetzung der Formatbindungen aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="20fd8-189">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="20fd8-190">![Benachrichtigung auf der Seite „Konfigurationen“](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot der Benachrichtigung auf der Seite „Konfigurationen“")</span><span class="sxs-lookup"><span data-stu-id="20fd8-190">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="20fd8-191">Warnungen zur Ersetzung von Formatbindungen unterdrücken</span><span class="sxs-lookup"><span data-stu-id="20fd8-191">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="20fd8-192">Durch das Festlegen bestimmter ER-Parameter können Sie Benachrichtigungen unterdrücken, die vor der Ersetzung von Formatbindungen warnen.</span><span class="sxs-lookup"><span data-stu-id="20fd8-192">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="20fd8-193">Diese Unterdrückung kann hilfreich sein, wenn Formatbindungen in einem unbeaufsichtigten Modus ersetzt werden, indem Regression Suite Automation Tool verwndet wird.</span><span class="sxs-lookup"><span data-stu-id="20fd8-193">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="20fd8-194">In diesem Fall kann die Warnung als ein Fehler des Testfalls, der ausgeführt wird, betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="20fd8-194">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="20fd8-195">Wählen Sie auf der Seite **Konfigurationen** im Aktivitätsbereich auf der Registerkarte **Konfigurationen** die Option **Benutzerparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="20fd8-196">Legen Sie die Option **Ausgangswertwarnungen unterdrücken** auf **Ja** fest, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-196">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

<span data-ttu-id="20fd8-197">![Benutzerparameterdialogfeld](media/GER-BaselineSample-ERUserParameters1.png "Screenshot des Benutzerparameterdialogfelds")</span><span class="sxs-lookup"><span data-stu-id="20fd8-197">![User parameters dialog box](media/GER-BaselineSample-ERUserParameters1.png "Screenshot of the User parameters dialog box")</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="20fd8-198">Überprüfen Sie die erstellte Ausgangswertdatei</span><span class="sxs-lookup"><span data-stu-id="20fd8-198">Review the generated baseline file</span></span>

1. <span data-ttu-id="20fd8-199">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-199">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="20fd8-200">Wählen Sie **Ausgangswerte** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-200">Select **Baselines**.</span></span>
3. <span data-ttu-id="20fd8-201">Wählen Sie **Anhänge** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-201">Select **Attachments**.</span></span>

    <span data-ttu-id="20fd8-202">![Anhangseite](media/GER-BaselineSample-AttachedBaselineFile.PNG "Screenshot der Anhangseite")</span><span class="sxs-lookup"><span data-stu-id="20fd8-202">![Attachments page](media/GER-BaselineSample-AttachedBaselineFile.PNG "Screenshot of the Attachments page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="20fd8-203">Die generierte Datei beinhaltet das Verarbeitungsdatum und den Zeittext (**"#"**) von der Bindung, die in der hinzugefügten Ausgangswertregel konfiguriert wurde, nicht aus der Bindung des Formats.</span><span class="sxs-lookup"><span data-stu-id="20fd8-203">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>

4. <span data-ttu-id="20fd8-204">Schließen Sie die Seite **Anhänge**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-204">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="20fd8-205">Führen Sie das entworfene ER-Format aus und prüfen Sie das Protokoll, um die Ergebnisse zu analysieren</span><span class="sxs-lookup"><span data-stu-id="20fd8-205">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="20fd8-206">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-206">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="20fd8-207">Erweitern Sie in der Struktur **Modell zum erlernen der ER-Grundwerte**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-207">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="20fd8-208">Wählen Sie in der Struktur das Format **Modell zum erlernen der ER-Grundwerte\\Format zum Erlernen des ER-Grundwerts** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-208">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="20fd8-209">Wählen Sie im Inforegister **Versionen** **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-209">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="20fd8-210">Geben Sie im Feld **Eingabe-Id** den Wert **1** ein.</span><span class="sxs-lookup"><span data-stu-id="20fd8-210">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="20fd8-211">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-211">Select **OK**.</span></span>
7. <span data-ttu-id="20fd8-212">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurations-Debug-Protokolle**.</span><span class="sxs-lookup"><span data-stu-id="20fd8-212">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="20fd8-213">Das Ausführungsprotokoll enthält Informationen über die Ergebnisse des Vergleichs der generierten Datei mit der konfigurierten Grundlage.</span><span class="sxs-lookup"><span data-stu-id="20fd8-213">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="20fd8-214">Das Protokoll gibt an, dass die generierte Datei und der Ausgangswert gleich sind, auch wenn das ausgeführte Format die Bindung enthält, mit der ein sich ständig ändernder Datums-und Uhrzeitwert in der ausgehenden Datei eingeben wird.</span><span class="sxs-lookup"><span data-stu-id="20fd8-214">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="20fd8-215">Obgleich die ausgehende Datei mit Ausgangswerteinstellungen erstellt wurde, die die Ersetzung der Bindungen des Formats erzwingen, erhalten Sie keine Warnungen zur Ersetzung.</span><span class="sxs-lookup"><span data-stu-id="20fd8-215">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="20fd8-216">Ausgangswerteinstellungen zwischen Umgebungen austauschen</span><span class="sxs-lookup"><span data-stu-id="20fd8-216">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="20fd8-217">Ausgangswerteinstellungen exportieren</span><span class="sxs-lookup"><span data-stu-id="20fd8-217">Export baseline settings</span></span>

<span data-ttu-id="20fd8-218">Mit den neuen ER-Funktionen können Sie Ausgangswerteinstellungen für das ausgewählte ER-Format aus der aktuellen Finance and Operations-Umgebung exportieren und als XML-Dateien speichern.</span><span class="sxs-lookup"><span data-stu-id="20fd8-218">The new ER capabilities let you export baseline settings for the selected ER format from the current Finance and Operations environment and store them as XML files.</span></span> 

<span data-ttu-id="20fd8-219">Um Ausgangswerteinstellungen zu exportieren,wählen Sie auf der Seite **Formatausgangswerte für elektronische Berichterstellung** **Exportieren** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-219">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="20fd8-220">Grundwerte-Einstellungen importieren</span><span class="sxs-lookup"><span data-stu-id="20fd8-220">Import baseline settings</span></span>

<span data-ttu-id="20fd8-221">Exportierte Ausgangswerteinstellungen können in eine andere Finance and Operations-Umgebung importiert werden.</span><span class="sxs-lookup"><span data-stu-id="20fd8-221">Exported baseline settings can be imported into a different Finance and Operations environment.</span></span> <span data-ttu-id="20fd8-222">Die Umgebung muss zuerst als ER-Format importiert werden.</span><span class="sxs-lookup"><span data-stu-id="20fd8-222">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="20fd8-223">Sie können anschließend die Ausgangswerteinstellungen importieren.</span><span class="sxs-lookup"><span data-stu-id="20fd8-223">You can then import the baseline settings.</span></span>

<span data-ttu-id="20fd8-224">Um Ausgangswerteinstellungen aus einer lokal gespeicherten XML-Datei zu importieren, wählen Sie auf der Seite **Formatausgangswerte für elektronische Berichterstellung** **Importieren** und anschließend **Durchsuchen** aus, um die XML-Datei auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="20fd8-224">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="20fd8-225">![Dialogfeld „Ausgangswerteinstellungen importieren“](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot des Dialogfelds „Ausgangswerteinstellungen importieren“")</span><span class="sxs-lookup"><span data-stu-id="20fd8-225">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="20fd8-226">Um Ausgangswerteinstellungen aus einer XML-Datei zu importieren, die auf dem Microsoft SharePoint-Server gespeichert ist, wählen Sie basierend auf den aktuellen Einstellungen der Dokumentverwaltung und dem ausgewählten Dokumenttyp, auf Basis der aktuellen Dokumentverwaltungseinstellungen gespeichert wird und den ausgewählten Dokumenttyp auf der Seite **Formatausgangswerte für elektronische Berichterstellung** **Importieren aus Quelle** aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-226">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="20fd8-227">Wählen Sie dann den Dokumenttyp und die XML-Datei aus.</span><span class="sxs-lookup"><span data-stu-id="20fd8-227">Then select the document type and the XML file.</span></span> <span data-ttu-id="20fd8-228">Der erforderliche Dokumenttyp, um auf den SharePoint-Ordner zuzugreifen, muss zuvor bereits konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="20fd8-228">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="20fd8-229">![Dialogfeld „Importieren aus Quelle“](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot des Dialogfelds „Importieren aus Quelle“")</span><span class="sxs-lookup"><span data-stu-id="20fd8-229">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="20fd8-230">Sie können die Aufgabenaufzeichnung verwenden, um die Schritte zum Auswählen des erforderlichen Dokumenttyps und des Dateinamens im Dialogfeld **Importieren aus Quelle** zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="20fd8-230">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="20fd8-231">Auf diese Weise können Sie erforderliche Ausgangswerteinstellungen auf dem SharePoint-Server behalten und anschließend automatisch importieren, indem Sie eine Aufgabenaufzeichnung wiedergeben, wenn Sie automatisierte Tests ausführen, indem Sie Regression Suite Automation Tool verwenden.</span><span class="sxs-lookup"><span data-stu-id="20fd8-231">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20fd8-232">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="20fd8-232">Additional resources</span></span>

- [<span data-ttu-id="20fd8-233">Erstellte Berichtsergebnisse protokollieren und mit Ausgangswerten vergleichen</span><span class="sxs-lookup"><span data-stu-id="20fd8-233">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="20fd8-234">Aufgabenaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="20fd8-234">Task recorder</span></span>](../user-interface/task-recorder.md)