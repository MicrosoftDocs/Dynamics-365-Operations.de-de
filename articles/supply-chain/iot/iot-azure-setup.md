---
title: Azure-Ressourcen für IoT-Intelligenz einrichten
description: In diesem Thema wird erläutert, wie Sie Microsoft Azure-Ressourcen erstellen und konfigurieren, die Sie für IoT-Intelligenz benötigen.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1f05f597f86df602c0e00af006b7ccf804f50929
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386519"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="ed4ae-103">Azure-Ressourcen für IoT-Intelligenz einrichten</span><span class="sxs-lookup"><span data-stu-id="ed4ae-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ed4ae-104">In diesem Thema wird erläutert, wie Sie Microsoft Azure-Ressourcen erstellen und konfigurieren, die Sie für IoT-Intelligenz benötigen.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="ed4ae-105">Azure-Ressourcen erstellen</span><span class="sxs-lookup"><span data-stu-id="ed4ae-105">Create Azure resources</span></span>

<span data-ttu-id="ed4ae-106">Führen Sie die folgenden Schritte aus, um einen IoT-Hub, einen Redis-Cache und einen Schlüsseltresor erstellen, auf den Microsoft Dynamics 365 Supply Chain Management zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="ed4ae-107">Sicherstellen, dass die Microsoft Dynamics ERP-Microservices sich in Ihrem Mandanten befinden</span><span class="sxs-lookup"><span data-stu-id="ed4ae-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="ed4ae-108">Führen Sie die folgenden Schritte aus, um zu überprüfen, ob die App-ID für Microsoft Dynamics ERP-Microservices sich in Ihrem Mandanten befindet.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="ed4ae-109">Melden Sie sich beim Azure-Portal an unter <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="ed4ae-110">Gehe zu **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="ed4ae-111">Wechseln Sie zu **Unternehmensanwendungen**.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="ed4ae-112">Wählen Sie im Feld **Anwendungstyp** die Option **Microsoft-Anwendungen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="ed4ae-113">Geben Sie **Microsoft Dynamics ERP-Microservices** in das Suchfeld ein.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="ed4ae-114">Überprüfen Sie, ob **Microsoft Dynamics ERP-Microservices** in der Liste enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="ed4ae-115">Andere Anwendungen haben ähnliche Namen.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-115">Other applications have similar names.</span></span> <span data-ttu-id="ed4ae-116">Achten Sie deshalb darauf, dass Sie die richtige Anwendung finden.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="ed4ae-117">Die App-ID lautet **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="ed4ae-118">Wenn die Anwendung nicht in der Liste enthalten ist, müssen Sie sie Ihrem Mandanten hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="ed4ae-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="ed4ae-119">Wählen Sie im Azure-Portal auf der Symbolleiste die Schaltfläche zum Öffnen von Azure Cloud Shell aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="ed4ae-120">Führen Sie den Befehl **Install-Module AzureAD** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="ed4ae-121">Geben Sie **Y** ein, um das Modul zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="ed4ae-122">Führen Sie den Befehl **Get-InstalledModule -Name "AzureAD"** aus, um zu überprüfen, ob das Modul installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="ed4ae-123">Führen Sie den Befehl **Connect-AzureAD -Confirm** aus, um die Authentifizierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="ed4ae-124">Führen Sie den Befehl **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="ed4ae-125">Sie können jetzt die Schritte 1 bis 6 wiederholen, um zu überprüfen, ob sich die App-ID in Ihrem Mandanten befindet.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="ed4ae-126">Schlüsseltresor-Ressource erstellen</span><span class="sxs-lookup"><span data-stu-id="ed4ae-126">Create a key vault resource</span></span>

