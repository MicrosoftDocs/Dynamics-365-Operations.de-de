---
title: Kontakte direkt von Sales mit Kontakten oder Debitoren in Supply Chain Management synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Entitäten „Kontakt (Kontakte)“ und „Kontakt (Debitoren)“ aus Dynamics 365 Sales mit Dynamics 365 Supply Chain Management zu synchronisieren.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 8cbc2909c3f4533b4ea68e522f0874873989f3ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994044"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a><span data-ttu-id="1c93d-103">Kontakte direkt von Sales mit Kontakten oder Debitoren in Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="1c93d-103">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="1c93d-104">Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Integration von Daten in Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="1c93d-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="1c93d-105">Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Tabellen „Kontakt (Kontakte)“ und „Kontakt (Debitoren)“ direkt aus Dynamics 365 Sales mit Dynamics 365 Supply Chain Management zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="1c93d-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) tables directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="1c93d-106">Datenfluss in Interessent nach Bargeld</span><span class="sxs-lookup"><span data-stu-id="1c93d-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="1c93d-107">Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Supply Chain Management und Sales hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="1c93d-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="1c93d-108">Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Supply Chain Management und Sales.</span><span class="sxs-lookup"><span data-stu-id="1c93d-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="1c93d-109">Die folgende Abbildung zeigt, wie Daten zwischen Supply Chain Management und Sales synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1c93d-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="1c93d-110">[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="1c93d-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1c93d-111">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="1c93d-111">Templates and tasks</span></span>

<span data-ttu-id="1c93d-112">Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [PowerApps-Administrator-Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="1c93d-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="1c93d-113">Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1c93d-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="1c93d-114">Die folgenden Vorlagen und grundlegenden Aufgaben werden für die Synchronisierung der Tabellen Kontakt (Kontakte) aus Sales mit den Tabellen Kontakt (Kunden) in Supply Chain Management verwendet:</span><span class="sxs-lookup"><span data-stu-id="1c93d-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) tables in Sales to Contact (Customers) tables in Supply Chain Management.</span></span>

- <span data-ttu-id="1c93d-115">**Namen der Vorlagen in der Datenintegration**</span><span class="sxs-lookup"><span data-stu-id="1c93d-115">**Names of the templates in Data integration**</span></span>

    - <span data-ttu-id="1c93d-116">Kontakte (Sales zu Supply Chain Management) – Direkt</span><span class="sxs-lookup"><span data-stu-id="1c93d-116">Contacts (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="1c93d-117">Kontakte zu Kunden (Sales zu Supply Chain Management) – Direkt</span><span class="sxs-lookup"><span data-stu-id="1c93d-117">Contacts to Customer (Sales to Supply Chain Management) - Direct</span></span>

- <span data-ttu-id="1c93d-118">**Namen der Aufgaben im Datenintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="1c93d-118">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="1c93d-119">Kontakte</span><span class="sxs-lookup"><span data-stu-id="1c93d-119">Contacts</span></span>
    - <span data-ttu-id="1c93d-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="1c93d-120">ContactToCustomer</span></span>

<span data-ttu-id="1c93d-121">Vor der Kontaktsynchronisierung kann die folgende Kontaktsynchronisierung auftreten: Konten (Sales in Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="1c93d-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Supply Chain Management)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="1c93d-122">Entitätssätze</span><span class="sxs-lookup"><span data-stu-id="1c93d-122">Entity sets</span></span>

| <span data-ttu-id="1c93d-123">Verk.</span><span class="sxs-lookup"><span data-stu-id="1c93d-123">Sales</span></span>    | <span data-ttu-id="1c93d-124">Lieferkettenverwaltung</span><span class="sxs-lookup"><span data-stu-id="1c93d-124">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="1c93d-125">Kontakte</span><span class="sxs-lookup"><span data-stu-id="1c93d-125">Contacts</span></span> | <span data-ttu-id="1c93d-126">Dataverse-Kontakte</span><span class="sxs-lookup"><span data-stu-id="1c93d-126">Dataverse Contacts</span></span>           |
| <span data-ttu-id="1c93d-127">Kontakte</span><span class="sxs-lookup"><span data-stu-id="1c93d-127">Contacts</span></span> | <span data-ttu-id="1c93d-128">Debitoren V2</span><span class="sxs-lookup"><span data-stu-id="1c93d-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="1c93d-129">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="1c93d-129">Entity flow</span></span>

<span data-ttu-id="1c93d-130">Kontakte werden in Sales verwaltet und mit Supply Chain Management synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="1c93d-130">Contacts are managed in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="1c93d-131">Ein Kontakt in Sales kann zu einem Kontakt oder Kunden in Supply Chain Management werden.</span><span class="sxs-lookup"><span data-stu-id="1c93d-131">A contact in Sales can become either a contact or a customer in Supply Chain Management.</span></span> <span data-ttu-id="1c93d-132">Um festzustellen, ob ein Kontakt in Sales mit Supply Chain Management als Kontakt oder Debitor synchronisiert werden soll, berücksichtigt das System die folgenden Eigenschaften für den Kontakt in Sales:</span><span class="sxs-lookup"><span data-stu-id="1c93d-132">To determine whether a contact in Sales should be synchronized to Supply Chain Management as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="1c93d-133">**Synchronisierung mit einem Kunden in Supply Chain Management:** Kontakte, wobei **Ist aktiver Kunde** auf **Ja** gesetzt ist</span><span class="sxs-lookup"><span data-stu-id="1c93d-133">**Synchronization to a customer in Supply Chain Management:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="1c93d-134">**Synchronisierung mit einem Kontakt in Supply Chain Management:** Kontakte, wobei **Ist aktiver Kunde** auf **Nein** gesetzt ist und **Unternehmen** (Übergeordnetes Konto/übergeordneter Kontakt) auf ein Konto (nicht auf einen Kontakt) verweist</span><span class="sxs-lookup"><span data-stu-id="1c93d-134">**Synchronization to a contact in Supply Chain Management:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="1c93d-135">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="1c93d-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="1c93d-136">Dem Kontakt wurde eine neue Spalte **Ist aktiver Kunde** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1c93d-136">A new **Is Active Customer** column has been added to the contact.</span></span> <span data-ttu-id="1c93d-137">Die Spalte wird genutzt, um Kontakte mit Vertriebsaktivität von Kontakten ohne Vertriebsaktivität zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="1c93d-137">This column is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="1c93d-138">**Ist aktiver Kunde** wird nur für Kontakte auf **Ja** gesetzt, für die es Angebote, Bestellungen oder Rechnungen gibt.</span><span class="sxs-lookup"><span data-stu-id="1c93d-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="1c93d-139">Nur diese Kontakte werden in Supply Chain Management als Kunden synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="1c93d-139">Only those contacts are synchronized to Supply Chain Management as customers.</span></span>

<span data-ttu-id="1c93d-140">Dem Kontakt wurde eine neue Spalte **IsCompanyAnAccount** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1c93d-140">A new **IsCompanyAnAccount** column has been added to the contact.</span></span> <span data-ttu-id="1c93d-141">Diese Spalte wird verwendet, um anzuzeigen, ob ein Kontakt mit einem Unternehmen (übergeordnetes Konto/übergeordneter Kontakt) des **Konto**-Typs verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="1c93d-141">This column indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="1c93d-142">Diese Information wird verwendet, um Kontakte zu identifizieren, die mit Supply Chain Management als Kontakte synchronisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1c93d-142">This information is used to identify contacts that should be synchronized to Supply Chain Management as contacts.</span></span>

<span data-ttu-id="1c93d-143">Dem Kontakt wurde eine neue Spalte **Kontaktnummer** hinzugefügt, um sicherzustellen, dass ein natürlicher und eindeutiger Schlüssel für die Integration bereitsteht.</span><span class="sxs-lookup"><span data-stu-id="1c93d-143">A new **Contact Number** column has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="1c93d-144">Wenn ein neuer Kontakt angelegt wird, wird automatisch ein **Kontaktnummer**-Wert unter Verwendung einer fortlaufenden Nummerierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="1c93d-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="1c93d-145">Der Wert besteht aus **CON**, gefolgt von einer aufsteigenden fortlaufenden Nummerierung und einem Suffix aus sechs Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1c93d-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="1c93d-146">Beispiel: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="1c93d-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="1c93d-147">Wenn Sales die Integrationslösung für Sales angewendet wird, füllt ein Upgrade-Skript die Spalte **Kontaktnummer** für vorhandene Kontakte unter Verwendung der oben genannten fortlaufenden Nummerierung aus.</span><span class="sxs-lookup"><span data-stu-id="1c93d-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** column for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="1c93d-148">Außerdem setzt das Upgrade-Skript die Spalte **Ist aktiver Kunde** für alle Kontakte mit Vertriebsaktivität auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1c93d-148">The upgrade script also sets the **Is Active Customer** column to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-supply-chain-management"></a><span data-ttu-id="1c93d-149">In Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1c93d-149">In Supply Chain Management</span></span>

<span data-ttu-id="1c93d-150">Kontakte werden mit der Eigenschaft **IsContactPersonExternallyMaintained** gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="1c93d-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="1c93d-151">Diese Eigenschaft zeigt an, das ein Kontakt extern verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="1c93d-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="1c93d-152">In diesem Fall werden extern verwaltete Kontakte in Sales verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1c93d-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="1c93d-153">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="1c93d-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="1c93d-154">Kontakt zu Kunde</span><span class="sxs-lookup"><span data-stu-id="1c93d-154">Contact to customer</span></span>

- <span data-ttu-id="1c93d-155">**CustomerGroup** ist in Supply Chain Management erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1c93d-155">**CustomerGroup** is required in Supply Chain Management.</span></span> <span data-ttu-id="1c93d-156">Um Synchronisierungsfehler zu vermeiden, können Sie in der Zuordnung einen Standardwert vorgeben.</span><span class="sxs-lookup"><span data-stu-id="1c93d-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="1c93d-157">Der Standardwert wird verwendet, wenn die Spalte in Sales leer geblieben ist.</span><span class="sxs-lookup"><span data-stu-id="1c93d-157">That default value is then used if the column is left blank in Sales.</span></span>

    <span data-ttu-id="1c93d-158">Der Standardvorlagenwert ist **10**.</span><span class="sxs-lookup"><span data-stu-id="1c93d-158">The default template value is **10**.</span></span>

- <span data-ttu-id="1c93d-159">Durch Hinzufügen der folgenden Zuordnungen können Sie die Anzahl der erforderlichen manuellen Updates in Supply Chain Management reduzieren.</span><span class="sxs-lookup"><span data-stu-id="1c93d-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="1c93d-160">Sie können einen Standardwert oder eine Wertzuordnung beispielsweise aus **Land/Region** oder **Stadt** verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c93d-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="1c93d-161">**SiteId** – Für Produkte in Supply Chain Management kann auch ein Standardstandort definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1c93d-161">**SiteId** – A default site can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="1c93d-162">Ein Standort ist erforderlich, um in Supply Chain Management Angebote und Aufträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c93d-162">A site is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="1c93d-163">Für **SiteId** ist kein Vorlagenwert definiert.</span><span class="sxs-lookup"><span data-stu-id="1c93d-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="1c93d-164">**WarehouseId** – Für Produkte in Supply Chain Management kann auch ein Standardlagerort definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1c93d-164">**WarehouseId** – A default warehouse can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="1c93d-165">Ein Lagerort ist erforderlich, um in Supply Chain Management Angebote und Aufträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c93d-165">A warehouse is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="1c93d-166">Für **WarehouseId** ist kein Vorlagenwert definiert.</span><span class="sxs-lookup"><span data-stu-id="1c93d-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="1c93d-167">**LanguageId** – Eine Sprache ist erforderlich, um in Supply Chain Management Angebote und Aufträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c93d-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>
    
        <span data-ttu-id="1c93d-168">Der Standardvorlagewert lautet **en-us**.</span><span class="sxs-lookup"><span data-stu-id="1c93d-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1c93d-169">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="1c93d-169">Template mapping in Data integration</span></span>

<span data-ttu-id="1c93d-170">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="1c93d-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="1c93d-171">Die Zuordnung zeigt, welche Spalteninformationen von Sales zu Supply Chain Management synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1c93d-171">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="1c93d-172">Kontakt zu Kontakt</span><span class="sxs-lookup"><span data-stu-id="1c93d-172">Contact to contact</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="1c93d-174">Kontakt zu Kunde</span><span class="sxs-lookup"><span data-stu-id="1c93d-174">Contact to customer</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="1c93d-176">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1c93d-176">Related topics</span></span>

[<span data-ttu-id="1c93d-177">Prospect-to-Cash</span><span class="sxs-lookup"><span data-stu-id="1c93d-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="1c93d-178">Konten direkt von Sales mit Konten in Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="1c93d-178">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="1c93d-179">Produkte direkt von Supply Chain Management mit Produkten in Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="1c93d-179">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="1c93d-180">Synchronisieren von Aufträgen direkt zwischen Sales und Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1c93d-180">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="1c93d-181">Rechnungskopfzeilen und ‑positionen direkt von Supply Chain Management zu Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="1c93d-181">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)


