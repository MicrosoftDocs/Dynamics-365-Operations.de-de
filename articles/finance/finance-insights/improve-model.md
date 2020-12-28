---
title: Vorhersagemodell verbessern (Vorschau)
description: In diesem Thema werden Funktionen beschrieben, mit denen Sie die Leistung von Vorhersagemodellen verbessern können.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 23c9062dcc13951792306c955b54cae6f656fec5
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646078"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="bb9b3-103">Vorhersagemodell verbessern (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="bb9b3-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="bb9b3-104">In diesem Thema werden Funktionen beschrieben, mit denen Sie die Leistung von Vorhersagemodellen verbessern können.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="bb9b3-105">Sie beginnen Ihr Modell im **Zahlungsvorhersagen für Debitoren**-Arbeitsbereich in Microsoft Dynamics 365 Finance zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="bb9b3-106">Die Verbesserungsschritte werden dann in AI Builder abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="bb9b3-107">Historische Ergebnisse auswählen</span><span class="sxs-lookup"><span data-stu-id="bb9b3-107">Select historical outcomes</span></span>

<span data-ttu-id="bb9b3-108">Sie wählen zunächst eines oder mehrere der drei möglichen Ergebnisse für Rechnungen aus: **Pünktlich**, **Verspätet** und **Sehr spät**.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="bb9b3-109">Alle drei Ergebnisse sollten ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-109">All three outcomes should be selected.</span></span> <span data-ttu-id="bb9b3-110">Wenn Sie die Auswahl eines der Ergebnisse deaktivieren, werden Rechnungen aus dem Trainingsprozess herausgefiltert und die Genauigkeit der Vorhersage wird verringert.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="bb9b3-111">[![Ergebnisse bestätigen](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="bb9b3-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="bb9b3-112">Wenn Ihre Organisation nur zwei Ergebnisse benötigt, ändern Sie die **Verspätet**- und **Sehr spät**-Schwellenwerte auf 0 (Null) Tage.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="bb9b3-113">Auf diese Weise reduzieren Sie die Vorhersage effektiv auf einen binären Zustand von **Pünktlich** oder **Verspätet**.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="bb9b3-114">Felder auswählen</span><span class="sxs-lookup"><span data-stu-id="bb9b3-114">Select fields</span></span>

<span data-ttu-id="bb9b3-115">Beachten Sie bei der Auswahl von Feldern, die in das Modell aufgenommen werden sollen, dass die Liste alle verfügbaren Felder in der Common Data Service-Entität enthält, die den Daten im Azure-Data Lake zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Common Data Service entity that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="bb9b3-116">Einige dieser Felder sollten **nicht** ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="bb9b3-117">Die Felder, die nicht ausgewählt werden sollten, fallen in eine von drei Kategorien:</span><span class="sxs-lookup"><span data-stu-id="bb9b3-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="bb9b3-118">Das Feld wird für die Common Data Service-Entität benötigt, aber es gibt keine Sicherungsdaten dafür im Data Lake.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-118">The field is required for the Common Data Service entity, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="bb9b3-119">Das Feld ist eine ID und daher für eine Machine-Learning-Funktion nicht sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="bb9b3-120">Das Feld stellt Informationen dar, die während der Vorhersage nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="bb9b3-121">In den folgenden Abschnitten werden die Felder angezeigt, die für die Rechnungs- und Kundenentitäten verfügbar sind, und es werden die Felder aufgelistet, die werden **nicht** für das Training ausgewählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="bb9b3-122">Die Kategorie, die für jedes dieser Felder angegeben ist, bezieht sich auf die Kategorien in der vorhergehenden Liste.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-common-data-model-entity"></a><span data-ttu-id="bb9b3-123">Common Data Model-Rechnungsentität</span><span class="sxs-lookup"><span data-stu-id="bb9b3-123">Invoice Common Data Model entity</span></span>

<span data-ttu-id="bb9b3-124">Die folgende Abbildung zeigt die Felder an, die für die Rechnungsentität verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-124">The following illustration shows the fields that are available for the invoice entity.</span></span>

<span data-ttu-id="bb9b3-125">[![Verfügbare Felder für die Rechnungsentität](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="bb9b3-125">[![Available fields for the invoice entity](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="bb9b3-126">Die folgenden Felder sollten nicht für das Training ausgewählt werden:</span><span class="sxs-lookup"><span data-stu-id="bb9b3-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="bb9b3-127">**Rechnungskonto** (Kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="bb9b3-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="bb9b3-128">**Ist geschlossen** (Kategorie 3) – In diesem Feld werden Rechnungen für Training (geschlossen) und Vorhersage (nicht geschlossen) gefiltert.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="bb9b3-129">**Name** (Kategorie 1)</span><span class="sxs-lookup"><span data-stu-id="bb9b3-129">**Name** (category 1)</span></span>
- <span data-ttu-id="bb9b3-130">**Quell-ID** (Kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="bb9b3-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="bb9b3-131">**Quelldatensatz** (Kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="bb9b3-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="bb9b3-132">**Quelltabelle** (Kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="bb9b3-132">**Source table** (category 2)</span></span>

### <a name="customer-common-data-model-entity"></a><span data-ttu-id="bb9b3-133">Common Data Model-Debitorenentität</span><span class="sxs-lookup"><span data-stu-id="bb9b3-133">Customer Common Data Model entity</span></span>

<span data-ttu-id="bb9b3-134">Die folgende Abbildung zeigt die Felder an, die für die Debitorenentität verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-134">The following illustration shows the fields that are available for the customer entity.</span></span>

<span data-ttu-id="bb9b3-135">[![Verfügbare Felder für die Debitorenentität](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="bb9b3-135">[![Available fields for the customer entity](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="bb9b3-136">Das folgende Feld sollte nicht für das Training ausgewählt werden:</span><span class="sxs-lookup"><span data-stu-id="bb9b3-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="bb9b3-137">**Eindeutiger Zeilenschlüssel** (Kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="bb9b3-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="bb9b3-138">Filter</span><span class="sxs-lookup"><span data-stu-id="bb9b3-138">Filters</span></span>

<span data-ttu-id="bb9b3-139">Die Filter unterstützen derzeit das Szenario des Debitorenzahlungsprädiktors nicht.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="bb9b3-140">Wählen Sie daher **Diesen Schritt überspringen** aus und fahren Sie mit der Übersichtsseite fort.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="bb9b3-141">[![Fokusmodell mit Filtern](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="bb9b3-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="bb9b3-142">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="bb9b3-142">Privacy notice</span></span>
<span data-ttu-id="bb9b3-143">Vorschauen (1) wenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen an als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement (SLA) für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
