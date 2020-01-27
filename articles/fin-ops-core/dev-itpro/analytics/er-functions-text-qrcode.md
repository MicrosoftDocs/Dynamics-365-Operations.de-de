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
# <a name="QRCODE">QRCODE EB-Funktion</a>

[!include [banner](../includes/banner.md)]

Die Funktion `QRCODE` gibt den Wert *Container* zurück, der das QR-Code-Bild (Quick Response Code) für die angegebene Zeichenfolge im Binärformat darstellt.

## <a name="syntax"></a>Syntax

```
QRCODE (text)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Der Wert *String*, der den Originaltext darstellt.

## <a name="return-values"></a>Rückgabewerte

*Container*

Der resultierende binäre Stream.

## <a name="example"></a>Beispiel

Sie können ein EB-Format (elektronische Berichtserstellung) konfigurieren, um ein ausgehendes Dokument im Microsoft Office-Format (Excel-Arbeitsmappen oder Word-Dokumente) mithilfe einer vordefinierten Vorlage zu generieren. Diese Vorlage kann das Objekt **Bild** (Excel-Arbeitsmappe) oder eine **Picture Content Control** (Word-Dokument) als Platzhalter für ein QR-Codebild enthalten. Sie müssen dem konfigurierten EB-Format das Element **Zelle** hinzufügen, das zum Ausfüllen dieses Platzhalters verwendet wird. Um festzulegen, welche Informationen in einem QR-Code gespeichert werden, müssen Sie eine Bindung für das Element **Zelle** definieren. Beispielsweise können Sie eine solche Bindung so konfigurieren, dass sie den folgenden Ausdruck enthält:

```
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Wenn Sie das konfigurierte EB-Format ausführen, wird der Textwert des Feldes **LabelText** von der Datenquelle **model.ListOfShelfLabels** verwendet, um ein QR-Codebild zu generieren. Dieses Bild ersetzt einen Platzhalter für ein QR-Code-Bild in der Dokumentvorlage, mit dem ein ausgehendes Dokument generiert wird. Wenn dieses Bild des generierten Dokuments gescannt wird, wird der Text zurückgegeben, der aus dem Feld **LabelText** der Datenquelle **model.ListOfShelfLabels** bezogen wurde. Weitere Informationen erhalten Sie unter [Einbetten von Bildern und Formen in generierten Dokumenten mithilfe von EB](electronic-reporting-embed-images-shapes.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)
