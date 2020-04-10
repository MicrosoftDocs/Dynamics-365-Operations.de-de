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
# <a name="general-troubleshooting"></a><span data-ttu-id="18f14-103">Allgemeine Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="18f14-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="18f14-104">Dieses Thema enthält allgemeine Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="18f14-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="18f14-105">Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators.</span><span class="sxs-lookup"><span data-stu-id="18f14-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="18f14-106">Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="18f14-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="18f14-107">Wenn Sie versuchen, das Dual-Write-Paket mithilfe des Package Deployer Tools zu installieren, werden keine verfügbaren Lösungen angezeigt</span><span class="sxs-lookup"><span data-stu-id="18f14-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="18f14-108">Einige Versionen des Package Deployer Tools sind nicht mit dem Dual-Write-Lösungspaket kompatibel.</span><span class="sxs-lookup"><span data-stu-id="18f14-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="18f14-109">Um das Paket erfolgreich zu installieren, müssen Sie [Version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) oder später des Package Deployer Tools verwenden.</span><span class="sxs-lookup"><span data-stu-id="18f14-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="18f14-110">Installieren Sie nach der Installation des Package Deployer Tools das Lösungspaket, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="18f14-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="18f14-111">Laden Sie die neueste Lösungspaketdatei von Yammer .com herunter.</span><span class="sxs-lookup"><span data-stu-id="18f14-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="18f14-112">Nachdem die Paket-Zip-Datei heruntergeladen wurde, klicken Sie mit der rechten Maustaste darauf und wählen Sie **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="18f14-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="18f14-113">Wählen Sie das Kontrollkästchen **Sperrung aufheben** und wählen Sie dann **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="18f14-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="18f14-114">Wenn Sie das Kontrollkästchen **Entsperren** nicht sehen, ist die Zip-Datei bereits entsperrt, und Sie können diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="18f14-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Dialogfeld Eigenschaften](media/unblock_option.png)

2. <span data-ttu-id="18f14-116">Extrahieren Sie die Paket-Zip-Datei und kopieren Sie alle Dateien in die **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** Mappe.</span><span class="sxs-lookup"><span data-stu-id="18f14-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Inhalt des Ordners Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="18f14-118">Fügen Sie alle kopierten Dateien in den Ordner **Werkzeuge** im Package Deployer hinzu.</span><span class="sxs-lookup"><span data-stu-id="18f14-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="18f14-119">Führen Sie **PackageDeployer.exe** aus, um die Common Data Service Umgebung auszuwählen und installieren Sie die Lösungen.</span><span class="sxs-lookup"><span data-stu-id="18f14-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Inhalt des Tools-Ordners](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="18f14-121">Aktivieren und Anzeigen der Plug-In-Ablaufverfolgungsanmeldung Common Data Service, um Fehlerdetails anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="18f14-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="18f14-122">**Erforderliche Rolle zum Aktivieren des Ablaufverfolgungsprotokolls und zum Anzeigen von Fehlern:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="18f14-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="18f14-123">Um die Nachverfolgung einzuschalten, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="18f14-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="18f14-124">Melden Sie sich bei der Finance and Operations App an, öffnen Sie die Seite **Einstellungen** und dann unter **System**, wählen Sie **Verwaltung**.</span><span class="sxs-lookup"><span data-stu-id="18f14-124">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="18f14-125">Wählen Sie auf der Seite **Verwaltung** die Option **Systemeinstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="18f14-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="18f14-126">Auf der Registerkarte **Anpassung** wählen Sie **Plug-In und benutzerdefinierte Workflow-Aktivitätsverfolgung** und **Alle**, um das Plug-Trace-Protokoll zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="18f14-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="18f14-127">Wenn Sie Ablaufverfolgungsprotokolle nur protokollieren möchten, wenn Ausnahmen auftreten, können Sie stattdessen **Ausnahme** auswählen.</span><span class="sxs-lookup"><span data-stu-id="18f14-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="18f14-128">Um die Nachverfolgung anzuzeigen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="18f14-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="18f14-129">Melden Sie sich bei der Finance and Operations App an, öffnen Sie die Seite **Einstellungen** und dann unter **Anpassung**, wählen Sie **Plug-In-Ablaufverfolgungsprotokoll**.</span><span class="sxs-lookup"><span data-stu-id="18f14-129">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="18f14-130">Suchen Sie die Ablaufverfolgungsprotokolle, in denen das Feld **Modellname** auf **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="18f14-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span></span>
3. <span data-ttu-id="18f14-131">Doppelklicken Sie auf ein Element, um das vollständige Protokoll anzuzeigen, und klicken Sie dann auf das Inforegister **Ausführung** und üerrprüfen Sie den Text **Nachrichtenblock**.</span><span class="sxs-lookup"><span data-stu-id="18f14-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="18f14-132">Aktivieren Sie den Debug-Modus, um Probleme mit der Live-Synchronisierung in Finance and Operations Apps zu beheben</span><span class="sxs-lookup"><span data-stu-id="18f14-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="18f14-133">**Erforderliche Rolle zum Anzeigen der Fehler:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="18f14-133">**Required role to view the errors:** System admin</span></span>

