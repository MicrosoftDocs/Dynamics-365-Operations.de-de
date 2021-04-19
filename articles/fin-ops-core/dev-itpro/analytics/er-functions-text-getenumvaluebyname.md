---
title: GETENUMVALUEBYNAME EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der GETENUMVALUEBYNAME-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 09/23/2020
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
ms.openlocfilehash: 72b5831e3d2bc2e839b0a569fb314a8ec074a5a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746410"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="13c84-103">GETENUMVALUEBYNAME EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="13c84-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13c84-104">Die Funktion `GETENUMVALUEBYNAME` sucht nach dem bestimmten Wert *Enum* in der angegebenen Aufzählungsdatenquelle unter Verwendung des Aufzählungsnamens, der mit dem Wert *String* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="13c84-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="13c84-105">Wenn der Wert *Enum* gefunden wird, gibt die Funktion ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="13c84-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="13c84-106">Andernfalls gibt die Funktion den Aufzählungswert **Null** zurück.</span><span class="sxs-lookup"><span data-stu-id="13c84-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c84-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="13c84-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="13c84-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="13c84-108">Arguments</span></span>

<span data-ttu-id="13c84-109">`enumeration data source path`: *Aufzählung*</span><span class="sxs-lookup"><span data-stu-id="13c84-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="13c84-110">Der gültige Pfad einer Datenquelle eines der folgenden Aufzählungstypen:</span><span class="sxs-lookup"><span data-stu-id="13c84-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="13c84-111">Modellenumeration für die elektronische Berichterstellung (EB)</span><span class="sxs-lookup"><span data-stu-id="13c84-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="13c84-112">EB-Formatenumeration</span><span class="sxs-lookup"><span data-stu-id="13c84-112">ER format enumeration</span></span>
- <span data-ttu-id="13c84-113">Microsoft Dynamics 365 Finance-Enumeration</span><span class="sxs-lookup"><span data-stu-id="13c84-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="13c84-114">`enumeration value text`: *String*</span><span class="sxs-lookup"><span data-stu-id="13c84-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="13c84-115">Ein Zeichenfolgewert, der den Namen eines einzelnen Aufzählungswerts darstellt.</span><span class="sxs-lookup"><span data-stu-id="13c84-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="13c84-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="13c84-116">Return values</span></span>

<span data-ttu-id="13c84-117">Nullbar *Enum*</span><span class="sxs-lookup"><span data-stu-id="13c84-117">Nullable *Enum*</span></span>

<span data-ttu-id="13c84-118">Der resultierende Aufzählungswert.</span><span class="sxs-lookup"><span data-stu-id="13c84-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="13c84-119">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="13c84-119">Usage notes</span></span>

<span data-ttu-id="13c84-120">Es wird keine Ausnahme ausgelöst, wenn ein Wert *Enum* nicht unter Verwendung des Namens des Aufzählungswerts gefunden wird, der mit dem Wert *String* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="13c84-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="13c84-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13c84-121">Example 1</span></span>

<span data-ttu-id="13c84-122">In der folgenden Abbildung wird die Aufzählung **ReportDirection** in einem Datenmodell eingeführt.</span><span class="sxs-lookup"><span data-stu-id="13c84-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="13c84-123">Beachten Sie, dass Beschriftungen für Enumerationswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="13c84-123">Notice that labels are defined for the enumeration values.</span></span>

