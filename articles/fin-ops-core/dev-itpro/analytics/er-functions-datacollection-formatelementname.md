---
title: FORMATELEMENTNAME EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von FORMATELEMENTNAME bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: f716fe779903b4e9142b7959d868256f2d84c624
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755227"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="be254-103">FORMATELEMENTNAME EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="be254-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be254-104">Die Funktion `FORMATELEMENTNAME` gibt den Wert *String* zurück, der den Namen des aktuellen Formatelements der elektronischen Berichterstattung (EB) darstellt.</span><span class="sxs-lookup"><span data-stu-id="be254-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="be254-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be254-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="be254-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="be254-106">Return values</span></span>

<span data-ttu-id="be254-107">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="be254-107">*String*</span></span>

<span data-ttu-id="be254-108">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="be254-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="be254-109">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="be254-109">Usage notes</span></span>

<span data-ttu-id="be254-110">Diese Funktion kann in EB-Ausdrücken abgerufen werden, die für die Eigenschaften **Gesammelter Datenschlüsselname** und **Gesammelter Datenschlüsselwert** einer EB-Formatskomponente aus der Gruppe **Text** konfiguriert wurde, die sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="be254-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="be254-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="be254-111">Example</span></span>

<span data-ttu-id="be254-112">Um mehr darüber zu erfahren, wie diese Funktion verwendet wird, finden Sie Informationen im Aufgabenleitfaden [EB – Verwendung von Daten der Formatausgabe für Inventur und Summierungen](tasks/er-format-counting-summing-1.md), der Teil des Geschäftsprozesses **IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln** ist.</span><span class="sxs-lookup"><span data-stu-id="be254-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be254-113">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="be254-113">Additional resources</span></span>

[<span data-ttu-id="be254-114">Datensammlungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="be254-114">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]