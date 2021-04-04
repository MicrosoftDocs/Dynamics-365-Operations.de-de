---
title: TEXT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der TEXT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 5da7375020be827f432ba97740da37abe48962fc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560060"
---
# <a name="text-er-function"></a><span data-ttu-id="9a233-103">TEXT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="9a233-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a233-104">Die Funktion `TEXT` gibt die angegebene Zahl mit dem Wert *String* zurück, nachdem sie in eine Textzeichenfolge konvertiert wurde, die gemäß den Servergebietsschemaeinstellungen der aktuellen Anwendungsinstanz formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="9a233-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a233-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a233-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="9a233-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="9a233-106">Arguments</span></span>

<span data-ttu-id="9a233-107">`number`: *Integer* oder *Real*</span><span class="sxs-lookup"><span data-stu-id="9a233-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="9a233-108">Eine Zahl, die in eine Textzeichenfolge konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="9a233-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="9a233-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="9a233-109">Return values</span></span>

<span data-ttu-id="9a233-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="9a233-110">*String*</span></span>

<span data-ttu-id="9a233-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="9a233-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9a233-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="9a233-112">Usage notes</span></span>

<span data-ttu-id="9a233-113">Für Werte für den Typ *Real* wird die Zeichenkonvertierung auf zwei Dezimalstellen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="9a233-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="9a233-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9a233-114">Example</span></span>

<span data-ttu-id="9a233-115">Wenn das Servergebietsschema der Microsoft Dynamics 365 Finance-Instanz als **EN-US** definiert wird, gibt `TEXT (NOW ())` das aktuelle Finance-Sitzungsdatum, 17. Dezember 2015, als Textzeichenfolge **"12/17/2015 07:59:23 AM"** zurück.</span><span class="sxs-lookup"><span data-stu-id="9a233-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="9a233-116">`TEXT (1/3)` gibt **"0.33"** zurück.</span><span class="sxs-lookup"><span data-stu-id="9a233-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a233-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9a233-117">Additional resources</span></span>

[<span data-ttu-id="9a233-118">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="9a233-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]