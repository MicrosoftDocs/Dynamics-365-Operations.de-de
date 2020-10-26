---
title: Bewertungen und Prüfungen verwalten
description: In diesem Thema wird erläutert, wie Sie Bewertungen und Prüfungen im Microsoft Dynamics 365 Commerce-Site Builder verwalten.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
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
ms.openlocfilehash: 3fc88bc5a5868dce7c0539bf3f0ddc5b751e7b75
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974005"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="d602d-103">Bewertungen und Prüfungen verwalten</span><span class="sxs-lookup"><span data-stu-id="d602d-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d602d-104">In diesem Thema wird erläutert, wie Sie Bewertungen und Prüfungen im Microsoft Dynamics 365 Commerce-Site Builder verwalten.</span><span class="sxs-lookup"><span data-stu-id="d602d-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="d602d-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d602d-105">Overview</span></span>

<span data-ttu-id="d602d-106">Dynamics 365 Commerce verwendet Microsoft Azure Cognitive Service, um den Prüftext automatisch zu moderieren, indem einfache Wörter redigiert werden.</span><span class="sxs-lookup"><span data-stu-id="d602d-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="d602d-107">Darüber hinaus können Moderatoren Dynamics 365 Commerce-Site Builder zum Implementieren der folgenden manuellen Aufgaben verwenden:</span><span class="sxs-lookup"><span data-stu-id="d602d-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="d602d-108">Moderieren Sie Prüfungen, indem Sie darauf antworten oder sie entfernen.</span><span class="sxs-lookup"><span data-stu-id="d602d-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="d602d-109">Löschen Sie die Bewertungen eines Kunden auf Kundenwunsch.</span><span class="sxs-lookup"><span data-stu-id="d602d-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="d602d-110">Importieren Sie Bewertungen und Überprüfungsdaten für alle Produkte in eine Power BI-Vorlage, damit Trends für Bewertungen und Überprüfungen analysiert werden können.</span><span class="sxs-lookup"><span data-stu-id="d602d-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="d602d-111">Lesen einer Prüfung</span><span class="sxs-lookup"><span data-stu-id="d602d-111">Read a review</span></span> 

<span data-ttu-id="d602d-112">Um eine Überprüfung in den Commerce Site Builder hochzuladen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="d602d-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d602d-113">Navigieren Sie zu **Start \> Bewertungen \> Moderation**.</span><span class="sxs-lookup"><span data-stu-id="d602d-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="d602d-114">Verwenden Sie das Suchfeld oben rechts auf der Seite, um die angezeigten Bewertungen nach Produkt-ID, Produktname oder Bewertungstext zu filtern.</span><span class="sxs-lookup"><span data-stu-id="d602d-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="d602d-115">Mit zusätzlichen Filtern können Sie die Überprüfungen nach Zeitraum, Bewertung, Kanal oder Anliegenstatus einschränken (deaktiviert, beantwortet oder gemeldet).</span><span class="sxs-lookup"><span data-stu-id="d602d-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Moderations-Startseite](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="d602d-117">Auf Bewertung antworten</span><span class="sxs-lookup"><span data-stu-id="d602d-117">Respond to a review</span></span> 

<span data-ttu-id="d602d-118">Manchmal äußern Kunden, die ein Produkt gekauft haben, ihre Zufriedenheit oder Unzufriedenheit, oder sie verstehen nicht, wie das Produkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d602d-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="d602d-119">Als Moderator können Sie eine Antwort auf eine Bewertung abgeben.</span><span class="sxs-lookup"><span data-stu-id="d602d-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="d602d-120">Diese Antwort wird zusammen mit der Überprüfung auf der Website angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d602d-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="d602d-121">Um auf eine Überprüfung im Commerce Site Builder zu antworten, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="d602d-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d602d-122">Navigieren Sie zu **Start \> Bewertungen \> Moderation**.</span><span class="sxs-lookup"><span data-stu-id="d602d-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="d602d-123">Suchen Sie die Überprüfung, für die eine Antwort erforderlich ist, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="d602d-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="d602d-124">Wählen Sie im Eigenschaftenbereich rechts **Eine Antwort hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="d602d-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="d602d-125">Geben Sie den Antworttext und den Namen ein, der für den Antwortenden angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d602d-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="d602d-126">Der Standardname des Antwortenden lautet **Moderator**.</span><span class="sxs-lookup"><span data-stu-id="d602d-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="d602d-127">Wählen Sie abschließend **Antwort senden** aus.</span><span class="sxs-lookup"><span data-stu-id="d602d-127">When you've finished, select **Post response**.</span></span>

