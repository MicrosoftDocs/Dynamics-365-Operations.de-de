---
title: Auftragskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren
description: "Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Auftragskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren."
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
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: e311b0becbb243cebdc265eccf3059eb46217dee
ms.contentlocale: de-de
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="e3007-103">Auftragskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="e3007-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e3007-104">Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Auftragskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="e3007-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="e3007-105">Datenfluss in Interessent nach Bargeld</span><span class="sxs-lookup"><span data-stu-id="e3007-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="e3007-106">Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Finance and Operations und Sales hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="e3007-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="e3007-107">Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Finance and Operations und Sales.</span><span class="sxs-lookup"><span data-stu-id="e3007-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="e3007-108">Die folgende Abbildung zeigt, wie Daten zwischen Finance and Operations und Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3007-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="e3007-109">[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="e3007-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e3007-110">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="e3007-110">Templates and tasks</span></span>

<span data-ttu-id="e3007-111">Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [PowerApps-Administrator-Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="e3007-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="e3007-112">Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="e3007-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e3007-113">Die folgende Vorlage und zugrunde liegenden Aufgaben werden verwendet, um Auftragskopfzeilen und -positionen von Finance and Operations mit Sales zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="e3007-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="e3007-114">**Name der Vorlage in der Datenintegration:** Verkaufsaufträge (Finance and Operations zu Sales) - direkt</span><span class="sxs-lookup"><span data-stu-id="e3007-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="e3007-115">**Namen der Aufgaben im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="e3007-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="e3007-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="e3007-116">OrderHeader</span></span>
    - <span data-ttu-id="e3007-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="e3007-117">OrderLine</span></span>

<span data-ttu-id="e3007-118">Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Rechnungskopfzeilen und -positionen erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="e3007-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="e3007-119">Produkte (Finance and Operations nach Sales) - Direkt</span><span class="sxs-lookup"><span data-stu-id="e3007-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="e3007-120">Konten (Sales nach Finance and Operations) - Direkt (wenn verwendet)</span><span class="sxs-lookup"><span data-stu-id="e3007-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="e3007-121">Kontakte nach Debitoren (Sales nach Finance and Operations) - Direkt (wenn verwendet)</span><span class="sxs-lookup"><span data-stu-id="e3007-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="e3007-122">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="e3007-122">Entity set</span></span>

| <span data-ttu-id="e3007-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e3007-123">Finance and Operations</span></span>  | <span data-ttu-id="e3007-124">Vertrieb</span><span class="sxs-lookup"><span data-stu-id="e3007-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="e3007-125">CDS-Auftragskopfzeilen</span><span class="sxs-lookup"><span data-stu-id="e3007-125">CDS sales order headers</span></span> | <span data-ttu-id="e3007-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="e3007-126">SalesOrders</span></span>       |
| <span data-ttu-id="e3007-127">CDS-Auftragspositionen</span><span class="sxs-lookup"><span data-stu-id="e3007-127">CDS sales order lines</span></span>   | <span data-ttu-id="e3007-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="e3007-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="e3007-129">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="e3007-129">Entity flow</span></span>

<span data-ttu-id="e3007-130">Aufträge werden in Finance and Operations erstellt und mit Sales synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="e3007-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="e3007-131">Filter in der Vorlage helfen, sicherzustellen, dass nur relevante Aufträge in die Synchronisierung einfließen:</span><span class="sxs-lookup"><span data-stu-id="e3007-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="e3007-132">Sowohl der Bestellungskunde als auch der Rechnungsdebitor auf dem Auftrag, der aus Sales stammt, werden in die Synchronisierung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="e3007-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="e3007-133">In Finance and Operations werden die Felder **OrderingCustomerIsExternallyMaintained** und **InvoiceCustomerIsExternallyMaintained** verwendet, um die Synchronisierung in den Datenentitäten zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="e3007-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="e3007-134">Der Auftrag in Finance and Operations muss bestätigt werden.</span><span class="sxs-lookup"><span data-stu-id="e3007-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="e3007-135">Nur bestätigte Aufträge oder Aufträge mit fortgeschrittenem Verarbeitungsstatus (beispielsweise **Versendet** oder **Fakturiert**) werden mit Sales synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="e3007-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="e3007-136">Nach dem Erstellen oder Ändern eines Auftrags, muss der Stapelverarbeitungsauftrag **Verkaufssummen berechnen** aus Finance and Operations ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e3007-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="e3007-137">Nur Aufträge, bei denen Auftragssummen berechnet wurden, werden mit Sales synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="e3007-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="e3007-138">Die Steuer für Belastungen auf dem Verkaufsauftragskopf ist derzeit nicht in der Synchronisierung von Finance and Operations mit Sales enthalten.</span><span class="sxs-lookup"><span data-stu-id="e3007-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="e3007-139">Sales unterstützt keine Steuerinformationen auf Kopfebene.</span><span class="sxs-lookup"><span data-stu-id="e3007-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="e3007-140">Allerdings sind Steuern, die den Belastungen auf Positionsebene zugeordnet sind, in die Synchronisierung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="e3007-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e3007-141">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="e3007-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="e3007-142">Neue Felder wurden der Entität **Auftrag** hinzugefügt und auf der Seite angezeigt:</span><span class="sxs-lookup"><span data-stu-id="e3007-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="e3007-143">**Wird extern verwaltet** – Auf **Ja** setzen, wenn der Auftrag aus Finance and Operations stammt.</span><span class="sxs-lookup"><span data-stu-id="e3007-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="e3007-144">**Verarbeitungsstatus** – Wird verwendet, um den Verarbeitungsstatus des Auftrags in Finance and Operations anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e3007-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="e3007-145">Folgende Werte sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="e3007-145">The following values are available:</span></span>

    - <span data-ttu-id="e3007-146">Aktiv</span><span class="sxs-lookup"><span data-stu-id="e3007-146">Active</span></span>
    - <span data-ttu-id="e3007-147">Bestätigt</span><span class="sxs-lookup"><span data-stu-id="e3007-147">Confirmed</span></span>
    - <span data-ttu-id="e3007-148">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="e3007-148">Packing Slip</span></span>
    - <span data-ttu-id="e3007-149">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="e3007-149">Invoiced</span></span>
    - <span data-ttu-id="e3007-150">Entnommen</span><span class="sxs-lookup"><span data-stu-id="e3007-150">Picked</span></span>
    - <span data-ttu-id="e3007-151">Teilweise kommissioniert</span><span class="sxs-lookup"><span data-stu-id="e3007-151">Partially Picked</span></span>
    - <span data-ttu-id="e3007-152">Teilweise verpackt</span><span class="sxs-lookup"><span data-stu-id="e3007-152">Partially Packed</span></span>
    - <span data-ttu-id="e3007-153">Versendet</span><span class="sxs-lookup"><span data-stu-id="e3007-153">Shipped</span></span>
    - <span data-ttu-id="e3007-154">Teilweise geliefert</span><span class="sxs-lookup"><span data-stu-id="e3007-154">Partially Shipped</span></span>
    - <span data-ttu-id="e3007-155">Teilweise fakturiert</span><span class="sxs-lookup"><span data-stu-id="e3007-155">Partially Invoiced</span></span>
    - <span data-ttu-id="e3007-156">Storniert</span><span class="sxs-lookup"><span data-stu-id="e3007-156">Cancelled</span></span>

<span data-ttu-id="e3007-157">Die Einstellung für **Verfügt nur über extern verwaltete Produkte** wird in anderen Auftragsszenarien (z. B. Synchronisierung von Sales mit Finance and Operation) verwendet, um permanent darüber auf dem Laufenden zu sein, ob der Auftrag vollständig aus extern verwalteten Produkten besteht.</span><span class="sxs-lookup"><span data-stu-id="e3007-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="e3007-158">Wenn ein Verkaufsauftrag nur aus extern verwalteten Produkten besteht, werden die Produkte in Finance and Operations verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e3007-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="e3007-159">Mit diesem Verhalten wird sichergestellt, dass Sie nicht versuchen, Verkaufsangebotspositionen mit Produkten zu synchronisieren, die in Finance and Operations unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="e3007-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="e3007-160">Bei extern verwalteten Aufträgen, werden die Schaltflächen **Rechnung erstellen**, **Auftrag stornieren**, **Neu berechnen** und die für **Produkte abrufen** und **Adresse suchen** auf der Seite **Auftrag** ausgeblendet, da Rechnungen in Finance and Operations erstellt und mit Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3007-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="e3007-161">Die Seite "Auftrag" kann nicht geändert werden, da Auftragsinformationen über Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3007-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="e3007-162">Der Auftragsstatus bleibt **Aktiv**, um sicherstellen, dass Änderungen aus Finance and Operations in Sales in den Auftrag einfließen.</span><span class="sxs-lookup"><span data-stu-id="e3007-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="e3007-163">Dies wird gesteuert, indem Sie den standardmäßigen **Statecode \[Status\]** Wert auf **Aktiv** setzen.</span><span class="sxs-lookup"><span data-stu-id="e3007-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="e3007-164">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="e3007-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="e3007-165">Vor dem Synchronisieren von Aufträgen müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:</span><span class="sxs-lookup"><span data-stu-id="e3007-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="e3007-166">Einrichtung in Sales</span><span class="sxs-lookup"><span data-stu-id="e3007-166">Setup in Sales</span></span>

- <span data-ttu-id="e3007-167">Stellen Sie sicher, dass Berechtigungen für das Team, zu dem der Benutzer (aus Ihren Verbindungseinstellungen in Sales) zugewiesen ist, vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e3007-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="e3007-168">Werden Demodaten verwendet, hat in der Regel der Benutzer einen Administratorzugriff aber nicht das Team.</span><span class="sxs-lookup"><span data-stu-id="e3007-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="e3007-169">Wenn dieses Team nicht auch Administratorzugriff hat, wenn Sie das Projekt vom Datenintegrator ausführen, erhalten Sie eine Fehlermeldung, die angibt, dass das Hauptteam fehlt.</span><span class="sxs-lookup"><span data-stu-id="e3007-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="e3007-170">Wählen Sie unter **Settings** > **Security** > **Teams** das relevante Team aus, klicken Sie auf die Option für **Rollen verwalten**, und wählen Sie eine Rolle mit den benötigten Berechtigungen aus, beispielsweise **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="e3007-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="e3007-171">Gehen Sie zu **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Sales**, und überprüfen Sie, ob die folgenden Einstellungen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="e3007-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="e3007-172">Die Option **Systempreisberechnungssystem verwenden** wird auf **Ja** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e3007-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="e3007-173">Das Feld **Rabattberechnungsmethode** wird auf **Positionsartikel** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e3007-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="e3007-174">Einrichtung in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e3007-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="e3007-175">Gehen Sie zu **Vertrieb und Marketing** > **Periodische Aufgaben** > **Vertriebssummen berechnen**, und richten Sie den Einzelvorgang so ein, dass er als Stapelverarbeitungslauf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3007-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="e3007-176">Legen sie Option **Berechnen Sie Summen für Aufträge** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="e3007-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="e3007-177">Diese Einstellung ist wichtig, da nur Aufträge, bei denen Auftragssummen berechnet wurden, werden mit Sales synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="e3007-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="e3007-178">Die Häufigkeit des Stapelverarbeitungsauftrags sollte sich an der Häufigkeit der Auftragssynchronisierung orientieren.</span><span class="sxs-lookup"><span data-stu-id="e3007-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="e3007-179">Einrichtung im Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="e3007-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="e3007-180">SalesHeader-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e3007-180">SalesHeader task</span></span>

- <span data-ttu-id="e3007-181">Vergewissern Sie sich, dass die erforderliche Zuordnung für **InvoiceCountryRegionId** zu **BillingAddress\_Country** und für **DeliveryCountryRegionId** zu **DeliveryAddress\_Country** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e3007-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="e3007-182">Der Vorlagenwert ist eine Wertzuordnung, in der verschiedene Länder/Regionen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e3007-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="e3007-183">Preisliste ist erforderlich, um Aufträge in Sales zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e3007-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="e3007-184">Aktualisieren Sie die Wertzuordnung für **pricelevelid.name \[Price list name\]** auf die Preisliste, die in Sales pro Währung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3007-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="e3007-185">Sie können die Standardpreisliste für eine einzelne Währung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e3007-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="e3007-186">Alternativ können Sie, wenn Sie Preislisten in mehreren Währungen haben, eine Zuordnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e3007-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="e3007-187">Der Standardvorlagewert für **pricelevelid.name \[Price list name\]** ist **CRM Service USA (Beispiel)**.</span><span class="sxs-lookup"><span data-stu-id="e3007-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="e3007-188">SalesLine-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e3007-188">SalesLine task</span></span>

- <span data-ttu-id="e3007-189">Vergewissern Sie sich, dass die erforderliche Zuordnung für **DeliveryCountryRegionId** zu **DeliveryAddress\_Country** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e3007-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="e3007-190">Der Vorlagenwert ist eine Wertzuordnung, in der verschiedene Länder/Regionen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e3007-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="e3007-191">tellen Sie sicher, dass die erforderliche Wertzuordnung für **SalesUnitSymbol** in Finance and Operations vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e3007-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="e3007-192">Ein Vorlagenwert, der eine Wertzuordnung hat, wird für **SalesUnitSymbol** als **Quantity\_UOM** definiert.</span><span class="sxs-lookup"><span data-stu-id="e3007-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e3007-193">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="e3007-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="e3007-194">Die Felder **Zahlungsbedingungen**, **Frachtbedingungen**, **Lieferbedingungen**, **Liefermethode** und **Bereitstellungsmodus** sind nicht in den Standardzuordnungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="e3007-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="e3007-195">Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e3007-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="e3007-196">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="e3007-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="e3007-197">Die Zuordnung zeigt, welche Feldinformationen von Sales zu Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3007-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="e3007-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="e3007-198">OrderHeader</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="e3007-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="e3007-200">OrderLine</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="e3007-202">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e3007-202">Related topics</span></span>

[<span data-ttu-id="e3007-203">Interessent zu Bargeld</span><span class="sxs-lookup"><span data-stu-id="e3007-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="e3007-204">Konten von Sales direkt mit Debitoren in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="e3007-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="e3007-205">Produkte direkt von Finance and Operations mit Produkten in Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="e3007-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="e3007-206">Kontakte direkt von Sales mit Kontakten oder Debitoren in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="e3007-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="e3007-207">Verkaufsrechnungskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="e3007-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




