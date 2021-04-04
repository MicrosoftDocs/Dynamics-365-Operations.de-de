---
title: Allgemeine Problembehandlung
description: Dieses Thema enthält allgemeine Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
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
ms.openlocfilehash: 4b97fffce6d1c3ea143e0d8445769e794d0c46a4
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566099"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="8f282-103">Allgemeine Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="8f282-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="8f282-104">Dieses Thema enthält allgemeine Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8f282-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f282-105">Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators.</span><span class="sxs-lookup"><span data-stu-id="8f282-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="8f282-106">Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8f282-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="8f282-107">Wenn Sie versuchen, das Dual-Write-Paket mithilfe des Package Deployer Tools zu installieren, werden keine verfügbaren Lösungen angezeigt</span><span class="sxs-lookup"><span data-stu-id="8f282-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="8f282-108">Einige Versionen des Package Deployer Tools sind nicht mit dem Dual-Write-Lösungspaket kompatibel.</span><span class="sxs-lookup"><span data-stu-id="8f282-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="8f282-109">Um das Paket erfolgreich zu installieren, müssen Sie [Version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) oder später des Package Deployer Tools verwenden.</span><span class="sxs-lookup"><span data-stu-id="8f282-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="8f282-110">Installieren Sie nach der Installation des Package Deployer Tools das Lösungspaket, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f282-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="8f282-111">Laden Sie die neueste Lösungspaketdatei von Yammer .com herunter.</span><span class="sxs-lookup"><span data-stu-id="8f282-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="8f282-112">Nachdem die Paket-Zip-Datei heruntergeladen wurde, klicken Sie mit der rechten Maustaste darauf und wählen Sie **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="8f282-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="8f282-113">Wählen Sie das Kontrollkästchen **Sperrung aufheben** und wählen Sie dann **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="8f282-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="8f282-114">Wenn Sie das Kontrollkästchen **Entsperren** nicht sehen, ist die Zip-Datei bereits entsperrt, und Sie können diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="8f282-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Dialogfeld Eigenschaften](media/unblock_option.png)

