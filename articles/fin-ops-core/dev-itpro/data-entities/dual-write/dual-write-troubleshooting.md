---
title: Allgemeine Problembehandlung
description: Dieses Thema enthält allgemeine Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172690"
---
# <a name="general-troubleshooting"></a>Allgemeine Problembehandlung

[!include [banner](../../includes/banner.md)]



Dieses Thema enthält allgemeine Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Common Data Service.

> [!IMPORTANT]
> Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Wenn Sie versuchen, das Dual-Write-Paket mithilfe des Package Deployer Tools zu installieren, werden keine verfügbaren Lösungen angezeigt

Einige Versionen des Package Deployer Tools sind nicht mit dem Dual-Write-Lösungspaket kompatibel. Um das Paket erfolgreich zu installieren, müssen Sie [Version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) oder später des Package Deployer Tools verwenden.

Installieren Sie nach der Installation des Package Deployer Tools das Lösungspaket, indem Sie die folgenden Schritte ausführen.

1. Laden Sie die neueste Lösungspaketdatei von Yammer .com herunter. Nachdem die Paket-Zip-Datei heruntergeladen wurde, klicken Sie mit der rechten Maustaste darauf und wählen Sie **Eigenschaften**. Wählen Sie das Kontrollkästchen **Sperrung aufheben** und wählen Sie dann **Anwenden** aus. Wenn Sie das Kontrollkästchen **Entsperren** nicht sehen, ist die Zip-Datei bereits entsperrt, und Sie können diesen Schritt überspringen.

    ![Dialogfeld Eigenschaften](media/unblock_option.png)

2. Extrahieren Sie die Paket-Zip-Datei und kopieren Sie alle Dateien in die **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** Mappe.

    ![Inhalt des Ordners Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. Fügen Sie alle kopierten Dateien in den Ordner **Werkzeuge** im Package Deployer hinzu. 
4. Führen Sie **PackageDeployer.exe** aus, um die Common Data Service Umgebung auszuwählen und installieren Sie die Lösungen.

    ![Inhalt des Tools-Ordners](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a>Aktivieren und Anzeigen der Plug-In-Ablaufverfolgungsanmeldung Common Data Service, um Fehlerdetails anzuzeigen

**Erforderliche Rolle zum Aktivieren des Ablaufverfolgungsprotokolls und zum Anzeigen von Fehlern:** System Administrator

Um die Nachverfolgung einzuschalten, führen Sie diese Schritte aus.

1. Melden Sie sich bei der Finance and Operations App an, öffnen Sie die Seite **Einstellungen** und dann unter **System**, wählen Sie **Verwaltung**.
2. Wählen Sie auf der Seite **Verwaltung** die Option **Systemeinstellungen** aus.
3. Auf der Registerkarte **Anpassung** wählen Sie **Plug-In und benutzerdefinierte Workflow-Aktivitätsverfolgung** und **Alle**, um das Plug-Trace-Protokoll zu aktivieren. Wenn Sie Ablaufverfolgungsprotokolle nur protokollieren möchten, wenn Ausnahmen auftreten, können Sie stattdessen **Ausnahme** auswählen.


Um die Nachverfolgung anzuzeigen, führen Sie diese Schritte aus.

1. Melden Sie sich bei der Finance and Operations App an, öffnen Sie die Seite **Einstellungen** und dann unter **Anpassung**, wählen Sie **Plug-In-Ablaufverfolgungsprotokoll**.
2. Suchen Sie die Ablaufverfolgungsprotokolle, in denen das Feld **Modellname** auf **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** festgelegt ist.
3. Doppelklicken Sie auf ein Element, um das vollständige Protokoll anzuzeigen, und klicken Sie dann auf das Inforegister **Ausführung** und üerrprüfen Sie den Text **Nachrichtenblock**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Aktivieren Sie den Debug-Modus, um Probleme mit der Live-Synchronisierung in Finance and Operations Apps zu beheben

**Erforderliche Rolle zum Anzeigen der Fehler:** System Administrator

Dual-Write-Fehler, die ihren Ursprung in Common Data Service haben, können in der Finance and Operations App angezeigt werden. In einigen Fällen ist der vollständige Text der Fehlermeldung nicht verfügbar, da die Nachricht zu lang ist oder personenbezogene Daten (PII) enthält. Sie können die ausführliche Protokollierung für Fehler aktivieren, indem Sie die folgenden Schritte ausführen.

1. Alle Projektkonfigurationen in Finance and Operations Apps haben eine **IsDebugMode** Eigenschaft in der **DualWriteProjectConfiguration** Entität. Entität in **DualWriteProjectConfiguration** mithilfe des Excel-Add-Ins öffnen.

    > [!TIP]
    > Eine einfache Möglichkeit, die Entität zu öffnen, ist das Einschalten des Modus **Design** im Excel-Add-In und dann das Hinzufügen von **DualWriteProjectConfigurationEntity** zum Arbeitsblatt. Weitere Informationen finden Sie unter [Entitätsdaten in Excel öffnen und sie mithilfe des Excel-Add-Ins aktualisieren](../../office-integration/use-excel-add-in.md).

2. Stellen Sie die **IsDebugMode** Eigenschaft auf **Ja** für das Projekt.
3. Führen Sie das Szenario aus, das Fehler generiert.
4. Die ausführlichen Protokolle sind in der Tabelle DualWriteErrorLog verfügbar. Verwenden Sie die folgende URL, um Daten im Tabellenbrowser nachzuschlagen (**XXX** wie erforderlich ersetzen):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Überprüfen Sie die Synchronisierungsfehler auf der virtuellen Maschine auf der Finance and Operations App

**Erforderliche Rolle zum Anzeigen der Fehler:** System Administrator

1. Melden Sie sich bei Microsoft Dynamics Lifecycle Services (LCS) an.
2. Öffnet das LCS-Projekt, das Sie ausgewählt haben, um das Testing für das duale Schreiben durchzuführen.
3. Wählen Sie die Kachel **Cloud gehostete Umgebungen** aus.
4. Verwenden Sie Remotedesktop, um sich bei der virtuellen Maschine (VM) für die Finance and Operations App anzumelden. Verwenden Sie das lokale Konte, das in LCS angezeigt wird.
5. Öffnen Sie nun die Ereignisanzeige.
6. Wählen Sie **Anwendungs- und Dienstprotokolle \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operativ**.
7. Überprüfen Sie die Liste der letzten Fehler.

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a>Verknüpfung aufheben und eine andere Common Data Service Umgebung aus einer Finance and Operations App verknüpfen

**Erforderliche Anmeldeinformationen zum Aufheben der Verknüpfung der Umgebung:** Azure AD Mandant admin

1. Bei der Finance and Operations App anmelden.
2. Gehe zu **Arbeitsbereiche \>Datenmanagement** und wählen Sie die Kachel **Duales Schreiben**.
3. Wählen Sie alle ausgeführten Zuordnungen aus, und wählen Sie **Beenden**.
4. Wählen Sie **Verknüpfung für Umgebung aufheben** aus.
5. Wählen Sie **Ja** aus, um den Vorgang zu bestätigen.

Sie können jetzt eine neue Umgebung verknüpfen.