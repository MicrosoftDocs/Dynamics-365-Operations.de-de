---
title: SEPA-Direkteinzugsvollmacht einrichten
description: Eine SEPA-Direktbelastung ermöglicht einem Kreditgeber Mittel vom Bankkonto eines Debitors einzuziehen, vorausgesetzt, dass eine signierte Einzugsermächtigung dem Kreditor vom Debitor gewährt wurde.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aba265e69bde9a9c194147d6ee6a806e9b2bd7c2
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772121"
---
# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="1da8f-103">SEPA-Direkteinzugsvollmacht einrichten</span><span class="sxs-lookup"><span data-stu-id="1da8f-103">Set up SEPA direct debit mandate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1da8f-104">Eine SEPA-Direktbelastung ermöglicht einem Kreditgeber Mittel vom Bankkonto eines Debitors einzuziehen, vorausgesetzt, dass eine signierte Einzugsermächtigung dem Kreditor vom Debitor gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="1da8f-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="1da8f-105">Der Debitor signiert eine Einzugsermächtigung, die den Lieferanten autorisiert, eine Zahlung einzuziehen und die Bank des Debitors anweist, die Sammlung zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="1da8f-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="1da8f-106">In diesem Thema wird erläutert, um den Prozess zum Einrichten von SEPA-Direktbelastungsvollmachten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1da8f-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1da8f-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1da8f-107">Prerequisites</span></span>
<span data-ttu-id="1da8f-108">In der folgenden Tabelle werden die Voraussetzungen angezeigt, die vorhanden sein müssen, bevor Sie beginnen können.</span><span class="sxs-lookup"><span data-stu-id="1da8f-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="1da8f-109">Kategorie</span><span class="sxs-lookup"><span data-stu-id="1da8f-109">Category</span></span>       | <span data-ttu-id="1da8f-110">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="1da8f-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1da8f-111">Land/Region</span><span class="sxs-lookup"><span data-stu-id="1da8f-111">Country/region</span></span> | <span data-ttu-id="1da8f-112">Die Hauptadresse für die juristische Person muss in den folgenden Ländern/Regionen sein: Österreich, Deutschland, Spanien, Frankreich, Italien, oder die Niederlande.</span><span class="sxs-lookup"><span data-stu-id="1da8f-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="1da8f-113">Einrichten eines Nummernkreises für Direktbelastungsvollmachten, die jede Direktbelastungsvollmacht eine eindeutige Zahl besitzen muss.</span><span class="sxs-lookup"><span data-stu-id="1da8f-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="1da8f-114">Verwenden Sie die Seite **Nummernkreis**, um einen Nummernkreis für Direktbelastungseinzugsermächtigungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1da8f-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="1da8f-115">Sie verwenden diese Kennung, um den Nummernkreis dem Direktbelastungseinzugsermächtigungssystem im Formular **Debitorenkontenparameter** zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="1da8f-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="1da8f-116">Einrichten von Debitorenparametern für Direktbelastungsvollmachten verwenden die **Debitorenparameter** Seite, um Parameter für Direktbelastungsvollmachten einzurichten.</span><span class="sxs-lookup"><span data-stu-id="1da8f-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="1da8f-117">Die Parameter, auf der Registerkarte einrichten **Direktbelastung** Änderung die Standardparameter, wie Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="1da8f-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="1da8f-118">Stellen Sie anschließend auf der Registerkarte **Nummernkreise** aktualisieren Sie das **Direktbelastungsvollmacht-Kennung** Feld dem Sie vor diesem Nummernkreis einrichten.</span><span class="sxs-lookup"><span data-stu-id="1da8f-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="1da8f-119">Einrichten einer Zahlungsmethode für Direktbelastungseinzugs-ermächtigungen. Um eine Zahlungsmethode für Direktbelastungseinzugsermächtigungen einzurichten, müssen Sie diese zusätzlichen Schritte für eine Zahlungsmethode durchführen:</span><span class="sxs-lookup"><span data-stu-id="1da8f-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="1da8f-120">Sie verwenden diese Zahlungsmethode, um Rechnungen abfragen, die das Abbuchen generieren.</span><span class="sxs-lookup"><span data-stu-id="1da8f-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="1da8f-121">Verwenden Sie die Seite **Zahlungsmethoden**, um die Zahlungsmethode einzurichten.</span><span class="sxs-lookup"><span data-stu-id="1da8f-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="1da8f-122">Um eine Zahlungsmethode für Direktbelastungseinzugsermächtigungen einzurichten, müssen Sie diese zusätzlichen Schritte für eine Zahlungsmethode durchführen:</span><span class="sxs-lookup"><span data-stu-id="1da8f-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="1da8f-123">Wählen Sie im Feld **Zahlungstyp** **Elektronischer Zahlungsverkehr** aus.</span><span class="sxs-lookup"><span data-stu-id="1da8f-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="1da8f-124">Optional: Wenn Sie von jedem Ihrer Debitoren erwarten, mehrere Einzugsermächtigungen zu haben, wählen Sie im Feld **Zeitraum** **Rechnung** aus.</span><span class="sxs-lookup"><span data-stu-id="1da8f-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="1da8f-125">Dieses erstellt eine separate Zahlung für jede Rechnung, und jede Zahlung verwendet die Einzugsermächtigung, die für die Rechnung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1da8f-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="1da8f-126">Wählen Sie die **Mandat anfordern**-Option aus, um Zahlungen zu erstellen, indem Sie Direktbelastungseinzugsermächtigungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1da8f-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="1da8f-127">Die **Mandat anfordern**-Option ist nur verfügbar, wenn Sie **Elektronischer Zahlungsverkehr** im Feld **Zahlungstyp** auswählen.</span><span class="sxs-lookup"><span data-stu-id="1da8f-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="1da8f-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1da8f-128">Additional resources</span></span>

[<span data-ttu-id="1da8f-129">SEPA-Lastschriftüberblick</span><span class="sxs-lookup"><span data-stu-id="1da8f-129">SEPA direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="1da8f-130">Direkteinzugsmandat für einen Debitor erstellen</span><span class="sxs-lookup"><span data-stu-id="1da8f-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 

