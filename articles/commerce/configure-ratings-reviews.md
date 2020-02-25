---
title: Konfigurieren von Bewertungen und Prüfungen
description: In diesem Thema wird beschrieben, wie Sie Ihre E-Commerce-Webseite konfigurieren, um Beurteilungen und Bewertungen in Microsoft Dynamics 365 Commerce anzuzeigen.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002196"
---
# <a name="configure-ratings-and-reviews"></a>Konfigurieren von Bewertungen und Prüfungen


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Ihre E-Commerce-Webseite konfigurieren, um Beurteilungen und Bewertungen in Microsoft Dynamics 365 Commerce anzuzeigen.

## <a name="overview"></a>Übersicht

Bewertungen und Prüfungen auf der E-Commerce-Website helfen Kunden, mehr über die Produkte zu erfahren, bevor Sie eine Einkaufentscheidung machen, indem angezeigt wird, was Kunden über diese Produkte denken. Für E-Commerce-Websites sind Bewertungen und Prüfungen auch ein Mechanismus für das Zusammenfassen des Kundenfeedbacks zu Produkten. 

Bewertungen werden in Produktlisteseiten, Kategorielistenseiten, Suchergebnisseiten und anderen Standortsseiten angezeigt. Bewertungshistogramme und Produktprüfungen werden auf Produktdetailseiten (PDPs) angezeigt. Eine Schaltfläche **Eine Bewertun schreiben** ermöglicht Kunden, Bewertungen und Prüfungen für ein Produkt senden.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Bewertungs- und Prüfungsmodule in PDPs 

Drei Module zeigen die Zusammenfassungen der Beurteilungen und Prüfungen an auf PDPs:

- Modul Bewertung schreiben
- Modul Produktbewertungsliste
- Bewertungshistogrammmodul
 
Die folgende Abbildung zeigt, wie die Bewertungen und Module aussehen auf einer PDP.

