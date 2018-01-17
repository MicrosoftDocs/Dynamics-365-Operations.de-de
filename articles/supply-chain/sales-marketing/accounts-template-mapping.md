---
title: "Synchronisierung von Konten aus Sales für Kunden in Finance and Operations"
description: "Das Thema beschreibt die Vorlagen und die grundlegenden Aufgaben, die verwendet werden, um Konten aus Microsoft Dynamics 365 for Sales für Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, zu synchronisieren."
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
ms.openlocfilehash: f1ddb3853d1cf0613ab324bb35c3f15ad1f4f984
ms.contentlocale: de-de
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="06cc3-103">Synchronisierung von Konten aus Sales für Kunden in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="06cc3-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="06cc3-104">Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="06cc3-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="06cc3-105">Das Thema beschreibt die Vorlagen und die grundlegenden Aufgaben, die verwendet werden, um Konten aus Microsoft Dynamics 365 for Sales (Sales) für Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations), zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="06cc3-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="06cc3-106">Vorlage und Aufgabe</span><span class="sxs-lookup"><span data-stu-id="06cc3-106">Template and task</span></span>

<span data-ttu-id="06cc3-107">Die folgenden Vorlagen und grundlegenden Aufgaben werden für die Synchronisierung von Konten aus Sales für Kunden in Finance and Operations verwendet:</span><span class="sxs-lookup"><span data-stu-id="06cc3-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="06cc3-108">**Name der Vorlage:** Konten (Sales in Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="06cc3-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="06cc3-109">**Name der Aufgabe im Projekt:** Konten – Konto – Kunden</span><span class="sxs-lookup"><span data-stu-id="06cc3-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="06cc3-110">Synchronisierungsaufgaben vor der Synchronisierung von Konto/Kunde: Keine</span><span class="sxs-lookup"><span data-stu-id="06cc3-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="06cc3-111">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="06cc3-111">Entity set</span></span>

| <span data-ttu-id="06cc3-112">Vertrieb</span><span class="sxs-lookup"><span data-stu-id="06cc3-112">Sales</span></span>    | <span data-ttu-id="06cc3-113">CDS</span><span class="sxs-lookup"><span data-stu-id="06cc3-113">CDS</span></span>     | <span data-ttu-id="06cc3-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="06cc3-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="06cc3-115">Konten</span><span class="sxs-lookup"><span data-stu-id="06cc3-115">Accounts</span></span> | <span data-ttu-id="06cc3-116">Konto</span><span class="sxs-lookup"><span data-stu-id="06cc3-116">Account</span></span> | <span data-ttu-id="06cc3-117">Debitoren</span><span class="sxs-lookup"><span data-stu-id="06cc3-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="06cc3-118">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="06cc3-118">Entity flow</span></span>

