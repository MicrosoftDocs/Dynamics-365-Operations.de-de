---
title: Synchronisieren von Produkten aus Finance und Operations mit Produkten in Sales
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte aus Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="e8383-103">Synchronisieren von Produkten aus Finance und Operations mit Produkten in Sales</span><span class="sxs-lookup"><span data-stu-id="e8383-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="e8383-104">Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="e8383-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="e8383-105">Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte aus Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="e8383-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="e8383-106">Vorlage und Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e8383-106">Template and task</span></span>

<span data-ttu-id="e8383-107">Die folgenden Vorlagen und zugrunde liegenden Aufgaben, die verwendet werden, um Produkte aus Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations), mit Microsoft Dynamics 365 for Sales (Sales) zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="e8383-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="e8383-108">Name der Vorlage: Produkte (Finance and Operations nach Sales)</span><span class="sxs-lookup"><span data-stu-id="e8383-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="e8383-109">Name de Aufgabe im Projekt: Produkte</span><span class="sxs-lookup"><span data-stu-id="e8383-109">Name of task in project: Products</span></span>

<span data-ttu-id="e8383-110">Synchronisierungsaufgaben, die vor der Produktsynchronisierung erforderlich sind: keine</span><span class="sxs-lookup"><span data-stu-id="e8383-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="e8383-111">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="e8383-111">Entity set</span></span>

| <span data-ttu-id="e8383-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="e8383-112">**Finance and Operations**</span></span> | <span data-ttu-id="e8383-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="e8383-113">**CDS**</span></span> | <span data-ttu-id="e8383-114">**Verkäufe**</span><span class="sxs-lookup"><span data-stu-id="e8383-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="e8383-115">Freigegebene Produkte für Verkauf</span><span class="sxs-lookup"><span data-stu-id="e8383-115">Sellable released products</span></span> | <span data-ttu-id="e8383-116">Produkt</span><span class="sxs-lookup"><span data-stu-id="e8383-116">Product</span></span> | <span data-ttu-id="e8383-117">Produkte</span><span class="sxs-lookup"><span data-stu-id="e8383-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="e8383-118">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="e8383-118">Entity flow</span></span>

<span data-ttu-id="e8383-119">Produkte werden in Finance and Operations verwaltet und mit Sales synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="e8383-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="e8383-120">Die Datenentität **Verkäufliche freigegebene Produkte** in Finance and Operations exportiert nur Produkte, die verkäuflich sind. Das bedeutet, dass Produkte die erforderlichen Informationen enthalten, die in einem Auftrag verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e8383-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="e8383-121">Die gleichen Regeln gelten, wenn ein Produkt mit der Funktion **Überprüfen** auf der Seite **Freigegebenes Produkt** überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="e8383-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="e8383-122">Die **Produktnummer** wird als Schlüssel verwendet. Das heißt, dass Produktvarianten mit CDS und Sales mit einzelnen **Produkt-IDs** pro **Produktvariante** synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e8383-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e8383-123">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="e8383-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="e8383-124">In Sales wird ein neues Feld bei den Produkten **Wird extern verwaltet** hinzugefügt, um anzugeben, dass ein bestimmtes Produkt extern verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="e8383-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="e8383-125">Der Wert wird beim Import nach Sales standardmäßig auf **Ja** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8383-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="e8383-126">**Wird extern verwaltet = Ja**: Produkt hat in Finance and Operations seinen Ursprung und kann in Sales nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="e8383-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="e8383-127">**Wird extern verwaltet = nein**: Produkt wird direkt in Sales eingegeben.</span><span class="sxs-lookup"><span data-stu-id="e8383-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="e8383-128">**Wird extern verwaltet = leer**: Produkt ist in Sales vorhanden, bevor die Lösung „Interessent zu Bargeld” aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="e8383-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="e8383-129">Die Informationen **Wird extern verwaltet** werden verwendet, um sicherzustellen, dass nur **Angebote** und **Aufträge** mit **Extern verwalteten Produkten** mit Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e8383-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="e8383-130">**Extern verwaltete Produkte** werden automatisch der ersten gültigen **Preisliste** mit derselben Währung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e8383-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="e8383-131">Beachten Sie, dass die Liste alphabetisch nach **Name** sortiert wird.</span><span class="sxs-lookup"><span data-stu-id="e8383-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="e8383-132">Der Produktverkaufspreis von Finance and Operations wird als Preis in der **Preisliste** verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8383-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="e8383-133">Das bedeutet, dass es erforderlich ist, eine **Preisliste** in Sales für jede **Produktverkaufswährung** in Finance and Operations zu haben.</span><span class="sxs-lookup"><span data-stu-id="e8383-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="e8383-134">Die Währung für die freigegebenen verkäuflichen Produkte ist auf die Buchhaltungswährung in der juristischen Person festgelegt, von der das Produkt exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="e8383-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="e8383-135">Produktsynchronisierung ist ohne eine **Preisliste** mit der übereinstimmenden Währung nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e8383-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="e8383-136">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="e8383-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="e8383-137">Bevor Sie die allererste Synchronisierung ausführen, müssen Sie die **Tabelle eindeutig identifizierbarer Produkte** für vorhandene Produkte in Finance and Operations auffüllen.</span><span class="sxs-lookup"><span data-stu-id="e8383-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="e8383-138">Vorhandene Produkte werden nicht synchronisiert, bis der Einzelvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e8383-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="e8383-139">In Finance and Operations verwenden Sie Suche, um nach **Tabelle eindeutig identifizierbarer Produkte auffüllen** zu suchen.</span><span class="sxs-lookup"><span data-stu-id="e8383-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="e8383-140">Klicken Sie auf **Tabelle eindeutig identifizierbarer Produkte auffüllen**, um den Einzelvorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e8383-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="e8383-141">Dieser Einzelvorgang muss nur einmal ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e8383-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="e8383-142">Stellen Sie sicher, dass die erforderliche **ValueMap** für den Verkauf von **Maßeinheit** (ME) in Finance and Operations vorhanden ist in der **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span><span class="sxs-lookup"><span data-stu-id="e8383-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="e8383-143">Stellen Sie sicher, dass **Dezimalstellen unterstützt** für ME Ihren Anfordernungen in **CDS -\> Destination** entspricht.</span><span class="sxs-lookup"><span data-stu-id="e8383-143">Ensure that **Decimals supported** for UOM match your requirements in **CDS -\> Destination**.</span></span> <span data-ttu-id="e8383-144">Wenn Sie andere Werte pro ME benötigen, kann dies mit **ValueMap** von Einheit erfolgen, beispielsweise [Each : 0] & [Pound : 2].</span><span class="sxs-lookup"><span data-stu-id="e8383-144">If you require different values per UOM, this can be done with **ValueMap** from Unit, for example, [Each : 0] & [Pound : 2].</span></span>

    -   <span data-ttu-id="e8383-145">Vorlagenwert ist standardmäßig auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8383-145">Template value is defaulted to 0.</span></span>

