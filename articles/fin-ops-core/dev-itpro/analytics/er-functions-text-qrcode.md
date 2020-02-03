---
title: QRCODE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der QRCODE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: bac0910d213ee05a2a7a7b218a6714d4f935be16
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916751"
---
# <span data-ttu-id="60460-103"><a name="QRCODE">QRCODE EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="60460-103"><a name="QRCODE">QRCODE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60460-104">Die Funktion `QRCODE` gibt den Wert *Container* zurück, der das QR-Code-Bild (Quick Response Code) für die angegebene Zeichenfolge im Binärformat darstellt.</span><span class="sxs-lookup"><span data-stu-id="60460-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="60460-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60460-105">Syntax</span></span>

```
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="60460-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="60460-106">Arguments</span></span>

<span data-ttu-id="60460-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="60460-107">`text`: *String*</span></span>

<span data-ttu-id="60460-108">Der Wert *String*, der den Originaltext darstellt.</span><span class="sxs-lookup"><span data-stu-id="60460-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="60460-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="60460-109">Return values</span></span>

<span data-ttu-id="60460-110">*Container*</span><span class="sxs-lookup"><span data-stu-id="60460-110">*Container*</span></span>

<span data-ttu-id="60460-111">Der resultierende binäre Stream.</span><span class="sxs-lookup"><span data-stu-id="60460-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="60460-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="60460-112">Example</span></span>

<span data-ttu-id="60460-113">Sie können ein EB-Format (elektronische Berichtserstellung) konfigurieren, um ein ausgehendes Dokument im Microsoft Office-Format (Excel-Arbeitsmappen oder Word-Dokumente) mithilfe einer vordefinierten Vorlage zu generieren.</span><span class="sxs-lookup"><span data-stu-id="60460-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="60460-114">Diese Vorlage kann das Objekt **Bild** (Excel-Arbeitsmappe) oder eine **Picture Content Control** (Word-Dokument) als Platzhalter für ein QR-Codebild enthalten.</span><span class="sxs-lookup"><span data-stu-id="60460-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="60460-115">Sie müssen dem konfigurierten EB-Format das Element **Zelle** hinzufügen, das zum Ausfüllen dieses Platzhalters verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60460-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="60460-116">Um festzulegen, welche Informationen in einem QR-Code gespeichert werden, müssen Sie eine Bindung für das Element **Zelle** definieren.</span><span class="sxs-lookup"><span data-stu-id="60460-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="60460-117">Beispielsweise können Sie eine solche Bindung so konfigurieren, dass sie den folgenden Ausdruck enthält:</span><span class="sxs-lookup"><span data-stu-id="60460-117">For example, you can configure such binding as containing the following expression:</span></span>

```
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="60460-118">Wenn Sie das konfigurierte EB-Format ausführen, wird der Textwert des Feldes **LabelText** von der Datenquelle **model.ListOfShelfLabels** verwendet, um ein QR-Codebild zu generieren.</span><span class="sxs-lookup"><span data-stu-id="60460-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="60460-119">Dieses Bild ersetzt einen Platzhalter für ein QR-Code-Bild in der Dokumentvorlage, mit dem ein ausgehendes Dokument generiert wird.</span><span class="sxs-lookup"><span data-stu-id="60460-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="60460-120">Wenn dieses Bild des generierten Dokuments gescannt wird, wird der Text zurückgegeben, der aus dem Feld **LabelText** der Datenquelle **model.ListOfShelfLabels** bezogen wurde.</span><span class="sxs-lookup"><span data-stu-id="60460-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="60460-121">Weitere Informationen erhalten Sie unter [Einbetten von Bildern und Formen in generierten Dokumenten mithilfe von EB](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="60460-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60460-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="60460-122">Additional resources</span></span>

[<span data-ttu-id="60460-123">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="60460-123">Text functions</span></span>](er-functions-category-text.md)