--- 
title: Beschaffungskatalog erstellen
description: Dieser Leitfaden zeigt Ihnen, wie ein Beschaffungskatalog erstellt wird.
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: df844ba3834972441daa61899294b3e95cac96c1
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="09138-103">Beschaffungskatalog erstellen</span><span class="sxs-lookup"><span data-stu-id="09138-103">Create a procurement catalog</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09138-104">Dieser Leitfaden zeigt Ihnen, wie ein Beschaffungskatalog erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="09138-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="09138-105">Diese Aufgabe wird normalerweise von einem Prokuristen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09138-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="09138-106">Sie erfahren auch, wie Mitarbeiter den Katalog verwenden können, wenn sie eine Anforderung erstellen.</span><span class="sxs-lookup"><span data-stu-id="09138-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="09138-107">Bevor Sie einen Katalog erstellen können, muss es in Ihrem System eine Beschaffungskategoriehierarchie geben.</span><span class="sxs-lookup"><span data-stu-id="09138-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="09138-108">Die Hierarchie wird vom neuen Katalog zusammen mit allen Produkten geerbt, die sich in der Hierarchie befinden.</span><span class="sxs-lookup"><span data-stu-id="09138-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="09138-109">Sie können diesen Leitfaden im Demodatenunternehmen USMF verwenden, in dem die Beschaffungskategoriehierarchie verfügbar ist, sowie die Beispiele, die in den Prozedurschritten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="09138-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="09138-110">Sicherstellen, dass eine Beschaffungskategoriehierarchie vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="09138-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="09138-111">Wechseln Sie zu "Beschaffung" > "Beschaffungskategorien".</span><span class="sxs-lookup"><span data-stu-id="09138-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="09138-112">Eine Beschaffungskategoriehierarchie ist im USMF-Demodatenunternehmen verfügbar und Produkte sind der Kategorie "Bürogeräte/Computer" hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="09138-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="09138-113">Wenn Sie diese Prozedur als Aufgabenleitfaden ausführen, müssen Sie den Leitfaden entsperren, wenn Sie die Kategorie durchsuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="09138-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="09138-114">Wenn eine Hierarchie nicht verfügbar wäre, würden Sie sie erstellen, indem Sie auf "Neu" klicken.</span><span class="sxs-lookup"><span data-stu-id="09138-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="09138-115">Dies kann nur einmal ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="09138-115">This can only be done once.</span></span>  
2. <span data-ttu-id="09138-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="09138-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="09138-117">Einen Katalog erstellen</span><span class="sxs-lookup"><span data-stu-id="09138-117">Create a catalog</span></span>
1. <span data-ttu-id="09138-118">Wechseln Sie zu Beschaffung > Kataloge > Beschaffungskataloge.</span><span class="sxs-lookup"><span data-stu-id="09138-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="09138-119">Klicken Sie auf "Neuer Beschaffungskatalog" um das Ablagedialogfeld zu öffnen</span><span class="sxs-lookup"><span data-stu-id="09138-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="09138-120">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="09138-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="09138-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="09138-121">Click OK.</span></span>
5. <span data-ttu-id="09138-122">Im Baum erweitern Sie "UNTERNEHMENSBESCHAFFUNGSKATEGORIEN".</span><span class="sxs-lookup"><span data-stu-id="09138-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="09138-123">Erweitern Sie "BÜROGERÄTE" im Baum.</span><span class="sxs-lookup"><span data-stu-id="09138-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="09138-124">Wählen Sie im Baum "Computer" aus.</span><span class="sxs-lookup"><span data-stu-id="09138-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="09138-125">Die Produkte aus der Beschaffungskategorie werden in der Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="09138-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="09138-126">Wenn Sie ein Produkt der Kategorie hinzufügen möchten, müssen Sie dies auf der Seite "Beschaffungskategoriehierarchie" oder auf der Seite "Artikeldetails" erledigen.</span><span class="sxs-lookup"><span data-stu-id="09138-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="09138-127">Der standardmäßige Aktualisierungstyp bestimmt, ob neue Produkte, die der Beschaffungskategoriehierarchie hinzugefügt wurden, im Katalog sofort sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="09138-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="09138-128">Wenn der Aktualisierungstyp auf "Dynamisch" festgelegt ist, sind Änderungen sofort sichtbar.</span><span class="sxs-lookup"><span data-stu-id="09138-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="09138-129">Wenn der Aktualisierungstyp auf "Statisch" festgelegt ist, sind neue Produkte nur sichtbar, wenn Personen den Katalog benutzen, nachdem der Katalog erneut veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="09138-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="09138-130">Die Aktivität "Veröffentlichen" ist im Aktionsbereich oben auf der Seite verfügbar.</span><span class="sxs-lookup"><span data-stu-id="09138-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="09138-131">Wenn Produkte von der Beschaffungskategoriehierarchie entfernt werden, ist die Änderung sofort sichtbar, unabhängig vom Wert im Feld "Standardmäßiger Aktualisierungstyp".</span><span class="sxs-lookup"><span data-stu-id="09138-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="09138-132">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="09138-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="09138-133">Klicken Sie auf "Ausblenden".</span><span class="sxs-lookup"><span data-stu-id="09138-133">Click Hide.</span></span>
10. <span data-ttu-id="09138-134">Klicken Sie im Aktionsbereich auf "Kategorienavigation".</span><span class="sxs-lookup"><span data-stu-id="09138-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="09138-135">Klicken Sie auf "Deaktivieren".</span><span class="sxs-lookup"><span data-stu-id="09138-135">Click Disable.</span></span>
12. <span data-ttu-id="09138-136">Klicken Sie im Aktionsbereich auf "Kategorienavigation".</span><span class="sxs-lookup"><span data-stu-id="09138-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="09138-137">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="09138-137">Click Enable.</span></span>
14. <span data-ttu-id="09138-138">Klicken Sie auf "Katalog aktivieren".</span><span class="sxs-lookup"><span data-stu-id="09138-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="09138-139">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="09138-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="09138-140">Den Katalog sichtbar machen</span><span class="sxs-lookup"><span data-stu-id="09138-140">Make the catalog visible</span></span>
1. <span data-ttu-id="09138-141">Wechseln Sie zu Beschaffung > Einstellungen > Richtlinien > Beschaffungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="09138-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="09138-142">Wählen Sie die "Beschaffungsrichtlinie USMF" aus.</span><span class="sxs-lookup"><span data-stu-id="09138-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="09138-143">Sie müssen die Einkaufsrichtlinie für die juristische Person auswählen, in der die Arbeitskraft, der mit Ihrem Benutzerprofil verbunden ist, Produkte bestellen darf.</span><span class="sxs-lookup"><span data-stu-id="09138-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="09138-144">In den USMF-Demodaten ist der Benutzer "Administrator" mit der Arbeitskraft mit Namen Julia Funderburk verbunden und sie bestellt standardmäßig Produkte in USMF.</span><span class="sxs-lookup"><span data-stu-id="09138-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="09138-145">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="09138-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="09138-146">Wählen Sie den Katalog aus, das Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="09138-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="09138-147">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="09138-147">Click OK.</span></span>
6. <span data-ttu-id="09138-148">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="09138-148">Close the page.</span></span>
7. <span data-ttu-id="09138-149">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="09138-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="09138-150">Den Katalog verwenden</span><span class="sxs-lookup"><span data-stu-id="09138-150">Use the catalog</span></span>
1. <span data-ttu-id="09138-151">Wechseln Sie zu Beschaffung > Bestellanforderungen > Alle Bestellanforderungen.</span><span class="sxs-lookup"><span data-stu-id="09138-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="09138-152">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="09138-152">Click New.</span></span>
3. <span data-ttu-id="09138-153">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="09138-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="09138-154">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="09138-154">Click OK.</span></span>
5. <span data-ttu-id="09138-155">Klicken Sie auf Produkte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="09138-155">Click Add products.</span></span>
6. <span data-ttu-id="09138-156">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="09138-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="09138-157">Sie können die Kategoriehierarchie auf der linken Seite oder den Filter oben an der Liste verwenden, um die Produkte zu filtern.</span><span class="sxs-lookup"><span data-stu-id="09138-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="09138-158">Zu Positionen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="09138-158">Click Add to lines.</span></span>
8. <span data-ttu-id="09138-159">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="09138-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="09138-160">Zu Positionen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="09138-160">Click Add to lines.</span></span>
10. <span data-ttu-id="09138-161">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="09138-161">Click OK.</span></span>


