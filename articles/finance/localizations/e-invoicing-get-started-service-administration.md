---
title: Erste Schritte in der Add-On-Dienstverwaltung für die elektronische Rechnungsstellung
description: Dieses Thema erläutert die ersten Schritte mit dem Add-On für die elektronische Rechnungsstellung.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104383"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="1510e-103">Erste Schritte in der Add-On-Dienstverwaltung für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="1510e-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="1510e-104">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1510e-104">Prerequisites</span></span>

<span data-ttu-id="1510e-105">Bevor Sie die Vorgehensweisen in diesem Thema abschließen, müssen die folgenden Voraussetzungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="1510e-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="1510e-106">Sie müssen Zugriff auf Ihr Microsoft Dynamics Lifecycle Services (LCS)-Konto haben.</span><span class="sxs-lookup"><span data-stu-id="1510e-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="1510e-107">Sie müssen über ein LCS-Projekt verfügen, das Version 10.0.13 oder höher von Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management umfasst.</span><span class="sxs-lookup"><span data-stu-id="1510e-107">You must have an LCS project that includes version 10.0.13 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1510e-108">Darüber hinaus müssen diese Apps in einer der folgenden Azure-Regionen bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="1510e-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="1510e-109">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="1510e-109">East US</span></span>
    - <span data-ttu-id="1510e-110">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="1510e-110">West US</span></span>
    - <span data-ttu-id="1510e-111">Norden, Europa</span><span class="sxs-lookup"><span data-stu-id="1510e-111">North EU</span></span>
    - <span data-ttu-id="1510e-112">Westen, Europa</span><span class="sxs-lookup"><span data-stu-id="1510e-112">West EU</span></span>

