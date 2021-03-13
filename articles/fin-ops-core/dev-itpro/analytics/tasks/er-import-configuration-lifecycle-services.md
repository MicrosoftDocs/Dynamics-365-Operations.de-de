---
title: Importieren einer Konfiguration von Lifecycle Services
description: In diesem Thema wird beschrieben, wie Sie eine neue Version einer EB-Konfiguration (elektronische Berichterstellung) aus Microsoft Dynamics Lifecycle Services (LCS) importieren.
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 602886b0dd729b8ec52940f42bd1c393dac8acda
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093694"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="0a73b-103">Importieren einer Konfiguration von Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="0a73b-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a73b-104">In diesem Thema wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ eine neue Konfiguration für [Elektronische Berichterstellung (EB)](../general-electronic-reporting.md#Configuration) aus der [Anlagenbibliothek auf Projektebene](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS) importieren kann.</span><span class="sxs-lookup"><span data-stu-id="0a73b-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="0a73b-105">In diesem Beispiel wählen Sie die gewünschte Version der EB-Konfiguration und importieren ein Beispielunternehmen namens Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen abgeschlossen werden, da EB-Konfigurationsanbieter unter allen Unternehmen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="0a73b-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="0a73b-106">Um diese Schritte abzuschließen, müssen Sie zunächst die Schritte in [Eine Konfiguration nach Lifecycle Services hochladen](er-upload-configuration-into-lifecycle-services.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="0a73b-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="0a73b-107">Zugriff auf LCS ist ebenfalls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0a73b-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="0a73b-108">Melden Sie sich in der Anwendung an, indem Sie eine der folgenden Rollen verwenden:</span><span class="sxs-lookup"><span data-stu-id="0a73b-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="0a73b-109">Entwickler für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="0a73b-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="0a73b-110">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="0a73b-110">System administrator</span></span>