<span data-ttu-id="06cc3-119">Konten werden in Sales verwaltet und in Finance and Operations als Kunden synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="06cc3-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="06cc3-120">Die Eigenschaft **Is Externally Maintained** dieser Kunden wird auf **Ja** gesetzt, um die Kunden nachzuverfolgen, die aus Sales stammen.</span><span class="sxs-lookup"><span data-stu-id="06cc3-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="06cc3-121">Während der Rechnungsstellung werden diese Informationen verwendet, um Rechnungen zu filtern, die für Sales synchronisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="06cc3-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="06cc3-122">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="06cc3-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="06cc3-123">Das Feld **Kontonummer** steht auf der Seite **Konto** zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="06cc3-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="06cc3-124">Es wurde zu einem natürlichen und eindeutigen Schlüssel für die Unterstützung der Integration gemacht.</span><span class="sxs-lookup"><span data-stu-id="06cc3-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="06cc3-125">Die natürliche Schlüsselfunktion der Customer Relationship Management (CRM)-Lösung wirkt sich möglicherweise auf Kunden aus, die das Feld **Kontonummer** bereits verwenden, aber keine eindeutigen **Kontonummer**-Werte pro Konto verwenden.</span><span class="sxs-lookup"><span data-stu-id="06cc3-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="06cc3-126">Derzeit unterstützt die Integrationslösung diesen Fall nicht.</span><span class="sxs-lookup"><span data-stu-id="06cc3-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="06cc3-127">Wenn ein neues Konto angelegt wird und noch kein **Kontonummer**-Wert vorhanden ist, wird es automatisch unter Verwendung einer fortlaufenden Nummerierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="06cc3-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="06cc3-128">Der Wert besteht aus **ACC**, gefolgt von einer aufsteigenden fortlaufenden Nummerierung und einem Suffix aus sechs Zeichen.</span><span class="sxs-lookup"><span data-stu-id="06cc3-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="06cc3-129">Beispiel: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="06cc3-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="06cc3-130">Wenn die Integrationslösung für Sales angewendet wird, füllt ein Upgrade-Skript das Feld **Kontonummer** für in Sales vorhandene Konten aus.</span><span class="sxs-lookup"><span data-stu-id="06cc3-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="06cc3-131">Wenn es keine **Kontonummer**-Werte gibt, wird die zuvor beschriebene laufende Nummerierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="06cc3-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="06cc3-132">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="06cc3-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="06cc3-133">**CustomerGroupId** Zuordnung von **CDS &gt; Ziele** muss aktualisiert werden, um einen gültigen Wert in Finance and Operations zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="06cc3-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="06cc3-134">Sie können einen Standardwert spezifizieren, oder den Wert unter Verwendung einer Wertezuordnung festlegen.</span><span class="sxs-lookup"><span data-stu-id="06cc3-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="06cc3-135">Der Standardvorlagenwert ist **10**.</span><span class="sxs-lookup"><span data-stu-id="06cc3-135">The default template value is **10**.</span></span>
- <span data-ttu-id="06cc3-136">In Finance and Operations ist ein **Address/Länder/Region-Code** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="06cc3-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="06cc3-137">Um Synchronisierungsfehler zu vermeiden, können Sie in der **CDS &gt; Ziel**-Zuordnung einen Standardwert vorgeben.</span><span class="sxs-lookup"><span data-stu-id="06cc3-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="06cc3-138">Der Standardwert wird verwendet, wenn das Feld in Sales leer geblieben ist.</span><span class="sxs-lookup"><span data-stu-id="06cc3-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="06cc3-139">Der Standardvorlagewert für **AddressCountryRegionISOCode** lautet **USA**.</span><span class="sxs-lookup"><span data-stu-id="06cc3-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="06cc3-140">Der Standardvorlagewert für **DeliveryAddressCountryRegionISOCode** lautet **USA**.</span><span class="sxs-lookup"><span data-stu-id="06cc3-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="06cc3-141">Durch Hinzufügen der folgenden Zuordnungen von **CDS &gt; Ziel** können Sie die Anzahl der erforderlichen manuellen Updates in Finance and Operations reduzieren.</span><span class="sxs-lookup"><span data-stu-id="06cc3-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="06cc3-142">Sie können einen Standardwert oder eine Wertzuordnung beispielsweise aus **Land/Region** oder **Stadt** verwenden.</span><span class="sxs-lookup"><span data-stu-id="06cc3-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="06cc3-143">**SiteId** – Ein Standort ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="06cc3-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="06cc3-144">Es kann ein Standardstandort vom Produkt oder vom Kunden aus dem Auftragskopf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06cc3-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="06cc3-145">Der Standardvorlagewert für **SiteId** lautet **1**.</span><span class="sxs-lookup"><span data-stu-id="06cc3-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="06cc3-146">**WarehouseId** – Ein Lager ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen verarbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="06cc3-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="06cc3-147">Es kann ein Standardlager vom Produkt oder vom Kunden aus dem Auftragskopf in Finance and Operations verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06cc3-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="06cc3-148">Der Standardvorlagewert für **WarehouseId** lautet **13**.</span><span class="sxs-lookup"><span data-stu-id="06cc3-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="06cc3-149">**LanguageId** – Eine Sprache ist erforderlich, um in Finance and Operations Angebote und Vertriebsaufträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="06cc3-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="06cc3-150">Standardmäßig wird die Sprache aus dem Auftragskopf des Kunden verwendet.</span><span class="sxs-lookup"><span data-stu-id="06cc3-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="06cc3-151">Der Standardvorlagewert für **LanguageId** lautet **en-us**.</span><span class="sxs-lookup"><span data-stu-id="06cc3-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="06cc3-152">Aktualisieren Sie die CDS Organisations-ID (**Organization_OrganizationId**) in der **Quell &gt; CDS**-Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="06cc3-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="06cc3-153">Der Standardvorlagenwert ist **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="06cc3-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="06cc3-154">Vorlagenzuordnung im Datenintegrator</span><span class="sxs-lookup"><span data-stu-id="06cc3-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="06cc3-155">Die Felder **Zahlungsbedingungen**, **Frachtbedingungen**, **Lieferbedingungen**, **Liefermethode** und **Bereitstellungsmodus** sind nicht in den Standardzuordnungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="06cc3-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="06cc3-156">Um diese Felder zuzuordnen, müssen Sie eine Wertzuordnung einrichten.</span><span class="sxs-lookup"><span data-stu-id="06cc3-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="06cc3-157">Wertzuordnungen sind spezifisch für die Daten in den Organisationen, zwischen denen die Entität synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="06cc3-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="06cc3-158">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="06cc3-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/accounts-template-mapping-data-integrator-1.png)

![Vorlagenzuordnung für Konten im Datenintegrator](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="06cc3-161">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="06cc3-161">Related topics</span></span>

[<span data-ttu-id="06cc3-162">Synchronisierung von Produkten aus Finance and Operations für Produkte in Sales</span><span class="sxs-lookup"><span data-stu-id="06cc3-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="06cc3-163">Synchronisierung von Kontakten aus Sales für Kontakte oder Kunden in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="06cc3-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="06cc3-164">Verkaufsangebotskopfzeilen und -positionen von Sales mit Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="06cc3-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="06cc3-165">Auftragskopfzeilen und -positionen von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="06cc3-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="06cc3-166">Verkaufsrechnungszeilen und -positionen von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="06cc3-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




