---
title: Inventory Visibility Add-In
description: In diesem Thema wird beschrieben, wie Sie das Inventory Visibility Add-in für Dynamics 365 Supply Chain Management installieren und konfigurieren.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114669"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="a4f7f-103">Inventory Visibility Add-in</span><span class="sxs-lookup"><span data-stu-id="a4f7f-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="a4f7f-104">Das Inventory Visibility Add-in ist ein unabhängiger und hoch skalierbarer Microservice, der die Verfolgung von Beständen in Echtzeit ermöglicht und so eine globale Sicht auf den Bestand bietet.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="a4f7f-105">Alle Informationen, die sich auf den Bestand beziehen, werden durch Low-Level-SQL-Integration nahezu in Echtzeit an den Dienst exportiert.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="a4f7f-106">Externe Systeme greifen über RESTful APIs auf den Dienst zu, um Bestandsinformationen über festgelegte Dimensionen abzufragen und so eine Liste der verfügbaren Bestandspositionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="a4f7f-107">Inventory Visibility ist ein Microservice, der auf der Microsoft Dataverse aufbaut, d. h. Sie können ihn mit der Power Apps erweitern und mit der Power BI kundenspezifische Funktionen bereitstellen, um Ihre Geschäftsanforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="a4f7f-108">Es ist auch möglich, den Index zu erweitern, um Bestandsabfragen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="a4f7f-109">Inventory Visibility bietet Konfigurationsoptionen, mit denen es sich in mehrere Drittsysteme integrieren lässt.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="a4f7f-110">Es unterstützt die standardisierte Dimension des Bestands, benutzerdefinierte Erweiterbarkeit und standardisierte, konfigurierbare berechnete Mengen.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="a4f7f-111">In diesem Thema wird beschrieben, wie Sie das Inventory Visibility Add-In für Dynamics 365 Supply Chain Management installieren und konfigurieren und wie Sie seine Anwendungsprogrammierschnittstelle (API) verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="a4f7f-112">Installieren Sie das Inventory Visibility Add-In</span><span class="sxs-lookup"><span data-stu-id="a4f7f-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="a4f7f-113">Sie müssen das Inventory Visibility Add-In über Microsoft Dynamics Lifecycle Services (LCS) installieren.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="a4f7f-114">LCS ist ein Portal für die Zusammenarbeit, das eine Umgebung und eine Reihe von regelmäßig aktualisierten Diensten bereitstellt, die Sie bei der Verwaltung des Lebenszyklus Ihrer Dynamics 365 Finance and Operations-Apps unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="a4f7f-115">Weitere Informationen finden Sie unter [Ressourcen für Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="a4f7f-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a4f7f-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a4f7f-116">Prerequisites</span></span>

<span data-ttu-id="a4f7f-117">Bevor Sie das Inventory Visibility Add-In installieren, müssen Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="a4f7f-118">Besorgen Sie sich ein LCS-Implementierungsprojekt mit mindestens einer bereitgestellten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="a4f7f-119">Erzeugen Sie die Beta-Schlüssel für Ihr Angebot in LCS.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="a4f7f-120">Aktivieren Sie die Betaschlüssel für Ihr Angebot für Ihren Benutzer in LCS.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="a4f7f-121">Wenden Sie sich an das Microsoft Inventory Visibility-Produktteam und geben Sie eine Umgebungs-ID an, in der Sie das Inventory Visibility-Add-In bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="a4f7f-122">Wenn Sie Fragen zu diesen Voraussetzungen haben, wenden Sie sich bitte an das Inventory Visibility-Produktteam.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="a4f7f-123">Installieren des Add-Ins</span><span class="sxs-lookup"><span data-stu-id="a4f7f-123">Install the add-in</span></span>

