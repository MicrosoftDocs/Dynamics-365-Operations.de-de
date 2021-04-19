---
title: LISTOFFIELDS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LISTOFFIELDS-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 4f394a557beaeb558f5c7065eefe16f4aadce6ac
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743773"
---
# <a name="listoffields-er-function"></a><span data-ttu-id="f67ef-103">LISTOFFIELDS EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="f67ef-103">LISTOFFIELDS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f67ef-104">Die Funktion `LISTOFFIELDS` gibt den Wert *Datensatzliste* zurück, der basierend auf der Struktur des angegebenen Arguments des Typs *Enumeration* oder *Container (Datensatz)* erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f67ef-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="f67ef-105">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="f67ef-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="f67ef-106">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="f67ef-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="f67ef-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="f67ef-107">Arguments</span></span>

<span data-ttu-id="f67ef-108">`path`: Referenz der Datenquelle</span><span class="sxs-lookup"><span data-stu-id="f67ef-108">`path`: Data source reference</span></span>

<span data-ttu-id="f67ef-109">Der gültige Referenzpfad einer Datenquelle einer der folgenden Datentypen:</span><span class="sxs-lookup"><span data-stu-id="f67ef-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="f67ef-110">Modellenumeration</span><span class="sxs-lookup"><span data-stu-id="f67ef-110">Model enumeration</span></span>
- <span data-ttu-id="f67ef-111">Formatenumeration</span><span class="sxs-lookup"><span data-stu-id="f67ef-111">Format enumeration</span></span>
- <span data-ttu-id="f67ef-112">Anwendungsaufzählung</span><span class="sxs-lookup"><span data-stu-id="f67ef-112">Application enumeration</span></span>
- <span data-ttu-id="f67ef-113">Container (Datensatz)</span><span class="sxs-lookup"><span data-stu-id="f67ef-113">Container (record)</span></span>

<span data-ttu-id="f67ef-114">`language`: *String*</span><span class="sxs-lookup"><span data-stu-id="f67ef-114">`language`: *String*</span></span>

<span data-ttu-id="f67ef-115">Text, der einen Sprachcode darstellt.</span><span class="sxs-lookup"><span data-stu-id="f67ef-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="f67ef-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f67ef-116">Return values</span></span>

<span data-ttu-id="f67ef-117">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="f67ef-117">*Record list*</span></span>

<span data-ttu-id="f67ef-118">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="f67ef-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f67ef-119">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="f67ef-119">Usage notes</span></span>

