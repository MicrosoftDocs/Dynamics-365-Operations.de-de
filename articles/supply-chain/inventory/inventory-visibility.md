---
title: Inventory Visibility Add-In
description: In diesem Thema wird beschrieben, wie Sie das Inventory Visibility Add-in für Dynamics 365 Supply Chain Management installieren und konfigurieren.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 84f5e949f0c81f840c8a9086d05bbcfc576e42aa
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017005"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="663dc-103">Inventory Visibility Add-in</span><span class="sxs-lookup"><span data-stu-id="663dc-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="663dc-104">Das Inventory Visibility Add-in ist ein unabhängiger und hoch skalierbarer Microservice, der die Verfolgung von Beständen in Echtzeit ermöglicht und so eine globale Sicht auf den Bestand bietet.</span><span class="sxs-lookup"><span data-stu-id="663dc-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="663dc-105">Alle Informationen, die sich auf den Bestand beziehen, werden durch Low-Level-SQL-Integration nahezu in Echtzeit an den Dienst exportiert.</span><span class="sxs-lookup"><span data-stu-id="663dc-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="663dc-106">Externe Systeme greifen über RESTful APIs auf den Dienst zu, um Bestandsinformationen über festgelegte Dimensionen abzufragen und so eine Liste der verfügbaren Bestandspositionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="663dc-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="663dc-107">Inventory Visibility ist ein Microservice, der auf der Microsoft Dataverse aufbaut, d. h. Sie können ihn mit der Power Apps erweitern und mit der Power BI kundenspezifische Funktionen bereitstellen, um Ihre Geschäftsanforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="663dc-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="663dc-108">Es ist auch möglich, den Index zu erweitern, um Bestandsabfragen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="663dc-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="663dc-109">Inventory Visibility bietet Konfigurationsoptionen, mit denen es sich in mehrere Drittsysteme integrieren lässt.</span><span class="sxs-lookup"><span data-stu-id="663dc-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="663dc-110">Es unterstützt die standardisierte Dimension des Bestands, benutzerdefinierte Erweiterbarkeit und standardisierte, konfigurierbare berechnete Mengen.</span><span class="sxs-lookup"><span data-stu-id="663dc-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="663dc-111">In diesem Thema wird beschrieben, wie Sie das Inventory Visibility Add-In für Dynamics 365 Supply Chain Management installieren und konfigurieren und wie Sie seine Anwendungsprogrammierschnittstelle (API) verwenden.</span><span class="sxs-lookup"><span data-stu-id="663dc-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="663dc-112">Installieren Sie das Inventory Visibility Add-In</span><span class="sxs-lookup"><span data-stu-id="663dc-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="663dc-113">Sie müssen das Inventory Visibility Add-In über Microsoft Dynamics Lifecycle Services (LCS) installieren.</span><span class="sxs-lookup"><span data-stu-id="663dc-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="663dc-114">LCS ist ein Portal für die Zusammenarbeit, das eine Umgebung und eine Reihe von regelmäßig aktualisierten Diensten bereitstellt, die Sie bei der Verwaltung des Lebenszyklus Ihrer Dynamics 365 Finance and Operations-Apps unterstützen.</span><span class="sxs-lookup"><span data-stu-id="663dc-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="663dc-115">Weitere Informationen finden Sie unter [Ressourcen für Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="663dc-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="inventory-visibility-add-in-prerequisites"></a><span data-ttu-id="663dc-116">Voraussetzungen Add-In Bestandstransparenz</span><span class="sxs-lookup"><span data-stu-id="663dc-116">Inventory Visibility Add-in prerequisites</span></span>

<span data-ttu-id="663dc-117">Bevor Sie das Inventory Visibility Add-In installieren, müssen Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="663dc-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="663dc-118">Besorgen Sie sich ein LCS-Implementierungsprojekt mit mindestens einer bereitgestellten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="663dc-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="663dc-119">Stellen Sie sicher, dass die Voraussetzungen für das Festlegen von Add-Ins, die in der [Add-Ins-Übersicht](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) bereitgestellt werden, erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="663dc-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="663dc-120">Bestandssichtbarkeit erfordert keine Dual-Write-Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="663dc-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="663dc-121">Wenden Sie sich an das Team für Bestandssichtbarkeit unter [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), um die folgenden drei erforderlichen Dateien zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="663dc-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - <span data-ttu-id="663dc-122">`Inventory Visibility Integration.zip` (wenn die Version von Supply Chain Management, die Sie verwenden, älter ist als Version 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="663dc-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="663dc-123">Wenden Sie sich alternativ an das Team für Bestandstransparenz unter [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), um die Package Deployer-Pakete zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="663dc-123">Alternatively, contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package deployer packages.</span></span> <span data-ttu-id="663dc-124">Diese Pakete können von einem offiziellen Package Deployer-Tool verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="663dc-124">These packages can be used by an official package deployer tool.</span></span>
  - `InventoryServiceBase.PackageDeployer.zip`
  - <span data-ttu-id="663dc-125">`InventoryServiceApplication.PackageDeployer.zip` (Dieses Paket enthält alle Änderungen im `InventoryServiceBase`-Paket sowie zusätzliche Anwendungskomponenten für die Benutzeroberfläche)</span><span class="sxs-lookup"><span data-stu-id="663dc-125">`InventoryServiceApplication.PackageDeployer.zip` (this package contains all of the changes in the `InventoryServiceBase` package, plus additional UI application components)</span></span>
