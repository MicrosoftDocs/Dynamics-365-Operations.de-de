---
title: Synchronisieren von Verkaufsangebotskopfzeilen und -positionen von Sales mit Finance and Operations
description: "Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen von Microsoft Dynamics 365 for Sales mit Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, zu synchronisieren."
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
ms.openlocfilehash: 172a3da1b6d90a25ea9ebd14265e70e4a6f9bd70
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="f7fe2-103">Synchronisieren von Verkaufsangebotskopfzeilen und -positionen von Sales mit Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f7fe2-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="f7fe2-104">Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="f7fe2-105">Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen von Microsoft Dynamics 365 for Sales (Sales) mit Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, (Finance and Operations) zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="f7fe2-106">Vorlage und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="f7fe2-106">Template and tasks</span></span>

<span data-ttu-id="f7fe2-107">Die folgenden Vorlagen und die zugrunde liegenden Aufgaben werden verwendet, um Verkaufsangebotskopfzeilen und -positionen von Sales mit Finance and Operations zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="f7fe2-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="f7fe2-108">**Name der Vorlage:** Verkaufsangebote (Sales mit Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="f7fe2-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="f7fe2-109">**Namen der Aufgaben im Projekt:**</span><span class="sxs-lookup"><span data-stu-id="f7fe2-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="f7fe2-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="f7fe2-110">QuoteHeader</span></span>
    - <span data-ttu-id="f7fe2-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="f7fe2-111">QuoteLine</span></span>

