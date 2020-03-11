---
title: TEXT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der TEXT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: c08aca949ffc7e62009bf3f6c664d96b368f43e7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040893"
---
# <a name="TEXT">TEXT EB-Funktion</a>

[!include [banner](../includes/banner.md)]

Die Funktion `TEXT` gibt die angegebene Zahl mit dem Wert *String* zurück, nachdem sie in eine Textzeichenfolge konvertiert wurde, die gemäß den Servergebietsschemaeinstellungen der aktuellen Anwendungsinstanz formatiert ist.

## <a name="syntax"></a>Syntax

```vb
TEXT (number)
```

## <a name="arguments"></a>Argumente

`number`: *Integer* oder *Real*

Eine Zahl, die in eine Textzeichenfolge konvertiert werden muss.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="usage-notes"></a>Anwendungshinweise

Für Werte für den Typ *Real* wird die Zeichenkonvertierung auf zwei Dezimalstellen beschränkt.

## <a name="example"></a>Beispiel

Wenn das Servergebietsschema der Microsoft Dynamics 365 Finance-Instanz als **EN-US** definiert wird, gibt `TEXT (NOW ())` das aktuelle Finance-Sitzungsdatum, 17. Dezember 2015, als Textzeichenfolge **"12/17/2015 07:59:23 AM"** zurück. `TEXT (1/3)` gibt **"0.33"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)
