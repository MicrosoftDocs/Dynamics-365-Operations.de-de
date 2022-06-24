---
title: Steuerberechnung und Rundung
description: Dieser Artikel bietet einen Überblick über die Mehrwertsteuerberechnung und Rundung und erläutert die zugehörigen Einrichtungsparameter.
author: wangchen
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2022-05-31
ms.dyn365.ops.version: AX 10.0.28
ms.openlocfilehash: aa3564f0fcf4a958637ba4a5cdcc497bffc50000
ms.sourcegitcommit: 8b716849707ec96d1cb4cac85b9e782dc25f5a70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/07/2022
ms.locfileid: "8939232"
---
# <a name="sales-tax-calculation-and-rounding"></a>Steuerberechnung und Rundung

[!include [banner](../includes/banner.md)]

Dieser Artikel gibt einen Überblick über die Berechnung und Rundung der Mehrwertsteuer in Microsoft Dynamics 365 Finance. Außerdem werden die Parameter erläutert, die im Setup für die Berechnung und Rundung der Mehrwertsteuer verwendet werden, und wie diese Parameter zusammenarbeiten.

## <a name="parameters"></a>Parameter

Mehrere Parameter steuern die Berechnung und Rundung der Mehrwertsteuer:

- **Berechnungsmethode** – Dieser Parameter wird auf der Seite **Hauptbuchparameter** eingestellt und legt fest, ob die Bemessungsgrundlage pro Beleg oder pro Position berechnet wird. Wenn der Parameter **Berechnungsgrundlage** für den Mehrwertsteuercode auf **Nettobetrag des Rechnungssaldos** gesetzt ist, wird der Steuerbasisbetrag immer pro Beleg berechnet, unabhängig von der Einstellung dieses Parameters.
- **Rundung nach** – Dieser Parameter wird für die Mehrwertsteuercode gesetzt und definiert, ob der Steuerbetrag pro Mehrwertsteuerkennzeichen oder pro Mehrwertsteuercode-Kombination gerundet wird.
- **Herkunft** – Dieser Parameter wird für den Mehrwertsteuercode gesetzt und definiert, wie der Steuerbetrag berechnet wird. Weitere Informationen finden Sie unter [Mehrwertsteuer-Berechnungsmethoden im Feld „Ursprung“](sales-tax-calculation-methods-origin-field.md).
- **Berechnungsgrundlage** – Dieser Parameter wird für den Mehrwertsteuercode gesetzt und bestimmt, welcher Betrag zur Auswahl der entsprechenden Steuersätze auf der Seite **Mehrwertsteuer-Codewerte** verwendet wird. Weitere Informationen finden Sie unter [Umsatzsätze auf Basis der Marginalbasis und Berechnungsmethoden](marginal-base-field.md).
- **Rundungsregel für Mehrwertsteuer** – Dieser Parameter wird für den Mehrwertsteuercode gesetzt und definiert, wie der ermittelte Mehrwertsteuerbetrag gerundet wird, einschließlich der Rundungsgenauigkeit und der Rundungsmethode.

Der Rest dieses Artikels enthält einige typische Beispiele für die Berechnung und Rundung der Mehrwertsteuer, die eine Kombination der vorstehenden Parameter verwenden.

## <a name="scenario-for-the-examples"></a>Szenario für die Beispiele

- Der steuerpflichtige Beleg enthält zwei Positionen, und der Steuerbasisbetrag für jede Position beträgt 42,42.
- Für jede Position sind zwei Mehrwertsteuercodes definiert: Mehrwertsteuercode 1 und Mehrwertsteuercode 2.
- Der Steuersatz von Steuercode 1 und Steuercode 2 beträgt jeweils 10 Prozent.
- Der Preis enthält keine Steuer.
- Die Rundungsgenauigkeit ist auf 0,01 festgelegt.
- Die Rundungsmethode ist festgelegt auf **Aufrunden**.

## <a name="example-1"></a>Beispiel 1

### <a name="parameter-values"></a>Parameterwerte

| Berechnungsmethode | Rundung nach    | Herkunft                   | Berechnungsgrundlage       |
| ------------------ | -------------- | ------------------------ | ------------------- |
| Position               | Mehrwertsteuercode | Prozentanteil am Nettobetrag | Nettobetrag pro Position |

### <a name="calculation-and-rounding-behavior"></a>Berechnung und Rundungsverhalten

