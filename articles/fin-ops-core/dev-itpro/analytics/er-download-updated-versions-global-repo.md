---
title: Importieren von aktualisierten Versionen von EB-Konfigurationen
description: In diesem Thema wird erläutert, wie Sie aktualisierte Versionen von EB-Konfigurationen (Elektronische Berichterstellung) aus dem globalen Repository des Konfigurationsdienstes importieren.
author: NickSelin
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 1e021105c19273db5ded7cb0902eca1d502ced8e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753359"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="8a525-103">Importieren von aktualisierten Versionen von EB-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="8a525-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a525-104">[Repositorys](general-electronic-reporting.md#Repository) für die elektronische Berichterstattung (EB) werden verwendet, um [EB-Konfigurationen](general-electronic-reporting.md#Configuration) freizugeben.</span><span class="sxs-lookup"><span data-stu-id="8a525-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="8a525-105">[Importieren](download-electronic-reporting-configuration-lcs.md) Sie EB-Konfigurationen aus verschiedenen Repositorys in Ihre Instanz von Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="8a525-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="8a525-106">Wenn Sie EB-Konfigurationen importieren, können [Konfigurationsanbieter](general-electronic-reporting.md#Provider) Repositorys mit neuen [Versionen](general-electronic-reporting.md#component-versioning) veröffentlichen, damit sie freigegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="8a525-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="8a525-107">In diesem Thema wird erläutert, wie Sie aktualisierte Versionen von EB-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes importieren.</span><span class="sxs-lookup"><span data-stu-id="8a525-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="8a525-108">Weitere Informationen finden Sie unter [Microsoft Dynamics 365 for Finance and Operations – Regulatory services](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="8a525-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="8a525-109">Überprüfen der verfügbaren aktualisierten Versionen</span><span class="sxs-lookup"><span data-stu-id="8a525-109">Review the available updated versions</span></span>

1. <span data-ttu-id="8a525-110">Melden Sie sich bei Finance an, indem Sie eine der folgenden Rollen verwenden:</span><span class="sxs-lookup"><span data-stu-id="8a525-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="8a525-111">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="8a525-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="8a525-112">Funktionaler Berater für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="8a525-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="8a525-113">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="8a525-113">System administrator</span></span>

