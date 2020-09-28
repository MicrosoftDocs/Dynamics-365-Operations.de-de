---
title: GETCURRENTCOMPANY EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der GETCURRENTCOMPANY-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 7e3c164c6d54d8387eed5018219da5fd82c765c8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744120"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="b5feb-103">GETCURRENTCOMPANY EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="b5feb-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5feb-104">Die Funktion `GETCURRENTCOMPANY` gibt den Wert *String* zurück, der den Code für die juristische Person (Unternehmen) darstellt, bei dem ein Benutzer derzeit angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="b5feb-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5feb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5feb-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="b5feb-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b5feb-106">Return values</span></span>

<span data-ttu-id="b5feb-107">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="b5feb-107">*String*</span></span>

<span data-ttu-id="b5feb-108">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="b5feb-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b5feb-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b5feb-109">Example</span></span>

<span data-ttu-id="b5feb-110">`GETCURRENTCOMPANY ()` gibt **USMF** für einen Benutzer zurück, der beim Unternehmen **Contoso Entertainment System USA** angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="b5feb-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5feb-111">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b5feb-111">Additional resources</span></span>

[<span data-ttu-id="b5feb-112">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="b5feb-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
