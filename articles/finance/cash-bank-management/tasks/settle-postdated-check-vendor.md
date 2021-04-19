---
title: Ausgleichen eines vordatierten Schecks für einen Kreditor
description: Gleichen Sie einen vordatierten Scheck aus, der an einen Kreditor ausgestellt wurde, wenn die Bank die Scheckbuchung ausgeglichen hat, nachdem der Scheck überfällig war und von der Bank verrechnet wurde.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89acad0c9421960ff4d07ed8eec798b9068424d5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834570"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="a8bfd-103">Ausgleichen eines vordatierten Schecks für einen Kreditor</span><span class="sxs-lookup"><span data-stu-id="a8bfd-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8bfd-104">Gleichen Sie einen vordatierten Scheck aus, der an einen Kreditor ausgestellt wurde, wenn die Bank die Scheckbuchung ausgeglichen hat, nachdem der Scheck überfällig war und von der Bank verrechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="a8bfd-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="a8bfd-105">Schließen Sie folgende Prozeduren ab, bevor Sie diese starten:</span><span class="sxs-lookup"><span data-stu-id="a8bfd-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="a8bfd-106">Einrichten von vordatierten Schecks</span><span class="sxs-lookup"><span data-stu-id="a8bfd-106">Set up postdated checks</span></span>

2) <span data-ttu-id="a8bfd-107">Erfassen und Buchen eines vordatierten Schecks für einen Kreditor</span><span class="sxs-lookup"><span data-stu-id="a8bfd-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="a8bfd-108">Die Rolle dieser Prozedur ist "Finanzverwalter".</span><span class="sxs-lookup"><span data-stu-id="a8bfd-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="a8bfd-109">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="a8bfd-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="a8bfd-110">Wechseln Sie zu Kreditoren > Zahlungen > Vordatierte Schecks von Händler.</span><span class="sxs-lookup"><span data-stu-id="a8bfd-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="a8bfd-111">Klicken Sie auf "Ausgleichen".</span><span class="sxs-lookup"><span data-stu-id="a8bfd-111">Click Settle.</span></span>
3. <span data-ttu-id="a8bfd-112">Klicken Sie auf Verrechnungsposten ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="a8bfd-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="a8bfd-113">Das Kreditorenkonto für Scheck-Transaktionen ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="a8bfd-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="a8bfd-114">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a8bfd-114">Close the page.</span></span>
5. <span data-ttu-id="a8bfd-115">Wechseln Sie zu "Hauptbuch" > "Journaleinträge" > "Allgemeine Erfassungen".</span><span class="sxs-lookup"><span data-stu-id="a8bfd-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="a8bfd-116">Wählen Sie im Feld "Anzeigen" die Option "Alle" aus.</span><span class="sxs-lookup"><span data-stu-id="a8bfd-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="a8bfd-117">Aktivieren oder deaktivieren Sie das vom Benutzer erstellte Kontrollkästchen Nur Anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a8bfd-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="a8bfd-118">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="a8bfd-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="a8bfd-119">Klicken Sie auf Positionen.</span><span class="sxs-lookup"><span data-stu-id="a8bfd-119">Click Lines.</span></span>
10. <span data-ttu-id="a8bfd-120">Klicken Sie auf Beleg.</span><span class="sxs-lookup"><span data-stu-id="a8bfd-120">Click Voucher.</span></span>
11. <span data-ttu-id="a8bfd-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a8bfd-121">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]