<span data-ttu-id="18f14-134">Dual-Write-Fehler, die ihren Ursprung in Common Data Service haben, können in der Finance and Operations App angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="18f14-134">Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="18f14-135">In einigen Fällen ist der vollständige Text der Fehlermeldung nicht verfügbar, da die Nachricht zu lang ist oder personenbezogene Daten (PII) enthält.</span><span class="sxs-lookup"><span data-stu-id="18f14-135">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="18f14-136">Sie können die ausführliche Protokollierung für Fehler aktivieren, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="18f14-136">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="18f14-137">Alle Projektkonfigurationen in Finance and Operations Apps haben eine **IsDebugMode** Eigenschaft in der **DualWriteProjectConfiguration** Entität.</span><span class="sxs-lookup"><span data-stu-id="18f14-137">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="18f14-138">Entität in **DualWriteProjectConfiguration** mithilfe des Excel-Add-Ins öffnen.</span><span class="sxs-lookup"><span data-stu-id="18f14-138">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="18f14-139">Eine einfache Möglichkeit, die Entität zu öffnen, ist das Einschalten des Modus **Design** im Excel-Add-In und dann das Hinzufügen von **DualWriteProjectConfigurationEntity** zum Arbeitsblatt.</span><span class="sxs-lookup"><span data-stu-id="18f14-139">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="18f14-140">Weitere Informationen finden Sie unter [Entitätsdaten in Excel öffnen und sie mithilfe des Excel-Add-Ins aktualisieren](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="18f14-140">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="18f14-141">Stellen Sie die **IsDebugMode** Eigenschaft auf **Ja** für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="18f14-141">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="18f14-142">Führen Sie das Szenario aus, das Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="18f14-142">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="18f14-143">Die ausführlichen Protokolle sind in der Tabelle DualWriteErrorLog verfügbar.</span><span class="sxs-lookup"><span data-stu-id="18f14-143">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="18f14-144">Verwenden Sie die folgende URL, um Daten im Tabellenbrowser nachzuschlagen (**XXX** wie erforderlich ersetzen):</span><span class="sxs-lookup"><span data-stu-id="18f14-144">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="18f14-145">Überprüfen Sie die Synchronisierungsfehler auf der virtuellen Maschine auf der Finance and Operations App</span><span class="sxs-lookup"><span data-stu-id="18f14-145">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="18f14-146">**Erforderliche Rolle zum Anzeigen der Fehler:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="18f14-146">**Required role to view the errors:** System admin</span></span>

1. <span data-ttu-id="18f14-147">Melden Sie sich bei Microsoft Dynamics Lifecycle Services (LCS) an.</span><span class="sxs-lookup"><span data-stu-id="18f14-147">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="18f14-148">Öffnet das LCS-Projekt, das Sie ausgewählt haben, um das Testing für das duale Schreiben durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="18f14-148">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="18f14-149">Wählen Sie die Kachel **Cloud gehostete Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="18f14-149">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="18f14-150">Verwenden Sie Remotedesktop, um sich bei der virtuellen Maschine (VM) für die Finance and Operations App anzumelden.</span><span class="sxs-lookup"><span data-stu-id="18f14-150">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="18f14-151">Verwenden Sie das lokale Konte, das in LCS angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="18f14-151">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="18f14-152">Öffnen Sie nun die Ereignisanzeige.</span><span class="sxs-lookup"><span data-stu-id="18f14-152">Open Event viewer.</span></span>
6. <span data-ttu-id="18f14-153">Wählen Sie **Anwendungs- und Dienstprotokolle \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operativ**.</span><span class="sxs-lookup"><span data-stu-id="18f14-153">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="18f14-154">Überprüfen Sie die Liste der letzten Fehler.</span><span class="sxs-lookup"><span data-stu-id="18f14-154">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="18f14-155">Verknüpfung aufheben und eine andere Common Data Service Umgebung aus einer Finance and Operations App verknüpfen</span><span class="sxs-lookup"><span data-stu-id="18f14-155">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="18f14-156">**Erforderliche Anmeldeinformationen zum Aufheben der Verknüpfung der Umgebung:** Azure AD Mandant admin</span><span class="sxs-lookup"><span data-stu-id="18f14-156">**Required credentials to unlink the environment:** Azure AD tenant admin</span></span>

1. <span data-ttu-id="18f14-157">Bei der Finance and Operations App anmelden.</span><span class="sxs-lookup"><span data-stu-id="18f14-157">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="18f14-158">Gehe zu **Arbeitsbereiche \>Datenmanagement** und wählen Sie die Kachel **Duales Schreiben**.</span><span class="sxs-lookup"><span data-stu-id="18f14-158">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="18f14-159">Wählen Sie alle ausgeführten Zuordnungen aus, und wählen Sie **Beenden**.</span><span class="sxs-lookup"><span data-stu-id="18f14-159">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="18f14-160">Wählen Sie **Verknüpfung für Umgebung aufheben** aus.</span><span class="sxs-lookup"><span data-stu-id="18f14-160">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="18f14-161">Wählen Sie **Ja** aus, um den Vorgang zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="18f14-161">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="18f14-162">Sie können jetzt eine neue Umgebung verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="18f14-162">You can now link a new environment.</span></span>
