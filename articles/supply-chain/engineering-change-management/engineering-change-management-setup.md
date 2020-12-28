---
title: Festlegen allgemeiner Werte für die Verwaltung für technische Änderung
description: Dieses Thema beschreibt, wie Sie allgemeine Werte festlegen, die für Parameter in verschiedenen Teilen der Verwaltung für technische Änderung verwendet werden.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 86de050ef4110e3485a77099440f3402e46cc498
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2020
ms.locfileid: "4429157"
---
# <a name="establish-common-values-for-engineering-change-management"></a><span data-ttu-id="31488-103">Festlegen allgemeiner Werte für die Verwaltung für technische Änderung</span><span class="sxs-lookup"><span data-stu-id="31488-103">Establish common values for engineering change management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31488-104">Wenn Sie die Verwaltung für technische Änderung festlegen, müssen Sie mehrere Sammlungen von Werten einrichten, die zum Ausfüllen von Dropdown-Listen in anderen Teilen der Benutzeroberfläche (UI) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31488-104">When you set up engineering change management, you must establish several collections of values that will be used to fill in drop-down lists in other parts of the user interface (UI).</span></span> <span data-ttu-id="31488-105">Sie sollten diese Werte entsprechend den Produkttypen, die Sie herstellen, und Ihren spezifischen Geschäftsanforderungen festlegen.</span><span class="sxs-lookup"><span data-stu-id="31488-105">You should specify these values according to the types of products that you produce and your specific business needs.</span></span>

## <a name="engineering-change-categories"></a><span data-ttu-id="31488-106">Kategorien der technischen Änderungen</span><span class="sxs-lookup"><span data-stu-id="31488-106">Engineering change categories</span></span>

<span data-ttu-id="31488-107">Sie verwenden Verwaltung für technische Änderungs-Kategorien, um Ihre Entwicklungsänderungsaufträge zu organisieren, sodass sie einfacher zu verwalten und zu überprüfen sind.</span><span class="sxs-lookup"><span data-stu-id="31488-107">You use engineering change categories to organize your engineering change orders, so that they are easier to manage and review.</span></span> <span data-ttu-id="31488-108">Es kann z. B. sinnvoll sein, einen Workflow festzulegen, bei dem je nach Kategorie eine bestimmte Abteilung die vorgeschlagenen Änderungen überprüfen muss.</span><span class="sxs-lookup"><span data-stu-id="31488-108">For example, you might find it useful to set up a workflow where, depending on the category, a specific department must review the proposed changes.</span></span> <span data-ttu-id="31488-109">Daher enthält der Änderungsauftrag ein **Kategorie**-Feld.</span><span class="sxs-lookup"><span data-stu-id="31488-109">Therefore, the engineering change order includes a **Category** field.</span></span>

<span data-ttu-id="31488-110">Um die Sammlung von Entwicklungsänderungs-Kategorien einzurichten, die in Ihrer Firma verwendet wird, gehen Sie zu **Verwaltung für technische Änderung \> Einrichtung \> Verwaltung für technische Änderung \> Entwicklungsänderungs-Kategorien**.</span><span class="sxs-lookup"><span data-stu-id="31488-110">To establish the collection of engineering change categories that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change categories**.</span></span> <span data-ttu-id="31488-111">Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.</span><span class="sxs-lookup"><span data-stu-id="31488-111">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-priorities"></a><span data-ttu-id="31488-112">Prioritäten der technischen Änderungen</span><span class="sxs-lookup"><span data-stu-id="31488-112">Engineering change priorities</span></span>

<span data-ttu-id="31488-113">Sie verwenden Änderungsprioritäten, um die Wichtigkeit oder Dringlichkeit eines Änderungsauftrags anzugeben.</span><span class="sxs-lookup"><span data-stu-id="31488-113">You use engineering change priorities to indicate the importance or urgency of an engineering change order.</span></span> <span data-ttu-id="31488-114">Sie können Ihnen helfen, die Wichtigkeit eines Änderungsauftrags im Auge zu behalten, sodass Sie leicht erkennen können, welche Aufträge zuerst und wie schnell bearbeitet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="31488-114">They can help you keep track of the importance of an engineering change order, so that you can easily identify which orders should be processed first, and how quickly.</span></span>

<span data-ttu-id="31488-115">Um die Sammlung von Entwicklungsänderungsprioritäten einzurichten, die in Ihrem Unternehmen verwendet wird, gehen Sie zu **Verwaltung für technische Änderung \> Einrichten \> Verwaltung für technische Änderung \> Entwicklungsänderungsprioritäten**.</span><span class="sxs-lookup"><span data-stu-id="31488-115">To establish the collection of engineering change priorities that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change priorities**.</span></span> <span data-ttu-id="31488-116">Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.</span><span class="sxs-lookup"><span data-stu-id="31488-116">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-reasons"></a><span data-ttu-id="31488-117">Gründe für technische Änderung</span><span class="sxs-lookup"><span data-stu-id="31488-117">Engineering change reasons</span></span>

