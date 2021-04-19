---
title: NULLDATE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der NULLDATE bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 6ac8da3f18c7793512685d52dd64a9bd55bfb8fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746842"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="837f9-103">NULLDATE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="837f9-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="837f9-104">Die Funktion `NULLDATE` gibt den Wert *Date* zurück, der das Datum **null** (01. Januar 1900) darstellt.</span><span class="sxs-lookup"><span data-stu-id="837f9-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="837f9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="837f9-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="837f9-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="837f9-106">Return values</span></span>

<span data-ttu-id="837f9-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="837f9-107">*Date*</span></span>

<span data-ttu-id="837f9-108">Der resultierende Datenwert.</span><span class="sxs-lookup"><span data-stu-id="837f9-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="837f9-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="837f9-109">Example 1</span></span>

<span data-ttu-id="837f9-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` gibt das Datum **null**, 01. Januar 1900, mit **"1900-01-01"** basierend auf dem angegebenen benutzerdefinierten Format zurück.</span><span class="sxs-lookup"><span data-stu-id="837f9-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="837f9-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="837f9-111">Example 2</span></span>

<span data-ttu-id="837f9-112">Der Ausdruck `IF( Invoice.DocumentDate = NULLDATE(), true, false)` gibt **True** zurück, wenn der Wert des Feldes **DocumentDate** dem Datum **null** entspricht.</span><span class="sxs-lookup"><span data-stu-id="837f9-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="837f9-113">In diesem Beispiel ist **Invoice** eine Datenquelle der elektronischen Berichterstellung (EB) des Typs **Finance/Tabellendatensätze** und bezieht sich auf die Tabelle „CustInvoiceJour“.</span><span class="sxs-lookup"><span data-stu-id="837f9-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="837f9-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="837f9-114">Additional resources</span></span>

[<span data-ttu-id="837f9-115">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="837f9-115">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]