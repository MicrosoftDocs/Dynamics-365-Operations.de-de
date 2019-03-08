---
title: Abgeleitete Bücher
description: Dieser Artikel enthält eine Übersicht der Funktion für abgeleitete Bücher.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 153b6437205d5a849fa6a90c0d3b9f3d51dd6768
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "313910"
---
# <a name="derived-books"></a><span data-ttu-id="15df6-103">Abgeleitete Bücher</span><span class="sxs-lookup"><span data-stu-id="15df6-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15df6-104">Dieser Artikel enthält eine Übersicht der Funktion für abgeleitete Bücher.</span><span class="sxs-lookup"><span data-stu-id="15df6-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="15df6-105">Abgeleitete Wertmodelle sollen Wertmodellbuchungen für Anlagen vereinfachen, die in regelmäßigen Zeitabständen erfolgen.</span><span class="sxs-lookup"><span data-stu-id="15df6-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="15df6-106">Sie wählen ein Buch als primäres Buch aus.</span><span class="sxs-lookup"><span data-stu-id="15df6-106">You choose one book as the primary book.</span></span> <span data-ttu-id="15df6-107">Dies ist üblicherweise das Buch für die buchhalterische Abschreibung.</span><span class="sxs-lookup"><span data-stu-id="15df6-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="15df6-108">Anschließend werden diesem Buch andere Bücher zugeordnet, die für Buchungen in den gleichen Intervallen eingerichtet werden wie das primäre Buch.</span><span class="sxs-lookup"><span data-stu-id="15df6-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="15df6-109">Bücher für steuerliche Abschreibung werden oft als abgeleitete Bücher eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="15df6-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="15df6-110">Die häufigsten Posten, die zum Buchen in abgeleitete Abschreibungsbücher eingerichtet werden, sind Anschaffungen, Anschaffungsänderungen und Veräußerungen.</span><span class="sxs-lookup"><span data-stu-id="15df6-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="15df6-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="15df6-111">Example</span></span>

<span data-ttu-id="15df6-112">Buch B und Buch C werden als abgeleitete Bücher für Buch für A die Buchungsart "Anschaffung" eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="15df6-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="15df6-113">Im Buch A wird eine Anschaffungsbuchung für die Anlage 123 mit einem Wert von 1.500,00 Einheiten eingegeben.</span><span class="sxs-lookup"><span data-stu-id="15df6-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="15df6-114">Beim Buchen wird eine Anschaffungsbuchung in der Anlage 123 für das Buch B und in der Anlage 123 für das Buch C mit einem Wert von 1.500,00 Einheiten generiert und gebucht.</span><span class="sxs-lookup"><span data-stu-id="15df6-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="15df6-115">Wenn Sie die Buchungen des primären Buchs in der Anlagenerfassung zur Ausführung vorbereiten, können Sie auch die Buchungen der abgeleiteten Abschreibungsbücher anzeigen und ändern.</span><span class="sxs-lookup"><span data-stu-id="15df6-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="15df6-116">Wenn Sie die Buchungen des primären Buchs in einer anderen Erfassung vorbereiten, werden die Buchungen des abgeleiteten Werts nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="15df6-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="15df6-117">Sie werden aber beim Buchen der Posten des primären Buchs auf die entsprechenden Konten und Buchungsebenen gebucht.</span><span class="sxs-lookup"><span data-stu-id="15df6-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="15df6-118">Bücher, die zum Buchen von Posten in Intervallen eingerichtet werden, bei denen es sich nicht um die Intervalle des primären Buches handelt, müssen der Anlage als separate Bücher (und nicht als abgeleitete Bücher) zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="15df6-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="15df6-119">Weitere Informationen finden Sie unter [Buchen mit abgeleiteten Büchern](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="15df6-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>



