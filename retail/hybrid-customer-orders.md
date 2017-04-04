---
title: Hybrid customer orders
description: "Ein hybrider Kundenauftrag ist einen einzelnen Auftrag, der Produkte enthält, die vom Shop des Debitors ausgeführt werden können, sowie Produkte, die verarbeitet werden oder später geliefert."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>Hybrid customer orders

Ein hybrider Kundenauftrag ist einen einzelnen Auftrag, der Produkte enthält, die vom Shop des Debitors ausgeführt werden können, sowie Produkte, die verarbeitet werden oder später geliefert.

In Microsoft Dynamics 365 - Arbeitsgänge für Einzelhandel, können Sie festlegen werden entweder alle oder ausgewählte Produkte ausführen für einen Kundenauftrag. Die Produktgruppen, die z ausführen fakturiert werden automatisch markiert werden, nachdem der Auftrag erstellt wurde, auf ähnliche Weise diese ist identisch für einen Auftrag, die eingeschlossen werden soll, nachdem der Auftrag erstellt wurde. Zahlbarer Betrag auf hybriden Aufträgen wird ermittelt, indem der Einzahlungsprozentsatz auf Entnahme- und Schiffsproduktgruppen mit dem Gesamtbetrag der Durchführungspositionen hinzufügt. Für hybride Aufträge die Systemschalter zwischen Debitorenauftragsmodus und Abholgrosshandelmodus, wie folgt:

-   Wenn alle Produkte im Einkaufskorb auf festgelegt werden ** Ausführen Lieferung durch **, wird der Auftrag als Cash-and-carry Buchung behandelt.
-   Werden irgendwelche oder alle Positionen werden im Einkaufskorb auf entweder ** Entnahme oder festgelegt ** ** Schiffslieferung **, wird der Auftrag als Debitorenauftragsbuchung behandelt.

Wenn eine Einkaufswagenposition und aktiviert ** die Übertragung ausgewählt **, ** Versand- wählte aus ** oder ** Carry Kassenlayout aktiviert ** ist aktiviert, nur bestimmte Einkaufswagenposition die mit der Zahlungsbedingung festgelegt wird. In diesem Fall wird der Ablauf des Arbeitsgangs abwärts gerichtete wie gewohnt fort. Wenn ** Entnahme wählte aus ** ** Versand- wählte aus, oder Carry ** ** Kassenlayout aktiviert ** ohne eine Einkaufswagenposition aktiviert, die ausgewählt wird, wird geöffnet eine neue Seite, die alle Einkaufswagenpositionen aufgelistet werden. Auf diesem Fenster können Sie mehrere Zeilen für das Festlegen der Zahlungsbedingung gleichzeitig auswählen. Bei dieser Methode für die Auswahl von Zeilen verwenden, wird einer vorherigen Übermittlungsmethode, die der Position zugewiesen wurde, überschrieben.

<a name="see-also"></a>Siehe auch
--------

Debitorenauftragsüberblick []( customer-orders-overview.md)


