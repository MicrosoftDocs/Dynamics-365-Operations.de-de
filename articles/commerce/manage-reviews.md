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
# <a name="manage-ratings-and-reviews"></a>Verwalten von Bewertungen und Prüfungen

[!include [banner](includes/banner.md)]

In diesem Thema wird das Verwalten von Bewertungen und Überprüfungen mit dem Moderationstool für Bewertungen und Überprüfungen von Microsoft Dynamics 365 Commerce erklärt.

## <a name="overview"></a>Übersicht

Dynamics 365 Commerce verwendet Microsoft Azure Cognitive Service, um den Prüftext automatisch zu moderieren, indem einfache Wörter redigiert werden. Darüber hinaus können Moderatoren das Moderationstool für Bewertungen und Prüfungen für die folgenden manuellen Aufgaben verwenden:

- Moderieren Sie Prüfungen, indem Sie darauf antworten oder sie entfernen.
- Löschen Sie die Bewertungen eines Kunden auf Kundenwunsch.
- Importieren Sie Bewertungen und Überprüfungsdaten für alle Produkte in eine Power BI-Vorlage, damit Trends für Bewertungen und Überprüfungen analysiert werden können.

## <a name="access-ratings-and-reviews-moderation-features"></a>Greifen Sie auf Moderationsfunktionen für Bewertungen zu

Führen Sie die folgenden Schritte aus, um im E-Commerce-Website-Verwaltungstool auf die Moderationsfunktionen für Bewertungen und Überprüfungen zuzugreifen.

1. Melden Sie sich bei [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com) an.
1. Öffnet das Projekt, das die Umgebung enthält, in der Sie E-Commerce initialisieren möchten.
1. Im Abschnitt **Umgebung** wählen Sie die Umgebung.
1. Wählen Sie unter **Umgebungsfunktionen** die Option **Einzelhandelsverwaltung** aus.
1. Auf der **E-Commerce** Registrkarte unter **Links**, wählen Sie **E-Commerce-Site-Management-Tool**.

## <a name="read-a-review"></a>Lesen einer Prüfung 

1. Navigieren Sie zu **Start \> Bewertungen \> Moderation**.
1. Verwenden Sie das Suchfeld oben rechts auf der Seite, um die angezeigten Bewertungen nach Produkt-ID, Produktname oder Bewertungstext zu filtern.

Mit zusätzlichen Filtern können Sie die Überprüfungen nach Zeitraum, Bewertung, Kanal oder Anliegenstatus einschränken (deaktiviert, beantwortet oder gemeldet).