<span data-ttu-id="ed4ae-127">Führen Sie die folgenden Schritte aus, um eine Schlüsseltresor-Ressource zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="ed4ae-128">Erstellen Sie im Azure-Portal eine Ressourcengruppe, oder wechseln Sie zu einer.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="ed4ae-129">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-129">Select **Add**.</span></span>
3. <span data-ttu-id="ed4ae-130">Geben Sie auf der Seite **Neu** **Schlüsseltresor** in das Suchfeld ein.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="ed4ae-131">Wählen Sie dann **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-131">Then select **Create**.</span></span>
4. <span data-ttu-id="ed4ae-132">Geben Sie auf der Seite **Schlüsseltresor erstellen** im Feld **Schlüsseltresor-Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="ed4ae-133">Überprüfen Sie die Standardwerte, und wählen Sie dann **Überprüfen + Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="ed4ae-134">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-134">Select **Create**.</span></span>

<span data-ttu-id="ed4ae-135">Der Schlüsseltresor wird im Hintergrund erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="ed4ae-136">IoT-Hub-Ressource erstellen</span><span class="sxs-lookup"><span data-stu-id="ed4ae-136">Create an IoT hub resource</span></span>

<span data-ttu-id="ed4ae-137">Führen Sie die folgenden Schritte aus, um eine IoT-Hub-Ressource zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="ed4ae-138">Erstellen Sie eine Ressourcengruppe, oder wechseln Sie zu einer.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="ed4ae-139">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-139">Select **Add**.</span></span>
3. <span data-ttu-id="ed4ae-140">Geben Sie auf der Seite **Neu** **IoT-Hub** in das Suchfeld ein.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="ed4ae-141">Wählen Sie dann **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-141">Then select **Create**.</span></span>
4. <span data-ttu-id="ed4ae-142">Geben Sie im Feld **IoT-Hub-Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="ed4ae-143">Überprüfen Sie die Standardwerte, und wählen Sie dann **Überprüfen + Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="ed4ae-144">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-144">Select **Create**.</span></span>

<span data-ttu-id="ed4ae-145">Der IoT-Hub wird im Hintergrund erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="ed4ae-146">Es wird empfohlen, nur eine IoT-Hub-Ressource pro Umgebung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="ed4ae-147">Redis-Cache-Ressource erstellen</span><span class="sxs-lookup"><span data-stu-id="ed4ae-147">Create a Redis cache resource</span></span>

<span data-ttu-id="ed4ae-148">Führen Sie die folgenden Schritte aus, um eine Redis-Cache-Ressource zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="ed4ae-149">Erstellen Sie eine Ressourcengruppe, oder wechseln Sie zu einer.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="ed4ae-150">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-150">Select **Add**.</span></span>
3. <span data-ttu-id="ed4ae-151">Geben Sie auf der Seite **Neu** **Azure Cache für Redis** in das Suchfeld ein.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="ed4ae-152">Wählen Sie dann **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-152">Then select **Create**.</span></span>
4. <span data-ttu-id="ed4ae-153">Geben Sie im Feld **DNS-Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="ed4ae-154">Überprüfen Sie die Standardwerte, und wählen Sie dann **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="ed4ae-155">Der Redis-Cache wird im Hintergrund erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="ed4ae-156">Es wird empfohlen, nur einen Redis-Cache pro Umgebung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="ed4ae-157">Alle Ressourcen wurden jetzt erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="ed4ae-158">Azure-Ressourcen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ed4ae-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="ed4ae-159">IoT-Hub konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ed4ae-159">Configure the IoT hub</span></span>

<span data-ttu-id="ed4ae-160">Führen Sie die folgenden Schritte aus, um den IoT-Hub zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="ed4ae-161">Wählen Sie die IoT-Hub-Ressource aus Ihren Ressourcen aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="ed4ae-162">Wählen Sie im linken Navigationsbereich **Integrierte Endpunkte** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="ed4ae-163">Fügen Sie die folgenden Consumergruppen unter **Consumergruppen** ein.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="ed4ae-164">Diese Consumergruppen entsprechen den vordefinierten Szenarien.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="ed4ae-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="ed4ae-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="ed4ae-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="ed4ae-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="ed4ae-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="ed4ae-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="ed4ae-168">Vault Key konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ed4ae-168">Configure the key vault</span></span>

