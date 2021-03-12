---
title: Physischen Wert einbeziehen
description: Verwenden Sie das Kontrollkästchen "Physischen Wert einbeziehen"auf dem Inforegister "Lagermodell" im Formular "Artikelmodellgruppen", um anzugeben, ob physisch aktualisierte Buchungen in der Berechnung des laufenden Durchschnittseinstandspreises für einen Artikel berücksichtigt werden sollen.
author: AndersGirke
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5685fd384e240c1bc6236dbddf678c8d6d9c8c66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005501"
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

**Beispiel 1** Bei aktiviertem Kontrollkästchen **Physischen Wert einbeziehen** gehen die folgenden Bestellungen ein:

-   Eine Bestellung über eine Menge von 2 und einen Einkaufspreis von 10,00 USD, die nach der Aktualisierung des Verpackungspakets aktualisiert wurde.
-   Eine Bestellung über eine Menge von 3 und einen Einkaufspreis von 12,00 USD, die rechnungsaktualisiert wurde.

In diesem Fall beträgt der laufende durchschnittliche Einstandspreis USD 11,20 = (2x10+3x12)/(2+3), da sowohl physisch aktualisierte Transaktionen als auch finanziell aktualisierte Transaktionen zur Berechnung des Einstandspreises verwendet werden. 

**Beispiel 2** Das Kontrollkästchen **Physischen Wert einbeziehen** ist nicht aktiviert, und der Einstandspreis in den Artikeleinstellungen beträgt EUR 10,00. 

-   Sie erhalten eine Bestellung mit einer Menge von 20 zu einem Einstandspreis von EUR 12,00, die auf Grundlage des Lieferscheins aktualisiert wurde.

Bei der Buchung eines Auftrags wird der Einstandspreis mit EUR 10,00 gebucht, da im laufenden Durchschnittseinstandspreis keine physisch gebuchten Posten enthalten sind. 

> [!NOTE]
> Wenn Sie zum Vergleich für diese Position das Kontrollkästchen **Physischen Wert** einbeziehen aktivieren, beträgt der gebuchte Kostenbetrag bei der Buchung eines Kundenauftrags USD 12,00.
