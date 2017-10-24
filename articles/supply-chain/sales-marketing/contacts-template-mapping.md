---
title: "Synchronisierung von Kontakten aus Sales für Kontakte oder Kunden in Finance and Operations"
description: "Dieses Thema beschreibt die Vorlagen und die grundlegenden Aufgaben, die verwendet werden, um Kontakt (Kontakte) und Kontakt (Kunden) aus Microsoft Dynamics 365 for Sales für Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, zu synchronisieren."
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
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 41e27776b94df059ada13efb9a3dbf6a29d67f36
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="c33aa-103">Synchronisierung von Kontakten aus Sales für Kontakte oder Kunden in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c33aa-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="c33aa-104">Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration) vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="c33aa-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="c33aa-105">Dieses Thema beschreibt die Vorlagen und die grundlegenden Aufgaben, die verwendet werden, um Kontakt-Entitäten (Kontakte) und Kontakt (Kunden) aus Microsoft Dynamics 365 for Sales (Sales) für Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations), zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="c33aa-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c33aa-106">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="c33aa-106">Templates and tasks</span></span>

<span data-ttu-id="c33aa-107">Die folgenden Vorlagen und grundlegenden Aufgaben werden für die Synchronisierung von Kontakt (Kontakte) aus Sales für Kontakt (Kunden) in Finance and Operations verwendet:</span><span class="sxs-lookup"><span data-stu-id="c33aa-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="c33aa-108">**Namen der Vorlagen:**</span><span class="sxs-lookup"><span data-stu-id="c33aa-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="c33aa-109">Kontakte (Finance and Operations nach Sales)</span><span class="sxs-lookup"><span data-stu-id="c33aa-109">Contacts (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="c33aa-110">Kontakte in Kunde (Sales in Fin und Ops)</span><span class="sxs-lookup"><span data-stu-id="c33aa-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="c33aa-111">**Namen der Aufgaben im Projekt:**</span><span class="sxs-lookup"><span data-stu-id="c33aa-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="c33aa-112">Kontakte</span><span class="sxs-lookup"><span data-stu-id="c33aa-112">Contacts</span></span>
    - <span data-ttu-id="c33aa-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="c33aa-113">ContactToCustomer</span></span>

<span data-ttu-id="c33aa-114">Vor der Kontaktsynchronisierung muss die folgende Synchronisierungsaufgabe ausgeführt werden: Konten (Sales in Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="c33aa-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="c33aa-115">Entitätssätze</span><span class="sxs-lookup"><span data-stu-id="c33aa-115">Entity sets</span></span>

| <span data-ttu-id="c33aa-116">Vertrieb</span><span class="sxs-lookup"><span data-stu-id="c33aa-116">Sales</span></span>    | <span data-ttu-id="c33aa-117">CDS</span><span class="sxs-lookup"><span data-stu-id="c33aa-117">CDS</span></span>     | <span data-ttu-id="c33aa-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c33aa-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="c33aa-119">Kontakte</span><span class="sxs-lookup"><span data-stu-id="c33aa-119">Contacts</span></span> | <span data-ttu-id="c33aa-120">Kontakt</span><span class="sxs-lookup"><span data-stu-id="c33aa-120">Contact</span></span> | <span data-ttu-id="c33aa-121">CDS-Kontakte</span><span class="sxs-lookup"><span data-stu-id="c33aa-121">CDS Contacts</span></span>           |
| <span data-ttu-id="c33aa-122">Kontakte</span><span class="sxs-lookup"><span data-stu-id="c33aa-122">Contacts</span></span> | <span data-ttu-id="c33aa-123">Konto</span><span class="sxs-lookup"><span data-stu-id="c33aa-123">Account</span></span> | <span data-ttu-id="c33aa-124">Debitoren V2</span><span class="sxs-lookup"><span data-stu-id="c33aa-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="c33aa-125">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="c33aa-125">Entity flow</span></span>

<span data-ttu-id="c33aa-126">Kontakte werden in Sales verwaltet und in Common Data Services (CDS) Finance and Operations synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="c33aa-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="c33aa-127">Ein Kontakt in Sales kann zu einem Kontakt in CDS und Finance and Operations werden.</span><span class="sxs-lookup"><span data-stu-id="c33aa-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="c33aa-128">Alternativ kann er zu einem Kontakt in CDS und einem Kunden in Finance and Operations werden.</span><span class="sxs-lookup"><span data-stu-id="c33aa-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="c33aa-129">Um festzustellen, ob ein Kontakt aus Sales für die Synchronisierung in CDS und Finance and Operations ausgewählt werden soll (z. B. Kontakte in Sales &gt; Kontakt in CDS &gt; Kontakte in Finance and Operations), überprüft das System die folgenden Eigenschaften von Kontakt in Sales:</span><span class="sxs-lookup"><span data-stu-id="c33aa-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="c33aa-130">**Synchronisierung auf Konto in CDS und Kunde in Finance and Operations:** Kontakte, wenn **Ist aktiver Kunde** auf **Ja** gesetzt ist</span><span class="sxs-lookup"><span data-stu-id="c33aa-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="c33aa-131">**Synchronisierung auf Kontakt in CDS und Kontakt in Finance and Operations:** Kontakte, wenn **Ist aktiver Kunde** auf **Nein** gesetzt ist und **Unternehmen** (Übergeordnetes Konto/übergeordneter Kontakt) auf ein Konto (nicht auf einen Kontakt) verweist</span><span class="sxs-lookup"><span data-stu-id="c33aa-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c33aa-132">Prospect to Cash-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="c33aa-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="c33aa-133">Dem Kontakt wurde ein neues **Ist aktiver Kunde**-Feld hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c33aa-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="c33aa-134">Das Feld wird genutzt, um Kontakte mit Vertriebsaktivität von Kontakten ohne Vertriebsaktivität zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="c33aa-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="c33aa-135">**Ist aktiver Kunde** wird nur für Kontakte auf **Ja** gesetzt, für die es Angebote, Bestellungen oder Rechnungen gibt.</span><span class="sxs-lookup"><span data-stu-id="c33aa-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="c33aa-136">Nur diese Kontakte werden in Finance and Operations als Kunden synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="c33aa-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="c33aa-137">Dem Kontakt wurde ein neues **IsCompanyAnAccount**-Feld hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c33aa-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="c33aa-138">Dieses Feld wird verwendet, um anzuzeigen, ob ein Kontakt mit einem Unternehmen (übergeordnetes Konto/übergeordneter Kontakt) des **Konto**-Typs verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="c33aa-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="c33aa-139">Diese Information wird verwendet, um Kontakte zu identifizieren, mit für Finance and Operations als Kontakte synchronisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c33aa-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="c33aa-140">Dem Kontakt wurde ein neues **Kontaktnummer**-Feld hinzugefügt, um sicherzustellen, dass ein natürlicher und eindeutiger Schlüssel für die Integration bereitsteht.</span><span class="sxs-lookup"><span data-stu-id="c33aa-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="c33aa-141">Wenn ein neuer Kontakt angelegt wird, wird automatisch ein **Kontaktnummer**-Wert unter Verwendung einer fortlaufenden Nummerierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="c33aa-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="c33aa-142">Der Wert besteht aus **CON**, gefolgt von einer aufsteigenden fortlaufenden Nummerierung und einem Suffix aus sechs Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c33aa-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="c33aa-143">Beispiel: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="c33aa-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="c33aa-144">Wenn Sales die Integrationslösung für Sales hinzugefügt wird, füllt ein Upgrade-Skript das Feld **Kontaktnummer** für vorhandene Kontakte unter Verwendung der oben genannten fortlaufenden Nummerierung aus.</span><span class="sxs-lookup"><span data-stu-id="c33aa-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="c33aa-145">Außerdem setzt das Upgrade-Skript das Feld **Ist aktiver Kunde** für alle Kontakte mit Vertriebsaktivität auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c33aa-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="c33aa-146">In Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c33aa-146">In Finance and Operations</span></span> 

<span data-ttu-id="c33aa-147">Kontakte werden mit der Eigenschaft **IsContactPersonExternallyMaintained** gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="c33aa-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="c33aa-148">Diese Eigenschaft zeigt an, das ein Kontakt extern verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="c33aa-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="c33aa-149">In diesem Fall werden extern verwaltete Kontakte in Sales verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c33aa-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="c33aa-150">Voraussetzungen und Einrichtung der Zuordnung</span><span class="sxs-lookup"><span data-stu-id="c33aa-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="c33aa-151">Kontakt zu Kontakt</span><span class="sxs-lookup"><span data-stu-id="c33aa-151">Contact to Contact</span></span>

- <span data-ttu-id="c33aa-152">Aktualisieren Sie die **CDS-Organisations-ID** in der **Quell &gt; CDS**-Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="c33aa-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="c33aa-153">Der Standardvorlagewert für **Organization_OrganizationId [Organisations-ID]** lautet **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="c33aa-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="c33aa-154">Der Standardvorlagewert für **PrimaryAccount_Organization_OrganizationId [Organisations-ID]** lautet **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="c33aa-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="c33aa-155">In Finance and Operations ist ein **Address/Länder/Region-Code** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c33aa-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="c33aa-156">Um Synchronisierungsfehler zu vermeiden, können Sie in der **CDS &gt; Operations**-Zuordnung einen Standardwert vorgeben.</span><span class="sxs-lookup"><span data-stu-id="c33aa-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="c33aa-157">Der Standardwert wird verwendet, wenn das Feld in Sales leer geblieben ist.</span><span class="sxs-lookup"><span data-stu-id="c33aa-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="c33aa-158">Der Standardvorlagewert für **PrimaryAddressCountryRegionISOCode** lautet **USA**.</span><span class="sxs-lookup"><span data-stu-id="c33aa-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="c33aa-159">Stellen Sie sicher, dass in Finance and Operations ein Wert für die folgenden Felder vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c33aa-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="c33aa-160">In Finance and Operations ist die Information nicht erforderlich, Sie können die Zuordnung aus der **CDS &gt; Ziel**-Zuordnung entfernen.</span><span class="sxs-lookup"><span data-stu-id="c33aa-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="c33aa-161">**Feldname in Finance and Operations:** Entscheidung</span><span class="sxs-lookup"><span data-stu-id="c33aa-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="c33aa-162">**Zuordnung:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="c33aa-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="c33aa-163">Kontakt zu Kunde</span><span class="sxs-lookup"><span data-stu-id="c33aa-163">Contact to Customer</span></span>

- <span data-ttu-id="c33aa-164">Aktualisieren Sie die **CDS-Organisations-ID** in der **Quell &gt; CDS**-Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="c33aa-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="c33aa-165">Der Standardvorlagewert für **Organization_OrganizationId [Organisations-ID]** lautet **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="c33aa-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="c33aa-166">In Finance and Operations ist ein **Address/Länder/Region-Code** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c33aa-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="c33aa-167">Um Synchronisierungsfehler zu vermeiden, können Sie in der **CDS &gt; Ziel**-Zuordnung einen Standardwert vorgeben.</span><span class="sxs-lookup"><span data-stu-id="c33aa-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="c33aa-168">Der Standardwert wird verwendet, wenn das Feld in Sales leer geblieben ist.</span><span class="sxs-lookup"><span data-stu-id="c33aa-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="c33aa-169">Der Standardvorlagewert für **PrimaryAddressCountryRegionISOCode** lautet **USA**.</span><span class="sxs-lookup"><span data-stu-id="c33aa-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="c33aa-170">**CustomerGroup** ist in Finance and Operations erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c33aa-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="c33aa-171">Um Synchronisierungsfehler zu vermeiden, können Sie in der **CDS &gt; Ziel**-Zuordnung einen Standardwert vorgeben.</span><span class="sxs-lookup"><span data-stu-id="c33aa-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="c33aa-172">Der Standardwert wird verwendet, wenn das Feld in Sales leer geblieben ist.</span><span class="sxs-lookup"><span data-stu-id="c33aa-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="c33aa-173">Der Standardvorlagewert für **CustomerGroupId** lautet **10**.</span><span class="sxs-lookup"><span data-stu-id="c33aa-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="c33aa-174">Durch Hinzufügen der folgenden Zuordnungen von **CDS &gt; Ziel** können Sie die Anzahl der manuellen Updates in Finance and Operations reduzieren.</span><span class="sxs-lookup"><span data-stu-id="c33aa-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="c33aa-175">Sie können einen Standardwert oder eine Wertzuordnung beispielsweise aus **Land/Region** oder **Stadt** verwenden.</span><span class="sxs-lookup"><span data-stu-id="c33aa-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="c33aa-176">**SiteId** – Für Produkte in Finance and Operations kann auch eine Standardstandort definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c33aa-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="c33aa-177">Ein Standort ist erforderlich, um in Finance and Operations Angebote und Vertriebsaufträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c33aa-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="c33aa-178">Für **SiteId** ist kein Vorlagenwert definiert.</span><span class="sxs-lookup"><span data-stu-id="c33aa-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="c33aa-179">**WarehouseId** – Für Produkte in Finance and Operations kann auch ein Standardlager definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c33aa-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="c33aa-180">Ein Lager ist erforderlich, um in Finance and Operations Angebote und Vertriebsaufträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c33aa-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="c33aa-181">Für **WarehouseId** ist kein Vorlagenwert definiert.</span><span class="sxs-lookup"><span data-stu-id="c33aa-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="c33aa-182">**LanguageId** – Eine Sprache ist erforderlich, um in Finance and Operations Angebote und Vertriebsaufträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c33aa-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="c33aa-183">Der Standardvorlagewert für **LanguageId** lautet **en-us**.</span><span class="sxs-lookup"><span data-stu-id="c33aa-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="c33aa-184">Vorlagenzuordnung im Datenintegrator</span><span class="sxs-lookup"><span data-stu-id="c33aa-184">Template mapping in data integrator</span></span>

<span data-ttu-id="c33aa-185">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="c33aa-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="c33aa-186">Kontakt zu Kontakt</span><span class="sxs-lookup"><span data-stu-id="c33aa-186">Contact to Contact</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/contacts-template-mapping-data-integrator-1.png)

![Vorlagenzuordnung für Kontakte im Datenintegrator](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="c33aa-189">Kontakt zu Kunde</span><span class="sxs-lookup"><span data-stu-id="c33aa-189">Contact to Customer</span></span>

![Vorlagenzuordnung im Datenintegrator](./media/contacts-template-mapping-data-integrator-3.png)

![Vorlagenzuordnung für Kontakte im Datenintegrator](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="c33aa-192">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c33aa-192">Related topics</span></span>

[<span data-ttu-id="c33aa-193">Synchronisierung von Produkten aus Finance and Operations für Produkte in Sales</span><span class="sxs-lookup"><span data-stu-id="c33aa-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="c33aa-194">Synchronisierung von Konten aus Sales für Kunden in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c33aa-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="c33aa-195">Verkaufsangebotskopfzeilen und -positionen von Sales mit Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="c33aa-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="c33aa-196">Auftragskopfzeilen und -positionen von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="c33aa-196">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="c33aa-197">Verkaufsrechnungszeilen und -positionen von Finance and Operations mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="c33aa-197">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)

