---
title: Laden Sie ER-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes herunter
description: In diesem Thema wird erläutert, wie Sie ER-Konfigurationen (Electronic Reporting) aus dem globalen Repository des Konfigurationsdienstes herunterladen.
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ed31cdee74c9db26ba76ed263b5e0578cd04bc3d
ms.sourcegitcommit: 7816902b59aa61d9183d54b50a86e282661e3971
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/02/2020
ms.locfileid: "3421701"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="2da29-103">Laden Sie ER-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes herunter</span><span class="sxs-lookup"><span data-stu-id="2da29-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2da29-104">In diesem Thema wird erläutert, wie Sie [ER-Konfigurationen (Electronic Reporting)](general-electronic-reporting.md#Configuration) aus dem globalen Repository des Konfigurationsdienstes herunterladen.</span><span class="sxs-lookup"><span data-stu-id="2da29-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="2da29-105">Weitere Informationen finden Sie unter [Microsoft Dynamics 365 for Finance and Operations – Regulatory services](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="2da29-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="2da29-106">Konfigurations-Repository öffnen</span><span class="sxs-lookup"><span data-stu-id="2da29-106">Open configurations repository</span></span>

1. <span data-ttu-id="2da29-107">Melden Sie sich bei der Dynamics 365 Finance Anwendung mithilfe der folgenden Rollen an:</span><span class="sxs-lookup"><span data-stu-id="2da29-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="2da29-108">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="2da29-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="2da29-109">Funktionaler Berater für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="2da29-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="2da29-110">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="2da29-110">System administrator</span></span>

2. <span data-ttu-id="2da29-111">Wechseln Sie zu **Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="2da29-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="2da29-112">Wählen Sie im Abschnitt **Konfigurationsanbieter** die Kachel **Microsoft** aus.</span><span class="sxs-lookup"><span data-stu-id="2da29-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="2da29-113">Klicken Sie auf der Kachel **Microsoft** auf **Repositorys**.</span><span class="sxs-lookup"><span data-stu-id="2da29-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![Elektronische Berichterstellung – Arbeitsbereich](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="2da29-115">Auf der Seite **Konfigurationsrepositorys** wählen Sie im Raster ein vorhandenes Repository vom Typ **Global** aus.</span><span class="sxs-lookup"><span data-stu-id="2da29-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="2da29-116">Wenn dieses Repository nicht im Raster angezeigt wird, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="2da29-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="2da29-117">Wählen Sie zum Hinzufügen neuer Repository **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="2da29-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="2da29-118">Wählen Sie **Global** als Repository-Typ, und wählen Sie dann **Repository erstellen**.</span><span class="sxs-lookup"><span data-stu-id="2da29-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="2da29-119">Wenn Sie aufgefordert werden, folgen Sie den Autorisierungsanweisungen.</span><span class="sxs-lookup"><span data-stu-id="2da29-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="2da29-120">Geben Sie einen Namen und eine Beschreibung für das Repository ein und wählen Sie dann **OK**, um den neuen Repository-Eintrag zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="2da29-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="2da29-121">Wählen Sie im Raster das neue Repository vom Typ **Global** aus.</span><span class="sxs-lookup"><span data-stu-id="2da29-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="2da29-122">Wählen Sie **Öffnen**, um die Liste der ER-Konfigurationen für das ausgewählte Repository anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2da29-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![Konfigurationsrepository-Seite](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="2da29-124">Einzelne Konfiguration importieren</span><span class="sxs-lookup"><span data-stu-id="2da29-124">Import a single configuration</span></span>

1. <span data-ttu-id="2da29-125">Auf der Seite **Konfigurations-Repositorys** wählen Sie auf der Seite im Konfigurationsbaum die gewünschte ER-Konfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="2da29-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="2da29-126">Wählen Sie im Inforegister **Versionen** die erforderliche Version der ausgewählten ER-Konfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="2da29-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="2da29-127">Wählen Sie **Importieren**, um die ausgewählte Version vom globalen Repository auf die aktuelle Finance and Operations Instanz herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="2da29-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2da29-128">Die Schaltfläche **Importieren** ist nicht für ER-Konfigurationsversionen verfügbar, die in der aktuellen Instanz bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="2da29-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![Konfigurationsrepository-Seite](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="2da29-130">Importierte Konfigurationen filtern</span><span class="sxs-lookup"><span data-stu-id="2da29-130">Import filtered configurations</span></span>

1. <span data-ttu-id="2da29-131">Auf der Seite **Konfigurations-Repositorys** erweitern Sie im Konfigurationsbaum die Seite **Filter** Infiregister.</span><span class="sxs-lookup"><span data-stu-id="2da29-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="2da29-132">In dem Raster **Stichworte** fügen Sie alle benötigten Tags hinzu.</span><span class="sxs-lookup"><span data-stu-id="2da29-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="2da29-133">In dem Feld **Anwendbarkeit des Landes/der Region** wählen Sie in diesem Feld die entsprechenden Länder-/Regionalcodes aus und wählen Sie dann **Filter anwenden**.</span><span class="sxs-lookup"><span data-stu-id="2da29-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2da29-134">Das Inforegister **Konfigurationen** zeigt alle Konfigurationen an, die die angegebenen Auswahlbedingungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="2da29-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="2da29-135">Auf dem Inforegister **Konfigurationen** wählen Sie **Importieren**, um die gefilterten Konfigurationen aus dem globalen Repository auf die aktuelle Instanz herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="2da29-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="2da29-136">Im Inforegister **Konfigurationen** wählen Sie **Filter zurücksetzen**, um die angegebenen Auswahlbedingungen zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="2da29-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![Konfigurationsrepository-Seite](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="2da29-138">Abhängig von den ER-Einstellungen werden Konfigurationen überprüft, nachdem diese importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="2da29-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="2da29-139">Sie werden über alle Inkonsistenz-Probleme benachrichtigt, die ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="2da29-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="2da29-140">Sie müssen diese Probleme beheben, bevor Sie die importierten Konfigurationsversionen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="2da29-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="2da29-141">Weitere Informationen finden Sie in der Liste der zugehörigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="2da29-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="2da29-142">ER-Konfigurationen können so konfiguriert werden, dass sie von anderen Konfigurationen abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="2da29-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="2da29-143">Daher werden möglicherweise zusammen mit einer ausgewählten Konfiguration andere Konfigurationen automatisch importiert.</span><span class="sxs-lookup"><span data-stu-id="2da29-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="2da29-144">Weitere Informationen zu Konfigurationsabhängigkeiten finden Sie unter [Definieren Sie die Abhängigkeit von ER-Konfigurationen von anderen Komponenten](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span><span class="sxs-lookup"><span data-stu-id="2da29-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2da29-145">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2da29-145">Additional resources</span></span>

[<span data-ttu-id="2da29-146">Überblick über die elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="2da29-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
