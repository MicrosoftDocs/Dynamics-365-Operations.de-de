---
title: Liste der EB-Funktionen in der Kategorie „Datum und Uhrzeit“
description: Dieser Artikel enthält Informationen zu den Datums- und Uhrzeitfunktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
author: NickSelin
ms.date: 09/09/2021
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
ms.openlocfilehash: e6e15d143bad016883f03ecf0125ce9429215a71
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880238"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Liste der EB-Funktionen in der Kategorie „Datum und Uhrzeit“

[!include [banner](../includes/banner.md)]

Datums- und Zeitfunktionen für die elektronische Berichterstellung (EB) können verwendet werden, um Informationen aus Datums- und Zeitwerten zu extrahieren und Operationen an diesen durchzuführen. Dieser Artikel enthält eine Zusammenfassung dieser Funktionen.

## <a name="list-of-supported-functions"></a>Liste der unterstützten Funktionen

| Funktion | Beschreibung |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Diese Funktion gibt den Wert *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* zurück, der die angegebene Anzahl von Tagen vor oder nach einem angegebenen Startdatum darstellt. |
| [ChangeTimeZone](er-functions-datetime-changetimezone.md) | Diese Funktion gibt den Wert *DateTime* zurück, der über einen vorgegebenen Datums-/Zeitwert in einer Zeitzone in einen Datum-/Uhrzeitwert in einer anderen Zeitzone konvertiert wird. |
| [DateFormat](er-functions-datetime-dateformat.md) | Diese Funktion gibt den Wert *[String](er-formula-supported-data-types-primitive.md#string)* zurück, der einen vorgegebenen Datenwert als Text im angegebenen Format und in einer optional angegebenen Kultur darstellt. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Diese Funktion gibt den Wert *String* zurück, der einen vorgegebenen Wert für Datum/Uhrzeit als Text im angegebenen Format und in einer optional angegebenen Kultur darstellt. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Diese Funktion gibt den Wert *DateTime* zurück, der über einen vorgegebenen Textwert in das spezielle Format und in einen optional angegebenen Wert für Datum/Uhrzeit konvertiert wird. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Diese Funktion gibt den Wert *DateTime* zurück, der über einen vorgegebenen Datumswert in einen Wert für Datum/Uhrzeit in der Koordinierten Weltzeit (Greenwich Mean Time \[GMT\]) konvertiert wird. |
| [DateValue](er-functions-datetime-datevalue.md) | Diese Funktion gibt den Wert *[Date](er-formula-supported-data-types-primitive.md#date)* zurück, der über einen vorgegebenen Textwert in das spezielle Format und in einen optional angegebenen Wert für Datum/Uhrzeit konvertiert wird. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Diese Funktion gibt einen *[Ganzzahl](er-formula-supported-data-types-primitive.md#integer)*-Wert zurück, der die Anzahl der Tage zwischen dem 01. Januar und dem angegebenen Datum darstellt. |
| [Tage](er-functions-datetime-days.md) | Diese Funktion gibt einen Wert für *Ganzzahl* zurück, der die Anzahl der Tage zwischen einem angegebenen Datum und einem zweiten angegebenen Datum darstellt. |
| [Now](er-functions-datetime-now.md) | Diese Funktion gibt den Wert *DateTime* zurück, der das aktuelle Datum und die Uhrzeit des Anwendungsservers darstellt. |
| [NullDate](er-functions-datetime-nulldate.md) | Diese Funktion gibt den Wert *Date* zurück, der das Datum **null** (01. Januar 1900) darstellt. |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Diese Funktion gibt den Wert *DateTime* zurück, der den Wert für Datum/Uhrzeit **null** (01. Januar 1900) in Koordinierter Weltzeit darstellt. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Diese Funktion gibt den Wert *DateTime* zurück, der das aktuelle Datum und die Uhrzeit der Anwendungssitzung darstellt. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Diese Funktion gibt den Wert *Date* zurück, der das aktuelle Anwendungssitzungsdatum darstellt. |
| [Heute](er-functions-datetime-today.md) | Diese Funktion gibt den Wert *Date* zurück, der das aktuelle Anwendungsserverdatum darstellt. |
| [WeekNum](er-functions-datetime-weeknum.md) | Diese Funktion gibt einen *Ganzzahl*-Wert zurück, der die Woche des Jahres darstellt. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
