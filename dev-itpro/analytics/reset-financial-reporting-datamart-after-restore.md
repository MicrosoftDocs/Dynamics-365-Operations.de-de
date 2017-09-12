---
title: "Finanzberichts-Data Mart noch Wiederherstellung der Datenbank Zurücksetzen"
description: "In diesem Thema wird beschrieben, wie Finanzberichts-Data Mart zurückgesetzt wird, nachdem die Microsoft Dynamics 365 for Finance and Operations-Datenbank wiederhergestellt wurde."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: de-de
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="7a8be-103">Finanzberichts-Data Mart noch Wiederherstellung der Datenbank Zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="7a8be-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7a8be-104">In diesem Thema wird beschrieben, wie Finanzberichts-Data Mart zurückgesetzt wird, nachdem die Microsoft Dynamics 365 for Finance and Operations-Datenbank wiederhergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7a8be-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="7a8be-105">Wenn Sie ggf. die Finanz- und Arbeitsgangsdatenbank aus einer Sicherung wiederherstellen oder die Datenbank aus einer anderen Umgebung kopieren, müssen Sie die Schritte in diesem Thema ausführen, um sicherzustellen, dass der Rechnungslegungs-datamart ordnungsgemäß die zu stornierenden Finanz- und Arbeitsgangsdatenbank verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a8be-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="7a8be-106">Beachten Sie, dass die Schritte dieses Prozesses für Dynamics 365 for Operations Mai 2016 (App-Build 7.0.1265.23014 und Financial Reporting Build 7.0.10000.4) und später Versionen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7a8be-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="7a8be-107">Wenn Sie eine frühere Version von Finance and Operations nutzen, wenden Sie sich bitte an unser Support-Team.</span><span class="sxs-lookup"><span data-stu-id="7a8be-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="7a8be-108">Exportieren von Berichtsdefinitionen</span><span class="sxs-lookup"><span data-stu-id="7a8be-108">Export report definitions</span></span>
<span data-ttu-id="7a8be-109">Zuerst exportieren Sie die Berichtsdesigns im Berichts-Designer, und zwar mithilfe der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="7a8be-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="7a8be-110">Wechseln Sie im Berichts-Designer zu **Unternehmen** &gt; **Bausteingruppen**.</span><span class="sxs-lookup"><span data-stu-id="7a8be-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="7a8be-111">Wählen Sie die Bausteingruppe aus, die exportiert werden soll, und klicken Sie **Export**.</span><span class="sxs-lookup"><span data-stu-id="7a8be-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="7a8be-112">Für Finance and Operations wird nur eine Bausteingruppe, unterstützt **Standard**.</span><span class="sxs-lookup"><span data-stu-id="7a8be-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="7a8be-113">Wählen Sie die Berichtsdefinition für den Export aus:</span><span class="sxs-lookup"><span data-stu-id="7a8be-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="7a8be-114">Um alle Ihre Berichtsdefinitionen und die zugeordneten Bausteine zu exportieren, klicken Sie auf **Alles auswählen**.</span><span class="sxs-lookup"><span data-stu-id="7a8be-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="7a8be-115">Um bestimmte Berichte, Zeilen, Spalten, Strukturen oder Dimensionssätze zu exportieren, klicken Sie auf die entsprechende Registerkarte und wählen die Artikel aus, die exportiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7a8be-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="7a8be-116">Drücken und halten Sie die STRG-Taste gedrückt, um mehrere Elemente in einer Registerkarte auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="7a8be-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="7a8be-117">Wenn Sie Berichte zum Exportieren auswählen, werden die zugeordneten Zeilen, Spalten, Baumstrukturen und Dimensionssätze ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="7a8be-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="7a8be-118">Klicken Sie auf "**Export**".</span><span class="sxs-lookup"><span data-stu-id="7a8be-118">Click **Export**.</span></span>
5.  <span data-ttu-id="7a8be-119">Geben Sie einen Dateinamen eingeben und einen sicheren Ort aus, an dem Sie die exportierten Berichtsdefinitionen speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="7a8be-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="7a8be-120">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7a8be-120">Click **Save**.</span></span>

