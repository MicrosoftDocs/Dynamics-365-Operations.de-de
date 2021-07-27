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
ms.openlocfilehash: eeb3061f215666d0aeb32094b5d04a9ae6e618f2
ms.sourcegitcommit: f6050b444e636ba662c00d0443c94a99f8ea0b0d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/28/2021
ms.locfileid: "6309664"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a>Konfiguration für Finance Insights für die öffentliche Vorschau (Vorschau) – Version 10.0.20 und höher

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Finance Insights kombiniert Funktionen von Microsoft Dynamics 365 Finance mit Dataverse, Azure und AI Builder, um leistungsstarke Prognosetools für Ihr Unternehmen zu bieten. In diesem Thema wird die Konfiguration von Dynamics 365 Finance Version 10.0.20 erläutert, mit denen Ihr System die in der öffentlichen Vorschau von Finance Insights verfügbaren Funktionen nutzen kann.

> [!NOTE]
> Die in diesem Thema beschriebenen Konfigurationsschritte gelten nur für Finance Version 10.0.20 und höher. Informationen zum Einrichten von Finance Insights in Version 10.0.19 und früher finden Sie unter [Konfiguration für Finance Insights – Versionen 10.0.19](configure-for-fin-insites.md).

## <a name="deploy-finance"></a>Finance bereitstellen

Gehen Sie folgendermaßen vor, um die Umgebungen bereitzustellen.

