---
title: Aufzinsungsintervallfunktionalität
description: Dieses Thema enthält Informationen, mit denen Sie zwischen monatlichen, vierteljährlichen, halbjährlichen und jährlichen Zinsintervallen wählen können.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5978abfd4341bbca76ff0211f029097c3d2d785c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971452"
---
# <a name="compounding-interval-functionality"></a>Aufzinsungsintervallfunktionalität

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dieses Thema enthält Informationen, mit denen Sie zwischen monatlichen, vierteljährlichen, halbjährlichen und jährlichen Zinsintervallen wählen können. Die Aufzinsungsintervallfunktion wird verwendet, um die Anzahl der Aufzinsungsperioden pro Jahr im Zahlungsplan eines Mietvertrags zu bestimmen. Jedes der vier Beispiele in diesem Thema zeigt, wie der Zahlungsplan eines Mietvertrags für ein anderes Intervall aussehen wird.

Sie können kein Aufzinsungsintervall auswählen, das weniger häufig ist als die Zahlungshäufigkeit des Mietvertrags. Beispielsweise kann ein vierteljährliches Zinsintervall nicht mit einer monatlichen Zahlungshäufigkeit verwendet werden, und ein jährliches Zinsintervall kann nicht mit einer halbjährlichen Zahlungshäufigkeit verwendet werden. Wenn Sie versuchen, ein Aufzinsungsintervall auszuwählen, dass weniger häufig ist als die Zahlungshäufigkeit des Mietvertrags, erhalten Sie einen Fehler.

> [!NOTE]
> In allen vier Beispielen in diesem Thema entspricht das Aufzinsungsintervall der Zahlungshäufigkeit.

## <a name="examples"></a>Beispiele

### <a name="setup-for-all-four-leases"></a>Einrichtung für alle vier Mietverträge

Die folgenden Tabellen zeigen die Werte, die auf den Registerkarten **Allgemeines** und **Zahlungspläne** für die vier Mietverträge festgelegt sind, die in den Beispielen verwendet werden.

**Registerkarte „Allgemeines“**

| Feld                      | Wert                        |
|----------------------------|------------------------------|
| Zinssatz für Neukredit | **5 %**                       |
| Annuitätstyp               | **Normale Annuität**         |
| Aufzinsungsintervall       | Siehe die einzelnen Beispiele. |
| Zahlungshäufigkeit          | **Monatlich**                  |
| Anfangsdatum          | **01.01.2020**                 |

**Registerkarte „Zahlungsplanpositionen“**

| Feld             | Wert                        |
|-------------------|------------------------------|
| Startdatum        | **01.01.2020**                 |
| Perioden           | **120**                      |
| Periodenintervall   | **Monate**                   |
| Enddatum          | **31.12.2029**               |
| Zahlungshäufigkeit | Siehe die einzelnen Beispiele. |
| Zahlungsbetrag    | **50,000**                   |

### <a name="lease-1-monthly-compounding-interval-and-monthly-payment-frequency"></a>Mietvertrag 1: Monatliches Aufzinsungsintervall und monatliche Zahlungshäufigkeit

In der folgenden Tabelle sind die ersten 12 Monate des Zahlungsplans aufgeführt. Beachten Sie jedoch die folgenden Details:

- Der Wert in der Spalte „Zeitraum“ erhöht sich jeden Monat um 1, da jeder Monat ein neues Zinsintervall ist.
- In der Formel in der Spalte „Aktueller Wert“ wird der Satz durch 12 geteilt, da es 12 Zinsperioden pro Jahr gibt. Der Exponent (d.h. die hochgestellte Ziffer) entspricht dem Wert in der Spalte „Zeitraum“.

| Periode | Monat | Datum       | Zahlungsbetrag | Barwert                                       |
|--------|-------|------------|----------------|-----------------------------------------------------|
| 1      | 1     | 31.01.2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>1</sup> = 49.792,53  |
| 2      | 2     | 29.02.2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>2</sup> = 49.585,92  |
| 3      | 3     | 31.03.2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>3</sup> = 49.380,17  |
| 4      | 4     | 30.04.2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>4</sup> = 49.175,28  |
| 5      | 5     | 31.05.2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>5</sup> = 48.971,23  |
| 6      | 6     | 30.06.2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>6</sup> = 48.768,03  |
| 7      | 7     | 31.07.2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>7</sup> = 48.565,67  |
| 8      | 8     | 31.08.2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>8</sup> = 48.364,15  |
| 9      | 9     | 30.09.2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>9</sup> = 48.163,47  |
| 10     | 10    | 31.10.2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>10</sup> = 47.963,62 |
| 11     | 11    | 30.11.2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>11</sup> = 47.764,61 |
| 12     | 12    | 31/12/2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 12\])<sup>12</sup> = 47.566,41 |

