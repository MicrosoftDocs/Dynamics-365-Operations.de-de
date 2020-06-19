---
title: Inventarverfügbarkeit in dualem Schreiben
description: Dieses Thema bietet Informationen über das Prüfen der Bestandverfügbarkeit in dualem Schreiben.
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
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426981"
---
# <a name="inventory-availability"></a><span data-ttu-id="4a2b9-103">Verfügbarkeit des Bestands</span><span class="sxs-lookup"><span data-stu-id="4a2b9-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="4a2b9-104">Mithilfe der Bestandverfügbarkeit können Sie Ihr Inventar überprüfen, bevor Sie ein Produkt zu den Formularen **Zitate**, **Aufträge** oder **Rechnungen** in modellgesteuerten Apps in Dynamics 365 hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4a2b9-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="4a2b9-105">Zum Beispiel ist die Überprüfung des Inventars und die Bestimmung eines Erfüllungstermins eine Schlüsselaufgabe im [Aussicht auf Bargeld](dual-write-prospect-to-cash.md) Prozess.</span><span class="sxs-lookup"><span data-stu-id="4a2b9-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="4a2b9-106">Wenn Sie nicht über genügend Bestandr verfügen, können Sie einen Liefertermin basierend auf den projizierten Bestandeinnahmen und -Problemen schätzen.</span><span class="sxs-lookup"><span data-stu-id="4a2b9-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="4a2b9-107">Sie können auch die ATP-Informationen des Produkts überprüfen, in denen Sie die ATP-Menge im vordefinierten Zeitrahmen finden.</span><span class="sxs-lookup"><span data-stu-id="4a2b9-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="4a2b9-108">Verfügbarer Bestand</span><span class="sxs-lookup"><span data-stu-id="4a2b9-108">On-hand Inventory</span></span> 

<span data-ttu-id="4a2b9-109">In der Kopfzeile des Formales **Angebote**, **Aufträge**, oder **Rechnungen** in Dynamics 365 Sales wurde eine neue Schaltfläche **Lagerbestand** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4a2b9-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="4a2b9-110">Wenn Sie auf die Schaltfläche klicken, wird ein Dialogfeld angezeigt, in dem Sie das Unternehmen und das Produkt angeben können, für das Sie den Lagerbestand überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="4a2b9-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="4a2b9-111">Es gibt die Bestandinformationen von Dynamics 365 Supply Chain Management zurück und zeigt die gleichen Informationen wie [Lagerbestand](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="4a2b9-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="4a2b9-112">Die Informationen enthalten diese Mengen:</span><span class="sxs-lookup"><span data-stu-id="4a2b9-112">The information includes these quantities:</span></span>

- <span data-ttu-id="4a2b9-113">**Verfügbare Menge**</span><span class="sxs-lookup"><span data-stu-id="4a2b9-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="4a2b9-114">**Verfügbare Menge in Reserve**</span><span class="sxs-lookup"><span data-stu-id="4a2b9-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="4a2b9-115">**Verfügbare Menge**</span><span class="sxs-lookup"><span data-stu-id="4a2b9-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="4a2b9-116">**Bestellte Menge**</span><span class="sxs-lookup"><span data-stu-id="4a2b9-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="4a2b9-117">**Auftragsmenge**</span><span class="sxs-lookup"><span data-stu-id="4a2b9-117">**On-order Quantity**</span></span>
- <span data-ttu-id="4a2b9-118">**Reservierte bestellte Menge**</span><span class="sxs-lookup"><span data-stu-id="4a2b9-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="4a2b9-119">**Insgesamt verfügbare Menge**</span><span class="sxs-lookup"><span data-stu-id="4a2b9-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="4a2b9-120">VfZ-Informationen</span><span class="sxs-lookup"><span data-stu-id="4a2b9-120">ATP information</span></span>

<span data-ttu-id="4a2b9-121">Bei Zeilenartikeln in den Formularen **Angebote**, **Aufträge**, oder **Rechnungen** in Dynamics 365 Sales wurde eine neue Schaltfläche **Lagerbestand** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4a2b9-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="4a2b9-122">Wenn Sie auf die Schaltfläche klicken, wird ein Dialogfeld angezeigt, in dem Sie das Unternehmen, Produkt, Lagerstandort, Lagerbestand und bestellte Menge angeben können..</span><span class="sxs-lookup"><span data-stu-id="4a2b9-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="4a2b9-123">Es gibt die **VIZ-Informationen** aus dem Supply Chain Management zurück und zeigt die Einstellungen, die in [vielversprechende Bestellung](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="4a2b9-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="4a2b9-124">Die Informationen umfassen **VfZ-Menge**, **Belegmenge**, **Ausgabemenge**, und **Verfügbare Menge**.</span><span class="sxs-lookup"><span data-stu-id="4a2b9-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
