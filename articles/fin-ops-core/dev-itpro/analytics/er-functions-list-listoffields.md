---
title: LISTOFFIELDS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LISTOFFIELDS-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: c288050fa1f9f1be9c38696e844e782794795471
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745080"
---
# <a name="listoffields-er-function"></a>LISTOFFIELDS EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `LISTOFFIELDS` gibt den Wert *Datensatzliste* zurück, der basierend auf der Struktur des angegebenen Arguments des Typs *Enumeration* oder *Container (Datensatz)* erstellt wird.

## <a name="syntax-1"></a>Syntax 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>Syntax 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>Argumente

`path`: Referenz der Datenquelle

Der gültige Referenzpfad einer Datenquelle einer der folgenden Datentypen:

- Modellenumeration
- Formatenumeration
- Anwendungsaufzählung
- Container (Datensatz)

`language`: *String*

Text, der einen Sprachcode darstellt.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

Die Liste, die erstellt wird, besteht aus Datensätzen, die die folgenden Felder haben:

- **Name** (Datentyp *String*)
- **Bezeichnung** (Datentyp *String*)
- **Beschreibung** (Datentyp *String*)
- **IsTranslated** (Datentyp *Boolesch*)

Wenn das Argument `path` sich auf eine Datenquelle des Typs *Container (Datensatz)* bezieht, geben Sie für jedes Feld des referenzierten Datensatzes, auf den verwiesen wird, einen neuen Datensatz in die Liste ein, die erstellt wird. Für jeden erstellten Datensatz gibt das Feld **Name** den Namen des Felds des referenzierten Containerdatensatzes zurück, für den der aktuelle Datensatz erstellt wurde.

Wenn das Argument `path` sich auf eine Datenquelle einer der Typen *Enumeration* bezieht, geben Sie für jeden Enumerationswert der referenzierten Enumeration, auf die verwiesen wird, einen neuen Datensatz in die Liste ein, die erstellt wird. Für jeden erstellten Datensatz gibt das Feld **Name** den Wert der referenzierten Enumeration zurück, für die der aktuelle Datensatz erstellt wurde, das Feld **Beschreibung** gibt die Beschreibung dieser Enumeration zurück, und das Feld **Bezeichnung** gibt die Bezeichnung dieser Enumeration zurück.

Wenn zur Laufzeit die Syntax 1 verwendet wird, müssen die Felder **Bezeichnung** und **Beschreibung** Werte zurückgeben, die auf den Spracheinstellungen des elektronischen Berichterstellungsformats (EB) basieren, das ausgeführt wird:

- Wenn die Bezeichnungen und Beschreibungen für die angeforderte Sprache verfügbar sind, geben die Felder **Bezeichnung** und **Beschreibung** Werte zurück, die auf dieser Sprache basieren, und das Feld **IsTranslated** gibt **True** zurück.
- Wenn die Bezeichnungen und Beschreibungen für die angeforderte Sprache nicht verfügbar sind, geben die Felder **Bezeichnung** und **Beschreibung** Werte zurück, die auf der Standardsprache **EN-US** basieren, und das Feld **IsTranslated** gibt **False** zurück.

Wenn zur Laufzeit die Syntax 2 verwendet wird, müssen die Felder **Bezeichnung** und **Beschreibung** Werte zurückgeben, die auf den Spracheinstellungen basieren, die als zweites Argument der aufgerufenen Funktion definiert sind:

- Wenn die Bezeichnungen und Beschreibungen für die angeforderte Sprache verfügbar sind, geben die Felder **Bezeichnung** und **Beschreibung** Werte zurück, die auf dieser Sprache basieren, und das Feld **IsTranslated** gibt **True** zurück.
- Wenn die Bezeichnungen und Beschreibungen für die angeforderte Sprache nicht verfügbar sind, geben die Felder **Bezeichnung** und **Beschreibung** Werte zurück, die auf der Standardsprache **EN-US** basieren, und das Feld **IsTranslated** gibt **False** zurück.

## <a name="example-1"></a>Beispiel 1

In der folgenden Abbildung wird eine Aufzählung in einem EB-Datenmodell vorgestellt.

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

Die folgende Abbildung zeigt diese Details an:

- Die Modellaufzählung ist eingefügt in einen Bericht als Datenquelle.
- Ein EB-Ausdruck verwendet die Modellaufzählung als Parameter der Funktion `LISTOFFIELDS`.
- Eine Datenquelle des Typs *Datensatzliste* wird in einen Bericht mithilfe des EB-Ausdrucks eingefügt, der erstellt wird.

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

Das folgende Beispiel zeigt die EB-Formatelemente, die an die Datenquelle des Typs *Datensatzliste* gebunden sind, der mithilfe der Funktion `LISTOFFIELDS` erstellt wurde.

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

Die folgende Abbildung zeigt das Ergebnis, wenn das entworfene Format ausgeführt wird.

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> Basierend auf den Spracheinstellungen des Formats von übergeordneten **DATEI**- und **ORDNER**-Elementen, wird übersetzter Text für Beschriftungen und Beschreibungen in der Ausgabe des EB-Formats eingegeben.

## <a name="example-2"></a>Beispiel 2

Sie verwenden den Datenquellentyp *Berechnetes Feld*, um die Datenquellen **enumType\_de** und **enumType\_deCH** für die Datenmodellaufzählung **enumType** zu konfigurieren:

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

In diesem Fall können Sie den folgenden Ausdruck verwenden, um die Beschriftung des Aufzählungswerts in Schweizer Deutsch abzurufen, wenn diese Übersetzung verfügbar ist. Wenn die schweizerdeutsche Übersetzung nicht verfügbar ist, ist das Etikett auf Deutsch.

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)
