---
title: Stornierte Produktzugänge aktualisieren den Status der Transaktion nicht auf Registriert
description: Nachdem Sie Produktzugänge bei einer eingehenden Ladung storniert haben, aktualisiert das System automatisch den Status der Transaktion im Bestand von „Erhalten“ auf „Bestellt“.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294081"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="1acd4-103">Stornierte Produktzugänge aktualisieren den Status der Transaktion nicht auf Registriert</span><span class="sxs-lookup"><span data-stu-id="1acd4-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="1acd4-104">Symptome</span><span class="sxs-lookup"><span data-stu-id="1acd4-104">Symptoms</span></span>

<span data-ttu-id="1acd4-105">Nachdem Sie die Aktion **Produktzugänge stornieren** bei einer eingehenden Ladung ausgeführt haben, aktualisiert das System automatisch den Status der Bestandstransaktionen von *Eingegangen* auf *Bestellt*.</span><span class="sxs-lookup"><span data-stu-id="1acd4-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="1acd4-106">Lösung</span><span class="sxs-lookup"><span data-stu-id="1acd4-106">Resolution</span></span>

<span data-ttu-id="1acd4-107">Wenn Lieferscheine für ausgehende Ladungen storniert werden, bleibt der Status von Bestandstransaktionen *Kommissioniert*.</span><span class="sxs-lookup"><span data-stu-id="1acd4-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="1acd4-108">Wenn jedoch Produktzugänge von einer eingehenden Ladung storniert werden, wird der Status von Bestandstransaktionen nicht auf *Registriert* zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1acd4-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="1acd4-109">Daher muss die Arbeitskraft am Lagerort nach der Stornierung eines Produktzugangs aus einer eingehenden Ladung die Artikelmengen für die Ladungen neu registrieren.</span><span class="sxs-lookup"><span data-stu-id="1acd4-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="1acd4-110">Weitere Informationen finden Sie unter [Artikelmengen registrieren, die mit einer eingehenden Ladung ankommen](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span><span class="sxs-lookup"><span data-stu-id="1acd4-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
