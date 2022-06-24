---
title: SPLITLIST EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der SPLITLIST-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 03/15/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30226b50f5705d5a43fa48ce5c6f92e150871b3a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845482"
---
# <a name="splitlist-er-function"></a>SPLITLIST EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `SPLITLIST` teilt die angegebene Liste in Unterlisten (oder Batches), die jeweils die angegebene Anzahl von Datensätzen enthalten. Sie gibt dann das Ergebnis als neuen Wert *Datensatzliste* zurück, der aus den Batches besteht.

## <a name="syntax-1"></a>Syntax 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>Syntax 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

`number`: *Integer*

Die maximale Anzahl angezeigter Datensätze pro Batch.

`on-demand reading flag`: *Boolesch*

Ein *Boolescher Wert*, der angibt, ob Elemente von Unterlisten bei Bedarf generiert werden sollen.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

Die Liste der Batches, die zurückgegeben wird, enthält die folgenden Elemente:

 - **Wert:** *Liste*

    Die Liste der Datensätze, die zum aktuellen Batch gehören.

- **BatchNumber:** *Integer*

    Die Nummer des aktuellen Batches in der zurückgegebenen Liste.

Wenn das On-Demand-Leseflag auf **Wahr**  gesetzt ist, werden Unterlisten auf Anforderung erstellt, was eine Reduzierung des Speicherverbrauchs ermöglicht, jedoch zu Leistungseinbußen führen kann, wenn Elemente nicht nacheinander verwendet werden.

## <a name="example"></a>Beispiel

In der folgenden Abbildung wird eine Datenquelle **Positionen** als eine Datensatzliste von drei Datensätzen erstellt. Diese Liste wird in Chargen aufgeteilt, die jeweils bis zu zwei Datensätze enthalten.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Die folgende Abbildung zeigt das entworfene Formatlayout. In diesem Formatlayout werden die Bindungen an die Datenquelle **Positionen** erstellt, mit Ausgabe im XML-Format zu generieren. Dies Ausgabe präsentiert einzelne Knoten für jede Charge und die darin befindlichen Datensätze.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

Die folgende Abbildung zeigt das Ergebnis, wenn das entworfene Format ausgeführt wird.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
