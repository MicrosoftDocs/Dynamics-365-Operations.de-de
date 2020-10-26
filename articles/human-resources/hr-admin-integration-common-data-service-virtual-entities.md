---
title: Konfigurieren von Common Data Service virtuellen Entitäten
description: In diesem Thema wird gezeigt, wie virtuelle Entitäten für Dynamics 365 Human Resources konfiguriert werden. Generieren und aktualisieren Sie vorhandene virtuelle Entitäten und analysieren Sie generierte und verfügbare Entitäten.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959574"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="f9dd3-104">Konfigurieren von Common Data Service virtuellen Entitäten</span><span class="sxs-lookup"><span data-stu-id="f9dd3-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f9dd3-105">Dynamics 365 Human Resources ist eine virtuelle Datenquelle in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="f9dd3-106">Es bietet vollständige CRUD-Vorgänge zum Erstellen, Lesen, Aktualisieren und Löschen von Common Data Service und Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="f9dd3-107">Die Daten für virtuelle Entitäten werden nicht in Common Data Service gespeichert, aber in der Anwendungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="f9dd3-108">Um CRUD-Vorgänge für Personalabteilungen von Common Data Service zu aktivieren, müssen Sie die Entitäten als virtuelle Entitäten in Common Data Service verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="f9dd3-109">Auf diese Weise können Sie CRUD-Vorgänge von Common Data Service und Microsoft Power Platform auf Daten ausführen, die sich in der Personalabteilung befinden.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="f9dd3-110">Die Vorgänge unterstützen auch die vollständige Überprüfung der Geschäftslogik der Personalabteilung, um die Datenintegrität beim Schreiben von Daten in die Entitäten sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="f9dd3-111">Verfügbare virtuelle Einheiten für die Personalabteilung</span><span class="sxs-lookup"><span data-stu-id="f9dd3-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="f9dd3-112">Alle Open Data Protocol (OData)-Entitäten in der Personalabteilung sind als virtuelle Entitäten in Common Data Service verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="f9dd3-113">Sie sind auch in Power Platform verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-113">They're also available in Power Platform.</span></span> <span data-ttu-id="f9dd3-114">Sie können jetzt Apps und Erfahrungen mit Daten direkt aus der Personalabteilung mit voller CRUD-Fähigkeit erstellen, ohne Daten nach Common Data Service kopieren oder synchronisieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="f9dd3-115">Sie können Power Apps-Portale zum Erstellen von nach außen gerichteten Websites, die Kollaborationsszenarien für Geschäftsprozesse in der Personalabteilung ermöglichen, verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="f9dd3-116">Sie können die Liste der in der Umgebung aktivierten virtuellen Entitäten anzeigen und mit den Entitäten in [Power Apps](https://make.powerapps.com) in der Lösung **Virtuelle Entitäten von Dynamics 365 HR** arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Dynamics 365 HR virtuelle Entitäten in Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="f9dd3-118">Virtuelle Entitäten versus natürliche Entitäten</span><span class="sxs-lookup"><span data-stu-id="f9dd3-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="f9dd3-119">Virtuelle Einheiten für die Personalabteilung sind nicht die gleichen wie die natürlichen Common Data Service-Entitäten, die für die Personalabteilung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="f9dd3-120">Die natürlichen Entitäten für die Personalabteilung werden separat generiert und in der HCM Common-Lösung in Common Data Service verwaltet.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="f9dd3-121">Bei natürlichen Entitäten werden die Daten in Common Data Service gespeichert und erfordern eine Synchronisation mit der Anwendungsdatenbank der Personalabteilung.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="f9dd3-122">Eine Liste der natürlichen Common Data Service-Entitäten für die Personalabteilung ist verfügbar unter [Common Data Service Entitäten](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="f9dd3-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="f9dd3-123">Einrichtung</span><span class="sxs-lookup"><span data-stu-id="f9dd3-123">Setup</span></span>

<span data-ttu-id="f9dd3-124">Befolgen Sie diese Einrichtungsschritte, um virtuelle Entitäten in Ihrer Umgebung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="f9dd3-125">Registrieren Sie die App in Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="f9dd3-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="f9dd3-126">Zunächst müssen Sie die App im Azure-Portal registrieren, damit die Microsoft-Identitätsplattform Authentifizierungs- und Autorisierungsdienste für die App und die Benutzer bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="f9dd3-127">Weitere Informationen zum Registrieren von Apps in Azure finden Sie unter [Schnellstart: Registrieren Sie eine Anwendung bei der Microsoft-Identitätsplattform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="f9dd3-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="f9dd3-128">Öffnen Sie das [Microsoft Azure-Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f9dd3-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="f9dd3-129">Wählen Sie in der Liste der Azure-Dienstleistungen die Option **App-Registrierungen** aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="f9dd3-130">Wählen Sie **Neue Registrierung** aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-130">Select **New registration**.</span></span>

4. <span data-ttu-id="f9dd3-131">Geben Sie im Feld **Name** einen aussagekräftigen Namen für die App ein.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="f9dd3-132">Beispielsweise, **Dynamics 365 Human Resources Virtuelle Entitäten**.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="f9dd3-133">Geben Sie im Feld **URI umleiten** die Namespace-URL Ihrer Instanz der Personalabteilung ein.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="f9dd3-134">Wählen Sie **Registrieren** aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-134">Select **Register**.</span></span>

7. <span data-ttu-id="f9dd3-135">Nach Abschluss der Registrierung zeigt das Azure-Portal den Bereich **Überblick** der App-Registrierung an, der dessen **Anwendungs-ID (Client-ID)** enthält.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="f9dd3-136">Beachten Sie die **Anwendungs-ID (Client-ID)** zu diesem Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="f9dd3-137">Sie geben diese Informationen ein, wenn Sie [Konfigurieren der Datenquelle der virtuellen Entität](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="f9dd3-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="f9dd3-138">Wählen Sie im linken Navigationsbereich **Zertifikate und Geheimnisse** aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="f9dd3-139">In dem Abschnitt **Kundengeheimnisse** der Seite wählen Sie **Neues Kundengeheimnis** aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="f9dd3-140">Geben Sie eine Beschreibung ein, wählen Sie eine Dauer aus und wählen Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="f9dd3-141">Erfassen Sie den Wert des Geheimnisses.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-141">Record the secret's value.</span></span> <span data-ttu-id="f9dd3-142">Sie geben diese Informationen ein, wenn Sie [Konfigurieren der Datenquelle der virtuellen Entität](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="f9dd3-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="f9dd3-143">Beachten Sie zu diesem Zeitpunkt unbedingt den Wert des Geheimnisses.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="f9dd3-144">Das Geheimnis wird nie wieder angezeigt, nachdem Sie diese Seite verlassen haben.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="f9dd3-145">Installieren Sie die Dynamics 365 HR Virtual Entity-App</span><span class="sxs-lookup"><span data-stu-id="f9dd3-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="f9dd3-146">Installieren Sie die Dynamics 365 HR Virtual Entity-App in Ihrer Power Apps-Umgebung, um das Lösungspaket für virtuelle Entitäten für Common Data Service bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="f9dd3-147">Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="f9dd3-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="f9dd3-148">In der Liste **Umgebungen** wählen Sie die Power Apps-Umgebung, die Ihrer Personalabteilungsinstanz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="f9dd3-149">In dem Abschnitt **Ressourcen** der Seite wählen Sie **Dynamics 365-Apps**.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="f9dd3-150">Wählen Sie die Aktion **App installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="f9dd3-151">Wählen Sie **Dynamics 365 HR Virtuelle Entität** und dann **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-151">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="f9dd3-152">Überprüfen und markieren Sie, um den Vertragsbedingungen zuzustimmen.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="f9dd3-153">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-153">Select **Install**.</span></span>

<span data-ttu-id="f9dd3-154">Die Installation dauert einige Minuten.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-154">The install takes a few minutes.</span></span> <span data-ttu-id="f9dd3-155">Fahren Sie nach Abschluss mit den nächsten Schritten fort.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-155">When it completes, continue to the next steps.</span></span>

![Installieren Sie die Dynamics 365 HR Virtual Entity-App vom Power Platform-Admin Center](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="f9dd3-157">Konfigurieren Sie die Datenquelle der virtuellen Entität</span><span class="sxs-lookup"><span data-stu-id="f9dd3-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="f9dd3-158">Der nächste Schritt besteht darin, die Datenquelle der virtuellen Entität in der Power Apps-Umgebung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="f9dd3-159">Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="f9dd3-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="f9dd3-160">In der Liste **Umgebungen** wählen Sie die Power Apps-Umgebung, die Ihrer Personalabteilungsinstanz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="f9dd3-161">Wählen Sie die **Umgebungs-URL** im Abschnitt **Details** der Seite aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="f9dd3-162">Im **Lösungsintegrität-Hub** wählen Sie das Symbol **Erweiterte Suche** oben rechts auf der Anwendungsseite aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-162">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="f9dd3-163">Wählen Sie auf der Seite **Erweiterte Suche** in der Dropdown-Liste **Suchen** **Finance and Operations Konfigurationen virtueller Datenquellen** aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="f9dd3-164">Wählen Sie **Ergebnisse** aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-164">Select **Results**.</span></span>

7. <span data-ttu-id="f9dd3-165">Wählen Sie den Datensatz **Microsoft HR-Datenquelle**.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="f9dd3-166">Geben Sie die erforderlichen Informationen für die Datenquellenkonfiguration ein.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="f9dd3-167">**Ziel-URL**: Die URL Ihres Personalabteilungs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-167">**Target URL**: The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="f9dd3-168">**Mandanten-ID**: Die Azure Active Directory (Azure AD)-Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-168">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="f9dd3-169">**AAD-Anwendungs-ID**: Die Anwendungs-ID (Client-ID), die für die im Microsoft Azure-Portal registrierte Anwendung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-169">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="f9dd3-170">Sie haben diese Informationen früher während des Schritts [Registrieren Sie die App in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) erhalten.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="f9dd3-171">**AAD-Anwendungs-Geheimnis**: Das Kundengeheimnis, das für die im Microsoft Azure-Portal registrierte Anwendung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-171">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="f9dd3-172">Sie haben diese Informationen früher während des Schritts [Registrieren Sie die App in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) erhalten.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="f9dd3-173">Wählen Sie **Speichern & Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-173">Select **Save & Close**.</span></span>

   ![Microsoft HR-Datenquelle](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="f9dd3-175">Erteilen Sie App-Berechtigungen in der Personalabteilung</span><span class="sxs-lookup"><span data-stu-id="f9dd3-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="f9dd3-176">Erteilen Sie Berechtigungen für die beiden Azure AD-Anwendungen in der Personalabteilung:</span><span class="sxs-lookup"><span data-stu-id="f9dd3-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="f9dd3-177">Die für Ihren Mandanten im Microsoft Azure-Portal erstellte App</span><span class="sxs-lookup"><span data-stu-id="f9dd3-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="f9dd3-178">Die Dynamics 365 HR Virtual Entity-App installiert in der Power Apps-Umgebung</span><span class="sxs-lookup"><span data-stu-id="f9dd3-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="f9dd3-179">Öffnen Sie in der Personalabteilung die Seite **Azure Active Directory-Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="f9dd3-180">Wählen Sie **Neu** aus, um einen neuen Anwendungsdatensatz zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="f9dd3-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="f9dd3-181">Geben Sie im Feld **Client-ID** die Client-ID der App ein, die Sie im Microsoft Azure-Portal registriert haben.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="f9dd3-182">Geben Sie im Feld **Name** den Namen der App ein, die Sie im Microsoft Azure-Portal registriert haben.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="f9dd3-183">Wählen Sie im Feld **Benutzer-ID** die Benutzer-ID eines Benutzers mit Administratorrechten in der Personalabteilung und der Power Apps-Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="f9dd3-184">Wählen Sie **Neu** aus, um einen zweiten Anwendungsdatensatz zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="f9dd3-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="f9dd3-185">**Client-ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="f9dd3-185">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="f9dd3-186">**Name**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="f9dd3-186">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="f9dd3-187">Wählen Sie im Feld **Benutzer-ID** die Benutzer-ID eines Benutzers mit Administratorrechten in der Personalabteilung und der Power Apps-Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="f9dd3-188">Erstellen virtueller Entitäten</span><span class="sxs-lookup"><span data-stu-id="f9dd3-188">Generate virtual entities</span></span>

<span data-ttu-id="f9dd3-189">Nach Abschluss des Setups können Sie die virtuellen Entitäten auswählen, die Sie generieren und in Ihrer Common Data Service-Instanz aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="f9dd3-190">Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="f9dd3-190">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="f9dd3-191">In der Liste **Umgebungen** wählen Sie die Power Apps-Umgebung, die Ihrer Personalabteilungsinstanz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-191">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="f9dd3-192">Wählen Sie die **Umgebungs-URL** im Abschnitt **Details** der Seite aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-192">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="f9dd3-193">Im **Lösungsintegrität-Hub** wählen Sie das Symbol **Erweiterte Suche** oben rechts auf der Seite aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-193">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the page.</span></span>

5. <span data-ttu-id="f9dd3-194">Wählen Sie auf der Seite **Erweiterte Suche** in der Dropdown-Liste **Suche** die Option **Verfügbare HR-Einheiten** aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-194">On the **Advanced Find** page, in the **Look for** dropdown list, select **Available HR Entities**.</span></span>

6. <span data-ttu-id="f9dd3-195">Verwenden Sie die Filteroptionen, um die Entität oder Entitäten zu finden, die Sie aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-195">Use the filter options to find the entity or entities you want to enable.</span></span>

7. <span data-ttu-id="f9dd3-196">Wählen Sie eine Entität aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-196">Select an entity from the list.</span></span>

8. <span data-ttu-id="f9dd3-197">Ändern Sie auf der Entitätsseite die Eigenschaft **Wurde erstellt** in **Ja** für die Entität.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-197">On the entity page, change the **Has Been Generated** property to **Yes** for the entity.</span></span>

9. <span data-ttu-id="f9dd3-198">Entitätsseite speichern und schließen.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-198">Save and close the entity page.</span></span>

> [!NOTE]
> <span data-ttu-id="f9dd3-199">Sie können mehrere virtuelle Entitäten gleichzeitig generieren, indem Sie die Seite **Mehrere Datensätze ändern** verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-199">You can generate multiple virtual entities at once by using the **Change Multiple Records** page.</span></span> <span data-ttu-id="f9dd3-200">Wählen Sie mehrere Datensätze auf der Seite aus und wählen Sie **Bearbeiten** auf dem Menüband aus.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-200">Select multiple records on the page, and select **Edit** on the ribbon.</span></span> <span data-ttu-id="f9dd3-201">Sie können dann die Eigenschaft **Wurde erstellt** für alle ausgewählten Datensätze ändern.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-201">You can then change the **Has Been Generated** property for all selected records.</span></span>

![Verfügbare HR-Entitäten](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> <span data-ttu-id="f9dd3-203">Um den Prozess der Generierung virtueller Entitäten in zukünftigen Versionen zu optimieren, wird der Prozess auf einer Seite in der Personalabteilung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9dd3-203">To streamline the process of generating virtual entities in future releases, the process will occur in a page in Human Resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9dd3-204">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9dd3-204">See also</span></span>

[<span data-ttu-id="f9dd3-205">Was ist Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="f9dd3-205">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="f9dd3-206">Entitätsübersicht</span><span class="sxs-lookup"><span data-stu-id="f9dd3-206">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="f9dd3-207">Übersicht über Entitätsbeziehungen</span><span class="sxs-lookup"><span data-stu-id="f9dd3-207">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="f9dd3-208">Erstellen und bearbeiten Sie virtuelle Entitäten, die Daten aus einer externen Datenquelle enthalten</span><span class="sxs-lookup"><span data-stu-id="f9dd3-208">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="f9dd3-209">Was sind Power Apps-Portale?</span><span class="sxs-lookup"><span data-stu-id="f9dd3-209">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="f9dd3-210">Übersicht über das Erstellen von Apps in Power Apps</span><span class="sxs-lookup"><span data-stu-id="f9dd3-210">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
