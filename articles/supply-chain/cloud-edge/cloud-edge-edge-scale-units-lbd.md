---
title: Edge-Skalierungseinheiten mithilfe von LBD auf benutzerdefinierter Hardware bereitstellen (Vorschau)
description: In diesem Thema wird erläutert, wie Sie lokale Edge-Skalierungseinheiten mithilfe von benutzerdefinierter Hardware und Bereitstellung bereitstellen, die auf lokalen Geschäftsdaten (LBD) basiert.
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678980"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>Edge-Skalierungseinheiten mithilfe von LBD auf benutzerdefinierter Hardware bereitstellen (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

Edge-Skalierungseinheiten spielen eine wichtige Rolle in der verteilten Hybridtopologie für das Supply Chain Management. In der Hybridtopologie können Sie Workloads zwischen Ihrem Supply Chain Management Cloud-Hub und zusätzlichen Skalierungseinheiten in der Cloud oder am Edge verteilen.

Edge-Skalierungseinheiten können bereitgestellt werden, indem eine [lokale Umgebung](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) mit lokalen Geschäftsdaten (LBD) erstellt wird und diese dann so konfiguriert wird, dass es als Skalierungseinheit in Ihrer verteilten Hybridtopologie für das Supply Chain Management fungiert. Dies wird erreicht, indem die lokale LBD-Umgebung mit einer Supply Chain Management-Umgebung in der Cloud verknüpft wird, die als Hub konfiguriert wurde.  

