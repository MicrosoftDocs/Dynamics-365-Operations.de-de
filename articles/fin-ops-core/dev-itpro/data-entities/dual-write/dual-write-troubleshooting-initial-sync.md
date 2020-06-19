---
title: Probleme bei der anfänglichen Synchronisierung behandeln
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Synchronisierung zusammenhängen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410080"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="a332c-103">Probleme bei der anfänglichen Synchronisierung behandeln</span><span class="sxs-lookup"><span data-stu-id="a332c-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a332c-104">Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a332c-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="a332c-105">Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Synchronisierung zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="a332c-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a332c-106">Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators.</span><span class="sxs-lookup"><span data-stu-id="a332c-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="a332c-107">Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a332c-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="a332c-108">Überprüfen Sie eine Finance and Operations App auf anfängliche Synchronisationsfehler</span><span class="sxs-lookup"><span data-stu-id="a332c-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="a332c-109">Nachdem Sie die Zuordnungsvorlagen aktiviert haben, sollte der Status der Zuordnungen lauten **Laufen**.</span><span class="sxs-lookup"><span data-stu-id="a332c-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="a332c-110">Wenn der Status ist **Nicht ausgeführt** angezeigt wird, sind bei der ersten Synchronisierung Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a332c-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="a332c-111">Um die Fehler anzuzeigen, wählen Sie die **Anfängliche Synchronisierungsdetail** Registerkarte auf der **Duales Schreiben** Seite.</span><span class="sxs-lookup"><span data-stu-id="a332c-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Registerkarte Details zur Erstsynchronisierung](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="a332c-113">Sie können die anfängliche Synchronisierung nicht abschließen: 400 Bad Request</span><span class="sxs-lookup"><span data-stu-id="a332c-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="a332c-114">**Erforderliche Rolle zum Beheben der Fehler:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="a332c-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="a332c-115">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, das Mapping und die anfängliche Synchronisierung auszuführen:</span><span class="sxs-lookup"><span data-stu-id="a332c-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="a332c-116">*Der Remote-Server hat einen Fehler zurückgegeben: (400) Bad Request.), beim AX Export ist ein Fehler aufgetreten*</span><span class="sxs-lookup"><span data-stu-id="a332c-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="a332c-117">Hier ist ein Beispiel für die vollständige Fehlernachricht.</span><span class="sxs-lookup"><span data-stu-id="a332c-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="a332c-118">Wenn dieser Fehler konsistent auftritt und Sie die anfängliche Synchronisierung nicht abschließen können, führen Sie die folgenden Schritte aus, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="a332c-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="a332c-119">Melden Sie sich bei der virtuellen Maschine (VM) für die Finance and Operations App an.</span><span class="sxs-lookup"><span data-stu-id="a332c-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="a332c-120">Öffnen Sie die Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="a332c-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="a332c-121">In dem Bereich **Dienstleistungen** stellen Sie sicher, dass der Microsoft Dynamics 365 Data Import Export Framework-Dienst wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a332c-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="a332c-122">Starten Sie ihn neu, wenn er gestoppt wurde, da die anfängliche Synchronisierung dies erfordert.</span><span class="sxs-lookup"><span data-stu-id="a332c-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="a332c-123">Anfänglicher Synchronisationsfehler: 403 Forbidden</span><span class="sxs-lookup"><span data-stu-id="a332c-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="a332c-124">Während der ersten Synchronisierung wird möglicherweise die folgende Fehlermeldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="a332c-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="a332c-125">*(\[Forbidden\], der Remote-Server hat einen Fehler zurückgegeben: (403) Forbidden.), AX beim Export ist ein Fehler aufgetreten*</span><span class="sxs-lookup"><span data-stu-id="a332c-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="a332c-126">Führen Sie folgende Schritte aus, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="a332c-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="a332c-127">Bei der Finance and Operations App anmelden.</span><span class="sxs-lookup"><span data-stu-id="a332c-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="a332c-128">Auf der **Azure Active Directory Anwendungen** Seite löschen Sie den **DtAppID** Client, und fügen Sie ihn dann erneut hinzu.</span><span class="sxs-lookup"><span data-stu-id="a332c-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Liste der Azure AD Bewerbungen](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="a332c-130">Selbstreferenzfehler oder Zirkelreferenzfehler während der ersten Synchronisation</span><span class="sxs-lookup"><span data-stu-id="a332c-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="a332c-131">Möglicherweise wird eine Fehlernachricht angezeigt, die dem folgenden Beispiel ähnelt, wenn eine Ihrer Zuordnungen Selbstreferenzen oder Zirkelreferenzen enthält:</span><span class="sxs-lookup"><span data-stu-id="a332c-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="a332c-132">Die Fehler fallen in folgende Kategorien:</span><span class="sxs-lookup"><span data-stu-id="a332c-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="a332c-133">Kreditoren V2 zu msdyn_vendors Entitätzuordnung</span><span class="sxs-lookup"><span data-stu-id="a332c-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="a332c-134">Zuordnung der Entitäten von Kunden V3 zu Konten</span><span class="sxs-lookup"><span data-stu-id="a332c-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="a332c-135">Beheben Sie einen Fehler in der Entitätszuordnung von Vendors V2 zu msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="a332c-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="a332c-136">Möglicherweise treten auf dem Computer die folgenden anfänglichen Synchronisierungsfehler auf **Anbieter V2** zu **msdyn_vendors** Zuordnung, wenn die Entitäten vorhandene Datensätze mit Werten in der **PrimaryContactPersonId** und **InvoiceVendorAccountNumber** Felder haben.</span><span class="sxs-lookup"><span data-stu-id="a332c-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="a332c-137">Das ist so, weil **InvoiceVendorAccountNumber** ein selbstreferenzierendes Feld ist und **PrimaryContactPersonId** eine Zirkelreferenz in der Lieferantenzuordnung ist.</span><span class="sxs-lookup"><span data-stu-id="a332c-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="a332c-138">*Die Anleitung für das Feld konnte nicht aufgelöst werden: <field>. Die Suche wurde nicht gefunden: <value>. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>? $ select =<field>& $ filter=<field> Gl <value>*</span><span class="sxs-lookup"><span data-stu-id="a332c-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="a332c-139">Hier einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="a332c-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="a332c-140">*Die GUID für das Feld konnte nicht aufgelöst werden: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Die Suche wurde nicht gefunden: 000056. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$ select = msdyn_contactpersonid.contactid & $ filter = msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="a332c-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="a332c-141">*Die GUID für das Feld konnte nicht aufgelöst werden: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Die Suche wurde nicht gefunden: 1. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="a332c-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="a332c-142">Wenn Sie Datensätze mit Werten in diesen Feldern in der Lieferantenentität haben, führen Sie die Schritte im folgenden Abschnitt aus, um die erste Synchronisierung erfolgreich abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a332c-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="a332c-143">In dem Finance and Operations App löschen Sie die **PrimaryContactPersonId** und **InvoiceVendorAccountNumber** Felder aus der Zuordnung und speichern Sie die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="a332c-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="a332c-144">Navigieren Sie zur Zuordnungsseite duales Schreiben für **Anbieter V2 (msdyn_vendors)** und wählen Sie die Registerkarte **Entitätszuordnungen**. Wählen Sie im linken Filter **Finance and Operations Apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="a332c-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="a332c-145">Wählen Sie im rechten Filter **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="a332c-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="a332c-146">Suchen Sie nach **Hauptkontaktperson**, um das Quellfeld zu finden **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="a332c-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="a332c-147">Klicken Sie auf die Schaltfläche **Aktionen** und wählen Sie **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="a332c-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![Selbst- oder Zirkelverweis 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="a332c-149">Wiederholen Sie diesen Vorgang, um das Feld **InvoiceVendorAccountNumber** zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a332c-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![Selbst- oder Zirkelverweis 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="a332c-151">Speichern Sie die Zuordnungsänderungen.</span><span class="sxs-lookup"><span data-stu-id="a332c-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="a332c-152">Deaktivieren Sie die Änderungsverfolgung für **Anbieter V2** Entität.</span><span class="sxs-lookup"><span data-stu-id="a332c-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="a332c-153">Navigieren Sie zu **Datenmanagement \> Dateneinheiten**.</span><span class="sxs-lookup"><span data-stu-id="a332c-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="a332c-154">Wählen Sie die Entität **Anbieter V2** aus.</span><span class="sxs-lookup"><span data-stu-id="a332c-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="a332c-155">Klicken Sie auf **Optionen** in der Menüleiste und dann **Nachverfolgung ändern**.</span><span class="sxs-lookup"><span data-stu-id="a332c-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![Selbst- oder Zirkelverweis 5](media/selfref_options.png)
    
    4. <span data-ttu-id="a332c-157">Klicken Sie auf **Änderungsverfolgung deaktivieren**.</span><span class="sxs-lookup"><span data-stu-id="a332c-157">Click **Disable Change Tracking**.</span></span>
    
        ![Selbst- oder Zirkelverweis 6](media/selfref_tracking.png)

3. <span data-ttu-id="a332c-159">Führen Sie die erste Synchronisierung von **Anbieter V2 (msdyn_vendors)** Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="a332c-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="a332c-160">Die anfängliche Synchronisierung sollte ohne Fehler erfolgreich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a332c-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="a332c-161">Führen Sie die erste Synchronisierung für die **CDS-Kontakte V2 (Kontakte)** Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="a332c-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="a332c-162">Sie müssen diese Zuordnung synchronisieren, wenn Sie das primäre Kontaktfeld auf der Entität des Anbieters synchronisieren möchten, da die Kontaktdatensätze auch zunächst synchronisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a332c-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="a332c-163">Fügen Sie die Felder **PrimaryContactPersonId** und **InvoiceVendorAccountNumber** wieder der **Anbieter V2 (msdyn_vendors)** Zuordnung hinzu und speichern Sie die Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="a332c-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="a332c-164">Führen Sie die erste Synchronisierung erneut für die **Anbieter V2 (msdyn_vendors)** Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="a332c-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="a332c-165">Alle Datensätze werden synchronisiert, da die Änderungsverfolgung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a332c-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="a332c-166">Aktivieren Sie die Änderungsverfolgung für **Anbieter V2** Entität.</span><span class="sxs-lookup"><span data-stu-id="a332c-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="a332c-167">Beheben Sie einen Fehler in der Entitätszuordnung von Kunden V3 zu Konten</span><span class="sxs-lookup"><span data-stu-id="a332c-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="a332c-168">Möglicherweise treten auf dem Computer die folgenden anfänglichen Synchronisierungsfehler auf **Anbieter V3** zu **msdyn_vendors** Zuordnung, wenn die Entitäten vorhandene Datensätze mit Werten in den Feldern **ContactPersonId** und **InvoiceAccount** haben.</span><span class="sxs-lookup"><span data-stu-id="a332c-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="a332c-169">Das ist so, weil **InvoiceAccount** ein selbstreferenzierendes Feld ist und **ContactPersonId** eine Zirkelreferenz in der Lieferantenzuordnung ist.</span><span class="sxs-lookup"><span data-stu-id="a332c-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="a332c-170">*Die Anleitung für das Feld konnte nicht aufgelöst werden: <field>. Die Suche wurde nicht gefunden: <value>. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>? $ select =<field>& $ filter=<field> Gl <value>*</span><span class="sxs-lookup"><span data-stu-id="a332c-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="a332c-171">*Die GUID für das Feld konnte nicht aufgelöst werden: primarycontactperson.msdyn_contactpersonid. Die Suche wurde nicht gefunden: 000056. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$ select = msdyn_contactpersonid.contactid & $ filter = msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="a332c-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="a332c-172">*Die GUID für das Feld konnte nicht aufgelöst werden: msdyn_billingacount.accountnumber. Die Suche wurde nicht gefunden: 1206-1. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq 1206-1*</span><span class="sxs-lookup"><span data-stu-id="a332c-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="a332c-173">Wenn Sie Datensätze mit Werten in diesen Feldern in der Kundenenentität haben, führen Sie die Schritte im folgenden Abschnitt aus, um die erste Synchronisierung erfolgreich abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a332c-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="a332c-174">Sie können diesen Ansatz für alle sofort einsatzbereiten Entitäten wie Konten und Kontakte verwenden.</span><span class="sxs-lookup"><span data-stu-id="a332c-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="a332c-175">In der Finance and Operations App löschen Sie Felder **ContactPersonID** und **InvoiceAccount** aus der Zuordnung **Kunden V3 (Konten)** und speichern Sie die Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="a332c-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="a332c-176">Navigieren Sie zur Zuordnungsseite duales Schreiben für **Kunden V3 (msdyn_vendors)** und wählen Sie die Registerkarte **Entitätszuordnungen**. Wählen Sie im linken Filter **Finance and Operations Apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="a332c-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="a332c-177">Wählen Sie im rechten Filter **Common Data Service Konto**.</span><span class="sxs-lookup"><span data-stu-id="a332c-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="a332c-178">Suchen Sie nach **contactperson**, um das Quellfeld **ContactPersonID** zu finden.</span><span class="sxs-lookup"><span data-stu-id="a332c-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="a332c-179">Klicken Sie auf die Schaltfläche **Aktionen** und wählen Sie **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="a332c-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![Selbst- oder Zirkelverweis 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="a332c-181">Wiederholen Sie diesen Vorgang, um das Feld **InvoiceAccount** zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a332c-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![Selbst- oder Zirkelverweis](media/cust_selfref4.png)
    
    5. <span data-ttu-id="a332c-183">Speichern Sie die Zuordnungsänderungen.</span><span class="sxs-lookup"><span data-stu-id="a332c-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="a332c-184">Deaktivieren Sie die Änderungsverfolgung für **Customers V3** Entität.</span><span class="sxs-lookup"><span data-stu-id="a332c-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="a332c-185">Navigieren Sie zu **Datenmanagement \> Dateneinheiten**.</span><span class="sxs-lookup"><span data-stu-id="a332c-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="a332c-186">Wählen Sie die Entität **Customers V3** aus.</span><span class="sxs-lookup"><span data-stu-id="a332c-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="a332c-187">Klicken Sie auf **Optionen** in der Menüleiste und dann **Nachverfolgung ändern**.</span><span class="sxs-lookup"><span data-stu-id="a332c-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![Selbst- oder Zirkelverweis 5](media/selfref_options.png)
    
    4. <span data-ttu-id="a332c-189">Klicken Sie auf **Änderungsverfolgung deaktivieren**.</span><span class="sxs-lookup"><span data-stu-id="a332c-189">Click **Disable Change Tracking**.</span></span>
    
        ![Selbst- oder Zirkelverweis 6](media/selfref_tracking.png)

3. <span data-ttu-id="a332c-191">Führen Sie die erste Synchronisierung für die **Customers V3 (Konten)** Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="a332c-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="a332c-192">Die anfängliche Synchronisierung sollte ohne Fehler erfolgreich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a332c-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="a332c-193">Führen Sie die erste Synchronisierung für die **CDS-Kontakte V2 (Kontakte)** Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="a332c-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="a332c-194">Es gibt 2 Karten mit dem gleichen Namen.</span><span class="sxs-lookup"><span data-stu-id="a332c-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="a332c-195">Wählen Sie jene mit der Beschreibung **Vorlage Duales Schreiben für die Synchronisierung zwischen FO.CDS-Kontakten V2 und CDS.Contacts. Benötigt neues Paket \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="a332c-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="a332c-196">Auf der Registerkarte **Einzelheiten** auf der Karte.</span><span class="sxs-lookup"><span data-stu-id="a332c-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="a332c-197">In der  App fügen Sie die Felder **InvoiceAccount** und **ContactPersonID** wieder der **Kunden V3 (Konten)** Zuordnung hinzu und speichern Sie die Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="a332c-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="a332c-198">Nun sind das Feld **Rechnungskonto** und das Feld **ContactPersonID** wieder Teil des Live-Synchronisationsmodus.</span><span class="sxs-lookup"><span data-stu-id="a332c-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="a332c-199">Im nächsten Schritt schließen Sie die anfängliche Synchronisierung für diese Felder ab.</span><span class="sxs-lookup"><span data-stu-id="a332c-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="a332c-200">Führen Sie die erste Synchronisierung nochmals für die **Customers V3 (Konten)** Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="a332c-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="a332c-201">Da die Änderungsverfolgung deaktiviert ist, werden beim Ausführen der Synchronisierung die Daten für **InvoiceAccount** und **ContactPersonId** von der Finance and Operations App zu Common Data Service synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="a332c-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="a332c-202">Um die Daten für **Rechnungskonto** und **ContactPersonId** von Common Data Service zu Finance and Operations zu synchronisieren, verwenden Sie ein Datenintegrationsprojekt.</span><span class="sxs-lookup"><span data-stu-id="a332c-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="a332c-203">Im Power Apps erstellen Sie ein Datenintegrationsprojekt zwischen dem **Verkaufskonto** und **Finance and Operations Apps.Customers V3** Entitäten.</span><span class="sxs-lookup"><span data-stu-id="a332c-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="a332c-204">Die Datenrichtung muss von Common Data Service zu Finance and Operations App sein.</span><span class="sxs-lookup"><span data-stu-id="a332c-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="a332c-205">Weil **Rechnungskonto** ein neues Attribut in dualem Schreiben ist, wollen Sie möglicherweise die anfängliche Synchronisierung für dieses Attribut überspringen.</span><span class="sxs-lookup"><span data-stu-id="a332c-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="a332c-206">Weitere Informationen finden Sie unter [Datenintegration in Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="a332c-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="a332c-207">Das folgende Bild zeigt ein Projekt, das **Kundenkonto** und **ContactPersonId** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a332c-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Selbst- oder Zirkelverweis](media/cust_selfref6.png)

    2. <span data-ttu-id="a332c-209">Fügen Sie die Firmenkriterien im Filter auf der Seite Common Data Service ein, da nur die Datensätze, die den Filterkriterien entsprechen, in der Finance and Operations App aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a332c-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="a332c-210">Klicken Sie zum Hinzufügen eines Filters auf das Filtersymbol.</span><span class="sxs-lookup"><span data-stu-id="a332c-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="a332c-211">In dem Dialog **Abfrage bearbeiten** können Sie eine Filterabfrage hinzufügen wie **_msdyn_company_value eq\<guid\>**.</span><span class="sxs-lookup"><span data-stu-id="a332c-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="a332c-212">Wenn das Filtersymbol nicht vorhanden ist, erstellen Sie ein Support-Ticket, um das Datenintegrationsteam zu bitten, die Filterfunktion für Ihren Mandanten zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a332c-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="a332c-213">Wenn Sie keine Filterabfrage für eingeben **_msdyn_company_value**, dann werden alle Datensätze synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="a332c-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![Selbst- oder Zirkelverweis](media/cust_selfref7.png)

        <span data-ttu-id="a332c-215">Damit ist die anfängliche Synchronisierung der Datensätze abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a332c-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="a332c-216">Aktivieren Sie die Änderungsverfolgung für **Customers V3** Entität in der Finance and Operations App.</span><span class="sxs-lookup"><span data-stu-id="a332c-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

