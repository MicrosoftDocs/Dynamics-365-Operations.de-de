---
title: GETLABELTEXT ER-Funktion
description: In diesem Artikel finden Sie Informationen zur Verwendung der Funktion GETLABELTEXT bei der elektronischen Berichterstellung (EB).
author: NickSelin
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: cb3af10d4725e87190f901aa99378e10bdf05bee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877066"
---
# <a name="getlabeltext-er-function"></a>GETLABELTEXT ER-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `GETLABELTEXT` sucht nach einem bestimmten Label und gibt einen *[String](er-formula-supported-data-types-primitive.md#string)*-Wert zurück, der die Übersetzung des angegebenen Labels in der angegebenen Sprache darstellt.

## <a name="syntax"></a>Syntax

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Argumente

### <a name="label-id"></a>Beschriftungskennung

`label id`: *String* oder *Label Id*

Die gültige ID eines der folgenden Label-Typen:

- [Elektronische Berichterstattung (ER)](general-electronic-reporting.md) Label
- Microsoft Dynamics 365 Finance-Bezeichnung

#### <a name="usage-notes"></a>Anwendungshinweise

Dieses Argument kann nur als Konstante definiert werden, indem eines der folgenden unterstützten Muster verwendet wird:

- Für ER Labels:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Für Finance Labels:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Zur Entwurfszeit wird auf der Seite **[Formulardesigner](er-advanced-formula-editor.md)** eine Fehlermeldung angezeigt, wenn unter Verwendung der angegebenen Label-ID kein Label gefunden werden kann.

### <a name="language"></a>Sprache

`language`: *String*

Eine Zeichenfolge, die einen Sprachcode darstellt.

#### <a name="usage-notes"></a>Anwendungshinweise

Dieses Argument kann entweder als Textkonstante oder als Pfad eines Datenquellenfeldes definiert werden, das einen *String*-Wert zurückgibt.

> [!NOTE]
> Zur Entwurfszeit wird eine Fehlermeldung angezeigt, wenn mit dem angegebenen Argument `language` kein Sprachcode gefunden werden kann, wenn es als Textkonstante definiert wurde.
>
> Zur Laufzeit wird für ein angegebenes Label die Übersetzung für die Systemsprache `EN-US` zurückgegeben, wenn mit dem angegebenen Argument `language` kein Sprachcode gefunden wurde.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example-1-system-label"></a><a name=example-1></a>Beispiel 1: System-Label

Die Ausdrücke `GETLABELTEXT (@"SYS70894", "en-us")` und `GETLABELTEXT ("SYS70894", "en-us")` geben die englische Übersetzung „Nothing to print“ für das Anwendungsetikett `@SYS70894` zurück.

## <a name="example-2-er-label"></a><a name=example-2></a>Beispiel 2: ER Label

Sie beginnen mit der Bearbeitung einer ER [Konfiguration](general-electronic-reporting.md#Configuration), die aus der **ISO20022 Überweisung (DE)** Konfiguration [abgeleitet](er-quick-start2-customize-report.md#DeriveProvidedFormat) wurde, geben eine neue Datenquelle vom Typ *[Berechnetes Feld](er-calculated-field-ds-performance.md)* ein und konfigurieren den Ausdruck `GETLABELTEXT(@"GER_LABEL:VendorName", "de")` für diese Datenquelle. In diesem Fall gibt die Datenquelle zur Laufzeit die deutsche Übersetzung „Kreditorenname“ für das Label `@GER_LABEL:VendorName` ER zurück, das ursprünglich in der Basis-Konfiguration **ISO20022 Überweisung (DE)** ER konfiguriert wurde.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)

[Entwerfen Sie mehrsprachige Berichte in der elektronischen Berichterstellung](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
