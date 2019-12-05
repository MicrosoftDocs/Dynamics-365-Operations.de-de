---
title: Einrichten von Parametern eines EB-Formats pro juristischer Person
description: In diesem Thema wird erläutert, wie Sie die Parameter eines Elektronische Berichterstellungs(EB)-Formats pro juristischer Entität konfigurieren können.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 9c5884bba494d2dd44f9204667144402a88ddec8
ms.sourcegitcommit: d6196d83c7b9166ddb4fe43a91e6bd0ad9da2099
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2019
ms.locfileid: "2694337"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="1cb96-103">Einrichten von Parametern eines EB-Formats pro juristischer Person</span><span class="sxs-lookup"><span data-stu-id="1cb96-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="1cb96-104">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1cb96-104">Prerequisites</span></span>

<span data-ttu-id="1cb96-105">Um diese Schritte auszuführen, müssen Sie zuerst die Schritte im Thema [Konfigurieren von EB-Formaten zur Verwendung von Parametern, die pro juristischer Person angegeben werden](er-app-specific-parameters-configure-format.md) ausführen.</span><span class="sxs-lookup"><span data-stu-id="1cb96-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="1cb96-106">Um die Beispiele in diesem Thema abzuschließen, müssen Sie für eine der folgenden Rollen Zugriff auf Microsoft Dynamics 365 Finance (Finance) haben:</span><span class="sxs-lookup"><span data-stu-id="1cb96-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="1cb96-107">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="1cb96-107">Electronic reporting developer</span></span>
- <span data-ttu-id="1cb96-108">Funktionaler Berater für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="1cb96-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="1cb96-109">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="1cb96-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="1cb96-110">ER Konfigurationen importieren</span><span class="sxs-lookup"><span data-stu-id="1cb96-110">Import ER configurations</span></span>

