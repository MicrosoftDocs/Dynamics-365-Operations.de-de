---
title: Erstellen eines Artikelersetzungsauftrags
description: Aufträge für die Ersetzung von Artikeln werden normalerweise nach der Rückgabe und Prüfung eines Produkts erstellt.
author: josaw1
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95227bbcb71a4c446b9d10cc0447bf2e64c6ef80
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840508"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="25b3d-103">Erstellen eines Artikelersetzungsauftrags</span><span class="sxs-lookup"><span data-stu-id="25b3d-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="25b3d-104">Aufträge für die Ersetzung von Artikeln werden normalerweise nach der Rückgabe und Prüfung eines Produkts erstellt.</span><span class="sxs-lookup"><span data-stu-id="25b3d-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="25b3d-105">Wenn jedoch ein Artikel ersetzt werden muss, bevor er zurückgegeben wurde, oder wenn der Originalartikel nicht zurückgegeben wird, können Sie einen Auftrag für die Ersetzung des Artikels sofort nach dem Erstellen einer Rücklieferung erstellen.</span><span class="sxs-lookup"><span data-stu-id="25b3d-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="25b3d-106">Erstellen eines Ersetzungsauftrags, nachdem Sie einen Artikel erhalten haben, der zurückgegeben wurde</span><span class="sxs-lookup"><span data-stu-id="25b3d-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="25b3d-107">Klicken auf **Vertrieb und Marketing** \> **Gemeinsam** \> **Rücklieferungen** \> **Alle Rücklieferungen**.</span><span class="sxs-lookup"><span data-stu-id="25b3d-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="25b3d-108">Erstellen Sie eine neue Rücklieferung, oder wählen Sie einen zurückgegebenen Auftrag aus der Liste aus, um das Formular **Rücklieferung - RMA-Nummer: %1, %2** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="25b3d-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="25b3d-109">Klicken Sie **Rücklieferungsposition** und wählen Sie anschließend **Wiederbeschaffungsartikel** aus.</span><span class="sxs-lookup"><span data-stu-id="25b3d-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="25b3d-110">Wählen Sie den Artikel aus, durch den der zurückgelieferten Artikel ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="25b3d-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="25b3d-111">Geben Sie die Artikelspezifikationen ein, und klicken Sie anschließend auf **Übernehmen**.</span><span class="sxs-lookup"><span data-stu-id="25b3d-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="25b3d-112">Klicken Sie auf **Lieferschein**, um den Lieferschein für die Rücklieferung zu generieren.</span><span class="sxs-lookup"><span data-stu-id="25b3d-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="25b3d-113">Ein Auftrag wird für den Ersetzungsartikel generiert, den Sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="25b3d-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="25b3d-114">Nachdem der Auftrag für den Ersetzungsartikel erstellt wurde, werden Kaufverträge automatisch durchsucht, und wenn es einen entsprechenden Kaufvertrag gibt, wird dieser für den Auftrag übernommen.</span><span class="sxs-lookup"><span data-stu-id="25b3d-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="25b3d-115">Erstellen Sie einen Ersetzungsauftrag, bevor Sie einen Artikel erhalten, der zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="25b3d-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="25b3d-116">Klicken auf **Vertrieb und Marketing** \> **Gemeinsam** \> **Rücklieferungen** \> **Alle Rücklieferungen**.</span><span class="sxs-lookup"><span data-stu-id="25b3d-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="25b3d-117">Erstellen Sie eine neue Rücklieferung, oder wählen Sie einen zurückgegebenen Auftrag aus der Liste aus, um das Formular **Rücklieferung - RMA-Nummer: %1, %2** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="25b3d-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="25b3d-118">Klicken Sie auf **Auftrag suchen**, wenn Sie den Auftrag für den zurückgelieferten Artikel ermitteln möchten.</span><span class="sxs-lookup"><span data-stu-id="25b3d-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="25b3d-119">Schließen Sie das Formular **Auftrag suchen** ab, und klicken Sie auf **OK**, um das Formular zu schließen und zum Formular **Rücklieferung - RMA-Nummer: %1, %2** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="25b3d-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="25b3d-120">Die Auftragsposition für den zurückgelieferten Artikel wird zur Rücklieferung kopiert.</span><span class="sxs-lookup"><span data-stu-id="25b3d-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="25b3d-121">Klicken Sie auf **Ersatzauftrag**, um das Formular **Auftrag erstellen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="25b3d-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="25b3d-122">Aktivieren Sie das Kontrollkästchen **Rücklieferungspositionen kopieren**, um Details aus der im Formular **Rücklieferung - RMA-Nummer: %1, %2** ausgewählten Rücklieferung in diesen Auftrag zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="25b3d-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="25b3d-123">Geben Sie ggf. Details ein oder ändern Sie diese.</span><span class="sxs-lookup"><span data-stu-id="25b3d-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="25b3d-124">Wenn Sie den Auftrag in Schritt 3 identifiziert haben und wenn die Auftragsposition für den zurückgelieferten Artikel mit einem Kaufvertrag verknüpft ist, wird die Kennung des entsprechenden Kaufvertrags für den Artikelersetzungsauftrags automatisch im Feld **Kaufvertragskennung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="25b3d-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="25b3d-125">Klicken Sie auf **OK**, um das Formular **Auftrag erstellen** zu schließen und das Formular **Auftrag** zu öffnen, in dem der Vorgang fortgesetzt werden kann, um Informationen für den neuen Auftrag einzugeben.</span><span class="sxs-lookup"><span data-stu-id="25b3d-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="25b3d-126">Alle zutreffenden Rücklieferungspositionen werden in den neuen Auftrag kopiert.</span><span class="sxs-lookup"><span data-stu-id="25b3d-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="25b3d-127">Wenn die Kennung des Kaufvertrags automatisch im Feld **Kaufvertragskennung** angezeigt wird, dann ist der Kaufvertrag mit dem Auftragskopf für den Artikelersetzungsauftrags verknüpft worden.</span><span class="sxs-lookup"><span data-stu-id="25b3d-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="25b3d-128">Wenn es eine entsprechende Zusage im Kaufvertrag gibt, die noch nicht erfüllt wurde und der Auftrag erstellt wird, bevor der Kaufvertrag abläuft, wird eine Verknüpfung zwischen der Kaufvertragsposition und der Auftragsposition eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="25b3d-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="25b3d-129">Daher werden Informationen aus dem Kaufvertrag, wie Artikelpreis, in die neue Auftragsposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="25b3d-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]