<span data-ttu-id="31488-118">Änderungsgründe geben die Ursache oder Art der Änderung im Änderungsauftrag an.</span><span class="sxs-lookup"><span data-stu-id="31488-118">Engineering change reasons indicate the cause or nature of the change in the change order.</span></span>

<span data-ttu-id="31488-119">Um die Sammlung von Entwicklungsänderungsgründen einzurichten, die in Ihrer Firma verwendet wird, gehen Sie zu **Verwaltung für technische Änderung \> Einrichten \> Verwaltung für technische Änderung \> Entwicklungsänderungsgründe**.</span><span class="sxs-lookup"><span data-stu-id="31488-119">To establish the collection of engineering change reasons that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change reasons**.</span></span> <span data-ttu-id="31488-120">Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.</span><span class="sxs-lookup"><span data-stu-id="31488-120">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="material-disposal-codes"></a><span data-ttu-id="31488-121">Materialdispositionscodes</span><span class="sxs-lookup"><span data-stu-id="31488-121">Material disposal codes</span></span>

<span data-ttu-id="31488-122">Sie verwenden Materialentsorgungscodes, um Materialien zu kategorisieren, die in Ihren fertigen Waren verwendet werden, oder Komponenten, die auf eine bestimmte Art und Weise entsorgt werden müssen oder eine bestimmte Behandlung erfordern, bevor sie dem normalen Müll hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="31488-122">You use material disposal codes to categorize materials that are used in your finished goods, or components that must be disposed of in a specific way or require some treatment before they can be added to your regular trash.</span></span> <span data-ttu-id="31488-123">Wenn Sie ein relevantes Produkt zu einem Änderungsauftrag hinzufügen, können Sie einen Entsorgungscode als Teil der Änderungsdetails zuweisen.</span><span class="sxs-lookup"><span data-stu-id="31488-123">When you add a relevant product to an engineering change order, you can assign a disposal code as part of the change details.</span></span>

<span data-ttu-id="31488-124">Um die Sammlung von Materialentsorgungscodes einzurichten, die in Ihrer Firma verwendet wird, gehen Sie zu **Verwaltung für technische Änderung \> Einrichtung \> Verwaltung für technische Änderung \> Materialentsorgungscodes**.</span><span class="sxs-lookup"><span data-stu-id="31488-124">To establish the collection of material disposal codes that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Material disposal codes**.</span></span> <span data-ttu-id="31488-125">Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.</span><span class="sxs-lookup"><span data-stu-id="31488-125">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="received-customer-approval"></a><span data-ttu-id="31488-126">Empfangene Debitorengenehmigung</span><span class="sxs-lookup"><span data-stu-id="31488-126">Received customer approval</span></span>

<span data-ttu-id="31488-127">Wenn Sie Produkte für einen bestimmten Kunden entwerfen, müssen der Entwurf und die Spezifikationen oft validiert werden, bevor das Produkt als fertig festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="31488-127">When you design products for a specific customer, the design and specifications often must be validated before the product can be set as ready.</span></span> <span data-ttu-id="31488-128">Im Feld **Erhaltene Kundenfreigabe** können Sie angeben, wie weit das Produkt im Prozess der Kundenfreigabe ist und/oder ob die Freigabe erhalten wurde.</span><span class="sxs-lookup"><span data-stu-id="31488-128">The **Received customer approval** field lets you indicate how far in the customer approval process the product is and/or whether the approval has been received.</span></span>

<span data-ttu-id="31488-129">Um die Sammlung der Werte für erhaltene Kundenfreigaben einzurichten, die in Ihrer Firma verwendet wird, gehen Sie zu **Verwaltung für technische Änderung \> Einrichten \> Verwaltung für technische Änderung \> Erhaltene Kundenfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="31488-129">To establish the collection of received customer approval values that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Received customer approval**.</span></span> <span data-ttu-id="31488-130">Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.</span><span class="sxs-lookup"><span data-stu-id="31488-130">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change--environmental-health-and-safety-codes"></a><span data-ttu-id="31488-131">Technische Änderungen - Umwelt- und Sicherheitsvorschriften</span><span class="sxs-lookup"><span data-stu-id="31488-131">Engineering change – Environmental health and safety codes</span></span>

