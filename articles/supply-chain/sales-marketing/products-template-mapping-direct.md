---
title: Produkte direkt von Supply Chain Management mit Produkten in Sales synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgaben, die verwendet werden, um die Produkte aus Dynamics 365 Supply Chain Management mit Dynamics 365 Sales zu synchronisieren.
author: ChristianRytt
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 29bb9d05aa939ec82595e153faf03f290e219589
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817820"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="c5b05-103">Produkte direkt von Supply Chain Management mit Produkten in Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="c5b05-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="c5b05-104">Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Integration von Daten in Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="c5b05-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="c5b05-105">Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgaben, die verwendet werden, um die Produkte direkt aus Dynamics 365 Supply Chain Management mit Dynamics 365 Sales zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="c5b05-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="c5b05-106">Datenfluss in Interessent nach Bargeld</span><span class="sxs-lookup"><span data-stu-id="c5b05-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="c5b05-107">Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Supply Chain Management und Sales hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="c5b05-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="c5b05-108">Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Supply Chain Management und Sales.</span><span class="sxs-lookup"><span data-stu-id="c5b05-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="c5b05-109">Die folgende Abbildung zeigt, wie Daten zwischen Supply Chain Management und Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c5b05-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="c5b05-110">[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="c5b05-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c5b05-111">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="c5b05-111">Templates and tasks</span></span>