- <span data-ttu-id="1510e-113">Sie müssen Zugriff auf Ihr RCS-Konto (Dynamics 365 Regulatory Configuration Services) haben.</span><span class="sxs-lookup"><span data-stu-id="1510e-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="1510e-114">Die Globalisierungsfunktion für Ihr RCS-Konto muss in der Funktionsverwaltung aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="1510e-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="1510e-115">Weitere Informationen finden Sie unter [Regulatory Configuration Services (RCS) – Globalisierungsfunktionen](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="1510e-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="1510e-116">Sie müssen einen Schlüsseltresor und ein Speicherkonto in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="1510e-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="1510e-117">Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="1510e-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="1510e-118">Das Add-On für Microservices in Lifecycle Services installieren</span><span class="sxs-lookup"><span data-stu-id="1510e-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="1510e-119">Melden Sie sich bei Ihrem LCS-Konto an.</span><span class="sxs-lookup"><span data-stu-id="1510e-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="1510e-120">Wählen Sie die Kachel **Verwaltung von Vorschaufunktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="1510e-121">Wählen Sie im Abschnitt **Verwaltung von Vorschaufunktionen** **E-Invoicing-Dienst** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="1510e-122">Stellen Sie sicher, dass die Option **Vorschaufunktion aktiviert** auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1510e-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="1510e-123">Richten Sie die Parameter für die RCS-Integration im Add-On für die elektronische Rechnungsstellung ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-123">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="1510e-124">Melden Sie sich bei Ihrem RCS-Konto an.</span><span class="sxs-lookup"><span data-stu-id="1510e-124">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="1510e-125">Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Zugehörige Links** **Elektronische Berichterstellungsparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-125">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="1510e-126">Geben Sie im Feld **Dienstendpunkt-URI** auf der Registerkarte **E-Invoicing-Dienst** den entsprechenden Dienstendpunkt für Ihre Azure-Region ein, wie in folgender Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1510e-126">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="1510e-127">Azure-Rechenzentrumgeografie</span><span class="sxs-lookup"><span data-stu-id="1510e-127">Datacenter Azure geography</span></span> | <span data-ttu-id="1510e-128">Dienst-Endpunkt-URI</span><span class="sxs-lookup"><span data-stu-id="1510e-128">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="1510e-129">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="1510e-129">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1510e-130">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="1510e-130">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1510e-131">Norden, Europa</span><span class="sxs-lookup"><span data-stu-id="1510e-131">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1510e-132">Westen, Europa</span><span class="sxs-lookup"><span data-stu-id="1510e-132">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="1510e-133">Vergewissern Sie sich, dass das Feld **Anwendungs-ID** auf **0cdb527f-a8d1-4bf8-9436-b352c68682b2** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="1510e-133">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="1510e-134">Dieser Wert ist ein fester Wert.</span><span class="sxs-lookup"><span data-stu-id="1510e-134">This value is a fixed value.</span></span>
5. <span data-ttu-id="1510e-135">Geben Sie in das Feld **LCS-Umgebungs-ID** die ID Ihres LCS-Abonnementkontos ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-135">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="1510e-136">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1510e-136">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="1510e-137">Ein Key Vault-Geheimnis erstellen</span><span class="sxs-lookup"><span data-stu-id="1510e-137">Create Key Vault secret</span></span>

1. <span data-ttu-id="1510e-138">Melden Sie sich bei Ihrem RCS-Konto an.</span><span class="sxs-lookup"><span data-stu-id="1510e-138">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="1510e-139">Wählen Sie im Arbeitsbereich **Globalisierungsfunktion** im Abschnitt **Umgebung** die Kachel **Elektronische Rechnungsstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-139">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="1510e-140">Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** und anschließend **Key Vault-Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-140">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="1510e-141">Wählen Sie **Neu** aus, um ein Schlüsseltresorgeheimnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1510e-141">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="1510e-142">Geben Sie im Feld **Name** den Namen des Schlüsseltresorgeheimnisses ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-142">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="1510e-143">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-143">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="1510e-144">Fügen Sie im Feld **Key Vault URI** das Geheimnis aus Azure Key Vault ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-144">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="1510e-145">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-145">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="1510e-146">Ein Speicherkontogeheimnis erstellen</span><span class="sxs-lookup"><span data-stu-id="1510e-146">Create Storage account secret</span></span>

1. <span data-ttu-id="1510e-147">Wählen Sie auf der Seite **Key Vault-Parameter** im Abschnitt **Zertifikate** **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-147">On **Key vault parameters** page, in the **Certificates** section, select **Add**.</span></span>
2. <span data-ttu-id="1510e-148">Geben Sie im Feld **Name** den Namen des Speicherkontogeheimnisses ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-148">In the **Name** field, enter the same of the storage account secret.</span></span> <span data-ttu-id="1510e-149">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-149">In the **Description** field, enter a description.</span></span>
3. <span data-ttu-id="1510e-150">Wählen Sie im Feld **Typ** die Option **Zertifikat** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-150">In the **Type** field, select **Certificate**.</span></span>
4. <span data-ttu-id="1510e-151">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1510e-151">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="1510e-152">Eine Add-On-Umgebung für die elektronische Rechnungsstellung erstellen</span><span class="sxs-lookup"><span data-stu-id="1510e-152">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="1510e-153">Melden Sie sich bei Ihrem RCS-Konto an.</span><span class="sxs-lookup"><span data-stu-id="1510e-153">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="1510e-154">Wählen Sie im Arbeitsbereich **Globalisierungsfunktion** im Abschnitt **Umgebung** die Kachel **Elektronische Rechnungsstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-154">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="1510e-155">Eine Service-Umgebung erstellen</span><span class="sxs-lookup"><span data-stu-id="1510e-155">Create a service environment</span></span>

1. <span data-ttu-id="1510e-156">Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-156">On the **Environment setups** page, on the action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="1510e-157">Wählen Sie **Neu** aus, um eine neue Service-Umgebung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1510e-157">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="1510e-158">Geben Sie im Feld **Name** den Namen der Umgebung für die elektronische Rechnungsstellung ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-158">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="1510e-159">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-159">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="1510e-160">Wählen Sie im Feld **Speicher SAS-Tokengeheimnis** den Namen des Zertifikats aus, das zur Authentifizierung des Zugriffs auf das Speicherkonto verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="1510e-160">In the **Storage SAS token secret** field, select the name of the certificate that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="1510e-161">Wählen Sie im Abschnitt **Benutzer** die Option **Hinzufügen** aus, um einen Benutzerhinzuzufügen, der elektronische Rechnungen über die Umgebung senden und eine Verbindung zum Speicherkonto herstellen darf.</span><span class="sxs-lookup"><span data-stu-id="1510e-161">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="1510e-162">Geben Sie im Feld **Benutzer-ID** den Alias des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-162">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="1510e-163">Geben Sie im Feld **E-Mail** die E-Mail-Adresse des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-163">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="1510e-164">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-164">Select **Save**.</span></span>
8. <span data-ttu-id="1510e-165">Wenn Ihre landes-/regionsspezifischen Rechnungen zur Anwendung digitaler Signaturen eine Zertifikatskette erfordern, wählen Sie im Aktivitätsbereich die Option **Key Vault-Parameter** und anschließend **Zertifikatskette** aus. Befolgen Sie dann diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="1510e-165">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="1510e-166">Wählen Sie **Neu** aus, um eine Zertifikatskette zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1510e-166">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="1510e-167">Geben Sie im Feld **Name** den Namen der Zertifikatskette ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-167">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="1510e-168">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-168">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="1510e-169">Wählen Sie im Abschnitt **Zertifikate** die Option **Hinzufügen** aus, um der Kette ein Zertifikat hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1510e-169">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="1510e-170">Verwenden Sie die Schaltflächen **Oben**- oder **Unten**-Schaltfläche, um die Position des Zertifikats in der Kette zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1510e-170">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="1510e-171">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1510e-171">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="1510e-172">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1510e-172">Close the page.</span></span>
9. <span data-ttu-id="1510e-173">Wählen Sie im Aktivitätsbereich auf der Seite **Service-Umgebung** die Option **Veröffentlichen** aus, um die Umgebung in der Cloud zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="1510e-173">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="1510e-174">Der Wert des Felds **Status** wird in **Veröffentlicht** geändert.</span><span class="sxs-lookup"><span data-stu-id="1510e-174">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="1510e-175">Eine verbundene Anwendung erstellen</span><span class="sxs-lookup"><span data-stu-id="1510e-175">Create a connected application</span></span>

1. <span data-ttu-id="1510e-176">Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Verbundene Anwendungen** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-176">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="1510e-177">Wählen Sie **Neu** aus, um eine verbundene Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1510e-177">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="1510e-178">Geben Sie im Feld **Name** den Namen der zu verbindenden Anwendung ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-178">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="1510e-179">Geben Sie im Feld **Anwendung** die URL der Finance- und Supply Chain Management-Umgebung ein, um eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="1510e-179">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="1510e-180">Geben Sie im Feld **Mandant** den Mandanten der Finance- und Supply Chain Management-Umgebung ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-180">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="1510e-181">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-181">Select **Save**.</span></span>
6. <span data-ttu-id="1510e-182">Wählen Sie im Aktivitätsbereich die Option **Verbindung prüfen** aus, um die Verbindung mit der Umgebung zu testen.</span><span class="sxs-lookup"><span data-stu-id="1510e-182">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="1510e-183">Schließen Sie nun die Seite.</span><span class="sxs-lookup"><span data-stu-id="1510e-183">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="1510e-184">Verbundene Anwendungen mit Umgebungen verknüpfen</span><span class="sxs-lookup"><span data-stu-id="1510e-184">Link connected applications to environments</span></span>

1. <span data-ttu-id="1510e-185">Wählen Sie auf der Seite **Umgebungseinrichtungen** die Option **Neu** aus, um einer Umgebung eine verbundene Anwendung zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="1510e-185">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="1510e-186">Wählen Sie im Feld **Verbundene Anwendung** eine verbundene Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-186">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="1510e-187">Wählen Sie im Feld **Service-Umgebung** eine Service-Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-187">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="1510e-188">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1510e-188">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="1510e-189">Die Add-On-Integration für die elektronische Rechnungsstellung in Finance oder Supply Chain Management einrichten</span><span class="sxs-lookup"><span data-stu-id="1510e-189">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="1510e-190">Aktivieren Sie die Integrationsfunktion für das Add-On für die elektronische Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="1510e-190">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="1510e-191">Melden Sie sich bei Ihrer Finance- oder Supply Chain Management-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="1510e-191">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="1510e-192">Suchen Sie im Arbeitsbereich **Funktionsverwaltung** nach der Funktion **Integration des Add-Ons für die elektronische Rechnungsstellung**.</span><span class="sxs-lookup"><span data-stu-id="1510e-192">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="1510e-193">Wenn diese Funktion nicht auf der Seite angezeigt wird, wählen Sie **Nach Updates suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-193">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="1510e-194">Wählen Sie die Funktion aus und wählen Sie dann **Jetzt aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="1510e-194">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="1510e-195">Einrichten der Service-Endpunkt-URL</span><span class="sxs-lookup"><span data-stu-id="1510e-195">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="1510e-196">Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="1510e-196">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="1510e-197">Geben Sie im Feld **Dienstendpunkt-URL** auf der Registerkarte **Übermittlungsdienst** den entsprechenden Dienstendpunkt für Ihre Azure-Region ein, wie in folgender Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1510e-197">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="1510e-198">Azure-Rechenzentrumgeografie</span><span class="sxs-lookup"><span data-stu-id="1510e-198">Datacenter Azure geography</span></span> | <span data-ttu-id="1510e-199">Dienstendpunkt-URL</span><span class="sxs-lookup"><span data-stu-id="1510e-199">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="1510e-200">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="1510e-200">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1510e-201">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="1510e-201">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1510e-202">Norden, Europa</span><span class="sxs-lookup"><span data-stu-id="1510e-202">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1510e-203">Westen, Europa</span><span class="sxs-lookup"><span data-stu-id="1510e-203">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="1510e-204">Geben Sie im Feld **Umgebung** den Namen der Add-On-Umgebung für die elektronische Rechnungsstellung ein.</span><span class="sxs-lookup"><span data-stu-id="1510e-204">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="1510e-205">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1510e-205">Select **Save**, and then close the page.</span></span>
