---
title: Angebotskopfzeilen und -positionen direkt von Sales zu Finance and Operations synchronisieren
description: "Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen direkt von Microsoft Dynamics 365 for Sales mit Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 3d546dc180ec53ad0fac40fe134ed811af68658f
ms.contentlocale: de-de
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="15c7a-103">Angebotskopfzeilen und -positionen direkt von Sales zu Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="15c7a-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="15c7a-104">Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen direkt von Microsoft Dynamics 365 for Sales mit Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="15c7a-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

> [!NOTE]
> <span data-ttu-id="15c7a-105">Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="15c7a-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="15c7a-106">Vorlage und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="15c7a-106">Template and tasks</span></span>

<span data-ttu-id="15c7a-107">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Verkaufsangebotskopfzeilen und -positionen direkt von Sales mit Finance and Operations zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="15c7a-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="15c7a-108">**Name der Vorlage in der Datenintegration:** Verkaufsangebote (Sales zu Finance and Operations) - direkt</span><span class="sxs-lookup"><span data-stu-id="15c7a-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="15c7a-109">**Namen der Aufgaben im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="15c7a-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="15c7a-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="15c7a-110">QuoteHeader</span></span>
    - <span data-ttu-id="15c7a-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="15c7a-111">QuoteLine</span></span>

<span data-ttu-id="15c7a-112">Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Verkaufsangebotskopfzeilen und -positionen erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="15c7a-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="15c7a-113">Produkte (Finance and Operations nach Sales) - Direkt</span><span class="sxs-lookup"><span data-stu-id="15c7a-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="15c7a-114">Konten (Sales nach Finance and Operations) - Direkt (wenn verwendet)</span><span class="sxs-lookup"><span data-stu-id="15c7a-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="15c7a-115">Kontakte nach Debitoren (Sales nach Finance and Operations) - Direkt (wenn verwendet)</span><span class="sxs-lookup"><span data-stu-id="15c7a-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="15c7a-116">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="15c7a-116">Entity set</span></span>

| <span data-ttu-id="15c7a-117">Vertrieb</span><span class="sxs-lookup"><span data-stu-id="15c7a-117">Sales</span></span>        | <span data-ttu-id="15c7a-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15c7a-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="15c7a-119">Angebote</span><span class="sxs-lookup"><span data-stu-id="15c7a-119">Quotes</span></span>       | <span data-ttu-id="15c7a-120">CDS-Verkaufsangebotskopf</span><span class="sxs-lookup"><span data-stu-id="15c7a-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="15c7a-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="15c7a-121">QuoteDetails</span></span> | <span data-ttu-id="15c7a-122">CDS-Verkaufsangebotspositionen</span><span class="sxs-lookup"><span data-stu-id="15c7a-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="15c7a-123">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="15c7a-123">Entity flow</span></span>

