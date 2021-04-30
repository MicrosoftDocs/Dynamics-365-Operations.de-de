---
title: Virtuelle Dataverse-Tabellen konfigurieren
description: In diesem Thema wird gezeigt, wie virtuelle Tabellen für Dynamics 365 Human Resources konfiguriert werden. Generieren und aktualisieren Sie vorhandene virtuelle Tabellen und analysieren Sie generierte und verfügbare Tabellen.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae36f1436ddd7f41bf0c3510b47cbc440224f484
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890051"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="6e558-104">Virtuelle Dataverse-Tabellen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6e558-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6e558-105">Dynamics 365 Human Resources ist eine virtuelle Datenquelle in Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6e558-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="6e558-106">Es bietet vollständige CRUD-Vorgänge zum Erstellen, Lesen, Aktualisieren und Löschen von Dataverse und Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="6e558-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="6e558-107">Die Daten für virtuelle Tabellen werden nicht in Dataverse gespeichert, aber in der Anwendungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="6e558-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="6e558-108">Um CRUD-Vorgänge für Human Resources-Entitäten von Dataverse zu aktivieren, müssen Sie die Entitäten als virtuelle Tabellen in Dataverse verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="6e558-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="6e558-109">Auf diese Weise können Sie CRUD-Vorgänge von Dataverse und Microsoft Power Platform auf Daten ausführen, die sich in Human Resources befinden.</span><span class="sxs-lookup"><span data-stu-id="6e558-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="6e558-110">Die Vorgänge unterstützen auch die vollständige Überprüfung der Geschäftslogik von Human Resources, um die Datenintegrität beim Schreiben von Daten in die Entitäten sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="6e558-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="6e558-111">Human Resources-Entitäten entsprechen Dataverse-Tabellen.</span><span class="sxs-lookup"><span data-stu-id="6e558-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="6e558-112">Weitere Informationen zu Dataverse (früher Common Data Service) und Terminologie-Updates finden Sie unter [Was ist Microsoft Dataverse ?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="6e558-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="6e558-113">Verfügbare virtuelle Tabellen für Human Resources</span><span class="sxs-lookup"><span data-stu-id="6e558-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="6e558-114">Alle Open Data Protocol (OData)-Entitäten in Human Resources sind als virtuelle Tabellen in Dataverse verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6e558-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="6e558-115">Sie sind auch in Power Platform verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6e558-115">They're also available in Power Platform.</span></span> <span data-ttu-id="6e558-116">Sie können jetzt Apps und Erfahrungen mit Daten direkt aus Human Resources mit voller CRUD-Fähigkeit erstellen, ohne Daten nach Dataverse kopieren oder synchronisieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="6e558-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="6e558-117">Sie können Power Apps-Portale zum Erstellen von nach außen gerichteten Websites, die Kollaborationsszenarien für Geschäftsprozesse in Human Resources ermöglichen, verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e558-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="6e558-118">Sie können die Liste der in der Umgebung aktivierten virtuellen Tabellen anzeigen und mit den Tabellen in [Power Apps](https://make.powerapps.com) in der Lösung **Virtuelle Tabellen von Dynamics 365 HR** arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6e558-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Dynamics 365 HR virtuelle Tabellen in Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="6e558-120">Virtuelle Tabellen gegenüber nativen Tabellen</span><span class="sxs-lookup"><span data-stu-id="6e558-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="6e558-121">Virtuelle Tabellen für Human Resources sind nicht die gleichen wie die nativen Dataverse-Tabellen, die für Human Resources erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="6e558-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="6e558-122">Die nativen Tabellen für Human Resources werden separat generiert und in der HCM Common-Lösung in Dataverse verwaltet.</span><span class="sxs-lookup"><span data-stu-id="6e558-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="6e558-123">Bei nativen Tabellen werden die Daten in Dataverse gespeichert und erfordern eine Synchronisation mit der Anwendungsdatenbank von Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6e558-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="6e558-124">Eine Liste der nativen Dataverse-Tabellen für Human Resources ist verfügbar unter [Dataverse Tabellen](./hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="6e558-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](./hr-developer-entities.md).</span></span>

## <a name="setup"></a><span data-ttu-id="6e558-125">Einstellung</span><span class="sxs-lookup"><span data-stu-id="6e558-125">Setup</span></span>

<span data-ttu-id="6e558-126">Befolgen Sie diese Einrichtungsschritte, um virtuelle Tabellen in Ihrer Umgebung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6e558-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="6e558-127">Virtuelle Tabellen in Human Resources aktivieren</span><span class="sxs-lookup"><span data-stu-id="6e558-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="6e558-128">Zunächst müssen Sie virtuelle Tabellen im Arbeitsplatz **Funktionsverwaltung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6e558-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="6e558-129">Wählen Sie in Human Resources **Systemverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="6e558-130">Wählen Sie die Kachel **Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="6e558-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="6e558-131">Wählen Sie **Support für virtuelle Tabellen für HR in Dataverse** und dann **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="6e558-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="6e558-132">Weitere Informationen zum Aktivieren und Deaktivieren von Funktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="6e558-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="6e558-133">Registrieren Sie die App in Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="6e558-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="6e558-134">Zunächst müssen Sie Ihre Human Resources-Instanz im Azure-Portal registrieren, damit die Microsoft-Identitätsplattform Authentifizierungs- und Autorisierungsdienste für die App und die Benutzer bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6e558-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="6e558-135">Weitere Informationen zum Registrieren von Apps in Azure finden Sie unter [Schnellstart: Registrieren Sie eine Anwendung bei der Microsoft-Identitätsplattform](/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="6e558-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="6e558-136">Öffnen Sie das [Microsoft Azure-Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="6e558-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="6e558-137">Wählen Sie in der Liste der Azure-Dienstleistungen die Option **App-Registrierungen** aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="6e558-138">Wählen Sie **Neue Registrierung** aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-138">Select **New registration**.</span></span>

4. <span data-ttu-id="6e558-139">Geben Sie im Feld **Name** einen aussagekräftigen Namen für die App ein.</span><span class="sxs-lookup"><span data-stu-id="6e558-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="6e558-140">Beispielsweise, **Dynamics 365 Human Resources Virtuelle Tabellen**.</span><span class="sxs-lookup"><span data-stu-id="6e558-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="6e558-141">Geben Sie im Feld **URI umleiten** die Namespace-URL Ihrer Instanz in Human Resources ein.</span><span class="sxs-lookup"><span data-stu-id="6e558-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="6e558-142">Wählen Sie **Registrieren** aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-142">Select **Register**.</span></span>

7. <span data-ttu-id="6e558-143">Nach Abschluss der Registrierung zeigt das Azure-Portal den Bereich **Überblick** der App-Registrierung an, der dessen **Anwendungs-ID (Client-ID)** enthält.</span><span class="sxs-lookup"><span data-stu-id="6e558-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="6e558-144">Beachten Sie die **Anwendungs-ID (Client-ID)** zu diesem Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="6e558-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="6e558-145">Sie geben diese Informationen ein, wenn Sie [Konfigurieren der Datenquelle der virtuellen Tabelle](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="6e558-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="6e558-146">Wählen Sie im linken Navigationsbereich **Zertifikate und Geheimnisse** aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="6e558-147">In dem Abschnitt **Kundengeheimnisse** der Seite wählen Sie **Neues Kundengeheimnis** aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="6e558-148">Geben Sie eine Beschreibung ein, wählen Sie eine Dauer aus und wählen Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="6e558-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="6e558-149">Erfassen Sie den Wert des Geheimnisses aus dem der Eigenschaft **Wert** der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6e558-149">Record the secret's value from the **Value** property of the table.</span></span> <span data-ttu-id="6e558-150">Sie geben diese Informationen ein, wenn Sie [Konfigurieren der Datenquelle der virtuellen Tabelle](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="6e558-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6e558-151">Beachten Sie zu diesem Zeitpunkt unbedingt den Wert des Geheimnisses.</span><span class="sxs-lookup"><span data-stu-id="6e558-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="6e558-152">Das Geheimnis wird nie wieder angezeigt, nachdem Sie diese Seite verlassen haben.</span><span class="sxs-lookup"><span data-stu-id="6e558-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="6e558-153">Installieren Sie die Dynamics 365 HR Virtual Table-App</span><span class="sxs-lookup"><span data-stu-id="6e558-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="6e558-154">Installieren Sie die Dynamics 365 HR Virtual Table-App in Ihrer Power Apps-Umgebung, um das Lösungspaket für virtuelle Tabellen für Dataverse bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6e558-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="6e558-155">Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="6e558-155">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="6e558-156">In der Liste **Umgebungen** wählen Sie die Power Apps-Umgebung, die Ihrer Human Resources-Instanz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6e558-156">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="6e558-157">In dem Abschnitt **Ressourcen** der Seite wählen Sie **Dynamics 365-Apps**.</span><span class="sxs-lookup"><span data-stu-id="6e558-157">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="6e558-158">Wählen Sie die Aktion **App installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-158">Select the **Install app** action.</span></span>

5. <span data-ttu-id="6e558-159">Wählen Sie **Dynamics 365 HR Virtual Table** und dann **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="6e558-159">Select **Dynamics 365 HR Virtual Table**, and select **Next**.</span></span>

6. <span data-ttu-id="6e558-160">Überprüfen und markieren Sie, um den Vertragsbedingungen zuzustimmen.</span><span class="sxs-lookup"><span data-stu-id="6e558-160">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="6e558-161">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="6e558-161">Select **Install**.</span></span>

<span data-ttu-id="6e558-162">Die Installation dauert einige Minuten.</span><span class="sxs-lookup"><span data-stu-id="6e558-162">The install takes a few minutes.</span></span> <span data-ttu-id="6e558-163">Fahren Sie nach Abschluss mit den nächsten Schritten fort.</span><span class="sxs-lookup"><span data-stu-id="6e558-163">When it completes, continue to the next steps.</span></span>

![Installieren Sie die Dynamics 365 HR Virtual Table-App vom Power Platform-Admin Center](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="6e558-165">Konfigurieren Sie die Datenquelle der virtuellen Tabelle</span><span class="sxs-lookup"><span data-stu-id="6e558-165">Configure the virtual table data source</span></span> 

<span data-ttu-id="6e558-166">Der nächste Schritt besteht darin, die Datenquelle der virtuellen Tabelle in der Power Apps-Umgebung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6e558-166">The next step is to configure the virtual table data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="6e558-167">Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="6e558-167">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="6e558-168">In der Liste **Umgebungen** wählen Sie die Power Apps-Umgebung, die Ihrer Human Resources-Instanz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6e558-168">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="6e558-169">Wählen Sie die **Umgebungs-URL** im Abschnitt **Details** der Seite aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-169">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="6e558-170">Im **Lösungsintegrität-Hub** wählen Sie das Symbol **Erweiterte Suche** oben rechts auf der Anwendungsseite aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-170">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="6e558-171">Wählen Sie auf der Seite **Erweiterte Suche** in der Dropdown-Liste **Suchen** **Finance and Operations Konfigurationen virtueller Datenquellen** aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-171">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="6e558-172">Wählen Sie **Ergebnisse** aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-172">Select **Results**.</span></span>

7. <span data-ttu-id="6e558-173">Wählen Sie den Datensatz **Microsoft HR-Datenquelle**.</span><span class="sxs-lookup"><span data-stu-id="6e558-173">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="6e558-174">Geben Sie die erforderlichen Informationen für die Datenquellenkonfiguration ein:</span><span class="sxs-lookup"><span data-stu-id="6e558-174">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="6e558-175">**Ziel-URL**: Die URL Ihres Human Resources-Namespace.</span><span class="sxs-lookup"><span data-stu-id="6e558-175">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="6e558-176">Das Format der Ziel-URL sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="6e558-176">The format of the target URL is:</span></span>
     
     <span data-ttu-id="6e558-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="6e558-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="6e558-178">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6e558-178">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="6e558-179">Vergessen Sie das „**/**“-Zeichen am Ende der URL nicht, um einen Fehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6e558-179">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="6e558-180">**Mandanten-ID**: Die Azure Active Directory (Azure AD)-Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="6e558-180">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="6e558-181">**AAD-Anwendungs-ID**: Die Anwendungs-ID (Client-ID), die für die im Microsoft Azure-Portal registrierte Anwendung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6e558-181">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="6e558-182">Sie haben diese Informationen früher während des Schritts [Registrieren Sie die App in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) erhalten.</span><span class="sxs-lookup"><span data-stu-id="6e558-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="6e558-183">**AAD-Anwendungs-Geheimnis**: Das Kundengeheimnis, das für die im Microsoft Azure-Portal registrierte Anwendung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6e558-183">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="6e558-184">Sie haben diese Informationen früher während des Schritts [Registrieren Sie die App in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) erhalten.</span><span class="sxs-lookup"><span data-stu-id="6e558-184">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR-Datenquelle](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="6e558-186">Wählen Sie **Speichern & Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-186">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="6e558-187">App-Berechtigungen in Human Resources erteilen</span><span class="sxs-lookup"><span data-stu-id="6e558-187">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="6e558-188">Erteilen Sie Berechtigungen für die beiden Azure AD-Anwendungen in Human Resources:</span><span class="sxs-lookup"><span data-stu-id="6e558-188">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="6e558-189">Die für Ihren Mandanten im Microsoft Azure-Portal erstellte App</span><span class="sxs-lookup"><span data-stu-id="6e558-189">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="6e558-190">Die Dynamics 365 HR Virtual Table-App installiert in der Power Apps-Umgebung</span><span class="sxs-lookup"><span data-stu-id="6e558-190">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="6e558-191">Öffnen Sie in Human Resources die Seite **Azure Active Directory-Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="6e558-191">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="6e558-192">Wählen Sie **Neu** aus, um einen neuen Anwendungsdatensatz zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="6e558-192">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="6e558-193">Geben Sie im Feld **Client-ID** die Client-ID der App ein, die Sie im Microsoft Azure-Portal registriert haben.</span><span class="sxs-lookup"><span data-stu-id="6e558-193">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="6e558-194">Geben Sie im Feld **Name** den Namen der App ein, die Sie im Microsoft Azure-Portal registriert haben.</span><span class="sxs-lookup"><span data-stu-id="6e558-194">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="6e558-195">Wählen Sie im Feld **Benutzer-ID** die Benutzer-ID eines Benutzers mit Administratorrechten in Human Resources und der Power Apps-Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-195">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="6e558-196">Wählen Sie **Neu** aus, um einen zweiten Anwendungsdatensatz zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="6e558-196">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="6e558-197">**Client-ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="6e558-197">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="6e558-198">**Name**: Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="6e558-198">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="6e558-199">Wählen Sie im Feld **Benutzer-ID** die Benutzer-ID eines Benutzers mit Administratorrechten in Human Resources und der Power Apps-Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="6e558-199">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="6e558-200">Erstellen virtueller Tabellen</span><span class="sxs-lookup"><span data-stu-id="6e558-200">Generate virtual tables</span></span>

<span data-ttu-id="6e558-201">Nach Abschluss des Setups können Sie die virtuellen Tabellen auswählen, die Sie generieren und in Ihrer Dataverse-Instanz aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6e558-201">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="6e558-202">Öffnen Sie in Human Resources die Seite **Dataverse-Integartion**.</span><span class="sxs-lookup"><span data-stu-id="6e558-202">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="6e558-203">Wählen Sie die Registerkarte **Virtuelle Tabellen**.</span><span class="sxs-lookup"><span data-stu-id="6e558-203">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="6e558-204">Die Umschaltung **Aktivieren Sie die virtuelle Tabelle** wird automatisch auf **Ja** gesetzt, wenn alle erforderlichen Einstellungen abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="6e558-204">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="6e558-205">Wenn der Schalter auf **Nein** eingestellt ist, überprüfen Sie die Schritte in den vorherigen Abschnitten dieses Dokuments, um sicherzustellen, dass alle erforderlichen Einstellungen abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="6e558-205">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="6e558-206">Wählen Sie die Tabelle oder Tabellen aus, die Sie in Dataverse generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6e558-206">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="6e558-207">Wählen Sie **Generieren/Aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="6e558-207">Select **Generate/refresh**.</span></span>

![Dataverse Integration](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a><span data-ttu-id="6e558-209">Überprüfen Sie den Status der Tabellengenerierung</span><span class="sxs-lookup"><span data-stu-id="6e558-209">Check table generation status</span></span>

<span data-ttu-id="6e558-210">Virtuelle Tabellen werden in Dataverse durch einen asynchronen Hintergrundprozess generiert.</span><span class="sxs-lookup"><span data-stu-id="6e558-210">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="6e558-211">Aktualisierungen der Prozessanzeige im Action Center.</span><span class="sxs-lookup"><span data-stu-id="6e558-211">Updates on the process display in the action center.</span></span> <span data-ttu-id="6e558-212">Details zum Prozess, einschließlich Fehlerprotokollen, werden in der Seite **Prozessautomatisierung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6e558-212">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="6e558-213">Öffnen Sie in Human Resources die Listenseite **Prozessautomatisierung**.</span><span class="sxs-lookup"><span data-stu-id="6e558-213">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="6e558-214">Wählen Sie die Registerkarte **Hintergrundprozesse**.</span><span class="sxs-lookup"><span data-stu-id="6e558-214">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="6e558-215">Wählen Sie **Hintergrundprozess für asynchrone Operationen einer virtuellen Tabelle**.</span><span class="sxs-lookup"><span data-stu-id="6e558-215">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="6e558-216">Wählen Sie **Aktuelle Ergebnisse anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="6e558-216">Select **View most recent results**.</span></span>

<span data-ttu-id="6e558-217">Im Slideout-Bereich werden die neuesten Ausführungsergebnisse für den Prozess angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6e558-217">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="6e558-218">Sie können das Protokoll für den Prozess anzeigen, einschließlich aller von Dataverse zurückgegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="6e558-218">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e558-219">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e558-219">See also</span></span>

[<span data-ttu-id="6e558-220">Was ist Dataverse?</span><span class="sxs-lookup"><span data-stu-id="6e558-220">What is Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="6e558-221">Tabellen in Dataverse</span><span class="sxs-lookup"><span data-stu-id="6e558-221">Tables in Dataverse</span></span>](/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="6e558-222">Übersicht über Tabellenbeziehungen</span><span class="sxs-lookup"><span data-stu-id="6e558-222">Table relationships overview</span></span>](/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="6e558-223">Erstellen und bearbeiten Sie virtuelle Tabellen, die Daten aus einer externen Datenquelle enthalten</span><span class="sxs-lookup"><span data-stu-id="6e558-223">Create and edit virtual tables that contain data from an external data source</span></span>](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="6e558-224">Was sind Power Apps-Portale?</span><span class="sxs-lookup"><span data-stu-id="6e558-224">What is Power Apps portals?</span></span>](/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="6e558-225">Übersicht über das Erstellen von Apps in Power Apps</span><span class="sxs-lookup"><span data-stu-id="6e558-225">Overview of creating apps in Power Apps</span></span>](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]