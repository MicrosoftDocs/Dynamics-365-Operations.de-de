---
title: Auftragskopfzeilen und -positionen von Finance and Operations mit Sales synchronisieren
description: "Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Auftragskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren."
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
ms.openlocfilehash: 707efc97afc0679ed1fc22539789e98cbabcb581
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="0a8f2-103">Auftragskopfzeilen und -positionen von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="0a8f2-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0a8f2-104">Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Auftragskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="0a8f2-105">Vorlage und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="0a8f2-105">Template and tasks</span></span>

<span data-ttu-id="0a8f2-106">Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Auftragskopfzeilen und -positionen von Finance and Operations mit Sales zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="0a8f2-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="0a8f2-107">**Name der Vorlage in der Datenintegration**</span><span class="sxs-lookup"><span data-stu-id="0a8f2-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="0a8f2-108">Aufträge (Finance and Operations nach Sales)</span><span class="sxs-lookup"><span data-stu-id="0a8f2-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="0a8f2-109">**Namen der Aufgaben im Datenintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="0a8f2-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="0a8f2-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="0a8f2-110">OrderHeader</span></span>
    - <span data-ttu-id="0a8f2-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="0a8f2-111">OrderLine</span></span>

<span data-ttu-id="0a8f2-112">Synchronisiert die Aufgaben, die vor der Verkaufsrechnungskopf- und -Positionssynchronisierung erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="0a8f2-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="0a8f2-113">Produkte (Finance and Operations nach Sales)</span><span class="sxs-lookup"><span data-stu-id="0a8f2-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="0a8f2-114">Konten (Sales nach Finance and Operations) (wenn verwendet)</span><span class="sxs-lookup"><span data-stu-id="0a8f2-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="0a8f2-115">Kontakte nach Debitoren (Sales nach Finance and Operations) (wenn verwendet)</span><span class="sxs-lookup"><span data-stu-id="0a8f2-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="0a8f2-116">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="0a8f2-116">Entity set</span></span>

| <span data-ttu-id="0a8f2-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0a8f2-117">Finance and Operations</span></span> |    <span data-ttu-id="0a8f2-118">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="0a8f2-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="0a8f2-119">Vertrieb</span><span class="sxs-lookup"><span data-stu-id="0a8f2-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="0a8f2-120">CDS-Auftragskopfzeilen</span><span class="sxs-lookup"><span data-stu-id="0a8f2-120">CDS sales order headers</span></span>| <span data-ttu-id="0a8f2-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="0a8f2-121">SalesOrder</span></span>     | <span data-ttu-id="0a8f2-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="0a8f2-122">SalesOrders</span></span> |
| <span data-ttu-id="0a8f2-123">CDS-Auftragspositionen</span><span class="sxs-lookup"><span data-stu-id="0a8f2-123">CDS sales order lines</span></span>  | <span data-ttu-id="0a8f2-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="0a8f2-124">SalesOrderLine</span></span> | <span data-ttu-id="0a8f2-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="0a8f2-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="0a8f2-126">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="0a8f2-126">Entity flow</span></span>

