---
title: Probleme bei der anfänglichen Synchronisierung behandeln
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Synchronisierung zusammenhängen.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: c716707140c85b06ad2f084c10c4b2d0ecfea82e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754013"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="fe4a2-103">Probleme bei der anfänglichen Synchronisierung behandeln</span><span class="sxs-lookup"><span data-stu-id="fe4a2-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="fe4a2-104">Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="fe4a2-105">Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Synchronisierung zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe4a2-106">Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="fe4a2-107">Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="fe4a2-108">Überprüfen Sie eine Finance and Operations App auf anfängliche Synchronisationsfehler</span><span class="sxs-lookup"><span data-stu-id="fe4a2-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="fe4a2-109">Nachdem Sie die Zuordnungsvorlagen aktiviert haben, sollte der Status der Zuordnungen lauten **Laufen**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="fe4a2-110">Wenn der Status ist **Nicht ausgeführt** angezeigt wird, sind bei der ersten Synchronisierung Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="fe4a2-111">Um die Fehler anzuzeigen, wählen Sie die **Anfängliche Synchronisierungsdetail** Registerkarte auf der **Duales Schreiben** Seite.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Fehler auf der Registerkarte Details zur Erstsynchronisierung](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="fe4a2-113">Sie können die anfängliche Synchronisierung nicht abschließen: 400 Bad Request</span><span class="sxs-lookup"><span data-stu-id="fe4a2-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="fe4a2-114">**Erforderliche Rolle zum Beheben der Fehler:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="fe4a2-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="fe4a2-115">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, das Mapping und die anfängliche Synchronisierung auszuführen:</span><span class="sxs-lookup"><span data-stu-id="fe4a2-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="fe4a2-116">*(\[Unzulässige Anforderung\], der Remote-Server hat einen Fehler zurückgegeben: (400) Unzulässige Anforderung), AX beim Export ist ein Fehler aufgetreten*</span><span class="sxs-lookup"><span data-stu-id="fe4a2-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="fe4a2-117">Hier ist ein Beispiel für die vollständige Fehlernachricht.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="fe4a2-118">Wenn dieser Fehler konsistent auftritt und Sie die anfängliche Synchronisierung nicht abschließen können, führen Sie die folgenden Schritte aus, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="fe4a2-119">Melden Sie sich bei der virtuellen Maschine (VM) für die Finance and Operations App an.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="fe4a2-120">Öffnen Sie die Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="fe4a2-121">In dem Bereich **Dienstleistungen** stellen Sie sicher, dass der Microsoft Dynamics 365 Data Import Export Framework-Dienst wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="fe4a2-122">Starten Sie ihn neu, wenn er gestoppt wurde, da die anfängliche Synchronisierung dies erfordert.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="fe4a2-123">Anfänglicher Synchronisationsfehler: 403 Forbidden</span><span class="sxs-lookup"><span data-stu-id="fe4a2-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="fe4a2-124">Während der ersten Synchronisierung wird möglicherweise die folgende Fehlermeldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="fe4a2-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="fe4a2-125">*(\[Forbidden\], der Remote-Server hat einen Fehler zurückgegeben: (403) Forbidden.), AX beim Export ist ein Fehler aufgetreten*</span><span class="sxs-lookup"><span data-stu-id="fe4a2-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="fe4a2-126">Führen Sie folgende Schritte aus, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="fe4a2-127">Bei der Finance and Operations App anmelden.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="fe4a2-128">Auf der **Azure Active Directory Anwendungen** Seite löschen Sie den **DtAppID** Client, und fügen Sie ihn dann erneut hinzu.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID-Client in der Liste von Azure AD Anwendungen](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="fe4a2-130">Selbstreferenzfehler oder Zirkelreferenzfehler während der ersten Synchronisation</span><span class="sxs-lookup"><span data-stu-id="fe4a2-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="fe4a2-131">Möglicherweise wird eine Fehlernachricht angezeigt, die dem folgenden Beispiel ähnelt, wenn eine Ihrer Zuordnungen Selbstreferenzen oder Zirkelreferenzen enthält:</span><span class="sxs-lookup"><span data-stu-id="fe4a2-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="fe4a2-132">Die Fehler fallen in folgende Kategorien:</span><span class="sxs-lookup"><span data-stu-id="fe4a2-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="fe4a2-133">Fehler in der Tabellenzuordnung Lieferanten V2 zu msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="fe4a2-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="fe4a2-134">Fehler in der Tabellenzuordnung Kunden V3 zu Konten</span><span class="sxs-lookup"><span data-stu-id="fe4a2-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="fe4a2-135">Fehler in der Tabellenzuordnung von Lieferanten V2 zu msdyn_vendors beheben</span><span class="sxs-lookup"><span data-stu-id="fe4a2-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="fe4a2-136">Möglicherweise treten auf dem Computer die folgenden anfänglichen Synchronisierungsfehler für die Zuordnung **Kreditoren V2** zu **msdyn\_vendors** auf, wenn die Tabellen vorhandene Zeilen mit Werten in den Spalten **PrimaryContactPersonId** und **InvoiceVendorAccountNumber** haben.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns.</span></span> <span data-ttu-id="fe4a2-137">Diese Fehler passieren, weil **InvoiceVendorAccountNumber** eine selbstreferenzierende Spalte ist und **PrimaryContactPersonId** eine Zirkelreferenz in der Kreditorenzuordnung ist.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing column, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="fe4a2-138">Die Fehlermeldungen, die Sie erhalten, haben das folgende Formular.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="fe4a2-139">*Die Anleitung für das Feld konnte nicht aufgelöst werden: \<field\>. Die Suche wurde nicht gefunden: \<value\>. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="fe4a2-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="fe4a2-140">Im Folgenden finden Sie einige Beispiele hierfür:</span><span class="sxs-lookup"><span data-stu-id="fe4a2-140">Here are some examples:</span></span>

- <span data-ttu-id="fe4a2-141">*Die Anleitung für das Feld konnte nicht aufgelöst werden: msdy\_vendorprimarycontactperson.msdyn\_contactpersonid. Die Suche wurde nicht gefunden: 000056. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="fe4a2-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="fe4a2-142">*Die Anleitung für das Feld konnte nicht aufgelöst werden: msdyn\_.invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Die Suche wurde nicht gefunden: V24-1. Testen Sie diese URL(s), um zu prüfen, ob die Referenzdaten vorhanden sind: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="fe4a2-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="fe4a2-143">Wenn Sie Zeilen mit Werten in der Kreditorentabelle in den Spalten **PrimaryContactPersonID** und **InvoiceVendorAccountNumber** haben, führen Sie die Schritte im folgenden Abschnitt aus, um die erste Synchronisierung erfolgreich abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-143">If any rows in the vendor table have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="fe4a2-144">In der Finance and Operations-App löschen Sie die Spalten **PrimaryContactPersonId** und **InvoiceVendorAccountNumber** aus der Zuordnung, und speichern Sie die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="fe4a2-145">Wählen Sie auf der Zuordnungsseite für duales Schreiben für **Lieferant V2 (msdyn\_vendors)** auf der Registerkarte **Tabellenzuordnungen** im linken Filter **Finance and Operations apps.Vendors V2** aus.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="fe4a2-146">Wählen Sie im rechten Filter **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="fe4a2-147">Suchen Sie nach **primarycontactperson**, um das Quellfeld **PrimaryContactPersonId** zu finden.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source column.</span></span>
    3. <span data-ttu-id="fe4a2-148">Wählen Sie **Aktionen** und dann **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-148">Select **Actions**, and then select **Delete**.</span></span>

        ![Löschen der Spalte „PrimaryContactPersonId“](media/vend_selfref3.png)

    4. <span data-ttu-id="fe4a2-150">Wiederholen Sie diese Schritte, um die Spalte **InvoiceVendorAccountNumber** zu löschen.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** column.</span></span>

        ![Löschen des Feldes „InvoiceVendorAccountNumber“](media/vend-selfref4.png)

    5. <span data-ttu-id="fe4a2-152">Speichern Sie Ihre Änderungen am Mapping.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="fe4a2-153">Deaktivieren Sie die Änderungsverfolgung für die Tabelle **Kreditoren V2**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-153">Turn off change tracking for the **Vendors V2** table.</span></span>

    1. <span data-ttu-id="fe4a2-154">Im Arbeitsbereich **Datenmanagement** wählen Sie die Kachel **Datentabellen** aus.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="fe4a2-155">Wählen Sie die Tabelle **Kreditoren V2** aus.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-155">Select the **Vendors V2** table.</span></span>
    3. <span data-ttu-id="fe4a2-156">Wählen Sie im Aktionsbereich **Optionen** und wählen Sie dann **Änderungsnachverfolgung**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Auswahl der Option Änderungsnachverfolgung ändern](media/selfref_options.png)

    4. <span data-ttu-id="fe4a2-158">Wählen Sie **Änderungsverfolgung deaktivieren**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-158">Select **Disable Change Tracking**.</span></span>

        ![Wählen Sie Änderungsverfolgung deaktivieren](media/selfref_tracking.png)