<span data-ttu-id="f7fe2-112">Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Verkaufsangebotskopfzeilen und -positionen erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="f7fe2-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="f7fe2-113">Produkte</span><span class="sxs-lookup"><span data-stu-id="f7fe2-113">Products</span></span>
- <span data-ttu-id="f7fe2-114">Konten (sofern verwendet)</span><span class="sxs-lookup"><span data-stu-id="f7fe2-114">Accounts (if used)</span></span>
- <span data-ttu-id="f7fe2-115">Kontakte (sofern verwendet)</span><span class="sxs-lookup"><span data-stu-id="f7fe2-115">Contacts (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="f7fe2-116">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="f7fe2-116">Entity set</span></span>

| <span data-ttu-id="f7fe2-117">Vertrieb</span><span class="sxs-lookup"><span data-stu-id="f7fe2-117">Sales</span></span>        | <span data-ttu-id="f7fe2-118">CDS</span><span class="sxs-lookup"><span data-stu-id="f7fe2-118">CDS</span></span>           | <span data-ttu-id="f7fe2-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f7fe2-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="f7fe2-120">Angebote</span><span class="sxs-lookup"><span data-stu-id="f7fe2-120">Quotes</span></span>       | <span data-ttu-id="f7fe2-121">Angebot</span><span class="sxs-lookup"><span data-stu-id="f7fe2-121">Quotation</span></span>     | <span data-ttu-id="f7fe2-122">Verkaufsangebotskopfzeilen</span><span class="sxs-lookup"><span data-stu-id="f7fe2-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="f7fe2-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="f7fe2-123">QuoteDetails</span></span> | <span data-ttu-id="f7fe2-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="f7fe2-124">QuotationLine</span></span> | <span data-ttu-id="f7fe2-125">CDS-Verkaufsangebotspositionen</span><span class="sxs-lookup"><span data-stu-id="f7fe2-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="f7fe2-126">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="f7fe2-126">Entity flow</span></span>

<span data-ttu-id="f7fe2-127">Verkaufsangebote werden in Sales erstellt und mit Finance and Operations synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="f7fe2-128">Verkaufsangebote aus Sales werden nur synchronisiert, wenn folgende Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="f7fe2-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="f7fe2-129">Alle Produkte in den Verkaufsangebotspositionen werden extern verwaltet.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="f7fe2-130">Das Verkaufsangebot ist aktiv oder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="f7fe2-131">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="f7fe2-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="f7fe2-132">Das Feld **Verfügt nur über extern verwaltete Produkte** ist der Entität „Angebot” hinzugefügt worden, um stets nachzuverfolgen, ob das Verkaufsangebot vollständig aus extern verwalteten Produkten besteht.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="f7fe2-133">Wenn ein Verkaufsangebot nur aus extern verwalteten Produkten besteht, werden die Produkte in Finance and Operations verwaltet.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="f7fe2-134">Mit diesem Verhalten wird sichergestellt, dass Sie nicht versuchen, Verkaufsangebotspositionen mit Produkten zu synchronisieren, die in Finance and Operations unbekannt sind.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="f7fe2-135">Alle Produkte und Positionen im Angebot werden mit der Information **Verfügt nur über extern verwaltete Produkte** aus der Angebotskopfzeile aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="f7fe2-136">Diese Informationen können im Feld **Angebot hat nur extern verwaltete Produkte** in der Entität „Angebotsanforderungsposition” gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="f7fe2-137">Die Felder **Rabatt**, **Belastungen** und **Steuer** werden durch komplizierte Einstellungen in Finance and Operations gesteuert.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="f7fe2-138">Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="f7fe2-139">Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** von Finance and Operations gemastert und gehandhabt.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="f7fe2-140">In Sales versieht die Lösung die folgenden Felder mit einem Schreibschutz, da die Werte nicht mit Finance and Operations synchronisiert werden:</span><span class="sxs-lookup"><span data-stu-id="f7fe2-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="f7fe2-141">**Schreibgeschützte Felder in de Verkaufsangebotskopfzeile:** Rabatt %, Rabatt, Frachtgebühr</span><span class="sxs-lookup"><span data-stu-id="f7fe2-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="f7fe2-142">**Schreibgeschützte Felder in Verkaufsangebotspositionen:** Steuer</span><span class="sxs-lookup"><span data-stu-id="f7fe2-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="f7fe2-143">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="f7fe2-143">Preconditions and mapping setup</span></span>

- <span data-ttu-id="f7fe2-144">Bevor Sie Verkaufsangebote in Sales synchronisieren, wechseln Sie zu **Einstellungen** &gt; **Verwaltung** &gt; **Systemeinstellungen** &gt; **Vertrieb**, und stellen Sie sicher, dass das Feld **Rabattberechnungsmethode** auf **Pro Einheit** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-144">Before you synchronize sales quotations, in Sales, go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="f7fe2-145">Diese Einstellung stellt sicher, dass der Positionsartikelrabatt von Sales mit der Einstellung in Finance and Operations übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-145">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="f7fe2-146">Andernfalls ist der Rabatt in Finance and Operations nicht korrekt, da Finance and Operations den Rabatt als Rabatt pro Einheit liest, selbst wenn es ein Rabatt pro Position in Sales war.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-146">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>
- <span data-ttu-id="f7fe2-147">In Finance and Operations wechseln Sie zu **Debitoren** &gt; **Einstellungen** &gt; **Debitorenparameter**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-147">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="f7fe2-148">Auf der Registerkarte **Nummernkreis** wählen Sie den Nummernkreis für Verkaufsangebote aus, und klicken Sie dann auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-148">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="f7fe2-149">Legen Sie dann unter **Allgemeine Einstellungen** das Feld **Manuell** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-149">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="f7fe2-150">In Finance and Operations wechseln Sie zu **Debitoren** &gt; **Einstellungen** &gt; **Debitorenparameter**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-150">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="f7fe2-151">Legen Sie anschließend auf der Registerkarte **Lieferungen** das Feld **Lieferdatumskontrolle** auf **Keine** fest.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-151">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="f7fe2-152">Diese Einstellung trägt dazu bei zu verhindern, dass die Synchronisierung für Verkaufsangebote fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-152">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="f7fe2-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="f7fe2-153">QuoteHeader</span></span>

- <span data-ttu-id="f7fe2-154">Das Feld **Angefordertes Lieferdatum** ist in Finance and Operations erforderlich, und die Synchronisierung schlägt fehl, wenn das Feld leer bleibt.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-154">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="f7fe2-155">Um dieses Problem zu verhindern, wenn das Feld leer ist, wird ein Standarddatum von **Quelle &gt; CDS** übernommen.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-155">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="f7fe2-156">Das Datum sollte auf einen bevorzugten Wert aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-156">The date should be updated to a preferred value.</span></span> <span data-ttu-id="f7fe2-157">Gegenwärtig können Sie keinen Wert wie beispielsweise **Heute** eingeben, um das heutige Datum anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-157">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="f7fe2-158">Sie müssen ein spezifisches Datum eingeben.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-158">You must enter a specific date.</span></span> <span data-ttu-id="f7fe2-159">Der Standardvorlagenwert für **Angefordertes Lieferdatum** ist **01.01.2020**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-159">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="f7fe2-160">Das Feld **Adressland-Regionscode** ist in Finance and Operations erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-160">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="f7fe2-161">Um Synchronisierungsfehler zu vermeiden, können Sie einen Standardwert angeben, der verwendet wird, wenn das Feld in Sales leer bleibt.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-161">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="f7fe2-162">Dieser Standardwert ist auch hilfreich, da Sie im Feld **Landregion** keinen Wert manuell für lokale Adressen eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-162">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="f7fe2-163">Es gibt keinen Standardvorlagenwert für **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-163">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="f7fe2-164">Aktualisieren Sie die Zuordnung für **CDS Organisationskennung** in **Quelle &gt; CDS**, sodass sie **CD-Organisation** in der Organisationsentität entspricht:</span><span class="sxs-lookup"><span data-stu-id="f7fe2-164">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="f7fe2-165">Der Standardvorlagenwert für **Organization_OrganizationId** ist **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-165">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="f7fe2-166">Der Standardvorlagenwert für **Account_Organization_OrganizationId** ist **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-166">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="f7fe2-167">Der Standardvorlagenwert für **InvoiceAccount_OrganizationId** ist **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-167">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

### <a name="quoteline"></a><span data-ttu-id="f7fe2-168">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="f7fe2-168">QuoteLine</span></span>

- <span data-ttu-id="f7fe2-169">Aktualisieren Sie die Zuordnung für **CDS Organisationskennung** in **Quelle &gt; CDS**, sodass sie **CD-Organisation** in der Organisationsentität entspricht:</span><span class="sxs-lookup"><span data-stu-id="f7fe2-169">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="f7fe2-170">Der Standardvorlagenwert für **Organization_OrganizationId** ist **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-170">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="f7fe2-171">Der Standardvorlagenwert für **Product_Organization_Organization_OrganizationId** ist **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-171">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="f7fe2-172">Der Standardvorlagenwert für **Quotation_Organization_Organization_OrganizationId** ist **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-172">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="f7fe2-173">Das Feld **Angefordertes Lieferdatum** ist in Finance and Operations erforderlich, und die Synchronisierung schlägt fehl, wenn das Feld leer bleibt.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-173">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="f7fe2-174">Um dieses Problem zu verhindern, wenn das Feld leer ist, wird ein Standarddatum von **Quelle &gt; CDS** übernommen.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-174">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="f7fe2-175">Das Datum sollte auf einen bevorzugten Wert aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-175">The date should be updated to a preferred value.</span></span> <span data-ttu-id="f7fe2-176">Gegenwärtig können Sie keinen Wert wie beispielsweise **Heute** eingeben, um das heutige Datum anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-176">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="f7fe2-177">Sie müssen ein spezifisches Datum eingeben.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-177">You must enter a specific date.</span></span> <span data-ttu-id="f7fe2-178">Der Standardvorlagenwert für **Angefordertes Lieferdatum** ist **01.01.2020**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-178">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="f7fe2-179">Sie können die folgende Zuordnungen von **CDS &gt; Ziel** hinzufügen, um sicherzustellen, dass Angebotspositionen nach Finance and Operations importiert werden, wenn es weder Standardinformationen vom Debitoren noch vom Produkt gibt:</span><span class="sxs-lookup"><span data-stu-id="f7fe2-179">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="f7fe2-180">**SiteId** – Ein Standort ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-180">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="f7fe2-181">Es gibt keinen Standardvorlagenwert für **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-181">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="f7fe2-182">**WarehouseId** – Ein Lager ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen verarbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-182">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="f7fe2-183">Es gibt keinen Standardvorlagenwert für **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-183">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="f7fe2-184">Vergewissern Sie sich, dass die erforderliche Wertzuordnung für die Verkaufsmaßeinheit (ME) in Finance and Operations in der Zuordnung **CDS &gt; Ziel** für **Mengenmaßeinheit** bis **VERKAUFSEINHEITSSYMBOL** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-184">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="f7fe2-185">Vorlagenzuordnung im Datenintegrator</span><span class="sxs-lookup"><span data-stu-id="f7fe2-185">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="f7fe2-186">Die Felder **Rabatt**, **Belastungen** und **Steuer** werden durch komplizierte Einstellungen in Finance and Operations gesteuert.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-186">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="f7fe2-187">Diese Einstellungen unterstützen aktuell nicht die Integrationszuordnung.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-187">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="f7fe2-188">Im aktuellen Entwurf werden die Felder **Preis**, **Rabatt**, **Belastung** und **Steuer** von Finance and Operations gehandhabt.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-188">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="f7fe2-189">Die Felder **Zahlungsbedingungen**, **Frachtkonditionen**, **Lieferbedingungen**, **Liefermethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-189">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="f7fe2-190">Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-190">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="f7fe2-191">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="f7fe2-191">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="f7fe2-192">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="f7fe2-192">QuoteHeader</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="f7fe2-195">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="f7fe2-195">QuoteLine</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="f7fe2-198">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f7fe2-198">Related topics</span></span>

[<span data-ttu-id="f7fe2-199">Synchronisierung von Produkten aus Finance and Operations für Produkte in Sales</span><span class="sxs-lookup"><span data-stu-id="f7fe2-199">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="f7fe2-200">Synchronisierung von Konten aus Sales für Kunden in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f7fe2-200">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="f7fe2-201">Synchronisierung von Kontakten aus Sales für Kontakte oder Kunden in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f7fe2-201">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



