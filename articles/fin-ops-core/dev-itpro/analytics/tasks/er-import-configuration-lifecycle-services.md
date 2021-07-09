---
title: Importieren einer Konfiguration von Lifecycle Services
description: In diesem Thema wird beschrieben, wie Sie eine neue Version einer EB-Konfiguration (elektronische Berichterstellung) aus Microsoft Dynamics Lifecycle Services (LCS) importieren.
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270836"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="89764-103">Importieren einer Konfiguration von Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="89764-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="89764-104">In diesem Thema wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ eine neue Konfiguration für [Elektronische Berichterstellung (EB)](../general-electronic-reporting.md#Configuration) aus der [Anlagenbibliothek auf Projektebene](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS) importieren kann.</span><span class="sxs-lookup"><span data-stu-id="89764-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89764-105">Die Verwendung von LCS als Speicherort für ER-Konfigurationen wird [veraltet](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="89764-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="89764-106">Weitere Informationen finden Sie unter [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="89764-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="89764-107">In diesem Beispiel wählen Sie die gewünschte Version der EB-Konfiguration und importieren ein Beispielunternehmen namens Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen abgeschlossen werden, da EB-Konfigurationsanbieter unter allen Unternehmen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="89764-107">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="89764-108">Um diese Schritte abzuschließen, müssen Sie zunächst die Schritte in [Eine Konfiguration nach Lifecycle Services hochladen](er-upload-configuration-into-lifecycle-services.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="89764-108">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="89764-109">Zugriff auf LCS ist ebenfalls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="89764-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="89764-110">Melden Sie sich in der Anwendung an, indem Sie eine der folgenden Rollen verwenden:</span><span class="sxs-lookup"><span data-stu-id="89764-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="89764-111">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="89764-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="89764-112">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="89764-112">System administrator</span></span>

2. <span data-ttu-id="89764-113">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="89764-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="89764-114">Wählen Sie **Konfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="89764-114">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="89764-115">Stellen Sie sicher, dass der aktuelle Dynamics 365 Finance-Benutzer Mitglied des LCS-Projekts ist, das die Anlagenbibliothek enthält, auf die der Benutzer [Zugriff](../../lifecycle-services/asset-library.md#asset-library-support) erhalten möchte, um EB-Konfigurationen zu importieren.</span><span class="sxs-lookup"><span data-stu-id="89764-115">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="89764-116">Sie können nicht über ein EB-Repository auf ein LCS-Projekt zugreifen, das eine andere Domäne als die in Finance verwendete Domäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="89764-116">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="89764-117">Wenn Sie dies versuchen, wird eine leere Liste der LCS-Projekte angezeigt, und Sie können keine EB-Konfigurationen aus der Analgenbibliothek auf Projektebene in LCS importieren.</span><span class="sxs-lookup"><span data-stu-id="89764-117">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="89764-118">Um von einem EB-Repository, das zum Importieren von EB-Konfigurationen verwendet wird, auf Analgenbibliotheken auf Projektebene zuzugreifen, melden Sie sich bei Finance an, indem Sie die Anmeldeinformationen eines Benutzers verwenden, der zu dem Mandanten (der Domäne) gehört, für den die aktuelle Finance-Instanz bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="89764-118">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="89764-119">Löschen Sie eine freigegebene Version einer Datenmodellkonfiguration</span><span class="sxs-lookup"><span data-stu-id="89764-119">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="89764-120">Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Beispielmodellkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="89764-120">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="89764-121">Sie haben die erste Version einer Beispieldaten-Modellkonfiguration erstellt und sie in LCS veröffentlicht, als Sie die Schritte in [Hochladen einer EB-Konfiguration nach Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="89764-121">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="89764-122">In dieser Prozedur löschen Sie diese Version der EB-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="89764-122">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="89764-123">Sie werden diese Version später in diesem Thema aus LCS importieren.</span><span class="sxs-lookup"><span data-stu-id="89764-123">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="89764-124">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="89764-124">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="89764-125">Wählen Sie für dieses Beispiel die Version der Konfiguration aus, die den Status **Freigegeben** hat.</span><span class="sxs-lookup"><span data-stu-id="89764-125">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="89764-126">Dieser Status gibt an, dass die Konfiguration nach LCS veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="89764-126">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="89764-127">Wählen Sie **Status ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="89764-127">Select **Change status**.</span></span>
4. <span data-ttu-id="89764-128">Wählen Sie **Nicht fortsetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="89764-128">Select **Discontinue**.</span></span>

    <span data-ttu-id="89764-129">Indem Sie den Status der ausgewählten Version von **Freigegeben** zu **Eingestellt** ändern, wird die Löschung zur Löschung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="89764-129">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="89764-130">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="89764-130">Select **OK**.</span></span>
6. <span data-ttu-id="89764-131">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="89764-131">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="89764-132">Wählen Sie für dieses Beispiel die Version der Konfiguration aus, die den Status **Eingestellt** hat.</span><span class="sxs-lookup"><span data-stu-id="89764-132">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="89764-133">Wählen Sei **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="89764-133">Select **Delete**.</span></span>
8. <span data-ttu-id="89764-134">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="89764-134">Select **Yes**.</span></span>

    <span data-ttu-id="89764-135">Beachten Sie, dass die einzige Entwurfsversion 2 der ausgewählten Datenmodellkonfiguration jetzt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="89764-135">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="89764-136">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="89764-136">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="89764-137">Importieren Sie eine freigegebene Version einer Datenmodellkonfiguration von LCS</span><span class="sxs-lookup"><span data-stu-id="89764-137">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="89764-138">Wechseln Sie zu **Organisationsverwaltung  \>Arbeitsbereiche \>  Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="89764-138">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="89764-139">Wählen Sie im Abschnitt **Konfigurationsanbieter** die Kachel **Litware, Inc.** aus.</span><span class="sxs-lookup"><span data-stu-id="89764-139">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="89764-140">Klicken Sie auf der Kachel **Litware, Inc.** auf **Repositorys**.</span><span class="sxs-lookup"><span data-stu-id="89764-140">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="89764-141">Sie können jetzt die Liste der Repositorys für Litware, Inc. als Konfigurationsanbieter öffnen.</span><span class="sxs-lookup"><span data-stu-id="89764-141">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="89764-142">Wählen Sie **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="89764-142">Select **Open**.</span></span>

    <span data-ttu-id="89764-143">Wählen Sie für dieses Beispiel das **LCS**-Repository aus und öffnen Sie es.</span><span class="sxs-lookup"><span data-stu-id="89764-143">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="89764-144">Sie benötigen [Zugriff](#accessconditions) auf das LCS-Projekt und zur Anlagenbibliothek, auf die das ausgewählte EB-Repository zugreift.</span><span class="sxs-lookup"><span data-stu-id="89764-144">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="89764-145">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="89764-145">In the list, mark the selected row.</span></span>

    <span data-ttu-id="89764-146">Wählen Sie für dieses Beispiel die erste Version der **Beispielmodellkonfiguration** in der Versionsliste aus.</span><span class="sxs-lookup"><span data-stu-id="89764-146">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="89764-147">**Import** auswählen</span><span class="sxs-lookup"><span data-stu-id="89764-147">Select **Import**.</span></span>
7. <span data-ttu-id="89764-148">Wählen Sie **Ja**, um den Import der ausgewählten Version von LCS nach Dynamics AX zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="89764-148">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="89764-149">Eine Informationsnachricht bestätigt, dass die ausgewählte Version erfolgreich importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="89764-149">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="89764-150">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="89764-150">Close the page.</span></span>
9. <span data-ttu-id="89764-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="89764-151">Close the page.</span></span>
10. <span data-ttu-id="89764-152">Wählen Sie **Konfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="89764-152">Select **Configurations**.</span></span>
11. <span data-ttu-id="89764-153">Wählen Sie in der Struktur **Beispielmodellkonfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="89764-153">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="89764-154">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="89764-154">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="89764-155">Wählen Sie für dieses Beispiel die Version der Konfiguration aus, die den Status **Freigegeben** hat.</span><span class="sxs-lookup"><span data-stu-id="89764-155">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="89764-156">Beachten Sie, dass die freigegebene Version 1 der ausgewählten Datenmodellkonfiguration ebenfalls verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="89764-156">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
