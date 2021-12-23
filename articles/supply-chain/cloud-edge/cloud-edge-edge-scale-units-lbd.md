---
title: Edge-Skalierungseinheiten mithilfe von LBD auf benutzerdefinierter Hardware bereitstellen
description: In diesem Thema wird erläutert, wie Sie lokale Edge-Skalierungseinheiten mithilfe von benutzerdefinierter Hardware und Bereitstellung bereitstellen, die auf lokalen Geschäftsdaten (LBD) basiert.
author: cabeln
ms.date: 11/29/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8913debd614827ef66ded88e0da61663ca9c6b3d
ms.sourcegitcommit: 29d34f2fd509e2bb27d8572cd57c397d014a8e38
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/07/2021
ms.locfileid: "7894717"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>Edge-Skalierungseinheiten mithilfe von LBD auf benutzerdefinierter Hardware bereitstellen

[!include [banner](../includes/banner.md)]

Edge-Skalierungseinheiten spielen eine wichtige Rolle in der verteilten Hybridtopologie für das Supply Chain Management. In der Hybridtopologie können Sie Workloads zwischen Ihrem Supply Chain Management Cloud-Hub und zusätzlichen Skalierungseinheiten in der Cloud oder am Edge verteilen.

Edge-Skalierungseinheiten können bereitgestellt werden, indem eine [lokale Umgebung](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) mit lokalen Geschäftsdaten (LBD) erstellt wird und diese dann so konfiguriert wird, dass es als Skalierungseinheit in Ihrer verteilten Hybridtopologie für das Supply Chain Management fungiert. Dies wird erreicht, indem die lokale LBD-Umgebung mit einer Supply Chain Management-Umgebung in der Cloud verknüpft wird, die als Hub konfiguriert wurde.  

In diesem Thema wird beschrieben, wie Sie eine lokale LBD-Umgebung als Edge-Skalierungseinheit einrichten und sie dann einem Hub zuordnen.

## <a name="deployment-overview"></a>Bereitstellungsübersicht

Hier ein Überblick über die Bereitstellungsschritte.

1. **Einen LBD-Slot in Ihrem LBD-Projekt in Microsoft Dynamics Lifecycle Services (LCS) verwenden.**

