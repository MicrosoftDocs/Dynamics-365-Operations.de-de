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
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412587"
---
# <a name="manage-ratings-and-reviews"></a>Bewertungen und Prüfungen verwalten

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Bewertungen und Prüfungen im Microsoft Dynamics 365 Commerce-Site Builder verwalten.

## <a name="overview"></a>Übersicht

Dynamics 365 Commerce verwendet Microsoft Azure Cognitive Service, um den Prüftext automatisch zu moderieren, indem einfache Wörter redigiert werden. Darüber hinaus können Moderatoren Dynamics 365 Commerce-Site Builder zum Implementieren der folgenden manuellen Aufgaben verwenden:

- Moderieren Sie Prüfungen, indem Sie darauf antworten oder sie entfernen.
- Löschen Sie die Bewertungen eines Kunden auf Kundenwunsch.
- Importieren Sie Bewertungen und Überprüfungsdaten für alle Produkte in eine Power BI-Vorlage, damit Trends für Bewertungen und Überprüfungen analysiert werden können.

## <a name="read-a-review"></a>Lesen einer Prüfung 

Um eine Überprüfung in den Commerce Site Builder hochzuladen, folgen Sie diesen Schritten.

1. Navigieren Sie zu **Start \> Bewertungen \> Moderation**.
1. Verwenden Sie das Suchfeld oben rechts auf der Seite, um die angezeigten Bewertungen nach Produkt-ID, Produktname oder Bewertungstext zu filtern.

Mit zusätzlichen Filtern können Sie die Überprüfungen nach Zeitraum, Bewertung, Kanal oder Anliegenstatus einschränken (deaktiviert, beantwortet oder gemeldet).

![Moderations-Startseite](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>Auf Bewertung antworten 

Manchmal äußern Kunden, die ein Produkt gekauft haben, ihre Zufriedenheit oder Unzufriedenheit, oder sie verstehen nicht, wie das Produkt verwendet wird. Als Moderator können Sie eine Antwort auf eine Bewertung abgeben. Diese Antwort wird zusammen mit der Überprüfung auf der Website angezeigt. 

Um auf eine Überprüfung im Commerce Site Builder zu antworten, folgen Sie diesen Schritten.

1. Navigieren Sie zu **Start \> Bewertungen \> Moderation**.
1. Suchen Sie die Überprüfung, für die eine Antwort erforderlich ist, und wählen Sie sie aus.
1. Wählen Sie im Eigenschaftenbereich rechts **Eine Antwort hinzufügen** aus.
1. Geben Sie den Antworttext und den Namen ein, der für den Antwortenden angezeigt werden soll. Der Standardname des Antwortenden lautet **Moderator**.
1. Wählen Sie abschließend **Antwort senden** aus.

![Beantworten einer Bewertung](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Entfernen einer Bewertung 

Manchmal gibt es eine geschäftliche Rechtfertigung dafür, dass Moderatoren Kundenbewertungen entfernen. 

Um eine Überprüfung aus dem Commerce Site Builder zu entfernen, folgen Sie diesen Schritten.

1. Navigieren Sie zu **Start \> Bewertungen \> Moderation**.
1. Suchen Sie die Bewertung, die entfernt werden muss, und wählen Sie sie aus.
1. Wählen Sie im Eigenschaftenbereich rechts einen Grund für das Entfernen unter **Enfernungsüberprüfung** und dann **Entfernen** aus.
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>Löschen von Bewertungen eines Kunden auf Kundenwunsch 

Manchmal möchten Kunden, dass ihre Bewertungen und Bewertungsdaten dauerhaft von einer E-Commerce-Website gelöscht werden. Ein Moderator, der eine Entfernungsanforderung von einem Kunden erhält, kann die Kundendaten mithilfe der Funktion zum Löschen von Überprüfungen entfernen. Um die Daten eines Kunden zu finden und zu löschen, benötigt der Moderator die E-Mail-Adresse, mit der sich der Kunde angemeldet und Bewertungen abgegeben hat. 

Führen Sie die folgenden Schritte aus, um Kundendaten im Commerce Site Builder zu suchen und zu löschen.

1. Navigieren Sie zu **Startseite \> Bewertungen \> Löschen**.
1. Geben Sie im Feld **Suche nach Benutzern über die E-Mail-Adresse** die E-Mail-Adresse des Kunden ein und wählen Sie dann **Suchen** aus.
1. Wenn der Kunde eine Überprüfungsaktivität hat (z. B. Überprüfungsbeiträge, Abstimmungen zur Nützlichkeit der Bewertungen eines anderen Kunden oder Kommentare zur Bewertung eines anderen Kunden), werden die Ergebnisse angezeigt. Für jedes Element gibt es die Schaltfläche **Löschen**.
1. Wählen Sie für jedes Element, das gelöscht werden muss, **Löschen** aus. Wenn Sie zur Bestätigung aufgefordert werden, wählen Sie **Ja** aus. 
    
![Löschen von Kundendaten](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Es kann bis zu sieben Tage dauern, bis die Daten vollständig aus dem System entfernt wurden. Moderatoren sollten Kunden über diese Verzögerung informieren.
> - Wenn Kunden ihren Namen in ihren Kontoeinstellungen geändert haben, werden möglicherweise mehrere Elemente in den Suchergebnissen angezeigt. Um die Kundendaten vollständig zu löschen, muss der Moderator in diesem Fall **Löschen** für jeden Artikel auswählen. 

## <a name="download-ratings-and-reviews-data"></a>Herunterladen von Bewertungs- und Prüfungsdaten

Mit Commerce Site Builder können Moderatoren umfassend Bewertungs- und Prüfdaten importieren, damit sie Trends analysieren können. Eine Power BI-Vorlage mit grundlegenden Metriken ist verfügbar. Moderatoren können diese Vorlage verwenden, um umfassend importierte Daten zu verknüpfen und ein Dashboard anzuzeigen. Sie müssen kein benutzerdefiniertes Dashboard erstellen. Moderatoren können die Power BI-Vorlage auch anpassen, damit sie ihre spezifischen Anforderungen erfüllt. 

Führen Sie die folgenden Schritte aus, um Bewertungs- und Prüfdaten im Commerce Site Builder herunterzuladen.

1. Navigieren Sie zu **Start \> Bewertungen \> Berichterstellung**.
1. Wählen Sie **Prüfdaten herunterladen** aus, um umfassende Bewertungs- und Prüfdaten im CSV-Format (Comma-Separated Values) herunterzuladen.

## <a name="view-ratings-and-reviews-trends"></a>Bewertungs- und Prüftrends anzeigen

Moderatoren können die Power BI-Vorlage herunterladen, damit sie Trends in einem Dashboard anzeigen können.

Führen Sie die folgenden Schritte aus, um Bewertungs- und Prüfdaten im Commerce Site Builder anzuzeigen.

1. Navigieren Sie zu **Start \> Bewertungen \> Berichterstellung**.
1. Wählen Sie **PowerBI-Vorlage** aus, um die Vorlage herunterzuladen.

    ![Laden Sie die Power BI-Vorlage herunter](media/rnr-moderation-reports.png) 

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]