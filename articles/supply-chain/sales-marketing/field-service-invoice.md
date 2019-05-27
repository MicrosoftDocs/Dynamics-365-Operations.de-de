---
title: Synchronisieren von Vereinbarungsrechnungen in Field Service mit Freitextrechnungen in Finance and Operations
description: Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Vereinbarungsrechnungen in Microsoft Dynamics 365 for Field Service mit Freitextrechnungen in Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
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
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560162"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="043cb-103">Vereinbarungsrechnungen in Field Service mit Freitextrechnungen in Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="043cb-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="043cb-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Vereinbarungsrechnungen in Microsoft Dynamics 365 for Field Service mit Freitextrechnungen in Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="043cb-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="043cb-105">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="043cb-105">Templates and tasks</span></span>

<span data-ttu-id="043cb-106">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um die Synchronisierung von Vereinbarungsrechnungen aus Field Service mit Freitextrechnungen in Finance and Operations auszuführen.</span><span class="sxs-lookup"><span data-stu-id="043cb-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="043cb-107">**Name der Vorlage in der Datenintegration:**</span><span class="sxs-lookup"><span data-stu-id="043cb-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="043cb-108">Vereinbarungsrechnungen (Field Service nach Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="043cb-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="043cb-109">**Namen der Aufgaben im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="043cb-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="043cb-110">Rechnungsköpfe</span><span class="sxs-lookup"><span data-stu-id="043cb-110">Invoice headers</span></span>
- <span data-ttu-id="043cb-111">Rechnungspositionen</span><span class="sxs-lookup"><span data-stu-id="043cb-111">Invoice lines</span></span>

<span data-ttu-id="043cb-112">Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von Vereinbarungsrechnungen erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="043cb-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="043cb-113">Konten (Sales nach Finance and Operations) – Direkt</span><span class="sxs-lookup"><span data-stu-id="043cb-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="043cb-114">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="043cb-114">Entity set</span></span>

| <span data-ttu-id="043cb-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="043cb-115">Field Service</span></span>  | <span data-ttu-id="043cb-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="043cb-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="043cb-117">Rechnungen</span><span class="sxs-lookup"><span data-stu-id="043cb-117">invoices</span></span>       | <span data-ttu-id="043cb-118">CDS-Debitoren-Freitextrechnungskopfzeilen</span><span class="sxs-lookup"><span data-stu-id="043cb-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="043cb-119">Rechnungsdetails</span><span class="sxs-lookup"><span data-stu-id="043cb-119">invoicedetails</span></span> | <span data-ttu-id="043cb-120">CDS-Debitoren-Freitextrechnungspositionen</span><span class="sxs-lookup"><span data-stu-id="043cb-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="043cb-121">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="043cb-121">Entity flow</span></span>

<span data-ttu-id="043cb-122">Rechnungen, die aus einer Vereinbarung in Field Service erstellt werden, können mit Finance and Operations über ein Common Data Service (CDS)-Datenintegrationsprojekt synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="043cb-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="043cb-123">Aktualisierungen dieser Rechnungen werden mit den Freitextrechnungen in Finance and Operations synchronisiert, wenn der Buchhaltungsstatus der Freitextrechnungen **In Bearbeitung** ist.</span><span class="sxs-lookup"><span data-stu-id="043cb-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="043cb-124">Nachdem die Freitextrechnungen in Finance and Operations gebucht werden und der Buchhaltungsstatus auf **Abgeschlossen** aktualisiert wird, können Sie keine Aktualisierungen aus Field Service mehr synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="043cb-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="043cb-125">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="043cb-125">Field Service CRM solution</span></span>

<span data-ttu-id="043cb-126">Das Feld **Hat Positionen mit Vereinbarungsursprung** ist der Entität **Rechnung** hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="043cb-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="043cb-127">Mithilfe dieses Felds wird sichergestellt, dass nur Rechnungen synchronisiert werden, die aus einer Vereinbarung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="043cb-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="043cb-128">Der Wert entspricht **true**, wenn die Rechnung mindestens eine Rechnungsposition enthält, die ihren Ursprung in einer Vereinbarung hat.</span><span class="sxs-lookup"><span data-stu-id="043cb-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="043cb-129">Das Feld **Hat Vereinbarungsursprung** ist der Entität **Rechnungsposition** hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="043cb-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="043cb-130">Mithilfe dieses Felds wird sichergestellt, dass nur Rechnungspositionen synchronisiert werden, die aus einer Vereinbarung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="043cb-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="043cb-131">Der Wert ist **true**, wenn die Rechnungsposition ihren Ursprung in einer Vereinbarung hat.</span><span class="sxs-lookup"><span data-stu-id="043cb-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="043cb-132">**Rechnungsdatum** ist ein Pflichtfeld in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="043cb-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="043cb-133">Daher muss das Feld einen Wert in Field Service haben, bevor eine Synchronisierung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="043cb-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="043cb-134">Um diese Anforderung zu erfüllen, wird die folgende Logik hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="043cb-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="043cb-135">Wenn das Feld **Rechnungsdatum** in der Entität **Rechnung** leer ist (das heißt, wenn es keinen Wert hat), wird es auf das aktuelle Datum festgelegt, wenn eine Rechnungsposition hinzugefügt wird, die ihren Ursprung in einer Vereinbarung hat.</span><span class="sxs-lookup"><span data-stu-id="043cb-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="043cb-136">Der Benutzer kann das Feld **Rechnungsdatum** ändern.</span><span class="sxs-lookup"><span data-stu-id="043cb-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="043cb-137">Wenn allerdings der Benutzer versucht, eine Rechnung zu speichern, die ihren Ursprung in einer Vereinbarung hat, erhält er oder sie einen Geschäftsprozessfehler, wenn das Feld **Rechnungsdatum** auf der Rechnung leer ist.</span><span class="sxs-lookup"><span data-stu-id="043cb-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="043cb-138">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="043cb-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="043cb-139">In Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="043cb-139">In Finance and Operations</span></span>

<span data-ttu-id="043cb-140">Ein Rechnungsursprung muss für die Integration eingerichtet werden, um die Freitextrechnungen in Finance and Operations zu unterscheiden, die aus Vereinbarungsrechnungen in Field Service erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="043cb-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="043cb-141">Wenn eine Rechnung einen Rechnungsursprung des Typs **Vereinbarungsrechnungsintegration** hat, wird das Feld **Externe Rechnungsnummer** in der Kopfzeile der **Verkaufsrechnung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="043cb-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="043cb-142">Außer dass sie im Rechnungskopf angezeigt wird, kann die Information **Externe Rechnungsnummer** verwendet werden, um zu gewährleisten, dass Rechnungen, die aus Field Service-Vereinbarungsrechnungen erstellt werden, während der Rechnungssynchronisierung von Finance and Operations mit Field Service herausgefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="043cb-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="043cb-143">Wechseln Sie zu **Debitoren** \> **Einstellungen** \> **Rechnungsursprungscodes**.</span><span class="sxs-lookup"><span data-stu-id="043cb-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="043cb-144">Wählen Sie **Neu** aus, um einen neuen Rechnungsursprung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="043cb-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="043cb-145">Geben Sie im Feld **Rechnungsursprung** einen Namen für den Rechnungsursprung ein, wie beispielsweise **FS**.</span><span class="sxs-lookup"><span data-stu-id="043cb-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="043cb-146">Geben Sie im Feld **Beschreibung** eine Beschreibung ein, wie beispielsweise **Field Service-Vereinbarungsrechnung**.</span><span class="sxs-lookup"><span data-stu-id="043cb-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="043cb-147">Aktivieren Sie das Kontrollkästchen **Ursprungstypzuweisung**.</span><span class="sxs-lookup"><span data-stu-id="043cb-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="043cb-148">Legen Sie das Feld **Rechnungsursprungstyp** auf **Vereinbarungsrechnungsintegration** fest.</span><span class="sxs-lookup"><span data-stu-id="043cb-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="043cb-149">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="043cb-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="043cb-150">Im Datenenintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="043cb-150">In the Data Integration project</span></span>

<span data-ttu-id="043cb-151">Aufgabe: **Rechnungspositionen**</span><span class="sxs-lookup"><span data-stu-id="043cb-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="043cb-152">Stellen Sie sicher, dass der Standardwert für das Finance and Operations-Feld **Hauptkonto-Anzeigewert** aktualisiert wird, um dem gewünschten Wert zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="043cb-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="043cb-153">Der Standardvorlagenwert ist **401100**.</span><span class="sxs-lookup"><span data-stu-id="043cb-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="043cb-154">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="043cb-154">Template mapping in Data integration</span></span>

<span data-ttu-id="043cb-155">Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="043cb-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a><span data-ttu-id="043cb-156">Vereinbarungsrechnungen (Field Service zu Fin und Ops): Rechnungsköpfe</span><span class="sxs-lookup"><span data-stu-id="043cb-156">Agreement invoices (Field Service to Fin and Ops): Invoice headers</span></span>

<span data-ttu-id="043cb-157">[![Vorlagenzuordnung in Datenintegration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="043cb-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a><span data-ttu-id="043cb-158">Vereinbarungsrechnungen (Field Service zu Fin und Ops): Rechnungspositionen</span><span class="sxs-lookup"><span data-stu-id="043cb-158">Agreement invoices (Field Service to Fin and Ops): Invoice lines</span></span>

<span data-ttu-id="043cb-159">[![Vorlagenzuordnung in Datenintegration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="043cb-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>
