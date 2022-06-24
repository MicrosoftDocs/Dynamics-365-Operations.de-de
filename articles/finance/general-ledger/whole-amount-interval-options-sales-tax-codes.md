---
title: Optionen zur Berechnung von Gesamtbetrag und Intervall für Mehrwertsteuercodes
description: Dieser Artikel beschreibt die Optionen des Felds "Berechnungsmethoden" für Mehrwertsteuercodes und wie die Mehrwertsteuer für Intervalle und gesamte Beträge berechnet wird.
author: kailiang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b02a0ced8b556cfc5a984d24ceaf982629fd69c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874460"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a>Optionen zur Berechnung von Gesamtbetrag und Intervall für Mehrwertsteuercodes

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Optionen des Felds **Berechnungsmethoden** für Mehrwertsteuercodes und wie die Mehrwertsteuer für Intervalle und gesamte Beträge berechnet wird.

Sie können einen Mehrwertsteuercode so einrichten, dass er basierend auf einen ganzen Betrag oder einen Intervallbetrag berechnet wird. Verwenden Sie auf der Seite **Mehrwertsteuercodes** das Feld **Berechnungsmethode** im Inforegister **Berechnung**, um auszuwählen, nach welcher Methode der Mehrwertsteuercode berechnet werden soll.
- Gesamtbetrag – Der Steuersatz wird auf den gesamten steuerbaren Betrag angewendet.
- Intervall – Der steuerbare Betrag wird aufgeteilt, und jeder Anteil wird in einen Bereich mit einem bestimmten Mehrwertsteuersatz eingeordnet. Der Anteil, der einem bestimmten Intervall angehört, wird gemäß dem Steuersatz für dieses Intervall versteuert. Die Mehrwertsteuer wird aus der Summe der Steuerbeträge gebildet, die für die einzelnen Betragsintervalle berechnet wurden.
  > [!NOTE]                                                                                                                              
  > Die Intervalloption ist nur verfügbar, wenn Sie im Feld "Berechnungsmethode" "Position" im Bereich "Mehrwertsteuer" der Parameterseite "Hauptbuch" auswählen. 

Intervalle werden auf der Seite "Mehrwertsteuer-Codewerte" eingerichtet, indem Sie minimale und maximale Grenzbeträge pro Steuersatz eingeben. Damit Steuern unabhängig von der ausgewählten Berechnungsmethode für alle steuerbaren Beträge berechnet werden, müssen die Intervalle die folgenden Bedingungen erfüllen:
-   Die Untergrenze des ersten Intervalls muss Null sein.
-   Die Obergrenze des letzten Intervalls muss Null sein (unbegrenzt).
-   Die Obergrenze eines beliebigen Intervalls muss kleiner als die Untergrenze des Folgeintervalls sein.

Bildet ein Betrag gleichzeitig die Obergrenze des vorherigen und die Untergrenze des nächsten Intervalls, gilt für den Betrag der Steuersatz des ersten Intervalls. Liegt ein Betrag außerhalb der Intervalle, die mittels Unter- und Obergrenzen definiert wurden, wird der Steuersatz "0" verwendet.

## <a name="example-whole-amount-method-of-calculation"></a>Beispiel: Berechnungsmethode mit Gesamtbetrag
Auf der Seite "Mehrwertsteuer-Codewerte" werden Mehrwertsteuersätze für die folgenden Intervalle eingerichtet:

| Untergrenze     | Höchstgrenze     | Steuersatz     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

Die Mehrwertsteuer wird mit dem gesamten steuerpflichtigen Betrag veranschlagt.

| Steuerpflichtiger Betrag (Preis) | Herstellkostenkalkulation    | Mehrwertsteuer |
|------------------------|----------------|-----------|
| 35,00                  | 35,00 \* 0,30  | 10,50     |
| 50,00                  | 50,00 \* 0,30  | 15:00     |
| 85,00                  | 85,00 \* 0,20  | 17,00     |
| 305,00                 | 305,00 \* 0,10 | 30,50     |

## <a name="example-interval-method-of-calculation"></a>Beispiel: Berechnungsmethode mit Intervall
Auf der Seite "Werte" werden Mehrwertsteuersätze für die folgenden Intervalle eingerichtet:

| Untergrenze     | Höchstgrenze     | Steuersatz     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

Die Mehrwertsteuer wird aus der Summe der Steuerbeträge gebildet, die für die einzelnen Betragsintervalle berechnet wurden.

| Steuerpflichtiger Betrag (Preis) | Herstellkostenkalkulation                                                               | Mehrwertsteuer |
|------------------------|---------------------------------------------------------------------------|-----------|
| 35,00                  | 35,00 \* 0,30                                                             | 10,50     |
| 50,00                  | 50,00 \* 0,30                                                             | 15:00     |
| 85,00                  | (50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)                          | 22,00     |
| 305,00                 | (50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50) | 45.50     |



Weitere Informationen finden Sie unter [Umsatzsätze auf Basis der Marginalbasis und Berechnungsmethoden](marginal-base-field.md).







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