<span data-ttu-id="f67ef-120">Die Liste, die erstellt wird, besteht aus Datensätzen, die die folgenden Felder haben:</span><span class="sxs-lookup"><span data-stu-id="f67ef-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="f67ef-121">**Name** (Datentyp *String*)</span><span class="sxs-lookup"><span data-stu-id="f67ef-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="f67ef-122">**Bezeichnung** (Datentyp *String*)</span><span class="sxs-lookup"><span data-stu-id="f67ef-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="f67ef-123">**Beschreibung** (Datentyp *String*)</span><span class="sxs-lookup"><span data-stu-id="f67ef-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="f67ef-124">**IsTranslated** (Datentyp *Boolesch*)</span><span class="sxs-lookup"><span data-stu-id="f67ef-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="f67ef-125">Wenn das Argument `path` sich auf eine Datenquelle des Typs *Container (Datensatz)* bezieht, geben Sie für jedes Feld des referenzierten Datensatzes, auf den verwiesen wird, einen neuen Datensatz in die Liste ein, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f67ef-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="f67ef-126">Für jeden erstellten Datensatz gibt das Feld **Name** den Namen des Felds des referenzierten Containerdatensatzes zurück, für den der aktuelle Datensatz erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f67ef-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="f67ef-127">Wenn das Argument `path` sich auf eine Datenquelle einer der Typen *Enumeration* bezieht, geben Sie für jeden Enumerationswert der referenzierten Enumeration, auf die verwiesen wird, einen neuen Datensatz in die Liste ein, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f67ef-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="f67ef-128">Für jeden erstellten Datensatz gibt das Feld **Name** den Wert der referenzierten Enumeration zurück, für die der aktuelle Datensatz erstellt wurde, das Feld **Beschreibung** gibt die Beschreibung dieser Enumeration zurück, und das Feld **Bezeichnung** gibt die Bezeichnung dieser Enumeration zurück.</span><span class="sxs-lookup"><span data-stu-id="f67ef-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="f67ef-129">Wenn zur Laufzeit die Syntax 1 verwendet wird, müssen die Felder **Bezeichnung** und **Beschreibung** Werte zurückgeben, die auf den Spracheinstellungen des elektronischen Berichterstellungsformats (EB) basieren, das ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="f67ef-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="f67ef-130">Wenn die Bezeichnungen und Beschreibungen für die angeforderte Sprache verfügbar sind, geben die Felder **Bezeichnung** und **Beschreibung** Werte zurück, die auf dieser Sprache basieren, und das Feld **IsTranslated** gibt **True** zurück.</span><span class="sxs-lookup"><span data-stu-id="f67ef-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="f67ef-131">Wenn die Bezeichnungen und Beschreibungen für die angeforderte Sprache nicht verfügbar sind, geben die Felder **Bezeichnung** und **Beschreibung** Werte zurück, die auf der Standardsprache **EN-US** basieren, und das Feld **IsTranslated** gibt **False** zurück.</span><span class="sxs-lookup"><span data-stu-id="f67ef-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="f67ef-132">Wenn zur Laufzeit die Syntax 2 verwendet wird, müssen die Felder **Bezeichnung** und **Beschreibung** Werte zurückgeben, die auf den Spracheinstellungen basieren, die als zweites Argument der aufgerufenen Funktion definiert sind:</span><span class="sxs-lookup"><span data-stu-id="f67ef-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="f67ef-133">Wenn die Bezeichnungen und Beschreibungen für die angeforderte Sprache verfügbar sind, geben die Felder **Bezeichnung** und **Beschreibung** Werte zurück, die auf dieser Sprache basieren, und das Feld **IsTranslated** gibt **True** zurück.</span><span class="sxs-lookup"><span data-stu-id="f67ef-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="f67ef-134">Wenn die Bezeichnungen und Beschreibungen für die angeforderte Sprache nicht verfügbar sind, geben die Felder **Bezeichnung** und **Beschreibung** Werte zurück, die auf der Standardsprache **EN-US** basieren, und das Feld **IsTranslated** gibt **False** zurück.</span><span class="sxs-lookup"><span data-stu-id="f67ef-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="f67ef-135">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f67ef-135">Example 1</span></span>

<span data-ttu-id="f67ef-136">In der folgenden Abbildung wird eine Aufzählung in einem EB-Datenmodell vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="f67ef-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="f67ef-137">Die folgende Abbildung zeigt diese Details an:</span><span class="sxs-lookup"><span data-stu-id="f67ef-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="f67ef-138">Die Modellaufzählung ist eingefügt in einen Bericht als Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="f67ef-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="f67ef-139">Ein EB-Ausdruck verwendet die Modellaufzählung als Parameter der Funktion `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="f67ef-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="f67ef-140">Eine Datenquelle des Typs *Datensatzliste* wird in einen Bericht mithilfe des EB-Ausdrucks eingefügt, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f67ef-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="f67ef-141">Das folgende Beispiel zeigt die EB-Formatelemente, die an die Datenquelle des Typs *Datensatzliste* gebunden sind, der mithilfe der Funktion `LISTOFFIELDS` erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f67ef-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="f67ef-142">Die folgende Abbildung zeigt das Ergebnis, wenn das entworfene Format ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f67ef-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="f67ef-143">Basierend auf den Spracheinstellungen des Formats von übergeordneten **DATEI**- und **ORDNER**-Elementen, wird übersetzter Text für Beschriftungen und Beschreibungen in der Ausgabe des EB-Formats eingegeben.</span><span class="sxs-lookup"><span data-stu-id="f67ef-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="f67ef-144">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f67ef-144">Example 2</span></span>

<span data-ttu-id="f67ef-145">Sie verwenden den Datenquellentyp *Berechnetes Feld*, um die Datenquellen **enumType\_de** und **enumType\_deCH** für die Datenmodellaufzählung **enumType** zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="f67ef-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="f67ef-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="f67ef-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="f67ef-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="f67ef-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="f67ef-148">In diesem Fall können Sie den folgenden Ausdruck verwenden, um die Beschriftung des Aufzählungswerts in Schweizer Deutsch abzurufen, wenn diese Übersetzung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f67ef-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="f67ef-149">Wenn die schweizerdeutsche Übersetzung nicht verfügbar ist, ist das Etikett auf Deutsch.</span><span class="sxs-lookup"><span data-stu-id="f67ef-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="f67ef-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f67ef-150">Additional resources</span></span>

[<span data-ttu-id="f67ef-151">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="f67ef-151">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]