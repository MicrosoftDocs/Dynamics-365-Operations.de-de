---
title: Regression Suite Automation Tool-Tutorial einrichten und installieren
description: Dieses Thema enthält ein Lernprogramm, das zeigt, wie das Regression Suite Automation Tool (RSAT) eingerichtet wird.
author: kfend
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 50450669387f4e2c9e81975d5345c525c7929c47
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180644"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="b515a-103">Regression Suite Automation Tool-Tutorial einrichten und installieren</span><span class="sxs-lookup"><span data-stu-id="b515a-103">Set up and install Regression suite automation tool tutorial</span></span>
<span data-ttu-id="b515a-104">Dieses Thema ist ein Tutorial, mit dem Sie RSAT sowie die Tools einrichten und verwenden können, die der Verwendung von RSAT zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b515a-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span> 

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b515a-105">Verwenden Sie das Internet-Browsertool, um die Seite in PDF-Format herunterzuladen und zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b515a-105">Use your internet browser tools to download and save this page in PDF format.</span></span> 

## <a name="key-concepts"></a><span data-ttu-id="b515a-106">Schlüsselkonzepte</span><span class="sxs-lookup"><span data-stu-id="b515a-106">Key concepts</span></span>

- <span data-ttu-id="b515a-107">Verstehen Sie die Installation und die vorausgesetzte Einrichtung, die für die verschiedenen Anwendungen erforderlich sind, die das Regression Suite Automation Tool (RSAT) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b515a-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="b515a-108">Verstehen Sie, wie die Aufgabenaufzeichnungsfunktion in Verbindung mit Microsoft Dynamics Lifecycle Services (LCS) und Microsoft Azure DevOps Sie Testfälle erstellen, konfigurieren, ausführen, untersuchen und melden lässt.</span><span class="sxs-lookup"><span data-stu-id="b515a-108">Understand how the Task recorder feature, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="b515a-109">Ermöglichen Sie es funktionalen Benutzern, mit der Aufgabenaufzeichnung Geschäftsaufgaben aufzuzeichnen, und die Aufgabenaufzeichnung in eine Suite automatisierter Tests zu konvertieren, ohne Quellcode zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="b515a-109">Empower functional users to record business tasks by using Task recorder, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="b515a-110">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="b515a-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="b515a-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="b515a-111">Prerequisites</span></span>

- <span data-ttu-id="b515a-112">Eine Umgebung, die Microsoft Dynamics 365 for Finance and Operations Version 10.0 (April 2019 ) oder höher ausführt ist für dieses Lernprogramm erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b515a-112">An environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="b515a-113">Für Kunden, die Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 verwenden, wird auch Plattform-Update 20 (PU20) oder später unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b515a-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="b515a-114">Der Benutzer muss über Administratorrechte für die Umgebung verfügen.</span><span class="sxs-lookup"><span data-stu-id="b515a-114">The user must have admin rights to the environment.</span></span>
- <span data-ttu-id="b515a-115">Sie müssen Zugriff auf den Debitorenmandant LCS und Azure DevOps (zuvor Microsoft Visual StudioTeam- Services\[VSTS\]) haben.</span><span class="sxs-lookup"><span data-stu-id="b515a-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="b515a-116">Der Benutzer, der Testsuites erstellt und verwaltet muss über eine Azure DevOps Test Plans oder Test Manager-Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="b515a-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="b515a-117">Die folgenden Lizenzen geben ebenfalls Zugriff auf Test Plans:</span><span class="sxs-lookup"><span data-stu-id="b515a-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="b515a-118">Visual Studio Enterprise Lizenz</span><span class="sxs-lookup"><span data-stu-id="b515a-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="b515a-119">Visual Studio Test Professional-Lizenz</span><span class="sxs-lookup"><span data-stu-id="b515a-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="b515a-120">MSDN Platforms-Abonnentenlizenz</span><span class="sxs-lookup"><span data-stu-id="b515a-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="b515a-121">RSAT muss Zugriff auf die Testumgebung über einen Webbrowser haben.</span><span class="sxs-lookup"><span data-stu-id="b515a-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="b515a-122">Um Testparameter zu generieren und zu bearbeiten muss Microsoft Excel installiert sein.</span><span class="sxs-lookup"><span data-stu-id="b515a-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="b515a-123">Azure DevOps konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b515a-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="b515a-124">Benutzerberechtigung</span><span class="sxs-lookup"><span data-stu-id="b515a-124">User eligibility</span></span>