<span data-ttu-id="31488-132">Wenn bei der Herstellung eines Produkts standardmäßige Umwelt- und Sicherheitsvorschriften oder firmenspezifische Vorschriften oder Verfahren berücksichtigt werden müssen, können Sie die Umwelt- und Sicherheitscodes verwenden, um diese zu definieren.</span><span class="sxs-lookup"><span data-stu-id="31488-132">If any standard environmental health and safety regulations, or company-specific regulations or procedures, must be considered in the manufacture of a product, you can use the environmental health and safety codes to define them.</span></span> <span data-ttu-id="31488-133">Im Änderungsauftrag können Sie angeben, welche Codes für die Herstellung eines Produkts gelten, während Sie die Details des betroffenen Produkts bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="31488-133">In the engineering change order, you can indicate which codes apply to the manufacture of a product while you edit the details of the affected product.</span></span>

<span data-ttu-id="31488-134">Um die Sammlung von Zustands- und Sicherheitswerten einzurichten, die in Ihrer Firma verwendet wird, gehen Sie zu **Verwaltung für technische Änderung \> Einrichten \> Verwaltung für technische Änderung \> Entwicklungsänderung - Umwelt- und Sicherheitscodes**.</span><span class="sxs-lookup"><span data-stu-id="31488-134">To establish the collection of health and safety values that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change - Environmental health and safety codes**.</span></span> <span data-ttu-id="31488-135">Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.</span><span class="sxs-lookup"><span data-stu-id="31488-135">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-severities"></a><span data-ttu-id="31488-136">Schweregrade der technischen Änderungen</span><span class="sxs-lookup"><span data-stu-id="31488-136">Engineering change severities</span></span>

<span data-ttu-id="31488-137">Sie verwenden Änderungsschweregrade, um den Grad der Auswirkungen anzugeben, der für die Produkte in einem Änderungsauftrag gilt.</span><span class="sxs-lookup"><span data-stu-id="31488-137">You use engineering change severities to indicate the level of impact that applies to the products in an engineering change order.</span></span>

<span data-ttu-id="31488-138">Um die Sammlung der Schweregrade für technische Änderungen einzurichten, die in Ihrer Firma verwendet wird, gehen Sie zu **Verwaltung für technische Änderungen \> Einrichten \> Verwaltung für technische Änderungen \> Schweregrade für technische Änderungen**.</span><span class="sxs-lookup"><span data-stu-id="31488-138">To establish the collection of engineering change severities that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change severities**.</span></span> <span data-ttu-id="31488-139">Sie können dann die Schaltflächen im Aktivitätsbereich verwenden, um Werte hinzuzufügen, zu entfernen und zu bearbeiten und um sie in der Reihenfolge anzuordnen, in der sie in den Dropdown-Listen, in denen sie angezeigt werden, erscheinen sollen.</span><span class="sxs-lookup"><span data-stu-id="31488-139">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

<span data-ttu-id="31488-140">Sie können Regeln festlegen, die für jeden von Ihnen erstellten Schweregrad gelten.</span><span class="sxs-lookup"><span data-stu-id="31488-140">You can establish rules that apply to each severity level that you create.</span></span> <span data-ttu-id="31488-141">Weitere Informationen darüber, wie Sie diese Regeln zuweisen, finden Sie im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="31488-141">For more information about how to assign these rules, see the next section.</span></span>

## <a name="engineering-change-severity-rule-sets"></a><span data-ttu-id="31488-142">Schweregradregelsatz für technische Änderung</span><span class="sxs-lookup"><span data-stu-id="31488-142">Engineering change severity rule sets</span></span>

<span data-ttu-id="31488-143">Mit den Regeln für den Schweregrad von technischen Änderungen legen Sie eine Gruppe von Regeln fest, mit denen Sie den Schweregrad des Änderungsauftrags automatisch berechnen können, basierend auf der Art der Änderungen in den betroffenen Produkten.</span><span class="sxs-lookup"><span data-stu-id="31488-143">You use engineering change severity rule sets to establish a group of rules that you can use to automatically calculate the severity of the change order, based on the type of changes in the affected products.</span></span> <span data-ttu-id="31488-144">Um die Schweregrad-Regeln zu verwenden, öffnen Sie die Seite **Parameter für die Verwaltung für technische Änderungen** und legen das Feld **Schweregrad-Regel** auf *Berechnen* oder *Automatisch berechnen* fest.</span><span class="sxs-lookup"><span data-stu-id="31488-144">To use the severity rules, open the **Engineering change management parameters** page, and set the **Severity rule** field to *Calculate* or *Calculate automatically*.</span></span>

