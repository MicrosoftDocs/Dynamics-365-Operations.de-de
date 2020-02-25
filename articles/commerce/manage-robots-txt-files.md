---
title: Verwalten von robots.txt-Dateien
description: In diesem Thema wird beschrieben, wie Sie robots.txt-Dateien in Microsoft Dynamics 365 Commerce verwalten.
author: BrianShook
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brishoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ce49f2968030ca4656a01c7646819c01635e12
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003486"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="34012-103">Verwalten von robots.txt-Dateien</span><span class="sxs-lookup"><span data-stu-id="34012-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="34012-104">In diesem Thema wird beschrieben, wie Sie robots.txt-Dateien in Microsoft Dynamics 365 Commerce verwalten.</span><span class="sxs-lookup"><span data-stu-id="34012-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="34012-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="34012-105">Overview</span></span>

<span data-ttu-id="34012-106">Der Robots-Ausschlussstandard oder robots.txt ist ein Standard, den Websites für die Kommunikation mit Webrobotern verwenden.</span><span class="sxs-lookup"><span data-stu-id="34012-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="34012-107">Er weist Webroboter an, welche Bereiche einer Website nicht besucht werden sollten.</span><span class="sxs-lookup"><span data-stu-id="34012-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="34012-108">Roboter werden häufig von Suchmaschinen verwendet, um Websites zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="34012-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="34012-109">Um Roboter von einem Server auszuschließen, erstellen Sie eine Datei auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="34012-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="34012-110">In dieser Datei geben Sie eine Zugriffsrichtlinie für Roboter an.</span><span class="sxs-lookup"><span data-stu-id="34012-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="34012-111">Die Datei muss über HTTP unter der lokalen URL **/robots.txt** erreichbar sein.</span><span class="sxs-lookup"><span data-stu-id="34012-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="34012-112">Mithilfe der robots.txt-Datei können Suchmaschinen den Inhalt Ihrer Website indizieren.</span><span class="sxs-lookup"><span data-stu-id="34012-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="34012-113">Mit Dynamics 365 Commerce können Sie eine robots.txt-Datei für Ihre Domain hochladen.</span><span class="sxs-lookup"><span data-stu-id="34012-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="34012-114">Für jede Domain in Ihrer Commerce-Umgebung können Sie eine robots.txt-Datei hochladen und dieser Domain zuordnen.</span><span class="sxs-lookup"><span data-stu-id="34012-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="34012-115">Weitere Informationen zur robots.txt-Datei finden Sie unter [Die Web Robots-Seiten](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="34012-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="34012-116">Laden Sie eine robots.txt-Datei hoch</span><span class="sxs-lookup"><span data-stu-id="34012-116">Upload a robots.txt file</span></span>

