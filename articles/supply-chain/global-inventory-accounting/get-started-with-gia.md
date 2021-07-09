---
title: Einstieg in die Globale Bestandsbuchhaltung
description: In diesem Thema wird beschrieben, wie Sie mit der Globalen Bestandsbuchhaltung loslegen.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301697"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="14a70-103">Einstieg in die Globale Bestandsbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="14a70-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="14a70-104">Mit der Globalen Bestandsbuchhaltung können Sie mehrere Bestandsbuchhaltungen in den von Ihnen festgelegten Sachkonten der Globalen Bestandsbuchhaltung durchführen.</span><span class="sxs-lookup"><span data-stu-id="14a70-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="14a70-105">Sie müssen jedes Sachkonto der Globalen Bestandsbuchhaltung mit einer *Konvention* verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="14a70-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="14a70-106">Eine Konvention ist eine Sammlung der folgenden Arten von Rechnungslegungsgrundsätzen:</span><span class="sxs-lookup"><span data-stu-id="14a70-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="14a70-107">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="14a70-107">Cost object</span></span>
- <span data-ttu-id="14a70-108">Messungsgrundlage für Eingabe</span><span class="sxs-lookup"><span data-stu-id="14a70-108">Input measurement basis</span></span>
- <span data-ttu-id="14a70-109">Kostenflussannahme</span><span class="sxs-lookup"><span data-stu-id="14a70-109">Cost flow assumption</span></span>
- <span data-ttu-id="14a70-110">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="14a70-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="14a70-111">Auch nachdem Sie die Globale Bestandsbuchhaltung eingeschaltet haben, können Sie die Bestandsbuchhaltung in Microsoft Dynamics 365 Supply Chain Management wie gewohnt durchführen.</span><span class="sxs-lookup"><span data-stu-id="14a70-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="14a70-112">Die Globale Bestandsbuchhaltung ist ein Add-In.</span><span class="sxs-lookup"><span data-stu-id="14a70-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="14a70-113">Um seine Funktionen verfügbar zu machen, müssen Sie es über die Microsoft Dynamics Lifecycle Services (LCS) installieren.</span><span class="sxs-lookup"><span data-stu-id="14a70-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="14a70-114">Sie können es in einer Testumgebung testen, bevor Sie es für Produktionsumgebungen einschalten.</span><span class="sxs-lookup"><span data-stu-id="14a70-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="14a70-115">Die Globale Bestandsbuchhaltung unterstützt derzeit nicht alle Funktionen der Kostenverwaltung, die in Supply Chain Management integriert sind.</span><span class="sxs-lookup"><span data-stu-id="14a70-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="14a70-116">Daher ist es wichtig, dass Sie prüfen, ob der derzeit verfügbare Funktionsumfang Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="14a70-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="14a70-117">Wie Sie die öffentliche Vorschau der Globalen Bestandsbuchhaltung erhalten</span><span class="sxs-lookup"><span data-stu-id="14a70-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14a70-118">Um die Globale Bestandsbuchhaltung zu verwenden, müssen Sie über eine LCS-fähige Hochverfügbarkeitsumgebung verfügen (keine OneBox-Umgebung).</span><span class="sxs-lookup"><span data-stu-id="14a70-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="14a70-119">Außerdem müssen Sie Supply Chain Management Version 10.0.19 oder höher ausführen.</span><span class="sxs-lookup"><span data-stu-id="14a70-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="14a70-120">Um sich für die öffentliche Vorschau der Globalen Bestandsbuchhaltung anzumelden, senden Sie Ihre LCS Umgebungs-ID per E-Mail an das [Globale Bestandsbuchhaltung Team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="14a70-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="14a70-121">Nachdem Sie für das Programm genehmigt wurden, sendet Ihnen das Team eine Nachverfolgungs-E-Mail, die einen Beta-Schlüssel für die Globale Bestandsbuchhaltung und Ihre Service-Endpunkte enthält.</span><span class="sxs-lookup"><span data-stu-id="14a70-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="14a70-122">Nachdem Sie den Beta-Schlüssel erhalten haben, können Sie [das Add-In installieren](#install).</span><span class="sxs-lookup"><span data-stu-id="14a70-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="14a70-123">Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="14a70-123">Licensing</span></span>

