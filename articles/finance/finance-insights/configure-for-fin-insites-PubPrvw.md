---
title: Konfiguration für Finance Insights für die öffentliche Vorschau (Vorschau) – Version 10.0.20 und höher
description: In diesem Thema wird die Konfiguration erläutert, mit denen Ihr System die in Finance Insights verfügbaren Funktionen für die öffentliche Vorschau in Version 10.0.20 und höher nutzen kann.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222611"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="20e59-103">Konfiguration für Finance Insights für die öffentliche Vorschau (Vorschau) – Version 10.0.20 und höher</span><span class="sxs-lookup"><span data-stu-id="20e59-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="20e59-104">Finance Insights kombiniert Funktionen von Microsoft Dynamics 365 Finance mit Dataverse, Azure und AI Builder, um leistungsstarke Prognosetools für Ihr Unternehmen zu bieten.</span><span class="sxs-lookup"><span data-stu-id="20e59-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="20e59-105">In diesem Thema wird die Konfiguration von Dynamics 365 Finance Version 10.0.20 erläutert, mit denen Ihr System die in der öffentlichen Vorschau von Finance Insights verfügbaren Funktionen nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="20e59-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="20e59-106">Die in diesem Thema beschriebenen Konfigurationsschritte gelten nur für Finance Version 10.0.20 und höher.</span><span class="sxs-lookup"><span data-stu-id="20e59-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="20e59-107">Informationen zum Einrichten von Finance Insights in Version 10.0.19 und früher finden Sie unter [Konfiguration für Finance Insights – Versionen 10.0.18](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="20e59-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="20e59-108">Finance bereitstellen</span><span class="sxs-lookup"><span data-stu-id="20e59-108">Deploy Finance</span></span>

