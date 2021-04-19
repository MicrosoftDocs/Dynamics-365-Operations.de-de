---
title: Liste der EB-Funktionen in der Typenumrechnungskategorie
description: Dieses Thema enthält Informationen zu den Umrechnungsfunktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
author: NickSelin
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
ms.openlocfilehash: 199d51ae8a4dbdd7d2f3bd290a2b487ceb1174dc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752603"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="329df-103">Liste der EB-Funktionen in der Typenumrechnungskategorie</span><span class="sxs-lookup"><span data-stu-id="329df-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="329df-104">Konvertierungsfunktionen für EB-Typen (elektronische Berichterstellung) können zum Konvertieren von Werten zwischen Typen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="329df-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="329df-105">Dieses Thema enthält eine Zusammenfassung dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="329df-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="329df-106">Funktionen zur Typenumrechnung</span><span class="sxs-lookup"><span data-stu-id="329df-106">Type conversion functions</span></span>

| <span data-ttu-id="329df-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="329df-107">Function</span></span> | <span data-ttu-id="329df-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="329df-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="329df-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="329df-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="329df-110">Diese Funktion gibt den Wert *Int64* zurück, der die angegebene Zeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="329df-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="329df-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="329df-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="329df-112">Diese Funktion gibt den Wert *Int* zurück, der die angegebene Zeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="329df-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="329df-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="329df-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="329df-114">Diese Funktion gibt den Wert *Real* zurück, der über den angegebenen Wert *String* konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="329df-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="329df-115">Bei der Konvertierung werden die angegebenen Trennzeichen für Dezimal- und Zifferngruppierungen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="329df-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="329df-116">Wert</span><span class="sxs-lookup"><span data-stu-id="329df-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="329df-117">Diese Funktion gibt den Wert *Real* zurück, der über den angegebenen Wert *String* konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="329df-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-container-category"></a><span data-ttu-id="329df-118">Typenumrechnungsfunktionen in der Containerkategorie</span><span class="sxs-lookup"><span data-stu-id="329df-118">Type conversion functions in the container category</span></span>

<span data-ttu-id="329df-119">Die folgende Tabelle beschreibt die Typenumrechnungsfunktionen in der [Container](er-functions-category-container.md)-Kategorie.</span><span class="sxs-lookup"><span data-stu-id="329df-119">The following table describes the type conversion functions in the [container](er-functions-category-container.md) category.</span></span>

