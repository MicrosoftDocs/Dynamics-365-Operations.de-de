---
title: EB-Funktion Base64StringToContainer
description: In diesem Artikel werden Informationen zur Verwendung der Base64StringToContainer-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 96dfffc3d899f1106c6c931efb08c941f5b3c1a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291233"
---
# <a name="base64stringtocontainer-er-function"></a>EB-Funktion Base64StringToContainer

[!include [banner](../includes/banner.md)]

Die `BASE64STRINGTOCONTAINER`-[Funktion](er-formula-language.md#Functions) konvertiert die angegebene Eingabe des Datentyps *String* in ein Datenelement des Typs *[Container](er-functions-category-container.md)*.

## <a name="syntax"></a>Syntax

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>Argumente

`input`: *String*

Der gültige Pfad einer Datenquelle des Typs *String*.

## <a name="return-values"></a>Rückgabewerte

*Behälter*

Der resultierende Binärwert im BLOB-Format (Binary Large Object).

## <a name="usage-notes"></a>Anwendungshinweise

Die Ausnahme „Parameter ist ungültig“ wird ausgegeben, wenn die Eingabezeichenfolge keine korrekte Base64-Gruppe von Binär-Text-Codierungsschemata enthält.

## <a name="example"></a>Beispiel

Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:

- Die Stammdatenquelle **DocuTypeGroupEnum** des Typs *Dynamics 365 for Operations / Aufzählung*, die sich auf die Anwendungsaufzählung **DocuTypeGroup** bezieht
- Die Stammdatenquelle **Debitor** des Typs *Dynamics 365 for Operations / Tabellendatensätze*, die auf die Anwendungstabelle **CustTable** verweist
- Die Datenaquelle **\#Medien** des Typs *Berechnetes Feld*, die folgendermaßen konfiguriert ist:

    - Sie wird als untergeordnete Datenquelle der Datenquelle **Debitor** hinzugefügt.
    - Sie enthält den Ausdruck `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.

- Die Datenquelle **\#MediaAsBase64String** des Typs *Berechnetes Feld*, die folgendermaßen konfiguriert ist:

    - Sie wird als untergeordnete Datenquelle der Datenquelle **Debitor.'\#Medien'** hinzugefügt.
    - Sie enthält den Ausdruck `Customer.'#Media'.'getFileContentAsBase64String()'`.

- Die Datenquelle **\#BlobFomBase64** des Typs *Berechnetes Feld*, die folgendermaßen konfiguriert ist:

    - Sie wird als untergeordnete Datenquelle der Datenquelle **Debitor.'\#Medien'** hinzugefügt.
    - Sie enthält den Ausdruck `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.

In diesem Beispiel codiert die Datenquelle **\#MediaAsBase64String** den binären Inhalt des aktuellen Medienanhangs als Text, der eine Base64-Gruppe von Binär-Text-Codierungsschemata darstellt. Die Datenquelle **\#BlobFomBase64** decodiert die Base64-Zeichenfolge und gibt einen Binärwert im BLOB-Format zurück.

![Beispieldatenquelle auf der Seite des EB-Modellzuordnungsdesigners.](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Containerfunktionen](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
