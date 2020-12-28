---
title: In LinkedIn Talent Hub integrieren
description: In diesem Thema wird erläutert, wie die Integration zwischen Microsoft Dynamics 365 Human Resources und LinkedIn Talent Hub eingerichtet werden.
author: jaredha
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6f70e3a6ccf9770c75334d355db5e9df9ee912dd
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527884"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="4694f-103">In LinkedIn Talent Hub integrieren</span><span class="sxs-lookup"><span data-stu-id="4694f-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4694f-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) ist eine Bewerber-Nachverfolgungssystemplattform (ATS).</span><span class="sxs-lookup"><span data-stu-id="4694f-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="4694f-105">Sie können damit Mitarbeiter an einem Ort suchen, verwalten und einstellen.</span><span class="sxs-lookup"><span data-stu-id="4694f-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="4694f-106">Durch die Integration von Microsoft Dynamics 365 Human Resources mit LinkedIn Talent Hub können Sie auf einfache Weise Mitarbeiterdatensätze in der Personalabteilung für Bewerber erstellen, die für eine Position eingestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4694f-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="4694f-107">Einrichtung</span><span class="sxs-lookup"><span data-stu-id="4694f-107">Setup</span></span>

<span data-ttu-id="4694f-108">Ein Systemadministrator muss Einrichtungs-Aufgaben ausführen, um die Integration mit LinkedIn Talent Hub zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="4694f-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="4694f-109">Erstens in der Power Apps In dieser Umgebung müssen Sie eine Benutzer- und Sicherheitsrolle einrichten, um LinkedIn Talent Hub die entsprechenden Berechtigungen zum Schreiben von Daten in die Personalabteilung zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="4694f-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="4694f-110">Verknüpfen Sie Ihre Umgebung mit LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="4694f-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="4694f-111">Öffnen Sie [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span><span class="sxs-lookup"><span data-stu-id="4694f-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="4694f-112">Wählen Sie im Dropdown-Menü Benutzer die Option **Produkteinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="4694f-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="4694f-113">Im linken Navigationsbereich im Abschnitt **Erweitert** wählen Sie **Integrationen**.</span><span class="sxs-lookup"><span data-stu-id="4694f-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="4694f-114">Wählen Sie **Autorisieren** für die Microsoft Dynamics 365 Human Resources Integration.</span><span class="sxs-lookup"><span data-stu-id="4694f-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="4694f-115">Auf der Seite **Dynamics 365 Human Resources** wählen Sie die Umgebung aus, mit der LinkedIn Talent Hub verknüpft werden soll, und wählen Sie dann **Verknüpfung**.</span><span class="sxs-lookup"><span data-stu-id="4694f-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![LinkedIn Talent Hub Onboarding](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="4694f-117">Sie können nur Links zu Umgebungen erstellen, in denen Ihr Benutzerkonto Administratorzugriff sowohl auf die Personalumgebung als auch auf die zugehörige Power Apps Umgebung hat.</span><span class="sxs-lookup"><span data-stu-id="4694f-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="4694f-118">Wenn auf der Linkseite Personal keine Umgebungen aufgeführt sind, stellen Sie sicher, dass Sie für den Mandanten Personalumgebungen lizenziert haben und dass der Benutzer, den Sie auf der Linkseite angemeldet haben, über Administratorrechte sowohl für die Personalumgebung als auch für die Power Apps Umgebung verfügt.</span><span class="sxs-lookup"><span data-stu-id="4694f-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="4694f-119">Eine Power Apps Sicherheitsrolle erstellen</span><span class="sxs-lookup"><span data-stu-id="4694f-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="4694f-120">Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="4694f-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="4694f-121">In der **Umgebungen**-Liste wählen Sie die Umgebung aus, die der Personalumgebung zugeordnet ist, mit der Sie Ihre Instanz von LinkedIn Talent Hub verknüpfen möchten.</span><span class="sxs-lookup"><span data-stu-id="4694f-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="4694f-122">Wählen Sie **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="4694f-122">Select **Settings**.</span></span>

4. <span data-ttu-id="4694f-123">Erweitern Sie die **Benutzer + Berechtigungen** Knoten und wählen Sie **Sicherheitsrollen**.</span><span class="sxs-lookup"><span data-stu-id="4694f-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="4694f-124">Auf der **Sicherheitsrollen** Seite in der Symbolleiste wählen Sie **Neue Rolle**.</span><span class="sxs-lookup"><span data-stu-id="4694f-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="4694f-125">Auf der Registerkarte **Einzelheiten** geben Sie auf der Registerkarte einen Namen für die Rolle ein, z.B. **LinkedIn Talent Hub HRIS-Integration**.</span><span class="sxs-lookup"><span data-stu-id="4694f-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="4694f-126">Auf der Registerkarte **Anpassung** wählen Sie auf der Registerkarte Organisationsebene **Lesen**-Berechtigung für die folgenden Entitäten aus:</span><span class="sxs-lookup"><span data-stu-id="4694f-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="4694f-127">Entität</span><span class="sxs-lookup"><span data-stu-id="4694f-127">Entity</span></span>
    - <span data-ttu-id="4694f-128">Feld</span><span class="sxs-lookup"><span data-stu-id="4694f-128">Field</span></span>
    - <span data-ttu-id="4694f-129">Beziehung</span><span class="sxs-lookup"><span data-stu-id="4694f-129">Relationship</span></span>

8. <span data-ttu-id="4694f-130">Speichern und schließen Sie die Sicherheitsrolle.</span><span class="sxs-lookup"><span data-stu-id="4694f-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="4694f-131">Erstellen Sie einen Power Apps Anwendungsbenutzer</span><span class="sxs-lookup"><span data-stu-id="4694f-131">Create a Power Apps application user</span></span>

<span data-ttu-id="4694f-132">Für den LinkedIn Talent Hub-Adapter muss ein Anwendungsbenutzer erstellt werden, der dem Adapter die Berechtigung zum Schreiben von Kandidatendatensätzen in der Power Apps Umgebung erteilt.</span><span class="sxs-lookup"><span data-stu-id="4694f-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="4694f-133">Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="4694f-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="4694f-134">In der **Umgebungen**-Liste wählen Sie die Umgebung aus, die der Personalumgebung zugeordnet ist, mit der Sie Ihre Instanz von LinkedIn Talent Hub verknüpfen möchten.</span><span class="sxs-lookup"><span data-stu-id="4694f-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="4694f-135">Wählen Sie **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="4694f-135">Select **Settings**.</span></span>

4. <span data-ttu-id="4694f-136">Erweitern Sie die **Benutzer + Berechtigungen** Knoten und wählen Sie **Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="4694f-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="4694f-137">Wählen Sie **Verwalten von Benutzern in Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="4694f-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="4694f-138">Verwenden Sie das Dropdown-Menü über der Liste, um die Ansicht von der Standardansicht **Aktivierte Benutzer** auf **Anwendungsbenutzer** zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4694f-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![Anwendungsbenutzeransicht](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="4694f-140">Wählen Sie auf der Symbolleiste auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="4694f-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="4694f-141">Gehen Sie auf der Seite **neuer Benutzer** folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="4694f-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="4694f-142">Ändern Sie den Wert des **Benutzertyp**-Felds auf **Anwendungsbenutzer**.</span><span class="sxs-lookup"><span data-stu-id="4694f-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="4694f-143">Stellen Sie das Feld **Benutzername** auf **Dynamics365 HR LinkedIn HRIS-Integration**.</span><span class="sxs-lookup"><span data-stu-id="4694f-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="4694f-144">Legen Sie das Feld **Anwendungs-ID** auf **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** fest.</span><span class="sxs-lookup"><span data-stu-id="4694f-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="4694f-145">Geben Sie einen beliebigen Wert in die Felder **Vorname**, **Nachname**, und **Erste E-Mail** ein.</span><span class="sxs-lookup"><span data-stu-id="4694f-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="4694f-146">Wählen Sie auf der Symbolleiste **Speichern \& Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="4694f-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="4694f-147">Zuweisen einer Sicherheitsrolle zu einem neuen Benutzer</span><span class="sxs-lookup"><span data-stu-id="4694f-147">Assign a security role to the new user</span></span>

<span data-ttu-id="4694f-148">Nachdem Sie den neuen Anwendungsbenutzer im vorherigen Abschnitt gespeichert und geschlossen haben, kehren Sie zur Seite **Benutzerliste** zurück.</span><span class="sxs-lookup"><span data-stu-id="4694f-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="4694f-149">Auf der Seite **Benutzerliste** ändern Sie die Ansicht in **Anwendungsbenutzer**.</span><span class="sxs-lookup"><span data-stu-id="4694f-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="4694f-150">Wählen Sie Anwendungsbenutzer aus, den Sie im vorherigen Abschnitt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4694f-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="4694f-151">Wählen Sie in der Symbolleiste **Rollen verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="4694f-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="4694f-152">Wählen Sie die Sicherheitsrolle aus, die Sie zuvor für die Integration erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4694f-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="4694f-153">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="4694f-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="4694f-154">Eine Azure Active Directory App in Human Resources hinzufügen</span><span class="sxs-lookup"><span data-stu-id="4694f-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="4694f-155">In Dynamics 365 Human Resources öffnen Sie die **Azure Active Directory Anwendungen** Seite.</span><span class="sxs-lookup"><span data-stu-id="4694f-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="4694f-156">Fügen Sie einen neuen Datensatz der Liste hinzu und wählen Sie die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="4694f-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="4694f-157">**Kundenkennung**: Geben Sie **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** ein.</span><span class="sxs-lookup"><span data-stu-id="4694f-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="4694f-158">**Name**: Geben Sie den Namen der Power Apps Sicherheitsrolle ein, die Sie zuvor erstellt haben, z.B. **LinkedIn Talent Hub HRIS-Integration**.</span><span class="sxs-lookup"><span data-stu-id="4694f-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="4694f-159">**Benutzer-ID**: Wählen Sie einen Benutzer aus, der zum Schreiben von Daten in der Personalverwaltung berechtigt ist.</span><span class="sxs-lookup"><span data-stu-id="4694f-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-entity-in-common-data-service"></a><span data-ttu-id="4694f-160">Erstellen Sie die Entität in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4694f-160">Create the entity in Common Data Service</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4694f-161">Die Integration mit LinkedIn Talent Hub hängt von virtuellen Entitäten ab in Common Data Service für Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4694f-161">The integration with LinkedIn Talent Hub depends on virtual entities in Common Data Service for Human Resources.</span></span> <span data-ttu-id="4694f-162">Als Voraussetzung für diesen Schritt bei der Einrichtung müssen Sie virtuelle Entitäten konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4694f-162">As a prerequisite for this step in the setup, you must configure virtual entities.</span></span> <span data-ttu-id="4694f-163">Informationen zum Konfigurieren virtueller Entitäten finden Sie unter [Konfigurieren von Common Data Service virtuellen Entitäten](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="4694f-163">For information about how to configure virtual entities, see [Configure Common Data Service virtual entities](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

1. <span data-ttu-id="4694f-164">Öffnen Sie in der Personalabteilung die Seite **Common Data Service (CDS) Integartion**.</span><span class="sxs-lookup"><span data-stu-id="4694f-164">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="4694f-165">Wählen Sie die Registerkarte **Virtuelle Entitäten**.</span><span class="sxs-lookup"><span data-stu-id="4694f-165">Select the **Virtual entities** tab.</span></span>

3. <span data-ttu-id="4694f-166">Filtern Sie die Entitätsliste nach der zu findenden Entitätsbezeichnung **LinkedIn exportierter Kandidat**.</span><span class="sxs-lookup"><span data-stu-id="4694f-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="4694f-167">Wählen Sie die juristische Person und dann **Erstellen/Aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="4694f-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="4694f-168">Kandidatendatensätze exportieren</span><span class="sxs-lookup"><span data-stu-id="4694f-168">Exporting candidate records</span></span>

<span data-ttu-id="4694f-169">Nach Abschluss der Einrichtung können Personalvermittler und Personalfachleute (HR) die Funktion **Export nach HRIS** in LinkedIn Talent Hub nutzen, um eingestellte Kandidatendatensätze von LinkedIn Talent Hub in die Personalabteilung zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="4694f-169">After the setup is completed, recruiters and Human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="4694f-170">Exportieren Sie Datensätze von LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="4694f-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="4694f-171">Nachdem ein Kandidat den Rekrutierungsprozess durchlaufen hat und eingestellt wurde, können Sie den Kandidatendatensatz von LinkedIn Talent Hub in die Personalabteilung exportieren.</span><span class="sxs-lookup"><span data-stu-id="4694f-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="4694f-172">Öffnen Sie in LinkedIn Talent Hub das Projekt, für das Sie den neuen Mitarbeiter eingestellt haben.</span><span class="sxs-lookup"><span data-stu-id="4694f-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="4694f-173">Wählen Sie einen Kandidaten-Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="4694f-173">Select a candidate record.</span></span>

3. <span data-ttu-id="4694f-174">Wählen Sie **Status ändern** und dann **Eingestellt**.</span><span class="sxs-lookup"><span data-stu-id="4694f-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="4694f-175">Im Auslassungsmenü (**...**) für den Kandidaten wählen Sie **Export nach HRIS**.</span><span class="sxs-lookup"><span data-stu-id="4694f-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="4694f-176">In dem Bereich **Export nach HRIS** geben Sie die Informationen ein, die exportiert werden müssen:</span><span class="sxs-lookup"><span data-stu-id="4694f-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="4694f-177">In dem Feld **HRIS-Anbieter** wählen Sie **Microsoft Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="4694f-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="4694f-178">Wählen Sie im Feld **Startdatum** ein Startdatum für den Mitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="4694f-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="4694f-179">In dem Feld **Berufsbezeichnung** geben Sie eine Berufsbezeichnung für den Job des neuen Mitarbeiters ein.</span><span class="sxs-lookup"><span data-stu-id="4694f-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="4694f-180">In dem Feld **Standort** geben Sie im Feld den Standort ein, an dem sich der Mitarbeiter befindet.</span><span class="sxs-lookup"><span data-stu-id="4694f-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="4694f-181">Geben Sie die E-Mail-Adresse des Mitarbeiters ein oder überprüfen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="4694f-181">Enter or verify the employee's email address.</span></span>

![In den HRIS-Bereich in LinkedIn Talent Hub exportieren](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="4694f-183">Komplettes Onboarding in der Personalabteilung</span><span class="sxs-lookup"><span data-stu-id="4694f-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="4694f-184">Kandidatendatensätze, die von LinkedIn Talent Hub in Human Resources exportiert werden, werden im Bereich **Kadidaten zum Einstellen** auf der Seite **Personalverwaltung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4694f-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="4694f-185">Öffnen Sie in Human Resources die Siete **Personalverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="4694f-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="4694f-186">In dem Abschnitt **Kandidaten zum Einstellen** wählen Sie **Einstellen** für den ausgewählten Kandidaten.</span><span class="sxs-lookup"><span data-stu-id="4694f-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="4694f-187">In dem Dialogfeld **Stellen Sie einen neuen Mitarbeiter ein** überprüfen Sie den Datensatz und fügen Sie alle erforderlichen Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="4694f-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="4694f-188">Sie können auch die Positionsnummer auswählen, für die der Kandidat eingestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4694f-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="4694f-189">Nachdem Sie die erforderlichen Informationen eingegeben haben, können Sie mit Ihren Standardprozessen zum Erstellen von Mitarbeiterdatensätzen und zum Einbinden von Mitarbeitern fortfahren.</span><span class="sxs-lookup"><span data-stu-id="4694f-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="4694f-190">Die folgenden Details werden importiert und in den neuen Mitarbeiterdatensatz aufgenommen:</span><span class="sxs-lookup"><span data-stu-id="4694f-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="4694f-191">Vorname</span><span class="sxs-lookup"><span data-stu-id="4694f-191">First name</span></span>
- <span data-ttu-id="4694f-192">Nachname</span><span class="sxs-lookup"><span data-stu-id="4694f-192">Last name</span></span>
- <span data-ttu-id="4694f-193">Datum des Beschäftigungsbeginns</span><span class="sxs-lookup"><span data-stu-id="4694f-193">Employment start date</span></span>
- <span data-ttu-id="4694f-194">E-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="4694f-194">Email address</span></span>
- <span data-ttu-id="4694f-195">Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="4694f-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="4694f-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4694f-196">See also</span></span>

[<span data-ttu-id="4694f-197">Konfigurieren von Common Data Service virtuellen Entitäten</span><span class="sxs-lookup"><span data-stu-id="4694f-197">Configure Common Data Service virtual entities</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="4694f-198">Was ist Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="4694f-198">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)