2. <span data-ttu-id="0a73b-111">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="0a73b-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="0a73b-112">Wählen Sie **Konfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="0a73b-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="0a73b-113">Stellen Sie sicher, dass der aktuelle Dynamics 365 Finance-Benutzer Mitglied des LCS-Projekts ist, das die Anlagenbibliothek enthält, auf die der Benutzer [Zugriff](../../lifecycle-services/asset-library.md#asset-library-support) erhalten möchte, um EB-Konfigurationen zu importieren.</span><span class="sxs-lookup"><span data-stu-id="0a73b-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="0a73b-114">Sie können nicht über ein EB-Repository auf ein LCS-Projekt zugreifen, das eine andere Domäne als die in Finance verwendete Domäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="0a73b-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="0a73b-115">Wenn Sie dies versuchen, wird eine leere Liste der LCS-Projekte angezeigt, und Sie können keine EB-Konfigurationen aus der Analgenbibliothek auf Projektebene in LCS importieren.</span><span class="sxs-lookup"><span data-stu-id="0a73b-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="0a73b-116">Um von einem EB-Repository, das zum Importieren von EB-Konfigurationen verwendet wird, auf Analgenbibliotheken auf Projektebene zuzugreifen, melden Sie sich bei Finance an, indem Sie die Anmeldeinformationen eines Benutzers verwenden, der zu dem Mandanten (der Domäne) gehört, für den die aktuelle Finance-Instanz bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0a73b-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="0a73b-117">Löschen Sie eine freigegebene Version einer Datenmodellkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0a73b-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="0a73b-118">Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Beispielmodellkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="0a73b-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="0a73b-119">Sie haben die erste Version einer Beispieldaten-Modellkonfiguration erstellt und sie in LCS veröffentlicht, als Sie die Schritte in [Hochladen einer EB-Konfiguration nach Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="0a73b-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="0a73b-120">In dieser Prozedur löschen Sie diese Version der EB-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a73b-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="0a73b-121">Sie werden diese Version später in diesem Thema aus LCS importieren.</span><span class="sxs-lookup"><span data-stu-id="0a73b-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="0a73b-122">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="0a73b-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="0a73b-123">Wählen Sie für dieses Beispiel die Version der Konfiguration aus, die den Status **Freigegeben** hat.</span><span class="sxs-lookup"><span data-stu-id="0a73b-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="0a73b-124">Dieser Status gibt an, dass die Konfiguration nach LCS veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="0a73b-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="0a73b-125">Wählen Sie **Status ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="0a73b-125">Select **Change status**.</span></span>
4. <span data-ttu-id="0a73b-126">Wählen Sie **Nicht fortsetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="0a73b-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="0a73b-127">Indem Sie den Status der ausgewählten Version von **Freigegeben** zu **Eingestellt** ändern, wird die Löschung zur Löschung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0a73b-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="0a73b-128">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a73b-128">Select **OK**.</span></span>
6. <span data-ttu-id="0a73b-129">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="0a73b-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="0a73b-130">Wählen Sie für dieses Beispiel die Version der Konfiguration aus, die den Status **Eingestellt** hat.</span><span class="sxs-lookup"><span data-stu-id="0a73b-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="0a73b-131">Wählen Sei **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="0a73b-131">Select **Delete**.</span></span>
8. <span data-ttu-id="0a73b-132">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="0a73b-132">Select **Yes**.</span></span>

    <span data-ttu-id="0a73b-133">Beachten Sie, dass die einzige Entwurfsversion 2 der ausgewählten Datenmodellkonfiguration jetzt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0a73b-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="0a73b-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0a73b-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="0a73b-135">Importieren Sie eine freigegebene Version einer Datenmodellkonfiguration von LCS</span><span class="sxs-lookup"><span data-stu-id="0a73b-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="0a73b-136">Wechseln Sie zu **Organisationsverwaltung  \>Arbeitsbereiche \>  Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="0a73b-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="0a73b-137">Wählen Sie im Abschnitt **Konfigurationsanbieter** die Kachel **Litware, Inc.** aus.</span><span class="sxs-lookup"><span data-stu-id="0a73b-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="0a73b-138">Klicken Sie auf der Kachel **Litware, Inc.** auf **Repositorys**.</span><span class="sxs-lookup"><span data-stu-id="0a73b-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="0a73b-139">Sie können jetzt die Liste der Repositorys für Litware, Inc. als Konfigurationsanbieter öffnen.</span><span class="sxs-lookup"><span data-stu-id="0a73b-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="0a73b-140">Wählen Sie **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="0a73b-140">Select **Open**.</span></span>

    <span data-ttu-id="0a73b-141">Wählen Sie für dieses Beispiel das **LCS**-Repository aus und öffnen Sie es.</span><span class="sxs-lookup"><span data-stu-id="0a73b-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="0a73b-142">Sie benötigen [Zugriff](#accessconditions) auf das LCS-Projekt und zur Anlagenbibliothek, auf die das ausgewählte EB-Repository zugreift.</span><span class="sxs-lookup"><span data-stu-id="0a73b-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="0a73b-143">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="0a73b-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="0a73b-144">Wählen Sie für dieses Beispiel die erste Version der **Beispielmodellkonfiguration** in der Versionsliste aus.</span><span class="sxs-lookup"><span data-stu-id="0a73b-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="0a73b-145">**Import** auswählen</span><span class="sxs-lookup"><span data-stu-id="0a73b-145">Select **Import**.</span></span>
7. <span data-ttu-id="0a73b-146">Wählen Sie **Ja**, um den Import der ausgewählten Version von LCS nach Dynamics AX zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="0a73b-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="0a73b-147">Eine Informationsnachricht bestätigt, dass die ausgewählte Version erfolgreich importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0a73b-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="0a73b-148">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0a73b-148">Close the page.</span></span>
9. <span data-ttu-id="0a73b-149">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0a73b-149">Close the page.</span></span>
10. <span data-ttu-id="0a73b-150">Wählen Sie **Konfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="0a73b-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="0a73b-151">Wählen Sie in der Struktur **Beispielmodellkonfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="0a73b-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="0a73b-152">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="0a73b-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="0a73b-153">Wählen Sie für dieses Beispiel die Version der Konfiguration aus, die den Status **Freigegeben** hat.</span><span class="sxs-lookup"><span data-stu-id="0a73b-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="0a73b-154">Beachten Sie, dass die freigegebene Version 1 der ausgewählten Datenmodellkonfiguration ebenfalls verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0a73b-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>
