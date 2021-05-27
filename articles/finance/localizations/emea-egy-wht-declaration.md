---
title: Quellensteuererklärung für Ägypten
description: In diesem Thema wird erläutert, wie Sie die Quellensteuererklärungen für Ägypten konfigurieren und generieren.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8c9aaa3868167806ce3189d724621991ec7e53eb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022810"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="ed3da-103">Quellensteuererklärung für Ägypten (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="ed3da-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="ed3da-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="ed3da-104">Overview</span></span>
<span data-ttu-id="ed3da-105">In diesem Thema wird erläutert, wie Sie die Quellensteuererklärung und die Quellensteuererklärungsformulare 41 und 11 für juristische Personen in Ägypten einrichten und erstellen.</span><span class="sxs-lookup"><span data-stu-id="ed3da-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="ed3da-106">Alle ägyptischen Unternehmen müssen das Formular 41 erstellen, in dem alle Steuern zusammengefasst sind, die von lokalen Lieferanten und Dienstleistern einbehalten werden.</span><span class="sxs-lookup"><span data-stu-id="ed3da-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="ed3da-107">Zusätzlich zu Formular 41 muss Formular 11 erstellt werden, in dem alle von ausländischen Anbietern einbehaltene Steuern aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ed3da-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="ed3da-108">Der Bericht **Quellensteuererklärung** in Dynamics 365 Finance enthält die folgenden Berichte:</span><span class="sxs-lookup"><span data-stu-id="ed3da-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="ed3da-109">Erklärungsformular Nr.</span><span class="sxs-lookup"><span data-stu-id="ed3da-109">Declaration form No.</span></span> <span data-ttu-id="ed3da-110">41</span><span class="sxs-lookup"><span data-stu-id="ed3da-110">41</span></span>
- <span data-ttu-id="ed3da-111">Erklärungsformular Nr.</span><span class="sxs-lookup"><span data-stu-id="ed3da-111">Declaration form No.</span></span> <span data-ttu-id="ed3da-112">11</span><span class="sxs-lookup"><span data-stu-id="ed3da-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="ed3da-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ed3da-113">Prerequisites</span></span>
<span data-ttu-id="ed3da-114">Die primäre Adresse der juristischen Person muss in Ägypten liegen.</span><span class="sxs-lookup"><span data-stu-id="ed3da-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="ed3da-115">Im Arbeitsbereich **Funktionsverwaltung** muss die folgende Funktion aktiviert sein:</span><span class="sxs-lookup"><span data-stu-id="ed3da-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="ed3da-116">**Globale Quellensteuer**</span><span class="sxs-lookup"><span data-stu-id="ed3da-116">**Global withholding tax**</span></span>

