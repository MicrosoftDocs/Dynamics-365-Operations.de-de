---
title: Physischen Wert einbeziehen
description: "Verwenden Sie das Kontrollkästchen \"Physischen Wert einbeziehen\"auf dem Inforegister \"Lagermodell\" im Formular \"Artikelmodellgruppen\", um anzugeben, ob physisch aktualisierte Buchungen in der Berechnung des laufenden Durchschnittseinstandspreises für einen Artikel berücksichtigt werden sollen."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4ea8fe31588dd0768e0651c9e1e332212a00cde2
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="include-physical-value"></a>Physischen Wert einbeziehen

[!include [banner](../includes/banner.md)]

Verwenden Sie das Kontrollkästchen "Physischen Wert einbeziehen"auf dem Inforegister "Lagermodell" im Formular "Artikelmodellgruppen", um anzugeben, ob physisch aktualisierte Buchungen in der Berechnung des laufenden Durchschnittseinstandspreises für einen Artikel berücksichtigt werden sollen.

Das Kontrollkästchen **Physischen Wert einbeziehen** weist die folgenden Werte.

| Wert    | Ergebnis                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Ausgewählt | Sowohl physisch als auch wertmäßig aktualisierte Buchungen werden verwendet, um den laufenden Durchschnittseinstandspreis zu berechnen. |
| Deaktiviert  | Es werden nur wertmäßig aktualisierte Buchungen verwendet, um den laufenden Durchschnittseinstandspreis zu berechnen.                                     |

Die Verwendung des Kontrollkästchens hat je nach genutztem Lagermodell etwas andere Auswirkungen.

-   Wird das Kontrollkästchen **Physischen Wert einbeziehen** bei Verwendung eines Lagermodells vom Typ "FIFO" (First in, first out), "LIFO" (Last in, first out) oder "LIFO-Datum" aktiviert, hat der Lagerabschluss auch Änderungen an physisch aktualisierten Buchungen zur Folge.
-   Wird das Kontrollkästchen **Physischen Wert einbeziehen** bei Verwendung dieser Lagermodelle nicht aktiviert, werden beim Lagerabschluss lediglich Ausgleichsvorgänge für wertmäßig aktualisierte Buchungen vorgenommen.
-   Bei Verwendung des Lagermodells mit gewichtetem Durchschnitt oder Datum für gewichteten Durchschnitt werden beim Lagerabschluss lediglich wertmäßig aktualisierte Buchungen ausgeglichen. Der Status des Kontrollkästchens **Physischen Wert einbeziehen** spielt in diesem Fall keine Rolle.

**Beispiel 1** Bei aktiviertem Kontrollkästchen**Physischen Wert einbeziehen** gehen die folgenden Bestellungen ein:

-   Eine Bestellung mit einer Menge von 2 zu einem Einstandspreis von EUR 10,00, die auf Grundlage des Lieferscheins aktualisiert wurde.
-   Eine Bestellung mit einer Menge von 3 zu einem Einstandspreis von EUR 12,00, die auf Grundlage einer Rechnung aktualisiert wurde.

In diesem Fall beträgt der laufende Durchschnittseinstandspreis EUR 11,20, da für die Einstandspreisberechnung sowohl physisch als auch wertmäßig aktualisierte Buchungen verwendet werden. **Beispiel 2** Das Kontrollkästchen **Physischen Wert einbeziehen** ist nicht aktiviert, und der Einstandspreis in den Artikeleinstellungen beträgt EUR 10,00. Sie erhalten eine Bestellung mit einer Menge von 20 zu einem Einstandspreis von EUR 12,00, die auf Grundlage des Lieferscheins aktualisiert wurde. Bei der Buchung eines Auftrags wird der Einstandspreis mit EUR 10,00 gebucht, da im laufenden Durchschnittseinstandspreis keine physisch gebuchten Posten enthalten sind. **Hinweis:** Wenn Sie zum Vergleich das Kontrollkästchen **Physischen Wert einbeziehen** bei der Auftragsbuchung für diesen Artikel aktivieren, beträgt der gebuchte Einstandspreis EUR 12.00.




