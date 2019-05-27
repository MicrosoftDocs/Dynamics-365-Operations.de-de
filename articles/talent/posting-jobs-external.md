---
title: Stellen aus Attract auf externen Karrierewebsites veröffentlichen
description: In diesem Thema wird erläutert, wie Dynamics 365 for Talent - Attract verwendet wird, um Stelle auf externe Stellenportalen zu veröffentlichen
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518093"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="c6e86-103">Stellen aus Attract auf externen Karrierewebsites veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="c6e86-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6e86-104">Sie möchten die offenen Stellen für möglichst viele qualifizierten Kandidaten bekannt machen.</span><span class="sxs-lookup"><span data-stu-id="c6e86-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="c6e86-105">Stellenportale wie Broadbean helfen Ihnen dabei</span><span class="sxs-lookup"><span data-stu-id="c6e86-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="c6e86-106">Microsoft Dynamics 365 Talent: Mit Attract können Sie nune Stellen auf Broadbean veröffentlichen und Microsoft ist ständig daran, neue Angebote in diesem Bereich bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c6e86-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="c6e86-107">Stellen auf Broadbean veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="c6e86-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="c6e86-108">Bevor Stellen in Broadbean gebucht werden können, müssen Sie die Broadbean-Integration konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c6e86-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="c6e86-109">Um Stellen an externen Standorten zu buchen, müssen Sie das [Umfassende Einstellungsadd-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) haben.</span><span class="sxs-lookup"><span data-stu-id="c6e86-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="c6e86-110">Diese Funktion befindet sich derzeit in der Vorschau.</span><span class="sxs-lookup"><span data-stu-id="c6e86-110">This feature is currently in preview.</span></span> <span data-ttu-id="c6e86-111">Wenn Sie sie ausprobieren möchten, müssen Sie [sie in den Attract-Administratoreinstellungen aktivieren](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) auf.</span><span class="sxs-lookup"><span data-stu-id="c6e86-111">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="c6e86-112">Broadbean-Integration konfigurieren</span><span class="sxs-lookup"><span data-stu-id="c6e86-112">Configure Broadbean integration</span></span>

1. <span data-ttu-id="c6e86-113">Bei Attract als Administrator anmelden.</span><span class="sxs-lookup"><span data-stu-id="c6e86-113">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="c6e86-114">Wählen Sie die Schaltfläche **Einstellungen** (das Rad-Symbol) in der rechten oberen Ecke der Seite aus, und wählen Sie dann **Administratorcenter**.</span><span class="sxs-lookup"><span data-stu-id="c6e86-114">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="c6e86-115">In der Registerkarte **Stellenbörseeinstellungen** im Abschnitt **Broadbeanintegration aktivieren**, aktivieren Sie die Integration.</span><span class="sxs-lookup"><span data-stu-id="c6e86-115">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="c6e86-116">Broadbean kontaktieren und die Informationen in **Benutzername, Client-ID, Verschlüsselungs-Token** eingeben.</span><span class="sxs-lookup"><span data-stu-id="c6e86-116">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="c6e86-117">Ihre Broadbean-Anmeldeinformationen sind vertraulich.</span><span class="sxs-lookup"><span data-stu-id="c6e86-117">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="c6e86-118">Daher müssen Sie diese sicher und verantwortungsvoll speichern.</span><span class="sxs-lookup"><span data-stu-id="c6e86-118">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="c6e86-119">Alle, die eine Administratorrolle in Attract haben, können diese Anmeldeinformationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c6e86-119">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="c6e86-120">Microsoft und Attract sind nicht involviert beim Erstellen und Verwalten dieser Werte.</span><span class="sxs-lookup"><span data-stu-id="c6e86-120">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="c6e86-121">Es ist Ihre Verantwortung, sie in Attract auf dem neuesten Stand zu halten und mit Broabean zusammen zu arbeiten, um Probleme zu beheben, die Ihre Anmeldeinformationen umfassen.</span><span class="sxs-lookup"><span data-stu-id="c6e86-121">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="c6e86-122">Eine Stelle auf Broadbean veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="c6e86-122">Post a job to Broadbean</span></span>

<span data-ttu-id="c6e86-123">Nachdem Broadbean aktiviert wurde, können Personaleschaffungsmanager und Administratoren Stellen darauf veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="c6e86-123">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="c6e86-124">Sie müssen eine URL für die Stelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6e86-124">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="c6e86-125">Öffnen Sie in Attract die Stelle, die Sie in Broadbean veröffentlichen möchten.</span><span class="sxs-lookup"><span data-stu-id="c6e86-125">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="c6e86-126">Im Abschnitt **Veröfffentlichungen** wählen Sie die Schaltfläche **Jetzt veröffentlichen** aus, die Broadbean entspricht.</span><span class="sxs-lookup"><span data-stu-id="c6e86-126">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="c6e86-127">Folgen Sie den Anweisunge im Broadbea Fenster.</span><span class="sxs-lookup"><span data-stu-id="c6e86-127">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="c6e86-128">Attract leitet folgenden Informationen an Broadbean weiter:</span><span class="sxs-lookup"><span data-stu-id="c6e86-128">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="c6e86-129">Anforderungskennung</span><span class="sxs-lookup"><span data-stu-id="c6e86-129">Request ID</span></span>
- <span data-ttu-id="c6e86-130">Stellenbezeichnung</span><span class="sxs-lookup"><span data-stu-id="c6e86-130">Job title</span></span>
- <span data-ttu-id="c6e86-131">Einzelvorgangsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="c6e86-131">Job description</span></span>
- <span data-ttu-id="c6e86-132">Arbeitsort</span><span class="sxs-lookup"><span data-stu-id="c6e86-132">Job location</span></span>
- <span data-ttu-id="c6e86-133">URL anwenden</span><span class="sxs-lookup"><span data-stu-id="c6e86-133">Apply URL</span></span>
- <span data-ttu-id="c6e86-134">Informationen zum Personalbeschaffungsmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="c6e86-134">Recruiter information</span></span>

