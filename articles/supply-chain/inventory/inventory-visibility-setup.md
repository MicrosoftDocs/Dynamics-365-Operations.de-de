---
title: Bestandstransparenz einrichten
description: In diesem Thema wird beschrieben, wie Sie das Bestandssichtbarkeit-Add-In für Microsoft Dynamics 365 Supply Chain Management installieren.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8573fe01abb1c6092012baf85e8b7df40b74a31f
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343583"
---
# <a name="set-up-inventory-visibility"></a>Bestandstransparenz einrichten

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

In diesem Thema wird beschrieben, wie Sie das Bestandssichtbarkeit-Add-In für Microsoft Dynamics 365 Supply Chain Management installieren.

Sie müssen Microsoft Dynamics Lifecycle Services (LCS) verwenden, um das Bestandssichtbarkeit-Add-In zu installieren. LCS ist ein Portal für die Zusammenarbeit, das eine Umgebung und eine Reihe von regelmäßig aktualisierten Diensten bereitstellt, die Sie bei der Verwaltung des Anwendungslebenszyklus Ihrer Apps für Finanzen und Vorgänge unterstützen.

Weitere Informationen finden Sie unter [Ressourcen für Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Voraussetzungen für Inventory Visibility

Bevor Sie die Inventory Visibility installieren, müssen Sie die folgenden Aufgaben erledigen:

- Besorgen Sie sich ein LCS-Implementierungsprojekt, in dem mindestens eine Umgebung bereitgestellt ist.
- Stellen Sie sicher, dass die Voraussetzungen für das Einrichten von Add-Ins erfüllt sind. Informationen zu diesen Voraussetzungen finden Sie unter [Übersicht Add-Ins](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Bestandssichtbarkeit erfordert keine Dual-Write-Verknüpfung.
- Wenden Sie sich an das Inventory Visibility Produktteam unter [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), um die folgenden erforderlichen Dateien zu erhalten:

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip` (wenn die Version von Supply Chain Management, die Sie verwenden, älter ist als Version 10.0.18)

> [!NOTE]
> Zu den Ländern und Regionen, die derzeit unterstützt werden, gehören Kanada (CCA, ECA), die Vereinigten Staaten (WUS, EUS), die Europäische Union (NEU, WEU), das Vereinigte Königreich (SUK, WUK) und Australien (EAU, SEAU).

Wenn Sie Fragen zu diesen Voraussetzungen haben, wenden Sie sich an das Inventory Visibility Produktteam.

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Einrichten von Dataverse

Um Dataverse so festzulegen, dass es mit Inventory Visibility verwendet werden kann, verwenden Sie das Package Deployer Tool, um das Inventory Visibility Paket bereitzustellen. In den folgenden Unterabschnitten wird beschrieben, wie Sie die einzelnen Aufgaben ausführen.

> [!NOTE]
> Derzeit werden nur Dataverse-Umgebungen unterstützt, die mit LCS erstellt wurden. Wenn Ihre Dataverse-Umgebung auf andere Weise erstellt wurde (z. B. mit dem Power Apps-Admin Center) und mit Ihrer Supply Chain Management-Umgebung verknüpft ist, müssen Sie sich zunächst an das Inventory Visibility Produktteam wenden, um das Zuordnungsproblem zu beheben. Anschließend können Sie Inventory Visibility installieren.

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>Migrieren Sie von einer alten Version der Dataverse-Lösung

Wenn Sie eine ältere Version der Inventory Visibility Dataverse-Lösung installiert haben, verwenden Sie diese Anweisungen, um Ihre Version zu aktualisieren. Es gibt zwei Fälle:

- **Fall 1:** Wenn Sie Dataverse manuell festgelegt haben, indem Sie die `Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip`-Lösung importiert haben, folgen Sie diesen Schritten:

    1. Laden Sie die folgenden drei Dateien herunter:

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. Importieren Sie `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` und `InventoryServiceBase_managed.cab` manuell in Dataverse, indem Sie die folgenden Schritte ausführen:

        1. Öffnen Sie die URL Ihrer Dataverse-Umgebung.
        1. Öffnen Sie die Seite **Lösungen**.
        1. **Import** auswählen

    1. Verwenden Sie das Package Deployer Tool, um das `InventoryServiceApplication.PackageDeployer.zip`-Paket bereitzustellen. Anweisungen dazu finden Sie im Abschnitt [Benutzen Sie das Package Deployer Tool, um das Paket bereitzustellen](#deploy-package) weiter unten in diesem Thema.

- **Fall 2:** Wenn Sie Dataverse mit dem Package Deployer Tool festgelegt haben, bevor Sie das ältere `.*PackageDeployer.zip`-Paket installiert haben, laden Sie `InventoryServiceApplication.PackageDeployer.zip` herunter und führen Sie ein Update durch. Anweisungen dazu finden Sie im Abschnitt [Benutzen Sie das Package Deployer Tool, um das Paket bereitzustellen](#deploy-package).

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>Benutzen Sie das Package Deployer Tool, um das Paket bereitzustellen

1. Installieren Sie die Entwickler-Tools wie in [Download von Tools aus NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget) beschrieben.
1. Heben Sie die Sperrung der Datei `InventoryServiceApplication.PackageDeployer.zip` auf, die Sie aus der Gruppe Teams heruntergeladen haben, indem Sie die folgenden Schritte ausführen:

    1. Wählen und halten Sie die Datei (oder klicken Sie mit der rechten Maustaste) und wählen Sie dann **Eigenschaften**.
    1. Suchen Sie im Dialogfeld **Eigenschaften** auf der Registerkarte **Allgemein** den Abschnitt **Sicherheit**, wählen Sie **Entsperren** und übernehmen Sie die Änderung. Wenn auf der Registerkarte **Allgemein** kein Abschnitt **Sicherheit** vorhanden ist, ist die Datei nicht blockiert. Fahren Sie in diesem Fall mit dem nächsten Schritt fort.

    ![Entblockieren der heruntergeladenen Datei](media/unblock-file.png "Entblockieren der heruntergeladenen Datei")

1. Entpacken Sie `InventoryServiceApplication.PackageDeployer.zip`, um die folgenden Artikel zu finden:

    - `InventoryServiceApplication`-Ordner
    - `[Content_Types].xml`-Datei
    - `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`-Datei

1. Kopieren Sie jedes dieser Elemente in das Verzeichnis `.\Tools\PackageDeployment`. (Dieses Verzeichnis wurde erstellt, als Sie die Entwickler-Tools installiert haben.)
1. Führen Sie `.\Tools\PackageDeployment\PackageDeployer.exe` aus, und folgen Sie den Anweisungen auf dem Bildschirm, um die Lösungen zu importieren.

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Installieren Sie das Inventory Visibility Add-In

Bevor Sie das Add-In installieren, registrieren Sie eine Anwendung und fügen Sie ein Client-Geheimnis zu Azure Active Directory (Azure AD) unter Ihrem Azure-Abonnement hinzu. Anweisungen finden Sie unter [Registrieren einer Anwendung](/azure/active-directory/develop/quickstart-register-app) und [Hinzufügen eines Client-Geheimnisses](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Notieren Sie sich unbedingt die Werte **Anwendungs-(Client-)ID**, **Client-Geheimnis** und **Mandanten-ID**, da Sie diese später noch benötigen werden.

Nachdem Sie eine Anwendung registriert und ein Client-Geheimnis zu Azure AD hinzugefügt haben, folgen Sie diesen Schritten, um das Bestandssichtbarkeit-Add-In zu installieren.

1. Melden Sie sich bei [LCS](https://lcs.dynamics.com/Logon/Index) an.
1. Wählen Sie auf der Startseite das Projekt aus, in dem Ihre Umgebung bereitgestellt ist.
1. Wählen Sie auf der Projektseite die Umgebung aus, in der Sie das Add-In installieren möchten.
1. Scrollen Sie auf der Umgebungsseite nach unten, bis Sie im Abschnitt **Power Platform-Integration** den Abschnitt **Umgebungs-Add-ins** finden. Dort finden Sie den Namen der Dataverse-Umgebung.
1. Wählen Sie Im Abschnitt **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.

    ![Umgebungsseite in LCS](media/inventory-visibility-environment.png "Umgebungsseite in LCS")

1. Wählen Sie den Link **Ein neues Add-In installieren**. Es wird eine Liste der verfügbaren Add-Ins angezeigt.
1. Wählen Sie in der Liste **Inventory Visibility**.
1. Legen Sie die folgenden Felder für Ihre Umgebung fest:

    - **AAD-Anwendungs-(Client-)ID** - Geben Sie die Azure AD Anwendungs-ID ein, die Sie zuvor erstellt und notiert haben.
    - **AAD-Mandanten-ID** - Geben Sie die Mandant-ID ein, die Sie sich zuvor notiert haben.

    ![Seite für die Einrichtung von Add-Ins](media/inventory-visibility-setup.png "Seite für die Einrichtung von Add-Ins")

1. Stimmen Sie den Bedingungen zu, indem Sie das Kontrollkästchen **Geschäftsbedingungen** aktivieren.
1. Wählen Sie **Installieren**. Der Status des Add-Ins wird als **Installation** angezeigt. Wenn die Installation abgeschlossen ist, aktualisieren Sie die Seite. Der Status sollte sich auf **Installiert** ändern.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Deinstallieren des Inventory Visibility-Add-Ins

Um das Bestandssichtbarkeits-Add-In zu deinstallieren, wählen Sie **Deinstallieren** auf der LCS-Seite. Der Deinstallationsvorgang beendet das Inventory Visibility-Add-In, hebt die Registrierung des Add-Ins im LCS auf und löscht alle temporären Daten, die im Daten-Cache des Inventory Visibility-Add-Ins gespeichert sind. Die primären Bestandsdaten, die in Ihrem Dataverse-Abonnement gespeichert sind, werden jedoch nicht gelöscht.

Um Bestandsdaten zu deinstallieren, die in Ihrem Dataverse-Abonnement gespeichert sind, öffnen Sie [Power Apps](https://make.powerapps.com), wählen Sie **Umgebung** in der Navigationsleiste und wählen Sie die Dataverse-Umgebung, die mit Ihrer LCS-Umgebung verbunden ist. Gehen Sie dann zu **Lösungen**, und löschen Sie die folgenden fünf Lösungen:

- Ankerlösung für Inventory Visibility-Anwendung in Dynamics 365-Lösungen
- Dynamics 365 FNO SCM Inventory Visibility-Anwendungslösung
- Bestandsservice-Konfiguration
- Eigenständige Inventory Visibility-Anwendung
- Dynamics 365 FNO SCM Inventory Visibility-Basislösung

Nachdem Sie diese Lösungen gelöscht haben, werden auch die Daten, die in Tabellen gespeichert sind, gelöscht.

## <a name="set-up-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Setup Supply Chain Management festlegen

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Bereitstellen des Integrationspakets für die Bestandssichtbarkeit

Wenn Sie Supply Chain Management Version 10.0.17 oder früher verwenden, wenden Sie sich an das Bestandssichtbarkeit On-Board-Support-Team unter [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), um die Paketdatei zu erhalten. Stellen Sie dann das Paket in LCS bereit.

> [!NOTE]
> Wenn beim Bereitstellen ein Fehler wegen Versionsinkongruenz auftritt, müssen Sie das X++ Projekt manuell in Ihre Entwicklungsumgebung importieren. Erstellen Sie dann das einsatzfähige Paket in Ihrer Entwicklungsumgebung und stellen Sie es in Ihrer Produktionsumgebung bereit.
>
> Der Code ist in der Supply Chain Management Version 10.0.18 enthalten. Wenn Sie diese Version oder eine spätere verwenden, ist das Bereitstellen nicht erforderlich.

Stellen Sie sicher, dass die folgenden Funktionen in Ihrer Supply Chain Management Umgebung aktiviert sind. (Standardmäßig sind sie eingeschaltet.)

| Beschreibung der Funktion | Code-Version | Klasse umschalten |
|---|---|---|
| Aktivieren oder deaktivieren Sie die Verwendung von Bestandsdimensionen in der Tabelle InventSum      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Aktivieren oder deaktivieren Sie die Verwendung von Bestandsdimensionen in der Tabelle InventSumDelta | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Integration der Bestandssichtbarkeit einrichten

1. Öffnen Sie im Supply Chain Management den Arbeitsbereich **[Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** und schalten Sie die Funktion *Bestandssichtbarkeit-Integration* ein.
1. Gehen Sie zu **Bestandsverwaltung \> Parameter für die \>-Bestandssichtbarkeits-Integration festlegen** und geben Sie die URL der Umgebung ein, in der Sie die Bestandssichtbarkeit ausführen. Weitere Informationen finden Sie unter [Finden Sie den Dienst-Endpunkt](inventory-visibility-power-platform.md#get-service-endpoint).
1. Gehen Sie zu **Bestandsverwaltung \> Periodisch \> Bestandssichtbarkeit-Integration**, und aktivieren Sie den Auftrag. Alle Ereignisse zu Bestandsänderungen aus dem Supply Chain Management werden nun in die Bestandssichtbarkeit übernommen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
