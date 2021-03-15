---
title: Dokumenten-Routing-Layout für Kennzeichenetiketten
description: In diesem Thema wird beschrieben, wie Formatierungsmethoden zum Drucken von Werten auf Etiketten verwendet werden.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 66ba73ab5c790aa4a67419842f63f6f741bf0d3a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973759"
---
# <a name="document-routing-layout-for-license-plate-labels"></a>Dokumenten-Routing-Layout für Kennzeichenetiketten

[!include [banner](../includes/banner.md)]

Das Layout des Dokumentroutings definiert das Layout der Kennzeichenetiketten und die darauf gedruckten Daten. Sie konfigurieren die Druckauslöserpunkte, wenn Sie Menüelemente und Arbeitsvorlagen für mobile Geräte einrichten.

In einem typischen Szenario drucken Lagerempfänger unmittelbar nach der Aufzeichnung des Inhalts von Paletten, die im Empfangsbereich eintreffen, Kennzeichenetiketten. Die physischen Etiketten werden auf die Paletten aufgebracht. Sie können dann zur Validierung als Teil des folgenden Einlagerungsprozesses und zukünftiger ausgehender Kommissioniervorgänge verwendet werden.

Sie können hochkomplexe Etiketten drucken, vorausgesetzt, das Druckgerät kann den an das Gerät gesendeten Text interpretieren. Beispielsweise kann ein ZPL-Layout (Zebra Programming Language), das einen Barcode enthält, dem folgenden Beispiel ähneln.

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

Im Rahmen des Etikettendruckprozesses wird der Text `$LicensePlateId$` in diesem Beispiel durch einen Datenwert ersetzt.

Um die Werte anzuzeigen, die gedruckt werden sollen, gehen Sie zu **Lagerverwaltung \> Anfragen und Berichte \> Kennzeichenetiketten**.

Mithilfe verschiedener weit verbreiteter Tools zur Etikettengenerierung können Sie den Text für das Etikettenlayout formatieren. Viele dieser Tools unterstützen das `$FieldName$` Format. Darüber hinaus verwendet Microsoft Dynamics 365 Supply Chain Management eine spezielle Formatierungslogik als Teil der Feldzuordnung für das Dokumentrouting-Layout.

## <a name="custom-number-formats"></a>Benutzerdefinierte Zahlenformate

Sie können die Formatierung der gedruckten numerischen Feldwerte mithilfe von Codes im folgenden Format anpassen.

```dos
$FieldName:FormatString$
```

Hier ist eine Erklärung für dieses Format:

- `FieldName` ist der Name des Datenfeldes (z. B. **Menge**).
- `FormatString` definiert, wie die Daten gedruckt werden müssen.

Die folgenden Beispiele zeigen, wie Sie die Arbeitsmenge anpassen können (**Menge**) Feld:

- Um immer vier Ziffern anzuzeigen (indem Sie Nullen als Platzhalter verwenden), verwenden Sie `$Qty:0000$`. Wenn die Menge beispielsweise 10 ist, wird auf dem Etikett 0010 angezeigt.
- Um immer zwei Dezimalstellen anzuzeigen, verwenden Sie `$Qty:0.00$`. Wenn die Menge beispielsweise 10 ist, wird auf dem Etikett 10.00 angezeigt.

Eine vollständige Liste der verfügbaren Zeichenfolgen im Zahlenformat finden Sie unter [Benutzerdefinierte Zeichenfolgen im numerischen Format](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="custom-string-formats"></a>Benutzerdefinierte Zeichenfolgenformate

Sie können die ersten Zeichen einer Zeichenfolge mithilfe des folgenden Feld- und Formatcodes entfernen.

```dos
$FieldName:#..$
```

Hier, `#` gibt die Anzahl der zu überspringenden Zeichen an. Verwenden Sie beispielsweise `$LicensePlateId:2..$`, um Serien-Versandcontainercode (SSCC) Kennzeichennummer zu drucken, das die ersten beiden Zeichen nicht enthält. In diesem Fall wird das Kennzeichen 0011111111111222221 als 11111111111222221 gedruckt.

## <a name="custom-datetime-formats"></a>Benutzerdefinierte Datums-/Uhrzeitformate

Das folgende Beispiel zeigt, wie Sie das Format steuern können, das zum Drucken von Datumsangaben verwendet wird.

```dos
$PrintedDate:dd-MM-yyyy$
```

In diesem Beispiel wird das Datum 30. April 2020 als 30-04-2020 gedruckt.

Eine vollständige Liste der verfügbaren Datums-/Zeitformate finden Sie unter [Benutzerdefinierte Datum-/Zeitformatzeichenfolgen](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="print-individual-lines-from-multiline-data"></a>Drucken Sie einzelne Zeilen aus mehrzeiligen Daten

Wenn ein Datenfeld mehrere Zeilen enthält (d.h Zeilen, die durch Zeilenumbrüche getrennt sind), können Sie eine einzelne Zeile im folgenden Format drucken.

```dos
$FieldName[#]$
```

Hier ist `#` die Zeilennummer, die Sie drucken möchten. (Verwenden Sie 1 für die erste Zeile.)

Zum Beispiel hat Ihr System ein Feld `AdditionalAddress`, in dem die folgende mehrzeilige Adresse gespeichert ist:

Contoso Inc.  
123 Straßenname  
Eine Stadt, ein Staat

Sie können diese Adresse zeilenweise mit den folgenden Codes drucken.

| Code | Text, der gedruckt wird |
|---|---|
| `$AdditionalAddress[1]$` | Contoso Inc. |
| `$AdditionalAddress[2]$` | 123 Straßenname |
| `$AdditionalAddress[3]$` | Eine Stadt, ein Staat |

## <a name="print-and-format-from-a-display-method"></a>Drucken und Formatieren über eine Anzeigemethode

Sie können von einer Anzeigemethode aus im folgenden Format drucken.

```dos
$DisplayMethod()$
```

Sie können dieses Format mit anderen Typen kombinieren, die weiter oben in diesem Thema beschrieben wurden. Sie haben beispielsweise eine Anzeigemethode mit dem Namen `DisplayListOfItemsNumbers()`, und Sie möchten die erste Artikelnummer dieser Methode drucken. In diesem Fall können Sie folgenden Code verwenden.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Weitere Informationen zum Drucken von Beschriftungen

Weitere Informationen zum Einrichten und Drucken von Etiketten finden Sie unter [Aktivieren Sie das Drucken von Kennzeichnungsetiketten](tasks/license-plate-label-printing.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]