<span data-ttu-id="15c7a-124">Verkaufsangebote werden in Sales erstellt und mit Finance and Operations synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="15c7a-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="15c7a-125">Verkaufsangebote aus Sales werden nur synchronisiert, wenn folgende Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="15c7a-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="15c7a-126">Alle Angebote in den Verkaufsangebotspositionen werden extern verwaltet.</span><span class="sxs-lookup"><span data-stu-id="15c7a-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="15c7a-127">Nachdem Sie **Angebot aktivieren** geklickt haben, ist das Verkaufsangebot aktiv.</span><span class="sxs-lookup"><span data-stu-id="15c7a-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="15c7a-128">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="15c7a-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="15c7a-129">Das Feld **Verfügt nur über extern verwaltete Produkte** ist der Entität **Angebot** hinzugefügt worden, um stets nachzuverfolgen, ob das Verkaufsangebot vollständig aus extern verwalteten Produkten besteht.</span><span class="sxs-lookup"><span data-stu-id="15c7a-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="15c7a-130">Wenn ein Verkaufsangebot nur aus extern verwalteten Produkten besteht, werden die Produkte in Finance and Operations verwaltet.</span><span class="sxs-lookup"><span data-stu-id="15c7a-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="15c7a-131">Mit diesem Verhalten wird sichergestellt, dass Sie nicht versuchen, Verkaufsangebotspositionen mit Produkten zu synchronisieren, die in Finance and Operations unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="15c7a-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="15c7a-132">Alle Angebotsprodukte im Vertriebsangebot werden mit der Information **Verfügt nur über extern verwaltete Produkte** aus der Vertriebsangebotskopfzeile aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="15c7a-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="15c7a-133">Diese Informationen können im Feld **Angebot hat nur extern verwaltete Produkte** in der Entität **QuoteDetails** gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="15c7a-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="15c7a-134">Ein Rabatt kann zum Angebotsprodukt hinzugefügt werden wird anschließend mit Finance and Operations synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="15c7a-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="15c7a-135">Die Felder **Rabatt**, **Belastungen** und **Steuer** in der Kopfzeile werden durch komplizierte Einstellungen in Finance and Operations gesteuert.</span><span class="sxs-lookup"><span data-stu-id="15c7a-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="15c7a-136">Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung.</span><span class="sxs-lookup"><span data-stu-id="15c7a-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="15c7a-137">Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** in Finance and Operations verwaltet und gehandhabt.</span><span class="sxs-lookup"><span data-stu-id="15c7a-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="15c7a-138">In Sales versieht die Lösung die folgenden Felder mit einem Schreibschutz, da die Werte nicht mit Finance and Operations synchronisiert werden:</span><span class="sxs-lookup"><span data-stu-id="15c7a-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="15c7a-139">Schreibgeschützte Felder in de Verkaufsangebotskopfzeile: **Rabatt %**, **Rabatt** und **Frachtbetrag**</span><span class="sxs-lookup"><span data-stu-id="15c7a-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="15c7a-140">Schreibgeschützte Felder auf Angebotsprodukten: **Steuer**</span><span class="sxs-lookup"><span data-stu-id="15c7a-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="15c7a-141">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="15c7a-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="15c7a-142">Vor dem Synchronisieren von Verkaufsangeboten müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:</span><span class="sxs-lookup"><span data-stu-id="15c7a-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="15c7a-143">Einrichtung in Sales</span><span class="sxs-lookup"><span data-stu-id="15c7a-143">Setup in Sales</span></span>

- <span data-ttu-id="15c7a-144">Stellen Sie sicher, dass Berechtigungen für das Team, zu dem der Benutzer (aus Ihren Verbindungseinstellungen in Sales) zugewiesen ist, vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="15c7a-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="15c7a-145">Werden Demodaten verwendet, hat in der Regel der Benutzer einen Administratorzugriff aber nicht das Team.</span><span class="sxs-lookup"><span data-stu-id="15c7a-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="15c7a-146">Wenn dieses Team nicht Administratorzugriff hat, wenn Sie das Projekt vom Datenintegrator ausführen, erhalten Sie eine Fehlermeldung, die angibt, dass das Hauptteam fehlt.</span><span class="sxs-lookup"><span data-stu-id="15c7a-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="15c7a-147">Wenn Sie Berechtigungen für das Team einrichten, gehen Sie &gt; zu **Einstellungen** **Sicherheit** &gt; **Teams**, und wählen Sie das zutreffende Team aus.</span><span class="sxs-lookup"><span data-stu-id="15c7a-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="15c7a-148">Wählen Sie **Verwalten Sie Rollen** und dann eine Rolle, die die erforderlichen Berechtigungen verfügt, beispielsweise **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="15c7a-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="15c7a-149">Gehen Sie zu &gt; Sie **Einstellungen** **Verwaltung** &gt; **Systemeinstellungen** &gt; **Sales** zu öffnen, und überprüfen Sie, ob die folgenden Einstellungen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="15c7a-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="15c7a-150">Die Option **Systempreisberechnungssystem verwenden** wird auf **Ja** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="15c7a-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="15c7a-151">Das Feld **Rabattberechnungsmethode** wird auf **Positionsartikel** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="15c7a-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="15c7a-152">Einrichtung im Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="15c7a-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="15c7a-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="15c7a-153">QuoteHeader</span></span>

