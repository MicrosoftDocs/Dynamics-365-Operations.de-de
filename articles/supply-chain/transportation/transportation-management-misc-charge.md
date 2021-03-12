---
title: Transportverwaltung - Sonstige Kosten
description: In diesem Thema wird erklärt, wie die durch den Transport erzeugten Gebühren mit einem Gebührencode verknüpft werden müssen.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cb503072fb76e04aa01ff2d231c756eeb244c65a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004700"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="874af-103">Transportverwaltung - Sonstige Kosten</span><span class="sxs-lookup"><span data-stu-id="874af-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="874af-104">Wie alle anderen Gebühren müssen auch die vom Transport erzeugten Gebühren mit einem Gebührencode verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="874af-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="874af-105">Andernfalls werden sie dem Auftrag nicht als sonstige Kosten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="874af-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="874af-106">Der **Gebührencode** bestimmt, wie die Gebühr in Bezug auf den Auftrag und die Auftragszeile, in der sie hinzugefügt wird, verbucht wird.</span><span class="sxs-lookup"><span data-stu-id="874af-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="874af-107">Gehen Sie zu **Transportverwaltung > Einrichten > Bewertung > Diverse Gebühren**, um die Qualifizierungskriterien zu definieren, die bestimmen, wann ein bestimmter **Gebührencode** auf eine Gebühr angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="874af-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="874af-108">Sie sollten mindestens eine Einrichtung für jede relevante **Gebührenmodul**-Einstellung (*Kunde* und *Lieferant*) haben, bei der die **Gebührenart Sonstiges** auf *Keine* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="874af-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="874af-109">Fehlt diese Angabe, wird die Zusatzgebühr *nicht* zur Bestellung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="874af-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>
