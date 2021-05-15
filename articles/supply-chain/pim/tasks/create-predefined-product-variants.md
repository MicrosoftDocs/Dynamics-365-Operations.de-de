---
title: Vordefinierte Produktvarianten erstellen
description: Diese Prozedur führt Sie durch das Erstellen von Produktvarianten für einen Produktmaster mithilfe der Kombinationen von Produktdimensionen.
author: t-benebo
manager: tfehr
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acd2e3f1464dfed09ee24764270b06970b747d7c
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938201"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="eef92-103">Vordefinierte Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="eef92-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="eef92-104">Beispielszenario: Erstellen von vordefinierten Produktvarianten</span><span class="sxs-lookup"><span data-stu-id="eef92-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="eef92-105">Dieses Beispielszenario zeigt, wie Sie Produktvarianten für einen Produktstamm mit einer Kombination von Produktdimensionen erstellen.</span><span class="sxs-lookup"><span data-stu-id="eef92-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="eef92-106">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="eef92-106">Make demo data available</span></span>

<span data-ttu-id="eef92-107">Um dieses Szenario mit den hier vorgeschlagenen Werten nachzuvollziehen, müssen Sie Demodaten installiert haben und die juristische Entität *USMF* auswählen.</span><span class="sxs-lookup"><span data-stu-id="eef92-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="eef92-108">Schritt 1: Erzeugen eines Produktstamms</span><span class="sxs-lookup"><span data-stu-id="eef92-108">Step 1: Create a product master</span></span>

<span data-ttu-id="eef92-109">So erstellen Sie einen Produktstamm:</span><span class="sxs-lookup"><span data-stu-id="eef92-109">To create a product master:</span></span>

1. <span data-ttu-id="eef92-110">Wechseln Sie zu **Produktinformationsmanagement > Produkte > Produktstämme**.</span><span class="sxs-lookup"><span data-stu-id="eef92-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="eef92-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="eef92-111">Select **New**.</span></span>
1. <span data-ttu-id="eef92-112">Wenn das Feld **Produktnummer** nicht bereits eine Zahl anzeigt, geben Sie einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="eef92-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="eef92-113">Dies ist nur erforderlich, wenn keine Sequenz für dieses Feld festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="eef92-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="eef92-114">Geben Sie einen Namen in das Feld **Produktname** ein.</span><span class="sxs-lookup"><span data-stu-id="eef92-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="eef92-115">Wählen Sie im Feld **Produktdimensionsgruppe** die Produktdimensionsgruppe *SizeCol* (Größe und Farbe).</span><span class="sxs-lookup"><span data-stu-id="eef92-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="eef92-116">Wählen Sie **OK**, um den neuen Produktstamm zu erstellen und zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="eef92-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="eef92-117">Schritt 2: Produktdimensionen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="eef92-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="eef92-118">Dieses Beispiel zeigt, wie Produktdimensionenen manuell eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="eef92-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="eef92-119">Sie können auch eine Größen-, Farb- oder Stilgruppe auswählen, die die Werte für die Produktdimensionen enthält, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="eef92-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="eef92-120">So fügen Sie Produktdimensionen hinzu:</span><span class="sxs-lookup"><span data-stu-id="eef92-120">To add product dimensions:</span></span>

