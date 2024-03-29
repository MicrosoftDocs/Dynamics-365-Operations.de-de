---
title: Produkte vom empfangenden Lagerort Filialen zuordnen
description: Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung und Verarbeitung eines Crossdocks zum Vertreiben von Produkten vom empfangenden Lagerplatz einer Bestellung an einen oder viele Shops.
author: Mirzaab
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBuyersPushPerPackage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e65535a1879eab229f185e0e97d81a304fd292d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572960"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a>Produkte vom empfangenden Lagerort Filialen zuordnen

[!include [banner](../../includes/banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung und Verarbeitung eines Crossdocks zum Vertreiben von Produkten vom empfangenden Lagerplatz einer Bestellung an einen oder viele Shops. Der Benutzer kann mehrere Varianten definieren und das System vorschlagen lassen, wie die Produkte vertrieben werden sollen, oder manuell eingeben, wo die Produkte vertrieben werden und wie viel an jeden Shop vertrieben wird. Das Verfahren umfasst nicht die Einrichtung von Daten, die im Crossdock verwendet werden können, wie Auffüllungsregeln, Organisationshierarchien und Shopgewichte. Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.

1. Wechseln Sie zu "Alle Bestellungen".
2. Wählen Sie eine Bestellung in der Liste aus und klicken Sie auf den Link, um den Auftrag zu öffnen.
3. Klicken Sie im Aktivitätsbereich auf „Retail und Commerce“.
4. Klicken Sie auf "Crossdocking".
5. Klicken Sie auf Bearbeiten.
    * Die Kategorie kann verwendet werden, um die Artikel im Abschnitt "Positionen" zu filtern.  
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Geben Sie im Crossdockingmengenfeld einen Wert ein, um anzugeben, wie viel der Menge, die vom ausgewählten Produkt gekauft wird, vertrieben werden soll.
8. Im Feld "Zusätzliche Crossdocking-Menge" geben Sie einen Wert ein, um die Mengen angeben, die für die verfügbaren gekauften Produkte vertrieben werden sollen.
9. Geben Sie im Verteilungs-Feld "Location weight" ein.
    * Sie können die anderen Typen auswählen, um verschiedene Regeln für die Verteilung zu verwenden.  
10. Wählen Sie im Feld "Auffüllungshierarchie" einen Wert aus.
11. Wählen Sie "Ja" im Feld "Sortimente berücksichtigen" aus.
12. Klicken Sie auf "Mengen berechnen".
13. Klicken Sie auf "Auftrag erstellen".
14. Klicken Sie auf "Ja".
15. Wählen Sie in der Liste einen Lagerort aus, der die Produkte empfangen hat.
16. Klicken Sie auf "Auftrag", um die Aufträge anzuzeigen, die für den ausgewählten Lagerort erstellt wurden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]