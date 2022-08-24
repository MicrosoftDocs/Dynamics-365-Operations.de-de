---
title: REPEAT EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der REPEAT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220690"
---
# <a name="repeat-er-function"></a>REPEAT EB-Funktion

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Die `REPEAT`-Funktion erstellt einen Datensatz, der das Feld enthält, dessen Wert der angegebenen Eingabe entspricht. Es gibt dann eine neue *Datensatzliste* eines Datensatzes zurück, der eine bestimmte Anzahl von Male wiederholt wird.

## <a name="syntax"></a>Syntax

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>Argumente

`item`: Alle unterstützten [primitiven](er-formula-supported-data-types-primitive.md) oder [zusammengesetzten](er-formula-supported-data-types-composite.md) Datentyp

Der zu wiederholende Wert.

`number`: *Integer*

Die Anzahl der Wiederholungen.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

Die Liste der wiederholten Aufzählungsdatensätze enthält die folgenden Felder:

- Der spezifische Wert (Feld `Item`)
- Der Index des aktuellen Datensatzes (Feld `Number`)

> [!NOTE]
> Geben Sie den Wert an, da für diese Funktion eine auf eins basierende Nummerierung verwendet wird. Das Feld `Number` hat für den ersten Datensatz der entstehenden Liste den Wert **1**.

Sie können diese Funktion verwenden, um vorhandene Daten zu multiplizieren, damit Sie Leistungs- und Volumentests der Lösungen zur [Elektronischen Berichterstellung (EB)](general-electronic-reporting.md) mit dem [Regression Suite Automation Tool (RSAT)](../perf-test/rsat/rsat-overview.md).

## <a name="example"></a>Beispiel

Sie möchten ein Dokument im XML-Format generieren, das möglichst viele `Party`-XML-Elemente enthalten muss, die Sie zur Laufzeit in einem Dateneingabefeld im Dialogfeld angeben, bevor die Ausführung eines EB-Formats beginnt.

Die folgende Abbildung zeigt das EB-[Format](er-overview-components.md#format-component). In diesem Format wird das einzelne `Party`-XML-Element hinzugefügt, um die Eigenschaften einer einzelnen Partei anzuzeigen.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

Die nächste Abbildung zeigt die folgenden konfigurierten Datenquellen:

- Die `Party`-Datenquelle, die eine einzelne Partei darstellt. Das `Party.Value`-Feld wird verwendet, um einen einzelnen Textwert verfügbar zu machen.
- Die `NumberOfRepeats`-[Datenquelle](er-user-input-parameter-data-sources.md) die verwendet wird, um zur Laufzeit ein Dateneingabefeld im Dialogfenster anzubieten, damit Sie die Anzahl der Parteien angeben können, die in das generierte Dokument eingetragen werden sollen.
- Die `Party2`-Datenquelle, die den `Party`-Datensatz der Anzahl der Male wiederholt, die Sie in der `NumberOfRepeats`-Datenquelle angegeben haben.

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

Die nächste Abbildung zeigt Datenbindungen im bearbeitbaren EB-Format, die erstellt werden, um eine Ausgabe im XML-Format zu generieren. In dieser Ausgabe werden einzelne Parteien als aufgezählte Knoten präsentiert.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

Die folgende Abbildung zeigt das Ergebnis, wenn das entworfene Format ausgeführt wird. Der Wert der `NumberOfRepeats`-Datenquelle ist auf **5** festgelegt.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
