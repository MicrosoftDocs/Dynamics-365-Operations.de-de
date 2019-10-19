---
title: Einrichten und Verarbeiten von Serienrechnungen
description: In diesem Artikel wird beschrieben, wie Serienrechnungen eingerichtet und verarbeitet werden. Sie können Serienrechnungen verwenden, wenn Sie Debitoren regelmäßig für den gleichen Betrag eine Rechnung stellen müssen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b443630d1612b5095fefa74b5ed6d057be534b7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188946"
---
# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="ed98e-104">Einrichten und Verarbeiten von Serienrechnungen</span><span class="sxs-lookup"><span data-stu-id="ed98e-104">Set up and process recurring invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed98e-105">In diesem Artikel wird beschrieben, wie Serienrechnungen eingerichtet und verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ed98e-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="ed98e-106">Sie können Serienrechnungen verwenden, wenn Sie Debitoren regelmäßig für den gleichen Betrag eine Rechnung stellen müssen.</span><span class="sxs-lookup"><span data-stu-id="ed98e-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

<a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="ed98e-107">Erstellen einer Vorlage für Freitext-Serienrechnungen</span><span class="sxs-lookup"><span data-stu-id="ed98e-107">Create a recurring free text invoice template</span></span>
---------------------------------------------

<span data-ttu-id="ed98e-108">Um Debitoren regelmäßig dieselben Dienstleistungen in Rechnung zu stellen, müssen Sie eine Freitext-Rechnungsvorlage definieren, die immer wieder zum Ausstellen der Rechnungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ed98e-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="ed98e-109">Diese Vorlage enthält folgende Informationen:</span><span class="sxs-lookup"><span data-stu-id="ed98e-109">This template contains the following information:</span></span>

-   <span data-ttu-id="ed98e-110">Kopfzeileninformationen, wie Steuergruppen, Zahlungsbedingungen und Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="ed98e-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="ed98e-111">Positionsinformationen, wie eine Beschreibung der Dienstleistung, Umsatzerlöskonten, Preis je Einheit und Rechnungsbetrag</span><span class="sxs-lookup"><span data-stu-id="ed98e-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="ed98e-112">Zuschläge für Versand- oder Bearbeitungskosten</span><span class="sxs-lookup"><span data-stu-id="ed98e-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="ed98e-113">Buchhaltungsverteilungen zusammen mit Finanzdimensionsinformationen, wie Kostenstellen und Unternehmenseinheiten</span><span class="sxs-lookup"><span data-stu-id="ed98e-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="ed98e-114">Im Prinzip erstellen Sie eine komplette Rechnung und speichern diese als Vorlage.</span><span class="sxs-lookup"><span data-stu-id="ed98e-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="ed98e-115">Sie können die Vorlagen unter Verwendung der Seite **Serienrechnungen** einrichten.</span><span class="sxs-lookup"><span data-stu-id="ed98e-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="ed98e-116">Zuweisen einer Freitextrechnungsvorlage zu einem Debitor und Eingabe von Seriendetails</span><span class="sxs-lookup"><span data-stu-id="ed98e-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="ed98e-117">Nachdem die Vorlage erstellt wurde, müssen Sie die Vorlage den Debitoren zuordnen, für die Rechnungen erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ed98e-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="ed98e-118">Darüber hinaus müssen Sie angeben, wann und wie häufig die Rechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed98e-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="ed98e-119">Sie können die Vorlagen auf der Registerkarte **Rechnung** der Seite **Debitoren** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="ed98e-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="ed98e-120">Fügen Sie die Vorlage der Liste hinzu, und aktualisieren Sie die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="ed98e-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="ed98e-121">Das Startdatum und (optional) das Enddatum für die Serienrechnung</span><span class="sxs-lookup"><span data-stu-id="ed98e-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="ed98e-122">Die Häufigkeit der Serienrechnung (beispielsweise täglich oder einmal im Monat)</span><span class="sxs-lookup"><span data-stu-id="ed98e-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="ed98e-123">Den maximalen Abrechnungsbetrag (wenn diese Angabe erforderlich ist)</span><span class="sxs-lookup"><span data-stu-id="ed98e-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="ed98e-124">Für einen Debitor können mehrere Vorlagen mit unterschiedlichen Zahlungshäufigkeiten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ed98e-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="ed98e-125">Generieren der Serienrechnungen</span><span class="sxs-lookup"><span data-stu-id="ed98e-125">Generate the recurring invoices</span></span>
<span data-ttu-id="ed98e-126">Auf der Seite **Serienrechnungen**gibt es eine Aufgabe zum Verarbeiten von Serienrechnungsvorlagen.</span><span class="sxs-lookup"><span data-stu-id="ed98e-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="ed98e-127">Sie geben das Rechnungsdatum und die Vorlage zum Generieren der Rechnungen an.</span><span class="sxs-lookup"><span data-stu-id="ed98e-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="ed98e-128">Die Rechnungen werden generiert, und jeder Gruppe von verarbeiteten Rechnungen wird eine individuelle Serienkennung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ed98e-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>

<a name="post-recurring-free-text-invoices"></a><span data-ttu-id="ed98e-129">Buchen von Freitext-Serienrechnungen</span><span class="sxs-lookup"><span data-stu-id="ed98e-129">Post recurring free text invoices</span></span>
---------------------------------

<span data-ttu-id="ed98e-130">Nachdem Serienrechnungen generiert wurden, werden die Serienkennungen in einer Buchungsaufgabe auf der Seite **Serienrechnungen**angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed98e-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="ed98e-131">Sie können alle Rechnungen für eine Serienkennung anzeigen, indem Sie auf den Link klicken.</span><span class="sxs-lookup"><span data-stu-id="ed98e-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="ed98e-132">Beim Überprüfen der Rechnungen für eine Serienkennung können Sie einzelne Rechnungen löschen.</span><span class="sxs-lookup"><span data-stu-id="ed98e-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="ed98e-133">Die Wiederholungseinstellungen für den Debitor werden für diese Vorlage zurückgesetzt und können später neu generiert werden.</span><span class="sxs-lookup"><span data-stu-id="ed98e-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="ed98e-134">Sie können eine, mehrere oder alle Rechnungen für eine Serienkennung buchen.</span><span class="sxs-lookup"><span data-stu-id="ed98e-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="ed98e-135">Wenn Workflows aktiviert sind, müssen Sie auf **Senden** klicken, bevor Sie die Rechnungen buchen können.</span><span class="sxs-lookup"><span data-stu-id="ed98e-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>

<a name="print-recurring-free-text-invoices"></a><span data-ttu-id="ed98e-136">Drucken von Freitext-Serienrechnungen</span><span class="sxs-lookup"><span data-stu-id="ed98e-136">Print recurring free text invoices</span></span>
----------------------------------

<span data-ttu-id="ed98e-137">Nach dem Buchen von Serienrechnungen können Sie die Rechnungen auf der Seite mit der Liste mit Freitextrechnungen drucken.</span><span class="sxs-lookup"><span data-stu-id="ed98e-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="ed98e-138">Sie können die ausgewählten Rechnungen drucken oder einen Bereich von Rechnungen auswählen und drucken.</span><span class="sxs-lookup"><span data-stu-id="ed98e-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>



