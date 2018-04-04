---
title: Konten von Sales direkt mit Debitoren in Finance and Operations synchronisieren
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Konten aus Microsoft Dynamics 365 for Sales mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: fb694db32638756328623c186594cf5ba2e7d6b8
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="2570e-103">Konten von Sales direkt mit Debitoren in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="2570e-103">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="2570e-104">Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="2570e-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="2570e-105">Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Konten direkt aus Microsoft Dynamics 365 for Sales mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="2570e-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="2570e-106">Datenfluss in Interessent nach Bargeld</span><span class="sxs-lookup"><span data-stu-id="2570e-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="2570e-107">Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Finance and Operations und Sales hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="2570e-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span>  <span data-ttu-id="2570e-108">Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Finance and Operations und Sales.</span><span class="sxs-lookup"><span data-stu-id="2570e-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="2570e-109">Die folgende Abbildung zeigt, wie Daten zwischen Finance and Operations und Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2570e-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="2570e-110">[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="2570e-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="2570e-111">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="2570e-111">Templates and tasks</span></span>

<span data-ttu-id="2570e-112">Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [PowerApps-Administrator-Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="2570e-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="2570e-113">Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2570e-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="2570e-114">Die folgende Vorlage und grundlegenden Aufgabe werden für die Synchronisierung von Konten aus Sales für Kunden in Finance and Operations verwendet:</span><span class="sxs-lookup"><span data-stu-id="2570e-114">The following template and underlying task are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="2570e-115">**Name der Vorlage in der Datenintegration:** Konten (Sales zu Finance and Operations) - direkt</span><span class="sxs-lookup"><span data-stu-id="2570e-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="2570e-116">**Name der Aufgabe im Projekt:** Konten – Kunden</span><span class="sxs-lookup"><span data-stu-id="2570e-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="2570e-117">Keine Synchronisierungsaufgaben sind erforderlich, damit Konto-Kunde-Synchronisierung auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="2570e-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="2570e-118">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="2570e-118">Entity set</span></span>

| <span data-ttu-id="2570e-119">Vertrieb</span><span class="sxs-lookup"><span data-stu-id="2570e-119">Sales</span></span>    | <span data-ttu-id="2570e-120">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2570e-120">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="2570e-121">Konten</span><span class="sxs-lookup"><span data-stu-id="2570e-121">Accounts</span></span> | <span data-ttu-id="2570e-122">Debitoren V2</span><span class="sxs-lookup"><span data-stu-id="2570e-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="2570e-123">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="2570e-123">Entity flow</span></span>

<span data-ttu-id="2570e-124">Konten werden in Sales verwaltet und in Finance and Operations als Kunden synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="2570e-124">Accounts are managed in Sales and synchronized to Finance and Operations as customers.</span></span> <span data-ttu-id="2570e-125">Die Eigenschaft **Is Externally Maintained** dieser Kunden wird auf **Ja** gesetzt, um die Kunden nachzuverfolgen, die aus Sales stammen.</span><span class="sxs-lookup"><span data-stu-id="2570e-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="2570e-126">Während der Rechnungsstellung werden diese Informationen verwendet, um Rechnungen zu filtern, die für Sales synchronisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="2570e-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="2570e-127">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="2570e-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="2570e-128">Das Feld **Kontonummer** steht auf der Seite **Konto** zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2570e-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="2570e-129">Es wurde zu einem natürlichen und eindeutigen Schlüssel für die Unterstützung der Integration gemacht.</span><span class="sxs-lookup"><span data-stu-id="2570e-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="2570e-130">Die natürliche Schlüsselfunktion der Customer Relationship Management (CRM)-Lösung wirkt sich möglicherweise auf Kunden aus, die das Feld **Kontonummer** bereits verwenden, aber keine eindeutigen **Kontonummer**-Werte pro Konto verwenden.</span><span class="sxs-lookup"><span data-stu-id="2570e-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="2570e-131">Derzeit unterstützt die Integrationslösung diesen Fall nicht.</span><span class="sxs-lookup"><span data-stu-id="2570e-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="2570e-132">Wenn ein neues Konto angelegt wird und noch kein **Kontonummer**-Wert vorhanden ist, wird es automatisch unter Verwendung einer fortlaufenden Nummerierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="2570e-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="2570e-133">Der Wert besteht aus **ACC**, gefolgt von einer aufsteigenden fortlaufenden Nummerierung und einem Suffix aus sechs Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2570e-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="2570e-134">Beispiel: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="2570e-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="2570e-135">Wenn die Integrationslösung für Sales angewendet wird, füllt ein Upgrade-Skript das Feld **Kontonummer** für in Sales vorhandene Konten aus.</span><span class="sxs-lookup"><span data-stu-id="2570e-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="2570e-136">Wenn es keine **Kontonummer**-Werte gibt, wird die zuvor beschriebene laufende Nummerierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2570e-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="2570e-137">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="2570e-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="2570e-138">Die **CustomerGroupId**-Zuordnung muss in Finance and Operations aktualisiert werden, um einen gültigen Wert zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="2570e-138">The **CustomerGroupId** mapping must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="2570e-139">Sie können einen Standardwert spezifizieren, oder den Wert unter Verwendung einer Wertezuordnung festlegen.</span><span class="sxs-lookup"><span data-stu-id="2570e-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="2570e-140">Der Standardvorlagenwert ist **10**.</span><span class="sxs-lookup"><span data-stu-id="2570e-140">The default template value is **10**.</span></span>

- <span data-ttu-id="2570e-141">Durch Hinzufügen der folgenden Zuordnungen können Sie die Anzahl der erforderlichen manuellen Updates in Finance and Operations reduzieren.</span><span class="sxs-lookup"><span data-stu-id="2570e-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="2570e-142">Sie können einen Standardwert oder eine Wertzuordnung beispielsweise aus **Land/Region** oder **Stadt** verwenden.</span><span class="sxs-lookup"><span data-stu-id="2570e-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="2570e-143">**SiteId** – Ein Standort ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2570e-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="2570e-144">Es kann ein Standardstandort vom Produkt oder vom Kunden aus dem Auftragskopf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2570e-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="2570e-145">Der Standardvorlagenwert ist **1**.</span><span class="sxs-lookup"><span data-stu-id="2570e-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="2570e-146">**WarehouseId** – Ein Lager ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen verarbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="2570e-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="2570e-147">Es kann ein Standardlager vom Produkt oder vom Kunden aus dem Auftragskopf in Finance and Operations verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2570e-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span>

        <span data-ttu-id="2570e-148">Der Standardvorlagenwert ist **13**.</span><span class="sxs-lookup"><span data-stu-id="2570e-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="2570e-149">**LanguageId** – Eine Sprache ist erforderlich, um in Finance and Operations Angebote und Vertriebsaufträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2570e-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="2570e-150">Standardmäßig wird die Sprache aus dem Auftragskopf des Kunden verwendet.</span><span class="sxs-lookup"><span data-stu-id="2570e-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="2570e-151">Der Standardvorlagewert lautet **en-us**.</span><span class="sxs-lookup"><span data-stu-id="2570e-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="2570e-152">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="2570e-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="2570e-153">Die Felder **Zahlungsbedingungen**, **Frachtbedingungen**, **Lieferbedingungen**, **Liefermethode** und **Bereitstellungsmodus** sind nicht in den Standardzuordnungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="2570e-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="2570e-154">Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2570e-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="2570e-155">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="2570e-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="2570e-156">Die Zuordnung zeigt, welche Feldinformationen von Sales zu Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2570e-156">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Vorlagenzuordnung in Datenintegration](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="2570e-158">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2570e-158">Related topics</span></span>


[<span data-ttu-id="2570e-159">Interessent zu Bargeld</span><span class="sxs-lookup"><span data-stu-id="2570e-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="2570e-160">Konten von Sales direkt mit Debitoren in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="2570e-160">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="2570e-161">Kontakte direkt von Sales mit Kontakten oder Debitoren in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="2570e-161">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="2570e-162">Auftragskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="2570e-162">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="2570e-163">Verkaufsrechnungskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="2570e-163">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)


