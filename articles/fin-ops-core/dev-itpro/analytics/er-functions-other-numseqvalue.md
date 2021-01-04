---
title: NUMSEQVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der NUMSEQVALUE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: b513d04bfeb3a37aa0b1703d0fdde040885a5159
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680589"
---
# <a name="numseqvalue-er-function"></a><span data-ttu-id="ceac5-103">NUMSEQVALUE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="ceac5-103">NUMSEQVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ceac5-104">Die Funktion `NUMSEQVALUE` gibt den Wert *String* zurück, der den neu generierten Wert einer Zahlenfolge basierend auf der angegebenen Zahlenfolge, dem Gültigkeitsbereich und der Gültigkeitsbereichskennung darstellt.</span><span class="sxs-lookup"><span data-stu-id="ceac5-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="ceac5-105">Die Bereichs-ID entspricht dem Buchungscode, der von dem Kontext bereitgestellt wird, in dem das Format für die elektronische Berichterstellung (EB) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ceac5-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="ceac5-106">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="ceac5-106">Syntax 1</span></span>

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="ceac5-107">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="ceac5-107">Syntax 2</span></span>

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="ceac5-108">Syntax 3</span><span class="sxs-lookup"><span data-stu-id="ceac5-108">Syntax 3</span></span>

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="ceac5-109">Argumente</span><span class="sxs-lookup"><span data-stu-id="ceac5-109">Arguments</span></span>

<span data-ttu-id="ceac5-110">`number sequence code`: *String*</span><span class="sxs-lookup"><span data-stu-id="ceac5-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="ceac5-111">Ein Textwert, der den Code der Zahlenfolge darstellt, in der ein neuer Wert erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ceac5-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="ceac5-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="ceac5-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="ceac5-113">Der Wert *Int64*, der die Datensatz-ID eines Datensatzes in der NumberSequenceTable-Tabelle darstellt, die die Definition der Nummernfolge enthält, in der ein neuer Wert erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ceac5-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="ceac5-114">`scope type`: *Enum value*</span><span class="sxs-lookup"><span data-stu-id="ceac5-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="ceac5-115">Ein Aufzählungswert der Aufzählung **ERExpressionNumberSequenceScopeType**, die den Umfang der Zahlenfolge definiert, in der ein neuer Wert erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ceac5-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="ceac5-116">Die verfügbaren Bereichstypen sind **Geteilt**, **Juristische Person** und **Unternehmen**.</span><span class="sxs-lookup"><span data-stu-id="ceac5-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="ceac5-117">`scope ID`: *String*</span><span class="sxs-lookup"><span data-stu-id="ceac5-117">`scope ID`: *String*</span></span>

<span data-ttu-id="ceac5-118">Der Wert *String*, der den Bereich basierend auf dem angegebenen Bereichstyp identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ceac5-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ceac5-119">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ceac5-119">Return values</span></span>

<span data-ttu-id="ceac5-120">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="ceac5-120">*String*</span></span>

<span data-ttu-id="ceac5-121">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="ceac5-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ceac5-122">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="ceac5-122">Usage notes</span></span>

<span data-ttu-id="ceac5-123">Für den Bereichstyp **Gemeinsam genutzt** geben Sie eine Nullkette als die Bereichs-ID an.</span><span class="sxs-lookup"><span data-stu-id="ceac5-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="ceac5-124">Für die Bereichstypen **Unternehmen** und **Juristische Person** geben Sie den Unternehmenscode als die Bereichs-ID an.</span><span class="sxs-lookup"><span data-stu-id="ceac5-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="ceac5-125">Wenn Sie eine Nullkette als Bereichs-ID für diese Bereichstypen angeben, wird der aktuelle Buchungskreis verwendet.</span><span class="sxs-lookup"><span data-stu-id="ceac5-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="ceac5-126">Bei Verwendung von Syntax 1 wird die Nummernfolge für den Bereichstyp **Unternehmen** angefordert, und der Buchungskreis wird durch den Kontext bereitgestellt, in dem das EB-Format ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ceac5-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="ceac5-127">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ceac5-127">Example 1</span></span>

