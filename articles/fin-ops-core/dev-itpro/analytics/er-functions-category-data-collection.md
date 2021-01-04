---
title: Liste der EB-Funktionen in der Datenerfassungskategorie
description: Dieses Thema enthält Informationen zu den Datenerfassungsfunktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 0ec6092f2992df91433bb8aaa4212fca2a0abf7c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686292"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="88221-103">Liste der EB-Funktionen in der Datenerfassungskategorie</span><span class="sxs-lookup"><span data-stu-id="88221-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88221-104">Datenerfassungsfunktionen für die elektronische Berichterstellung (EB) werden verwendet, um basierend auf den Daten der Ausgabe, die bereits im Format **Text** oder **Xml** generiert wurden, in einem EB-Format zu zählen und zu summieren, das gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88221-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="88221-105">Dieser Ansatz wird verwendet, um die Leistung eines ausgeführten EB-Formats zu verbessern, um Werte für laufende Summen in generierte Dokumente sowie für andere Zwecke einzugeben.</span><span class="sxs-lookup"><span data-stu-id="88221-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="88221-106">Dieses Thema enthält eine Zusammenfassung dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="88221-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="88221-107">Liste der unterstützten Funktionen</span><span class="sxs-lookup"><span data-stu-id="88221-107">List of supported functions</span></span>

| <span data-ttu-id="88221-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="88221-108">Function</span></span> | <span data-ttu-id="88221-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88221-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="88221-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="88221-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="88221-111">Diese Funktion gibt den Wert *Datensatzliste* zurück, der die Liste der Werte enthält, die von der Eigenschaft **Gesammelter Datenschlüsselwert** des Formatelements zurückgegeben und erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebenen Bedingungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="88221-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="88221-112">Jede Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="88221-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="88221-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="88221-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="88221-114">Diese Funktion gibt den Wert *Ganzzahl* zurück, der die Anzahl der Formatelemente darstellt, die erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebene Bedingung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="88221-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="88221-115">Die Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="88221-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="88221-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="88221-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="88221-117">Diese Funktion gibt den Wert *Ganzzahl* zurück, der die Anzahl der Formatelemente darstellt, die erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebenen Bedingungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="88221-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="88221-118">Jede Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="88221-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="88221-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="88221-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="88221-120">Diese Funktion gibt den Wert *String* zurück, der den Namen des aktuellen EB-Formatelements darstellt.</span><span class="sxs-lookup"><span data-stu-id="88221-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="88221-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="88221-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="88221-122">Diese Funktion gibt den Wert *Real* zurück, der die Summe der Werte darstellt, die bei Bindungen der Formatelemente zurückgegeben und erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebene Bedingung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="88221-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="88221-123">Die Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="88221-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="88221-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="88221-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="88221-125">Diese Funktion gibt den Wert *Real* zurück, der die Summe der Werte darstellt, die bei Bindungen der Formatelemente zurückgegeben und erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebenen Bedingungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="88221-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="88221-126">Jede Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="88221-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="88221-127">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="88221-127">Additional resources</span></span>

[<span data-ttu-id="88221-128">Überblick über die elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="88221-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="88221-129">Formeldesigner in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="88221-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="88221-130">Formelsprache in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="88221-130">Electronic reporting formula language</span></span>](er-formula-language.md)
