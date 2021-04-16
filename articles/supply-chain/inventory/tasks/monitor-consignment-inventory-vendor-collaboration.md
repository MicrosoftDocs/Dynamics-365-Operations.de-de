---
title: Lagerbestand mithilfe der Kreditorenkooperation überwachen
description: Dieses Verfahren zeigt, wie Sie Kreditor-Kooperationen nutzen, um Informationen zum Bestand des Produkts anzuzeigen, den Sie in der Lieferung des Debitors platziert haben.
author: sherry-zheng
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e397c12b9f605d1c864ce053477090ed8c1700
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839270"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="9b765-103">Lagerbestand mithilfe der Kreditorenkooperation überwachen</span><span class="sxs-lookup"><span data-stu-id="9b765-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b765-104">Dieses Verfahren zeigt, wie Sie Kreditor-Kooperationen nutzen, um Informationen zum Bestand des Produkts anzuzeigen, den Sie in der Lieferung des Debitors platziert haben.</span><span class="sxs-lookup"><span data-stu-id="9b765-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="9b765-105">Sie können außerdem den Verbrauch des Bestandes überwachen, wenn der Debitor den Besitz übernimmt.</span><span class="sxs-lookup"><span data-stu-id="9b765-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="9b765-106">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b765-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="9b765-107">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="9b765-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="9b765-108">Verbrauchten Bestand anzeigen</span><span class="sxs-lookup"><span data-stu-id="9b765-108">View consumed inventory</span></span>
1. <span data-ttu-id="9b765-109">Wechseln Sie zu "Kreditor-Kooperation" > "Lieferbestand" > "Aus Unterlieferungsbestand erhaltene Produkte".</span><span class="sxs-lookup"><span data-stu-id="9b765-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="9b765-110">Die Liste enthält die Produktzugangspositionen, die generiert wurden, als der Besitzer des Lieferungsbestandes vom Kreditor auf den Debitor geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="9b765-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="9b765-111">Möglicherweise müssen Sie rechts nach unten scrollen, um die Mengen und weitere Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9b765-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="9b765-112">Sie können die Informationen in dieser Liste verwenden, um Rechnungen für den Debitor zu generieren.</span><span class="sxs-lookup"><span data-stu-id="9b765-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="9b765-113">Sie können die Daten auch nach Microsoft Excel exportieren.</span><span class="sxs-lookup"><span data-stu-id="9b765-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="9b765-114">Klicken Sie auf "Bestellung anzeigen".</span><span class="sxs-lookup"><span data-stu-id="9b765-114">Click View purchase order.</span></span>
3. <span data-ttu-id="9b765-115">Erweitern Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="9b765-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="9b765-116">Die Position wird als Lieferung markiert und der Kopfbereich zeigt an, dass die Bestellung den Status "Eingegangen" hat.</span><span class="sxs-lookup"><span data-stu-id="9b765-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="9b765-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9b765-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="9b765-118">Verfügbaren Lagerbestand anzeigen</span><span class="sxs-lookup"><span data-stu-id="9b765-118">View on-hand inventory</span></span>
1. <span data-ttu-id="9b765-119">Wechseln Sie zu "Kreditor-Kooperation" > "Lieferbestand" > "Verfügbarer Lagerbestand".</span><span class="sxs-lookup"><span data-stu-id="9b765-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="9b765-120">Die Seite „Verfügbare Lieferungsbestand“ zeigt den Bestand, den Sie am Lagerort des Debitors besitzen.</span><span class="sxs-lookup"><span data-stu-id="9b765-120">The On-hand consignment inventory page shows the stock that you own at the customer's warehouse.</span></span> <span data-ttu-id="9b765-121">Sie können zusätzliche Dimensionen eingegeben, z. B. der Standort und der Lagerort, indem Sie auf die Registerkarte "Dimensionen anzeigen" klicken.</span><span class="sxs-lookup"><span data-stu-id="9b765-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]