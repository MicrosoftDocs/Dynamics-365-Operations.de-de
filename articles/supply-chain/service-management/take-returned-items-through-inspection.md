---
title: Prüfen von zurückgelieferten Artikeln
description: Prüfen von zurückgelieferten Artikeln.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53cb727cc0f001a6ac344d37f25273999f992d8a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974084"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="e41db-103">Prüfen von zurückgelieferten Artikeln</span><span class="sxs-lookup"><span data-stu-id="e41db-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="e41db-104">Klicken Sie auf **Lagerverwaltung** \> **Periodisch** \> **Qualitätsmanagement** \> **Quarantäneaufträge**.</span><span class="sxs-lookup"><span data-stu-id="e41db-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="e41db-105">Suchen Sie nach der Auftragsposition für den zurückgelieferten Artikel, den Sie gerade untersuchen.</span><span class="sxs-lookup"><span data-stu-id="e41db-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="e41db-106">Ein Quarantäneauftrag kann jeweils nur einer Artikelnummer zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="e41db-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="e41db-107">Werden im Rahmen einer einzelnen Lieferung zehn Artikel mit unterschiedlicher Artikelnummer zurückgesendet und in Quarantäne geschickt, werden zehn einzelne Quarantäneaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="e41db-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="e41db-108">Geben Sie nach der Untersuchung des Artikels im Feld **Dispositionscode** an, wie mit dem Artikel und mit der zugehörigen wertmäßigen Buchung verfahren werden soll.</span><span class="sxs-lookup"><span data-stu-id="e41db-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="e41db-109">Sie können beispielsweise festlegen, dass der Artikel wieder dem Lager zugeführt werden und der Debitor eine Gutschrift erhalten soll, dass der Artikel verschrottet und ein Ersatzartikel an den Debitor gesendet werden soll oder dass der Artikel ohne Gutschrift an den Kunden zurückgesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e41db-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="e41db-110">Sollte mehreren zurückgelieferten Artikeln eines Stapels mit gleicher Artikelnummer nicht der gleiche Dispositionscode zugewiesen werden können, muss der Quarantäneauftrag aufgeteilt werden (unter <STRONG>Funktionen</STRONG> &gt; <STRONG>Teilen</STRONG>), um den einzelnen Teilmengen jeweils einen eigenen Dispositionscode zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="e41db-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="e41db-111">Klicken Sie nach Abschluss der Untersuchung auf **Fertigmeldung**, um die zurückgelieferten Artikel freizugeben und einen entsprechenden Eintrag für die Wareneingangserfassung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e41db-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="e41db-112">Die Erfassung wird dann von der Person oder Abteilung verarbeitet, von der die Artikel entgegengenommen werden, damit die Artikel wieder dem Bestand zugeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e41db-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="e41db-113">- oder -</span><span class="sxs-lookup"><span data-stu-id="e41db-113">–or–</span></span>
    
    <span data-ttu-id="e41db-114">Beenden Sie den Quarantäneauftrag, und führen Sie die Artikel direkt mithilfe einer der Funktionen für **Lagerartikel** wieder dem Bestand zu.</span><span class="sxs-lookup"><span data-stu-id="e41db-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="e41db-115">Schließen Sie das Formular, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e41db-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="e41db-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e41db-116">See also</span></span>

[<span data-ttu-id="e41db-117">Angeben zur Entsorgung zurückgelieferter Artikel</span><span class="sxs-lookup"><span data-stu-id="e41db-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  