<span data-ttu-id="14a70-124">Globale Bestandsbuchhaltung wird zusammen mit den Standardfunktionen der Bestandsbuchhaltung lizenziert, die für Supply Chain Management verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="14a70-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="14a70-125">Sie müssen keine zusätzliche Lizenz kaufen, um die Globale Bestandsbuchhaltung zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="14a70-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="14a70-126">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="14a70-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="14a70-127">Microsoft Power Platform-Integration einrichten</span><span class="sxs-lookup"><span data-stu-id="14a70-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="14a70-128">Bevor Sie die Add-In-Funktionalität aktivieren können, müssen Sie die Microsoft Power Platform-Integration durchführen, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="14a70-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="14a70-129">Öffnen Sie die LCS-Umgebung, in der Sie den Dienst hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="14a70-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="14a70-130">Gehen Sie zu **Vollständige Details**.</span><span class="sxs-lookup"><span data-stu-id="14a70-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="14a70-131">Wählen Sie im Abschnitt **Power Platform-Integration** die Option **Einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="14a70-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="14a70-132">Aktivieren Sie im Dialogfeld **Einrichten der Power Platform Umgebung** das Kontrollkästchen und wählen Sie dann **Einrichten**.</span><span class="sxs-lookup"><span data-stu-id="14a70-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="14a70-133">In der Regel dauert das Einrichten zwischen 60 und 90 Minuten.</span><span class="sxs-lookup"><span data-stu-id="14a70-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="14a70-134">Nachdem das Einrichten der Microsoft Power Platform-Umgebung abgeschlossen ist, wird auf der Seite der Name Ihrer Umgebung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="14a70-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="14a70-135">Außerdem wird im Abschnitt **Power Platform-Integration** die Aussage „Power Platform-Umgebung einrichten ist abgeschlossen.“</span><span class="sxs-lookup"><span data-stu-id="14a70-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="14a70-136">Für die Globale Bestandsbuchhaltung ist keine Dual-Write-Anwendung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="14a70-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="14a70-137">Weitere Informationen finden Sie unter [Einrichten nach Bereitstellen der Umgebung](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span><span class="sxs-lookup"><span data-stu-id="14a70-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="14a70-138">Festlegen von Dataverse</span><span class="sxs-lookup"><span data-stu-id="14a70-138">Set up Dataverse</span></span>

