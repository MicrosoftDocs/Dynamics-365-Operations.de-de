---
title: Liste der EB-Funktionen in der Containerkategorie
description: Dieses Thema enthält Informationen zu den Containerfunktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
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
ms.openlocfilehash: b7e7d770c334647f8f11338d49b39a2e9cb5c04c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561757"
---
# <a name="list-of-er-functions-in-the-container-category"></a><span data-ttu-id="bb7d2-103">Liste der EB-Funktionen in der Containerkategorie</span><span class="sxs-lookup"><span data-stu-id="bb7d2-103">List of ER functions in the container category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb7d2-104">Mithilfe der Container-[Funktionen](er-formula-language.md#functions) für die [elektronische Berichterstellung (EB)](general-electronic-reporting.md) können Operationen durchgeführt werden, die Datenquellen des Datentyps *Container* betreffen.</span><span class="sxs-lookup"><span data-stu-id="bb7d2-104">[Electronic reporting (ER)](general-electronic-reporting.md) container [functions](er-formula-language.md#functions) can be used to perform operations that involve data sources of the *Container* data type.</span></span> <span data-ttu-id="bb7d2-105">Diese Operationen treten auf, wenn die Verarbeitungsdaten eine Sammlung von Binärdaten im BLOB-Format (Binary Large Object) darstellen.</span><span class="sxs-lookup"><span data-stu-id="bb7d2-105">These operations occur when the processing data represents a collection of binary data in binary large object (BLOB) format.</span></span> <span data-ttu-id="bb7d2-106">Dieses Thema enthält eine Zusammenfassung dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="bb7d2-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="bb7d2-107">Liste der unterstützten Funktionen</span><span class="sxs-lookup"><span data-stu-id="bb7d2-107">List of supported functions</span></span>

| <span data-ttu-id="bb7d2-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="bb7d2-108">Function</span></span> | <span data-ttu-id="bb7d2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb7d2-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="bb7d2-110">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="bb7d2-110">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="bb7d2-111">Diese Funktion gibt einen *Containerwert* zurück, der aus binärem Inhalt besteht, der aus der angegebenen ASCII-Zeichenfolge decodiert wird, die eine Base64-Gruppe von Binär-Text-Codierungsschemata darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb7d2-111">This function returns a *Container* value that consists of binary content that is decoded from the specified ASCII string that represents a Base64 group of binary-to-text encoding schemes.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="bb7d2-112">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bb7d2-112">Additional resources</span></span>

[<span data-ttu-id="bb7d2-113">Überblick über die elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="bb7d2-113">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="bb7d2-114">Formeldesigner in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="bb7d2-114">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="bb7d2-115">Formelsprache in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="bb7d2-115">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]