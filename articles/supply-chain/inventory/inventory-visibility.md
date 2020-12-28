---
title: Inventory Visibility Add-In
description: In diesem Thema wird beschrieben, wie Sie das Inventory Visibility Add-in für Dynamics 365 Supply Chain Management installieren und konfigurieren.
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625064"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="0bd19-103">Inventory Visibility Add-in</span><span class="sxs-lookup"><span data-stu-id="0bd19-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="0bd19-104">Das Inventory Visibility Add-in ist ein unabhängiger und hoch skalierbarer Microservice, der die Verfolgung von Beständen in Echtzeit ermöglicht und so eine globale Sicht auf den Bestand bietet.</span><span class="sxs-lookup"><span data-stu-id="0bd19-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="0bd19-105">Alle Informationen, die sich auf den Bestand beziehen, werden durch Low-Level-SQL-Integration nahezu in Echtzeit an den Dienst exportiert.</span><span class="sxs-lookup"><span data-stu-id="0bd19-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="0bd19-106">Externe Systeme greifen über RESTful APIs auf den Dienst zu, um Bestandsinformationen über festgelegte Dimensionen abzufragen und so eine Liste der verfügbaren Bestandspositionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0bd19-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="0bd19-107">Inventory Visibility ist ein Microservice, der auf der Common Data Service aufbaut, d.h. Sie können ihn mit der Power Apps erweitern und mit der Power BI kundenspezifische Funktionen bereitstellen, um Ihre Geschäftsanforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-107">Inventory Visibility is a microservice built on the Common Data Service, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="0bd19-108">Es ist auch möglich, den Index zu erweitern, um Bestandsabfragen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="0bd19-109">Inventory Visibility bietet Konfigurationsoptionen, mit denen es sich in mehrere Drittsysteme integrieren lässt.</span><span class="sxs-lookup"><span data-stu-id="0bd19-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="0bd19-110">Es unterstützt die standardisierte Dimension des Bestands, benutzerdefinierte Erweiterbarkeit und standardisierte, konfigurierbare berechnete Mengen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="0bd19-111">In diesem Thema wird beschrieben, wie Sie das Inventory Visibility Add-In für Dynamics 365 Supply Chain Management installieren und konfigurieren und wie Sie seine Anwendungsprogrammierschnittstelle (API) verwenden.</span><span class="sxs-lookup"><span data-stu-id="0bd19-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="0bd19-112">Installieren Sie das Inventory Visibility Add-In</span><span class="sxs-lookup"><span data-stu-id="0bd19-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="0bd19-113">Sie müssen das Inventory Visibility Add-In über Microsoft Dynamics Lifecycle Services (LCS) installieren.</span><span class="sxs-lookup"><span data-stu-id="0bd19-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0bd19-114">LCS ist ein Portal für die Zusammenarbeit, das eine Umgebung und eine Reihe von regelmäßig aktualisierten Diensten bereitstellt, die Sie bei der Verwaltung des Lebenszyklus Ihrer Dynamics 365 Finance and Operations-Apps unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="0bd19-115">Weitere Informationen finden Sie unter [Ressourcen für Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="0bd19-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0bd19-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="0bd19-116">Prerequisites</span></span>

<span data-ttu-id="0bd19-117">Bevor Sie das Inventory Visibility Add-In installieren, müssen Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="0bd19-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="0bd19-118">Besorgen Sie sich ein LCS-Implementierungsprojekt mit mindestens einer bereitgestellten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0bd19-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="0bd19-119">Erzeugen Sie die Beta-Schlüssel für Ihr Angebot in LCS.</span><span class="sxs-lookup"><span data-stu-id="0bd19-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="0bd19-120">Aktivieren Sie die Betaschlüssel für Ihr Angebot für Ihren Benutzer in LCS.</span><span class="sxs-lookup"><span data-stu-id="0bd19-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="0bd19-121">Wenden Sie sich an das Microsoft Inventory Visibility-Produktteam und geben Sie eine Umgebungs-ID an, in der Sie das Inventory Visibility-Add-In bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="0bd19-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="0bd19-122">Wenn Sie Fragen zu diesen Voraussetzungen haben, wenden Sie sich bitte an das Inventory Visibility-Produktteam.</span><span class="sxs-lookup"><span data-stu-id="0bd19-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="0bd19-123">Installieren des Add-Ins</span><span class="sxs-lookup"><span data-stu-id="0bd19-123">Install the add-in</span></span>

<span data-ttu-id="0bd19-124">Um das Inventory Visibility Add-In zu installieren, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="0bd19-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="0bd19-125">Melden Sie sich am [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) Portal an.</span><span class="sxs-lookup"><span data-stu-id="0bd19-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="0bd19-126">Wählen Sie auf der Startseite das Projekt aus, in dem Ihre Umgebung bereitgestellt ist.</span><span class="sxs-lookup"><span data-stu-id="0bd19-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="0bd19-127">Wählen Sie auf der Projektseite die Umgebung aus, in der Sie das Add-In installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0bd19-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="0bd19-128">Scrollen Sie auf der Seite der Umgebung nach unten, bis Sie den Abschnitt **Umgebungs-Add-Ins** sehen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="0bd19-129">Wenn der Abschnitt nicht sichtbar ist, stellen Sie sicher, dass die vorausgesetzten Beta-Schlüssel vollständig verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="0bd19-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="0bd19-130">Wählen Sie im Abschnitt **Umgebungs-Add-Ins** die Option **Ein neues Add-In installieren**.</span><span class="sxs-lookup"><span data-stu-id="0bd19-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="0bd19-131">![Die Umgebungsseite in LCS](media/inventory-visibility-environment.png "Die Seite „Umgebung“ in LCS")</span><span class="sxs-lookup"><span data-stu-id="0bd19-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="0bd19-132">Wählen Sie den Link **Ein neues Add-In installieren**.</span><span class="sxs-lookup"><span data-stu-id="0bd19-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="0bd19-133">Es öffnet sich eine Liste der verfügbaren Add-Ins.</span><span class="sxs-lookup"><span data-stu-id="0bd19-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="0bd19-134">Wählen Sie **Bestandsdienst** aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="0bd19-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="0bd19-135">(Beachten Sie, dass dies jetzt möglicherweise als **Add-In Inventory Visibility für Dynamics 365 Supply Chain Management** aufgeführt wird).</span><span class="sxs-lookup"><span data-stu-id="0bd19-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="0bd19-136">Geben Sie Werte für die folgenden Felder für Ihre Umgebung ein:</span><span class="sxs-lookup"><span data-stu-id="0bd19-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="0bd19-137">**AAD-Anwendungs-ID**</span><span class="sxs-lookup"><span data-stu-id="0bd19-137">**AAD application ID**</span></span>
    - <span data-ttu-id="0bd19-138">**AAD-Mandanten-ID**</span><span class="sxs-lookup"><span data-stu-id="0bd19-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="0bd19-139">![Einrichtungsseite hinzufügen](media/inventory-visibility-setup.png "Seite zum Einrichten des Add-Ins")</span><span class="sxs-lookup"><span data-stu-id="0bd19-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="0bd19-140">Stimmen Sie den Bedingungen zu, indem Sie das Kontrollkästchen **Bedingungen und Konditionen** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0bd19-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="0bd19-141">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="0bd19-141">Select **Install**.</span></span> <span data-ttu-id="0bd19-142">Der Status des Add-Ins wird als **Installation** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0bd19-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="0bd19-143">Wenn es fertig ist, aktualisieren Sie die Seite, um den Status auf **Installiert** zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0bd19-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="0bd19-144">Abrufen eines Sicherheitsdienst-Tokens</span><span class="sxs-lookup"><span data-stu-id="0bd19-144">Get a security service token</span></span>

<span data-ttu-id="0bd19-145">Um ein Sicherheitsdienst-Token zu erhalten, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="0bd19-145">To get a security service token, do the following:</span></span>

1. <span data-ttu-id="0bd19-146">Holen Sie sich Ihre `aadToken` und rufen Sie den Endpunkt: https://securityservice.operations365.dynamics.com/token auf.</span><span class="sxs-lookup"><span data-stu-id="0bd19-146">Get your `aadToken` and call the endpoint: https://securityservice.operations365.dynamics.com/token.</span></span>
1. <span data-ttu-id="0bd19-147">Ersetzen Sie die `client_assertion` im Body durch Ihre `aadToken`.</span><span class="sxs-lookup"><span data-stu-id="0bd19-147">Replace the `client_assertion` in the body with your `aadToken`.</span></span>
1. <span data-ttu-id="0bd19-148">Ersetzen Sie den Kontext im Body durch die Umgebung, in der Sie das Add-In bereitstellen wollen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-148">Replace the context in the body with the environment where you want to deploy the add-in.</span></span>
1. <span data-ttu-id="0bd19-149">Ersetzen Sie den Bereich im Body durch den folgenden:</span><span class="sxs-lookup"><span data-stu-id="0bd19-149">Replace the scope in the body with the following:</span></span>

    - <span data-ttu-id="0bd19-150">Bereich für MCK - „https://inventoryservice.operations365.dynamics.cn/.default“</span><span class="sxs-lookup"><span data-stu-id="0bd19-150">Scope for MCK - "https://inventoryservice.operations365.dynamics.cn/.default"</span></span>  
    <span data-ttu-id="0bd19-151">(Die Anwendungs-ID Azure Active Directory und die Mandant-ID für MCK finden Sie in `appsettings.mck.json`.)</span><span class="sxs-lookup"><span data-stu-id="0bd19-151">(You can find the Azure Active Directory application ID and tenant ID for MCK in `appsettings.mck.json`.)</span></span>
    - <span data-ttu-id="0bd19-152">Geltungsbereich für PROD - „https://inventoryservice.operations365.dynamics.com/.default“</span><span class="sxs-lookup"><span data-stu-id="0bd19-152">Scope for PROD - "https://inventoryservice.operations365.dynamics.com/.default"</span></span>  
    <span data-ttu-id="0bd19-153">(Die Azure Active Directory Anwendungs-ID und Mandanten-ID für PROD finden Sie in `appsettings.prod.json`.)</span><span class="sxs-lookup"><span data-stu-id="0bd19-153">(You can find the Azure Active Directory application ID and tenant ID for PROD in `appsettings.prod.json`.)</span></span>

    <span data-ttu-id="0bd19-154">Das Ergebnis sollte dem folgenden Beispiel ähneln.</span><span class="sxs-lookup"><span data-stu-id="0bd19-154">The result should resemble the following example.</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. <span data-ttu-id="0bd19-155">Sie werden eine `access_token` als Antwort erhalten.</span><span class="sxs-lookup"><span data-stu-id="0bd19-155">You will get an `access_token` in response.</span></span> <span data-ttu-id="0bd19-156">Diese benötigen Sie als Inhaber-Token, um die Inventory Visibility API aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-156">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="0bd19-157">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="0bd19-157">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="0bd19-158">Add-In deinstallieren</span><span class="sxs-lookup"><span data-stu-id="0bd19-158">Uninstall the add-in</span></span>

<span data-ttu-id="0bd19-159">Um das Add-In zu deinstallieren, wählen Sie **Deinstallieren**.</span><span class="sxs-lookup"><span data-stu-id="0bd19-159">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="0bd19-160">Aktualisieren Sie LCS und das Inventory Visibility Add-in wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="0bd19-160">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="0bd19-161">Der Deinstallationsprozess entfernt die Registrierung des Add-Ins und startet außerdem einen Job zum Bereinigen aller im Dienst gespeicherten Geschäftsdaten.</span><span class="sxs-lookup"><span data-stu-id="0bd19-161">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="0bd19-162">Öffentliches API des Inventory Visibility Add-Ins</span><span class="sxs-lookup"><span data-stu-id="0bd19-162">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="0bd19-163">Die öffentliche REST-API des Inventory Visibility Add-Ins bietet mehrere spezifische Endpunkte für die Integration.</span><span class="sxs-lookup"><span data-stu-id="0bd19-163">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="0bd19-164">Sie unterstützt drei Hauptinteraktionstypen:</span><span class="sxs-lookup"><span data-stu-id="0bd19-164">It supports three main interaction types:</span></span>

- <span data-ttu-id="0bd19-165">Buchen von Bestandsänderungen an das Add-In aus einem externen System.</span><span class="sxs-lookup"><span data-stu-id="0bd19-165">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="0bd19-166">Abfrage von aktuellen Bestandsmengen aus einem externen System.</span><span class="sxs-lookup"><span data-stu-id="0bd19-166">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="0bd19-167">Automatische Synchronisation mit dem Supply Chain Management-Bestand.</span><span class="sxs-lookup"><span data-stu-id="0bd19-167">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="0bd19-168">Die automatische Synchronisation ist nicht Teil der öffentlichen API, sondern wird für Umgebungen, die das Inventory Visibility Add-in aktiviert haben, im Hintergrund ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0bd19-168">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="0bd19-169">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="0bd19-169">Authentication</span></span>

<span data-ttu-id="0bd19-170">Das Plattform-Sicherheits-Token wird verwendet, um das Inventory Visibility Add-in aufzurufen, daher müssen Sie ein Azure Active Directory-Token mit Ihrer Azure Active Directory-Anwendung erzeugen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-170">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="0bd19-171">Weitere Informationen darüber, wie Sie das Sicherheitstoken erhalten, finden Sie unter [Installieren des Inventory Visibility Add-Ins](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="0bd19-171">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="0bd19-172">Konfigurieren Sie die Inventory Visibility API</span><span class="sxs-lookup"><span data-stu-id="0bd19-172">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="0bd19-173">Bevor Sie den Dienst verwenden, müssen Sie die in den folgenden Unterabschnitten beschriebenen Konfigurationen durchführen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-173">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="0bd19-174">Die Konfiguration kann je nach den Details Ihrer Umgebung variieren.</span><span class="sxs-lookup"><span data-stu-id="0bd19-174">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="0bd19-175">Sie besteht im Wesentlichen aus vier Teilen:</span><span class="sxs-lookup"><span data-stu-id="0bd19-175">It primarily includes four parts:</span></span>

- [<span data-ttu-id="0bd19-176">Partitionierung</span><span class="sxs-lookup"><span data-stu-id="0bd19-176">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="0bd19-177">Dimensions-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="0bd19-177">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="0bd19-178">Indizierung</span><span class="sxs-lookup"><span data-stu-id="0bd19-178">Indexing</span></span>](#indexing)
- [<span data-ttu-id="0bd19-179">Benutzerdefinierte Messung</span><span class="sxs-lookup"><span data-stu-id="0bd19-179">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="0bd19-180">Partitionierung</span><span class="sxs-lookup"><span data-stu-id="0bd19-180">Partitioning</span></span>

<span data-ttu-id="0bd19-181">Die Partitionierung kann die Leistung der Inventory Visibility API erheblich beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-181">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="0bd19-182">Es ist eine gute Idee, ein Schema zu definieren, das kleine Gruppierungen von Daten zulässt und trotzdem sinnvolle Datenabfragen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="0bd19-182">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="0bd19-183">Die `organizationId` (`dataAreaId` im Supply Chain Management) wird immer Teil der Partitionierung sein, und standardmäßig ist Inventory Visibility so festgelegt, dass es nach Dimensionen wie *Standort + Lagerplatz* partitioniert.</span><span class="sxs-lookup"><span data-stu-id="0bd19-183">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="0bd19-184">Das bedeutet, dass der Dienst immer mit diesen in den Filtern definierten Dimensionen abgefragt werden muss.</span><span class="sxs-lookup"><span data-stu-id="0bd19-184">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="0bd19-185">*Standort* und *Lagerplatz* sind zwei allgemeine Standarddimensionen in Inventory Visibility.</span><span class="sxs-lookup"><span data-stu-id="0bd19-185">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="0bd19-186">Im Supply Chain Management heißen diese Dimensionen *Standort* (`InventSiteId`) und *Lagerort* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="0bd19-186">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="0bd19-187">Konfigurationen der Dimensionen</span><span class="sxs-lookup"><span data-stu-id="0bd19-187">Dimension configurations</span></span>

<span data-ttu-id="0bd19-188">Inventory Visibility stellt eine Liste allgemeiner Standarddimensionen zur Verfügung, um die Integration mehrerer Quellsysteme zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-188">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="0bd19-189">In der folgenden Tabelle sind die Bestandsdimensionen aufgeführt, die als Standarddimensionen in Inventory Visibility verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bd19-189">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="0bd19-190">Dimensionstyp</span><span class="sxs-lookup"><span data-stu-id="0bd19-190">Dimension type</span></span> | <span data-ttu-id="0bd19-191">Dimensionsname</span><span class="sxs-lookup"><span data-stu-id="0bd19-191">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="0bd19-192">Produkt</span><span class="sxs-lookup"><span data-stu-id="0bd19-192">Product</span></span> | `ColorId` |
| <span data-ttu-id="0bd19-193">Produkt</span><span class="sxs-lookup"><span data-stu-id="0bd19-193">Product</span></span> | `SizeId` |
| <span data-ttu-id="0bd19-194">Produkt</span><span class="sxs-lookup"><span data-stu-id="0bd19-194">Product</span></span> | `StyleId` |
| <span data-ttu-id="0bd19-195">Produkt</span><span class="sxs-lookup"><span data-stu-id="0bd19-195">Product</span></span> | `ConfigId` |
| <span data-ttu-id="0bd19-196">Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="0bd19-196">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="0bd19-197">Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="0bd19-197">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="0bd19-198">Ziel</span><span class="sxs-lookup"><span data-stu-id="0bd19-198">Location</span></span> | `LocationId` |
| <span data-ttu-id="0bd19-199">Ziel</span><span class="sxs-lookup"><span data-stu-id="0bd19-199">Location</span></span> | `SiteId` |
| <span data-ttu-id="0bd19-200">Bestand Status</span><span class="sxs-lookup"><span data-stu-id="0bd19-200">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="0bd19-201">Lagerspezifisch</span><span class="sxs-lookup"><span data-stu-id="0bd19-201">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="0bd19-202">Lagerspezifisch</span><span class="sxs-lookup"><span data-stu-id="0bd19-202">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="0bd19-203">Lagerort-spezifisch</span><span class="sxs-lookup"><span data-stu-id="0bd19-203">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="0bd19-204">Der in der vorherigen Tabelle aufgeführte Dimensionstyp dient nur als Referenz.</span><span class="sxs-lookup"><span data-stu-id="0bd19-204">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="0bd19-205">Sie müssen den Dimensionstyp nicht in Inventory Visibility definieren.</span><span class="sxs-lookup"><span data-stu-id="0bd19-205">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="0bd19-206">Wenn eine benutzerdefinierte Dimension existiert und zu einem Standardwert fließen muss, wenn sie von Inventory Visibility konsumiert wird, können Sie den Namen **Benutzerdefinierte Dimension** in Inventory Visibility konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0bd19-206">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="0bd19-207">Externe Systeme greifen auf Inventory Visibility über RESTful-APIs zu, mit denen Bestandsinformationen über festgelegte Dimensionen abgefragt werden können.</span><span class="sxs-lookup"><span data-stu-id="0bd19-207">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="0bd19-208">Für die Integration können Sie in Inventory Visibility die *Externe Kanaldatenquelle* und die Quelldimension zu den *Zieldimensionen* konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0bd19-208">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="0bd19-209">Die Zieldimensionen sollten eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="0bd19-209">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="0bd19-210">Standarddimensionen in Inventory Visibility</span><span class="sxs-lookup"><span data-stu-id="0bd19-210">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="0bd19-211">Benutzerdefinierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="0bd19-211">Custom dimensions</span></span>

<span data-ttu-id="0bd19-212">Der Zweck der Dimensionskonfiguration ist es, die Multisystem-Integration für die Abfrage auf Dimensionen und das Buchungsereignis mit Dimensionen zu standardisieren.</span><span class="sxs-lookup"><span data-stu-id="0bd19-212">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="0bd19-213">Indizierung</span><span class="sxs-lookup"><span data-stu-id="0bd19-213">Indexing</span></span>

<span data-ttu-id="0bd19-214">In den meisten Fällen wird die Bestandsabfrage nicht nur auf der höchsten „Gesamt“-Ebene erfolgen, sondern Sie möchten die Ergebnisse möglicherweise auf der Basis der Bestandsdimensionen aggregiert sehen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-214">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="0bd19-215">Inventory Visibility bietet Flexibilität, indem es Ihnen erlaubt, die Indizes festzulegen, die auf der Dimension oder der Kombination der Dimensionen basieren.</span><span class="sxs-lookup"><span data-stu-id="0bd19-215">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="0bd19-216">Derzeit können Sie nur Indizes bis maximal fünf konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0bd19-216">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="0bd19-217">Sie müssen vor der Implementierung sorgfältig abwägen, welche Dimension oder Dimensionskombination Sie verwenden wollen, um sicherzustellen, dass sie Ihren geschäftlichen Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="0bd19-217">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="0bd19-218">Wenn Sie z. B. Produkte wie folgt abfragen wollen:</span><span class="sxs-lookup"><span data-stu-id="0bd19-218">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="0bd19-219">Abfrage des aggregierten Produktbestandes nach den Dimensionen *Farbe* und *Größe*.</span><span class="sxs-lookup"><span data-stu-id="0bd19-219">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="0bd19-220">In manchen Fällen wollen Sie nur das Produkt insgesamt abfragen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-220">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="0bd19-221">Dann würden Sie zwei Indizes wie folgt definieren:</span><span class="sxs-lookup"><span data-stu-id="0bd19-221">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="0bd19-222">Die leere Klammer wird auf Basis der Produkt-ID innerhalb der Partition aggregiert.</span><span class="sxs-lookup"><span data-stu-id="0bd19-222">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="0bd19-223">Die Indizierung definiert, wie Sie Ihre Ergebnisse basierend auf der Abfrageeinstellung `groupBy` gruppieren können.</span><span class="sxs-lookup"><span data-stu-id="0bd19-223">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="0bd19-224">Wenn Sie in diesem Fall keine `groupBy`-Werte definieren, erhalten Sie Summen nach `productid`.</span><span class="sxs-lookup"><span data-stu-id="0bd19-224">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="0bd19-225">Wenn Sie dagegen `groupBy` als `groupBy=ColorId&groupBy=SizeId` definieren, erhalten Sie mehrere Zeilen zurück, basierend auf den verschiedenen Farb- und Größenkombinationen im System.</span><span class="sxs-lookup"><span data-stu-id="0bd19-225">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="0bd19-226">Sie können Ihre Abfragekriterien in den Abfragekörper einlagern.</span><span class="sxs-lookup"><span data-stu-id="0bd19-226">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="0bd19-227">Hier ist eine Beispielabfrage für das Produkt mit Farb- und Größenkombination.</span><span class="sxs-lookup"><span data-stu-id="0bd19-227">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="0bd19-228">Benutzerdefinierte Messung</span><span class="sxs-lookup"><span data-stu-id="0bd19-228">Custom measurement</span></span>

<span data-ttu-id="0bd19-229">Die voreingestellten Messungen sind mit dem Supply Chain Management verknüpft, aber Sie möchten vielleicht eine Menge haben, die sich aus einer Kombination der voreingestellten Kennzahlen zusammensetzt.</span><span class="sxs-lookup"><span data-stu-id="0bd19-229">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="0bd19-230">Dazu können Sie eine Konfiguration von benutzerdefinierten Mengen haben, die zur Ausgabe der Bestandsabfragen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0bd19-230">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="0bd19-231">Die Funktionalität erlaubt es Ihnen einfach, eine Reihe von Kennzahlen festzulegen, die addiert werden, und/oder eine Reihe von Kennzahlen, die subtrahiert werden, um die benutzerdefinierte Messung zu bilden.</span><span class="sxs-lookup"><span data-stu-id="0bd19-231">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="0bd19-232">Mit der folgenden Abfragebedingung konfigurieren Sie zum Beispiel die benutzerdefinierte Messung als `MyCustomAvailableforReservation`, die vom Verbrauchssystem verbraucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="0bd19-232">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="0bd19-233">Verbrauchs-System</span><span class="sxs-lookup"><span data-stu-id="0bd19-233">Consumption system</span></span> | <span data-ttu-id="0bd19-234">Berechnete Kennzahlen</span><span class="sxs-lookup"><span data-stu-id="0bd19-234">Calculated measurers</span></span> | <span data-ttu-id="0bd19-235">Datenquelle</span><span class="sxs-lookup"><span data-stu-id="0bd19-235">Data source</span></span> | <span data-ttu-id="0bd19-236">Modifikator</span><span class="sxs-lookup"><span data-stu-id="0bd19-236">Modifier</span></span> | <span data-ttu-id="0bd19-237">Modifikator Berechnungsart</span><span class="sxs-lookup"><span data-stu-id="0bd19-237">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="0bd19-238">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="0bd19-238">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="0bd19-239">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="0bd19-239">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="0bd19-240">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="0bd19-240">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="0bd19-241">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="0bd19-241">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="0bd19-242">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="0bd19-242">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="0bd19-243">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="0bd19-243">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="0bd19-244">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="0bd19-244">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="0bd19-245">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="0bd19-245">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="0bd19-246">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="0bd19-246">Subtraction</span></span> |

<span data-ttu-id="0bd19-247">Damit wird die Abfrage auf die benutzerdefinierte Messung Menge die folgende Ausgabe zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0bd19-247">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="0bd19-248">Die Ausgabe `MyCustomAvailableforReservation` basiert auf der Berechnungseinstellung in den benutzerdefinierten Messungen als:</span><span class="sxs-lookup"><span data-stu-id="0bd19-248">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="0bd19-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="0bd19-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="0bd19-250">Verbuchung von Vorratsänderungen</span><span class="sxs-lookup"><span data-stu-id="0bd19-250">Posting on-hand changes</span></span>

<span data-ttu-id="0bd19-251">Die genaue URL, unter der das Ereignis gepostet wird, hängt von Ihrer geografischen Region ab.</span><span class="sxs-lookup"><span data-stu-id="0bd19-251">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="0bd19-252">Sie wird die Form haben:</span><span class="sxs-lookup"><span data-stu-id="0bd19-252">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="0bd19-253">Wenn Sie authentifiziert sind, kann diese URL zusammen mit der HTTP-Methode `POST` verwendet werden, um Ereignisse zu senden, die von Hand geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0bd19-253">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="0bd19-254">Für die Kommunikation mit Dynamics 365-Diensten über HTTP-Anfragen wird ein spezieller Header verwendet, der die Umgebungs-ID der Supply Chain Management-Instanz angibt, mit der die Daten verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="0bd19-254">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="0bd19-255">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0bd19-255">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="0bd19-256">Buchen von On-Hand-Änderungen Abfragebeispiel 1</span><span class="sxs-lookup"><span data-stu-id="0bd19-256">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="0bd19-257">Dieses Beispiel zeigt ein Szenario, in dem Sie die Konfiguration der Dimension in Power Apps festlegen werden.</span><span class="sxs-lookup"><span data-stu-id="0bd19-257">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="0bd19-258">Verwenden Sie die folgende Abfrage, um die Zuordnung der Dimension in Power Apps zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="0bd19-258">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="0bd19-259">Jetzt können Sie die `dimensionDataSource` angeben und benutzerdefinierte Dimensionen in Ihren Abfragen verwenden.</span><span class="sxs-lookup"><span data-stu-id="0bd19-259">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="0bd19-260">Das System wird die benutzerdefinierten Dimensionen automatisch in Basisdimensionen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="0bd19-260">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="0bd19-261">Buchen von Bestandsänderungen Abfragebeispiel 2</span><span class="sxs-lookup"><span data-stu-id="0bd19-261">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="0bd19-262">Dieses Beispiel zeigt ein Szenario, in dem keine Zuordnungen für die Dimensionskonfiguration in Power Apps festgelegt sind, sodass die Buchung auch die Basisdimensionen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="0bd19-262">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="0bd19-263">Alle Dimensionen müssen Basisdimensionen sein, wenn das Feld `dimensionDataSource` null, leer oder ein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="0bd19-263">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="0bd19-264">JSON-Dokument-Feldeigenschaften</span><span class="sxs-lookup"><span data-stu-id="0bd19-264">JSON document field properties</span></span>

<span data-ttu-id="0bd19-265">Die Felder aus den zuvor angegebenen JSON-Abfragebeispielen haben die in der folgenden Tabelle aufgeführten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0bd19-265">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="0bd19-266">Feldkennung</span><span class="sxs-lookup"><span data-stu-id="0bd19-266">Field ID</span></span> | <span data-ttu-id="0bd19-267">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0bd19-267">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="0bd19-268">Eine eindeutige ID für das spezifische Änderungsereignis.</span><span class="sxs-lookup"><span data-stu-id="0bd19-268">A unique ID for the specific change event.</span></span> <span data-ttu-id="0bd19-269">Diese ID wird verwendet, um sicherzustellen, dass, wenn die Kommunikation mit dem Dienst während der Buchung fehlschlägt, ein erneutes Einreichen des Ereignisses nicht dazu führt, dass dasselbe Ereignis im System doppelt gezählt wird.</span><span class="sxs-lookup"><span data-stu-id="0bd19-269">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="0bd19-270">Die Kennung der Organisation, die mit dem Ereignis verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="0bd19-270">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="0bd19-271">Dies entspricht der Zuordnung zu Supply Chain Management-Organisationen oder Datenbereichs-IDs.</span><span class="sxs-lookup"><span data-stu-id="0bd19-271">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="0bd19-272">Die Kennung des betreffenden Produkts.</span><span class="sxs-lookup"><span data-stu-id="0bd19-272">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="0bd19-273">Die Menge, um die der Lagerbestand geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="0bd19-273">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="0bd19-274">Wenn z.B. 10 neue Bagels in ein Regal gestellt wurden, wäre dieser Wert 10.</span><span class="sxs-lookup"><span data-stu-id="0bd19-274">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="0bd19-275">Wenn dann 3 Bagels aus dem Regal entfernt oder verkauft würden, wäre dieser Wert -3.</span><span class="sxs-lookup"><span data-stu-id="0bd19-275">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="0bd19-276">Die Datenquelle der Dimensionen, die im Umbuchungsereignis und in der Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bd19-276">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="0bd19-277">Wenn Sie die Datenquelle angeben, können Sie die benutzerdefinierten Dimensionen aus der angegebenen Datenquelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="0bd19-277">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="0bd19-278">Mit der Dimensionskonfiguration kann Inventory Visibility die benutzerdefinierten Dimensionen den allgemeinen Standarddimensionen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="0bd19-278">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="0bd19-279">Wenn die `dimensionDataSource` nicht angegeben wird, können Sie nur die allgemeinen Standarddimensionen in Ihren Abfragen verwenden.</span><span class="sxs-lookup"><span data-stu-id="0bd19-279">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="0bd19-280">Eine dynamische Tasche mit Schlüssel/Wertpaaren.</span><span class="sxs-lookup"><span data-stu-id="0bd19-280">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="0bd19-281">Diese werden einigen der Dimensionen im Supply Chain Management zugeordnet, aber Sie können auch benutzerdefinierte Dimensionen hinzufügen (wie *Quelle*), die angeben, ob das Ereignis aus dem Supply Chain Management oder einem externen System stammt.</span><span class="sxs-lookup"><span data-stu-id="0bd19-281">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="0bd19-282">Abfrage des aktuellen Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="0bd19-282">Querying current on-hand</span></span>

<span data-ttu-id="0bd19-283">Der Endpunkt für die Abfrage des aktuellen Lagerbestands wird eine ähnliche URL haben:</span><span class="sxs-lookup"><span data-stu-id="0bd19-283">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="0bd19-284">Er wird mit der HTTP-Methode `POST` abgefragt.</span><span class="sxs-lookup"><span data-stu-id="0bd19-284">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="0bd19-285">Abfrage des aktuellen Lagerbestands Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0bd19-285">Current on-hand query example 1</span></span>

<span data-ttu-id="0bd19-286">Dieses Beispiel zeigt ein Szenario, bei dem Sie die Konfiguration der Dimension in Power Apps bereits abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="0bd19-286">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="0bd19-287">Verwenden Sie die folgende Abfrage, um die Zuordnung der Dimension in Power Apps zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="0bd19-287">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="0bd19-288">Jetzt können Sie die `dimensionDataSource` angeben und benutzerdefinierte Dimensionen in Ihren Abfragen verwenden.</span><span class="sxs-lookup"><span data-stu-id="0bd19-288">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="0bd19-289">Das System wird die benutzerdefinierten Dimensionen automatisch in Basisdimensionen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="0bd19-289">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="0bd19-290">Sie können die `DimensionDataSource` in `filters` angeben und benutzerdefinierte Dimensionen sowohl in `filters` als auch in `groupByValues` angeben.</span><span class="sxs-lookup"><span data-stu-id="0bd19-290">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="0bd19-291">Das System wird die benutzerdefinierten Dimensionen automatisch in Basisdimensionen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="0bd19-291">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="0bd19-292">Aktuelle Bestandsabfrage Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0bd19-292">Current on-hand query example 2</span></span>

<span data-ttu-id="0bd19-293">Dieses Beispiel zeigt ein Szenario, in dem keine Zuordnungen für die Dimensionskonfiguration in Power Apps festgelegt sind, sodass die Buchung auch die Basisdimensionen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="0bd19-293">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="0bd19-294">Alle Dimensionen müssen Basisdimensionen sein, wenn das Feld `dimensionDataSource` unter `filters` null, leer oder ein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="0bd19-294">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="0bd19-295">Beispiel Rückgabeergebnis</span><span class="sxs-lookup"><span data-stu-id="0bd19-295">Example return result</span></span>

<span data-ttu-id="0bd19-296">Die in den vorherigen Beispielen gezeigten Abfragen könnten ein Ergebnis wie dieses zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0bd19-296">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="0bd19-297">Beachten Sie, dass die Mengen-Felder als ein Wörterbuch von Kennzahlen und ihren zugehörigen Werten strukturiert sind.</span><span class="sxs-lookup"><span data-stu-id="0bd19-297">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