1.  <span data-ttu-id="1cb96-111">Melden Sie sich in Ihrer Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="1cb96-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="1cb96-112">Wählen Sie im Standard-Dashboard **Elektronische Berichterstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="1cb96-113">Wählen Sie **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="1cb96-114">Importieren Sie die Konfigurationen, die Sie während der Ausführung der Schritte im Thema [Konfigurieren von EB-Formaten zur Verwendung von Parametern, die pro juristischer Person angegeben werden](er-app-specific-parameters-configure-format.md) aus Regulatory Configuration Service (RCS) exportiert haben, in die aktuelle Instanz von Finance.</span><span class="sxs-lookup"><span data-stu-id="1cb96-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="1cb96-115">Führen Sie diese Schritte für jede Konfiguration der elektronischen Berichterstellung (EB) in der folgenden Reihenfolge aus: Datenmodell, Modellzuordnung und Formate.</span><span class="sxs-lookup"><span data-stu-id="1cb96-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="1cb96-116">Wählen Sie **Austausch \> Aus XML-Datei laden** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="1cb96-117">Wählen Sie **Durchsuchen** aus, um die Datei für die erforderliche EB-Konfiguration im XML-Format auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1cb96-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="1cb96-118">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="1cb96-118">Select **OK**.</span></span>
    
    <span data-ttu-id="1cb96-119">Die folgende Abbildung zeigt die Konfigurationen, die Sie haben müssen, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="1cb96-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![ER-Konfigurationsseite](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="1cb96-121">Einrichten von Parametern für das DEMF-Unternehmen</span><span class="sxs-lookup"><span data-stu-id="1cb96-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="1cb96-122">Sie können das EB-Framework verwenden, um anwendungsspezifische Parameter für ein EB-Format einzurichten.</span><span class="sxs-lookup"><span data-stu-id="1cb96-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="1cb96-123">Wählen Sie die juristische Person **DEMF** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="1cb96-124">Wählen Sie in der Konfigurationsstruktur das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="1cb96-125">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Konfigurationen** in der Gruppe **Anwendungsspezifische Parameter** die Option **Einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![Seite für anwendungsspezifische EB-Parameter](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="1cb96-127">Auf der Seite **Anwendungsspezifische Parameter** können Sie die Regeln für die Datenquelle **Auswahl** des Formats **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1cb96-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="1cb96-128">Wenn das Basis-EB-Format mehrere Datenquellen des Typs **Suche** enthält, müssen Sie die gewünschte Datenquelle im Inforegister **Suchen** auswählen, bevor Sie beginnen können, die Gruppe von Regeln für die Datenquelle zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1cb96-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="1cb96-129">Für jede Datenquelle können Sie separate Regeln für jede Version des ausgewählten EB-Formats konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1cb96-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="1cb96-130">Die gesamten Regeln für alle Suchendatenquellen, die in der ausgewählten Version des Basis-EB-Formats zur Verfügung stehen, stellen die anwendungsspezifischen Parameter für das EB-Format dar.</span><span class="sxs-lookup"><span data-stu-id="1cb96-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="1cb96-131">Wählen Sie Version **1.1.1** des EB-Formats aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="1cb96-132">Auf dem Inforegister **Bedingungen** wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="1cb96-133">Wählen Sie im Feld **Code** des neuen Datensatzes den Dropdown-Pfeil aus, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1cb96-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="1cb96-134">Die Suche zeigt die Liste der Steuercodes für die Auswahl an.</span><span class="sxs-lookup"><span data-stu-id="1cb96-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="1cb96-135">Diese Liste wird durch die Datenquelle **Model.Data.Tax** zurückgegeben, die im Basis-EB-Format konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="1cb96-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="1cb96-136">Da diese Datenquelle das Feld **Name** enthält, wird der Name jedes Steuercodes in der Suche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1cb96-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![Seite für anwendungsspezifische EB-Parameter](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="1cb96-138">Wählen Sie den Steuercode **VAT19** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="1cb96-139">Wählen Sie im Feld **Suchergebnis** des neuen Datensatzes den Dropdown-Pfeil aus, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1cb96-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="1cb96-140">Die Suche zeigt die Liste der Werte für die TaxationLevel-Formatenumeration zur Auswahl an.</span><span class="sxs-lookup"><span data-stu-id="1cb96-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="1cb96-141">Hinweis: Wenn Deutsch als bevorzugte Sprache des Benutzers ausgewählt wird, als der Sie angemeldet sind, werden die Beschriftungen der Werte in der Suche auf Deutsch angezeigt, sofern sie im Basis-EB-Format übersetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="1cb96-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="1cb96-142">Darüber hinaus erscheint die Beschriftung in der bevorzugten Sprache des Benutzers auf der Registerkarte **Suchen**, wennn die Beschriftung einer Suchendatenquelle übersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="1cb96-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![Seite für anwendungsspezifische EB-Parameter](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="1cb96-144">Wählen Sie den Wert **Reguläre Besteuerung** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="1cb96-145">Wenn Sie diesen Datensatz hinzufügen, legen Sie die folgende Regel fest: Sobald die Suchendatenquelle **Auswahl** angefordert wird und der Steuercode **VAT19** als Argument weitergegeben wird, wird **Reguläre Besteuerung** als erforderliche Besteuerungsstufe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1cb96-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="1cb96-146">Wählen Sie **Hinzufügen** aus und führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="1cb96-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="1cb96-147">Wählen Sie im Feld **Code** den Steuercode **InVAT19** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="1cb96-148">Wählen Sie im Feld **Suchergebnis** den Wert **Reguläre Besteuerung** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="1cb96-149">Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="1cb96-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="1cb96-150">Wählen Sie im Feld **Code** den Steuercode **VAT7** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="1cb96-151">Wählen Sie im Feld **Suchergebnis** den Wert **Reduzierte Besteuerung** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="1cb96-152">Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="1cb96-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="1cb96-153">Wählen Sie im Feld **Code** den Steuercode **InVAT7** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="1cb96-154">Wählen Sie im Feld **Suchergebnis** den Wert **Reduzierte Besteuerung** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="1cb96-155">Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="1cb96-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="1cb96-156">Wählen Sie im Feld **Code** den Steuercode **THIRD** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="1cb96-157">Wählen Sie im Feld **Suchergebnis** den Wert **Keine Besteuerung** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="1cb96-158">Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="1cb96-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="1cb96-159">Wählen Sie im Feld **Code** den Steuercode **InVAT0** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="1cb96-160">Wählen Sie im Feld **Suchergebnis** den Wert **Keine Besteuerung** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="1cb96-161">Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="1cb96-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="1cb96-162">Wählen Sie im Feld **Code** die Option **\*Nicht leer\*** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="1cb96-163">Wählen Sie im Feld **Suchergebnis** den Wert **Sonstige** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="1cb96-164">Wenn Sie diesen letzten Datensatz hinzufügen, legen Sie die folgende Regel fest: Sobald der Steuercode, der als Argument weitergegeben wird, keine der vorherigen Regeln erfüllt, gibt die Suchdatenquelle **Sonstige** als erforderliche Besteuerungsstufe zurück.</span><span class="sxs-lookup"><span data-stu-id="1cb96-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![Seite für anwendungsspezifische EB-Parameter](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="1cb96-166">Wählen Sie im Feld **Status** die Option **Abgeschlossen** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="1cb96-167">Wenn Sie eine EB-Formatversion ausführen, die entweder über den Status **Abgeschlossen** oder **Geteilt** verfügt, muss diese Gruppe von Regeln im Status **Abgeschlossen** sein.</span><span class="sxs-lookup"><span data-stu-id="1cb96-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="1cb96-168">Andernfalls wird Ausführung des Basis-EB-Formats unterbrochen, wenn das Format versucht, Daten aus dieser Gruppe von Regeln zu laden, während die Suchdatenquelle **Auswahl** ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1cb96-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="1cb96-169">Wenn Sie eine EB-Formatversion ausführen, die den Status **Entwurf** hat, kann das Basis-EB-Format unabhängig von deren Status auf diese Gruppe von Regeln zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1cb96-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="1cb96-170">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="1cb96-170">Select **Save**.</span></span>
18. <span data-ttu-id="1cb96-171">Schließen Sie die Seite **Anwendungsspezifische Parameter**.</span><span class="sxs-lookup"><span data-stu-id="1cb96-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="1cb96-172">Ausführen des EB-Formats im Unternehmen DEMF</span><span class="sxs-lookup"><span data-stu-id="1cb96-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="1cb96-173">Wählen Sie in der Konfigurationsstruktur das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="1cb96-174">Wählen Sie im Aktivitätsbereich auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="1cb96-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="1cb96-175">Im angezeigten Dialogfeld wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="1cb96-176">Laden Sie den erzeugten Auszug herunter und speichern Sie ihn lokal.</span><span class="sxs-lookup"><span data-stu-id="1cb96-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="1cb96-177">Beachten Sie, dass im generierten Auszug die Zusammenfassung des Steuercodes **InVAT7** auf die Ebene **Reduziert** festgelegt wurde, und Zusammenfassungen der Steuercodes **VAT19** und **InVA19** auf die Ebene **Regulär** festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="1cb96-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="1cb96-178">Dieses Verhalten wird von der Konfiguration in der Gruppe von Regeln bestimmt, die von juristischen Entitäten abhängen.</span><span class="sxs-lookup"><span data-stu-id="1cb96-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="1cb96-179">Gehen Sie zu **Steuer \> Indirekte Steuern \> Mehrwertsteuer \> Mehrwertsteuercodes**.</span><span class="sxs-lookup"><span data-stu-id="1cb96-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="1cb96-180">Wählen Sie den Steuercode **InVAT7** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="1cb96-181">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Mehrwertsteuercode** in der Gruppe **Abfragen** die Option **Gebuchte Mehrwertsteuer** aus, um Informationen zum Steuerwert und dem angewendeten Steuersatz pro Steuercode anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1cb96-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![Veröffentlichte Umsatzsteuer-Seite](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="1cb96-183">Schließen Sie die Seite „Gebuchte Mehrwertsteuer“.</span><span class="sxs-lookup"><span data-stu-id="1cb96-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="1cb96-184">Einrichten von Parametern für das USMF-Unternehmen</span><span class="sxs-lookup"><span data-stu-id="1cb96-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="1cb96-185">Wählen Sie die juristische Person **USMF** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="1cb96-186">Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="1cb96-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="1cb96-187">Erweitern Sie in der Konfigurationsstruktur das Element **Modell zum Lernern parametrisierter Aufrufe**, erweitern Sie das Element **Format zum Ermitteln parametrisierter Anrufe**, und wählen Sie das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="1cb96-188">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Konfigurationen** in der Gruppe **Anwendungsspezifische Parameter** die Option **Einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="1cb96-189">Wählen Sie Version **1.1.1** des ausgewählten EB-Formats aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="1cb96-190">Auf dem Inforegister **Bedingungen** wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="1cb96-191">Wählen Sie im Feld **Code** des neuen Datensatzes den Dropdown-Pfeil aus, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1cb96-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="1cb96-192">Die Suche zeigt nun die Liste der Steuercodes für die Steuer des **USMF**-Unternehmens zur Auswahl an.</span><span class="sxs-lookup"><span data-stu-id="1cb96-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![Seite für anwendungsspezifische EB-Parameter](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="1cb96-194">Wählen Sie den Steuercode **BEFREIT** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="1cb96-195">Wählen Sie im Feld **Suchergebnis** des neuen Datensatzes den Wert **Keine Besteuerung** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-195">In the **Lookup resul**t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="1cb96-196">Wählen Sie erneut **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-196">Select **Add** again.</span></span>
11. <span data-ttu-id="1cb96-197">Wählen Sie im Feld **Code** des neuen Datensatzes die Option **\*Nicht leer\*** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="1cb96-198">Wählen Sie im Feld **Suchergebnis** des neuen Datensatzes den Wert **Reguläre Besteuerung** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="1cb96-199">Wählen Sie im Feld **Status** die Option **Abgeschlossen** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="1cb96-200">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="1cb96-200">Select **Save**.</span></span>

    ![Seite für anwendungsspezifische EB-Parameter](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="1cb96-202">Schließen Sie die Seite **Anwendungsspezifische Parameter**.</span><span class="sxs-lookup"><span data-stu-id="1cb96-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="1cb96-203">Ausführen des EB-Formats im Unternehmen USMF</span><span class="sxs-lookup"><span data-stu-id="1cb96-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="1cb96-204">Wählen Sie in der Konfigurationsstruktur das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="1cb96-205">Wählen Sie im Aktivitätsbereich auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="1cb96-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="1cb96-206">Im angezeigten Dialogfeld wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="1cb96-207">Laden Sie den erzeugten Auszug herunter und speichern Sie ihn lokal.</span><span class="sxs-lookup"><span data-stu-id="1cb96-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="1cb96-208">Beachten Sie, dass Sie nun im generierten Auszug dasselbe EB-Format wieder für eine andere juristische Person verwendet haben, ohne jedoch Änderungen am EB-Format vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="1cb96-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="1cb96-209">Wiederverwenden von Parametern, die von juristischen Personen abhängen</span><span class="sxs-lookup"><span data-stu-id="1cb96-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="1cb96-210">Exportieren von Parametern</span><span class="sxs-lookup"><span data-stu-id="1cb96-210">Export parameters</span></span>

1.  <span data-ttu-id="1cb96-211">Wechseln Sie zu **Organisationsverwaltung  \>Arbeitsbereiche \>  Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="1cb96-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="1cb96-212">Wählen Sie **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="1cb96-213">Wählen Sie in der Konfigurationsstruktur das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="1cb96-214">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Konfigurationen** in der Gruppe **Anwendungsspezifische Parameter** die Option **Einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="1cb96-215">Wählen Sie Version **1.1.1** des EB-Formats aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="1cb96-216">Wählen Sie im Aktivitätsbereich **Exportieren** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="1cb96-217">Laden Sie die erzeugte Datei herunter und speichern Sie sie lokal.</span><span class="sxs-lookup"><span data-stu-id="1cb96-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="1cb96-218">Die konfigurierte Gruppe von anwendungsspezifischen Parametern wurde nun als XML-Datei exportiert.</span><span class="sxs-lookup"><span data-stu-id="1cb96-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="1cb96-219">Importieren von Parametern</span><span class="sxs-lookup"><span data-stu-id="1cb96-219">Import parameters</span></span>

1.  <span data-ttu-id="1cb96-220">Wählen Sie Version **1.1.2** des EB-Formats aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="1cb96-221">Wählen Sie im Aktivitätsbereich **Importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="1cb96-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="1cb96-222">Wählen Sie **Ja** aus, um zu bestätigen, dass Sie die vorhandenen anwendungsspezifischen Parameter für diese Formatversion überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="1cb96-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="1cb96-223">Wählen Sie **Durchsuchen** aus, um die Datei zu suchen, die die exportierten anwendungsspezifischen Parameter für Version **1.1.1** enthält.</span><span class="sxs-lookup"><span data-stu-id="1cb96-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="1cb96-224">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="1cb96-224">Select **OK**.</span></span>

    <span data-ttu-id="1cb96-225">Version **1.1.2** des EB-Formats verfügt jetzt über die gleichen anwendungsspezifischen Parameter, die Sie ursprünglich für Version **1.1.1** konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="1cb96-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="1cb96-226">Beachten Sie, dass die anwendungsspezifischen Parameter eines EB-Formats von der juristischen Person abhängen.</span><span class="sxs-lookup"><span data-stu-id="1cb96-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="1cb96-227">Um die anwendungsspezifischen Parameter wieder zu verwenden, die für eine juristische Person in einer anderen juristischen Person konfiguriert wurden, müssen Sie sie exportieren, während Sie in der ersten juristischen Person angemeldet sind, und sie dann importieren, nachdem Sie sich in der anderen juristischen Person angemeldet haben.</span><span class="sxs-lookup"><span data-stu-id="1cb96-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="1cb96-228">Sie können diesen Ansatz auch verwenden, um EB-Format-zugehörige anwendungsspezifische Parameter, die ursprünglich in einer Instanz von Finance konfiguriert wurden, in eine andere Instanz von Finance zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="1cb96-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="1cb96-229">Beachten Sie, dass die vorhandenen anwendungsspezifischen Parameter nicht für die importierte Version angewendet werden, wenn Sie anwendungsspezifische Parameter für eine Version eines EB-Formats konfigurieren und eine höhere Version desselben Formats in die aktuelle Finance-Instanz importieren.</span><span class="sxs-lookup"><span data-stu-id="1cb96-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="1cb96-230">Beachten Sie auch, dass, wenn Sie eine Datei für den Import auswählen, die Struktur der anwendungsspezifischen Parameter in dieser Datei mit der Struktur der entsprechenden Datenquelle des Typs **Suche** im EB-Format verglichen wird, die für den Import ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="1cb96-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="1cb96-231">Der Import ist erledigt, wenn die Struktur jedes anwendungsspezifischen Parameters mit der Struktur der entsprechenden Datenquelle im EB-Format übereinstimmt, die für den Import ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="1cb96-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="1cb96-232">Wenn die Strukturen nicht übereinstimmen, erhalten Sie eine Warnmeldung, die angibt, dass der Import nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1cb96-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="1cb96-233">Wenn Sie den Abschluss des Imports erzwingen, werden die vorhandenen anwendungsspezifischen Parameter für das ausgewählte EB-Format bereinigt, und Sie müssen Sie noch einmal neu einrichten.</span><span class="sxs-lookup"><span data-stu-id="1cb96-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="1cb96-234">Beziehung zwischen anwendungsspezifischen Parametern und einem EB-Format</span><span class="sxs-lookup"><span data-stu-id="1cb96-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="1cb96-235">Die Beziehung zwischen einem EB-Format und seinen anwendungsspezifischen Parametern wird durch den instanzunabhängigen eindeutigen Kennungscode der EB-Instanz bestimmt.</span><span class="sxs-lookup"><span data-stu-id="1cb96-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="1cb96-236">Wenn Sie also ein EB-Format aus Finance entfernen, werden die anwendungsspezifischen Parameter, die für das EB-Format konfiguriert werden, in der aktuelle Instanz von Finance beibehalten.</span><span class="sxs-lookup"><span data-stu-id="1cb96-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="1cb96-237">Auf sie kann zugegriffen werden, sobald das Basis-EB-Format wieder in diese Finance-Instanz importiert wird.</span><span class="sxs-lookup"><span data-stu-id="1cb96-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="1cb96-238">Zugreifen auf anwendungsspezifische Parameter durch Verwendung des EB-Frameworks</span><span class="sxs-lookup"><span data-stu-id="1cb96-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="1cb96-239">Im vorherigen Beispiel haben Sie auf anwendungsspezifische Parameter eines EB-Formats zugegriffen, indem Sie das EB-Framework verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="1cb96-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="1cb96-240">Durch diesen Ansatz können Sie den Zugriff auf die anwendungsspezifischen Parameter eines bestimmten EB-Formats nicht einschränken.</span><span class="sxs-lookup"><span data-stu-id="1cb96-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="1cb96-241">Wenn Sie solche Einschränkungen anwenden möchten, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="1cb96-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="1cb96-242">Verwenden Sie entweder eine vorhandene Menüoption **ERSolutionAppSpecificParametersDesigner** erneut oder implementieren Sie Ihre eigene Menüoption **ERSolutionAppSpecificParametersDesigner**.</span><span class="sxs-lookup"><span data-stu-id="1cb96-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![Visual Studio-Seite](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="1cb96-244">Führen Sie einen dieser Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="1cb96-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="1cb96-245">Erstellen Sie eine neue Menüoptionsschaltfläche und verknüpfen Sie diese mit dem gewünschten Datensatz aus der Tabelle **ERSolutionTable**, indem Sie die Eigenschaft **Datenquelle** auf **ERSolutionTable** festlegen.</span><span class="sxs-lookup"><span data-stu-id="1cb96-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![Visual Studio-Seite](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="1cb96-247">Erstellen Sie eine einfache Schaltfläche und überschreiben Sie die Methode **Geklickt** wie im folgenden Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1cb96-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="1cb96-248">Wenn Sie diesen Ansatz verwenden, können Sie eine eindeutige Lösungskennung angeben (definiert über den Wert **GUID** ), um den Zugriff auf die anwendungsspezifischen Parameter eines bestimmten EB-Formats und nachfolgenden Kopien zuzulassen, die davon abgeleitet wurden.</span><span class="sxs-lookup"><span data-stu-id="1cb96-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="1cb96-249">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1cb96-249">Additional resources</span></span>

[<span data-ttu-id="1cb96-250">Formeldesigner in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="1cb96-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="1cb96-251">Konfigurieren von ER-Formaten zur Verwendung von Parametern, die pro juristischer Person angegeben werden</span><span class="sxs-lookup"><span data-stu-id="1cb96-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)
