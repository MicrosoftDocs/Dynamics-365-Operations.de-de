--- 
title: "Zahlungen für einen Debitor erstellen, der Direkteinzugsmandate verwendet"
description: "Dieses Verfahren zeigt das Generieren einer ISO20022-Direktbelastungsdateien für einen Debitor, bei dem eine Direktbelastung konfiguriert und eine Rechnung zu bezahlen ist."
author: mrolecki
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6e1f6fea560db0e1f96123040f80e79f5fe80886
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="2a157-103">Zahlungen für einen Debitor erstellen, der Direkteinzugsmandate verwendet</span><span class="sxs-lookup"><span data-stu-id="2a157-103">Create payments for a customer who have direct debit mandates</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2a157-104">Dieses Verfahren zeigt das Generieren einer ISO20022-Direktbelastungsdateien für einen Debitor, bei dem eine Direktbelastung konfiguriert und eine Rechnung zu bezahlen ist.</span><span class="sxs-lookup"><span data-stu-id="2a157-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="2a157-105">Eine Rechnung zu erstellen und zu Buchen ist optional.</span><span class="sxs-lookup"><span data-stu-id="2a157-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="2a157-106">Anstatt eine Rechnung zu bezahlende können Sie vor dem Generieren einer Zahlungsdatei eine Vollmacht in einer Erfassung auswählen, um ein Szenario mit Debitorenvorauszahlungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2a157-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="2a157-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DEMF.</span><span class="sxs-lookup"><span data-stu-id="2a157-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="2a157-108">Dies ist der fünfte von sechs Aufgaben, die das Verfahren für Debitorenzahlungen über elektronischen Berichterstellungskonfigurationen zeigen.</span><span class="sxs-lookup"><span data-stu-id="2a157-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="2a157-109">Damit diese Aufgabe ausgeführt werden kann, müssen zuvor alle vorherigen Aufgaben ausgeführt sein.</span><span class="sxs-lookup"><span data-stu-id="2a157-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="2a157-110">Sie müssen zuerst die elektronischen Berichtskonfigurationen der Debitorenzahlungen importieren, die Zahlungmethode konfigurieren und ihr Unternehmen und die Debitoreninformationen einrichten.</span><span class="sxs-lookup"><span data-stu-id="2a157-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="2a157-111">Freitextrechnung mit Informationen zum Direkteinzugsmandat buchen</span><span class="sxs-lookup"><span data-stu-id="2a157-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="2a157-112">Wechseln Sie zu "Debitoren" > "Rechnungen" > "Alle Freitextrechnungen".</span><span class="sxs-lookup"><span data-stu-id="2a157-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="2a157-113">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="2a157-113">Click New.</span></span>
3. <span data-ttu-id="2a157-114">Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2a157-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="2a157-115">Wählen Sie z. B. DE-010 aus.</span><span class="sxs-lookup"><span data-stu-id="2a157-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="2a157-116">Geben Sie im Feld "Zahlungsmethode" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2a157-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="2a157-117">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2a157-117">For example.</span></span> <span data-ttu-id="2a157-118">Wählen Sie "Elektronisch" aus.</span><span class="sxs-lookup"><span data-stu-id="2a157-118">select Electronic.</span></span>  
5. <span data-ttu-id="2a157-119">Geben Sie im Feld "Direkteinzugsmandats-ID" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2a157-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="2a157-120">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="2a157-120">Click Add line.</span></span>
7. <span data-ttu-id="2a157-121">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="2a157-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="2a157-122">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="2a157-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="2a157-123">Geben Sie im Feld "Preis je Einheit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="2a157-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="2a157-124">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="2a157-124">Click Post.</span></span>
11. <span data-ttu-id="2a157-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2a157-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="2a157-126">Zahlung erstellen</span><span class="sxs-lookup"><span data-stu-id="2a157-126">Create a payment</span></span>
1. <span data-ttu-id="2a157-127">Wechseln Sie zu "Debitoren" > "Zahlungen" > "Zahlungserfassung".</span><span class="sxs-lookup"><span data-stu-id="2a157-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="2a157-128">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="2a157-128">Click New.</span></span>
3. <span data-ttu-id="2a157-129">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2a157-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="2a157-130">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="2a157-130">Click Lines.</span></span>
5. <span data-ttu-id="2a157-131">Klicken Sie auf "Zahlungsvorschlag".</span><span class="sxs-lookup"><span data-stu-id="2a157-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="2a157-132">Klicken Sie auf "Zahlungsvorschlag erstellen".</span><span class="sxs-lookup"><span data-stu-id="2a157-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="2a157-133">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="2a157-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="2a157-134">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="2a157-134">Click Filter.</span></span>
9. <span data-ttu-id="2a157-135">In der Liste wählen Sie die Zeile für die Tabelle Debitorenbuchungen und das Zahlungsmethode-Feld aus.</span><span class="sxs-lookup"><span data-stu-id="2a157-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="2a157-136">Sie können alle beliebigen Kriterien zur Auswahl von Debitorenbuchungen anwenden, die gezahlt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a157-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="2a157-137">Dazu Verwenden Sie in diesem Beispiel "Elektronisch" als Zahlungsmethode, um Buchungen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="2a157-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="2a157-138">Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2a157-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="2a157-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2a157-139">Click OK.</span></span>
12. <span data-ttu-id="2a157-140">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2a157-140">Click OK.</span></span>
13. <span data-ttu-id="2a157-141">Klicken Sie auf "Zahlungen erstellen".</span><span class="sxs-lookup"><span data-stu-id="2a157-141">Click Create payments.</span></span>

## <a name="generate-a-payment-file"></a><span data-ttu-id="2a157-142">Zahlungsdatei generieren</span><span class="sxs-lookup"><span data-stu-id="2a157-142">Generate a payment file</span></span>


