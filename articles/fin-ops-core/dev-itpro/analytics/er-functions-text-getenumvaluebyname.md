---
title: GETENUMVALUEBYNAME EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der GETENUMVALUEBYNAME-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 09/23/2020
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
ms.openlocfilehash: eb0c4818c8d5020125d198da4ceb0562605da397
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285968"
---
# <a name="getenumvaluebyname-er-function"></a>GETENUMVALUEBYNAME EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `GETENUMVALUEBYNAME` sucht nach dem bestimmten Wert *Enum* in der angegebenen Aufzählungsdatenquelle unter Verwendung des Aufzählungsnamens, der mit dem Wert *String* angegeben ist. Wenn der Wert *Enum* gefunden wird, gibt die Funktion ihn zurück. Andernfalls gibt die Funktion den Aufzählungswert **Null** zurück.

## <a name="syntax"></a>Syntax

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumente

`enumeration data source path`: *Aufzählung*

Der gültige Pfad einer Datenquelle eines der folgenden Aufzählungstypen:

- Modellenumeration für die elektronische Berichterstellung (EB)
- EB-Formatenumeration
- Microsoft Dynamics 365 Finance-Aufzählung

`enumeration value text`: *String*

Ein Zeichenfolgewert, der den Namen eines einzelnen Aufzählungswerts darstellt.

## <a name="return-values"></a>Rückgabewerte

Nullbar *Enum*

Der resultierende Aufzählungswert.

## <a name="usage-notes"></a>Anwendungshinweise

Es wird keine Ausnahme ausgelöst, wenn ein Wert *Enum* nicht unter Verwendung des Namens des Aufzählungswerts gefunden wird, der mit dem Wert *String* angegeben ist.

## <a name="example-1"></a>Beispiel 1

In der folgenden Abbildung wird die Aufzählung **ReportDirection** in einem Datenmodell eingeführt. Beachten Sie, dass Beschriftungen für Enumerationswerte definiert werden.

![Verfügbare Werte für eine Datenmodellenumeration.](./media/ER-data-model-enumeration-values.PNG)

Die folgende Abbildung zeigt diese Details an:

- Die Datenquelle **$Direction** wird in einem EB-Bericht konfiguriert. Diese Datenquelle wird basierend auf der Modellenumeration **ReportDirection** konfiguriert.
- Der Ausdruck `$IsArrivals` ist dazu konzipiert, die auf der Modellenumeration basierende Datenquelle **$Direction** als Parameter dieser Funktion zu verwenden.
- Der Wert dieses Vergleichswerts lautet **TRUE**.

![Beispiel einer Datenmodellenumeration.](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>Beispiel 2

Die Funktionen `GETENUMVALUEBYNAME` und [`LISTOFFIELDS`](er-functions-list-listoffields.md) ermöglichen das Abrufen von Werten und Bezeichnungen unterstützter Enumerationen als Textwerte. (Die unterstützten Enumerationen sind Anwendungsenumerationen, Datenmodellenumerationen und Formatenumerationen.)

In der folgenden Abbildung wird die Datenquelle **TransType** in einer Modellzuordnung eingeführt. Diese Datenquelle bezieht sich auf die Anwendungsenumeration **LedgerTransType**.

![Datenquelle einer Modellzuordnung, die sich auf eine Anwendungsenumeration bezieht.](./media/er-functions-text-getenumvaluebyname-example2-1.png)

Die folgende Abbildung zeigt die Datenquelle **TransTypeList**, die in einer Modellzuordnung konfiguriert ist. Diese Datenquelle wird basierend auf der Anwendungsenumeration **TransType** konfiguriert. Die Funktion `LISTOFFIELDS` wird verwendet, um alle Enumerationswerte als Liste von Datensätzen zurückzugeben, die Felder enthalten. Auf diese Weise werden die Details jedes Enumerationswerts angezeigt.

> [!NOTE]
> Das Feld **EnumValue** ist für die Datenquelle **TransTypeList** konfiguriert, wofür der Ausdruck `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` verwendet wird. Dieses Feld gibt einen Enumerationswert für jeden Datensatz in dieser Liste zurück.

![Datenquelle einer Modellzuordnung, die alle Enumerationswerte einer ausgewählten Enumeration als Liste von Datensätzen zurückgibt.](./media/er-functions-text-getenumvaluebyname-example2-2.png)

Die folgende Abbildung zeigt die Datenquelle **VendTrans**, die in einer Modellzuordnung konfiguriert ist. Diese Datenquelle gibt Lieferantentransaktionsdatensätze aus der Anwendungstabelle **VendTrans** zurück. Der Sachkontotyp jeder Transaktion wird durch den Wert im Feld **TransType** definiert.

> [!NOTE]
> Das Feld **TransTypeTitle** ist für die Datenquelle **VendTrans** konfiguriert, wofür der Ausdruck `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` verwendet wird. Dieses Feld gibt die Bezeichnung eines Enumerationswerts der aktuellen Transaktion als Text zurück, wenn dieser Enumerationswert verfügbar ist. Andernfalls wird eine leere Zeichenfolge zurückgegeben.
>
> Das Feld **TransTypeTitle** ist an das Feld **LedgerType** eines Datenmodells gebunden, mit dem diese Informationen in jedem EB-Format verwendet werden können, das dieses Datenmodell als Datenquelle verwendet.

![Datenquelle einer Modellzuordnung, die Lieferantentransaktionen zurückgibt.](./media/er-functions-text-getenumvaluebyname-example2-3.png)

Die folgende Abbildung zeigt, wie Sie den [Datenquellen-Debugger](er-debug-data-sources.md) verwenden können, um die konfigurierte Modellzuordnung zu testen.

![Verwenden des Datenquellen-Debuggers zum Testen der konfigurierten Modellzuordnung.](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

Das Feld **LedgerType** eines Datenmodells legt erwartungsgemäß Bezeichnungen von Transaktionstypen offen.

Wenn Sie diesen Ansatz für eine große Menge von Transaktionsdaten verwenden möchten, müssen Sie die Ausführungsleistung berücksichtigen. Weitere Informationen finden Sie unter [Überwachen der Ausführung von EB-Formaten zur Behebung von Leistungsproblemen](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)

[Überwachen der Ausführung von ER-Formaten zur Behebung von Leistungsproblemen](trace-execution-er-troubleshoot-perf.md)

[LISTOFFIELDS EB-Funktion](er-functions-list-listoffields.md)

[FIRSTORNULL EB-Funktion](er-functions-list-firstornull.md)

[WHERE EB-Funktion](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
