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
ms.openlocfilehash: 0907cb8cb4bc1e90b9fb59eccedb699a894b5cc9
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916015"
---
# <span data-ttu-id="1ea49-103"><a name="FA_BALANCE">FA_BALANCE EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="1ea49-103"><a name="FA_BALANCE">FA_BALANCE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ea49-104">Die Funktion `FA_BALANCE` gibt den Wert *Container (Datensatz)* zurück, der aus Daten für den Anlagensaldo für die angegebene Anlagenposition, dem Wertmodellcode, dem Berichtsjahr und dem Berichtsdatum besteht.</span><span class="sxs-lookup"><span data-stu-id="1ea49-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ea49-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ea49-105">Syntax</span></span>

```
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="1ea49-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="1ea49-106">Arguments</span></span>

<span data-ttu-id="1ea49-107">`fixed asset code`: *String*</span><span class="sxs-lookup"><span data-stu-id="1ea49-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="1ea49-108">Der Wert *String*, der den Code eines Gegenstands des Anlagevermögens darstellt, für den der Saldo berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="1ea49-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="1ea49-109">`value model code`: *String*</span><span class="sxs-lookup"><span data-stu-id="1ea49-109">`value model code`: *String*</span></span>

<span data-ttu-id="1ea49-110">Der Wert *String*, der den Code eines Gegenstands des Wertmodells darstellt, für das der Saldo berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="1ea49-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="1ea49-111">`reporting year`: *Aufzählungswert*</span><span class="sxs-lookup"><span data-stu-id="1ea49-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="1ea49-112">Ein Aufzählungswert der Anwendungsaufzählung **AssetYear**, der einen Zeitraum für die Saldenberechnung definiert.</span><span class="sxs-lookup"><span data-stu-id="1ea49-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="1ea49-113">`reporting date`: *Date*</span><span class="sxs-lookup"><span data-stu-id="1ea49-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="1ea49-114">Der Wert *Date*, der ein Datum für die Saldenberechnung definiert.</span><span class="sxs-lookup"><span data-stu-id="1ea49-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="1ea49-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1ea49-115">Return values</span></span>

<span data-ttu-id="1ea49-116">*Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="1ea49-116">*Container (record)*</span></span>

<span data-ttu-id="1ea49-117">Der resultierende Datensatzwert.</span><span class="sxs-lookup"><span data-stu-id="1ea49-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="1ea49-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1ea49-118">Example</span></span>

<span data-ttu-id="1ea49-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` gibt den vorbereiteten Datencontainer von Salden für Anlage **COMP-000001** zurück, der das Wertmodell **Current** zum aktuellen Anwendungs-Sitzungsdatum hat.</span><span class="sxs-lookup"><span data-stu-id="1ea49-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ea49-120">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1ea49-120">Additional resources</span></span>

[<span data-ttu-id="1ea49-121">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="1ea49-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)