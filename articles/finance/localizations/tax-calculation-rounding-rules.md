---
title: Rundungsregeln für die Steuerberechnung
description: Dieser Artikel liefert Informationen über die Rundungsregeln in den Steuerberechnungsparametern des Steuerberechnungsdienstes.
author: kailiang
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0f6182ab18a5a408a6e526feec7014ccdfce8af0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858300"
---
# <a name="tax-calculation-rounding-rules"></a>Rundungsregeln für die Steuerberechnung

[!include [banner](../includes/banner.md)]

Dieser Artikel liefert Informationen darüber, wie die Rundungsregeln in den Steuerberechnungsparametern des Steuerberechnungsdienstes funktionieren.

> [!NOTE] 
> Wenn der Steuerberechnungsdienst aktiviert ist, sind die Rundungsregeln auf den Seiten **Umsatzsteuer-Code** und **Umsatzsteuer-Gruppe** nicht wirksam.

Sie können die Konfiguration der Rundungsregeln für den Steuerberechnungsdienst im Abschnitt **Umsatzsteuer-Rundungsregel** im Inforegister **Berechnung** auf der Registerkarte **Allgemein** der Seite **Steuerberechnungsparameter** (**Steuern** \> **Einrichtung** \> **Steuerkonfiguration** \> **Steuerberechnungsparameter**) einsehen.

[![Rundungsregel-Konfiguration auf der Seite Steuerberechnungsparameter](./media/tax-calculation-parameters-calculation-1.png)](./media/tax-calculation-parameters-calculation-1.png)

Die Felder **Rundungsgenauigkeit** und **Rundungsmethode** bestimmen, wie berechnete Beträge in der Payload vom Steuerberechnungsdienst gerundet werden.

## <a name="rounding-precision"></a>Rundungsgenauigkeit

Das Feld **Rundungsgenauigkeit** unterstützt einen Wert, der bis zu sechs Dezimalstellen hat. Wenn Sie zum Beispiel das Feld **Rundungsgenauigkeit** auf **0,000000** festlegen, werden berechnete Beträge auf sechs Dezimalstellen gerundet und dann an Microsoft Dynamics 365 Finance gesendet. Wenn zum Beispiel die Rundungsmethode **Normal** verwendet wird, wird der Betrag **987.1234567** auf **987.123457** gerundet.

> [!NOTE]
> Finance rundet Beträge gemäß den Währungsrundungsregeln. Daher werden die Steuerbeträge, die in Transaktionen angezeigt und erfasst werden, sowohl von den Rundungsregeln für die Steuerberechnung als auch von den Rundungsregeln für die Währung beeinflusst.

## <a name="rounding-method"></a>Rundungsmethode

Die Rundungsmethode für die Steuerberechnung kann für jede juristische Entität konfiguriert werden. Im Feld **Rundungsmethode** können Sie zwischen drei Optionen wählen: **Normal**, **Abwärts** und **Aufwärtsrunden**.

### <a name="rounding-example"></a>Beispiel für Aufrundung

In der folgenden Tabelle finden Sie ein Beispiel, das zeigt, wie der Betrag **987,345** für verschiedene Kombinationen von Rundungsgenauigkeiten und Rundungsmethoden gerundet wird.

<table>
<thead>
<tr>
<th rowspan="2">Rundungsmethode</th>
<th colspan="8">Rundungsgenauigkeit</th>
</tr>
<tr>
<th>0,00</th>
<th>0.01</th>
<th>0.10</th>
<th>1.00</th>
<th>10.00</th>
<th>0.02</th>
<th>0.05</th>
<th>0.25</th>
</tr>
</thead>
<tbody>
<tr>
<td>Normal</td>
<td>987.35</td>
<td>987.35</td>
<td>987.30</td>
<td>987.00</td>
<td>990.00</td>
<td>987.34</td>
<td>987.35</td>
<td>987.25</td>
</tr>
<tr>
<td>Abwärts</td>
<td>987.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.00</td>
<td>980.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.25</td>
</tr>
<tr>
<td>Aufrunden</td>
<td>988.00</td>
<td>987.35</td>
<td>987.40</td>
<td>988.00</td>
<td>990.00</td>
<td>987.36</td>
<td>987.35</td>
<td>987.50</td>
</tr>
</tbody>
</table>

Die Berechnungs- und Rundungslogik von Steuerbeträgen kann entsprechend den Besteuerungsregeln konfiguriert werden.

## <a name="rounding-by"></a>Rundung nach 

Wählen Sie im Feld **Rundung durch** das Rundungsprinzip, das für die Steuern gilt. Die folgenden Optionen stehen zur Verfügung:

- **Steuercodes** - Runden Sie den Steuerbetrag innerhalb jedes Steuercodes.
- **Steuercode-Kombinationen** - Runden Sie den Steuerbetrag innerhalb der Steuercode-Kombination in der Zeile.

