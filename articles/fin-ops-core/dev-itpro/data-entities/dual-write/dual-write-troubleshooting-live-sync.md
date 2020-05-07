---
title: Live-Synchronisierungsprobleme behandeln
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der Live-Synchronisierung zusammenhängen.
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
ms.openlocfilehash: d45b19c1e88e6a27bde4335d4a356f2173bdfcd3
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275416"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="b89bb-103">Live-Synchronisierungsprobleme behandeln</span><span class="sxs-lookup"><span data-stu-id="b89bb-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="b89bb-104">Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b89bb-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="b89bb-105">Dieses Thema enthält speziell Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der Live-Synchronisierung zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="b89bb-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b89bb-106">Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators.</span><span class="sxs-lookup"><span data-stu-id="b89bb-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="b89bb-107">Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b89bb-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="b89bb-108">Bei der Live-Synchronisierung wird ein 403 Forbidden-Fehler ausgegeben, wenn Sie einen Datensatz in einer Finance and Operations App erstelllen</span><span class="sxs-lookup"><span data-stu-id="b89bb-108">Live synchronization throws a 403 Forbidden error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="b89bb-109">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie einen Datensatz in einer Finance and Operations App erstellen:</span><span class="sxs-lookup"><span data-stu-id="b89bb-109">You might receive the following error message when you create a record in a Finance and Operations app:</span></span>

<span data-ttu-id="b89bb-110">*\[{\\„Fehler\\“:{\\„Code\\“:\\„0x80072560\\“,\\„Botschaft\\“:\\„Der Benutzer ist kein Mitglied der Organisation.\\“}}\], Der Remote-Server hat einen Fehler zurückgegeben: (403) Verboten. „}}“.*</span><span class="sxs-lookup"><span data-stu-id="b89bb-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="b89bb-111">Befolgen Sie die Schritte, um das Problem zu beheben unter [Systemanforderungen und -voraussetzungen](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="b89bb-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="b89bb-112">Um diese Schritte auszuführen, müssen die Benutzer der Dual-Write-Anwendung, die in Common Data Service erstellt wurde, die Systemadministratorrolle haben.</span><span class="sxs-lookup"><span data-stu-id="b89bb-112">To complete those steps, the dual-write application users who are created in Common Data Service must have the system admin role.</span></span> <span data-ttu-id="b89bb-113">Das Standard-Besitzerteam muss auch die Systemadministratorrolle haben.</span><span class="sxs-lookup"><span data-stu-id="b89bb-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="b89bb-114">Bei der Live-Synchronisierung für eine Entität wird immer der gleiche Fehler ausgegeben, wenn Sie einen Datensatz in einer Finance and Operations App erstelllen</span><span class="sxs-lookup"><span data-stu-id="b89bb-114">Live synchronization for any entity consistently throws a similar error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="b89bb-115">**Erforderliche Rolle zum Beheben der Fehler:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="b89bb-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="b89bb-116">Möglicherweise erhalten Sie jedes Mal eine Fehlermeldung wie die folgende, wenn Sie versuchen, Entitätsdaten in einer Finance and Operations App zu speichern:</span><span class="sxs-lookup"><span data-stu-id="b89bb-116">You might receive an error message like the following every time that you try to save entity data in a Finance and Operations app:</span></span>

<span data-ttu-id="b89bb-117">*Die Änderungen können nicht in der Datenbank gespeichert werden. Arbeitseinheit kann keine Transaktion festschreiben. Daten können nicht in Entitäts-Uoms geschrieben werden. Das Schreiben in UnitOfMeasureEntity ist mit der Fehlermeldung fehlgeschlagen. Synchronisierung mit Entitäts-Uoms nicht möglich.*</span><span class="sxs-lookup"><span data-stu-id="b89bb-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="b89bb-118">Um das Problem zu beheben, müssen Sie sicherstellen, dass die erforderlichen Referenzdaten in beiden Finance and Operations App und Common Data Service vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b89bb-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Common Data Service.</span></span> <span data-ttu-id="b89bb-119">Zum Beispiel, wenn der Kunde, wenn Sie sich in der Finance and Operations App befinden, zu einer bestimmten Kundengruppe gehört, stellen Sie sicher, dass die Kundengruppe in Common Data Service vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b89bb-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Common Data Service.</span></span>