<span data-ttu-id="0a8f2-127">Aufträge werden in Finance and Operations erstellt und mit Sales synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="0a8f2-128">Filter in der Vorlage stellen sicher, dass nur relevante Aufträge in die Synchronisierung einfließen:</span><span class="sxs-lookup"><span data-stu-id="0a8f2-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="0a8f2-129">Sowohl der Bestellungs- als auch der Rechnungsdebitor auf dem Auftrag, der aus Sales stammt, werden in die Synchronisierung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="0a8f2-130">In Finance and Operations werden die Felder **OrderingCustomerIsExternallyMaintained** und **InvoiceCustomerIsExternallyMaintained** verwendet, um die Synchronisierung in den Datenentitäten zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="0a8f2-131">Der **Auftrag** in Finance and Operations muss bestätigt werden.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="0a8f2-132">Nur bestätigte Aufträge oder Aufträge mit fortgeschrittenem Verarbeitungsstatus (beispielsweise "Versendet" oder "Fakturiert") werden mit Sales synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="0a8f2-133">Nach dem Erstellen oder Ändern eines Auftrags, muss der Stapelverarbeitungsauftrag **Verkaufssummen berechnen** aus Finance and Operations ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="0a8f2-134">Nur die Aufträge mit den berechneten Gesamtumsätzen werden mit CDS und Sales synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="0a8f2-135">Die Steuer für Belastungen auf dem **Auftragskopf** ist derzeit nicht in der Synchronisierung von Finance and Operations mit Sales enthalten.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="0a8f2-136">Der Grund dafür ist, dass Sales keine Steuerinformationen auf Kopfebene unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="0a8f2-137">Die Steuer, die sich auf Belastungen auf Positionsebene bezieht, ist enthalten.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="0a8f2-138">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="0a8f2-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="0a8f2-139">Neue Felder werden der Entität **Auftrag** hinzugefügt und auf der Seite angezeigt:</span><span class="sxs-lookup"><span data-stu-id="0a8f2-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="0a8f2-140">**Wird extern verwaltet** – Auf **Ja** gesetzt, wenn der Auftrag aus Finance and Operations stammt.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="0a8f2-141">**Verarbeitungsstatus** – Wird verwendet, um den Verarbeitungsstatus des Auftrags in Finance and Operations anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="0a8f2-142">Werte sind:</span><span class="sxs-lookup"><span data-stu-id="0a8f2-142">Values are:</span></span>

    - <span data-ttu-id="0a8f2-143">Aktiv</span><span class="sxs-lookup"><span data-stu-id="0a8f2-143">Active</span></span>
    - <span data-ttu-id="0a8f2-144">Bestätigt</span><span class="sxs-lookup"><span data-stu-id="0a8f2-144">Confirmed</span></span>
    - <span data-ttu-id="0a8f2-145">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="0a8f2-145">Packing Slip</span></span>
    - <span data-ttu-id="0a8f2-146">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="0a8f2-146">Invoiced</span></span>
    - <span data-ttu-id="0a8f2-147">Entnommen</span><span class="sxs-lookup"><span data-stu-id="0a8f2-147">Picked</span></span>
    - <span data-ttu-id="0a8f2-148">Teilweise kommissioniert</span><span class="sxs-lookup"><span data-stu-id="0a8f2-148">Partially Picked</span></span>
    - <span data-ttu-id="0a8f2-149">Teilweise verpackt</span><span class="sxs-lookup"><span data-stu-id="0a8f2-149">Partially Packed</span></span>
    - <span data-ttu-id="0a8f2-150">Versendet</span><span class="sxs-lookup"><span data-stu-id="0a8f2-150">Shipped</span></span>
    - <span data-ttu-id="0a8f2-151">Teilweise geliefert</span><span class="sxs-lookup"><span data-stu-id="0a8f2-151">Partially Shipped</span></span>
    - <span data-ttu-id="0a8f2-152">Teilweise fakturiert</span><span class="sxs-lookup"><span data-stu-id="0a8f2-152">Partially Invoiced</span></span>
    - <span data-ttu-id="0a8f2-153">Storniert</span><span class="sxs-lookup"><span data-stu-id="0a8f2-153">Cancelled</span></span>

<span data-ttu-id="0a8f2-154">Die Einstellung für **Verfügt nur über extern verwaltete Produkte** wird in anderen Auftragsszenarien (Synchronisierung von Sales mit Finance and Operation) verwendet, um permanent darüber auf dem Laufenden zu sein, ob der Auftrag vollständig aus **Extern verwalteten Produkten** besteht. In diesem Fall werden Produkte in Finance and Operations verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="0a8f2-155">Dadurch wird sichergestellt, dass Sie nicht versuchen, Auftragspositionen mit Produkten zu synchronisieren, die in Finance and Operations unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="0a8f2-156">Die Schaltflächen **Rechnung erstellen**, **Auftrag stornieren**, **Neu berechnen** und die für **Produkte abrufen** und **Adresse suchen** auf der Seite **Auftrag** sind bei extern verwalteten Aufträgen ausgeblendet, da Rechnungen in Finance and Operations erstellt und mit Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="0a8f2-157">Die Seite "Auftrag" kann nicht geändert werden, da Auftragsinformationen über Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="0a8f2-158">Der **Auftragsstatus** bleibt aktiv, um sicherstellen, dass Änderungen aus Finance and Operations in Sales in den **Auftrag** einfließen.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="0a8f2-159">Dies wird gesteuert, indem Sie den standardmäßigen **Statecode [Status]** im Datenintegrationsprojekt auf **Aktiv** setzen.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="0a8f2-160">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="0a8f2-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="0a8f2-161">Vor dem Synchronisieren von Aufträgen müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:</span><span class="sxs-lookup"><span data-stu-id="0a8f2-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="0a8f2-162">Einrichtung in Sales</span><span class="sxs-lookup"><span data-stu-id="0a8f2-162">Setup in Sales</span></span>

