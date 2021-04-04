---
title: EB-Funktion Base64StringToContainer
description: In diesem Thema werden Informationen zur Verwendung der Base64StringToContainer-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 612590dacc1887b87677c12eddaef42660a7a154
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561541"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="b0487-103">EB-Funktion Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="b0487-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0487-104">Die `BASE64STRINGTOCONTAINER`-[Funktion](er-formula-language.md#functions) konvertiert die angegebene Eingabe des Datentyps *String* in ein Datenelement des Typs *[Container](er-functions-category-container.md)*.</span><span class="sxs-lookup"><span data-stu-id="b0487-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0487-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0487-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="b0487-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="b0487-106">Arguments</span></span>

<span data-ttu-id="b0487-107">`input`: *String*</span><span class="sxs-lookup"><span data-stu-id="b0487-107">`input`: *String*</span></span>

<span data-ttu-id="b0487-108">Der gültige Pfad einer Datenquelle des Typs *String*.</span><span class="sxs-lookup"><span data-stu-id="b0487-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b0487-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b0487-109">Return values</span></span>

<span data-ttu-id="b0487-110">*Behälter*</span><span class="sxs-lookup"><span data-stu-id="b0487-110">*Container*</span></span>

<span data-ttu-id="b0487-111">Der resultierende Binärwert im BLOB-Format (Binary Large Object).</span><span class="sxs-lookup"><span data-stu-id="b0487-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b0487-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="b0487-112">Usage notes</span></span>

<span data-ttu-id="b0487-113">Die Ausnahme „Parameter ist ungültig“ wird ausgegeben, wenn die Eingabezeichenfolge keine korrekte Base64-Gruppe von Binär-Text-Codierungsschemata enthält.</span><span class="sxs-lookup"><span data-stu-id="b0487-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="b0487-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b0487-114">Example</span></span>

<span data-ttu-id="b0487-115">Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:</span><span class="sxs-lookup"><span data-stu-id="b0487-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="b0487-116">Die Stammdatenquelle **DocuTypeGroupEnum** des Typs *Dynamics 365 for Operations/Aufzählung*, die sich auf die Anwendungsaufzählung **DocuTypeGroup** bezieht</span><span class="sxs-lookup"><span data-stu-id="b0487-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="b0487-117">Die Stammdatenquelle **Debitor** des Typs *Dynamics 365 for Operations/Tabellendatensätze*, die auf die Anwendungstabelle **CustTable** verweist</span><span class="sxs-lookup"><span data-stu-id="b0487-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="b0487-118">Die Datenaquelle **\#Medien** des Typs *Berechnetes Feld*, die folgendermaßen konfiguriert ist:</span><span class="sxs-lookup"><span data-stu-id="b0487-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="b0487-119">Sie wird als untergeordnete Datenquelle der Datenquelle **Debitor** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b0487-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="b0487-120">Sie enthält den Ausdruck `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span><span class="sxs-lookup"><span data-stu-id="b0487-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="b0487-121">Die Datenquelle **\#MediaAsBase64String** des Typs *Berechnetes Feld*, die folgendermaßen konfiguriert ist:</span><span class="sxs-lookup"><span data-stu-id="b0487-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="b0487-122">Sie wird als untergeordnete Datenquelle der Datenquelle **Debitor.'\#Medien'** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b0487-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="b0487-123">Sie enthält den Ausdruck `Customer.'#Media'.'getFileContentAsBase64String()'`.</span><span class="sxs-lookup"><span data-stu-id="b0487-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="b0487-124">Die Datenquelle **\#BlobFomBase64** des Typs *Berechnetes Feld*, die folgendermaßen konfiguriert ist:</span><span class="sxs-lookup"><span data-stu-id="b0487-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="b0487-125">Sie wird als untergeordnete Datenquelle der Datenquelle **Debitor.'\#Medien'** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b0487-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="b0487-126">Sie enthält den Ausdruck `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span><span class="sxs-lookup"><span data-stu-id="b0487-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="b0487-127">In diesem Beispiel codiert die Datenquelle **\#MediaAsBase64String** den binären Inhalt des aktuellen Medienanhangs als Text, der eine Base64-Gruppe von Binär-Text-Codierungsschemata darstellt.</span><span class="sxs-lookup"><span data-stu-id="b0487-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="b0487-128">Die Datenquelle **\#BlobFomBase64** decodiert die Base64-Zeichenfolge und gibt einen Binärwert im BLOB-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="b0487-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![Beispieldatenquelle auf der Seite des EB-Modellzuordnungsdesigners](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="b0487-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b0487-130">Additional resources</span></span>

[<span data-ttu-id="b0487-131">Containerfunktionen</span><span class="sxs-lookup"><span data-stu-id="b0487-131">Container functions</span></span>](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]