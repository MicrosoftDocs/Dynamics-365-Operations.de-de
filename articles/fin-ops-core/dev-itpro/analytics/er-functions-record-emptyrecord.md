---
title: EMPTYRECORD EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der EMPTYRECORD-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: e614c06b4cfad628bbd8a966719ed994ce05b792
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746530"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="d9a22-103">EMPTYRECORD EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="d9a22-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9a22-104">Die Funktion `EMPTYRECORD` gibt für *Container (Datensatz)* den Wert null zurück, der dieselbe Struktur wie die angegebene Datensatzliste oder der angegebene Datensatz besitzt.</span><span class="sxs-lookup"><span data-stu-id="d9a22-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a22-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9a22-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="d9a22-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="d9a22-106">Arguments</span></span>

<span data-ttu-id="d9a22-107">`list`: *Datensatzliste* oder *Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="d9a22-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="d9a22-108">Der gültige Pfad einer Datenquelle des Typs *Datensatzliste* oder *Container (Datensatz)*.</span><span class="sxs-lookup"><span data-stu-id="d9a22-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d9a22-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d9a22-109">Return values</span></span>

<span data-ttu-id="d9a22-110">*Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="d9a22-110">*Container (record)*</span></span>

<span data-ttu-id="d9a22-111">Der resultierende Datensatzwert.</span><span class="sxs-lookup"><span data-stu-id="d9a22-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d9a22-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="d9a22-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="d9a22-113">Ein Datensatz NULL ist ein Datensatz, in dem alle Felder einen leeren Wert haben.</span><span class="sxs-lookup"><span data-stu-id="d9a22-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="d9a22-114">Ein leerer Wert ist **0** (null) für Zahlen, eine leere Zeichenfolge für Zeichenfolgen usw.</span><span class="sxs-lookup"><span data-stu-id="d9a22-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="d9a22-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d9a22-115">Example</span></span>

<span data-ttu-id="d9a22-116">`EMPTYRECORD (SPLIT ("abc", 1))` gibt einen neuen leeren Datensatz zurück, der dieselbe Struktur wie die Liste hat, die durch die Funktion `SPLIT` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d9a22-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="d9a22-117">Weitere Informationen finden Sie unter [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="d9a22-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9a22-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d9a22-118">Additional resources</span></span>

[<span data-ttu-id="d9a22-119">Datensatzfunktionen</span><span class="sxs-lookup"><span data-stu-id="d9a22-119">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]