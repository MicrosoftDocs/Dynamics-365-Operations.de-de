---
title: Eine Bestellung für einen einmaligen Lieferanten erstellen
description: Diese Prozedur zeigt Ihnen, wie Sie eine Bestellung für einen einmaligen Lieferanten erstellen.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c4885547cdf2f8496446761e27ce39e67e670f15
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016401"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="68b68-103">Eine Bestellung für einen einmaligen Lieferanten erstellen</span><span class="sxs-lookup"><span data-stu-id="68b68-103">Create a purchase order for a one-time supplier</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="68b68-104">Diese Prozedur zeigt Ihnen, wie Sie eine Bestellung für einen einmaligen Lieferanten erstellen.</span><span class="sxs-lookup"><span data-stu-id="68b68-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="68b68-105">Der Lieferant wird automatisch mit der Bestellung erstellt und somit muss das Kreditorenkonto nicht manuell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="68b68-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="68b68-106">Bestellungen werden normalerweise von einem Einkaufsvertreter erstellt.</span><span class="sxs-lookup"><span data-stu-id="68b68-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="68b68-107">Das Beispiel, das in diesem Leitfaden angezeigt wird, kann im Demodatenunternehmen USMF verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68b68-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="68b68-108">Es ist eine Voraussetzung, dass ein einmaliges Kreditorenkonto auf der Seite "Kreditorenkontenparameter" eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="68b68-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="68b68-109">Eine Bestellung für einen einmaligen Lieferanten erstellen</span><span class="sxs-lookup"><span data-stu-id="68b68-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="68b68-110">Wechseln Sie zu "Beschaffung" > "Bestellung" > "Alle Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="68b68-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="68b68-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="68b68-111">Click New.</span></span>
3. <span data-ttu-id="68b68-112">Wählen Sie "Ja" im Feld "Einmaliger Lieferant" aus.</span><span class="sxs-lookup"><span data-stu-id="68b68-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="68b68-113">Ein Kreditorenkonto wird automatisch erstellt und der Bestellung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="68b68-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="68b68-114">Das Kreditorenkonto wird auf Basis der Vorlage erstellt, die auf der Registerkarte "Allgemein" auf der Seite "Kreditorenkontenparameter" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="68b68-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="68b68-115">Geben Sie im Feld "Name" einen Namen für den Lieferanten ein.</span><span class="sxs-lookup"><span data-stu-id="68b68-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="68b68-116">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="68b68-116">Click OK.</span></span>
    * <span data-ttu-id="68b68-117">Die Bestellung kann jetzt wie jeder andere Auftrag abgeschlossen und verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="68b68-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="68b68-118">Es gibt keine speziellen Eigenschaften, in Bezug darauf, wie dies erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="68b68-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="68b68-119">Die Rechnung berücksichtigt eine fällige Transaktion zum Kreditorenkonto, das mit dem Auftrag erstellt wurde, und die Zahlung wird dann verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="68b68-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>