<span data-ttu-id="b89bb-120">Wenn auf beiden Seiten Daten vorhanden sind und Sie bestätigt haben, dass das Problem nicht datenbezogen ist, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="b89bb-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="b89bb-121">Stoppen Sie die zugehörige Entität.</span><span class="sxs-lookup"><span data-stu-id="b89bb-121">Stop the related entity.</span></span>
2. <span data-ttu-id="b89bb-122">Melden Sie sich bei Finance and Operations an. Stellen Sie sicher, dass Datensätze für die fehlerhafte Entität in den Tabellen DualWriteProjectConfiguration und DualWriteProjectFieldConfiguration vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b89bb-122">Sign in to the Finance and Operations app, and make sure that records for the failing entity exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="b89bb-123">Beispielsweise sieht die Abfrage so aus, wenn die **Kundenentität** fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="b89bb-123">For example, here is what the query looks like if the **Customers** entity is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="b89bb-124">Wenn es Datensätze für die fehlerhafte Entität gibt, auch nachdem Sie die Entitätszuordnung gestoppt haben, löschen Sie die Datensätze, die sich auf die fehlerhafte Entität beziehen.</span><span class="sxs-lookup"><span data-stu-id="b89bb-124">If there are records for the failing entity even after you stop the entity mapping, delete the records that are related to the failing entity.</span></span> <span data-ttu-id="b89bb-125">Notieren Sie sich die Spalte **Projektname** in der DualWriteProjectConfiguration-Tabelle und rufen Sie den Datensatz in der DualWriteProjectFieldConfiguration-Tabelle ab, indem Sie den Datensatz mithilfe des Projektnamens löschen.</span><span class="sxs-lookup"><span data-stu-id="b89bb-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the record in the DualWriteProjectFieldConfiguration table by using the project name to delete the record.</span></span>
4. <span data-ttu-id="b89bb-126">Starten Sie die Entitätszuordnung.</span><span class="sxs-lookup"><span data-stu-id="b89bb-126">Start the entity mapping.</span></span> <span data-ttu-id="b89bb-127">Überprüfen Sie, ob die Daten ohne Probleme synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b89bb-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="b89bb-128">Behandeln Sie Lese- oder Schreibberechtigungsfehler, wenn Sie Daten in einer Finance and Operations App erstellen</span><span class="sxs-lookup"><span data-stu-id="b89bb-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="b89bb-129">Möglicherweise wird eine Fehlermeldung Bad Request angezeigt, die dem folgenden Beispiel ähnelt, wenn Sie Daten in einer Finance and Operations App erstellen.</span><span class="sxs-lookup"><span data-stu-id="b89bb-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Beispiel für die Fehlermeldung Bad Request](media/error_record_id_source.png)

<span data-ttu-id="b89bb-131">Um das Problem zu beheben, müssen Sie dem Team der zugeordneten Geschäftseinheit Dynamics 365 Sales oder Dynamics 365 Customer Service die richtige Sicherheitsrolle zuweisen, um die fehlenden Berechtigungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b89bb-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="b89bb-132">In der Finance and Operations App finden Sie den Geschäftsbereich, der im Verbindungssatz Datenintegration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b89bb-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organisationszuordnung](media/mapped_business_unit.png)

2. <span data-ttu-id="b89bb-134">Melden Sie sich in der modellgesteuerten App in Dynamics 365 bei der Umgebung an und navigieren Sie zu **Einstellungen \> Sicherheit**und finden Sie das Team der zugeordneten Geschäftseinheit.</span><span class="sxs-lookup"><span data-stu-id="b89bb-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![Team des zugeordneten Geschäftsbereichs](media/setting_security_page.png)

3. <span data-ttu-id="b89bb-136">Öffnen Sie die Seite für das Team zur Bearbeitung und wählen Sie dann **Rollen verwalten**, um das Dialogfeld **Teamrollen verwalten** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b89bb-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Schaltfläche Rollen verwalten](media/manage_team_roles.png)

