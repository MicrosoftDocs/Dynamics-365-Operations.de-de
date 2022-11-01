---
title: Etiketten-Layouts für die Dokumentenlenkung
description: In diesem Artikel wird beschrieben, wie Formatierungsmethoden zum Drucken von Werten auf Etiketten verwendet werden.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: a4e0c16b71c257cae832870ca58679884047ea16
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708644"
---
# <a name="document-routing-label-layout"></a>Dokument-Routing-Etiketten-Layout

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Layouts für Kennzeichen-, Container- und Wellenetiketten erstellen können. Er enthält außerdem Richtlinien für die Verwendung der Zebra Programming Language (ZPL), mit der die Layouts erstellt werden.

Die Layouts für Document Routing-Etiketten definieren die Art und Weise, wie die Etiketten gestaltet werden und welche Daten auf sie gedruckt werden. Sie konfigurieren die Druckauslöserpunkte, wenn Sie Menüelemente und Arbeitsvorlagen für mobile Geräte einrichten.

Die Informationen in diesem Artikel gelten für alle Dokument-Routing-Etiketten-Layouts, einschließlich der Layouts für [Kennzeichen-Etiketten](tasks/license-plate-label-printing.md), [Container-Etiketten](print-container-labels.md) und [Wellen-Etiketten](configure-wave-label-printing.md).

Sie können hochkomplexe Etiketten drucken, vorausgesetzt, das Druckgerät kann den an das Gerät gesendeten Text interpretieren. Ein ZPL-Layout, das einen Strichcode enthält, könnte zum Beispiel wie folgt aussehen.

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

Im Rahmen des Etikettendruckprozesses wird der Text `$LicensePlateId$` in diesem Beispiel durch einen Datenwert ersetzt. Mithilfe verschiedener weit verbreiteter Tools zur Etikettengenerierung können Sie den Text für das Etikettenlayout formatieren. Viele dieser Tools unterstützen das `$FieldName$` Format. Darüber hinaus verwendet Microsoft Dynamics 365 Supply Chain Management eine spezielle Formatierungslogik als Teil der Feldzuordnung für das Dokumentrouting-Layout.

Um die Werte anzuzeigen, die gedruckt werden sollen, gehen Sie zu **Lagerverwaltung \> Anfragen und Berichte \> Kennzeichenetiketten**.

## <a name="turn-on-this-feature-for-your-system"></a>Schalten Sie diese Funktion für Ihr System ein

Wenn Ihr System nicht bereits die in diesem Artikel beschriebenen Funktionen enthält, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die Funktion *Erweiterte Layouts für Ladungsträger* ein. (Ab Supply Chain Management Version 10.0.21 ist diese Funktion standardmäßig aktiviert. Ab Supply Chain Management 10.0.25 ist diese Funktion obligatorisch und kann nicht deaktiviert werden.)

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

Eine vollständige Liste der verfügbaren Zeichenfolgen im Zahlenformat finden Sie unter [Benutzerdefinierte Zeichenfolgen im numerischen Format](/dotnet/standard/base-types/custom-numeric-format-strings).

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

Eine vollständige Liste der verfügbaren Datums-/Zeitformate finden Sie unter [Benutzerdefinierte Datum-/Zeitformatzeichenfolgen](/dotnet/standard/base-types/custom-date-and-time-format-strings).

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

Sie können dieses Format mit anderen Typen kombinieren, die weiter oben in diesem Artikel beschrieben wurden. Sie haben beispielsweise eine Anzeigemethode mit dem Namen `DisplayListOfItemsNumbers()`, und Sie möchten die erste Artikelnummer dieser Methode drucken. In diesem Fall können Sie folgenden Code verwenden.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Weitere Informationen zum Drucken von Beschriftungen

Weitere Informationen über das Festlegen und Drucken von Etiketten finden Sie in den folgenden Artikeln:

- [Drucken von Etiketten für Ladungsträger](tasks/license-plate-label-printing.md)
- [Drucken von Etiketten für Container](print-container-labels.md)
- [Wellenbeschriftungsdruck](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