<span data-ttu-id="a4f7f-124">Um das Inventory Visibility Add-In zu installieren, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="a4f7f-125">Melden Sie sich am [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) Portal an.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="a4f7f-126">Wählen Sie auf der Startseite das Projekt aus, in dem Ihre Umgebung bereitgestellt ist.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="a4f7f-127">Wählen Sie auf der Projektseite die Umgebung aus, in der Sie das Add-In installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="a4f7f-128">Scrollen Sie auf der Seite der Umgebung nach unten, bis Sie den Abschnitt **Umgebungs-Add-Ins** sehen.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="a4f7f-129">Wenn der Abschnitt nicht sichtbar ist, stellen Sie sicher, dass die vorausgesetzten Beta-Schlüssel vollständig verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="a4f7f-130">Wählen Sie im Abschnitt **Umgebungs-Add-Ins** die Option **Ein neues Add-In installieren**.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="a4f7f-131">![Die Umgebungsseite in LCS](media/inventory-visibility-environment.png "Die Seite „Umgebung“ in LCS")</span><span class="sxs-lookup"><span data-stu-id="a4f7f-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="a4f7f-132">Wählen Sie den Link **Ein neues Add-In installieren**.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="a4f7f-133">Es öffnet sich eine Liste der verfügbaren Add-Ins.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="a4f7f-134">Wählen Sie **Bestandsdienst** aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="a4f7f-135">(Beachten Sie, dass dies jetzt möglicherweise als **Add-In Inventory Visibility für Dynamics 365 Supply Chain Management** aufgeführt wird).</span><span class="sxs-lookup"><span data-stu-id="a4f7f-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="a4f7f-136">Geben Sie Werte für die folgenden Felder für Ihre Umgebung ein:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="a4f7f-137">**AAD-Anwendungs-ID**</span><span class="sxs-lookup"><span data-stu-id="a4f7f-137">**AAD application ID**</span></span>
    - <span data-ttu-id="a4f7f-138">**AAD-Mandanten-ID**</span><span class="sxs-lookup"><span data-stu-id="a4f7f-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="a4f7f-139">![Einrichtungsseite hinzufügen](media/inventory-visibility-setup.png "Seite zum Einrichten des Add-Ins")</span><span class="sxs-lookup"><span data-stu-id="a4f7f-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="a4f7f-140">Stimmen Sie den Bedingungen zu, indem Sie das Kontrollkästchen **Bedingungen und Konditionen** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="a4f7f-141">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-141">Select **Install**.</span></span> <span data-ttu-id="a4f7f-142">Der Status des Add-Ins wird als **Installation** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="a4f7f-143">Wenn es fertig ist, aktualisieren Sie die Seite, um den Status auf **Installiert** zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="a4f7f-144">Abrufen eines Sicherheitsdienst-Tokens</span><span class="sxs-lookup"><span data-stu-id="a4f7f-144">Get a security service token</span></span>