1. <span data-ttu-id="eef92-121">Wenn Ihr neuer Produktstamm noch geöffnet ist, wählen Sie **Produktdimensionen** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="eef92-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="eef92-122">Öffnen Sie die Registerkarte **Größe** und wählen Sie **Neu** in der Symbolleiste, um dem Raster eine Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="eef92-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="eef92-123">Legen Sie die folgenden Einstellungen für die neue Zeile fest:</span><span class="sxs-lookup"><span data-stu-id="eef92-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="eef92-124">**Größe:** Wählen Sie einen Größenwert.</span><span class="sxs-lookup"><span data-stu-id="eef92-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="eef92-125">**Name:** Geben Sie einen Namen für die Größe ein.</span><span class="sxs-lookup"><span data-stu-id="eef92-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="eef92-126">Wählen Sie **Neu** in der Symbolleiste und fügen Sie dem Raster eine zweite Größe mit einem neuen **Größe** und **Name** hinzu.</span><span class="sxs-lookup"><span data-stu-id="eef92-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="eef92-127">Öffnen Sie die Registerkarte **Farben** und wählen Sie **Neu** in der Werkzeugleiste, um dem Raster eine Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="eef92-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="eef92-128">Legen Sie die folgenden Einstellungen für die neue Zeile fest:</span><span class="sxs-lookup"><span data-stu-id="eef92-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="eef92-129">**Farbe:** Wählen Sie einen Farbwert.</span><span class="sxs-lookup"><span data-stu-id="eef92-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="eef92-130">**Name:** Geben Sie einen Namen für die Farbe ein.</span><span class="sxs-lookup"><span data-stu-id="eef92-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="eef92-131">Wählen Sie **Neu** in der Symbolleiste und fügen Sie dem Raster eine zweite Farbe mit einer neuen **Farbe** und **Name** hinzu.</span><span class="sxs-lookup"><span data-stu-id="eef92-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="eef92-132">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="eef92-132">Select **Save**.</span></span>
1. <span data-ttu-id="eef92-133">Schließen Sie die Seite, um zu Ihrem neuen Produktstamm zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="eef92-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="eef92-134">Schritt 3: Produktvarianten generieren</span><span class="sxs-lookup"><span data-stu-id="eef92-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="eef92-135">Dieser Abschnitt beschreibt, wie Produktvarianten generiert werden können, wenn die Funktion *Variantenvorschläge Seitenverbesserungen* nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="eef92-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="eef92-136">Im nächsten Abschnitt erfahren Sie, wie Sie Produktvarianten erzeugen, wenn diese Funktion verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="eef92-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="eef92-137">Um Produktvarianten zu generieren:</span><span class="sxs-lookup"><span data-stu-id="eef92-137">To generate product variants:</span></span>

