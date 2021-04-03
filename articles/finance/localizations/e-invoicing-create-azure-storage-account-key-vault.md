---
title: Erstellen eines Azure-Speicherkontos und eines Schlüsseltresors
description: In diesem Thema wird erläutert, wie Sie ein Azure-Speicherkonto und einen Schlüsseltresor erstellen.
author: gionoder
manager: AnnBe
ms.date: 02/12/2021
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
ms.openlocfilehash: 14463abe7782d786d286fcc619dee00ce85bb620
ms.sourcegitcommit: 4adc57b0e43d9627dca70762ac941762ec4934e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2021
ms.locfileid: "5479344"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="482cc-103">Erstellen eines Azure-Speicherkontos und eines Schlüsseltresors</span><span class="sxs-lookup"><span data-stu-id="482cc-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="482cc-104">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="482cc-104">Prerequisites</span></span>

<span data-ttu-id="482cc-105">Bevor Sie die Schritte in diesem Thema abschließen können, müssen Sie sicherstellen, dass die folgenden Aufgaben abgeschlossen werden:</span><span class="sxs-lookup"><span data-stu-id="482cc-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="482cc-106">Erstellen Sie eine Schlüsseltresor-Ressource in Azure.</span><span class="sxs-lookup"><span data-stu-id="482cc-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="482cc-107">Weitere Informationen finden Sie unter [Über Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="482cc-107">For more information, see [About Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="482cc-108">Erstellen Sie ein Azure-Speicherkonto (Blob-Speicher).</span><span class="sxs-lookup"><span data-stu-id="482cc-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="482cc-109">Weitere Informationen finden Sie unter [Verwalten des Azure-Speicherkontos](https://docs.microsoft.com/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="482cc-109">For more information, see [Maintaining Azure Storage Account](https://docs.microsoft.com/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="482cc-110">Übersicht</span><span class="sxs-lookup"><span data-stu-id="482cc-110">Overview</span></span>

<span data-ttu-id="482cc-111">In diesem Thema führen Sie zwei Hauptschritte aus:</span><span class="sxs-lookup"><span data-stu-id="482cc-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="482cc-112">Richten Sie das Azure-Speicherkonto ein, um den URI des Speicherkontos abzurufen.</span><span class="sxs-lookup"><span data-stu-id="482cc-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="482cc-113">Richten Sie den Schlüsseltresor zum Speichern des Speicherkonto-URI ein.</span><span class="sxs-lookup"><span data-stu-id="482cc-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="482cc-114">Einrichten des Azure-Speicherkontos, um den URI des Speicherkontos abzurufen</span><span class="sxs-lookup"><span data-stu-id="482cc-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="482cc-115">Öffnen Sie das Speicherkonto, das Sie mit dem Add-On für die elektronische Rechnungsstellung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="482cc-115">Open the storage account that you plan to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="482cc-116">Navigieren Sie zu **Blob-Dienst** \> **Container** und erstellen Sie einen neuen Container.</span><span class="sxs-lookup"><span data-stu-id="482cc-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="482cc-117">Geben Sie einen Namen für den Container ein und legen Sie das Feld **Öffentliche Zugriffsebene** auf **Privat (kein anonymer Zugriff)** fest.</span><span class="sxs-lookup"><span data-stu-id="482cc-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="482cc-118">Öffnen Sie den Container und navigieren Sie zu **Einstellungen \> Zugriffsrichtlinie**.</span><span class="sxs-lookup"><span data-stu-id="482cc-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="482cc-119">Wählen Sie **Richtlinie hinzufügen** aus, um eine gespeicherte Zugriffsrichtlinie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="482cc-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="482cc-120">Legen Sie die Felder **Bezeichner** und **Berechtigungen** nach Bedarf fest.</span><span class="sxs-lookup"><span data-stu-id="482cc-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="482cc-121">Im Feld **Berechtigungen** sollten Sie alle Berechtigungen auswählen.</span><span class="sxs-lookup"><span data-stu-id="482cc-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Erteilen der Blob-Speicherberechtigung](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="482cc-123">Geben Sie das Start- und das Ablaufdatum ein.</span><span class="sxs-lookup"><span data-stu-id="482cc-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="482cc-124">Das Ablaufdatum sollte in der Zukunft liegen.</span><span class="sxs-lookup"><span data-stu-id="482cc-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="482cc-125">Wählen Sie **OK** aus, um die Richtlinie zu speichern. Anschließend speichern Sie Ihre Änderungen im Container.</span><span class="sxs-lookup"><span data-stu-id="482cc-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="482cc-126">Kehren Sie zum Speicherkonto zurück und öffnen Sie **Storage-Explorer (Vorschau)**.</span><span class="sxs-lookup"><span data-stu-id="482cc-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="482cc-127">Klicken Sie mit der rechten Maustaste auf den Container und wählen Sie **Shared Access Signature abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="482cc-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="482cc-128">Kopieren und speichern Sie im Dialogfeld **Shared Access Signatur** den Wert im Feld **URI**.</span><span class="sxs-lookup"><span data-stu-id="482cc-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="482cc-129">Dieser Wert wird in der nächsten Prozedur verwendet und als *URI für die Shared Access Signature* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="482cc-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![Auswählen und Kopieren des URI-Werts](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="482cc-131">Einrichten des Schlüsseltresor zum Speichern des Speicherkonto-URI</span><span class="sxs-lookup"><span data-stu-id="482cc-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="482cc-132">Öffnen Sie den Schlüsseltresor, den Sie mit dem Add-On für die elektronische Rechnungsstellung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="482cc-132">Open the key vault that you intend to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="482cc-133">Navigieren Sie zu **Einstellungen** \> **Geheimnisse** und wählen Sie dann **Generieren/Importieren** aus, um ein neues Geheimnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="482cc-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="482cc-134">Wählen Sie auf der Seite **Geheimnis erstellen** im Feld **Uploadoptionen** die Option **Manuell** aus.</span><span class="sxs-lookup"><span data-stu-id="482cc-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="482cc-135">Geben Sie den Namen für das Geheimnis ein.</span><span class="sxs-lookup"><span data-stu-id="482cc-135">Enter the name of the secret.</span></span> <span data-ttu-id="482cc-136">Dieser Name wird während der Einrichtung des Service im Regulatory Configuration Service (RCS) verwendet und als *geheimer Name des Schlüsseltresors* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="482cc-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="482cc-137">Wählen Sie im Feld **Wert** die Option **URI für die Shared Access Signature** aus und wählen Sie dann **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="482cc-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="482cc-138">Richten Sie die Zugriffsrichtlinie ein, um dem Add-On für die elektronische Rechnungsstellung die richtige Zugriffsebene für den sicheren Zugriff auf das von Ihnen erstellte Geheimnis zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="482cc-138">Set up the access policy to grant the Electronic invoicing add-on the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="482cc-139">Navigieren Sie zu **Einstellungen \> Zugriffsrichtlinie** und wählen Sie **Zugriffsrichtlinie hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="482cc-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="482cc-140">Legen Sie die geheimen Berechtigungen für die Vorgänge **Abrufen** und **Auflisten** fest.</span><span class="sxs-lookup"><span data-stu-id="482cc-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Gewähren des Servicezugriffs](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="482cc-142">Legen Sie die Zertifikatsberechtigungen für die Vorgänge **Abrufen** und **Auflisten** fest.</span><span class="sxs-lookup"><span data-stu-id="482cc-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Gewähren der Zertifikatsberechtigung](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="482cc-144">In dem **Prinzipal auswählen**-Feld wählen Sie **Nichts ausgewählt** aus.</span><span class="sxs-lookup"><span data-stu-id="482cc-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="482cc-145">Wählen Sie im Dialogfeld **Prinzipal** den Prinzipal aus, indem Sie **E-Invoicing-Dienst** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="482cc-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="482cc-146">Wählen Sie **Hinzufügen** aus und wählen Sie dann **Änderungen am Schlüsseltresor speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="482cc-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="482cc-147">Kopieren Sie auf der Seite **Übersicht** den Wert von **DNS-Name** für den Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="482cc-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="482cc-148">Dieser Wert wird während der Einrichtung des Service in RCS verwendet und als *Schlüsseltresor-URI* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="482cc-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

