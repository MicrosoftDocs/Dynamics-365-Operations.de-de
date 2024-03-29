---
title: Liste der EB-Funktionen in der Typenumrechnungskategorie
description: Dieser Artikel enthält Informationen zu den Umrechnungsfunktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
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
ms.openlocfilehash: 00fe8c5bce40a59580509a719212f163238815be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292615"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>Liste der EB-Funktionen in der Typenumrechnungskategorie

[!include [banner](../includes/banner.md)]

Konvertierungsfunktionen für EB-Typen (elektronische Berichterstellung) können zum Konvertieren von Werten zwischen Typen verwendet werden. Dieser Artikel enthält eine Zusammenfassung dieser Funktionen.

## <a name="type-conversion-functions"></a>Funktionen zur Typenumrechnung

| Funktion | Beschreibung |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | Diese Funktion gibt den Wert *Int64* zurück, der die angegebene Zeichenfolge darstellt. |
| [IntValue](er-functions-conversion-intvalue.md)       | Diese Funktion gibt den Wert *Int* zurück, der die angegebene Zeichenfolge darstellt. |
| [NumberValue](er-functions-conversion-numbervalue.md) | Diese Funktion gibt den Wert *Real* zurück, der über den angegebenen Wert *String* konvertiert wird. Bei der Konvertierung werden die angegebenen Trennzeichen für Dezimal- und Zifferngruppierungen berücksichtigt. |
| [Wert](er-functions-conversion-value.md)             | Diese Funktion gibt den Wert *Real* zurück, der über den angegebenen Wert *String* konvertiert wird. |

## <a name="type-conversion-functions-in-the-container-category"></a>Typenumrechnungsfunktionen in der Containerkategorie

Die folgende Tabelle beschreibt die Typenumrechnungsfunktionen in der [Container](er-functions-category-container.md)-Kategorie.

| Funktion | Beschreibung |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Diese Funktion konvertiert die angegebene Eingabe des Datentyps *String* in ein Datenelement des Typs *Container*. |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>Typenumrechnungsfunktionen in der Kategorie „Datum und Uhrzeit“

Die folgende Tabelle beschreibt die Typenumrechnungsfunktionen in der [Kategorie „Datum und Uhrzeit“](er-functions-category-datetime.md).

| Funktion | Beschreibung |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | Diese Funktion gibt den Wert *DateTime* zurück, der über den vorgegebenen Wert *String* im speziellen Format und in der optional angegebenen Kultur in den Wert für Datum/Uhrzeit konvertiert wird. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Diese Funktion gibt den Wert *DateTime* zurück, der über den vorgegebenen Wert *Date* in einen Wert für Datum/Uhrzeit in der Koordinierten Weltzeit (Greenwich Mean Time \[GMT\]) konvertiert wird. |
| [DateValue](er-functions-datetime-datevalue.md)           | Diese Funktion gibt den Wert *Date* zurück, der über den vorgegebenen Wert *String* im speziellen Format und in der optional angegebenen Kultur in den Wert für Datum konvertiert wird. |

## <a name="type-conversion-functions-in-the-list-category"></a>Typenumrechnungsfunktionen in der Listenkategorie

Die folgende Tabelle beschreibt die Typenumrechnungsfunktionen in der [Listenkategorie](er-functions-category-list.md).

| Funktion | Beschreibung |
|----------|-------------|
| [Liste](er-functions-list-list.md)                 | Diese Funktion gibt den Wert *Datensatzliste* als neue Liste zurück, die anhand der angegebenen Argumente des Typs *Container (Datensatz)* erstellt wird. |
| [ListOfFields](er-functions-list-listoffields.md) | Diese Funktion gibt den Wert *Datensatzliste* zurück, der basierend auf der Struktur des angegebenen Arguments des Typs *Aufzählung* oder *Container (Datensatz)* erstellt wird. |
| [Teilen](er-functions-list-split.md)               | Diese Funktion teilt den angegebenen Wert *String* in Teilzeichenfolgen auf und gibt das Ergebnis als neuen Wert *Datensatzliste* zurück. |
| [StringJoin](er-functions-list-stringjoin.md)     | Diese Funktion gibt den Wert *String* zurück, der aus verketteten Werten des angegebenen Feldes aus dem angegebenen Wert *Datensatzliste* besteht. Die Werte können durch das angegebene Trennzeichen getrennt werden. |

## <a name="type-conversion-functions-in-the-text-category"></a>Typenumrechnungsfunktionen in der Textkategorie

Die folgende Tabelle beschreibt die Typenumrechnungsfunktionen in der [Textkategorie](er-functions-category-text.md).

| Funktion | Beschreibung |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | Diese Funktion gibt den Wert *String* zurück, der ein einzelnes Zeichen darstellt, auf das durch die angegebene Unicode-Nummer verwiesen wird. |
| [GuidValue](er-functions-text-guidvalue.md)       | Diese Funktion konvertiert die angegebene Eingabe des Datentyps *String* in ein Datenelement des Typs *GUID*. |
| [NumberFormat](er-functions-text-numberformat.md) | Diese Funktion gibt den Wert *String* zurück, der eine angegebene Zahl im angegebenen Format und in einer optional angegebenen Kultur darstellt. |
| [QrCode](er-functions-text-qrcode.md)             | Diese Funktion gibt den Wert *Container* zurück, der das QR-Code-Bild (Quick Response Code) für die angegebene Zeichenfolge im Binärformat darstellt. |
| [Text](er-functions-text-text.md)                 | Diese Funktion gibt den Wert *String* zurück, der die angegebene Zahl darstellt, nachdem sie in eine Textzeichenfolge konvertiert wurde, die gemäß den Servergebietsschemaeinstellungen der aktuellen Anwendungsinstanz formatiert ist. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
