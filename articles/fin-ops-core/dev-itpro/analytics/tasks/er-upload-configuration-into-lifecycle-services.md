---
title: Upload einer Konfiguration nach Lifecycle Services
description: Dieses Thema zeigt, wie Sie eine neue Konfiguration zur elektronischen Berichterstellung (EB) erstellen und nach Microsoft Dynamics Lifecycle Services (LCS) hochladen.
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f17763236594092d04dfe2d2f9912e764b4f8d4
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562636"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="6ab6e-103">Upload einer Konfiguration nach Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="6ab6e-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6ab6e-104">In diesem Thema wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ eine neue [Konfiguration für Elektronische Berichterstellung (EB)](../general-electronic-reporting.md#Configuration)  erstellen und in die [Anlagenbibliothek auf Projektebene](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS) hochladen kann.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="6ab6e-105">In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen namens Litware, Inc. und laden Sie in LCS hoch. Diese Schritte können in einem beliebigen Unternehmen abgeschlossen werden, da EB-Konfigurationen unter Unternehmen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-105">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="6ab6e-106">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte in [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-106">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="6ab6e-107">Zugriff auf LCS ist ebenfalls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="6ab6e-108">Melden Sie sich in der Anwendung an, indem Sie eine der folgenden Rollen verwenden:</span><span class="sxs-lookup"><span data-stu-id="6ab6e-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="6ab6e-109">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="6ab6e-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="6ab6e-110">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="6ab6e-110">System administrator</span></span>

2. <span data-ttu-id="6ab6e-111">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="6ab6e-112">Wählen Sie **Litware, Inc.** aus und markieren Sie es als **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-112">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="6ab6e-113">Wählen Sie **Konfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-113">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="6ab6e-114">Stellen Sie sicher, dass der aktuelle Dynamics 365 Finance-Benutzer Mitglied des LCS-Projekts ist, das die [Anlagenbibliothek](../../lifecycle-services/asset-library.md#asset-library-support) enthält, die verwendet wird, um EB-Konfigurationen zu importieren.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-114">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="6ab6e-115">Sie können nicht über ein EB-Repository auf ein LCS-Projekt zugreifen, das eine andere Domäne als die in Finance verwendete Domäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-115">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="6ab6e-116">Wenn Sie dies versuchen, wird eine leere Liste der LCS-Projekte angezeigt, und Sie können keine EB-Konfigurationen aus der Analgenbibliothek auf Projektebene in LCS importieren.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-116">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="6ab6e-117">Um von einem EB-Repository, das zum Importieren von EB-Konfigurationen verwendet wird, auf Analgenbibliotheken auf Projektebene zuzugreifen, melden Sie sich bei Finance an, indem Sie die Anmeldeinformationen eines Benutzers verwenden, der zu dem Mandanten (der Domäne) gehört, für den die aktuelle Finance-Instanz bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-117">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="6ab6e-118">Neue Datenmodellkonfiguration erstellen</span><span class="sxs-lookup"><span data-stu-id="6ab6e-118">Create a new data model configuration</span></span>

1. <span data-ttu-id="6ab6e-119">Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-119">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="6ab6e-120">Wählen Sie auf der Seite **Konfigurationen** **Konfiguration erstellen** aus, um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-120">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="6ab6e-121">In diesem Beispiel erstellen Sie eine Konfiguration, die ein Beispieldatenmodell für elektronische Dokumente enthält.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-121">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="6ab6e-122">Diese Datenmodellkonfiguration wird später in LCS hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-122">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="6ab6e-123">Geben Sie im Feld **Name** die Bezeichnung **Beispielmodellkonfiguration** ein.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-123">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="6ab6e-124">Geben Sie im Feld **Beschreibung** die Bezeichnung **Beispielmodellkonfiguration** ein.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-124">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="6ab6e-125">Wählen Sie **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-125">Select **Create configuration**.</span></span>
6. <span data-ttu-id="6ab6e-126">Wählen Sie **Modelldesigner**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-126">Select **Model designer**.</span></span>
7. <span data-ttu-id="6ab6e-127">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-127">Select **New**.</span></span>
8. <span data-ttu-id="6ab6e-128">Geben Sie im Feld **Name** **Eingabepunkt** ein.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-128">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="6ab6e-129">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-129">Select **Add**.</span></span>
10. <span data-ttu-id="6ab6e-130">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-130">Select **Save**.</span></span>
11. <span data-ttu-id="6ab6e-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-131">Close the page.</span></span>
12. <span data-ttu-id="6ab6e-132">Wählen Sie **Status ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-132">Select **Change status**.</span></span>
13. <span data-ttu-id="6ab6e-133">Wählen Sie **Abgeschlossen** aus.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-133">Select **Complete**.</span></span>
14. <span data-ttu-id="6ab6e-134">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-134">Select **OK**.</span></span>
15. <span data-ttu-id="6ab6e-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-135">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="6ab6e-136">Registrieren eines neuen Repositorys</span><span class="sxs-lookup"><span data-stu-id="6ab6e-136">Register a new repository</span></span>

1. <span data-ttu-id="6ab6e-137">Wechseln Sie zu **Organisationsverwaltung  \>Arbeitsbereiche \>  Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-137">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="6ab6e-138">Wählen Sie im Abschnitt **Konfigurationsanbieter** die Kachel **Litware, Inc.** aus.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-138">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="6ab6e-139">Klicken Sie auf der Kachel **Litware, Inc.** auf **Repositorys**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-139">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="6ab6e-140">Sie können jetzt die Liste der Repositorys für Litware, Inc. als Konfigurationsanbieter öffnen.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-140">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="6ab6e-141">Wählen Sie **Hinzufügen** aus, um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-141">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="6ab6e-142">Sie können jetzt ein neues Repository verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-142">You can now add a new repository.</span></span>

5. <span data-ttu-id="6ab6e-143">Wählen Sie im Feld **Konfigurationsrepository eingeben** die Option **LCS** aus.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-143">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="6ab6e-144">Wählen Sie **Repository erstellen**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-144">Select **Create repository**.</span></span>
7. <span data-ttu-id="6ab6e-145">Geben Sie im Feld **Projekt** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-145">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="6ab6e-146">Wählen Sie für dieses Beispiel das gewünschte LCS-Projekt.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-146">For this example, select the desired LCS project.</span></span> <span data-ttu-id="6ab6e-147">Sie müssen [Zugriff](#accessconditions) auf das Projekt besitzen.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-147">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="6ab6e-148">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-148">Select **OK**.</span></span>

    <span data-ttu-id="6ab6e-149">Schließen Sie einen neuen Repositoryeintrag ab.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-149">Complete a new repository entry.</span></span>

9. <span data-ttu-id="6ab6e-150">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-150">In the list, mark the selected row.</span></span>

    <span data-ttu-id="6ab6e-151">Wählen Sie für dieses Beispiel den **LCS**-Repository-Datensatz aus und öffnen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-151">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="6ab6e-152">Beachten Sie, dass ein registriertes Repository vom aktuellen Anbieter markiert wird.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-152">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="6ab6e-153">Mit anderen Worten, nur Konfigurationen, die diesem Anbieter gehören, können in dieses Repository gestellt und daher in das ausgewählte LCS-Projekt hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-153">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="6ab6e-154">Wählen Sie **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-154">Select **Open**.</span></span>

    <span data-ttu-id="6ab6e-155">Sie öffnen das Repository, um die Liste der EB-Konfigurationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-155">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="6ab6e-156">Wenn das ausgewählte Projekt nicht zum Freigeben von EB-Konfigurationen verwendet wurde, ist die Liste leer.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-156">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="6ab6e-157">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-157">Close the page.</span></span>
12. <span data-ttu-id="6ab6e-158">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-158">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="6ab6e-159">Eine Konfiguration in LCS hochladen</span><span class="sxs-lookup"><span data-stu-id="6ab6e-159">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="6ab6e-160">Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-160">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="6ab6e-161">Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Beispielmodellkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-161">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="6ab6e-162">Sie müssen eine erstellte Konfiguration auswählen, die bereits abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-162">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="6ab6e-163">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-163">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="6ab6e-164">Wählen Sie für dieses Beispiel die Version der ausgewählten Konfiguration aus, die den Status **Abgeschlossen** hat.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-164">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="6ab6e-165">Wählen Sie **Status ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-165">Select **Change status**.</span></span>
5. <span data-ttu-id="6ab6e-166">Wählen Sie **Teilen**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-166">Select **Share**.</span></span>

    <span data-ttu-id="6ab6e-167">Der Status der Konfiguration wird von **Abgeschlossen** zu **Freigegeben** geändert, wenn die Konfiguration in LCS veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-167">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="6ab6e-168">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-168">Select **OK**.</span></span>
7. <span data-ttu-id="6ab6e-169">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-169">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="6ab6e-170">Wählen Sie für dieses Beispiel die Konfigurationsversion aus, die den Status **Freigegeben** hat.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-170">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="6ab6e-171">Beachten Sie, dass der Status der ausgewählten Version von **Abgeschlossen** zu **Freigegeben** geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-171">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="6ab6e-172">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-172">Close the page.</span></span>
9. <span data-ttu-id="6ab6e-173">Wählen Sie **Repositorys** aus.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-173">Select **Repositories**.</span></span>

    <span data-ttu-id="6ab6e-174">Sie können jetzt die Liste der Repositorys für Litware, Inc. als Konfigurationsanbieter öffnen.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-174">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="6ab6e-175">Wählen Sie **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-175">Select **Open**.</span></span>

    <span data-ttu-id="6ab6e-176">Wählen Sie für dieses Beispiel das **LCS**-Repository aus und öffnen Sie es.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-176">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="6ab6e-177">Beachten Sie, dass die ausgewählte Variante als Anlage des ausgewählten LCS-Projekts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-177">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="6ab6e-178">Öffnen Sie LCS, indem Sie zu <https://lcs.dynamics.com> gehen.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-178">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="6ab6e-179">Öffnen Sie ein Projekt, das zuvor für die Repository-Registrierung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-179">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="6ab6e-180">Öffnen Sie die Anlagenbibliothek des Projekts.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-180">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="6ab6e-181">Wählen Sie den **GER-Konfiguration**-Anlagentyp.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-181">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="6ab6e-182">Die von Ihnen hochgeladene EB-Konfiguration sollte aufgelistet sein.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-182">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="6ab6e-183">Beachten Sie, dass die hochgeladene LCS-Konfiguration zu einer anderen Instance werden kann, wenn Anbieter Zugriff auf dieses LCS-Projekt haben.</span><span class="sxs-lookup"><span data-stu-id="6ab6e-183">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]