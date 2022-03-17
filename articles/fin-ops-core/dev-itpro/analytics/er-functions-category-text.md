---
title: Liste der EB-Funktionen in der Textkategorie
description: Dieses Thema enthält Informationen zu den Textfunktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: 5d185c128de1120e93d1779db04a7666ba557707
ms.sourcegitcommit: 753714ac0dabc4b7ce91509757cd19f7be4a4793
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/01/2022
ms.locfileid: "8367766"
---
# <a name="list-of-er-functions-of-the-text-category"></a>Liste der EB-Funktionen in der Textkategorie

[!include [banner](../includes/banner.md)]

Mithilfe der Textfunktionen für die elektronische Berichterstellung (EB) können Informationen aus den Datenquellen des Datentyps *String* zum Durchführen von Operationen an diesen verwendet werden. Dieses Thema enthält eine Zusammenfassung dieser Funktionen.

## <a name="list-of-supported-functions"></a>Liste der unterstützten Funktionen

| Funktion | Beschreibung |
|----------|-------------|
| [Char](er-functions-text-char.md) | Diese Funktion gibt den Wert *String* zurück, der ein einzelnes Zeichen darstellt, auf das durch die angegebene Unicode-Nummer verwiesen wird. |
| [Verketten](er-functions-text-concatenate.md) | Diese Funktion gibt alle angegebenen Textzeichenfolgen mit dem Wert *String* zurück, nachdem sie zu einer Zeichenfolge zusammengefügt wurden. |
| [Format](er-functions-text-format.md) | Diese Funktion gibt den angegebenen Zeichenfolgenwert *String* zurück, nachdem sie durch Ersetzen sämtlicher Vorkommnisse von **%N** durch das *N*. Argument formatiert wurde. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Diese Funktion sucht nach dem bestimmten Wert *Enum* in der angegebenen Aufzählungsdatenquelle unter Verwendung des Aufzählungsnamens, der mit dem Wert *String* angegeben ist. Wenn der Wert *Enum* gefunden wird, gibt die Funktion ihn zurück. |
| [GetLabelText](er-functions-text-getlabeltext.md) | Diese Funktion sucht nach einem bestimmten Label und gibt einen *[String](er-formula-supported-data-types-primitive.md#string)*-Wert zurück, der die Übersetzung des angegebenen Labels in der angegebenen Sprache darstellt. |
| [GuidValue](er-functions-text-guidvalue.md) | Diese Funktion konvertiert die angegebene Eingabe des Datentyps *String* in ein Datenelement des Typs *GUID*. |
| [JsonValue](er-functions-text-jsonvalue.md) | Diese Funktion analysiert Daten im JavaScript Object Notation (JSON)-Format, auf die über den angegebenen Pfad zugegriffen wird, und sie extrahiert einen Skalarwert, der auf der angegebenen ID basiert. Anschließend wird der extrahierte Skalarwert als Wert *String* zurückgegeben. |
| [NACH-LINKS-TASTE](er-functions-text-left.md) | Diese Funktion gibt den Wert *String* zurück, der die angegebene Anzahl von Zeichen ab dem Anfang der angegebenen Zeichenfolge angibt. |
| [Len](er-functions-text-len.md) | Diese Funktion gibt den Wert *Integer* zurück, der die angegebene Anzahl von Zeichen in der angegebenen Zeichenfolge angibt. |
| [Lower](er-functions-text-lower.md) | Diese Funktion gibt die angegebene Textzeichenfolge mit dem Wert *String* zurück, nachdem er in Kleinbuchstaben umgewandelt wurde. |
| [Mid](er-functions-text-mid.md) | Diese Funktion gibt den Wert *[String](er-formula-supported-data-types-primitive.md#string)* zurück, der die angegebene Anzahl von Zeichen ab der angegebenen Zeichenfolge angibt, wobei an der angegebenen Position gestartet wird. |
| [NewGUID](er-functions-text-newguid.md) | Diese Funktion gibt einen neu generierten *[ GUID](er-formula-supported-data-types-primitive.md#guid)*-Wert zurück. |
| [NumberFormat](er-functions-text-numberformat.md) | Diese Funktion gibt den Wert *String* zurück, der eine angegebene Zahl im angegebenen Format und in einer optional angegebenen Kultur darstellt. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Diese Funktion gibt die angegebene Zahl mit dem Wert *String* zurück, nachdem er in der angegebenen Sprache geschrieben (d. h. in Textzeichenfolgen konvertiert) wurde. |
| [PadLeft](er-functions-text-padleft.md) | Diese Funktion gibt den Wert *String* mit der angegebenen Länge zurück, bei der der Anfang der angegebenen Zeichenfolge mit einer oder mehrerer Instanzen des angegebenen Zeichens aufgefüllt ist. |
| [QrCode](er-functions-text-qrcode.md) | Diese Funktion gibt den Wert *Container* zurück, der das QR-Code-Bild (Quick Response Code) für die angegebene Zeichenfolge im Binärformat darstellt. |
| [Ersetzen](er-functions-text-replace.md) | Diese Funktion gibt die angegebene Textzeichenfolge mit dem Wert *String* zurück, nachdem er ganz oder teilweise durch eine andere Zeichenfolge ersetzt wurde. |
| [NACH-RECHTS-TASTE](er-functions-text-right.md) | Diese Funktion gibt den Wert *String* zurück, der die angegebene Anzahl von Zeichen ab dem Ende der angegebenen Zeichenfolge angibt. |
| [Text](er-functions-text-text.md) | Diese Funktion gibt die angegebene Zahl mit dem Wert *String* zurück, nachdem sie in eine Textzeichenfolge konvertiert wurde, die gemäß den Servergebietsschemaeinstellungen der aktuellen Anwendungsinstanz formatiert ist. |
| [Übersetzen](er-functions-text-translate.md) | Diese Funktion gibt einen *Zeichenfolgen* Wert zurück, der das Ergebnis der Ersetzung des angegebenen Textes in Zeichen für einen anderen bereitgestellten Zeichensatz enthält. |
| [Trim](er-functions-text-trim.md) | Diese Funktion gibt die angegebene Textzeichenfolge als *String* zurück, nachdem Tabulator-, Wagenrücklauf-, Zeilenvorschub- und Formularvorschubzeichen durch ein einzelnes Leerzeichen ersetzt wurden, nachdem führende und nachfolgende Leerzeichen abgeschnitten wurden und nachdem mehrere Leerzeichen zwischen Wörtern entfernt wurden. |
| [Upper](er-functions-text-upper.md) | Diese Funktion gibt die angegebene Textzeichenfolge mit dem Wert *String* zurück, nachdem er in Großbuchstaben umgewandelt wurde. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