### <a name="lease-2-quarterly-compounding-interval-and-quarterly-payment-frequency"></a>Mietvertrag 2: Vierteljährliches Aufzinsungsintervall und vierteljährliche Zahlungshäufigkeit

In der folgenden Tabelle sind die ersten 12 Monate des Zahlungsplans aufgeführt. Beachten Sie jedoch die folgenden Details:

- Der Wert in der Spalte „Zeitraum“ erhöht sich alle drei Monate (also jedes Quartal) um 1, da jedes Quartal ein neues Zinsintervall ist.
- In der Formel in der Spalte „Aktueller Wert“ wird der Satz durch 4 geteilt, da es vier Zinsperioden pro Jahr gibt. Der Exponent entspricht dem Wert in der Spalte „Zeitraum“.

| Periode | Monat | Datum       | Zahlungsbetrag | Barwert                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.01.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>1</sup> = 0           |
| 1      | 2     | 29.02.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>1</sup> = 0           |
| 1      | 3     | 31.03.2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 4\])<sup>1</sup> = 49.382,72 |
| 2      | 4     | 30.04.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>2</sup> = 0           |
| 2      | 5     | 31.05.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>2</sup> = 0           |
| 2      | 6     | 30.06.2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 4\])<sup>2</sup> = 48.773,05 |
| 3      | 7     | 31.07.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>3</sup> = 0           |
| 3      | 8     | 31.08.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>3</sup> = 0           |
| 3      | 9     | 30.09.2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 4\])<sup>3</sup> = 48.170,92 |
| 4      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>4</sup> = 0           |
| 4      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>4</sup> = 0           |
| 4      | 12    | 31/12/2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 4\])<sup>4</sup> = 47.576,21 |

> [!NOTE]
> Wenn der Annuitätentyp in **Annuität fällig** geändert wird, erfolgt die Zahlung zu Beginn des Quartals statt zum Ende des Quartals.

### <a name="lease-3-semiannual-compounding-interval-and-semiannual-payment-frequency"></a>Mietvertrag 3: Halbjährliches Aufzinsungsintervall und halbjährliche Zahlungshäufigkeit

In der folgenden Tabelle sind die ersten 12 Monate des Zahlungsplans aufgeführt. Beachten Sie jedoch die folgenden Details:

- Der Wert in der Spalte „Zeitraum“ erhöht sich alle sechs Monate (also halbjährlich) um 1, da jedes halbe Jahr ein neues Zinsintervall ist.
- In der Formel in der Spalte „Aktueller Wert“ wird der Satz durch 2 geteilt, da es zwei Zinsperioden pro Jahr gibt. Der Exponent entspricht dem Wert in der Spalte „Zeitraum“.

| Periode | Monat | Datum       | Zahlungsbetrag | Barwert                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.01.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 2     | 29.02.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 3     | 31.03.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 4     | 30.04.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 5     | 31.05.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 6     | 30.06.2020  | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 48.780,49 |
| 2      | 7     | 31.07.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 8     | 31.08.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 9     | 30.09.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 12    | 31/12/2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 47.590,72 |

> [!NOTE]
> Wenn der Annuitätentyp in **Annuität fällig** geändert wird, erfolgt die Zahlung im Januar und Juli anstelle von Juni und Dezember.

### <a name="lease-4-annual-compounding-interval-and-annual-payment-frequency"></a>Mietvertrag 4: Jährliches Aufzinsungsintervall und jährliche Zahlungshäufigkeit

In der folgenden Tabelle sind die ersten 12 Monate des Zahlungsplans aufgeführt. Beachten Sie jedoch die folgenden Details:

- Der Wert in der Spalte „Zeitraum“ erhöht sich alle 12 Monate (also jährlich) um 1, da jedes Jahr ein neues Zinsintervall ist.
- In der Formel in der Spalte „Aktueller Wert“ wird der Satz durch 1 geteilt, da es eine Zinsperiode pro Jahr gibt. Der Exponent entspricht dem Wert in der Spalte „Zeitraum“.

| Periode | Monat | Datum       | Zahlungsbetrag | Barwert                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.01.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 2     | 29.02.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 3     | 31.03.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 4     | 30.04.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 5     | 31.05.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 6     | 30.06.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 7     | 31.07.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 8     | 31.08.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 9     | 30.09.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 12    | 31/12/2020 | 50,000.00      | 50.000 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 47.619,05 |

> [!NOTE]
> Wenn der Annuitätentyp in **Annuität fällig** geändert wird, erfolgt die Zahlung im Januar anstelle von Dezember.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]