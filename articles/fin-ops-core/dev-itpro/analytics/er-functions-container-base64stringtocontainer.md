---
title: EB-Funktion Base64StringToContainer
description: In diesem Thema werden Informationen zur Verwendung der Base64StringToContainer-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 6fd08d9a2522bdf497b1926c884a4583065d9f19
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754373"
---
# <a name="base64stringtocontainer-er-function"></a>EB-Funktion Base64StringToContainer

[!include [banner](../includes/banner.md)]

Die `BASE64STRINGTOCONTAINER`-[Funktion](er-formula-language.md#functions) konvertiert die angegebene Eingabe des Datentyps *String* in ein Datenelement des Typs *[Container](er-functions-category-container.md)*.

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

- Die Stammdatenquelle **DocuTypeGroupEnum** des Typs *Dynamics 365 for Operations/Aufzählung*, die sich auf die Anwendungsaufzählung **DocuTypeGroup** bezieht
- Die Stammdatenquelle **Debitor** des Typs *Dynamics 365 for Operations/Tabellendatensätze*, die auf die Anwendungstabelle **CustTable** verweist
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

![Beispieldatenquelle auf der Seite des EB-Modellzuordnungsdesigners](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Containerfunktionen](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]