---
title: Verweise auf Originalrechnungen in Gutschriften
description: In diesem Thema wird erläutert, wie Sie die ursprünglichen Rechnungsnummern in zugehörigen Gutschriften einrichten und ausdrucken.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 04a4fc96cb7de60052b17e36c33ad5d5be322be4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207350"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="3dd07-103">Verweise auf Originalrechnungen in Gutschriften</span><span class="sxs-lookup"><span data-stu-id="3dd07-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="3dd07-104">In einigen Ländern und Regionen ist es gesetzlich vorgeschrieben, dass gedruckte Gutschriften Verweise auf die Originalrechnungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="3dd07-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="3dd07-105">In diesem Thema wird erläutert, wie Sie die ursprünglichen Rechnungsnummern in zugehörigen Gutschriften einrichten und ausdrucken.</span><span class="sxs-lookup"><span data-stu-id="3dd07-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3dd07-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3dd07-106">Prerequisites</span></span>

- <span data-ttu-id="3dd07-107">Aktivieren Sie im **Funktionsverwaltung**-Arbeitsbereich die Funktion **Layout für die Fakturierung von Gutschriften auf Verkaufs- und Projektrechnungsberichte**.</span><span class="sxs-lookup"><span data-stu-id="3dd07-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="3dd07-108">Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3dd07-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="3dd07-109">Die druckbaren Formate der erforderlichen Dokumente müssen in der Druckverwaltung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="3dd07-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="3dd07-110">Die in diesem Thema beschriebene Funktionalität gilt für die folgenden Dokumente:</span><span class="sxs-lookup"><span data-stu-id="3dd07-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="3dd07-111">**Debitorenkonten**</span><span class="sxs-lookup"><span data-stu-id="3dd07-111">**Accounts receivable**</span></span>

- <span data-ttu-id="3dd07-112">Freitext-Gutschrift</span><span class="sxs-lookup"><span data-stu-id="3dd07-112">Free text credit note</span></span>
- <span data-ttu-id="3dd07-113">Debitorengutschrift</span><span class="sxs-lookup"><span data-stu-id="3dd07-113">Customer credit note</span></span>

<span data-ttu-id="3dd07-114">**Projektverwaltung und Buchhaltung**</span><span class="sxs-lookup"><span data-stu-id="3dd07-114">**Project management and accounting**</span></span>

