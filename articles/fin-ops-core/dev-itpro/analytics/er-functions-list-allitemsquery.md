---
title: ALLITEMSQUERY EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ALLITEMSQUERY-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: ed21252fbbe3d4adad106625062e10e3de712bb0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687743"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="129f0-103">ALLITEMSQUERY EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="129f0-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="129f0-104">Die Funktion `ALLITEMSQUERY` wird als verknüpfte SQL-Abfrage ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="129f0-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="129f0-105">Es wird ein neuer vereinfachter Wert von *Datensatzliste* zurückgegeben, der aus einer Liste von Datensätzen besteht, die alle Elemente darstellen, die dem angegebenen Pfad entsprechen.</span><span class="sxs-lookup"><span data-stu-id="129f0-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="129f0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="129f0-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="129f0-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="129f0-107">Arguments</span></span>

<span data-ttu-id="129f0-108">`path`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="129f0-108">`path`: *Record list*</span></span>

<span data-ttu-id="129f0-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="129f0-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="129f0-110">Sie muss mindestens eine Beziehung enthalten.</span><span class="sxs-lookup"><span data-stu-id="129f0-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="129f0-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="129f0-111">Return values</span></span>

<span data-ttu-id="129f0-112">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="129f0-112">*Record list*</span></span>

<span data-ttu-id="129f0-113">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="129f0-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="129f0-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="129f0-114">Usage notes</span></span>

<span data-ttu-id="129f0-115">Der angegebene Pfad muss als gültiger Datenquellenpfad eines Datenquellenelements eines *Datensatzlisten*-Datentyps definiert werden.</span><span class="sxs-lookup"><span data-stu-id="129f0-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="129f0-116">Er muss zusätzlich mindestens eine Beziehung enthalten.</span><span class="sxs-lookup"><span data-stu-id="129f0-116">It must also contain at least one relation.</span></span> <span data-ttu-id="129f0-117">Datenelemente, wie beispielsweise der Pfad *String* und *Date*, sollten ein Fehler im Ausdrucksgenerator der elektronischen Berichterstellung (EB) zur Entwurfszeit erzeugen.</span><span class="sxs-lookup"><span data-stu-id="129f0-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="129f0-118">Wenn diese Funktion auf Datenquellen des Datentyps *Datensatzliste* angewendet wird, der sich auf ein Anwendungsobjekt bezieht, das direkt mit SQL aufgerufen werden kann (z. B. eine Tabelle, Entität oder Abfrage), wird sie als verknüpfte SQL-Abfrage ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="129f0-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="129f0-119">Ansonsten wird sie im Speicher als [ALLITEMS](er-functions-list-allitems.md)-Funktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="129f0-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="129f0-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="129f0-120">Example</span></span>

<span data-ttu-id="129f0-121">Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:</span><span class="sxs-lookup"><span data-stu-id="129f0-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="129f0-122">Die Datenquelle **CustInv** des Typs *Tabellendatensätze*, der sich auf die CustInvoiceTable-Tabelle verweist</span><span class="sxs-lookup"><span data-stu-id="129f0-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="129f0-123">Die Datenquelle **FilteredInv** des Typs *Berechnetes Feld*, die den Ausdruck `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")` enthält</span><span class="sxs-lookup"><span data-stu-id="129f0-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="129f0-124">**JourLines** des Typs *Berechnetes Feld*, das den Ausdruck `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)` enthält</span><span class="sxs-lookup"><span data-stu-id="129f0-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="129f0-125">Wenn Sie die Modellzuordnung ausführen, um die Datenquelle **JourLines** aufzurufen, wird die folgende SQL-Anweisung ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="129f0-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="129f0-126">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="129f0-126">Additional resources</span></span>

[<span data-ttu-id="129f0-127">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="129f0-127">List functions</span></span>](er-functions-category-list.md)
