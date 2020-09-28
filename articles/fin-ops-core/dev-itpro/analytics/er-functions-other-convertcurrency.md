---
title: CONVERTCURRENCY EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CONVERTCURRENCY-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: ae6e0069c6e9227d4cf1045eeebbb825a2f943c3
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744310"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="3ea22-103">CONVERTCURRENCY EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="3ea22-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ea22-104">Die Funktion `CONVERTCURRENCY` gibt den Wert *Real* zurück, der das Konvertieren des angegebenen Geldbetrags aus der angegebenen Ausgangswährung in die angegebene Zielwährung darstellt, indem die Einstellungen des angegebenen Unternehmens am angegebenen Datum verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ea22-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ea22-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ea22-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="3ea22-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="3ea22-106">Arguments</span></span>

<span data-ttu-id="3ea22-107">`amount`: *Integer* oder *Real*</span><span class="sxs-lookup"><span data-stu-id="3ea22-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="3ea22-108">Ein numerischer Wert, der den umzurechnenden Geldbetrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="3ea22-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="3ea22-109">`source currency`: *String*</span><span class="sxs-lookup"><span data-stu-id="3ea22-109">`source currency`: *String*</span></span>

<span data-ttu-id="3ea22-110">Der Code der Ausgangswährung.</span><span class="sxs-lookup"><span data-stu-id="3ea22-110">The code of the source currency.</span></span>

<span data-ttu-id="3ea22-111">`target currency`: *String*</span><span class="sxs-lookup"><span data-stu-id="3ea22-111">`target currency`: *String*</span></span>

<span data-ttu-id="3ea22-112">Der Code der Zielwährung.</span><span class="sxs-lookup"><span data-stu-id="3ea22-112">The code of the target currency.</span></span>

<span data-ttu-id="3ea22-113">`date`: *Date*</span><span class="sxs-lookup"><span data-stu-id="3ea22-113">`date`: *Date*</span></span>

<span data-ttu-id="3ea22-114">Der Wert *Datum*, der das Datum darstellt, mit dem der Wechselkurs für die Konvertierung bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="3ea22-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="3ea22-115">`company`: *String*</span><span class="sxs-lookup"><span data-stu-id="3ea22-115">`company`: *String*</span></span>

<span data-ttu-id="3ea22-116">Der Wert *String*, der den Code einer Firma darstellt, die die für die Konvertierung verwendeten Einstellungen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3ea22-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="3ea22-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="3ea22-117">Return values</span></span>

<span data-ttu-id="3ea22-118">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="3ea22-118">*Real*</span></span>

<span data-ttu-id="3ea22-119">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="3ea22-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="3ea22-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3ea22-120">Example</span></span>

<span data-ttu-id="3ea22-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` gibt die Entsprechung von einem Euro in US Dollar am Datum der aktuellen Sitzung basierend auf den Einstellungen für das **DEMF**-Unternehmen zurück.</span><span class="sxs-lookup"><span data-stu-id="3ea22-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ea22-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3ea22-122">Additional resources</span></span>

[<span data-ttu-id="3ea22-123">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="3ea22-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