<span data-ttu-id="34012-117">Stellen Sie sicher, nachdem Sie Ihre robots.txt-Datei gemäß dem [Roboter-Ausschlussstandard](https://www.robotstxt.org/orig.html) erstellt und bearbeitet haben, dass die Datei auf dem Computer zugänglich ist, auf dem Sie auch die Commerce-Authoring-Tools verwenden.</span><span class="sxs-lookup"><span data-stu-id="34012-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="34012-118">Die Datei muss **robots.txt** genannt werden.</span><span class="sxs-lookup"><span data-stu-id="34012-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="34012-119">Für beste Ergebnisse muss es das Format haben, das in der Norm angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="34012-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="34012-120">Jeder Commerce-Kunde ist für die Validierung und Pflege des Inhalts seiner robots.txt-Datei verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="34012-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="34012-121">Um eine robots.txt-Datei hochzuladen, müssen Sie als Systemadministrator bei Commerce angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="34012-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="34012-122">Gehen Sie folgendermaßen vor, um eine robots.txt-Datei in Commerce hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="34012-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="34012-123">Melden Sie sich bei Commerce als Systemadministrator an.</span><span class="sxs-lookup"><span data-stu-id="34012-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="34012-124">Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen** (neben dem Zahnradsymbol) aus, um es zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="34012-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="34012-125">Wählen Sie unter **Mandanteneinstellungen** die Option **Robots.txt** aus.</span><span class="sxs-lookup"><span data-stu-id="34012-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="34012-126">Eine Liste aller Ihrer Umgebung zugeordneten Domänen wird im Hauptteil des Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34012-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="34012-127">Wählen Sie **Verwalten** aus, um eine robots.txt-Datei für eine Domäne in Ihrer Umgebung hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="34012-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="34012-128">Wählen Sie im rechten Menü **Hochladen** (den nach oben zeigenden Pfeil) neben der Domäne aus, die der robots.txt-Datei zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="34012-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="34012-129">Ein Dateibrowser-Dialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34012-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="34012-130">Navigieren Sie im Dialogfeld zu der robots.txt-Datei, die Sie für die zugeordnete Domäne hochladen möchten, und wählen Sie dann **Öffnen** aus, um den Upload abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="34012-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="34012-131">Während des Uploads überprüft Commerce, ob es sich bei der Datei um eine Textdatei handelt, überprüft jedoch nicht den Inhalt der Datei.</span><span class="sxs-lookup"><span data-stu-id="34012-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="34012-132">Laden Sie eine robots.txt-Datei hoch</span><span class="sxs-lookup"><span data-stu-id="34012-132">Download a robots.txt file</span></span>

<span data-ttu-id="34012-133">Gehen Sie folgendermaßen vor, um eine robots.txt-Datei in Commerce herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="34012-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="34012-134">Melden Sie sich bei Commerce als Systemadministrator an.</span><span class="sxs-lookup"><span data-stu-id="34012-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="34012-135">Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen** (neben dem Zahnradsymbol) aus, um es zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="34012-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="34012-136">Wählen Sie unter **Mandanteneinstellungen** die Option **Robots.txt** aus.</span><span class="sxs-lookup"><span data-stu-id="34012-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="34012-137">Eine Liste aller Ihrer Umgebung zugeordneten Domänen wird im Hauptteil des Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34012-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="34012-138">Wählen Sie **Verwalten** aus, um eine robots.txt-Datei für eine Domäne in Ihrer Umgebung herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="34012-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="34012-139">Wählen Sie rechts im Menü die Schaltfläche **Herunterladen** aus (der nach unten zeigende Pfeil) neben der Domäne, die der robots.txt-Datei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="34012-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="34012-140">Ein Dateibrowser-Dialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34012-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="34012-141">Navigieren Sie im Dialogfeld zum gewünschten Speicherort auf Ihrem lokalen Laufwerk, bestätigen Sie einen Dateinamen oder geben Sie einen ein. Wählen Sie dann **Speichern** aus, um den Download abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="34012-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="34012-142">Mit diesem Verfahren können nur robots.txt-Dateien heruntergeladen werden, die zuvor mit den Commerce-Authoring-Tools hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="34012-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="34012-143">Laden Sie eine robots.txt-Datei hoch</span><span class="sxs-lookup"><span data-stu-id="34012-143">Delete a robots.txt file</span></span>

<span data-ttu-id="34012-144">Gehen Sie folgendermaßen vor, um eine robots.txt-Datei in Commerce zu löschen.</span><span class="sxs-lookup"><span data-stu-id="34012-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="34012-145">Melden Sie sich bei Commerce als Systemadministrator an.</span><span class="sxs-lookup"><span data-stu-id="34012-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="34012-146">Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen** (neben dem Zahnradsymbol) aus, um es zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="34012-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="34012-147">Wählen Sie unter **Mandanteneinstellungen** die Option **Robots.txt** aus.</span><span class="sxs-lookup"><span data-stu-id="34012-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="34012-148">Eine Liste aller Ihrer Umgebung zugeordneten Domänen wird im Hauptteil des Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34012-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="34012-149">Wählen Sie **Verwalten** aus, um eine robots.txt-Datei für eine Domäne in Ihrer Umgebung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="34012-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="34012-150">Wählen Sie im Menü rechts die Schaltfläche **Löschen** (das Papierkorb-Symbol) neben der Domäne aus, die der robots.txt-Datei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="34012-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="34012-151">Ein Dateibrowserfenster wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34012-151">A file browser window appears.</span></span>
6. <span data-ttu-id="34012-152">Navigieren Sie im Dateibrowser-Fenster zu der robots.txt-Datei, die Sie für die Domäne löschen möchten, wählen Sie sie aus und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="34012-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="34012-153">Eine Warnmeldung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34012-153">A warning message box appears.</span></span>
7. <span data-ttu-id="34012-154">Wählen Sie im Nachrichtenfeld **Löschen** aus, um das Löschen der robots.txt-Datei zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="34012-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="34012-155">Mit diesem Verfahren können nur robots.txt-Dateien gelöscht werden, die zuvor mit den Commerce-Authoring-Tools hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="34012-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34012-156">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="34012-156">Additional resources</span></span>

[<span data-ttu-id="34012-157">Konfigurieren Ihres Domänennamens</span><span class="sxs-lookup"><span data-stu-id="34012-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="34012-158">Bereitstellen einer neuen E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="34012-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="34012-159">Erstellen einer E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="34012-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="34012-160">Zuordnen einer Onlinewebseite zu einem Kanal</span><span class="sxs-lookup"><span data-stu-id="34012-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="34012-161">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="34012-161">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="34012-162">Unterstützung für ein Content Delivery Network (CDN) hinzufügen</span><span class="sxs-lookup"><span data-stu-id="34012-162">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="34012-163">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="34012-163">Enable location-based store detection</span></span>](enable-store-detection.md)
