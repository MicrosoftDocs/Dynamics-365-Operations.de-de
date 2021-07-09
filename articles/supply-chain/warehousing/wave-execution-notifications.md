---
title: Wellenausführungsbenachrichtigungen
description: In diesem Thema Wellenausführungsbenachrichtungen beschrieben und die Einrichtung erläutert.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 47f270b5fff37e8e231d8a9c4a011172df3d9385
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271376"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="f1140-103">Wellenausführungsbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="f1140-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1140-104">Die Funktion *Wellenausführungsbenachrichtigungen* verwendet Geschäftsereignisse und das Aktionszentrum, um Benachrichtigungen zu übermitteln, die sich auf die Wellenausführung beziehen.</span><span class="sxs-lookup"><span data-stu-id="f1140-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="f1140-105">Hier können Sie die Ereignistypen, die Benachrichtigungen generieren, die Lagerorte, von denen sie generiert werden, und die Benutzer, die sie erhalten, angeben.</span><span class="sxs-lookup"><span data-stu-id="f1140-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="f1140-106">Die Schaltfläche **Nachrichten anzeigen** (Glockensymbol) auf der rechten Seite der Navigationsleiste zeigt an, wann eine Aktionszentrumsnachricht für den aktuellen Benutzer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f1140-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="f1140-107">Der Benutzer kann die Schaltfläche **Nachrichten anzeigen** auswählen, um das Aktionszentrum zu öffnen und die Nachrichten zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f1140-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="f1140-108">Geschäftsereignisse treten auf, wenn Geschäftsprozesse ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f1140-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="f1140-109">Geschäftsprozesse bestehen aus Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="f1140-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="f1140-110">Während eines Geschäftsprozesses führen die Benutzer, die daran teilnehmen, Geschäftsaktionen aus, um diese Aufgaben zu erledigen.</span><span class="sxs-lookup"><span data-stu-id="f1140-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="f1140-111">Geschäftsereignisse bieten einen Mechanismus, mit dem externe Systeme Benachrichtigungen von Finance and Operations-Anwendungen erhalten.</span><span class="sxs-lookup"><span data-stu-id="f1140-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="f1140-112">Auf diese Weise können die Systeme Geschäftsaktionen als Reaktion auf die Geschäftsereignisse ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1140-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="f1140-113">Weitere Informationen finden Sie unter [Übersicht über Geschäftsereignisse](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span><span class="sxs-lookup"><span data-stu-id="f1140-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="f1140-114">Funktion für Wellenausführungsbenachrichtigungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="f1140-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="f1140-115">Bevor Sie die Funktion *Wellenausführungsbenachrichtigungen* verwenden können, muss sie in Ihrem System aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="f1140-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="f1140-116">Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f1140-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f1140-117">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="f1140-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f1140-118">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="f1140-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f1140-119">**Funktionsname:** *Wellenausführungsbenachrichtigungen*</span><span class="sxs-lookup"><span data-stu-id="f1140-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="f1140-120">Szenario: Senden Sie Benachrichtigungen zur Ausführung von Wellenstapelverarbeitungen an das Aktionszentrum</span><span class="sxs-lookup"><span data-stu-id="f1140-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="f1140-121">Dieses Szenario zeigt den End-to-End-Flow zum Senden von Benachrichtigungen über Ausführungsfehler bei Wellenstapelverarbeitungen an eine bestimmte Rolle über das Aktionszentrum.</span><span class="sxs-lookup"><span data-stu-id="f1140-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="f1140-122">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="f1140-122">Make demo data available</span></span>

<span data-ttu-id="f1140-123">Um diesem Szenario zu folgen, müssen Demodaten installiert sein, und Sie müssen die juristische Person **USMF** auswählen.</span><span class="sxs-lookup"><span data-stu-id="f1140-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="f1140-124">Sicherstellen, dass Wellen im Stapelverarbeitungsmodus ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="f1140-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="f1140-125">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="f1140-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="f1140-126">Im Inforegister **Wellenverarbeitung** setzen Sie die Option **Wellen in einem Stapel verarbeiten** auf *Ja*.</span><span class="sxs-lookup"><span data-stu-id="f1140-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="f1140-127">Wenn Sie Wellenausführungsbenachrichtigungen deaktivieren möchten, legen Sie die Option **Wellenausführungsbenachrichtigungen deaktivieren** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="f1140-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="f1140-128">Eine Wellenbenachrichtigungsrichtlinie konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f1140-128">Configure a wave notification policy</span></span>

<span data-ttu-id="f1140-129">Wellenenachrichtigungsrichtlinien definieren die Arten der gesendeten Benachrichtigungen und die Benutzer, die benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="f1140-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="f1140-130">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenbenachrichtigungsrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="f1140-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="f1140-131">Erstellen Sie einen Datensatz mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="f1140-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="f1140-132">**Wellenbenachrichtigungsrichtlinie:** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="f1140-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="f1140-133">**Beschreibung:** *Wellenstapelverarbeitungsfehler bei Lagerort 24*</span><span class="sxs-lookup"><span data-stu-id="f1140-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="f1140-134">**Benachrichtigung senden an:** *Nur Fehler*</span><span class="sxs-lookup"><span data-stu-id="f1140-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="f1140-135">**An Rolle:** *Systemadministratorrolle*</span><span class="sxs-lookup"><span data-stu-id="f1140-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="f1140-136">Da in diesem Szenario Demodaten verwendet werden, wird die Rolle *Systemadministrator* der Einfachheit halber ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f1140-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="f1140-137">Da Sie als Systemadministrator angemeldet sind, erhalten Sie daher die Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="f1140-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="f1140-138">In der Praxis sollten Sie jedoch normalerweise eine spezifischere Rolle auswählen, um über Fehler bei der Ausführung von Wellenstapelverarbeitungen zu informieren, z. B. den *Lagerortleiter*.</span><span class="sxs-lookup"><span data-stu-id="f1140-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="f1140-139">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="f1140-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="f1140-140">Eine Wellenvorlage konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f1140-140">Configure a wave template</span></span>

<span data-ttu-id="f1140-141">Mit Wellenvorlagen können Sie bestimmte Instanzen von Wellenmethoden mit entsprechenden Wellenetikettenvorlagen verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="f1140-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="f1140-142">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="f1140-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="f1140-143">Stellen Sie im Listenbereich das Feld **Wellenvorlagentyp** auf *Versand* und wählen Sie dann die Wellenvorlage *Standard-24-Lieferung* für Lagerort 24 aus.</span><span class="sxs-lookup"><span data-stu-id="f1140-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="f1140-144">Im Inforegister **Allgemein** legen Sie das Feld **Wellenbenachrichtigungsrichtlinie** auf *24BatchError* fest.</span><span class="sxs-lookup"><span data-stu-id="f1140-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="f1140-145">Eine Arbeitsvorlage konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f1140-145">Configure a work template</span></span>

<span data-ttu-id="f1140-146">Arbeitsvorlagen werden während der Wellenausführung verwendet, um Arbeit zu generieren.</span><span class="sxs-lookup"><span data-stu-id="f1140-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="f1140-147">In diesem Szenario sollte die Wellenausführung einen Fehler auslösen.</span><span class="sxs-lookup"><span data-stu-id="f1140-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="f1140-148">Indem Sie die Arbeitsvorlagenabfrage so einstellen, dass ein nicht vorhandene Lagerort verwendet wird, stellen Sie sicher, dass die Wellenausführung fehlschlägt und daher eine Benachrichtigung sendet.</span><span class="sxs-lookup"><span data-stu-id="f1140-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="f1140-149">Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="f1140-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="f1140-150">Stellen Sie im Listenbereich das Feld **Arbeitsvorlagentyp** auf *Aufträge* und wählen Sie dann die Arbeitsvorlage *24 SO-Phase* für Lagerort 24 aus.</span><span class="sxs-lookup"><span data-stu-id="f1140-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="f1140-151">Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="f1140-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="f1140-152">Bearbeiten Sie in der Registerkarte **Bereich** des Dialogfelds des Abfrageeditors die folgende Zeile (oder fügen Sie sie hinzu, wenn sie nicht vorhanden ist):</span><span class="sxs-lookup"><span data-stu-id="f1140-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="f1140-153">**Tabelle:** *Temporäre Arbeitstransaktionen*</span><span class="sxs-lookup"><span data-stu-id="f1140-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="f1140-154">**Abgeleitete Tabelle:** *Temporäre Arbeitstransaktionen*</span><span class="sxs-lookup"><span data-stu-id="f1140-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="f1140-155">**Feld:** *Lagerort*</span><span class="sxs-lookup"><span data-stu-id="f1140-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="f1140-156">**Kriterien:** Ändern Sie den Wert von *24* auf *Fehler*.</span><span class="sxs-lookup"><span data-stu-id="f1140-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="f1140-157">Bestätigen Sie die Änderung mit **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1140-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="f1140-158">Einen Auftrag erstellen und ihn für den Lagerort freigeben</span><span class="sxs-lookup"><span data-stu-id="f1140-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="f1140-159">Gehen Sie zu **Vertrieb und Marketing \> Auftrag \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="f1140-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="f1140-160">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="f1140-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="f1140-161">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f1140-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f1140-162">**Lagerort:** *24*</span><span class="sxs-lookup"><span data-stu-id="f1140-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="f1140-163">Fügen Sie im Inforegister **Auftragspositionen** eine Auftragsposition mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="f1140-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="f1140-164">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="f1140-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="f1140-165">**Menge** *10*</span><span class="sxs-lookup"><span data-stu-id="f1140-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="f1140-166">Diese Artikel und Mengen sind nur Beispiele.</span><span class="sxs-lookup"><span data-stu-id="f1140-166">These items and quantities are only examples.</span></span> <span data-ttu-id="f1140-167">Der betroffene Lagerort muss ausreichen Bestände haben.</span><span class="sxs-lookup"><span data-stu-id="f1140-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="f1140-168">Während die neue Auftragsposition weiterhin im Inforegister **Auftragspositionen** ausgewählt ist, wählen Sie im Menü **Bestand \> Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="f1140-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="f1140-169">Wählen Sie auf der Seite **Reservierung** im Aktivitätsbereich **Los reservieren** aus.</span><span class="sxs-lookup"><span data-stu-id="f1140-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="f1140-170">Schließen Sie nun die Seite.</span><span class="sxs-lookup"><span data-stu-id="f1140-170">Then close the page.</span></span>
1. <span data-ttu-id="f1140-171">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="f1140-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="f1140-172">Benachrichtigungen von der Ausführung von Wellenstapelverarbeitungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="f1140-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="f1140-173">Abhängig von der Einrichtung Ihrer Geschäftsereignisse erhalten Sie möglicherweise eine Benachrichtigung über einen Fehler bei der Wellenausführung.</span><span class="sxs-lookup"><span data-stu-id="f1140-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="f1140-174">Die Aktionszentrumsnachricht ähnelt dem folgenden Beispiel und enthält einen Link zu der Welle, die fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="f1140-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="f1140-175">**Fehler bei der Zyklusausführung**</span><span class="sxs-lookup"><span data-stu-id="f1140-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="f1140-176">Beim Ausführen der Welle USMF-000000001 ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f1140-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="f1140-177">Letzte Nachrichten: Für Welle USMF-000000001 wurde keine Arbeit erstellt.</span><span class="sxs-lookup"><span data-stu-id="f1140-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="f1140-178">**STATUS**</span><span class="sxs-lookup"><span data-stu-id="f1140-178">**STATUS**</span></span>  
> <span data-ttu-id="f1140-179">Aktiv</span><span class="sxs-lookup"><span data-stu-id="f1140-179">Active</span></span>
>
> <span data-ttu-id="f1140-180">Offene Zyklusdetails</span><span class="sxs-lookup"><span data-stu-id="f1140-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