![Beantworten einer Bewertung](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="d602d-129">Entfernen einer Bewertung</span><span class="sxs-lookup"><span data-stu-id="d602d-129">Take down a review</span></span> 

<span data-ttu-id="d602d-130">Manchmal gibt es eine geschäftliche Rechtfertigung dafür, dass Moderatoren Kundenbewertungen entfernen.</span><span class="sxs-lookup"><span data-stu-id="d602d-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="d602d-131">Um eine Überprüfung aus dem Commerce Site Builder zu entfernen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="d602d-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d602d-132">Navigieren Sie zu **Start \> Bewertungen \> Moderation**.</span><span class="sxs-lookup"><span data-stu-id="d602d-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="d602d-133">Suchen Sie die Bewertung, die entfernt werden muss, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="d602d-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="d602d-134">Wählen Sie im Eigenschaftenbereich rechts einen Grund für das Entfernen unter **Enfernungsüberprüfung** und dann **Entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="d602d-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="d602d-135">Löschen von Bewertungen eines Kunden auf Kundenwunsch</span><span class="sxs-lookup"><span data-stu-id="d602d-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="d602d-136">Manchmal möchten Kunden, dass ihre Bewertungen und Bewertungsdaten dauerhaft von einer E-Commerce-Website gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="d602d-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="d602d-137">Ein Moderator, der eine Entfernungsanforderung von einem Kunden erhält, kann die Kundendaten mithilfe der Funktion zum Löschen von Überprüfungen entfernen.</span><span class="sxs-lookup"><span data-stu-id="d602d-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="d602d-138">Um die Daten eines Kunden zu finden und zu löschen, benötigt der Moderator die E-Mail-Adresse, mit der sich der Kunde angemeldet und Bewertungen abgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="d602d-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="d602d-139">Führen Sie die folgenden Schritte aus, um Kundendaten im Commerce Site Builder zu suchen und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d602d-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d602d-140">Navigieren Sie zu **Startseite \> Bewertungen \> Löschen**.</span><span class="sxs-lookup"><span data-stu-id="d602d-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="d602d-141">Geben Sie im Feld **Suche nach Benutzern über die E-Mail-Adresse** die E-Mail-Adresse des Kunden ein und wählen Sie dann **Suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="d602d-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="d602d-142">Wenn der Kunde eine Überprüfungsaktivität hat (z. B. Überprüfungsbeiträge, Abstimmungen zur Nützlichkeit der Bewertungen eines anderen Kunden oder Kommentare zur Bewertung eines anderen Kunden), werden die Ergebnisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d602d-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="d602d-143">Für jedes Element gibt es die Schaltfläche **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="d602d-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="d602d-144">Wählen Sie für jedes Element, das gelöscht werden muss, **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="d602d-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="d602d-145">Wenn Sie zur Bestätigung aufgefordert werden, wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="d602d-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Löschen von Kundendaten](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="d602d-147">Es kann bis zu sieben Tage dauern, bis die Daten vollständig aus dem System entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="d602d-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="d602d-148">Moderatoren sollten Kunden über diese Verzögerung informieren.</span><span class="sxs-lookup"><span data-stu-id="d602d-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="d602d-149">Wenn Kunden ihren Namen in ihren Kontoeinstellungen geändert haben, werden möglicherweise mehrere Elemente in den Suchergebnissen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d602d-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="d602d-150">Um die Kundendaten vollständig zu löschen, muss der Moderator in diesem Fall **Löschen** für jeden Artikel auswählen.</span><span class="sxs-lookup"><span data-stu-id="d602d-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="d602d-151">Herunterladen von Bewertungs- und Prüfungsdaten</span><span class="sxs-lookup"><span data-stu-id="d602d-151">Download ratings and reviews data</span></span>

<span data-ttu-id="d602d-152">Mit Commerce Site Builder können Moderatoren umfassend Bewertungs- und Prüfdaten importieren, damit sie Trends analysieren können.</span><span class="sxs-lookup"><span data-stu-id="d602d-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="d602d-153">Eine Power BI-Vorlage mit grundlegenden Metriken ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d602d-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="d602d-154">Moderatoren können diese Vorlage verwenden, um umfassend importierte Daten zu verknüpfen und ein Dashboard anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d602d-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="d602d-155">Sie müssen kein benutzerdefiniertes Dashboard erstellen.</span><span class="sxs-lookup"><span data-stu-id="d602d-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="d602d-156">Moderatoren können die Power BI-Vorlage auch anpassen, damit sie ihre spezifischen Anforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="d602d-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="d602d-157">Führen Sie die folgenden Schritte aus, um Bewertungs- und Prüfdaten im Commerce Site Builder herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="d602d-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d602d-158">Navigieren Sie zu **Start \> Bewertungen \> Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="d602d-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="d602d-159">Wählen Sie **Prüfdaten herunterladen** aus, um umfassende Bewertungs- und Prüfdaten im CSV-Format (Comma-Separated Values) herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="d602d-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="d602d-160">Bewertungs- und Prüftrends anzeigen</span><span class="sxs-lookup"><span data-stu-id="d602d-160">View ratings and reviews trends</span></span>

<span data-ttu-id="d602d-161">Moderatoren können die Power BI-Vorlage herunterladen, damit sie Trends in einem Dashboard anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="d602d-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="d602d-162">Führen Sie die folgenden Schritte aus, um Bewertungs- und Prüfdaten im Commerce Site Builder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d602d-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d602d-163">Navigieren Sie zu **Start \> Bewertungen \> Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="d602d-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="d602d-164">Wählen Sie **PowerBI-Vorlage** aus, um die Vorlage herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="d602d-164">Select **PowerBI template** to download the template.</span></span>

    ![Laden Sie die Power BI-Vorlage herunter](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="d602d-166">Öffnen Sie die heruntergeladene Vorlage durch Verwendung der Power BI-App.</span><span class="sxs-lookup"><span data-stu-id="d602d-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="d602d-167">Schließen Sie das Dialogfeld **Zugriff auf Webinhalt**, das angezeigt wird, und schließen Sie dann die angezeigte Fehlermeldung „Aktualisieren“.</span><span class="sxs-lookup"><span data-stu-id="d602d-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="d602d-168">Navigieren Sie zu **Startseite**, wählen Sie **Abfragen bearbeiten** und dann **Datenquelleneinstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="d602d-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="d602d-169">Wählen Sie im Dialogfeld **Datenquelleneinstellungen** die Option **Quelle ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="d602d-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="d602d-170">Geben Sie im Feld **URL** den Pfad der Prüfdaten ein, die Sie in der vorherigen Prozedur (Beispiel: **c:\\reviews\\ReviewsData.csv**) heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="d602d-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL-Feld im Dialogfeld „Kommagetrennte Werte“](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="d602d-172">Wählen Sie **OK** und dann **Änderungen anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="d602d-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="d602d-173">Es dauert ein bis zwei Minuten, um Ihre Änderungen auf die Datenquelle anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="d602d-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="d602d-174">Wählen Sie **Trendbilanz** aus, um die Trends für Bewertungen und Prüfungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d602d-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Trends für Bewertungen und Prüfungen](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="d602d-176">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d602d-176">Additional resources</span></span>

[<span data-ttu-id="d602d-177">Überblick über Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="d602d-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="d602d-178">Abonnieren zum Verwenden von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="d602d-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="d602d-179">Konfigurieren von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="d602d-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="d602d-180">Synchronisieren von Produktbewertungen in Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="d602d-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
