---
title: GETCURRENTCOMPANY EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der GETCURRENTCOMPANY-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 3e14c6a8aaff0a32a115117938d0e853bb34bb14
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684858"
---
# <a name="getcurrentcompany-er-function"></a>GETCURRENTCOMPANY EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `GETCURRENTCOMPANY` gibt den Wert *String* zurück, der den Code für die juristische Person (Unternehmen) darstellt, bei dem ein Benutzer derzeit angemeldet ist.

## <a name="syntax"></a>Syntax

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example"></a>Beispiel

`GETCURRENTCOMPANY ()` gibt **USMF** für einen Benutzer zurück, der beim Unternehmen **Contoso Entertainment System USA** angemeldet ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Andere (geschäftsdomänenspezifische) Funktionen](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]