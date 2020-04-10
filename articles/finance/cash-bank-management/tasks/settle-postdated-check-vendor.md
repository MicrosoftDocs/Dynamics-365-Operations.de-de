---
title: Ausgleichen eines vordatierten Schecks für einen Kreditor
description: Gleichen Sie einen vordatierten Scheck aus, der an einen Kreditor ausgestellt wurde, wenn die Bank die Scheckbuchung ausgeglichen hat, nachdem der Scheck überfällig war und von der Bank verrechnet wurde.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee66bdb93d1252486efc7be25adeb6ee7cc6ce05
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144238"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="b9654-103">Ausgleichen eines vordatierten Schecks für einen Kreditor</span><span class="sxs-lookup"><span data-stu-id="b9654-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b9654-104">Gleichen Sie einen vordatierten Scheck aus, der an einen Kreditor ausgestellt wurde, wenn die Bank die Scheckbuchung ausgeglichen hat, nachdem der Scheck überfällig war und von der Bank verrechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="b9654-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="b9654-105">Schließen Sie folgende Prozeduren ab, bevor Sie diese starten:</span><span class="sxs-lookup"><span data-stu-id="b9654-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="b9654-106">Einrichten von vordatierten Schecks</span><span class="sxs-lookup"><span data-stu-id="b9654-106">Set up postdated checks</span></span>

2) <span data-ttu-id="b9654-107">Erfassen und Buchen eines vordatierten Schecks für einen Kreditor</span><span class="sxs-lookup"><span data-stu-id="b9654-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="b9654-108">Die Rolle dieser Prozedur ist "Finanzverwalter".</span><span class="sxs-lookup"><span data-stu-id="b9654-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="b9654-109">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="b9654-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="b9654-110">Wechseln Sie zu Kreditoren > Zahlungen > Vordatierte Schecks von Händler.</span><span class="sxs-lookup"><span data-stu-id="b9654-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="b9654-111">Klicken Sie auf "Ausgleichen".</span><span class="sxs-lookup"><span data-stu-id="b9654-111">Click Settle.</span></span>
3. <span data-ttu-id="b9654-112">Klicken Sie auf Verrechnungsposten ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="b9654-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="b9654-113">Das Kreditorenkonto für Scheck-Transaktionen ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="b9654-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="b9654-114">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b9654-114">Close the page.</span></span>
5. <span data-ttu-id="b9654-115">Wechseln Sie zu "Hauptbuch" > "Journaleinträge" > "Allgemeine Erfassungen".</span><span class="sxs-lookup"><span data-stu-id="b9654-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="b9654-116">Wählen Sie im Feld "Anzeigen" die Option "Alle" aus.</span><span class="sxs-lookup"><span data-stu-id="b9654-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="b9654-117">Aktivieren oder deaktivieren Sie das vom Benutzer erstellte Kontrollkästchen Nur Anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b9654-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="b9654-118">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="b9654-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b9654-119">Klicken Sie auf Positionen.</span><span class="sxs-lookup"><span data-stu-id="b9654-119">Click Lines.</span></span>
10. <span data-ttu-id="b9654-120">Klicken Sie auf Beleg.</span><span class="sxs-lookup"><span data-stu-id="b9654-120">Click Voucher.</span></span>
11. <span data-ttu-id="b9654-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b9654-121">Close the page.</span></span>

