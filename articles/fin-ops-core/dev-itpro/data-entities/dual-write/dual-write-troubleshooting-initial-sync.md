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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172713"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="c41db-103">Probleme bei der anfänglichen Synchronisierung behandeln</span><span class="sxs-lookup"><span data-stu-id="c41db-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="c41db-104">Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c41db-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="c41db-105">Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Synchronisierung zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="c41db-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="c41db-106">Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators.</span><span class="sxs-lookup"><span data-stu-id="c41db-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="c41db-107">Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c41db-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="c41db-108">Überprüfen Sie eine Finance and Operations App auf anfängliche Synchronisationsfehler</span><span class="sxs-lookup"><span data-stu-id="c41db-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="c41db-109">Nachdem Sie die Zuordnungsvorlagen aktiviert haben, sollte der Status der Zuordnungen lauten **Laufen**.</span><span class="sxs-lookup"><span data-stu-id="c41db-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="c41db-110">Wenn der Status ist **Nicht ausgeführt** angezeigt wird, sind bei der ersten Synchronisierung Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c41db-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="c41db-111">Um die Fehler anzuzeigen, wählen Sie die **Anfängliche Synchronisierungsdetail** Registerkarte auf der **Duales Schreiben** Seite.</span><span class="sxs-lookup"><span data-stu-id="c41db-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Registerkarte Details zur Erstsynchronisierung](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="c41db-113">Sie können die anfängliche Synchronisierung nicht abschließen: 400 Bad Request</span><span class="sxs-lookup"><span data-stu-id="c41db-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="c41db-114">**Erforderliche Rolle zum Beheben der Fehler:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="c41db-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="c41db-115">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, das Mapping und die anfängliche Synchronisierung auszuführen:</span><span class="sxs-lookup"><span data-stu-id="c41db-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="c41db-116">*Der Remote-Server hat einen Fehler zurückgegeben: (400) Bad Request.), beim AX Export ist ein Fehler aufgetreten*</span><span class="sxs-lookup"><span data-stu-id="c41db-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="c41db-117">Hier ist ein Beispiel für die vollständige Fehlernachricht.</span><span class="sxs-lookup"><span data-stu-id="c41db-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="c41db-118">Wenn dieser Fehler konsistent auftritt und Sie die anfängliche Synchronisierung nicht abschließen können, führen Sie die folgenden Schritte aus, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="c41db-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="c41db-119">Melden Sie sich bei der virtuellen Maschine (VM) für die Finance and Operations App an.</span><span class="sxs-lookup"><span data-stu-id="c41db-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="c41db-120">Öffnen Sie die Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="c41db-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="c41db-121">In dem Bereich **Dienstleistungen** stellen Sie sicher, dass der Microsoft Dynamics 365 Data Import Export Framework-Dienst wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c41db-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="c41db-122">Starten Sie ihn neu, wenn er gestoppt wurde, da die anfängliche Synchronisierung dies erfordert.</span><span class="sxs-lookup"><span data-stu-id="c41db-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="c41db-123">Anfänglicher Synchronisationsfehler: 403 Forbidden</span><span class="sxs-lookup"><span data-stu-id="c41db-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="c41db-124">Während der ersten Synchronisierung wird möglicherweise die folgende Fehlermeldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="c41db-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="c41db-125">*(\[Forbidden\], der Remote-Server hat einen Fehler zurückgegeben: (403) Forbidden.), AX beim Export ist ein Fehler aufgetreten*</span><span class="sxs-lookup"><span data-stu-id="c41db-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="c41db-126">Führen Sie folgende Schritte aus, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="c41db-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="c41db-127">Bei der Finance and Operations App anmelden.</span><span class="sxs-lookup"><span data-stu-id="c41db-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="c41db-128">Auf der **Azure Active Directory Anwendungen** Seite löschen Sie den **DtAppID** Client, und fügen Sie ihn dann erneut hinzu.</span><span class="sxs-lookup"><span data-stu-id="c41db-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Liste der Azure AD Bewerbungen](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="c41db-130">Selbstreferenzfehler während der ersten Synchronisation</span><span class="sxs-lookup"><span data-stu-id="c41db-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="c41db-131">Möglicherweise wird eine Fehlermeldung angezeigt, die dem folgenden Beispiel ähnelt, wenn eine Ihrer Zuordnungen Selbstreferenzen enthält:</span><span class="sxs-lookup"><span data-stu-id="c41db-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="c41db-132">*Auf dem Vendors V2 tritt der folgende Fehler auf: Datensatz-ID: Neuer Datensatz, ErrorMessage: Die GUID für das Feld konnte nicht aufgelöst werden: msdyn\_rechnungvendoraccountnumber.msdyn\_vendoraccountnumber. Der Suchwert wurde nicht gefunden: CN-001. Versuchen Sie diese URLs, um zu überprüfen, ob die Referenzdaten vorhanden sind: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` Gleichung 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="c41db-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="c41db-133">Diese Art von Fehler tritt während der anfänglichen Synchronisation von Zuordnungen mit Selbstreferenzen auf.</span><span class="sxs-lookup"><span data-stu-id="c41db-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="c41db-134">Im vorherigen Beispiel verweist das Feld Rechnungskonto auf die Lieferantenentität.</span><span class="sxs-lookup"><span data-stu-id="c41db-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="c41db-135">Um das Problem zu beheben, müssen Sie die Zuordnung möglicherweise zweimal ausführen, bevor die anfängliche Synchronisierung erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c41db-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>

