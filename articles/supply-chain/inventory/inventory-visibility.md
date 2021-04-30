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
ms.openlocfilehash: d09c7be5de75511b10d7a69d4b8ac12917b0dbe8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910424"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="4bd1b-103">Inventory Visibility Add-in</span><span class="sxs-lookup"><span data-stu-id="4bd1b-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="4bd1b-104">Das Inventory Visibility Add-in ist ein unabhängiger und hoch skalierbarer Microservice, der die Verfolgung von Beständen in Echtzeit ermöglicht und so eine globale Sicht auf den Bestand bietet.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="4bd1b-105">Alle Informationen, die sich auf den Bestand beziehen, werden durch Low-Level-SQL-Integration nahezu in Echtzeit an den Dienst exportiert.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="4bd1b-106">Externe Systeme greifen über RESTful APIs auf den Dienst zu, um Bestandsinformationen über festgelegte Dimensionen abzufragen und so eine Liste der verfügbaren Bestandspositionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="4bd1b-107">Inventory Visibility ist ein Microservice, der auf der Microsoft Dataverse aufbaut, d. h. Sie können ihn mit der Power Apps erweitern und mit der Power BI kundenspezifische Funktionen bereitstellen, um Ihre Geschäftsanforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="4bd1b-108">Es ist auch möglich, den Index zu erweitern, um Bestandsabfragen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="4bd1b-109">Inventory Visibility bietet Konfigurationsoptionen, mit denen es sich in mehrere Drittsysteme integrieren lässt.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="4bd1b-110">Es unterstützt die standardisierte Dimension des Bestands, benutzerdefinierte Erweiterbarkeit und standardisierte, konfigurierbare berechnete Mengen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="4bd1b-111">In diesem Thema wird beschrieben, wie Sie das Inventory Visibility Add-In für Dynamics 365 Supply Chain Management installieren und konfigurieren und wie Sie seine Anwendungsprogrammierschnittstelle (API) verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="4bd1b-112">Installieren Sie das Inventory Visibility Add-In</span><span class="sxs-lookup"><span data-stu-id="4bd1b-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="4bd1b-113">Sie müssen das Inventory Visibility Add-In über Microsoft Dynamics Lifecycle Services (LCS) installieren.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="4bd1b-114">LCS ist ein Portal für die Zusammenarbeit, das eine Umgebung und eine Reihe von regelmäßig aktualisierten Diensten bereitstellt, die Sie bei der Verwaltung des Lebenszyklus Ihrer Dynamics 365 Finance and Operations-Apps unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="4bd1b-115">Weitere Informationen finden Sie unter [Ressourcen für Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="4bd1b-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4bd1b-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="4bd1b-116">Prerequisites</span></span>

