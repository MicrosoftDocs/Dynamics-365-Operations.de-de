---
title: Konfiguration für Finance Insights (Vorschau)
description: In diesem Thema werden die Konfigurationsschritte erläutert, mit denen Ihr System die in Finance Insights verfügbaren Funktionen nutzen kann.
author: ShivamPandey-msft
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 60e4d69157d7b73bd9e47310adae320687230080
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941225"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="39806-103">Konfiguration für Finance Insights (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="39806-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="39806-104">Finance Insights kombiniert Funktionen von Microsoft Dynamics 365 Finance mit Microsoft Dataverse, Azure und AI Builder, um leistungsstarke Prognosetools für Ihr Unternehmen zu bieten.</span><span class="sxs-lookup"><span data-stu-id="39806-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="39806-105">In diesem Thema werden die Konfigurationsschritte erläutert, mit denen Ihr System die in Finance Insights verfügbaren Funktionen nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="39806-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="39806-106">Bereitstellung von Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="39806-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="39806-107">Stellen Sie die Umgebungen bereit, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="39806-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="39806-108">Im Microsoft Dynamics Lifecycle Services (LCS) erstellen oder aktualisieren Sie eine Dynamics 365 Finance-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="39806-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="39806-109">Die Umgebung erfordert das App-Version 10.0.11/Plattform-Update 35 oder höher.</span><span class="sxs-lookup"><span data-stu-id="39806-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="39806-110">Die Umgebung muss eine Hochverfügbarkeitsumgebung (HA) in einer Sandbox sein.</span><span class="sxs-lookup"><span data-stu-id="39806-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="39806-111">(Diese Art von Umgebung wird auch als Ebene-2-Umgebung bezeichnet.) Weitere Informationen finden Sie unter [Umgebungsplanung](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="39806-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="39806-112">Wenn Sie Contoso-Demodaten verwenden, benötigen Sie zusätzliche Beispieldaten, um die Funktionen Zahlungsvorhersagen für Kunden, Cashflow-Planungen und Budgetprognosen verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="39806-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="39806-113">Dataverse konfigurieren</span><span class="sxs-lookup"><span data-stu-id="39806-113">Configure Dataverse</span></span>

