---
title: Die Produktprogrammplanung generiert geplante Aufträge für Phantomprodukte
description: Nach Durchführung der Produktprogrammplanung werden geplante Aufträge für Phantomprodukte generiert.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026548"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="a4fd6-103">Die Produktprogrammplanung generiert geplante Aufträge für Phantomprodukte</span><span class="sxs-lookup"><span data-stu-id="a4fd6-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="a4fd6-104">KB-Nummer: 4614729</span><span class="sxs-lookup"><span data-stu-id="a4fd6-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="a4fd6-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="a4fd6-105">Symptoms</span></span>

<span data-ttu-id="a4fd6-106">Nach Durchführung der Produktprogrammplanung werden geplante Aufträge für Phantomprodukte generiert.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="a4fd6-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="a4fd6-107">Resolution</span></span>

<span data-ttu-id="a4fd6-108">Die Einstellung der Option **Phantom** für freigegebene Produkte bestimmt den standardmäßigen Positionstyp in der Stückliste.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="a4fd6-109">Wenn die Option **Phantom** auf *Ja* gesetzt ist, erstellt das System weiterhin geplante Aufträge für den Artikel, aber die Option **Direkt abgeleitete Anforderung** wird für jeden geplanten Auftrag auf *Ja* gesetzt.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="a4fd6-110">Daher kann der geplante Produktionsauftrag nicht allein umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="a4fd6-111">Stattdessen wird er immer automatisch aufgenommen, wenn der übergeordnete Produktionsauftrag bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="a4fd6-112">Zusätzlich werden die Stücklistenpositionen des geplanten Phantomauftrags in die Stückliste des übergeordneten Produktionsauftrags aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="a4fd6-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