- <span data-ttu-id="663dc-126">Befolgen Sie die Anweisungen in [Schnellstart: Eine Anwendung bei der Microsoft Identity Platform registrieren](/azure/active-directory/develop/quickstart-register-app), um eine Anwendung zu registrieren und AAD unter Ihrem Azure-Abonnement einen geheimen Clientschlüssel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="663dc-126">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
  - [<span data-ttu-id="663dc-127">Anwendung registrieren</span><span class="sxs-lookup"><span data-stu-id="663dc-127">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
  - [<span data-ttu-id="663dc-128">Geheimen Clientschlüssel hinzufügen</span><span class="sxs-lookup"><span data-stu-id="663dc-128">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - <span data-ttu-id="663dc-129">Die **Anwendungs-ID (Client-ID)**, der **geheime Clientschlüssel** und die **Mandanten-ID** werden in den folgenden Schritten verwendet.</span><span class="sxs-lookup"><span data-stu-id="663dc-129">The **Application(Client) Id**, **Client Secret**, and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="663dc-130">Zu den derzeit unterstützten Ländern und Regionen gehören Kanada, die Vereinigten Staaten und die Europäische Union (EU).</span><span class="sxs-lookup"><span data-stu-id="663dc-130">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="663dc-131">Wenn Sie Fragen zu diesen Voraussetzungen haben, wenden Sie sich bitte an das Inventory Visibility-Produktteam.</span><span class="sxs-lookup"><span data-stu-id="663dc-131">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="663dc-132">Einrichten von Dataverse</span><span class="sxs-lookup"><span data-stu-id="663dc-132">Set up Dataverse</span></span>

<span data-ttu-id="663dc-133">Um Dataverse für die Verwendung mit der Bestandstransparenz einzurichten, müssen Sie zuerst die Voraussetzungen vorbereiten und dann entscheiden, ob Sie Dataverse entweder mit dem Package Deployer-Tool oder durch einen manuellen Import der Lösungen einrichten möchten (Sie müssen nicht beides tun).</span><span class="sxs-lookup"><span data-stu-id="663dc-133">To set up Dataverse for use with Inventory Visibility, you must first prepare the prerequisites and then decide whether to set up Dataverse using either the package deployer tool or by manually importing the solutions (you don't have to do both).</span></span> <span data-ttu-id="663dc-134">Instellieren Sie dann das Bestandstransparenz-Add-In.</span><span class="sxs-lookup"><span data-stu-id="663dc-134">Then install the Inventory Visibility Add-in.</span></span> <span data-ttu-id="663dc-135">In den folgenden Unterabschnitten beschrieben, wie Sie diese Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="663dc-135">The following subsections describe how to complete each of these tasks.</span></span>

#### <a name="prepare-dataverse-prerequisites"></a><span data-ttu-id="663dc-136">Dataverse-Voraussetzungen vorbereiten</span><span class="sxs-lookup"><span data-stu-id="663dc-136">Prepare Dataverse prerequisites</span></span>

<span data-ttu-id="663dc-137">Bevor Sie damit beginnen Dataverse einzurichten, fügen Sie Ihrem Mandanten ein Dienstprinzip hinzu, indem Sie folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="663dc-137">Before you start to set up Dataverse, add a service principle to your tenant by doing the following:</span></span>

1. <span data-ttu-id="663dc-138">Installieren Sie Azure AD PowerShell-Modul v2 wie in [Installieren Sie Azure Active Directory PowerShell für Graph](/powershell/azure/active-directory/install-adv2) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="663dc-138">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>

1. <span data-ttu-id="663dc-139">Führen Sie den folgenden PowerShell-Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="663dc-139">Run the following PowerShell command:</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a><span data-ttu-id="663dc-140">Dataverse mit dem Package Deployer-Tool einrichten</span><span class="sxs-lookup"><span data-stu-id="663dc-140">Set up Dataverse using the package deployer tool</span></span>

<span data-ttu-id="663dc-141">Nachdem Sie die Voraussetzungen erfüllt haben, gehen Sie wie folgt vor, wenn Sie Dataverse lieber mit dem Package Deployer-Tool einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="663dc-141">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse using the package deployer tool.</span></span> <span data-ttu-id="663dc-142">Im nächsten Abschnitt erfahren Sie, wie Sie die Lösungen stattdessen manuell importieren (tun Sie nicht beides).</span><span class="sxs-lookup"><span data-stu-id="663dc-142">See the next section for details about how to import the solutions manually instead (don't do both).</span></span>

1. <span data-ttu-id="663dc-143">Installieren Sie die Entwicklertools wie in [Herunterladen von NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="663dc-143">Install developer tools as described in [Download tools from NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span></span>

1. <span data-ttu-id="663dc-144">Wählen Sie basierend auf Ihren Geschäftsanforderungen das Paket `InventoryServiceBase` oder `InventoryServiceApplication` aus.</span><span class="sxs-lookup"><span data-stu-id="663dc-144">Based on your business requirements, choose the `InventoryServiceBase` or `InventoryServiceApplication` package.</span></span>

1. <span data-ttu-id="663dc-145">Importieren Sie die Lösungen:</span><span class="sxs-lookup"><span data-stu-id="663dc-145">Import the solutions:</span></span>
    1. <span data-ttu-id="663dc-146">Für das `InventoryServiceBase`-Paket:</span><span class="sxs-lookup"><span data-stu-id="663dc-146">For the `InventoryServiceBase` package:</span></span>
        - <span data-ttu-id="663dc-147">Entpacken Sie `InventoryServiceBase.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="663dc-147">Unzip `InventoryServiceBase.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="663dc-148">Suchen Sie den Ordner `InventoryServiceBase`, die Datei `[Content_Types].xml`, die Datei `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, die Datei `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` und die Datei `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span><span class="sxs-lookup"><span data-stu-id="663dc-148">Find folder `InventoryServiceBase`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span></span> 
        - <span data-ttu-id="663dc-149">Kopieren Sie diese Ordner und Dateien in das Verzeichnis `.\Tools\PackageDeployment`, das bei der Installation der Entwicklertools erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="663dc-149">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="663dc-150">Für das `InventoryServiceApplication`-Paket:</span><span class="sxs-lookup"><span data-stu-id="663dc-150">For the `InventoryServiceApplication` package:</span></span>
        - <span data-ttu-id="663dc-151">Entpacken Sie `InventoryServiceApplication.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="663dc-151">Unzip `InventoryServiceApplication.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="663dc-152">Suchen Sie den Ordner `InventoryServiceApplication`, die Datei `[Content_Types].xml`, die Datei `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, die Datei `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` und die Datei `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span><span class="sxs-lookup"><span data-stu-id="663dc-152">Find folder `InventoryServiceApplication`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span></span>
        - <span data-ttu-id="663dc-153">Kopieren Sie diese Ordner und Dateien in das Verzeichnis `.\Tools\PackageDeployment`, das bei der Installation der Entwicklertools erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="663dc-153">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="663dc-154">Führen Sie `.\Tools\PackageDeployment\PackageDeployer.exe` aus.</span><span class="sxs-lookup"><span data-stu-id="663dc-154">Execute `.\Tools\PackageDeployment\PackageDeployer.exe`.</span></span> <span data-ttu-id="663dc-155">Befolgen Sie die Anweisungen auf Ihrem Bildschirm, um die Lösungen zu importieren.</span><span class="sxs-lookup"><span data-stu-id="663dc-155">Follow the instructions on your screen to import the solutions.</span></span>

1. <span data-ttu-id="663dc-156">Weisen Sie dem Anwendungsnutzer Sicherheitsrollen zu.</span><span class="sxs-lookup"><span data-stu-id="663dc-156">Assign security roles to the application user.</span></span>
    1. <span data-ttu-id="663dc-157">Öffnen Sie die URL Ihrer Dataverse-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="663dc-157">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="663dc-158">Gehen Sie zu **Erweiterte Einstellungen \> System \> Sicherheit \> Benutzer** und finden Sie den Benutzer **# InventoryVisibility**.</span><span class="sxs-lookup"><span data-stu-id="663dc-158">Go to **Advanced Setting \> System \> Security \> Users**, and find user the named **# InventoryVisibility**.</span></span>
    1. <span data-ttu-id="663dc-159">Wählen Sie **Rolle zuweisen**, und wählen Sie dann **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="663dc-159">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="663dc-160">Wenn es eine Rolle namens **Common Data Service-Benutzer** gibt, wählen Sie diese ebenfalls aus.</span><span class="sxs-lookup"><span data-stu-id="663dc-160">If there is a role that is named **Common Data Service User**, select it as well.</span></span>

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a><span data-ttu-id="663dc-161">Dataverse manuell durch Importieren von Lösungen einrichten</span><span class="sxs-lookup"><span data-stu-id="663dc-161">Set up Dataverse manually by importing solutions</span></span>

<span data-ttu-id="663dc-162">Nachdem Sie die Voraussetzungen erfüllt haben, gehen Sie wie folgt vor, wenn Sie Dataverse lieber durch manuelles Importieren der Lösungen einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="663dc-162">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse by manually importing solutions.</span></span> <span data-ttu-id="663dc-163">Weitere Informationen zur Verwendung des Package Deployer-Tools finden Sie im vorherigen Abschnitt (tun Sie nicht beides).</span><span class="sxs-lookup"><span data-stu-id="663dc-163">See the previous section for details about how to use the package deployer tool instead (don't do both).</span></span>

1. <span data-ttu-id="663dc-164">Erstellen Sie einen Anwendungsbenutzer für Bestandssichtbarkeit in Dataverse:</span><span class="sxs-lookup"><span data-stu-id="663dc-164">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="663dc-165">Öffnen Sie die URL Ihrer Dataverse-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="663dc-165">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="663dc-166">Gehen Sie zu **Erweiterte Einstellung \> System \> Sicherheit \> Benutzer**, und erstellen Sie einen Anwendungsbenutzer.</span><span class="sxs-lookup"><span data-stu-id="663dc-166">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="663dc-167">Verwenden Sie das Menü Ansicht, um die Seitenansicht auf **Anwendungsbenutzer** zu ändern.</span><span class="sxs-lookup"><span data-stu-id="663dc-167">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="663dc-168">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="663dc-168">Select **New**.</span></span> <span data-ttu-id="663dc-169">Legen Sie die Anwendungs-ID auf *3022308a-b9bd-4a18-b8ac-2ddedb2075e1* fest.</span><span class="sxs-lookup"><span data-stu-id="663dc-169">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="663dc-170">(Die Objekt-ID wird automatisch geladen, wenn Sie Ihre Änderungen speichern.) Sie können den Namen anpassen.</span><span class="sxs-lookup"><span data-stu-id="663dc-170">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="663dc-171">Zum Beispiel können Sie ihn in *Bestandssichtbarkeit* ändern.</span><span class="sxs-lookup"><span data-stu-id="663dc-171">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="663dc-172">Klicken Sie abschließend auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="663dc-172">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="663dc-173">Wählen Sie **Rolle zuweisen**, und wählen Sie dann **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="663dc-173">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="663dc-174">Wenn es eine Rolle gibt, die **Common Data Service Benutzer** heißt, wählen Sie diese ebenfalls aus.</span><span class="sxs-lookup"><span data-stu-id="663dc-174">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="663dc-175">Weitere Informationen finden Sie unter [Erstellen eines Anwendungsbenutzers](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="663dc-175">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="663dc-176">Wenn die Standardsprache Ihres Dataverse nicht **Englisch** ist:</span><span class="sxs-lookup"><span data-stu-id="663dc-176">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="663dc-177">Gehen Sie zu **Erweiterte Einstellungen \> Verwaltung \> Sprachen**,</span><span class="sxs-lookup"><span data-stu-id="663dc-177">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="663dc-178">Wählen Sie **Englisch (LanguageCode = 1033)** und dann **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="663dc-178">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="663dc-179">Importieren Sie die Datei `Inventory Visibility Dataverse Solution.zip`, die Dataverse-Konfigurationsbezogene Entitäten und Power Apps enthält:</span><span class="sxs-lookup"><span data-stu-id="663dc-179">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="663dc-180">Gehen Sie auf die Seite **Lösungen**.</span><span class="sxs-lookup"><span data-stu-id="663dc-180">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="663dc-181">**Import** auswählen</span><span class="sxs-lookup"><span data-stu-id="663dc-181">Select **Import**.</span></span>

1. <span data-ttu-id="663dc-182">Importieren Sie den Auslöser-Flow für das Konfigurations-Upgrade:</span><span class="sxs-lookup"><span data-stu-id="663dc-182">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="663dc-183">Gehen Sie auf die Seite Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="663dc-183">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="663dc-184">Stellen Sie sicher, dass die Verbindung mit dem Namen *Dataverse (veraltet)* existiert.</span><span class="sxs-lookup"><span data-stu-id="663dc-184">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="663dc-185">(Wenn sie nicht existiert, erstellen Sie sie.)</span><span class="sxs-lookup"><span data-stu-id="663dc-185">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="663dc-186">Importieren Sie die `Inventory Visibility Configuration Trigger.zip`-Datei.</span><span class="sxs-lookup"><span data-stu-id="663dc-186">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="663dc-187">Nachdem sie importiert wurde, erscheint der Auslöser unter **Meine Flows**.</span><span class="sxs-lookup"><span data-stu-id="663dc-187">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="663dc-188">Initialisieren Sie die folgenden vier Variablen, basierend auf den Umgebungsinformationen:</span><span class="sxs-lookup"><span data-stu-id="663dc-188">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="663dc-189">Azure Mandant ID</span><span class="sxs-lookup"><span data-stu-id="663dc-189">Azure Tenant ID</span></span>
        - <span data-ttu-id="663dc-190">Azure-Anwendungs-Client-ID</span><span class="sxs-lookup"><span data-stu-id="663dc-190">Azure Application Client ID</span></span>
        - <span data-ttu-id="663dc-191">Azure-Anwendungs-Client-Geheimnis</span><span class="sxs-lookup"><span data-stu-id="663dc-191">Azure Application Client Secret</span></span>
        - <span data-ttu-id="663dc-192">Bestandssichtbarkeit Endpunkt</span><span class="sxs-lookup"><span data-stu-id="663dc-192">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="663dc-193">Weitere Informationen über diese Variable finden Sie im Abschnitt [Integration der Bestandssichtbarkeit festlegen](#setup-inventory-visibility-integration) weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="663dc-193">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="663dc-194">![Konfiguration Auslöser](media/configuration-trigger.png "Konfiguration Auslöser")</span><span class="sxs-lookup"><span data-stu-id="663dc-194">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="663dc-195">Wählen Sie **Einschalten**.</span><span class="sxs-lookup"><span data-stu-id="663dc-195">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="663dc-196">Installieren des Add-Ins</span><span class="sxs-lookup"><span data-stu-id="663dc-196">Install the add-in</span></span>

<span data-ttu-id="663dc-197">Um das Inventory Visibility Add-In zu installieren, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="663dc-197">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="663dc-198">Melden Sie sich am [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) Portal an.</span><span class="sxs-lookup"><span data-stu-id="663dc-198">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="663dc-199">Wählen Sie auf der Startseite das Projekt aus, in dem Ihre Umgebung bereitgestellt ist.</span><span class="sxs-lookup"><span data-stu-id="663dc-199">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="663dc-200">Wählen Sie auf der Projektseite die Umgebung aus, in der Sie das Add-In installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="663dc-200">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="663dc-201">Scrollen Sie auf der Umgebungsseite nach unten, bis Sie den Abschnitt **Umgebungs-Add-Ins** im Abschnitt **Power Platform-Integration** sehen, wo Sie den Umgebungsnamen Dataverse finden.</span><span class="sxs-lookup"><span data-stu-id="663dc-201">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="663dc-202">Wählen Sie Im Abschnitt **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="663dc-202">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="663dc-203">![Die Umgebungsseite in LCS](media/inventory-visibility-environment.png "Die Seite „Umgebung“ in LCS")</span><span class="sxs-lookup"><span data-stu-id="663dc-203">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="663dc-204">Wählen Sie den Link **Ein neues Add-In installieren**.</span><span class="sxs-lookup"><span data-stu-id="663dc-204">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="663dc-205">Es öffnet sich eine Liste der verfügbaren Add-Ins.</span><span class="sxs-lookup"><span data-stu-id="663dc-205">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="663dc-206">Wählen Sie **Bestandssichtbarkeit** in der Liste.</span><span class="sxs-lookup"><span data-stu-id="663dc-206">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="663dc-207">Geben Sie Werte für die folgenden Felder für Ihre Umgebung ein:</span><span class="sxs-lookup"><span data-stu-id="663dc-207">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="663dc-208">**AAD-Anwendung (Client) ID**</span><span class="sxs-lookup"><span data-stu-id="663dc-208">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="663dc-209">**AAD-Mandanten-ID**</span><span class="sxs-lookup"><span data-stu-id="663dc-209">**AAD tenant ID**</span></span>

    <span data-ttu-id="663dc-210">![Einrichtungsseite hinzufügen](media/inventory-visibility-setup.png "Seite zum Einrichten des Add-Ins")</span><span class="sxs-lookup"><span data-stu-id="663dc-210">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="663dc-211">Stimmen Sie den Bedingungen zu, indem Sie das Kontrollkästchen **Bedingungen und Konditionen** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="663dc-211">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="663dc-212">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="663dc-212">Select **Install**.</span></span> <span data-ttu-id="663dc-213">Der Status des Add-Ins wird als **Installation** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="663dc-213">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="663dc-214">Wenn es fertig ist, aktualisieren Sie die Seite, um den Status auf **Installiert** zu ändern.</span><span class="sxs-lookup"><span data-stu-id="663dc-214">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="663dc-215">Add-In deinstallieren</span><span class="sxs-lookup"><span data-stu-id="663dc-215">Uninstall the add-in</span></span>

<span data-ttu-id="663dc-216">Um das Add-In zu deinstallieren, wählen Sie **Deinstallieren**.</span><span class="sxs-lookup"><span data-stu-id="663dc-216">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="663dc-217">Wenn Sie LCS aktualisieren, wird das Bestandssichtbarkeit-Add-In entfernt.</span><span class="sxs-lookup"><span data-stu-id="663dc-217">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="663dc-218">Der Deinstallationsprozess entfernt die Registrierung des Add-Ins und startet außerdem einen Job zum Bereinigen aller Geschäftsdaten, die im Dienst gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="663dc-218">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="663dc-219">Verbrauchen von Lagerbestandsdaten aus Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="663dc-219">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="663dc-220">Bereitstellen des Integrationspakets für die Bestandssichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="663dc-220">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="663dc-221">Wenn Sie Supply Chain Management Version 10.0.17 oder früher verwenden, wenden Sie sich an das Bestandssichtbarkeit On-Board-Support-Team unter [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), um die Paketdatei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="663dc-221">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="663dc-222">Stellen Sie dann das Paket in LCS bereit.</span><span class="sxs-lookup"><span data-stu-id="663dc-222">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="663dc-223">Wenn beim Bereitstellen ein Fehler wegen Versionsinkongruenz auftritt, müssen Sie das X++ Projekt manuell in Ihre Entwicklungsumgebung importieren.</span><span class="sxs-lookup"><span data-stu-id="663dc-223">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="663dc-224">Erstellen Sie dann das einsatzfähige Paket in Ihrer Entwicklungsumgebung und stellen Sie es in Ihrer Produktionsumgebung bereit.</span><span class="sxs-lookup"><span data-stu-id="663dc-224">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="663dc-225">Der Code ist in der Supply Chain Management Version 10.0.18 enthalten.</span><span class="sxs-lookup"><span data-stu-id="663dc-225">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="663dc-226">Wenn Sie diese Version oder eine spätere verwenden, ist das Bereitstellen nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="663dc-226">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="663dc-227">Stellen Sie sicher, dass die folgenden Funktionen in Ihrer Supply Chain Management Umgebung aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="663dc-227">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="663dc-228">(Standardmäßig sind sie eingeschaltet.)</span><span class="sxs-lookup"><span data-stu-id="663dc-228">(By default, they are turned on.)</span></span>

| <span data-ttu-id="663dc-229">Beschreibung der Funktion</span><span class="sxs-lookup"><span data-stu-id="663dc-229">Feature description</span></span> | <span data-ttu-id="663dc-230">Code-Version</span><span class="sxs-lookup"><span data-stu-id="663dc-230">Code version</span></span> | <span data-ttu-id="663dc-231">Klasse umschalten</span><span class="sxs-lookup"><span data-stu-id="663dc-231">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="663dc-232">Aktivieren oder deaktivieren Sie die Verwendung von Bestandsdimensionen in der Tabelle InventSum</span><span class="sxs-lookup"><span data-stu-id="663dc-232">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="663dc-233">10.0.11</span><span class="sxs-lookup"><span data-stu-id="663dc-233">10.0.11</span></span> | <span data-ttu-id="663dc-234">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="663dc-234">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="663dc-235">Aktivieren oder deaktivieren Sie die Verwendung von Bestandsdimensionen in der Tabelle InventSumDelta</span><span class="sxs-lookup"><span data-stu-id="663dc-235">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="663dc-236">10.0.12</span><span class="sxs-lookup"><span data-stu-id="663dc-236">10.0.12</span></span> | <span data-ttu-id="663dc-237">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="663dc-237">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="663dc-238">Integration der Bestandssichtbarkeit einrichten</span><span class="sxs-lookup"><span data-stu-id="663dc-238">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="663dc-239">Öffnen Sie im Supply Chain Management den Arbeitsbereich **[Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** und schalten Sie die Funktion **Bestandssichtbarkeit-Integration** ein.</span><span class="sxs-lookup"><span data-stu-id="663dc-239">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="663dc-240">Gehen Sie zu **Bestandsverwaltung \> Parameter für die \>-Bestandssichtbarkeits-Integration festlegen** und geben Sie die URL der Umgebung ein, in der Sie die Bestandssichtbarkeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="663dc-240">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="663dc-241">Suchen Sie die Azure-Region Ihrer LCS Umgebung und geben Sie dann die URL ein.</span><span class="sxs-lookup"><span data-stu-id="663dc-241">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="663dc-242">Die URL hat die folgende Form:</span><span class="sxs-lookup"><span data-stu-id="663dc-242">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="663dc-243">Wenn Sie sich zum Beispiel in Europa befinden, hat Ihre Umgebung eine der folgenden URLs:</span><span class="sxs-lookup"><span data-stu-id="663dc-243">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="663dc-244">Die folgenden Regionen sind derzeit verfügbar.</span><span class="sxs-lookup"><span data-stu-id="663dc-244">The following regions are currently available.</span></span>

    | <span data-ttu-id="663dc-245">Azure-Region</span><span class="sxs-lookup"><span data-stu-id="663dc-245">Azure region</span></span> | <span data-ttu-id="663dc-246">Region Kurzname</span><span class="sxs-lookup"><span data-stu-id="663dc-246">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="663dc-247">Australien Ost</span><span class="sxs-lookup"><span data-stu-id="663dc-247">Australia east</span></span> | <span data-ttu-id="663dc-248">eau</span><span class="sxs-lookup"><span data-stu-id="663dc-248">eau</span></span> |
    | <span data-ttu-id="663dc-249">Australien Südost</span><span class="sxs-lookup"><span data-stu-id="663dc-249">Australia southeast</span></span> | <span data-ttu-id="663dc-250">seau</span><span class="sxs-lookup"><span data-stu-id="663dc-250">seau</span></span> |
    | <span data-ttu-id="663dc-251">Kanada Mitte</span><span class="sxs-lookup"><span data-stu-id="663dc-251">Canada central</span></span> | <span data-ttu-id="663dc-252">cca</span><span class="sxs-lookup"><span data-stu-id="663dc-252">cca</span></span> |
    | <span data-ttu-id="663dc-253">Kanada Ost</span><span class="sxs-lookup"><span data-stu-id="663dc-253">Canada east</span></span> | <span data-ttu-id="663dc-254">eca</span><span class="sxs-lookup"><span data-stu-id="663dc-254">eca</span></span> |
    | <span data-ttu-id="663dc-255">Europa, Norden</span><span class="sxs-lookup"><span data-stu-id="663dc-255">North Europe</span></span> | <span data-ttu-id="663dc-256">neu</span><span class="sxs-lookup"><span data-stu-id="663dc-256">neu</span></span> |
    | <span data-ttu-id="663dc-257">Europa, Westen</span><span class="sxs-lookup"><span data-stu-id="663dc-257">West Europe</span></span> | <span data-ttu-id="663dc-258">weu</span><span class="sxs-lookup"><span data-stu-id="663dc-258">weu</span></span> |
    | <span data-ttu-id="663dc-259">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="663dc-259">East US</span></span> | <span data-ttu-id="663dc-260">eus</span><span class="sxs-lookup"><span data-stu-id="663dc-260">eus</span></span> |
    | <span data-ttu-id="663dc-261">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="663dc-261">West US</span></span> | <span data-ttu-id="663dc-262">wus</span><span class="sxs-lookup"><span data-stu-id="663dc-262">wus</span></span> |

1. <span data-ttu-id="663dc-263">Gehen Sie zu **Bestandsverwaltung \> Periodisch \> Bestandssichtbarkeit-Integration**, und aktivieren Sie den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="663dc-263">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="663dc-264">Alle Ereignisse zu Bestandsänderungen aus dem Supply Chain Management werden nun in die Bestandssichtbarkeit übernommen.</span><span class="sxs-lookup"><span data-stu-id="663dc-264">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="663dc-265">Das öffentliche API des Bestandssichtbarkeit-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="663dc-265">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="663dc-266">Die öffentliche REST-API des Bestandssichtbarkeit-Add-Ins stellt mehrere spezifische Endpunkte für die Integration bereit.</span><span class="sxs-lookup"><span data-stu-id="663dc-266">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="663dc-267">Sie unterstützt drei Hauptinteraktionstypen:</span><span class="sxs-lookup"><span data-stu-id="663dc-267">It supports three main interaction types:</span></span>

- <span data-ttu-id="663dc-268">Verbuchung von Änderungen des Lagerbestands aus einem externen System in das Add-In</span><span class="sxs-lookup"><span data-stu-id="663dc-268">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="663dc-269">Abfrage aktueller Lagerbestände von einem externen System</span><span class="sxs-lookup"><span data-stu-id="663dc-269">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="663dc-270">Automatische Synchronisation mit dem Lagerbestand des Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="663dc-270">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="663dc-271">Die automatische Synchronisation ist nicht Teil der öffentlichen API.</span><span class="sxs-lookup"><span data-stu-id="663dc-271">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="663dc-272">Stattdessen wird sie in Umgebungen, in denen das Bestandssichtbarkeit-Add-In aktiviert ist, im Hintergrund ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="663dc-272">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="663dc-273">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="663dc-273">Authentication</span></span>

<span data-ttu-id="663dc-274">Für den Aufruf des Bestandssichtbarkeit-Add-Ins wird das Plattform-Sicherheitstoken verwendet.</span><span class="sxs-lookup"><span data-stu-id="663dc-274">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="663dc-275">Daher müssen Sie ein *Azure Active Directory (Azure AD) Token* generieren, indem Sie Ihre Azure AD Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="663dc-275">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="663dc-276">Sie müssen dann das Azure AD-Token verwenden, um das *Zugriffstoken* vom Sicherheitsdienst zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="663dc-276">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="663dc-277">Um ein Sicherheitsdienst-Token zu erhalten, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="663dc-277">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="663dc-278">Melden Sie sich am Azure-Portal an und verwenden Sie es, um die `clientId` und `clientSecret` für Ihre Supply Chain Management-Anwendung zu finden.</span><span class="sxs-lookup"><span data-stu-id="663dc-278">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="663dc-279">Rufen Sie ein Azure Active Directory-Token (`aadToken`) durch Senden einer HTTP-Anfrage mit den folgenden Eigenschaften ab:</span><span class="sxs-lookup"><span data-stu-id="663dc-279">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="663dc-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="663dc-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="663dc-281">**Methode** - `GET`</span><span class="sxs-lookup"><span data-stu-id="663dc-281">**Method** - `GET`</span></span>
    - <span data-ttu-id="663dc-282">**Textinhalt (Formulardaten)**:</span><span class="sxs-lookup"><span data-stu-id="663dc-282">**Body content (form data)**:</span></span>

        | <span data-ttu-id="663dc-283">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="663dc-283">key</span></span> | <span data-ttu-id="663dc-284">Wert</span><span class="sxs-lookup"><span data-stu-id="663dc-284">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="663dc-285">client_id</span><span class="sxs-lookup"><span data-stu-id="663dc-285">client_id</span></span> | <span data-ttu-id="663dc-286">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="663dc-286">${aadAppId}</span></span> |
        | <span data-ttu-id="663dc-287">client_secret</span><span class="sxs-lookup"><span data-stu-id="663dc-287">client_secret</span></span> | <span data-ttu-id="663dc-288">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="663dc-288">${aadAppSecret}</span></span> |
        | <span data-ttu-id="663dc-289">grant_type</span><span class="sxs-lookup"><span data-stu-id="663dc-289">grant_type</span></span> | <span data-ttu-id="663dc-290">client_credentials</span><span class="sxs-lookup"><span data-stu-id="663dc-290">client_credentials</span></span> |
        | <span data-ttu-id="663dc-291">resource</span><span class="sxs-lookup"><span data-stu-id="663dc-291">resource</span></span> | <span data-ttu-id="663dc-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="663dc-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="663dc-293">Sie sollten ein `aadToken` als Antwort erhalten, die dem folgenden Beispiel ähnelt.</span><span class="sxs-lookup"><span data-stu-id="663dc-293">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="663dc-294">Formulieren Sie eine JSON-Anforderung, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="663dc-294">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="663dc-295">Wobei:</span><span class="sxs-lookup"><span data-stu-id="663dc-295">Where:</span></span>
    - <span data-ttu-id="663dc-296">Der Wert von `client_assertion` muss das `aadToken`, das Sie im vorherigen Schritt erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="663dc-296">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="663dc-297">Der Wert von `context` muss die Umgebungs-ID sein, unter der Sie das Add-In bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="663dc-297">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="663dc-298">Stellen Sie alle anderen Werte wie im Beispiel gezeigt ein.</span><span class="sxs-lookup"><span data-stu-id="663dc-298">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="663dc-299">Senden Sie eine HTTP-Anforderung mit den folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="663dc-299">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="663dc-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="663dc-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="663dc-301">**Methode** - `POST`</span><span class="sxs-lookup"><span data-stu-id="663dc-301">**Method** - `POST`</span></span>
    - <span data-ttu-id="663dc-302">**HTTP-Header** – Fügen Sie die API-Version hinzu (Schlüssel ist `Api-Version`, und Wert ist `1.0`).</span><span class="sxs-lookup"><span data-stu-id="663dc-302">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="663dc-303">**Körperinhalt** – Fügen Sie die JSON-Anforderung ein, die Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="663dc-303">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="663dc-304">Sie werden eine `access_token` als Antwort erhalten.</span><span class="sxs-lookup"><span data-stu-id="663dc-304">You will get an `access_token` in response.</span></span> <span data-ttu-id="663dc-305">Diese benötigen Sie als Inhaber-Token, um die Inventory Visibility API aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="663dc-305">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="663dc-306">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="663dc-306">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="663dc-307">Beispielanforderung</span><span class="sxs-lookup"><span data-stu-id="663dc-307">Sample Request</span></span>

<span data-ttu-id="663dc-308">Als Referenz finden Sie hier ein Beispiel für eine http-Anfrage. Sie können beliebige Tools oder Codierungssprachen verwenden, um diese Anfrage zu senden, z. B. ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="663dc-308">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="663dc-309">Konfigurieren Sie die Inventory Visibility API</span><span class="sxs-lookup"><span data-stu-id="663dc-309">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="663dc-310">Bevor Sie den Dienst verwenden, müssen Sie die in den folgenden Unterabschnitten beschriebenen Konfigurationen durchführen.</span><span class="sxs-lookup"><span data-stu-id="663dc-310">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="663dc-311">Die Konfiguration kann je nach den Details Ihrer Umgebung variieren.</span><span class="sxs-lookup"><span data-stu-id="663dc-311">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="663dc-312">Sie besteht im Wesentlichen aus vier Teilen:</span><span class="sxs-lookup"><span data-stu-id="663dc-312">It primarily includes four parts:</span></span>

- [<span data-ttu-id="663dc-313">Partitionierung</span><span class="sxs-lookup"><span data-stu-id="663dc-313">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="663dc-314">Dimensions-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="663dc-314">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="663dc-315">Indizierung</span><span class="sxs-lookup"><span data-stu-id="663dc-315">Indexing</span></span>](#indexing)
- [<span data-ttu-id="663dc-316">Benutzerdefinierte Messung</span><span class="sxs-lookup"><span data-stu-id="663dc-316">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="663dc-317">Partitionierung</span><span class="sxs-lookup"><span data-stu-id="663dc-317">Partitioning</span></span>

<span data-ttu-id="663dc-318">Die Partitionierung kann die Leistung der Inventory Visibility API erheblich beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="663dc-318">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="663dc-319">Es ist eine gute Idee, ein Schema zu definieren, das kleine Gruppierungen von Daten zulässt und trotzdem sinnvolle Datenabfragen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="663dc-319">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="663dc-320">Die `organizationId` (`dataAreaId` im Supply Chain Management) wird immer Teil der Partitionierung sein, und standardmäßig ist Inventory Visibility so festgelegt, dass es nach Dimensionen wie *Standort + Lagerplatz* partitioniert.</span><span class="sxs-lookup"><span data-stu-id="663dc-320">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="663dc-321">Das bedeutet, dass der Dienst immer mit diesen in den Filtern definierten Dimensionen abgefragt werden muss.</span><span class="sxs-lookup"><span data-stu-id="663dc-321">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="663dc-322">*Standort* und *Lagerplatz* sind zwei allgemeine Standarddimensionen in Inventory Visibility.</span><span class="sxs-lookup"><span data-stu-id="663dc-322">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="663dc-323">Im Supply Chain Management heißen diese Dimensionen *Standort* (`InventSiteId`) und *Lagerort* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="663dc-323">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="663dc-324">Konfigurationen der Dimensionen</span><span class="sxs-lookup"><span data-stu-id="663dc-324">Dimension configurations</span></span>

<span data-ttu-id="663dc-325">Inventory Visibility stellt eine Liste allgemeiner Standarddimensionen zur Verfügung, um die Integration mehrerer Quellsysteme zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="663dc-325">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="663dc-326">In der folgenden Tabelle sind die Bestandsdimensionen aufgeführt, die als Standarddimensionen in Inventory Visibility verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="663dc-326">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="663dc-327">Dimensionstyp</span><span class="sxs-lookup"><span data-stu-id="663dc-327">Dimension type</span></span> | <span data-ttu-id="663dc-328">Dimensionsname</span><span class="sxs-lookup"><span data-stu-id="663dc-328">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="663dc-329">Produkt</span><span class="sxs-lookup"><span data-stu-id="663dc-329">Product</span></span> | `ColorId` |
| <span data-ttu-id="663dc-330">Produkt</span><span class="sxs-lookup"><span data-stu-id="663dc-330">Product</span></span> | `SizeId` |
| <span data-ttu-id="663dc-331">Produkt</span><span class="sxs-lookup"><span data-stu-id="663dc-331">Product</span></span> | `StyleId` |
| <span data-ttu-id="663dc-332">Produkt</span><span class="sxs-lookup"><span data-stu-id="663dc-332">Product</span></span> | `ConfigId` |
| <span data-ttu-id="663dc-333">Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="663dc-333">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="663dc-334">Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="663dc-334">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="663dc-335">Ziel</span><span class="sxs-lookup"><span data-stu-id="663dc-335">Location</span></span> | `LocationId` |
| <span data-ttu-id="663dc-336">Ziel</span><span class="sxs-lookup"><span data-stu-id="663dc-336">Location</span></span> | `SiteId` |
| <span data-ttu-id="663dc-337">Bestand Status</span><span class="sxs-lookup"><span data-stu-id="663dc-337">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="663dc-338">Lagerspezifisch</span><span class="sxs-lookup"><span data-stu-id="663dc-338">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="663dc-339">Lagerspezifisch</span><span class="sxs-lookup"><span data-stu-id="663dc-339">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="663dc-340">Lagerort-spezifisch</span><span class="sxs-lookup"><span data-stu-id="663dc-340">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="663dc-341">Der in der vorherigen Tabelle aufgeführte Dimensionstyp dient nur als Referenz.</span><span class="sxs-lookup"><span data-stu-id="663dc-341">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="663dc-342">Sie müssen den Dimensionstyp nicht in Inventory Visibility definieren.</span><span class="sxs-lookup"><span data-stu-id="663dc-342">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="663dc-343">Wenn eine benutzerdefinierte Dimension existiert und zu einem Standardwert fließen muss, wenn sie von Inventory Visibility konsumiert wird, können Sie den Namen **Benutzerdefinierte Dimension** in Inventory Visibility konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="663dc-343">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="663dc-344">Externe Systeme greifen auf Inventory Visibility über RESTful-APIs zu, mit denen Bestandsinformationen über festgelegte Dimensionen abgefragt werden können.</span><span class="sxs-lookup"><span data-stu-id="663dc-344">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="663dc-345">Für die Integration können Sie in Inventory Visibility die *Externe Kanaldatenquelle* und die Quelldimension zu den *Zieldimensionen* konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="663dc-345">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="663dc-346">Die Zieldimensionen sollten eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="663dc-346">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="663dc-347">Standarddimensionen in Inventory Visibility</span><span class="sxs-lookup"><span data-stu-id="663dc-347">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="663dc-348">Benutzerdefinierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="663dc-348">Custom dimensions</span></span>

<span data-ttu-id="663dc-349">Der Zweck der Dimensionskonfiguration ist es, die Multisystem-Integration für die Abfrage auf Dimensionen und das Buchungsereignis mit Dimensionen zu standardisieren.</span><span class="sxs-lookup"><span data-stu-id="663dc-349">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="663dc-350">Indizierung</span><span class="sxs-lookup"><span data-stu-id="663dc-350">Indexing</span></span>

<span data-ttu-id="663dc-351">In den meisten Fällen wird die Bestandsabfrage nicht nur auf der höchsten „Gesamt“-Ebene erfolgen, sondern Sie möchten die Ergebnisse möglicherweise auf der Basis der Bestandsdimensionen aggregiert sehen.</span><span class="sxs-lookup"><span data-stu-id="663dc-351">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="663dc-352">Inventory Visibility bietet Flexibilität, indem es Ihnen erlaubt, die Indizes festzulegen, die auf der Dimension oder der Kombination der Dimensionen basieren.</span><span class="sxs-lookup"><span data-stu-id="663dc-352">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="663dc-353">Derzeit können Sie nur Indizes bis maximal fünf konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="663dc-353">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="663dc-354">Sie müssen vor der Implementierung sorgfältig abwägen, welche Dimension oder Dimensionskombination Sie verwenden wollen, um sicherzustellen, dass sie Ihren geschäftlichen Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="663dc-354">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="663dc-355">Wenn Sie z. B. Produkte wie folgt abfragen wollen:</span><span class="sxs-lookup"><span data-stu-id="663dc-355">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="663dc-356">Abfrage des aggregierten Produktbestandes nach den Dimensionen *Farbe* und *Größe*.</span><span class="sxs-lookup"><span data-stu-id="663dc-356">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="663dc-357">In manchen Fällen wollen Sie nur das Produkt insgesamt abfragen.</span><span class="sxs-lookup"><span data-stu-id="663dc-357">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="663dc-358">Dann würden Sie zwei Indizes wie folgt definieren:</span><span class="sxs-lookup"><span data-stu-id="663dc-358">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="663dc-359">Die leere Klammer wird auf Basis der Produkt-ID innerhalb der Partition aggregiert.</span><span class="sxs-lookup"><span data-stu-id="663dc-359">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="663dc-360">Die Indizierung definiert, wie Sie Ihre Ergebnisse basierend auf der Abfrageeinstellung `groupBy` gruppieren können.</span><span class="sxs-lookup"><span data-stu-id="663dc-360">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="663dc-361">Wenn Sie in diesem Fall keine `groupBy`-Werte definieren, erhalten Sie Summen nach `productid`.</span><span class="sxs-lookup"><span data-stu-id="663dc-361">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="663dc-362">Andernfalls, wenn Sie `groupBy` als `groupBy=ColorId&groupBy=SizeId` definieren, erhalten Sie mehrere Zeilen zurück, basierend auf den verschiedenen Farb- und Größenkombinationen im System.</span><span class="sxs-lookup"><span data-stu-id="663dc-362">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="663dc-363">Sie können Ihre Abfragekriterien in den Abfragekörper einlagern.</span><span class="sxs-lookup"><span data-stu-id="663dc-363">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="663dc-364">Hier ist eine Beispielabfrage für das Produkt mit Farb- und Größenkombination.</span><span class="sxs-lookup"><span data-stu-id="663dc-364">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

<span data-ttu-id="663dc-365">Für das Feld `filters` unterstützt derzeit nur `ProductId` mehrere Werte.</span><span class="sxs-lookup"><span data-stu-id="663dc-365">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="663dc-366">Wenn die `ProductId` ein leeres Array ist, werden alle Produkte abgefragt.</span><span class="sxs-lookup"><span data-stu-id="663dc-366">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="663dc-367">Benutzerdefinierte Messung</span><span class="sxs-lookup"><span data-stu-id="663dc-367">Custom measurement</span></span>

<span data-ttu-id="663dc-368">Die voreingestellten Messungen sind mit dem Supply Chain Management verknüpft.</span><span class="sxs-lookup"><span data-stu-id="663dc-368">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="663dc-369">Möglicherweise möchten Sie jedoch eine Menge haben, die sich aus einer Kombination der Standard Messungen zusammensetzt.</span><span class="sxs-lookup"><span data-stu-id="663dc-369">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="663dc-370">Dazu können Sie eine Konfiguration von benutzerdefinierten Mengen haben, die zur Ausgabe der Bestandsabfragen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="663dc-370">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="663dc-371">Die Funktionalität erlaubt es Ihnen einfach, eine Reihe von Kennzahlen festzulegen, die addiert werden, und/oder eine Reihe von Kennzahlen, die subtrahiert werden, um die benutzerdefinierte Messung zu bilden.</span><span class="sxs-lookup"><span data-stu-id="663dc-371">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="663dc-372">Mit der folgenden Abfragebedingung konfigurieren Sie zum Beispiel die benutzerdefinierte Messung als `MyCustomAvailableforReservation`, die vom Verbrauchssystem verbraucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="663dc-372">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="663dc-373">Verbrauchs-System</span><span class="sxs-lookup"><span data-stu-id="663dc-373">Consumption system</span></span> | <span data-ttu-id="663dc-374">Berechnete Kennzahlen</span><span class="sxs-lookup"><span data-stu-id="663dc-374">Calculated measurers</span></span> | <span data-ttu-id="663dc-375">Datenquelle</span><span class="sxs-lookup"><span data-stu-id="663dc-375">Data source</span></span> | <span data-ttu-id="663dc-376">Modifikator</span><span class="sxs-lookup"><span data-stu-id="663dc-376">Modifier</span></span> | <span data-ttu-id="663dc-377">Modifikator Berechnungsart</span><span class="sxs-lookup"><span data-stu-id="663dc-377">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="663dc-378">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="663dc-378">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="663dc-379">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="663dc-379">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="663dc-380">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="663dc-380">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="663dc-381">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="663dc-381">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="663dc-382">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="663dc-382">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="663dc-383">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="663dc-383">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="663dc-384">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="663dc-384">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="663dc-385">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="663dc-385">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="663dc-386">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="663dc-386">Subtraction</span></span> |

<span data-ttu-id="663dc-387">Damit wird die Abfrage auf die benutzerdefinierte Messung Menge die folgende Ausgabe zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="663dc-387">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="663dc-388">Die Ausgabe `MyCustomAvailableforReservation` basiert auf der Berechnungseinstellung in den benutzerdefinierten Messungen als:</span><span class="sxs-lookup"><span data-stu-id="663dc-388">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="663dc-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="663dc-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="663dc-390">Verbuchung von Vorratsänderungen</span><span class="sxs-lookup"><span data-stu-id="663dc-390">Posting on-hand changes</span></span>

<span data-ttu-id="663dc-391">Die genaue URL, unter der das Ereignis gepostet wird, hängt von Ihrer geografischen Region ab.</span><span class="sxs-lookup"><span data-stu-id="663dc-391">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="663dc-392">Sie wird die Form haben:</span><span class="sxs-lookup"><span data-stu-id="663dc-392">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="663dc-393">Wenn Sie authentifiziert sind, kann diese URL zusammen mit der HTTP-Methode `POST` verwendet werden, um Ereignisse zu senden, die von Hand geändert werden.</span><span class="sxs-lookup"><span data-stu-id="663dc-393">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="663dc-394">Für die Kommunikation mit Dynamics 365-Diensten über HTTP-Anfragen wird ein spezieller Header verwendet, der die Umgebungs-ID der Supply Chain Management-Instanz angibt, mit der die Daten verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="663dc-394">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="663dc-395">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="663dc-395">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="663dc-396">Buchen von On-Hand-Änderungen Abfragebeispiel 1</span><span class="sxs-lookup"><span data-stu-id="663dc-396">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="663dc-397">Dieses Beispiel zeigt ein Szenario, in dem Sie die Konfiguration der Dimension in Power Apps festlegen werden.</span><span class="sxs-lookup"><span data-stu-id="663dc-397">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="663dc-398">Verwenden Sie die folgende Abfrage, um die Zuordnung der Dimension in Power Apps zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="663dc-398">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="663dc-399">Jetzt können Sie die `dimensionDataSource` angeben und benutzerdefinierte Dimensionen in Ihren Abfragen verwenden.</span><span class="sxs-lookup"><span data-stu-id="663dc-399">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="663dc-400">Das System wird die benutzerdefinierten Dimensionen automatisch in Basisdimensionen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="663dc-400">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="663dc-401">Buchen von Bestandsänderungen Abfragebeispiel 2</span><span class="sxs-lookup"><span data-stu-id="663dc-401">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="663dc-402">Dieses Beispiel zeigt ein Szenario, in dem keine Zuordnungen für die Dimensionskonfiguration in Power Apps festgelegt sind, sodass die Buchung auch die Basisdimensionen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="663dc-402">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="663dc-403">Alle Dimensionen müssen Basisdimensionen sein, wenn das Feld `dimensionDataSource` null, leer oder ein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="663dc-403">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="663dc-404">JSON-Dokument-Feldeigenschaften</span><span class="sxs-lookup"><span data-stu-id="663dc-404">JSON document field properties</span></span>

<span data-ttu-id="663dc-405">Die Felder aus den zuvor angegebenen JSON-Abfragebeispielen haben die in der folgenden Tabelle aufgeführten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="663dc-405">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="663dc-406">Feldkennung</span><span class="sxs-lookup"><span data-stu-id="663dc-406">Field ID</span></span> | <span data-ttu-id="663dc-407">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="663dc-407">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="663dc-408">Eine eindeutige ID für das spezifische Änderungsereignis.</span><span class="sxs-lookup"><span data-stu-id="663dc-408">A unique ID for the specific change event.</span></span> <span data-ttu-id="663dc-409">Diese ID wird verwendet, um sicherzustellen, dass, wenn die Kommunikation mit dem Dienst während der Buchung fehlschlägt, ein erneutes Einreichen des Ereignisses nicht dazu führt, dass dasselbe Ereignis im System doppelt gezählt wird.</span><span class="sxs-lookup"><span data-stu-id="663dc-409">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="663dc-410">Die Kennung der Organisation, die mit dem Ereignis verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="663dc-410">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="663dc-411">Dies entspricht der Zuordnung zu Supply Chain Management-Organisationen oder Datenbereichs-IDs.</span><span class="sxs-lookup"><span data-stu-id="663dc-411">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="663dc-412">Die Kennung des betreffenden Produkts.</span><span class="sxs-lookup"><span data-stu-id="663dc-412">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="663dc-413">Die Menge, um die der Lagerbestand geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="663dc-413">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="663dc-414">Wenn z.B. 10 neue Bagels in ein Regal gestellt wurden, wäre dieser Wert 10.</span><span class="sxs-lookup"><span data-stu-id="663dc-414">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="663dc-415">Wenn dann 3 Bagels aus dem Regal entfernt oder verkauft würden, wäre dieser Wert -3.</span><span class="sxs-lookup"><span data-stu-id="663dc-415">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="663dc-416">Die Datenquelle der Dimensionen, die im Umbuchungsereignis und in der Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="663dc-416">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="663dc-417">Wenn Sie die Datenquelle angeben, können Sie die benutzerdefinierten Dimensionen aus der angegebenen Datenquelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="663dc-417">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="663dc-418">Mit der Dimensionskonfiguration kann Inventory Visibility die benutzerdefinierten Dimensionen den allgemeinen Standarddimensionen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="663dc-418">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="663dc-419">Wenn die `dimensionDataSource` nicht angegeben wird, können Sie nur die allgemeinen Standarddimensionen in Ihren Abfragen verwenden.</span><span class="sxs-lookup"><span data-stu-id="663dc-419">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="663dc-420">Eine dynamische Tasche mit Schlüssel/Wertpaaren.</span><span class="sxs-lookup"><span data-stu-id="663dc-420">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="663dc-421">Diese werden einigen der Dimensionen im Supply Chain Management zugeordnet, aber Sie können auch benutzerdefinierte Dimensionen hinzufügen (wie *Quelle*), die angeben, ob das Ereignis aus dem Supply Chain Management oder einem externen System stammt.</span><span class="sxs-lookup"><span data-stu-id="663dc-421">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="663dc-422">Abfrage des aktuellen Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="663dc-422">Querying current on-hand</span></span>

<span data-ttu-id="663dc-423">Der Endpunkt für die Abfrage des aktuellen Lagerbestands wird eine ähnliche URL haben:</span><span class="sxs-lookup"><span data-stu-id="663dc-423">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="663dc-424">Er wird mit der HTTP-Methode `POST` abgefragt.</span><span class="sxs-lookup"><span data-stu-id="663dc-424">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="663dc-425">Abfrage des aktuellen Lagerbestands Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="663dc-425">Current on-hand query example 1</span></span>

<span data-ttu-id="663dc-426">Dieses Beispiel zeigt ein Szenario, bei dem Sie die Konfiguration der Dimension in Power Apps bereits abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="663dc-426">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="663dc-427">Verwenden Sie die folgende Abfrage, um die Zuordnung der Dimension in Power Apps zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="663dc-427">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="663dc-428">Jetzt können Sie die `dimensionDataSource` angeben und benutzerdefinierte Dimensionen in Ihren Abfragen verwenden.</span><span class="sxs-lookup"><span data-stu-id="663dc-428">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="663dc-429">Das System wird die benutzerdefinierten Dimensionen automatisch in Basisdimensionen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="663dc-429">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="663dc-430">Sie können die `DimensionDataSource` in `filters` angeben und benutzerdefinierte Dimensionen sowohl in `filters` als auch in `groupByValues` angeben.</span><span class="sxs-lookup"><span data-stu-id="663dc-430">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="663dc-431">Das System wird die benutzerdefinierten Dimensionen automatisch in Basisdimensionen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="663dc-431">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="663dc-432">Aktuelle Bestandsabfrage Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="663dc-432">Current on-hand query example 2</span></span>

<span data-ttu-id="663dc-433">Dieses Beispiel zeigt ein Szenario, in dem keine Zuordnungen für die Dimensionskonfiguration in Power Apps festgelegt sind, sodass die Buchung auch die Basisdimensionen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="663dc-433">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="663dc-434">Alle Dimensionen müssen Basisdimensionen sein, wenn das Feld `dimensionDataSource` unter `filters` null, leer oder ein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="663dc-434">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="663dc-435">Beispiel Rückgabeergebnis</span><span class="sxs-lookup"><span data-stu-id="663dc-435">Example return result</span></span>

<span data-ttu-id="663dc-436">Die in den vorherigen Beispielen gezeigten Abfragen könnten ein Ergebnis wie dieses zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="663dc-436">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="663dc-437">Beachten Sie, dass die Mengen-Felder als ein Wörterbuch von Kennzahlen und ihren zugehörigen Werten strukturiert sind.</span><span class="sxs-lookup"><span data-stu-id="663dc-437">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