3. <span data-ttu-id="fe4a2-160">Führen Sie die erste Synchronisierung erneut für die **Anbieter V2** (msdyn\_vendors) Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="fe4a2-161">Die erstmalige Synchronisierung sollte ohne Fehler erfolgreich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="fe4a2-162">Führen Sie die erste Synchronisierung für **CDS-Kontakte V2 (Kontakte)** Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="fe4a2-163">Sie müssen diese Zuordnung synchronisieren, wenn Sie die Spalte des primären Kontakts in der Tabelle der Kreditoren synchronisieren möchten, da die Kontaktzeilen zunächst synchronisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-163">You must sync this mapping if you want to sync the primary contact column on the vendors table, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="fe4a2-164">Fügen Sie die Spalten **PrimaryContactPersonId** und **InvoiceVendorAccountNumber** wieder der **Kreditor V2 (msdyn\_vendors)** Zuordnung hinzu, und speichern Sie die Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="fe4a2-165">Führen Sie die erste Synchronisierung noch einmal für die **Anbieter V2** (msdyn\_vendors) Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="fe4a2-166">Weil die Änderungsnachverfolgung deaktiviert ist, werden alle Zeilen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="fe4a2-167">Aktivieren Sie die Änderungsnachverfolgung für die Tabelle **Kreditor V2**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-167">Turn change tracking back on for the **Vendors V2** table.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="fe4a2-168">Beheben von Fehlern in der Tabellenzuordnung von Kunden V3 zu Konten</span><span class="sxs-lookup"><span data-stu-id="fe4a2-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="fe4a2-169">Möglicherweise treten auf dem Computer die folgenden anfänglichen Synchronisierungsfehler von **Debitoren V3** zu **Konten** auf, wenn die Tabellen vorhandene Zeilen mit Werten in den Spalten **ContactPersonID** und **InvoiceAccount** haben.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** columns.</span></span> <span data-ttu-id="fe4a2-170">Diese Fehler passieren, weil **InvoiceAccount** eine selbstreferenzierende Spalte ist und **ContactPersonId** eine Zirkelreferenz in der Kreditorenzuordnung ist.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-170">These errors occur because **InvoiceAccount** is a self-referencing column, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="fe4a2-171">Die Fehlermeldungen, die Sie erhalten, haben das folgende Formular.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="fe4a2-172">*Die Anleitung für das Feld konnte nicht aufgelöst werden: \<field\>. Die Suche wurde nicht gefunden: \<value\>. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="fe4a2-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="fe4a2-173">Im Folgenden finden Sie einige Beispiele hierfür:</span><span class="sxs-lookup"><span data-stu-id="fe4a2-173">Here are some examples:</span></span>

