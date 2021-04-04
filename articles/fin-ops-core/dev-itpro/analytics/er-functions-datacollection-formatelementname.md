---
title: FORMATELEMENTNAME EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von FORMATELEMENTNAME bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 1e2ee2faa2784f34d540c113622cee2090f24cef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561301"
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