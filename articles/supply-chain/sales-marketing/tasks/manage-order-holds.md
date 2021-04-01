---
title: Auftragssperren verwalten
description: In dieser Prozedur wird gezeigt, wie Debitorenaufträge gesperrt werden, wie mit Auscheckvorgängen von Auftragssperren gearbeitet wird und wie Auftragssperren entfernt werden.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e9c91061b82b8e172d8b93e9b255d0c9f400b5b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254988"
---
# <a name="manage-order-holds"></a><span data-ttu-id="c8edc-103">Auftragssperren verwalten</span><span class="sxs-lookup"><span data-stu-id="c8edc-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8edc-104">In dieser Prozedur wird gezeigt, wie Debitorenaufträge gesperrt werden, wie mit Auscheckvorgängen von Auftragssperren gearbeitet wird und wie Auftragssperren entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c8edc-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="c8edc-105">Ein Auftrag kann aus unterschiedlichen Gründen gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="c8edc-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="c8edc-106">Sie können beispielsweise einen Auftrag sperren, bis eine Debitorenadresse oder eine Zahlungsmethode überprüft werden können, oder bis ein Manager das Kreditlimit des Debitors prüfen kann.</span><span class="sxs-lookup"><span data-stu-id="c8edc-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="c8edc-107">Während der Auftrag gesperrt ist, kann er vom Lager nicht für den Versand bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c8edc-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="c8edc-108">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8edc-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="c8edc-109">Auftragssperren einrichten</span><span class="sxs-lookup"><span data-stu-id="c8edc-109">Set up order holds</span></span>
1. <span data-ttu-id="c8edc-110">Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Einrichtung > Aufträge > Auftragssperrcodes**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="c8edc-111">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-111">Click **New**.</span></span>
3. <span data-ttu-id="c8edc-112">Geben Sie im Feld **Sperrcode** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c8edc-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="c8edc-113">Geben Sie beispielsweise „Rückruf” ein.</span><span class="sxs-lookup"><span data-stu-id="c8edc-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="c8edc-114">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c8edc-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="c8edc-115">Beispielsweise „Auftrag gesperrt bis Kundenrückruf”.</span><span class="sxs-lookup"><span data-stu-id="c8edc-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="c8edc-116">Aktivieren Sie optional das Kontrollkästchen **Erfassungen entfernen**, um sämtliche physischen Erfassungen aus dem Auftrag zu entfernen, wenn dieser Sperrcode hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c8edc-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="c8edc-117">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="c8edc-118">Auftrag sperren</span><span class="sxs-lookup"><span data-stu-id="c8edc-118">Place order on hold</span></span>
1. <span data-ttu-id="c8edc-119">Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Aufträge > Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="c8edc-120">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-120">Click **New**.</span></span>
3. <span data-ttu-id="c8edc-121">Geben Sie im Feld **Debitorenkonto** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c8edc-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="c8edc-122">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-122">Click **OK**.</span></span>
5. <span data-ttu-id="c8edc-123">Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c8edc-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="c8edc-124">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="c8edc-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="c8edc-125">Klicken Sie im **Aktivitätsbereich** auf **Auftrag**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="c8edc-126">Klicken Sie auf **Auftragssperren**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="c8edc-127">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-127">Click **New**.</span></span>
10. <span data-ttu-id="c8edc-128">Wählen Sie im Feld **Sperrcode** einen Code aus, den Sie in der vorherigen Teilaufgabe erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c8edc-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="c8edc-129">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-129">Click **Save**.</span></span>
12. <span data-ttu-id="c8edc-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c8edc-130">Close the page.</span></span>
13. <span data-ttu-id="c8edc-131">Wechseln Sie zu **Vertrieb und Marketing > Aufträge > Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="c8edc-132">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c8edc-132">In the list, mark the selected row.</span></span> <span data-ttu-id="c8edc-133">Bei Aufträge, der derzeit gespert sind, sind die Felder „Nicht verarbeiten” und „Sperren” markiert.</span><span class="sxs-lookup"><span data-stu-id="c8edc-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="c8edc-134">Klicken Sie im Aktivitätsbereich auf **Entnehmen und verpacken**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="c8edc-135">Auftragssperren verwalten</span><span class="sxs-lookup"><span data-stu-id="c8edc-135">Manage order holds</span></span>
1. <span data-ttu-id="c8edc-136">Wechseln Sie zu **Vertrieb und Marketing > Aufträge > Offene Bestellungen > Auftragsssperren**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="c8edc-137">Die Seite **Auftragssperren** funktioniert als Workbench, wo Sie einen Überblick über alle aktuellen und verarbeiteten Sperren abrufen können sowie zugeordnete Verkaufsaufträge bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="c8edc-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="c8edc-138">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c8edc-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c8edc-139">Klicken Sie im **Aktivitätsbereich** auf **Sperre ausschecken**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="c8edc-140">Klicken Sie auf **Auschecken**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-140">Click **Check out**.</span></span>
5. <span data-ttu-id="c8edc-141">Heben Sie in der Liste die Markierung der ausgewählten Zeile auf.</span><span class="sxs-lookup"><span data-stu-id="c8edc-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="c8edc-142">Das **Auschecken nach Feld** zeigt jetzt Ihre Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="c8edc-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="c8edc-143">Klicken Sie auf **Auschchecken löschen**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="c8edc-144">Klicken Sie im **Aktivitätsbereich** auf **Sperre aufheben**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="c8edc-145">Wenn Sie bereit sind, die Sperre aufzuheben und die Verarbeitung des Auftrags bis zum nächsten Erfüllungsschritt zulassen, müssen Sie die Sperre aufheben.</span><span class="sxs-lookup"><span data-stu-id="c8edc-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="c8edc-146">Wenn der Auftrag keine Änderungen erfordert, können Sie die Aktion „Sperren aufheben” ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8edc-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="c8edc-147">Allerdings können Sie die Aktion „Deaktivieren und ändern” verwenden, wenn bei der Aufhebung der Sperre der Auftrag aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c8edc-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="c8edc-148">Die Aktion **Deaktivieren und übermitteln** kann nur verwendet werden, wenn Sie Callsenterfunktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8edc-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="c8edc-149">Klicken Sie auf **Sperren aufhaben**.</span><span class="sxs-lookup"><span data-stu-id="c8edc-149">Click **Clear holds**.</span></span> <span data-ttu-id="c8edc-150">Die Sperre ist nun aus dem Auftrag deaktiviert worden und aus der Liste von aktiver Sperren entfernt worden.</span><span class="sxs-lookup"><span data-stu-id="c8edc-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="c8edc-151">Um alle Sperren oder ihre Teilmengen nach einem spezifischen Status anzuzeigen, ändern Sie den Wert im Feld „Anzeigen”.</span><span class="sxs-lookup"><span data-stu-id="c8edc-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]