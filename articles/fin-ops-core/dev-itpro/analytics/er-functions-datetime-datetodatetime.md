---
title: DATETODATETIME EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von DATETODATETIME bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 8c5ad1d304f0914a9ddbca951cdb7419dbcc1f46
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682438"
---
# <a name="datetodatetime-er-function"></a>DATETODATETIME EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `DATETODATETIME` gibt den Wert *DateTime* zurück, der über den vorgegebenen Datumswert in einen Wert für Datum/Uhrzeit in der Koordinierten Weltzeit (Greenwich Mean Time \[GMT\]) konvertiert wird.

## <a name="syntax"></a>Syntax

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>Argumente

`date`: *Date*

Ein Datumswert, der das zu konvertierende Datum darstellt.

## <a name="return-values"></a>Rückgabewerte

*DateTime*

Der resultierende Wert für Datum/Uhrzeit.

## <a name="example-1"></a>Beispiel 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` gibt das Datum der aktuellen Microsoft Dynamics 365 Finance-Sitzung, Dezember 24, 2015, mit **12/24/2015 12:00:00 AM** zurück. In diesem Beispiel ist **CompInfo** eine Datenquelle für die elektronische Berichterstattung (ER) vom Typ **Finance and Operations/Tabelle**, und sie bezieht sich auf die Tabelle CompanyInfo.

## <a name="example-2"></a>Beispiel 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` gibt den Wert **11/12/2019 12:00:00 AM** für Datum/Uhrzeit zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datums- und Zeitfunktionen](er-functions-category-datetime.md)