- <span data-ttu-id="0a8f2-163">Stellen Sie sicher, dass Berechtigungen für das Team, zu dem der Benutzer (aus Ihren **Verbindungseinstellungen** in Sales) zugewiesen ist, vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="0a8f2-164">Werden Demodaten verwendet, hat in der Regel der Benutzer einen Administratorzugriff aber nicht das Team.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="0a8f2-165">Ohne erhalten Sie eine Fehlermeldung, die besagt, dass das Prinzipal-Team fehlt, wenn Sie das Projekt über den Datenintegrator ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="0a8f2-166">Wählen Sie unter **Einstellungen** > **Sicherheit** > **Teams** das relevante Team aus, klicken Sie auf die Option für **Rollen verwalten**, und wählen Sie eine Rolle mit den benötigten Berechtigungen aus, beispielsweise Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="0a8f2-167">Stellen Sie unter **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Verkäufe** sicher, dass das **Systempreisberechnungssystem** auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="0a8f2-168">Stellen Sie unter **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Verkäufe** sicher, dass **Rabattberechnungsmethode** auf **Positionsartikel** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="0a8f2-169">Einrichtung in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0a8f2-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="0a8f2-170">Legen Sie **Vertrieb und Marketing** > **Periodische Aufgaben** > **Verkaufssummen berechnen** für eine Ausführung als Stapelverarbeitungsauftrag fest und setzen Sie **Summen für Aufträge berechnen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="0a8f2-171">Dies ist wichtig, da nur Aufträge mit berechneten Gesamtumsätzen mit CDS und Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="0a8f2-172">Die Häufigkeit des Stapelverarbeitungsauftrags sollte sich an der Häufigkeit der Auftragssynchronisierung orientieren.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-172">The frequence of the batch job should be alligned with the frequence of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="0a8f2-173">Einrichtung im Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="0a8f2-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="0a8f2-174">SalesHeader-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0a8f2-174">SalesHeader task</span></span>

- <span data-ttu-id="0a8f2-175">Aktualisieren Sie die Zuordnung für **CDS-Organisations-ID in Quelle** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="0a8f2-176">Der Standardvorlagenwert für **Account_Organization_OrganizationId** ist ORG001.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="0a8f2-177">Der Standardvorlagenwert für **InvoiceAccount_Organization_OrganizationId** ist ORG001.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="0a8f2-178">Der Standardvorlagenwert für **Organization_OrganizationId** ist ORG001.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="0a8f2-179">Vergewissern Sie sich, dass die erforderliche Zuordnung in **Quelle** > **CDS für InvoiceCountryRegionId zu BillingAddress_Country** und für **DeliveryCountryRegionId zu DeliveryAddress_Country** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="0a8f2-180">Der Vorlagenwert ist **ValueMap** mit einer Reihe zugeordneter Länder.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="0a8f2-181">**Preisliste** ist erforderlich, um Aufträge in Sales zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="0a8f2-182">Aktualisieren Sie die **ValueMap** in **CDS** > **Ziel** für **pricelevelid.name [Preislistenname]** auf die **Preisliste**, die in Sales pro Währung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="0a8f2-183">Sie können entweder die standardmäßige **Preisliste** bei einer einheitlichen Währung verwenden oder **ValueMap** nutzen, wenn Sie **Preislisten** in mehreren Währungen haben.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="0a8f2-184">Der Standardvorlagewert für **pricelevelid.name [Preislistenname]** ist CRM-Service USA (Beispiel).</span><span class="sxs-lookup"><span data-stu-id="0a8f2-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="0a8f2-185">SalesLine-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0a8f2-185">SalesLine task</span></span>

- <span data-ttu-id="0a8f2-186">Aktualisieren Sie die Zuordnung für **CDS-Organisations-ID in Quelle** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="0a8f2-187">Der Standardvorlagenwert für **SalesOrder_Organization_OrganizationId** ist ORG001.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="0a8f2-188">Der Standardvorlagenwert für **Product_Organization_OrganizationId** ist ORG001.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="0a8f2-189">Vergewissern Sie sich, dass die erforderliche Zuordnung in **Quelle** > **CDS** für **DeliveryCountryRegionId** zu **DeliveryAddress_Country** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="0a8f2-190">Der Vorlagenwert ist **ValueMap** mit einer Reihe zugeordneter Länder.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="0a8f2-191">Stellen Sie sicher, dass die erforderliche **ValueMap** für **SalesUnitSymbol** in Finance and Operations unter **Quelle** > **CDS-Zuordnung** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="0a8f2-192">Der Vorlagenwert für **ValueMap** ist für **SalesUnitSymbol zu Quantity_UOM** definiert.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="0a8f2-193">Vorlagenzuordnung im Datenintegrator</span><span class="sxs-lookup"><span data-stu-id="0a8f2-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="0a8f2-194">Die Felder **Zahlungsbedingungen**, **Frachtkonditionen**, **Lieferbedingungen**, **Liefermethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="0a8f2-195">Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="0a8f2-196">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="0a8f2-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="0a8f2-197">OrderHeader</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/sales-order-template-mapping-data-integrator-1.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="0a8f2-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="0a8f2-200">OrderLine</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/sales-order-template-mapping-data-integrator-3.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="0a8f2-203">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0a8f2-203">Related topics</span></span>

[<span data-ttu-id="0a8f2-204">Synchronisierung von Produkten aus Finance and Operations für Produkte in Sales</span><span class="sxs-lookup"><span data-stu-id="0a8f2-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="0a8f2-205">Konten von Sales mit Debitoren in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="0a8f2-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="0a8f2-206">Kontakte von Sales mit Kontakten oder Debitoren in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="0a8f2-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="0a8f2-207">Verkaufsangebotskopfzeilen und -positionen von Sales mit Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="0a8f2-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="0a8f2-208">Verkaufsrechnungszeilen und -positionen von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="0a8f2-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


