---
title: Beheben von Abweichungen beim Abgleich von Rechnungssummen
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f7e1261838866688c97529b0edfa1354034247b
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="7b1a6-102">Beheben von Abweichungen beim Abgleich von Rechnungssummen</span><span class="sxs-lookup"><span data-stu-id="7b1a6-102">Resolve discrepancies during invoice totals matching</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="7b1a6-103">Ein Typ der Rechnungsabgleichüberprüfung ist der Rechnungssummenabgleich.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-103">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="7b1a6-104">Um anzugeben, dass das System einen Rechnungssummenabgleich ausführen soll, legen Sie auf der Seite **Kreditorenkontenparameter** auf der Registerkarte **Rechnungsprüfung** die **Rechnungssummen abgleichen**-Option auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-104">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="7b1a6-105">Mit dem Rechnungssummenabgleich können Sie sicherstellen, dass die Abweichung der Gesamtbeträge in Rechnungen von den erwarteten Beträgen in einem akzeptablen Rahmen bleibt.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-105">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="7b1a6-106">Sechs Summen werden auf der Seite **Detailabgleich für Rechnungssummen** verglichen.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-106">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="7b1a6-107">Weicht irgendeine der Summen von der erwarteten entsprechenden Bestellungssumme ab, wird eine Abgleichsabweichung markiert.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-107">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="7b1a6-108">Um die Rechnung zu prüfen, die die Summenabgleichsabweichungen aufweist, klicken Sie im Arbeitsbereich, **Kreditorenrechnungseintrag** auf die Kachel **Ausstehende Rechnungen**.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-108">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="7b1a6-109">Klicken Sie dann im Aktivitätsbereich auf der Registerkarte **Prüfen** auf **Detailabgleich**.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-109">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="7b1a6-110">Wenn Abgleichsabweichungen erfasst wurden, werden Warnsymbole neben dem Rechnungsbetrag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-110">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="7b1a6-111">Sie können weitere Details zu den Summen anzeigen, indem Sie den Detailabgleich für Rechnungssummen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-111">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="7b1a6-112">Sollten Sie nach Erkennung der Abweichung der Meinung sein, die Abweichung sei auf fehlerhafte Rechnungsinformationen zurückzuführen, müssen Sie sich möglicherweise mit dem Kreditor in Verbindung setzen.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-112">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="7b1a6-113">Abhängig von der Einigung mit dem Kreditor stehen folgende Möglichkeiten zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="7b1a6-113">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="7b1a6-114">Akzeptieren der Preisabweichung und Buchen der Rechnung mit den Abgleichsabweichungen</span><span class="sxs-lookup"><span data-stu-id="7b1a6-114">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="7b1a6-115">Ihr System kann auch so eingerichtet werden, dass eine Genehmigung vor dem Buchen erforderlich ist, wenn es Abgleichsabweichungen gibt.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-115">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="7b1a6-116">In diesem Fall müssen Sie die Abgleichsabweichung genehmigen und können einen Genehmigungskommentar optional eingeben.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-116">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="7b1a6-117">Sie können dann die Buchung der Rechnung auswählen.</span><span class="sxs-lookup"><span data-stu-id="7b1a6-117">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="7b1a6-118">Ändern des Rechnungsbetrags auf den erwarteten Betrag und Buchen der Rechnung</span><span class="sxs-lookup"><span data-stu-id="7b1a6-118">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="7b1a6-119">Anfordern einer Gutschrift über den vollen Betrag sowie einer neuen korrigierten Rechnung des Kreditors</span><span class="sxs-lookup"><span data-stu-id="7b1a6-119">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="7b1a6-120">Weitere Informationen finden Sie unter [Erforschen oder Beheben von Ausnahmen](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="7b1a6-120">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