![Moderations-Startseite](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>Auf Bewertung antworten 

Manchmal äußern Kunden, die ein Produkt gekauft haben, ihre Zufriedenheit oder Unzufriedenheit, oder sie verstehen nicht, wie das Produkt verwendet wird. Als Moderator können Sie eine Antwort auf eine Bewertung abgeben. Diese Antwort wird zusammen mit der Überprüfung auf der Website angezeigt. 

Gehen Sie folgendermaßen vor, um auf eine Bewertung zu antworten.

1. Navigieren Sie zu **Start \> Bewertungen \> Moderation**.
1. Suchen Sie die Überprüfung, für die eine Antwort erforderlich ist, und wählen Sie sie aus.
1. Wählen Sie im Eigenschaftenbereich rechts **Eine Antwort hinzufügen** aus.
1. Geben Sie den Antworttext und den Namen ein, der für den Antwortenden angezeigt werden soll. Der Standardname des Antwortenden lautet **Moderator**.
1. Wählen Sie abschließend **Antwort senden** aus.

![Beantworten einer Bewertung](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Entfernen einer Bewertung 

Manchmal gibt es eine geschäftliche Rechtfertigung dafür, dass Moderatoren Kundenbewertungen entfernen. 

Gehen Sie folgendermaßen vor, um auf eine Bewertung zu entfernen.

1. Navigieren Sie zu **Start \> Bewertungen \> Moderation**.
1. Suchen Sie die Bewertung, die entfernt werden muss, und wählen Sie sie aus.
1. Wählen Sie im Eigenschaftenbereich rechts einen Grund für das Entfernen und dann **Entfernen** aus.
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>Löschen von Bewertungen eines Kunden auf Kundenwunsch 

Manchmal möchten Kunden, dass ihre Bewertungen und Bewertungsdaten dauerhaft von einer E-Commerce-Website gelöscht werden. Ein Moderator, der eine Entfernungsanforderung von einem Kunden erhält, kann die Kundendaten mithilfe der Funktion zum Löschen von Überprüfungen entfernen. Um die Daten eines Kunden zu finden und zu löschen, benötigt der Moderator die E-Mail-Adresse, mit der sich der Kunde angemeldet und Bewertungen abgegeben hat. 

Gehen Sie folgendermaßen vor, um Kundendaten zu suchen und zu löschen.

1. Navigieren Sie zu **Startseite \> Bewertungen \> Löschen**.
1. Geben Sie im Feld **Über die E-Mail-Adresse nach Benutzern suchen** die E-Mail-Adresse des Kunden ein und wählen Sie dann **Suchen** aus.
1. Wenn der Kunde eine Überprüfungsaktivität hat (z. B. Überprüfungsbeiträge, Abstimmungen zur Nützlichkeit der Bewertungen eines anderen Kunden oder Kommentare zur Bewertung eines anderen Kunden), werden die Ergebnisse angezeigt. Für jedes Element gibt es die Schaltfläche **Löschen**.
1. Wählen Sie für jedes Element, das gelöscht werden muss, **Löschen** aus. Wenn Sie zur Bestätigung aufgefordert werden, wählen Sie **Ja** aus. 
    
![Löschen von Kundendaten](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Es kann bis zu sieben Tage dauern, bis die Daten vollständig aus dem System entfernt wurden. Moderatoren sollten Kunden über diese Verzögerung informieren.
> - Wenn Kunden ihren Namen in ihren Kontoeinstellungen geändert haben, werden möglicherweise mehrere Elemente in den Suchergebnissen angezeigt. Um die Kundendaten vollständig zu löschen, muss der Moderator in diesem Fall **Löschen** für jeden Artikel auswählen. 

## <a name="download-ratings-and-reviews-data"></a>Herunterladen von Bewertungs- und Prüfungsdaten

Mit dem Moderationstool für Bewertungen und Überprüfungen können Moderatoren, umfassend Bewertungs- und Prüfdaten importieren, damit sie Trends analysieren können. Eine Power BI-Vorlage mit grundlegenden Metriken ist verfügbar. Moderatoren können diese Vorlage verwenden, um umfassend importierte Daten zu verknüpfen und ein Dashboard anzuzeigen. Sie müssen kein benutzerdefiniertes Dashboard erstellen. Moderatoren können die Power BI-Vorlage auch anpassen, damit sie ihre spezifischen Anforderungen erfüllt. 

Befolgen Sie diese Schritte, um Bewertungs- und Prüfdaten herunterzuladen.

1. Navigieren Sie zu **Start \> Bewertungen \> Berichterstellung**.
1. Wählen Sie **Prüfdaten herunterladen** aus, um Bewertungs- und Prüfdaten im CSV-Format (Comma-Separated Values) herunterzuladen.

## <a name="view-ratings-and-reviews-trends"></a>Bewertungs- und Prüftrends anzeigen

Moderatoren können die Power BI-Vorlage herunterladen, damit sie Trends in einem Dashboard anzeigen können.

Befolgen Sie diese Schritte, um Bewertungs- und Prüftrends anzuzeigen.

1. Navigieren Sie zu **Start \> Bewertungen \> Berichterstellung**.
1. Wählen Sie **PowerBI-Vorlage** aus, um die Vorlage herunterzuladen.

    ![Herunterladen der Power BI-Vorlage](media/rnr-moderation-reports.png) 

1. Öffnen Sie die heruntergeladene Vorlage durch Verwendung der Power BI-App. Schließen Sie das Dialogfeld **Zugriff auf Webinhalt**, das angezeigt wird, und schließen Sie dann die angezeigte Fehlermeldung „Aktualisieren“.
1. Navigieren Sie zu **Startseite**, wählen Sie **Abfragen bearbeiten** und dann **Datenquelleneinstellungen** aus.
1. Wählen Sie im Dialogfeld **Datenquelleneinstellungen** die Option **Quelle ändern** aus.
1. Geben Sie im Feld **URL** den Pfad der Prüfdaten ein, die Sie in der vorherigen Prozedur (Beispiel: **c:\\reviews\\ReviewsData.csv**) heruntergeladen haben.

    ![URL-Feld im Dialogfeld „Kommagetrennte Werte“](media/rnr-powerbi-datasource-settings.png) 

1. Wählen Sie **OK** und dann **Änderungen anwenden** aus. Es dauert ein bis zwei Minuten, um Ihre Änderungen auf die Datenquelle anzuwenden.
1. Wählen Sie **Trendbilanz** aus, um die Trends für Bewertungen und Prüfungen anzuzeigen.

    ![Trends für Bewertungen und Prüfungen](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Bewertungen und Prüfungen](ratings-reviews-overview.md)

[Abonnieren zum Verwenden von Bewertungen und Prüfungen](opt-in-ratings-reviews.md)

[Konfigurieren von Bewertungen und Prüfungen](configure-ratings-reviews.md)

[Synchronisieren von Produktbewertungen in Dynamics 365 Retail](sync-product-ratings.md)
