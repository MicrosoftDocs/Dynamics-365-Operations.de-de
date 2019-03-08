---
title: Buchen mit abgeleiteten Büchern
description: Dieser Artikel beschreibt, wie Sie die abgeleiteten Bücher verwenden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff1dbf67a53a5639e448da707898b55cd00cba94
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "339141"
---
# <a name="post-with-derived-books"></a><span data-ttu-id="199de-103">Buchen mit abgeleiteten Büchern</span><span class="sxs-lookup"><span data-stu-id="199de-103">Post with derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="199de-104">Dieser Artikel beschreibt, wie Sie die abgeleiteten Bücher verwenden.</span><span class="sxs-lookup"><span data-stu-id="199de-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="199de-105">Beim Buchen einer Transaktion für ein Buch, das abgeleitete Bücher enthält, werden die Transaktionen für das abgeleitete Buch automatisch aus Erfassungen, Bestellungen oder Freitextrechnungen gebucht.</span><span class="sxs-lookup"><span data-stu-id="199de-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="199de-106">Wenn Sie die primären Buchtransaktionen in der Anlagenerfassung vorbereiten, können Sie die Beträge der abgeleiteten Buchungen anzeigen und ändern, bevor diese gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="199de-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="199de-107">Bestimmte Konten wie Mehrwertsteuer-, Debitoren- oder Kreditorenkonten werden nur einmal durch Buchung des primären Buchs aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="199de-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="199de-108">Buchungen für Transaktionen im abgeleiteten Buch erfolgen auf Konten, die hierfür auf der Seite Anlagenbuchungsprofile definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="199de-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="199de-109">Akquisitionen werden oftmals als Buchungsart für das abgeleitete Buch verwendet.</span><span class="sxs-lookup"><span data-stu-id="199de-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="199de-110">Diese Buchungsart wird verwendet, wenn das Wertmodell und das abgeleitete Abschreibungsbuch ab dem Zeitpunkt der Anschaffung auf eine Anlage angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="199de-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="199de-111">Für die Buchungsart können auch andere Werte zutreffend sein.</span><span class="sxs-lookup"><span data-stu-id="199de-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="199de-112">Besitzen das primäre Buch und das abgeleitete Buch beispielsweise die gleichen Kauf- oder Abgangsintervalle, stehen bei der Einrichtung eines abgeleiteten Abschreibungsbuchs alle Anlagenbuchungsarten zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="199de-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="199de-113">Der Abschreibungsbetrag, der im abgeleiteten Buch gebucht wird, ist der gleiche wie der für das primäre Buch gebuchte.</span><span class="sxs-lookup"><span data-stu-id="199de-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="199de-114">Wenn die Abschreibungsmethoden zwischen den Büchern unterschiedlich sind, sollten Sie keine Abschreibungsbuchungen mit dem Ableitungsverfahren generieren.</span><span class="sxs-lookup"><span data-stu-id="199de-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="199de-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="199de-115">Example</span></span> 
<span data-ttu-id="199de-116">Nachfolgend wird beschrieben, wie Anschaffungsbuchungen mit der Funktion für abgeleitete Buchfunktionalitäten eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="199de-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="199de-117">Erstellt die Bücher auf der Buchseite.</span><span class="sxs-lookup"><span data-stu-id="199de-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="199de-118">Das Buch für die Buchhaltung: WM 1, aktuelle Buchungsebene</span><span class="sxs-lookup"><span data-stu-id="199de-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="199de-119">Das Buch für steuerliche Zwecke: WM 2, Steuerbuchungsebene</span><span class="sxs-lookup"><span data-stu-id="199de-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="199de-120">Klicken Sie für "VM 1" auf die Registerkarte "Abgeleitete Bücher". Wählen Sie im Feld "Buch" "VM 2" aus und im Feld "Buchungsart" "Anschaffen".</span><span class="sxs-lookup"><span data-stu-id="199de-120">On VM 1, click the Derived books tab. Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="199de-121">Das Buch kann nun bestimmten Anlagen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="199de-121">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="199de-122">Wenn für eine Anlage mit Wertmodell WM 1 eine Anschaffung gebucht wird, wird diese Anschaffung nicht nur für WM 1, sondern auch im abgeleiteten Abschreibungsbuch WM 2 gebucht.</span><span class="sxs-lookup"><span data-stu-id="199de-122">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="199de-123">Der Status beider Anlagenwertbücher wird auf Offen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="199de-123">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="199de-124">Wenn Sie nicht mit abgeleiteten Abschreibungsbüchern arbeiten, müssen Sie die Anschaffung der Anlage sowohl für Buch WM 1 als auch für Abschreibungsbuch WM 2 buchen.</span><span class="sxs-lookup"><span data-stu-id="199de-124">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="199de-125">Weitere Informationen finden Sie unter [Abgeleitete Bücher](derived-books.md).</span><span class="sxs-lookup"><span data-stu-id="199de-125">For more information, see [Derived books](derived-books.md)</span></span>



