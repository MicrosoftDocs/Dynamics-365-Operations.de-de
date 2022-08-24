---
title: FORMATELEMENTNAME EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung von FORMATELEMENTNAME bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 1c8c319075f8f39bec963df2c88d2d8d3beace43
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275424"
---
# <a name="formatelementname-er-function"></a>FORMATELEMENTNAME EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `FORMATELEMENTNAME` gibt den Wert *String* zurück, der den Namen des aktuellen Formatelements der elektronischen Berichterstattung (EB) darstellt.

## <a name="syntax"></a>Syntax

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="usage-notes"></a>Anwendungshinweise

Diese Funktion kann in EB-Ausdrücken abgerufen werden, die für die Eigenschaften **Gesammelter Datenschlüsselname** und **Gesammelter Datenschlüsselwert** einer EB-Formatskomponente aus der Gruppe **Text** konfiguriert wurde, die sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.

## <a name="example"></a>Beispiel

Um mehr darüber zu erfahren, wie diese Funktion verwendet wird, finden Sie Informationen im Aufgabenleitfaden [EB – Verwendung von Daten der Formatausgabe für Inventur und Summierungen](tasks/er-format-counting-summing-1.md), der Teil des Geschäftsprozesses **IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln** ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datensammlungsfunktionen](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
