---
title: SPLITLIST EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der SPLITLIST-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: af8c413726ca8d9f92eff18807e7fa9002fc9d37
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559137"
---
# <a name="splitlist-er-function"></a>SPLITLIST EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `SPLITLIST` teilt die angegebene Liste in Unterlisten (oder Batches), die jeweils die angegebene Anzahl von Datensätzen enthalten. Sie gibt dann das Ergebnis als neuen Wert *Datensatzliste* zurück, der aus den Batches besteht.

## <a name="syntax"></a>Syntax

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

`number`: *Integer*

Die maximale Anzahl angezeigter Datensätze pro Batch.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

Die Liste der Batches, die zurückgegeben wird, enthält die folgenden Elemente:

 - **Wert:** *Liste*

    Die Liste der Datensätze, die zum aktuellen Batch gehören.

- **BatchNumber:** *Integer*

    Die Nummer des aktuellen Batches in der zurückgegebenen Liste.

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