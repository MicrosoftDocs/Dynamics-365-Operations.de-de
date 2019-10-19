---
title: Auftragssperren verwalten
description: In dieser Prozedur wird gezeigt, wie Debitorenaufträge gesperrt werden, wie mit Auscheckvorgängen von Auftragssperren gearbeitet wird und wie Auftragssperren entfernt werden.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7168d13ef0b24d06aa28fbbc22bbb4e6093df24
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/11/2019
ms.locfileid: "1994909"
---
# <a name="manage-order-holds"></a><span data-ttu-id="c2792-103">Auftragssperren verwalten</span><span class="sxs-lookup"><span data-stu-id="c2792-103">Manage order holds</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c2792-104">In dieser Prozedur wird gezeigt, wie Debitorenaufträge gesperrt werden, wie mit Auscheckvorgängen von Auftragssperren gearbeitet wird und wie Auftragssperren entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c2792-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="c2792-105">Ein Auftrag kann aus unterschiedlichen Gründen gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="c2792-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="c2792-106">Sie können beispielsweise einen Auftrag sperren, bis eine Debitorenadresse oder eine Zahlungsmethode überprüft werden können, oder bis ein Manager das Kreditlimit des Debitors prüfen kann.</span><span class="sxs-lookup"><span data-stu-id="c2792-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="c2792-107">Während der Auftrag gesperrt ist, kann er vom Lager nicht für den Versand bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c2792-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="c2792-108">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2792-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="c2792-109">Auftragssperren einrichten</span><span class="sxs-lookup"><span data-stu-id="c2792-109">Set up order holds</span></span>
1. <span data-ttu-id="c2792-110">Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Einrichtung > Aufträge > Auftragssperrcodes**.</span><span class="sxs-lookup"><span data-stu-id="c2792-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="c2792-111">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="c2792-111">Click **New**.</span></span>
3. <span data-ttu-id="c2792-112">Geben Sie im Feld **Sperrcode** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c2792-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="c2792-113">Geben Sie beispielsweise „Rückruf” ein.</span><span class="sxs-lookup"><span data-stu-id="c2792-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="c2792-114">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c2792-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="c2792-115">Beispielsweise „Auftrag gesperrt bis Kundenrückruf”.</span><span class="sxs-lookup"><span data-stu-id="c2792-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="c2792-116">Aktivieren Sie optional das Kontrollkästchen **Erfassungen entfernen**, um sämtliche physischen Erfassungen aus dem Auftrag zu entfernen, wenn dieser Sperrcode hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c2792-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="c2792-117">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="c2792-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="c2792-118">Auftrag sperren</span><span class="sxs-lookup"><span data-stu-id="c2792-118">Place order on hold</span></span>
1. <span data-ttu-id="c2792-119">Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Aufträge > Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="c2792-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="c2792-120">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="c2792-120">Click **New**.</span></span>
3. <span data-ttu-id="c2792-121">Geben Sie im Feld **Debitorenkonto** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c2792-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="c2792-122">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2792-122">Click **OK**.</span></span>
5. <span data-ttu-id="c2792-123">Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c2792-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="c2792-124">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="c2792-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="c2792-125">Klicken Sie im **Aktivitätsbereich** auf **Auftrag**.</span><span class="sxs-lookup"><span data-stu-id="c2792-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="c2792-126">Klicken Sie auf **Auftragssperren**.</span><span class="sxs-lookup"><span data-stu-id="c2792-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="c2792-127">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="c2792-127">Click **New**.</span></span>
10. <span data-ttu-id="c2792-128">Wählen Sie im Feld **Sperrcode** einen Code aus, den Sie in der vorherigen Teilaufgabe erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c2792-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="c2792-129">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="c2792-129">Click **Save**.</span></span>
12. <span data-ttu-id="c2792-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c2792-130">Close the page.</span></span>
13. <span data-ttu-id="c2792-131">Wechseln Sie zu **Vertrieb und Marketing > Aufträge > Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="c2792-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="c2792-132">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c2792-132">In the list, mark the selected row.</span></span> <span data-ttu-id="c2792-133">Bei Aufträge, der derzeit gespert sind, sind die Felder „Nicht verarbeiten” und „Sperren” markiert.</span><span class="sxs-lookup"><span data-stu-id="c2792-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="c2792-134">Klicken Sie im Aktivitätsbereich auf **Entnehmen und verpacken**.</span><span class="sxs-lookup"><span data-stu-id="c2792-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="c2792-135">Auftragssperren verwalten</span><span class="sxs-lookup"><span data-stu-id="c2792-135">Manage order holds</span></span>
1. <span data-ttu-id="c2792-136">Wechseln Sie zu **Vertrieb und Marketing > Aufträge > Offene Bestellungen > Auftragsssperren**.</span><span class="sxs-lookup"><span data-stu-id="c2792-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="c2792-137">Die Seite **Auftragssperren** funktioniert als Workbench, wo Sie einen Überblick über alle aktuellen und verarbeiteten Sperren abrufen können sowie zugeordnete Verkaufsaufträge bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="c2792-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="c2792-138">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c2792-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c2792-139">Klicken Sie im **Aktivitätsbereich** auf **Sperre ausschecken**.</span><span class="sxs-lookup"><span data-stu-id="c2792-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="c2792-140">Klicken Sie auf **Auschecken**.</span><span class="sxs-lookup"><span data-stu-id="c2792-140">Click **Check out**.</span></span>
5. <span data-ttu-id="c2792-141">Heben Sie in der Liste die Markierung der ausgewählten Zeile auf.</span><span class="sxs-lookup"><span data-stu-id="c2792-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="c2792-142">Das **Auschecken nach Feld** zeigt jetzt Ihre Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="c2792-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="c2792-143">Klicken Sie auf **Auschchecken löschen**.</span><span class="sxs-lookup"><span data-stu-id="c2792-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="c2792-144">Klicken Sie im **Aktivitätsbereich** auf **Sperre aufheben**.</span><span class="sxs-lookup"><span data-stu-id="c2792-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="c2792-145">Wenn Sie bereit sind, die Sperre aufzuheben und die Verarbeitung des Auftrags bis zum nächsten Erfüllungsschritt zulassen, müssen Sie die Sperre aufheben.</span><span class="sxs-lookup"><span data-stu-id="c2792-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="c2792-146">Wenn der Auftrag keine Änderungen erfordert, können Sie die Aktion „Sperren aufheben” ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2792-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="c2792-147">Allerdings können Sie die Aktion „Deaktivieren und ändern” verwenden, wenn bei der Aufhebung der Sperre der Auftrag aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c2792-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="c2792-148">Die Aktion **Deaktivieren und übermitteln** kann nur verwendet werden, wenn Sie Callsenterfunktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2792-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="c2792-149">Klicken Sie auf **Sperren aufhaben**.</span><span class="sxs-lookup"><span data-stu-id="c2792-149">Click **Clear holds**.</span></span> <span data-ttu-id="c2792-150">Die Sperre ist nun aus dem Auftrag deaktiviert worden und aus der Liste von aktiver Sperren entfernt worden.</span><span class="sxs-lookup"><span data-stu-id="c2792-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="c2792-151">Um alle Sperren oder ihre Teilmengen nach einem spezifischen Status anzuzeigen, ändern Sie den Wert im Feld „Anzeigen”.</span><span class="sxs-lookup"><span data-stu-id="c2792-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