<span data-ttu-id="c6e86-135">Nachdem Broadbean die Veröffentlichung erfolgreich abgeschlossen hat, zeigt der Abschnitt **Veröffentlichung** der Stelle in Attract den Broadbean Status als **veröffentlicht**.</span><span class="sxs-lookup"><span data-stu-id="c6e86-135">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="c6e86-136">Broadbean erfordert das Feld **Branche**.</span><span class="sxs-lookup"><span data-stu-id="c6e86-136">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="c6e86-137">Zurzeit ist dieses Feld standardmäßig auf **IT** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c6e86-137">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="c6e86-138">Sie können den Wert jedoch im Fenster für die Broadbean Stellenveröffentlichung auf die richtige Branche anpassen.</span><span class="sxs-lookup"><span data-stu-id="c6e86-138">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="c6e86-139">Es dauert einige Zeit, bis Broadbean die Veröffentlichung Ihrer Stelle in allen Stellenportalen, die Sie ausgewählt haben, abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="c6e86-139">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="c6e86-140">Daher kann es möglicherweise eine geringfügige Verzögerung geben, bevor Attract eine Statusaktualisierung für die Stelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c6e86-140">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="c6e86-141">Eine Broadbean Stellenausschreibung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c6e86-141">View a Broadbean job posting</span></span>

<span data-ttu-id="c6e86-142">Nachdem Sie eine Stelle in Broadbean veröffentlich haben, können Sie diese über Attract ansehen.</span><span class="sxs-lookup"><span data-stu-id="c6e86-142">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="c6e86-143">Öffnen Sie in Attract die Stelle, die Sie in Broadbean anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="c6e86-143">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="c6e86-144">Im Abschnitt **Stelle** wählen Sie die Ellipsenschaltfläche (**...**), die Broadbean entspricht und wählen Sie  dann **Ansicht** aus.</span><span class="sxs-lookup"><span data-stu-id="c6e86-144">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="c6e86-145">Die Broadbean Stellenausschreibung wird in einem neuen Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6e86-145">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="c6e86-146">Eine Broadbean Stellenausschreibung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c6e86-146">Update a Broadbean job posting</span></span>

<span data-ttu-id="c6e86-147">Sie können eine Broadbean Stellenausschreibung auf zwei Arten aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c6e86-147">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="c6e86-148">In Attract öffnen Sie die Stelle, die Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="c6e86-148">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="c6e86-149">Im Abschnitt **Veröfffentlichungen** wählen Sie die Schaltfläche **Veröffentlichung aktualisieren**, die Broadbean entspricht.</span><span class="sxs-lookup"><span data-stu-id="c6e86-149">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="c6e86-150">Bearbeiten Sie die Veröffentlichung im Fenster Broadbean.</span><span class="sxs-lookup"><span data-stu-id="c6e86-150">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="c6e86-151">- oder -</span><span class="sxs-lookup"><span data-stu-id="c6e86-151">–or–</span></span>

1. <span data-ttu-id="c6e86-152">Öffnen Sie in Attract die Stelle, die Sie in Broadbean anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="c6e86-152">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="c6e86-153">Im Abschnitt **Stelle** wählen Sie die Ellipsenschaltfläche (**...**), die Broadbean entspricht und wählen Sie  dann **Ansicht** aus.</span><span class="sxs-lookup"><span data-stu-id="c6e86-153">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="c6e86-154">Im Fenster Broadbean bearbeiten Sie die Stellendetails und veröffentlichen die Stelle erneut.</span><span class="sxs-lookup"><span data-stu-id="c6e86-154">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="c6e86-155">Die Stellendetails in Attract sind unverändert.</span><span class="sxs-lookup"><span data-stu-id="c6e86-155">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="c6e86-156">Entfernen einer Broadbean Stellenausschreibung</span><span class="sxs-lookup"><span data-stu-id="c6e86-156">Remove a Broadbean job posting</span></span>

<span data-ttu-id="c6e86-157">Sie können eine Stellenausschreibung aus Broadbean wieder entfernen.</span><span class="sxs-lookup"><span data-stu-id="c6e86-157">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="c6e86-158">In Attract öffnen Sie die Stelle, die Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="c6e86-158">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="c6e86-159">Im Abschnitt **Stelle** wählen Sie die Ellipsenschaltfläche (**...**), die Broadbean entspricht und wählen Sie  dann **Stelle entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="c6e86-159">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="c6e86-160">Nachdem Broadbean die Stelle entfernt hat, hat das Broadbean Element in Attact eine Schaltfläche **Jetzt veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="c6e86-160">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="c6e86-161">Das Vorhandensein dieser Schaltfläche gibt an, dass die Stelle entfernt wurde und erneut gebucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="c6e86-161">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="c6e86-162">Problembehandlung bei der Broadbean Integration</span><span class="sxs-lookup"><span data-stu-id="c6e86-162">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="c6e86-163">Wenn Sie Probleme haben, eine Stelle in Broadbean zu veröffentlichen, versuchen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="c6e86-163">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="c6e86-164">Überprüfen Sie, dass die Broadbean Anmeldeinformationen, die Sie in Attract eingegeben haben, gültig und korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="c6e86-164">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="c6e86-165">Wenn die Anmeldeinformationen gültig sind und korrekt sind, kontaktieren Sie den [Broadbean Support](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="c6e86-165">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="c6e86-166">Wenn das Problem weiterhin besteht, kontaktieren Sie den [Microsoft Support](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="c6e86-166">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
