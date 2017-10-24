---
title: SEPA-Direkteinzugsmandate einrichten
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8b50c2d585c7e0bcd8dc15aa70446cd7346ad33c
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="dc84f-102">SEPA-Direkteinzugsmandate einrichten</span><span class="sxs-lookup"><span data-stu-id="dc84f-102">Set up SEPA direct debit mandate</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="dc84f-103">Eine SEPA-Direktbelastung ermöglicht einem Kreditgeber Mittel vom Bankkonto eines Debitors einzuziehen, vorausgesetzt, dass eine signierte Einzugsermächtigung dem Kreditor vom Debitor gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="dc84f-103">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="dc84f-104">Der Debitor signiert eine Einzugsermächtigung, die den Lieferanten autorisiert, eine Zahlung einzuziehen und die Bank des Debitors anweist, die Sammlung zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="dc84f-104">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="dc84f-105">In diesem Thema wird erläutert, um den Prozess zum Einrichten von SEPA-Direktbelastungsvollmachten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dc84f-105">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dc84f-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="dc84f-106">Prerequisites</span></span>
<span data-ttu-id="dc84f-107">In der folgenden Tabelle werden die Voraussetzungen angezeigt, die vorhanden sein müssen, bevor Sie beginnen können.</span><span class="sxs-lookup"><span data-stu-id="dc84f-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="dc84f-108">Kategorie</span><span class="sxs-lookup"><span data-stu-id="dc84f-108">Category</span></span>       | <span data-ttu-id="dc84f-109">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="dc84f-109">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc84f-110">Land/Region</span><span class="sxs-lookup"><span data-stu-id="dc84f-110">Country/region</span></span> | <span data-ttu-id="dc84f-111">Die Hauptadresse für die juristische Person muss in den folgenden Ländern/Regionen sein: Österreich, Deutschland, Spanien, Frankreich, Italien, oder die Niederlande.</span><span class="sxs-lookup"><span data-stu-id="dc84f-111">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="dc84f-112">Einrichten eines Nummernkreises für Direktbelastungsvollmachten, die jede Direktbelastungsvollmacht eine eindeutige Zahl besitzen muss.</span><span class="sxs-lookup"><span data-stu-id="dc84f-112">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="dc84f-113">Verwenden Sie die Seite **Nummernkreis**, um einen Nummernkreis für Direktbelastungseinzugsermächtigungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dc84f-113">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="dc84f-114">Sie verwenden diese Kennung, um den Nummernkreis dem Direktbelastungseinzugsermächtigungssystem im Formular **Debitorenkontenparameter** zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="dc84f-114">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="dc84f-115">Einrichten von Debitorenparametern für Direktbelastungsvollmachten verwenden die **Debitorenparameter** Seite, um Parameter für Direktbelastungsvollmachten einzurichten.</span><span class="sxs-lookup"><span data-stu-id="dc84f-115">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="dc84f-116">Die Parameter, auf der Registerkarte einrichten **Direktbelastung** Änderung die Standardparameter, wie Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="dc84f-116">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="dc84f-117">Stellen Sie anschließend auf der Registerkarte **Nummernkreise** aktualisieren Sie das **Direktbelastungsvollmacht-Kennung** Feld dem Sie vor diesem Nummernkreis einrichten.</span><span class="sxs-lookup"><span data-stu-id="dc84f-117">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="dc84f-118">Einrichten einer Zahlungsmethode für Direktbelastungseinzugs-ermächtigungen. Um eine Zahlungsmethode für Direktbelastungseinzugsermächtigungen einzurichten, müssen Sie diese zusätzlichen Schritte für eine Zahlungsmethode durchführen:</span><span class="sxs-lookup"><span data-stu-id="dc84f-118">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="dc84f-119">Sie verwenden diese Zahlungsmethode, um Rechnungen abfragen, die das Abbuchen generieren.</span><span class="sxs-lookup"><span data-stu-id="dc84f-119">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="dc84f-120">Verwenden Sie die Seite **Zahlungsmethoden**, um die Zahlungsmethode einzurichten.</span><span class="sxs-lookup"><span data-stu-id="dc84f-120">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="dc84f-121">Um eine Zahlungsmethode für Direktbelastungseinzugsermächtigungen einzurichten, müssen Sie diese zusätzlichen Schritte für eine Zahlungsmethode durchführen:</span><span class="sxs-lookup"><span data-stu-id="dc84f-121">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="dc84f-122">Wählen Sie im Feld **Zahlungstyp** **Elektronischer Zahlungsverkehr** aus.</span><span class="sxs-lookup"><span data-stu-id="dc84f-122">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="dc84f-123">Optional: Wenn Sie von jedem Ihrer Debitoren erwarten, mehrere Einzugsermächtigungen zu haben, wählen Sie im Feld **Zeitraum** **Rechnung** aus.</span><span class="sxs-lookup"><span data-stu-id="dc84f-123">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="dc84f-124">Dieses erstellt eine separate Zahlung für jede Rechnung, und jede Zahlung verwendet die Einzugsermächtigung, die für die Rechnung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="dc84f-124">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="dc84f-125">Wählen Sie die **Mandat anfordern**-Option aus, um Zahlungen zu erstellen, indem Sie Direktbelastungseinzugsermächtigungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc84f-125">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="dc84f-126">Die **Mandat anfordern**-Option ist nur verfügbar, wenn Sie **Elektronischer Zahlungsverkehr** im Feld **Zahlungstyp** auswählen.</span><span class="sxs-lookup"><span data-stu-id="dc84f-126">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="dc84f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc84f-127">See Also</span></span>

[<span data-ttu-id="dc84f-128">Direktbelastungsüberblick</span><span class="sxs-lookup"><span data-stu-id="dc84f-128">Direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="dc84f-129">Direkteinzugsmandat für einen Debitor erstellen</span><span class="sxs-lookup"><span data-stu-id="dc84f-129">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 


