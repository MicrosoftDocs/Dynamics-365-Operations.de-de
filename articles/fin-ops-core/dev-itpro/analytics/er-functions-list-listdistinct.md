---
title: LISTDISTINCT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LISTDISTINCT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 9ab9354b0fdb1c08c192b90e6bab303cb85ea41a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743822"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="892cc-103">LISTDISTINCT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="892cc-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="892cc-104">Die `LISTDISTINCT`-Funktion berechnet den angegebenen Ausdruck als Selektor für jeden Datensatz der angegebenen Liste.</span><span class="sxs-lookup"><span data-stu-id="892cc-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="892cc-105">Es wird ein neuer Wert *Datensatzliste*, der einen einzelnen Datensatz für jeden eindeutigen Auswahlwert enthält.</span><span class="sxs-lookup"><span data-stu-id="892cc-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="892cc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="892cc-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="892cc-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="892cc-107">Arguments</span></span>

<span data-ttu-id="892cc-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="892cc-108">`list`: *Record list*</span></span>

<span data-ttu-id="892cc-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="892cc-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="892cc-110">`selector`: *Primitiver Datentyp*</span><span class="sxs-lookup"><span data-stu-id="892cc-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="892cc-111">Ein gültiger Ausdruck, mit dem ein Auswahlwert für jeden Datensatz in der angegebenen Liste berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="892cc-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="892cc-112">Die folgenden Datentypen werden für diesen Parameter unterstützt:</span><span class="sxs-lookup"><span data-stu-id="892cc-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="892cc-113">Aktiv</span><span class="sxs-lookup"><span data-stu-id="892cc-113">Boolean</span></span>
- <span data-ttu-id="892cc-114">Datum</span><span class="sxs-lookup"><span data-stu-id="892cc-114">Date</span></span>
- <span data-ttu-id="892cc-115">DateTime</span><span class="sxs-lookup"><span data-stu-id="892cc-115">DateTime</span></span>
- <span data-ttu-id="892cc-116">GUID</span><span class="sxs-lookup"><span data-stu-id="892cc-116">GUID</span></span>
- <span data-ttu-id="892cc-117">Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="892cc-117">Integer</span></span>
- <span data-ttu-id="892cc-118">Int64</span><span class="sxs-lookup"><span data-stu-id="892cc-118">Int64</span></span>
- <span data-ttu-id="892cc-119">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="892cc-119">Real</span></span>
- <span data-ttu-id="892cc-120">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="892cc-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="892cc-121">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="892cc-121">Return values</span></span>

<span data-ttu-id="892cc-122">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="892cc-122">*Record list*</span></span>

<span data-ttu-id="892cc-123">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="892cc-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="892cc-124">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="892cc-124">Usage notes</span></span>

<span data-ttu-id="892cc-125">Die Struktur der erstellten Liste entspricht der Struktur der angegebenen Liste.</span><span class="sxs-lookup"><span data-stu-id="892cc-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="892cc-126">Der gleiche Auswahlwert kann für mehrere Datensätze in der angegebenen Liste berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="892cc-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="892cc-127">In diesem Fall entsprechen die Feldwerte des entsprechenden Datensatzes in der erstellten Liste den Werten des ersten Datensatzes aus der angegebenen Liste, für die der Auswahlwert berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="892cc-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="892cc-128">Die Ausführung dieser Funktion erfolgt auf jedem [Elektronische Berichterstattung (EB)](general-electronic-reporting.md) Datenquelle des Typs *Datensatzliste*, der im Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="892cc-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="892cc-129">Die Datenquelle **GROUPBY** kann auch verwendet werden, um die Liste der Datensätze zu generieren, für die der Selektor mit unterschiedlichen Werten berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="892cc-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="892cc-130">Aus Sicht der Leistung und des Speicherverbrauchs ist es jedoch besser, die Funktion `LISTDISTINCT` zu verwenden als die Datenquelle **GROUPBY**, da die Ausführung der Funktion im Speicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="892cc-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="892cc-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="892cc-131">Example</span></span>

<span data-ttu-id="892cc-132">Das folgende Beispiel zeigt, wie Sie die Liste der eindeutigen Kundenkontonummern abrufen können, für die in einem bestimmten Zeitraum mindestens eine Verkaufs- oder Projektrechnung ausgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="892cc-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="892cc-133">Geben Sie die Datenquelle **SalesInvoice** des Typs `Record list` ein, der sich auf die Anwendungstabelle **CustInvoiceJour** und Filterverkaufsrechnungen für bestimmte Zeiträume bezieht.</span><span class="sxs-lookup"><span data-stu-id="892cc-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="892cc-134">Im Feld `InvoiceAccount` dieser Datenquelle wird die Kontonummer eines fakturierten Kunden angegeben.</span><span class="sxs-lookup"><span data-stu-id="892cc-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="892cc-135">Geben Sie die Datenquelle **ProjectInvoice** des Typs `Record list` ein, der sich auf die Anwendungstabelle **ProjInvoiceJour** und Filterprojektrechnungen für bestimmte Zeiträume bezieht.</span><span class="sxs-lookup"><span data-stu-id="892cc-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="892cc-136">Im Feld `InvoiceAccount` dieser Datenquelle wird die Kontonummer eines fakturierten Kunden angegeben.</span><span class="sxs-lookup"><span data-stu-id="892cc-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="892cc-137">Konfigurieren Sie die Datenquelle **AllInvoices** des Typs `Calculated field`, der den Ausdruck `LISTJOIN(SalesInvoice, ProjectInvoice)` enthält.</span><span class="sxs-lookup"><span data-stu-id="892cc-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="892cc-138">Diese Datenquelle gibt die verknüpfte Liste der Verkaufsrechnungen und Projektrechnungen zurück.</span><span class="sxs-lookup"><span data-stu-id="892cc-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="892cc-139">Konfigurieren Sie die Datenquelle **InvoicedCustomer** des Typs `Record list`, der den Ausdruck `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)` enthält.</span><span class="sxs-lookup"><span data-stu-id="892cc-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="892cc-140">Diese Datenquelle gibt eine neue Liste zurück, die einen einzelnen Datensatz für jeden einzelnen Kunden enthält, der während des definierten Zeitraums in Rechnung gestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="892cc-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="892cc-141">Das Feld `InvoiceAccount` dieser Liste enthält eine Kundenkontonummer.</span><span class="sxs-lookup"><span data-stu-id="892cc-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="892cc-142">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="892cc-142">Additional resources</span></span>

[<span data-ttu-id="892cc-143">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="892cc-143">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]