- <span data-ttu-id="3dd07-115">Projektgutschrift</span><span class="sxs-lookup"><span data-stu-id="3dd07-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="3dd07-116">Debitorenparameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="3dd07-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="3dd07-117">Befolgen Sie diese Schritte, um den Parameter festzulegen, der steuert, ob Verweise auf die Originalrechnungen in zugehörigen Gutschriften gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="3dd07-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="3dd07-118">Gehen Sie zu **Debitoren** \> **Einrichtung** \> **Debitorenparameter**.</span><span class="sxs-lookup"><span data-stu-id="3dd07-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="3dd07-119">Auf der **Updates**-Registerkarte auf im Inforegister **Rechnung** stellen Sie die Option **Das Layout für die Fakturierung von Gutschriften auf Verkaufs- und Projektrechnungsberichte anwenden** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3dd07-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![Konfigurieren von Debitorenparametern](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="3dd07-121">Verweise auf Originalrechnungen definieren</span><span class="sxs-lookup"><span data-stu-id="3dd07-121">Define references to original invoices</span></span>

<span data-ttu-id="3dd07-122">Verwenden Sie die folgenden Verfahren, um Verweise auf Originalrechnungen basierend auf dem Dokumenttyp zu definieren.</span><span class="sxs-lookup"><span data-stu-id="3dd07-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="3dd07-123">Freitext-Gutschrift</span><span class="sxs-lookup"><span data-stu-id="3dd07-123">Free text credit note</span></span>

1. <span data-ttu-id="3dd07-124">Wechseln Sie zu **Debitoren** \> **Rechnungen** \> **Alle Freitextrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="3dd07-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="3dd07-125">Erstellen Sie eine neue Gutschrift oder wählen Sie eine vorhandene Gutschrift aus.</span><span class="sxs-lookup"><span data-stu-id="3dd07-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="3dd07-126">Öffnen Sie die Rechnung.</span><span class="sxs-lookup"><span data-stu-id="3dd07-126">Open the invoice.</span></span>
4. <span data-ttu-id="3dd07-127">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Funktionen** **Fakturierung von Gutschriften** aus.</span><span class="sxs-lookup"><span data-stu-id="3dd07-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="3dd07-128">Geben Sie den Verweis auf die Originalrechnung ein und wählen Sie den Grund für die Korrektur aus.</span><span class="sxs-lookup"><span data-stu-id="3dd07-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![Definieren des Verweises für eine Freitextrechnung](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="3dd07-130">Debitorengutschrift</span><span class="sxs-lookup"><span data-stu-id="3dd07-130">Customer credit note</span></span>

1. <span data-ttu-id="3dd07-131">Wechseln Sie zu **Debitoren** \> **Aufträge** \> **Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="3dd07-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="3dd07-132">Wählen Sie den in Rechnung gestellten zu korrigierenden Auftrag aus und öffnen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="3dd07-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="3dd07-133">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Verkaufen** in der Gruppe **Gutschrift** die Option **Gutschrift**.</span><span class="sxs-lookup"><span data-stu-id="3dd07-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="3dd07-134">Geben Sie hier die Ursache für die Korrektur ein.</span><span class="sxs-lookup"><span data-stu-id="3dd07-134">Enter the reason for the correction.</span></span> <span data-ttu-id="3dd07-135">Der Verweis auf die Originalrechnung wird automatisch hergestellt.</span><span class="sxs-lookup"><span data-stu-id="3dd07-135">The reference to the original invoice is automatically established.</span></span>

![Definieren des Verweises für einen Auftrag](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="3dd07-137">Projektgutschrift</span><span class="sxs-lookup"><span data-stu-id="3dd07-137">Project credit note</span></span>

1. <span data-ttu-id="3dd07-138">Wechseln Sie zu **Projektverwaltung und -verrechnung** \> **Projektrechnungen** \> **Projektrechnung**.</span><span class="sxs-lookup"><span data-stu-id="3dd07-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="3dd07-139">Wählen Sie die zu korrigierende Projektrechnung aus und öffnen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="3dd07-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="3dd07-140">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Projektrechnung** in der Gruppe **Funktionen** **Für Gutschrift auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="3dd07-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="3dd07-141">Wählen Sie **Gutschriftenfakturierung** aus.</span><span class="sxs-lookup"><span data-stu-id="3dd07-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="3dd07-142">Geben Sie hier die Ursache für die Korrektur ein.</span><span class="sxs-lookup"><span data-stu-id="3dd07-142">Enter the reason for the correction.</span></span> <span data-ttu-id="3dd07-143">Der Verweis auf die Originalrechnung wird automatisch hergestellt.</span><span class="sxs-lookup"><span data-stu-id="3dd07-143">The reference to the original invoice is automatically established.</span></span>

![Definieren des Verweises für eine Projektrechnung](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="3dd07-145">Drucken von Gutschriften</span><span class="sxs-lookup"><span data-stu-id="3dd07-145">Printing credit notes</span></span>

<span data-ttu-id="3dd07-146">Wenn Sie Freitext-, Kunden- und Projektgutschriften drucken, enthalten diese den Verweis auf die Originalrechnung und den Korrekturgrund.</span><span class="sxs-lookup"><span data-stu-id="3dd07-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Gedruckte Gutschrift](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="3dd07-148">Stellen Sie, davon ausgehend, dass Verweise auf Originalrechnungen gedruckt werden, sicher, dass die druckbaren Formate der Dokumente korrekt konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="3dd07-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]