---
title: SPLITLISTBYLIMIT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der SPLITLISTBYLIMIT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bf13b7c1e7cab7c803b352370084421a8180dee
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743429"
---
# <a name="splitlistbylimit-er-function"></a>SPLITLISTBYLIMIT EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `SPLITLISTBYLIMIT` teilt die angegebene Liste in eine neue Liste von Unterlisten (Batches) auf. Die Anzahl der Datensätze in jedem Batch wird dynamisch berechnet. Die Funktion gibt dann das Ergebnis als neuen Wert *Datensatzliste* zurück, der aus den Batches besteht.

## <a name="syntax"></a>Syntax

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

`limit value`: *Integer* oder *Real*

Der maximale Wert des Grenzwerts, der zum Aufteilen der ursprünglichen Liste in Batches verwendet wird.

`limit source`: *Feld*

Der gültige Pfad eines Feldes des Typs *Integer* oder *Real* in der angegebenen Liste. Der Wert dieses Feldes definiert den Schritt, bei dem die Gesamtsumme erhöht wird.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

Die Liste der Batches, die zurückgegeben wird, enthält die folgenden Elemente:

- **Wert**: *Liste*

    Die Liste der Datensätze, die zum aktuellen Batch gehören.

- **BatchNumber**: *Integer*

    Die Nummer des aktuellen Batches in der zurückgegebenen Liste.

Die Begrenzung wird auf keinen einzelnen Artikel der ursprünglichen Liste angewendet, wenn die Begrenzungsquelle die definierte Begrenzung überschreitet.

## <a name="example"></a>Beispiel

Die folgende Abbildung zeigt das Format der elektronischen Berichterstattung (EB).

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

Die folgende Abbildung zeigt die Datenquellen an, die für das Format verwendet werden.

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

Die folgende Abbildung zeigt das Ergebnis an, wenn Format ausgeführt wird. In diesem Fall ist die Ausgabeliste eine flache Liste von Warenartikeln.

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

In den folgenden Abbildungen ist dasselbe Format so angepasst worden, dass es die Liste der Warenpositionen in Chargen präsentiert, wenn eine einzelne Charge Waren enthalten muss und das Gesamtgewicht nicht die Begrenzung von 9 überschreiten sollte.

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

Die folgende Abbildung zeigt das Ergebnis, wenn das angepasste Format ausgeführt wird.

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> Die Begrenzung wird nicht auf den letzten Artikel der ursprünglichen Liste angewendet, weil der Wert (**11**) der Begrenzungsquelle (**Gewicht**) die definierte Begrenzung (**9**) überschreitet. Um Unterlisten beim Erstellen von Berichten zu ignorieren, verwenden Sie entweder die Funktion `WHERE` oder den Ausdruck **Aktiviert** des entsprechenden Formatelements.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)