<span data-ttu-id="a4f7f-145">Um ein Sicherheitsdienst-Token zu erhalten, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-145">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="a4f7f-146">Melden Sie sich beim Azure Portal an, und verwenden Sie es, um die `clientId` und das `clientSecret` für Ihre Supply Chain Management-Anwendung zu finden.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-146">Sign in to Azure Portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="a4f7f-147">Rufen Sie ein Azure Active Directory-Token (`aadToken`) durch Senden einer HTTP-Anfrage mit den folgenden Eigenschaften ab:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-147">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="a4f7f-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="a4f7f-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="a4f7f-149">**Methode** - `GET`</span><span class="sxs-lookup"><span data-stu-id="a4f7f-149">**Method** - `GET`</span></span>
    - <span data-ttu-id="a4f7f-150">**Textinhalt (Formulardaten)**:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-150">**Body content (form data)**:</span></span>

        | <span data-ttu-id="a4f7f-151">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="a4f7f-151">key</span></span> | <span data-ttu-id="a4f7f-152">Wert</span><span class="sxs-lookup"><span data-stu-id="a4f7f-152">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="a4f7f-153">client_id</span><span class="sxs-lookup"><span data-stu-id="a4f7f-153">client_id</span></span> | <span data-ttu-id="a4f7f-154">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="a4f7f-154">${aadAppId}</span></span> |
        | <span data-ttu-id="a4f7f-155">client_secret</span><span class="sxs-lookup"><span data-stu-id="a4f7f-155">client_secret</span></span> | <span data-ttu-id="a4f7f-156">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="a4f7f-156">${aadAppSecret}</span></span> |
        | <span data-ttu-id="a4f7f-157">grant_type</span><span class="sxs-lookup"><span data-stu-id="a4f7f-157">grant_type</span></span> | <span data-ttu-id="a4f7f-158">client_credentials</span><span class="sxs-lookup"><span data-stu-id="a4f7f-158">client_credentials</span></span> |
        | <span data-ttu-id="a4f7f-159">resource</span><span class="sxs-lookup"><span data-stu-id="a4f7f-159">resource</span></span> | <span data-ttu-id="a4f7f-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="a4f7f-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="a4f7f-161">Sie sollten ein `aadToken` als Antwort erhalten, die dem folgenden Beispiel ähnelt.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-161">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="a4f7f-162">Formulieren Sie eine JSON-Anforderung, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-162">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="a4f7f-163">Wobei:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-163">Where:</span></span>
    - <span data-ttu-id="a4f7f-164">Der Wert von `client_assertion` muss das `aadToken`, das Sie im vorherigen Schritt erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-164">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="a4f7f-165">Der Wert von `context` muss die Umgebungs-ID sein, unter der Sie das Add-In bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-165">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="a4f7f-166">Stellen Sie alle anderen Werte wie im Beispiel gezeigt ein.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-166">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="a4f7f-167">Senden Sie eine HTTP-Anforderung mit den folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-167">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="a4f7f-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="a4f7f-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="a4f7f-169">**Methode** - `POST`</span><span class="sxs-lookup"><span data-stu-id="a4f7f-169">**Method** - `POST`</span></span>
    - <span data-ttu-id="a4f7f-170">**HTTP-Header** – Fügen Sie die API-Version hinzu (Schlüssel ist `Api-Version`, und Wert ist `1.0`).</span><span class="sxs-lookup"><span data-stu-id="a4f7f-170">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="a4f7f-171">**Körperinhalt** – Fügen Sie die JSON-Anforderung ein, die Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-171">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="a4f7f-172">Sie werden eine `access_token` als Antwort erhalten.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-172">You will get an `access_token` in response.</span></span> <span data-ttu-id="a4f7f-173">Diese benötigen Sie als Inhaber-Token, um die Inventory Visibility API aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-173">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="a4f7f-174">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-174">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="a4f7f-175">Add-In deinstallieren</span><span class="sxs-lookup"><span data-stu-id="a4f7f-175">Uninstall the add-in</span></span>

<span data-ttu-id="a4f7f-176">Um das Add-In zu deinstallieren, wählen Sie **Deinstallieren**.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-176">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="a4f7f-177">Aktualisieren Sie LCS und das Inventory Visibility Add-in wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-177">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="a4f7f-178">Der Deinstallationsprozess entfernt die Registrierung des Add-Ins und startet außerdem einen Job zum Bereinigen aller im Dienst gespeicherten Geschäftsdaten.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-178">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="a4f7f-179">Öffentliches API des Inventory Visibility Add-Ins</span><span class="sxs-lookup"><span data-stu-id="a4f7f-179">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="a4f7f-180">Die öffentliche REST-API des Inventory Visibility Add-Ins bietet mehrere spezifische Endpunkte für die Integration.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-180">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="a4f7f-181">Sie unterstützt drei Hauptinteraktionstypen:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-181">It supports three main interaction types:</span></span>

