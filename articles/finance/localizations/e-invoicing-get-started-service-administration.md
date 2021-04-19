---
title: Erste Schritte mit der Dienstverwaltung für die elektronische Rechnungsstellung
description: Dieses Thema erläutert die ersten Schritte mit der elektronischen Rechnungsstellung.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840147"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="e0385-103">Erste Schritte mit der Dienstverwaltung für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="e0385-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="e0385-104">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="e0385-104">Prerequisites</span></span>

<span data-ttu-id="e0385-105">Bevor Sie die Vorgehensweisen in diesem Thema abschließen, müssen die folgenden Voraussetzungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="e0385-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="e0385-106">Sie müssen Zugriff auf Ihr Microsoft Dynamics Lifecycle Services (LCS)-Konto haben.</span><span class="sxs-lookup"><span data-stu-id="e0385-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="e0385-107">Sie müssen über ein LCS-Projekt verfügen, das Version 10.0.17 oder höher von Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management umfasst.</span><span class="sxs-lookup"><span data-stu-id="e0385-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e0385-108">Darüber hinaus müssen diese Apps in einer der folgenden Azure-Regionen bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="e0385-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="e0385-109">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="e0385-109">East US</span></span>
    - <span data-ttu-id="e0385-110">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="e0385-110">West US</span></span>
    - <span data-ttu-id="e0385-111">Norden, Europa</span><span class="sxs-lookup"><span data-stu-id="e0385-111">North EU</span></span>
    - <span data-ttu-id="e0385-112">Westen, Europa</span><span class="sxs-lookup"><span data-stu-id="e0385-112">West EU</span></span>

