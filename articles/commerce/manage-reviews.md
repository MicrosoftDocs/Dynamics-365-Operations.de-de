---
title: Verwalten von Bewertungen und Prüfungen
description: In diesem Thema wird das Verwalten von Bewertungen und Überprüfungen mit dem Moderationstool für Bewertungen und Überprüfungen von Microsoft Dynamics 365 Commerce erklärt.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027241"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="89483-103">Verwalten von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="89483-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="89483-104">In diesem Thema wird das Verwalten von Bewertungen und Überprüfungen mit dem Moderationstool für Bewertungen und Überprüfungen von Microsoft Dynamics 365 Commerce erklärt.</span><span class="sxs-lookup"><span data-stu-id="89483-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="89483-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="89483-105">Overview</span></span>

<span data-ttu-id="89483-106">Dynamics 365 Commerce verwendet Microsoft Azure Cognitive Service, um den Prüftext automatisch zu moderieren, indem einfache Wörter redigiert werden.</span><span class="sxs-lookup"><span data-stu-id="89483-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="89483-107">Darüber hinaus können Moderatoren das Moderationstool für Bewertungen und Prüfungen für die folgenden manuellen Aufgaben verwenden:</span><span class="sxs-lookup"><span data-stu-id="89483-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="89483-108">Moderieren Sie Prüfungen, indem Sie darauf antworten oder sie entfernen.</span><span class="sxs-lookup"><span data-stu-id="89483-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="89483-109">Löschen Sie die Bewertungen eines Kunden auf Kundenwunsch.</span><span class="sxs-lookup"><span data-stu-id="89483-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="89483-110">Importieren Sie Bewertungen und Überprüfungsdaten für alle Produkte in eine Power BI-Vorlage, damit Trends für Bewertungen und Überprüfungen analysiert werden können.</span><span class="sxs-lookup"><span data-stu-id="89483-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="access-ratings-and-reviews-moderation-features"></a><span data-ttu-id="89483-111">Greifen Sie auf Moderationsfunktionen für Bewertungen zu</span><span class="sxs-lookup"><span data-stu-id="89483-111">Access ratings and reviews moderation features</span></span>

<span data-ttu-id="89483-112">Führen Sie die folgenden Schritte aus, um im E-Commerce-Website-Verwaltungstool auf die Moderationsfunktionen für Bewertungen und Überprüfungen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="89483-112">To access ratings and reviews moderation features in the e-Commerce site management tool, follow these steps.</span></span>