- <span data-ttu-id="a4f7f-182">Buchen von Bestandsänderungen an das Add-In aus einem externen System.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-182">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="a4f7f-183">Abfrage von aktuellen Bestandsmengen aus einem externen System.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-183">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="a4f7f-184">Automatische Synchronisation mit dem Supply Chain Management-Bestand.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-184">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="a4f7f-185">Die automatische Synchronisation ist nicht Teil der öffentlichen API, sondern wird für Umgebungen, die das Inventory Visibility Add-in aktiviert haben, im Hintergrund ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-185">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="a4f7f-186">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-186">Authentication</span></span>

<span data-ttu-id="a4f7f-187">Das Plattform-Sicherheits-Token wird verwendet, um das Inventory Visibility Add-in aufzurufen, daher müssen Sie ein Azure Active Directory-Token mit Ihrer Azure Active Directory-Anwendung erzeugen.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-187">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="a4f7f-188">Weitere Informationen darüber, wie Sie das Sicherheitstoken erhalten, finden Sie unter [Installieren des Inventory Visibility Add-Ins](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="a4f7f-188">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="a4f7f-189">Konfigurieren Sie die Inventory Visibility API</span><span class="sxs-lookup"><span data-stu-id="a4f7f-189">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="a4f7f-190">Bevor Sie den Dienst verwenden, müssen Sie die in den folgenden Unterabschnitten beschriebenen Konfigurationen durchführen.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-190">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="a4f7f-191">Die Konfiguration kann je nach den Details Ihrer Umgebung variieren.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-191">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="a4f7f-192">Sie besteht im Wesentlichen aus vier Teilen:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-192">It primarily includes four parts:</span></span>

