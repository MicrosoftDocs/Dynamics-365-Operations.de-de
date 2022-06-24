---
title: FA_SUM EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der FA_SUM-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 1c15c8d76536ac27fc687541f9396bbb750a2de2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869285"
---
# <a name="fa_sum-er-function"></a>FA_SUM EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `FA_SUM` gibt den Wert *Container (Datensatz)* zurück, der aus Daten für die Anlagenbeträge für die angegebene Anlagenposition, dem Wertmodellcode und den Datumszeiträumen besteht.

## <a name="syntax"></a>Syntax

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Argumente

`fixed asset code`: *String*

Der Wert *String*, der den Code eines Gegenstands des Anlagevermögens darstellt, für den der Saldo berechnet wird.

`value model code`: *String*

Der Wert *String*, der den Code eines Gegenstands des Wertmodells darstellt, für das der Saldo berechnet wird.

`start date`: *Date*

Ein Wert *Date*, der das Startdatum eines Zeitraums darstellt, für den die Beträge des Anlagevermögens berechnet werden.

`end date`: *Date*

Ein Wert *Date*, der das Enddatum eines Zeitraums darstellt, für den die Beträge des Anlagevermögens berechnet werden.

## <a name="return-values"></a>Rückgabewerte

*Container (Datensatz)*

Der resultierende Datensatzwert.

## <a name="example"></a>Beispiel

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` gibt den Datencontainer für Anlage **COMP-000001** zurück, der für das Wertmodell **Aktuell** und für einen Zeitraum von **Date1** bis **Date2** vorbereitet wurde.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Andere (geschäftsdomänenspezifische) Funktionen](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]