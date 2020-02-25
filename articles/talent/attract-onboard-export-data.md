---
title: Daten aus Attract und Onboard exportieren
description: Exportieren Sie Daten aus Dynamics 365 Talent – Attract und Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: acdd93637385246f9c5c652cccdf2cbfb263cc33
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2020
ms.locfileid: "2975933"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="166a4-103">Daten aus Attract und Onboard exportieren</span><span class="sxs-lookup"><span data-stu-id="166a4-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="166a4-104">Wie in [Ruhestand Dynamics 365 Talent: Attract und Dynamics 365 Talent: OnboardApps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps) angekündigt, ziehen wir Dynamics 365 Talent: Attract und Dynamics 365 Talent: Onboard am 1. Februar 2022 zurück.</span><span class="sxs-lookup"><span data-stu-id="166a4-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="166a4-105">Um die Migration auf ein anderes Produkt zu erleichtern, bieten beide Apps jetzt Datenexportfunktionen.</span><span class="sxs-lookup"><span data-stu-id="166a4-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="166a4-106">Daten aus Attract exportieren</span><span class="sxs-lookup"><span data-stu-id="166a4-106">Export data from Attract</span></span>

<span data-ttu-id="166a4-107">Sie können Ihre Daten exportieren, ohne den Zugriff auf Ihre Umgebung einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="166a4-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="166a4-108">Möglicherweise möchten Sie dies zu Testzwecken ausführen oder um unsere Datenstruktur verstehen.</span><span class="sxs-lookup"><span data-stu-id="166a4-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="166a4-109">Wenn Sie zur Migration bereit sind, beschränken Sie den Zugriff auf Ihre Attract-Umgebung mithilfe der Anweisungen nach diesem Verfahren.</span><span class="sxs-lookup"><span data-stu-id="166a4-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="166a4-110">Stellen Sie sicher, dass Sie Ihre Daten erneut exportieren.</span><span class="sxs-lookup"><span data-stu-id="166a4-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="166a4-111">Gehe zu [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="166a4-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="166a4-112">Unter **Datenexport** wählen Sie **Datenexport anfordern**.</span><span class="sxs-lookup"><span data-stu-id="166a4-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="166a4-113">Einen Datenexport bei Attract anfodern</span><span class="sxs-lookup"><span data-stu-id="166a4-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="166a4-114">Wenn das Meldungsfeld **Ihre Anfrage wird bearbeitet** erscheint, wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="166a4-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="166a4-115">Der Datenexport kann je nach Exportgröße bis zu 20 Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="166a4-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="166a4-116">Wenn Ihr Export abgeschlossen ist, wählen Sie die Schaltfläche **Herunterladen** daneben.</span><span class="sxs-lookup"><span data-stu-id="166a4-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="166a4-117">Alle Datenexporte sind sieben Tage lang verfügbar, danach läuft der Link **Herunterladen** ab.</span><span class="sxs-lookup"><span data-stu-id="166a4-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="166a4-118">Der Download enthält eine ZIP-Datei mit Ihren Attract-Daten, einschließlich der folgenden Ordner:</span><span class="sxs-lookup"><span data-stu-id="166a4-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="166a4-119">Ordnername</span><span class="sxs-lookup"><span data-stu-id="166a4-119">Folder name</span></span> | <span data-ttu-id="166a4-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="166a4-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="166a4-121">Administratoreinstellungen</span><span class="sxs-lookup"><span data-stu-id="166a4-121">Admin settings</span></span> | <span data-ttu-id="166a4-122">Konfigurationen des Attract Admin Center.</span><span class="sxs-lookup"><span data-stu-id="166a4-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="166a4-123">Kandidaten</span><span class="sxs-lookup"><span data-stu-id="166a4-123">Candidates</span></span> | <span data-ttu-id="166a4-124">Alle Kandidaten, die zu Jobs oder Talentpools hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="166a4-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="166a4-125">E-Mail-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="166a4-125">Email templates</span></span> | <span data-ttu-id="166a4-126">Alle E-Mail-Vorlagen, die für die Umgebung konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="166a4-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="166a4-127">Jobangebotsvorlagenpaket</span><span class="sxs-lookup"><span data-stu-id="166a4-127">Job offer package templates</span></span> | <span data-ttu-id="166a4-128">Alle erstellten Jobangebotspaketvorlagen sowie die zugehörigen Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="166a4-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="166a4-129">Regelsätze für Jobangebote</span><span class="sxs-lookup"><span data-stu-id="166a4-129">Job offer rule sets</span></span> |  <span data-ttu-id="166a4-130">Alle Regelsatzdateien, die zur Angebotsverwaltung hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="166a4-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="166a4-131">Jobangebotsvorlagen</span><span class="sxs-lookup"><span data-stu-id="166a4-131">Job offer templates</span></span> | <span data-ttu-id="166a4-132">Alle Jobangebot-Dokumentvorlagen, die für die Umgebung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="166a4-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="166a4-133">Jobangebote</span><span class="sxs-lookup"><span data-stu-id="166a4-133">Job openings</span></span> | <span data-ttu-id="166a4-134">Alle erstellten Jobs.</span><span class="sxs-lookup"><span data-stu-id="166a4-134">All created jobs.</span></span> <span data-ttu-id="166a4-135">Gelöschte Jobs werden nicht exportiert.</span><span class="sxs-lookup"><span data-stu-id="166a4-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="166a4-136">Die Unterordner enthalten Bewerbungsunterlagen mit Unterordnern für Bewerbungsanlagen und Angebotspakete, sofern zutreffend.</span><span class="sxs-lookup"><span data-stu-id="166a4-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="166a4-137">Jobangebotsvorlagen</span><span class="sxs-lookup"><span data-stu-id="166a4-137">Job opening templates</span></span> | <span data-ttu-id="166a4-138">Stellenprozessvorlagen, die in der Umgebung konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="166a4-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="166a4-139">Talentpools</span><span class="sxs-lookup"><span data-stu-id="166a4-139">Talent pools</span></span> | <span data-ttu-id="166a4-140">Alle erstellten Talentpools, ihre Beitragslisten und die Kandidatenlisten für die Talentpools.</span><span class="sxs-lookup"><span data-stu-id="166a4-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="166a4-141">Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="166a4-141">Workers</span></span> | <span data-ttu-id="166a4-142">Liste aller Mitarbeiter, die in der Umgebung anwesend sind, sowie deren Rollen.</span><span class="sxs-lookup"><span data-stu-id="166a4-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="166a4-143">(Stammordner)</span><span class="sxs-lookup"><span data-stu-id="166a4-143">(root folder)</span></span> | <span data-ttu-id="166a4-144">Eine JSON-Schemadatei, die die Datenstrukturfelder beschreibt.</span><span class="sxs-lookup"><span data-stu-id="166a4-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="166a4-145">Zugriff auf Attract beschränken</span><span class="sxs-lookup"><span data-stu-id="166a4-145">Restrict access to Attract</span></span>

<span data-ttu-id="166a4-146">Wenn Sie zur Migration bereit sind, hindern Sie Nicht-Administratoren daran, auf Ihre Attract-Umgebung zuzugreifen, und exportieren Sie Ihre Daten.</span><span class="sxs-lookup"><span data-stu-id="166a4-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="166a4-147">Die Einschränkung des Zugriffs auf Ihre Attract-Umgebung ist dauerhaft und kann nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="166a4-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="166a4-148">Wenn Sie möchten, dass Benutzer ohne Administratorrechte weiterhin auf Ihre Umgebung zugreifen können, überspringen Sie diesen Schritt.</span><span class="sxs-lookup"><span data-stu-id="166a4-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="166a4-149">Gehe zu [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="166a4-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="166a4-150">Um zu verhindern, dass Nicht-Administratoren auf Ihre Attract-Umgebung zugreifen, klicken Sie unter **Zugriff auf diese App beschränken** auf **Zugriff jetzt beschränken**.</span><span class="sxs-lookup"><span data-stu-id="166a4-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="166a4-151">Durch das Einschränken des Zugriffs werden auch alle aktiven Jobs, die veröffentlicht wurden, gelöscht.</span><span class="sxs-lookup"><span data-stu-id="166a4-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="166a4-152">Nicht-Admin-Zugriff auf Attract beschränken</span><span class="sxs-lookup"><span data-stu-id="166a4-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="166a4-153">Wenn Sie die Warnung **Dies ist eine permanente Veränderung** sehen, wählen Sie **Zugriff einschränken**, um Nicht-Administrator-Benutzer dauerhaft aus dieser Umgebung auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="166a4-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="166a4-154">Wenn Sie diesen Schritt nicht ausführen möchten, wählen Sie **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="166a4-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="166a4-155">Warnung, dass die Einschränkung des Zugriffs eine permanente Änderung ist</span><span class="sxs-lookup"><span data-stu-id="166a4-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="166a4-156">Administratoren können weiterhin auf die Datenexport- und Personenberichtseiten zugreifen, nachdem Sie den Zugriff auf die Attract-Umgebung eingeschränkt haben.</span><span class="sxs-lookup"><span data-stu-id="166a4-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="166a4-157">Daten aus Onboard exportieren</span><span class="sxs-lookup"><span data-stu-id="166a4-157">Export data from Onboard</span></span>

<span data-ttu-id="166a4-158">Wenn Sie bereit sind, können Sie Vorlagen, Handbücher und Kandidatendaten von Onboard herunterladen.</span><span class="sxs-lookup"><span data-stu-id="166a4-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="166a4-159">Gehe zu [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span><span class="sxs-lookup"><span data-stu-id="166a4-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="166a4-160">Unter **Datenexport** wählen Sie **Datenexport anfordern**.</span><span class="sxs-lookup"><span data-stu-id="166a4-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="166a4-161">Einen Datenexport von Onboard exportieren</span><span class="sxs-lookup"><span data-stu-id="166a4-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="166a4-162">Wenn das Meldungsfeld **Ihre Anfrage wird bearbeitet** erscheint, wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="166a4-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="166a4-163">Der Datenexport kann je nach Exportgröße bis zu 20 Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="166a4-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="166a4-164">Wenn Ihr Export abgeschlossen ist, wählen Sie die Schaltfläche **Herunterladen** daneben.</span><span class="sxs-lookup"><span data-stu-id="166a4-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="166a4-165">Datenexport aus Onboard herunterladen</span><span class="sxs-lookup"><span data-stu-id="166a4-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="166a4-166">Ihr Datenexport ist sieben Tage lang verfügbar.</span><span class="sxs-lookup"><span data-stu-id="166a4-166">Your data export is available for seven days.</span></span> <span data-ttu-id="166a4-167">Nach sieben Tagen ist der Link **Herunterladen** abgelaufen und Sie müssen einen neuen Export anfordern, wenn Sie Ihre Daten erneut herunterladen müssen.</span><span class="sxs-lookup"><span data-stu-id="166a4-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="166a4-168">Wenn Sie einen neuen Datenexport starten, laufen alle vorhandenen Downloads ab, wenn der neue Export erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="166a4-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="166a4-169">Der Download ist eine .zip-Datei, die Folgendes enthält:</span><span class="sxs-lookup"><span data-stu-id="166a4-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="166a4-170">Ein **Vorlagen**-Ordner, der Ihre Onboard-Vorlagen im Word-Dokumentformat enthält.</span><span class="sxs-lookup"><span data-stu-id="166a4-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="166a4-171">Ein **Guides**-Ordner, der Ihre Onboard-Guides im Word-Dokumentformat enthält.</span><span class="sxs-lookup"><span data-stu-id="166a4-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="166a4-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="166a4-172">See also</span></span>

[<span data-ttu-id="166a4-173">Einstellen von Dynamics 365 Talent: Attract und Dynamics 365 Talent: Onboard Apps</span><span class="sxs-lookup"><span data-stu-id="166a4-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)