1. Erstellen oder aktualisieren Sie im Microsoft Dynamics Lifecycle Services (LCS) eine Finance-Umgebung. Die Umgebung erfordert App-Version 10.0.20 oder höher der Finance and Operations-Apps.
2. Die Umgebung muss eine Hochverfügbarkeitsumgebung (HA) in einer Sandbox sein. (Diese Art von Umgebung wird auch als Ebene-2-Umgebung bezeichnet.) Weitere Informationen finden Sie unter [Umgebungsplanung](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Wenn Sie Finance Insights in einer Sandbox-Umgebung konfigurieren, müssen Sie möglicherweise Produktionsdaten in diese Umgebung kopieren, damit Vorhersagen funktionieren. Das Vorhersagemodell verwendet Daten aus mehreren Jahren, um Vorhersagen zu erstellen. Die Contoso Demodaten enthalten nicht genügend historische Daten, um das Vorhersagemodell angemessen zu trainieren. 

## <a name="configure-dataverse"></a>Dataverse konfigurieren

Gehen Sie folgendernamßen vor, um Dataverse für Finance Insights zu konfigurieren.

1. Öffnen Sie die Seite „Umgebung“ in LCS und überprüfen Sie, ob der Abschnitt **Power Platform-Integration** bereits eingerichtet ist.

    - Wenn es bereits festgelegt ist, sollte der Name der Dataverse-Umgebung, die mit der Finance -Umgebung verknüpft ist, aufgelistet sein.
    - Wenn sie nicht festgelegt ist, gehen Sie wie folgt vor:

        1. Wählen Sie im Abschnitt **Power Platform-Integration** die Option **Einrichten** aus. Die Einrichtung der Umgebung kann bis zu einer Stunde dauern.
        2. Wenn die Dataverse-Umgebung erfolgreich festgelegt wurde, sollte der Name der Dataverse-Umgebung, die mit der Finance-Umgebung verknüpft ist, aufgelistet werden.

        > [!NOTE]
        > Nachdem Sie die Umgebungseinrichtung abgeschlossen haben, wählen Sie **nicht** den Link **Link zu CDS für Apps**. Diese Schaltfläche ist für Finance insights nicht erforderlich. Wenn Sie sie auswählen, können Sie die erforderlichen Umgebungs-Add-Ins in LCS nicht konfigurieren.

## <a name="configure-azure"></a>Azure konfigurieren

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Die Azure Cloud Shell verwenden, um Financial Insights Data Lake-Ressourcen einzurichten

# <a name="use-a-windows-powershell-script"></a>[Verwenden eines Windows PowerShell-Konfigurationsskripts](#tab/use-a-powershell-script)

Es wurde ein Windows PowerShell-Skript bereitgestellt, mit dem Sie die in [Konfigurieren des Exports nach Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) beschriebenen Azure-Ressourcen problemlos einrichten können. Wenn Sie eine manuelle Einrichtung bevorzugen, überspringen Sie diesen Vorgang und schließen Sie stattdessen den Vorgang im Abschnitt [Manuelle Einrichtung](#manual-setup) durch.

> [!NOTE]
> Verwenden Sie das folgende Verfahren, um das Windows PowerShell-Skript auszuführen. Die Einrichtung funktioniert möglicherweise nicht, wenn Sie die Option **Testen** in der Azure CLI oder wenn Sie das Skript auf Ihrem Computer ausführen.

Führen Sie die folgenden Schritte aus, um Azure mithilfe des Windows PowerShell-Skripts zu konfigurieren. Sie müssen über Rechte zum Erstellen einer Azure-Ressourcengruppe, von Azure-Ressourcen und einer Azure AD-Anwendung verfügen. Informationen zu den erforderlichen Berechtigungen finden Sie unter [Prüfen der Azure AD-Berechtigungen](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. Wechseln Sie im [Azure-Portal](https://portal.azure.com) zu Ihrem Azure-Zielabonnement.
2. Wählen Sie **Cloud Shell** rechts neben dem **Suche**-Feld aus.
3. Wählen Sie **Power Shell**.
4. Erstellen Sie eine Speicherung, wenn Sie dazu aufgefordert werden.
5. Wählen Sie auf der Registerkarte **Azure CLI** die Option **Kopieren**.
6. Öffnen Sie in Notepad eine neue Datei, und fügen Sie das Windows PowerShell-Skript ein.
7. Speichern Sie die Datei als **ConfigureDataLake.ps1**.
8. Laden Sie das Windows PowerShell-Skript in die Sitzung hoch, indem Sie die Menüoption zum Hochladen in Cloud Shell verwenden.
9. Führen Sie das Script **.\ConfigureDataLake.ps1** aus.
10. Befolgen Sie die Anweisungen, um das Skript auszuführen.
11. Verwenden Sie die Informationen aus der Skriptausgabe, um das Add-In Export nach Data Lake in LCS zu installieren.

### <a name="manual-setup"></a>Manuelle Einrichtung

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Dem Azure AD-Mandanten Anwendungen zum hinzufügen

1. Wechseln Sie im [Azure-Portal](https://portal.azure.com) zu **Azure Active Directory**.
2. Wählen Sie **Verwalten \> Unternehmensanwendungen**.
3. Suchen Sie nach den folgenden Anwendungen anhand der App-ID.

    | Bewerbung                              | App-Kennung                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP-Microservices     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP-Microservices-CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | AI Builder-Autorisierungsdienst         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

Wenn Sie keine der vorhergehenden Anwendungen finden können, führen Sie die folgenden Schritte aus.

1. Wählen Sie auf Ihrem lokalen Computer das Menü **Start** aus und suchen Sie nach **powershell**.
2. Wählen und halten Sie **Windows PowerShell** (oder klicken Sie mit der rechten Maustaste darauf) und wählen Sie dann **Als Administrator ausführen**.
3. Führen Sie den folgenden Befehl aus, um das **AzureAD**-Modul zu installieren.

    `Install-Module -Name AzureAD`

4. Wenn ein NuGet-Anbieter erforderlich ist, um fortzufahren, wählen Sie zum Installieren **J** aus.
5. Wenn die Meldung „Nicht vertrauenswürdiges Repository“ angezeigt wird, wählen Sie **J** aus, um weiterzumachen.
6. Führen Sie für jede Anwendung, die hinzugefügt werden muss, die folgenden Befehle aus, um die Anwendung in Azure AD hinzuzufügen. Wenn Sie dazu aufgefordert werden, melden Sie sich als Azure AD-Administrator an.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Azure-Ressourcen erstellen

> [!NOTE]
> Stellen Sie sicher, dass Sie die folgenden Ressourcen in derselben Azure AD-Instanz erstellen, in der sich die Dataverse-Umgebung befindet. Sie können keine Ressourcen von keiner anderen Azure AD-Instanz verwenden.

1. Erstellen eines Speicherkontos:

    1. Erstellen Sie im [Azure-Portal](https://portal.azure.com) ein Speicherkonto.
    2. Legen Sie im Dialogfeld **Speicherkonto erstellen** die folgenden Felder fest:

        - **Ort** – Wählen Sie das Rechenzentrum aus, in dem sich Ihre Umgebung befindet.
        - **Leistung** – Es wird empfohlen, dass Sie **Standard** auswählen.
        - **Art des Kontos** – Sie müssen **StorageV2** auswählen.

    3. Wählen Sie im **Erweiterte Optionen**-Dialogfeld für die **Data Lake Storage Gen2**-Option **Aktivieren** unter der **Hierarchische Namespaces**-Funktion aus. Wenn Sie diese Funktion nicht deaktivieren, können Sie keine Daten nutzen, die von Finance and Operations-Apps geschrieben werden, indem Dienste wie Power BI-Datenflüsse verwendet werden.
    4. Wählen Sie **Überprüfen und erstellen**. Nach Abschluss der Bereitstellung wird die neue Ressource im Azure-Portal angezeigt.
    5. Wechseln Sie zu dem von Ihnen erstellten Speicherkonto.
    6. Wählen Sie im linken Menü **Zugriffsschlüssel** aus.
    7. Kopieren und speichern Sie den Namen des Speicherkontos. Diesen Wert müssen Sie später beim Einrichten der Schlüsseltresorgeheimnisse angeben.

2. Erstellen eines neuen Schlüsseltresors:

    1. Erstellen Sie im [Azure-Portal](https://portal.azure.com) einen Schlüsseltresor.
    2. Wählen Sie im **Einen Key Vault erstellen**-Dialogfeld im Feld **Ort** das Rechenzentrum aus, in dem sich Ihre Umgebung befindet.
    3. Nachdem der Schlüsseltresor erstellt wurde, gehen Sie zu **Übersicht über den Schlüsseltresor**, und kopieren und speichern Sie den DNS-Namen. Diesen Wert müssen Sie später beim Einrichten des Data Lake Add-ins angeben.

3. Erstellen und registrieren Sie eine Azure AD-Anwendung:

    1. Wechseln Sie im [Azure-Portal](https://portal.azure.com) zu **Azure Active Directory** und wählen Sie dann **App-Registrierungen** aus.
    2. Wählen Sie **Neue Anwendungsregistrierung** aus und legen Sie die folgenden Felder fest:

        - **Name** – Geben Sie den Namen der App ein.
        - **Anwendungstyp** – Wählen Sie **Web-API** aus.
        - **URI-Setup umleiten** – Geben Sie die URL für Ihre Dynamics 365-Instanz ein, z. B. `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Wechseln Sie zu der App, die Sie gerade erstellt haben, und kopieren und speichern Sie deren **Anwendungs-ID (Client-ID)**-Wert. Diesen Wert müssen Sie später beim Einrichten der Schlüsseltresorgeheimnisse angeben.
    4. Wechseln Sie zu **API-Berechtigungen** und befolgen Sie diese Schritte:

        1. Wählen Sie **Eine Berechtigung hinzufügen**.
        2. Wählen Sie **Azure Key Vault**.
        3. Nachdem Sie delegierte Berechtigungen ausgewählt haben, wählen Sie **Benutzer\_Identitätswechsel**.
        4. Wählen Sie **Berechtigungen hinzufügen**.

    5. Wählen Sie im Menü für die App **Zertifikate \& Geheimnisse** aus und führen die folgenden Schritte aus, um die Key Vault-Geheimnisse zu erstellen:

        1. Wählen Sie **Neuer Clientschlüssel**.
        2. Geben Sie im Feld **Schlüsselbeschreibung** einen Namen ein.
        3. Wählen Sie eine Dauer und wählen Sie dann **Hinzufügen**. Ein Geheimnis wird im Feld **Wert** generiert.
        4. Kopieren und speichern Sie den Wert des geheimen Clientschlüssels. Diesen Wert müssen Sie später beim Einrichten der Schlüsseltresorgeheimnisse angeben.

4. Erstellen eines neuen Key Vault-Geheimnisses:

    1. Wechseln Sie zu dem zuvor erstellten Key Vault und wählen Sie **Geheimnisse** aus.
    2. Führen Sie für jeden geheimen Namen in der folgenden Tabelle die folgenden Schritte aus:

        1. Wählen Sie **Generieren/Importieren** aus.
        2. Wählen Sie im Dialogfeld **Geheimnis erstellen** im Feld **Uploadoptionen** die Option **Manuell** aus.
        3. Erstellen Sie den geheimen Namen und Wert aus der Tabelle.
        4. Wählen Sie **Aktiviert** und dann **Erstellen** aus. Das Geheimnis wird erstellt und Key Vault hinzugefügt.

        | Geheimnisname                       | Geheimer Wert                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | app-id                            | Die App-ID der zuvor erstellten Anwendung.                                      |
        | app-secret                        | Der Clientschlüssel, den Sie zuvor gespeichert haben.                                                    |
        | storage-account-name              | Der Name des Speicherkontos, das Sie zuvor erstellt haben, z. B. **storageaccount1**.       |

5. Autorisieren Sie die Anwendung für den Zugriff auf den Schlüsseldepot:

    1. Öffnen Sie im [Azure-Portal](https://portal.azure.com) den zuvor erstellten Key Vault.
    2. Wählen Sie die Zugriffsrichtlinien aus.
    3. Führen Sie für jede Anwendung in der folgenden Tabelle die folgenden Schritte aus:

        1. Wählen Sie **Zugriffsrichtlinie hinzufügen**, um eine Zugriffsrichtlinie zu erstellen.
        2. Wählen Sie im Feld **Geheimnisberechtigungen** die Berechtigungen aus der Tabelle aus.
        3. Suchen Sie im Feld **Prinzipal auswählen** nach dem Anzeigenamen der Anwendung in der Tabelle.
        4. Wählen Sie **Auswählen**.
        5. Wählen Sie **Hinzufügen** aus.
        6. Wählen Sie **Speichern** aus.

        | Bewerbung                                              | Berechtigungen |
        |----------------------------------------------------------|-------------|
        | Der Anzeigename der neu erstellten Anwendung | Get, List   |
        | **Microsoft Dynamics-ERP-Microservices**                 | Get, List   |

6. Weisen Sie Rollen zu, um auf das Speicherkonto zuzugreifen:

    1. Öffnen Sie im [Azure-Portal](https://portal.azure.com) das zuvor erstellte Speicherkonto.
    2. Wählen Sie **Zugriffssteuerung (IAM)** und dann **Rollenzuweisungen** aus.
    3. Wählen Sie **Hinzufügen, Rollenzuweisung hinzufügen**.
    4. Führen Sie für jede Anwendung in der folgenden Tabelle die folgenden Schritte aus:

        1. Wählen Sie die Rolle aus der Tabelle aus.
        2. Lassen Sie das Feld **Zugriff gewähren auf** auf **Azure AD-Benutzer, -Gruppe oder -Serviceprinzipal**.
        3. Geben Sie im Feld **Geheimnis** die Anwendung aus der Tabelle ein.
        4. Wählen Sie **Speichern** aus.

        | Bewerbung                                              | Rolle                        |
        |----------------------------------------------------------|-----------------------------|
        | Der Anzeigename der neu erstellten Anwendung | Eigentümer                       |
        | Der Anzeigename der neu erstellten Anwendung | Mitwirkender                 |
        | Der Anzeigename der neu erstellten Anwendung | Mitwirkender am Speicherkonto |
        | Der Anzeigename der neu erstellten Anwendung | Datenbesitzer des Speicher-Blobs     |
        | **AI Builder-Autorisierungsdienst**                     | Datenleser des Speicher-Blobs    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a>Export in Data Lake Add-in konfigurieren

Führen Sie die folgenden Schritte aus, um der Umgebung mithilfe von LCS den Export in das Data Lake-Add-In hinzuzufügen.

1. Melden Sie sich bei LCS an und wählen Sie dann unter dem Umgebungsnamen auf der rechten Seite der Seite **Alle Einzelheiten** aus.
2. Wählen Sie Im Abschnitt **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.
3. Wählen Sie das **Export nach Data Lake**-Add-In.
4. Geben Sie die folgenden Werte ein.

    | Wert                                                              | Beschreibung |
    |--------------------------------------------------------------------|-------------|
    | Mandanten-ID des Azure-Abonnements, in dem sich der Key Vault befindet | Die Mandanten-ID, in der sich das Speicherkonto, die Apps und die Key Vaults befinden. Um diesen Wert zu finden, öffnen Sie das [Azure-Portal](https://portal.azure.com), wechseln Sie zu **Azure Active Directory** und kopieren Sie den **Mandanten-ID**-Wert. |
    | DNS-Namen Ihres Key Vault angeben                             | Der DNS-Name des Key Vaults, z. B. `https://customkeyvault.vault.azure.net/`. |
    | Geben Sie das Geheimnis an, das den Namen des Speicherkontos enthält   | **storage-account-name** |
    | Geheimname für die App-ID für den Zugriff auf Data Lake          | **app-id** |
    | Geheimname für geheimen Clientschlüssel für die App                                  | **app-secret** |

5. Stimmen Sie den Bedingungen zu und wählen Sie dann **Installieren**.

Das Add-In wird innerhalb weniger Minuten installiert.

## <a name="configure-the-finance-insights-add-in"></a>Finance Insights Add-in konfigurieren

> [!NOTE]
> Wenn Sie das Get Insights Add-In bereits installiert haben, deinstallieren Sie es, bevor Sie das folgende Verfahren ausführen.

Führen Sie diese Schritte aus, um das Finance Insights-Add-In zu installieren.

1. Melden Sie sich bei LCS an und wählen Sie dann unter dem Umgebungsnamen auf der rechten Seite der Seite **Alle Einzelheiten** aus.
2. Wählen Sie Im Abschnitt **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.
3. Wählen Sie das **Finance insights**-Add-In aus.
4. Stimmen Sie den Bedingungen zu und wählen Sie dann **Installieren**.

Die Installation des Add-Ins kann einige Minuten dauern.

## <a name="feedback-and-support"></a>Feedback und Support

Wenn Sie an Feedback interessiert sind oder Support benötigen, senden Sie eine E-Mail an [Finance insights (Vorschau)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
