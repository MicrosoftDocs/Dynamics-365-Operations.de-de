---
title: Lieferzeitpläne
description: Lieferzeitpläne ermöglichen Ihnen, Auftragspositionsmengen zu verfolgen, wenn Sie mehrere Lieferungen für einen einzelnen Auftrag, ein Verkaufsangebot oder eine Bestellung verwenden.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dbd66d499b5d5f9f8ef21c0ce3752031a5f4672
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193781"
---
# <a name="delivery-schedules"></a>Lieferzeitpläne

[!include [banner](../includes/banner.md)]

Lieferzeitpläne ermöglichen Ihnen, Auftragspositionsmengen zu verfolgen, wenn Sie mehrere Lieferungen für einen einzelnen Auftrag, ein Verkaufsangebot oder eine Bestellung verwenden.

Ein Lieferzeitplan wird verwendet, wenn eine Gesamtmenge für einen Auftrag oder ein Angebot angefordert wird, um in mehreren Lieferungen geliefert zu werden. Einzelne Sendungen werden von Lieferpositionen angezeigt. Zwei oder mehr Lieferpositionen bilden einen Lieferzeitplan. Die Lieferpositionen können verschiedene Lieferdaten, Mengen, Lieferarten und Lagerdimensionen haben, wie Standort und Lagerort.  

**Beispiel zum Löschen eines gesamten Lieferzeitplans**

| Artikel                              | Wert                                    |
|-----------------------------------|------------------------------------------|
| Gesamte Bestellung (ursprüngliche Auftragsposition) | 600 Stühle                               |
| Angeforderter Lieferzeitplan       | 100 Stühle pro Monat                     |
| Angeforderter Lieferzeitrahmen | 6 Monate, jeweils am 1 Tag jedes Monats |

In diesem Szenario fordert der Debitor die Lieferung von 600 Stühlen in Chargen von 100 Stühlen über einen Zeitraum von sechs Monaten hinweg. Um die Lieferungsanforderungen zu verfolgen, erstellen Sie einen Lieferzeitplan. Erstellen Sie auf der Lieferzeitplan-Seite sechs separate Lieferpositionen. Jede Lieferposition umfasst 100 Stühle und gibt das Lieferdatum für die jeweiligen 100 Stühle an. In diesem Fall wird die erste Position sechs Monate hintereinander jeweils für den 1. des Monats versetzt.  

Wenn Sie den Lieferzeitplan erstellt haben, wird der Typ der ursprünglichen Auftragsposition automatisch auf **Auftragsposition mit mehreren Lieferungen** geändert. Eine Position dieses Typs verweist auf eine geschäftsbezogene Position und wird durch ein Symbol gekennzeichnet. Die Lieferposition wird durch ein anderes Symbol gekennzeichnet. Wenn Sie eine Menge in einer Lieferposition ändern, wird die Position in der Gesamtmenge des Lieferzeitplans aktualisiert. Falls eine Handelsvereinbarung mit einem definierten Gesamtauftragsrabatt besteht, wird mithilfe des Lieferzeitplans außerdem sichergestellt, dass der Gesamtauftragsrabatt auch dann für den Auftrag gilt, wenn dieser in einzelne Lieferungen unterteilt ist.  

Aufträge, die einen Lieferzeitplan haben, werden mit den Lieferpositionen verarbeitet. Die Verarbeitung umfasst die Buchung von Lieferscheinen, Produktzugängen und die Rechnungsstellung.  

Dokumentausdrucke von Aufträgen und Angeboten mit Lieferzeitplan zeigen nur die Lieferpositionen an. Sie zeigen nicht die ursprünglichen Positionen an (geschäftsbezogene Positionen). **Hinweis:** Außerdem werden die Lieferpositionen angezeigt, wenn Sie diese Aktivitäten ausführen:

-   Buchen
-   Seiten kopieren
-   Durchsuchen von Listenseiten und Berichten

Beim Bestätigen eines Verkaufsangebots zeigt der Auftrag den gesamte Lieferzeitplan Auftragsposition an – auch dann, wenn Auftragspositionen mehrere Lieferungen haben. Außerdem wird der gesamte Lieferzeitplan in allen Haupseiten angezeigt, z. B. Aufträgen, Verkaufsangeboten und Bestellungen.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]