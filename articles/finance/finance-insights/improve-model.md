---
title: Vorhersagemodell verbessern (Vorschau)
description: In diesem Thema werden Funktionen beschrieben, mit denen Sie die Leistung von Vorhersagemodellen verbessern können.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186641"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="ce8ce-103">Vorhersagemodell verbessern (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="ce8ce-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ce8ce-104">In diesem Thema werden Funktionen beschrieben, mit denen Sie die Leistung von Vorhersagemodellen verbessern können.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="ce8ce-105">Sie beginnen Ihr Modell im **Zahlungsvorhersagen für Debitoren**-Arbeitsbereich in Microsoft Dynamics 365 Finance zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="ce8ce-106">Die Verbesserungsschritte werden dann in AI Builder abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="ce8ce-107">Historische Ergebnisse auswählen</span><span class="sxs-lookup"><span data-stu-id="ce8ce-107">Select historical outcomes</span></span>

<span data-ttu-id="ce8ce-108">Sie wählen zunächst eines oder mehrere der drei möglichen Ergebnisse für Rechnungen aus: **Pünktlich**, **Verspätet** und **Sehr spät**.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="ce8ce-109">Alle drei Ergebnisse sollten ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-109">All three outcomes should be selected.</span></span> <span data-ttu-id="ce8ce-110">Wenn Sie die Auswahl eines der Ergebnisse deaktivieren, werden Rechnungen aus dem Trainingsprozess herausgefiltert und die Genauigkeit der Vorhersage wird verringert.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="ce8ce-111">[![Ergebnisse bestätigen](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="ce8ce-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="ce8ce-112">Wenn Ihre Organisation nur zwei Ergebnisse benötigt, ändern Sie die **Verspätet**- und **Sehr spät**-Schwellenwerte auf 0 (Null) Tage.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="ce8ce-113">Auf diese Weise reduzieren Sie die Vorhersage effektiv auf einen binären Zustand von **Pünktlich** oder **Verspätet**.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="ce8ce-114">Felder auswählen</span><span class="sxs-lookup"><span data-stu-id="ce8ce-114">Select fields</span></span>

<span data-ttu-id="ce8ce-115">Beachten Sie bei der Auswahl von Feldern, die in das Modell aufgenommen werden sollen, dass die Liste alle verfügbaren Felder in der Microsoft Dataverse-Tabelle enthält, die den Daten im Azure-Data Lake zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="ce8ce-116">Einige dieser Felder sollten **nicht** ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="ce8ce-117">Die Felder, die nicht ausgewählt werden sollten, fallen in eine von drei Kategorien:</span><span class="sxs-lookup"><span data-stu-id="ce8ce-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="ce8ce-118">Das Feld wird für die Dataverse-Tabelle benötigt, aber es gibt keine Sicherungsdaten dafür im Data Lake.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="ce8ce-119">Das Feld ist eine ID und daher für eine Machine-Learning-Funktion nicht sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="ce8ce-120">Das Feld stellt Informationen dar, die während der Vorhersage nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="ce8ce-121">In den folgenden Abschnitten werden die Felder angezeigt, die für die Rechnungs- und Kundenentitäten verfügbar sind, und es werden die Felder aufgelistet, die werden **nicht** für das Training ausgewählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="ce8ce-122">Die Kategorie, die für jedes dieser Felder angegeben ist, bezieht sich auf die Kategorien in der vorhergehenden Liste.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="ce8ce-123">Rechnungs-Dataverse-Tabelle</span><span class="sxs-lookup"><span data-stu-id="ce8ce-123">Invoice Dataverse table</span></span>

<span data-ttu-id="ce8ce-124">Die folgende Abbildung zeigt die Felder an, die für die Rechnungstabelle verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="ce8ce-125">[![Verfügbare Felder für die Rechnungstabelle](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="ce8ce-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="ce8ce-126">Die folgenden Felder sollten nicht für das Training ausgewählt werden:</span><span class="sxs-lookup"><span data-stu-id="ce8ce-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="ce8ce-127">**Rechnungskonto** (Kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="ce8ce-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="ce8ce-128">**Ist geschlossen** (Kategorie 3) – In diesem Feld werden Rechnungen für Training (geschlossen) und Vorhersage (nicht geschlossen) gefiltert.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="ce8ce-129">**Name** (Kategorie 1)</span><span class="sxs-lookup"><span data-stu-id="ce8ce-129">**Name** (category 1)</span></span>
- <span data-ttu-id="ce8ce-130">**Quell-ID** (Kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="ce8ce-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="ce8ce-131">**Quelldatensatz** (Kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="ce8ce-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="ce8ce-132">**Quelltabelle** (Kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="ce8ce-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="ce8ce-133">Debitoren-Dataverse-Tabelle</span><span class="sxs-lookup"><span data-stu-id="ce8ce-133">Customer Dataverse table</span></span>

<span data-ttu-id="ce8ce-134">Die folgende Abbildung zeigt die Felder an, die für die Debitorentabelle verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="ce8ce-135">[![Verfügbare Felder für die Debitorentabelle](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="ce8ce-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="ce8ce-136">Das folgende Feld sollte nicht für das Training ausgewählt werden:</span><span class="sxs-lookup"><span data-stu-id="ce8ce-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="ce8ce-137">**Eindeutiger Zeilenschlüssel** (Kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="ce8ce-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="ce8ce-138">Filter</span><span class="sxs-lookup"><span data-stu-id="ce8ce-138">Filters</span></span>

<span data-ttu-id="ce8ce-139">Die Filter unterstützen derzeit das Szenario des Debitorenzahlungsprädiktors nicht.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="ce8ce-140">Wählen Sie daher **Diesen Schritt überspringen** aus und fahren Sie mit der Übersichtsseite fort.</span><span class="sxs-lookup"><span data-stu-id="ce8ce-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="ce8ce-141">[![Fokusmodell mit Filtern](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="ce8ce-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