| Positionsnummer | Mehrwertsteuercode | Betragsursprung | Mehrwertsteuerbetrag |
| ------------| ---------------| --------------| -----------------|
| 1           | Code 1         | 42.42         | 4.25             |
| 1           | Code 2         | 42.42         | 4.25             |
| 2           | Code 1         | 42.42         | 4.25             |
| 2           | Code 2         | 42.42         | 4.25             |

Der Steuerbasisbetrag wird pro Position berechnet:

- **Position 1:** 42,42
- **Position 2:** 42,42

Der Steuerbetrag wird pro Mehrwertsteuercode berechnet:

- **Position 1:**

    - Steuerbetrag für Mehrwertsteuercode 1 = 42,42 &times; 10 Prozent = 4,242
    - Steuerbetrag für Mehrwertsteuercode 2 = 42,42 &times; 10 Prozent = 4,242

- **Position 2:**

    - Steuerbetrag für Mehrwertsteuercode 1 = 42,42 &times; 10 Prozent = 4,242
    - Steuerbetrag für Mehrwertsteuercode 2 = 42,42 &times; 10 Prozent = 4,242

Der Steuerbetrag wird pro Mehrwertsteuercode gerundet:

- **Position 1:**

    - Gerundeter Steuerbetrag für Mehrwertsteuercode 1 = 4,25
    - Gerundeter Steuerbetrag für Mehrwertsteuercode 2 = 4,25

- **Position 2:**

    - Gerundeter Steuerbetrag für Mehrwertsteuercode 1 = 4,25
    - Gerundeter Steuerbetrag für Mehrwertsteuercode 2 = 4,25

## <a name="example-2"></a>Beispiel 2

### <a name="parameter-values"></a>Parameterwerte

| Berechnungsmethode | Rundung nach    | Herkunft                   | Berechnungsgrundlage                 |
| ------------------ | -------------- | ------------------------ | ----------------------------- |
| Position/Gesamt         | Mehrwertsteuercode | Prozentanteil am Nettobetrag | Nettobetrag des Rechnungssaldos |

### <a name="calculation-and-rounding-behavior"></a>Berechnung und Rundungsverhalten

| Positionsnummer | Mehrwertsteuercode | Betragsursprung | Mehrwertsteuerbetrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.25             |
| 1           | Code 2         | 42.42         | 4.25             |
| 2           | Code 1         | 42.42         | 4.24             |
| 2           | Code 2         | 42.42         | 4.24             |

Der Steuerbasisbetrag wird pro Beleg berechnet:

- Steuergrundbetrag = 42,42 + 42,42 = 84,84

Der Steuerbetrag wird pro Mehrwertsteuercode berechnet:

- Steuerbetrag für Mehrwertsteuercode 1 = 84,84 &times; 10 Prozent = 8,484
- Steuerbetrag für Mehrwertsteuercode 2 = 84,84 &times; 10 Prozent = 8,484

Der Steuerbetrag wird pro Mehrwertsteuercode gerundet:

- Gerundeter Steuerbetrag für Mehrwertsteuercode 1 = 8,49
- Gerundeter Steuerbetrag für Mehrwertsteuercode 2 = 8,49

Der gerundete Steuerbetrag wird jeder Position nach Mehrwertsteuercode zugeordnet:

- Ordnen Sie den gerundeten Steuerbetrag für Mehrwertsteuercode 1 (8,49) der Position 1 (4,25) und der Position 2 (4,24) zu.
- Ordnen Sie den gerundeten Steuerbetrag für Mehrwertsteuercode 2 (8,49) der Position 1 (4,25) und der Position 2 (4,24) zu.

## <a name="example-3"></a>Beispiel 3

### <a name="parameter-values"></a>Parameterwerte

| Berechnungsmethode | Rundung nach    | Herkunft                              | Berechnungsgrundlage       |
| ------------------ | -------------- | ----------------------------------- | ------------------- |
| Position               | Mehrwertsteuercode | Berechneter Prozentanteil am Nettobetrag | Nettobetrag pro Position |

### <a name="calculation-and-rounding-behavior"></a>Berechnung und Rundungsverhalten

| Positionsnummer | Mehrwertsteuercode | Betragsursprung | Mehrwertsteuerbetrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.72             |
| 1           | Code 2         | 42.42         | 4.72             |
| 2           | Code 1         | 42.42         | 4.72             |
| 2           | Code 2         | 42.42         | 4.72             |

