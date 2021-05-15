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
# <a name="configuration-for-finance-insights-preview"></a>Konfiguration für Finance Insights (Vorschau)

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Finance Insights kombiniert Funktionen von Microsoft Dynamics 365 Finance mit Microsoft Dataverse, Azure und AI Builder, um leistungsstarke Prognosetools für Ihr Unternehmen zu bieten. In diesem Thema werden die Konfigurationsschritte erläutert, mit denen Ihr System die in Finance Insights verfügbaren Funktionen nutzen kann.

## <a name="deploy-dynamics-365-finance"></a>Bereitstellung von Dynamics 365 Finance

Stellen Sie die Umgebungen bereit, indem Sie die folgenden Schritte ausführen.

1. Im Microsoft Dynamics Lifecycle Services (LCS) erstellen oder aktualisieren Sie eine Dynamics 365 Finance-Umgebung. Die Umgebung erfordert das App-Version 10.0.11/Plattform-Update 35 oder höher.
2. Die Umgebung muss eine Hochverfügbarkeitsumgebung (HA) in einer Sandbox sein. (Diese Art von Umgebung wird auch als Ebene-2-Umgebung bezeichnet.) Weitere Informationen finden Sie unter [Umgebungsplanung](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Wenn Sie Contoso-Demodaten verwenden, benötigen Sie zusätzliche Beispieldaten, um die Funktionen Zahlungsvorhersagen für Kunden, Cashflow-Planungen und Budgetprognosen verwenden zu können. 

## <a name="configure-dataverse"></a>Dataverse konfigurieren

Verwenden Sie die folgenden Schritte, um Dataverse für Finance Insights zu konfigurieren.

1. Öffnen Sie die Seite „Umgebung“ in LCS und überprüfen Sie, ob der Abschnitt **Power Platform-Integration** bereits eingerichtet ist.
    1. Wenn es bereits festgelegt ist, sollte der Name der Dataverse-Umgebung, die mit der Dynamics 365 Finance-Umgebung verknüpft ist, aufgelistet sein. Kopieren Sie den Namen der Dataverse-Umgebung.
    2. Wenn sie nicht festgelegt ist, gehen Sie wie folgt vor:
        1. Wählen Sie die Schaltfläche **Einrichten** im Bereich Power Platform Integration. Es kann bis zu einer Stunde dauern, bis die Umgebung festgelegt ist.
        2. Wenn die Dataverse-Umgebung erfolgreich festgelegt wurde, sollte der Name der Dataverse-Umgebung, die mit der Dynamics 365 Finance-Umgebung verknüpft ist, aufgelistet werden. Kopieren Sie den Namen der Dataverse-Umgebung.
> [!NOTE]
> Nachdem Sie die Umgebung festgelegt haben, wählen Sie **NICHT** die Schaltfläche **Verbindung zu CDS für Apps**. Dies wird für Finance Insights nicht benötigt und deaktiviert die Möglichkeit, die erforderlichen Umgebungs-Add-Ins in LCS zu vervollständigen.

2. Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/) und befolgen Sie diese Schritte, um eine neue Dataverse-Umgebung im selben Active Directory-Mandanten zu erstellen:

    1. Öffnen Sie der Seite **Umgebungen**.

        [![Umgebungen-Seite](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. Wählen Sie die oben erstellte Dataverse-Umgebung und wählen Sie dann **Einstellungen**.
    3. Wählen Sie **Ressourcen \> Alle Legacy-Einstellungen**.
    4. Wählen Sie in der oberen Navigationsleiste **Einstellungen** und dann **Anpassungen**.
    5. Wählen Sie **Entwicklerressourcen**.
    6. Kopieren Sie den Wert der **Dataverse-Organisations-ID** ein.
    7. Notieren Sie sich in der Adressleiste des Browsers die URL der Dataverse-Organisation. Zum Beispiel könnte die URL `https://org42b2b3d3.crm.dynamics.com` lauten.

3. Wenn Sie die Funktion „Cashflow-Planung“ oder „Budget-Plaung“ verwenden möchten, führen Sie die folgenden Schritte aus, um das Anmerkungslimit für Ihre Organisation auf mindestens 50 Megabyte (MB) zu aktualisieren:

    1. Öffnen Sie das [Power Apps-Portal](https://make.powerapps.com).
    2. Wählen Sie die gerade erstellte Umgebung dann **Erweiterte Einstellungen** aus.
    3. Wählen Sie **Einstellungen \> E-Mail-Konfiguration**.
    4. Ändern Sie den Wert des Felds **Maximale Dateigröße** auf **51.200**. (Der Wert wird in Kilobyte \[KB\] angegeben.)
    5. Wählen Sie **OK** aus, um Ihre Änderungen zu speichern.

## <a name="configure-the-azure-setup"></a>Azure-Einrichtung konfigurieren

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a>Die Dataverse-Verzeichnis-ID und die Azure AD-Objekt-DI des Benutzers eingeben

1. Geben Sie die Dataverse-Verzeichnis-ID ein:

    1. Öffnen Sie das [Azure-Portal](https://portal.azure.com).
    2. Melden Sie sich mit der Benutzer-ID an, mit der die Dataverse-Umgebung erstellt wurde.
    3. Gehe zu **Azure Active Directory**.
    4. Kopieren Sie den **Mieter-ID**-Wert.

2. Geben Sie die Azure Active Directory (Azure AD)-Objekt-ID des Benutzers ein:

    1. Wechseln Sie im [Azure-Portal](https://portal.azure.com) zu **Benutzer** und suchen Sie den Benutzer anhand der E-Mail-Adresse.
    2. Wählen Sie den Namen des Benutzers aus.
    3. Kopieren Sie den **Objekt-ID**-Wert.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Die Azure Cloud Shell verwenden, um Financial Insights Data Lake-Ressourcen einzurichten

# <a name="use-a-windows-powershell-script"></a>[Verwenden eines Windows PowerShell-Konfigurationsskripts](#tab/use-a-powershell-script)

Es wurde ein Windows PowerShell-Skript bereitgestellt, mit dem Sie die in [Konfigurieren des Exports nach Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) beschriebenen Azure-Ressourcen problemlos einrichten können. Wenn Sie eine manuelle Einrichtung bevorzugen, überspringen Sie diesen Vorgang und fahren Sie mit dem Vorgang im Abschnitt [Manuelle Einrichtung](#manual-setup) fort.

> [!NOTE]
> Führen Sie die folgenden Schritte aus, um das PowerShell-Skript auszuführen: Die Azure CLI-Option „Try it“ oder das Ausführen des Skripts auf Ihrem PC funktioniert möglicherweise nicht.

Führen Sie die folgenden Schritte aus, um Azure mithilfe des Windows PowerShell-Skripts zu konfigurieren. Sie müssen über Rechte zum Erstellen einer Azure-Ressourcengruppe, von Azure-Ressourcen und einer Azure AD-Anwendung verfügen. Informationen zu den erforderlichen Berechtigungen finden Sie unter [Prüfen der Azure AD-Berechtigungen](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. Wechseln Sie im [Azure-Portal](https://portal.azure.com) zu Ihrem Azure-Zielabonnement. Wählen Sie die **Cloud Shell**-Schaltfläche rechts neben dem **Suche**-Feld aus.
2. Wählen Sie **Power Shell**.
3. Erstellen Sie eine Speicherung, wenn Sie dazu aufgefordert werden.
4. Gehen Sie auf die Registerkarte **Azure CLI** und wählen Sie **Kopieren**.  
5. Öffnen Sie Notepad und fügen Sie das PowerShell-Skript ein. Speichern Sie die Datei als ConfigureDataLake.ps1.
6. Laden Sie das Windows PowerShell-Skript in die Sitzung hoch, indem Sie die Menüoption zum Hochladen in Cloud Shell verwenden.
7. Führen Sie das Script .\ConfigureDataLake.ps1 aus.
8. Befolgen Sie die Anweisungen, um das Skript auszuführen.
9. Verwenden Sie die Informationen aus der Skriptausgabe, um das Add-In **Export nach Data Lake** in LCS zu installieren.
10. Verwenden Sie die Informationen aus der Skriptausgabe, um den Entitätsspeicher auf der Seite **Datenverbindungen** in Finance (**Systemadministration \> Systemparameter \> Datenverbindungen**) zu aktivieren.

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
> Stellen Sie sicher, dass Sie die folgenden Ressourcen in derselben Azure AD-Instanz erstellen, wie die der Dataverse-Umgebung. Sie können keine Ressourcen von keiner anderen Azure AD-Instanz verwenden.

1. Erstellen eines neuen Speicherkontos:

    1. Erstellen Sie im [Azure-Portal](https://portal.azure.com) ein Speicherkonto.
    2. Legen Sie im Dialogfeld **Speicherkonto erstellen** die folgenden Felder fest:

        - **Ort** – Wählen Sie das Rechenzentrum aus, in dem sich Ihre Umgebung befindet.
        - **Leistung** – Es wird empfohlen, dass Sie **Standard** auswählen.
        - **Art des Kontos** – Sie müssen **StorageV2** auswählen.

    3. Wählen Sie im **Erweiterte Optionen**-Dialogfeld für die **Data Lake Storage Gen2**-Option **Aktivieren** unter der **Hierarchische Namespaces**-Funktion aus. Wenn Sie diese Funktion deaktivieren, können Sie keine Daten nutzen, die von Finance and Operations-Apps geschrieben werden, indem Dienste wie Power BI-Datenflüsse verwendet werden.
    4. Wählen Sie **Überprüfen und erstellen**. Nach Abschluss der Bereitstellung wird die neue Ressource im Azure-Portal angezeigt.
    5. Wechseln Sie zu dem von Ihnen erstellten Speicherkonto.
    6. Wählen Sie im linken Menü **Zugriffsschlüssel** aus.
    7. Kopieren und speichern Sie die Verbindungszeichenfolge für **Key1** oder **Key2**.
    8. Kopieren und speichern Sie den Namen des Speicherkontos.

2. Erstellen eines neuen Key Vaults:

    1. Erstellen Sie im [Azure-Portal](https://portal.azure.com) einen Schlüsseltresor.
    2. Wählen Sie im **Einen Key Vault erstellen**-Dialogfeld im Feld **Ort** das Rechenzentrum aus, in dem sich Ihre Umgebung befindet.
    3. Nachdem der Key Vault erstellt wurde, wählen Sie ihn in der Liste aus und wählen dann **Geheimnisse**.
    4. Wählen Sie **Generieren/Importieren** aus.
    5. Wählen Sie im Dialogfeld **Geheimnis erstellen** im Feld **Uploadoptionen** die Option **Manuell** aus.
    6. Geben Sie einen Namen für das Geheimnis ein. Notieren Sie sich den Namen, da Sie ihn später angeben müssen.
    7. Geben Sie im Feld **Wert** die Verbindungszeichenfolge ein, die Sie im vorherigen Verfahren vom Speicherkonto erhalten haben.
    8. Wählen Sie **Aktiviert** und dann **Erstellen** aus. Das Geheimnis wird erstellt und Key Vault hinzugefügt.
    9. Wechseln Sie zur **Key Vault-Übersicht** und notieren Sie sich den DNS-Namen.

3. Erstellen und registrieren Sie eine Azure AD-Anwendung:

    1. Wechseln Sie im [Azure-Portal](https://portal.azure.com) zu **Azure Active Directory** und wählen Sie dann **App-Registrierungen** aus.
    2. Wählen Sie **Neue Anwendungsregistrierung** aus und legen Sie die folgenden Felder fest:

        - **Name** – Geben Sie den Namen der App ein.
        - **Anwendungstyp** – Wählen Sie **Web-API** aus.
        - **URI-Setup umleiten** – Geben Sie die URL für Ihre Dynamics 365-Instanz ein, z. B. `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Wechseln Sie zu der App, die Sie gerade erstellt haben, und kopieren und speichern Sie deren **Anwendungs-ID (Client-ID)**-Wert. Diesen Wert müssen Sie später beim Einrichten des Key Vaults angeben.
    4. Wechseln Sie zu **API-Berechtigungen** und befolgen Sie diese Schritte:

        1. Wählen Sie **Eine Berechtigung hinzufügen**.
        2. Wählen Sie **Azure Key Vault**.
        3. Nachdem Sie delegierte Berechtigungen ausgewählt haben, wählen Sie **Benutzer\_Identitätswechsel**.
        4. Wählen Sie **Berechtigungen hinzufügen**.

    5. Wählen Sie im Menü für die App **Zertifikate \& Geheimnisse** aus und führen die folgenden Schritte aus, um die Key Vault-Geheimnisse zu erstellen:

        1. Wählen Sie **Neuer Clientschlüssel**.
        2. Geben Sie im Feld **Schlüsselbeschreibung** einen Namen ein.
        3. Wählen Sie eine Dauer und wählen Sie dann **Hinzufügen**. Ein Geheimnis wird im Feld **Wert** generiert.
        4. Kopieren und speichern Sie den geheimen Wert.

4. Erstellen eines neuen Key Vault-Geheimnisses:

    1. Wechseln Sie zu dem zuvor erstellten Key Vault und wählen Sie **Geheimnisse** aus.
    2. Führen Sie für jeden geheimen Namen in der folgenden Tabelle die folgenden Schritte aus:

        1. Wählen Sie **Generieren/Importieren** aus.
        2. Wählen Sie im Dialogfeld **Geheimnis erstellen** im Feld **Uploadoptionen** die Option **Manuell** aus.
        3. Erstellen Sie den geheimen Namen und Wert aus der folgenden Tabelle.
        4. Wählen Sie **Aktiviert** und dann **Erstellen** aus. Das Geheimnis wird erstellt und Key Vault hinzugefügt.

        | Geheimnisname                       | Geheimer Wert                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | app-id                            | Die App-ID der zuvor erstellten Anwendung                                      |
        | app-secret                        | Der Clientschlüssel, den Sie zuvor gespeichert haben                                                    |
        | storage-account-name              | Der Name des Speicherkontos, das Sie zuvor erstellt haben, z. B. **storageaccount1**       |
        | storage-account-connection-string | Die Verbindungszeichenfolge, die Sie von der **Zugangsschlüssel**-Seite für das Speicherkonto kopiert haben |

5. Autorisieren Sie die Anwendung für den Zugriff auf den Schlüsseldepot:

    1. Öffnen Sie im [Azure-Portal](https://portal.azure.com) den zuvor erstellten Key Vault.
    2. Wählen Sie die Zugriffsrichtlinien aus.
    3. Führen Sie für jede Anwendung in der folgenden Tabelle die folgenden Schritte aus:

        1. Wählen Sie **Zugriffsrichtlinie hinzufügen**, um eine Zugriffsrichtlinie zu erstellen.
        2. Wählen Sie im Feld **Geheimnisberechtigungen** die Berechtigungen aus der folgenden Tabelle aus.
        3. Suchen Sie im Feld **Prinzipal auswählen** nach dem Anzeigenamen der Anwendung in der folgenden Tabelle.
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

        1. Wählen Sie die Rolle aus der folgenden Tabelle aus.
        2. Lassen Sie das Feld **Zugriff gewähren auf** auf **Azure AD-Benutzer, -Gruppe oder -Serviceprinzipal**.
        3. Geben Sie im Feld **Geheimnis** die Anwendung aus der folgenden Tabelle ein.
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



## <a name="configure-the-data-lake"></a>Den Data Lake konfigurieren

Führen Sie die folgenden Schritte aus, um der Umgebung mithilfe von LCS das Azure Data Lake-Add-In hinzuzufügen.

1. Melden Sie sich bei LCS an und wählen Sie dann unter dem Umgebungsnamen auf der rechten Seite der Seite **Alle Einzelheiten** aus.
2. Wählen Sie Im Abschnitt **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.
3. Wählen Sie das **Export nach Data Lake**-Add-In.
4. Geben Sie die folgenden Werte ein.

    | Wert                                                              | Beschreibung |
    |--------------------------------------------------------------------|-------------|
    | Mandanten-ID des Azure-Abonnements, in dem sich der Key Vault befindet | Die Mandanten-ID, in der sich das Speicherkonto, die Apps und die Key Vaults befinden. Um diesen Wert zu finden, öffnen Sie das [Azure-Portal](https://portal.azure.com), wechseln Sie zu **Azure Active Directory** und kopieren Sie den **Mandanten-ID**-Wert. |
    | DNS-Namen Ihres Key Vault angeben                             | Der DNS-Name des Key Vaults, z. B. `https://customkeyvault.vault.azure.net/`. (Dieser Wert entspricht dem DNS-Namen, der im Entitätsspeicher verwendet wird.) |
    | Geben Sie das Geheimnis an, das den Namen des Speicherkontos enthält   | **storage-account-name** |
    | Geheimname für die App-ID für den Zugriff auf Data Lake          | **app-id** |
    | Geheimname, der mit der App-ID verwendet werden soll                                 | **app-secret** |

5. Stimmen Sie den Bedingungen zu und wählen Sie **Installieren**.

Das Add-In wird innerhalb weniger Minuten installiert.

## <a name="configure-ai-builder"></a>Konfigurieren von AI Builder

1. Melden Sie sich bei LCS an und öffnen Sie die Seite **Umgebungsdetails**.
2. Scrollen Sie zum Abschnitt **Umgebungs-Add-Ins**. Sie sollten die Add-Ins sehen, die bereits in dieser Umgebung installiert sind. Wenn das **Export nach Data Lake**-Add-In nicht dazu gehört, konfigurieren Sie dieses Add-In.
3. Wählen Sie das **Einblicke erhalten** Add-In.
4. Geben Sie auf der Detailseite mit den **Einblicke erhalten**-Add-In die folgenden Werte ein.

    | Wert                                                    | Beschreibung |
    |----------------------------------------------------------|-------------|
    | CDS-Organisations-URL                                     | Die Dataverse-Organisations-URL wurde von oben kopiert. |
    | CDS-Organisationskennung                                               | Die Dataverse-Organisations-ID wurde von oben kopiert. |
5. Aktivieren **Ist dies die Standardumgebung für Ihren Mandanten**.
    
## <a name="configure-the-entity-store"></a>Konfigurieren des Entitätsspeichers

Führen Sie die folgenden Schritte aus, um den Entitätsspeicher in Ihrer Finance-Umgebung einzurichten.

1. Gehen Sie zu **Systemadministration \> Einrichten \> Systemparameter \> Datenverbindungen**.
2. Legen Sie die folgenden Schlüsseltresorfelder fest:

    - **Anwendungs(client)-ID** – Geben Sie die zuvor erstellte Anwendungsclient-ID ein.
    - **Anwendungsgeheimnis** – Geben Sie das Geheimnis ein, das Sie für die zuvor erstellte Anwendung gespeichert haben.
    - **DNS-Name** – Den DNS(Domain Name System)-Namen finden Sie auf der Seite mit den Anwendungsdetails für die zuvor erstellte Anwendung.
    - **Geheimer Name** – Geben Sie **storage-account-connection-string** ein.
3. Aktivieren **Data-Lake-Integration aktivieren**.
4. Wählen Sie **Azure Key Vault testen** und überprüfen Sie, ob es keine Fehler gibt.
5. Wählen Sie **Test Azure-Storage** und überprüfen Sie, ob es keine Fehler gibt.

## <a name="feedback-and-support"></a>Feedback und Support

Bitte senden Sie eine E-Mail an [Debitorenzahlungseinblicke (Vorschau)](mailto:fiap@microsoft.com), wenn Sie an Feedback interessiert sind oder Support benötigen.

## <a name="privacy-notice"></a>Datenschutzhinweis

Vorschauen (1) wenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen an als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement (SLA) für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
