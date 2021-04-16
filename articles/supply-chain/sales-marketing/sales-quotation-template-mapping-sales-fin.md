---
title: Verkaufsangebotskopfzeilen und ‑positionen direkt von Sales zu Supply Chain Management synchronisieren
description: Das Thema erklärt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen direkt aus Dynamics 365 Sales mit Dynamics 365 Supply Chain Management zu synchronisieren.
author: ChristianRytt
ms.date: 10/25/2018
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
ms.openlocfilehash: 848464cbc62623502b9b87b9b41dcc17150e85ba
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839004"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="00a0d-103">Verkaufsangebotskopfzeilen und ‑positionen direkt von Sales zu Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="00a0d-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="00a0d-104">Das Thema erklärt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen direkt aus Dynamics 365 Sales mit Dynamics 365 Supply Chain Management zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="00a0d-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="00a0d-105">Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Integration von Daten in Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="00a0d-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="00a0d-106">Datenfluss in Interessent nach Bargeld</span><span class="sxs-lookup"><span data-stu-id="00a0d-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="00a0d-107">Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Supply Chain Management und Sales hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="00a0d-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="00a0d-108">Die „Interessent zu Bargeld“-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Supply Chain Management und Sales.</span><span class="sxs-lookup"><span data-stu-id="00a0d-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="00a0d-109">Die folgende Abbildung zeigt, wie Daten zwischen Supply Chain Management und Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="00a0d-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="00a0d-110">[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="00a0d-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="00a0d-111">Vorlage und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="00a0d-111">Template and tasks</span></span>

<span data-ttu-id="00a0d-112">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Verkaufsangebotskopfzeilen und -positionen direkt von Sales mit Supply Chain Management zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="00a0d-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="00a0d-113">**Name der Vorlage in der Datenintegration:** Verkaufsangebote (Sales zu Supply Chain Management) - Direkt</span><span class="sxs-lookup"><span data-stu-id="00a0d-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="00a0d-114">**Namen der Aufgaben im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="00a0d-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="00a0d-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="00a0d-115">QuoteHeader</span></span>
    - <span data-ttu-id="00a0d-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="00a0d-116">QuoteLine</span></span>

<span data-ttu-id="00a0d-117">Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Verkaufsangebotskopfzeilen und -positionen erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="00a0d-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="00a0d-118">Produkte (Supply Chain Management zu Sales) – Direkt</span><span class="sxs-lookup"><span data-stu-id="00a0d-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="00a0d-119">Konten (Sales zu Supply Chain Management) – Direkt (falls verwendet)</span><span class="sxs-lookup"><span data-stu-id="00a0d-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="00a0d-120">Kontakte zu Kunden (Sales zu Supply Chain Management) – Direkt (falls verwendet)</span><span class="sxs-lookup"><span data-stu-id="00a0d-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="00a0d-121">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="00a0d-121">Entity set</span></span>

| <span data-ttu-id="00a0d-122">Verk.</span><span class="sxs-lookup"><span data-stu-id="00a0d-122">Sales</span></span>        | <span data-ttu-id="00a0d-123">Lieferkettenverwaltung</span><span class="sxs-lookup"><span data-stu-id="00a0d-123">Supply Chain Management</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="00a0d-124">Angebote</span><span class="sxs-lookup"><span data-stu-id="00a0d-124">Quotes</span></span>       | <span data-ttu-id="00a0d-125">Dataverse-Verkaufsangebotskopf</span><span class="sxs-lookup"><span data-stu-id="00a0d-125">Dataverse sales quotation header</span></span> |
| <span data-ttu-id="00a0d-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="00a0d-126">QuoteDetails</span></span> | <span data-ttu-id="00a0d-127">Dataverse-Verkaufsangebotspositionen</span><span class="sxs-lookup"><span data-stu-id="00a0d-127">Dataverse sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="00a0d-128">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="00a0d-128">Entity flow</span></span>

<span data-ttu-id="00a0d-129">Verkaufsangebote werden in Sales erstellt und mit Supply Chain Management synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="00a0d-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="00a0d-130">Verkaufsangebote aus Sales werden nur synchronisiert, wenn folgende Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="00a0d-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="00a0d-131">Alle Angebote in den Verkaufsangebotspositionen werden extern verwaltet.</span><span class="sxs-lookup"><span data-stu-id="00a0d-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="00a0d-132">Nachdem Sie **Angebot aktivieren** geklickt haben, ist das Verkaufsangebot aktiv.</span><span class="sxs-lookup"><span data-stu-id="00a0d-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="00a0d-133">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="00a0d-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="00a0d-134">Das Feld **Verfügt nur über extern verwaltete Produkte** ist der Entität **Angebot** hinzugefügt worden, um stets nachzuverfolgen, ob das Verkaufsangebot vollständig aus extern verwalteten Produkten besteht.</span><span class="sxs-lookup"><span data-stu-id="00a0d-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="00a0d-135">Wenn ein Verkaufsangebot nur aus extern verwalteten Produkten besteht, werden die Produkte in Supply Chain Management verwaltet.</span><span class="sxs-lookup"><span data-stu-id="00a0d-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="00a0d-136">Mit diesem Verhalten wird sichergestellt, dass Sie nicht versuchen, Verkaufsangebotspositionen mit Produkten zu synchronisieren, die in Supply Chain Management unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="00a0d-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="00a0d-137">Alle Angebotsprodukte im Vertriebsangebot werden mit der Information **Verfügt nur über extern verwaltete Produkte** aus der Vertriebsangebotskopfzeile aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="00a0d-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="00a0d-138">Diese Informationen können im Feld **Angebot hat nur extern verwaltete Produkte** in der Entität **QuoteDetails** gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="00a0d-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="00a0d-139">Ein Rabatt kann zum Angebotsprodukt hinzugefügt werden wird anschließend mit Supply Chain Management synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="00a0d-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="00a0d-140">Die Felder **Rabatt**, **Belastungen** und **Steuer** in der Kopfzeile werden durch komplizierte Einstellungen in Supply Chain Management gesteuert.</span><span class="sxs-lookup"><span data-stu-id="00a0d-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="00a0d-141">Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung.</span><span class="sxs-lookup"><span data-stu-id="00a0d-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="00a0d-142">Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** in Supply Chain Management verwaltet und gehandhabt.</span><span class="sxs-lookup"><span data-stu-id="00a0d-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="00a0d-143">In Sales versieht die Lösung die folgenden Felder mit einem Schreibschutz, da die Werte nicht mit Supply Chain Management synchronisiert werden:</span><span class="sxs-lookup"><span data-stu-id="00a0d-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="00a0d-144">Schreibgeschützte Felder in de Verkaufsangebotskopfzeile: **Rabatt %**, **Rabatt** und **Frachtbetrag**</span><span class="sxs-lookup"><span data-stu-id="00a0d-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="00a0d-145">Schreibgeschützte Felder auf Angebotsprodukten: **Steuer**</span><span class="sxs-lookup"><span data-stu-id="00a0d-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="00a0d-146">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="00a0d-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="00a0d-147">Vor dem Synchronisieren von Verkaufsangeboten müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:</span><span class="sxs-lookup"><span data-stu-id="00a0d-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="00a0d-148">Einrichtung in Sales</span><span class="sxs-lookup"><span data-stu-id="00a0d-148">Setup in Sales</span></span>

- <span data-ttu-id="00a0d-149">Stellen Sie sicher, dass Berechtigungen für das Team, zu dem der Benutzer (aus Ihren Verbindungseinstellungen in Sales) zugewiesen ist, vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="00a0d-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="00a0d-150">Werden Demodaten verwendet, hat in der Regel der Benutzer einen Administratorzugriff aber nicht das Team.</span><span class="sxs-lookup"><span data-stu-id="00a0d-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="00a0d-151">Wenn dieses Team nicht Administratorzugriff hat, wenn Sie das Projekt vom Datenintegrator ausführen, erhalten Sie eine Fehlermeldung, die angibt, dass das Hauptteam fehlt.</span><span class="sxs-lookup"><span data-stu-id="00a0d-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="00a0d-152">Wenn Sie Berechtigungen für das Team einrichten, gehen Sie &gt; zu **Einstellungen** **Sicherheit** &gt; **Teams**, und wählen Sie das zutreffende Team aus.</span><span class="sxs-lookup"><span data-stu-id="00a0d-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="00a0d-153">Wählen Sie **Verwalten Sie Rollen** und dann eine Rolle, die die erforderlichen Berechtigungen verfügt, beispielsweise **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="00a0d-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="00a0d-154">Gehen Sie zu &gt; Sie **Einstellungen** **Verwaltung** &gt; **Systemeinstellungen** &gt; **Sales** zu öffnen, und überprüfen Sie, ob die folgenden Einstellungen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="00a0d-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="00a0d-155">Die Option **Systempreisberechnungssystem verwenden** wird auf **Ja** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="00a0d-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="00a0d-156">Das Feld **Rabattberechnungsmethode** wird auf **Positionsartikel** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="00a0d-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="00a0d-157">Einrichtung im Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="00a0d-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="00a0d-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="00a0d-158">QuoteHeader</span></span>

- <span data-ttu-id="00a0d-159">Vergewissern Sie sich, dass die erforderliche Zuordnung für **Shipto\_Land** zu **DeliveryAddressCountryRegionISOCode** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="00a0d-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="00a0d-160">In der Wertzuordnungen können Sie einen Standardwert definieren, der verwendet wird, wenn der Wert nicht aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="00a0d-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="00a0d-161">Lassen Sie einfach die linken Seite leer, und legen die rechte Seite auf das gewünschte Land oder die Region fest.</span><span class="sxs-lookup"><span data-stu-id="00a0d-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="00a0d-162">Auf diese Weise müssen Sie das Land oder die Region für Zahlungen nationaler Aufträge nicht eingeben.</span><span class="sxs-lookup"><span data-stu-id="00a0d-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="00a0d-163">Der Vorlagenwert ist eine Wertzuordnung, in der verschiedene Länder/Regionen zugeordnet sind, und wo ein leerer Wert dem Wert **USA** entspricht.</span><span class="sxs-lookup"><span data-stu-id="00a0d-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="00a0d-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="00a0d-164">QuoteLine</span></span>

- <span data-ttu-id="00a0d-165">Stellen Sie sicher, dass die erforderliche Wertzuordnung für **SalesUnitSymbol** in Supply Chain Management vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="00a0d-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="00a0d-166">Überprüfen Sie, dass die obligatorischen Einheiten in Sales definiert sind.</span><span class="sxs-lookup"><span data-stu-id="00a0d-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="00a0d-167">Ein Vorlagenwert, eine der Wertzuordnung ist, wird für **oumid.name** auf **SalesUnitSymbol** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="00a0d-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="00a0d-168">Optional: Sie können die folgende Zuordnungen hinzufügen, um sicherzustellen, dass Verkaufsangebotspositionen nach Supply Chain Management importiert werden, wenn es weder Standardinformationen vom Debitoren noch vom Produkt gibt:</span><span class="sxs-lookup"><span data-stu-id="00a0d-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="00a0d-169">**SiteId** – Ein Standort ist erforderlich, um in Supply Chain Management Angebots- und Vertriebsauftragspositionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="00a0d-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="00a0d-170">Es gibt keinen Standardvorlagenwert für **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="00a0d-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="00a0d-171">**WarehouseId** – Ein Lager ist erforderlich, um in Supply Chain Management Angebots- und Vertriebsauftragspositionen verarbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="00a0d-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="00a0d-172">Es gibt keinen Standardvorlagenwert für **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="00a0d-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="00a0d-173">Vorlagenzuordnung im Datenintegrator</span><span class="sxs-lookup"><span data-stu-id="00a0d-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="00a0d-174">Die Felder **Rabatt**, **Belastungen** und **Steuer** werden durch komplizierte Einstellungen in Supply Chain Management gesteuert.</span><span class="sxs-lookup"><span data-stu-id="00a0d-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="00a0d-175">Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung.</span><span class="sxs-lookup"><span data-stu-id="00a0d-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="00a0d-176">Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** von Supply Chain Management gehandhabt.</span><span class="sxs-lookup"><span data-stu-id="00a0d-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="00a0d-177">Die Felder **Zahlungsbedingungen**, **Frachtkonditionen**, **Lieferbedingungen**, **Liefermethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="00a0d-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="00a0d-178">Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="00a0d-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="00a0d-179">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="00a0d-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="00a0d-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="00a0d-180">QuoteHeader</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="00a0d-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="00a0d-182">QuoteLine</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="00a0d-184">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="00a0d-184">Related topics</span></span>

[<span data-ttu-id="00a0d-185">Interessent zu Bargeld</span><span class="sxs-lookup"><span data-stu-id="00a0d-185">Prospect to cash</span></span>](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]