2. <span data-ttu-id="8a525-114">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="8a525-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="8a525-115">Auf der Seite **Lokalisierungskonfigurationen** wählen Sie im Bereich **Zugehörige Links** die Option **Aktualisierte Versionen von Konfigurationen importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="8a525-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![Seite „Lokalisierungskonfigurationen“](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="8a525-117">Wählen Sie im Dialogfeld **Aktualisierte Versionen von elektronischen Berichtskonfigurationen importieren** im Feld **Ausführungsmodus** die Option **Nur verfügbare Updates anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="8a525-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="8a525-118">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="8a525-118">Then select **OK**.</span></span> 

    ![Feld „Ausführungsmodus“ auf „Nur verfügbare Updates anzeigen“ eingestellt](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="8a525-120">Überprüfen Sie die Meldungen, die angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8a525-120">Review the messages that you receive.</span></span> <span data-ttu-id="8a525-121">Diese Meldungen enthalten die folgenden Informationen zu den EB-Konfigurationen in der aktuellen Finance-Instanz und zu Unterschieden zum Inhalt des globalen Repositorys:</span><span class="sxs-lookup"><span data-stu-id="8a525-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="8a525-122">Die Gesamtzahl der EB-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="8a525-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="8a525-123">EB-Konfigurationen, die nicht im globalen Repository vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="8a525-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="8a525-124">EB-Konfigurationen, für die die neueste Version bereits in der aktuellen Finance-Instanz verfügbar ist (Um die vollständige Liste dieser EB-Konfigurationen anzuzeigen, wählen Sie den Link **Meldungsdetails** aus.)</span><span class="sxs-lookup"><span data-stu-id="8a525-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Meldung „Neueste Versionen der folgenden Konfigurationen sind bereits importiert“ und Meldungsdetails](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="8a525-126">EB-Konfigurationen, für die die neueste Version im globalen Repository verfügbar ist und in die aktuelle Finance-Instanz importiert werden kann (Um die vollständige Liste dieser EB-Konfigurationen anzuzeigen, wählen Sie den Link **Meldungsdetails** aus.)</span><span class="sxs-lookup"><span data-stu-id="8a525-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Meldung „Verfügbare Updates“ und Meldungsdetails](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="8a525-128">Importieren verfügbarer aktualisierter Versionen</span><span class="sxs-lookup"><span data-stu-id="8a525-128">Import available updated versions</span></span>

1. <span data-ttu-id="8a525-129">Melden Sie sich bei Finance an, indem Sie eine der folgenden Rollen verwenden:</span><span class="sxs-lookup"><span data-stu-id="8a525-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="8a525-130">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="8a525-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="8a525-131">Funktionaler Berater für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="8a525-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="8a525-132">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="8a525-132">System administrator</span></span>

2. <span data-ttu-id="8a525-133">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="8a525-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="8a525-134">Auf der Seite **Lokalisierungskonfigurationen** wählen Sie im Bereich **Zugehörige Links** die Option **Aktualisierte Versionen von Konfigurationen importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="8a525-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="8a525-135">Wählen Sie im Dialogfeld **Aktualisierte Versionen von elektronischen Berichtskonfigurationen importieren** im Feld **Ausführungsmodus** die Option **Neueste Updates importieren** aus, um die neuesten Versionen von EB-Konfigurationen aus dem globalen Repository in die aktuelle Finance-Instanz zu importieren.</span><span class="sxs-lookup"><span data-stu-id="8a525-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="8a525-136">Um einen Batchauftrag für den Import zu planen, legen Sie auf dem Inforegister **Im Hintergrund ausführen** die Option **Batchverarbeitung** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="8a525-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="8a525-137">Wenn Sie den Import regelmäßig wiederholen möchten, konfigurieren Sie die erforderliche Wiederholung.</span><span class="sxs-lookup"><span data-stu-id="8a525-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![Feld „Ausführungsmodus“ ist auf „Neueste Updates importieren“ festgelegt](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="8a525-139">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a525-139">Select **OK**.</span></span>
7. <span data-ttu-id="8a525-140">Führen Sie einen der folgenden Schritte aus, um zu erfahren, welche Konfigurationsversionen importiert wurden:</span><span class="sxs-lookup"><span data-stu-id="8a525-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="8a525-141">Wenn Sie den Import interaktiv ausführen und keinen Batchauftrag verwenden, überprüfen Sie die angezeigten Meldungen.</span><span class="sxs-lookup"><span data-stu-id="8a525-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![Während einer interaktiven Importausführung eingehende Meldungen](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="8a525-143">Wenn Sie den Import im Batchmodus ausführen, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="8a525-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="8a525-144">Wechseln Sie zu **Allgemeines** \> **Anfragen** \> **Batchaufträge** \> **Meine Batchaufträge**.</span><span class="sxs-lookup"><span data-stu-id="8a525-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="8a525-145">Suchen Sie den Auftrag **Aktualisierte Versionen von elektronischen Berichtskonfigurationen importieren** und wählen Sie ihn aus. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Batchauftrag** die Option **Batchauftrag-Historie** aus, um die Historie des Auftrags anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8a525-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="8a525-146">Wählen Sie auf der Seite **Batchauftrag-Historie** die Option **Protokoll** aus.</span><span class="sxs-lookup"><span data-stu-id="8a525-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="8a525-147">Wählen Sie dann in der angezeigten Meldung den Link **Meldungsdetails** aus, um das Auftragsprotokoll anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8a525-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![Auftragsprotokoll](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="8a525-149">Es wird nicht empfohlen, einen sich wiederholenden Batchauftrag zu planen, um aktualisierte Versionen von EB-Konfigurationen direkt aus dem globalen Repository in eine Produktionsumgebung zu importieren, da die importierten Versionen sofort zur Verwendung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8a525-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="8a525-150">Verwenden Sie diesen Ansatz stattdessen, um Versionen von EB-Konfigurationen in einer Sandbox-Umgebung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8a525-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="8a525-151">Sie können dann vor der Bereitstellung in einer Produktionsumgebung in der Sandbox-Umgebung ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="8a525-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a525-152">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8a525-152">Additional resources</span></span>

- [<span data-ttu-id="8a525-153">Überblick über die elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="8a525-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="8a525-154">Laden Sie ER-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes herunter</span><span class="sxs-lookup"><span data-stu-id="8a525-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]