---
title: Buchungsmethoden für Stundung
description: Dieser Artikel beschreibt die Unterschiede zwischen den Abgrenzungsbuchungsmethoden für Einnahmen- und Ausgabenabgrenzungen in der Abonnementabrechnung.
author: JodiChristiansen
ms.date: 6/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c66ed1c38251140dd798c39797873ceb5f7121a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9019096"
---
# <a name="deferral-posting-methods"></a>Buchungsmethoden für Stundung

Dieser Artikel beschreibt die Unterschiede zwischen den Abgrenzungsbuchungsmethoden für Einnahmen- und Ausgabenabgrenzungen in der Abonnementabrechnung.

Auf der Seite **Parameter für Umsatzerlös- und Ausgabenstundung** sind die Optionen für Stundungsbuchungsmethoden **Bilanz** und **Gewinn und Verlust**. Anhand des Beispiels in diesem Artikel werden die Unterschiede zwischen den beiden Methoden und die Gründe erläutert, warum Sie möglicherweise die eine oder andere Methode verwenden.

Die **Bilanz**-Methode verwendet nur zwei Konten. Daher ist weniger Einrichtung erforderlich. Die **Gewinn- und Verlust**-Methode die beiden zusätzlichen Konten **Erste Anerkennung** und **Anerkennung, Gegenkonto** für Umsatzerlös, Rabatte und Kosten, je nach Transaktionstyp. Diese Konten werden auf der **Standardstundungseinstellungen**-Seite (**Abonnementabrechnung \> Umsatzerlös- und Ausgabenstundungen \> Konfiguration**) eingerichtet. Obwohl sich das Beispiel auf aufgeschobene Einnahmen konzentriert, kann das gleiche Konzept auf gestundete Rabatte und gestundete Kosten angewendet werden.

## <a name="example"></a>Beispiel

Verkaufsrechnung 1 hat eine Summe von 3.000 USD und hat einen gestundeten Umsatzerlös. Die folgenden Tabellen zeigen die Verteilungen, wenn diese Verkaufsrechnung gebucht wird.

**Bilanzmethode**

| Typ | Konto | Belastung | Gutschrift|
|---|---|---|---|
| Belastung | Debitorenkonten | 3,000.00 | |
| Gutschrift | Verzögerter Umsatzerlös | | 3,000.00 |

**GuV-Methode**

| Typ | Konto | Belastung | Gutschrift |
|---|---|---|---|
| Belastung | Debitorenkonten | 3,000.00 | |
| Belastung | Umsatzerkennung, Gegenkonto | 3,000.00 | |
| Gutschrift | Verzögerter Umsatzerlös | | 3,000.00 |
| Gutschrift | Anfänglichen Umsatzerkennung | | 3,000.00 |

Verkaufsrechnung 2 hat eine Summe von 2.000 USD und hat keinen gestundeten Umsatzerlös.

| Typ | Konto | Betrag |
|---|---|---|
| Belastung | Debitorenkonten | 3,000.00 |
| Gutschrift | Umsatzerlös | 3,000.00 |

**Summen nach Bilanzmethode für Verkaufsrechnung 1 und 2 kombiniert**

| Konto | Belastung | Gutschrift |
|---|---|---|
| Debitorenkonten | 5,000.00 | |
| Umsatzerlös | | 2,000.00 |
| Verzögerter Umsatzerlös | | 3,000.00 |

Wenn die **Bilanz**-Methode verwendet wird, ist es nicht so einfach, den Bruttoumsatz für einen Zeitraum zu sehen. Ein Teil des Umsatzerlöses wird auf das Konto **Gestundeter Umsatzerlös** gebucht. Beachten Sie, dass es im Konto **Gestundeter Umsatzerlös** mehrere Soll- und Habenbeträge gibt, wenn Umsatzerlös in jeder Periode erkannt wird. Der Bruttoumsatz für eine bestimmten Periode wird mit den Einnahmen/Ausgaben der Umsatzerkennung gemischt.

**Summen nach GuV-Methode für Verkaufsrechnung 1 und 2 kombiniert**

| Konto | Belastung | Gutschrift |
|---|---|---|
| Debitorenkonten | 5,000.00 | |
| Umsatzerlös | | 5,000.00 |
| Umsatzerlös, Gegenkonto | 3,000.00 | |
| Verzögerter Umsatzerlös | | 3,000.00 |

Alle Umsatzerlöse gehen in das **Umsatzerlös**-Konto der Gewinn- und Verlustrechnung. Dann werden die gestundeten Umsatzerlöse aus der Gewinn- und Verlustrechnung in die Bilanz verschoben. Sie können den Bruttoumsatzerlös leicht sehen, da alles auf das Konto **Umsatzerlös** gebucht wird. Ein Teil dieser Bruttoeinnahmen wird jedoch gestundet. Daher wurde er in das Konto **Gestundeter Umsatzerlös** verschoben und später erkannt.

Bei der **Gewinn- und Verlust**-Methode können Sie sich das **Umsatzerlös**-Konto und das **Umsatzerlös, Gegenkonto** ansehen, um die Bruttoeinnahmen von 5.000 USD und den Nettoumsatzerlös (Netto der gestundeten Beträge) von 2.000 USD anzuzeigen. Obwohl die **Gewinn- und Verlust**-Methode die Berichterstellung vereinfachen kann, müssen mehr Konten eingerichtet werden.