<span data-ttu-id="ed4ae-169">Führen Sie die folgenden Schritte aus, um den Vault Key zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="ed4ae-170">Wählen Sie die Vault Key-Ressource aus Ihren Ressourcen aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="ed4ae-171">Wählen Sie im linken Navigationsbereich **Zugriffsrichtlinien** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="ed4ae-172">Wählen Sie **Zugriffsrichtlinie hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="ed4ae-173">Wählen Sie auf der Seite **Zugriffsrichtlinie hinzufügen** im Feld **Berechtigungen für Geheimnis** die Optionen **Abrufen** und **Liste** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="ed4ae-174">Klicken Sie auf **Prinzipal auswählen**.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="ed4ae-175">Suchen Sie im Dialogfeld **Prinzipal** nach **Microsoft Dynamics ERP-Microservices**, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="ed4ae-176">Klicken Sie dann auf **Auswählen**.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-176">Then select **Select**.</span></span>
7. <span data-ttu-id="ed4ae-177">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-177">Select **Add**.</span></span>
8. <span data-ttu-id="ed4ae-178">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-178">Select **Save**.</span></span>

<span data-ttu-id="ed4ae-179">Die App hat jetzt Zugriff auf die geheimen Schlüssel im Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="ed4ae-180">Geheimen Schlüssel der IoT-Hub-Verbindungszeichenfolge speichern</span><span class="sxs-lookup"><span data-stu-id="ed4ae-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="ed4ae-181">Führen Sie die folgenden Schritte aus, um den geheimen Schlüssel der IoT-Hub-Verbindungszeichenfolge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="ed4ae-182">Wählen Sie die IoT-Hub-Ressource aus Ihren Ressourcen aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="ed4ae-183">Wählen Sie im linken Navigationsbereich **Integrierte Endpunkte** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="ed4ae-184">Kopieren Sie den Wert im Feld **Event Hub-kompatibler Endpunkt**.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="ed4ae-185">Wechseln Sie zur Vault Key-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="ed4ae-186">Wählen Sie im linken Navigationsbereich die Option **Geheime Schlüssel** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="ed4ae-187">Wählen Sie **Generieren/Importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="ed4ae-188">Geben Sie im Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="ed4ae-189">Fügen Sie den zuvor kopierten Endpunktwert in das Feld **Wert** ein.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="ed4ae-190">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="ed4ae-191">Geheimen Schlüssel der Redis-Cache-Verbindungszeichenfolge speichern</span><span class="sxs-lookup"><span data-stu-id="ed4ae-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="ed4ae-192">Führen Sie die folgenden Schritte aus, um den geheimen Schlüssel der Redis-Cache-Verbindungszeichenfolge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="ed4ae-193">Wählen Sie die Redis-Cache-Ressource aus Ihren Ressourcen aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="ed4ae-194">Wählen Sie **Zugangsschlüssel** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="ed4ae-195">Kopieren Sie den Wert in das Feld **Primäre Verbindungszeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="ed4ae-196">Wechseln Sie zur Vault Key-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="ed4ae-197">Wählen Sie im linken Navigationsbereich die Option **Geheime Schlüssel** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="ed4ae-198">Wählen Sie **Generieren/Importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="ed4ae-199">Geben Sie im Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="ed4ae-200">Fügen Sie die zuvor kopierte Verbindungszeichenfolge in das Feld **Wert** ein.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="ed4ae-201">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="ed4ae-202">Wenn Sie eine der Verbindungszeichenfolgen aktualisieren, müssen Sie auch die Werte der geheimen Schlüssel aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="ed4ae-203">Sie haben nun die Bereitstellung der erforderlichen Azure-Ressourcen abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="ed4ae-204">Als Nächstes muss der Schritt [IoT-Intelligenz-Add-In in Microsoft Dynamics Lifecycle Services (LCS) installieren](iot-lcs-setup.md) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ed4ae-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>
