---
title: Rechnungskopfzeilen und ‑positionen direkt von Supply Chain Management zu Sales synchronisieren
description: Das Thema erklärt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Rechnungskopfzeilen und -positionen direkt aus Dynamics 365 Supply Chain Management zu Dynamics 365 Sales zu synchronisieren.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: fa2772db63332319c399999bd5f747b2ac729d9e
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653274"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="89b4b-103">Rechnungskopfzeilen und ‑positionen aus Sales direkt von Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="89b4b-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89b4b-104">Das Thema erklärt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Rechnungskopfzeilen und -positionen direkt aus Dynamics 365 Supply Chain Management zu Dynamics 365 Sales zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="89b4b-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="89b4b-105">Datenfluss in Interessent nach Bargeld</span><span class="sxs-lookup"><span data-stu-id="89b4b-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="89b4b-106">Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Supply Chain Management und Sales hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="89b4b-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="89b4b-107">Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Supply Chain Management und Sales.</span><span class="sxs-lookup"><span data-stu-id="89b4b-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="89b4b-108">Die folgende Abbildung zeigt, wie Daten zwischen Supply Chain Management und Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="89b4b-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="89b4b-109">[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="89b4b-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="89b4b-110">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="89b4b-110">Templates and tasks</span></span>

<span data-ttu-id="89b4b-111">Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [PowerApps-Administrator-Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="89b4b-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="89b4b-112">Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="89b4b-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="89b4b-113">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Rechnungskopfzeilen und -positionen aus Supply Chain Management mit Sales zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="89b4b-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Supply Chain Management to Sales:</span></span>

- <span data-ttu-id="89b4b-114">**Name der Vorlage in der Datenintegration:** Verkaufsrechnungen (Finance and Operations zu Sales) - direkt</span><span class="sxs-lookup"><span data-stu-id="89b4b-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="89b4b-115">**Namen der Aufgaben im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="89b4b-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="89b4b-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="89b4b-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="89b4b-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="89b4b-117">SalesInvoiceLine</span></span>

<span data-ttu-id="89b4b-118">Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Rechnungskopfzeilen und -positionen erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="89b4b-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="89b4b-119">Produkte (Supply Chain Management zu Sales) – Direkt</span><span class="sxs-lookup"><span data-stu-id="89b4b-119">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="89b4b-120">Konten (Sales zu Supply Chain Management) – Direkt (falls verwendet)</span><span class="sxs-lookup"><span data-stu-id="89b4b-120">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="89b4b-121">Kontakte (Sales zu Supply Chain Management) – Direkt (falls verwendet)</span><span class="sxs-lookup"><span data-stu-id="89b4b-121">Contacts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="89b4b-122">Auftragskopf und -positionen (Supply Chain Management zu Sales) – Direkt</span><span class="sxs-lookup"><span data-stu-id="89b4b-122">Sales order header and lines (Supply Chain Management to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="89b4b-123">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="89b4b-123">Entity set</span></span>

| <span data-ttu-id="89b4b-124">Lieferkettenverwaltung</span><span class="sxs-lookup"><span data-stu-id="89b4b-124">Supply Chain Management</span></span>                              | <span data-ttu-id="89b4b-125">Verk.</span><span class="sxs-lookup"><span data-stu-id="89b4b-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="89b4b-126">Extern gepflegte Debitorenverkaufsrechnungs-Kopfzeilen</span><span class="sxs-lookup"><span data-stu-id="89b4b-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="89b4b-127">Rechnungen</span><span class="sxs-lookup"><span data-stu-id="89b4b-127">Invoices</span></span>       |
| <span data-ttu-id="89b4b-128">Extern gepflegte Debitorenverkaufsrechnungs-Positionen</span><span class="sxs-lookup"><span data-stu-id="89b4b-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="89b4b-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="89b4b-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="89b4b-130">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="89b4b-130">Entity flow</span></span>

<span data-ttu-id="89b4b-131">Verkaufsrechnungen werden in Supply Chain Management erstellt und mit Sales synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="89b4b-131">Sales invoices are created in Supply Chain Management and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="89b4b-132">Die Steuer für Belastungen auf dem Verkaufsrechnungskopf ist derzeit nicht in der Synchronisierung von Supply Chain Management mit Sales enthalten.</span><span class="sxs-lookup"><span data-stu-id="89b4b-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Supply Chain Managements to Sales.</span></span> <span data-ttu-id="89b4b-133">Sales unterstützt keine Steuerinformationen auf Kopfebene.</span><span class="sxs-lookup"><span data-stu-id="89b4b-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="89b4b-134">Allerdings sind Steuern, die den Belastungen auf Positionsebene zugeordnet sind, in die Synchronisierung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="89b4b-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="89b4b-135">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="89b4b-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="89b4b-136">Ein Feld **Rechnungsnummer** wurde zur Entität **Rechnung** hinzugefügt und wird auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89b4b-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="89b4b-137">Die Schaltfläche **Rechnung erstellen** auf der Seite **Auftrag** ist ausgeblendet, da Rechnungen in Supply Chain Management erstellt und mit Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="89b4b-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="89b4b-138">Die Seite **Rechnung** kann nicht geändert werden, da Rechnungen über Supply Chain Management synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="89b4b-138">The **Invoice** page can't be edited, because invoices will be synchronized from Supply Chain Management.</span></span>
- <span data-ttu-id="89b4b-139">Der **Auftragsstatus**-Wert wird automatisch in **Fakturiert** geändert, wenn die zugehörige Rechnung aus Supply Chain Management mit Sales synchronisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="89b4b-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synchronized to Sales.</span></span> <span data-ttu-id="89b4b-140">Darüber hinaus wird der Eigentümer des Auftrags, aufgrund dessen die Rechnung erstellt wurde, als Eigentümer der Rechnung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="89b4b-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="89b4b-141">Daher kann der Besitzer des Auftrags die Rechnung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="89b4b-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="89b4b-142">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="89b4b-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="89b4b-143">Vor dem Synchronisieren von Rechnungen müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:</span><span class="sxs-lookup"><span data-stu-id="89b4b-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="89b4b-144">Einrichtung in Sales</span><span class="sxs-lookup"><span data-stu-id="89b4b-144">Setup in Sales</span></span>

<span data-ttu-id="89b4b-145">Gehen Sie zu **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Sales**, und überprüfen Sie, ob die folgenden Einstellungen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="89b4b-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="89b4b-146">Die Option **Systempreisberechnungssystem verwenden** wird auf **Ja** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89b4b-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="89b4b-147">Das Feld **Rabattberechnungsmethode** wird auf **Positionsartikel** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89b4b-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="89b4b-148">Einrichtung im Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="89b4b-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="89b4b-149">SalesInvoiceHeader-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="89b4b-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="89b4b-150">Vergewissern Sie sich, dass die erforderliche Zuordnung für **InvoiceCountryRegionId** zu **BillingAddress\_Country** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="89b4b-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="89b4b-151">Der Vorlagenwert ist eine Wertzuordnung, in der verschiedene Länder/Regionen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="89b4b-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="89b4b-152">Preisliste ist erforderlich, um Rechnungen in Sales zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="89b4b-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="89b4b-153">Aktualisieren Sie die Wertzuordnung für **pricelevelid.name \[Price list name\]** auf die Preisliste, die in Sales pro Währung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="89b4b-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="89b4b-154">Sie können die Standardpreisliste für eine einzelne Währung verwenden.</span><span class="sxs-lookup"><span data-stu-id="89b4b-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="89b4b-155">Alternativ können Sie, wenn Sie Preislisten in mehreren Währungen haben, eine Zuordnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="89b4b-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="89b4b-156">Der Vorlagenwert für **pricelevelid.name \[Price list name\]** ist ein Wertzuordnung, die auf Währung mit USD = CRM Service USA (Beispiel) basiert.</span><span class="sxs-lookup"><span data-stu-id="89b4b-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="89b4b-157">SalesInvoiceLine-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="89b4b-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="89b4b-158">Vergewissern Sie sich, dass die erforderliche Zuordnung für **Maßeinheit** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="89b4b-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="89b4b-159">Stellen Sie sicher, dass die erforderliche Wertzuordnung für **SalesUnitSymbol** in Supply Chain Management vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="89b4b-159">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>

    <span data-ttu-id="89b4b-160">Ein Vorlagenwert, der eine Wertzuordnung hat, wird für **SalesUnitSymbol** als **Quantity\_UOM** definiert.</span><span class="sxs-lookup"><span data-stu-id="89b4b-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="89b4b-161">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="89b4b-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="89b4b-162">Die Felder **Zahlungsbedingungen**, **Frachtbedingungen**, **Lieferbedingungen**, **Liefermethode** und **Bereitstellungsmodus** sind nicht in den Standardzuordnungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="89b4b-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="89b4b-163">Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="89b4b-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="89b4b-164">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="89b4b-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="89b4b-165">Die Zuordnung zeigt, welche Feldinformationen von Sales zu Supply Chain Management synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="89b4b-165">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="89b4b-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="89b4b-166">SalesInvoiceHeader</span></span>

![Vorlagenzuordnung in Datenintegration](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="89b4b-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="89b4b-168">SalesInvoiceLine</span></span>

![Vorlagenzuordnung in Datenintegration](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="89b4b-170">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="89b4b-170">Related topics</span></span>

[<span data-ttu-id="89b4b-171">Prospect-to-Cash</span><span class="sxs-lookup"><span data-stu-id="89b4b-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="89b4b-172">Konten direkt von Sales mit Konten in Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="89b4b-172">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="89b4b-173">Produkte direkt von Supply Chain Management mit Produkten in Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="89b4b-173">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="89b4b-174">Kontakte direkt von Sales mit Kontakten oder Debitoren in Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="89b4b-174">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="89b4b-175">Auftragskopfzeilen und ‑positionen direkt von Supply Chain Management zu Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="89b4b-175">Synchronize sales order headers and lines directly from Supply Chain Management to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)