<span data-ttu-id="4bd1b-117">Bevor Sie das Inventory Visibility Add-In installieren, müssen Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="4bd1b-118">Besorgen Sie sich ein LCS-Implementierungsprojekt mit mindestens einer bereitgestellten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="4bd1b-119">Stellen Sie sicher, dass die Voraussetzungen für das Festlegen von Add-Ins, die in der [Add-Ins-Übersicht](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) bereitgestellt werden, erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="4bd1b-120">Bestandssichtbarkeit erfordert keine Dual-Write-Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="4bd1b-121">Wenden Sie sich an das Team für Bestandssichtbarkeit unter [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), um die folgenden drei erforderlichen Dateien zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="4bd1b-122">`Inventory Visibility Integration.zip` (wenn die Version von Supply Chain Management, die Sie verwenden, älter ist als Version 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="4bd1b-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="4bd1b-123">Befolgen Sie die Anweisungen in [Schnellstart: Eine Anwendung bei der Microsoft Identity Platform registrieren](/azure/active-directory/develop/quickstart-register-app), um eine Anwendung zu registrieren und AAD unter Ihrem Azure-Abonnement einen geheimen Clientschlüssel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-123">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
    - [<span data-ttu-id="4bd1b-124">Anwendung registrieren</span><span class="sxs-lookup"><span data-stu-id="4bd1b-124">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
    - [<span data-ttu-id="4bd1b-125">Geheimen Clientschlüssel hinzufügen</span><span class="sxs-lookup"><span data-stu-id="4bd1b-125">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
    - <span data-ttu-id="4bd1b-126">Die **Anwendungs-ID (Client-ID)**, der **geheime Clientschlüssel** und die **Mandanten-ID** werden in den folgenden Schritten verwendet.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-126">The **Application(Client) Id**, **Client Secret** and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="4bd1b-127">Zu den derzeit unterstützten Ländern und Regionen gehören Kanada, die Vereinigten Staaten und die Europäische Union (EU).</span><span class="sxs-lookup"><span data-stu-id="4bd1b-127">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="4bd1b-128">Wenn Sie Fragen zu diesen Voraussetzungen haben, wenden Sie sich bitte an das Inventory Visibility-Produktteam.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-128">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="4bd1b-129">Einrichten von Dataverse</span><span class="sxs-lookup"><span data-stu-id="4bd1b-129">Set up Dataverse</span></span>

<span data-ttu-id="4bd1b-130">Folgen Sie diesen Schritten, um Dataverse festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-130">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="4bd1b-131">Fügen Sie Ihrem Mandanten ein Dienstprinzip hinzu:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-131">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="4bd1b-132">Installieren Sie Azure AD PowerShell-Modul v2 wie in [Installieren Sie Azure Active Directory PowerShell für Graph](/powershell/azure/active-directory/install-adv2) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-132">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="4bd1b-133">Führen Sie den folgenden PowerShell-Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-133">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="4bd1b-134">Erstellen Sie einen Anwendungsbenutzer für Bestandssichtbarkeit in Dataverse:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-134">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="4bd1b-135">Öffnen Sie die URL Ihrer Dataverse-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-135">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="4bd1b-136">Gehen Sie zu **Erweiterte Einstellung \> System \> Sicherheit \> Benutzer**, und erstellen Sie einen Anwendungsbenutzer.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-136">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="4bd1b-137">Verwenden Sie das Menü Ansicht, um die Seitenansicht auf **Anwendungsbenutzer** zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-137">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="4bd1b-138">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-138">Select **New**.</span></span> <span data-ttu-id="4bd1b-139">Legen Sie die Anwendungs-ID auf *3022308a-b9bd-4a18-b8ac-2ddedb2075e1* fest.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-139">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="4bd1b-140">(Die Objekt-ID wird automatisch geladen, wenn Sie Ihre Änderungen speichern.) Sie können den Namen anpassen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-140">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="4bd1b-141">Zum Beispiel können Sie ihn in *Bestandssichtbarkeit* ändern.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-141">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="4bd1b-142">Klicken Sie abschließend auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-142">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="4bd1b-143">Wählen Sie **Rolle zuweisen**, und wählen Sie dann **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-143">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="4bd1b-144">Wenn es eine Rolle gibt, die **Common Data Service Benutzer** heißt, wählen Sie diese ebenfalls aus.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-144">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="4bd1b-145">Weitere Informationen finden Sie unter [Erstellen eines Anwendungsbenutzers](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="4bd1b-145">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="4bd1b-146">Wenn die Standardsprache Ihres Dataverse nicht **Englisch** ist:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-146">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="4bd1b-147">Gehen Sie zu **Erweiterte Einstellungen \> Verwaltung \> Sprachen**,</span><span class="sxs-lookup"><span data-stu-id="4bd1b-147">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="4bd1b-148">Wählen Sie **Englisch (LanguageCode = 1033)** und dann **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-148">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="4bd1b-149">Importieren Sie die Datei `Inventory Visibility Dataverse Solution.zip`, die Dataverse-Konfigurationsbezogene Entitäten und Power Apps enthält:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-149">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="4bd1b-150">Gehen Sie auf die Seite **Lösungen**.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-150">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="4bd1b-151">**Import** auswählen</span><span class="sxs-lookup"><span data-stu-id="4bd1b-151">Select **Import**.</span></span>

1. <span data-ttu-id="4bd1b-152">Importieren Sie den Auslöser-Flow für das Konfigurations-Upgrade:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-152">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="4bd1b-153">Gehen Sie auf die Seite Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-153">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="4bd1b-154">Stellen Sie sicher, dass die Verbindung mit dem Namen *Dataverse (veraltet)* existiert.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-154">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="4bd1b-155">(Wenn sie nicht existiert, erstellen Sie sie.)</span><span class="sxs-lookup"><span data-stu-id="4bd1b-155">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="4bd1b-156">Importieren Sie die `Inventory Visibility Configuration Trigger.zip`-Datei.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-156">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="4bd1b-157">Nachdem sie importiert wurde, erscheint der Auslöser unter **Meine Flows**.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-157">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="4bd1b-158">Initialisieren Sie die folgenden vier Variablen, basierend auf den Umgebungsinformationen:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-158">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="4bd1b-159">Azure Mandant ID</span><span class="sxs-lookup"><span data-stu-id="4bd1b-159">Azure Tenant ID</span></span>
        - <span data-ttu-id="4bd1b-160">Azure-Anwendungs-Client-ID</span><span class="sxs-lookup"><span data-stu-id="4bd1b-160">Azure Application Client ID</span></span>
        - <span data-ttu-id="4bd1b-161">Azure-Anwendungs-Client-Geheimnis</span><span class="sxs-lookup"><span data-stu-id="4bd1b-161">Azure Application Client Secret</span></span>
        - <span data-ttu-id="4bd1b-162">Bestandssichtbarkeit Endpunkt</span><span class="sxs-lookup"><span data-stu-id="4bd1b-162">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="4bd1b-163">Weitere Informationen über diese Variable finden Sie im Abschnitt [Integration der Bestandssichtbarkeit festlegen](#setup-inventory-visibility-integration) weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-163">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="4bd1b-164">![Konfiguration Auslöser](media/configuration-trigger.png "Konfiguration Auslöser")</span><span class="sxs-lookup"><span data-stu-id="4bd1b-164">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="4bd1b-165">Wählen Sie **Einschalten**.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-165">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="4bd1b-166">Installieren des Add-Ins</span><span class="sxs-lookup"><span data-stu-id="4bd1b-166">Install the add-in</span></span>

<span data-ttu-id="4bd1b-167">Um das Inventory Visibility Add-In zu installieren, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-167">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="4bd1b-168">Melden Sie sich am [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) Portal an.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-168">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="4bd1b-169">Wählen Sie auf der Startseite das Projekt aus, in dem Ihre Umgebung bereitgestellt ist.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-169">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="4bd1b-170">Wählen Sie auf der Projektseite die Umgebung aus, in der Sie das Add-In installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-170">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="4bd1b-171">Scrollen Sie auf der Umgebungsseite nach unten, bis Sie den Abschnitt **Umgebungs-Add-Ins** im Abschnitt **Power Platform-Integration** sehen, wo Sie den Umgebungsnamen Dataverse finden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-171">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="4bd1b-172">Wählen Sie Im Abschnitt **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-172">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="4bd1b-173">![Die Umgebungsseite in LCS](media/inventory-visibility-environment.png "Die Seite „Umgebung“ in LCS")</span><span class="sxs-lookup"><span data-stu-id="4bd1b-173">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="4bd1b-174">Wählen Sie den Link **Ein neues Add-In installieren**.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-174">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="4bd1b-175">Es öffnet sich eine Liste der verfügbaren Add-Ins.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-175">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="4bd1b-176">Wählen Sie **Bestandssichtbarkeit** in der Liste.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-176">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="4bd1b-177">Geben Sie Werte für die folgenden Felder für Ihre Umgebung ein:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-177">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="4bd1b-178">**AAD-Anwendung (Client) ID**</span><span class="sxs-lookup"><span data-stu-id="4bd1b-178">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="4bd1b-179">**AAD-Mandanten-ID**</span><span class="sxs-lookup"><span data-stu-id="4bd1b-179">**AAD tenant ID**</span></span>

    <span data-ttu-id="4bd1b-180">![Einrichtungsseite hinzufügen](media/inventory-visibility-setup.png "Seite zum Einrichten des Add-Ins")</span><span class="sxs-lookup"><span data-stu-id="4bd1b-180">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="4bd1b-181">Stimmen Sie den Bedingungen zu, indem Sie das Kontrollkästchen **Bedingungen und Konditionen** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-181">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="4bd1b-182">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-182">Select **Install**.</span></span> <span data-ttu-id="4bd1b-183">Der Status des Add-Ins wird als **Installation** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-183">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="4bd1b-184">Wenn es fertig ist, aktualisieren Sie die Seite, um den Status auf **Installiert** zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-184">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="4bd1b-185">Add-In deinstallieren</span><span class="sxs-lookup"><span data-stu-id="4bd1b-185">Uninstall the add-in</span></span>

<span data-ttu-id="4bd1b-186">Um das Add-In zu deinstallieren, wählen Sie **Deinstallieren**.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-186">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="4bd1b-187">Wenn Sie LCS aktualisieren, wird das Bestandssichtbarkeit-Add-In entfernt.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-187">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="4bd1b-188">Der Deinstallationsprozess entfernt die Registrierung des Add-Ins und startet außerdem einen Job zum Bereinigen aller Geschäftsdaten, die im Dienst gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-188">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="4bd1b-189">Verbrauchen von Lagerbestandsdaten aus Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4bd1b-189">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="4bd1b-190">Bereitstellen des Integrationspakets für die Bestandssichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="4bd1b-190">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="4bd1b-191">Wenn Sie Supply Chain Management Version 10.0.17 oder früher verwenden, wenden Sie sich an das Bestandssichtbarkeit On-Board-Support-Team unter [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), um die Paketdatei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-191">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="4bd1b-192">Stellen Sie dann das Paket in LCS bereit.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-192">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="4bd1b-193">Wenn beim Bereitstellen ein Fehler wegen Versionsinkongruenz auftritt, müssen Sie das X++ Projekt manuell in Ihre Entwicklungsumgebung importieren.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-193">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="4bd1b-194">Erstellen Sie dann das einsatzfähige Paket in Ihrer Entwicklungsumgebung und stellen Sie es in Ihrer Produktionsumgebung bereit.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-194">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="4bd1b-195">Der Code ist in der Supply Chain Management Version 10.0.18 enthalten.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-195">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="4bd1b-196">Wenn Sie diese Version oder eine spätere verwenden, ist das Bereitstellen nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-196">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="4bd1b-197">Stellen Sie sicher, dass die folgenden Funktionen in Ihrer Supply Chain Management Umgebung aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-197">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="4bd1b-198">(Standardmäßig sind sie eingeschaltet.)</span><span class="sxs-lookup"><span data-stu-id="4bd1b-198">(By default, they are turned on.)</span></span>

| <span data-ttu-id="4bd1b-199">Beschreibung der Funktion</span><span class="sxs-lookup"><span data-stu-id="4bd1b-199">Feature description</span></span> | <span data-ttu-id="4bd1b-200">Code-Version</span><span class="sxs-lookup"><span data-stu-id="4bd1b-200">Code version</span></span> | <span data-ttu-id="4bd1b-201">Klasse umschalten</span><span class="sxs-lookup"><span data-stu-id="4bd1b-201">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="4bd1b-202">Aktivieren oder deaktivieren Sie die Verwendung von Bestandsdimensionen in der Tabelle InventSum</span><span class="sxs-lookup"><span data-stu-id="4bd1b-202">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="4bd1b-203">10.0.11</span><span class="sxs-lookup"><span data-stu-id="4bd1b-203">10.0.11</span></span> | <span data-ttu-id="4bd1b-204">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="4bd1b-204">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="4bd1b-205">Aktivieren oder deaktivieren Sie die Verwendung von Bestandsdimensionen in der Tabelle InventSumDelta</span><span class="sxs-lookup"><span data-stu-id="4bd1b-205">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="4bd1b-206">10.0.12</span><span class="sxs-lookup"><span data-stu-id="4bd1b-206">10.0.12</span></span> | <span data-ttu-id="4bd1b-207">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="4bd1b-207">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="4bd1b-208">Integration der Bestandssichtbarkeit einrichten</span><span class="sxs-lookup"><span data-stu-id="4bd1b-208">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="4bd1b-209">Öffnen Sie im Supply Chain Management den Arbeitsbereich **[Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** und schalten Sie die Funktion **Bestandssichtbarkeit-Integration** ein.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-209">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="4bd1b-210">Gehen Sie zu **Bestandsverwaltung \> Parameter für die \>-Bestandssichtbarkeits-Integration festlegen** und geben Sie die URL der Umgebung ein, in der Sie die Bestandssichtbarkeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-210">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="4bd1b-211">Suchen Sie die Azure-Region Ihrer LCS Umgebung und geben Sie dann die URL ein.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-211">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="4bd1b-212">Die URL hat die folgende Form:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-212">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="4bd1b-213">Wenn Sie sich zum Beispiel in Europa befinden, hat Ihre Umgebung eine der folgenden URLs:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-213">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="4bd1b-214">Die folgenden Regionen sind derzeit verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-214">The following regions are currently available.</span></span>

    | <span data-ttu-id="4bd1b-215">Azure-Region</span><span class="sxs-lookup"><span data-stu-id="4bd1b-215">Azure region</span></span> | <span data-ttu-id="4bd1b-216">Region Kurzname</span><span class="sxs-lookup"><span data-stu-id="4bd1b-216">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="4bd1b-217">Australien Ost</span><span class="sxs-lookup"><span data-stu-id="4bd1b-217">Australia east</span></span> | <span data-ttu-id="4bd1b-218">eau</span><span class="sxs-lookup"><span data-stu-id="4bd1b-218">eau</span></span> |
    | <span data-ttu-id="4bd1b-219">Australien Südost</span><span class="sxs-lookup"><span data-stu-id="4bd1b-219">Australia southeast</span></span> | <span data-ttu-id="4bd1b-220">seau</span><span class="sxs-lookup"><span data-stu-id="4bd1b-220">seau</span></span> |
    | <span data-ttu-id="4bd1b-221">Kanada Mitte</span><span class="sxs-lookup"><span data-stu-id="4bd1b-221">Canada central</span></span> | <span data-ttu-id="4bd1b-222">cca</span><span class="sxs-lookup"><span data-stu-id="4bd1b-222">cca</span></span> |
    | <span data-ttu-id="4bd1b-223">Kanada Ost</span><span class="sxs-lookup"><span data-stu-id="4bd1b-223">Canada east</span></span> | <span data-ttu-id="4bd1b-224">eca</span><span class="sxs-lookup"><span data-stu-id="4bd1b-224">eca</span></span> |
    | <span data-ttu-id="4bd1b-225">Europa, Norden</span><span class="sxs-lookup"><span data-stu-id="4bd1b-225">North Europe</span></span> | <span data-ttu-id="4bd1b-226">neu</span><span class="sxs-lookup"><span data-stu-id="4bd1b-226">neu</span></span> |
    | <span data-ttu-id="4bd1b-227">Europa, Westen</span><span class="sxs-lookup"><span data-stu-id="4bd1b-227">West Europe</span></span> | <span data-ttu-id="4bd1b-228">weu</span><span class="sxs-lookup"><span data-stu-id="4bd1b-228">weu</span></span> |
    | <span data-ttu-id="4bd1b-229">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="4bd1b-229">East US</span></span> | <span data-ttu-id="4bd1b-230">eus</span><span class="sxs-lookup"><span data-stu-id="4bd1b-230">eus</span></span> |
    | <span data-ttu-id="4bd1b-231">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="4bd1b-231">West US</span></span> | <span data-ttu-id="4bd1b-232">wus</span><span class="sxs-lookup"><span data-stu-id="4bd1b-232">wus</span></span> |

1. <span data-ttu-id="4bd1b-233">Gehen Sie zu **Bestandsverwaltung \> Periodisch \> Bestandssichtbarkeit-Integration**, und aktivieren Sie den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-233">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="4bd1b-234">Alle Ereignisse zu Bestandsänderungen aus dem Supply Chain Management werden nun in die Bestandssichtbarkeit übernommen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-234">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="4bd1b-235">Das öffentliche API des Bestandssichtbarkeit-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="4bd1b-235">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="4bd1b-236">Die öffentliche REST-API des Bestandssichtbarkeit-Add-Ins stellt mehrere spezifische Endpunkte für die Integration bereit.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-236">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="4bd1b-237">Sie unterstützt drei Hauptinteraktionstypen:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-237">It supports three main interaction types:</span></span>

- <span data-ttu-id="4bd1b-238">Verbuchung von Änderungen des Lagerbestands aus einem externen System in das Add-In</span><span class="sxs-lookup"><span data-stu-id="4bd1b-238">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="4bd1b-239">Abfrage aktueller Lagerbestände von einem externen System</span><span class="sxs-lookup"><span data-stu-id="4bd1b-239">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="4bd1b-240">Automatische Synchronisation mit dem Lagerbestand des Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4bd1b-240">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="4bd1b-241">Die automatische Synchronisation ist nicht Teil der öffentlichen API.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-241">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="4bd1b-242">Stattdessen wird sie in Umgebungen, in denen das Bestandssichtbarkeit-Add-In aktiviert ist, im Hintergrund ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-242">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="4bd1b-243">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-243">Authentication</span></span>

<span data-ttu-id="4bd1b-244">Für den Aufruf des Bestandssichtbarkeit-Add-Ins wird das Plattform-Sicherheitstoken verwendet.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-244">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="4bd1b-245">Daher müssen Sie ein *Azure Active Directory (Azure AD) Token* generieren, indem Sie Ihre Azure AD Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-245">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="4bd1b-246">Sie müssen dann das Azure AD-Token verwenden, um das *Zugriffstoken* vom Sicherheitsdienst zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-246">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="4bd1b-247">Um ein Sicherheitsdienst-Token zu erhalten, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-247">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="4bd1b-248">Melden Sie sich am Azure-Portal an und verwenden Sie es, um die `clientId` und `clientSecret` für Ihre Supply Chain Management-Anwendung zu finden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-248">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="4bd1b-249">Rufen Sie ein Azure Active Directory-Token (`aadToken`) durch Senden einer HTTP-Anfrage mit den folgenden Eigenschaften ab:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-249">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="4bd1b-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="4bd1b-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="4bd1b-251">**Methode** - `GET`</span><span class="sxs-lookup"><span data-stu-id="4bd1b-251">**Method** - `GET`</span></span>
    - <span data-ttu-id="4bd1b-252">**Textinhalt (Formulardaten)**:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-252">**Body content (form data)**:</span></span>

        | <span data-ttu-id="4bd1b-253">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="4bd1b-253">key</span></span> | <span data-ttu-id="4bd1b-254">Wert</span><span class="sxs-lookup"><span data-stu-id="4bd1b-254">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="4bd1b-255">client_id</span><span class="sxs-lookup"><span data-stu-id="4bd1b-255">client_id</span></span> | <span data-ttu-id="4bd1b-256">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="4bd1b-256">${aadAppId}</span></span> |
        | <span data-ttu-id="4bd1b-257">client_secret</span><span class="sxs-lookup"><span data-stu-id="4bd1b-257">client_secret</span></span> | <span data-ttu-id="4bd1b-258">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="4bd1b-258">${aadAppSecret}</span></span> |
        | <span data-ttu-id="4bd1b-259">grant_type</span><span class="sxs-lookup"><span data-stu-id="4bd1b-259">grant_type</span></span> | <span data-ttu-id="4bd1b-260">client_credentials</span><span class="sxs-lookup"><span data-stu-id="4bd1b-260">client_credentials</span></span> |
        | <span data-ttu-id="4bd1b-261">resource</span><span class="sxs-lookup"><span data-stu-id="4bd1b-261">resource</span></span> | <span data-ttu-id="4bd1b-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="4bd1b-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="4bd1b-263">Sie sollten ein `aadToken` als Antwort erhalten, die dem folgenden Beispiel ähnelt.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-263">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="4bd1b-264">Formulieren Sie eine JSON-Anforderung, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-264">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="4bd1b-265">Wobei:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-265">Where:</span></span>
    - <span data-ttu-id="4bd1b-266">Der Wert von `client_assertion` muss das `aadToken`, das Sie im vorherigen Schritt erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-266">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="4bd1b-267">Der Wert von `context` muss die Umgebungs-ID sein, unter der Sie das Add-In bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-267">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="4bd1b-268">Stellen Sie alle anderen Werte wie im Beispiel gezeigt ein.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-268">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="4bd1b-269">Senden Sie eine HTTP-Anforderung mit den folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-269">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="4bd1b-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="4bd1b-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="4bd1b-271">**Methode** - `POST`</span><span class="sxs-lookup"><span data-stu-id="4bd1b-271">**Method** - `POST`</span></span>
    - <span data-ttu-id="4bd1b-272">**HTTP-Header** – Fügen Sie die API-Version hinzu (Schlüssel ist `Api-Version`, und Wert ist `1.0`).</span><span class="sxs-lookup"><span data-stu-id="4bd1b-272">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="4bd1b-273">**Körperinhalt** – Fügen Sie die JSON-Anforderung ein, die Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-273">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="4bd1b-274">Sie werden eine `access_token` als Antwort erhalten.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-274">You will get an `access_token` in response.</span></span> <span data-ttu-id="4bd1b-275">Diese benötigen Sie als Inhaber-Token, um die Inventory Visibility API aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-275">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="4bd1b-276">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-276">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="4bd1b-277">Beispielanforderung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-277">Sample Request</span></span>

<span data-ttu-id="4bd1b-278">Als Referenz finden Sie hier ein Beispiel für eine http-Anfrage. Sie können beliebige Tools oder Codierungssprachen verwenden, um diese Anfrage zu senden, z. B. ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-278">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

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

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="4bd1b-279">Konfigurieren Sie die Inventory Visibility API</span><span class="sxs-lookup"><span data-stu-id="4bd1b-279">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="4bd1b-280">Bevor Sie den Dienst verwenden, müssen Sie die in den folgenden Unterabschnitten beschriebenen Konfigurationen durchführen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-280">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="4bd1b-281">Die Konfiguration kann je nach den Details Ihrer Umgebung variieren.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-281">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="4bd1b-282">Sie besteht im Wesentlichen aus vier Teilen:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-282">It primarily includes four parts:</span></span>

- [<span data-ttu-id="4bd1b-283">Partitionierung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-283">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="4bd1b-284">Dimensions-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="4bd1b-284">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="4bd1b-285">Indizierung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-285">Indexing</span></span>](#indexing)
- [<span data-ttu-id="4bd1b-286">Benutzerdefinierte Messung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-286">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="4bd1b-287">Partitionierung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-287">Partitioning</span></span>

<span data-ttu-id="4bd1b-288">Die Partitionierung kann die Leistung der Inventory Visibility API erheblich beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-288">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="4bd1b-289">Es ist eine gute Idee, ein Schema zu definieren, das kleine Gruppierungen von Daten zulässt und trotzdem sinnvolle Datenabfragen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-289">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="4bd1b-290">Die `organizationId` (`dataAreaId` im Supply Chain Management) wird immer Teil der Partitionierung sein, und standardmäßig ist Inventory Visibility so festgelegt, dass es nach Dimensionen wie *Standort + Lagerplatz* partitioniert.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-290">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="4bd1b-291">Das bedeutet, dass der Dienst immer mit diesen in den Filtern definierten Dimensionen abgefragt werden muss.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-291">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="4bd1b-292">*Standort* und *Lagerplatz* sind zwei allgemeine Standarddimensionen in Inventory Visibility.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-292">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="4bd1b-293">Im Supply Chain Management heißen diese Dimensionen *Standort* (`InventSiteId`) und *Lagerort* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="4bd1b-293">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="4bd1b-294">Konfigurationen der Dimensionen</span><span class="sxs-lookup"><span data-stu-id="4bd1b-294">Dimension configurations</span></span>

<span data-ttu-id="4bd1b-295">Inventory Visibility stellt eine Liste allgemeiner Standarddimensionen zur Verfügung, um die Integration mehrerer Quellsysteme zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-295">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="4bd1b-296">In der folgenden Tabelle sind die Bestandsdimensionen aufgeführt, die als Standarddimensionen in Inventory Visibility verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-296">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="4bd1b-297">Dimensionstyp</span><span class="sxs-lookup"><span data-stu-id="4bd1b-297">Dimension type</span></span> | <span data-ttu-id="4bd1b-298">Dimensionsname</span><span class="sxs-lookup"><span data-stu-id="4bd1b-298">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="4bd1b-299">Produkt</span><span class="sxs-lookup"><span data-stu-id="4bd1b-299">Product</span></span> | `ColorId` |
| <span data-ttu-id="4bd1b-300">Produkt</span><span class="sxs-lookup"><span data-stu-id="4bd1b-300">Product</span></span> | `SizeId` |
| <span data-ttu-id="4bd1b-301">Produkt</span><span class="sxs-lookup"><span data-stu-id="4bd1b-301">Product</span></span> | `StyleId` |
| <span data-ttu-id="4bd1b-302">Produkt</span><span class="sxs-lookup"><span data-stu-id="4bd1b-302">Product</span></span> | `ConfigId` |
| <span data-ttu-id="4bd1b-303">Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-303">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="4bd1b-304">Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-304">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="4bd1b-305">Ziel</span><span class="sxs-lookup"><span data-stu-id="4bd1b-305">Location</span></span> | `LocationId` |
| <span data-ttu-id="4bd1b-306">Ziel</span><span class="sxs-lookup"><span data-stu-id="4bd1b-306">Location</span></span> | `SiteId` |
| <span data-ttu-id="4bd1b-307">Bestand Status</span><span class="sxs-lookup"><span data-stu-id="4bd1b-307">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="4bd1b-308">Lagerspezifisch</span><span class="sxs-lookup"><span data-stu-id="4bd1b-308">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="4bd1b-309">Lagerspezifisch</span><span class="sxs-lookup"><span data-stu-id="4bd1b-309">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="4bd1b-310">Lagerort-spezifisch</span><span class="sxs-lookup"><span data-stu-id="4bd1b-310">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="4bd1b-311">Der in der vorherigen Tabelle aufgeführte Dimensionstyp dient nur als Referenz.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-311">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="4bd1b-312">Sie müssen den Dimensionstyp nicht in Inventory Visibility definieren.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-312">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="4bd1b-313">Wenn eine benutzerdefinierte Dimension existiert und zu einem Standardwert fließen muss, wenn sie von Inventory Visibility konsumiert wird, können Sie den Namen **Benutzerdefinierte Dimension** in Inventory Visibility konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-313">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="4bd1b-314">Externe Systeme greifen auf Inventory Visibility über RESTful-APIs zu, mit denen Bestandsinformationen über festgelegte Dimensionen abgefragt werden können.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-314">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="4bd1b-315">Für die Integration können Sie in Inventory Visibility die *Externe Kanaldatenquelle* und die Quelldimension zu den *Zieldimensionen* konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-315">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="4bd1b-316">Die Zieldimensionen sollten eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-316">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="4bd1b-317">Standarddimensionen in Inventory Visibility</span><span class="sxs-lookup"><span data-stu-id="4bd1b-317">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="4bd1b-318">Benutzerdefinierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="4bd1b-318">Custom dimensions</span></span>

<span data-ttu-id="4bd1b-319">Der Zweck der Dimensionskonfiguration ist es, die Multisystem-Integration für die Abfrage auf Dimensionen und das Buchungsereignis mit Dimensionen zu standardisieren.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-319">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="4bd1b-320">Indizierung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-320">Indexing</span></span>

<span data-ttu-id="4bd1b-321">In den meisten Fällen wird die Bestandsabfrage nicht nur auf der höchsten „Gesamt“-Ebene erfolgen, sondern Sie möchten die Ergebnisse möglicherweise auf der Basis der Bestandsdimensionen aggregiert sehen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-321">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="4bd1b-322">Inventory Visibility bietet Flexibilität, indem es Ihnen erlaubt, die Indizes festzulegen, die auf der Dimension oder der Kombination der Dimensionen basieren.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-322">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="4bd1b-323">Derzeit können Sie nur Indizes bis maximal fünf konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-323">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="4bd1b-324">Sie müssen vor der Implementierung sorgfältig abwägen, welche Dimension oder Dimensionskombination Sie verwenden wollen, um sicherzustellen, dass sie Ihren geschäftlichen Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-324">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="4bd1b-325">Wenn Sie z. B. Produkte wie folgt abfragen wollen:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-325">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="4bd1b-326">Abfrage des aggregierten Produktbestandes nach den Dimensionen *Farbe* und *Größe*.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-326">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="4bd1b-327">In manchen Fällen wollen Sie nur das Produkt insgesamt abfragen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-327">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="4bd1b-328">Dann würden Sie zwei Indizes wie folgt definieren:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-328">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="4bd1b-329">Die leere Klammer wird auf Basis der Produkt-ID innerhalb der Partition aggregiert.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-329">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="4bd1b-330">Die Indizierung definiert, wie Sie Ihre Ergebnisse basierend auf der Abfrageeinstellung `groupBy` gruppieren können.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-330">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="4bd1b-331">Wenn Sie in diesem Fall keine `groupBy`-Werte definieren, erhalten Sie Summen nach `productid`.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-331">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="4bd1b-332">Andernfalls, wenn Sie `groupBy` als `groupBy=ColorId&groupBy=SizeId` definieren, erhalten Sie mehrere Zeilen zurück, basierend auf den verschiedenen Farb- und Größenkombinationen im System.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-332">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="4bd1b-333">Sie können Ihre Abfragekriterien in den Abfragekörper einlagern.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-333">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="4bd1b-334">Hier ist eine Beispielabfrage für das Produkt mit Farb- und Größenkombination.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-334">Here is a sample query on the product with color and size combination.</span></span>

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

<span data-ttu-id="4bd1b-335">Für das Feld `filters` unterstützt derzeit nur `ProductId` mehrere Werte.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-335">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="4bd1b-336">Wenn die `ProductId` ein leeres Array ist, werden alle Produkte abgefragt.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-336">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="4bd1b-337">Benutzerdefinierte Messung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-337">Custom measurement</span></span>

<span data-ttu-id="4bd1b-338">Die voreingestellten Messungen sind mit dem Supply Chain Management verknüpft.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-338">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="4bd1b-339">Möglicherweise möchten Sie jedoch eine Menge haben, die sich aus einer Kombination der Standard Messungen zusammensetzt.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-339">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="4bd1b-340">Dazu können Sie eine Konfiguration von benutzerdefinierten Mengen haben, die zur Ausgabe der Bestandsabfragen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-340">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="4bd1b-341">Die Funktionalität erlaubt es Ihnen einfach, eine Reihe von Kennzahlen festzulegen, die addiert werden, und/oder eine Reihe von Kennzahlen, die subtrahiert werden, um die benutzerdefinierte Messung zu bilden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-341">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="4bd1b-342">Mit der folgenden Abfragebedingung konfigurieren Sie zum Beispiel die benutzerdefinierte Messung als `MyCustomAvailableforReservation`, die vom Verbrauchssystem verbraucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-342">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="4bd1b-343">Verbrauchs-System</span><span class="sxs-lookup"><span data-stu-id="4bd1b-343">Consumption system</span></span> | <span data-ttu-id="4bd1b-344">Berechnete Kennzahlen</span><span class="sxs-lookup"><span data-stu-id="4bd1b-344">Calculated measurers</span></span> | <span data-ttu-id="4bd1b-345">Datenquelle</span><span class="sxs-lookup"><span data-stu-id="4bd1b-345">Data source</span></span> | <span data-ttu-id="4bd1b-346">Modifikator</span><span class="sxs-lookup"><span data-stu-id="4bd1b-346">Modifier</span></span> | <span data-ttu-id="4bd1b-347">Modifikator Berechnungsart</span><span class="sxs-lookup"><span data-stu-id="4bd1b-347">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="4bd1b-348">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-348">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="4bd1b-349">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-349">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="4bd1b-350">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="4bd1b-350">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="4bd1b-351">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-351">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="4bd1b-352">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="4bd1b-352">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="4bd1b-353">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-353">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="4bd1b-354">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-354">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="4bd1b-355">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="4bd1b-355">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="4bd1b-356">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="4bd1b-356">Subtraction</span></span> |

<span data-ttu-id="4bd1b-357">Damit wird die Abfrage auf die benutzerdefinierte Messung Menge die folgende Ausgabe zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-357">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="4bd1b-358">Die Ausgabe `MyCustomAvailableforReservation` basiert auf der Berechnungseinstellung in den benutzerdefinierten Messungen als:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-358">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="4bd1b-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="4bd1b-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="4bd1b-360">Verbuchung von Vorratsänderungen</span><span class="sxs-lookup"><span data-stu-id="4bd1b-360">Posting on-hand changes</span></span>

<span data-ttu-id="4bd1b-361">Die genaue URL, unter der das Ereignis gepostet wird, hängt von Ihrer geografischen Region ab.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-361">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="4bd1b-362">Sie wird die Form haben:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-362">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="4bd1b-363">Wenn Sie authentifiziert sind, kann diese URL zusammen mit der HTTP-Methode `POST` verwendet werden, um Ereignisse zu senden, die von Hand geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-363">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="4bd1b-364">Für die Kommunikation mit Dynamics 365-Diensten über HTTP-Anfragen wird ein spezieller Header verwendet, der die Umgebungs-ID der Supply Chain Management-Instanz angibt, mit der die Daten verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-364">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="4bd1b-365">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-365">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="4bd1b-366">Buchen von On-Hand-Änderungen Abfragebeispiel 1</span><span class="sxs-lookup"><span data-stu-id="4bd1b-366">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="4bd1b-367">Dieses Beispiel zeigt ein Szenario, in dem Sie die Konfiguration der Dimension in Power Apps festlegen werden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-367">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="4bd1b-368">Verwenden Sie die folgende Abfrage, um die Zuordnung der Dimension in Power Apps zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-368">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="4bd1b-369">Jetzt können Sie die `dimensionDataSource` angeben und benutzerdefinierte Dimensionen in Ihren Abfragen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-369">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="4bd1b-370">Das System wird die benutzerdefinierten Dimensionen automatisch in Basisdimensionen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-370">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="4bd1b-371">Buchen von Bestandsänderungen Abfragebeispiel 2</span><span class="sxs-lookup"><span data-stu-id="4bd1b-371">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="4bd1b-372">Dieses Beispiel zeigt ein Szenario, in dem keine Zuordnungen für die Dimensionskonfiguration in Power Apps festgelegt sind, sodass die Buchung auch die Basisdimensionen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-372">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="4bd1b-373">Alle Dimensionen müssen Basisdimensionen sein, wenn das Feld `dimensionDataSource` null, leer oder ein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-373">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="4bd1b-374">JSON-Dokument-Feldeigenschaften</span><span class="sxs-lookup"><span data-stu-id="4bd1b-374">JSON document field properties</span></span>

<span data-ttu-id="4bd1b-375">Die Felder aus den zuvor angegebenen JSON-Abfragebeispielen haben die in der folgenden Tabelle aufgeführten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-375">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="4bd1b-376">Feldkennung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-376">Field ID</span></span> | <span data-ttu-id="4bd1b-377">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bd1b-377">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="4bd1b-378">Eine eindeutige ID für das spezifische Änderungsereignis.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-378">A unique ID for the specific change event.</span></span> <span data-ttu-id="4bd1b-379">Diese ID wird verwendet, um sicherzustellen, dass, wenn die Kommunikation mit dem Dienst während der Buchung fehlschlägt, ein erneutes Einreichen des Ereignisses nicht dazu führt, dass dasselbe Ereignis im System doppelt gezählt wird.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-379">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="4bd1b-380">Die Kennung der Organisation, die mit dem Ereignis verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-380">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="4bd1b-381">Dies entspricht der Zuordnung zu Supply Chain Management-Organisationen oder Datenbereichs-IDs.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-381">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="4bd1b-382">Die Kennung des betreffenden Produkts.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-382">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="4bd1b-383">Die Menge, um die der Lagerbestand geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-383">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="4bd1b-384">Wenn z.B. 10 neue Bagels in ein Regal gestellt wurden, wäre dieser Wert 10.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-384">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="4bd1b-385">Wenn dann 3 Bagels aus dem Regal entfernt oder verkauft würden, wäre dieser Wert -3.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-385">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="4bd1b-386">Die Datenquelle der Dimensionen, die im Umbuchungsereignis und in der Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-386">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="4bd1b-387">Wenn Sie die Datenquelle angeben, können Sie die benutzerdefinierten Dimensionen aus der angegebenen Datenquelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-387">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="4bd1b-388">Mit der Dimensionskonfiguration kann Inventory Visibility die benutzerdefinierten Dimensionen den allgemeinen Standarddimensionen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-388">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="4bd1b-389">Wenn die `dimensionDataSource` nicht angegeben wird, können Sie nur die allgemeinen Standarddimensionen in Ihren Abfragen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-389">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="4bd1b-390">Eine dynamische Tasche mit Schlüssel/Wertpaaren.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-390">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="4bd1b-391">Diese werden einigen der Dimensionen im Supply Chain Management zugeordnet, aber Sie können auch benutzerdefinierte Dimensionen hinzufügen (wie *Quelle*), die angeben, ob das Ereignis aus dem Supply Chain Management oder einem externen System stammt.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-391">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="4bd1b-392">Abfrage des aktuellen Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="4bd1b-392">Querying current on-hand</span></span>

<span data-ttu-id="4bd1b-393">Der Endpunkt für die Abfrage des aktuellen Lagerbestands wird eine ähnliche URL haben:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-393">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="4bd1b-394">Er wird mit der HTTP-Methode `POST` abgefragt.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-394">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="4bd1b-395">Abfrage des aktuellen Lagerbestands Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4bd1b-395">Current on-hand query example 1</span></span>

<span data-ttu-id="4bd1b-396">Dieses Beispiel zeigt ein Szenario, bei dem Sie die Konfiguration der Dimension in Power Apps bereits abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-396">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="4bd1b-397">Verwenden Sie die folgende Abfrage, um die Zuordnung der Dimension in Power Apps zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="4bd1b-397">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="4bd1b-398">Jetzt können Sie die `dimensionDataSource` angeben und benutzerdefinierte Dimensionen in Ihren Abfragen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-398">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="4bd1b-399">Das System wird die benutzerdefinierten Dimensionen automatisch in Basisdimensionen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-399">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="4bd1b-400">Sie können die `DimensionDataSource` in `filters` angeben und benutzerdefinierte Dimensionen sowohl in `filters` als auch in `groupByValues` angeben.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-400">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="4bd1b-401">Das System wird die benutzerdefinierten Dimensionen automatisch in Basisdimensionen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-401">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="4bd1b-402">Aktuelle Bestandsabfrage Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4bd1b-402">Current on-hand query example 2</span></span>

<span data-ttu-id="4bd1b-403">Dieses Beispiel zeigt ein Szenario, in dem keine Zuordnungen für die Dimensionskonfiguration in Power Apps festgelegt sind, sodass die Buchung auch die Basisdimensionen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-403">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="4bd1b-404">Alle Dimensionen müssen Basisdimensionen sein, wenn das Feld `dimensionDataSource` unter `filters` null, leer oder ein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-404">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="4bd1b-405">Beispiel Rückgabeergebnis</span><span class="sxs-lookup"><span data-stu-id="4bd1b-405">Example return result</span></span>

<span data-ttu-id="4bd1b-406">Die in den vorherigen Beispielen gezeigten Abfragen könnten ein Ergebnis wie dieses zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-406">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="4bd1b-407">Beachten Sie, dass die Mengen-Felder als ein Wörterbuch von Kennzahlen und ihren zugehörigen Werten strukturiert sind.</span><span class="sxs-lookup"><span data-stu-id="4bd1b-407">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]