2. <span data-ttu-id="8f282-116">Extrahieren Sie die Paket-Zip-Datei und kopieren Sie alle Dateien in die **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** Mappe.</span><span class="sxs-lookup"><span data-stu-id="8f282-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Inhalt des Ordners Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="8f282-118">Fügen Sie alle kopierten Dateien in den Ordner **Werkzeuge** im Package Deployer hinzu.</span><span class="sxs-lookup"><span data-stu-id="8f282-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="8f282-119">Führen Sie **PackageDeployer.exe** aus, um die Dataverse Umgebung auszuwählen und installieren Sie die Lösungen.</span><span class="sxs-lookup"><span data-stu-id="8f282-119">Run **PackageDeployer.exe** to select the Dataverse environment and install the solutions.</span></span>

    ![Inhalt des Tools-Ordners](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a><span data-ttu-id="8f282-121">Aktivieren und Anzeigen des Plug-In-Überwachungsprotokolls in Dataverse, um Fehlerdetails anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="8f282-121">Enable and view the plug-in trace log in Dataverse to view error details</span></span>

<span data-ttu-id="8f282-122">**Erforderliche Rolle zum Aktivieren des Ablaufverfolgungsprotokolls und zum Anzeigen von Fehlern:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="8f282-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="8f282-123">Um die Nachverfolgung einzuschalten, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="8f282-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="8f282-124">Melden Sie sich bei der modellgesteuerten App in Dynamics 365 an, öffnen Sie die Seite **Einstellungen** und dann unter **System** wählen Sie **Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="8f282-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="8f282-125">Wählen Sie auf der Seite **Verwaltung** die Option **Systemeinstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="8f282-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="8f282-126">Auf der Registerkarte **Anpassung** wählen Sie in der Spalte **Plug-In und benutzerdefinierte Workflow-Aktivitätsverfolgung** **Alle** aus, um das Plug-Trace-Protokoll zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f282-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** column, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="8f282-127">Wenn Sie Ablaufverfolgungsprotokolle nur protokollieren möchten, wenn Ausnahmen auftreten, können Sie stattdessen **Ausnahme** auswählen.</span><span class="sxs-lookup"><span data-stu-id="8f282-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="8f282-128">Um die Nachverfolgung anzuzeigen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="8f282-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="8f282-129">Melden Sie sich bei der modellgesteuerten App in Dynamics 365 an, öffnen Sie die Seite **Einstellungen** und dann unter **Anpassung** wählen Sie **Plug-In-Nachverfolgungsprotokoll** aus.</span><span class="sxs-lookup"><span data-stu-id="8f282-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="8f282-130">Suchen Sie die Ablaufverfolgungsprotokolle, in denen die Spalte **Typname** auf **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8f282-130">Find the trace logs where the **Type Name** column is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="8f282-131">Doppelklicken Sie auf ein Element, um das vollständige Protokoll anzuzeigen, und klicken Sie dann auf das Inforegister **Ausführung** und üerrprüfen Sie den Text **Nachrichtenblock**.</span><span class="sxs-lookup"><span data-stu-id="8f282-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="8f282-132">Aktivieren Sie den Debug-Modus, um Probleme mit der Live-Synchronisierung in Finance and Operations Apps zu beheben</span><span class="sxs-lookup"><span data-stu-id="8f282-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="8f282-133">**Erforderliche Rolle zum Anzeigen der Fehler:** Systemadministrator – duale Schreibfehler, die ihren Ursprung im Dataverse haben, können in der Finance and Operations-App auftreten.</span><span class="sxs-lookup"><span data-stu-id="8f282-133">**Required role to view the errors:** System admin Dual-write errors that originate in Dataverse can appear in the Finance and Operations app.</span></span> <span data-ttu-id="8f282-134">In einigen Fällen ist der vollständige Text der Fehlermeldung nicht verfügbar, da die Nachricht zu lang ist oder personenbezogene Daten (PII) enthält.</span><span class="sxs-lookup"><span data-stu-id="8f282-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="8f282-135">Sie können die ausführliche Protokollierung für Fehler aktivieren, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f282-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="8f282-136">Alle Projektkonfigurationen in Finance and Operations-Apps haben eine **IsDebugMode**-Eigenschaft in der Tabelle **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8f282-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** table.</span></span> <span data-ttu-id="8f282-137">Öffnen Sie die Tabelle **DualWriteProjectConfiguration** mithilfe des Excel-Add-Ins.</span><span class="sxs-lookup"><span data-stu-id="8f282-137">Open the **DualWriteProjectConfiguration** table by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="8f282-138">Eine einfache Möglichkeit, die Tabelle zu öffnen, ist das Einschalten des Modus **Entwurf** im Excel-Add-In und dann das Hinzufügen von **DualWriteProjectConfigurationEntity** zum Arbeitsblatt.</span><span class="sxs-lookup"><span data-stu-id="8f282-138">An easy way to open the table is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="8f282-139">Weitere Informationen finden Sie unter [Tabellendaten in Excel öffnen und sie mithilfe des Excel-Add-Ins aktualisieren](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="8f282-139">For more information, see [Open table data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="8f282-140">Stellen Sie die **IsDebugMode** Eigenschaft auf **Ja** für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="8f282-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="8f282-141">Führen Sie das Szenario aus, das Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="8f282-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="8f282-142">Die ausführlichen Protokolle sind in der Tabelle DualWriteErrorLog verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8f282-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="8f282-143">Verwenden Sie die folgende URL, um Daten im Tabellenbrowser nachzuschlagen (**XXX** wie erforderlich ersetzen):</span><span class="sxs-lookup"><span data-stu-id="8f282-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="8f282-144">Überprüfen Sie die Synchronisierungsfehler auf der virtuellen Maschine auf der Finance and Operations App</span><span class="sxs-lookup"><span data-stu-id="8f282-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="8f282-145">**Erforderliche Rolle zum Anzeigen der Fehler:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="8f282-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="8f282-146">Melden Sie sich bei Microsoft Dynamics Lifecycle Services (LCS) an.</span><span class="sxs-lookup"><span data-stu-id="8f282-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="8f282-147">Öffnet das LCS-Projekt, das Sie ausgewählt haben, um das Testing für das duale Schreiben durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="8f282-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="8f282-148">Wählen Sie die Kachel **Cloud gehostete Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="8f282-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="8f282-149">Verwenden Sie Remotedesktop, um sich bei der virtuellen Maschine (VM) für die Finance and Operations App anzumelden.</span><span class="sxs-lookup"><span data-stu-id="8f282-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="8f282-150">Verwenden Sie das lokale Konte, das in LCS angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8f282-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="8f282-151">Öffnen Sie nun die Ereignisanzeige.</span><span class="sxs-lookup"><span data-stu-id="8f282-151">Open Event viewer.</span></span>
6. <span data-ttu-id="8f282-152">Wählen Sie **Anwendungs- und Dienstprotokolle \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operativ**.</span><span class="sxs-lookup"><span data-stu-id="8f282-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="8f282-153">Überprüfen Sie die Liste der letzten Fehler.</span><span class="sxs-lookup"><span data-stu-id="8f282-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="8f282-154">Verknüpfung aufheben und eine andere Dataverse Umgebung aus einer Finance and Operations App verknüpfen</span><span class="sxs-lookup"><span data-stu-id="8f282-154">Unlink and link another Dataverse environment from a Finance and Operations app</span></span>

<span data-ttu-id="8f282-155">**Erforderliche Rolle zum Aufheben der Umgebungsverknüpfung:** Systemadministrator für die Finance and Operations-App oder Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8f282-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Dataverse.</span></span>

1. <span data-ttu-id="8f282-156">Bei der Finance and Operations App anmelden.</span><span class="sxs-lookup"><span data-stu-id="8f282-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="8f282-157">Gehe zu **Arbeitsbereiche \>Datenmanagement** und wählen Sie die Kachel **Duales Schreiben**.</span><span class="sxs-lookup"><span data-stu-id="8f282-157">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="8f282-158">Wählen Sie alle ausgeführten Zuordnungen aus, und wählen Sie **Beenden**.</span><span class="sxs-lookup"><span data-stu-id="8f282-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="8f282-159">Wählen Sie **Verknüpfung für Umgebung aufheben** aus.</span><span class="sxs-lookup"><span data-stu-id="8f282-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="8f282-160">Wählen Sie **Ja** aus, um den Vorgang zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="8f282-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="8f282-161">Sie können jetzt eine neue Umgebung verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="8f282-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="8f282-162">Das Formular für die Auftragspositionsinformationen können nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8f282-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="8f282-163">Wenn Sie in Dynamics 365 Sales einen Autrag erstellen, können Sie durch das Klicken auf **+ Produkte hinzufügen** möglicherweise zum Bestellformular für Dynamics 365 Project Operations weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="8f282-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="8f282-164">Von diesem Formular aus gibt es keine Möglichkeit, das Formular **Information** der Kundenauftragsposition anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8f282-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="8f282-165">Die Option für **Information** wird in der Dropdownliste unter **Neue Auftragsposition** nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f282-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="8f282-166">Dies liegt daran, dass Project Operations in Ihrer Umgebung installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8f282-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="8f282-167">Um die Formularoption **Information** wieder zu aktivieren, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="8f282-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="8f282-168">Navigieren Sie zur Tabelle **Auftragsposition**.</span><span class="sxs-lookup"><span data-stu-id="8f282-168">Navigate to the **Order Line** table.</span></span>
2. <span data-ttu-id="8f282-169">Suchen Sie das **Information**-Formular unter dem Formularknoten.</span><span class="sxs-lookup"><span data-stu-id="8f282-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="8f282-170">Wählen Sie das Formular **Information** und klicken Sie auf **Sicherheitsrollen aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="8f282-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="8f282-171">Ändern Sie die Sicherheitseinstellung in **Anzeige für alle**.</span><span class="sxs-lookup"><span data-stu-id="8f282-171">Change the security setting to **Display to everyone**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]