<span data-ttu-id="31488-145">Wenn das System den Schweregrad bewertet, verarbeitet es die Regeln in der Reihenfolge, in der sie auf der Seite erscheinen, von oben nach unten.</span><span class="sxs-lookup"><span data-stu-id="31488-145">When the system evaluates severity, it processes the rules in the order in which they appear on the page, from top to bottom.</span></span> <span data-ttu-id="31488-146">Damit eine Regel ausgewählt und ihre Priorität festgelegt werden kann, müssen alle Regeln in einem Regelsatz erfüllt sein.</span><span class="sxs-lookup"><span data-stu-id="31488-146">For a rule to be selected and have its priority established, all the rules in a rule set must be met.</span></span>

<span data-ttu-id="31488-147">Um die Regeln festzulegen, die für jeden von Ihnen definierten Schweregrad einer Änderung gelten, gehen Sie zu **Verwaltung für technische Änderungen \> Einrichtung \> Verwaltung für technische Änderungen \> Regelsätze für den Schweregrad technischer Änderungen**.</span><span class="sxs-lookup"><span data-stu-id="31488-147">To set up the rules that apply to each change severity level that you've defined, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change severity rule sets**.</span></span> <span data-ttu-id="31488-148">Führen Sie dann einen der folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="31488-148">Then follow one of these steps.</span></span>

- <span data-ttu-id="31488-149">Um einen neuen Regelsatz zu erstellen, wählen Sie **Neu** im Aktivitätsbereich und legen Sie dann die Felder fest, wie später in diesem Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="31488-149">To create a new rule set, select **New** on the Action Pane, and then set the fields as described later in this section.</span></span>
- <span data-ttu-id="31488-150">Um einen vorhandenen Regelsatz zu bearbeiten, wählen Sie ihn im Listenbereich aus, wählen Sie **Bearbeiten** im Aktivitätsbereich und legen Sie dann die Felder fest, wie später in diesem Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="31488-150">To edit an existing rule set, select it in the list pane, select **Edit** on the Action Pane, and then set the fields as described later in this section.</span></span>
- <span data-ttu-id="31488-151">Um einen bestehenden Regelsatz zu löschen, wählen Sie ihn im Listenbereich aus und wählen Sie dann **Löschen** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="31488-151">To delete an existing rule set, select it in the list pane, and then select **Delete** on the Action Pane.</span></span>
- <span data-ttu-id="31488-152">Um die Liste der Regelsätze neu anzuordnen, wählen Sie einen Regelsatz im Listenbereich aus und verwenden dann die Schaltflächen **Aufwärts** und **Abwärts** im Aktivitätsbereich, um ihn neu zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="31488-152">To rearrange the list of rule sets, select a rule set in the list pane, and then use the **Up** and **Down** buttons on the Action Pane to reposition it.</span></span>

<span data-ttu-id="31488-153">Legen Sie für jeden Regelsatz das folgende Feld fest:</span><span class="sxs-lookup"><span data-stu-id="31488-153">For each rule set, set the following field:</span></span>

- <span data-ttu-id="31488-154">**Schweregrad** - Wählen Sie den Schweregrad, für den Regeln aufgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="31488-154">**Severity** – Select the severity level to establish rules for.</span></span> <span data-ttu-id="31488-155">Sie verwenden die Seite **Schweregrade ändern**, um die Stufen zu erstellen und zu benennen.</span><span class="sxs-lookup"><span data-stu-id="31488-155">You use the **Engineering change severities** page to create and name the levels.</span></span> <span data-ttu-id="31488-156">(Weitere Informationen finden Sie im vorherigen Abschnitt.)</span><span class="sxs-lookup"><span data-stu-id="31488-156">(For more information, see the previous section.)</span></span>

<span data-ttu-id="31488-157">Verwenden Sie die Schaltflächen auf dem Inforegister **Regeln**, um eine Regel für die aktuelle Schweregrad-Einstellung hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="31488-157">Use the buttons on the **Rules** FastTab to add or remove a rule for the current severity setting.</span></span> <span data-ttu-id="31488-158">Jede Regel hat ein Feld **Regel** und ein Feld **Name**.</span><span class="sxs-lookup"><span data-stu-id="31488-158">Each rule has a **Rule** field and a **Name** field.</span></span> <span data-ttu-id="31488-159">Die Regeln werden vom System festgelegt und geben die Arten von Änderungen an, die ein Produkt haben kann.</span><span class="sxs-lookup"><span data-stu-id="31488-159">The rules are established by the system and indicate the types of changes that a product can have.</span></span> <span data-ttu-id="31488-160">Der Name gibt die Art der Änderung an.</span><span class="sxs-lookup"><span data-stu-id="31488-160">The name indicates the type of change.</span></span>