4. <span data-ttu-id="b89bb-138">Weisen Sie die Rolle zu, die über die Lese-/Schreibberechtigung für die relevanten Entitäten verfügt, und wählen Sie dann aus **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b89bb-138">Assign the role that has the read/write privilege for the relevant entities, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a><span data-ttu-id="b89bb-139">Beheben Sie Synchronisierungsprobleme in einer Umgebung, die eine kürzlich geändert Common Data Service Umgebung hat</span><span class="sxs-lookup"><span data-stu-id="b89bb-139">Fix synchronization issues in an environment that has a recently changed Common Data Service environment</span></span>

<span data-ttu-id="b89bb-140">**Erforderliche Rolle zum Beheben der Fehler:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="b89bb-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="b89bb-141">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie Daten in einer Finance and Operations App erstellen:</span><span class="sxs-lookup"><span data-stu-id="b89bb-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="b89bb-142">*{„entityName“:„CustCustomerV3Entity“,„executeStatus“:2,„fieldResponses“:\[\],„recordResponses“:\[{„Fehlermeldung“:„**Nutzdaten für die Entität CustCustomerV3Entity können nicht generiert werden**“,„logDateTime“:„2019-08-27T18:51:52.5843124Z“,„verboseError“:„Die Erstellung der Nutzdaten ist mit dem Fehler fehlgeschlagen. Ungültiger URI: URI ist leer.“}\],„isErrorCountUpdated“: true}*</span><span class="sxs-lookup"><span data-stu-id="b89bb-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="b89bb-143">So sieht der Fehler in der modellgesteuerten App in Dynamics 365 aus:</span><span class="sxs-lookup"><span data-stu-id="b89bb-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="b89bb-144">*Ein unerwarteter Fehler ist im ISV-Code aufgetreten. (ErrorType = ClientError) Unerwartete Ausnahme vom Plug-In (Ausführen): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: Entitätskonto konnte nicht verarbeitet werden – (Ein Verbindungsversuch ist fehlgeschlagen, da die verbundene Partei nach a nicht ordnungsgemäß geantwortet hat Zeitraum oder Verbindungsaufbau fehlgeschlagen hat, da der verbundene Host nicht reagiert hat*</span><span class="sxs-lookup"><span data-stu-id="b89bb-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="b89bb-145">Dieser Fehler tritt auf, wenn die Common Data Service Umgebung fälschlicherweise zurückgesetzt wird, während Sie versuchen, Daten in der Finance and Operations App zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b89bb-145">This error occurs when the Common Data Service environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="b89bb-146">Führen Sie folgende Schritte aus, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="b89bb-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="b89bb-147">Melden Sie sich bei der Finance and Operations virtuellen Maschine (VM) an, öffnen Sie SQL Server Management Studio (SSMS) und suchen Sie in der Tabelle DUALWRITEPROJECTCONFIGURATIONENTITY nach Datensätzen **Internalitätsname** gleich **Kunden V3** und **externalentityname** gleich **Konten**.</span><span class="sxs-lookup"><span data-stu-id="b89bb-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for records in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="b89bb-148">So sieht die Abfrage aus.</span><span class="sxs-lookup"><span data-stu-id="b89bb-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="b89bb-149">Verwenden Sie den Projektnamen aus den Ergebnissen der vorherigen Abfrage, um die folgende Abfrage auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b89bb-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="b89bb-150">Stellen Sie sicher, dass die **externalenvironmentURL** Spalte die richtige Common Data Service oder App-URL hat.</span><span class="sxs-lookup"><span data-stu-id="b89bb-150">Make sure that the **externalenvironmentURL** column has the correct Common Data Service or app URL.</span></span> <span data-ttu-id="b89bb-151">Löschen Sie doppelte Datensätze, die auf die falsche Common Data Service URL verweisen.</span><span class="sxs-lookup"><span data-stu-id="b89bb-151">Delete any duplicate records that point to the wrong Common Data Service URL.</span></span> <span data-ttu-id="b89bb-152">Löschen Sie die entsprechenden Datensätze in den Tabellen DUALWRITEPROJECTFIELDCONFIGURATION und DUALWRITEPROJECTCONFIGURATION.</span><span class="sxs-lookup"><span data-stu-id="b89bb-152">Delete the corresponding records in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="b89bb-153">Stoppen Sie die Entitätszuordnung und starten Sie sie neu</span><span class="sxs-lookup"><span data-stu-id="b89bb-153">Stop the entity mapping, and then restart it</span></span>
