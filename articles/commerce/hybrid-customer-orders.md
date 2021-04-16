---
title: Hybrid-Kundenaufträge
description: Ein hybrider Kundenauftrag ist einen einzelnen Auftrag, der Produkte enthält, die vom Shop des Debitors ausgeführt werden können, sowie Produkte, die verarbeitet werden oder später geliefert.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6357c034059523f83ba05a1da53cae691ef74758
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798936"
---
# <a name="hybrid-customer-orders"></a>Hybrid-Kundenaufträge

[!include [banner](includes/banner.md)]

Ein hybrider Kundenauftrag ist einen einzelnen Auftrag, der Produkte enthält, die vom Shop des Debitors ausgeführt werden können, sowie Produkte, die verarbeitet werden oder später geliefert.

In Commerce können Sie festlegen, entweder alle oder ausgewählte Produkte für einen Kundenauftrag auszuführen. Die Produktgruppen, die z ausführen fakturiert werden automatisch markiert werden, nachdem der Auftrag erstellt wurde, auf ähnliche Weise diese ist identisch für einen Auftrag, die eingeschlossen werden soll, nachdem der Auftrag erstellt wurde. Zahlbarer Betrag auf hybriden Aufträgen wird ermittelt, indem der Einzahlungsprozentsatz auf Entnahme- und Schiffsproduktgruppen mit dem Gesamtbetrag der Durchführungspositionen hinzufügt. Für hybride Aufträge die Systemschalter zwischen Debitorenauftragsmodus und Abholgrosshandelmodus, wie folgt:

- Wenn alle Produkte im Einkaufskorb auf **Lieferung ausführen** festgelegt werden, wird der Auftrag als Cash-and-carry Buchung behandelt.
- Werden irgendwelche oder alle Positionen werden im Einkaufskorb auf entweder **Entnahme** oder **Lieferung versenden** festgelegt, wird der Auftrag als Debitorenauftragsbuchung behandelt.

Wenn eine Einkaufswagenposition ausgewählt und **Auswahl entnehmen**, **Auswahl senden** oder **Auswahl ausliefern** aktiviert ist, nur bestimmte Einkaufswagenposition die mit der Zahlungsbedingung festgelegt wird. In diesem Fall wird der Ablauf des Arbeitsgangs abwärts gerichtete wie gewohnt fort. Wenn **Auswahl entnehmen**, **Auswahl senden** oder **Auswahl ausliefern** aktiviert ist, ohne das eine Einkaufswagenposition aktiviert ist, die ausgewählt wird, wird geöffnet eine neue Seite, die alle Einkaufswagenpositionen aufgelistet werden. Auf diesem Fenster können Sie mehrere Zeilen für das Festlegen der Zahlungsbedingung gleichzeitig auswählen. Bei dieser Methode für die Auswahl von Zeilen verwenden, wird einer vorherigen Übermittlungsmethode, die der Position zugewiesen wurde, überschrieben.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Debitorenaufträge in Modern POS (MPOS)](customer-orders-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]