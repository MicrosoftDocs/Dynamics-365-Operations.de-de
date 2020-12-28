---
title: Lieferscheinaktualisierungen für Rücklieferungen
description: Bevor zurückgelieferte Artikel im Lager entgegengenommen werden können, muss der Lieferschein für den zugehörigen Auftrag aktualisiert werden.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7f5bf5adb603d7edb40960b70cb71e25a2f0456
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428729"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="03799-103">Lieferscheinaktualisierungen für Rücklieferungen</span><span class="sxs-lookup"><span data-stu-id="03799-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="03799-104">Bevor zurückgelieferte Artikel im Lager entgegengenommen werden können, muss der Lieferschein für den zugehörigen Auftrag aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="03799-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="03799-105">So wie die Rechnungsaktualisierung die Aktualisierung für die Finanzbuchung darstellt, ist die Lieferscheinaktualisierung die physische Aktualisierung des Lagerdatensatzes. Das heißt, die Änderungen werden in das Lager übernommen.</span><span class="sxs-lookup"><span data-stu-id="03799-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="03799-106">Bei Retouren werden die der Dispositionsaktivität zugeordneten Schritte bei der Lieferscheinaktualisierung implementiert.</span><span class="sxs-lookup"><span data-stu-id="03799-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="03799-107">Die Lieferscheinaktualisierung kann in der Wareneingangserfassung oder in der Rücklieferung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="03799-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="03799-108">Als Teil des Prozesses der Lieferscheinbuchung kann die Lieferschein-Referenznummer aus den Versanddokumenten des Debitors den Auftragspositionen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="03799-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="03799-109">Diese Zuordnung dient lediglich Referenzzwecken</span><span class="sxs-lookup"><span data-stu-id="03799-109">This association is optional and for reference only.</span></span> <span data-ttu-id="03799-110">und führt nicht zu Buchungsaktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="03799-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="03799-111">Wenn nicht alle erwarteten Rückgabeartikel eingegangen sind, sollten Sie nur die eingegangene Menge in die Lieferscheinaktualisierung aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="03799-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="03799-112">Belassen Sie die übrigen Artikel bis zum Eingang der restlichen Rücklieferung im Auftrag.</span><span class="sxs-lookup"><span data-stu-id="03799-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="03799-113">Wenn ein Artikel aus der Quarantäne zurück an die Versand- und Empfangsabteilung gesendet wird, z. B. wenn der Quarantäneprüfer nicht weiß, wo der Artikel im Lager abgelegt werden soll, muss der entsprechende Lieferschein zum richtigen Erfassen und Handeln gemäß des als Ergebnis der Quarantäne angegebenen Dispositionscodes aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="03799-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="03799-114">Wenn Sie einen Lieferschein für einen zurückgelieferten Artikel aktualisieren, der aus einer Rahmenbestellung ist, wird die Kaufvertragszusage für diesen Artikel automatisch aktualisiert, um die Änderung in der Menge oder im Betrag widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="03799-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="03799-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03799-115">See also</span></span>

[<span data-ttu-id="03799-116">Ausführen von Rechnungsaktualisierungen für Rücklieferungen</span><span class="sxs-lookup"><span data-stu-id="03799-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  


