---
title: Erste Schritte in der Add-On-Dienstverwaltung für die elektronische Rechnungsstellung
description: Dieses Thema erläutert die ersten Schritte mit dem Add-On für die elektronische Rechnungsstellung.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
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
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592525"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="0d227-103">Erste Schritte in der Add-On-Dienstverwaltung für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="0d227-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="0d227-104">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="0d227-104">Prerequisites</span></span>

<span data-ttu-id="0d227-105">Bevor Sie die Vorgehensweisen in diesem Thema abschließen, müssen die folgenden Voraussetzungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="0d227-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="0d227-106">Sie müssen Zugriff auf Ihr Microsoft Dynamics Lifecycle Services (LCS)-Konto haben.</span><span class="sxs-lookup"><span data-stu-id="0d227-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="0d227-107">Sie müssen über ein LCS-Projekt verfügen, das Version 10.0.17 oder höher von Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management umfasst.</span><span class="sxs-lookup"><span data-stu-id="0d227-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0d227-108">Darüber hinaus müssen diese Apps in einer der folgenden Azure-Regionen bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="0d227-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="0d227-109">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="0d227-109">East US</span></span>
    - <span data-ttu-id="0d227-110">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="0d227-110">West US</span></span>
    - <span data-ttu-id="0d227-111">Norden, Europa</span><span class="sxs-lookup"><span data-stu-id="0d227-111">North EU</span></span>
    - <span data-ttu-id="0d227-112">Westen, Europa</span><span class="sxs-lookup"><span data-stu-id="0d227-112">West EU</span></span>

