---
title: QRCODE EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der QRCODE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 12/10/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 9de62eefb82942ccc72e81bd9bf36eed07c99dba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287187"
---
# <a name="qrcode-er-function"></a>QRCODE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `QRCODE` gibt den Wert *Container* zurück, der das QR-Code-Bild (Quick Response Code) für die angegebene Zeichenfolge im Binärformat darstellt.

## <a name="syntax"></a>Syntax

```vb
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

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Wenn Sie das konfigurierte EB-Format ausführen, wird der Textwert des Feldes **LabelText** von der Datenquelle **model.ListOfShelfLabels** verwendet, um ein QR-Codebild zu generieren. Dieses Bild ersetzt einen Platzhalter für ein QR-Code-Bild in der Dokumentvorlage, mit dem ein ausgehendes Dokument generiert wird. Wenn dieses Bild des generierten Dokuments gescannt wird, wird der Text zurückgegeben, der aus dem Feld **LabelText** der Datenquelle **model.ListOfShelfLabels** bezogen wurde. Weitere Informationen erhalten Sie unter [Einbetten von Bildern und Formen in generierten Dokumenten mithilfe von EB](electronic-reporting-embed-images-shapes.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