-   <span data-ttu-id="e8383-146">Aktualisieren Sie die **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="e8383-146">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="e8383-147">Vorlagenwert ist standardmäßig auf ORG001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8383-147">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="e8383-148">Aktualisieren Sie **ValueMap** für **Einheitengruppe** (**defaultuomscheduleid.name**) in **CDS -\> Destination**, um der **Einheitengruppe** in Sales zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e8383-148">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="e8383-149">Vorlagenwert ist standardmäßig auf **Standardeinheit** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8383-149">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="e8383-150">Stellen Sie sicher, dass alle Maßseinheiten für Produktverkäufe von Finance and Operations in Sales mit dem Wert **CDS-Entnahmelisten** vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e8383-150">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="e8383-151">Vergewissern Sie sich, dass **Preislisten** in Sales für jede Produktverkaufswährung in Finance and Operations vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e8383-151">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="e8383-152">Produkte können in Sales mit dem Status **Entwurf** oder **Aktiv** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e8383-152">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="e8383-153">Dies wird in **Systemeinstellungen** unter **Vertrieb** in Sales gesteuert.</span><span class="sxs-lookup"><span data-stu-id="e8383-153">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="e8383-154">Produkte, die mit Entwurfsstatus erstellt werden, müssen aktiviert werden, bevor Sie zu **Angebot** oder **Auftrag** hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e8383-154">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="e8383-155">Vorlagenzuordnung im Datenintegrator</span><span class="sxs-lookup"><span data-stu-id="e8383-155">Template mapping in data integrator</span></span>

<span data-ttu-id="e8383-156">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="e8383-156">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/products-template-mapping-data-integrator-1.png)

![Vorlagenzuordnung für Produkte im Datenintegrator](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="e8383-159">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e8383-159">Related topics</span></span>

[<span data-ttu-id="e8383-160">Synchronisierung von Konten aus Sales für Kunden in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e8383-160">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="e8383-161">Synchronisierung von Kontakten aus Sales für Kontakte oder Kunden in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e8383-161">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="e8383-162">Synchronisierung von Vertriebsangebotsköpfen und -positionen aus Sales für Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e8383-162">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)


