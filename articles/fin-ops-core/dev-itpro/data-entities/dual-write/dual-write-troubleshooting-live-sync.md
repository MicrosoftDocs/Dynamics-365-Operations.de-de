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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 59c8bd80b167cdfaa7a65e469f4dc7ebf8f50844
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744612"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="50651-103">Live-Synchronisierungsprobleme behandeln</span><span class="sxs-lookup"><span data-stu-id="50651-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="50651-104">Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse.</span><span class="sxs-lookup"><span data-stu-id="50651-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="50651-105">Dieses Thema enthält speziell Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der Live-Synchronisierung zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="50651-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50651-106">Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators.</span><span class="sxs-lookup"><span data-stu-id="50651-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="50651-107">Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="50651-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="50651-108">Bei der Live-Synchronisierung wird ein 403 Forbidden-Fehler ausgegeben, wenn Sie eine Zeile in einer Finance and Operations-App erstelllen.</span><span class="sxs-lookup"><span data-stu-id="50651-108">Live synchronization throws a 403 Forbidden error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="50651-109">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie eine Zeile in einer Finance and Operations-App erstellen:</span><span class="sxs-lookup"><span data-stu-id="50651-109">You might receive the following error message when you create a row in a Finance and Operations app:</span></span>

<span data-ttu-id="50651-110">*\[{\\„Fehler\\“:{\\„Code\\“:\\„0x80072560\\“,\\„Botschaft\\“:\\„Der Benutzer ist kein Mitglied der Organisation.\\“}}\], Der Remote-Server hat einen Fehler zurückgegeben: (403) Verboten. „}}“.*</span><span class="sxs-lookup"><span data-stu-id="50651-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="50651-111">Befolgen Sie die Schritte, um das Problem zu beheben unter [Systemanforderungen und -voraussetzungen](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="50651-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="50651-112">Um diese Schritte auszuführen, müssen die Benutzer der Dual-Write-Anwendung, die in Dataverse erstellt wurde, die Systemadministratorrolle haben.</span><span class="sxs-lookup"><span data-stu-id="50651-112">To complete those steps, the dual-write application users who are created in Dataverse must have the system admin role.</span></span> <span data-ttu-id="50651-113">Das Standard-Besitzerteam muss auch die Systemadministratorrolle haben.</span><span class="sxs-lookup"><span data-stu-id="50651-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="50651-114">Bei der Live-Synchronisierung für eine Tabelle wird immer der gleiche Fehler ausgegeben, wenn Sie eine Zeile in einer Finance and Operations-App erstellen.</span><span class="sxs-lookup"><span data-stu-id="50651-114">Live synchronization for any table consistently throws a similar error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="50651-115">**Erforderliche Rolle zum Beheben der Fehler:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="50651-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="50651-116">Möglicherweise erhalten Sie jedes Mal eine Fehlermeldung wie die folgende, wenn Sie versuchen, Tabellendaten in einer Finance and Operations-App zu speichern:</span><span class="sxs-lookup"><span data-stu-id="50651-116">You might receive an error message like the following every time that you try to save table data in a Finance and Operations app:</span></span>

<span data-ttu-id="50651-117">*Die Änderungen können nicht in der Datenbank gespeichert werden. Arbeitseinheit kann keine Transaktion festschreiben. Daten können nicht in Entitäts-Uoms geschrieben werden. Das Schreiben in UnitOfMeasureEntity ist mit der Fehlermeldung fehlgeschlagen. Synchronisierung mit Entitäts-Uoms nicht möglich.*</span><span class="sxs-lookup"><span data-stu-id="50651-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="50651-118">Um das Problem zu beheben, müssen Sie sicherstellen, dass die erforderlichen Referenzdaten in beiden Finance and Operations App und Dataverse vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="50651-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Dataverse.</span></span> <span data-ttu-id="50651-119">Zum Beispiel, wenn der Kunde, wenn Sie sich in der Finance and Operations App befinden, zu einer bestimmten Kundengruppe gehört, stellen Sie sicher, dass die Kundengruppe in Dataverse vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="50651-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Dataverse.</span></span>