<span data-ttu-id="ed3da-117">Weitere Informationen zur Aktivierung von Funktionen finden Sie unter [Funktionsverwaltungsüberblick](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ed3da-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="ed3da-118">Rufen Sie **Steuer** > **Einrichtung** > **Parameter** > **Hauptbuchparameter** auf. Setzen Sie anschließend auf der **Quellensteuer**-Registerkarte **Globale Quellensteuer aktivieren** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ed3da-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="ed3da-119">Importieren Sie im Arbeitsbereich **Elektronische Berichterstattung** die folgenden elektronischen Berichtsformate aus dem Repository:</span><span class="sxs-lookup"><span data-stu-id="ed3da-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="ed3da-120">Quellensteuererklärung Excel (EG)</span><span class="sxs-lookup"><span data-stu-id="ed3da-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="ed3da-121">Das obige Format basiert auf dem **Steuererklärungsmodell** und verwendet die **Zuordnung des Steuererklärungsmodells**.</span><span class="sxs-lookup"><span data-stu-id="ed3da-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="ed3da-122">Diese zusätzliche Konfiguration wird automatisch importiert.</span><span class="sxs-lookup"><span data-stu-id="ed3da-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="ed3da-123">Weitere Informationen zum Importieren von Konfigurationen für elektronische Berichte finden Sie unter [Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="ed3da-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="ed3da-124">Elektronische Berichtskonfigurationen herunterladen</span><span class="sxs-lookup"><span data-stu-id="ed3da-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="ed3da-125">Die Implementierung der Quellensteuererklärungsformulare für Ägypten basiert auf Konfigurationen für die elektronische Berichterstattung (ER).</span><span class="sxs-lookup"><span data-stu-id="ed3da-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="ed3da-126">Weitere Informationen zu den Funktionen und Konzepten der konfigurierbaren Berichterstellung finden Sie unter [Elektronische Berichterstattung](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="ed3da-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="ed3da-127">Befolgen Sie für Produktions- und UAT-Umgebungen (User Acceptance Testing) die Anweisungen im Thema: [Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="ed3da-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="ed3da-128">Um die Quellensteuererklärungen in einer ägyptischen juristischen Person zu generieren, müssen Sie die folgenden Konfigurationen hochladen:</span><span class="sxs-lookup"><span data-stu-id="ed3da-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="ed3da-129">Steuererklärung model.version.82.xml oder eine neuere Version</span><span class="sxs-lookup"><span data-stu-id="ed3da-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="ed3da-130">Steuererklärungsmodell mapping.version.82.133.xml oder eine neuere Version</span><span class="sxs-lookup"><span data-stu-id="ed3da-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="ed3da-131">Quellensteuererklärung Excel (EG).version.82.21 oder eine neuere Version</span><span class="sxs-lookup"><span data-stu-id="ed3da-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="ed3da-132">Führen Sie die folgenden Schritte aus, nachdem Sie die ER-Konfigurationen von Lifecycle Services (LCS) oder dem globalen Repository heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="ed3da-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="ed3da-133">Wechseln Sie in den Arbeitsbereich **Elektronische Berichterstellung** und wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed3da-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="ed3da-134">Wählen Sie auf der Seite **Konfigurationen** im Aktionsbereich **Austausch > Aus XML-Datei laden** aus.</span><span class="sxs-lookup"><span data-stu-id="ed3da-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="ed3da-135">Laden Sie alle Dateien in der Reihenfolge hoch, in der sie in den vorherigen Aufzählungszeichen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ed3da-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="ed3da-136">Nachdem alle Konfigurationen hochgeladen wurden, sollte der Konfigurationsbaum in Finance vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ed3da-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="ed3da-137">Anwendungsspezifische Parameter einrichten</span><span class="sxs-lookup"><span data-stu-id="ed3da-137">Set up application-specific parameters</span></span>

<span data-ttu-id="ed3da-138">Mit der Option für anwendungsspezifische Parameter können Benutzer die Kriterien festlegen, nach denen die Steuertransaktionen in jeder Zeile eines generierten Berichts abhängig von der Konfiguration von **Artikel-Quellensteuergruppe** oder andere Kriterien, die in der Definition der Suche festgelegt sind, klassifiziert und berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="ed3da-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="ed3da-139">Das Quellensteuererklärungsformular 41 enthält eine bestimmte Spalte, in der die Quellensteuertransaktion gemäß der Klassifizierung der Steuerbehörde namens **Rabattcode-Typ** klassifiziert werden muss.</span><span class="sxs-lookup"><span data-stu-id="ed3da-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="ed3da-140">Anstatt diese neuen Klassifizierungen als neue Eintragsdaten einzuschließen, wenn die Transaktionen gebucht werden, werden die Klassifizierungen basierend auf den verschiedenen in **Konfigurationen** > **Anwendungsspezifische Parameter einrichten** > **Einrichten** eingeführten Suchvorgängen bestimmt, um die Anforderungen der Quellensteuerberichte für Ägypten zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ed3da-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="ed3da-141">Die folgende Konfiguration wird verwendet, um die Transaktionen im Bericht des Quellensteuererklärungsformulars 41 zu klassifizieren:</span><span class="sxs-lookup"><span data-stu-id="ed3da-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="ed3da-142">**DiscountTaxTypeLookup**-> Spalte Nr. 18</span><span class="sxs-lookup"><span data-stu-id="ed3da-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="ed3da-143">Führen Sie die folgenden Schritte aus, um die verschiedenen Suchvorgänge einzurichten, die zum Generieren der Quellensteuererklärung und der zugehörigen Buchberichte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed3da-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="ed3da-144">In dem Arbeitsbereich **Elektronische Berichterstattung** wählen Sie **Konfigurationen** > **Einrichten** aus, um die Regeln zur Identifizierung der Klassifizierung von Transaktionen im Quellensteuererklärungsbericht einzurichten.</span><span class="sxs-lookup"><span data-stu-id="ed3da-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="ed3da-145">Wählen Sie die aktuelle Version aus und wählen Sie im Inforegister **Suchvorgänge** den Suchnamen.</span><span class="sxs-lookup"><span data-stu-id="ed3da-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="ed3da-146">Zum Beispiel **DiscountTaxTypeLookup**.</span><span class="sxs-lookup"><span data-stu-id="ed3da-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="ed3da-147">Diese Suche identifiziert die Liste der von der Steuerbehörde benötigten Rabattarten.</span><span class="sxs-lookup"><span data-stu-id="ed3da-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="ed3da-148">Im Inforegister **Bedingungen** wählen Sie **Hinzufügen** aus und in der neuen Zeile in der Spalte **Suchergebnis** wählen Sie die zugehörige Zeile aus, die die Klassifizierung in der **Spalte 18** darstellt.</span><span class="sxs-lookup"><span data-stu-id="ed3da-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="ed3da-149">In der Spalte **Artikel-Quellensteuergruppe** wählen Sie den zugehörigen Code aus, mit dem die Klassifizierung identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="ed3da-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="ed3da-150">Zum Beispiel **Zulässiger Rabatt**.</span><span class="sxs-lookup"><span data-stu-id="ed3da-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="ed3da-151">Wiederholen Sie die Schritte 3 und 4 für alle verfügbaren Suchvorgänge.</span><span class="sxs-lookup"><span data-stu-id="ed3da-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="ed3da-152">Wählen Sie erneut **Hinzufügen** aus, um die letzte Belegzeile aufzunehmen, und in der **Suchergebnis**-Spalte wählen Sie **Unzutreffend** aus.</span><span class="sxs-lookup"><span data-stu-id="ed3da-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="ed3da-153">Wählen Sie in den verbleibenden Spalten **Nicht leer** aus.</span><span class="sxs-lookup"><span data-stu-id="ed3da-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="ed3da-154">Einrichten der Hauptbuchparameter</span><span class="sxs-lookup"><span data-stu-id="ed3da-154">Set up General ledger parameters</span></span>

<span data-ttu-id="ed3da-155">Um die Quellensteuer-Erklärungsformularberichte in Microsoft Excel zu generieren, definieren Sie ein ER-Format auf der **Hauptbuchparameter**-Seite.</span><span class="sxs-lookup"><span data-stu-id="ed3da-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="ed3da-156">Gehen Sie zu **Steuer** > **Einrichten** > **Hauptbuchparameter**.</span><span class="sxs-lookup"><span data-stu-id="ed3da-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="ed3da-157">Auf der **Quellensteuer**-Registerkarte im Feld **Quellensteuer-Erklärungsformularzuordnung** wählen Sie **Quellensteuererklärung Excel (EG)** aus.</span><span class="sxs-lookup"><span data-stu-id="ed3da-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="ed3da-158">Wenn Sie das Feld leer lassen, wird der Standardmehrwertsteuerbericht im SSRS-Format erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed3da-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![Erklärungsformular](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="ed3da-160">Quellensteuererklärungsformulare generieren</span><span class="sxs-lookup"><span data-stu-id="ed3da-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="ed3da-161">Der Prozess der Erstellung und Übermittlung eines Quellensteuererklärungsformulars für einen bestimmten Zeitraum basiert auf den Quellensteuertransaktionen, die während des Abrechnungs- und Nachzahlungssteuerauftrags gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="ed3da-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="ed3da-162">Weitere Informationen zur globalen Quellensteuer finden Sie unter [Globale Quellensteuer](../general-ledger/global-withholding-tax-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ed3da-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="ed3da-163">Führen Sie die folgenden Schritte zum Generieren des Steuererklärungsberichts aus:</span><span class="sxs-lookup"><span data-stu-id="ed3da-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="ed3da-164">Gehen Sie zu **Steuer** > **Erklärungen** > **Quellensteuer** > \**Quellensteuerzahlung*.</span><span class="sxs-lookup"><span data-stu-id="ed3da-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="ed3da-165">Wählen Sie den Abrechnungszeitraum und dann das Anfangsdatum für den Bericht aus.</span><span class="sxs-lookup"><span data-stu-id="ed3da-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="ed3da-166">Geben Sie Transaktionsdatum ein, und wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ed3da-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="ed3da-167">Wählen Sie im daraufhin angezeigten Dialogfeld einen oder mehrere der Formulartypen **Formular Nr. 41**, **Formular Nr. 11** oder **Keiner** aus.</span><span class="sxs-lookup"><span data-stu-id="ed3da-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="ed3da-168">Wenn Sie **Keiner** auswählen, wird der Standardbericht generiert.</span><span class="sxs-lookup"><span data-stu-id="ed3da-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="ed3da-169">Wählen Sie die Sprache aus.</span><span class="sxs-lookup"><span data-stu-id="ed3da-169">Select the language.</span></span> <span data-ttu-id="ed3da-170">Alle Berichte werden in **en-us** und **ar-eg** übersetzt.</span><span class="sxs-lookup"><span data-stu-id="ed3da-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="ed3da-171">Geben Sie die Filiale und den Namen der Bank ein, bei der die Steuerzahlung erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="ed3da-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="ed3da-172">Wählen Sie den Geschäftstyp aus und geben Sie die Scheck- und Belegnummern ein.</span><span class="sxs-lookup"><span data-stu-id="ed3da-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="ed3da-173">Geben Sie den Entitätstyp ein.</span><span class="sxs-lookup"><span data-stu-id="ed3da-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="ed3da-174">Geben Sie den Namen der registrierten Person ein, um das Formular zuzuweisen, und wählen Sie **OK**, um die Berichterstellung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="ed3da-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
