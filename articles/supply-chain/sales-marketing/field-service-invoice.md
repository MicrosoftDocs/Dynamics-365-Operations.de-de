---
title: Vereinbarungsrechnungen in Field Service mit Freitextrechnungen in Supply Chain Management synchronisieren
description: Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Vereinbarungsrechnungen in Dynamics 365  Field Service mit Freitextrechnungen in Dynamics 365 Supply Chain Management zu synchronisieren.
author: ChristianRytt
ms.date: 04/10/2018
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
ms.openlocfilehash: f3066741781bd9058e09d7f577a35df4c9b453d4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819207"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="abac8-103">Vereinbarungsrechnungen in Field Service mit Freitextrechnungen in Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="abac8-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="abac8-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Vereinbarungsrechnungen in Dynamics 365 Field Service mit Freitextrechnungen in Dynamics 365 Supply Chain Management zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="abac8-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="abac8-105">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="abac8-105">Templates and tasks</span></span>

<span data-ttu-id="abac8-106">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um die Synchronisierung von Vereinbarungsrechnungen aus Field Service mit Freitextrechnungen in Supply Chain Management auszuführen.</span><span class="sxs-lookup"><span data-stu-id="abac8-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="abac8-107">**Name der Vorlage in der Datenintegration**</span><span class="sxs-lookup"><span data-stu-id="abac8-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="abac8-108">Vereinbarungsrechnungen (Field Service an Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="abac8-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="abac8-109">**Namen der Aufgaben im Datenintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="abac8-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="abac8-110">Rechnungsköpfe</span><span class="sxs-lookup"><span data-stu-id="abac8-110">Invoice headers</span></span>
- <span data-ttu-id="abac8-111">Rechnungspositionen</span><span class="sxs-lookup"><span data-stu-id="abac8-111">Invoice lines</span></span>

<span data-ttu-id="abac8-112">Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von Vereinbarungsrechnungen erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="abac8-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="abac8-113">Konten (Sales zu Supply Chain Management) – Direkt</span><span class="sxs-lookup"><span data-stu-id="abac8-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="abac8-114">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="abac8-114">Entity set</span></span>

| <span data-ttu-id="abac8-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="abac8-115">Field Service</span></span>  | <span data-ttu-id="abac8-116">Lieferkettenverwaltung</span><span class="sxs-lookup"><span data-stu-id="abac8-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="abac8-117">Rechnungen</span><span class="sxs-lookup"><span data-stu-id="abac8-117">invoices</span></span>       | <span data-ttu-id="abac8-118">Debitoren-Freitextrechnungskopfzeilen in Dataverse</span><span class="sxs-lookup"><span data-stu-id="abac8-118">Dataverse customer free text invoice headers</span></span> |
| <span data-ttu-id="abac8-119">Rechnungsdetails</span><span class="sxs-lookup"><span data-stu-id="abac8-119">invoicedetails</span></span> | <span data-ttu-id="abac8-120">Debitoren-Freitextrechnungspositionen in Dataverse</span><span class="sxs-lookup"><span data-stu-id="abac8-120">Dataverse customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="abac8-121">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="abac8-121">Entity flow</span></span>

<span data-ttu-id="abac8-122">Rechnungen, die aus einer Vereinbarung in Field Service erstellt werden, können mit Supply Chain Management über ein Microsoft Dataverse-Datenintegrationsprojekt synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="abac8-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="abac8-123">Aktualisierungen dieser Rechnungen werden mit den Freitextrechnungen in Supply Chain Management synchronisiert, wenn der Buchhaltungsstatus der Freitextrechnungen **In Bearbeitung** ist.</span><span class="sxs-lookup"><span data-stu-id="abac8-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="abac8-124">Nachdem die Freitextrechnungen in Supply Chain Management gebucht werden und der Buchhaltungsstatus auf **Abgeschlossen** aktualisiert wird, können Sie keine Aktualisierungen aus Field Service mehr synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="abac8-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="abac8-125">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="abac8-125">Field Service CRM solution</span></span>

<span data-ttu-id="abac8-126">Die Spalte **Hat Positionen mit Vereinbarungsursprung** ist der Tabelle **Rechnung** hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="abac8-126">The **Has Lines With Agreement Origin** column has been added to the **Invoice** table.</span></span> <span data-ttu-id="abac8-127">Mithilfe dieser Spalte wird sichergestellt, dass nur Rechnungen synchronisiert werden, die aus einer Vereinbarung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="abac8-127">This column helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="abac8-128">Der Wert entspricht **true**, wenn die Rechnung mindestens eine Rechnungsposition enthält, die ihren Ursprung in einer Vereinbarung hat.</span><span class="sxs-lookup"><span data-stu-id="abac8-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="abac8-129">Die Spalte **Hat Positionen mit Vereinbarungsursprung** ist der Tabelle **Rechnungsposition** hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="abac8-129">The **Has Agreement Origin** column has been added to the **Invoice Line** table.</span></span> <span data-ttu-id="abac8-130">Mithilfe dieser Spalte wird sichergestellt, dass nur Rechnungspositionen synchronisiert werden, die aus einer Vereinbarung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="abac8-130">This column helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="abac8-131">Der Wert ist **true**, wenn die Rechnungsposition ihren Ursprung in einer Vereinbarung hat.</span><span class="sxs-lookup"><span data-stu-id="abac8-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="abac8-132">**Rechnungsdatum** ist ein Pflichtfeld in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="abac8-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="abac8-133">Daher muss die Spalte einen Wert in Field Service haben, bevor eine Synchronisierung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="abac8-133">Therefore, the column must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="abac8-134">Um diese Anforderung zu erfüllen, wird die folgende Logik hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="abac8-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="abac8-135">Wenn die Spalte **Rechnungsdatum** in der Tabelle **Rechnung** leer ist (das heißt, wenn sie keinen Wert hat), wird sie auf das aktuelle Datum festgelegt, wenn eine Rechnungsposition hinzugefügt wird, die ihren Ursprung in einer Vereinbarung hat.</span><span class="sxs-lookup"><span data-stu-id="abac8-135">If the **Invoice Date** column is blank on the **Invoice** table (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="abac8-136">Der Benutzer kann die Spalte **Rechnungsdatum** ändern.</span><span class="sxs-lookup"><span data-stu-id="abac8-136">The user can change the **Invoice Date** column.</span></span> <span data-ttu-id="abac8-137">Wenn allerdings der Benutzer versucht, eine Rechnung zu speichern, die ihren Ursprung in einer Vereinbarung hat, erhält er oder sie einen Geschäftsprozessfehler, wenn die Spalte **Rechnungsdatum** auf der Rechnung leer ist.</span><span class="sxs-lookup"><span data-stu-id="abac8-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** column is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="abac8-138">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="abac8-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="abac8-139">In Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="abac8-139">In Supply Chain Management</span></span>

<span data-ttu-id="abac8-140">Ein Rechnungsursprung muss für die Integration eingerichtet werden, um die Freitextrechnungen in Supply Chain Management zu unterscheiden, die aus Vereinbarungsrechnungen in Field Service erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="abac8-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="abac8-141">Wenn eine Rechnung einen Rechnungsursprung des Typs **Vereinbarungsrechnungsintegration** hat, wird das Feld **Externe Rechnungsnummer** in der Kopfzeile der **Verkaufsrechnung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="abac8-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="abac8-142">Außer dass sie im Rechnungskopf angezeigt wird, kann die Information **Externe Rechnungsnummer** verwendet werden, um zu gewährleisten, dass Rechnungen, die aus Field Service-Vereinbarungsrechnungen erstellt werden, während der Rechnungssynchronisierung von Supply Chain Management mit Field Service herausgefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="abac8-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="abac8-143">Wechseln Sie zu **Debitoren** \> **Einstellungen** \> **Rechnungsursprungscodes**.</span><span class="sxs-lookup"><span data-stu-id="abac8-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="abac8-144">Wählen Sie **Neu** aus, um einen neuen Rechnungsursprung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="abac8-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="abac8-145">Geben Sie im Feld **Rechnungsursprung** einen Namen für den Rechnungsursprung ein, wie beispielsweise **FS**.</span><span class="sxs-lookup"><span data-stu-id="abac8-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="abac8-146">Geben Sie im Feld **Beschreibung** eine Beschreibung ein, wie beispielsweise **Field Service-Vereinbarungsrechnung**.</span><span class="sxs-lookup"><span data-stu-id="abac8-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="abac8-147">Aktivieren Sie das Kontrollkästchen **Ursprungstypzuweisung**.</span><span class="sxs-lookup"><span data-stu-id="abac8-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="abac8-148">Legen Sie das Feld **Rechnungsursprungstyp** auf **Vereinbarungsrechnungsintegration** fest.</span><span class="sxs-lookup"><span data-stu-id="abac8-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="abac8-149">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="abac8-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="abac8-150">Im Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="abac8-150">In the Data Integration project</span></span>

<span data-ttu-id="abac8-151">Aufgabe: **Rechnungspositionen**</span><span class="sxs-lookup"><span data-stu-id="abac8-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="abac8-152">Stellen Sie sicher, dass der Standardwert für das Supply Chain Management-Feld **Hauptkonto-Anzeigewert** aktualisiert wird, um dem gewünschten Wert zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="abac8-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="abac8-153">Der Standardvorlagenwert ist **401100**.</span><span class="sxs-lookup"><span data-stu-id="abac8-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="abac8-154">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="abac8-154">Template mapping in Data integration</span></span>

<span data-ttu-id="abac8-155">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="abac8-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="abac8-156">Vereinbarungsrechnungen (Field Service an Supply Chain Management): Rechnungskopfzeilen</span><span class="sxs-lookup"><span data-stu-id="abac8-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="abac8-157">[![Vorlagenzuordnung in Datenintegration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="abac8-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="abac8-158">Vereinbarungsrechnungen (Field Service an Supply Chain Management): Rechnungspositionen</span><span class="sxs-lookup"><span data-stu-id="abac8-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="abac8-159">[![Vorlagenzuordnung in Datenintegration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="abac8-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]