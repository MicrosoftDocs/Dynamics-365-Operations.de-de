---
title: Authentifizierung zwischen Diensten konfigurieren
description: In diesem Artikel wird beschrieben, wie Sie die Authentifizierung zwischen Diensten in Microsoft Dynamics 365 Commerce zum sicheren Aufrufen von Service-APIs für Bewertungen und Rezensionen konfigurieren.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: acb3a6220d146d32bbeb5bd8169033bc897ec3fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871606"
---
# <a name="configure-service-to-service-authentication"></a>Authentifizierung zwischen Diensten konfigurieren

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie die Authentifizierung zwischen Diensten (S2S)in Microsoft Dynamics 365 Commerce zum sicheren Aufrufen von Anwendungsprogrammierschnittstellen (APIs) für Bewertungen und Rezensionen konfigurieren.

Dynamics 365 Commerce bietet [Bewertungen und Rezensionen](ratings-reviews-overview.md) als eine Mehrkanallösung. Diese Lösung ermöglicht den Zugriff auf Service-APIs von außerhalb des Handels, sodass verschiedene Aufgaben ausgeführt werden können. Zu diesen Aufgaben gehören das Importieren von Bewertungen und Rezensionen aus Ihrem externen System in Commerce und das Exportieren von Bewertungen und Rezensionen aus Commerce. Damit Commerce APIs für Bewertungs- und Rezensionsdienste sicher aufrufen kann, müssen Sie zuerst die S2S-Authentifizierung konfigurieren, indem Sie die Verfahren in diesem Artikel ausführen.

## <a name="add-a-new-app-registration"></a>Neue App-Registrierung hinzufügen

Bevor Sie eine neue App-Registrierung hinzufügen, müssen Sie mithilfe von [Azure-Portal](https://portal.azure.com) eine Anwendung erstellen. Wenn Sie eine App in Azure Active Directory (Azure AD) registrieren und die Authentifizierung aktivieren möchten, folgen Sie den Schritten in [Verwenden von Azure Active Directory mit einem benutzerdefinierten Connector in Power Automate](/connectors/custom-connectors/azure-active-directory-authentication).

Sammeln Sie die folgenden IDs aus dem Azure-Portal. Sie benötigen diese IDs in den folgenden Schritten.

- Clientanwendungskennung
- Client-Verzeichnis-ID (Mandant)

Führen Sie die folgenden Schritte aus, um eine neue App-Registrierung im Commerce Site Builder hinzuzufügen.

1. Navigieren Sie zu **Start \> Bewertungen \> Einstellungen**.
1. Unter **Authentifizierung zwischen Diensten (S2S)** wählen Sie **Verwalten**.

    ![Schaltfläche „Verwalten“ im Abschnitt „Authentifizierung zwischen Diensten (S2S)“ im Commerce-Site-Builder.](media/Ratings-reviews-settings-service-to-service-authentication.png)

1. Im **S2S-App-Einträge**-Bereich, der auf der rechten Seite angezeigt wird, wählen Sie **Eine neue S2S-App-Registrierung hinzufügen**.
1. Geben Sie im Dialogfeld **S2S-App-Eintrag hinzufügen** die erforderlichen Informationen ein. Verwenden Sie die Werte aus Ihrer Azure-Anwendungsregistrierung.

    - **Name** – Geben Sie den Namen Ihre Anwendung ein (z. B. **Fabrikam-App**).
    - **Client-App-ID** – Geben Sie die Anwendungs-ID ein (zum Beispiel **00000000-0000-0000-0000-000000000000**).
    - **Verzeichnis-ID (Mandant)** – Geben Sie die Verzeichnis-ID ein (z. B. **00000000-0000-0000-0000-000000000000**).

    ![Fügen Sie das Dialogfeld „S2S-App-Eintrag“ im Commerce-Website-Generator hinzu.](media/Ratings-reviews-settings-S2S-APP-entry.png)

1. Wählen Sie **Senden**. Der Namen Ihrer S2S-Anwendung sollte in der Liste im Bereich **S2S-App-Einträge** erscheinen.
1. Schließen Sie den Bereich **S2S-App-Einträge**.
1. Wählen Sie **Speichern** aus.

## <a name="edit-an-existing-app-registration"></a>Bearbeiten einer vorhandenen App-Registrierung

Wenn Sie eine vorhandene App-Registrierung im Commerce Site Builder bearbeiten möchten, führen Sie diese Schritte aus.

1. Navigieren Sie zu **Start \> Bewertungen \> Einstellungen**.
1. Unter **Authentifizierung zwischen Diensten (S2S)** wählen Sie **Verwalten**.
1. Im **S2S-App-Einträge**-Bereich wählen Sie das Stiftsymbol neben dem Eintrag, den Sie bearbeiten möchten.
1. Aktualisieren Sie die Werte in den Feldern **Name**, **Client-App-ID** und **Verzeichnis-ID (Mandant)** nach Bedarf.
1. Wählen Sie **Senden**.
1. Schließen Sie den Bereich **S2S-App-Einträge**.
1. Wählen Sie **Speichern** aus.

## <a name="remove-an-existing-app-registration"></a>Entfernen einer vorhandenen App-Registrierung

Wenn Sie eine vorhandene App-Registrierung im Commerce Site Builder entfernen möchten, führen Sie diese Schritte aus.

1. Navigieren Sie zu **Start \> Bewertungen \> Einstellungen**.
1. Unter **Authentifizierung zwischen Diensten (S2S)** wählen Sie **Verwalten**.
1. Im **S2S-App-Einträge**-Bereich wählen Sie das Papierkorbsymbol neben dem Eintrag, den Sie entfernen möchten. Der Eintrag wird aus der Liste entfernt.
1. Schließen Sie den Bereich **S2S-App-Einträge**.
1. Wählen Sie **Speichern** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Bewertungen und Prüfungen](ratings-reviews-overview.md)

[Nutzung von Bewertungen und Prüfungen aktivieren](opt-in-ratings-reviews.md)

[Bewertungen und Prüfungen verwalten](manage-reviews.md)

[Bewertungen und Prüfungen konfigurieren](configure-ratings-reviews.md)

[Produktbewertungen synchronisieren](sync-product-ratings.md)

[Manuelle Veröffentlichung von Bewertungen und Prüfungen durch einen Moderator aktivieren](manual-publish-rating-reviews.md)

[Bewertungen und Rezensionen importieren und exportieren](import-export-reviews.md)

[Häufig gestellte Fragen zu Bewertungen und Prüfungen](ratings-reviews-faq.md) 