| <span data-ttu-id="329df-120">Funktion</span><span class="sxs-lookup"><span data-stu-id="329df-120">Function</span></span> | <span data-ttu-id="329df-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="329df-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="329df-122">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="329df-122">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="329df-123">Diese Funktion konvertiert die angegebene Eingabe des Datentyps *String* in ein Datenelement des Typs *Container*.</span><span class="sxs-lookup"><span data-stu-id="329df-123">This function converts the specified input of the *String* type to a data item of the *Container* type.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="329df-124">Typenumrechnungsfunktionen in der Kategorie „Datum und Uhrzeit“</span><span class="sxs-lookup"><span data-stu-id="329df-124">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="329df-125">Die folgende Tabelle beschreibt die Typenumrechnungsfunktionen in der [Kategorie „Datum und Uhrzeit“](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="329df-125">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="329df-126">Funktion</span><span class="sxs-lookup"><span data-stu-id="329df-126">Function</span></span> | <span data-ttu-id="329df-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="329df-127">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="329df-128">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="329df-128">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="329df-129">Diese Funktion gibt den Wert *DateTime* zurück, der über den vorgegebenen Wert *String* im speziellen Format und in der optional angegebenen Kultur in den Wert für Datum/Uhrzeit konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="329df-129">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="329df-130">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="329df-130">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="329df-131">Diese Funktion gibt den Wert *DateTime* zurück, der über den vorgegebenen Wert *Date* in einen Wert für Datum/Uhrzeit in der Koordinierten Weltzeit (Greenwich Mean Time \[GMT\]) konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="329df-131">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="329df-132">DateValue</span><span class="sxs-lookup"><span data-stu-id="329df-132">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="329df-133">Diese Funktion gibt den Wert *Date* zurück, der über den vorgegebenen Wert *String* im speziellen Format und in der optional angegebenen Kultur in den Wert für Datum konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="329df-133">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="329df-134">Typenumrechnungsfunktionen in der Listenkategorie</span><span class="sxs-lookup"><span data-stu-id="329df-134">Type conversion functions in the list category</span></span>

<span data-ttu-id="329df-135">Die folgende Tabelle beschreibt die Typenumrechnungsfunktionen in der [Listenkategorie](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="329df-135">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="329df-136">Funktion</span><span class="sxs-lookup"><span data-stu-id="329df-136">Function</span></span> | <span data-ttu-id="329df-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="329df-137">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="329df-138">Liste</span><span class="sxs-lookup"><span data-stu-id="329df-138">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="329df-139">Diese Funktion gibt den Wert *Datensatzliste* als neue Liste zurück, die anhand der angegebenen Argumente des Typs *Container (Datensatz)* erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="329df-139">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="329df-140">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="329df-140">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="329df-141">Diese Funktion gibt den Wert *Datensatzliste* zurück, der basierend auf der Struktur des angegebenen Arguments des Typs *Aufzählung* oder *Container (Datensatz)* erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="329df-141">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="329df-142">Teilen</span><span class="sxs-lookup"><span data-stu-id="329df-142">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="329df-143">Diese Funktion teilt den angegebenen Wert *String* in Teilzeichenfolgen auf und gibt das Ergebnis als neuen Wert *Datensatzliste* zurück.</span><span class="sxs-lookup"><span data-stu-id="329df-143">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="329df-144">StringJoin</span><span class="sxs-lookup"><span data-stu-id="329df-144">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="329df-145">Diese Funktion gibt den Wert *String* zurück, der aus verketteten Werten des angegebenen Feldes aus dem angegebenen Wert *Datensatzliste* besteht.</span><span class="sxs-lookup"><span data-stu-id="329df-145">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="329df-146">Die Werte können durch das angegebene Trennzeichen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="329df-146">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="329df-147">Typenumrechnungsfunktionen in der Textkategorie</span><span class="sxs-lookup"><span data-stu-id="329df-147">Type conversion functions in the text category</span></span>

<span data-ttu-id="329df-148">Die folgende Tabelle beschreibt die Typenumrechnungsfunktionen in der [Textkategorie](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="329df-148">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="329df-149">Funktion</span><span class="sxs-lookup"><span data-stu-id="329df-149">Function</span></span> | <span data-ttu-id="329df-150">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="329df-150">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="329df-151">Char</span><span class="sxs-lookup"><span data-stu-id="329df-151">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="329df-152">Diese Funktion gibt den Wert *String* zurück, der ein einzelnes Zeichen darstellt, auf das durch die angegebene Unicode-Nummer verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="329df-152">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="329df-153">GuidValue</span><span class="sxs-lookup"><span data-stu-id="329df-153">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="329df-154">Diese Funktion konvertiert die angegebene Eingabe des Datentyps *String* in ein Datenelement des Typs *GUID*.</span><span class="sxs-lookup"><span data-stu-id="329df-154">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="329df-155">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="329df-155">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="329df-156">Diese Funktion gibt den Wert *String* zurück, der eine angegebene Zahl im angegebenen Format und in einer optional angegebenen Kultur darstellt.</span><span class="sxs-lookup"><span data-stu-id="329df-156">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="329df-157">QrCode</span><span class="sxs-lookup"><span data-stu-id="329df-157">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="329df-158">Diese Funktion gibt den Wert *Container* zurück, der das QR-Code-Bild (Quick Response Code) für die angegebene Zeichenfolge im Binärformat darstellt.</span><span class="sxs-lookup"><span data-stu-id="329df-158">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="329df-159">Text</span><span class="sxs-lookup"><span data-stu-id="329df-159">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="329df-160">Diese Funktion gibt den Wert *String* zurück, der die angegebene Zahl darstellt, nachdem sie in eine Textzeichenfolge konvertiert wurde, die gemäß den Servergebietsschemaeinstellungen der aktuellen Anwendungsinstanz formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="329df-160">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="329df-161">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="329df-161">Additional resources</span></span>

[<span data-ttu-id="329df-162">Überblick über die elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="329df-162">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="329df-163">Formeldesigner in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="329df-163">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="329df-164">Formelsprache in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="329df-164">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]