<span data-ttu-id="c5b05-112">Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [Power Apps-Administrator-Center](https://admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="c5b05-112">To access the available templates, open [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="c5b05-113">Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c5b05-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c5b05-114">Die folgenden Vorlagen und grundlegenden Aufgaben werden für die Synchronisierung von Konten aus Sales für Kunden in Supply Chain Management verwendet:</span><span class="sxs-lookup"><span data-stu-id="c5b05-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="c5b05-115">**Name der Vorlage in der Datenintegration:** Produkte (Supply Chain Management zu Sales) - direkt</span><span class="sxs-lookup"><span data-stu-id="c5b05-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="c5b05-116">**Name der Aufgaben im Datenintegrationsprojekt**: Podukte</span><span class="sxs-lookup"><span data-stu-id="c5b05-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="c5b05-117">Keine Synchronisierungsaufgaben sind erforderlich, damit Produktsynchronisierung auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="c5b05-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="c5b05-118">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="c5b05-118">Entity set</span></span>

| <span data-ttu-id="c5b05-119">Lieferkettenverwaltung</span><span class="sxs-lookup"><span data-stu-id="c5b05-119">Supply Chain Management</span></span>    | <span data-ttu-id="c5b05-120">Verk.</span><span class="sxs-lookup"><span data-stu-id="c5b05-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="c5b05-121">Freigegebene Produkte für Verkauf</span><span class="sxs-lookup"><span data-stu-id="c5b05-121">Sellable released products</span></span> | <span data-ttu-id="c5b05-122">Produkte</span><span class="sxs-lookup"><span data-stu-id="c5b05-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="c5b05-123">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="c5b05-123">Entity flow</span></span>

<span data-ttu-id="c5b05-124">Produkte werden in Supply Chain Management verwaltet und mit Sales synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="c5b05-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="c5b05-125">Die **Verkäufliche freigegebene Produkte**-Datenentität im Bereich Supply Chain Management exportiert nur Produkte, die *verkäuflich* sind.</span><span class="sxs-lookup"><span data-stu-id="c5b05-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="c5b05-126">Verkäufliche Produkte sind Produkte, die die Informationen enthalten, die diese benötigen, damit sie in Aufträgen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c5b05-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="c5b05-127">Die gleichen Regeln gelten, wenn ein Produkt mit der Funktion **Überprüfen** auf der Seite **Freigegebenes Produkt** überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="c5b05-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="c5b05-128">Die Produktnummer wird als Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5b05-128">The product number is used as a key.</span></span> <span data-ttu-id="c5b05-129">Wenn Produktvarianten mit Sales synchronisiert werden, hat jede eine Produktvariante individuelle Produkt-Kennung</span><span class="sxs-lookup"><span data-stu-id="c5b05-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c5b05-130">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="c5b05-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="c5b05-131">In Sales wurde ein neues Feld **Wird extern verwaltet** bei Produkten hinzugefügt, um anzugeben, dass ein bestimmtes Produkt extern verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="c5b05-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="c5b05-132">Der Wert wird beim Import nach Sales standardmäßig auf **Ja** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c5b05-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="c5b05-133">Folgende Werte sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="c5b05-133">The following values are available:</span></span>

- <span data-ttu-id="c5b05-134">**Ja** – Das Produkt, stammt aus Supply Chain Management und wird nicht in Sales bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="c5b05-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="c5b05-135">**Nein** – Das Produkt wurde direkt in Sales eingegeben.</span><span class="sxs-lookup"><span data-stu-id="c5b05-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="c5b05-136">**(Kein Wert)** – Das Produkt war in Sales vorhanden, bevor der Interessent für Bargeldlösung aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="c5b05-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="c5b05-137">Das Feld **Wird extern verwaltet** hilft, sicherzustellen, dass nur Angebote und Aufträge mit Extern verwalteten Produkten mit Supply Chain Management synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c5b05-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="c5b05-138">Extern verwaltete Produkte werden automatisch der ersten gültigen Preisliste mit derselben Währung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c5b05-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="c5b05-139">Preislisten sind alphabetisch sortiert nach Name.</span><span class="sxs-lookup"><span data-stu-id="c5b05-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="c5b05-140">Der Produktverkaufspreis von Supply Chain Management wird als Preis in der Preisliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5b05-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="c5b05-141">Vergewissern Sie sich daher, dass Preislisten in Sales für jede Produktverkaufswährung in Supply Chain Management vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c5b05-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="c5b05-142">Die Währung für die freigegebenen verkäuflichen Produkte ist auf die Buchhaltungswährung in der juristischen Person festgelegt, von der das Produkt exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="c5b05-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="c5b05-143">Produktsynchronisierung ist nicht erfolgreich, es sei denn, es gibt eine Liste mit Preisen, die eine entsprechende Währung haben.</span><span class="sxs-lookup"><span data-stu-id="c5b05-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="c5b05-144">Sie können auch die verwendete Preisliste mit der Integration steuern, indem Sie den pricelevelid.name [Standard-Preisliste (Name)] im Daten-Integrationsprojekt zuordnen.</span><span class="sxs-lookup"><span data-stu-id="c5b05-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="c5b05-145">Die Eingabe muss in Kleinbuchstaben sein.</span><span class="sxs-lookup"><span data-stu-id="c5b05-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="c5b05-146">Beispielsweise kann der Standardwert für eine Liste mit Preisen auf Verkäufen mit dem Namen "Standard" wie folgt sein: Empfangsfeld: pricelevelid.name [Standard-Preisliste (Name)] und Zuordnungstyp: [ { "transformType" "Standard", "defaultValue": "Standard" } ].</span><span class="sxs-lookup"><span data-stu-id="c5b05-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="c5b05-147">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="c5b05-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="c5b05-148">Bevor Sie die allererste Synchronisierung ausführen, müssen Sie die Tabelle eindeutig identifizierbarer Produkte für vorhandene Produkte in Supply Chain Management auffüllen.</span><span class="sxs-lookup"><span data-stu-id="c5b05-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="c5b05-149">Vorhandene Produkte werden nicht synchronisiert, bis der Einzelvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c5b05-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="c5b05-150">In Supply Chain Management verwenden Sie Suche, um nach **Tabelle eindeutig identifizierbarer Produkte auffüllen** zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c5b05-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="c5b05-151">Klicken Sie auf **Tabelle eindeutig identifizierbarer Produkte auffüllen**, um den Einzelvorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c5b05-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="c5b05-152">Dieser Vorgang muss nur einmal aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c5b05-152">This job must be run only one time.</span></span>

- <span data-ttu-id="c5b05-153">Vergewissern Sie sich, dass die erforderliche Wertzuordnung für die Verkaufsmaßeinheit (ME) zwischen Supply Chain Management und Sales in der Zuordnung von **SalesUnitSymbol** zu **DefaultUnit (Name)** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c5b05-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="c5b05-154">Aktualisieren Sie Wertzuordnung für **Einheitengruppe** (**defaultuomscheduleid.name**), um den **Einheitengruppen** in Sales zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c5b05-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="c5b05-155">Der Vorlagenwert ist standardmäßig auf **Standardeinheit** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c5b05-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="c5b05-156">Stellen Sie sicher, dass alle Maßseinheiten für Produktverkäufe von Supply Chain Management in Sales vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c5b05-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="c5b05-157">Vergewissern Sie sich, dass Preislisten in Sales für jede Produktverkaufswährung in Supply Chain Management vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c5b05-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="c5b05-158">Wenn Produkte in Sales erstellt werden, können sie den Status **Entwurf** oder **Aktiv** besitzen.</span><span class="sxs-lookup"><span data-stu-id="c5b05-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="c5b05-159">Das Verhalten wird mit **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Verkäufe** in Sales gesteuert.</span><span class="sxs-lookup"><span data-stu-id="c5b05-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="c5b05-160">Produkte, die den Status **Entwurf** besitzen, wenn sie erstellt werden, müssen aktiviert werden, bevor sie in Anführungszeichen gesetzt oder ausgewählten Aufträgen hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="c5b05-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c5b05-161">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="c5b05-161">Template mapping in Data integration</span></span>

<span data-ttu-id="c5b05-162">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="c5b05-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="c5b05-163">Die Zuordnung zeigt, welche Feldinformationen von Sales zu Supply Chain Management synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c5b05-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="c5b05-165">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c5b05-165">Related topics</span></span>

[<span data-ttu-id="c5b05-166">Prospect-to-Cash</span><span class="sxs-lookup"><span data-stu-id="c5b05-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="c5b05-167">Konten direkt von Sales mit Konten in Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="c5b05-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="c5b05-168">Kontakte direkt von Sales mit Kontakten oder Debitoren in Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="c5b05-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="c5b05-169">Synchronisieren von Aufträgen direkt zwischen Sales und Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c5b05-169">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="c5b05-170">Rechnungskopfzeilen und ‑positionen direkt von Supply Chain Management zu Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="c5b05-170">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]