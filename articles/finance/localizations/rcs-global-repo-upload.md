---
title: ER-Konfigurationen in RCS erstellen und sie in das globale Repository hochladen
description: In diesem Thema wird erläutert, wie Sie eine ER-Konfiguration (Electronic Reporting) in Microsoft Regulatory Configuration Services (RCS) erstellen und in das globale Repository hochladen.
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f45749e1bf26eb6f19f326ba8bd15c08436943ad
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218805"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="d113f-103">ER-Konfigurationen in gesetzlichen Konfigurationsdiensten (Regulatory Configuration Services, RCS) erstellen und sie in das globale Repository hochladen</span><span class="sxs-lookup"><span data-stu-id="d113f-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d113f-104">Mit Microsoft Regulatory Configuration Services (RCS) können Sie ER-Konfigurationen (Electronic Reporting) entwerfen und veröffentlichen, damit sie in Ihrem Unternehmen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d113f-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="d113f-105">In den folgenden Verfahren wird erläutert, wie ein Benutzer in der Rolle „Systemadministrator“ oder „Entwickler für elektronische Berichterstellung“ eine abgeleitete Version einer ER-Konfiguration erstellen kann, die in einer RCS-Instanz konfiguriert wurde, und anschließend die abgeleitete Konfiguration in das globale Repository hochlädt.</span><span class="sxs-lookup"><span data-stu-id="d113f-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="d113f-106">Bevor Sie diese Prozeduren abschließen können, müssen Sie zunächst die folgende Voraussetzungen abschließen.</span><span class="sxs-lookup"><span data-stu-id="d113f-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="d113f-107">Auf eine RCS-Instanz zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d113f-107">Access an RCS instance.</span></span>
- <span data-ttu-id="d113f-108">Einen aktiven Konfigurationsanbieter erstellen.</span><span class="sxs-lookup"><span data-stu-id="d113f-108">Create an active configuration provider.</span></span> <span data-ttu-id="d113f-109">Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d113f-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="d113f-110">Sie müssen auch sicherstellen, dass eine RCS-Umgebung für Ihr Unternehmen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d113f-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="d113f-111">Wechseln Sie in der Finance and Operations-App zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="d113f-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d113f-112">Wenn keine RCS-Umgebung für Ihr Unternehmen bereitgestellt wurde, klicken Sie auf **Regulatory services – externe Konfiguration** und folgen Sie den Anweisungen zur Bereitstellung einer RCS-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d113f-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="d113f-113">Wenn für Ihr Unternehmen bereits eine RCS-Umgebung bereitgestellt wurde, verwenden Sie die Seiten-URL, um darauf zuzugreifen, indem Sie die Anmeldeoption auswählen.</span><span class="sxs-lookup"><span data-stu-id="d113f-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="d113f-114">Erstellen Sie eine abgeleitete Version einer Konfiguration in RCS</span><span class="sxs-lookup"><span data-stu-id="d113f-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="d113f-115">Stellen Sie im Arbeitsbereich **Elektronische Berichterstattung** sicher, dass Sie einen aktiven Konfigurationsanbieter für Ihre Organisation haben.</span><span class="sxs-lookup"><span data-stu-id="d113f-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="d113f-116">Wählen Sie **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="d113f-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="d113f-117">Wählen Sie die Konfiguration aus, von der Sie eine neue Version ableiten möchten.</span><span class="sxs-lookup"><span data-stu-id="d113f-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="d113f-118">Sie können das Filterfeld über der Struktur verwenden, um Ihre Suche einzugrenzen.</span><span class="sxs-lookup"><span data-stu-id="d113f-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="d113f-119">Wählen Sie **Konfiguration erstellen** \> **Vom Namen ableiten**.</span><span class="sxs-lookup"><span data-stu-id="d113f-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="d113f-120">Geben Sie einen Namen und eine Beschreibung ein und wählen Sie dann **Konfiguration erstellen** aus, um eine neue abgeleitete Version zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d113f-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="d113f-121">Wählen Sie die neu abgeleitete Konfiguration aus, fügen Sie eine Beschreibung der Version hinzu, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="d113f-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="d113f-122">Der Status der Konfiguration in wird in **Abgeschlossen** geändert.</span><span class="sxs-lookup"><span data-stu-id="d113f-122">The status of the configuration to is changed to **Completed**.</span></span>

