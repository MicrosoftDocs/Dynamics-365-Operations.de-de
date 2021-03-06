---
title: ADDDAYS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von ADDDAYS bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 0c420daa04b8e22504d25d317c75826f1d1914b7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747058"
---
# <a name="adddays-er-function"></a>ADDDAYS EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `ADDDAYS` berechnet den Wert *DateTime*, der die angegebene Anzahl von Tagen vor oder nach einem angegebenen Startdatum darstellt.

## <a name="syntax"></a>Syntax

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Argumente

`datetime`: *DateTime*

Ein Datums-/Zeitwert, der das Startdatum darstellt.

`days`: *Integer*

Die Anzahl von Tagen vor oder nach `datetime`.

## <a name="return-values"></a>Rückgabewerte

*DateTime*

Der resultierende Wert für Datum/Uhrzeit.

## <a name="usage-notes"></a>Anwendungshinweise

Ein positiver Wert für `days` ergibt ein zukünftiges Datum. Ein negativer Wert ergibt ein vergangenes Datum.

## <a name="example-1"></a>Beispiel 1

`ADDDAYS (NOW(), 7)` gibt das Datum und die Uhrzeit sieben Tage in der Zukunft zurück.

## <a name="example-2"></a>Beispiel 2

`ADDDAYS (NOW(), -3)` gibt das Datum und die Uhrzeit drei Tage in der Vergangenheit zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datums- und Zeitfunktionen](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]