Edge-Skalierungseinheiten befinden sich derzeit in der Vorschau. Daher dürfen Sie eine Umgebung dieser Art nur gemäß den [Vorschaubedingungen](https://aka.ms/scmcnepreviewterms) verwendet werden.

In diesem Thema wird beschrieben, wie Sie eine lokale LBD-Umgebung als Edge-Skalierungseinheit einrichten und sie dann einem Hub zuordnen.

## <a name="deployment-overview"></a>Bereitstellungsübersicht

Hier ein Überblick über die Bereitstellungsschritte.

1. **Einen LBD-Slot in Ihrem LBD-Projekt in Microsoft Dynamics Lifecycle Services (LCS) verwenden.**

    Während der Vorschau zielen LBD-Edge-Skalierungseinheiten auf bestehende LBD-Kunden ab. Ein zusätzlicher 60-Tage-begrenzter LBD-Sandbox-Slot wird nur in bestimmten Kundensituationen bereitgestellt.

1. **Einrichten und Bereitstellen einer LBD-Umgebung mit einer *leeren* Datenbank.**

    Verwenden Sie LCS, um die LBD-Umgebung mit der neuesten Topologie und einer leeren Datenbank bereitzustellen. Weitere Informationen finden Sie im Abschnitt [Einrichten und Bereitstellen einer LBD-Umgebung mit leerer Datenbank](#set-up-deploy) weiter unten in diesem Thema. Sie müssen Supply Chain Management Version 10.0.19 mit Plattform-Update 43 oder höher in Hub- und Skalierungseinheitumgebungen verwenden.

1. **Zielpakete in LBD-Projektassets in LCS hochladen.**

    Bereiten Sie Anwendungs-, Plattform- und Anpassungspakete vor, die Sie im Hub und in der Skalierungseinheit verwenden. Weitere Informationen finden Sie im Abschnitt [Hochladen von Zielpaketen in LBD-Projektassets in LCS](#upload-packages) weiter unten in diesem Thema.

1. **Warten Sie die LBD-Umgebung mit den Zielpaketen.**

    Dieser Schritt stellt sicher, dass auf dem Hub und dem Spoke der gleiche Build und die gleichen Anpassungen bereitgestellt werden. Weitere Informationen finden Sie im Abschnitt [Warten der LBD-Umgebung mit Zielpaketen](#service-target-packages) weiter unten in diesem Thema.

1. **Schließen Sie die Konfiguration der Skalierungseinheit und die Arbeitslastzuweisung ab.**

    Weitere Informationen finden Sie im Abschnitt [Weisen Sie Ihr LBD Edge-Skalierungseinheit einem Hub zu](#assign-edge-to-hub) weiter unten in diesem Thema.

Die verbleibenden Themen enthalten zusätzliche Details zum Durchführen dieser Schritte.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Einrichten und Bereitstellen einer LBD-Umgebung mit einer leeren Datenbank

Dieser Schritt erstellt eine funktionale LBD-Umgebung. Die Umgebung hat jedoch nicht unbedingt die gleichen Anwendungs- und Plattformversionen wie die Hub-Umgebung. Darüber hinaus fehlen noch die Anpassungen und es wurde noch nicht aktiviert, um als Skalierungseinheit zu funktionieren.

1. Folgen Sie den Anweisungen in [Lokale Umgebungen einrichten und bereitstellen (Plattformupdate 41 und höher)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Sie müssen Supply Chain Management Version 10.0.19 mit Plattform-Update 43 oder höher in Hub- und Skalierungseinheitumgebungen verwenden

    > [!IMPORTANT]
    > Lesen Sie den Rest dieses Abschnitts, **bevor** Sie die Schritte in diesem Thema durchführen.

1. Bevor Sie Ihre Konfiguration in der Infrastruktur\\ConfigTemplate.xml-Datei beschreiben, führen Sie das folgende Skript aus:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Dieses Skript entfernt alle Konfigurationen, die für die Bereitstellung von Edge-Skalierungseinheiten nicht erforderlich sind.

1. Richten Sie eine Datenbank mit leeren Daten ein, wie beschrieben in [Datenbanken konfigurieren](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Verwenden Sie für diesen Schritt die leere Datei data.bak.
1. Richten Sie das Skript vor der Bereitstellung ein. Weitere Informationen finden Sie in [Skripts des lokalen Agenten vor und nach der Bereitstellung](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Kopieren Sie den Inhalt aus dem Ordner **ScaleUnit** in **Infrastruktur-Skripte** in den Ordner **Skripte** in der Dateispeicherfreigabe des Agenten, die in der Umgebung eingerichtet wurde. Ein typischer Pfad ist \\\\lbdiscsi01\\Agent\\Skripte.
    2. Erstellen Sie das Skript **PreDeployment.ps1**, das die Skripte mit den erforderlichen Parametern aufruft. Das Vor-Bereitstellungsskript muss in den Ordner **Skripte** in der Dateispeicherfreigabe des Agenten abgelegt werden. Andernfalls kann es nicht ausgeführt werden. Ein typischer Pfad ist \\\\lbdiscsi01\\Agent\\Skripte\\PreDeployment.ps1.

        Der Inhalt des Skripts PreDeployment.ps1 ähnelt dem folgenden Beispiel.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
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

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Zielpakete in LBD-Projektassets in LCS hochladen

In diesem Schritt werden die Anwendungsversion, die Plattformversion und die Anpassungen vorbereitet, die auf Ihre LBD-Skalierungseinheitsumgebung übertragen werden.

1. Laden Sie dasselbe kombinierte Anwendungs-/Plattformpaket, das auf die Hub-Umgebung angewendet wurde, in die Asset-Bibliothek des lokalen LCS-Projekts hoch.
1. Holen Sie sich eine Kopie des benuzerdefinierten bereitstellbaren Pakets, das auf die Hub-Umgebung angewendet wurde, und laden Sie es in die Asset-Bibliothek des lokalen LCS-Projekts hoch.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Warten Sie die LBD-Umgebung mit den Zielpaketen

In diesem Schritt werden die Anwendungsversion, die Plattformversion und die Anpassungen in Ihre LBD-Skalierungseinheitsumgebung mit dem Hub eingepasst.

1. Warten Sie die LBD-Umgebung mit dem kombinierten Anwendungs-/Plattformpaket, das Sie im vorherigen Schritt hochgeladen haben.
1. Warten Sie die LBD-Umgebung mit dem benutzerdefinierten bereistellbaren Paket, das Sie im vorherigen Schritt hochgeladen haben.

    ![Wählen Sie Verwalten > Updates in LCS anwenden.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Wählen Sie Verwalten > Updates in LCS anwenden")

    ![Auswahl Ihres Individualisierungspakets.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Auswahl Ihres Individualisierungspakets")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Weisen Sie Ihr LBD Edge Scale-Gerät einem Hub zu

Während sich die Edge-Skalierungseinheiten noch in der Vorschau befinden, müssen Sie die [Skalierungseinheitsbereitstellungs- und Konfigurationstools](https://github.com/microsoft/SCMScaleUnitDevTools) verwenden, die auf GitHub verfügbar sind, um Ihre LBD-Edge-Scale-Einheit einem Hub zuzuweisen. Der Prozess ermöglicht es einer LBD-Konfiguration, als Edge-Skalierungseinheit zu fungieren, und ordnet sie dem Hub zu. Der Prozess ähnelt dem Konfigurieren einer One-Box-Entwicklungsumgebung.

1. Laden Sie die neueste Version von [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) herunter und entpacken Sie den Inhalt der Datei.
1. Erstellen Sie eine Kopie der `UserConfig.sample.xml`-Datei und benennen Sie sie `UserConfig.xml`.
1. Erstellen Sie eine Microsoft Azure Active Directory (Azure AD)-Anwendung in Ihrem Azure AD-Mandanten, wie in [Bereitstellungsleitfaden für Skalierungseinheit und Workloads](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations) erwähnt.
    1. Navigieren Sie nach der Erstellung zum Azure AD-Anwendungsformular (SysAADClientTable) auf Ihrem Hub.
    1. Erstellen Sie einen neuen Eintrag und setzen Sie die **Kunden-ID** auf die ID der von Ihnen erstellten Anwendung. Stellen Sie **Name** zu *ScaleUnits* und **Benutzer-ID** zu *Administrator*.

1. Erstellen Sie eine Active Directory-Verbunddienst (AD FS)-Anwendung, wie in [Bereitstellungsleitfaden für Skalierungseinheit und Workloads](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations) erwähnt.
    1. Navigieren Sie nach der Erstellung zum Azure AD-Anwendungsformular (SysAADClientTable) auf Ihre Edge-Skalierungseinheit.
    1. Erstellen Sie einen neuen Eintrag und setzen Sie die **Kunden-ID** auf die ID der von Ihnen erstellten Anwendung. Stellen Sie **Benutzer-ID** zu *Administrator*.

1. Bearbeiten Sie die `UserConfig.xml`-Datei.
    1. Unter dem `InterAOSAADConfiguration`-Abschnitt geben Sie die Informationen aus der Azure AD-Anwendung ein, die Sie zuvor erstellt haben.
        - In dem `AppId`-Element geben Sie die Anwendungs-ID der Azure-Anwendung ein.
        - In dem `AppSecret`-Element geben Sie das Anwendungsgeheimnis der Azure-Anwendung ein.
        - Das `Authority`-Element muss die URL enthalten, die die Sicherheitsautorität für Ihren Mandanten angibt.

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. Unter dem `ScaleUnitConfiguration`-Abschnitt für die erste `ScaleUnitInstance` bearbeiten Sie den Abschnitt `AuthConfiguration`.
        - In dem `AppId`-Element geben Sie die Anwendungs-ID der Azure-Anwendung ein.
        - In dem `AppSecret`-Element geben Sie das Anwendungsgeheimnis der Azure-Anwendung ein.
        - Das `Authority`-Element muss die URL enthalten, die die Sicherheitsautorität für Ihren Mandanten angibt.

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. Legen Sie für dieselbe `ScaleUnitInstance` zusätzlich die folgenden Werte fest:
        - In dem `Domain`-Element geben Sie die URL Ihres Hubs an. Zum Beispiel: `https://cloudhub.sandbox.operations.dynamics.com/`
        - In dem `EnvironmentType`-Element stellen Sie sicher, dass `LCSHosted` eingestellt ist.

    1. Unter dem `ScaleUnitConfiguration`-Abschnitt für die zweite `ScaleUnitInstance` bearbeiten Sie den Abschnitt `AuthConfiguration`.
        - In dem `AppId`-Element geben Sie die Anwendungs-ID der AD FS-Anwendung ein.
        - In dem `AppSecret`-Element geben Sie das Anwendungsgeheimnis der ADFS-Anwendung ein.
        - Das `Authority`-Element muss die URL Ihrer AD FS-Instanz enthalten.

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. Legen Sie für dieselbe `ScaleUnitInstance` zusätzlich die folgenden Werte fest:
        - In dem `Domain`-Element geben Sie die URL Ihrer Edge-Skalierungseinheit an. Zum Beispiel: https://ax.contoso.com/
        - In dem `EnvironmentType`-Element stellen Sie sicher, dass der Wert LBD eingestellt ist.
        - In dem `ScaleUnitId`-Element geben Sie denselben Wert ein, den Sie für `InstanceId` bei der Konfiguration des `Configure-CloudandEdge.ps1`-Skripts vor der Bereitstellung angegeben haben.

        > [!NOTE]
        > Wenn Sie nicht die Standard-ID (@A) verwenden, stellen Sie sicher, dass Sie die ScaleUnitId für jedes ConfiguredWorkload-Element im Abschnitt Arbeitslasten aktualisieren.

1. Öffnen Sie PowerShell und navigieren Sie zu dem Ordner mit der `UserConfig.xml`-Datei.

1. Führen Sie das Tool mit diesem Befehl aus.

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > Nach jeder Aktion müssen Sie das Tool erneut starten.

1. Wählen Sie im Tool **2. Umgebungen für die Workload-Installation vorbereiten**. Führen Sie dann die folgenden Schritte aus:
    1. Wählen Sie **1. Bereiten Sie den Hub vor**.
    1. Wählen Sie **2. Bereiten Sie die Skalierungseinheit vor**.

    > [!NOTE]
    > Wenn Sie diesen Befehl nicht von einer Neuinstallation ausführen und er fehlschlägt, führen Sie die folgenden Aktionen aus:
    >
    > - Entfernen Sie alle Ordner aus dem `aos-storage`-Ordner (außer `GACAssemblies`).
    > - Führen Sie den folgenden SQL-Befehl in Ihrer Geschäftsdatenbank (AXDB) aus:
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. Führen Sie die folgenden SQL-Befehle in Ihrer Geschäftsdatenbank (AXDB) aus:

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. Stellen Sie sicher, dass die Änderungsverfolgung in Ihrer Geschäftsdatenbank (AXDB) aktiviert wurde
    1. SQL Server Management Studio (SSMS) starten.
    1. Klicken Sie mit der rechten Maustaste auf Ihre Geschäftsdatenbank (AXDB) und wählen Sie Eigenschaften aus.
    1. Wählen Sie im sich öffnenden Fenster **Änderungsverfolgung** und nehmen Sie folgende Einstellungen vor:

        - **Änderungsnachverfolgung:** *True*
        - **Aufbewahrungsfrist:** *7*
        - **Rückhalteeinheiten:** *Tage*
        - **Automatische Bereinigung:** *True*

1. Wählen Sie im Tool **3. Workloads installieren**. Führen Sie dann die folgenden Schritte aus:
    1. Wählen Sie **1. Auf Hub installieren**.
    1. Wählen Sie **2. Auf Waageneinheit installieren**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