<span data-ttu-id="7a8be-121">Die Datei kann an einem sicheren Speicherort kopiert oder hochgeladen werden und in einer anderen Umgebung, in einer anderen der Zeitpunkt importiert werden können.</span><span class="sxs-lookup"><span data-stu-id="7a8be-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="7a8be-122">Informationen zur Verwendung eines Microsoft Azure Storage-Kontos können gefunden werden in [Daten mit dem AzCopy-Kommandozeilenutility übertragen](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="7a8be-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="7a8be-123">Microsoft stellt kein Speicherkonto im Rahmen der Finance and Operations Vereinbarung bereit.</span><span class="sxs-lookup"><span data-stu-id="7a8be-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="7a8be-124">Sie müssen entweder ein Speicherkonto kaufen oder ein Speicherkonto von einem separaten Azure-Abonnement verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a8be-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="7a8be-125">Wichtig: Berücksichtigen Sie das Verhalten des D-Laufwerks von Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="7a8be-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="7a8be-126">Speichern Sie nicht die exportierten Bausteingruppen dort dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="7a8be-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="7a8be-127">Weitere Informationen zu temporären, finden Sie unter [Informationen zum temporären Laufwerk in Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="7a8be-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="7a8be-128">Services anhalten</span><span class="sxs-lookup"><span data-stu-id="7a8be-128">Stop services</span></span>
<span data-ttu-id="7a8be-129">Verwenden den Remotedesktop, um sich mit allen Computern in der Umgebung zu verbinden und die folgenden Windows-Dienste zu beenden, indem Sie services.msc verwenden:</span><span class="sxs-lookup"><span data-stu-id="7a8be-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="7a8be-130">Per Internet WWW-Publishing-Dienst (für alle AOS-Computer)</span><span class="sxs-lookup"><span data-stu-id="7a8be-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="7a8be-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (nur nicht-private AOS-Computern)</span><span class="sxs-lookup"><span data-stu-id="7a8be-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="7a8be-132">Management Reporter 2012 Process Service (nur BI-Computer)</span><span class="sxs-lookup"><span data-stu-id="7a8be-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="7a8be-133">Diese Dienste haben offene Verbindungen zur Finance and Operations-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7a8be-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="7a8be-134">Zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="7a8be-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="7a8be-135">Suchen und laden Sie das letzte MinorVersionDataUpgrade.zip-Paket herunter</span><span class="sxs-lookup"><span data-stu-id="7a8be-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="7a8be-136">Suchen Sie das letzte MinorVersionDataUpgrade.zip-Paket mithilfe der Anweisungen in [Skript DataUpgrade.zip herunterladen](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package) herunter.</span><span class="sxs-lookup"><span data-stu-id="7a8be-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="7a8be-137">Die Anweisungen zeigen, wie Sie die korrekte Version des Datenaktualisierungspakets für Ihre Umgebung lokalisieren und herunterladen.</span><span class="sxs-lookup"><span data-stu-id="7a8be-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="7a8be-138">Eine Aktualisierung ist nicht erforderlich, um das MinorVersionDataUpgrade.zip-Paket herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="7a8be-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="7a8be-139">Sie müssen nur die Schritte des "Herunterladen zur Bereitstellung geeigneter Paket der letzten Aktualisierung abschließen" Bereich, ohne einen der Schritte im anderen Artikel, um eine Kopie des MinorVersionDataUpgrade.zip-Pakets abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7a8be-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="7a8be-140">Ausführen von Skripts für die Finance and Operations-Datenbank</span><span class="sxs-lookup"><span data-stu-id="7a8be-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="7a8be-141">Führen Sie die folgenden Skripts für die Finance and Operations-Datenbank aus (nicht für die Financial-Reporting-Datenbank).</span><span class="sxs-lookup"><span data-stu-id="7a8be-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="7a8be-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="7a8be-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="7a8be-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="7a8be-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="7a8be-144">Diese Skripts sicherstellen, dass die Benutzer, die Rollen und die Änderungsnachverfolgungseinstellungen korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="7a8be-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="7a8be-145">PowerShell-Befehle zum zurückzusetzen der Datenbank</span><span class="sxs-lookup"><span data-stu-id="7a8be-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="7a8be-146">Führen Sie den folgenden Befehl direkt auf dem AOS-Computer aus, um die Integration zwischen Finance and Operations und Financial Reporting zurückzusetzen:</span><span class="sxs-lookup"><span data-stu-id="7a8be-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="7a8be-147">Windows PowerShell als Administrator öffnen.</span><span class="sxs-lookup"><span data-stu-id="7a8be-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="7a8be-148">Ausführen: F:</span><span class="sxs-lookup"><span data-stu-id="7a8be-148">Execute: F:</span></span>
3.  <span data-ttu-id="7a8be-149">Ausführen: cd F:\\MRApplicationService\\MRInstallDirectory</span><span class="sxs-lookup"><span data-stu-id="7a8be-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="7a8be-150">Ausführen: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="7a8be-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="7a8be-151">Ausführen: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span><span class="sxs-lookup"><span data-stu-id="7a8be-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="7a8be-152">Sie werden gegebenenfalls aufgefordert, "Y" einzugeben, um zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="7a8be-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="7a8be-153">Erläuterung der Parameter:</span><span class="sxs-lookup"><span data-stu-id="7a8be-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="7a8be-154">Die gültigen Werte für -Reason sind: SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="7a8be-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="7a8be-155">Der -ReasonDetail-Parameter ist Freitext.</span><span class="sxs-lookup"><span data-stu-id="7a8be-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="7a8be-156">Der Grund und reasonDetail werden in der Telemetrie-/Umgebungsüberwachung erfasst.</span><span class="sxs-lookup"><span data-stu-id="7a8be-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="7a8be-157">Dienste starten</span><span class="sxs-lookup"><span data-stu-id="7a8be-157">Start services</span></span>
<span data-ttu-id="7a8be-158">Verwenden Sie services.msc, um die Services neu zu starten, die Sie eben beendeten:</span><span class="sxs-lookup"><span data-stu-id="7a8be-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="7a8be-159">Per Internet WWW-Publishing-Dienst (für alle AOS-Computer)</span><span class="sxs-lookup"><span data-stu-id="7a8be-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="7a8be-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (nur nicht-private AOS-Computern)</span><span class="sxs-lookup"><span data-stu-id="7a8be-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="7a8be-161">Management Reporter 2012 Process Service (nur BI-Computer)</span><span class="sxs-lookup"><span data-stu-id="7a8be-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="7a8be-162">Imporiteren von Berichtsdefinitionen</span><span class="sxs-lookup"><span data-stu-id="7a8be-162">Import report definitions</span></span>
<span data-ttu-id="7a8be-163">Importieren Sie die Berichtsdesigns im Berichts-Designer, und zwar mithilfe der Datei, die während des Exports erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="7a8be-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="7a8be-164">Wechseln Sie im Berichts-Designer zu **Unternehmen** &gt; **Bausteingruppen**.</span><span class="sxs-lookup"><span data-stu-id="7a8be-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="7a8be-165">Wählen Sie die Bausteingruppe aus, die exportiert werden soll, und klicken Sie **Export**.</span><span class="sxs-lookup"><span data-stu-id="7a8be-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="7a8be-166">Für Finance and Operations wird nur eine Bausteingruppe, unterstützt **Standard**.</span><span class="sxs-lookup"><span data-stu-id="7a8be-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="7a8be-167">Wählen Sie den **Standard**-Baustein und klicken Sie auf **Importieren**.</span><span class="sxs-lookup"><span data-stu-id="7a8be-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="7a8be-168">Wählen Sie die Datei aus, welche die exportierten Berichtsdefinitionen enthält und klicken Sie auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="7a8be-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="7a8be-169">Wählen Sie im Dialogfeld Importieren die Berichtsdefinitionen aus, die importiert werden soll:</span><span class="sxs-lookup"><span data-stu-id="7a8be-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="7a8be-170">Um alle Berichtsdefinitionen und die unterstützenden Bausteine zu importieren, klicken Sie auf **Alles auswählen**.</span><span class="sxs-lookup"><span data-stu-id="7a8be-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="7a8be-171">Um bestimmte Berichte, Zeilen, Spalten, Baumstrukturen oder Dimensionssätze zu importieren, wählen Sie die Berichte, Zeilen, Spalten, Baumstrukturen oder Dimensionssätze aus, die importiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7a8be-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="7a8be-172">Klicken Sie auf **Importieren**.</span><span class="sxs-lookup"><span data-stu-id="7a8be-172">Click **Import**.</span></span>





