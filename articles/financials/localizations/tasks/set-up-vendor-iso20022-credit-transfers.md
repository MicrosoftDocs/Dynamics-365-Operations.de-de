---
title: Kreditoren und Kreditorenbankkonten für ISO20022-Überweisungen einrichten
description: Diese Verfahren zeigt, wie Sie den Kreditor und dessen spezifische Bankkontoinformationen einrichten, die für ISO20022-Kreditübertragung-Dateigenerierung oder jede andere Kreditorenzahlung erforderlich sind.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13b3c37f5d013dd896a456018813f20e5e70350b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565042"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="bc19a-103">Kreditoren und Kreditorenbankkonten für ISO20022-Überweisungen einrichten</span><span class="sxs-lookup"><span data-stu-id="bc19a-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bc19a-104">Diese Verfahren zeigt, wie Sie den Kreditor und dessen spezifische Bankkontoinformationen einrichten, die für ISO20022-Kreditübertragung-Dateigenerierung oder jede andere Kreditorenzahlung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="bc19a-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="bc19a-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DEMF.</span><span class="sxs-lookup"><span data-stu-id="bc19a-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="bc19a-106">Dies ist der vierte von fünf Aufgaben, die das Verfahren für Kreditorenzahlung über elektronischen Berichterstellungskonfigurationen zeigen.</span><span class="sxs-lookup"><span data-stu-id="bc19a-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="bc19a-107">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="bc19a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="bc19a-108">Bankdetails einrichten</span><span class="sxs-lookup"><span data-stu-id="bc19a-108">Set up bank details</span></span>
1. <span data-ttu-id="bc19a-109">Gehen Sie zu "Kreditoren" > "Händler" > "Alle Händler".</span><span class="sxs-lookup"><span data-stu-id="bc19a-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="bc19a-110">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bc19a-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bc19a-111">Filtern Sie beispielsweise im Feld "Kreditorenkonto" mit dem Wert "DE-001".</span><span class="sxs-lookup"><span data-stu-id="bc19a-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="bc19a-112">Klicken Sie auf "DE-001", um die Kreditorendetails zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bc19a-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="bc19a-113">Klicken Sie im Aktivitätsbereich auf "Händler".</span><span class="sxs-lookup"><span data-stu-id="bc19a-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="bc19a-114">Klicken Sie auf Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="bc19a-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="bc19a-115">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="bc19a-115">Click Edit.</span></span>
    * <span data-ttu-id="bc19a-116">Wenn kein verfügbares Bankkonto vorhanden ist, müssen Sie ein neuer Datensatz erstellen.</span><span class="sxs-lookup"><span data-stu-id="bc19a-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="bc19a-117">Geben Sie im Feld "SWIFT-Code" "COBADEFFXXX" ein.</span><span class="sxs-lookup"><span data-stu-id="bc19a-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="bc19a-118">Geben Sie im Feld "IBAN" den Wert "DE36200400000628808808" ein.</span><span class="sxs-lookup"><span data-stu-id="bc19a-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="bc19a-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bc19a-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="bc19a-120">Zahlungsmethode für den Kreditor einrichten</span><span class="sxs-lookup"><span data-stu-id="bc19a-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="bc19a-121">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="bc19a-121">Click Edit.</span></span>
2. <span data-ttu-id="bc19a-122">Erweitern oder reduzieren Sie den Abschnitt "Zahlung".</span><span class="sxs-lookup"><span data-stu-id="bc19a-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="bc19a-123">Klicken Sie im Feld "Zahlungsmethode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bc19a-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bc19a-124">Klicken Sie in der Liste auf den Link in der Zeile "SEPA CT".</span><span class="sxs-lookup"><span data-stu-id="bc19a-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="bc19a-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="bc19a-125">Click Save.</span></span>