- <span data-ttu-id="fe4a2-174">*Die Anleitung für das Feld konnte nicht aufgelöst werden: primarycontactid.msdyn\_contactpersonid. Die Suche wurde nicht gefunden: 000056. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="fe4a2-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="fe4a2-175">*Die Anleitung für das Feld konnte nicht aufgelöst werden: msdyn\_billingaccount.accountnumber. Die Suche wurde nicht gefunden: 1206-1. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="fe4a2-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="fe4a2-176">Wenn Sie Zeilen mit Werten in der Debitorentabelle in den Spalten **ContactPersonID** und **InvoiceAccount** haben, führen Sie die Schritte im folgenden Abschnitt aus, um die erste Synchronisierung erfolgreich abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-176">If any rows in the customer table have values in the **ContactPersonID** and **InvoiceAccount** columns, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="fe4a2-177">Sie können diesen Ansatz für alle sofort einsatzbereiten Tabellen wie **Konten** und **Kontakte** verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="fe4a2-178">In der Finance and Operations-App löschen Sie Spalten **ContactPersonID** und **InvoiceAccount** aus der Zuordnung **Debitoren V3 (Konten)**, und speichern Sie dann die Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** columns from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="fe4a2-179">Wählen Sie auf der Zuordnungsseite für duales Schreiben für **Kunden V3 (Konten)** auf der Registerkarte **Tabellenzuordnungen** im linken Filter **Finance and Operations app.Customers V3** aus.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="fe4a2-180">Wählen Sie im rechten Filter **Dataverse Konto**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="fe4a2-181">Suchen Sie nach **contactperson**, um die Quellspalte **ContactPersonID** zu finden.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-181">Search for **contactperson** to find the **ContactPersonID** source column.</span></span>
    3. <span data-ttu-id="fe4a2-182">Wählen Sie **Aktionen** und dann **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-182">Select **Actions**, and then select **Delete**.</span></span>

        ![Löschen der Spalte „ContactPersonID“](media/cust_selfref3.png)

    4. <span data-ttu-id="fe4a2-184">Wiederholen Sie diese Schritte, um die Spalte **InvoiceAccount** zu löschen.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-184">Repeat these steps to delete the **InvoiceAccount** column.</span></span>

        ![Löschen der Spalte „InvoiceAccount“](media/cust_selfref4.png)

    5. <span data-ttu-id="fe4a2-186">Speichern Sie Ihre Änderungen am Mapping.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="fe4a2-187">Deaktivieren Sie die Änderungsverfolgung für die Tabelle **Debitoren V3**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-187">Turn off change tracking for the **Customers V3** table.</span></span>

    1. <span data-ttu-id="fe4a2-188">Im Arbeitsbereich **Datenmanagement** wählen Sie die Kachel **Datentabellen** aus.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="fe4a2-189">Wählen Sie die Tabelle **Debitoren V3** aus.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-189">Select the **Customers V3** table.</span></span>
    3. <span data-ttu-id="fe4a2-190">Wählen Sie im Aktionsbereich **Optionen** und wählen Sie dann **Änderungsnachverfolgung**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Auswahl der Option Änderungsnachverfolgung ändern](media/selfref_options.png)

    4. <span data-ttu-id="fe4a2-192">Wählen Sie **Änderungsverfolgung deaktivieren**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-192">Select **Disable Change Tracking**.</span></span>

        ![Wählen Sie Änderungsverfolgung deaktivieren](media/selfref_tracking.png)

