---
title: Bewertungs‑ und Prüfungsmodule
description: Dieser Artikel umfasst Bewertungen und Rezensionsmodule, die auf den Produktdetailseiten in Microsoft Dynamics 365 Commerce verwendet werden.
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ede42caac78dc48fa6315a2d3c22f1e0f12f0810
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283586"
---
# <a name="ratings-and-reviews-modules"></a>Bewertungs‑ und Prüfungsmodule

[!include [banner](includes/banner.md)]

Dieser Artikel umfasst Bewertungen und Rezensionsmodule, die auf den Produktdetailseiten (PDPs) in Microsoft Dynamics 365 Commerce verwendet werden.

Bewertungen und Rezensionen auf E-Commerce-Websites helfen Kunden, sich über Produkte zu informieren, bevor sie eine Kaufentscheidung treffen, und sind auch ein Mechanismus zum Sammeln von Kundenfeedback zu Produkten. 

Bewertungen werden in Produktlisteseiten, Kategorielistenseiten, Suchergebnisseiten und anderen Standortsseiten angezeigt. 

Rating-Histogramme und Produktbesprechungen werden auf PDPs angezeigt. Eine Schaltfläche **Eine Bewertun schreiben** ermöglicht Kunden, Bewertungen und Prüfungen für ein Produkt senden. Diese PDP-Funktionen werden durch Bewertungen und Rezensionsmodule gesteuert.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Bewertungs- und Prüfungsmodule in PDPs 

Drei Module zeigen die Zusammenfassungen der Beurteilungen und Prüfungen an auf PDPs:
- Modul Bewertung schreiben
- Modul Produktbewertungsliste
- Bewertungshistogrammmodul
 
Die folgende Abbildung zeigt, wie die Bewertungen und Module aussehen auf einer PDP.

![Bewertungs- und Prüfungsmodule in einer PDP.](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Informationen darüber, wie PDP-Vorlagen und -Layouts optimiert werden, sodass Sie die Konfigurationen der Module für Beurteilungen und Prüfungen unter verschiedenen PDPs auf Ihrer E-Commerce-Webseite freigeben können, finden Sie unter. [Vorlagen und Layoutüberblick](templates-layouts-overview.md).

Die folgende Abbildung zeigt, wie das Dialogfeld **Modul hinzufügen** Bewertungs- und Prüfungsmodule in Dynamics 365 Commerce darstellt.
![Fügen Sie ein Moduldialogfeld hinzu.](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Modul Bewertung schreiben

Das Modul Bewertung schreiben enhält eine Schaltfläche **Bewertung schreiben**, bei der sich Benutzer anmelden, eine Bewertung zuweisen und eine Überprüfung eines Produkts schreiben können. Mit diesem Modul können Benutzer eine Bewertung oder Prüfung bearbeiten, die sie zuvor übermittelt haben. Dieses Modul wird in der Regel über den Produktbewertungs-Histogramm- und Produktbewertungslistenmodulen auf einem PDP angezeigt.
Die folgende Abbildung zeigt das Dialogfeld **Eine Bewertung schreiben**, das angezeigt wird, wenn ein Debitor **Eine Bewertung schreiben** auswählt. Der Debitor kann dieses Dialogfeld verwenden, um eine Bewertung und eine Prüfung zu übermitteln.

![Schreiben Sie ein Bewertungsdialogfeld.](media/rnr-eCommerce-write-review-module.png)

In der folgenden Tabelle wird die Eigenschaft für das Modul Bewertung schreiben angezeigt, die im Erstellungstool konfiguriert werden muss.

| Eigenschaftenname | Wert        | Eigenschaftbeschreibung                 |
|---------------|--------------|--------------------------------------|
| Name          | Bewertung schreiben | Der Name des Moduls Bewertung schreiben |

### <a name="ratings-histogram-module"></a>Bewertungshistogrammmodul

Das Bewertungshistogrammmodul zeigt ein Bewertungshistogramm. Dieses Modul wird zwischen dem Modul Bewertung schreiben und dem Produktbewertungslistenmodul auf einem PDP angezeigt.
Das Bewertungshistogrammmodul erfordert keine Konfiguration. Sie müssen das Modul in der PDP-Vorlage nur hinzufügen. Die folgende Abbildung zeigt, wie eine PDP-Vorlage in Dynamics 365 Commerce aussieht, wenn Prüfungs- und Bewertungsmodule zur Anzeige auf PDPs konfiguriert werden.
![PDP-Vorlage, wenn Bewertungen und Prüfungen für die Anzeige auf PDP konfiguriert werden.](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Modul Produktbewertungsliste

Das Produktprüfungs-Listenmodul zeigt eine Liste der Produktprüfungen zusammen mit Sortierung, Filter, und Paginierungsoptionen an. Dieses wird normalerweise nach dem Bewertungshistogrammmodul auf einem PDP angezeigt.
In der folgenden Tabelle wird die Eigenschaft für das Produktbewertungslistenmodul angezeigt, das im Erstellungstool konfiguriert werden muss.

| Eigenschaftenname              | Wert | Eigenschaftbeschreibung |
|----------------------------|-------| ---------------------|
| Auf jeder Seite angezeigte Bewertungen | 10    | Die Anzahl der Bewertungen, die gleichzeitig auf einem PDP angezeigt werden sollen. Schaltflächen **Weiter** und **Vorherige** werden eingeschlossen, damit Benutzer die Seiten der Bewertungen durchsuchen können. |

#### <a name="ratings-histogram--summary-view"></a>Bewertungshistogramm - Zusammenfassungsansicht

Das Produktprüfungs-Listenmodul enthält einen Slot, in dem Sie ein Bewertungshistogrammmodul hinzufügen können. Die folgende Abbildung zeigt, wie Sie ein Bewertungshistogrammmodul im Produktprüfungs-Listenmodul in Dynamics 365 Commerce hinzufügen können.

![Das Hinzufügen eines Bewertungshistogrammmoduls in einem Produktbewertungslistenmodul.](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
