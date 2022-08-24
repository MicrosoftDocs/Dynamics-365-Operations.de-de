---
title: NUMSEQVALUE EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der NUMSEQVALUE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 62255f0a47d3c67468cf2cf3922a1886c29c03d6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271552"
---
# <a name="numseqvalue-er-function"></a>NUMSEQVALUE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `NUMSEQVALUE` gibt den Wert *String* zurück, der den neu generierten Wert einer Zahlenfolge basierend auf der angegebenen Zahlenfolge, dem Gültigkeitsbereich und der Gültigkeitsbereichskennung darstellt. Die Bereichs-ID entspricht dem Buchungscode, der von dem Kontext bereitgestellt wird, in dem das Format für die elektronische Berichterstellung (EB) ausgeführt wird.

## <a name="syntax-1"></a>Syntax 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>Syntax 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>Syntax 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>Argumente

`number sequence code`: *String*

Ein Textwert, der den Code der Zahlenfolge darstellt, in der ein neuer Wert erforderlich ist.

`number sequence record ID`: *Int64*

Der Wert *Int64*, der die Datensatz-ID eines Datensatzes in der NumberSequenceTable-Tabelle darstellt, die die Definition der Nummernfolge enthält, in der ein neuer Wert erforderlich ist.

`scope type`: *Enum value*

Ein Aufzählungswert der Aufzählung **ERExpressionNumberSequenceScopeType**, die den Umfang der Zahlenfolge definiert, in der ein neuer Wert erforderlich ist. Die verfügbaren Bereichstypen sind **Geteilt**, **Juristische Person** und **Unternehmen**.

`scope ID`: *String*

Der Wert *String*, der den Bereich basierend auf dem angegebenen Bereichstyp identifiziert.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="usage-notes"></a>Anwendungshinweise

Für den Bereichstyp **Gemeinsam genutzt** geben Sie eine Nullkette als die Bereichs-ID an.

Für die Bereichstypen **Unternehmen** und **Juristische Person** geben Sie den Unternehmenscode als die Bereichs-ID an. Wenn Sie eine Nullkette als Bereichs-ID für diese Bereichstypen angeben, wird der aktuelle Buchungskreis verwendet.

Bei Verwendung von Syntax 1 wird die Nummernfolge für den Bereichstyp **Unternehmen** angefordert, und der Buchungskreis wird durch den Kontext bereitgestellt, in dem das EB-Format ausgeführt wird.

## <a name="example-1"></a>Beispiel 1

In Ihrem EB-Format definieren Sie die Datenquelle **AskNumSeq** des Typs *Benutzereingabeparameter*. Diese Datenquelle bezieht sich auf den Extended Data Type (EDT) **Beschreibung**. Als Nächstes definieren Sie die Datenquelle **NumSeq** des Typs *Berechnetes Feld*. Diese Datenquelle enthält den Ausdruck `NUMSEQVALUE (AskNumSeq)`. Wenn die Datenquelle **NumSeq** aufgerufen wird, gibt sie den neu generierten Wert der Zahlenfolge zurück, der zur Laufzeit durch Eingabe des Codes im Dialogfeld angegeben wurde. Die Nummernfolge wird für den Bereichstyp **Unternehmen** angefordert. Der Buchungscode wird vom Kontext bereitgestellt, in dem das EB-Format ausgeführt wird.

## <a name="example-2"></a>Beispiel 2

Die folgenden Datenquellen sind in Ihrer Modellzuordnung definiert.

- Die Datenquelle **LedgerParms** des Typs *Tabelle* . Diese Datenquelle bezieht sich auf die LedgerParameters-Tabelle.
- Die Datenquelle **NumSeq** des Typs *Berechnetes Feld*. Diese Datenquelle enthält den Ausdruck `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.

Wenn die Datenquelle **NumSeq** aufgerufen wird, wird er dem generierten neuen Wert des Gen 1 Nummernkreis zurückgegeben, der für die Hauptbuch-Parameter für das Unternehmen konfiguriert wurde, der den Kontext liefert, unter dem das ER-Format ausgeführt wird. Dieser Nummernkreis kennzeichnet eindeutige Erfassungen und fungiert als eine Chargennummer, die die Buchungen zusammen verknüpft.

## <a name="example-3"></a>Beispiel 3

Die folgenden Datenquellen sind in Ihrer Modellzuordnung definiert.

- Die Datenquelle **enumScope** des Typs *Aufzählung* von Microsoft Dynamics 365 Finance. Diese Datenquelle bezieht sich auf die Aufzählung **ERExpressionNumberSequenceScopeType**.
- Die Datenquelle **NumSeq** des Typs *Berechnetes Feld*. Diese Datenquelle enthält den Ausdruck `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.

Wenn die Datenquelle **NumSeq** aufgerufen wird, wird er dem generierten neuen Wert des **Gen \_1** Nummernkreis zurückgegeben, der für das Unternehmen konfiguriert wurde, der den Kontext liefe, unter dem das ER-Format ausgeführt wird.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Andere (geschäftsdomänenspezifische) Funktionen](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