1. <span data-ttu-id="89483-113">Melden Sie sich bei [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com) an.</span><span class="sxs-lookup"><span data-stu-id="89483-113">Sign in to [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="89483-114">Öffnet das Projekt, das die Umgebung enthält, in der Sie E-Commerce initialisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="89483-114">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="89483-115">Im Abschnitt **Umgebung** wählen Sie die Umgebung.</span><span class="sxs-lookup"><span data-stu-id="89483-115">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="89483-116">Wählen Sie unter **Umgebungsfunktionen** die Option **Einzelhandelsverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="89483-116">Under **Environment features**, select **Retail manage**.</span></span>
1. <span data-ttu-id="89483-117">Auf der **E-Commerce** Registrkarte unter **Links**, wählen Sie **E-Commerce-Site-Management-Tool**.</span><span class="sxs-lookup"><span data-stu-id="89483-117">On the **e-Commerce** tab under **Links**, select **e-Commerce Site management tool**.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="89483-118">Lesen einer Prüfung</span><span class="sxs-lookup"><span data-stu-id="89483-118">Read a review</span></span> 

1. <span data-ttu-id="89483-119">Navigieren Sie zu **Start \> Bewertungen \> Moderation**.</span><span class="sxs-lookup"><span data-stu-id="89483-119">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="89483-120">Verwenden Sie das Suchfeld oben rechts auf der Seite, um die angezeigten Bewertungen nach Produkt-ID, Produktname oder Bewertungstext zu filtern.</span><span class="sxs-lookup"><span data-stu-id="89483-120">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="89483-121">Mit zusätzlichen Filtern können Sie die Überprüfungen nach Zeitraum, Bewertung, Kanal oder Anliegenstatus einschränken (deaktiviert, beantwortet oder gemeldet).</span><span class="sxs-lookup"><span data-stu-id="89483-121">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Moderations-Startseite](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="89483-123">Auf Bewertung antworten</span><span class="sxs-lookup"><span data-stu-id="89483-123">Respond to a review</span></span> 

<span data-ttu-id="89483-124">Manchmal äußern Kunden, die ein Produkt gekauft haben, ihre Zufriedenheit oder Unzufriedenheit, oder sie verstehen nicht, wie das Produkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="89483-124">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="89483-125">Als Moderator können Sie eine Antwort auf eine Bewertung abgeben.</span><span class="sxs-lookup"><span data-stu-id="89483-125">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="89483-126">Diese Antwort wird zusammen mit der Überprüfung auf der Website angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89483-126">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="89483-127">Gehen Sie folgendermaßen vor, um auf eine Bewertung zu antworten.</span><span class="sxs-lookup"><span data-stu-id="89483-127">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="89483-128">Navigieren Sie zu **Start \> Bewertungen \> Moderation**.</span><span class="sxs-lookup"><span data-stu-id="89483-128">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="89483-129">Suchen Sie die Überprüfung, für die eine Antwort erforderlich ist, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="89483-129">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="89483-130">Wählen Sie im Eigenschaftenbereich rechts **Eine Antwort hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="89483-130">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="89483-131">Geben Sie den Antworttext und den Namen ein, der für den Antwortenden angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="89483-131">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="89483-132">Der Standardname des Antwortenden lautet **Moderator**.</span><span class="sxs-lookup"><span data-stu-id="89483-132">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="89483-133">Wählen Sie abschließend **Antwort senden** aus.</span><span class="sxs-lookup"><span data-stu-id="89483-133">When you've finished, select **Post response**.</span></span>

![Beantworten einer Bewertung](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="89483-135">Entfernen einer Bewertung</span><span class="sxs-lookup"><span data-stu-id="89483-135">Take down a review</span></span> 

<span data-ttu-id="89483-136">Manchmal gibt es eine geschäftliche Rechtfertigung dafür, dass Moderatoren Kundenbewertungen entfernen.</span><span class="sxs-lookup"><span data-stu-id="89483-136">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="89483-137">Gehen Sie folgendermaßen vor, um auf eine Bewertung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="89483-137">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="89483-138">Navigieren Sie zu **Start \> Bewertungen \> Moderation**.</span><span class="sxs-lookup"><span data-stu-id="89483-138">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="89483-139">Suchen Sie die Bewertung, die entfernt werden muss, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="89483-139">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="89483-140">Wählen Sie im Eigenschaftenbereich rechts einen Grund für das Entfernen und dann **Entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="89483-140">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="89483-141">Löschen von Bewertungen eines Kunden auf Kundenwunsch</span><span class="sxs-lookup"><span data-stu-id="89483-141">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="89483-142">Manchmal möchten Kunden, dass ihre Bewertungen und Bewertungsdaten dauerhaft von einer E-Commerce-Website gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="89483-142">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="89483-143">Ein Moderator, der eine Entfernungsanforderung von einem Kunden erhält, kann die Kundendaten mithilfe der Funktion zum Löschen von Überprüfungen entfernen.</span><span class="sxs-lookup"><span data-stu-id="89483-143">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="89483-144">Um die Daten eines Kunden zu finden und zu löschen, benötigt der Moderator die E-Mail-Adresse, mit der sich der Kunde angemeldet und Bewertungen abgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="89483-144">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="89483-145">Gehen Sie folgendermaßen vor, um Kundendaten zu suchen und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="89483-145">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="89483-146">Navigieren Sie zu **Startseite \> Bewertungen \> Löschen**.</span><span class="sxs-lookup"><span data-stu-id="89483-146">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="89483-147">Geben Sie im Feld **Über die E-Mail-Adresse nach Benutzern suchen** die E-Mail-Adresse des Kunden ein und wählen Sie dann **Suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="89483-147">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="89483-148">Wenn der Kunde eine Überprüfungsaktivität hat (z. B. Überprüfungsbeiträge, Abstimmungen zur Nützlichkeit der Bewertungen eines anderen Kunden oder Kommentare zur Bewertung eines anderen Kunden), werden die Ergebnisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89483-148">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="89483-149">Für jedes Element gibt es die Schaltfläche **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="89483-149">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="89483-150">Wählen Sie für jedes Element, das gelöscht werden muss, **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="89483-150">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="89483-151">Wenn Sie zur Bestätigung aufgefordert werden, wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="89483-151">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Löschen von Kundendaten](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="89483-153">Es kann bis zu sieben Tage dauern, bis die Daten vollständig aus dem System entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="89483-153">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="89483-154">Moderatoren sollten Kunden über diese Verzögerung informieren.</span><span class="sxs-lookup"><span data-stu-id="89483-154">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="89483-155">Wenn Kunden ihren Namen in ihren Kontoeinstellungen geändert haben, werden möglicherweise mehrere Elemente in den Suchergebnissen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89483-155">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="89483-156">Um die Kundendaten vollständig zu löschen, muss der Moderator in diesem Fall **Löschen** für jeden Artikel auswählen.</span><span class="sxs-lookup"><span data-stu-id="89483-156">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="89483-157">Herunterladen von Bewertungs- und Prüfungsdaten</span><span class="sxs-lookup"><span data-stu-id="89483-157">Download ratings and reviews data</span></span>

<span data-ttu-id="89483-158">Mit dem Moderationstool für Bewertungen und Überprüfungen können Moderatoren, umfassend Bewertungs- und Prüfdaten importieren, damit sie Trends analysieren können.</span><span class="sxs-lookup"><span data-stu-id="89483-158">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="89483-159">Eine Power BI-Vorlage mit grundlegenden Metriken ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="89483-159">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="89483-160">Moderatoren können diese Vorlage verwenden, um umfassend importierte Daten zu verknüpfen und ein Dashboard anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="89483-160">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="89483-161">Sie müssen kein benutzerdefiniertes Dashboard erstellen.</span><span class="sxs-lookup"><span data-stu-id="89483-161">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="89483-162">Moderatoren können die Power BI-Vorlage auch anpassen, damit sie ihre spezifischen Anforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="89483-162">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="89483-163">Befolgen Sie diese Schritte, um Bewertungs- und Prüfdaten herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="89483-163">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="89483-164">Navigieren Sie zu **Start \> Bewertungen \> Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="89483-164">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="89483-165">Wählen Sie **Prüfdaten herunterladen** aus, um Bewertungs- und Prüfdaten im CSV-Format (Comma-Separated Values) herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="89483-165">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="89483-166">Bewertungs- und Prüftrends anzeigen</span><span class="sxs-lookup"><span data-stu-id="89483-166">View ratings and reviews trends</span></span>

<span data-ttu-id="89483-167">Moderatoren können die Power BI-Vorlage herunterladen, damit sie Trends in einem Dashboard anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="89483-167">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="89483-168">Befolgen Sie diese Schritte, um Bewertungs- und Prüftrends anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="89483-168">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="89483-169">Navigieren Sie zu **Start \> Bewertungen \> Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="89483-169">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="89483-170">Wählen Sie **PowerBI-Vorlage** aus, um die Vorlage herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="89483-170">Select **PowerBI template** to download the template.</span></span>

    ![Herunterladen der Power BI-Vorlage](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="89483-172">Öffnen Sie die heruntergeladene Vorlage durch Verwendung der Power BI-App.</span><span class="sxs-lookup"><span data-stu-id="89483-172">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="89483-173">Schließen Sie das Dialogfeld **Zugriff auf Webinhalt**, das angezeigt wird, und schließen Sie dann die angezeigte Fehlermeldung „Aktualisieren“.</span><span class="sxs-lookup"><span data-stu-id="89483-173">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="89483-174">Navigieren Sie zu **Startseite**, wählen Sie **Abfragen bearbeiten** und dann **Datenquelleneinstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="89483-174">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="89483-175">Wählen Sie im Dialogfeld **Datenquelleneinstellungen** die Option **Quelle ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="89483-175">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="89483-176">Geben Sie im Feld **URL** den Pfad der Prüfdaten ein, die Sie in der vorherigen Prozedur (Beispiel: **c:\\reviews\\ReviewsData.csv**) heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="89483-176">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL-Feld im Dialogfeld „Kommagetrennte Werte“](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="89483-178">Wählen Sie **OK** und dann **Änderungen anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="89483-178">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="89483-179">Es dauert ein bis zwei Minuten, um Ihre Änderungen auf die Datenquelle anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="89483-179">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="89483-180">Wählen Sie **Trendbilanz** aus, um die Trends für Bewertungen und Prüfungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="89483-180">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Trends für Bewertungen und Prüfungen](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="89483-182">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="89483-182">Additional resources</span></span>

[<span data-ttu-id="89483-183">Überblick über Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="89483-183">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="89483-184">Abonnieren zum Verwenden von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="89483-184">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="89483-185">Konfigurieren von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="89483-185">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="89483-186">Synchronisieren von Produktbewertungen in Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="89483-186">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