<span data-ttu-id="50651-120">Wenn auf beiden Seiten Daten vorhanden sind und Sie bestätigt haben, dass das Problem nicht datenbezogen ist, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="50651-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="50651-121">Stoppen Sie die zugehörige Tabelle.</span><span class="sxs-lookup"><span data-stu-id="50651-121">Stop the related table.</span></span>
2. <span data-ttu-id="50651-122">Melden Sie sich bei der Finance and Operations-App an. Stellen Sie sicher, dass Zeilen für die fehlerhafte Tabelle in den Tabellen DualWriteProjectConfiguration und DualWriteProjectFieldConfiguration vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="50651-122">Sign in to the Finance and Operations app, and make sure that rows for the failing table exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="50651-123">Beispielsweise sieht die Abfrage so aus, wenn die Tabelle **Debitoren** fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="50651-123">For example, here is what the query looks like if the **Customers** table is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="50651-124">Wenn es Zeilen für die fehlerhafte Tabelle gibt, auch nachdem Sie die Tabellenzuordnung gestoppt haben, löschen Sie die Zeilen, die sich auf die fehlerhafte Tabelle beziehen.</span><span class="sxs-lookup"><span data-stu-id="50651-124">If there are rows for the failing table even after you stop the table mapping, delete the rows that are related to the failing table.</span></span> <span data-ttu-id="50651-125">Notieren Sie sich die Spalte **projectname** in der Tabelle DualWriteProjectConfiguration, und rufen Sie die Zeile in der Tabelle DualWriteProjectFieldConfiguration ab, indem Sie die Zeile mithilfe des Projektnamens löschen.</span><span class="sxs-lookup"><span data-stu-id="50651-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the row in the DualWriteProjectFieldConfiguration table by using the project name to delete the row.</span></span>
4. <span data-ttu-id="50651-126">Starten Sie die Tabellenzuordnung.</span><span class="sxs-lookup"><span data-stu-id="50651-126">Start the table mapping.</span></span> <span data-ttu-id="50651-127">Überprüfen Sie, ob die Daten ohne Probleme synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="50651-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="50651-128">Behandeln Sie Lese- oder Schreibberechtigungsfehler, wenn Sie Daten in einer Finance and Operations App erstellen</span><span class="sxs-lookup"><span data-stu-id="50651-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="50651-129">Möglicherweise wird eine Fehlermeldung Bad Request angezeigt, die dem folgenden Beispiel ähnelt, wenn Sie Daten in einer Finance and Operations App erstellen.</span><span class="sxs-lookup"><span data-stu-id="50651-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Beispiel für die Fehlermeldung Bad Request](media/error_record_id_source.png)

<span data-ttu-id="50651-131">Um das Problem zu beheben, müssen Sie dem Team der zugeordneten Geschäftseinheit Dynamics 365 Sales oder Dynamics 365 Customer Service die richtige Sicherheitsrolle zuweisen, um die fehlenden Berechtigungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="50651-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="50651-132">In der Finance and Operations App finden Sie den Geschäftsbereich, der im Verbindungssatz Datenintegration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="50651-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organisationszuordnung](media/mapped_business_unit.png)

2. <span data-ttu-id="50651-134">Melden Sie sich in der modellgesteuerten App in Dynamics 365 bei der Umgebung an und navigieren Sie zu **Einstellungen \> Sicherheit** und finden Sie das Team der zugeordneten Geschäftseinheit.</span><span class="sxs-lookup"><span data-stu-id="50651-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![Team des zugeordneten Geschäftsbereichs](media/setting_security_page.png)

3. <span data-ttu-id="50651-136">Öffnen Sie die Seite für das Team zur Bearbeitung und wählen Sie dann **Rollen verwalten**, um das Dialogfeld **Teamrollen verwalten** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="50651-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Schaltfläche Rollen verwalten](media/manage_team_roles.png)