Der Steuerbasisbetrag wird pro Position berechnet:

- **Position 1:** 42,42
- **Position 2:** 42,42

Der Steuerbetrag wird pro Mehrwertsteuercode berechnet:

- **Position 1:**

    - Steuerbetrag für Mehrwertsteuercode 1 = 42,42 &times; 10 Prozent &divide; (1 – 10 Prozent) = 4,7133
    - Steuerbetrag für Mehrwertsteuercode 2 = 42,42 &times; 10 Prozent &divide; (1 – 10 Prozent) = 4,7133

- **Position 2:**

    - Steuerbetrag für Mehrwertsteuercode 1 = 42,42 &times; 10 Prozent &divide; (1 – 10 Prozent) = 4,7133
    - Steuerbetrag für Mehrwertsteuercode 2 = 42,42 &times; 10 Prozent &divide; (1 – 10 Prozent) = 4,7133

Der Steuerbetrag wird pro Mehrwertsteuercode gerundet:

- **Position 1:**

    - Gerundeter Steuerbetrag für Mehrwertsteuercode 1 = 4,72
    - Gerundeter Steuerbetrag für Mehrwertsteuercode 2 = 4,72

- **Position 2:**

    - Gerundeter Steuerbetrag für Mehrwertsteuercode 1 = 4,72
    - Gerundeter Steuerbetrag für Mehrwertsteuercode 2 = 4,72

## <a name="example-4"></a>Beispiel 4

### <a name="parameter-values"></a>Parameterwerte

| Berechnungsmethode | Rundung nach    | Herkunft                              | Berechnungsgrundlage                 |
| ------------------ | -------------- | ----------------------------------- | ----------------------------- |
| Position/Gesamt         | Mehrwertsteuercode | Berechneter Prozentanteil am Nettobetrag | Nettobetrag des Rechnungssaldos |

### <a name="calculation-and-rounding-behavior"></a>Berechnung und Rundungsverhalten

| Positionsnummer | Mehrwertsteuercode | Betragsursprung | Mehrwertsteuerbetrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.72             |
| 1           | Code 2         | 42.42         | 4.72             |
| 2           | Code 1         | 42.42         | 4.71             |
| 2           | Code 2         | 42.42         | 4.71             |

Der Steuerbasisbetrag wird pro Beleg berechnet:

- Steuergrundbetrag = 42,42 + 42,42 = 84,84

Der Steuerbetrag wird pro Mehrwertsteuercode berechnet:

- Steuerbetrag für Mehrwertsteuercode 1 = 84,84 &times; 10 Prozent &divide; (1 – 10 Prozent) = 9,4267
- Steuerbetrag für Mehrwertsteuercode 2 = 84,84 &times; 10 Prozent &divide; (1 – 10 Prozent) = 9,4267

Der Steuerbetrag wird pro Mehrwertsteuercode gerundet:

- Gerundeter Steuerbetrag für Mehrwertsteuercode 1 = 9,43
- Gerundeter Steuerbetrag für Mehrwertsteuercode 2 = 9,43

Der gerundete Steuerbetrag wird jeder Position nach Mehrwertsteuercode zugeordnet:

- Ordnen Sie den Steuerbetrag für Mehrwertsteuercode 1 (9,43) der Position 1 (4,72) und der Position 2 (4,71) zu.
- Ordnen Sie den Steuerbetrag für Mehrwertsteuercode 2 (9,43) der Position 1 (4,72) und der Position 2 (4,71) zu.

## <a name="example-5"></a>Beispiel 5

### <a name="parameter-values"></a>Parameterwerte

| Berechnungsmethode | Rundung nach                | Herkunft                   | Berechnungsgrundlage       |
| ------------------ | -------------------------- | ------------------------ | ------------------- |
| Position               | Mehrwertsteuer-Codekombination | Prozentanteil am Nettobetrag | Nettobetrag pro Position |

### <a name="calculation-and-rounding-behavior"></a>Berechnung und Rundungsverhalten

| Positionsnummer | Mehrwertsteuercode | Betragsursprung | Mehrwertsteuerbetrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.25             |
| 1           | Code 2         | 42.42         | 4.24             |
| 2           | Code 1         | 42.42         | 4.24             |
| 2           | Code 2         | 42.42         | 4.24             |

Der Steuerbasisbetrag wird pro Position berechnet:

- **Position 1:** 42,42
- **Position 2:** 42,42

