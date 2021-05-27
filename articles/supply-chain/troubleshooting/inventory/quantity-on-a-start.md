---
title: Die Menge eines begonnen Quarantäneauftrags wird nicht aktualisiert, wenn der Auftrag aufgeteilt wird
description: Wenn Sie einen Quarantäneauftrag anlegen und versuchen, ihn aufzuteilen, wird die Auftragsmenge nicht auf die nach der Aufteilung verbleibende Menge aktualisiert.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026554"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="33822-103">Die Menge eines begonnen Quarantäneauftrags wird nicht aktualisiert, wenn der Auftrag aufgeteilt wird</span><span class="sxs-lookup"><span data-stu-id="33822-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="33822-104">KB-Nummer: 4613113</span><span class="sxs-lookup"><span data-stu-id="33822-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="33822-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="33822-105">Symptoms</span></span>

<span data-ttu-id="33822-106">Wenn Sie einen Quarantäneauftrag anlegen und versuchen, ihn aufzuteilen, wird die Auftragsmenge nicht auf die nach der Aufteilung verbleibende Menge aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="33822-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="33822-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="33822-107">Resolution</span></span>

<span data-ttu-id="33822-108">Das System ändert die ursprüngliche Menge aus einem Quarantäneauftrag nicht, um sicherzustellen, dass Sie die ursprüngliche Menge verfolgen können, die für diesen Quarantäneauftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="33822-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="33822-109">Das System verfolgt jedoch die Menge, die von einem Quarantäneauftrag abgetrennt wird.</span><span class="sxs-lookup"><span data-stu-id="33822-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="33822-110">Für diese Verfolgung wird ein Datenbankfeld mit dem Namen `QuantityThatHasSplitIntoOtherQuarantineOrders` verwendet.</span><span class="sxs-lookup"><span data-stu-id="33822-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="33822-111">Dieses Feld ist jedoch auf der Benutzeroberfläche (UI) nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="33822-111">However, this field isn't visible in the user interface (UI).</span></span>
