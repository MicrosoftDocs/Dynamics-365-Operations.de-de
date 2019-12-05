---
title: Konten direkt von Sales mit Konten in Supply Chain Management synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgaben, die verwendet werden, um die Konten aus Dynamics 365 Sales mit Supply Chain Management zu synchronisieren.
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
ms.openlocfilehash: ebca416e94f44d0448a4f4d0be08f13e30e749e9
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813223"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="b7baf-103">Konten direkt von Sales mit Konten in Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="b7baf-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b7baf-104">Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Integration von Daten in Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="b7baf-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="b7baf-105">Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgaben, die verwendet werden, um Konten direkt aus Dynamics 365 Sales mit Dynamics 365 Supply Chain Management zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b7baf-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="b7baf-106">Datenfluss in Interessent nach Bargeld</span><span class="sxs-lookup"><span data-stu-id="b7baf-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="b7baf-107">Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Supply Chain Management und Sales hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b7baf-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="b7baf-108">Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Supply Chain Management und Sales.</span><span class="sxs-lookup"><span data-stu-id="b7baf-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="b7baf-109">Die folgende Abbildung zeigt, wie Daten zwischen Supply Chain Management und Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b7baf-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="b7baf-110">[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="b7baf-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b7baf-111">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="b7baf-111">Templates and tasks</span></span>

<span data-ttu-id="b7baf-112">Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [Power Apps-Administrator-Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="b7baf-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="b7baf-113">Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b7baf-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b7baf-114">Die folgende Vorlage und grundlegende Aufgabe werden für die Synchronisierung von Konten aus Sales in Supply Chain Management verwendet:</span><span class="sxs-lookup"><span data-stu-id="b7baf-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="b7baf-115">**Name der Vorlage in der Datenintegration:** Konten (Sales zu Finance and Operations) - direkt</span><span class="sxs-lookup"><span data-stu-id="b7baf-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="b7baf-116">**Name der Aufgabe im Projekt:** Konten – Kunden</span><span class="sxs-lookup"><span data-stu-id="b7baf-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="b7baf-117">Keine Synchronisierungsaufgaben sind erforderlich, damit Konto-Kunde-Synchronisierung auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="b7baf-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="b7baf-118">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="b7baf-118">Entity set</span></span>

| <span data-ttu-id="b7baf-119">Verk.</span><span class="sxs-lookup"><span data-stu-id="b7baf-119">Sales</span></span>    | <span data-ttu-id="b7baf-120">Lieferkettenverwaltung</span><span class="sxs-lookup"><span data-stu-id="b7baf-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="b7baf-121">Konten</span><span class="sxs-lookup"><span data-stu-id="b7baf-121">Accounts</span></span> | <span data-ttu-id="b7baf-122">Debitoren V2</span><span class="sxs-lookup"><span data-stu-id="b7baf-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="b7baf-123">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="b7baf-123">Entity flow</span></span>

<span data-ttu-id="b7baf-124">Konten werden in Sales verwaltet und mit Supply Chain Management als Kunden synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="b7baf-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="b7baf-125">Die Eigenschaft **Is Externally Maintained** dieser Kunden wird auf **Ja** gesetzt, um die Kunden nachzuverfolgen, die aus Sales stammen.</span><span class="sxs-lookup"><span data-stu-id="b7baf-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="b7baf-126">Während der Rechnungsstellung werden diese Informationen verwendet, um Rechnungen zu filtern, die für Sales synchronisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="b7baf-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b7baf-127">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="b7baf-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="b7baf-128">Das Feld **Kontonummer** steht auf der Seite **Konto** zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b7baf-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="b7baf-129">Es wurde zu einem natürlichen und eindeutigen Schlüssel für die Unterstützung der Integration gemacht.</span><span class="sxs-lookup"><span data-stu-id="b7baf-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="b7baf-130">Die natürliche Schlüsselfunktion der Customer Relationship Management (CRM)-Lösung wirkt sich möglicherweise auf Kunden aus, die das Feld **Kontonummer** bereits verwenden, aber keine eindeutigen **Kontonummer**-Werte pro Konto verwenden.</span><span class="sxs-lookup"><span data-stu-id="b7baf-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="b7baf-131">Derzeit unterstützt die Integrationslösung diesen Fall nicht.</span><span class="sxs-lookup"><span data-stu-id="b7baf-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="b7baf-132">Wenn ein neues Konto angelegt wird und noch kein **Kontonummer**-Wert vorhanden ist, wird es automatisch unter Verwendung einer fortlaufenden Nummerierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b7baf-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="b7baf-133">Der Wert besteht aus **ACC**, gefolgt von einer aufsteigenden fortlaufenden Nummerierung und einem Suffix aus sechs Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b7baf-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="b7baf-134">Beispiel: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="b7baf-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="b7baf-135">Wenn die Integrationslösung für Sales angewendet wird, füllt ein Upgrade-Skript das Feld **Kontonummer** für in Sales vorhandene Konten aus.</span><span class="sxs-lookup"><span data-stu-id="b7baf-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="b7baf-136">Wenn es keine **Kontonummer**-Werte gibt, wird die zuvor beschriebene laufende Nummerierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7baf-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b7baf-137">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="b7baf-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="b7baf-138">Die **CustomerGroupId**-Zuordnung muss in Supply Chain Management aktualisiert werden, um einen gültigen Wert zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="b7baf-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="b7baf-139">Sie können einen Standardwert spezifizieren, oder den Wert unter Verwendung einer Wertezuordnung festlegen.</span><span class="sxs-lookup"><span data-stu-id="b7baf-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="b7baf-140">Der Standardvorlagenwert ist **10**.</span><span class="sxs-lookup"><span data-stu-id="b7baf-140">The default template value is **10**.</span></span>

- <span data-ttu-id="b7baf-141">Durch Hinzufügen der folgenden Zuordnungen können Sie die Anzahl der erforderlichen manuellen Updates in Supply Chain Management reduzieren.</span><span class="sxs-lookup"><span data-stu-id="b7baf-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="b7baf-142">Sie können einen Standardwert oder eine Wertzuordnung beispielsweise aus **Land/Region** oder **Stadt** verwenden.</span><span class="sxs-lookup"><span data-stu-id="b7baf-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="b7baf-143">**SiteId** – Ein Standort ist erforderlich, um in Supply Chain Management Angebots- und Vertriebsauftragspositionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b7baf-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="b7baf-144">Es kann ein Standardstandort vom Produkt oder vom Kunden aus dem Auftragskopf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7baf-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="b7baf-145">Der Standardvorlagenwert ist **1**.</span><span class="sxs-lookup"><span data-stu-id="b7baf-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="b7baf-146">**WarehouseId** – Ein Lager ist erforderlich, um in Supply Chain Management Angebots- und Vertriebsauftragspositionen verarbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="b7baf-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="b7baf-147">Es kann ein Standardlager vom Produkt oder vom Kunden aus dem Auftragskopf in Supply Chain Management verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7baf-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="b7baf-148">Der Standardvorlagenwert ist **13**.</span><span class="sxs-lookup"><span data-stu-id="b7baf-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="b7baf-149">**LanguageId** – Eine Sprache ist erforderlich, um in Supply Chain Management Angebote und Aufträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b7baf-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="b7baf-150">Standardmäßig wird die Sprache aus dem Auftragskopf des Kunden verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7baf-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="b7baf-151">Der Standardvorlagewert lautet **en-us**.</span><span class="sxs-lookup"><span data-stu-id="b7baf-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b7baf-152">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="b7baf-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="b7baf-153">Die Felder **Zahlungsbedingungen**, **Frachtbedingungen**, **Lieferbedingungen**, **Liefermethode** und **Bereitstellungsmodus** sind nicht in den Standardzuordnungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b7baf-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="b7baf-154">Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b7baf-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="b7baf-155">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="b7baf-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="b7baf-156">Die Zuordnung zeigt, welche Feldinformationen von Sales zu Supply Chain Management synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b7baf-156">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Vorlagenzuordnung in Datenintegration](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="b7baf-158">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b7baf-158">Related topics</span></span>


[<span data-ttu-id="b7baf-159">Prospect-to-Cash</span><span class="sxs-lookup"><span data-stu-id="b7baf-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="b7baf-160">Konten direkt von Sales mit Konten in Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="b7baf-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="b7baf-161">Kontakte direkt von Sales mit Kontakten oder Debitoren in Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="b7baf-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="b7baf-162">Synchronisieren von Aufträgen direkt zwischen Sales und Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b7baf-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="b7baf-163">Rechnungskopfzeilen und ‑positionen direkt von Supply Chain Management zu Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="b7baf-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

