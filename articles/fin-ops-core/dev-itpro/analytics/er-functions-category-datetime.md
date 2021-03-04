---
title: Liste der EB-Funktionen in der Kategorie „Datum und Uhrzeit“
description: Dieses Thema enthält Informationen zu den Datums- und Uhrzeitfunktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2745298ae1f6787c3de5a4aaf6a2a6350f5f3e85
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686218"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Liste der EB-Funktionen in der Kategorie „Datum und Uhrzeit“

[!include [banner](../includes/banner.md)]

Datums- und Zeitfunktionen für die elektronische Berichterstellung (EB) können verwendet werden, um Informationen aus Datums- und Zeitwerten zu extrahieren und Operationen an diesen durchzuführen. Dieses Thema enthält eine Zusammenfassung dieser Funktionen.

## <a name="list-of-supported-functions"></a>Liste der unterstützten Funktionen

| Funktion | Beschreibung |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Diese Funktion gibt den Wert *DateTime* zurück, der die angegebene Anzahl von Tagen vor oder nach einem angegebenen Startdatum darstellt. |
| [DateFormat](er-functions-datetime-dateformat.md) | Diese Funktion gibt den Wert *String* zurück, der einen vorgegebenen Datenwert als Text im angegebenen Format und in einer optional angegebenen Kultur darstellt. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Diese Funktion gibt den Wert *String* zurück, der einen vorgegebenen Wert für Datum/Uhrzeit als Text im angegebenen Format und in einer optional angegebenen Kultur darstellt. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Diese Funktion gibt den Wert *DateTime* zurück, der über einen vorgegebenen Textwert in das spezielle Format und in einen optional angegebenen Wert für Datum/Uhrzeit konvertiert wird. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Diese Funktion gibt den Wert *DateTime* zurück, der über einen vorgegebenen Datumswert in einen Wert für Datum/Uhrzeit in der Koordinierten Weltzeit (Greenwich Mean Time \[GMT\]) konvertiert wird. |
| [DateValue](er-functions-datetime-datevalue.md) | Diese Funktion gibt den Wert *Date* zurück, der über einen vorgegebenen Textwert in das spezielle Format und in einen optional angegebenen Wert für Datum/Uhrzeit konvertiert wird. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Diese Funktion gibt einen Wert für *Ganzzahl* zurück, der die Anzahl der Tage zwischen dem 01. Januar und dem angegebenen Datum darstellt. |
| [Tage](er-functions-datetime-days.md) | Diese Funktion gibt einen Wert für *Ganzzahl* zurück, der die Anzahl der Tage zwischen einem angegebenen Datum und einem zweiten angegebenen Datum darstellt. |
| [Now](er-functions-datetime-now.md) | Diese Funktion gibt den Wert *DateTime* zurück, der das aktuelle Datum und die Uhrzeit des Anwendungsservers darstellt. |
| [NullDate](er-functions-datetime-nulldate.md) | Diese Funktion gibt den Wert *Date* zurück, der das Datum **null** (01. Januar 1900) darstellt. |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Diese Funktion gibt den Wert *DateTime* zurück, der den Wert für Datum/Uhrzeit **null** (01. Januar 1900) in Koordinierter Weltzeit darstellt. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Diese Funktion gibt den Wert *DateTime* zurück, der das aktuelle Datum und die Uhrzeit der Anwendungssitzung darstellt. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Diese Funktion gibt den Wert *Date* zurück, der das aktuelle Anwendungssitzungsdatum darstellt. |
| [Heute](er-functions-datetime-today.md) | Diese Funktion gibt den Wert *Date* zurück, der das aktuelle Anwendungsserverdatum darstellt. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]