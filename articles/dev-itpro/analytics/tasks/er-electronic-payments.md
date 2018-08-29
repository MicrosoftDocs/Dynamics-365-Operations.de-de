--- 
title: "Elektronische Dokumente für Zahlungen mithilfe von Formatkonfigurationen generieren"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle \"Entwickler für elektronische Berichterstellung\" angehört, eine neue Formatkonfiguration für elektronische Berichterstellung (ER) verwenden kann, um elektronische Dokumente zur Verarbeitung von Zahlungen zu generieren."
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 805e6f377d452e9c50240c8c9fc2ea6f5cb487e6
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="generate-electronic-documents-for-payments-by-using-format-configurations"></a><span data-ttu-id="d0136-103">Elektronische Dokumente für Zahlungen mithilfe von Formatkonfigurationen generieren</span><span class="sxs-lookup"><span data-stu-id="d0136-103">Generate electronic documents for payments by using format configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d0136-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine neue Formatkonfiguration für elektronische Berichterstellung (ER) verwenden kann, um elektronische Dokumente zur Verarbeitung von Zahlungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d0136-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="d0136-105">Diese Schritte können im GBSI-Beispielunternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d0136-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="d0136-106">Um diese Schritte abzuschließen, müssen Sie zunächst die Schritte in der Prozedur "Eine Konfiguration mit Zahlungsformatdokument erstellen" abschließen.</span><span class="sxs-lookup"><span data-stu-id="d0136-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="d0136-107">Ändern Sie die Konfiguration der Methode der elektronischen Zahlung</span><span class="sxs-lookup"><span data-stu-id="d0136-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="d0136-108">Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".</span><span class="sxs-lookup"><span data-stu-id="d0136-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="d0136-109">Schalten Sie den Abschnitt "Dateiformat" um, um ihn bei Bedarf zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="d0136-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="d0136-110">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="d0136-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d0136-111">Filtern Sie beispielsweise nach dem Feld "Zahlungsmethode" mit einem Wert von "Elektronisch".</span><span class="sxs-lookup"><span data-stu-id="d0136-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="d0136-112">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="d0136-112">Click Edit.</span></span>
5. <span data-ttu-id="d0136-113">Legen Sie das Feld "Allgemeine elektronische Berichterstellung" auf "Ja" fest.</span><span class="sxs-lookup"><span data-stu-id="d0136-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="d0136-114">Wählen Sie "Ja" aus, um das "Allgemeine elektronische Berichterstellungsmuster" für die Zahlungsdateigenerierung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d0136-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="d0136-115">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d0136-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d0136-116">Wählen Sie die Formatkonfiguration BACS (Großbritannien, fiktiv) aus.</span><span class="sxs-lookup"><span data-stu-id="d0136-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="d0136-117">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d0136-117">Click Save.</span></span>
9. <span data-ttu-id="d0136-118">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d0136-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="d0136-119">Testen Sie das Format von generierten Zahlungsdateien</span><span class="sxs-lookup"><span data-stu-id="d0136-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="d0136-120">Wechseln Sie zu "Kreditoren" > "Zahlungen" > "Zahlungserfassung".</span><span class="sxs-lookup"><span data-stu-id="d0136-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="d0136-121">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d0136-121">Click New.</span></span>
3. <span data-ttu-id="d0136-122">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="d0136-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d0136-123">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d0136-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d0136-124">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d0136-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d0136-125">Wählen Sie "VendPay" aus.</span><span class="sxs-lookup"><span data-stu-id="d0136-125">Select VendPay.</span></span>  
6. <span data-ttu-id="d0136-126">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d0136-126">Click Save.</span></span>
7. <span data-ttu-id="d0136-127">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="d0136-127">Click Lines.</span></span>
8. <span data-ttu-id="d0136-128">Geben Sie im Feld "Unternehmen" die Zeichenfolge "DEMF" ein.</span><span class="sxs-lookup"><span data-stu-id="d0136-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="d0136-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="d0136-129">DEMF</span></span>  
9. <span data-ttu-id="d0136-130">Geben Sie im Feld "Konto" die Werte "De-01001" an.</span><span class="sxs-lookup"><span data-stu-id="d0136-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="d0136-131">DE- 01001</span><span class="sxs-lookup"><span data-stu-id="d0136-131">DE-01001</span></span>  
10. <span data-ttu-id="d0136-132">Geben Sie im Feld "Beschreibung" die Bezeichnung "Zahlung" ein.</span><span class="sxs-lookup"><span data-stu-id="d0136-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="d0136-133">Zahlung</span><span class="sxs-lookup"><span data-stu-id="d0136-133">Payment</span></span>  
11. <span data-ttu-id="d0136-134">Geben Sie im Feld "Soll" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d0136-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="d0136-135">1.000</span><span class="sxs-lookup"><span data-stu-id="d0136-135">1000</span></span>  
12. <span data-ttu-id="d0136-136">Klicken Sie auf die Registerkarte Zahlung.</span><span class="sxs-lookup"><span data-stu-id="d0136-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="d0136-137">Klicken Sie im Feld "Zahlungsmethode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d0136-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="d0136-138">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="d0136-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d0136-139">Wählen Sie den Elektronischen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d0136-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="d0136-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d0136-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="d0136-141">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d0136-141">Click Save.</span></span>
17. <span data-ttu-id="d0136-142">Klicken Sie auf Zahlungen generieren.</span><span class="sxs-lookup"><span data-stu-id="d0136-142">Click Generate payments.</span></span>
18. <span data-ttu-id="d0136-143">Klicken Sie im Feld "Zahlungsmethode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d0136-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="d0136-144">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="d0136-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d0136-145">Wählen Sie den Elektronischen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d0136-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="d0136-146">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d0136-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d0136-147">Wählen Sie den Elektronischen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d0136-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="d0136-148">Geben Sie im Feld "Dateiname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d0136-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="d0136-149">Geben Sie beispielsweise "Zahlungen" ein.</span><span class="sxs-lookup"><span data-stu-id="d0136-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="d0136-150">Klicken Sie im Feld "Bankkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d0136-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="d0136-151">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d0136-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d0136-152">Wählen Sie das Wert "GBSI OPER" aus.</span><span class="sxs-lookup"><span data-stu-id="d0136-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="d0136-153">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d0136-153">Click OK.</span></span>
25. <span data-ttu-id="d0136-154">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d0136-154">Click OK.</span></span>
    * <span data-ttu-id="d0136-155">Analysieren Sie die erstellte Zahlungsdatei im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="d0136-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="d0136-156">Vergleichen Sie diese mit dem entworfenen Dokumentlayout und den definierten Zahlungstransaktionsattributen.</span><span class="sxs-lookup"><span data-stu-id="d0136-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  


