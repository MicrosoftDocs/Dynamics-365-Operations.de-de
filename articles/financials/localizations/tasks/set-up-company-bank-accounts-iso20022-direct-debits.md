--- 
title: "Unternehmens-Bankkonten für ISO20022-Lastschriften einrichten"
description: "Diese Aufgabe führt Sie durch die Einrichtung der unternehmensspezifischen Bankkontoinformationen, die zum Erstellen von Debitoren-Zahlungsdateien erforderlich sind."
author: mrolecki
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 6b61495342b18d6dbadb36d8ca146f5a68ba9f6c
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="d4c19-103">Unternehmens-Bankkonten für ISO20022-Lastschriften einrichten</span><span class="sxs-lookup"><span data-stu-id="d4c19-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4c19-104">Diese Aufgabe führt Sie durch die Einrichtung der unternehmensspezifischen Bankkontoinformationen, die zum Erstellen von Debitoren-Zahlungsdateien erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d4c19-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="d4c19-105">Diese Verfahren verwendet das ISO 20022-Direktbelastungsformat als Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d4c19-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="d4c19-106">Andere Formate erfordern ggf. zusätzliche Einrichtungsinformationen wie die Unternehmenskennung oder die Bankleitzahl.</span><span class="sxs-lookup"><span data-stu-id="d4c19-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="d4c19-107">Diese Aufgabe wurde mit dem Demodatenunternehmen DEMF erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4c19-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="d4c19-108">Dies ist die zweite von sechs Aufgaben, die das Verfahren für Debitorenzahlungen über elektronischen Berichterstellungskonfigurationen zeigen.</span><span class="sxs-lookup"><span data-stu-id="d4c19-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="d4c19-109">IBAN- und SWIFT -Codes einrichten</span><span class="sxs-lookup"><span data-stu-id="d4c19-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="d4c19-110">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Bankkonten".</span><span class="sxs-lookup"><span data-stu-id="d4c19-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="d4c19-111">Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "DEMF OPER" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="d4c19-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="d4c19-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d4c19-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d4c19-113">Beispiel: Klicken Sie auf "DEMF OPER", um die Bankkontodetails zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d4c19-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="d4c19-114">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="d4c19-114">Click Edit.</span></span>
5. <span data-ttu-id="d4c19-115">Erweitern oder reduzieren Sie den Abschnitt "Zusätzliche Kennung".</span><span class="sxs-lookup"><span data-stu-id="d4c19-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="d4c19-116">Geben Sie im Feld "IBAN" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d4c19-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="d4c19-117">Geben Sie beispielsweise 'DE89370400440532013000' ein.</span><span class="sxs-lookup"><span data-stu-id="d4c19-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="d4c19-118">Geben Sie im Feld "SWIFT-Code" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d4c19-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="d4c19-119">Geben Sie z. B. 'DEUTDEFF' ein.</span><span class="sxs-lookup"><span data-stu-id="d4c19-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="d4c19-120">Beachten Sie, dass die SWIFT\BIC nicht für mehrere Zahlungsformate erforderlich ist, jedoch empfohlen wird, um sie für ein Bankkonto zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="d4c19-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="d4c19-121">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d4c19-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="d4c19-122">Bankkonto für die juristische Person einrichten</span><span class="sxs-lookup"><span data-stu-id="d4c19-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="d4c19-123">Wechseln Sie zu Organisationsverwaltung > Organisationen > Juristische Personen.</span><span class="sxs-lookup"><span data-stu-id="d4c19-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="d4c19-124">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="d4c19-124">Click Edit.</span></span>
3. <span data-ttu-id="d4c19-125">Erweitern oder reduzieren Sie den Abschnitt "Bankkontoinformationen".</span><span class="sxs-lookup"><span data-stu-id="d4c19-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="d4c19-126">Klicken Sie im Feld "Bankkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d4c19-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d4c19-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d4c19-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d4c19-128">Beispiel: Wählen Sie das "DEMF-OPER" Bankkonto aus.</span><span class="sxs-lookup"><span data-stu-id="d4c19-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="d4c19-129">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d4c19-129">Click Save.</span></span>