- [<span data-ttu-id="a4f7f-193">Partitionierung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-193">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="a4f7f-194">Dimensions-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="a4f7f-194">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="a4f7f-195">Indizierung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-195">Indexing</span></span>](#indexing)
- [<span data-ttu-id="a4f7f-196">Benutzerdefinierte Messung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-196">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="a4f7f-197">Partitionierung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-197">Partitioning</span></span>

<span data-ttu-id="a4f7f-198">Die Partitionierung kann die Leistung der Inventory Visibility API erheblich beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-198">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="a4f7f-199">Es ist eine gute Idee, ein Schema zu definieren, das kleine Gruppierungen von Daten zulässt und trotzdem sinnvolle Datenabfragen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-199">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="a4f7f-200">Die `organizationId` (`dataAreaId` im Supply Chain Management) wird immer Teil der Partitionierung sein, und standardmäßig ist Inventory Visibility so festgelegt, dass es nach Dimensionen wie *Standort + Lagerplatz* partitioniert.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-200">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="a4f7f-201">Das bedeutet, dass der Dienst immer mit diesen in den Filtern definierten Dimensionen abgefragt werden muss.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-201">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="a4f7f-202">*Standort* und *Lagerplatz* sind zwei allgemeine Standarddimensionen in Inventory Visibility.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-202">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="a4f7f-203">Im Supply Chain Management heißen diese Dimensionen *Standort* (`InventSiteId`) und *Lagerort* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="a4f7f-203">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="a4f7f-204">Konfigurationen der Dimensionen</span><span class="sxs-lookup"><span data-stu-id="a4f7f-204">Dimension configurations</span></span>

<span data-ttu-id="a4f7f-205">Inventory Visibility stellt eine Liste allgemeiner Standarddimensionen zur Verfügung, um die Integration mehrerer Quellsysteme zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-205">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="a4f7f-206">In der folgenden Tabelle sind die Bestandsdimensionen aufgeführt, die als Standarddimensionen in Inventory Visibility verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-206">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="a4f7f-207">Dimensionstyp</span><span class="sxs-lookup"><span data-stu-id="a4f7f-207">Dimension type</span></span> | <span data-ttu-id="a4f7f-208">Dimensionsname</span><span class="sxs-lookup"><span data-stu-id="a4f7f-208">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="a4f7f-209">Produkt</span><span class="sxs-lookup"><span data-stu-id="a4f7f-209">Product</span></span> | `ColorId` |
| <span data-ttu-id="a4f7f-210">Produkt</span><span class="sxs-lookup"><span data-stu-id="a4f7f-210">Product</span></span> | `SizeId` |
| <span data-ttu-id="a4f7f-211">Produkt</span><span class="sxs-lookup"><span data-stu-id="a4f7f-211">Product</span></span> | `StyleId` |
| <span data-ttu-id="a4f7f-212">Produkt</span><span class="sxs-lookup"><span data-stu-id="a4f7f-212">Product</span></span> | `ConfigId` |
| <span data-ttu-id="a4f7f-213">Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-213">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="a4f7f-214">Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-214">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="a4f7f-215">Ziel</span><span class="sxs-lookup"><span data-stu-id="a4f7f-215">Location</span></span> | `LocationId` |
| <span data-ttu-id="a4f7f-216">Ziel</span><span class="sxs-lookup"><span data-stu-id="a4f7f-216">Location</span></span> | `SiteId` |
| <span data-ttu-id="a4f7f-217">Bestand Status</span><span class="sxs-lookup"><span data-stu-id="a4f7f-217">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="a4f7f-218">Lagerspezifisch</span><span class="sxs-lookup"><span data-stu-id="a4f7f-218">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="a4f7f-219">Lagerspezifisch</span><span class="sxs-lookup"><span data-stu-id="a4f7f-219">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="a4f7f-220">Lagerort-spezifisch</span><span class="sxs-lookup"><span data-stu-id="a4f7f-220">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="a4f7f-221">Der in der vorherigen Tabelle aufgeführte Dimensionstyp dient nur als Referenz.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-221">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="a4f7f-222">Sie müssen den Dimensionstyp nicht in Inventory Visibility definieren.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-222">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="a4f7f-223">Wenn eine benutzerdefinierte Dimension existiert und zu einem Standardwert fließen muss, wenn sie von Inventory Visibility konsumiert wird, können Sie den Namen **Benutzerdefinierte Dimension** in Inventory Visibility konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-223">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="a4f7f-224">Externe Systeme greifen auf Inventory Visibility über RESTful-APIs zu, mit denen Bestandsinformationen über festgelegte Dimensionen abgefragt werden können.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-224">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="a4f7f-225">Für die Integration können Sie in Inventory Visibility die *Externe Kanaldatenquelle* und die Quelldimension zu den *Zieldimensionen* konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-225">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="a4f7f-226">Die Zieldimensionen sollten eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-226">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="a4f7f-227">Standarddimensionen in Inventory Visibility</span><span class="sxs-lookup"><span data-stu-id="a4f7f-227">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="a4f7f-228">Benutzerdefinierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="a4f7f-228">Custom dimensions</span></span>

<span data-ttu-id="a4f7f-229">Der Zweck der Dimensionskonfiguration ist es, die Multisystem-Integration für die Abfrage auf Dimensionen und das Buchungsereignis mit Dimensionen zu standardisieren.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-229">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="a4f7f-230">Indizierung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-230">Indexing</span></span>

<span data-ttu-id="a4f7f-231">In den meisten Fällen wird die Bestandsabfrage nicht nur auf der höchsten „Gesamt“-Ebene erfolgen, sondern Sie möchten die Ergebnisse möglicherweise auf der Basis der Bestandsdimensionen aggregiert sehen.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-231">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="a4f7f-232">Inventory Visibility bietet Flexibilität, indem es Ihnen erlaubt, die Indizes festzulegen, die auf der Dimension oder der Kombination der Dimensionen basieren.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-232">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="a4f7f-233">Derzeit können Sie nur Indizes bis maximal fünf konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-233">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="a4f7f-234">Sie müssen vor der Implementierung sorgfältig abwägen, welche Dimension oder Dimensionskombination Sie verwenden wollen, um sicherzustellen, dass sie Ihren geschäftlichen Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-234">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="a4f7f-235">Wenn Sie z. B. Produkte wie folgt abfragen wollen:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-235">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="a4f7f-236">Abfrage des aggregierten Produktbestandes nach den Dimensionen *Farbe* und *Größe*.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-236">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="a4f7f-237">In manchen Fällen wollen Sie nur das Produkt insgesamt abfragen.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-237">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="a4f7f-238">Dann würden Sie zwei Indizes wie folgt definieren:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-238">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="a4f7f-239">Die leere Klammer wird auf Basis der Produkt-ID innerhalb der Partition aggregiert.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-239">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="a4f7f-240">Die Indizierung definiert, wie Sie Ihre Ergebnisse basierend auf der Abfrageeinstellung `groupBy` gruppieren können.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-240">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="a4f7f-241">Wenn Sie in diesem Fall keine `groupBy`-Werte definieren, erhalten Sie Summen nach `productid`.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-241">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="a4f7f-242">Wenn Sie dagegen `groupBy` als `groupBy=ColorId&groupBy=SizeId` definieren, erhalten Sie mehrere Zeilen zurück, basierend auf den verschiedenen Farb- und Größenkombinationen im System.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-242">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="a4f7f-243">Sie können Ihre Abfragekriterien in den Abfragekörper einlagern.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-243">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="a4f7f-244">Hier ist eine Beispielabfrage für das Produkt mit Farb- und Größenkombination.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-244">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="a4f7f-245">Benutzerdefinierte Messung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-245">Custom measurement</span></span>

<span data-ttu-id="a4f7f-246">Die voreingestellten Messungen sind mit dem Supply Chain Management verknüpft, aber Sie möchten vielleicht eine Menge haben, die sich aus einer Kombination der voreingestellten Kennzahlen zusammensetzt.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-246">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="a4f7f-247">Dazu können Sie eine Konfiguration von benutzerdefinierten Mengen haben, die zur Ausgabe der Bestandsabfragen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-247">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="a4f7f-248">Die Funktionalität erlaubt es Ihnen einfach, eine Reihe von Kennzahlen festzulegen, die addiert werden, und/oder eine Reihe von Kennzahlen, die subtrahiert werden, um die benutzerdefinierte Messung zu bilden.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-248">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="a4f7f-249">Mit der folgenden Abfragebedingung konfigurieren Sie zum Beispiel die benutzerdefinierte Messung als `MyCustomAvailableforReservation`, die vom Verbrauchssystem verbraucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-249">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="a4f7f-250">Verbrauchs-System</span><span class="sxs-lookup"><span data-stu-id="a4f7f-250">Consumption system</span></span> | <span data-ttu-id="a4f7f-251">Berechnete Kennzahlen</span><span class="sxs-lookup"><span data-stu-id="a4f7f-251">Calculated measurers</span></span> | <span data-ttu-id="a4f7f-252">Datenquelle</span><span class="sxs-lookup"><span data-stu-id="a4f7f-252">Data source</span></span> | <span data-ttu-id="a4f7f-253">Modifikator</span><span class="sxs-lookup"><span data-stu-id="a4f7f-253">Modifier</span></span> | <span data-ttu-id="a4f7f-254">Modifikator Berechnungsart</span><span class="sxs-lookup"><span data-stu-id="a4f7f-254">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="a4f7f-255">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-255">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="a4f7f-256">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-256">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="a4f7f-257">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="a4f7f-257">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="a4f7f-258">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-258">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="a4f7f-259">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="a4f7f-259">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="a4f7f-260">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-260">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="a4f7f-261">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-261">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="a4f7f-262">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="a4f7f-262">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="a4f7f-263">Subtrahieren</span><span class="sxs-lookup"><span data-stu-id="a4f7f-263">Subtraction</span></span> |

<span data-ttu-id="a4f7f-264">Damit wird die Abfrage auf die benutzerdefinierte Messung Menge die folgende Ausgabe zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-264">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="a4f7f-265">Die Ausgabe `MyCustomAvailableforReservation` basiert auf der Berechnungseinstellung in den benutzerdefinierten Messungen als:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-265">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="a4f7f-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="a4f7f-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="a4f7f-267">Verbuchung von Vorratsänderungen</span><span class="sxs-lookup"><span data-stu-id="a4f7f-267">Posting on-hand changes</span></span>

<span data-ttu-id="a4f7f-268">Die genaue URL, unter der das Ereignis gepostet wird, hängt von Ihrer geografischen Region ab.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-268">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="a4f7f-269">Sie wird die Form haben:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-269">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="a4f7f-270">Wenn Sie authentifiziert sind, kann diese URL zusammen mit der HTTP-Methode `POST` verwendet werden, um Ereignisse zu senden, die von Hand geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-270">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="a4f7f-271">Für die Kommunikation mit Dynamics 365-Diensten über HTTP-Anfragen wird ein spezieller Header verwendet, der die Umgebungs-ID der Supply Chain Management-Instanz angibt, mit der die Daten verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-271">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="a4f7f-272">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-272">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="a4f7f-273">Buchen von On-Hand-Änderungen Abfragebeispiel 1</span><span class="sxs-lookup"><span data-stu-id="a4f7f-273">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="a4f7f-274">Dieses Beispiel zeigt ein Szenario, in dem Sie die Konfiguration der Dimension in Power Apps festlegen werden.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-274">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="a4f7f-275">Verwenden Sie die folgende Abfrage, um die Zuordnung der Dimension in Power Apps zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-275">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="a4f7f-276">Jetzt können Sie die `dimensionDataSource` angeben und benutzerdefinierte Dimensionen in Ihren Abfragen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-276">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="a4f7f-277">Das System wird die benutzerdefinierten Dimensionen automatisch in Basisdimensionen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-277">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="a4f7f-278">Buchen von Bestandsänderungen Abfragebeispiel 2</span><span class="sxs-lookup"><span data-stu-id="a4f7f-278">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="a4f7f-279">Dieses Beispiel zeigt ein Szenario, in dem keine Zuordnungen für die Dimensionskonfiguration in Power Apps festgelegt sind, sodass die Buchung auch die Basisdimensionen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-279">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="a4f7f-280">Alle Dimensionen müssen Basisdimensionen sein, wenn das Feld `dimensionDataSource` null, leer oder ein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-280">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="a4f7f-281">JSON-Dokument-Feldeigenschaften</span><span class="sxs-lookup"><span data-stu-id="a4f7f-281">JSON document field properties</span></span>

<span data-ttu-id="a4f7f-282">Die Felder aus den zuvor angegebenen JSON-Abfragebeispielen haben die in der folgenden Tabelle aufgeführten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-282">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="a4f7f-283">Feldkennung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-283">Field ID</span></span> | <span data-ttu-id="a4f7f-284">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4f7f-284">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="a4f7f-285">Eine eindeutige ID für das spezifische Änderungsereignis.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-285">A unique ID for the specific change event.</span></span> <span data-ttu-id="a4f7f-286">Diese ID wird verwendet, um sicherzustellen, dass, wenn die Kommunikation mit dem Dienst während der Buchung fehlschlägt, ein erneutes Einreichen des Ereignisses nicht dazu führt, dass dasselbe Ereignis im System doppelt gezählt wird.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-286">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="a4f7f-287">Die Kennung der Organisation, die mit dem Ereignis verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-287">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="a4f7f-288">Dies entspricht der Zuordnung zu Supply Chain Management-Organisationen oder Datenbereichs-IDs.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-288">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="a4f7f-289">Die Kennung des betreffenden Produkts.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-289">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="a4f7f-290">Die Menge, um die der Lagerbestand geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-290">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="a4f7f-291">Wenn z.B. 10 neue Bagels in ein Regal gestellt wurden, wäre dieser Wert 10.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-291">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="a4f7f-292">Wenn dann 3 Bagels aus dem Regal entfernt oder verkauft würden, wäre dieser Wert -3.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-292">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="a4f7f-293">Die Datenquelle der Dimensionen, die im Umbuchungsereignis und in der Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-293">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="a4f7f-294">Wenn Sie die Datenquelle angeben, können Sie die benutzerdefinierten Dimensionen aus der angegebenen Datenquelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-294">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="a4f7f-295">Mit der Dimensionskonfiguration kann Inventory Visibility die benutzerdefinierten Dimensionen den allgemeinen Standarddimensionen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-295">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="a4f7f-296">Wenn die `dimensionDataSource` nicht angegeben wird, können Sie nur die allgemeinen Standarddimensionen in Ihren Abfragen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-296">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="a4f7f-297">Eine dynamische Tasche mit Schlüssel/Wertpaaren.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-297">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="a4f7f-298">Diese werden einigen der Dimensionen im Supply Chain Management zugeordnet, aber Sie können auch benutzerdefinierte Dimensionen hinzufügen (wie *Quelle*), die angeben, ob das Ereignis aus dem Supply Chain Management oder einem externen System stammt.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-298">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="a4f7f-299">Abfrage des aktuellen Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="a4f7f-299">Querying current on-hand</span></span>

<span data-ttu-id="a4f7f-300">Der Endpunkt für die Abfrage des aktuellen Lagerbestands wird eine ähnliche URL haben:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-300">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="a4f7f-301">Er wird mit der HTTP-Methode `POST` abgefragt.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-301">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="a4f7f-302">Abfrage des aktuellen Lagerbestands Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a4f7f-302">Current on-hand query example 1</span></span>

<span data-ttu-id="a4f7f-303">Dieses Beispiel zeigt ein Szenario, bei dem Sie die Konfiguration der Dimension in Power Apps bereits abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-303">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="a4f7f-304">Verwenden Sie die folgende Abfrage, um die Zuordnung der Dimension in Power Apps zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="a4f7f-304">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="a4f7f-305">Jetzt können Sie die `dimensionDataSource` angeben und benutzerdefinierte Dimensionen in Ihren Abfragen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-305">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="a4f7f-306">Das System wird die benutzerdefinierten Dimensionen automatisch in Basisdimensionen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-306">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="a4f7f-307">Sie können die `DimensionDataSource` in `filters` angeben und benutzerdefinierte Dimensionen sowohl in `filters` als auch in `groupByValues` angeben.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-307">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="a4f7f-308">Das System wird die benutzerdefinierten Dimensionen automatisch in Basisdimensionen umwandeln.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-308">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="a4f7f-309">Aktuelle Bestandsabfrage Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a4f7f-309">Current on-hand query example 2</span></span>

<span data-ttu-id="a4f7f-310">Dieses Beispiel zeigt ein Szenario, in dem keine Zuordnungen für die Dimensionskonfiguration in Power Apps festgelegt sind, sodass die Buchung auch die Basisdimensionen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-310">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="a4f7f-311">Alle Dimensionen müssen Basisdimensionen sein, wenn das Feld `dimensionDataSource` unter `filters` null, leer oder ein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-311">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="a4f7f-312">Beispiel Rückgabeergebnis</span><span class="sxs-lookup"><span data-stu-id="a4f7f-312">Example return result</span></span>

<span data-ttu-id="a4f7f-313">Die in den vorherigen Beispielen gezeigten Abfragen könnten ein Ergebnis wie dieses zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-313">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="a4f7f-314">Beachten Sie, dass die Mengen-Felder als ein Wörterbuch von Kennzahlen und ihren zugehörigen Werten strukturiert sind.</span><span class="sxs-lookup"><span data-stu-id="a4f7f-314">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
