---
title: ALLITEMS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von ALLITEMS bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47113d52e15d3d61f00b3c54229e286eb0f1a8d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745392"
---
# <a name="allitems-er-function"></a><span data-ttu-id="6ab7c-103">ALLITEMS EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="6ab7c-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ab7c-104">Die Funktion `ALLITEMS` führt eine speicherinterne Auswahl durch und gibt einen neuen vereinfachten Wert *Datensatzliste* als Liste der Datensätze zurück, die alle Elemente darstellen, die dem angegebenen Pfad entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ab7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ab7c-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="6ab7c-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="6ab7c-106">Arguments</span></span>

<span data-ttu-id="6ab7c-107">`path`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="6ab7c-107">`path`: *Record list*</span></span>

<span data-ttu-id="6ab7c-108">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="6ab7c-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="6ab7c-109">Return values</span></span>

<span data-ttu-id="6ab7c-110">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="6ab7c-110">*Record list*</span></span>

<span data-ttu-id="6ab7c-111">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6ab7c-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="6ab7c-112">Usage notes</span></span>

<span data-ttu-id="6ab7c-113">Der Pfad muss als gültiger Datenquellenpfad eines Datenquellenelements eines *Datensatzlisten*-Datentyps definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="6ab7c-114">Datenelemente, wie beispielsweise die Pfadzeichenfolge und Datum, sollten ein Fehler im Ausdrucksgenerator der elektronischen Berichterstellung (EB) zur Entwurfszeit erzeugen.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="6ab7c-115">Es wird nicht empfohlen, diese Funktion für Transaktionsdatenquellen zu verwenden, die möglicherweise ein großes Datenvolumen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="6ab7c-116">Verwenden Sie stattdessen die Funktion [ALLTEMSQUERY ](er-functions-list-allitemsquery.md).</span><span class="sxs-lookup"><span data-stu-id="6ab7c-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="6ab7c-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6ab7c-117">Example 1</span></span>

<span data-ttu-id="6ab7c-118">Wenn Sie `SPLIT("abcdef" , 2)` als Datenquelle **DS** eingeben, gibt der Ausdruck `COUNT( ALLITEMS (DS))` **3** zurück.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6ab7c-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6ab7c-119">Example 2</span></span>

<span data-ttu-id="6ab7c-120">Wenn Sie **Vend** als Datenquelle des Datentyps *Datensatzliste* eingeben, der auf die VendTable-Anwendungstabelle verweist, gibt der Ausdruck `ALLITEMS (Vend.'<Relations'.ContactPerson)` eine vereinfachte Liste an Datensätzen zurück, die die Tabellenstruktur **ContactPerson** aufweist und alle Kontaktpersonen enthält, auf die durch Verwendung der Beziehung **ContactPerson.ContactForParty == VendTable.Party** zugegriffen werden kann, und die für alle Kreditoren über die referenzierte Kreditorentabelle verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6ab7c-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ab7c-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6ab7c-121">Additional resources</span></span>

[<span data-ttu-id="6ab7c-122">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="6ab7c-122">List functions</span></span>](er-functions-category-list.md)
