---
title: Allgemeine Problembehandlung
description: Dieses Thema enthält allgemeine Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b4de461d26fc6d5c39c1ac0c49201f265f562f5a
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542490"
---
# <a name="general-troubleshooting"></a>Allgemeine Problembehandlung

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dieses Thema enthält allgemeine Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse.

> [!IMPORTANT]
> Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Wenn Sie versuchen, das Dual-Write-Paket mithilfe des Package Deployer Tools zu installieren, werden keine verfügbaren Lösungen angezeigt

Einige Versionen des Package Deployer Tools sind nicht mit dem Dual-Write-Lösungspaket kompatibel. Um das Paket erfolgreich zu installieren, müssen Sie [Version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) oder später des Package Deployer Tools verwenden.

Installieren Sie nach der Installation des Package Deployer Tools das Lösungspaket, indem Sie die folgenden Schritte ausführen.

1. Laden Sie die neueste Lösungspaketdatei von Yammer .com herunter. Nachdem die Paket-Zip-Datei heruntergeladen wurde, klicken Sie mit der rechten Maustaste darauf und wählen Sie **Eigenschaften**. Wählen Sie das Kontrollkästchen **Sperrung aufheben** und wählen Sie dann **Anwenden** aus. Wenn Sie das Kontrollkästchen **Entsperren** nicht sehen, ist die Zip-Datei bereits entsperrt, und Sie können diesen Schritt überspringen.

    ![Dialogfeld „Eigenschaften“.](media/unblock_option.png)

2. Extrahieren Sie die Paket-Zip-Datei und kopieren Sie alle Dateien in die **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** Mappe.

    ![Inhalt des Ordners Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438.](media/extract_package.png)

