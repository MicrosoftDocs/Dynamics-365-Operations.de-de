---
title: ENUMERATE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ENUMERATE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
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
ms.openlocfilehash: b05448b57d3b08af61144dacdfa2a4e1ba30d009
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746650"
---
# <a name="enumerate-er-function"></a>ENUMERATE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `ENUMERATE` gibt einen neuen Wert von *Datensatzliste* zurück, der aus Aufzählungsdatensätzen der angegebenen Liste besteht.

## <a name="syntax"></a>Syntax

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

Die Liste der zurückgegebenen Aufzählungsdatensätze enthält die folgenden zusätzlichen Elemente:

- Den Datensatz der Felder (Komponente **Wert**)
- Der Index des aktuellen Datensatzes (**Nummer** komponente)

## <a name="example"></a>Beispiel

In der folgenden Abbildung wird eine Datenquelle **Aufgezählt** als Aufzählungsliste von Lieferantendatensätzen von der Datenquelle **Lieferanten** erstellt, die sich auf die Tabelle „VendTable” bezieht.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

Die folgende Abbildung zeigt das Format der elektronischen Berichterstattung. In diesem Format werden Datenbindungen erstellt, um eine Ausgabe im XML-Format zu generieren. In dieser Ausgabe werden einzelne Lieferanten als aufgezählte Knoten präsentiert.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

Die folgende Abbildung zeigt das Ergebnis, wenn das entworfene Format ausgeführt wird.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]