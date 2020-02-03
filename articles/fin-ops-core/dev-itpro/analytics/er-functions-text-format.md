---
title: FORMAT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der FORMAT-Funktion bei der elektronischen Berichterstellung bereitgestellt.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df158e80bd1c11832376678a631a9e0e162534ad
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915716"
---
# <span data-ttu-id="2e44f-103"><a name="FORMAT">FORMAT EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="2e44f-103"><a name="FORMAT">FORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e44f-104">Die Funktion `FORMAT` gibt den angegebenen Zeichenfolgenwert mit dem Wert *String* zurück, nachdem sie durch Ersetzen sämtlicher Vorkommnisse von **%N** durch das *N*. Argument formatiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2e44f-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e44f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e44f-105">Syntax</span></span>

```
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="2e44f-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="2e44f-106">Arguments</span></span>

<span data-ttu-id="2e44f-107">`string`: *String*</span><span class="sxs-lookup"><span data-stu-id="2e44f-107">`string`: *String*</span></span>

<span data-ttu-id="2e44f-108">Ein Verweis auf die Datenquelle des Typs *String*, die formatiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="2e44f-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="2e44f-109">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2e44f-109">This argument is required.</span></span>

<span data-ttu-id="2e44f-110">`argument 1`: *String*</span><span class="sxs-lookup"><span data-stu-id="2e44f-110">`argument 1`: *String*</span></span>

<span data-ttu-id="2e44f-111">Das erste Argument, das verwendet wird, um Vorkommnisse von **%1** zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="2e44f-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="2e44f-112">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2e44f-112">This argument is required.</span></span>

<span data-ttu-id="2e44f-113">`argument N`: *String*</span><span class="sxs-lookup"><span data-stu-id="2e44f-113">`argument N`: *String*</span></span>

<span data-ttu-id="2e44f-114">Das *N*. Argument, das verwendet wird, um Vorkommnisse von **%2**, **%3** usw. zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="2e44f-114">The *N*th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="2e44f-115">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="2e44f-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="2e44f-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2e44f-116">Return values</span></span>

<span data-ttu-id="2e44f-117">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="2e44f-117">*String*</span></span>

<span data-ttu-id="2e44f-118">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="2e44f-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2e44f-119">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="2e44f-119">Usage notes</span></span>

<span data-ttu-id="2e44f-120">Wenn eine Anfrage nicht für einen Parameter angegeben wird, wird der Parameter als **"%N"** in der Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2e44f-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="2e44f-121">Für Werte für den Typ *Real*, wird die Standard-Zeichenkonvertierung auf zwei Dezimalstellen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2e44f-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="2e44f-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2e44f-122">Example</span></span>

<span data-ttu-id="2e44f-123">In der folgenden Abbildung gibt die Datenquelle **PaymentModel** eine Liste der Kundendatensätze zurück, indem die Komponente **Debitor** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2e44f-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="2e44f-124">Sie gibt den Wert des Verarbeitungsdatums über das Feld **ProcessingDate** zurück.</span><span class="sxs-lookup"><span data-stu-id="2e44f-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="2e44f-125">Im Format für die elektronische Berichterstellung (EB), das entworfen wurde, um eine Datei für ausgewählte Debitoren zu generieren, wird **PaymentModel** als Datenquelle ausgewählt, um den Prozessablauf zu steuern.</span><span class="sxs-lookup"><span data-stu-id="2e44f-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="2e44f-126">Wenn ein ausgewählter Debitor zu dem Datum angehalten wird, an dem der Bericht verarbeitet wird, wird zur Benachrichtigung des Benutzers eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="2e44f-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="2e44f-127">Die Formel, die für diese Art von Prozesssteuerung entworfen wurde, kann die folgenden Ressourcen verwenden:</span><span class="sxs-lookup"><span data-stu-id="2e44f-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="2e44f-128">Beschriftung SYS70894, die den folgenden Text hat:</span><span class="sxs-lookup"><span data-stu-id="2e44f-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="2e44f-129">**Für die EN-US-Sprache:** "Nichts zu drucken"</span><span class="sxs-lookup"><span data-stu-id="2e44f-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="2e44f-130">**Für deutsche Sprache:** "Nichts zu drucken"</span><span class="sxs-lookup"><span data-stu-id="2e44f-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="2e44f-131">Beschriftung SYS18389, die den folgenden Text hat:</span><span class="sxs-lookup"><span data-stu-id="2e44f-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="2e44f-132">**Für die Sprache EN-US:** "Debitor %1 wird für %2 beendet."</span><span class="sxs-lookup"><span data-stu-id="2e44f-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="2e44f-133">**Für die Sprache DE:** "Debitor '%1' wird für %2 gesperrt."</span><span class="sxs-lookup"><span data-stu-id="2e44f-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="2e44f-134">Hier ist der Ausdruck, der gestaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2e44f-134">Here is the expression that can be designed.</span></span>

```
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="2e44f-135">Wenn ein Bericht für den Kunden **Litware Retail** am 17. Dezember 2015 in der **EN-US**-Kultur und in der **EN-US**-Sprache verarbeitet wird, gibt diese Formel den folgenden Text zurück, der dann als Ausnahmenachricht für den Benutzer präsentiert werden kann:</span><span class="sxs-lookup"><span data-stu-id="2e44f-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="2e44f-136">*Nichts zu drucken. Debitor Litware Retail wird am 12/17/2015 beendet.*</span><span class="sxs-lookup"><span data-stu-id="2e44f-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="2e44f-137">Wenn derselbe Bericht für den Kunden **Litware Retail** am 17. Dezember 2015 in der **DE**-Kultur und in der **DE**-Sprache verarbeitet wird, gibt diese Formel den folgenden Text zurück, der ein anderes Datumsformat verwendet:</span><span class="sxs-lookup"><span data-stu-id="2e44f-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="2e44f-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="2e44f-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="2e44f-139">Die folgende Syntax wird in EB-Formeln für Beschriftungen angewendet:</span><span class="sxs-lookup"><span data-stu-id="2e44f-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="2e44f-140">**Für Bezeichnungen aus Ressourcen in der Microsoft Dynamics 365 Finance-App:** **@X**, wobei **X** die Bezeichnungs-ID in der Entwicklungsumgebung ist.</span><span class="sxs-lookup"><span data-stu-id="2e44f-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="2e44f-141">**Für Bezeichnungen in EB-Konfigurationen:** **@"GER_LABEL:X"**, wobei **X** die Bezeichnungs-ID in der EB-Konfiguration ist</span><span class="sxs-lookup"><span data-stu-id="2e44f-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e44f-142">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2e44f-142">Additional resources</span></span>

[<span data-ttu-id="2e44f-143">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="2e44f-143">Text functions</span></span>](er-functions-category-text.md)