3. Fügen Sie alle kopierten Dateien in den Ordner **Werkzeuge** im Package Deployer hinzu. 
4. Führen Sie **PackageDeployer.exe** aus, um die Dataverse Umgebung auszuwählen und installieren Sie die Lösungen.

    ![Inhalt des Tools-Ordners.](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Aktivieren und Anzeigen des Plug-In-Überwachungsprotokolls in Dataverse, um Fehlerdetails anzuzeigen

**Erforderliche Rolle zum Aktivieren des Ablaufverfolgungsprotokolls und zum Anzeigen von Fehlern:** System Administrator

Um die Nachverfolgung einzuschalten, führen Sie diese Schritte aus.

1. Melden Sie sich bei der Kundenbindungs-App an, öffnen Sie die Seite **Einstellungen** und dann unter **System**, wählen Sie **Verwaltung**.
2. Wählen Sie auf der Seite **Verwaltung** die Option **Systemeinstellungen** aus.
3. Auf der Registerkarte **Anpassung** wählen Sie in der Spalte **Plug-In und benutzerdefinierte Workflow-Aktivitätsverfolgung** **Alle** aus, um das Plug-Trace-Protokoll zu aktivieren. Wenn Sie Ablaufverfolgungsprotokolle nur protokollieren möchten, wenn Ausnahmen auftreten, können Sie stattdessen **Ausnahme** auswählen.


Um die Nachverfolgung anzuzeigen, führen Sie diese Schritte aus.

1. Melden Sie sich bei der Kundenbindungs-App an, öffnen Sie die Seite **Einstellungen** und dann unter **Anpassung**, wählen Sie **Plug-In-Ablaufverfolgungsprotokoll**.
2. Suchen Sie die Ablaufverfolgungsprotokolle, in denen die Spalte **Typname** auf **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin** festgelegt ist.
3. Doppelklicken Sie auf ein Element, um das vollständige Protokoll anzuzeigen, und klicken Sie dann auf das Inforegister **Ausführung** und üerrprüfen Sie den Text **Nachrichtenblock**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Aktivieren Sie den Debug-Modus, um Probleme mit der Live-Synchronisierung in Finance and Operations Apps zu beheben

**Erforderliche Rolle zum Anzeigen der Fehler:** Systemadministrator – duale Schreibfehler, die ihren Ursprung im Dataverse haben, können in der Finance and Operations-App auftreten. In einigen Fällen ist der vollständige Text der Fehlermeldung nicht verfügbar, da die Nachricht zu lang ist oder personenbezogene Daten (PII) enthält. Sie können die ausführliche Protokollierung für Fehler aktivieren, indem Sie die folgenden Schritte ausführen.

1. Alle Projektkonfigurationen in Finance and Operations-Apps haben eine **IsDebugMode**-Eigenschaft in der Tabelle **DualWriteProjectConfiguration**. Öffnen Sie die Tabelle **DualWriteProjectConfiguration** mithilfe des Excel-Add-Ins.

    > [!TIP]
    > Eine einfache Möglichkeit, die Tabelle zu öffnen, ist das Einschalten des Modus **Entwurf** im Excel-Add-In und dann das Hinzufügen von **DualWriteProjectConfigurationEntity** zum Arbeitsblatt. Weitere Informationen finden Sie unter [Tabellendaten in Excel öffnen und sie mithilfe des Excel-Add-Ins aktualisieren](../../office-integration/use-excel-add-in.md).

2. Stellen Sie die **IsDebugMode** Eigenschaft auf **Ja** für das Projekt.
3. Führen Sie das Szenario aus, das Fehler generiert.
4. Die ausführlichen Protokolle sind in der Tabelle DualWriteErrorLog verfügbar. Verwenden Sie die folgende URL, um Daten im Tabellenbrowser nachzuschlagen (**XXX** wie erforderlich ersetzen):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Überprüfen Sie die Synchronisierungsfehler auf der virtuellen Maschine auf der Finance and Operations App

**Erforderliche Rolle zum Anzeigen der Fehler:** Systemadministrator

1. Melden Sie sich bei Microsoft Dynamics Lifecycle Services (LCS) an.
2. Öffnet das LCS-Projekt, das Sie ausgewählt haben, um das Testing für das duale Schreiben durchzuführen.
3. Wählen Sie die Kachel **Cloud gehostete Umgebungen** aus.
4. Verwenden Sie Remotedesktop, um sich bei der virtuellen Maschine (VM) für die Finance and Operations App anzumelden. Verwenden Sie das lokale Konte, das in LCS angezeigt wird.
5. Öffnen Sie nun die Ereignisanzeige.
6. Wählen Sie **Anwendungs- und Dienstprotokolle \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operativ**.
7. Überprüfen Sie die Liste der letzten Fehler.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Verknüpfung aufheben und eine andere Dataverse Umgebung aus einer Finance and Operations App verknüpfen

**Erforderliche Rolle zum Aufheben der Umgebungsverknüpfung:** Systemadministrator für die Finance and Operations-App oder Dataverse.

1. Bei der Finance and Operations App anmelden.
2. Gehe zu **Arbeitsbereiche \> Datenmanagement** und wählen Sie die Kachel **Duales Schreiben**.
3. Wählen Sie alle ausgeführten Zuordnungen aus, und wählen Sie **Beenden**.
4. Wählen Sie **Verknüpfung für Umgebung aufheben** aus.
5. Wählen Sie **Ja** aus, um den Vorgang zu bestätigen.

Sie können jetzt eine neue Umgebung verknüpfen.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Das Formular für die Auftragspositionsinformationen können nicht angezeigt werden. 

Wenn Sie in Dynamics 365 Sales einen Autrag erstellen, können Sie durch das Klicken auf **+ Produkte hinzufügen** möglicherweise zum Bestellformular für Dynamics 365 Project Operations weitergeleitet werden. Von diesem Formular aus gibt es keine Möglichkeit, das Formular **Information** der Kundenauftragsposition anzuzeigen. Die Option für **Information** wird in der Dropdownliste unter **Neue Auftragsposition** nicht angezeigt. Dies liegt daran, dass Project Operations in Ihrer Umgebung installiert wurde.

Um die Formularoption **Information** wieder zu aktivieren, führen Sie die folgenden Schritte aus:
1. Navigieren Sie zur Tabelle **Auftragsposition**.
2. Suchen Sie das **Information**-Formular unter dem Formularknoten. 
3. Wählen Sie das Formular **Information** und klicken Sie auf **Sicherheitsrollen aktivieren**. 
4. Ändern Sie die Sicherheitseinstellung in **Anzeige für alle**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]