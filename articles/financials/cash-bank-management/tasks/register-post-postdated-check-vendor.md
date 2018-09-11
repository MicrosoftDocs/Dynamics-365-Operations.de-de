--- 
title: "Erfassen und Buchen eines vordatierten Schecks für einen Kreditor"
description: "Mithilfe eines Erfassungsbelegs können Sie die Details eines vordatierten Schecks erfassen, bevor der Scheck an einen Kreditor ausgestellt wird."
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 3b69178124e0bced65232277c422ceb5986e1a76
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2018

---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="74d68-103">Erfassen und Buchen eines vordatierten Schecks für einen Kreditor</span><span class="sxs-lookup"><span data-stu-id="74d68-103">Register and post a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74d68-104">Mithilfe eines Erfassungsbelegs können Sie die Details eines vordatierten Schecks erfassen, bevor der Scheck an einen Kreditor ausgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="74d68-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="74d68-105">Sie können den vordatierten Scheck buchen und Finanzbuchungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="74d68-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="74d68-106">Führen Sie die folgenden Schritte aus, bevor Sie einen vordatierten Scheck registrieren und buchen, den Sie von einem Debitor erhalten haben:</span><span class="sxs-lookup"><span data-stu-id="74d68-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="74d68-107">Einrichten von vordatierten Schecks in bar und in der Bankverwaltungsseite.</span><span class="sxs-lookup"><span data-stu-id="74d68-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="74d68-108">Die Rolle dieses Aufgabenleitfadens ist "Finanzverwalter".</span><span class="sxs-lookup"><span data-stu-id="74d68-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="74d68-109">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="74d68-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="74d68-110">Wechseln Sie zu Kreditoren > Zahlungen > Zahlungserfassung</span><span class="sxs-lookup"><span data-stu-id="74d68-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="74d68-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="74d68-111">Click New.</span></span>
3. <span data-ttu-id="74d68-112">Geben Sie im Namensfeld "VendPay" ein.</span><span class="sxs-lookup"><span data-stu-id="74d68-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="74d68-113">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="74d68-113">Click Lines.</span></span>
5. <span data-ttu-id="74d68-114">Geben Sie im Feld "Konto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="74d68-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="74d68-115">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="74d68-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="74d68-116">Geben Sie im Feld "Soll" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="74d68-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="74d68-117">Klicken Sie im Feld "Zahlungsmethode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="74d68-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="74d68-118">Wählen Sie die Zahlungsmethode für den vordatierten Scheck aus.</span><span class="sxs-lookup"><span data-stu-id="74d68-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="74d68-119">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="74d68-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="74d68-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="74d68-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="74d68-121">Klicken Sie auf die Registerkarte "Vordatierte Schecks".</span><span class="sxs-lookup"><span data-stu-id="74d68-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="74d68-122">Geben Sie im Feld "Schecknummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="74d68-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="74d68-123">Geben Sie die Nummer des vordatierten Schecks ein oder ändern Sie sie.</span><span class="sxs-lookup"><span data-stu-id="74d68-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="74d68-124">Geben Sie im Feld "Ausstellender Bankname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="74d68-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="74d68-125">Geben Sie die Bankdetails für die ausgebende Bank ein.</span><span class="sxs-lookup"><span data-stu-id="74d68-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="74d68-126">Klicken Sie auf die Registerkarte "Liste".</span><span class="sxs-lookup"><span data-stu-id="74d68-126">Click the List tab.</span></span>
15. <span data-ttu-id="74d68-127">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="74d68-127">Click Post.</span></span>
16. <span data-ttu-id="74d68-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="74d68-128">Close the page.</span></span>
17. <span data-ttu-id="74d68-129">Klicken Sie auf die Registerkarte "Vordatierte Schecks".</span><span class="sxs-lookup"><span data-stu-id="74d68-129">Click the Postdated checks tab.</span></span>


