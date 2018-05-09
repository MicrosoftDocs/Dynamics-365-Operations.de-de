---
title: Produkte direkt von Finance and Operations mit Produkten in Sales synchronisieren
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Sales zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 821ba4f0957d8bb84fc188c86895700631b46fed
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="3b3cf-103">Produkte direkt von Finance and Operations mit Produkten in Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="3b3cf-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="3b3cf-104">Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="3b3cf-105">Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte direkt aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Sales zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="3b3cf-106">Datenfluss in Interessent nach Bargeld</span><span class="sxs-lookup"><span data-stu-id="3b3cf-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="3b3cf-107">Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Finance and Operations und Sales hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="3b3cf-108">Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Finance and Operations und Sales.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="3b3cf-109">Die folgende Abbildung zeigt, wie Daten zwischen Finance and Operations und Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="3b3cf-110">[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="3b3cf-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="3b3cf-111">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="3b3cf-111">Templates and tasks</span></span>

<span data-ttu-id="3b3cf-112">Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [PowerApps-Administrator-Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="3b3cf-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="3b3cf-113">Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="3b3cf-114">Die folgenden Vorlagen und grundlegenden Aufgaben werden für die Synchronisierung von Konten aus Sales für Kunden in Finance and Operations verwendet:</span><span class="sxs-lookup"><span data-stu-id="3b3cf-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="3b3cf-115">**Name der Vorlage in der Datenintegration:** Produkte (Finance and Operations zu Sales) - direkt</span><span class="sxs-lookup"><span data-stu-id="3b3cf-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="3b3cf-116">**Name der Aufgaben im Datenintegrationsprojekt**: Podukte</span><span class="sxs-lookup"><span data-stu-id="3b3cf-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="3b3cf-117">Keine Synchronisierungsaufgaben sind erforderlich, damit Produktsynchronisierung auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="3b3cf-118">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="3b3cf-118">Entity set</span></span>

| <span data-ttu-id="3b3cf-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3b3cf-119">Finance and Operations</span></span>     | <span data-ttu-id="3b3cf-120">Vertrieb</span><span class="sxs-lookup"><span data-stu-id="3b3cf-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="3b3cf-121">Freigegebene Produkte für Verkauf</span><span class="sxs-lookup"><span data-stu-id="3b3cf-121">Sellable released products</span></span> | <span data-ttu-id="3b3cf-122">Produkte</span><span class="sxs-lookup"><span data-stu-id="3b3cf-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="3b3cf-123">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="3b3cf-123">Entity flow</span></span>

<span data-ttu-id="3b3cf-124">Produkte werden in Finance and Operations verwaltet und mit Sales synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="3b3cf-125">Die **Verkäufliche freigegebene Produkte**-Datenentität im Bereich Finance and Operations exportiert nur Produkte, die *verkäuflich* sind.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="3b3cf-126">Verkäufliche Produkte sind Produkte, die die Informationen enthalten, die diese benötigen, damit sie in Aufträgen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="3b3cf-127">Die gleichen Regeln gelten, wenn ein Produkt mit der Funktion **Überprüfen** auf der Seite **Freigegebenes Produkt** überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="3b3cf-128">Die Produktnummer wird als Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-128">The product number is used as a key.</span></span> <span data-ttu-id="3b3cf-129">Wenn Produktvarianten mit Sales synchronisiert werden, hat jede eine Produktvariante individuelle Produkt-Kennung</span><span class="sxs-lookup"><span data-stu-id="3b3cf-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="3b3cf-130">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="3b3cf-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="3b3cf-131">In Sales wurde ein neues Feld **Wird extern verwaltet** bei Produkten hinzugefügt, um anzugeben, dass ein bestimmtes Produkt extern verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="3b3cf-132">Der Wert wird beim Import nach Sales standardmäßig auf **Ja** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="3b3cf-133">Folgende Werte sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="3b3cf-133">The following values are available:</span></span>

- <span data-ttu-id="3b3cf-134">**Ja** – Das Produkt, stammt aus Finance and Operations und wird nicht in Sales bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="3b3cf-135">**Nein** – Das Produkt wurde direkt in Sales eingegeben.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="3b3cf-136">**(Kein Wert)** – Das Produkt war in Sales vorhanden, bevor der Interessent für Bargeldlösung aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="3b3cf-137">Das Feld **Wird extern verwaltet** hilft, sicherzustellen, dass nur Angebote und Aufträge mit Extern verwalteten Produkten mit Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="3b3cf-138">Extern verwaltete Produkte werden automatisch der ersten gültigen Preisliste mit derselben Währung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="3b3cf-139">Preislisten sind alphabetisch sortiert nach Name.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="3b3cf-140">Der Produktverkaufspreis von Finance and Operations wird als Preis in der Preisliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="3b3cf-141">Vergewissern Sie sich daher, dass Preislisten in Sales für jede Produktverkaufswährung in Finance and Operations vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="3b3cf-142">Die Währung für die freigegebenen verkäuflichen Produkte ist auf die Buchhaltungswährung in der juristischen Person festgelegt, von der das Produkt exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> <span data-ttu-id="3b3cf-143">Produktsynchronisierung erfolgt nicht, es sei denn, es gibt eine Liste mit Preisen, die eine entsprechende Währung haben.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-143">Product synchronization won't succeed unless there is a price list that has a matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="3b3cf-144">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="3b3cf-144">Preconditions and mapping setup</span></span>

- <span data-ttu-id="3b3cf-145">Bevor Sie die allererste Synchronisierung ausführen, müssen Sie die Tabelle eindeutig identifizierbarer Produkte für vorhandene Produkte in Finance and Operations auffüllen.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-145">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="3b3cf-146">Vorhandene Produkte werden nicht synchronisiert, bis der Einzelvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-146">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="3b3cf-147">In Finance and Operations verwenden Sie Suche, um nach **Tabelle eindeutig identifizierbarer Produkte auffüllen** zu suchen.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-147">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="3b3cf-148">Klicken Sie auf **Tabelle eindeutig identifizierbarer Produkte auffüllen**, um den Einzelvorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-148">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="3b3cf-149">Dieser Vorgang muss nur einmal aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-149">This job must be run only one time.</span></span>

- <span data-ttu-id="3b3cf-150">Vergewissern Sie sich, dass die erforderliche Wertzuordnung für die Verkaufsmaßeinheit (ME) zwischen Finance and Operations und Sales in der Zuordnung von **SalesUnitSymbol** zu **DefaultUnit (Name)** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-150">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="3b3cf-151">Aktualisieren Sie Wertzuordnung für **Einheitengruppe** (**defaultuomscheduleid.name**), um den **Einheitengruppen** in Sales zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-151">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="3b3cf-152">Der Vorlagenwert ist standardmäßig auf **Standardeinheit** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-152">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="3b3cf-153">Stellen Sie sicher, dass alle Maßseinheiten für Produktverkäufe von Finance and Operations in Sales vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-153">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="3b3cf-154">Vergewissern Sie sich, dass Preislisten in Sales für jede Produktverkaufswährung in Finance and Operations vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-154">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="3b3cf-155">Wenn Produkte in Sales erstellt werden, können sie den Status **Entwurf** oder **Aktiv** besitzen.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-155">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="3b3cf-156">Das Verhalten wird mit **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Verkäufe** in Sales gesteuert.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-156">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="3b3cf-157">Produkte, die den Status **Entwurf** besitzen, wenn sie erstellt werden, müssen aktiviert werden, bevor sie in Anführungszeichen gesetzt oder ausgewählten Aufträgen hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-157">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3b3cf-158">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="3b3cf-158">Template mapping in Data integration</span></span>

<span data-ttu-id="3b3cf-159">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-159">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="3b3cf-160">Die Zuordnung zeigt, welche Feldinformationen von Sales zu Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b3cf-160">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="3b3cf-162">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3b3cf-162">Related topics</span></span>

[<span data-ttu-id="3b3cf-163">Interessent zu Bargeld</span><span class="sxs-lookup"><span data-stu-id="3b3cf-163">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="3b3cf-164">Konten von Sales direkt mit Debitoren in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="3b3cf-164">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="3b3cf-165">Kontakte direkt von Sales mit Kontakten oder Debitoren in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="3b3cf-165">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="3b3cf-166">Auftragskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="3b3cf-166">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="3b3cf-167">Verkaufsrechnungskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="3b3cf-167">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




