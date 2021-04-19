---
title: Liste der EB-Funktionen in der Containerkategorie
description: Dieses Thema enthält Informationen zu den Containerfunktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
author: NickSelin
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
ms.openlocfilehash: 95f207538ea4f0f7df775bf28d0dcf6529d1a91c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753239"
---
# <a name="list-of-er-functions-in-the-container-category"></a><span data-ttu-id="9c81c-103">Liste der EB-Funktionen in der Containerkategorie</span><span class="sxs-lookup"><span data-stu-id="9c81c-103">List of ER functions in the container category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c81c-104">Mithilfe der Container-[Funktionen](er-formula-language.md#functions) für die [elektronische Berichterstellung (EB)](general-electronic-reporting.md) können Operationen durchgeführt werden, die Datenquellen des Datentyps *Container* betreffen.</span><span class="sxs-lookup"><span data-stu-id="9c81c-104">[Electronic reporting (ER)](general-electronic-reporting.md) container [functions](er-formula-language.md#functions) can be used to perform operations that involve data sources of the *Container* data type.</span></span> <span data-ttu-id="9c81c-105">Diese Operationen treten auf, wenn die Verarbeitungsdaten eine Sammlung von Binärdaten im BLOB-Format (Binary Large Object) darstellen.</span><span class="sxs-lookup"><span data-stu-id="9c81c-105">These operations occur when the processing data represents a collection of binary data in binary large object (BLOB) format.</span></span> <span data-ttu-id="9c81c-106">Dieses Thema enthält eine Zusammenfassung dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9c81c-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="9c81c-107">Liste der unterstützten Funktionen</span><span class="sxs-lookup"><span data-stu-id="9c81c-107">List of supported functions</span></span>

| <span data-ttu-id="9c81c-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="9c81c-108">Function</span></span> | <span data-ttu-id="9c81c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c81c-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9c81c-110">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="9c81c-110">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="9c81c-111">Diese Funktion gibt einen *Containerwert* zurück, der aus binärem Inhalt besteht, der aus der angegebenen ASCII-Zeichenfolge decodiert wird, die eine Base64-Gruppe von Binär-Text-Codierungsschemata darstellt.</span><span class="sxs-lookup"><span data-stu-id="9c81c-111">This function returns a *Container* value that consists of binary content that is decoded from the specified ASCII string that represents a Base64 group of binary-to-text encoding schemes.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="9c81c-112">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9c81c-112">Additional resources</span></span>

[<span data-ttu-id="9c81c-113">Überblick über die elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="9c81c-113">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="9c81c-114">Formeldesigner in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="9c81c-114">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="9c81c-115">Formelsprache in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="9c81c-115">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]