## <a name="calculation-method"></a>Berechnungsmethode

Wählen Sie im Feld **Berechnungsmethode**, ob die Steuern auf Rechnungen für jede Zeile oder für alle Zeilen berechnet werden. Die folgenden Optionen stehen zur Verfügung:

- **Zeile** - Berechnen Sie den Steuerbetrag zeilenweise. Der Steuerbetrag in jeder Zeile wird nicht durch den Steuerbetrag in anderen Zeilen beeinflusst.
- **Gesamt** - Berechnen Sie den Steuerbetrag über alle Zeilen eines Belegs.

### <a name="rounding-calculation-example"></a>Beispiel für Rundungsberechnungen

Dieses Beispiel zeigt die verschiedenen Berechnungen, die für eine Rechnung durchgeführt werden können, für verschiedene Kombinationen der Werte **Rundung durch** und **Berechnungsmethode**. Für dieses Beispiel ist die folgende Einrichtung vorhanden:

- Die Rechnung hat vier Zeilen.
- Es gibt zwei Steuerkennzeichen: **VAT1** (10 Prozent) und **VAT2** (10 Prozent).
- Die Rundungsgenauigkeit ist auf **0,01** festgelegt.
- Die Rundungsmethode ist festgelegt auf **Aufrunden**.

#### <a name="rounding-by--tax-codes-and-calculation-method--line"></a>Rundung durch = Steuerkennzeichen und Berechnungsmethode = Zeile

| Positionsnummer | Nettobetrag der Zeile | Ermittelte Steuerkennzeichen | Steuerbetrag vor Rundung | Gerundeter Steuerbetrag |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2           | 22.22           | VAT1; VAT2           | 2.222; 2.222               | 2.23; 2.23         |
| 3           | 33.33           | VAT1                 | 3.333                      | 3.34               |
| 4           | 44.44           | VAT1; VAT2           | 4.444; 4;444               | 4.45; 4.45         |

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--line"></a>Rundung durch = Steuerkennzeichen-Kombinationen und Berechnungsmethode = Zeile

| Positionsnummer | Nettobetrag der Zeile | Ermittelte Steuerkennzeichen | Steuerbetrag vor Rundung | Gerundeter Steuerbetrag |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2\*         | 22.22           | VAT1; VAT2           | 2.222; 2.222               | 2.23; 2.22         |
| 3           | 33.33           | VAT1                 | 3.333                      | 3.34               |
| 4\*\*       | 44.44           | VAT1; VAT2           | 4.444; 4;444               | 4.45; 4.44         |

\* Zeile 2 = Round\[22.22 × (10 percent + 10 percent)\] = 2.23 + 2.22

\*\* Line 4 = Round\[44.44 × (10 percent + 10 percent)\] = 4.45 + 4.44

#### <a name="rounding-by--tax-codes-and-calculation-method--total"></a>Rundung durch = Steuerkennzeichen und Berechnungsmethode = Summe

| Positionsnummer | Nettobetrag der Zeile | Ermittelte Steuerkennzeichen | Steuerbetrag vor Rundung | Gerundeter Steuerbetrag |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1\*               | 1.111                      | 1.12               |
| 2           | 22.22           | VAT1\*; VAT2\*\*     | 2.222; 2.222               | 2.22; 2.23         |
| 3           | 33.33           | VAT1\*               | 3.333                      | 3.33               |
| 4           | 44.44           | VAT1\*; VAT2\*\*     | 4.444; 4;444               | 4.44; 4.44         |

\* VAT1(Line 1, Line 2, Line 3, Line 4) = Round\[(11.11 + 22.22 + 33.33 + 44.44) × 10 percent\] = 1.12 + 2.22 + 3.33 + 4.44

\*\* VAT2(Line 2, Line 4) = Round\[(22.22 + 44.44) × 10 percent\] = 2.23 + 4.44

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--total"></a>Rundung durch = Steuerkennzeichen-Kombinationen und Berechnungsmethode = Summe

| Positionsnummer | Nettobetrag der Zeile | Ermittelte Steuerkennzeichen | Steuerbetrag vor Rundung | Gerundeter Steuerbetrag |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1\*         | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2\*\*       | 22.22           | VAT1; VAT2           | 2.222; 2.222               | 2.23; 2.22         |
| 3\*         | 33.33           | VAT1                 | 3.333                      | 3.33               |
| 4\*\*       | 44.44           | VAT1; VAT2           | 4.444; 4;444               | 4.44; 4.45         |

\* Line 1, Line 3 = Round\[(11.11 + 33.33) × 10 percent\] = 1.12 + 3.33

\*\* Line 2, Line 4 = Round\[(22.22 + 44.44) × (10 percent + 10 percent)\] = 2.23 + 2.22 + 4.44 + 4.45

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