- <span data-ttu-id="e0385-113">Sie müssen Zugriff auf Ihr RCS-Konto (Dynamics 365 Regulatory Configuration Services) haben.</span><span class="sxs-lookup"><span data-stu-id="e0385-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="e0385-114">Die Globalisierungsfunktion für Ihr RCS-Konto muss in der Funktionsverwaltung aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="e0385-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="e0385-115">Weitere Informationen finden Sie unter [Regulatory Configuration Services (RCS) – Globalisierungsfunktionen](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="e0385-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="e0385-116">Sie müssen einen Schlüsseltresor und ein Speicherkonto in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="e0385-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="e0385-117">Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="e0385-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="e0385-118">Das Add-In für Microservices in Lifecycle Services installieren</span><span class="sxs-lookup"><span data-stu-id="e0385-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="e0385-119">Melden Sie sich bei Ihrem LCS-Konto an.</span><span class="sxs-lookup"><span data-stu-id="e0385-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="e0385-120">Wählen Sie die Kachel **Verwaltung von Vorschaufunktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="e0385-121">Wählen Sie im Abschnitt **Verwaltung von Vorschaufunktionen** **E-Invoicing-Dienst** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="e0385-122">Stellen Sie sicher, dass die Option **Vorschaufunktion aktiviert** auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e0385-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="e0385-123">Wählen Sie in Ihrem LCS-Dashboard Ihr LCS-Bereitstellungsprojekt aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="e0385-124">Das LCS-Projekt muss ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e0385-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="e0385-125">Wählen Sie auf der Registerkarte **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="e0385-126">Wählen Sie **E-Invoicing-Services** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="e0385-127">Geben Sie im **AAD-Anwendungs-ID**-Feld **091c98b0-a1c9-4b02-b62c-7753395ccabe** ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="e0385-128">Dies ist ein fester Wert.</span><span class="sxs-lookup"><span data-stu-id="e0385-128">This is a fixed value.</span></span>
10. <span data-ttu-id="e0385-129">Geben Sie in das Feld **AAD-Mandanten-ID** die Mandanten-ID Ihres Azure-Abonnementkontos ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="e0385-130">Lesen Sie die allgemeinen Geschäftsbedingungen, und aktivieren Sie dann das Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="e0385-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="e0385-131">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="e0385-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="e0385-132">Parameter für die RCS-Integration in die elektronische Rechnungsstellung einrichten</span><span class="sxs-lookup"><span data-stu-id="e0385-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="e0385-133">Melden Sie sich bei Ihrem RCS-Konto an.</span><span class="sxs-lookup"><span data-stu-id="e0385-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="e0385-134">Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Zugehörige Links** **Elektronische Berichterstellungsparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="e0385-135">Geben Sie im Feld **Dienstendpunkt-URI** auf der Registerkarte **E-Invoicing-Dienst** den entsprechenden Dienstendpunkt für Ihre Azure-Region ein, wie in folgender Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e0385-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="e0385-136">Azure-Rechenzentrumgeografie</span><span class="sxs-lookup"><span data-stu-id="e0385-136">Datacenter Azure geography</span></span> | <span data-ttu-id="e0385-137">Dienst-Endpunkt-URI</span><span class="sxs-lookup"><span data-stu-id="e0385-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="e0385-138">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="e0385-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e0385-139">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="e0385-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e0385-140">Norden, Europa</span><span class="sxs-lookup"><span data-stu-id="e0385-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e0385-141">Westen, Europa</span><span class="sxs-lookup"><span data-stu-id="e0385-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="e0385-142">Vergewissern Sie sich, dass das Feld **Anwendungs-ID** auf **0cdb527f-a8d1-4bf8-9436-b352c68682b2** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="e0385-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="e0385-143">Dieser Wert ist ein fester Wert.</span><span class="sxs-lookup"><span data-stu-id="e0385-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="e0385-144">Geben Sie in das Feld **LCS-Umgebungs-ID** die ID Ihrer LCS-Umgebung ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="e0385-145">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e0385-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="e0385-146">Schlüsseltresorreferenzen erstellen</span><span class="sxs-lookup"><span data-stu-id="e0385-146">Create Key Vault references</span></span>

1. <span data-ttu-id="e0385-147">Melden Sie sich bei Ihrem RCS-Konto an.</span><span class="sxs-lookup"><span data-stu-id="e0385-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="e0385-148">Wählen Sie im Arbeitsbereich **Globalisierungsfunktion** im Abschnitt **Umgebung** die Kachel **Elektronische Rechnungsstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="e0385-149">Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** und anschließend **Key Vault-Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="e0385-150">Wählen Sie **Neu** aus, um eine Schlüsseltresorreferenz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e0385-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="e0385-151">Geben Sie im Feld **Name** den Namen des Schlüsseltresorreferenz ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="e0385-152">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="e0385-153">Fügen Sie im Feld **Key Vault-URI** das Schlüsseltresorgeheimnis aus Azure Key Vault ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="e0385-154">Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="e0385-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="e0385-155">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="e0385-156">Ein Speicherkontogeheimnis erstellen</span><span class="sxs-lookup"><span data-stu-id="e0385-156">Create Storage account secret</span></span>

1. <span data-ttu-id="e0385-157">Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** > **Key Vault-Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="e0385-158">Wählen Sie eine **Key Vault-Referenz** und im Abschnitt **Zertifikate** **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="e0385-159">Geben Sie im Feld **Name** den Namen des Speicherkontogeheimnisses ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="e0385-160">Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="e0385-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="e0385-161">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="e0385-162">Wählen Sie im Feld **Typ** **Geheimnis** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="e0385-163">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e0385-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="e0385-164">Ein digitales Zertifikatgeheimnis erstellen</span><span class="sxs-lookup"><span data-stu-id="e0385-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="e0385-165">Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** und anschließend **Key Vault-Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="e0385-166">Wählen Sie eine **Key Vault-Referenz** und dann im Abschnitt **Zertifikate** **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="e0385-167">Geben Sie im Feld **Name** den Namen des digitalen Zertifikatsgeheimnisses ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="e0385-168">Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="e0385-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="e0385-169">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="e0385-170">Wählen Sie im Feld **Typ** die Option **Zertifikat** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="e0385-171">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e0385-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="e0385-172">Eine Service-Umgebung erstellen</span><span class="sxs-lookup"><span data-stu-id="e0385-172">Create a service environment</span></span>

1. <span data-ttu-id="e0385-173">Melden Sie sich bei Ihrem RCS-Konto an.</span><span class="sxs-lookup"><span data-stu-id="e0385-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="e0385-174">Wählen Sie im Arbeitsbereich **Globalisierungsfunktion** im Abschnitt **Umgebung** die Kachel **Elektronische Rechnungsstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="e0385-175">Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="e0385-176">Wählen Sie **Neu** aus, um eine neue Service-Umgebung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e0385-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="e0385-177">Geben Sie im Feld **Name** den Namen der Umgebung für die elektronische Rechnungsstellung ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="e0385-178">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="e0385-179">Wählen Sie im Feld **Storage SAS-Tokengeheimnis** den Namen des Speicherkontogeheimnisses aus, das zur Authentifizierung des Zugriffs auf das Speicherkonto verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="e0385-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="e0385-180">Wählen Sie im Abschnitt **Benutzer** die Option **Hinzufügen** aus, um einen Benutzerhinzuzufügen, der elektronische Rechnungen über die Umgebung senden und eine Verbindung zum Speicherkonto herstellen darf.</span><span class="sxs-lookup"><span data-stu-id="e0385-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="e0385-181">Geben Sie im Feld **Benutzer-ID** den Alias des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="e0385-182">Geben Sie im Feld **E-Mail** die E-Mail-Adresse des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="e0385-183">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-183">Select **Save**.</span></span>
10. <span data-ttu-id="e0385-184">Wenn Ihre landes-/regionsspezifischen Rechnungen zur Anwendung digitaler Signaturen eine Zertifikatskette erfordern, wählen Sie im Aktivitätsbereich die Option **Key Vault-Parameter** und anschließend **Zertifikatskette** aus. Befolgen Sie dann diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="e0385-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="e0385-185">Wählen Sie **Neu** aus, um eine Zertifikatskette zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e0385-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="e0385-186">Geben Sie im Feld **Name** den Namen der Zertifikatskette ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="e0385-187">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="e0385-188">Wählen Sie im Abschnitt **Zertifikate** die Option **Hinzufügen** aus, um der Kette ein Zertifikat hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e0385-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="e0385-189">Verwenden Sie die Schaltflächen **Oben**- oder **Unten**-Schaltfläche, um die Position des Zertifikats in der Kette zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e0385-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="e0385-190">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e0385-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="e0385-191">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e0385-191">Close the page.</span></span>
11. <span data-ttu-id="e0385-192">Wählen Sie im Aktivitätsbereich auf der Seite **Service-Umgebung** die Option **Veröffentlichen** aus, um die Umgebung in der Cloud zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="e0385-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="e0385-193">Der Wert des Felds **Status** wird in **Veröffentlicht** geändert.</span><span class="sxs-lookup"><span data-stu-id="e0385-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="e0385-194">Eine verbundene Anwendung erstellen</span><span class="sxs-lookup"><span data-stu-id="e0385-194">Create a connected application</span></span>

1. <span data-ttu-id="e0385-195">Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Verbundene Anwendungen** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="e0385-196">Wählen Sie **Neu** aus, um eine verbundene Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e0385-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="e0385-197">Geben Sie im Feld **Name** den Namen der zu verbindenden Anwendung ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="e0385-198">Geben Sie im Feld **Anwendung** die URL der Finance- und Supply Chain Management-Umgebung ein, um eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="e0385-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="e0385-199">Geben Sie im Feld **Mandant** den Mandanten der Finance- und Supply Chain Management-Umgebung ein.</span><span class="sxs-lookup"><span data-stu-id="e0385-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="e0385-200">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-200">Select **Save**.</span></span>
6. <span data-ttu-id="e0385-201">Wählen Sie im Aktivitätsbereich die Option **Verbindung prüfen** aus, um die Verbindung mit der Umgebung zu testen.</span><span class="sxs-lookup"><span data-stu-id="e0385-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="e0385-202">Schließen Sie nun die Seite.</span><span class="sxs-lookup"><span data-stu-id="e0385-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="e0385-203">Verbundene Anwendungen mit Umgebungen verknüpfen</span><span class="sxs-lookup"><span data-stu-id="e0385-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="e0385-204">Wählen Sie auf der Seite **Umgebungseinrichtungen** die Option **Neu** aus, um einer Umgebung eine verbundene Anwendung zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="e0385-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="e0385-205">Wählen Sie im Feld **Verbundene Anwendung** eine verbundene Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="e0385-206">Wählen Sie im Feld **Service-Umgebung** eine Service-Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="e0385-207">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e0385-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="e0385-208">Einrichten der Integration für die elektronische Rechnungsstellung in Finance und Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e0385-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="e0385-209">Aktivieren der Integrationsfunktion für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="e0385-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="e0385-210">Melden Sie sich bei Ihrer Finance- oder Supply Chain Management-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="e0385-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="e0385-211">Suchen Sie im Arbeitsbereich **Funktionsverwaltung** nach der Funktion **Integration für die elektronische Rechnungsstellung**.</span><span class="sxs-lookup"><span data-stu-id="e0385-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="e0385-212">Wenn diese Funktion nicht auf der Seite angezeigt wird, wählen Sie **Nach Updates suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="e0385-213">Wählen Sie die Funktion aus und wählen Sie dann **Jetzt aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="e0385-214">Einrichten der Service-Endpunkt-URL</span><span class="sxs-lookup"><span data-stu-id="e0385-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="e0385-215">Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="e0385-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="e0385-216">Geben Sie im Feld **Dienstendpunkt-URL** auf der Registerkarte **Übermittlungsdienst** den entsprechenden Dienstendpunkt für Ihre Azure-Region ein, wie in folgender Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e0385-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="e0385-217">Azure-Rechenzentrumgeografie</span><span class="sxs-lookup"><span data-stu-id="e0385-217">Datacenter Azure geography</span></span> | <span data-ttu-id="e0385-218">Dienstendpunkt-URL</span><span class="sxs-lookup"><span data-stu-id="e0385-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="e0385-219">USA, Osten</span><span class="sxs-lookup"><span data-stu-id="e0385-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e0385-220">USA, Westen</span><span class="sxs-lookup"><span data-stu-id="e0385-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e0385-221">Norden, Europa</span><span class="sxs-lookup"><span data-stu-id="e0385-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="e0385-222">Westen, Europa</span><span class="sxs-lookup"><span data-stu-id="e0385-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="e0385-223">Geben Sie im Feld **Umgebung** den Namen der Service-Umgebung ein, die in der elektronischen Rechnungsstellung veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="e0385-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="e0385-224">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e0385-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="e0385-225">Flighting-Schlüssel aktivieren</span><span class="sxs-lookup"><span data-stu-id="e0385-225">Enable Flighting keys</span></span>

<span data-ttu-id="e0385-226">Aktivieren Sie Flighting-Schlüssel für Microsoft Dynamics 365 Finance- oder Microsoft Dynamics 365 Supply Chain Management-Versionen 10.0.17 oder früher.</span><span class="sxs-lookup"><span data-stu-id="e0385-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="e0385-227">Führen Sie den folgenden SQL-Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="e0385-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="e0385-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="e0385-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="e0385-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="e0385-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="e0385-230">Führen Sie einen IISreset-Befehl für alle AOS aus.</span><span class="sxs-lookup"><span data-stu-id="e0385-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
