---
title: Verkaufsrechnungszeilen und -positionen von Finance and Operations mit Sales synchronisieren
description: "Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fb5ba099911deda5308daf92d82cd6b3489995bf
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="ef7a7-103">Verkaufsrechnungszeilen und -positionen von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="ef7a7-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ef7a7-104">Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="ef7a7-105">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ef7a7-105">Templates and tasks</span></span>

<span data-ttu-id="ef7a7-106">Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Rechnungskopfzeilen und -positionen von Finance and Operations mit Sales zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="ef7a7-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="ef7a7-107">**Name der Vorlage in der Datenintegration**</span><span class="sxs-lookup"><span data-stu-id="ef7a7-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="ef7a7-108">Verkaufsrechnungen (Finance and Operations nach Sales)</span><span class="sxs-lookup"><span data-stu-id="ef7a7-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="ef7a7-109">**Namen der Aufgaben im Datenintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="ef7a7-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="ef7a7-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="ef7a7-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="ef7a7-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="ef7a7-111">SalesInvoiceLine</span></span>

<span data-ttu-id="ef7a7-112">Synchronisiert die Aufgaben, die vor der Verkaufsrechnungskopf- und -Positionssynchronisierung erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="ef7a7-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="ef7a7-113">Produkte (Finance and Operations nach Sales)</span><span class="sxs-lookup"><span data-stu-id="ef7a7-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="ef7a7-114">Konten (Sales nach Finance and Operations) (wenn verwendet)</span><span class="sxs-lookup"><span data-stu-id="ef7a7-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="ef7a7-115">Kontakte (Sales nach Finance and Operations) (wenn verwendet)</span><span class="sxs-lookup"><span data-stu-id="ef7a7-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="ef7a7-116">Auftragskopf und -positionen (Finance and Operations nach Sales)</span><span class="sxs-lookup"><span data-stu-id="ef7a7-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="ef7a7-117">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="ef7a7-117">Entity set</span></span>

| <span data-ttu-id="ef7a7-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ef7a7-118">Finance and Operations</span></span>                               | <span data-ttu-id="ef7a7-119">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="ef7a7-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="ef7a7-120">Vertrieb</span><span class="sxs-lookup"><span data-stu-id="ef7a7-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="ef7a7-121">Extern gepflegte Debitorenverkaufsrechnungs-Kopfzeilen</span><span class="sxs-lookup"><span data-stu-id="ef7a7-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="ef7a7-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="ef7a7-122">SalesInvoice</span></span>     | <span data-ttu-id="ef7a7-123">Rechnungen</span><span class="sxs-lookup"><span data-stu-id="ef7a7-123">Invoices</span></span>       |
| <span data-ttu-id="ef7a7-124">Extern gepflegte Debitorenverkaufsrechnungs-Positionen</span><span class="sxs-lookup"><span data-stu-id="ef7a7-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="ef7a7-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="ef7a7-125">SalesInvoiceLine</span></span> | <span data-ttu-id="ef7a7-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="ef7a7-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="ef7a7-127">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="ef7a7-127">Entity flow</span></span>

<span data-ttu-id="ef7a7-128">Verkaufsrechnungen werden in Finance and Operations erstellt und mit Sales synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="ef7a7-129">Die Steuer für Belastungen auf dem **Verkaufsrechnungskopf** ist derzeit nicht in der Synchronisierung von Finance and Operations mit Sales enthalten.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="ef7a7-130">Der Grund dafür ist, dass Sales keine Steuerinformationen auf Kopfebene unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="ef7a7-131">Die Steuer, die sich auf Belastungen auf Positionsebene bezieht, ist enthalten.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="ef7a7-132">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="ef7a7-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="ef7a7-133">Ein **Rechnungsnummernfeld** wird zur Entität **Rechnung** hinzugefügt und auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="ef7a7-134">Die Schaltfläche **Rechnung erstellen** auf der Seite **Auftrag** ist ausgeblendet, da Rechnungen in Finance and Operations erstellt und mit Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="ef7a7-135">Die Seite **Rechnung** kann nicht geändert werden, da Rechnungen über Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="ef7a7-136">Der **Auftragsstatus** wird automatisch in **Fakturiert** geändert, wenn die zugehörige Rechnung aus Finance and Operations mit Sales synchronisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="ef7a7-137">Darüber hinaus wird der Eigentümer des Auftrags, aufgrund dessen die Rechnung erstellt wurde, als Eigentümer der Rechnung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="ef7a7-138">Dadurch kann der Eigentümer des Auftrags die Rechnung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="ef7a7-139">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="ef7a7-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="ef7a7-140">Vor dem Synchronisieren von Verkaufsrechnungen müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:</span><span class="sxs-lookup"><span data-stu-id="ef7a7-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="ef7a7-141">Einrichtung in Sales</span><span class="sxs-lookup"><span data-stu-id="ef7a7-141">Setup in Sales</span></span>

