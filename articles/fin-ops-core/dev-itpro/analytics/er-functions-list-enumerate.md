---
title: ENUMERATE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ENUMERATE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 34ebbec94644276be4ef9beb1c77638606dd37a0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679461"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="f9798-103">ENUMERATE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="f9798-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9798-104">Die Funktion `ENUMERATE` gibt einen neuen Wert von *Datensatzliste* zurück, der aus Aufzählungsdatensätzen der angegebenen Liste besteht.</span><span class="sxs-lookup"><span data-stu-id="f9798-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9798-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9798-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="f9798-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="f9798-106">Arguments</span></span>

<span data-ttu-id="f9798-107">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="f9798-107">`list`: *Record list*</span></span>

<span data-ttu-id="f9798-108">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="f9798-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f9798-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f9798-109">Return values</span></span>

<span data-ttu-id="f9798-110">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="f9798-110">*Record list*</span></span>

<span data-ttu-id="f9798-111">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="f9798-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f9798-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="f9798-112">Usage notes</span></span>

<span data-ttu-id="f9798-113">Die Liste der zurückgegebenen Aufzählungsdatensätze enthält die folgenden zusätzlichen Elemente:</span><span class="sxs-lookup"><span data-stu-id="f9798-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="f9798-114">Den Datensatz der Felder (Komponente **Wert**)</span><span class="sxs-lookup"><span data-stu-id="f9798-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="f9798-115">Der Index des aktuellen Datensatzes (**Nummer** komponente)</span><span class="sxs-lookup"><span data-stu-id="f9798-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="f9798-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f9798-116">Example</span></span>

<span data-ttu-id="f9798-117">In der folgenden Abbildung wird eine Datenquelle **Aufgezählt** als Aufzählungsliste von Lieferantendatensätzen von der Datenquelle **Lieferanten** erstellt, die sich auf die Tabelle „VendTable” bezieht.</span><span class="sxs-lookup"><span data-stu-id="f9798-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="f9798-118">Die folgende Abbildung zeigt das Format der elektronischen Berichterstattung.</span><span class="sxs-lookup"><span data-stu-id="f9798-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="f9798-119">In diesem Format werden Datenbindungen erstellt, um eine Ausgabe im XML-Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="f9798-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="f9798-120">In dieser Ausgabe werden einzelne Lieferanten als aufgezählte Knoten präsentiert.</span><span class="sxs-lookup"><span data-stu-id="f9798-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="f9798-121">Die folgende Abbildung zeigt das Ergebnis, wenn das entworfene Format ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9798-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="f9798-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f9798-122">Additional resources</span></span>

[<span data-ttu-id="f9798-123">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="f9798-123">List functions</span></span>](er-functions-category-list.md)
