---
title: Laden Sie die elektronische Berichtskonfigurationen der Lifecycle Services herunter
description: Dieses Thema zeigt, wie Sie Konfigurationen zur elektronischen Berichterstellung (EB) von Microsoft Dynamics Lifecycle Services (LCS) herunterladen.
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 14f0f2b1a4d63101d432b1361379c61a70ac9345
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271182"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="c61c9-103">Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen</span><span class="sxs-lookup"><span data-stu-id="c61c9-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c61c9-104">In diesem Thema wird erläutert, wie Sie die neueste Version der [Konfigurationen für elektronische Berichte (EB)](general-electronic-reporting.md#Configuration) aus der [Bibliothek für freigegebene Anlagen](../lifecycle-services/asset-library.md) in den Microsoft Dynamics Lifecycle Services (LCS) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="c61c9-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c61c9-105">Die Verwendung von LCS als Speicher-Repository für ER-Konfigurationen wird [außer Betrieb genommen](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="c61c9-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="c61c9-106">Weitere Informationen finden Sie unter [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="c61c9-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

1. <span data-ttu-id="c61c9-107">Melden Sie sich in der Anwendung an, indem Sie eine der folgenden Rollen verwenden:</span><span class="sxs-lookup"><span data-stu-id="c61c9-107">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="c61c9-108">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="c61c9-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="c61c9-109">Funktionaler Berater für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="c61c9-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="c61c9-110">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="c61c9-110">System administrator</span></span>

2. <span data-ttu-id="c61c9-111">Wechseln Sie zu **Organisationsverwaltung** &gt; **Arbeitsbereiche** &gt; **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="c61c9-111">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="c61c9-112">Wählen Sie im Abschnitt **Konfigurationsanbieter** die Kachel **Microsoft** aus.</span><span class="sxs-lookup"><span data-stu-id="c61c9-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="c61c9-113">Klicken Sie auf der Kachel **Microsoft** auf **Repositorys**.</span><span class="sxs-lookup"><span data-stu-id="c61c9-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="c61c9-114">[![Microsoft-Kachel auf der Seite für Lokalisierungskonfigurationen](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="c61c9-114">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="c61c9-115">Auf der Seite **Konfigurationsrepositorys** wählen Sie im Raster ein vorhandenes Repository vom Typ **LCS** aus.</span><span class="sxs-lookup"><span data-stu-id="c61c9-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="c61c9-116">Wenn dieses Repository nicht im Raster angezeigt wird, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="c61c9-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="c61c9-117">Wählen Sie zum Hinzufügen eines Repositorys **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c61c9-117">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="c61c9-118">Aktivieren Sie **LCS** als Repository-Typ.</span><span class="sxs-lookup"><span data-stu-id="c61c9-118">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="c61c9-119">Wählen Sie **Repository erstellen**.</span><span class="sxs-lookup"><span data-stu-id="c61c9-119">Select **Create repository**.</span></span>
    4. <span data-ttu-id="c61c9-120">Wenn Sie zur Autorisierung aufgefordert werden, befolgen Sie die Anweisungen auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="c61c9-120">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="c61c9-121">Geben Sie einen Namen und eine Beschreibung für das Repository ein.</span><span class="sxs-lookup"><span data-stu-id="c61c9-121">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="c61c9-122">Wählen Sie **OK**, um den neuen Repositoryeintrag zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="c61c9-122">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="c61c9-123">Wählen Sie im Raster das neue Repository vom Typ **LCS** aus.</span><span class="sxs-lookup"><span data-stu-id="c61c9-123">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="c61c9-124">Wählen Sie **Öffnen**, um die Liste der ER-Konfigurationen für das ausgewählte Repository anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c61c9-124">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="c61c9-125">[![Konfigurationsrepository-Seite](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="c61c9-125">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="c61c9-126">Wenn Sie Probleme beim Zugriff auf das LCS-Repository haben, um Konfigurationen aus der Bibliothek für freigegebene Anlagen in LCS herunterzuladen, können Sie stattdessen Konfigurationen aus dem [globalen Repository](er-download-configurations-global-repo.md) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="c61c9-126">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="c61c9-127">Wählen Sie in der Konfigurationsstruktur im linken Bereich die erforderliche EB-Konfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="c61c9-127">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="c61c9-128">Wählen Sie im Inforegister **Versionen** die erforderliche Version der ausgewählten ER-Konfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="c61c9-128">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="c61c9-129">Wählen Sie **Importieren**, um die ausgewählte Version vom LCS auf die aktuelle Instanz herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="c61c9-129">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c61c9-130">Die Schaltfläche **Importieren** ist nicht für ER-Konfigurationsversionen verfügbar, die in der aktuellen Instanz bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c61c9-130">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="c61c9-131">[![Konfigurationsrepository-Seite](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="c61c9-131">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="c61c9-132">Abhängig von den ER-Einstellungen werden Konfigurationen überprüft, nachdem diese importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c61c9-132">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="c61c9-133">Sie werden über alle Inkonsistenz-Probleme benachrichtigt, die ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="c61c9-133">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="c61c9-134">Sie müssen diese Probleme beheben, bevor Sie die importierten Konfigurationsversionen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c61c9-134">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="c61c9-135">Weitere Informationen finden Sie in der Liste der zugehörigen Themen.</span><span class="sxs-lookup"><span data-stu-id="c61c9-135">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c61c9-136">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c61c9-136">Additional resources</span></span>

[<span data-ttu-id="c61c9-137">Überblick über die elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="c61c9-137">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="c61c9-138">Laden Sie ER-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes herunter</span><span class="sxs-lookup"><span data-stu-id="c61c9-138">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
