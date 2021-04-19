---
title: ER-Konfigurationen in RCS/dem globalen Repository mit externen Organisationen teilen
description: In diesem Thema wird erläutert, wie Sie eine ER-Konfiguration (Electronic Reporting) in Microsoft Regulatory Configuration Services (RCS) /im globalen Repository mit externen Organisationen teilen.
author: JaneA07
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ace62319bbfa38bcf4be7157882dd0c8989e25bc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838744"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="cc716-103">ER-Konfigurationen (Electronic Reporting) in Microsoft Regulatory Configuration Services (RCS) /im globalen Repository mit externen Organisationen teilen</span><span class="sxs-lookup"><span data-stu-id="cc716-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc716-104">Mit Microsoft Regulatory Configuration Services (RCS) können Sie ER-Konfigurationen (Electronic Reporting) freigeben und für externe Organisationen veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="cc716-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="cc716-105">In den folgenden Verfahren wird erläutert, wie ein RCS-Benutzer eine Version einer ER-Konfiguration, die in einer RCS-Instanz konfiguriert wurde, für eine externe Organisation freigeben kann.</span><span class="sxs-lookup"><span data-stu-id="cc716-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="cc716-106">Bevor Sie diese Prozeduren abschließen können, müssen Sie zunächst die folgende Voraussetzungen abschließen.</span><span class="sxs-lookup"><span data-stu-id="cc716-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="cc716-107">Auf eine RCS-Instanz zugreifen.</span><span class="sxs-lookup"><span data-stu-id="cc716-107">Access an RCS instance.</span></span>
- <span data-ttu-id="cc716-108">Einen aktiven Konfigurationsanbieter erstellen.</span><span class="sxs-lookup"><span data-stu-id="cc716-108">Create an active configuration provider.</span></span> <span data-ttu-id="cc716-109">Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="cc716-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="cc716-110">Erstellen Sie eine neue Version einer ER-Konfiguration und laden Sie sie hoch.</span><span class="sxs-lookup"><span data-stu-id="cc716-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="cc716-111">Weitere Informationen finden Sie unter [Eine neue Version einer ER-Konfiguration (Electronic Reporting) erstellen und hochladen](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="cc716-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="cc716-112">Sie müssen auch sicherstellen, dass eine RCS-Umgebung für Ihr Unternehmen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cc716-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="cc716-113">Wechseln Sie in der Finance and Operations-App zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="cc716-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="cc716-114">Wenn keine RCS-Umgebung für Ihr Unternehmen bereitgestellt wurde, klicken Sie auf **Regulatory services – externe Konfiguration** und folgen Sie den Anweisungen zur Bereitstellung einer RCS-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="cc716-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="cc716-115">Wenn für Ihr Unternehmen bereits eine RCS-Umgebung bereitgestellt wurde, verwenden Sie die Seiten-URL, um darauf zuzugreifen, indem Sie die Anmeldeoption auswählen.</span><span class="sxs-lookup"><span data-stu-id="cc716-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="cc716-116">Konfiguration überprüfen, die Sie freigeben möchten</span><span class="sxs-lookup"><span data-stu-id="cc716-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="cc716-117">Führen Sie die folgenden Schritte aus, um sicherzustellen, dass die Konfiguration, die Sie freigeben möchten, bereits in das globale Repository hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="cc716-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="cc716-118">Wählen Sie im Arbeitsbereich **Elektronische Berichterstattung** **Repositorys** für Ihren Konfigurationsanbieter aus.</span><span class="sxs-lookup"><span data-stu-id="cc716-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![Konfigurationsanbieter](media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="cc716-120">Wählen Sie **Globales Repository** \> **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="cc716-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="cc716-121">Konfiguration suchen, die Sie freigeben möchten</span><span class="sxs-lookup"><span data-stu-id="cc716-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="cc716-122">Sie können das Filterfeld verwenden, um Ihre Suche einzugrenzen.</span><span class="sxs-lookup"><span data-stu-id="cc716-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="cc716-123">Wenn Sie die Konfiguration nicht im globalen Repository finden können, führen Sie die Schritte in [Eine neue Version einer ER-Konfiguration (Electronic Reporting) erstellen und hochladen](rcs-global-repo-upload.md) aus.</span><span class="sxs-lookup"><span data-stu-id="cc716-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="cc716-124">EB-Konfigurationen für externe Organisationen freigeben</span><span class="sxs-lookup"><span data-stu-id="cc716-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="cc716-125">Nachdem eine Konfiguration unter Ihrem Konfigurationsanbieter erstellt wurde, können Sie sie direkt für externe Organisationen über das Inforegister **Geteilt mit** auf der Seite **Globales Konfigurations-Repository** freigeben.</span><span class="sxs-lookup"><span data-stu-id="cc716-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="cc716-126">Wählen Sie im Arbeitsbereich **Elektronische Berichterstattung** **Repositorys** für Ihren Konfigurationsanbieter aus.</span><span class="sxs-lookup"><span data-stu-id="cc716-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="cc716-127">Wählen Sie **Globales Repository** \> **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="cc716-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="cc716-128">Konfiguration auswählen, die Sie freigeben möchten</span><span class="sxs-lookup"><span data-stu-id="cc716-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="cc716-129">Wählen Sie auf dem Inforegister **Geteilt mit** eine **Organisation** aus.</span><span class="sxs-lookup"><span data-stu-id="cc716-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![Inforegister „Geteilt mit“](media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="cc716-131">Geben Sie im Dialogfeld den Domänennamen für die externe Organisation ein und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc716-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![Dialogfeld „Konfigurationsversion für externes Organisation freigeben“](media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="cc716-133">Die Konfiguration wird für die externe Organisation freigegeben und steht dieser Organisation im globalen Repository zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="cc716-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="cc716-134">Von dort kann es in die RCS-Instanz der Organisation oder in deren Instanzen von Finance and Operations-Apps importiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc716-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

6. <span data-ttu-id="cc716-135">Um die Freigabe einer Konfiguration aufzuheben, die zuvor für eine externe Organisation freigegeben wurde, wählen Sie die Konfiguration aus und klicken Sie auf **Freigabe aufheben** und dann **OK**</span><span class="sxs-lookup"><span data-stu-id="cc716-135">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]