![Neue Konfigurationsversion in RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="d113f-124">Wenn der Konfigurationsstatus geändert wird, wird möglicherweise eine Validierungsfehlermeldung angezeigt, die sich auf die verbundenen Anwendungen bezieht.</span><span class="sxs-lookup"><span data-stu-id="d113f-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="d113f-125">Um die Validierung zu deaktivieren, klicken Sie im Aktionsbereich auf der Registerkarte **Konfigurationen** auf **Benutzerparameter**, und setzen Sie dann **Validierung bei der Statusänderung und Neubasis der Konfiguration überspringen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d113f-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="d113f-126">Eine Konfiguration in das globale Repository hochladen</span><span class="sxs-lookup"><span data-stu-id="d113f-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="d113f-127">Um eine neue oder abgeleitete Konfiguration für Ihre Organisation freizugeben, können Sie sie in das globale Repository hochladen.</span><span class="sxs-lookup"><span data-stu-id="d113f-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="d113f-128">Wählen Sie die fertige Version der Konfiguration aus und wählen Sie dann **In das Repository hochladen**.</span><span class="sxs-lookup"><span data-stu-id="d113f-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="d113f-129">Wählen Sie die Option **Global (Microsoft)** aus und dann **Hochladen**.</span><span class="sxs-lookup"><span data-stu-id="d113f-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![In Repository-Optionen hochladen](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="d113f-131">Wählen Sie im Benachrichtigungsfeld **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="d113f-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="d113f-132">Aktualisieren Sie die Beschreibung der Version nach Bedarf und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="d113f-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="d113f-133">Der Status der Konfiguration wird auf **Teilen** aktualisiert, und die Konfiguration wird in das globale Repository hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="d113f-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="d113f-134">Hier können Sie damit auf folgende Arten arbeiten:</span><span class="sxs-lookup"><span data-stu-id="d113f-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="d113f-135">Sie in die Dynamics 365-Instanz importieren</span><span class="sxs-lookup"><span data-stu-id="d113f-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="d113f-136">Weitere Informationen finden Sie unter [Elektronische Berichterstellungskonfigurationen (ER) aus RCS importieren](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="d113f-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="d113f-137">Teilen Sie die Version mit Dritten oder einer externen Organisation [RCS Share Electronic Reporting (ER) -Konfigurationen mit externen Organisationen teilen](rcs-global-repo-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="d113f-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![Abgeleitete Intrastat Contoso-Konfigurationsversion im globalen Repository](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="d113f-139">Eine Konfiguration aus dem globalen Repository löschen</span><span class="sxs-lookup"><span data-stu-id="d113f-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="d113f-140">Führen Sie die folgenden Schritte aus, um eine von Ihrer Organisation erstellte Konfiguration zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d113f-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="d113f-141">Bestätigen Sie im Arbeitsbereich **Elektronische Berichterstattung** dass Ihr Konfigurationsanbieter **Aktiv** ist.</span><span class="sxs-lookup"><span data-stu-id="d113f-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="d113f-142">Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d113f-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="d113f-143">Wählen Sie auf Ihrem aktiven Konfigurationsanbieter **Repository**.</span><span class="sxs-lookup"><span data-stu-id="d113f-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="d113f-144">Wählen Sie den Repository-Typ **Global** und **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="d113f-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="d113f-145">Suchen Sie im Inforegister **Filter** nach der Konfiguration, die Sie löschen möchten, indem Sie die **Filter**-Funktionalität verwenden.</span><span class="sxs-lookup"><span data-stu-id="d113f-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="d113f-146">Im Inforegister **Version** wählen Sie die Version der Konfiguration aus, die Sie löschen möchten, und wählen dann **Löschen**:</span><span class="sxs-lookup"><span data-stu-id="d113f-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![Konfiguration aus dem globalen Repository löschen](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="d113f-148">Wählen Sie im Benachrichtigungsfeld **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="d113f-148">In the confirmation message box, select **Yes**.</span></span>

    ![Bestätigungsmeldung zum Löschen der Konfigurationsversion](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="d113f-150">Die Konfigurationsversion wird gelöscht und eine Bestätigungsmeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d113f-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="d113f-151">Konfigurationen können nur von dem Konfigurationsanbieter gelöscht werden, der sie erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="d113f-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="d113f-152">Wenn die Konfiguration für eine andere Organisation freigegeben wurde, muss die Freigabe der Konfiguration aufgehoben werden, bevor Sie sie löschen können.</span><span class="sxs-lookup"><span data-stu-id="d113f-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]