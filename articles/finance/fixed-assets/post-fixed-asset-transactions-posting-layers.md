---
title: Buchen von Anlagenbuchungen auf Buchungsebenen
description: Dieser Artikel gibt eine Übersicht über das Buchen von Ebenenfunktionen für Anlagenbuchungen.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc8c4f4f41ed39447ae441dd8e01cfcf80c939b5
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770711"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="cff47-103">Buchen von Anlagenbuchungen auf Buchungsebenen</span><span class="sxs-lookup"><span data-stu-id="cff47-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cff47-104">Dieser Artikel gibt eine Übersicht über das Buchen von Ebenenfunktionen für Anlagenbuchungen.</span><span class="sxs-lookup"><span data-stu-id="cff47-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="cff47-105">Eine Anlage wird für unterschiedliche Zwecke häufig mit unterschiedlichen Methoden abgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="cff47-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="cff47-106">Die Abschreibung zu steuerlichen Zwecken wird anhand der aktuellen Steuerregeln berechnet, um die höchstmögliche Abschreibung vor Steuern zu erreichen, wohingegen die Abschreibung zu Berichtszwecken entsprechend den Buchhaltungsgesetzen und -standards berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="cff47-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="cff47-107">Die unterschiedlichen Abschreibungsarten werden auf den Buchungsebenen separat berechnet und aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cff47-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="cff47-108">Jedes Buch, das einer Anlage zugeordnet ist, wird für eine bestimmte Buchungsebene eingerichtet, die ein übergeordnetes Abschreibungsziel aufweist.</span><span class="sxs-lookup"><span data-stu-id="cff47-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="cff47-109">Es gibt zehn Buchungsebenen: Aktuelle, Vorgänge, Steuern und sieben benutzerdefinierte Ebenen.</span><span class="sxs-lookup"><span data-stu-id="cff47-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="cff47-110">Sie können Buchungen im Hauptbuch für das Buch deaktivieren, indem Sie das Feld Ins Hauptbuch buchen auf Nein festlegen.</span><span class="sxs-lookup"><span data-stu-id="cff47-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="cff47-111">Das Feld Buchungsebene wird dann automatisch auf Keine gesetzt.</span><span class="sxs-lookup"><span data-stu-id="cff47-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="cff47-112">Bücher, die nicht im Hauptbuch buchen, werden in der Regel für die Steuererklärung verwendet.</span><span class="sxs-lookup"><span data-stu-id="cff47-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="cff47-113">Dies bietet zusätzliche Flexibilität zur Löschung von historischen Buchungen für das Anlagenbuch, da sie nicht im Hauptbuch eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="cff47-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="cff47-114">Anlagenerfassungen definieren sich durch die Nutzung der Seite  Journalnamen unter Hauptbuch > Journaleinrichtung > Journalnamen.</span><span class="sxs-lookup"><span data-stu-id="cff47-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="cff47-115">Jede Erfassung, in der Sie Abschreibungen buchen können, wird anhand des Erfassungsnamens (Journal) für eine einzelne Buchungsebene definiert.</span><span class="sxs-lookup"><span data-stu-id="cff47-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="cff47-116">Die Buchungsebene kann im Journal nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cff47-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="cff47-117">Diese Einschränkung hilft sicherzustellen, dass Buchungen für die einzelnen Buchungsebenen getrennt gehalten werden.</span><span class="sxs-lookup"><span data-stu-id="cff47-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="cff47-118">Für jede Buchungsebene muss mindestens ein Journal angelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cff47-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="cff47-119">Auf wenn Sie Bücher verwenden, die nicht auf das Sachkonto buchen, müssen Sie ein Journal erstellen, bei dem die Buchungsebene auf Kein festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cff47-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="cff47-120">Sie können Sachkonten für Anlagenbuchungen auf der Seite Anlagenbuchungsprofile festlegen.</span><span class="sxs-lookup"><span data-stu-id="cff47-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="cff47-121">Sie müssen für jedes Buchungsprofil die relevante Buchungsart und das Buch auswählen und können dann die Sachkonten angeben.</span><span class="sxs-lookup"><span data-stu-id="cff47-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="cff47-122">Einrichten eines Buchungsprofildatensatz für jedes Buch, das im Hauptbuch gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="cff47-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

> [!NOTE] 
> <span data-ttu-id="cff47-123">Bei Verwendung von abgeleiteten Büchern können Buchungen gleichzeitig auf unterschiedlichen Buchungsebenen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cff47-123">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="cff47-124">Sie erstellen die Buchungen des primären Buchs in einem Journal mit der Buchungsebene, die der Buchungsebene des Wertmodells entspricht.</span><span class="sxs-lookup"><span data-stu-id="cff47-124">You create the transactions of the primary book in a journal where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="cff47-125">Beim Buchen werden die Buchungen der abgeleiteten Buchtransaktionen dann auf den entsprechenden Buchungsebenen gebucht.</span><span class="sxs-lookup"><span data-stu-id="cff47-125">During posting, the derived book transactions are posted to the appropriate posting layers.</span></span>

<span data-ttu-id="cff47-126">Weitere Informationen finden Sie unter [Abgeleitete Bücher](derived-books.md) und [Post mit abgeleiteten Büchern](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="cff47-126">For more information see, [Derived books](derived-books.md) and [Post with derived books](post-derived-value-models.md).</span></span>