<span data-ttu-id="14a70-139">Bevor Sie Dataverse festlegen, fügen Sie die Serviceprinzipien der Globalen Bestandsbuchhaltung zu Ihrem Mandant hinzu, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="14a70-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="14a70-140">Installieren Sie Azure AD Modul für Windows PowerShell v2 wie in [Installieren von Azure Active Directory PowerShell für Graph](/powershell/azure/active-directory/install-adv2) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="14a70-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="14a70-141">Führen Sie den folgenden PowerShell-Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="14a70-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="14a70-142">Erstellen Sie anschließend Anwendungsbenutzer für die Globale Bestandsbuchhaltung in Dataverse, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="14a70-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="14a70-143">Öffnen Sie die URL Ihrer Dataverse-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="14a70-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="14a70-144">Gehen Sie zu **Erweiterte Einstellung \> System \> Sicherheit \> Benutzer**, und erstellen Sie einen Anwendungsbenutzer.</span><span class="sxs-lookup"><span data-stu-id="14a70-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="14a70-145">Verwenden Sie das Feld **Ansicht**, um die Seitenansicht auf *Anwendungsbenutzer* zu ändern.</span><span class="sxs-lookup"><span data-stu-id="14a70-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="14a70-146">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="14a70-146">Select **New**.</span></span>
1. <span data-ttu-id="14a70-147">Legen Sie das Feld **Anwendungs-ID** auf *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9* fest.</span><span class="sxs-lookup"><span data-stu-id="14a70-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="14a70-148">Wählen Sie **Rolle zuweisen**, und wählen Sie dann *Systemadministrator*.</span><span class="sxs-lookup"><span data-stu-id="14a70-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="14a70-149">Wenn es eine Rolle gibt, die *Common Data Service Benutzer* heißt, wählen Sie diese ebenfalls aus.</span><span class="sxs-lookup"><span data-stu-id="14a70-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="14a70-150">Wiederholen Sie die vorangegangenen Schritte, aber legen Sie das Feld **Anwendungs-ID** auf *5f58fc56-0202-49a8-ac9e-0946b049718b* fest.</span><span class="sxs-lookup"><span data-stu-id="14a70-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="14a70-151">Weitere Informationen finden Sie unter [Erstellen eines Anwendungsbenutzers](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="14a70-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="14a70-152">Wenn die Standardsprache Ihrer Dataverse-Installation nicht Englisch ist, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="14a70-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="14a70-153">Gehen Sie zu **Erweiterte Einstellung \> Verwaltung \> Sprachen**.</span><span class="sxs-lookup"><span data-stu-id="14a70-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="14a70-154">Wählen Sie *Englisch* (*LanguageCode=1033*), und wählen Sie dann **Anwenden**.</span><span class="sxs-lookup"><span data-stu-id="14a70-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="14a70-155">Installieren des Add-Ins</span><span class="sxs-lookup"><span data-stu-id="14a70-155">Install the add-in</span></span>

<span data-ttu-id="14a70-156">Gehen Sie folgendermaßen vor, um das Add-In zu installieren, damit Sie die Globale Bestandsbuchhaltung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="14a70-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="14a70-157">[Melden Sie sich](#sign-up) für die öffentliche Vorschau der Globalen Bestandsbuchhaltung an.</span><span class="sxs-lookup"><span data-stu-id="14a70-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="14a70-158">Melden Sie sich bei [LCS](https://lcs.dynamics.com/Logon/Index) an.</span><span class="sxs-lookup"><span data-stu-id="14a70-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="14a70-159">Navigieren Sie zu **Verwaltung von Vorschaufunktionen**.</span><span class="sxs-lookup"><span data-stu-id="14a70-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="14a70-160">Wählen Sie das Pluszeichen (**+**).</span><span class="sxs-lookup"><span data-stu-id="14a70-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="14a70-161">Geben Sie in das Feld **Code** Ihren Add-In-Betaschlüssel für die Globale Bestandsbuchhaltung ein.</span><span class="sxs-lookup"><span data-stu-id="14a70-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="14a70-162">(Sie sollten Ihren Beta-Schlüssel per E-Mail erhalten haben, als Sie sich angemeldet haben.)</span><span class="sxs-lookup"><span data-stu-id="14a70-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="14a70-163">Wählen Sie **Entsperren** aus.</span><span class="sxs-lookup"><span data-stu-id="14a70-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="14a70-164">Öffnen Sie die LCS-Umgebung, in der Sie den Dienst hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="14a70-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="14a70-165">Gehen Sie zu **Vollständige Details**.</span><span class="sxs-lookup"><span data-stu-id="14a70-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="14a70-166">Gehen Sie zu **Power Platform Integration**, und wählen Sie **Einrichten**.</span><span class="sxs-lookup"><span data-stu-id="14a70-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="14a70-167">Aktivieren Sie im Dialogfeld **Einrichten der Power Platform Umgebung** das Kontrollkästchen und wählen Sie dann **Einrichten**.</span><span class="sxs-lookup"><span data-stu-id="14a70-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="14a70-168">In der Regel dauert das Einrichten zwischen 60 und 90 Minuten.</span><span class="sxs-lookup"><span data-stu-id="14a70-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="14a70-169">Nach dem Einrichten der Microsoft Power Platform-Umgebung wählen Sie auf dem Inforegister **Umgebungs-Add-Ins** die Option **Ein neues Add-In installieren**.</span><span class="sxs-lookup"><span data-stu-id="14a70-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="14a70-170">Wählen Sie **Globale Bestandsbuchhaltung**.</span><span class="sxs-lookup"><span data-stu-id="14a70-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="14a70-171">Befolgen Sie die Installationsanleitung und erklären Sie sich mit den Allgemeinen Geschäftsbedingungen einverstanden.</span><span class="sxs-lookup"><span data-stu-id="14a70-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="14a70-172">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="14a70-172">Select **Install**.</span></span>
1. <span data-ttu-id="14a70-173">Auf der Registerkarte **Umgebungs-Add-Ins** Inforegister sollten Sie sehen, dass Globale Bestandsbuchhaltung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="14a70-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="14a70-174">Nach einigen Minuten sollte sich der Status von *Installieren* in *Installiert* ändern.</span><span class="sxs-lookup"><span data-stu-id="14a70-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="14a70-175">(Möglicherweise müssen Sie die Seite aktualisieren, um diese Änderung zu sehen.) An diesem Punkt ist die Globale Bestandsbuchhaltung einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="14a70-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="14a70-176">Einrichten der Integration</span><span class="sxs-lookup"><span data-stu-id="14a70-176">Set up the integration</span></span>

<span data-ttu-id="14a70-177">Führen Sie die folgenden Schritte aus, um die Integration zwischen Globaler Bestandsbuchhaltung und Supply Chain Management festzulegen.</span><span class="sxs-lookup"><span data-stu-id="14a70-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="14a70-178">Melden Sie sich im Supply Chain Management an.</span><span class="sxs-lookup"><span data-stu-id="14a70-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="14a70-179">Gehen Sie zu **Systemadministration \> Funktion Management**.</span><span class="sxs-lookup"><span data-stu-id="14a70-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="14a70-180">Wählen Sie **Nach Updates suchen**.</span><span class="sxs-lookup"><span data-stu-id="14a70-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="14a70-181">Suchen Sie auf der Registerkarte **Alle** nach der Funktion mit dem Namen *Globale Bestandsbuchhaltung*.</span><span class="sxs-lookup"><span data-stu-id="14a70-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="14a70-182">Wählen Sie **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="14a70-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="14a70-183">Gehen Sie zu **Globale Bestandsbuchhaltung \> Einrichten \> Globale Bestandsbuchhaltungsparameter \> Integrationsparameter**.</span><span class="sxs-lookup"><span data-stu-id="14a70-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="14a70-184">Geben Sie in die Felder **Datendienst-Endpunkt** und **Endpunkt Globale Bestandsbuchhaltung** die URLs aus der E-Mail ein, die das Team der Globalen Bestandsbuchhaltung bei der Anmeldung für die Vorschau gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="14a70-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="14a70-185">Die Globale Bestandsbuchhaltung ist nun einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="14a70-185">Global Inventory Accounting is now ready to use.</span></span>