<span data-ttu-id="20e59-109">Gehen Sie folgendermaßen vor, um die Umgebungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="20e59-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="20e59-110">Erstellen oder aktualisieren Sie im Microsoft Dynamics Lifecycle Services (LCS) eine Finance-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="20e59-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="20e59-111">Die Umgebung erfordert App-Version 10.0.20 oder höher der Finance and Operations-Apps.</span><span class="sxs-lookup"><span data-stu-id="20e59-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="20e59-112">Die Umgebung muss eine Hochverfügbarkeitsumgebung (HA) in einer Sandbox sein.</span><span class="sxs-lookup"><span data-stu-id="20e59-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="20e59-113">(Diese Art von Umgebung wird auch als Ebene-2-Umgebung bezeichnet.) Weitere Informationen finden Sie unter [Umgebungsplanung](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="20e59-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="20e59-114">Wenn Sie Finance Insights in einer Sandbox-Umgebung konfigurieren, müssen Sie möglicherweise Produktionsdaten in diese Umgebung kopieren, damit Vorhersagen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="20e59-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="20e59-115">Das Vorhersagemodell verwendet Daten aus mehreren Jahren, um Vorhersagen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="20e59-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="20e59-116">Die Contoso Demodaten enthalten nicht genügend historische Daten, um das Vorhersagemodell angemessen zu trainieren.</span><span class="sxs-lookup"><span data-stu-id="20e59-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="20e59-117">Dataverse konfigurieren</span><span class="sxs-lookup"><span data-stu-id="20e59-117">Configure Dataverse</span></span>

<span data-ttu-id="20e59-118">Gehen Sie folgendernamßen vor, um Dataverse für Finance Insights zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="20e59-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="20e59-119">Öffnen Sie die Seite „Umgebung“ in LCS und überprüfen Sie, ob der Abschnitt **Power Platform-Integration** bereits eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="20e59-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="20e59-120">Wenn es bereits festgelegt ist, sollte der Name der Dataverse-Umgebung, die mit der Finance -Umgebung verknüpft ist, aufgelistet sein.</span><span class="sxs-lookup"><span data-stu-id="20e59-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="20e59-121">Wenn sie nicht festgelegt ist, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="20e59-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="20e59-122">Wählen Sie im Abschnitt **Power Platform-Integration** die Option **Einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="20e59-123">Die Einrichtung der Umgebung kann bis zu einer Stunde dauern.</span><span class="sxs-lookup"><span data-stu-id="20e59-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="20e59-124">Wenn die Dataverse-Umgebung erfolgreich festgelegt wurde, sollte der Name der Dataverse-Umgebung, die mit der Finance-Umgebung verknüpft ist, aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="20e59-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="20e59-125">Nachdem Sie die Umgebungseinrichtung abgeschlossen haben, wählen Sie **nicht** den Link **Link zu CDS für Apps**.</span><span class="sxs-lookup"><span data-stu-id="20e59-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="20e59-126">Diese Schaltfläche ist für Finance insights nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="20e59-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="20e59-127">Wenn Sie sie auswählen, können Sie die erforderlichen Umgebungs-Add-Ins in LCS nicht konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="20e59-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="20e59-128">Azure konfigurieren</span><span class="sxs-lookup"><span data-stu-id="20e59-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="20e59-129">Die Azure Cloud Shell verwenden, um Financial Insights Data Lake-Ressourcen einzurichten</span><span class="sxs-lookup"><span data-stu-id="20e59-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="20e59-130">Verwenden eines Windows PowerShell-Konfigurationsskripts</span><span class="sxs-lookup"><span data-stu-id="20e59-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="20e59-131">Es wurde ein Windows PowerShell-Skript bereitgestellt, mit dem Sie die in [Konfigurieren des Exports nach Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) beschriebenen Azure-Ressourcen problemlos einrichten können.</span><span class="sxs-lookup"><span data-stu-id="20e59-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="20e59-132">Wenn Sie eine manuelle Einrichtung bevorzugen, überspringen Sie diesen Vorgang und schließen Sie stattdessen den Vorgang im Abschnitt [Manuelle Einrichtung](#manual-setup) durch.</span><span class="sxs-lookup"><span data-stu-id="20e59-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="20e59-133">Verwenden Sie das folgende Verfahren, um das Windows PowerShell-Skript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="20e59-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="20e59-134">Die Einrichtung funktioniert möglicherweise nicht, wenn Sie die Option **Testen** in der Azure CLI oder wenn Sie das Skript auf Ihrem Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="20e59-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="20e59-135">Führen Sie die folgenden Schritte aus, um Azure mithilfe des Windows PowerShell-Skripts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="20e59-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="20e59-136">Sie müssen über Rechte zum Erstellen einer Azure-Ressourcengruppe, von Azure-Ressourcen und einer Azure AD-Anwendung verfügen.</span><span class="sxs-lookup"><span data-stu-id="20e59-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="20e59-137">Informationen zu den erforderlichen Berechtigungen finden Sie unter [Prüfen der Azure AD-Berechtigungen](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="20e59-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="20e59-138">Wechseln Sie im [Azure-Portal](https://portal.azure.com) zu Ihrem Azure-Zielabonnement.</span><span class="sxs-lookup"><span data-stu-id="20e59-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="20e59-139">Wählen Sie **Cloud Shell** rechts neben dem **Suche**-Feld aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="20e59-140">Wählen Sie **Power Shell**.</span><span class="sxs-lookup"><span data-stu-id="20e59-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="20e59-141">Erstellen Sie eine Speicherung, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="20e59-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="20e59-142">Wählen Sie auf der Registerkarte **Azure CLI** die Option **Kopieren**.</span><span class="sxs-lookup"><span data-stu-id="20e59-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="20e59-143">Öffnen Sie in Notepad eine neue Datei, und fügen Sie das Windows PowerShell-Skript ein.</span><span class="sxs-lookup"><span data-stu-id="20e59-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="20e59-144">Speichern Sie die Datei als **ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="20e59-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="20e59-145">Laden Sie das Windows PowerShell-Skript in die Sitzung hoch, indem Sie die Menüoption zum Hochladen in Cloud Shell verwenden.</span><span class="sxs-lookup"><span data-stu-id="20e59-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="20e59-146">Führen Sie das Script **.\ConfigureDataLake.ps1** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="20e59-147">Befolgen Sie die Anweisungen, um das Skript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="20e59-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="20e59-148">Verwenden Sie die Informationen aus der Skriptausgabe, um das Add-In Export nach Data Lake in LCS zu installieren.</span><span class="sxs-lookup"><span data-stu-id="20e59-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="20e59-149">Manuelle Einrichtung</span><span class="sxs-lookup"><span data-stu-id="20e59-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="20e59-150">Dem Azure AD-Mandanten Anwendungen zum hinzufügen</span><span class="sxs-lookup"><span data-stu-id="20e59-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="20e59-151">Wechseln Sie im [Azure-Portal](https://portal.azure.com) zu **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="20e59-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="20e59-152">Wählen Sie **Verwalten \> Unternehmensanwendungen**.</span><span class="sxs-lookup"><span data-stu-id="20e59-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="20e59-153">Suchen Sie nach den folgenden Anwendungen anhand der App-ID.</span><span class="sxs-lookup"><span data-stu-id="20e59-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="20e59-154">Bewerbung</span><span class="sxs-lookup"><span data-stu-id="20e59-154">Application</span></span>                              | <span data-ttu-id="20e59-155">App-Kennung</span><span class="sxs-lookup"><span data-stu-id="20e59-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="20e59-156">Microsoft Dynamics ERP-Microservices</span><span class="sxs-lookup"><span data-stu-id="20e59-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="20e59-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="20e59-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="20e59-158">Microsoft Dynamics ERP-Microservices-CDS</span><span class="sxs-lookup"><span data-stu-id="20e59-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="20e59-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="20e59-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="20e59-160">AI Builder-Autorisierungsdienst</span><span class="sxs-lookup"><span data-stu-id="20e59-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="20e59-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="20e59-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="20e59-162">Wenn Sie keine der vorhergehenden Anwendungen finden können, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="20e59-163">Wählen Sie auf Ihrem lokalen Computer das Menü **Start** aus und suchen Sie nach **powershell**.</span><span class="sxs-lookup"><span data-stu-id="20e59-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="20e59-164">Wählen und halten Sie **Windows PowerShell** (oder klicken Sie mit der rechten Maustaste darauf) und wählen Sie dann **Als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="20e59-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="20e59-165">Führen Sie den folgenden Befehl aus, um das **AzureAD**-Modul zu installieren.</span><span class="sxs-lookup"><span data-stu-id="20e59-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="20e59-166">Wenn ein NuGet-Anbieter erforderlich ist, um fortzufahren, wählen Sie zum Installieren **J** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="20e59-167">Wenn die Meldung „Nicht vertrauenswürdiges Repository“ angezeigt wird, wählen Sie **J** aus, um weiterzumachen.</span><span class="sxs-lookup"><span data-stu-id="20e59-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="20e59-168">Führen Sie für jede Anwendung, die hinzugefügt werden muss, die folgenden Befehle aus, um die Anwendung in Azure AD hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="20e59-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="20e59-169">Wenn Sie dazu aufgefordert werden, melden Sie sich als Azure AD-Administrator an.</span><span class="sxs-lookup"><span data-stu-id="20e59-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="20e59-170">Azure-Ressourcen erstellen</span><span class="sxs-lookup"><span data-stu-id="20e59-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="20e59-171">Stellen Sie sicher, dass Sie die folgenden Ressourcen in derselben Azure AD-Instanz erstellen, in der sich die Dataverse-Umgebung befindet.</span><span class="sxs-lookup"><span data-stu-id="20e59-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="20e59-172">Sie können keine Ressourcen von keiner anderen Azure AD-Instanz verwenden.</span><span class="sxs-lookup"><span data-stu-id="20e59-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="20e59-173">Erstellen eines Speicherkontos:</span><span class="sxs-lookup"><span data-stu-id="20e59-173">Create a storage account:</span></span>

    1. <span data-ttu-id="20e59-174">Erstellen Sie im [Azure-Portal](https://portal.azure.com) ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="20e59-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="20e59-175">Legen Sie im Dialogfeld **Speicherkonto erstellen** die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="20e59-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="20e59-176">**Ort** – Wählen Sie das Rechenzentrum aus, in dem sich Ihre Umgebung befindet.</span><span class="sxs-lookup"><span data-stu-id="20e59-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="20e59-177">**Leistung** – Es wird empfohlen, dass Sie **Standard** auswählen.</span><span class="sxs-lookup"><span data-stu-id="20e59-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="20e59-178">**Art des Kontos** – Sie müssen **StorageV2** auswählen.</span><span class="sxs-lookup"><span data-stu-id="20e59-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="20e59-179">Wählen Sie im **Erweiterte Optionen**-Dialogfeld für die **Data Lake Storage Gen2**-Option **Aktivieren** unter der **Hierarchische Namespaces**-Funktion aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="20e59-180">Wenn Sie diese Funktion nicht deaktivieren, können Sie keine Daten nutzen, die von Finance and Operations-Apps geschrieben werden, indem Dienste wie Power BI-Datenflüsse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20e59-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="20e59-181">Wählen Sie **Überprüfen und erstellen**.</span><span class="sxs-lookup"><span data-stu-id="20e59-181">Select **Review and create**.</span></span> <span data-ttu-id="20e59-182">Nach Abschluss der Bereitstellung wird die neue Ressource im Azure-Portal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="20e59-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="20e59-183">Wechseln Sie zu dem von Ihnen erstellten Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="20e59-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="20e59-184">Wählen Sie im linken Menü **Zugriffsschlüssel** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="20e59-185">Kopieren und speichern Sie den Namen des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="20e59-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="20e59-186">Diesen Wert müssen Sie später beim Einrichten der Schlüsseltresorgeheimnisse angeben.</span><span class="sxs-lookup"><span data-stu-id="20e59-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="20e59-187">Erstellen eines neuen Schlüsseltresors:</span><span class="sxs-lookup"><span data-stu-id="20e59-187">Create a key vault:</span></span>

    1. <span data-ttu-id="20e59-188">Erstellen Sie im [Azure-Portal](https://portal.azure.com) einen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="20e59-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="20e59-189">Wählen Sie im **Einen Key Vault erstellen**-Dialogfeld im Feld **Ort** das Rechenzentrum aus, in dem sich Ihre Umgebung befindet.</span><span class="sxs-lookup"><span data-stu-id="20e59-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="20e59-190">Nachdem der Schlüsseltresor erstellt wurde, gehen Sie zu **Übersicht über den Schlüsseltresor**, und kopieren und speichern Sie den DNS-Namen.</span><span class="sxs-lookup"><span data-stu-id="20e59-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="20e59-191">Diesen Wert müssen Sie später beim Einrichten des Data Lake Add-ins angeben.</span><span class="sxs-lookup"><span data-stu-id="20e59-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="20e59-192">Erstellen und registrieren Sie eine Azure AD-Anwendung:</span><span class="sxs-lookup"><span data-stu-id="20e59-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="20e59-193">Wechseln Sie im [Azure-Portal](https://portal.azure.com) zu **Azure Active Directory** und wählen Sie dann **App-Registrierungen** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="20e59-194">Wählen Sie **Neue Anwendungsregistrierung** aus und legen Sie die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="20e59-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="20e59-195">**Name** – Geben Sie den Namen der App ein.</span><span class="sxs-lookup"><span data-stu-id="20e59-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="20e59-196">**Anwendungstyp** – Wählen Sie **Web-API** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="20e59-197">**URI-Setup umleiten** – Geben Sie die URL für Ihre Dynamics 365-Instanz ein, z. B. `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="20e59-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="20e59-198">Wechseln Sie zu der App, die Sie gerade erstellt haben, und kopieren und speichern Sie deren **Anwendungs-ID (Client-ID)**-Wert.</span><span class="sxs-lookup"><span data-stu-id="20e59-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="20e59-199">Diesen Wert müssen Sie später beim Einrichten der Schlüsseltresorgeheimnisse angeben.</span><span class="sxs-lookup"><span data-stu-id="20e59-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="20e59-200">Wechseln Sie zu **API-Berechtigungen** und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="20e59-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="20e59-201">Wählen Sie **Eine Berechtigung hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="20e59-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="20e59-202">Wählen Sie **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="20e59-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="20e59-203">Nachdem Sie delegierte Berechtigungen ausgewählt haben, wählen Sie **Benutzer\_Identitätswechsel**.</span><span class="sxs-lookup"><span data-stu-id="20e59-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="20e59-204">Wählen Sie **Berechtigungen hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="20e59-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="20e59-205">Wählen Sie im Menü für die App **Zertifikate \& Geheimnisse** aus und führen die folgenden Schritte aus, um die Key Vault-Geheimnisse zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="20e59-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="20e59-206">Wählen Sie **Neuer Clientschlüssel**.</span><span class="sxs-lookup"><span data-stu-id="20e59-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="20e59-207">Geben Sie im Feld **Schlüsselbeschreibung** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="20e59-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="20e59-208">Wählen Sie eine Dauer und wählen Sie dann **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="20e59-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="20e59-209">Ein Geheimnis wird im Feld **Wert** generiert.</span><span class="sxs-lookup"><span data-stu-id="20e59-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="20e59-210">Kopieren und speichern Sie den Wert des geheimen Clientschlüssels.</span><span class="sxs-lookup"><span data-stu-id="20e59-210">Copy and save the client secret value.</span></span> <span data-ttu-id="20e59-211">Diesen Wert müssen Sie später beim Einrichten der Schlüsseltresorgeheimnisse angeben.</span><span class="sxs-lookup"><span data-stu-id="20e59-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="20e59-212">Erstellen eines neuen Key Vault-Geheimnisses:</span><span class="sxs-lookup"><span data-stu-id="20e59-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="20e59-213">Wechseln Sie zu dem zuvor erstellten Key Vault und wählen Sie **Geheimnisse** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="20e59-214">Führen Sie für jeden geheimen Namen in der folgenden Tabelle die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="20e59-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="20e59-215">Wählen Sie **Generieren/Importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="20e59-216">Wählen Sie im Dialogfeld **Geheimnis erstellen** im Feld **Uploadoptionen** die Option **Manuell** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="20e59-217">Erstellen Sie den geheimen Namen und Wert aus der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="20e59-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="20e59-218">Wählen Sie **Aktiviert** und dann **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="20e59-219">Das Geheimnis wird erstellt und Key Vault hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="20e59-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="20e59-220">Geheimnisname</span><span class="sxs-lookup"><span data-stu-id="20e59-220">Secret name</span></span>                       | <span data-ttu-id="20e59-221">Geheimer Wert</span><span class="sxs-lookup"><span data-stu-id="20e59-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="20e59-222">app-id</span><span class="sxs-lookup"><span data-stu-id="20e59-222">app-id</span></span>                            | <span data-ttu-id="20e59-223">Die App-ID der zuvor erstellten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="20e59-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="20e59-224">app-secret</span><span class="sxs-lookup"><span data-stu-id="20e59-224">app-secret</span></span>                        | <span data-ttu-id="20e59-225">Der Clientschlüssel, den Sie zuvor gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="20e59-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="20e59-226">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="20e59-226">storage-account-name</span></span>              | <span data-ttu-id="20e59-227">Der Name des Speicherkontos, das Sie zuvor erstellt haben, z. B. **storageaccount1**.</span><span class="sxs-lookup"><span data-stu-id="20e59-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="20e59-228">Autorisieren Sie die Anwendung für den Zugriff auf den Schlüsseldepot:</span><span class="sxs-lookup"><span data-stu-id="20e59-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="20e59-229">Öffnen Sie im [Azure-Portal](https://portal.azure.com) den zuvor erstellten Key Vault.</span><span class="sxs-lookup"><span data-stu-id="20e59-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="20e59-230">Wählen Sie die Zugriffsrichtlinien aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-230">Select the access policies.</span></span>
    3. <span data-ttu-id="20e59-231">Führen Sie für jede Anwendung in der folgenden Tabelle die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="20e59-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="20e59-232">Wählen Sie **Zugriffsrichtlinie hinzufügen**, um eine Zugriffsrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="20e59-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="20e59-233">Wählen Sie im Feld **Geheimnisberechtigungen** die Berechtigungen aus der Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="20e59-234">Suchen Sie im Feld **Prinzipal auswählen** nach dem Anzeigenamen der Anwendung in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="20e59-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="20e59-235">Wählen Sie **Auswählen**.</span><span class="sxs-lookup"><span data-stu-id="20e59-235">Select **Select**.</span></span>
        5. <span data-ttu-id="20e59-236">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-236">Select **Add**.</span></span>
        6. <span data-ttu-id="20e59-237">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-237">Select **Save**.</span></span>

        | <span data-ttu-id="20e59-238">Bewerbung</span><span class="sxs-lookup"><span data-stu-id="20e59-238">Application</span></span>                                              | <span data-ttu-id="20e59-239">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="20e59-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="20e59-240">Der Anzeigename der neu erstellten Anwendung</span><span class="sxs-lookup"><span data-stu-id="20e59-240">The display name of the new application that you created</span></span> | <span data-ttu-id="20e59-241">Get, List</span><span class="sxs-lookup"><span data-stu-id="20e59-241">Get, List</span></span>   |
        | <span data-ttu-id="20e59-242">**Microsoft Dynamics-ERP-Microservices**</span><span class="sxs-lookup"><span data-stu-id="20e59-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="20e59-243">Get, List</span><span class="sxs-lookup"><span data-stu-id="20e59-243">Get, List</span></span>   |

6. <span data-ttu-id="20e59-244">Weisen Sie Rollen zu, um auf das Speicherkonto zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="20e59-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="20e59-245">Öffnen Sie im [Azure-Portal](https://portal.azure.com) das zuvor erstellte Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="20e59-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="20e59-246">Wählen Sie **Zugriffssteuerung (IAM)** und dann **Rollenzuweisungen** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="20e59-247">Wählen Sie **Hinzufügen, Rollenzuweisung hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="20e59-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="20e59-248">Führen Sie für jede Anwendung in der folgenden Tabelle die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="20e59-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="20e59-249">Wählen Sie die Rolle aus der Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="20e59-250">Lassen Sie das Feld **Zugriff gewähren auf** auf **Azure AD-Benutzer, -Gruppe oder -Serviceprinzipal**.</span><span class="sxs-lookup"><span data-stu-id="20e59-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="20e59-251">Geben Sie im Feld **Geheimnis** die Anwendung aus der Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="20e59-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="20e59-252">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-252">Select **Save**.</span></span>

        | <span data-ttu-id="20e59-253">Bewerbung</span><span class="sxs-lookup"><span data-stu-id="20e59-253">Application</span></span>                                              | <span data-ttu-id="20e59-254">Rolle</span><span class="sxs-lookup"><span data-stu-id="20e59-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="20e59-255">Der Anzeigename der neu erstellten Anwendung</span><span class="sxs-lookup"><span data-stu-id="20e59-255">The display name of the new application that you created</span></span> | <span data-ttu-id="20e59-256">Eigentümer</span><span class="sxs-lookup"><span data-stu-id="20e59-256">Owner</span></span>                       |
        | <span data-ttu-id="20e59-257">Der Anzeigename der neu erstellten Anwendung</span><span class="sxs-lookup"><span data-stu-id="20e59-257">The display name of the new application that you created</span></span> | <span data-ttu-id="20e59-258">Mitwirkender</span><span class="sxs-lookup"><span data-stu-id="20e59-258">Contributor</span></span>                 |
        | <span data-ttu-id="20e59-259">Der Anzeigename der neu erstellten Anwendung</span><span class="sxs-lookup"><span data-stu-id="20e59-259">The display name of the new application that you created</span></span> | <span data-ttu-id="20e59-260">Mitwirkender am Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="20e59-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="20e59-261">Der Anzeigename der neu erstellten Anwendung</span><span class="sxs-lookup"><span data-stu-id="20e59-261">The display name of the new application that you created</span></span> | <span data-ttu-id="20e59-262">Datenbesitzer des Speicher-Blobs</span><span class="sxs-lookup"><span data-stu-id="20e59-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="20e59-263">**AI Builder-Autorisierungsdienst**</span><span class="sxs-lookup"><span data-stu-id="20e59-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="20e59-264">Datenleser des Speicher-Blobs</span><span class="sxs-lookup"><span data-stu-id="20e59-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="20e59-265">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="20e59-265">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="20e59-266">Export in Data Lake Add-in konfigurieren</span><span class="sxs-lookup"><span data-stu-id="20e59-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="20e59-267">Führen Sie die folgenden Schritte aus, um der Umgebung mithilfe von LCS den Export in das Data Lake-Add-In hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="20e59-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="20e59-268">Melden Sie sich bei LCS an und wählen Sie dann unter dem Umgebungsnamen auf der rechten Seite der Seite **Alle Einzelheiten** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="20e59-269">Wählen Sie Im Abschnitt **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="20e59-270">Wählen Sie das **Export nach Data Lake**-Add-In.</span><span class="sxs-lookup"><span data-stu-id="20e59-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="20e59-271">Geben Sie die folgenden Werte ein.</span><span class="sxs-lookup"><span data-stu-id="20e59-271">Enter the following values.</span></span>

    | <span data-ttu-id="20e59-272">Wert</span><span class="sxs-lookup"><span data-stu-id="20e59-272">Value</span></span>                                                              | <span data-ttu-id="20e59-273">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20e59-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="20e59-274">Mandanten-ID des Azure-Abonnements, in dem sich der Key Vault befindet</span><span class="sxs-lookup"><span data-stu-id="20e59-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="20e59-275">Die Mandanten-ID, in der sich das Speicherkonto, die Apps und die Key Vaults befinden.</span><span class="sxs-lookup"><span data-stu-id="20e59-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="20e59-276">Um diesen Wert zu finden, öffnen Sie das [Azure-Portal](https://portal.azure.com), wechseln Sie zu **Azure Active Directory** und kopieren Sie den **Mandanten-ID**-Wert.</span><span class="sxs-lookup"><span data-stu-id="20e59-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="20e59-277">DNS-Namen Ihres Key Vault angeben</span><span class="sxs-lookup"><span data-stu-id="20e59-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="20e59-278">Der DNS-Name des Key Vaults, z. B. `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="20e59-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="20e59-279">Geben Sie das Geheimnis an, das den Namen des Speicherkontos enthält</span><span class="sxs-lookup"><span data-stu-id="20e59-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="20e59-280">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="20e59-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="20e59-281">Geheimname für die App-ID für den Zugriff auf Data Lake</span><span class="sxs-lookup"><span data-stu-id="20e59-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="20e59-282">**app-id**</span><span class="sxs-lookup"><span data-stu-id="20e59-282">**app-id**</span></span> |
    | <span data-ttu-id="20e59-283">Geheimname für geheimen Clientschlüssel für die App</span><span class="sxs-lookup"><span data-stu-id="20e59-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="20e59-284">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="20e59-284">**app-secret**</span></span> |

5. <span data-ttu-id="20e59-285">Stimmen Sie den Bedingungen zu und wählen Sie dann **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="20e59-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="20e59-286">Das Add-In wird innerhalb weniger Minuten installiert.</span><span class="sxs-lookup"><span data-stu-id="20e59-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="20e59-287">Finance Insights Add-in konfigurieren</span><span class="sxs-lookup"><span data-stu-id="20e59-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="20e59-288">Wenn Sie das Get Insights Add-In bereits installiert haben, deinstallieren Sie es, bevor Sie das folgende Verfahren ausführen.</span><span class="sxs-lookup"><span data-stu-id="20e59-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="20e59-289">Führen Sie diese Schritte aus, um das Finance Insights-Add-In zu installieren.</span><span class="sxs-lookup"><span data-stu-id="20e59-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="20e59-290">Melden Sie sich bei LCS an und wählen Sie dann unter dem Umgebungsnamen auf der rechten Seite der Seite **Alle Einzelheiten** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="20e59-291">Wählen Sie Im Abschnitt **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="20e59-292">Wählen Sie das **Finance insights**-Add-In aus.</span><span class="sxs-lookup"><span data-stu-id="20e59-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="20e59-293">Stimmen Sie den Bedingungen zu und wählen Sie dann **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="20e59-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="20e59-294">Feedback und Support</span><span class="sxs-lookup"><span data-stu-id="20e59-294">Feedback and support</span></span>

<span data-ttu-id="20e59-295">Wenn Sie an Feedback interessiert sind oder Support benötigen, senden Sie eine E-Mail an [Finance insights (Vorschau)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="20e59-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