<span data-ttu-id="b515a-125">Überprüfen Sie, ob der Benutzer in Azure DevOps erstellt ist und über eine Abonnementstufe verfügt, die Zugriff auf Azure Test Plans bietet.</span><span class="sxs-lookup"><span data-stu-id="b515a-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="b515a-126">Eine Azure DevOps Test Plan Lizenz ist nur erforderlich, wenn der Benutzer Testfälle erstellt und verwaltet (das heißt, nicht alle RSAT-Benutzer benötigen eine Lizenz).</span><span class="sxs-lookup"><span data-stu-id="b515a-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="b515a-127">Informationen zur Lizenzanforderungen finden Sie unter [Lizenzanforderungen](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span><span class="sxs-lookup"><span data-stu-id="b515a-127">For information about the license requirements, see [License requirements](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="b515a-128">Erstellen eines neuen Azure DevOps-Projekts</span><span class="sxs-lookup"><span data-stu-id="b515a-128">Create a new Azure DevOps project</span></span>
<span data-ttu-id="b515a-129">RSAT verwendet Azure Devops für Testfall- und Testsuiteverwaltungs, -berichterstellung und die Untersuchung von Testlaufergebnissen.</span><span class="sxs-lookup"><span data-stu-id="b515a-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span> 

> [!NOTE]
> <span data-ttu-id="b515a-130">Sie können ein vorhandenes Azure DevOps-Projekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="b515a-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="b515a-131">Wenn Ihr vorhandenes Azure DevOps-Projekt allerdings so eingerichtet ist, dass es über eine benutzerdefinierte Vorlage verfügt, erhalten Sie einen „VSTS-Synchronisierungsfehler“-Fehler, wenn Sie Testfälle vom Geschäftsprozessmodellierer (BPM) zu Azure DevOps synchronisieren (Informationen dazu finden Sie im Abschnitt [Testen der Synchronisierung von BPM zu Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).)</span><span class="sxs-lookup"><span data-stu-id="b515a-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="b515a-132">Wenn die folgenden bewährten Methoden für die benutzerdefinierte Vorlage befolgt wurden, können Sie die Testfälle zu Azure DevOps synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b515a-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="b515a-133">(Diese bewährten Methoden werden in der Fehlermeldung aufgeführt).</span><span class="sxs-lookup"><span data-stu-id="b515a-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="b515a-134">Löschen Sie keine Arbeitsaufgabentypen oder integrierten Felder.</span><span class="sxs-lookup"><span data-stu-id="b515a-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="b515a-135">Löschen Sie keinen Status eines Arbeitsaufgabentyps.</span><span class="sxs-lookup"><span data-stu-id="b515a-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="b515a-136">Fügen Sie keine erforderlichen Arbeitsaufgabentypen hinzu.</span><span class="sxs-lookup"><span data-stu-id="b515a-136">Do not add any required fields to a work item type.</span></span>

![Fehlermeldung mit einer Liste der bewährten Methoden](./media/setup_rsa_tool_02.png)

<span data-ttu-id="b515a-138">Andernfalls wird für dieses Lernprogramm empfohlen, dass Sie ein neues Azure DevOps-Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="b515a-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="b515a-139">Weitere Informationen finden Sie unter [Probleme bei der Synchronisierung zu BPM mithilfe einer benutzerdefinierten Azure DevOps (VSTS) Prozessvorlage](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span><span class="sxs-lookup"><span data-stu-id="b515a-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="b515a-140">Öffnen Sie die Azure DevOps-URL (`https://dev.azure.com/<Azure DevOps Name>`).</span><span class="sxs-lookup"><span data-stu-id="b515a-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="b515a-141">Wählen Sie in der rechten oberen Ecke der Azure DevOps-Seite **Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![Schalfläche „Projekt erstellen“](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="b515a-143">Füllen Sie die folgenden Felder aus, und wählen Sie dann **Erstellen** aus:</span><span class="sxs-lookup"><span data-stu-id="b515a-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="b515a-144">**Projektname**</span><span class="sxs-lookup"><span data-stu-id="b515a-144">**Project name**</span></span>
    - <span data-ttu-id="b515a-145">**Versionskontrolle** – Wählen Sie **Team Foundation-Versionskontrolle** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="b515a-146">Beachten Sie, dass die Standardoption **Git** nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b515a-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="b515a-147">**Arbeitsaufgabenprozess**</span><span class="sxs-lookup"><span data-stu-id="b515a-147">**Work item process**</span></span>

    ![Erstellen eines neuen Projektdialogfelds](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="b515a-149">Erstellen eines persönlichen Zugangstokens</span><span class="sxs-lookup"><span data-stu-id="b515a-149">Create a personal access token</span></span>

<span data-ttu-id="b515a-150">In diesem Lernprogramm verwenden Sie den LCS-Geschäftsprozessmodellierer (BPM), um eine Testfallbibliothek zu erstellen und Ihre Testfälle mit Azure DevOps zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b515a-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="b515a-151">Sie benötigen einen persönlichen Zugriffstoken, um BPM mit Azure DevOps zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b515a-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="b515a-152">Wählen Sie das Profilsymbol in der rechten oberen Ecke der Seite für Ihr Azure DevOps-Projekt aus, und wählen Sie dann **Sicherheit** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![Sicherheitsbefehl](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="b515a-154">Im linken Bereich unter **Sicherheit** wählen Sie **Persönliches Zugriffstoken** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="b515a-155">Wählen Sie dann **Neues Token** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-155">Then select **New Token**.</span></span>

    ![Scheinschaltfläche „Neues Token“ auf der Registerkarte „Persönliches Zugangstoken“ in den Benutzereinstellungen](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="b515a-157">Füllen Sie die folgenden Felder aus, und wählen Sie dann **Erstellen** aus:</span><span class="sxs-lookup"><span data-stu-id="b515a-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="b515a-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="b515a-158">**Name**</span></span>
    - <span data-ttu-id="b515a-159">**Ablauf (UTC)** – Wählen Sie **Benutzerdefiniert** aus und verwenden Sie dann die Datumsauswahl, um das letzte verfügbare Datum auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b515a-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="b515a-160">**Bereiche** – Wählen Sie die Option **Vollzugriff** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-160">**Scopes** – Select the **Full access** option.</span></span>

    ![Dialogfeld „Neues Zugriffstoken erstellen“](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="b515a-162">Notieren Sie das persönliche Zugriffstoken, das erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b515a-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="b515a-163">Sie benötigen es später, wenn Sie die RSAT-Konfiguration einrichten.</span><span class="sxs-lookup"><span data-stu-id="b515a-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![Persönliches Zugangstoken](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="b515a-165">Konfigurieren des LCS-Projekts</span><span class="sxs-lookup"><span data-stu-id="b515a-165">Configure the LCS project</span></span>

<span data-ttu-id="b515a-166">Sie benötigen ein Lifecycle Services (LCS)-Projekt für Ihre Mastertestbibliothek.</span><span class="sxs-lookup"><span data-stu-id="b515a-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="b515a-167">Der LCS-Geschäftsprozessmodellierer (BPM) wird als Master-Bibliothek für Ihre Testfälle verwendet.</span><span class="sxs-lookup"><span data-stu-id="b515a-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="b515a-168">BPM wird verwendet, um Testbibliotheken in LCS-Projekten zu verwalten und zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="b515a-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="b515a-169">Beispielsweise veröffentlicht ein Microsoft-Partner oder ein unabhängiger Softwareanbieter (ISV), der Testbibliotheken erstellt, Testfälle in Form von BPM-Bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="b515a-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="b515a-170">In BPM werden Testfälle nach Geschäftsprozess sortiert.</span><span class="sxs-lookup"><span data-stu-id="b515a-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="b515a-171">BPM definiert die Ausführungsreihenfolge der die Häufigkeit des Testerfolgs nicht.</span><span class="sxs-lookup"><span data-stu-id="b515a-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="b515a-172">Diese Details werden in Azure DevOps verwaltet, wie später in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b515a-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="b515a-173">Für das LCS-Projekt können Sie eine vorhandene Benutzerimplementierung oder ein Partnerprojekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="b515a-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="b515a-174">Aktualisieren der LCS-Sprache</span><span class="sxs-lookup"><span data-stu-id="b515a-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="b515a-175">Damit die Benutzeroberfläche (UI) die Geschäftsprozesse korrekt anzeigt, muss die bevorzugte Sprache von LCS auf **Englisch (USA)** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b515a-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="b515a-176">Gehen Sie zum LCS-Implementierungsprojekt.</span><span class="sxs-lookup"><span data-stu-id="b515a-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="b515a-177">Wählen Sie die Schaltfläche **Einstellungen** (das Rad-Symbol) in der rechten oberen Ecke der Seite aus, und wählen Sie dann **Spracheinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="b515a-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![Befehle im Einstellungsmenü](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="b515a-179">Im Feld **Bevorzugte Sprache** wählen Sie **Englisch (USA)** und **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![Registerkarte „Spracheneinstellung“ in den Benutzereinstellungen](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="b515a-181">Konfigurieren von LCS, um eine Verbindung mit dem Azure DevOps-Projekt herzustellen</span><span class="sxs-lookup"><span data-stu-id="b515a-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="b515a-182">Wenn Sie zuvor ein neues Azure DevOps-Projekt erstellt haben, konfigurieren Sie das LCS-Projekt, um eine Verbindung damit herzustellen.</span><span class="sxs-lookup"><span data-stu-id="b515a-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="b515a-183">Andernfalls wenn Ihr LCS-Projekt bereits mit Ihrem Azure DevOps-Projekt verbunden ist, können Sie mit dem nächsten Abschnitt fortfahren.</span><span class="sxs-lookup"><span data-stu-id="b515a-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="b515a-184">Gehen Sie zum LCS-Implementierungsprojekt.</span><span class="sxs-lookup"><span data-stu-id="b515a-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="b515a-185">Aktivieren Sie die Schaltfläche **Menü**, und wählen Sie dann **Projekteinstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![Befehl „Projekteinstellungen“](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="b515a-187">Wählen Sie im linken Bereich **Visual Studio Team Services** aus und wählen Sie dann **Einstellungen Visual Studio Team Services** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![Registerkarten Visual Studio-Projekteinstellungen in den Projekteinstellungen](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="b515a-189">Geben Sie im Feld **Azure DevOpsWebsite-URL** die URL der Azure DevOps-Website ein.</span><span class="sxs-lookup"><span data-stu-id="b515a-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="b515a-190">Wählen Sie im Feld **Persönliches Zugriffstoken** das persönliche Zugriffstoken aus, das zuvor erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b515a-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b515a-191">Obwohl VSTS nun als Azure DevOps bezeichnet wird, verwenden Sie die alte URL, um LCS mit Ihrem Azure DevOps-Projekt zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="b515a-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="b515a-192">Beispielsweise lautet die Azure DevOps-URL, die in diesem Lernprogramm verwendet wird `https://dev.azure.com/D365FOFastTrack/`.</span><span class="sxs-lookup"><span data-stu-id="b515a-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="b515a-193">In der folgenden Abbildung wird sie allerdings als `https://D365FOFastTrack.visualstudio.com/` eingegeben.</span><span class="sxs-lookup"><span data-stu-id="b515a-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![Schritt 1 in „Einrichten von Visual Studio Team Services“](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="b515a-195">Wählen Sie **Fortsetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-195">Select **Continue**.</span></span>
6. <span data-ttu-id="b515a-196">Wählen Sie im Feld **Visual Studio Team Services-Projekt** das VSTS-Projekt auf der ausgewählten Website aus, die mit dem LCS-Projekt verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="b515a-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="b515a-197">Das Feld**Vorlage verarbeiten** wird standardmäßig auf **Agile** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b515a-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="b515a-198">Für eine benutzerdefinierte Vorlage überprüfen Sie den Leitfaden zu bewährten Methoden im Abschnitt [Neues Azure DevOps-Projekt erstellen ](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="b515a-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="b515a-199">Wählen Sie dann **Fortsetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-199">Then select **Continue**.</span></span>

    ![Schritt 2 in „Einrichten von Visual Studio Team Services“](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="b515a-201">Überprüfen Sie die Einstellungen, und wählen Sie dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-201">Review your settings, and then select **Save**.</span></span>

    ![Schritt 3 in „Einrichten von Visual Studio Team Services“](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="b515a-203">Wählen Sie **Autorisieren** aus, um LCS zu autorisieren, um auf die konfigurierten Azure DevOps-Website in Ihrem Auftrag zuzugreifen und Funktionen zu aktivieren, die mit VSTS integrieren.</span><span class="sxs-lookup"><span data-stu-id="b515a-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![Schaltfläche „Autorisieren“](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="b515a-205">Ein Nachrichtenfeld mit folgender Meldung wird angezeigt: „Sie werden auf eine externe Website weitergeleitet, um LCS zu autorisieren, und in Ihrem Namen eine Verbindung mit Visual Studio-Team Services herzustellen.</span><span class="sxs-lookup"><span data-stu-id="b515a-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="b515a-206">Fortfahren?“</span><span class="sxs-lookup"><span data-stu-id="b515a-206">Proceed?"</span></span> <span data-ttu-id="b515a-207">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-207">Select **Yes**.</span></span>

    ![Meldungsfeld](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="b515a-209">Wählen Sie **Akzeptieren** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-209">Select **Accept**.</span></span>

    ![Autorisieren des Zugriffs](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="b515a-211">Wenn Sie als Benutzer berechtigt sind, sollte Sie die Benutzeroberfläche zur LCS-Projekteinstellungsseite zurückbringen.</span><span class="sxs-lookup"><span data-stu-id="b515a-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![Autorisierter Benutzer](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="b515a-213">Eine neue BPM-Bibliothek erstellen</span><span class="sxs-lookup"><span data-stu-id="b515a-213">Create a new BPM library</span></span>

1. <span data-ttu-id="b515a-214">Gehen Sie zum LCS-Implementierungsprojekt.</span><span class="sxs-lookup"><span data-stu-id="b515a-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="b515a-215">Aktivieren Sie die Schaltfläche **Menü**, und wählen Sie dann **Geschäftsprozessmodellierer** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![Befehl „Geschäftsprozessmodellierer“](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="b515a-217">Wählen Sie **Neue Bibliothek** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-217">Select **New library**.</span></span>

    ![Schaltfläche „Neue Bibliothek“](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="b515a-219">Geben Sie im Feld **Bibliotheksname** einen Namen ein, und wählen Sie dann **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="b515a-220">Nennen Sie die BPM-Bibliothek in diesem Lernprogramm **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="b515a-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![Dialogfeld „Neue Bibliothek erstellen“](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="b515a-222">Öffnen Sie die neue BPM-Bibliothek **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="b515a-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="b515a-223">Wählen Sie den Prozess **Beispielkerngeschäftsprozess** und dann auf der rechten Seite die Option **Bearbeitungsmodus** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![Schaltfläche „Bearbeitungsmodus“](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="b515a-225">Ändern Sie den Wert der beiden Felder **Name** und **Beschreibung** zu **Ein Produkt erstellen**.</span><span class="sxs-lookup"><span data-stu-id="b515a-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="b515a-226">Wählen Sie dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-226">Then select **Save**.</span></span>

    ![Die Felder „Name“ und „Beschreibung“](./media/setup_rsa_tool_24.png)

## <a name="environment"></a><span data-ttu-id="b515a-228">Umgebung</span><span class="sxs-lookup"><span data-stu-id="b515a-228">Environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="b515a-229">Versionsanforderung</span><span class="sxs-lookup"><span data-stu-id="b515a-229">Version requirement</span></span>

<span data-ttu-id="b515a-230">Eine Test- oder Sandboxumgebung, die Version 10 ausführt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b515a-230">A test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="b515a-231">Für Kunden, die Version 7.3 verwenden, wird auch Plattform-Update 20 oder später unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b515a-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="b515a-232">RSAT muss Zugriff auf Ihre Testumgebung über einen Webbrowser haben.</span><span class="sxs-lookup"><span data-stu-id="b515a-232">RSAT must have access to your test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="b515a-233">Benutzerkriterien</span><span class="sxs-lookup"><span data-stu-id="b515a-233">User criteria</span></span>

<span data-ttu-id="b515a-234">Der Benutzer muss über Administratorrechte für diese Umgebung verfügen.</span><span class="sxs-lookup"><span data-stu-id="b515a-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="b515a-235">Richten Sie Hilfeeinstellungen ein, um eine Verbindung mit LCS herzustellen</span><span class="sxs-lookup"><span data-stu-id="b515a-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="b515a-236">Dieser Schritt ist erforderlich, um eine Verbindung mit LCS herzustellen, damit die Aufgabenaufzeichnungen über den Client in der entsprechenden BPM-Bibliothek in LCS gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="b515a-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the client.</span></span>

1. <span data-ttu-id="b515a-237">Öffnen Sie den Client.</span><span class="sxs-lookup"><span data-stu-id="b515a-237">Open the client.</span></span>
2. <span data-ttu-id="b515a-238">Gehen Sie zu **Systemadministration \> Einrichten \> Systemparameter**.</span><span class="sxs-lookup"><span data-stu-id="b515a-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="b515a-239">Wählen Sie auf der Registerkarte **Hilfe** im Feld **Lifecycle Services-Hilfekonfiguration** das betreffende LCS-Projekt (**RSAT** für dieses Lernprogramm) aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![Feld „Lifecycle Services-Hilfekonfiguration“ auf der Registerkarte „Hilfe“](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="b515a-241">BPM-Bibliotheken werden im entsprechenden LCS-Projekt ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="b515a-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="b515a-242">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="b515a-242">Select **Save**.</span></span>
5. <span data-ttu-id="b515a-243">Möglicherweise müssen Sie den Browser aktualisieren, um den aktualisierten Hilfeinhalt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b515a-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![Benachrichtigung zum Aktualisieren des Browsers](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="b515a-245">Aufgabenaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="b515a-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="b515a-246">Stellen Sie sicher dass alle Aufgabenaufzeichnungen im Hauptdashboard starten.</span><span class="sxs-lookup"><span data-stu-id="b515a-246">Make sure that all your task recordings start on the main dashboard.</span></span> <span data-ttu-id="b515a-247">Halten Sie Einzelaufzeichnungen kurz und konzentrieren Sie sich auf eine Geschäftsaufgabe, wie die Erstellung eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="b515a-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="b515a-248">Eine Aufgabenaufzeichnung erstellen und in der BPM-Bibliothek speichern</span><span class="sxs-lookup"><span data-stu-id="b515a-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="b515a-249">Erstellen Sie eine entsprechende Aufgabenaufzeichnung, die Sie dem einfachen Geschäftsprozess anfügen können, der in der neuen BPM-Bibliothek erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b515a-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="b515a-250">Öffnen Sie den Client.</span><span class="sxs-lookup"><span data-stu-id="b515a-250">Open the client.</span></span>
2. <span data-ttu-id="b515a-251">Wählen Sie im Hauptdashboard die Schaltfläche **Einstellungen** (das Zahnradsymbol) aus, und wählen Sie dann **Aufgabenaufzeichnung** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![Befehle im Einstellungsmenü](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="b515a-253">Wählen Sie **Aufzeichnung erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-253">Select **Create recording**.</span></span>

    ![Schaltfläche „Aufzeichnung erstellen“](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="b515a-255">Füllen Sie die Felder **Aufzeichnungsname** und **Aufzeichnungsbeschreibung** aus, und wählen Sie dann **Starten** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![Felder „Aufzeichnungsname“ und „Aufzeichnungsbeschreibung“](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="b515a-257">Erfassen Sie die Schritte zum Erstellen eines Produkts.</span><span class="sxs-lookup"><span data-stu-id="b515a-257">Record the steps for creating a product.</span></span> <span data-ttu-id="b515a-258">Wenn Sie fertig sind, wählen Sie **Beenden** aus, um die Erfassung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="b515a-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![Schritte zum Erstellen eines Produkts](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="b515a-260">Wählen Sie **In Lifecycle Services speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-260">Select **Save to Lifecycle Services**.</span></span>

    ![Speicheroptionen](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="b515a-262">Bibliotheksinformationen werden aus LCS geladen.</span><span class="sxs-lookup"><span data-stu-id="b515a-262">Library information is loaded from LCS.</span></span>

    ![Fortschrittsanzeige](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="b515a-264">Wählen Sie die BPM-Bibliothek aus, die der Aufgabenaufzeichnung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b515a-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="b515a-265">In diesem Lernprogramm wählen Sie die **RSAT**-BPM-Bibliothek aus, die zuvor erstellt wurde, und den Geschäftsprozess **Ein Produkt erstellen** darunter.</span><span class="sxs-lookup"><span data-stu-id="b515a-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="b515a-266">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-266">Then select **OK**.</span></span>

    ![Die Aufgabenaufzeichnung einer BPM-Bibliothek und einem Geschäftsprozess zuordnen](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="b515a-268">Die Meldung „Das Speichern in Lifecycle Services war erfolgreich“ erscheint.</span><span class="sxs-lookup"><span data-stu-id="b515a-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![Meldung einer erfolgreichen Speicherung in LCS](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="b515a-270">Wenn Sie die Aufgabenaufzeichnung lokal speichern und dann durch LCS zu BPM hochladen möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="b515a-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="b515a-271">Nachdem die Aufzeichnung abgeschlossen ist, wählen Sie **Auf diesem PC speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![Speicheroptionen](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="b515a-273">In der Benachrichtigungsleiste des Browsers wählen Sie **Speichern** oder **Speichern unter** aus, um die Datei auf dem lokalen Computer zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b515a-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![Benachrichtigungsleiste](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="b515a-275">Wechseln Sie zur BPM-Bibliothek **RSAT**, und wählen Sie den Geschäftsprozess aus, für den die Aufgabenaufzeichnung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="b515a-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="b515a-276">Auf der Registerkarte **Überblick** wählen Sie **Hochladen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-276">On the **Overview** tab, select **Upload**.</span></span>

        ![Schaltfläche „Hochladen“](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="b515a-278">Wählen Sie **Durchsuchen** und dann die .axtr-Datei aus, die Sie zuvor gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="b515a-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="b515a-279">Wählen Sie dann **Hochladen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-279">Then select **Upload**.</span></span>

        ![Auswählen der .axtr-Datei zum Hochladen](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="b515a-281">Testen der Synchronisierung von BPM zu Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="b515a-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="b515a-282">Da jetzt eine Aufgabenaufzeichnung dem Geschäftsprozess zugeordnet ist, müssen Sie überprüfen, dass der Geschäftsprozess und die zugehörige Aufgabenaufzeichnung mithilfe der in VSTS-Synchronisierungsfunktion in LCS (je) mit Azure DevOps als eine Funktion und ein Testfall synchronisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b515a-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="b515a-283">Der entsprechende Arbeitsaufgabentyp, der in Azure DevOps erstellt wird, variiert abhängig von der Prozessvorlage, die Sie ausgewählt haben, als Sie das LCS-Projekt mit Azure DevOps konfiguriert haben, wie im Abschnitt [Erstellen eines neuen Azure DevOps-Projekt](#create-a-new-azure-devops-project) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b515a-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="b515a-284">Wechseln Sie zur BPM-Bibliothek und öffnen Sie die **RSAT**-Bibliothek, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b515a-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="b515a-285">Aktivieren Sie die Ellipsen-Schaltfläche (**…**), und wählen Sie **VSTS-Synchronisierung** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![Befehl „VSTS-Synchronisierung“ im Ellipsen-Menü](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="b515a-287">Nachdem die VSTS-Synchronisierung abgeschlossen ist, wird auf der linken Seite die Registerkarte **Anforderungen** angezeigt, die die entsprechende Azure DevOps-Arbeitsaufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="b515a-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b515a-288">Die Arbeitsaufgabe, die in Azure DevOps erstellt wird, weist den BPM-Bibliotheksnamen als Titelpräfix vor.</span><span class="sxs-lookup"><span data-stu-id="b515a-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![Registerkarte „Anforderungen“](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="b515a-290">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b515a-290">Refresh the page.</span></span>
4. <span data-ttu-id="b515a-291">Wählen Sie die Elipsen-Schaltfläche (**...**) aus. Es wird die Zusatzfunktion **Testfälle synchronisieren** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b515a-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="b515a-292">Wählen Sie diese Option aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-292">Select this option.</span></span>

    ![Befehl „Testfälle synchronisieren“ im Ellipsen-Menü](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="b515a-294">Wenn die Option **Testfälle synchronisieren** nicht verfügbar ist, nachdem Sie die Seite aktualisieren, wechseln zur Hauptseite für BPM, und wählen Sie **Testfälle synchronisieren** für die gesamte Bibliothek aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="b515a-295">Hierdurch erzwingen Sie eine Synchronisierung für die gesamte Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="b515a-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    > 
    > ![Auswählen der Synchronisierung von Testfällen für die gesamte Bibliothek](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="b515a-297">Nachdem die Synchronisierung der Testfälle abgeschlossen ist, wird auf der Registerkarte **Anforderungen** ein neuer Testfall erstellt.</span><span class="sxs-lookup"><span data-stu-id="b515a-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![Neuer Testfall auf der Registerkarte „Anforderungen“](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="b515a-299">Wechseln Sie zu Ihrem Azure DevOps-Projekt, und wählen Sie **Übersichten \> Arbeitsaufgaben** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![Befehl „Arbeitsaufgaben“ unter „Übersichten“](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="b515a-301">Überprüfen Sie, ob die Arbeitsaufgabe und der Testfall, die Sie durch BPM-Synchronisierung erstellt haben, vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b515a-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![Arbeitsaufgabe und Testfall](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="b515a-303">RSAT installieren und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b515a-303">Install and Configure RSAT</span></span>

<span data-ttu-id="b515a-304">RSAT kann auf einem beliebigen Computer installiert werden, der Windows 10 ausführt und der eine Verbindung mit der Umgebung über einen Webbrowser herstellen kann (Internet Explorer oder Google Chrome).</span><span class="sxs-lookup"><span data-stu-id="b515a-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="b515a-305">Bevor Sie eine neue Version des Tools installieren, wird empfohlen, dass Sie die vorherige Version deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="b515a-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="b515a-306">Installieren eines Authentifizierungszertifikats</span><span class="sxs-lookup"><span data-stu-id="b515a-306">Install an authentication certificate</span></span>

<span data-ttu-id="b515a-307">Um die Authentifizierung zu aktivieren, müssen Sie ein Zertifikat auf dem gleichen Computer generieren und installieren, auf dem RSAT ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b515a-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="b515a-308">Generieren eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="b515a-308">Generate a certificate</span></span>

1. <span data-ttu-id="b515a-309">Um eine Zertifikatsdatei zu generieren, öffnen Sie ein Microsoft Windows PowerShell-Fenster als Administrator, und führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="b515a-310">Öffnen Sie den Zertifikatsmanager, indem Sie **certlm.msc** in das Dialogfeld **Ausführen** eingeben und bestätigen, dass das **D365 Automated-Testzertifikats** unter **Persönlich \> Zertifikate** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b515a-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b515a-311">Stellen Sie sicher, dass Sie **certlm.msc** und nicht **certmgr.msc** eingeben, da die Zertifikate auf dem lokalen Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b515a-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![Zertifikat „D365 Automated-Testzertifikat“](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="b515a-313">Klicken Sie mit der rechten Maustaste auf das Zertifikat, und wählen Sie dann **Kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="b515a-314">Wechseln Sie zu **Vertrauenswürdige Stammzertifizierungsstellen \> Zertifikate**.</span><span class="sxs-lookup"><span data-stu-id="b515a-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![Zertifikatsordner unter dem Ordner „Vertrauenswürdige Stammzertifizierungsstellen“](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="b515a-316">Wählen Sie im Menü **Aktivität** **Einfügen** aus, um das Zertifikat in den Speicherort der **Vertrauenswürdigen Stammzertifizierungsstellen** zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="b515a-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![Befehl „Einfügen“ im Menü „Aktivität“](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="b515a-318">Um die Fingerabdruck des installierten Zertifikats zu erhalten, aber ohne Leerzeichen und Sonderzeichen, öffnen Sie ein Windows PowerShell-Fenster als Administrator und führen die folgenden Befehle aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="b515a-319">Speichern Sie den Fingerabdruck, da Sie ihn später benötigen, wenn Sie die .wif-Dateien für Application Object Server (AOS) aktualisieren und die RSAT-Konfiguration einrichten.</span><span class="sxs-lookup"><span data-stu-id="b515a-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="b515a-320">Konfigurieren des AOS-Computers, um der Verbindung zu vertrauen</span><span class="sxs-lookup"><span data-stu-id="b515a-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="b515a-321">Wenn die Umgebung eine Umgebung der Ebene 2+ ist, muss der Zertifikatsfingerabdruck in der wif.config-Datei für **alle** dAOS-Computer der Umgebung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b515a-321">If the environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="b515a-322">Stellen Sie eine Remote Desktop Protocol (RDP)-Verbindung mit dem AOS-Computer her.</span><span class="sxs-lookup"><span data-stu-id="b515a-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="b515a-323">Anmeldungsdetails sind auf der Umgebungsdetailseite in LCS verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b515a-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="b515a-324">Öffnen Sie Microsoft-Internetinformationsdienste (IIS) und navigieren Sie zu **AOSService** in der Website-Liste.</span><span class="sxs-lookup"><span data-stu-id="b515a-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![AOSService in der Website-Liste](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="b515a-326">Klicken Sie mit der rechten Maustaste auf **Erkunden**, um **\<Laufwerk\>: \\AosService\\Webroot**-Ordners zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b515a-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="b515a-327">Suchen Sie die Datei **wif.config**.</span><span class="sxs-lookup"><span data-stu-id="b515a-327">Find the **wif.config** file.</span></span>

    ![Wif.config-Datei im Webroot-Ordner](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="b515a-329">Aktualisieren Sie die Datei **wif.config**, indem Sie einen neuen Zertifikatseintrag für Ihr Zertifikat und den Behördennamen hinzufügen, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b515a-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="b515a-330">Wenn mehrere Benutzer dieselbe Anwendung verwenden, muss jeder Benutzer separate Fingerabdrücke generieren, und jeder dieser Fingerabdrücke muss dem Abschnitt **\<Schlüssel\>** hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b515a-330">If multiple users are using the same application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="b515a-331">Sind es mehrere AOS-Computer gibt, wiederholen Sie die Schritte 3 bis 4 für jeden weiteren Computer.</span><span class="sxs-lookup"><span data-stu-id="b515a-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b515a-332">Im Gegensatz zu älteren Umgebung der Ebene 2 werden neue Umgebung der Ebene 2 mit zwei AOS-Instanzen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b515a-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="b515a-333">Führen Sie **iisreset** für alle AOS-Computer aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b515a-334">Wenn Sie nicht über Administratorrechte verfügen, um **iisreset** auf einem Computer der Ebene 1 auszuführen, wählen Sie auf der Umgebungsdetailseite in LCS „Verwalten > Dienste neustarten“ aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="b515a-335">Ebene 2+-Umgebung</span><span class="sxs-lookup"><span data-stu-id="b515a-335">Tier 2+ environment</span></span>

<span data-ttu-id="b515a-336">Wenn eine Umgebung der Ebene 2+ (Standard-Akzeptanztestsandbox oder höher) verwendet wird, prüfen Sie die folgende Registrierungseinstellung auf dem Computer, auf dem RSAT eingerichtet ist, oder legen Sie die Einstellung dort fest.</span><span class="sxs-lookup"><span data-stu-id="b515a-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="b515a-337">Dieser Schritt ist erforderlich, da er Sie dabei unterstützt, Authentifizierungs- oder RSAT-Verbindungsfehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="b515a-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="b515a-338">Installieren von RSAT</span><span class="sxs-lookup"><span data-stu-id="b515a-338">Install RSAT</span></span>

1. <span data-ttu-id="b515a-339">Wechseln Sie zu <https://www.microsoft.com/download/details.aspx?id=57357> und wählen Sie **Download** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="b515a-340">Wählen Sie alle Dateien aus, und wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-340">Select all the files, and then select **Next**.</span></span>

    ![Auswählen aller Dateien](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="b515a-342">Doppelklicken Sie auf das .msi-Paket, um das Installationsprogramm auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b515a-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="b515a-343">Wenn die Installation abgeschlossen ist, wählen Sie **Fertig stellen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![RSAT-Installationsprogrammdatei](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="b515a-345">Einrichten von Selenium- und Browsertreibern</span><span class="sxs-lookup"><span data-stu-id="b515a-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="b515a-346">In den Vorgängerversionen von RSAT mussten Sie Selenium- und Browsertreiber einrichten.</span><span class="sxs-lookup"><span data-stu-id="b515a-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="b515a-347">Sie müssen dieses Treiber nicht mehr installieren, da sie automatisch installiert werden.</span><span class="sxs-lookup"><span data-stu-id="b515a-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="b515a-348">Beim erstmaligen Öffnen von RSAT werden Sie aufgefordert, Selenium automatisch herunterzuladen und zu installieren.</span><span class="sxs-lookup"><span data-stu-id="b515a-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="b515a-349">Weitere Informationen finden Sie im Abshnitt [RSAT konfigurieren](#configure-rsat).</span><span class="sxs-lookup"><span data-stu-id="b515a-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="b515a-350">Bevor Sie einen Testfall ausführen können, werden Sie aufgefordert, den Browsertreiber automatisch herunterzuladen und zu installieren, der dem Standardbrowser entspricht, der in der RSAT-Konfiguration aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b515a-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="b515a-351">Weitere Informationen finden Sie im Abschnitt [Testfälle laden und ausführen](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="b515a-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="b515a-352">Erste Schritte mit RSAT</span><span class="sxs-lookup"><span data-stu-id="b515a-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="b515a-353">Einen Testplan und Testsuiten erstellen</span><span class="sxs-lookup"><span data-stu-id="b515a-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="b515a-354">Wechseln Sie zum Azure DevOps-Projekt, und wählen Sie **Testpläne** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![Befehl „Testpläne“](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="b515a-356">Wählen Sie **Neuer Testplan** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-356">Select **New Test Plan**.</span></span>

    ![Schaltfläche „Neuer Testplan“](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="b515a-358">Füllen Sie das Feld **Name** aus, und wählen Sie dann **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="b515a-359">In diesem Lernprogramm geben Sie dem Testplan den Namen **RSAT-Testplan**.</span><span class="sxs-lookup"><span data-stu-id="b515a-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![Dialogfeld „Neuer Testplan“](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="b515a-361">Wählen Sie das Pluszeichen (**+**) aus, und wählen Sie dann **Statische Suite** aus, um eine statische Suite unterhalb des neuen Testplans zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b515a-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="b515a-362">Nennen Sie die neue Testsuite **T01 – Fertigung auf Lager**</span><span class="sxs-lookup"><span data-stu-id="b515a-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b515a-363">Sie können auch eine abfragebasierte Suite erstellen, wenn die neuen Testfälle von BPM automatisch in die RSAT-Testsuite gezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b515a-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![Erstellen einer statischen Suite](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="b515a-365">Anfügen von Testfällen an Testsuiten</span><span class="sxs-lookup"><span data-stu-id="b515a-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="b515a-366">Wählen Sie rechts **Vorhandenes Element hinzufügen** aus, um vorhandene Testfälle der Testsuite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b515a-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![Schaltfläche „Vorhandenes Element hinzufügen“](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="b515a-368">Auf der Seite **Testfälle der Suite hinzufügen** wählen Sie **Abfrage ausführen** aus, und dann wählen Sie den Testfall aus, der der Testsuite hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b515a-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="b515a-369">In diesem Lernprogramm wählen Sie den Testfall **Neues Produkt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="b515a-370">Wählen Sie dann in der unteren rechten Ecke der Seite **Testfälle hinzufügen** aus (diese Schaltfläche wird in der folgenden Abbildung nicht dargestellt).</span><span class="sxs-lookup"><span data-stu-id="b515a-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Schalfläche „Abfrage ausführen“](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="b515a-372">Der Testfall wird der Testsuite **T01-Fertigung auf Lager** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b515a-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![Testfall der Testsuite hinzugefügt](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="b515a-374">RSAT konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b515a-374">Configure RSAT</span></span>

1. <span data-ttu-id="b515a-375">RSAT öffnen</span><span class="sxs-lookup"><span data-stu-id="b515a-375">Open RSAT.</span></span>

    ![RSAT-Symbol](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="b515a-377">Andernfalls wird folgende Warnung angezeigt: „Regression Suite Automation Tool benötigt Selenium. Soll es jetzt automatisch heruntergeladen und installiert werden?“</span><span class="sxs-lookup"><span data-stu-id="b515a-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="b515a-378">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-378">Select **Yes**.</span></span>

    ![Warnmeldung](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="b515a-380">Wählen Sie die Schaltfläche **Einstellungen** (das Zahnradsymbol) in der oberen rechten Ecke aus, und füllen Sie dann im angezeigten Dialogfeld die folgenden Felder aus:</span><span class="sxs-lookup"><span data-stu-id="b515a-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="b515a-381">**Azure DevOps URL** – Geben Sie die URL Ihres Azure DevOps Projekts ein, wie `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span><span class="sxs-lookup"><span data-stu-id="b515a-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="b515a-382">**Zugriffstoken** – Geben Sie das Zugriffstoken ein, mit dem das Tool eine Verbindung mit Azure DevOps herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="b515a-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="b515a-383">Verwenden Sie das persönliche Zugriffstoken, Sie zuvor in diesem Lernprogramm erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b515a-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="b515a-384">Weitere Informationen finden Sie unter [Authentifizieren des Zugriffs mit persönlichen Zugriffstoken](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span><span class="sxs-lookup"><span data-stu-id="b515a-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="b515a-385">**Projektname** – Wählen Sie den Namen Ihres Azure DevOps-Projekts aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="b515a-386">**Testplan** – Wählen Sie den Azure DevOps-Testplan aus, der die Testfälle enthält.</span><span class="sxs-lookup"><span data-stu-id="b515a-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="b515a-387">Weitere Informationen finden Sie unter [Erstellen von Testplänen und Testsuiten](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span><span class="sxs-lookup"><span data-stu-id="b515a-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="b515a-388">Nachdem Sie einen Testplan ausgewählt haben, wählen Sie **Verbindung testen** aus, um die Verbindung mit Azure DevOps zu testen.</span><span class="sxs-lookup"><span data-stu-id="b515a-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="b515a-389">**Hostname** – Geben Sie den Hostnamen der Testumgebung ein, z. B. **\<myaos\>.cloudax.dynamics.com**</span><span class="sxs-lookup"><span data-stu-id="b515a-389">**Hostname** – Enter the host name of the test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="b515a-390">Schließen Sie kein **https://** oder **http://** Präfix ein.</span><span class="sxs-lookup"><span data-stu-id="b515a-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="b515a-391">**SOAP Hostname** – Geben Sie den SOAP-Hostnamen der Testumgebung ein.</span><span class="sxs-lookup"><span data-stu-id="b515a-391">**SOAP Hostname** – Enter the SOAP host name of the test environment.</span></span> <span data-ttu-id="b515a-392">Normalerweise entspricht der SOAP-Hostname dem Hostnamen, hat aber ein **soap**-Suffix.</span><span class="sxs-lookup"><span data-stu-id="b515a-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="b515a-393">Es folgt ein Beispiel: **\<myaos\>soap.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="b515a-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="b515a-394">Schließen Sie kein **https://** oder **http://** Präfix ein.</span><span class="sxs-lookup"><span data-stu-id="b515a-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b515a-395">Um den Hostnamen und den SOAP-Hostnamen zu finden, öffnen Sie den IIS-Manager, klicken Sie mit der rechten Maustaste auf **Websites \> AOSService**, und wählen Sie dann **Bindungen bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="b515a-396">Die Werte in der Spalte **Hostname** geben Ihnen den Hostnamen und den SOAP-Hostnamen (der SOAP-Hostname hat das Suffix **soap** in der URL).</span><span class="sxs-lookup"><span data-stu-id="b515a-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![Hostname und SOAP-Hostname in der Spalte „Hostname“](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="b515a-398">**Benutzername des Administrators** – Geben Sie die E-Mail-Adresse des Administratorbenutzers in der Testumgebung ein.</span><span class="sxs-lookup"><span data-stu-id="b515a-398">**Admin user name** – Enter the email address of an admin user in the test environment.</span></span>
    - <span data-ttu-id="b515a-399">**Fingerabdruck** – Geben Sie den Fingerabdruck für das Authentifizierungszertifikat ein, wie zuvor in diesem Lernprogramm beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b515a-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="b515a-400">**Arbeitsverzeichnis** – Geben Sie den Speicherort des Ordners zum Speichern von Testautomatisierungsdateien wie Excel-Testdatendateien ein.</span><span class="sxs-lookup"><span data-stu-id="b515a-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="b515a-401">Geben Sie beispielsweise **C:\\Temp\\RegressionTool** ein oder wählen Sie den Pfad aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b515a-402">Wenn der Name des Ordners Leerzeichen hat, schlägt die Ausführung fehl, da der Ordner nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="b515a-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="b515a-403">Dieses Problem ist bekannt und sollte in der neuesten Version des Tools korrigiert werden.</span><span class="sxs-lookup"><span data-stu-id="b515a-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="b515a-404">**Standardbrowser** – Wählen Sie entweder **Internet Explorer** oder **Google Chrome** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="b515a-405">Stellen Sie sicher, dass die entsprechenden Browsertreiber eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="b515a-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="b515a-406">**Testlauf-Timeout** – Geben Sie den Timeout-Zeitraum für Testläufe in Minuten an.</span><span class="sxs-lookup"><span data-stu-id="b515a-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="b515a-407">Wenn der Timeout-Zeitraum vergeht, werden alle aktiven Fenster geschlossen und ausstehende Testfälle schlagen fehl.</span><span class="sxs-lookup"><span data-stu-id="b515a-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="b515a-408">**Testaktion-Timeout** – Dieses Feld steuert den Timeout-Zeitraum für Serveranforderungen der Finance and Operation-Umgebung in Minuten.</span><span class="sxs-lookup"><span data-stu-id="b515a-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="b515a-409">Normalerweise sollte der Standardwert (2 Minuten) ausreichen.</span><span class="sxs-lookup"><span data-stu-id="b515a-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="b515a-410">Bei langsameren Umgebungen können Sie den Wert ggf. erhöhen wollen, falls Fehler in Zusammenhang mit Timeouts auftreten.</span><span class="sxs-lookup"><span data-stu-id="b515a-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="b515a-411">**Unternehmensname** – Geben Sie den Unternehmensnamen zur Verwendung als Standardunternehmen ein, wenn Excel-Parameterdateien erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b515a-411">**Company name** – Enter the company name to use as your default company when Excel parameter files are created.</span></span> <span data-ttu-id="b515a-412">Sie können das Unternehmen später ändern, indem Sie die Excel-Parameterdatei bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b515a-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![Dialogfeld „Einstellungen“](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="b515a-414">Wählen Sie **Übernehmen** aus, um die Einstellungen anzuwenden und zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b515a-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="b515a-415">Um Ihre aktuellen Einstellungen in einer Konfigurationsdatei auf dem Computer zu speichern, wählen Sie **Speichern unter** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="b515a-416">Um Ihre aktuellen Einstellungen aus einer Konfigurationsdatei auf dem Computer wiederherzustellen, wählen Sie **Öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="b515a-417">Klicken Sie auf **Schließen**, um die Dialogfelder zu schließen.</span><span class="sxs-lookup"><span data-stu-id="b515a-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="b515a-418">Laden und Ausführen von Testfällen</span><span class="sxs-lookup"><span data-stu-id="b515a-418">Load and run test cases</span></span>

1. <span data-ttu-id="b515a-419">Wählen Sie **Laden** aus, um den Testplan **RSAT-Testplan** aus dem Azure DevOps-Projekt zu laden.</span><span class="sxs-lookup"><span data-stu-id="b515a-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![Schaltfläche „Laden“](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="b515a-421">Wählen Sie den Testfall **Neues Produkt erstellen** aus der Testsuite aus, und wählen Sie dann **Neu \>Testausführung und Parameterdateien generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![Befehl „Testausführung und Parameterdateien generieren“ im Menü „Neu“](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="b515a-423">Die Excel-Parameterdatei wird im lokalen Ordner erstellt, den Sie in der RSAT-Konfiguration angegeben haben (z. B. **C:\\Temp \\RegressionTool**).</span><span class="sxs-lookup"><span data-stu-id="b515a-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![Excel-Parameterdatei erstellt](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="b515a-425">Wenn Sie die Parameterdateien speichern möchten, wählen Sie **Hochladen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="b515a-426">Testautomatisierungsdateien aller ausgewählten Testfälle werden für künftige Verwendung in Azure DevOps hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="b515a-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="b515a-427">(Diese Dateien enthalten Excel-Testparameterdateien.)</span><span class="sxs-lookup"><span data-stu-id="b515a-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="b515a-428">Auf diese Weise können Sie **Laden** auswählen, um die Parameterdateien (und die Automatisierungsdateien) aus dem Testfall direkt aus Azure DevOps zu laden.</span><span class="sxs-lookup"><span data-stu-id="b515a-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="b515a-429">Sie müssen die Parameterdateien nicht erneut generieren.</span><span class="sxs-lookup"><span data-stu-id="b515a-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="b515a-430">Dieser Ansatz wird später wichtig, wenn Sie die Änderungen in der Parameterdatei beibehalten möchten und diese nicht überschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b515a-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="b515a-431">Um sicherzustellen, dass die Automatisierungsdateien und die Parameterdateien in Azure DevOps gespeichert werden, wechseln Sie zum Azure DevOps- Projekt, wählen Sie **Üersichten \> Arbeitsaufgaben** aus und wählen Sie den Testfall **Neues Produkt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="b515a-432">Auf der Registerkarte **Anhänge** können Sie vier Dateien sehen:</span><span class="sxs-lookup"><span data-stu-id="b515a-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="b515a-433">**.cs** – C-\#-Automatisierungsdatei</span><span class="sxs-lookup"><span data-stu-id="b515a-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="b515a-434">**.dll** – als Assembly kompilierte Automatisierungsdatei</span><span class="sxs-lookup"><span data-stu-id="b515a-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="b515a-435">**.xlsx** – Excel-Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="b515a-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="b515a-436">**.xml** – Aufzeichnungsdatei</span><span class="sxs-lookup"><span data-stu-id="b515a-436">**.xml** – Recording file</span></span>

    ![Dateien auf der Registerkarte „Anhänge“](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="b515a-438">Wählen Sie den Testfall aus, der ausgeführt werden soll, und wählen Sie dann **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b515a-439">Bevor Sie Testfälle ausführen, wenn Sie Internet Explorer als Browser verwenden, stellen Sie sicher, dass die Desktop-Auflösung unter **Windows-Anzeigeeinstellungen \> Maßstab und Layout** auf **100 %** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b515a-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="b515a-440">Wenn Sie diese Einstellungen auf einem virtuellen Computer (VM) nicht ändern können, ändern Sie ihn auf dem Client (Laptop), von dem Sie auf die WM zuzugreifen versuchen.</span><span class="sxs-lookup"><span data-stu-id="b515a-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="b515a-441">Die Auflösungseinstellungen werden dann von den VM-Anzeigeeinstellungen geerbt.</span><span class="sxs-lookup"><span data-stu-id="b515a-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![Desktopauflösung auf 100 % eingestellt](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="b515a-443">Wenn die Browsertreiber nicht im System installiert sind, erhalten Sie folgende Warnmeldung: „Dieser Vorgang erfordert den Treiber \<Browsername\>.</span><span class="sxs-lookup"><span data-stu-id="b515a-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="b515a-444">Möchten Sie ihn jetzt automatisch herunterladen und installieren?“</span><span class="sxs-lookup"><span data-stu-id="b515a-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="b515a-445">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-445">Select **Yes**.</span></span>

    ![Warnmeldung für Internet Explorer](./media/setup_rsa_tool_69.png)

    ![Warnmeldung für Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="b515a-448">Wenn Sie Chrome als Browser verwenden und eine Fehlermeldung erhalten, die angibt, dass die Sitzung nicht erstellt wurde, da die Chrome-Version falsch ist, laden Sie den letzten Chrome-Treiber von <http://chromedriver.chromium.org/downloads> in den Ordner **C:\\Programme (x86)\\Regression Suite Automation Tool\\Allgemein\\Extern\\ Selenium** herunter.</span><span class="sxs-lookup"><span data-stu-id="b515a-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Fehlermeldung für Chrome](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="b515a-450">Der Testfall wird ausgeführt und das Feld **Ergebnis** wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b515a-450">The test case is run, and the **Result** field is updated.</span></span>

    ![Fortschrittsanzeige](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="b515a-452">Wenn Sie diesem Lernprogramm folgen, schlägt der **Neues Produkt erstellen**-Testfall fehlt, da die Aufgabenaufzeichnung für das Erstellen eines Produkts den Produktname als hartcodierten Wert gespeichert hat.</span><span class="sxs-lookup"><span data-stu-id="b515a-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="b515a-453">Wenn Sie den gleichen Testfall wiederholen, sollten Sie eine Fehlermeldung erhalten, da das Produkt bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b515a-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![Auf „Fehlgeschlagen“ festgelegtes Ergebnisfeld](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="b515a-455">Anzeigen des Testergebnisses</span><span class="sxs-lookup"><span data-stu-id="b515a-455">View the test results</span></span>

1. <span data-ttu-id="b515a-456">Doppelklicken Sie auf den fehlgeschlagenen Testfall.</span><span class="sxs-lookup"><span data-stu-id="b515a-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="b515a-457">Es wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b515a-457">You receive an error message.</span></span>

    ![Fehlermeldung](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="b515a-459">Wählen Sie **Detail**, um die gesamten Fehlermeldung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b515a-459">Select **Details** to view the whole error message.</span></span>

    ![Die ganze Fehlermeldung](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="b515a-461">Um eine ausführliche Version eine Fehlermeldung in Azure DevOps anzuzeigen, wählen Sie **In Azure DevOps öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="b515a-462">In Azure DevOps können Sie den Status des Testfalls und die detaillierte Fehlermeldung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b515a-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Detaillierte Fehlermeldung in Azure DevOps](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="b515a-464">Um die Testergebnisse direkt im Azure DevOps-Projekt anzuzeigen, navigieren Sie zu **Testpläne \> Testpläne \> Ausführungen**.</span><span class="sxs-lookup"><span data-stu-id="b515a-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="b515a-465">Doppelklicken Sie auf den Test, für den weitere Details angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b515a-465">Double-click the test run that you want to see more details for.</span></span>

    ![Liste der Testläufe in Azure DevOps](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="b515a-467">Die Registerkarte **Ausführungszusammenfassung** gibt an, dass der Testfall fehlgeschlagen ist, aber die tatsächliche Fehlermeldung wird nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b515a-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="b515a-468">Um die detaillierten Fehlermeldung anzuzeigen, wählen Sie die Registerkarte **Testergebnisse** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![Registerkarte „Ausführungszusammenfassung“](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="b515a-470">Die Registerkarte **Testergebnisse** enthält die Testfallinformationen, zusammen mit dem Ergebnis und die Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="b515a-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![Registerkarte „Testergebnis“](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="b515a-472">Doppelklicken Sie auf den entsprechenden Datensatz, um die detaillierte Fehlermeldung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b515a-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![Detaillierter Fehlermeldung](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="b515a-474">Alle Fehlermeldungen sind auch lokal in **C:\\Benutzer\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b515a-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="b515a-475">Sie können die Testlaufergebnisse auch von der Testplanebene exportieren, indem Sie **Exportieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="b515a-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![Exportieren eines Testplans](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="b515a-477">Ändern Sie die Excel-Parameterdatei.</span><span class="sxs-lookup"><span data-stu-id="b515a-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="b515a-478">RSAT öffnen</span><span class="sxs-lookup"><span data-stu-id="b515a-478">Open RSAT.</span></span>
2. <span data-ttu-id="b515a-479">Wählen Sie den Testfall aus, und wählen Sie dann **Bearbeiten** aus, um die Excel-Parameterdatei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b515a-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="b515a-480">Beachten Sie auf dem **EcoResProductCreate**-Arbeitsblatt, dass der Wert des Feldes **Produktnummer** fest hartcodiert ist.</span><span class="sxs-lookup"><span data-stu-id="b515a-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="b515a-481">Sie müssen dieses Feld auf eine neue Produktnummer aktualisieren, bevor Sie den Testfall erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="b515a-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="b515a-482">Um eine eindeutige Produktnummer für jeden Lauf zu generieren, ohne die Excel-Parameterdatei jedes Mal erneut zu öffnen und die Produktnummer manuell zu aktualisieren, verwenden Sie die folgende Excel-Formel.</span><span class="sxs-lookup"><span data-stu-id="b515a-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="b515a-483">Zusätzlich zur Registerkarte **Allgemein** enthält die Excel-Parameterdatei eine Datenregisterkarte für jede Formularseite, die der Testfall besucht.</span><span class="sxs-lookup"><span data-stu-id="b515a-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every form page the test case visits.</span></span>

    ![Produktnummernfeld](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="b515a-485">Wählen Sie **Speichern** aus und schließen die Excel-Arbeitsmappe.</span><span class="sxs-lookup"><span data-stu-id="b515a-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="b515a-486">Wählen Sie **Hochladen** aus, um die Excel-Parameterdatei in Azure DevOps zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b515a-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![Meldung für erfolgreichen Upload](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="b515a-488">Um Testfälle in einem bestimmten Benutzerkontext auszuführen, geben Sie die E-Mail-Kennung des Benutzers im Feld **Testbenutzer** auf der Registerkarte **Allgemein** der Excel-Parameterdatei ein.</span><span class="sxs-lookup"><span data-stu-id="b515a-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="b515a-489">In der neuesten Version von RSAT wurde das Layout der Felder in der Excel-Parameterdatei aktualisiert, das Konzept bleibt jedoch gleich.</span><span class="sxs-lookup"><span data-stu-id="b515a-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![Feld „Testbenutzer“](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="b515a-491">Das Ergebnis validieren</span><span class="sxs-lookup"><span data-stu-id="b515a-491">Validate the results</span></span>

- <span data-ttu-id="b515a-492">Wählen Sie **Ausführen** aus, um den Testfall erneut auszuführen, und überprüfen Sie, ob der Testfall erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b515a-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="b515a-493">Sie können die Testergebnisse wie im Abschnitt [Anzeigen der Testergebnisse](#view-the-test-results) beschrieben anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b515a-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![Auf „Erfolgreich“ festgelegtes Ergebnisfeld](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="b515a-495">Verketten von Testfällen</span><span class="sxs-lookup"><span data-stu-id="b515a-495">Chaining of test cases</span></span>

<span data-ttu-id="b515a-496">Eine wichtige Funktion von RSAT ist das Verketten von Testfällen (das heißt, die Fähigkeit eines Tests, Werte an andere Tests zu übergeben).</span><span class="sxs-lookup"><span data-stu-id="b515a-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="b515a-497">Testfälle werden entsprechend ihrer im Azure DevOps Testplan definierten Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b515a-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="b515a-498">(Diese Reihenfolge kann im Testtool auch aktualisiert werden.) Wenn Sie also Variablen von einem Testfall an den anderen übergeben möchten, ist es sehr wichtig, dass die Tests in der richtigen Reihenfolge sind.</span><span class="sxs-lookup"><span data-stu-id="b515a-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="b515a-499">In diesem Abschnitt erstellen Sie eine gespeicherte Variable im ersten Testfall. Sie erstellen einen zweiten Testfall und übergeben die gespeicherte Variable vom ersten Testfall an den zweiten Testfall.</span><span class="sxs-lookup"><span data-stu-id="b515a-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="b515a-500">Sie führen die Testfälle dann als verketteten Testfall in RSAT aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="b515a-501">Ändern einer vorhandenen Aufgabenaufzeichnung, um eine gespeicherte Variablen zu erstellen</span><span class="sxs-lookup"><span data-stu-id="b515a-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="b515a-502">Öffnen Sie den Client.</span><span class="sxs-lookup"><span data-stu-id="b515a-502">Open the client.</span></span>
2. <span data-ttu-id="b515a-503">Wählen Sie die Schaltfläche **Einstellungen** (das Zahnradsymbol) aus, und wählen Sie dann **Aufgabenaufzeichnung** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="b515a-504">Wählen Sie **Aufzeichnung bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-504">Select **Edit Recording**.</span></span>

    ![Schalfläche „Aufzeichnung bearbeiten“](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="b515a-506">Wählen Sie **In Lifecycle Services öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-506">Select **Open from Lifecycle Services**.</span></span>

    ![Schalfläche „In Lifecycle Services öffnen“](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="b515a-508">Wählen Sie **Lifecycle Services-Bibliothek auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-508">Select **Select the Lifecycle Services library**.</span></span>

    ![Schaltfläche „Lifecycle Services-Bibliothek auswählen“](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="b515a-510">BPM-Bibliotheken werden aus LCS geladen.</span><span class="sxs-lookup"><span data-stu-id="b515a-510">BPM libraries are loaded from LCS.</span></span>

    ![Fortschrittsanzeige](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="b515a-512">Nachdem die BPM-Bibliotheken aus LCS geladen wurden, wählen Sie die BPM-Bibliothek **RSAT** und den Geschäftsprozess **Neues Produkt erstellen** aus, dem die Aufgabenaufzeichnung zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="b515a-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="b515a-513">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-513">Then select **OK**.</span></span>

    ![Auswählen einer BPM-Bibliothek und eines Geschäftsprozesses](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="b515a-515">Der Name der entsprechenden Aufgabenaufzeichnung wird im Feld **Aufzeichnungsname** eingegeben.</span><span class="sxs-lookup"><span data-stu-id="b515a-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="b515a-516">Wählen Sie **Starten** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-516">Select **Start**.</span></span>

    ![Name der Aufgabenaufzeichnung im Feld „Aufzeichnungsname“](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="b515a-518">Navigieren Sie zu **Produktinformationsverwaltung \> Produkte**, und wählen Sie **Neu** aus, um die Seite zu öffnen, in der die ursprüngliche Aufgabenaufzeichnung **Ein Produkt erstellen** aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="b515a-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="b515a-519">Wählen Sie **Schritt einfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b515a-520">Der neue Schritt wird **nach** dem Schritt eingefügtes, den Sie im Bereich ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="b515a-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![Schaltfläche „Schritt einfügen“](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="b515a-522">Klicken Sie mit der rechten Maustaste auf das Feld **Produktnummer**, und wählen Sie dann **Aufgabenaufzeichnung \> Kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![Kopieren-Befehl](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="b515a-524">Ein neuer Schritt wird dem Bereich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b515a-524">A new step is added in the pane.</span></span> <span data-ttu-id="b515a-525">Notieren Sie sich den Wert im Feld **Produktnummer**, da Sie ihn zu einem späteren Zeitpunkt benötigen.</span><span class="sxs-lookup"><span data-stu-id="b515a-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![Neuer Schritt hinzugefügt](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="b515a-527">Wählen Sie **Bearbeitung beendet** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="b515a-528">Wählen Sie **In Lifecycle Services speichern** aus, und ordnen Sie die neue Aufgabenaufzeichnung der gleichen BPM-Bibliothek und demselben Geschäftsprozess zu, der die ursprüngliche Aufgabenaufzeichnung zugeordnet war.</span><span class="sxs-lookup"><span data-stu-id="b515a-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="b515a-529">Weitere Informationen finden Sie im Abschnitt [Erstellen einer Aufgabenaufzeichnung und Speichern in der BPM-Bibliothek](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="b515a-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="b515a-530">Navigieren Sie zur BPM-Bibliothek, und wählen Sie **Testfälle synchronisieren** aus, um die Aufgabenaufzeichnung zu überschreiben, die dem Testfall in Azure DevOps zugeordnet ist, wie im Abschnitt [Testen der Synchronisierung von BPM zu Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b515a-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="b515a-531">Öffnen Sie RSAT und wählen Sie **Laden** aus, um alle Testfälle in der Testsuite erneut zu laden.</span><span class="sxs-lookup"><span data-stu-id="b515a-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="b515a-532">Sie müssen die Automatisierung und die Parameterdateien für den entsprechenden Testfall erneut generieren, indem Sie den Testfall auswählen und dann **Neu \> Test-Ausführung und Parameterdateien generieren** auswählen, wie im Abschnitt [Laden und Ausführen von Testfällen](#load-and-run-test-cases) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b515a-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b515a-533">Wenn die Excel-Parameterdatei offen gelassen wurde, schlägt die Regeneration fehl.</span><span class="sxs-lookup"><span data-stu-id="b515a-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="b515a-534">Daher sollten Sie sicherstellen, dass die Excel-Parameterdatei für den Testfall geschlossen ist, bevor Sie die neue Excel-Parameterdatei generieren.</span><span class="sxs-lookup"><span data-stu-id="b515a-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="b515a-535">Wählen Sie **Bearbeiten** aus, um die neue Excel-Parameterdatei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b515a-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="b515a-536">Sie finden einen neuen **Gespeicherte Variable**-Eintrag in Zeile 9.</span><span class="sxs-lookup"><span data-stu-id="b515a-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="b515a-537">Diese Variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** wird in der XML-Datei der Aufgabenaufzeichnung gespeichert und kann in folgenden Tests verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b515a-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![Eintrag der gespeicherten Variable](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="b515a-539">Neuen Testfall erstellen</span><span class="sxs-lookup"><span data-stu-id="b515a-539">Create a new test case</span></span>

1. <span data-ttu-id="b515a-540">Navigieren Sie zur **RSAT**-BPM-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b515a-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="b515a-541">Wählen Sie den Prozess **Beispiel-Support-Geschäftsprozess** und dann auf der rechten Seite die Option **Bearbeitungsmodus** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="b515a-542">Ändern Sie den Wert der beiden Felder **Name** und **Beschreibung** zu **Ein Produkt veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="b515a-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="b515a-543">Wählen Sie dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-543">Then select **Save**.</span></span>

    ![Name und Beschreibung geändert, um ein Produkt zu veröffentlichen](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="b515a-545">Erstellen einer neuen Aufgabenaufzeichnung, die eine Validierungsfunktion hat</span><span class="sxs-lookup"><span data-stu-id="b515a-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="b515a-546">Erstellen Sie einer Aufgabenaufzeichnung, um das Produkt zu veröffentlichen, das zuvor in der juristische USRT-Person erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b515a-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="b515a-547">Weitere Informationen finden Sie im Abschnitt [Erstellen einer Aufgabenaufzeichnung und Speichern in der BPM-Bibliothek](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="b515a-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b515a-548">Für verkettete Testfälle wird immer empfohlen, dass Sie den erforderlichen Datensatz suchen oder danach filtern, indem Sie *den Wert des Felds manuell eingeben*.</span><span class="sxs-lookup"><span data-stu-id="b515a-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="b515a-549">Auf diese Weise kann das Tool den Datensatz bestimmen, für den die Aktion im folgenden Testfall ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="b515a-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![Neue Aufgabenaufzeichnung, die eine Validierungsfunktion hat](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="b515a-551">Für die vorherige Darstellung zeigt, validieren Sie den Wert des Felds **Produktnummer** nachdem das Produkt mit dem Schnellfilter gefunden wurde, aber bevor Sie **Produkte veröffentlichen** auswählen, um sicherzustellen, dass es sich bei der Produktkennung um die von zuvor handelt.</span><span class="sxs-lookup"><span data-stu-id="b515a-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="b515a-552">Um den Wert zu überprüfen, klicken Sie mit der rechten Maustaste auf das Feld **Produktnummer**, und wählen Sie dann **Aufgabenaufzeichnung \> Überprüfen \> Aktueller Wert** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![Validieren des aktuellen Werts](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="b515a-554">Aufgabenaufzeichnung in BPM speichern</span><span class="sxs-lookup"><span data-stu-id="b515a-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="b515a-555">Nachdem die Aufgabenaufzeichnung abgeschlossen ist, wählen Sie **Lifecycle Services** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![Speicheroptionen](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="b515a-557">Bibliotheksinformationen werden aus LCS geladen.</span><span class="sxs-lookup"><span data-stu-id="b515a-557">Library information is loaded from LCS.</span></span>

    ![Fortschrittsanzeige](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="b515a-559">Wählen Sie die BPM-Bibliothek aus, die der Aufgabenaufzeichnung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b515a-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="b515a-560">In diesem Lernprogramm wählen Sie die **RSAT**-BPM-Bibliothek aus, die zuvor erstellt wurde, und den Geschäftsprozess **Ein Produkt veröffentlichen** darunter.</span><span class="sxs-lookup"><span data-stu-id="b515a-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="b515a-561">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="b515a-562">BPM mit Azure DevOps synchronisieren</span><span class="sxs-lookup"><span data-stu-id="b515a-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="b515a-563">Navigieren Sie zur BPM-Bibliothek, und öffnen Sie die Bibliothek **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="b515a-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="b515a-564">Wählen Sie **VSTS-Synchronisierung** und anschließend **Testfälle synchronisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="b515a-565">Weitere Informationen finden Sie im Abschnitt [Testen der Synchronisierung von BPM mit Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="b515a-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="b515a-566">Nach Abschluss der Synchronisierung wird die neue Arbeitsaufgabe und der entsprechende Testfall für den Geschäftsprozess **Ein Produkt veröffentlichen** in Azure DevOps unter **Karten \> Arbeitsaufgaben** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b515a-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="b515a-567">Den neuen Testfall der vorhandenen Testsuite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="b515a-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="b515a-568">Navigieren Sie zu **Testpläne \> Testpläne** und wählen Sie den Plan **RSAT-Testplan** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="b515a-569">Wählen Sie **Vorhandene Elemente auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="b515a-570">Wählen Sie auf der Seite **Testfällen der Suite hinzufügen** **Abfrage ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="b515a-571">Wählen Sie den neuen Testfall aus, der für **Produkt veröffentlichen** erstellt wurde, und wählen Sie dann **Testfälle hinzufügen** in der unteren rechten Ecke der Seite aus (diese Schaltfläche wird in der folgenden Abbildung nicht dargestellt).</span><span class="sxs-lookup"><span data-stu-id="b515a-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Seite „Testfällen der Suite hinzufügen“](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="b515a-573">Die Testsuite besitzt nun zwei Testfälle.</span><span class="sxs-lookup"><span data-stu-id="b515a-573">The test suite now has two test cases.</span></span>

    ![Zwei Testfälle in der Testsuite.](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="b515a-575">Testfälle in RSAT laden</span><span class="sxs-lookup"><span data-stu-id="b515a-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="b515a-576">Öffnen Sie RSAT und wählen Sie **Laden** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="b515a-577">Die Testfälle werden geladen und Sie erhalten folgende Warnung „Diese Aktivität überschreibt Excel-Testdatendateien, lokale Änderungen gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="b515a-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="b515a-578">Möchten Sie den Vorgang fortsetzen?“</span><span class="sxs-lookup"><span data-stu-id="b515a-578">Do you want to proceed?"</span></span> <span data-ttu-id="b515a-579">Wählen Sie **Ja**, um die Excel-Parameterdateien im lokalen System zu aktualisieren, ohne die Excel-Parameterdateien zu aktualisieren, die zu Azure DevOps hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="b515a-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![Warnmeldung](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="b515a-581">Beide Testfälle werden geladen, zusammen mit der Excel-Parameterdatei für den ersten Testfall.</span><span class="sxs-lookup"><span data-stu-id="b515a-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="b515a-582">Da Sie bei der letzten Ausführung **Hochladen** ausgewählt haben, werden die Parameterdateien von Azure DevOps gezogen.</span><span class="sxs-lookup"><span data-stu-id="b515a-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![Testfälle geladen](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="b515a-584">Wählen Sie nur den zweiten Testfall, und wählen Sie dann **Neu \> Testausführungs- und Parameterdateien generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="b515a-585">Excel-Parameterdatei bearbeiten</span><span class="sxs-lookup"><span data-stu-id="b515a-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="b515a-586">Wählen Sie nur den zweiten Testfall aus, und wählen Sie dann **Bearbeiten** aus, um die entsprechenden Excel-Parameterdatei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b515a-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="b515a-587">Kopieren Sie die gespeicherte Variable **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (weitere Informationen im Abschnitt [Ändern einer vorhandenen Aufgabenaufzeichnung, um einer gespeicherte Variablen zu erstellen](#modify-an-existing-task-recording-to-create-a-saved-variable)) aus dem ersten Testfall in alle Felder, in denen die Produktnummer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b515a-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="b515a-588">In diesem Fall kopieren Sie die Variable in die Felder **Produktnummer** und **Produktnummer prüfen** im Arbeitsblatt **EcoResProductListPage**.</span><span class="sxs-lookup"><span data-stu-id="b515a-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![Felder „Produktnummer und Produktnummer prüfen“](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="b515a-590">Variablen können nur zwischen Tests für den gleichen Testlauf übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="b515a-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="b515a-591">Die Namen der Variablen müssen genau übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b515a-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="b515a-592">Wählen Sie **Speichern** aus und schließen die Excel-Arbeitsmappe.</span><span class="sxs-lookup"><span data-stu-id="b515a-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="b515a-593">Wählen Sie **Hochladen** aus, um die Änderungen zu speichern, die Sie an der Excel-Parameterdatei vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="b515a-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="b515a-594">Verkettete Testfälle ausführen</span><span class="sxs-lookup"><span data-stu-id="b515a-594">Run the chained test cases</span></span>

1. <span data-ttu-id="b515a-595">Wählen Sie beide Testfälle aus, die ausgeführt werden sollen, und wählen Sie dann **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="b515a-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="b515a-596">Überprüfen Sie, dass beide Testfälle erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="b515a-596">Verify that both test cases have passed.</span></span>

    ![Auf „Erfolgreich“ festgelegtes Ergebnisfeld für beide Testfälle](./media/setup_rsa_tool_105.png)
