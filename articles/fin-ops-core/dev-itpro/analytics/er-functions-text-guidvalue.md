---
title: GUIDVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der GUIDVALUE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: eb6f301cf7a39208aa23337401a9684fb5b3a73d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685953"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="bcac6-103">GUIDVALUE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="bcac6-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcac6-104">Die Funktion `GUIDVALUE` konvertiert die angegebene Eingabe des Datentyps *String* in ein Datenelement des Typs *GUID*.</span><span class="sxs-lookup"><span data-stu-id="bcac6-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcac6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcac6-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="bcac6-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="bcac6-106">Arguments</span></span>

<span data-ttu-id="bcac6-107">`input`: *String*</span><span class="sxs-lookup"><span data-stu-id="bcac6-107">`input`: *String*</span></span>

<span data-ttu-id="bcac6-108">Der gültige Pfad einer Datenquelle des Typs *String*.</span><span class="sxs-lookup"><span data-stu-id="bcac6-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="bcac6-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="bcac6-109">Return values</span></span>

<span data-ttu-id="bcac6-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="bcac6-110">*GUID*</span></span>

<span data-ttu-id="bcac6-111">Der resultierende GUID-Wert (Globally Unique Identifier).</span><span class="sxs-lookup"><span data-stu-id="bcac6-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bcac6-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="bcac6-112">Usage notes</span></span>

<span data-ttu-id="bcac6-113">Um eine Umwandlung in der entgegengesetzten Richtung auszuführen (das heißt, die angegebene Eingabe des Datentyps *GUID* in ein Datenelement des Datentyps *String* zu konvertieren), können Sie die Funktion [TEXT()](er-functions-text-text.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="bcac6-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="bcac6-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bcac6-114">Example</span></span>

<span data-ttu-id="bcac6-115">Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:</span><span class="sxs-lookup"><span data-stu-id="bcac6-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="bcac6-116">Die Datenquelle **myID** des Typs *Berechnetes Feld*, die den Ausdruck `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")` enthält</span><span class="sxs-lookup"><span data-stu-id="bcac6-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="bcac6-117">Die Datenquelle **Benutzer** des Typs *Tabellendatensätze*, der auf die UserInfo-Tabelle verweist</span><span class="sxs-lookup"><span data-stu-id="bcac6-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="bcac6-118">Sie können dann einen Ausdruck wie `FILTER (Users, Users.objectId = myID)` verwenden, um die UserInfo-Tabelle nach dem Feld **objectID** des Datentyps *GUID* zu filtern.</span><span class="sxs-lookup"><span data-stu-id="bcac6-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bcac6-119">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bcac6-119">Additional resources</span></span>

[<span data-ttu-id="bcac6-120">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="bcac6-120">Text functions</span></span>](er-functions-category-text.md)