![Bewertungs- und Prüfungsmodule in einer PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Informationen darüber, wie PDP-Vorlagen und -Layouts optimiert werden, sodass Sie die Konfigurationen der Module für Beurteilungen und Prüfungen unter verschiedenen PDPs auf Ihrer E-Commerce-Webseite freigeben können, finden Sie unter. [Vorlagen und Layoutüberblick](templates-layouts-overview.md).

Die folgende Abbildung zeigt, wie das Dialogfeld **Modul hinzufügen** Bewertungs- und Prüfungsmodule in Dynamics 365 Commerce darstellt.

![Fügen Sie ein Moduldialogfeld hinzu](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Modul Bewertung schreiben

Das Modul Bewertung schreiben enhält eine Schaltfläche **Bewertung schreiben**, bei der sich Benutzer anmelden, eine Bewertung zuweisen und eine Überprüfung eines Produkts schreiben können. Mit diesem Modul können Benutzer eine Bewertung oder Prüfung bearbeiten, die sie zuvor übermittelt haben. Dieses Modul wird in der Regel über den Produktbewertungs-Histogramm- und Produktbewertungslistenmodulen auf einem PDP angezeigt.

Die folgende Abbildung zeigt das Dialogfeld **Eine Bewertung schreiben**, das angezeigt wird, wenn ein Debitor **Eine Bewertung schreiben** auswählt. Der Debitor kann dieses Dialogfeld verwenden, um eine Bewertung und eine Prüfung zu übermitteln.

![Schreiben Sie ein Bewertungsdialogfeld](media/rnr-eCommerce-write-review-module.png)

In der folgenden Tabelle wird die Eigenschaft für das Modul Bewertung schreiben angezeigt, die im Erstellungstool konfiguriert werden muss.

| Eigenschaftenname | Wert        | Eigenschaftbeschreibung                 |
|---------------|--------------|--------------------------------------|
| Name          | Bewertung schreiben | Der Name des Moduls Bewertung schreiben |

### <a name="ratings-histogram-module"></a>Bewertungshistogrammmodul

Das Bewertungshistogrammmodul zeigt ein Bewertungshistogramm. Dieses Modul wird zwischen dem Modul Bewertung schreiben und dem Produktbewertungslistenmodul auf einem PDP angezeigt.

Das Bewertungshistogrammmodul erfordert keine Konfiguration. Sie müssen das Modul in der PDP-Vorlage nur hinzufügen. 

Die folgende Abbildung zeigt, wie eine PDP-Vorlage in Dynamics 365 Commerce aussieht, wenn Prüfungs- und Bewertungsmodule zur Anzeige auf PDPs konfiguriert werden.

![PDP-Vorlage, wenn Bewertungen und Prüfungen für die Anzeige auf PDPs konfiguriert werden](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Modul Produktbewertungsliste

Das Produktprüfungs-Listenmodul zeigt eine Liste der Produktprüfungen zusammen mit Sortierung, Filter, und Paginierungsoptionen an. Dieses wird normalerweise nach dem Bewertungshistogrammmodul auf einem PDP angezeigt.

In der folgenden Tabelle wird die Eigenschaft für das Produktbewertungslistenmodul angezeigt, das im Erstellungstool konfiguriert werden muss.

| Eigenschaftenname              | Wert | Eigenschaftbeschreibung |
|----------------------------|-------| ---------------------|
| Auf jeder Seite angezeigte Bewertungen | 10    | Die Anzahl der Bewertungen, die gleichzeitig auf einem PDP angezeigt werden sollen. Schaltflächen **Weiter** und **Vorherige** werden eingeschlossen, damit Benutzer die Seiten der Bewertungen durchsuchen können. |

#### <a name="ratings-histogram--summary-view"></a>Bewertungshistogramm - Zusammenfassungsansicht

Das Produktprüfungs-Listenmodul enthält einen Slot, in dem Sie ein Bewertungshistogrammmodul hinzufügen können. Die folgende Abbildung zeigt, wie Sie ein Bewertungshistogrammmodul im Produktprüfungs-Listenmodul in Dynamics 365 Commerce hinzufügen können.

![Das Hinzufügen eines Bewertungshistogrammmoduls in einem Produktbewertungslistenmodul](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Konfigurieren einer Site, die Bewertungen und Prüfungen anzeigt

Konfigurationswerte von Beurteilungen und Prüfungen wie die Mandant-Kennung, Prüfung der Textlänge und Prüfung der Titellänge werden auf Sitebene konfiguriert. 

Um eine Site zu konfigurieren, damit Bewertungen und Prüfungen angezeigt werden, führen Sie die folgenden Schritte aus. 

1. Gehen Sie zu **Startseite \> Sites**.
1. Wählen Sie den Namen Ihrer Site. 
1. Gehen Sie zu **Siteverwaltung \> Erweiterbarkeit**. 
1. Wählen Sie im Feld **Maximale Textlänge prüfen** geben Sie die maximale Anzahl von Zeichen ein, die der Prüfungstext haben darf (z.B. **1000**). 
1. Im Feld **Maximale Titellänge prüfen** geben Sie die maximale Anzahl von Zeichen ein, die der Titel haben darf (z.B. **55**). 
1. Wählen Sie **Speichern und veröffentlichen**. 

Die folgende Abbildung zeigt, wie diese Kongiguration aussieht in Dynamics 365 Commerce.

![Konfigurieren einer Site, die Bewertungen und Prüfungen anzeigt](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Verknüpfen Sie eine Produktbewertung mit dem Bewertungsbereich auf einer PDP

Eine Produktbewertung wird unter dem Produkttitel oben auf der PDP angezeigt. Die Produktbewertung kann so konfiguriert werden, dass diese mit dem Bereich **Bewertung** der gleichen PDP verknüpft ist. 

Wenn Sie eine Produktbewertung mit dem Abschnitt **Bewertung** des PDP bewerten, führen Sie die folgenden Schritte aus.

1. Öffnen Sie die PDP-Vorlage. 
1. Gehen Sie zu **Containerfeld-Moduleinstellungen kaufen**.
1. Wählen Sie unter **Feld kaufen** die Option **Produktbewertungen** und anschließend das Kontrollkästchen **Verknüpfen des vollständigen Prüfungsmoduls**.

Die folgende Abbildung zeigt, wie diese Kongiguration aussieht in Dynamics 365 Commerce.

![Verknüpfen Sie eine Produktbewertung mit dem Bewertungsbereich auf einer PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Konfigurieren Sie den Link für die Datenschutz- und Richtlinienseite

Um den Link für die Datenschutz- und Richtlinienseite zu konfigurieren, gehen Sie wie folgt vor.

1. Gehen Sie zu **Startseite \> Sites**.
1. Wählen Sie den Namen Ihrer Site. 
1. Gehen Sie zu **Siteverwaltung \> Erweiterbarkeit**
1. Auf der Registerkarte **Arbeitspläne** unter **RNR-Datenschutz und Richtlinie**, wählen Sie **Fügen Sie einen Link hinzu** aus. Wenn bereits ein Link eingegeben wurde und Sie diesen ersetzen möchten, wählen Sie den Link. 
1. Im Dialogfeld **Fügen Sie einen Link hinzu** wählen Sie den Link für die Datenschutzrichtlinienseite und wählen Sie **OK**. 
1. Wählen Sie **Speichern und veröffentlichen**. 

Die folgende Abbildung zeigt, wie diese Kongiguration aussieht in Dynamics 365 Commerce.

![Konfigurieren Sie den Link für die Datenschutz- und Richtlinienseite](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Bewertungen und Prüfungen](ratings-reviews-overview.md)

[Abonnieren zum Verwenden von Bewertungen und Prüfungen](opt-in-ratings-reviews.md)

[Verwalten von Bewertungen und Prüfungen](manage-reviews.md)

[Synchronisieren von Produktbewertungen in Dynamics 365 Retail](sync-product-ratings.md)
