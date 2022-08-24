---
title: SPLITLIST EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der SPLITLIST-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 03/15/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 38ac7e6c6bdf53705d1374c173422f7347253a5f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292525"
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
