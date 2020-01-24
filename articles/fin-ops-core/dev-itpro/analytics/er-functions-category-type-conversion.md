---
title: Liste der EB-Funktionen in der Typenumrechnungskategorie
description: Dieses Thema enthält Informationen zu den Umrechnungsfunktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2cfa5deb3b2c00565759e4334a002bf112f888ac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917648"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="ee79f-103">Liste der EB-Funktionen in der Typenumrechnungskategorie</span><span class="sxs-lookup"><span data-stu-id="ee79f-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee79f-104">Konvertierungsfunktionen für EB-Typen (elektronische Berichterstellung) können zum Konvertieren von Werten zwischen Typen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee79f-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="ee79f-105">Dieses Thema enthält eine Zusammenfassung dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="ee79f-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="ee79f-106">Funktionen zur Typenumrechnung</span><span class="sxs-lookup"><span data-stu-id="ee79f-106">Type conversion functions</span></span>

| <span data-ttu-id="ee79f-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="ee79f-107">Function</span></span> | <span data-ttu-id="ee79f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee79f-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ee79f-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="ee79f-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="ee79f-110">Diese Funktion gibt den Wert *Int64* zurück, der die angegebene Zeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="ee79f-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="ee79f-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="ee79f-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="ee79f-112">Diese Funktion gibt den Wert *Int* zurück, der die angegebene Zeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="ee79f-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="ee79f-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="ee79f-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="ee79f-114">Diese Funktion gibt den Wert *Real* zurück, der über den angegebenen Wert *String* konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="ee79f-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="ee79f-115">Bei der Konvertierung werden die angegebenen Trennzeichen für Dezimal- und Zifferngruppierungen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ee79f-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="ee79f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ee79f-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="ee79f-117">Diese Funktion gibt den Wert *Real* zurück, der über den angegebenen Wert *String* konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="ee79f-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="ee79f-118">Typenumrechnungsfunktionen in der Kategorie „Datum und Uhrzeit“</span><span class="sxs-lookup"><span data-stu-id="ee79f-118">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="ee79f-119">Die folgende Tabelle beschreibt die Typenumrechnungsfunktionen in der [Kategorie „Datum und Uhrzeit“](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="ee79f-119">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="ee79f-120">Funktion</span><span class="sxs-lookup"><span data-stu-id="ee79f-120">Function</span></span> | <span data-ttu-id="ee79f-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee79f-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ee79f-122">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="ee79f-122">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="ee79f-123">Diese Funktion gibt den Wert *DateTime* zurück, der über den vorgegebenen Wert *String* im speziellen Format und in der optional angegebenen Kultur in den Wert für Datum/Uhrzeit konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="ee79f-123">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="ee79f-124">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="ee79f-124">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="ee79f-125">Diese Funktion gibt den Wert *DateTime* zurück, der über den vorgegebenen Wert *Date* in einen Wert für Datum/Uhrzeit in der Koordinierten Weltzeit (Greenwich Mean Time \[GMT\]) konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="ee79f-125">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="ee79f-126">DateValue</span><span class="sxs-lookup"><span data-stu-id="ee79f-126">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="ee79f-127">Diese Funktion gibt den Wert *Date* zurück, der über den vorgegebenen Wert *String* im speziellen Format und in der optional angegebenen Kultur in den Wert für Datum konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="ee79f-127">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="ee79f-128">Typenumrechnungsfunktionen in der Listenkategorie</span><span class="sxs-lookup"><span data-stu-id="ee79f-128">Type conversion functions in the list category</span></span>

<span data-ttu-id="ee79f-129">Die folgende Tabelle beschreibt die Typenumrechnungsfunktionen in der [Listenkategorie](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="ee79f-129">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="ee79f-130">Funktion</span><span class="sxs-lookup"><span data-stu-id="ee79f-130">Function</span></span> | <span data-ttu-id="ee79f-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee79f-131">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ee79f-132">Liste</span><span class="sxs-lookup"><span data-stu-id="ee79f-132">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="ee79f-133">Diese Funktion gibt den Wert *Datensatzliste* als neue Liste zurück, die anhand der angegebenen Argumente des Typs *Container (Datensatz)* erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ee79f-133">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="ee79f-134">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="ee79f-134">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="ee79f-135">Diese Funktion gibt den Wert *Datensatzliste* zurück, der basierend auf der Struktur des angegebenen Arguments des Typs *Aufzählung* oder *Container (Datensatz)* erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ee79f-135">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="ee79f-136">Teilen</span><span class="sxs-lookup"><span data-stu-id="ee79f-136">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="ee79f-137">Diese Funktion teilt den angegebenen Wert *String* in Teilzeichenfolgen auf und gibt das Ergebnis als neuen Wert *Datensatzliste* zurück.</span><span class="sxs-lookup"><span data-stu-id="ee79f-137">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="ee79f-138">StringJoin</span><span class="sxs-lookup"><span data-stu-id="ee79f-138">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="ee79f-139">Diese Funktion gibt den Wert *String* zurück, der aus verketteten Werten des angegebenen Feldes aus dem angegebenen Wert *Datensatzliste* besteht.</span><span class="sxs-lookup"><span data-stu-id="ee79f-139">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="ee79f-140">Die Werte können durch das angegebene Trennzeichen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="ee79f-140">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="ee79f-141">Typenumrechnungsfunktionen in der Textkategorie</span><span class="sxs-lookup"><span data-stu-id="ee79f-141">Type conversion functions in the text category</span></span>

<span data-ttu-id="ee79f-142">Die folgende Tabelle beschreibt die Typenumrechnungsfunktionen in der [Textkategorie](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="ee79f-142">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="ee79f-143">Funktion</span><span class="sxs-lookup"><span data-stu-id="ee79f-143">Function</span></span> | <span data-ttu-id="ee79f-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee79f-144">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ee79f-145">Char</span><span class="sxs-lookup"><span data-stu-id="ee79f-145">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="ee79f-146">Diese Funktion gibt den Wert *String* zurück, der ein einzelnes Zeichen darstellt, auf das durch die angegebene Unicode-Nummer verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ee79f-146">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="ee79f-147">GuidValue</span><span class="sxs-lookup"><span data-stu-id="ee79f-147">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="ee79f-148">Diese Funktion konvertiert die angegebene Eingabe des Datentyps *String* in ein Datenelement des Typs *GUID*.</span><span class="sxs-lookup"><span data-stu-id="ee79f-148">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="ee79f-149">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="ee79f-149">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="ee79f-150">Diese Funktion gibt den Wert *String* zurück, der eine angegebene Zahl im angegebenen Format und in einer optional angegebenen Kultur darstellt.</span><span class="sxs-lookup"><span data-stu-id="ee79f-150">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="ee79f-151">QrCode</span><span class="sxs-lookup"><span data-stu-id="ee79f-151">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="ee79f-152">Diese Funktion gibt den Wert *Container* zurück, der das QR-Code-Bild (Quick Response Code) für die angegebene Zeichenfolge im Binärformat darstellt.</span><span class="sxs-lookup"><span data-stu-id="ee79f-152">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="ee79f-153">Text</span><span class="sxs-lookup"><span data-stu-id="ee79f-153">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="ee79f-154">Diese Funktion gibt den Wert *String* zurück, der die angegebene Zahl darstellt, nachdem sie in eine Textzeichenfolge konvertiert wurde, die gemäß den Servergebietsschemaeinstellungen der aktuellen Anwendungsinstanz formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="ee79f-154">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="ee79f-155">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ee79f-155">Additional resources</span></span>

[<span data-ttu-id="ee79f-156">Überblick über die elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="ee79f-156">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="ee79f-157">Formeldesigner in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="ee79f-157">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="ee79f-158">Formelsprache in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="ee79f-158">Electronic reporting formula language</span></span>](er-formula-language.md)