- <span data-ttu-id="ef7a7-142">Stellen Sie unter **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Verkäufe** sicher, dass das **Systempreisberechnungssystem** auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="ef7a7-143">Stellen Sie unter **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Verkäufe** sicher, dass **Rabattberechnungsmethode** auf **Positionsartikel** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="ef7a7-144">Einrichtung im Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="ef7a7-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="ef7a7-145">SalesInvoiceHeader-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="ef7a7-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="ef7a7-146">Aktualisieren Sie die Zuordnung für **CDS-Organisations-ID** in **Quelle** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="ef7a7-147">Der Standardvorlagenwert für **SalesOrder_Organization_OrganizationId** ist ORG001.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="ef7a7-148">Der Standardvorlagenwert für **Account_Organization_OrganizationId** ist ORG001.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="ef7a7-149">Der Standardvorlagenwert für **Organization_OrganizationId** ist ORG001.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="ef7a7-150">Vergewissern Sie sich, dass die erforderliche Zuordnung in **Quelle** > **CDS für InvoiceCountryRegionId** in **BillingAddress_Country** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="ef7a7-151">Der Vorlagenwert ist **ValueMap** mit einer Reihe zugeordneter Länder.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="ef7a7-152">**Preisliste** ist erforderlich, um Rechnungen in Sales zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="ef7a7-153">Aktualisieren Sie die **ValueMap** in **CDS** > **Ziel für pricelevelid.name [Preislistenname]** auf die **Preisliste**, die in Sales pro Währung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="ef7a7-154">Sie können entweder die standardmäßige **Preisliste** bei einer einheitlichen Währung verwenden oder **ValueMap** nutzen, wenn Sie **Preislisten** in mehreren Währungen haben.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="ef7a7-155">Der Vorlagenwert für **pricelevelid.name [Preislistenanme]** ist **ValueMap** basierend auf **Währung**.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="ef7a7-156">usd: CRM-Service USA (Beispiel).</span><span class="sxs-lookup"><span data-stu-id="ef7a7-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="ef7a7-157">SalesInvoiceLine-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="ef7a7-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="ef7a7-158">Vergewissern Sie sich, dass die erforderliche Zuordnung in **Quelle** > **CDS für Maßeinheit** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="ef7a7-159">Stellen Sie sicher, dass die erforderliche **ValueMap** für **SalesUnitSymbol** in Finance and Operations unter **Quelle** > **CDS-Zuordnung** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="ef7a7-160">Der Vorlagenwert für **ValueMap** ist für **SalesUnitSymbol zu Quantity_UOM** definiert.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="ef7a7-161">Aktualisieren Sie die Zuordnung für **CDS-Organisations-ID in Quelle** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="ef7a7-162">Der Standardvorlagenwert für **SalesInvoicer_Organization_OrganizationId** ist ORG001.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="ef7a7-163">Der Standardvorlagenwert für **Product_Organization_OrganizationId** ist ORG001.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="ef7a7-164">Vorlagenzuordnung im Datenintegrator</span><span class="sxs-lookup"><span data-stu-id="ef7a7-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="ef7a7-165">Die Felder **Zahlungsbedingungen**, **Frachtkonditionen**, **Lieferbedingungen**, **Liefermethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="ef7a7-166">Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="ef7a7-167">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="ef7a7-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="ef7a7-172">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ef7a7-172">Related topics</span></span>

[<span data-ttu-id="ef7a7-173">Synchronisierung von Produkten aus Finance and Operations für Produkte in Sales</span><span class="sxs-lookup"><span data-stu-id="ef7a7-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="ef7a7-174">Konten von Sales mit Debitoren in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="ef7a7-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="ef7a7-175">Kontakte von Sales mit Kontakten oder Debitoren in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="ef7a7-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="ef7a7-176">Verkaufsangebotskopfzeilen und -positionen von Sales mit Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="ef7a7-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="ef7a7-177">Auftragskopfzeilen und -positionen von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="ef7a7-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