<span data-ttu-id="ceac5-128">In Ihrem EB-Format definieren Sie die Datenquelle **AskNumSeq** des Typs *Benutzereingabeparameter*.</span><span class="sxs-lookup"><span data-stu-id="ceac5-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="ceac5-129">Diese Datenquelle bezieht sich auf den Extended Data Type (EDT) **Beschreibung**.</span><span class="sxs-lookup"><span data-stu-id="ceac5-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="ceac5-130">Als Nächstes definieren Sie die Datenquelle **NumSeq** des Typs *Berechnetes Feld*.</span><span class="sxs-lookup"><span data-stu-id="ceac5-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="ceac5-131">Diese Datenquelle enthält den Ausdruck `NUMSEQVALUE (AskNumSeq)`.</span><span class="sxs-lookup"><span data-stu-id="ceac5-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="ceac5-132">Wenn die Datenquelle **NumSeq** aufgerufen wird, gibt sie den neu generierten Wert der Zahlenfolge zurück, der zur Laufzeit durch Eingabe des Codes im Dialogfeld angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ceac5-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="ceac5-133">Die Nummernfolge wird für den Bereichstyp **Unternehmen** angefordert.</span><span class="sxs-lookup"><span data-stu-id="ceac5-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="ceac5-134">Der Buchungscode wird vom Kontext bereitgestellt, in dem das EB-Format ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ceac5-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="ceac5-135">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ceac5-135">Example 2</span></span>

<span data-ttu-id="ceac5-136">Die folgenden Datenquellen sind in Ihrer Modellzuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="ceac5-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="ceac5-137">Die Datenquelle **LedgerParms** des Typs *Tabelle* .</span><span class="sxs-lookup"><span data-stu-id="ceac5-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="ceac5-138">Diese Datenquelle bezieht sich auf die LedgerParameters-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ceac5-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="ceac5-139">Die Datenquelle **NumSeq** des Typs *Berechnetes Feld*.</span><span class="sxs-lookup"><span data-stu-id="ceac5-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="ceac5-140">Diese Datenquelle enthält den Ausdruck `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span><span class="sxs-lookup"><span data-stu-id="ceac5-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="ceac5-141">Wenn die Datenquelle **NumSeq** aufgerufen wird, wird er dem generierten neuen Wert des Gen 1 Nummernkreis zurückgegeben, der für die Hauptbuch-Parameter für das Unternehmen konfiguriert wurde, der den Kontext liefert, unter dem das ER-Format ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ceac5-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="ceac5-142">Dieser Nummernkreis kennzeichnet eindeutige Erfassungen und fungiert als eine Chargennummer, die die Buchungen zusammen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="ceac5-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="ceac5-143">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ceac5-143">Example 3</span></span>

<span data-ttu-id="ceac5-144">Die folgenden Datenquellen sind in Ihrer Modellzuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="ceac5-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="ceac5-145">Die Datenquelle **enumScope** des Typs *Aufzählung* von Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ceac5-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="ceac5-146">Diese Datenquelle bezieht sich auf die Aufzählung **ERExpressionNumberSequenceScopeType**.</span><span class="sxs-lookup"><span data-stu-id="ceac5-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="ceac5-147">Die Datenquelle **NumSeq** des Typs *Berechnetes Feld*.</span><span class="sxs-lookup"><span data-stu-id="ceac5-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="ceac5-148">Diese Datenquelle enthält den Ausdruck `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span><span class="sxs-lookup"><span data-stu-id="ceac5-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="ceac5-149">Wenn die Datenquelle **NumSeq** aufgerufen wird, wird er dem generierten neuen Wert des **Gen \_1** Nummernkreis zurückgegeben, der für das Unternehmen konfiguriert wurde, der den Kontext liefe, unter dem das ER-Format ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ceac5-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ceac5-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ceac5-150">Additional resources</span></span>

[<span data-ttu-id="ceac5-151">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="ceac5-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