Der Steuerbetrag wird pro Mehrwertsteuercode berechnet:

- **Position 1:**

    - Steuerbetrag für Mehrwertsteuercode 1 = 42,42 &times; 10 Prozent = 4,242
    - Steuerbetrag für Mehrwertsteuercode 2 = 42,42 &times; 10 Prozent = 4,242

- **Position 2:**

    - Steuerbetrag für Mehrwertsteuercode 1 = 42,42 &times; 10 Prozent = 4,242
    - Steuerbetrag für Mehrwertsteuercode 2 = 42,42 &times; 10 Prozent = 4,242

Der Steuerbetrag wird pro Mehrwertsteuercode-Kombination gerundet:

- Gesamt-Mehrwertsteuerbetrag = 4,242 + 4,242 + 4,242 + 4,242 = 16,968, was auf 16,97 aufgerundet wird

Der gerundete Steuerbetrag wird jeder Position nach Mehrwertsteuercode zugeordnet:

- Ordnen Sie den Mehrwertsteuerbetrag (16,97) Position 1 und Position 2 zu:

    - **Position 1:**

        - Steuerbetrag für Mehrwertsteuercode 1 = 4,25
        - Steuerbetrag für Mehrwertsteuercode 2 = 4,24

    - **Position 2:**

        - Steuerbetrag für Mehrwertsteuercode 1 = 4,24
        - Steuerbetrag für Mehrwertsteuercode 2 = 4,24

## <a name="example-6"></a>Beispiel 6

### <a name="parameter-values"></a>Parameterwerte

| Berechnungsmethode | Rundung nach                | Herkunft                   | Berechnungsgrundlage                 |
| ------------------ | -------------------------- | ------------------------ | ----------------------------- |
| Position/Gesamt         | Mehrwertsteuer-Codekombination | Prozentanteil am Nettobetrag | Nettobetrag des Rechnungssaldos |

### <a name="calculation-and-rounding-behavior"></a>Berechnung und Rundungsverhalten

| Positionsnummer | Mehrwertsteuercode | Betragsursprung | Mehrwertsteuerbetrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.25             |
| 1           | Code 2         | 42.42         | 4.24             |
| 2           | Code 1         | 42.42         | 4.24             |
| 2           | Code 2         | 42.42         | 4.24             |

Der Steuerbasisbetrag wird pro Beleg berechnet:

- Steuergrundbetrag = 42,42 + 42,42 = 84,84

Der Steuerbetrag wird pro Mehrwertsteuercode berechnet:

- Steuerbetrag für Mehrwertsteuercode 1 = 84,84 &times; 10 Prozent = 8,484
- Steuerbetrag für Mehrwertsteuercode 2 = 84,84 &times; 10 Prozent = 8,484

Der Steuerbetrag wird pro Mehrwertsteuercode-Kombination gerundet:

- Gesamt-Mehrwertsteuerbetrag = 8,484 +8,484 = 16,968, was auf 16,97 aufgerundet wird

Der gerundete Steuerbetrag wird jeder Position nach Mehrwertsteuercode zugeordnet:

- Ordnen Sie den Mehrwertsteuerbetrag (16,97) Position 1 und Position 2 zu:

    - **Position 1:**

        - Steuerbetrag für Mehrwertsteuercode 1 = 4,25
        - Steuerbetrag für Mehrwertsteuercode 2 = 4,24

    - **Position 2:**

        - Steuerbetrag für Mehrwertsteuercode 1 = 4,24
        - Steuerbetrag für Mehrwertsteuercode 2 = 4,24

## <a name="example-7"></a>Beispiel 7

### <a name="parameter-values"></a>Parameterwerte

| Berechnungsmethode | Rundung nach                | Herkunft                              | Berechnungsgrundlage       |
| ------------------ | -------------------------- | ----------------------------------- | ------------------- |
| Position               | Mehrwertsteuer-Codekombination | Berechneter Prozentanteil am Nettobetrag | Nettobetrag pro Position |

### <a name="calculation-and-rounding-behavior"></a>Berechnung und Rundungsverhalten

| Positionsnummer | Mehrwertsteuercode | Betragsursprung | Mehrwertsteuerbetrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.72             |
| 1           | Code 2         | 42.42         | 4.71             |
| 2           | Code 1         | 42.42         | 4.71             |
| 2           | Code 2         | 42.42         | 4.72             |

Der Steuerbasisbetrag wird pro Position berechnet:

- **Position 1:** 42,42
- **Position 2:** 42,42

Der Steuerbetrag wird pro Mehrwertsteuercode berechnet:

- **Position 1:**

    - Steuerbetrag für Mehrwertsteuercode 1 = 42,42 &times; 10 Prozent &divide; (1 – 10 Prozent) = 4,7133
    - Steuerbetrag für Mehrwertsteuercode 2 = 42,42 &times; 10 Prozent &divide; (1 – 10 Prozent) = 4,7133

- **Position 2:**

    - Steuerbetrag für Mehrwertsteuercode 1 = 42,42 &times; 10 Prozent &divide; (1 – 10 Prozent) = 4,7133
    - Steuerbetrag für Mehrwertsteuercode 2 = 42,42 &times; 10 Prozent &divide; (1 – 10 Prozent) = 4,7133

Der Steuerbetrag wird pro Mehrwertsteuercode-Kombination gerundet:

- Gesamt-Mehrwertsteuerbetrag = 4,7133 + 4,7133 + 4,7133 + 4,7133 = 18,8532, was auf 18,86 aufgerundet wird

Der gerundete Steuerbetrag wird jeder Position nach Mehrwertsteuercode zugeordnet:

- Ordnen Sie den Mehrwertsteuerbetrag (18,86) Position 1 und Position 2 zu:

    - **Position 1:**

        - Steuerbetrag für Mehrwertsteuercode 1 = 4,72
        - Steuerbetrag für Mehrwertsteuercode 2 = 4,71

    - **Position 2:**

        - Steuerbetrag für Mehrwertsteuercode 1 = 4,71
        - Steuerbetrag für Mehrwertsteuercode 2 = 4,72

## <a name="example-8"></a>Beispiel 8

### <a name="parameter-values"></a>Parameterwerte

| Berechnungsmethode | Rundung nach                | Herkunft                              | Berechnungsgrundlage                 |
| ------------------ | -------------------------- | ----------------------------------- | ----------------------------- |
| Position/Gesamt         | Mehrwertsteuer-Codekombination | Berechneter Prozentanteil am Nettobetrag | Nettobetrag des Rechnungssaldos |

### <a name="calculation-and-rounding-behavior"></a>Berechnung und Rundungsverhalten

| Positionsnummer | Mehrwertsteuercode | Betragsursprung | Mehrwertsteuerbetrag |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Code 1         | 42.42         | 4.72             |
| 1           | Code 2         | 42.42         | 4.71             |
| 2           | Code 1         | 42.42         | 4.71             |
| 2           | Code 2         | 42.42         | 4.72             |

Der Steuerbasisbetrag wird pro Beleg berechnet:

- Steuergrundbetrag = 42,42 + 42,42 = 84,84

Der Steuerbetrag wird pro Mehrwertsteuercode berechnet:

- Steuerbetrag für Mehrwertsteuercode 1 = 84,84 &times; 10 Prozent &divide; (1 – 10 Prozent) = 9,4267
- Steuerbetrag für Mehrwertsteuercode 2 = 84,84 &times; 10 Prozent &divide; (1 – 10 Prozent) = 9,4267

Der Steuerbetrag wird pro Mehrwertsteuercode-Kombination gerundet:

- Gesamt-Mehrwertsteuerbetrag = 9,4267 +9,4267 = 18,8534, was auf 18,86 aufgerundet wird

Der gerundete Steuerbetrag wird jeder Position nach Mehrwertsteuercode zugeordnet:

- Ordnen Sie den Mehrwertsteuerbetrag (18,86) Position 1 und Position 2 zu:

    - **Position 1:**

        - Steuerbetrag für Mehrwertsteuercode 1 = 4,72
        - Steuerbetrag für Mehrwertsteuercode 2 = 4,71

    - **Position 2:**

        - Steuerbetrag für Mehrwertsteuercode 1 = 4,71
        - Steuerbetrag für Mehrwertsteuercode 2 = 4,72

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Mehrwertsteuer-Berechnungsmethoden im Feld „Ursprung“](sales-tax-calculation-methods-origin-field.md)
- [Mehrwertsteuersteuersätze auf Grundlage der Felder Berechnungsgrundlage und Berechnungsmethode](marginal-base-field.md)
- [Optionen zur Berechnung von Gesamtbetrag und Intervall für Mehrwertsteuercodes](whole-amount-interval-options-sales-tax-codes.md)