<span data-ttu-id="39806-114">Verwenden Sie die folgenden Schritte, um Dataverse für Finance Insights zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="39806-114">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="39806-115">Öffnen Sie die Seite „Umgebung“ in LCS und überprüfen Sie, ob der Abschnitt **Power Platform-Integration** bereits eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="39806-115">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="39806-116">Wenn es bereits festgelegt ist, sollte der Name der Dataverse-Umgebung, die mit der Dynamics 365 Finance-Umgebung verknüpft ist, aufgelistet sein.</span><span class="sxs-lookup"><span data-stu-id="39806-116">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="39806-117">Kopieren Sie den Namen der Dataverse-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="39806-117">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="39806-118">Wenn sie nicht festgelegt ist, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="39806-118">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="39806-119">Wählen Sie die Schaltfläche **Einrichten** im Bereich Power Platform Integration.</span><span class="sxs-lookup"><span data-stu-id="39806-119">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="39806-120">Es kann bis zu einer Stunde dauern, bis die Umgebung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="39806-120">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="39806-121">Wenn die Dataverse-Umgebung erfolgreich festgelegt wurde, sollte der Name der Dataverse-Umgebung, die mit der Dynamics 365 Finance-Umgebung verknüpft ist, aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="39806-121">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="39806-122">Kopieren Sie den Namen der Dataverse-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="39806-122">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="39806-123">Nachdem Sie die Umgebung festgelegt haben, wählen Sie **NICHT** die Schaltfläche **Verbindung zu CDS für Apps**.</span><span class="sxs-lookup"><span data-stu-id="39806-123">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="39806-124">Dies wird für Finance Insights nicht benötigt und deaktiviert die Möglichkeit, die erforderlichen Umgebungs-Add-Ins in LCS zu vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="39806-124">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="39806-125">Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/) und befolgen Sie diese Schritte, um eine neue Dataverse-Umgebung im selben Active Directory-Mandanten zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="39806-125">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="39806-126">Öffnen Sie der Seite **Umgebungen**.</span><span class="sxs-lookup"><span data-stu-id="39806-126">Open the **Environments** page.</span></span>

        <span data-ttu-id="39806-127">[![Umgebungen-Seite](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="39806-127">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="39806-128">Wählen Sie die oben erstellte Dataverse-Umgebung und wählen Sie dann **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="39806-128">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="39806-129">Wählen Sie **Ressourcen \> Alle Legacy-Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="39806-129">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="39806-130">Wählen Sie in der oberen Navigationsleiste **Einstellungen** und dann **Anpassungen**.</span><span class="sxs-lookup"><span data-stu-id="39806-130">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="39806-131">Wählen Sie **Entwicklerressourcen**.</span><span class="sxs-lookup"><span data-stu-id="39806-131">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="39806-132">Kopieren Sie den Wert der **Dataverse-Organisations-ID** ein.</span><span class="sxs-lookup"><span data-stu-id="39806-132">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="39806-133">Notieren Sie sich in der Adressleiste des Browsers die URL der Dataverse-Organisation.</span><span class="sxs-lookup"><span data-stu-id="39806-133">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="39806-134">Zum Beispiel könnte die URL `https://org42b2b3d3.crm.dynamics.com` lauten.</span><span class="sxs-lookup"><span data-stu-id="39806-134">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="39806-135">Wenn Sie die Funktion „Cashflow-Planung“ oder „Budget-Plaung“ verwenden möchten, führen Sie die folgenden Schritte aus, um das Anmerkungslimit für Ihre Organisation auf mindestens 50 Megabyte (MB) zu aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="39806-135">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="39806-136">Öffnen Sie das [Power Apps-Portal](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="39806-136">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="39806-137">Wählen Sie die gerade erstellte Umgebung dann **Erweiterte Einstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-137">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="39806-138">Wählen Sie **Einstellungen \> E-Mail-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="39806-138">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="39806-139">Ändern Sie den Wert des Felds **Maximale Dateigröße** auf **51.200**.</span><span class="sxs-lookup"><span data-stu-id="39806-139">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="39806-140">(Der Wert wird in Kilobyte \[KB\] angegeben.)</span><span class="sxs-lookup"><span data-stu-id="39806-140">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="39806-141">Wählen Sie **OK** aus, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="39806-141">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="39806-142">Azure-Einrichtung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="39806-142">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="39806-143">Die Dataverse-Verzeichnis-ID und die Azure AD-Objekt-DI des Benutzers eingeben</span><span class="sxs-lookup"><span data-stu-id="39806-143">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="39806-144">Geben Sie die Dataverse-Verzeichnis-ID ein:</span><span class="sxs-lookup"><span data-stu-id="39806-144">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="39806-145">Öffnen Sie das [Azure-Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="39806-145">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="39806-146">Melden Sie sich mit der Benutzer-ID an, mit der die Dataverse-Umgebung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="39806-146">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="39806-147">Gehe zu **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="39806-147">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="39806-148">Kopieren Sie den **Mieter-ID**-Wert.</span><span class="sxs-lookup"><span data-stu-id="39806-148">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="39806-149">Geben Sie die Azure Active Directory (Azure AD)-Objekt-ID des Benutzers ein:</span><span class="sxs-lookup"><span data-stu-id="39806-149">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="39806-150">Wechseln Sie im [Azure-Portal](https://portal.azure.com) zu **Benutzer** und suchen Sie den Benutzer anhand der E-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="39806-150">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="39806-151">Wählen Sie den Namen des Benutzers aus.</span><span class="sxs-lookup"><span data-stu-id="39806-151">Select the user's name.</span></span>
    3. <span data-ttu-id="39806-152">Kopieren Sie den **Objekt-ID**-Wert.</span><span class="sxs-lookup"><span data-stu-id="39806-152">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="39806-153">Die Azure Cloud Shell verwenden, um Financial Insights Data Lake-Ressourcen einzurichten</span><span class="sxs-lookup"><span data-stu-id="39806-153">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="39806-154">Verwenden eines Windows PowerShell-Konfigurationsskripts</span><span class="sxs-lookup"><span data-stu-id="39806-154">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="39806-155">Es wurde ein Windows PowerShell-Skript bereitgestellt, mit dem Sie die in [Konfigurieren des Exports nach Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) beschriebenen Azure-Ressourcen problemlos einrichten können.</span><span class="sxs-lookup"><span data-stu-id="39806-155">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="39806-156">Wenn Sie eine manuelle Einrichtung bevorzugen, überspringen Sie diesen Vorgang und fahren Sie mit dem Vorgang im Abschnitt [Manuelle Einrichtung](#manual-setup) fort.</span><span class="sxs-lookup"><span data-stu-id="39806-156">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="39806-157">Führen Sie die folgenden Schritte aus, um das PowerShell-Skript auszuführen:</span><span class="sxs-lookup"><span data-stu-id="39806-157">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="39806-158">Die Azure CLI-Option „Try it“ oder das Ausführen des Skripts auf Ihrem PC funktioniert möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="39806-158">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="39806-159">Führen Sie die folgenden Schritte aus, um Azure mithilfe des Windows PowerShell-Skripts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="39806-159">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="39806-160">Sie müssen über Rechte zum Erstellen einer Azure-Ressourcengruppe, von Azure-Ressourcen und einer Azure AD-Anwendung verfügen.</span><span class="sxs-lookup"><span data-stu-id="39806-160">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="39806-161">Informationen zu den erforderlichen Berechtigungen finden Sie unter [Prüfen der Azure AD-Berechtigungen](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="39806-161">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="39806-162">Wechseln Sie im [Azure-Portal](https://portal.azure.com) zu Ihrem Azure-Zielabonnement.</span><span class="sxs-lookup"><span data-stu-id="39806-162">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="39806-163">Wählen Sie die **Cloud Shell**-Schaltfläche rechts neben dem **Suche**-Feld aus.</span><span class="sxs-lookup"><span data-stu-id="39806-163">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="39806-164">Wählen Sie **Power Shell**.</span><span class="sxs-lookup"><span data-stu-id="39806-164">Select **PowerShell**.</span></span>
3. <span data-ttu-id="39806-165">Erstellen Sie eine Speicherung, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="39806-165">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="39806-166">Gehen Sie auf die Registerkarte **Azure CLI** und wählen Sie **Kopieren**.</span><span class="sxs-lookup"><span data-stu-id="39806-166">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="39806-167">Öffnen Sie Notepad und fügen Sie das PowerShell-Skript ein.</span><span class="sxs-lookup"><span data-stu-id="39806-167">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="39806-168">Speichern Sie die Datei als ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="39806-168">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="39806-169">Laden Sie das Windows PowerShell-Skript in die Sitzung hoch, indem Sie die Menüoption zum Hochladen in Cloud Shell verwenden.</span><span class="sxs-lookup"><span data-stu-id="39806-169">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="39806-170">Führen Sie das Script .\ConfigureDataLake.ps1 aus.</span><span class="sxs-lookup"><span data-stu-id="39806-170">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="39806-171">Befolgen Sie die Anweisungen, um das Skript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="39806-171">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="39806-172">Verwenden Sie die Informationen aus der Skriptausgabe, um das Add-In **Export nach Data Lake** in LCS zu installieren.</span><span class="sxs-lookup"><span data-stu-id="39806-172">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="39806-173">Verwenden Sie die Informationen aus der Skriptausgabe, um den Entitätsspeicher auf der Seite **Datenverbindungen** in Finance (**Systemadministration \> Systemparameter \> Datenverbindungen**) zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="39806-173">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="39806-174">Manuelle Einrichtung</span><span class="sxs-lookup"><span data-stu-id="39806-174">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="39806-175">Dem Azure AD-Mandanten Anwendungen zum hinzufügen</span><span class="sxs-lookup"><span data-stu-id="39806-175">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="39806-176">Wechseln Sie im [Azure-Portal](https://portal.azure.com) zu **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="39806-176">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="39806-177">Wählen Sie **Verwalten \> Unternehmensanwendungen**.</span><span class="sxs-lookup"><span data-stu-id="39806-177">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="39806-178">Suchen Sie nach den folgenden Anwendungen anhand der App-ID.</span><span class="sxs-lookup"><span data-stu-id="39806-178">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="39806-179">Bewerbung</span><span class="sxs-lookup"><span data-stu-id="39806-179">Application</span></span>                              | <span data-ttu-id="39806-180">App-Kennung</span><span class="sxs-lookup"><span data-stu-id="39806-180">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="39806-181">Microsoft Dynamics ERP-Microservices</span><span class="sxs-lookup"><span data-stu-id="39806-181">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="39806-182">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="39806-182">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="39806-183">Microsoft Dynamics ERP-Microservices-CDS</span><span class="sxs-lookup"><span data-stu-id="39806-183">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="39806-184">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="39806-184">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="39806-185">AI Builder-Autorisierungsdienst</span><span class="sxs-lookup"><span data-stu-id="39806-185">AI Builder Authorization Service</span></span>         | <span data-ttu-id="39806-186">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="39806-186">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="39806-187">Wenn Sie keine der vorhergehenden Anwendungen finden können, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="39806-187">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="39806-188">Wählen Sie auf Ihrem lokalen Computer das Menü **Start** aus und suchen Sie nach **powershell**.</span><span class="sxs-lookup"><span data-stu-id="39806-188">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="39806-189">Wählen und halten Sie **Windows PowerShell** (oder klicken Sie mit der rechten Maustaste darauf) und wählen Sie dann **Als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="39806-189">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="39806-190">Führen Sie den folgenden Befehl aus, um das **AzureAD**-Modul zu installieren.</span><span class="sxs-lookup"><span data-stu-id="39806-190">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="39806-191">Wenn ein NuGet-Anbieter erforderlich ist, um fortzufahren, wählen Sie zum Installieren **J** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-191">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="39806-192">Wenn die Meldung „Nicht vertrauenswürdiges Repository“ angezeigt wird, wählen Sie **J** aus, um weiterzumachen.</span><span class="sxs-lookup"><span data-stu-id="39806-192">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="39806-193">Führen Sie für jede Anwendung, die hinzugefügt werden muss, die folgenden Befehle aus, um die Anwendung in Azure AD hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="39806-193">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="39806-194">Wenn Sie dazu aufgefordert werden, melden Sie sich als Azure AD-Administrator an.</span><span class="sxs-lookup"><span data-stu-id="39806-194">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="39806-195">Azure-Ressourcen erstellen</span><span class="sxs-lookup"><span data-stu-id="39806-195">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="39806-196">Stellen Sie sicher, dass Sie die folgenden Ressourcen in derselben Azure AD-Instanz erstellen, wie die der Dataverse-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="39806-196">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="39806-197">Sie können keine Ressourcen von keiner anderen Azure AD-Instanz verwenden.</span><span class="sxs-lookup"><span data-stu-id="39806-197">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="39806-198">Erstellen eines neuen Speicherkontos:</span><span class="sxs-lookup"><span data-stu-id="39806-198">Create a new storage account:</span></span>

    1. <span data-ttu-id="39806-199">Erstellen Sie im [Azure-Portal](https://portal.azure.com) ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="39806-199">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="39806-200">Legen Sie im Dialogfeld **Speicherkonto erstellen** die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="39806-200">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="39806-201">**Ort** – Wählen Sie das Rechenzentrum aus, in dem sich Ihre Umgebung befindet.</span><span class="sxs-lookup"><span data-stu-id="39806-201">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="39806-202">**Leistung** – Es wird empfohlen, dass Sie **Standard** auswählen.</span><span class="sxs-lookup"><span data-stu-id="39806-202">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="39806-203">**Art des Kontos** – Sie müssen **StorageV2** auswählen.</span><span class="sxs-lookup"><span data-stu-id="39806-203">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="39806-204">Wählen Sie im **Erweiterte Optionen**-Dialogfeld für die **Data Lake Storage Gen2**-Option **Aktivieren** unter der **Hierarchische Namespaces**-Funktion aus.</span><span class="sxs-lookup"><span data-stu-id="39806-204">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="39806-205">Wenn Sie diese Funktion deaktivieren, können Sie keine Daten nutzen, die von Finance and Operations-Apps geschrieben werden, indem Dienste wie Power BI-Datenflüsse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39806-205">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="39806-206">Wählen Sie **Überprüfen und erstellen**.</span><span class="sxs-lookup"><span data-stu-id="39806-206">Select **Review and create**.</span></span> <span data-ttu-id="39806-207">Nach Abschluss der Bereitstellung wird die neue Ressource im Azure-Portal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39806-207">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="39806-208">Wechseln Sie zu dem von Ihnen erstellten Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="39806-208">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="39806-209">Wählen Sie im linken Menü **Zugriffsschlüssel** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-209">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="39806-210">Kopieren und speichern Sie die Verbindungszeichenfolge für **Key1** oder **Key2**.</span><span class="sxs-lookup"><span data-stu-id="39806-210">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="39806-211">Kopieren und speichern Sie den Namen des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="39806-211">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="39806-212">Erstellen eines neuen Key Vaults:</span><span class="sxs-lookup"><span data-stu-id="39806-212">Create a new key vault:</span></span>

    1. <span data-ttu-id="39806-213">Erstellen Sie im [Azure-Portal](https://portal.azure.com) einen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="39806-213">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="39806-214">Wählen Sie im **Einen Key Vault erstellen**-Dialogfeld im Feld **Ort** das Rechenzentrum aus, in dem sich Ihre Umgebung befindet.</span><span class="sxs-lookup"><span data-stu-id="39806-214">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="39806-215">Nachdem der Key Vault erstellt wurde, wählen Sie ihn in der Liste aus und wählen dann **Geheimnisse**.</span><span class="sxs-lookup"><span data-stu-id="39806-215">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="39806-216">Wählen Sie **Generieren/Importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-216">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="39806-217">Wählen Sie im Dialogfeld **Geheimnis erstellen** im Feld **Uploadoptionen** die Option **Manuell** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-217">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="39806-218">Geben Sie einen Namen für das Geheimnis ein.</span><span class="sxs-lookup"><span data-stu-id="39806-218">Enter a name for the secret.</span></span> <span data-ttu-id="39806-219">Notieren Sie sich den Namen, da Sie ihn später angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="39806-219">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="39806-220">Geben Sie im Feld **Wert** die Verbindungszeichenfolge ein, die Sie im vorherigen Verfahren vom Speicherkonto erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="39806-220">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="39806-221">Wählen Sie **Aktiviert** und dann **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-221">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="39806-222">Das Geheimnis wird erstellt und Key Vault hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="39806-222">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="39806-223">Wechseln Sie zur **Key Vault-Übersicht** und notieren Sie sich den DNS-Namen.</span><span class="sxs-lookup"><span data-stu-id="39806-223">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="39806-224">Erstellen und registrieren Sie eine Azure AD-Anwendung:</span><span class="sxs-lookup"><span data-stu-id="39806-224">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="39806-225">Wechseln Sie im [Azure-Portal](https://portal.azure.com) zu **Azure Active Directory** und wählen Sie dann **App-Registrierungen** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-225">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="39806-226">Wählen Sie **Neue Anwendungsregistrierung** aus und legen Sie die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="39806-226">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="39806-227">**Name** – Geben Sie den Namen der App ein.</span><span class="sxs-lookup"><span data-stu-id="39806-227">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="39806-228">**Anwendungstyp** – Wählen Sie **Web-API** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-228">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="39806-229">**URI-Setup umleiten** – Geben Sie die URL für Ihre Dynamics 365-Instanz ein, z. B. `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="39806-229">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="39806-230">Wechseln Sie zu der App, die Sie gerade erstellt haben, und kopieren und speichern Sie deren **Anwendungs-ID (Client-ID)**-Wert.</span><span class="sxs-lookup"><span data-stu-id="39806-230">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="39806-231">Diesen Wert müssen Sie später beim Einrichten des Key Vaults angeben.</span><span class="sxs-lookup"><span data-stu-id="39806-231">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="39806-232">Wechseln Sie zu **API-Berechtigungen** und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="39806-232">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="39806-233">Wählen Sie **Eine Berechtigung hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="39806-233">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="39806-234">Wählen Sie **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="39806-234">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="39806-235">Nachdem Sie delegierte Berechtigungen ausgewählt haben, wählen Sie **Benutzer\_Identitätswechsel**.</span><span class="sxs-lookup"><span data-stu-id="39806-235">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="39806-236">Wählen Sie **Berechtigungen hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="39806-236">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="39806-237">Wählen Sie im Menü für die App **Zertifikate \& Geheimnisse** aus und führen die folgenden Schritte aus, um die Key Vault-Geheimnisse zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="39806-237">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="39806-238">Wählen Sie **Neuer Clientschlüssel**.</span><span class="sxs-lookup"><span data-stu-id="39806-238">Select **New client secret**.</span></span>
        2. <span data-ttu-id="39806-239">Geben Sie im Feld **Schlüsselbeschreibung** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="39806-239">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="39806-240">Wählen Sie eine Dauer und wählen Sie dann **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="39806-240">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="39806-241">Ein Geheimnis wird im Feld **Wert** generiert.</span><span class="sxs-lookup"><span data-stu-id="39806-241">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="39806-242">Kopieren und speichern Sie den geheimen Wert.</span><span class="sxs-lookup"><span data-stu-id="39806-242">Copy and save the secret value.</span></span>

4. <span data-ttu-id="39806-243">Erstellen eines neuen Key Vault-Geheimnisses:</span><span class="sxs-lookup"><span data-stu-id="39806-243">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="39806-244">Wechseln Sie zu dem zuvor erstellten Key Vault und wählen Sie **Geheimnisse** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-244">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="39806-245">Führen Sie für jeden geheimen Namen in der folgenden Tabelle die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="39806-245">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="39806-246">Wählen Sie **Generieren/Importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-246">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="39806-247">Wählen Sie im Dialogfeld **Geheimnis erstellen** im Feld **Uploadoptionen** die Option **Manuell** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-247">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="39806-248">Erstellen Sie den geheimen Namen und Wert aus der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="39806-248">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="39806-249">Wählen Sie **Aktiviert** und dann **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-249">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="39806-250">Das Geheimnis wird erstellt und Key Vault hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="39806-250">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="39806-251">Geheimnisname</span><span class="sxs-lookup"><span data-stu-id="39806-251">Secret name</span></span>                       | <span data-ttu-id="39806-252">Geheimer Wert</span><span class="sxs-lookup"><span data-stu-id="39806-252">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="39806-253">app-id</span><span class="sxs-lookup"><span data-stu-id="39806-253">app-id</span></span>                            | <span data-ttu-id="39806-254">Die App-ID der zuvor erstellten Anwendung</span><span class="sxs-lookup"><span data-stu-id="39806-254">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="39806-255">app-secret</span><span class="sxs-lookup"><span data-stu-id="39806-255">app-secret</span></span>                        | <span data-ttu-id="39806-256">Der Clientschlüssel, den Sie zuvor gespeichert haben</span><span class="sxs-lookup"><span data-stu-id="39806-256">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="39806-257">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="39806-257">storage-account-name</span></span>              | <span data-ttu-id="39806-258">Der Name des Speicherkontos, das Sie zuvor erstellt haben, z. B. **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="39806-258">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="39806-259">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="39806-259">storage-account-connection-string</span></span> | <span data-ttu-id="39806-260">Die Verbindungszeichenfolge, die Sie von der **Zugangsschlüssel**-Seite für das Speicherkonto kopiert haben</span><span class="sxs-lookup"><span data-stu-id="39806-260">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="39806-261">Autorisieren Sie die Anwendung für den Zugriff auf den Schlüsseldepot:</span><span class="sxs-lookup"><span data-stu-id="39806-261">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="39806-262">Öffnen Sie im [Azure-Portal](https://portal.azure.com) den zuvor erstellten Key Vault.</span><span class="sxs-lookup"><span data-stu-id="39806-262">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="39806-263">Wählen Sie die Zugriffsrichtlinien aus.</span><span class="sxs-lookup"><span data-stu-id="39806-263">Select the access policies.</span></span>
    3. <span data-ttu-id="39806-264">Führen Sie für jede Anwendung in der folgenden Tabelle die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="39806-264">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="39806-265">Wählen Sie **Zugriffsrichtlinie hinzufügen**, um eine Zugriffsrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39806-265">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="39806-266">Wählen Sie im Feld **Geheimnisberechtigungen** die Berechtigungen aus der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="39806-266">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="39806-267">Suchen Sie im Feld **Prinzipal auswählen** nach dem Anzeigenamen der Anwendung in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="39806-267">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="39806-268">Wählen Sie **Auswählen**.</span><span class="sxs-lookup"><span data-stu-id="39806-268">Select **Select**.</span></span>
        5. <span data-ttu-id="39806-269">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-269">Select **Add**.</span></span>
        6. <span data-ttu-id="39806-270">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-270">Select **Save**.</span></span>

        | <span data-ttu-id="39806-271">Bewerbung</span><span class="sxs-lookup"><span data-stu-id="39806-271">Application</span></span>                                              | <span data-ttu-id="39806-272">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="39806-272">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="39806-273">Der Anzeigename der neu erstellten Anwendung</span><span class="sxs-lookup"><span data-stu-id="39806-273">The display name of the new application that you created</span></span> | <span data-ttu-id="39806-274">Get, List</span><span class="sxs-lookup"><span data-stu-id="39806-274">Get, List</span></span>   |
        | <span data-ttu-id="39806-275">**Microsoft Dynamics-ERP-Microservices**</span><span class="sxs-lookup"><span data-stu-id="39806-275">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="39806-276">Get, List</span><span class="sxs-lookup"><span data-stu-id="39806-276">Get, List</span></span>   |

6. <span data-ttu-id="39806-277">Weisen Sie Rollen zu, um auf das Speicherkonto zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="39806-277">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="39806-278">Öffnen Sie im [Azure-Portal](https://portal.azure.com) das zuvor erstellte Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="39806-278">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="39806-279">Wählen Sie **Zugriffssteuerung (IAM)** und dann **Rollenzuweisungen** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-279">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="39806-280">Wählen Sie **Hinzufügen, Rollenzuweisung hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="39806-280">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="39806-281">Führen Sie für jede Anwendung in der folgenden Tabelle die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="39806-281">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="39806-282">Wählen Sie die Rolle aus der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="39806-282">Select the role from the following table.</span></span>
        2. <span data-ttu-id="39806-283">Lassen Sie das Feld **Zugriff gewähren auf** auf **Azure AD-Benutzer, -Gruppe oder -Serviceprinzipal**.</span><span class="sxs-lookup"><span data-stu-id="39806-283">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="39806-284">Geben Sie im Feld **Geheimnis** die Anwendung aus der folgenden Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="39806-284">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="39806-285">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-285">Select **Save**.</span></span>

        | <span data-ttu-id="39806-286">Bewerbung</span><span class="sxs-lookup"><span data-stu-id="39806-286">Application</span></span>                                              | <span data-ttu-id="39806-287">Rolle</span><span class="sxs-lookup"><span data-stu-id="39806-287">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="39806-288">Der Anzeigename der neu erstellten Anwendung</span><span class="sxs-lookup"><span data-stu-id="39806-288">The display name of the new application that you created</span></span> | <span data-ttu-id="39806-289">Eigentümer</span><span class="sxs-lookup"><span data-stu-id="39806-289">Owner</span></span>                       |
        | <span data-ttu-id="39806-290">Der Anzeigename der neu erstellten Anwendung</span><span class="sxs-lookup"><span data-stu-id="39806-290">The display name of the new application that you created</span></span> | <span data-ttu-id="39806-291">Mitwirkender</span><span class="sxs-lookup"><span data-stu-id="39806-291">Contributor</span></span>                 |
        | <span data-ttu-id="39806-292">Der Anzeigename der neu erstellten Anwendung</span><span class="sxs-lookup"><span data-stu-id="39806-292">The display name of the new application that you created</span></span> | <span data-ttu-id="39806-293">Mitwirkender am Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="39806-293">Storage Account Contributor</span></span> |
        | <span data-ttu-id="39806-294">Der Anzeigename der neu erstellten Anwendung</span><span class="sxs-lookup"><span data-stu-id="39806-294">The display name of the new application that you created</span></span> | <span data-ttu-id="39806-295">Datenbesitzer des Speicher-Blobs</span><span class="sxs-lookup"><span data-stu-id="39806-295">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="39806-296">**AI Builder-Autorisierungsdienst**</span><span class="sxs-lookup"><span data-stu-id="39806-296">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="39806-297">Datenleser des Speicher-Blobs</span><span class="sxs-lookup"><span data-stu-id="39806-297">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="39806-298">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="39806-298">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}

```
---



## <a name="configure-the-data-lake"></a><span data-ttu-id="39806-299">Den Data Lake konfigurieren</span><span class="sxs-lookup"><span data-stu-id="39806-299">Configure the data lake</span></span>

<span data-ttu-id="39806-300">Führen Sie die folgenden Schritte aus, um der Umgebung mithilfe von LCS das Azure Data Lake-Add-In hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="39806-300">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="39806-301">Melden Sie sich bei LCS an und wählen Sie dann unter dem Umgebungsnamen auf der rechten Seite der Seite **Alle Einzelheiten** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-301">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="39806-302">Wählen Sie Im Abschnitt **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="39806-302">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="39806-303">Wählen Sie das **Export nach Data Lake**-Add-In.</span><span class="sxs-lookup"><span data-stu-id="39806-303">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="39806-304">Geben Sie die folgenden Werte ein.</span><span class="sxs-lookup"><span data-stu-id="39806-304">Enter the following values.</span></span>

    | <span data-ttu-id="39806-305">Wert</span><span class="sxs-lookup"><span data-stu-id="39806-305">Value</span></span>                                                              | <span data-ttu-id="39806-306">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39806-306">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="39806-307">Mandanten-ID des Azure-Abonnements, in dem sich der Key Vault befindet</span><span class="sxs-lookup"><span data-stu-id="39806-307">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="39806-308">Die Mandanten-ID, in der sich das Speicherkonto, die Apps und die Key Vaults befinden.</span><span class="sxs-lookup"><span data-stu-id="39806-308">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="39806-309">Um diesen Wert zu finden, öffnen Sie das [Azure-Portal](https://portal.azure.com), wechseln Sie zu **Azure Active Directory** und kopieren Sie den **Mandanten-ID**-Wert.</span><span class="sxs-lookup"><span data-stu-id="39806-309">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="39806-310">DNS-Namen Ihres Key Vault angeben</span><span class="sxs-lookup"><span data-stu-id="39806-310">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="39806-311">Der DNS-Name des Key Vaults, z. B. `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="39806-311">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="39806-312">(Dieser Wert entspricht dem DNS-Namen, der im Entitätsspeicher verwendet wird.)</span><span class="sxs-lookup"><span data-stu-id="39806-312">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="39806-313">Geben Sie das Geheimnis an, das den Namen des Speicherkontos enthält</span><span class="sxs-lookup"><span data-stu-id="39806-313">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="39806-314">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="39806-314">**storage-account-name**</span></span> |
    | <span data-ttu-id="39806-315">Geheimname für die App-ID für den Zugriff auf Data Lake</span><span class="sxs-lookup"><span data-stu-id="39806-315">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="39806-316">**app-id**</span><span class="sxs-lookup"><span data-stu-id="39806-316">**app-id**</span></span> |
    | <span data-ttu-id="39806-317">Geheimname, der mit der App-ID verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="39806-317">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="39806-318">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="39806-318">**app-secret**</span></span> |

5. <span data-ttu-id="39806-319">Stimmen Sie den Bedingungen zu und wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="39806-319">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="39806-320">Das Add-In wird innerhalb weniger Minuten installiert.</span><span class="sxs-lookup"><span data-stu-id="39806-320">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="39806-321">Konfigurieren von AI Builder</span><span class="sxs-lookup"><span data-stu-id="39806-321">Configure AI Builder</span></span>

1. <span data-ttu-id="39806-322">Melden Sie sich bei LCS an und öffnen Sie die Seite **Umgebungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="39806-322">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="39806-323">Scrollen Sie zum Abschnitt **Umgebungs-Add-Ins**.</span><span class="sxs-lookup"><span data-stu-id="39806-323">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="39806-324">Sie sollten die Add-Ins sehen, die bereits in dieser Umgebung installiert sind.</span><span class="sxs-lookup"><span data-stu-id="39806-324">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="39806-325">Wenn das **Export nach Data Lake**-Add-In nicht dazu gehört, konfigurieren Sie dieses Add-In.</span><span class="sxs-lookup"><span data-stu-id="39806-325">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="39806-326">Wählen Sie das **Einblicke erhalten** Add-In.</span><span class="sxs-lookup"><span data-stu-id="39806-326">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="39806-327">Geben Sie auf der Detailseite mit den **Einblicke erhalten**-Add-In die folgenden Werte ein.</span><span class="sxs-lookup"><span data-stu-id="39806-327">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="39806-328">Wert</span><span class="sxs-lookup"><span data-stu-id="39806-328">Value</span></span>                                                    | <span data-ttu-id="39806-329">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39806-329">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="39806-330">CDS-Organisations-URL</span><span class="sxs-lookup"><span data-stu-id="39806-330">CDS Organization URL</span></span>                                     | <span data-ttu-id="39806-331">Die Dataverse-Organisations-URL wurde von oben kopiert.</span><span class="sxs-lookup"><span data-stu-id="39806-331">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="39806-332">CDS-Organisationskennung</span><span class="sxs-lookup"><span data-stu-id="39806-332">CDS Org ID</span></span>                                               | <span data-ttu-id="39806-333">Die Dataverse-Organisations-ID wurde von oben kopiert.</span><span class="sxs-lookup"><span data-stu-id="39806-333">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="39806-334">Aktivieren **Ist dies die Standardumgebung für Ihren Mandanten**.</span><span class="sxs-lookup"><span data-stu-id="39806-334">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="39806-335">Konfigurieren des Entitätsspeichers</span><span class="sxs-lookup"><span data-stu-id="39806-335">Configure the entity store</span></span>

<span data-ttu-id="39806-336">Führen Sie die folgenden Schritte aus, um den Entitätsspeicher in Ihrer Finance-Umgebung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="39806-336">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="39806-337">Gehen Sie zu **Systemadministration \> Einrichten \> Systemparameter \> Datenverbindungen**.</span><span class="sxs-lookup"><span data-stu-id="39806-337">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="39806-338">Legen Sie die folgenden Schlüsseltresorfelder fest:</span><span class="sxs-lookup"><span data-stu-id="39806-338">Set the following key vault fields:</span></span>

    - <span data-ttu-id="39806-339">**Anwendungs(client)-ID** – Geben Sie die zuvor erstellte Anwendungsclient-ID ein.</span><span class="sxs-lookup"><span data-stu-id="39806-339">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="39806-340">**Anwendungsgeheimnis** – Geben Sie das Geheimnis ein, das Sie für die zuvor erstellte Anwendung gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="39806-340">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="39806-341">**DNS-Name** – Den DNS(Domain Name System)-Namen finden Sie auf der Seite mit den Anwendungsdetails für die zuvor erstellte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="39806-341">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="39806-342">**Geheimer Name** – Geben Sie **storage-account-connection-string** ein.</span><span class="sxs-lookup"><span data-stu-id="39806-342">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="39806-343">Aktivieren **Data-Lake-Integration aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="39806-343">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="39806-344">Wählen Sie **Azure Key Vault testen** und überprüfen Sie, ob es keine Fehler gibt.</span><span class="sxs-lookup"><span data-stu-id="39806-344">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="39806-345">Wählen Sie **Test Azure-Storage** und überprüfen Sie, ob es keine Fehler gibt.</span><span class="sxs-lookup"><span data-stu-id="39806-345">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="39806-346">Feedback und Support</span><span class="sxs-lookup"><span data-stu-id="39806-346">Feedback and support</span></span>

<span data-ttu-id="39806-347">Bitte senden Sie eine E-Mail an [Debitorenzahlungseinblicke (Vorschau)](mailto:fiap@microsoft.com), wenn Sie an Feedback interessiert sind oder Support benötigen.</span><span class="sxs-lookup"><span data-stu-id="39806-347">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="39806-348">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="39806-348">Privacy notice</span></span>

<span data-ttu-id="39806-349">Vorschauen (1) wenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen an als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement (SLA) für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.</span><span class="sxs-lookup"><span data-stu-id="39806-349">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
