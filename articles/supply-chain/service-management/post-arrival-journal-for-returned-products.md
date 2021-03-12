---
title: Buchen der Wareneingangserfassung für zurückgelieferte Produkte
description: Buchen der Wareneingangserfassung für zurückgelieferte Produkte.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 184ce418ff2ec4b891a24b2b75d37b6b4f5d23f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006640"
---
# <a name="post-arrival-journal-for-returned-products"></a><span data-ttu-id="e9fdc-103">Buchen der Wareneingangserfassung für zurückgelieferte Produkte</span><span class="sxs-lookup"><span data-stu-id="e9fdc-103">Post arrival journal for returned products</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e9fdc-104">Prüfen Sie zum Verarbeiten einer Rücklieferung zuerst die Rückgabemenge, und aktualisieren Sie das Mengenfeld in der Wareneingangserfassung.</span><span class="sxs-lookup"><span data-stu-id="e9fdc-104">To process a return, first validate the return quantity, update the quantity field in the item arrival journal.</span></span> <span data-ttu-id="e9fdc-105">Wählen Sie anschließend einen Dispositionscode aus, oder geben Sie an, dass die zurückgelieferten Artikel geprüft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e9fdc-105">Then select a disposition code or indicate that the returned items have to be inspected.</span></span> <span data-ttu-id="e9fdc-106">Nach Ausführung dieser Schritte kann die Wareneingangserfassung für die Rücklieferung gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="e9fdc-106">After completing these steps, you can post the item arrival journal for the return order.</span></span>

1.  <span data-ttu-id="e9fdc-107">Klicken Sie auf **Lagerverwaltung** \> **Periodisch** \> **Wareneingangsübersicht**.</span><span class="sxs-lookup"><span data-stu-id="e9fdc-107">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="e9fdc-108">Im **Setupname** Filter wählen Sie **Rücklieferung** aus.</span><span class="sxs-lookup"><span data-stu-id="e9fdc-108">In the **Setup name** filter, select **Return order**.</span></span>

3.  <span data-ttu-id="e9fdc-109">Wenn die Liste der Zugänge lang ist, schränken Sie die Liste mithilfe der Felder im Bereich **Bereich** ein.</span><span class="sxs-lookup"><span data-stu-id="e9fdc-109">If the list of receipts is long, use the fields in the **Range** area to narrow the list.</span></span>

4.  <span data-ttu-id="e9fdc-110">Suchen Sie die Position der Rücklieferung, die gebucht werden soll, aktivieren Sie das entsprechende Feld **Für Wareneingang auswählen**, und klicken Sie dann auf **Wareneingang starten**.</span><span class="sxs-lookup"><span data-stu-id="e9fdc-110">Locate the line of the return order that you want to post, select its **Select for arrival** box, and then click **Start arrival**.</span></span>

5.  <span data-ttu-id="e9fdc-111">Klicken Sie **Erfassungen** \> **Wareneingänge aus Zugängen anzeigen**, um das Formular **Lagerplatzerfassung** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e9fdc-111">Click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="e9fdc-112">Wählen Sie eine Erfassung aus, und klicken Sie auf <STRONG>Positionen</STRONG>, um detaillierte Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e9fdc-112">To view detailed information, select a journal, and then click <STRONG>Lines</STRONG>.</span></span></P>


6.  <span data-ttu-id="e9fdc-113">Nehmen Sie erforderliche Aktualisierungen vor, und klicken Sie anschließend auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="e9fdc-113">Make any necessary updates, and then click **Post**.</span></span>

<span data-ttu-id="e9fdc-114">Nach der Buchung der Erfassung werden die zurückgelieferten Artikel im Lagerbestand erfasst, und im Formular **Rücksendungen** wird angezeigt, dass die Artikel am Lagerort eingegangen sind.</span><span class="sxs-lookup"><span data-stu-id="e9fdc-114">After the journal is posted, the returned items are registered in inventory, and the **Return orders** form indicates that the items have arrived at the warehouse.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9fdc-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9fdc-115">See also</span></span>

<span data-ttu-id="e9fdc-116">[Formular "Lagerplatzerfassung"](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="e9fdc-116">[Location journal (form)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span></span>

  


