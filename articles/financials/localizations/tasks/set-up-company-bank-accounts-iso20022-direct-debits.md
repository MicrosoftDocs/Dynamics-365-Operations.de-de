---
title: Unternehmens-Bankkonten für ISO20022-Lastschriften einrichten
description: Diese Aufgabe führt Sie durch die Einrichtung der unternehmensspezifischen Bankkontoinformationen, die zum Erstellen von Debitoren-Zahlungsdateien erforderlich sind.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89c4a8d3cb504df97bad5679bf12b3cdb5931d95
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852573"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="dd6d6-103">Unternehmens-Bankkonten für ISO20022-Lastschriften einrichten</span><span class="sxs-lookup"><span data-stu-id="dd6d6-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd6d6-104">Diese Aufgabe führt Sie durch die Einrichtung der unternehmensspezifischen Bankkontoinformationen, die zum Erstellen von Debitoren-Zahlungsdateien erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="dd6d6-105">Diese Verfahren verwendet das ISO 20022-Direktbelastungsformat als Beispiel.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="dd6d6-106">Andere Formate erfordern ggf. zusätzliche Einrichtungsinformationen wie die Unternehmenskennung oder die Bankleitzahl.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="dd6d6-107">Diese Aufgabe wurde mit dem Demodatenunternehmen DEMF erstellt.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="dd6d6-108">Dies ist die zweite von sechs Aufgaben, die das Verfahren für Debitorenzahlungen über elektronischen Berichterstellungskonfigurationen zeigen.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="dd6d6-109">IBAN- und SWIFT -Codes einrichten</span><span class="sxs-lookup"><span data-stu-id="dd6d6-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="dd6d6-110">Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Bankkonten".</span><span class="sxs-lookup"><span data-stu-id="dd6d6-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="dd6d6-111">Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "DEMF OPER" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="dd6d6-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dd6d6-113">Beispiel: Klicken Sie auf "DEMF OPER", um die Bankkontodetails zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="dd6d6-114">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="dd6d6-114">Click Edit.</span></span>
5. <span data-ttu-id="dd6d6-115">Erweitern oder reduzieren Sie den Abschnitt "Zusätzliche Kennung".</span><span class="sxs-lookup"><span data-stu-id="dd6d6-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="dd6d6-116">Geben Sie im Feld "IBAN" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="dd6d6-117">Geben Sie beispielsweise 'DE89370400440532013000' ein.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="dd6d6-118">Geben Sie im Feld "SWIFT-Code" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="dd6d6-119">Geben Sie z. B. 'DEUTDEFF' ein.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="dd6d6-120">Beachten Sie, dass die SWIFT\BIC nicht für mehrere Zahlungsformate erforderlich ist, jedoch empfohlen wird, um sie für ein Bankkonto zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="dd6d6-121">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="dd6d6-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="dd6d6-122">Bankkonto für die juristische Person einrichten</span><span class="sxs-lookup"><span data-stu-id="dd6d6-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="dd6d6-123">Wechseln Sie zu Organisationsverwaltung > Organisationen > Juristische Personen.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="dd6d6-124">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="dd6d6-124">Click Edit.</span></span>
3. <span data-ttu-id="dd6d6-125">Erweitern oder reduzieren Sie den Abschnitt "Bankkontoinformationen".</span><span class="sxs-lookup"><span data-stu-id="dd6d6-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="dd6d6-126">Klicken Sie im Feld "Bankkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="dd6d6-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dd6d6-128">Beispiel: Wählen Sie das "DEMF-OPER" Bankkonto aus.</span><span class="sxs-lookup"><span data-stu-id="dd6d6-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="dd6d6-129">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="dd6d6-129">Click Save.</span></span>

