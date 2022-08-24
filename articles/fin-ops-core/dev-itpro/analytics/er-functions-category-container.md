---
title: Liste der EB-Funktionen in der Containerkategorie
description: Dieser Artikel enthält Informationen zu den Containerfunktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
author: kfend
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: f07c3645f824fc2fe8ca156c8cf06840e993a9a5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282650"
---
# <a name="list-of-er-functions-in-the-container-category"></a>Liste der EB-Funktionen in der Containerkategorie

[!include [banner](../includes/banner.md)]

Mithilfe der Container-[Funktionen](er-formula-language.md#Functions) für die [elektronische Berichterstellung (EB)](general-electronic-reporting.md) können Operationen durchgeführt werden, die Datenquellen des Datentyps *Container* betreffen. Diese Operationen treten auf, wenn die Verarbeitungsdaten eine Sammlung von Binärdaten im BLOB-Format (Binary Large Object) darstellen. Dieser Artikel enthält eine Zusammenfassung dieser Funktionen.

## <a name="list-of-supported-functions"></a>Liste der unterstützten Funktionen

| Funktion | Beschreibung |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Diese Funktion gibt einen *Containerwert* zurück, der aus binärem Inhalt besteht, der aus der angegebenen ASCII-Zeichenfolge decodiert wird, die eine Base64-Gruppe von Binär-Text-Codierungsschemata darstellt. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
