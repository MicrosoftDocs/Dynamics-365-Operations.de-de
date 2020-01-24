---
title: Liste der EB-Funktionen in der logischen Kategorie
description: Dieses Thema enthält Informationen zu den logischen Funktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
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
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916636"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="97ad1-103">Liste der EB-Funktionen in der logischen Kategorie</span><span class="sxs-lookup"><span data-stu-id="97ad1-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97ad1-104">Logische elektronische Berichtsfunktionen (EB) können verwendet werden, um mit logischen Werten zu arbeiten und mehr als einen Vergleich in einem einzelnen Ausdruck durchzuführen oder mehrere Bedingungen zu testen.</span><span class="sxs-lookup"><span data-stu-id="97ad1-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="97ad1-105">Dieses Thema enthält eine Zusammenfassung dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="97ad1-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="97ad1-106">Liste der unterstützten Funktionen</span><span class="sxs-lookup"><span data-stu-id="97ad1-106">List of supported functions</span></span>

| <span data-ttu-id="97ad1-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="97ad1-107">Function</span></span> | <span data-ttu-id="97ad1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97ad1-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="97ad1-109">Und</span><span class="sxs-lookup"><span data-stu-id="97ad1-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="97ad1-110">Diese Funktion gibt den *booleschen* Wert **TRUE** zurück, wenn alle angegebenen Bedingungen wahr sind.</span><span class="sxs-lookup"><span data-stu-id="97ad1-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="97ad1-111">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="97ad1-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="97ad1-112">Behälter</span><span class="sxs-lookup"><span data-stu-id="97ad1-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="97ad1-113">Diese Funktion bewertet den Wert des angegebenen Ausdrucks anhand der angegebenen alternativen Optionen und gibt das Ergebnis der ersten Option zurück, die dem Wert des angegebenen Ausdrucks entspricht.</span><span class="sxs-lookup"><span data-stu-id="97ad1-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="97ad1-114">Andernfalls wird ein optionales Standardergebnis zurückgegeben, wenn als letztes Argument der aufgerufenen Funktion ein Standardergebnis angegeben wird, dem keine Option vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="97ad1-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="97ad1-115">Der zurückgegebene Wert kann ein Wert eines beliebigen unterstützten Datentyps sein.</span><span class="sxs-lookup"><span data-stu-id="97ad1-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="97ad1-116">Falls</span><span class="sxs-lookup"><span data-stu-id="97ad1-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="97ad1-117">Diese Funktion gibt den ersten angegebenen Wert zurück, wenn die angegebene Bedingung zutrifft.</span><span class="sxs-lookup"><span data-stu-id="97ad1-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="97ad1-118">Sie gibt andernfalls den zweiten angegebenen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="97ad1-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="97ad1-119">Der zurückgegebene Wert kann ein Wert eines beliebigen unterstützten Datentyps sein.</span><span class="sxs-lookup"><span data-stu-id="97ad1-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="97ad1-120">Nicht</span><span class="sxs-lookup"><span data-stu-id="97ad1-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="97ad1-121">Diese Funktion gibt den umgekehrten logischen Wert der angegebenen Bedingung als *booleschen* Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="97ad1-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="97ad1-122">Or</span><span class="sxs-lookup"><span data-stu-id="97ad1-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="97ad1-123">Diese Funktion gibt den *booleschen* Wert **FALSE** zurück, wenn alle angegebenen Bedingungen falsch sind.</span><span class="sxs-lookup"><span data-stu-id="97ad1-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="97ad1-124">Wenn eine der angegebenen Bedingungen wahr ist, gibt die Funktion den *booleschen* Wert **TRUE** zurück.</span><span class="sxs-lookup"><span data-stu-id="97ad1-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="97ad1-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="97ad1-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="97ad1-126">Diese Funktion bestimmt, ob die Eingabe mit einem angegebenen Wert eines angegebenen Artikels in der angegebenen Liste übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="97ad1-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="97ad1-127">Sie gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Eingabe mit dem Ergebnis der Ausführung des angegebenen Ausdrucks für mindestens einen Datensatz der entsprechenden Liste übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="97ad1-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="97ad1-128">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="97ad1-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="97ad1-129">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="97ad1-129">Additional resources</span></span>

[<span data-ttu-id="97ad1-130">Überblick über die elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="97ad1-130">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="97ad1-131">Formeldesigner in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="97ad1-131">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="97ad1-132">Formelsprache in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="97ad1-132">Electronic reporting formula language</span></span>](er-formula-language.md)