1. <span data-ttu-id="eef92-138">Wenn Ihr neuer Produktstamm noch geöffnet ist, wählen Sie **Produktvarianten** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="eef92-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="eef92-139">Wählen Sie **Variantenvorschläge** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="eef92-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="eef92-140">Das System generiert eine Liste mit allen möglichen Kombinationen der Größen und Farben, die Sie für das Produkt definiert haben.</span><span class="sxs-lookup"><span data-stu-id="eef92-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="eef92-141">Wählen Sie **Alles auswählen** in der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="eef92-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="eef92-142">Wählen Sie in diesem Beispiel alle möglichen Varianten aus.</span><span class="sxs-lookup"><span data-stu-id="eef92-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="eef92-143">Wenn Sie nur eine Teilmenge der möglichen Kombinationen von Produktdimensionen verwenden möchten, aktivieren Sie bei Bedarf nur die erforderlichen Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="eef92-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="eef92-144">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="eef92-144">Select **Create**.</span></span>
1. <span data-ttu-id="eef92-145">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="eef92-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="eef92-146">Verbesserte Variantenvorschläge</span><span class="sxs-lookup"><span data-stu-id="eef92-146">Improved variant suggestions</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="eef92-147">Die Funktion *Verbesserungen auf der Seite für Variantenvorschläge* verbessert die Seite **Variant suggestions**, um Probleme mit der Leistung und der Benutzerfreundlichkeit für Firmen zu beheben, die eine hohe Anzahl von Produktdimensions-Kombinationen haben.</span><span class="sxs-lookup"><span data-stu-id="eef92-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="eef92-148">Der verbesserte Prozess zur Auswahl der Werte für die Produktdimensionen, für die Variantenvorschläge generiert werden sollen, macht es schneller und einfacher, den relevanten Satz von Produktvarianten festzulegen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="eef92-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="eef92-149">Die folgenden Verbesserungen werden durch diese Funktion hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="eef92-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="eef92-150">**Aufgeschobene Generierung von Variantenvorschlägen:** Die Seite **Variantenvorschläge** zeigt keine Vorschläge mehr an, wenn Sie sie zum ersten Mal öffnen.</span><span class="sxs-lookup"><span data-stu-id="eef92-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="eef92-151">Stattdessen müssen Sie explizit auswählen, welche Werte Sie benötigen und dann die Schaltfläche **Vorschlagen** wählen, um die Kombinationen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="eef92-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="eef92-152">Dadurch wird der Prozess sichtbarer und interaktiver.</span><span class="sxs-lookup"><span data-stu-id="eef92-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="eef92-153">**Auswahl von Dimensions-Werten:** Wenn Sie viele Dimensions-Werte haben, sind Sie typischerweise daran interessiert, Variantenvorschläge zu generieren, die nur einige von ihnen enthalten (z. B. bei der Einführung eines neuen Satzes von Farben oder Stilen).</span><span class="sxs-lookup"><span data-stu-id="eef92-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="eef92-154">Mit dem verbesserten Design können Sie die Dimensionswerte auswählen, für die Sie Produktvariantenvorschläge generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="eef92-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="eef92-155">Dies erhöht die Relevanz der vorgeschlagenen Varianten erheblich und verbessert sowohl die Systemleistung als auch die Benutzerproduktivität.</span><span class="sxs-lookup"><span data-stu-id="eef92-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="eef92-156">Schalten Sie die Funktion Variantenvorschläge Seitenverbesserungen ein</span><span class="sxs-lookup"><span data-stu-id="eef92-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="eef92-157">Bevor Sie die Funktion *Variantenvorschläge Seitenverbesserungen* verwenden können, muss sie in Ihrem System eingeschaltet sein.</span><span class="sxs-lookup"><span data-stu-id="eef92-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="eef92-158">Administratoren können mit den Einstellungen [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="eef92-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="eef92-159">Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="eef92-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="eef92-160">**Modul:** *Produktinformationsverwaltung*</span><span class="sxs-lookup"><span data-stu-id="eef92-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="eef92-161">**Funktionsname:** *Variantenvorschläge Seite Verbesserungen*</span><span class="sxs-lookup"><span data-stu-id="eef92-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="eef92-162">Arbeit mit den verbesserten Variantenvorschlägen</span><span class="sxs-lookup"><span data-stu-id="eef92-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="eef92-163">So generieren Sie Produktvariantenvorschläge, wenn die Funktion *Variantenvorschläge Seitenverbesserungen* aktiviert ist:</span><span class="sxs-lookup"><span data-stu-id="eef92-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="eef92-164">Öffnen oder erstellen Sie einen Produktstamm und fügen Sie ihm die erforderlichen Produktdimensionen hinzu, wie im vorherigen Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="eef92-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="eef92-165">Wählen Sie bei geöffnetem Produktstamm **Produktvarianten** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="eef92-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="eef92-166">Wählen Sie **Variantenvorschläge** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="eef92-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="eef92-167">Wählen Sie die Werte aus, die Sie für die einzelnen Dimensionen verwenden wollen.</span><span class="sxs-lookup"><span data-stu-id="eef92-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="eef92-168">Wählen Sie in der oberen Symbolleiste **Vorschlagen**.</span><span class="sxs-lookup"><span data-stu-id="eef92-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="eef92-169">Das System generiert eine Liste mit allen möglichen Kombinationen der von Ihnen gewählten Größen und Farben.</span><span class="sxs-lookup"><span data-stu-id="eef92-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="eef92-170">Aktivieren Sie im Inforegister **Vorgeschlagene Varianten** das Kontrollkästchen für jede Produktdimensions-Kombination, die Sie verwenden möchten, oder wählen Sie **Alle auswählen** in der Symbolleiste, um alle auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="eef92-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="eef92-171">Wählen Sie **Erstellen**, um die Varianten zum aktuellen Produktstamm hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="eef92-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
