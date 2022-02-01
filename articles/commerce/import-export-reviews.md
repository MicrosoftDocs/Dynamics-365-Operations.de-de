---
title: Bewertungen und Rezensionen importieren und exportieren
description: In diesem Thema wird beschrieben, wie Sie Produktbewertungen und Rezensionen in Microsoft Dynamics 365 Commerce importieren und exportieren.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 3ae85f21f7a78d56621aed60527207badcee9c75
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968532"
---
# <a name="import-and-export-ratings-and-reviews"></a>Bewertungen und Rezensionen importieren und exportieren

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Produktbewertungen und Rezensionen in Microsoft Dynamics 365 Commerce importieren und exportieren.

Dynamics 365 Commerce bietet [Bewertungen und Rezensionen](ratings-reviews-overview.md) als eine Mehrkanallösung. Beim Wechsel auf die Bewertungs- und Rezensionslösung von Dynamics 365 Commerce sollten Sie möglicherweise Ihre vorhandenen Bewertungs- und Rezensionsdaten auf die E-Commerce-Plattform verschieben. Je nach Ihren geschäftlichen Anforderungen sollten Sie möglicherweise auch Bewertungs- und Rezensionsdaten aus Commerce exportieren. Mit einem Power Automate Connector können Sie Bewertungen und Rezensionen in Commerce importieren und aus Commerce exportieren.

> [!NOTE]
> Informationen zu den ersten Schritten mit Logik-Flows in Power Automate finden Sie unter [Erstellen eines Cloud-Flows in Power Automate](/power-automate/get-started-logic-flow).

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie Bewertungen und Rezensionen importieren und exportieren können, müssen Sie die folgenden Voraussetzungen erfüllen:

- Die Bewertungs- und Rezensionen-Lösung muss für Ihre E-Commerce-Site auf der Commerce-Plattform aktiviert sein. Weitere Informationen finden Sie unter [Melden Sie sich an, um Bewertungen und Rezensionen zu verwenden](opt-in-ratings-reviews.md).
- Der Dynamics 365 Ratings and Reviews Power App Connector muss konfiguriert werden, um entweder die Aktionen „Bewertungen senden“ oder „Bewertungen exportieren“ in Power Automate zu aktivieren. Weitere Informationen finden Sie unter [Dynamics 365 Commerce- Bewertungen und Rezensionen (Vorschau)](/connectors/dynamics365ratingsre/).
- Die Authentifizierung zwischen Diensten (S2S) muss konfiguriert werden, um die Anwendungsprogrammierschnittstelle (API) für Bewertungen und Rezensionen von außerhalb von Commerce sicher aufzurufen. Weitere Informationen finden Sie unter [Authentifizierung zwischen Diensten konfigurieren](service-to-service-auth.md).

## <a name="import-ratings-and-reviews"></a>Bewertungen und Rezensionen importieren

Um Bewertungs- und Rezensionen-Daten aus Ihrem bestehenden System in Commerce zu importieren, müssen Sie den Dynamics 365 Ratings and Review Power Automate-Connector entweder in einem vorhandenen Power Automate-Flow oder einem neuen hinzufügen. Weitere Informationen finden Sie unter [Dynamics 365 Commerce- Bewertungen und Rezensionen (Vorschau)](/connectors/dynamics365ratingsre/).

> [!IMPORTANT]
> Vor der Ausführung dieses Schritts müssen Sie [S2S-Authentifizierung konfigurieren](service-to-service-auth.md).

Zum Importieren von Bewertungen und Rezensionen in Commerce mithilfe des Dynamics 365 Ratings and Reviews Power Automate-Connectors befolgen Sie diese Schritte.

1. Wählen Sie die Aktion **Benutzerbewertung senden**.
1. Stellen Sie eine Verbindung her, indem Sie Azure Active Directory (Azure AD) App-Informationen verwenden, die erstellt wurden, als Sie die S2S-Authentifizierung konfiguriert haben. Weitere Informationen finden Sie unter [Authentifizierung zwischen Diensten konfigurieren](service-to-service-auth.md).
1. Die **Benutzerbewertung senden**-Aktion nimmt jeweils eine Bewertung vor. Wiederholen Sie daher die Aktion. Verwenden Sie die Quellbewertung als Liste, um Sammelbewertungen einzureichen.
    
## <a name="export-ratings-and-reviews"></a>Bewertungen und Rezensionen exportieren

Um Bewertungs- und Rezensionen-Daten aus Commerce zu exportieren, müssen Sie den Dynamics 365 Ratings and Review Power Automate-Connector entweder in einem vorhandenen Power Automate-Flow oder einem neuen hinzufügen. Weitere Informationen finden Sie unter [Dynamics 365 Commerce- Bewertungen und Rezensionen (Vorschau)](/connectors/dynamics365ratingsre/).

Zum Exportieren von Bewertungen und Rezensionen aus Commerce mithilfe des Dynamics 365 Ratings and Reviews Power Automate-Connectors befolgen Sie diese Schritte.

1. Wählen Sie die Aktion **Alle Bewertungen exportieren** aus.
1. Schließen Sie die Aktion ab. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Bewertungen und Prüfungen](ratings-reviews-overview.md)

[Nutzung von Bewertungen und Prüfungen aktivieren](opt-in-ratings-reviews.md)

[Bewertungen und Prüfungen verwalten](manage-reviews.md)

[Bewertungen und Prüfungen konfigurieren](configure-ratings-reviews.md)

[Produktbewertungen synchronisieren](sync-product-ratings.md)

[Manuelle Veröffentlichung von Bewertungen und Prüfungen durch einen Moderator aktivieren](manual-publish-rating-reviews.md)

[Authentifizierung zwischen Diensten konfigurieren](service-to-service-auth.md)

[Häufig gestellte Fragen zu Bewertungen und Prüfungen](ratings-reviews-faq.md)
