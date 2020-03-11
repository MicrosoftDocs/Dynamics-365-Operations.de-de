---
title: FA_BALANCE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der FA_BALANCE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 76a087157ae53e2c571654ade7383d7bd7a005c3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041445"
---
# <span data-ttu-id="c4f52-103"><a name="FA_BALANCE">FA_BALANCE EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="c4f52-103"><a name="FA_BALANCE">FA_BALANCE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4f52-104">Die Funktion `FA_BALANCE` gibt den Wert *Container (Datensatz)* zurück, der aus Daten für den Anlagensaldo für die angegebene Anlagenposition, dem Wertmodellcode, dem Berichtsjahr und dem Berichtsdatum besteht.</span><span class="sxs-lookup"><span data-stu-id="c4f52-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4f52-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4f52-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="c4f52-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="c4f52-106">Arguments</span></span>

<span data-ttu-id="c4f52-107">`fixed asset code`: *String*</span><span class="sxs-lookup"><span data-stu-id="c4f52-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="c4f52-108">Der Wert *String*, der den Code eines Gegenstands des Anlagevermögens darstellt, für den der Saldo berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="c4f52-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="c4f52-109">`value model code`: *String*</span><span class="sxs-lookup"><span data-stu-id="c4f52-109">`value model code`: *String*</span></span>

<span data-ttu-id="c4f52-110">Der Wert *String*, der den Code eines Gegenstands des Wertmodells darstellt, für das der Saldo berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="c4f52-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="c4f52-111">`reporting year`: *Aufzählungswert*</span><span class="sxs-lookup"><span data-stu-id="c4f52-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="c4f52-112">Ein Aufzählungswert der Anwendungsaufzählung **AssetYear**, der einen Zeitraum für die Saldenberechnung definiert.</span><span class="sxs-lookup"><span data-stu-id="c4f52-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="c4f52-113">`reporting date`: *Date*</span><span class="sxs-lookup"><span data-stu-id="c4f52-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="c4f52-114">Der Wert *Date*, der ein Datum für die Saldenberechnung definiert.</span><span class="sxs-lookup"><span data-stu-id="c4f52-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="c4f52-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="c4f52-115">Return values</span></span>

<span data-ttu-id="c4f52-116">*Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="c4f52-116">*Container (record)*</span></span>

<span data-ttu-id="c4f52-117">Der resultierende Datensatzwert.</span><span class="sxs-lookup"><span data-stu-id="c4f52-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="c4f52-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c4f52-118">Example</span></span>

<span data-ttu-id="c4f52-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` gibt den vorbereiteten Datencontainer von Salden für Anlage **COMP-000001** zurück, der das Wertmodell **Current** zum aktuellen Anwendungs-Sitzungsdatum hat.</span><span class="sxs-lookup"><span data-stu-id="c4f52-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4f52-120">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c4f52-120">Additional resources</span></span>

[<span data-ttu-id="c4f52-121">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="c4f52-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
