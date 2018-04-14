--- 
title: "Debitoren und Debitoren-Bankkonten für ISO20022-Lastschriften einrichten"
description: "Diese Aufgabe führt Sie durch die Einrichtung eines Debitorenbankkontos und eines Direkteinzugsmandats des Debitors, die erforderlich sind, um die ISO20022-Kreditoren-Direktbelastungszahlungsdatei zu generieren."
author: mrolecki
manager: AnnBe
ms.date: 10/31/2017
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
ms.openlocfilehash: 16c59a53a5708a470fc1aa02d6730b7e83eece18
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="d4ec8-103">Debitoren und Debitoren-Bankkonten für ISO20022-Lastschriften einrichten</span><span class="sxs-lookup"><span data-stu-id="d4ec8-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4ec8-104">Diese Aufgabe führt Sie durch die Einrichtung eines Debitorenbankkontos und eines Direkteinzugsmandats des Debitors, die erforderlich sind, um die ISO20022-Kreditoren-Direktbelastungszahlungsdatei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="d4ec8-105">Abhängig von Debitorenzahlungsformaten, die eingerichtet sind, sind zusätzliche Informationen erforderlich, die nicht in dieser Prozedur abgedeckt werden, aber für einen Debitor oder ein Debitorenbankkonto erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-105">Depending on the customer payment formats that are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="d4ec8-106">Diese Aufgabe wurde mithilfe des Demodatenunternehmens DEMF mit der primären Adresse einer juristischen Person in Deutschland erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="d4ec8-107">Dies ist der vierte von sechs Aufgaben, die das Verfahren für Debitorenzahlungen über elektronischen Berichterstellungskonfigurationen zeigen.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="d4ec8-108">Einrichten eines Debitorenbankkontos</span><span class="sxs-lookup"><span data-stu-id="d4ec8-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="d4ec8-109">Wechseln Sie zu "Debitoren" > "Debitoren" > "Alle Debitoren".</span><span class="sxs-lookup"><span data-stu-id="d4ec8-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="d4ec8-110">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d4ec8-111">Filtern Sie beispielsweise im Feld "Konto" mit dem Wert "DE-010".</span><span class="sxs-lookup"><span data-stu-id="d4ec8-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="d4ec8-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d4ec8-113">Klicken Sie im Aktivitätsbereich auf "Debitor".</span><span class="sxs-lookup"><span data-stu-id="d4ec8-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="d4ec8-114">Klicken Sie auf Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="d4ec8-115">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d4ec8-115">Click New.</span></span>
7. <span data-ttu-id="d4ec8-116">Geben Sie im Feld "Bankkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="d4ec8-117">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d4ec8-118">Geben Sie beispielsweise 'EUR Bank'. ein.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="d4ec8-119">Geben Sie im Feld 'Bankgruppen' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="d4ec8-120">Geben Sie im Feld "IBAN" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="d4ec8-121">Geben Sie beispielsweise 'DE36200400000628808808' ein.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="d4ec8-122">Geben Sie im Feld "SWIFT-Code" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="d4ec8-123">Geben Sie beispielsweise "COBADEFFXXX" ein.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="d4ec8-124">Beachten Sie, dass die SWIFT\BIC nicht für mehrere Zahlungsformate erforderlich ist, jedoch empfohlen wird, um sie für ein Bankkonto zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="d4ec8-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d4ec8-125">Click Save.</span></span>
13. <span data-ttu-id="d4ec8-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-126">Close the page.</span></span>
14. <span data-ttu-id="d4ec8-127">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="d4ec8-127">Click Edit.</span></span>
15. <span data-ttu-id="d4ec8-128">Erweitern Sie den Abschnitt "Zahlungsausfälle".</span><span class="sxs-lookup"><span data-stu-id="d4ec8-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="d4ec8-129">Geben Sie im Feld 'Bankkonto' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="d4ec8-130">Direkteinzugsmandats-ID hinzufügen</span><span class="sxs-lookup"><span data-stu-id="d4ec8-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="d4ec8-131">Erweitern Sie den Abschnitt "Einzugsermächtigungen".</span><span class="sxs-lookup"><span data-stu-id="d4ec8-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="d4ec8-132">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-132">Click Add.</span></span>
3. <span data-ttu-id="d4ec8-133">Geben Sie im Feld 'Kreditorenbankkonto' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="d4ec8-134">Wählen Sie z. B. DEMF OPER. aus.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="d4ec8-135">Geben Sie im Feld "Unterschriftsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="d4ec8-136">Klicken Sie auf "Ja", um die Datumsaktualisierung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="d4ec8-137">Geben Sie im Feld "Ort der Signatur" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="d4ec8-138">Geben Sie im Feld "Erwartete Anzahl der Zahlungen" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d4ec8-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="d4ec8-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d4ec8-139">Click OK.</span></span>
9. <span data-ttu-id="d4ec8-140">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d4ec8-140">Click Save.</span></span>