- <span data-ttu-id="0d227-113">Sie müssen Zugriff auf Ihr RCS-Konto (Dynamics 365 Regulatory Configuration Services) haben.</span><span class="sxs-lookup"><span data-stu-id="0d227-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="0d227-114">Die Globalisierungsfunktion für Ihr RCS-Konto muss in der Funktionsverwaltung aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="0d227-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="0d227-115">Weitere Informationen finden Sie unter [Regulatory Configuration Services (RCS) – Globalisierungsfunktionen](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="0d227-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="0d227-116">Sie müssen einen Schlüsseltresor und ein Speicherkonto in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d227-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="0d227-117">Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="0d227-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="0d227-118">Das Add-On für Microservices in Lifecycle Services installieren</span><span class="sxs-lookup"><span data-stu-id="0d227-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="0d227-119">Melden Sie sich bei Ihrem LCS-Konto an.</span><span class="sxs-lookup"><span data-stu-id="0d227-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="0d227-120">Wählen Sie die Kachel **Verwaltung von Vorschaufunktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="0d227-121">Wählen Sie im Abschnitt **Verwaltung von Vorschaufunktionen** **E-Invoicing-Dienst** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="0d227-122">Stellen Sie sicher, dass die Option **Vorschaufunktion aktiviert** auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0d227-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="0d227-123">Wählen Sie in Ihrem LCS-Dashboard Ihr LCS-Bereitstellungsprojekt aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="0d227-124">Das LCS-Projekt muss ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0d227-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="0d227-125">Wählen Sie auf der Registerkarte **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="0d227-126">Wählen Sie **E-Invoicing-Dienste** aus, und geben Sie im Feld **AAD-Anwendungs-ID** die ID **091c98b0-a1c9-4b02-b62c-7753395ccabe** ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="0d227-127">Dies ist ein fester Wert.</span><span class="sxs-lookup"><span data-stu-id="0d227-127">This is a fixed value.</span></span>
10. <span data-ttu-id="0d227-128">Geben Sie in das Feld **AAD-Mandanten-ID** die Mandanten-ID Ihres Azure-Abonnementkontos ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="0d227-129">Lesen Sie die allgemeinen Geschäftsbedingungen, und aktivieren Sie dann das Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="0d227-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="0d227-130">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="0d227-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="0d227-131">Richten Sie die Parameter für die RCS-Integration im Add-On für die elektronische Rechnungsstellung ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="0d227-132">Melden Sie sich bei Ihrem RCS-Konto an.</span><span class="sxs-lookup"><span data-stu-id="0d227-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="0d227-133">Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Zugehörige Links** **Elektronische Berichterstellungsparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="0d227-134">Geben Sie im Feld **Dienstendpunkt-URI** auf der Registerkarte **E-Invoicing-Dienst** den entsprechenden Dienstendpunkt für Ihre Azure-Region ein, wie in folgender Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0d227-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="0d227-135">Azure-Rechenzentrumgeografie</span><span class="sxs-lookup"><span data-stu-id="0d227-135">Datacenter Azure geography</span></span> | <span data-ttu-id="0d227-136">Dienst-Endpunkt-URI</span><span class="sxs-lookup"><span data-stu-id="0d227-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="0d227-137">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="0d227-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0d227-138">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="0d227-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0d227-139">Norden, Europa</span><span class="sxs-lookup"><span data-stu-id="0d227-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0d227-140">Westen, Europa</span><span class="sxs-lookup"><span data-stu-id="0d227-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="0d227-141">Vergewissern Sie sich, dass das Feld **Anwendungs-ID** auf **0cdb527f-a8d1-4bf8-9436-b352c68682b2** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="0d227-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="0d227-142">Dieser Wert ist ein fester Wert.</span><span class="sxs-lookup"><span data-stu-id="0d227-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="0d227-143">Geben Sie in das Feld **LCS-Umgebungs-ID** die ID Ihres LCS-Abonnementkontos ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="0d227-144">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0d227-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="0d227-145">Ein Key Vault-Geheimnis erstellen</span><span class="sxs-lookup"><span data-stu-id="0d227-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="0d227-146">Melden Sie sich bei Ihrem RCS-Konto an.</span><span class="sxs-lookup"><span data-stu-id="0d227-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="0d227-147">Wählen Sie im Arbeitsbereich **Globalisierungsfunktion** im Abschnitt **Umgebung** die Kachel **Add-On für die elektronische Rechnungsstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="0d227-148">Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** und anschließend **Key Vault-Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="0d227-149">Wählen Sie **Neu** aus, um ein Schlüsseltresorgeheimnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d227-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="0d227-150">Geben Sie im Feld **Name** den Namen des Schlüsseltresorgeheimnisses ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="0d227-151">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="0d227-152">Fügen Sie im Feld **Key Vault URI** das Geheimnis aus Azure Key Vault ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="0d227-153">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="0d227-154">Ein Speicherkontogeheimnis erstellen</span><span class="sxs-lookup"><span data-stu-id="0d227-154">Create Storage account secret</span></span>

1. <span data-ttu-id="0d227-155">Gehen Sie zu **Systemadministration** > **Einrichten** > **Key Vault-Parameter** und wählen Sie ein Schlüsseltresorgeheimnis aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="0d227-156">Wählen Sie im **Zertifikate**-Abschnitt **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="0d227-157">Geben Sie im Feld **Name** den Namen des Speicherkontogeheimnisses und in das Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="0d227-158">Wählen Sie im Feld **Typ** die Option **Zertifikat** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="0d227-159">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0d227-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="0d227-160">Ein digitales Zertifikatgeheimnis erstellen</span><span class="sxs-lookup"><span data-stu-id="0d227-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="0d227-161">Gehen Sie zu **Systemadministration** > **Einrichten** > **Key Vault-Parameter** und wählen Sie ein Schlüsseltresorgeheimnis aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="0d227-162">Wählen Sie im **Zertifikate**-Abschnitt **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="0d227-163">Geben Sie im Feld **Name** den Namen des digitalen Zertifikatgeheimnisses und in das Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="0d227-164">Wählen Sie im Feld **Typ** die Option **Zertifikat** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="0d227-165">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0d227-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="0d227-166">Eine Add-On-Umgebung für die elektronische Rechnungsstellung erstellen</span><span class="sxs-lookup"><span data-stu-id="0d227-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="0d227-167">Melden Sie sich bei Ihrem RCS-Konto an.</span><span class="sxs-lookup"><span data-stu-id="0d227-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="0d227-168">Wählen Sie im Arbeitsbereich **Globalisierungsfunktion** im Abschnitt **Umgebung** die Kachel **Add-On für die elektronische Rechnungsstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="0d227-169">Eine Service-Umgebung erstellen</span><span class="sxs-lookup"><span data-stu-id="0d227-169">Create a service environment</span></span>

1. <span data-ttu-id="0d227-170">Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="0d227-171">Wählen Sie **Neu** aus, um eine neue Service-Umgebung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d227-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="0d227-172">Geben Sie im Feld **Name** den Namen der Umgebung für die elektronische Rechnungsstellung ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="0d227-173">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="0d227-174">Wählen Sie im Feld **Storage SAS-Tokengeheimnis** den Namen des Speicherkontogeheimnisses aus, das zur Authentifizierung des Zugriffs auf das Speicherkonto verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="0d227-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="0d227-175">Wählen Sie im Abschnitt **Benutzer** die Option **Hinzufügen** aus, um einen Benutzerhinzuzufügen, der elektronische Rechnungen über die Umgebung senden und eine Verbindung zum Speicherkonto herstellen darf.</span><span class="sxs-lookup"><span data-stu-id="0d227-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="0d227-176">Geben Sie im Feld **Benutzer-ID** den Alias des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="0d227-177">Geben Sie im Feld **E-Mail** die E-Mail-Adresse des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="0d227-178">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-178">Select **Save**.</span></span>
8. <span data-ttu-id="0d227-179">Wenn Ihre landes-/regionsspezifischen Rechnungen zur Anwendung digitaler Signaturen eine Zertifikatskette erfordern, wählen Sie im Aktivitätsbereich die Option **Key Vault-Parameter** und anschließend **Zertifikatskette** aus. Befolgen Sie dann diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="0d227-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="0d227-180">Wählen Sie **Neu** aus, um eine Zertifikatskette zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d227-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="0d227-181">Geben Sie im Feld **Name** den Namen der Zertifikatskette ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="0d227-182">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="0d227-183">Wählen Sie im Abschnitt **Zertifikate** die Option **Hinzufügen** aus, um der Kette ein Zertifikat hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d227-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="0d227-184">Verwenden Sie die Schaltflächen **Oben**- oder **Unten**-Schaltfläche, um die Position des Zertifikats in der Kette zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0d227-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="0d227-185">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0d227-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="0d227-186">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0d227-186">Close the page.</span></span>
9. <span data-ttu-id="0d227-187">Wählen Sie im Aktivitätsbereich auf der Seite **Service-Umgebung** die Option **Veröffentlichen** aus, um die Umgebung in der Cloud zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0d227-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="0d227-188">Der Wert des Felds **Status** wird in **Veröffentlicht** geändert.</span><span class="sxs-lookup"><span data-stu-id="0d227-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="0d227-189">Eine verbundene Anwendung erstellen</span><span class="sxs-lookup"><span data-stu-id="0d227-189">Create a connected application</span></span>

1. <span data-ttu-id="0d227-190">Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Verbundene Anwendungen** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="0d227-191">Wählen Sie **Neu** aus, um eine verbundene Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d227-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="0d227-192">Geben Sie im Feld **Name** den Namen der zu verbindenden Anwendung ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="0d227-193">Geben Sie im Feld **Anwendung** die URL der Finance- und Supply Chain Management-Umgebung ein, um eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="0d227-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="0d227-194">Geben Sie im Feld **Mandant** den Mandanten der Finance- und Supply Chain Management-Umgebung ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="0d227-195">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-195">Select **Save**.</span></span>
6. <span data-ttu-id="0d227-196">Wählen Sie im Aktivitätsbereich die Option **Verbindung prüfen** aus, um die Verbindung mit der Umgebung zu testen.</span><span class="sxs-lookup"><span data-stu-id="0d227-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="0d227-197">Schließen Sie nun die Seite.</span><span class="sxs-lookup"><span data-stu-id="0d227-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="0d227-198">Verbundene Anwendungen mit Umgebungen verknüpfen</span><span class="sxs-lookup"><span data-stu-id="0d227-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="0d227-199">Wählen Sie auf der Seite **Umgebungseinrichtungen** die Option **Neu** aus, um einer Umgebung eine verbundene Anwendung zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="0d227-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="0d227-200">Wählen Sie im Feld **Verbundene Anwendung** eine verbundene Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="0d227-201">Wählen Sie im Feld **Service-Umgebung** eine Service-Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="0d227-202">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0d227-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="0d227-203">Die Add-On-Integration für die elektronische Rechnungsstellung in Finance oder Supply Chain Management einrichten</span><span class="sxs-lookup"><span data-stu-id="0d227-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="0d227-204">Aktivieren Sie die Integrationsfunktion für das Add-On für die elektronische Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="0d227-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="0d227-205">Melden Sie sich bei Ihrer Finance- oder Supply Chain Management-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="0d227-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="0d227-206">Suchen Sie im Arbeitsbereich **Funktionsverwaltung** nach der Funktion **Integration des Add-Ons für die elektronische Rechnungsstellung**.</span><span class="sxs-lookup"><span data-stu-id="0d227-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="0d227-207">Wenn diese Funktion nicht auf der Seite angezeigt wird, wählen Sie **Nach Updates suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="0d227-208">Wählen Sie die Funktion aus und wählen Sie dann **Jetzt aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="0d227-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="0d227-209">Einrichten der Service-Endpunkt-URL</span><span class="sxs-lookup"><span data-stu-id="0d227-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="0d227-210">Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="0d227-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="0d227-211">Geben Sie im Feld **Dienstendpunkt-URL** auf der Registerkarte **Übermittlungsdienst** den entsprechenden Dienstendpunkt für Ihre Azure-Region ein, wie in folgender Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0d227-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="0d227-212">Azure-Rechenzentrumgeografie</span><span class="sxs-lookup"><span data-stu-id="0d227-212">Datacenter Azure geography</span></span> | <span data-ttu-id="0d227-213">Dienstendpunkt-URL</span><span class="sxs-lookup"><span data-stu-id="0d227-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="0d227-214">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="0d227-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0d227-215">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="0d227-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0d227-216">Norden, Europa</span><span class="sxs-lookup"><span data-stu-id="0d227-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0d227-217">Westen, Europa</span><span class="sxs-lookup"><span data-stu-id="0d227-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="0d227-218">Geben Sie im Feld **Umgebung** den Namen der Add-On-Umgebung für die elektronische Rechnungsstellung ein.</span><span class="sxs-lookup"><span data-stu-id="0d227-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="0d227-219">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0d227-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
