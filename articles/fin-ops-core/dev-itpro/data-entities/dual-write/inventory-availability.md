---
title: Inventarverfügbarkeit in dualem Schreiben
description: Dieses Thema bietet Informationen zum Prüfen der Bestandverfügbarkeit in dualem Schreiben.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 227a2062a7985a787f8278c196f7df2fb6f31691
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443871"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="3e029-103">Inventarverfügbarkeit in dualem Schreiben</span><span class="sxs-lookup"><span data-stu-id="3e029-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e029-104">Mithilfe der Bestandverfügbarkeit können Sie Ihr Inventar überprüfen, bevor Sie ein Produkt zu den Formularen **Zitate**, **Aufträge** oder **Rechnungen** in Microsoft Dynamics 365 Sales hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3e029-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="3e029-105">Zum Beispiel ist die Überprüfung des Inventars und die Bestimmung eines Erfüllungstermins eine Schlüsselaufgabe in [Aussicht auf Bargeld](dual-write-prospect-to-cash.md) Prozess.</span><span class="sxs-lookup"><span data-stu-id="3e029-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="3e029-106">Wenn Sie nicht über genügend Bestand verfügen, können Sie einen Liefertermin basierend auf den projizierten Bestandeinnahmen und -Problemen schätzen.</span><span class="sxs-lookup"><span data-stu-id="3e029-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="3e029-107">Sie können auch die ATP-Informationen des Produkts überprüfen, in denen Sie die ATP-Menge in dem vordefinierten Zeitrahmen finden.</span><span class="sxs-lookup"><span data-stu-id="3e029-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="3e029-108">Verfügbarer Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="3e029-108">On-hand inventory</span></span>

<span data-ttu-id="3e029-109">In der Kopfzeile der Seiten **Angebote**, **Aufträge** und **Rechnungen** in Dynamics 365 Sales wurde eine neue Schaltfläche **Lagerbestand** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3e029-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="3e029-110">Wenn Sie auf die Schaltfläche klicken, wird ein Dialogfeld angezeigt, in dem Sie das Unternehmen und das Produkt angeben können, für das Sie dann den Lagerbestand überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="3e029-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="3e029-111">Dieses Dialogfeld zeigt die gleichen Informationen wie [Lagerbestand](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="3e029-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="3e029-112">Das Dialogfeld gibt die Inventarinformationen von Dynamics 365 Supply Chain Management zurück.</span><span class="sxs-lookup"><span data-stu-id="3e029-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3e029-113">Diese Informationen umfassen die folgenden Mengen:</span><span class="sxs-lookup"><span data-stu-id="3e029-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="3e029-114">Verfügbare Menge</span><span class="sxs-lookup"><span data-stu-id="3e029-114">On-hand quantity</span></span>
- <span data-ttu-id="3e029-115">Die verfügbare Menge in Reserve</span><span class="sxs-lookup"><span data-stu-id="3e029-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="3e029-116">Die verfügbare Menge</span><span class="sxs-lookup"><span data-stu-id="3e029-116">Available on-hand quantity</span></span>
- <span data-ttu-id="3e029-117">Bestellte Menge</span><span class="sxs-lookup"><span data-stu-id="3e029-117">Ordered quantity</span></span>
- <span data-ttu-id="3e029-118">Die Auftragsmenge</span><span class="sxs-lookup"><span data-stu-id="3e029-118">On-order quantity</span></span>
- <span data-ttu-id="3e029-119">Reservierte bestellte Menge</span><span class="sxs-lookup"><span data-stu-id="3e029-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="3e029-120">Die insgesamt verfügbare Menge</span><span class="sxs-lookup"><span data-stu-id="3e029-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="3e029-121">VfZ-Informationen</span><span class="sxs-lookup"><span data-stu-id="3e029-121">ATP information</span></span>

<span data-ttu-id="3e029-122">In Sales wurde eine neue Schaltfläche **ATP-Informationen** wurde zu den Seite **Zitate**, **Aufträge**, und **Rechnungen** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3e029-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="3e029-123">Wenn Sie auf diese Schaltfläche klicken, wird ein Dialogfeld angezeigt, in dem Sie das Unternehmen, Produkt, Lagerstandort, Lagerbestand und bestellte Menge angeben können..</span><span class="sxs-lookup"><span data-stu-id="3e029-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="3e029-124">Dieses Dialogfeld hat dieselben Einstellungen wie in [Bestellung vielversprechend](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="3e029-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="3e029-125">Das Dialogfeld gibt die ATP-Informationen aus dem Supply Chain Management zurück.</span><span class="sxs-lookup"><span data-stu-id="3e029-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="3e029-126">Diese Informationen umfassen die folgenden Mengen:</span><span class="sxs-lookup"><span data-stu-id="3e029-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="3e029-127">VfZ-Menge</span><span class="sxs-lookup"><span data-stu-id="3e029-127">ATP quantity</span></span>
- <span data-ttu-id="3e029-128">Zugangsmenge</span><span class="sxs-lookup"><span data-stu-id="3e029-128">Receipt quantity</span></span>
- <span data-ttu-id="3e029-129">Abgangsmenge</span><span class="sxs-lookup"><span data-stu-id="3e029-129">Issue quantity</span></span>
- <span data-ttu-id="3e029-130">Verfügbare Menge</span><span class="sxs-lookup"><span data-stu-id="3e029-130">On-hand quantity</span></span>