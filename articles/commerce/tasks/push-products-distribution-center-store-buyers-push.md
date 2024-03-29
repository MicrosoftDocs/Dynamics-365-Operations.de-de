---
title: Produkte vom Verteilzentrum zu Shops mithilfe von Käuferübertragung übertragen
description: Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung und Verarbeitung einer Käuferübertragung zum Vertreiben von Produkten von einem Lagerplatz an einen oder viele Shops.
author: BrianShook
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 30d82e4b282bac2ea888971ad5c6298adfa8332b
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779619"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a>Produkte vom Verteilzentrum zu Shops mithilfe von Käuferübertragung übertragen

[!include [banner](../includes/banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung und Verarbeitung einer Käuferübertragung zum Vertreiben von Produkten von einem Lagerplatz an einen oder viele Shops. Der Benutzer kann mehrere Varianten definieren und das System vorschlagen lassen, wie die Produkte vertrieben werden sollen, oder manuell eingeben, wo die Produkte vertrieben werden und wie viel an jeden Shop vertrieben wird. Das Verfahren umfasst nicht die Einrichtung von Daten, die in der Käuferübertragung verwendet werden können, wie Auffüllungsregeln, Organisationshierarchien und Shopgewichte. Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.

1. Gehen Sie zu "Käuferübertragung".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Beschreibung" einen Wert ein.
4. Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.
5. Wählen Sie im Feld "Lagerort" einen Lagerort aus (bzw. geben Sie einen ein), der Produkte mit Lagerbestandsmengen hat.
6. Klicken Sie auf Hinzufügen.
7. Markieren Sie in der Liste die ausgewählte Zeile.
8. Geben Sie im Feld "Artikelnummer" ein Produkt ein oder wählen Sie ein Produkt aus.
9. Klicken Sie auf Hinzufügen.
10. Markieren Sie in der Liste die ausgewählte Zeile.
11. Geben Sie im Feld "Artikelnummer" eine Produktvariante ein oder wählen Sie eine Produktvariante aus.
    * Wenn Sie eine Produktvariante eingeben, werden Positionen für jede Variante erstellt.  
12. Markieren Sie in der Liste eine Zeile.
13. Im Feld "Übertragene Menge" geben Sie ein, wieviel des ausgewählten Produkts Sie verteilen möchten.
14. Im Feld "Zusätzliche zu übertragende Menge" geben Sie die Menge der Produkte ein, die eine verfügbare zu verteilende Menge haben.
15. Geben Sie im Verteilungs-Feld "Location weight" ein.
    * Sie können die anderen Typen auswählen, um andere Regeln für die Verteilung zu verwenden.  
16. Wählen Sie im Feld "Auffüllungshierarchie" einen Wert aus.
17. Wählen Sie "Ja" im Feld "Sortimente berücksichtigen" aus.
18. Klicken Sie auf "Mengen berechnen" und überprüfen Sie die Mengen, die zu den Zeilen im Lagerortabschnitt hinzugefügt werden.
19. Klicken Sie auf "Auftrag erstellen".
20. Klicken Sie auf "Ja".



[!INCLUDE[footer-include](../../includes/footer-banner.md)]