---
title: Robots.txt-Dateien verwalten
description: In diesem Thema wird beschrieben, wie Sie robots.txt-Dateien in Microsoft Dynamics 365 Commerce verwalten.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: afd7982179dc9845c9adc24e8c7c9951a04460a3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477707"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="0ea5b-103">Robots.txt-Dateien verwalten</span><span class="sxs-lookup"><span data-stu-id="0ea5b-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0ea5b-104">In diesem Thema wird beschrieben, wie Sie robots.txt-Dateien in Microsoft Dynamics 365 Commerce verwalten.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0ea5b-105">Der Robots-Ausschlussstandard oder robots.txt ist ein Standard, den Websites für die Kommunikation mit Webrobotern verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="0ea5b-106">Er weist Webroboter an, welche Bereiche einer Website nicht besucht werden sollten.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="0ea5b-107">Roboter werden häufig von Suchmaschinen verwendet, um Websites zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="0ea5b-108">Um Roboter von einem Server auszuschließen, erstellen Sie eine Datei auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="0ea5b-109">In dieser Datei geben Sie eine Zugriffsrichtlinie für Roboter an.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="0ea5b-110">Die Datei muss über HTTP unter der lokalen URL **/robots.txt** erreichbar sein.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="0ea5b-111">Mithilfe der robots.txt-Datei können Suchmaschinen den Inhalt Ihrer Website indizieren.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="0ea5b-112">Mit Dynamics 365 Commerce können Sie eine robots.txt-Datei für Ihre Domain hochladen.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="0ea5b-113">Für jede Domain in Ihrer Commerce-Umgebung können Sie eine robots.txt-Datei hochladen und dieser Domain zuordnen.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="0ea5b-114">Weitere Informationen zur robots.txt-Datei finden Sie unter [Die Web Robots-Seiten](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="0ea5b-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="0ea5b-115">Laden Sie eine robots.txt-Datei hoch</span><span class="sxs-lookup"><span data-stu-id="0ea5b-115">Upload a robots.txt file</span></span>

<span data-ttu-id="0ea5b-116">Stellen Sie sicher, nachdem Sie Ihre robots.txt-Datei gemäß dem [Roboter-Ausschlussstandard](https://www.robotstxt.org/orig.html) erstellt und bearbeitet haben, dass die Datei auf dem Computer zugänglich ist, auf dem Sie auch die Commerce-Authoring-Tools verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="0ea5b-117">Die Datei muss **robots.txt** genannt werden.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="0ea5b-118">Für beste Ergebnisse muss es das Format haben, das in der Norm angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="0ea5b-119">Jeder Commerce-Kunde ist für die Validierung und Pflege des Inhalts seiner robots.txt-Datei verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="0ea5b-120">Um eine robots.txt-Datei hochzuladen, müssen Sie als Systemadministrator bei Commerce angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="0ea5b-121">Gehen Sie folgendermaßen vor, um eine robots.txt-Datei in Commerce hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="0ea5b-122">Melden Sie sich bei Commerce als Systemadministrator an.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="0ea5b-123">Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen** (neben dem Zahnradsymbol) aus, um es zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="0ea5b-124">Wählen Sie unter **Mandanteneinstellungen** die Option **Robots.txt** aus.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="0ea5b-125">Eine Liste aller Ihrer Umgebung zugeordneten Domänen wird im Hauptteil des Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="0ea5b-126">Wählen Sie **Verwalten** aus, um eine robots.txt-Datei für eine Domäne in Ihrer Umgebung hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="0ea5b-127">Wählen Sie im rechten Menü **Hochladen** (den nach oben zeigenden Pfeil) neben der Domäne aus, die der robots.txt-Datei zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="0ea5b-128">Ein Dateibrowser-Dialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="0ea5b-129">Navigieren Sie im Dialogfeld zu der robots.txt-Datei, die Sie für die zugeordnete Domäne hochladen möchten, und wählen Sie dann **Öffnen** aus, um den Upload abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="0ea5b-130">Während des Uploads überprüft Commerce, ob es sich bei der Datei um eine Textdatei handelt, überprüft jedoch nicht den Inhalt der Datei.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="0ea5b-131">Laden Sie eine robots.txt-Datei hoch</span><span class="sxs-lookup"><span data-stu-id="0ea5b-131">Download a robots.txt file</span></span>

<span data-ttu-id="0ea5b-132">Gehen Sie folgendermaßen vor, um eine robots.txt-Datei in Commerce herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="0ea5b-133">Melden Sie sich bei Commerce als Systemadministrator an.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="0ea5b-134">Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen** (neben dem Zahnradsymbol) aus, um es zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="0ea5b-135">Wählen Sie unter **Mandanteneinstellungen** die Option **Robots.txt** aus.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="0ea5b-136">Eine Liste aller Ihrer Umgebung zugeordneten Domänen wird im Hauptteil des Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="0ea5b-137">Wählen Sie **Verwalten** aus, um eine robots.txt-Datei für eine Domäne in Ihrer Umgebung herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="0ea5b-138">Wählen Sie rechts im Menü die Schaltfläche **Herunterladen** aus (der nach unten zeigende Pfeil) neben der Domäne, die der robots.txt-Datei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="0ea5b-139">Ein Dateibrowser-Dialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="0ea5b-140">Navigieren Sie im Dialogfeld zum gewünschten Speicherort auf Ihrem lokalen Laufwerk, bestätigen Sie einen Dateinamen oder geben Sie einen ein. Wählen Sie dann **Speichern** aus, um den Download abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="0ea5b-141">Mit diesem Verfahren können nur robots.txt-Dateien heruntergeladen werden, die zuvor mit den Commerce-Authoring-Tools hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="0ea5b-142">Laden Sie eine robots.txt-Datei hoch</span><span class="sxs-lookup"><span data-stu-id="0ea5b-142">Delete a robots.txt file</span></span>

<span data-ttu-id="0ea5b-143">Gehen Sie folgendermaßen vor, um eine robots.txt-Datei in Commerce zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="0ea5b-144">Melden Sie sich bei Commerce als Systemadministrator an.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="0ea5b-145">Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen** (neben dem Zahnradsymbol) aus, um es zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="0ea5b-146">Wählen Sie unter **Mandanteneinstellungen** die Option **Robots.txt** aus.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="0ea5b-147">Eine Liste aller Ihrer Umgebung zugeordneten Domänen wird im Hauptteil des Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="0ea5b-148">Wählen Sie **Verwalten** aus, um eine robots.txt-Datei für eine Domäne in Ihrer Umgebung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="0ea5b-149">Wählen Sie im Menü rechts die Schaltfläche **Löschen** (das Papierkorb-Symbol) neben der Domäne aus, die der robots.txt-Datei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="0ea5b-150">Ein Dateibrowserfenster wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-150">A file browser window appears.</span></span>
6. <span data-ttu-id="0ea5b-151">Navigieren Sie im Dateibrowser-Fenster zu der robots.txt-Datei, die Sie für die Domäne löschen möchten, wählen Sie sie aus und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="0ea5b-152">Eine Warnmeldung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-152">A warning message box appears.</span></span>
7. <span data-ttu-id="0ea5b-153">Wählen Sie im Nachrichtenfeld **Löschen** aus, um das Löschen der robots.txt-Datei zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="0ea5b-154">Mit diesem Verfahren können nur robots.txt-Dateien gelöscht werden, die zuvor mit den Commerce-Authoring-Tools hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="0ea5b-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ea5b-155">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0ea5b-155">Additional resources</span></span>

[<span data-ttu-id="0ea5b-156">Domänennamen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0ea5b-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="0ea5b-157">Neuen E-Commerce-Mandanten bereitstellen</span><span class="sxs-lookup"><span data-stu-id="0ea5b-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="0ea5b-158">E-Commerce-Website erstellen</span><span class="sxs-lookup"><span data-stu-id="0ea5b-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="0ea5b-159">Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal</span><span class="sxs-lookup"><span data-stu-id="0ea5b-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="0ea5b-160">URL-Umleitungen in Massen hochladen</span><span class="sxs-lookup"><span data-stu-id="0ea5b-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="0ea5b-161">B2C-Mandanten in Commerce einrichten</span><span class="sxs-lookup"><span data-stu-id="0ea5b-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="0ea5b-162">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="0ea5b-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="0ea5b-163">Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung</span><span class="sxs-lookup"><span data-stu-id="0ea5b-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="0ea5b-164">Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)</span><span class="sxs-lookup"><span data-stu-id="0ea5b-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="0ea5b-165">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="0ea5b-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
