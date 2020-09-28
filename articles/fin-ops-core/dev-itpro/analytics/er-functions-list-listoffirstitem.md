---
title: LISTOFFIRSTITEM EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LISTOFFIRSTITEM-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 069ec0c6d5578ca6ab68814adf325bd79e73b9e8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745056"
---
# <a name="listoffirstitem-er-function"></a>LISTOFFIRSTITEM EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `LISTOFFIRSTITEM` gibt den Wert *Datensatzliste* zurück, der nur aus dem ersten Datensatz der angegebenen Liste besteht.

## <a name="syntax"></a>Syntax

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="example"></a>Beispiel

Der Ausdruck `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` gibt den Textwert **"A"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)