3. <span data-ttu-id="fe4a2-194">Führen Sie die erste Synchronisierung nochmals für die **Debitoren V3 (Konten)** Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="fe4a2-195">Die erstmalige Synchronisierung sollte ohne Fehler erfolgreich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="fe4a2-196">Führen Sie die erste Synchronisierung für **CDS-Kontakte V2 (Kontakte)** Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fe4a2-197">Es gibt zwei Karten mit demselben Namen.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-197">There are two maps that have the same name.</span></span> <span data-ttu-id="fe4a2-198">Stellen Sie sicher, dass Sie jene Zuordnung mit der folgenden Beschreibung auf der Registerkarte **Details** auswählen: Duales Schreiben für die Synchronisierung zwischen FO.CDS-Kontakten V2 und CDS.Contacts.  Benötigt neues Paket \[**Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="fe4a2-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="fe4a2-199">Fügen Sie die Spalten **InvoiceAccount** und **ContactPersonID** wieder der Zuordnung **Debitoren V3 (Konten)** hinzu, und speichern Sie dann die Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-199">Add the **InvoiceAccount** and **ContactPersonId** columns back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="fe4a2-200">Jetzt sind die Spalte **InvoiceAccount** und die Spalte **ContactPersonID** wieder Teil des Live-Synchronisationsmodus.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-200">Both the **InvoiceAccount** column and the **ContactPersonId** column are now part of live synchronization mode again.</span></span> <span data-ttu-id="fe4a2-201">Im nächsten Schritt machen Sie die anfängliche Synchronisierung für diese Spalten.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-201">In the next step, you will do the initial synchronization for these columns.</span></span>
6. <span data-ttu-id="fe4a2-202">Führen Sie die erste Synchronisierung noch einmal für die **Debitoren V3 (Konten)** Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="fe4a2-203">Da die Änderungsverfolgung deaktiviert ist, werden die Daten für **InvoiceAccount** und **ContactPersonId** von der Finance and Operations App zu Dataverse synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="fe4a2-204">Um die Daten für **Rechnungskonto** und **ContactPersonId** von Dataverse zu Finance and Operations zu synchronisieren, müssen Sie ein Datenintegrationsprojekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="fe4a2-205">Erstellen Sie in Power Apps ein Datenintegrationsprojekt zwischen den Tabellen **Sales.Account** und **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="fe4a2-206">Die Datenrichtung muss von Dataverse zu Finance and Operations App sein.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="fe4a2-207">Weil **Rechnungskonto** ein neues Attribut in dualem Schreiben ist, wollen Sie möglicherweise die anfängliche Synchronisierung dazu überspringen.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="fe4a2-208">Weitere Informationen finden Sie unter [Datenintegration in Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="fe4a2-208">For more information, see [Integrate data into Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="fe4a2-209">Das folgende Illustration zeigt ein Projekt, das **Kundenkonto** und **ContactPersonId** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Datenintegrationsprojekt zum Aktualisieren von CustomerAccount und ContactPersonId](media/cust_selfref6.png)

    2. <span data-ttu-id="fe4a2-211">Fügen Sie die Firmenkriterien im Filter auf der Seite von Dataverse ein, da nur die Zeilen, die den Filterkriterien entsprechen, in der Finance and Operations-App aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="fe4a2-212">Wählen Sie zum Hinzufügen die Schaltfläche Filter.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="fe4a2-213">In dem Dialog **Abfrage bearbeiten** können Sie eine Filterabfrage hinzufügen wie **\_msdyn\__company\_value eq\<guid\>**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="fe4a2-214">[HINWEIS] Wenn die Schaltfläche Filter nicht vorhanden ist, erstellen Sie ein Support-Ticket, um das Datenintegrationsteam zu bitten, die Filterfunktion für Ihren Mandanten zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="fe4a2-215">Wenn Sie keine Filterabfrage für **\_msdyn\_company\_value** eingeben, werden alle Zeilen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![Hinzufügen einer Filterabfrage](media/cust_selfref7.png)

    <span data-ttu-id="fe4a2-217">Die anfängliche Synchronisierung der Zeilen ist nun abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="fe4a2-218">Aktivieren Sie die Änderungsnachverfolgung in Finance and Operations für die Tabelle **Debitoren V3**.</span><span class="sxs-lookup"><span data-stu-id="fe4a2-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** table.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]