![Verfügbare Werte für eine Datenmodellenumeration](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="13c84-125">Die folgende Abbildung zeigt diese Details an:</span><span class="sxs-lookup"><span data-stu-id="13c84-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="13c84-126">Die Datenquelle **$Direction** wird in einem EB-Bericht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="13c84-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="13c84-127">Diese Datenquelle wird basierend auf der Modellenumeration **ReportDirection** konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="13c84-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="13c84-128">Der Ausdruck `$IsArrivals` ist dazu konzipiert, die auf der Modellenumeration basierende Datenquelle **$Direction** als Parameter dieser Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="13c84-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="13c84-129">Der Wert dieses Vergleichswerts lautet **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="13c84-129">The value of this comparison expression is **TRUE**.</span></span>

![Beispiel einer Datenmodellenumeration](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="13c84-131">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="13c84-131">Example 2</span></span>

<span data-ttu-id="13c84-132">Die Funktionen `GETENUMVALUEBYNAME` und [`LISTOFFIELDS`](er-functions-list-listoffields.md) ermöglichen das Abrufen von Werten und Bezeichnungen unterstützter Enumerationen als Textwerte.</span><span class="sxs-lookup"><span data-stu-id="13c84-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="13c84-133">(Die unterstützten Enumerationen sind Anwendungsenumerationen, Datenmodellenumerationen und Formatenumerationen.)</span><span class="sxs-lookup"><span data-stu-id="13c84-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="13c84-134">In der folgenden Abbildung wird die Datenquelle **TransType** in einer Modellzuordnung eingeführt.</span><span class="sxs-lookup"><span data-stu-id="13c84-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="13c84-135">Diese Datenquelle bezieht sich auf die Anwendungsenumeration **LedgerTransType**.</span><span class="sxs-lookup"><span data-stu-id="13c84-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![Datenquelle einer Modellzuordnung, die sich auf eine Anwendungsenumeration bezieht](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="13c84-137">Die folgende Abbildung zeigt die Datenquelle **TransTypeList**, die in einer Modellzuordnung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="13c84-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="13c84-138">Diese Datenquelle wird basierend auf der Anwendungsenumeration **TransType** konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="13c84-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="13c84-139">Die Funktion `LISTOFFIELDS` wird verwendet, um alle Enumerationswerte als Liste von Datensätzen zurückzugeben, die Felder enthalten.</span><span class="sxs-lookup"><span data-stu-id="13c84-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="13c84-140">Auf diese Weise werden die Details jedes Enumerationswerts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="13c84-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="13c84-141">Das Feld **EnumValue** ist für die Datenquelle **TransTypeList** konfiguriert, wofür der Ausdruck `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13c84-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="13c84-142">Dieses Feld gibt einen Enumerationswert für jeden Datensatz in dieser Liste zurück.</span><span class="sxs-lookup"><span data-stu-id="13c84-142">This field returns an enumeration value for every record in this list.</span></span>

![Datenquelle einer Modellzuordnung, die alle Enumerationswerte einer ausgewählten Enumeration als Liste von Datensätzen zurückgibt](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="13c84-144">Die folgende Abbildung zeigt die Datenquelle **VendTrans**, die in einer Modellzuordnung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="13c84-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="13c84-145">Diese Datenquelle gibt Lieferantentransaktionsdatensätze aus der Anwendungstabelle **VendTrans** zurück.</span><span class="sxs-lookup"><span data-stu-id="13c84-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="13c84-146">Der Sachkontotyp jeder Transaktion wird durch den Wert im Feld **TransType** definiert.</span><span class="sxs-lookup"><span data-stu-id="13c84-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="13c84-147">Das Feld **TransTypeTitle** ist für die Datenquelle **VendTrans** konfiguriert, wofür der Ausdruck `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13c84-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="13c84-148">Dieses Feld gibt die Bezeichnung eines Enumerationswerts der aktuellen Transaktion als Text zurück, wenn dieser Enumerationswert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="13c84-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="13c84-149">Andernfalls wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13c84-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="13c84-150">Das Feld **TransTypeTitle** ist an das Feld **LedgerType** eines Datenmodells gebunden, mit dem diese Informationen in jedem EB-Format verwendet werden können, das dieses Datenmodell als Datenquelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="13c84-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![Datenquelle einer Modellzuordnung, die Lieferantentransaktionen zurückgibt](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="13c84-152">Die folgende Abbildung zeigt, wie Sie den [Datenquellen-Debugger](er-debug-data-sources.md) verwenden können, um die konfigurierte Modellzuordnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="13c84-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![Verwenden des Datenquellen-Debuggers zum Testen der konfigurierten Modellzuordnung](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="13c84-154">Das Feld **LedgerType** eines Datenmodells legt erwartungsgemäß Bezeichnungen von Transaktionstypen offen.</span><span class="sxs-lookup"><span data-stu-id="13c84-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="13c84-155">Wenn Sie diesen Ansatz für eine große Menge von Transaktionsdaten verwenden möchten, müssen Sie die Ausführungsleistung berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="13c84-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="13c84-156">Weitere Informationen finden Sie unter [Überwachen der Ausführung von EB-Formaten zur Behebung von Leistungsproblemen](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="13c84-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13c84-157">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="13c84-157">Additional resources</span></span>

[<span data-ttu-id="13c84-158">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="13c84-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="13c84-159">Überwachen der Ausführung von ER-Formaten zur Behebung von Leistungsproblemen</span><span class="sxs-lookup"><span data-stu-id="13c84-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="13c84-160">LISTOFFIELDS EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="13c84-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="13c84-161">FIRSTORNULL EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="13c84-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="13c84-162">WHERE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="13c84-162">WHERE ER function</span></span>](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]