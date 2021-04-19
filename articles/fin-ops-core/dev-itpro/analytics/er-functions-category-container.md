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
# <a name="list-of-er-functions-in-the-container-category"></a>Liste der EB-Funktionen in der Containerkategorie

[!include [banner](../includes/banner.md)]

Mithilfe der Container-[Funktionen](er-formula-language.md#functions) für die [elektronische Berichterstellung (EB)](general-electronic-reporting.md) können Operationen durchgeführt werden, die Datenquellen des Datentyps *Container* betreffen. Diese Operationen treten auf, wenn die Verarbeitungsdaten eine Sammlung von Binärdaten im BLOB-Format (Binary Large Object) darstellen. Dieses Thema enthält eine Zusammenfassung dieser Funktionen.

## <a name="list-of-supported-functions"></a>Liste der unterstützten Funktionen

| Funktion | Beschreibung |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Diese Funktion gibt einen *Containerwert* zurück, der aus binärem Inhalt besteht, der aus der angegebenen ASCII-Zeichenfolge decodiert wird, die eine Base64-Gruppe von Binär-Text-Codierungsschemata darstellt. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]