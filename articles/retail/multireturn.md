---
title: Artikel über mehrere Debitorenaufträgen und Rechnungen zurückgeben
description: In diesem Thema werden die Funktionen erläutert, um Rücklieferungen über mehrere Debitorenaufträgen und Rechnungen in Dynamics 365 Retail zu ermöglichen.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017988"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="0209b-103">Artikel über mehrere Debitorenaufträgen und Rechnungen zurückgeben</span><span class="sxs-lookup"><span data-stu-id="0209b-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="0209b-104">Rücklieferungen können über mehrere Aufträge und Rechnungen erfolgen.</span><span class="sxs-lookup"><span data-stu-id="0209b-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="0209b-105">Retail konfigurieren, um Rücklieferungen für mehrere Debitorenaufträge und Rechnungen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="0209b-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="0209b-106">Wechseln Sie zu **Retail-Parameter \> Debitorenaufträge**.</span><span class="sxs-lookup"><span data-stu-id="0209b-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="0209b-107">Aktivieren Sie den Parameter **Rücklieferungen für mehrere Aufträge aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="0209b-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="0209b-108">Rücklieferungen verarbeiten</span><span class="sxs-lookup"><span data-stu-id="0209b-108">Process returns</span></span>

<span data-ttu-id="0209b-109">Nachdem der Parameter aktiviert und die Änderungen mit den Shops synchronisiert wurden, kann der Kassierer im Shop mehrere Aufträge für einen Debitor zur Rücklieferung auswählen.</span><span class="sxs-lookup"><span data-stu-id="0209b-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="0209b-110">Wenn die Aufträge ausgewählt werden, wird eine Liste aller retournierbaren Produkte für alle Rechnungen des Auftrags angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0209b-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="0209b-111">Der Kassierer kann dann die Produkte auswählen, die retourniert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0209b-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="0209b-112">Es wird ein einzelner Rücklieferungsauftrag für alle ausgewählten Produkte erstellt.</span><span class="sxs-lookup"><span data-stu-id="0209b-112">A single return order will be created for all the selected products.</span></span>
