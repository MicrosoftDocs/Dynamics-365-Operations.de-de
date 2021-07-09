---
title: Element kann keine Stückliste oder Formel haben
description: Wenn Sie versuchen, einen Auftrag zu fixieren, erhalten Sie während der Positionsvalidierung eine Fehlermeldung. Sie besagt, dass das Element keine Stückliste oder Formel haben kann.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294083"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="6f12a-104">Element kann keine Stückliste oder Formel haben</span><span class="sxs-lookup"><span data-stu-id="6f12a-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="6f12a-105">Fehlercode: PRO2614</span><span class="sxs-lookup"><span data-stu-id="6f12a-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="6f12a-106">Symptome</span><span class="sxs-lookup"><span data-stu-id="6f12a-106">Symptoms</span></span>

<span data-ttu-id="6f12a-107">Wenn Sie versuchen, einen Auftrag zu fixieren, erhalten Sie während der Positionsvalidierung die folgende Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="6f12a-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="6f12a-108">Element kann keine Stückliste oder Formel haben</span><span class="sxs-lookup"><span data-stu-id="6f12a-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="6f12a-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="6f12a-109">Resolution</span></span>

<span data-ttu-id="6f12a-110">Elemente, die eine Stückliste oder eine Formel haben, müssen vom Typ *Planungselement*, *Stückliste* oder *Formel* sein.</span><span class="sxs-lookup"><span data-stu-id="6f12a-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="6f12a-111">Um den Typ eines Elements zu ändern, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="6f12a-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="6f12a-112">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="6f12a-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="6f12a-113">Öffnen Sie das entsprechende Produkt.</span><span class="sxs-lookup"><span data-stu-id="6f12a-113">Open the relevant product.</span></span>
1. <span data-ttu-id="6f12a-114">Legen Sie auf dem Inforegister **Ingenieur** das Feld **Produktionstyp** auf *Planungselement*, *Stückliste* oder *Formel* fest.</span><span class="sxs-lookup"><span data-stu-id="6f12a-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>