4. <span data-ttu-id="50651-138">Weisen Sie die Rolle zu, die über die Lese-/Schreibberechtigung für die relevanten Tabellen verfügt, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="50651-138">Assign the role that has the read/write privilege for the relevant tables, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a><span data-ttu-id="50651-139">Beheben Sie Synchronisierungsprobleme in einer Umgebung, die eine kürzlich geändert Dataverse Umgebung hat</span><span class="sxs-lookup"><span data-stu-id="50651-139">Fix synchronization issues in an environment that has a recently changed Dataverse environment</span></span>

<span data-ttu-id="50651-140">**Erforderliche Rolle zum Beheben der Fehler:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="50651-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="50651-141">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie Daten in einer Finance and Operations App erstellen:</span><span class="sxs-lookup"><span data-stu-id="50651-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="50651-142">*{„entityName“:„CustCustomerV3Entity“,„executeStatus“:2,„fieldResponses“:\[\],„recordResponses“:\[{„Fehlermeldung“:„**Nutzdaten für die Entität CustCustomerV3Entity können nicht generiert werden**“,„logDateTime“:„2019-08-27T18:51:52.5843124Z“,„verboseError“:„Die Erstellung der Nutzdaten ist mit dem Fehler fehlgeschlagen. Ungültiger URI: URI ist leer.“}\],„isErrorCountUpdated“: true}*</span><span class="sxs-lookup"><span data-stu-id="50651-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="50651-143">So sieht der Fehler in der modellgesteuerten App in Dynamics 365 aus:</span><span class="sxs-lookup"><span data-stu-id="50651-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="50651-144">*Ein unerwarteter Fehler ist im ISV-Code aufgetreten. (ErrorType = ClientError) Unerwartete Ausnahme vom Plug-In (Ausführen): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: Entitätskonto konnte nicht verarbeitet werden – (Ein Verbindungsversuch ist fehlgeschlagen, da die verbundene Partei nach a nicht ordnungsgemäß geantwortet hat Zeitraum oder Verbindungsaufbau fehlgeschlagen hat, da der verbundene Host nicht reagiert hat*</span><span class="sxs-lookup"><span data-stu-id="50651-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="50651-145">Dieser Fehler tritt auf, wenn die Dataverse Umgebung fälschlicherweise zurückgesetzt wird, während Sie versuchen, Daten in der Finance and Operations App zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="50651-145">This error occurs when the Dataverse environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="50651-146">Führen Sie folgende Schritte aus, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="50651-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="50651-147">Melden Sie sich bei der virtuellen Maschine (VM) für Finance and Operations an, öffnen Sie SQL Server Management Studio (SSMS) und suchen Sie in der Tabelle DUALWRITEPROJECTCONFIGURATIONENTITY nach Zeilen, für die **internalentityname** gleich **Kunden V3** und **externalentityname** gleich **Konten** ist.</span><span class="sxs-lookup"><span data-stu-id="50651-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for rows in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="50651-148">So sieht die Abfrage aus.</span><span class="sxs-lookup"><span data-stu-id="50651-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="50651-149">Verwenden Sie den Projektnamen aus den Ergebnissen der vorherigen Abfrage, um die folgende Abfrage auszuführen.</span><span class="sxs-lookup"><span data-stu-id="50651-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="50651-150">Stellen Sie sicher, dass die **externalenvironmentURL** Spalte die richtige Dataverse oder App-URL hat.</span><span class="sxs-lookup"><span data-stu-id="50651-150">Make sure that the **externalenvironmentURL** column has the correct Dataverse or app URL.</span></span> <span data-ttu-id="50651-151">Löschen Sie doppelte Zeilen, die auf die falsche Dataverse-URL verweisen.</span><span class="sxs-lookup"><span data-stu-id="50651-151">Delete any duplicate rows that point to the wrong Dataverse URL.</span></span> <span data-ttu-id="50651-152">Löschen Sie die entsprechenden Zeilen in den Tabellen DUALWRITEPROJECTFIELDCONFIGURATION und DUALWRITEPROJECTCONFIGURATION.</span><span class="sxs-lookup"><span data-stu-id="50651-152">Delete the corresponding rows in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="50651-153">Stoppen Sie die Tabellenzuordnung und starten Sie sie neu.</span><span class="sxs-lookup"><span data-stu-id="50651-153">Stop the table mapping, and then restart it</span></span>
