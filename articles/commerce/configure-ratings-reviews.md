---
title: Bewertungen und Prüfungen konfigurieren
description: In diesem Artikel wird beschrieben, wie Sie Ihre E-Commerce-Webseite konfigurieren, um Beurteilungen und Bewertungen in Microsoft Dynamics 365 Commerce anzuzeigen.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 27b1beddd474a2ca4db73f8e344b2d85934c43b1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276864"
---
# <a name="configure-ratings-and-reviews"></a>Bewertungen und Prüfungen konfigurieren

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Ihre E-Commerce-Webseite konfigurieren, um Beurteilungen und Bewertungen in Microsoft Dynamics 365 Commerce anzuzeigen.

Bewertungen und Rezensionen auf E-Commerce-Websites helfen den Kunden, sich über Produkte zu informieren, bevor sie eine Kaufentscheidung treffen, indem sie ihnen zeigen, was andere Kunden über diese Produkte denken. Für E-Commerce-Websites sind Bewertungen und Prüfungen auch ein Mechanismus für das Zusammenfassen des Kundenfeedbacks zu Produkten. 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Konfigurieren einer Site, die Bewertungen und Prüfungen anzeigt

Konfigurationswerte von Beurteilungen und Prüfungen wie die Mandant-Kennung, Prüfung der Textlänge und Prüfung der Titellänge werden auf Sitebene konfiguriert. 

Um eine Site zu konfigurieren, damit Bewertungen und Prüfungen angezeigt werden, führen Sie die folgenden Schritte aus. 

1. Gehen Sie zu **Startseite \> Sites**.
1. Wählen Sie den Namen Ihrer Site. 
1. Gehen Sie zu **Site-Einstellungen \> Erweiterungen**. 
1. Geben Sie in das Feld **Bewertungstext maximale Länge** die maximale Anzahl von Zeichen ein, die ein Bewertungstext haben kann (z.B. **1000**). 
1. Geben Sie in das Feld **Rezensionstitel maximale Länge** die maximale Anzahl von Zeichen ein, die ein Rezensionstitel haben kann (z.B. **55**). 
1. Wählen Sie **Speichern und veröffentlichen**. 

Die folgende Abbildung zeigt, wie diese Kongiguration aussieht in Dynamics 365 Commerce.

![Konfigurieren einer Site, die Bewertungen und Prüfungen anzeigt.](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Verknüpfen Sie eine Produktbewertung mit dem Bewertungsbereich auf einer PDP

Eine Produktbewertung wird unter dem Produkttitel oben auf der PDP angezeigt. Die Produktbewertung kann so konfiguriert werden, dass diese mit dem Bereich **Bewertung** der gleichen PDP verknüpft ist. 

Wenn Sie eine Produktbewertung mit dem Abschnitt **Bewertung** des PDP bewerten, führen Sie die folgenden Schritte aus.

1. Öffnen Sie die PDP-Vorlage. 
1. Gehen Sie zu **Containerfeld-Moduleinstellungen kaufen**.
1. Wählen Sie unter **Feld kaufen** die Option **Produktbewertungen** und anschließend das Kontrollkästchen **Verknüpfen des vollständigen Prüfungsmoduls**.

Die folgende Abbildung zeigt, wie diese Kongiguration aussieht in Dynamics 365 Commerce.

![Verknüpfen Sie eine Produktbewertung mit dem Bewertungsbereich auf einer PDP.](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Konfigurieren Sie den Link für die Datenschutz- und Richtlinienseite

Um den Link für die Datenschutz- und Richtlinienseite zu konfigurieren, gehen Sie wie folgt vor.

1. Gehen Sie zu **Startseite \> Sites**.
1. Wählen Sie den Namen Ihrer Site. 
1. Gehen Sie zu **Site-Einstellungen \> Erweiterungen**.
1. Auf der Registerkarte **Arbeitspläne** unter **RNR-Datenschutz und Richtlinie**, wählen Sie **Fügen Sie einen Link hinzu** aus. Wenn bereits ein Link eingegeben wurde und Sie diesen ersetzen möchten, wählen Sie den Link. 
1. Im Dialogfeld **Fügen Sie einen Link hinzu** wählen Sie den Link für die Datenschutzrichtlinienseite und wählen Sie **OK**. 
1. Wählen Sie **Speichern und veröffentlichen**. 

Die folgende Abbildung zeigt, wie diese Kongiguration aussieht in Dynamics 365 Commerce.

![Konfigurieren Sie den Link für die Datenschutz- und Richtlinienseite.](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>Konfigurieren Sie Bewertungen und Rezensionsmodule auf den Produktdetailseiten

Informationen zur Konfiguration von Bewertungen und Rezensionsmodulen auf den Produktdetailseiten finden Sie unter [Bewertungen und Rezensionsmodule](ratings-reviews-modules.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Bewertungen und Prüfungen](ratings-reviews-overview.md)

[Nutzung von Bewertungen und Prüfungen aktivieren](opt-in-ratings-reviews.md)

[Bewertungen und Prüfungen verwalten](manage-reviews.md)

[Synchronisieren von Produktbewertungen in Dynamics 365 Retail](sync-product-ratings.md)

[Manuelle Veröffentlichung von Bewertungen und Prüfungen durch einen Moderator aktivieren](manual-publish-rating-reviews.md)

[Bewertungen und Rezensionen importieren und exportieren](import-export-reviews.md)

[Authentifizierung zwischen Diensten konfigurieren](service-to-service-auth.md)

[Häufig gestellte Fragen zu Bewertungen und Prüfungen](ratings-reviews-faq.md)

[Bewertungs‑ und Prüfungsmodule](ratings-reviews-modules.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