- <span data-ttu-id="15c7a-154">Vergewissern Sie sich, dass die erforderliche Zuordnung für **Shipto\_Land** zu **DeliveryAddressCountryRegionISOCode** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="15c7a-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="15c7a-155">In der Wertzuordnungen können Sie einen Standardwert definieren, der verwendet wird, wenn der Wert nicht aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="15c7a-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="15c7a-156">Lassen Sie einfach die linken Seite leer, und legen die rechte Seite auf das gewünschte Land oder die Region fest.</span><span class="sxs-lookup"><span data-stu-id="15c7a-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="15c7a-157">Auf diese Weise müssen Sie das Land oder die Region für Zahlungen nationaler Aufträge nicht eingeben.</span><span class="sxs-lookup"><span data-stu-id="15c7a-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="15c7a-158">Der Vorlagenwert ist eine Wertzuordnung, in der verschiedene Länder/Regionen zugeordnet sind, und wo ein leerer Wert dem Wert **USA** entspricht.</span><span class="sxs-lookup"><span data-stu-id="15c7a-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="15c7a-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="15c7a-159">QuoteLine</span></span>

- <span data-ttu-id="15c7a-160">Stellen Sie sicher, dass die erforderliche Wertzuordnung für **SalesUnitSymbol** in Finance and Operations vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="15c7a-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="15c7a-161">Überprüfen Sie, dass die obligatorischen Einheiten in Sales definiert sind.</span><span class="sxs-lookup"><span data-stu-id="15c7a-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="15c7a-162">Ein Vorlagenwert, eine der Wertzuordnung ist, wird für **oumid.name** auf **SalesUnitSymbol** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="15c7a-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="15c7a-163">Optional: Sie können die folgende Zuordnungen hinzufügen, um sicherzustellen, dass Verkaufsangebotspositionen nach Finance and Operations importiert werden, wenn es weder Standardinformationen vom Debitoren noch vom Produkt gibt:</span><span class="sxs-lookup"><span data-stu-id="15c7a-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="15c7a-164">**SiteId** – Ein Standort ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="15c7a-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="15c7a-165">Es gibt keinen Standardvorlagenwert für **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="15c7a-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="15c7a-166">**WarehouseId** – Ein Lager ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen verarbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="15c7a-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="15c7a-167">Es gibt keinen Standardvorlagenwert für **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="15c7a-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="15c7a-168">Vorlagenzuordnung im Datenintegrator</span><span class="sxs-lookup"><span data-stu-id="15c7a-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="15c7a-169">Die Felder **Rabatt**, **Belastungen** und **Steuer** werden durch komplizierte Einstellungen in Finance and Operations gesteuert.</span><span class="sxs-lookup"><span data-stu-id="15c7a-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="15c7a-170">Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung.</span><span class="sxs-lookup"><span data-stu-id="15c7a-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="15c7a-171">Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** von Finance and Operations gehandhabt.</span><span class="sxs-lookup"><span data-stu-id="15c7a-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="15c7a-172">Die Felder **Zahlungsbedingungen**, **Frachtkonditionen**, **Lieferbedingungen**, **Liefermethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="15c7a-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="15c7a-173">Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="15c7a-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="15c7a-174">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="15c7a-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="15c7a-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="15c7a-175">QuoteHeader</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="15c7a-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="15c7a-177">QuoteLine</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="15c7a-179">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="15c7a-179">Related topics</span></span>

[<span data-ttu-id="15c7a-180">Interessent zu Bargeld</span><span class="sxs-lookup"><span data-stu-id="15c7a-180">Prospect to cash</span></span>](prospect-to-cash.md)


