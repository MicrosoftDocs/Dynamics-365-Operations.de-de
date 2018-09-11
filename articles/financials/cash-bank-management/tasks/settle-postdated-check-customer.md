--- 
title: Ausgleichen eines vordatierten Schecks von einem Debitor
description: "Sie können einen vordatierten Scheck ausgleichen, nachdem der Scheck von der Bank verrechnet wurde."
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: aaaee86d966e7144911f36a8d1419d991ace10d8
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2018

---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="9ef70-103">Ausgleichen eines vordatierten Schecks von einem Debitor</span><span class="sxs-lookup"><span data-stu-id="9ef70-103">Settle a postdated check from a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ef70-104">Sie können einen vordatierten Scheck ausgleichen, nachdem der Scheck von der Bank verrechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="9ef70-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="9ef70-105">Bei dieser Finanzbuchung wird auch die Übergangskontobuchung für den vordatierten Scheck ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="9ef70-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="9ef70-106">Schließen Sie folgende Prozeduren ab, bevor Sie diese starten:</span><span class="sxs-lookup"><span data-stu-id="9ef70-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="9ef70-107">Einrichten von vordatierten Schecks</span><span class="sxs-lookup"><span data-stu-id="9ef70-107">Set up postdated checks</span></span>

2) <span data-ttu-id="9ef70-108">Einen vordatierten Scheck für einen Debitor erfassen und buchen</span><span class="sxs-lookup"><span data-stu-id="9ef70-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="9ef70-109">Die Rolle dieses Aufgabenleitfadens ist "Finanzverwalter".</span><span class="sxs-lookup"><span data-stu-id="9ef70-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="9ef70-110">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ef70-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="9ef70-111">Wechseln Sie zu Kredit und Inkasso > Abfragen und Berichte > Zahlungen > Vordatierte Schecks.</span><span class="sxs-lookup"><span data-stu-id="9ef70-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="9ef70-112">Klicken Sie auf "Ausgleichen".</span><span class="sxs-lookup"><span data-stu-id="9ef70-112">Click Settle.</span></span>
3. <span data-ttu-id="9ef70-113">Klicken Sie auf Verrechnungsposten ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="9ef70-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="9ef70-114">Gleichen Sie das Debitorenkonto für die Scheck-Transaktionen aus.</span><span class="sxs-lookup"><span data-stu-id="9ef70-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="9ef70-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9ef70-115">Close the page.</span></span>
5. <span data-ttu-id="9ef70-116">Wechseln Sie zu "Hauptbuch" > "Journaleinträge" > "Allgemeine Erfassungen".</span><span class="sxs-lookup"><span data-stu-id="9ef70-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="9ef70-117">Wählen Sie im Feld 'Anzeigen:' eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="9ef70-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="9ef70-118">Aktivieren oder deaktivieren Sie das vom Benutzer erstellte Kontrollkästchen Nur Anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9ef70-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="9ef70-119">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9ef70-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="9ef70-120">Klicken Sie auf Positionen.</span><span class="sxs-lookup"><span data-stu-id="9ef70-120">Click Lines.</span></span>
10. <span data-ttu-id="9ef70-121">Klicken Sie auf Beleg.</span><span class="sxs-lookup"><span data-stu-id="9ef70-121">Click Voucher.</span></span>
11. <span data-ttu-id="9ef70-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9ef70-122">Close the page.</span></span>


