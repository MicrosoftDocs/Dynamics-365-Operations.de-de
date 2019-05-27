---
title: Angebotskopfzeilen und -positionen direkt von Sales zu Finance and Operations synchronisieren
description: Das Thema erklärt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen direkt aus Microsoft Dynamics 365 for Sales mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
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
ms.openlocfilehash: efe943f5c874ed041ce7984272ebc19f57cca6ef
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572580"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="e8f05-103">Verkaufsangebotskopfzeilen und -positionen direkt von Sales mit Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="e8f05-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8f05-104">Das Thema erklärt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen direkt aus Microsoft Dynamics 365 for Sales mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="e8f05-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="e8f05-105">Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Integration von Daten in Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="e8f05-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="e8f05-106">Datenfluss in Interessent nach Bargeld</span><span class="sxs-lookup"><span data-stu-id="e8f05-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="e8f05-107">Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Finance and Operations und Sales hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="e8f05-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="e8f05-108">Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Finance and Operations und Sales.</span><span class="sxs-lookup"><span data-stu-id="e8f05-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="e8f05-109">Die folgende Abbildung zeigt, wie Daten zwischen Finance and Operations und Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e8f05-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="e8f05-110">[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="e8f05-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="e8f05-111">Vorlage und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="e8f05-111">Template and tasks</span></span>

<span data-ttu-id="e8f05-112">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Verkaufsangebotskopfzeilen und -positionen direkt von Sales mit Finance and Operations zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="e8f05-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="e8f05-113">**Name der Vorlage in der Datenintegration:** Verkaufsangebote (Sales zu Finance and Operations) - direkt</span><span class="sxs-lookup"><span data-stu-id="e8f05-113">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="e8f05-114">**Namen der Aufgaben im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="e8f05-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="e8f05-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e8f05-115">QuoteHeader</span></span>
    - <span data-ttu-id="e8f05-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e8f05-116">QuoteLine</span></span>

<span data-ttu-id="e8f05-117">Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Verkaufsangebotskopfzeilen und -positionen erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="e8f05-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="e8f05-118">Produkte (Finance and Operations nach Sales) - Direkt</span><span class="sxs-lookup"><span data-stu-id="e8f05-118">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="e8f05-119">Konten (Sales nach Finance and Operations) - Direkt (wenn verwendet)</span><span class="sxs-lookup"><span data-stu-id="e8f05-119">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="e8f05-120">Kontakte nach Debitoren (Sales nach Finance and Operations) - Direkt (wenn verwendet)</span><span class="sxs-lookup"><span data-stu-id="e8f05-120">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="e8f05-121">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="e8f05-121">Entity set</span></span>

| <span data-ttu-id="e8f05-122">Vertrieb</span><span class="sxs-lookup"><span data-stu-id="e8f05-122">Sales</span></span>        | <span data-ttu-id="e8f05-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e8f05-123">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="e8f05-124">Angebote</span><span class="sxs-lookup"><span data-stu-id="e8f05-124">Quotes</span></span>       | <span data-ttu-id="e8f05-125">CDS-Verkaufsangebotskopf</span><span class="sxs-lookup"><span data-stu-id="e8f05-125">CDS sales quotation header</span></span> |
| <span data-ttu-id="e8f05-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="e8f05-126">QuoteDetails</span></span> | <span data-ttu-id="e8f05-127">CDS-Verkaufsangebotspositionen</span><span class="sxs-lookup"><span data-stu-id="e8f05-127">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="e8f05-128">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="e8f05-128">Entity flow</span></span>

<span data-ttu-id="e8f05-129">Verkaufsangebote werden in Sales erstellt und mit Finance and Operations synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="e8f05-129">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="e8f05-130">Verkaufsangebote aus Sales werden nur synchronisiert, wenn folgende Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="e8f05-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="e8f05-131">Alle Angebote in den Verkaufsangebotspositionen werden extern verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e8f05-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="e8f05-132">Nachdem Sie **Angebot aktivieren** geklickt haben, ist das Verkaufsangebot aktiv.</span><span class="sxs-lookup"><span data-stu-id="e8f05-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e8f05-133">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="e8f05-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="e8f05-134">Das Feld **Verfügt nur über extern verwaltete Produkte** ist der Entität **Angebot** hinzugefügt worden, um stets nachzuverfolgen, ob das Verkaufsangebot vollständig aus extern verwalteten Produkten besteht.</span><span class="sxs-lookup"><span data-stu-id="e8f05-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="e8f05-135">Wenn ein Verkaufsangebot nur aus extern verwalteten Produkten besteht, werden die Produkte in Finance and Operations verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e8f05-135">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="e8f05-136">Mit diesem Verhalten wird sichergestellt, dass Sie nicht versuchen, Verkaufsangebotspositionen mit Produkten zu synchronisieren, die in Finance and Operations unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="e8f05-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="e8f05-137">Alle Angebotsprodukte im Vertriebsangebot werden mit der Information **Verfügt nur über extern verwaltete Produkte** aus der Vertriebsangebotskopfzeile aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e8f05-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="e8f05-138">Diese Informationen können im Feld **Angebot hat nur extern verwaltete Produkte** in der Entität **QuoteDetails** gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e8f05-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="e8f05-139">Ein Rabatt kann zum Angebotsprodukt hinzugefügt werden wird anschließend mit Finance and Operations synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="e8f05-139">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="e8f05-140">Die Felder **Rabatt**, **Belastungen** und **Steuer** in der Kopfzeile werden durch komplizierte Einstellungen in Finance and Operations gesteuert.</span><span class="sxs-lookup"><span data-stu-id="e8f05-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="e8f05-141">Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung.</span><span class="sxs-lookup"><span data-stu-id="e8f05-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="e8f05-142">Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** in Finance and Operations verwaltet und gehandhabt.</span><span class="sxs-lookup"><span data-stu-id="e8f05-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="e8f05-143">In Sales versieht die Lösung die folgenden Felder mit einem Schreibschutz, da die Werte nicht mit Finance and Operations synchronisiert werden:</span><span class="sxs-lookup"><span data-stu-id="e8f05-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="e8f05-144">Schreibgeschützte Felder in de Verkaufsangebotskopfzeile: **Rabatt %**, **Rabatt** und **Frachtbetrag**</span><span class="sxs-lookup"><span data-stu-id="e8f05-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="e8f05-145">Schreibgeschützte Felder auf Angebotsprodukten: **Steuer**</span><span class="sxs-lookup"><span data-stu-id="e8f05-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="e8f05-146">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="e8f05-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="e8f05-147">Vor dem Synchronisieren von Verkaufsangeboten müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:</span><span class="sxs-lookup"><span data-stu-id="e8f05-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="e8f05-148">Einrichtung in Sales</span><span class="sxs-lookup"><span data-stu-id="e8f05-148">Setup in Sales</span></span>

- <span data-ttu-id="e8f05-149">Stellen Sie sicher, dass Berechtigungen für das Team, zu dem der Benutzer (aus Ihren Verbindungseinstellungen in Sales) zugewiesen ist, vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e8f05-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="e8f05-150">Werden Demodaten verwendet, hat in der Regel der Benutzer einen Administratorzugriff aber nicht das Team.</span><span class="sxs-lookup"><span data-stu-id="e8f05-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="e8f05-151">Wenn dieses Team nicht Administratorzugriff hat, wenn Sie das Projekt vom Datenintegrator ausführen, erhalten Sie eine Fehlermeldung, die angibt, dass das Hauptteam fehlt.</span><span class="sxs-lookup"><span data-stu-id="e8f05-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="e8f05-152">Wenn Sie Berechtigungen für das Team einrichten, gehen Sie &gt; zu **Einstellungen** **Sicherheit** &gt; **Teams**, und wählen Sie das zutreffende Team aus.</span><span class="sxs-lookup"><span data-stu-id="e8f05-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="e8f05-153">Wählen Sie **Verwalten Sie Rollen** und dann eine Rolle, die die erforderlichen Berechtigungen verfügt, beispielsweise **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="e8f05-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="e8f05-154">Gehen Sie zu &gt; Sie **Einstellungen** **Verwaltung** &gt; **Systemeinstellungen** &gt; **Sales** zu öffnen, und überprüfen Sie, ob die folgenden Einstellungen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="e8f05-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="e8f05-155">Die Option **Systempreisberechnungssystem verwenden** wird auf **Ja** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8f05-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="e8f05-156">Das Feld **Rabattberechnungsmethode** wird auf **Positionsartikel** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8f05-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="e8f05-157">Einrichtung im Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="e8f05-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="e8f05-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e8f05-158">QuoteHeader</span></span>

- <span data-ttu-id="e8f05-159">Vergewissern Sie sich, dass die erforderliche Zuordnung für **Shipto\_Land** zu **DeliveryAddressCountryRegionISOCode** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e8f05-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="e8f05-160">In der Wertzuordnungen können Sie einen Standardwert definieren, der verwendet wird, wenn der Wert nicht aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="e8f05-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="e8f05-161">Lassen Sie einfach die linken Seite leer, und legen die rechte Seite auf das gewünschte Land oder die Region fest.</span><span class="sxs-lookup"><span data-stu-id="e8f05-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="e8f05-162">Auf diese Weise müssen Sie das Land oder die Region für Zahlungen nationaler Aufträge nicht eingeben.</span><span class="sxs-lookup"><span data-stu-id="e8f05-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="e8f05-163">Der Vorlagenwert ist eine Wertzuordnung, in der verschiedene Länder/Regionen zugeordnet sind, und wo ein leerer Wert dem Wert **USA** entspricht.</span><span class="sxs-lookup"><span data-stu-id="e8f05-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="e8f05-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e8f05-164">QuoteLine</span></span>

- <span data-ttu-id="e8f05-165">Stellen Sie sicher, dass die erforderliche Wertzuordnung für **SalesUnitSymbol** in Finance and Operations vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e8f05-165">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="e8f05-166">Überprüfen Sie, dass die obligatorischen Einheiten in Sales definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e8f05-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="e8f05-167">Ein Vorlagenwert, eine der Wertzuordnung ist, wird für **oumid.name** auf **SalesUnitSymbol** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8f05-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="e8f05-168">Optional: Sie können die folgende Zuordnungen hinzufügen, um sicherzustellen, dass Verkaufsangebotspositionen nach Finance and Operations importiert werden, wenn es weder Standardinformationen vom Debitoren noch vom Produkt gibt:</span><span class="sxs-lookup"><span data-stu-id="e8f05-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="e8f05-169">**SiteId** – Ein Standort ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e8f05-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="e8f05-170">Es gibt keinen Standardvorlagenwert für **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="e8f05-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="e8f05-171">**WarehouseId** – Ein Lager ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen verarbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="e8f05-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="e8f05-172">Es gibt keinen Standardvorlagenwert für **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="e8f05-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="e8f05-173">Vorlagenzuordnung im Datenintegrator</span><span class="sxs-lookup"><span data-stu-id="e8f05-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="e8f05-174">Die Felder **Rabatt**, **Belastungen** und **Steuer** werden durch komplizierte Einstellungen in Finance and Operations gesteuert.</span><span class="sxs-lookup"><span data-stu-id="e8f05-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="e8f05-175">Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung.</span><span class="sxs-lookup"><span data-stu-id="e8f05-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="e8f05-176">Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** von Finance and Operations gehandhabt.</span><span class="sxs-lookup"><span data-stu-id="e8f05-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="e8f05-177">Die Felder **Zahlungsbedingungen**, **Frachtkonditionen**, **Lieferbedingungen**, **Liefermethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="e8f05-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="e8f05-178">Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e8f05-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="e8f05-179">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="e8f05-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="e8f05-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e8f05-180">QuoteHeader</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="e8f05-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e8f05-182">QuoteLine</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="e8f05-184">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e8f05-184">Related topics</span></span>

[<span data-ttu-id="e8f05-185">Interessent zu Bargeld</span><span class="sxs-lookup"><span data-stu-id="e8f05-185">Prospect to cash</span></span>](prospect-to-cash.md)