1. **Einrichten und Bereitstellen einer LBD-Umgebung mit einer *leeren* Datenbank.**

    Verwenden Sie LCS, um die LBD-Umgebung mit der neuesten Topologie und einer leeren Datenbank bereitzustellen. Weitere Informationen finden Sie im Abschnitt [Einrichten und Bereitstellen einer LBD-Umgebung mit leerer Datenbank](#set-up-deploy) weiter unten in diesem Thema. Sie müssen mindestens die Supply Chain Management Version 10.0.21 in Hub- und Skalierungseinheitumgebungen verwenden.

1. **Zielpakete in LBD-Projektassets in LCS hochladen.**

    Bereiten Sie Anwendungs-, Plattform- und Anpassungspakete vor, die Sie im Hub und in der Skalierungseinheit verwenden. Weitere Informationen finden Sie im Abschnitt [Hochladen von Zielpaketen in LBD-Projektassets in LCS](#upload-packages) weiter unten in diesem Thema.

1. **Warten Sie die LBD-Umgebung mit den Zielpaketen.**

    Dieser Schritt stellt sicher, dass auf dem Hub und dem Spoke der gleiche Build und die gleichen Anpassungen bereitgestellt werden. Weitere Informationen finden Sie im Abschnitt [Warten der LBD-Umgebung mit Zielpaketen](#service-target-packages) weiter unten in diesem Thema.

1. **Schließen Sie die Konfiguration der Skalierungseinheit und die Arbeitslastzuweisung ab.**

    Weitere Informationen finden Sie im Abschnitt [Weisen Sie Ihr LBD Edge-Skalierungseinheit einem Hub zu](#assign-edge-to-hub) weiter unten in diesem Thema.

Die verbleibenden Themen enthalten zusätzliche Details zum Durchführen dieser Schritte.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Einrichten und Bereitstellen einer LBD-Umgebung mit einer leeren Datenbank

Dieser Schritt erstellt eine funktionale LBD-Umgebung. Die Umgebung hat jedoch nicht unbedingt die gleichen Anwendungs- und Plattformversionen wie die Hub-Umgebung. Darüber hinaus fehlen noch die Anpassungen und es wurde noch nicht aktiviert, um als Skalierungseinheit zu funktionieren.

1. Folgen Sie den Anweisungen in [Lokale Umgebungen einrichten und bereitstellen (Plattformupdate 41 und höher)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Sie müssen mindestens die Supply Chain Management Version 10.0.21 in Hub- und Skalierungseinheitumgebungen verwenden. Darüber hinaus müssen Sie mindestens Version 2.12.0 der Infrastruktur-Skripts verwenden. 

    > [!IMPORTANT]
    > Lesen Sie den Rest dieses Abschnitts, **bevor** Sie die Schritte in diesem Thema durchführen.

1. Bevor Sie Ihre Konfiguration in der Infrastruktur\\ConfigTemplate.xml-Datei beschreiben, führen Sie das folgende Skript aus:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Dieses Skript entfernt alle Konfigurationen, die für die Bereitstellung von Edge-Skalierungseinheiten nicht erforderlich sind.

1. Richten Sie eine Datenbank mit leeren Daten ein, wie beschrieben in [Datenbanken konfigurieren](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Verwenden Sie für diesen Schritt die leere Datei data.bak.
1. Nachdem Sie mit dem Schritt [Datenbanken konfigurieren](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) fertig sind, führen Sie das folgende Skript aus, um die Skalierungseinheit-ALM-Orchestrator-Datenbank zu konfigurieren.

    > [!NOTE]
    > Konfigurieren Sie die Financial Reporting-Datenbank nicht während des Schritts [Datenbanken konfigurieren](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb).

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Das Initialize-Database.ps1-Skript führt die folgenden Aktionen aus:

    1. Erstellen Sie eine leere Datenbank mit dem Namen **ScaleUnitAlmDb**.
    2. Ordnen Sie die Benutzer basierend auf der folgenden Tabelle Datenbankrollen zu.

        | Benutzer            | Typ | Datenbankrolle |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_owner     |

1. Folgen Sie weiter den Anweisungen in [Lokale Umgebungen einrichten und bereitstellen (Plattformupdate 41 und höher)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).
1. Nachdem Sie den Schritt [AD FS konfigurieren](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) abgeschlossen haben, gehen Sie folgendermaßen vor:

    1. Erstellen Sie eine neue „Active Directory-Verbunddienste“-Anwendung (AD FS), die es dem ALM-Orchestrierungsdienst ermöglicht, mit Ihrem Anwendungsobjektserver (AOS) zu kommunizieren.

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. Erstellen Sie eine neue Azure Active Directory (Azure AD) Anwendung, die es dem ALM-Orchestrierungsdienst ermöglicht, mit dem Dienst zum Verwalten der Skalierungseinheit zu kommunizieren.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. Folgen Sie weiter den Anweisungen in [Lokale Umgebungen einrichten und bereitstellen (Plattformupdate 41 und höher)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Wenn Sie die Konfiguration für den lokalen Agenten eingeben müssen, stellen Sie sicher, dass Sie die Funktionen der Edge-Skalierungseinheit aktivieren und alle erforderlichen Parameter angeben.

    ![Funktionen der Edge-Skalierungseinheiten aktivieren.](media/EnableEdgeScaleUnitFeatures.png "Funktionen der Edge-Skalierungseinheiten aktivieren.")

1. Bevor Sie Ihre Umgebung über LCS bereitstellen, richten Sie das Skript vor der Bereitstellung ein. Weitere Informationen finden Sie in [Skripts des lokalen Agenten vor und nach der Bereitstellung](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Kopieren Sie das Configure-CloudAndEdge.ps1-Skript aus dem Ordner **ScaleUnit** in **Infrastruktur-Skripte** in den Ordner **Skripte** in der Dateispeicherfreigabe des Agenten, die in der Umgebung eingerichtet wurde. Ein typischer Pfad ist \\\\lbdiscsi01\\Agent\\Skripte.
    2. Erstellen Sie das Skript **PreDeployment.ps1**, das die Skripte mit den erforderlichen Parametern aufruft. Das Vor-Bereitstellungsskript muss in den Ordner **Skripte** in der Dateispeicherfreigabe des Agenten abgelegt werden. Andernfalls kann es nicht ausgeführt werden. Ein typischer Pfad ist \\\\lbdiscsi01\\Agent\\Skripte\\PreDeployment.ps1.

        Der Inhalt des Skripts PreDeployment.ps1 ähnelt dem folgenden Beispiel.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
        ```

        > [!NOTE]
        > Der Parameter InstanceId sollte nur aus zwei Zeichen bestehen. Das erste Zeichen ist @ und das zweite kann ein beliebiger Großbuchstabe des englischen Alphabets sein.
        >
        > - Gültige Werte:
        >   - @D
        >   - @X
        > - Ungültige Werte:
        >   - @a
        >   - @4
        >   - @#

1. Stellen Sie die Umgebung mithilfe der neuesten verfügbaren Basistopologie bereit.
1. Gehen Sie folgendermaßen vor, nachdem Ihre Umgebung bereitgestellt wurde:

    1. Führen Sie die folgenden SQL-Befehle in Ihrer Geschäftsdatenbank (AXDB) aus.

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Erhöhen Sie die gleichzeitige maximale Batchsitzung auf einen Wert, der über 4 liegt.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Stellen Sie sicher, dass die Änderungsverfolgung in Ihrer Geschäftsdatenbank (AXDB) aktiviert wurde.

        1. Öffnen Sie SQL Server Management Studio (SSMS).
        1. Wählen und halten Sie Ihre Geschäftsdatenbank (AXDB) aus (oder klicken Sie sie mit der rechten Maustaste an) und wählen Sie dann **Eigenschaften**.
        1. Wählen Sie im erscheinenden Fenster **Änderungsverfolgung** und legen Sie dann die folgenden Werte fest:

            - **Änderungsnachverfolgung:** *True*
            - **Aufbewahrungsfrist:** *7*
            - **Rückhalteeinheiten:** *Tage*
            - **Automatische Bereinigung:** *True*

    1. Fügen Sie die zuvor erstellte AD FS-Anwendungs-ID (mithilfe des Skripts Create-ADFSServerApplicationForEdgeScaleUnits.ps1) zur Azure AD Anwendungstabelle in Ihrer Skalierungseinheit. Sie können diesen Schritt manuell über die Benutzeroberfläche (UI) ausführen. Alternativ können Sie ihn über die Datenbank erledigen, indem Sie das folgende Skript verwenden.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a>Richten Sie einen Azure Key Vault und eine Azure AD-Anwendung ein, um die Kommunikation zwischen Skalierungseinheiten zu ermöglichen

1. Nachdem Ihre Umgebung bereitgestellt wurde, erstellen Sie eine zusätzliche Azure AD-Anwendung, um eine vertrauenswürdige Kommunikation zwischen Ihrer Hub und der Skalierungseinheit zu ermöglichen.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. Nachdem Sie die Anwendung erstellt haben, müssen Sie einen geheimen Clientschlüssel erstellen und die Informationen in einem Azure Key Vault speichern. Außerdem müssen Sie den Zugriff auf die erstellte Azure AD-Anwendung gewähren, damit sie die im Schlüsseltresor gespeicherten Geheimnisse abrufen kann. Zu Ihrer Bequemlichkeit führt das folgende Skript automatisch alle erforderlichen Aktionen aus.

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > Wenn kein Schlüsseltresor mit den angegebenen **KeyVaultName**-Wert vorhanden ist, erstellt das Skript automatisch einen.

1. Fügen Sie die Azure AD-Anwendungs-ID, die Sie gerade erstellt haben (bei Verwendung des Skripts Create-SpokeToHubAADApplication.ps1), der Azure AD-Anwendungstabelle in Ihrem Hub hinzu. Sie können diesen Schritt manuell über die UI ausführen.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Zielpakete in LBD-Projektassets in LCS hochladen

In diesem Schritt werden die Anwendungsversion, die Plattformversion und die Anpassungen vorbereitet, die auf Ihre LBD-Skalierungseinheitsumgebung übertragen werden.

1. Laden Sie dasselbe kombinierte Anwendungs-/Plattformpaket, das auf die Hub-Umgebung angewendet wurde, in die Asset-Bibliothek des lokalen LCS-Projekts hoch.
1. Holen Sie sich eine Kopie des benuzerdefinierten bereitstellbaren Pakets, das auf die Hub-Umgebung angewendet wurde, und laden Sie es in die Asset-Bibliothek des lokalen LCS-Projekts hoch.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Warten Sie die LBD-Umgebung mit den Zielpaketen

In diesem Schritt werden die Anwendungsversion, die Plattformversion und die Anpassungen in Ihre LBD-Skalierungseinheitsumgebung mit dem Hub eingepasst.

1. Warten Sie die LBD-Umgebung mit dem kombinierten Anwendungs-/Plattformpaket, das Sie im vorherigen Schritt hochgeladen haben.
1. Warten Sie die LBD-Umgebung mit dem benutzerdefinierten bereistellbaren Paket, das Sie im vorherigen Schritt hochgeladen haben.

    ![Updates in LCS anwenden.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Updates in LCS anwenden")

    ![Auswahl Ihres Individualisierungspakets.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Auswahl Ihres Individualisierungspakets")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Weisen Sie Ihr LBD Edge Scale-Gerät einem Hub zu

Sie konfigurieren und verwalten Ihre Edge-Skalierungseinheit über das Verwaltungsportal der Skalierungseinheit. Weiter Informationen finden Sie in [Verwalten Sie Cloud-Skalierungseinheiten und Arbeitsauslastungen mithilfe des Scale Unit Manager-Portals](./cloud-edge-landing-page.md#scale-unit-manager-portal).

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
