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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a27fd30236a61576ab9063010ea6bc38d9cf7a1e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686785"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="93817-103">CONVERTCURRENCY EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="93817-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93817-104">Die Funktion `CONVERTCURRENCY` gibt den Wert *Real* zurück, der das Konvertieren des angegebenen Geldbetrags aus der angegebenen Ausgangswährung in die angegebene Zielwährung darstellt, indem die Einstellungen des angegebenen Unternehmens am angegebenen Datum verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93817-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="93817-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="93817-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="93817-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="93817-106">Arguments</span></span>

<span data-ttu-id="93817-107">`amount`: *Integer* oder *Real*</span><span class="sxs-lookup"><span data-stu-id="93817-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="93817-108">Ein numerischer Wert, der den umzurechnenden Geldbetrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="93817-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="93817-109">`source currency`: *String*</span><span class="sxs-lookup"><span data-stu-id="93817-109">`source currency`: *String*</span></span>

<span data-ttu-id="93817-110">Der Code der Ausgangswährung.</span><span class="sxs-lookup"><span data-stu-id="93817-110">The code of the source currency.</span></span>

<span data-ttu-id="93817-111">`target currency`: *String*</span><span class="sxs-lookup"><span data-stu-id="93817-111">`target currency`: *String*</span></span>

<span data-ttu-id="93817-112">Der Code der Zielwährung.</span><span class="sxs-lookup"><span data-stu-id="93817-112">The code of the target currency.</span></span>

<span data-ttu-id="93817-113">`date`: *Date*</span><span class="sxs-lookup"><span data-stu-id="93817-113">`date`: *Date*</span></span>

<span data-ttu-id="93817-114">Der Wert *Datum*, der das Datum darstellt, mit dem der Wechselkurs für die Konvertierung bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="93817-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="93817-115">`company`: *String*</span><span class="sxs-lookup"><span data-stu-id="93817-115">`company`: *String*</span></span>

<span data-ttu-id="93817-116">Der Wert *String*, der den Code einer Firma darstellt, die die für die Konvertierung verwendeten Einstellungen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="93817-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="93817-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="93817-117">Return values</span></span>

<span data-ttu-id="93817-118">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="93817-118">*Real*</span></span>

<span data-ttu-id="93817-119">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="93817-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="93817-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="93817-120">Example</span></span>

<span data-ttu-id="93817-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` gibt die Entsprechung von einem Euro in US Dollar am Datum der aktuellen Sitzung basierend auf den Einstellungen für das **DEMF**-Unternehmen zurück.</span><span class="sxs-lookup"><span data-stu-id="93817-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93817-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="93817-122">Additional resources</span></span>

[<span data-ttu-id="93817-123">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="93817-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
