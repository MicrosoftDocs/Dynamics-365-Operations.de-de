---
title: FORMATELEMENTNAME EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von FORMATELEMENTNAME bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 5f299a4bb697afce152a61ec35fcefab7157f356
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042526"
---
# <span data-ttu-id="ab7e8-103"><a name="FORMATELEMENTNAME">FORMATELEMENTNAME EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="ab7e8-103"><a name="FORMATELEMENTNAME">FORMATELEMENTNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab7e8-104">Die Funktion `FORMATELEMENTNAME` gibt den Wert *String* zurück, der den Namen des aktuellen Formatelements der elektronischen Berichterstattung (EB) darstellt.</span><span class="sxs-lookup"><span data-stu-id="ab7e8-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab7e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab7e8-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="ab7e8-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ab7e8-106">Return values</span></span>

<span data-ttu-id="ab7e8-107">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="ab7e8-107">*String*</span></span>

<span data-ttu-id="ab7e8-108">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="ab7e8-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ab7e8-109">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="ab7e8-109">Usage notes</span></span>

<span data-ttu-id="ab7e8-110">Diese Funktion kann in EB-Ausdrücken abgerufen werden, die für die Eigenschaften **Gesammelter Datenschlüsselname** und **Gesammelter Datenschlüsselwert** einer EB-Formatskomponente aus der Gruppe **Text** konfiguriert wurde, die sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ab7e8-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="ab7e8-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ab7e8-111">Example</span></span>

<span data-ttu-id="ab7e8-112">Um mehr darüber zu erfahren, wie diese Funktion verwendet wird, finden Sie Informationen im Aufgabenleitfaden [EB – Verwendung von Daten der Formatausgabe für Inventur und Summierungen](tasks/er-format-counting-summing-1.md), der Teil des Geschäftsprozesses **IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln** ist.</span><span class="sxs-lookup"><span data-stu-id="ab7e8-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab7e8-113">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ab7e8-113">Additional resources</span></span>

[<span data-ttu-id="ab7e8-114">Datensammlungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ab7e8-114">Data collection functions</span></span>](er-functions-category-data-collection.md)
