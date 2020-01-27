---
title: Liste der EB-Funktionen in der geschäftsdomänenspezifischen Kategorie
description: Dieses Thema enthält Informationen zu den geschäftsdomänenspezifischen Funktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
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
ms.openlocfilehash: 5a1d9869584d0f98e2ce00b1bca669395b43ca6f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916590"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>Liste der EB-Funktionen in der geschäftsdomänenspezifischen Kategorie

[!include [banner](../includes/banner.md)]

Mit domänenspezifischen Funktionen für die elektronische Berichterstellung (EB) können Berechnungen und Datenzugriffsanforderungen ausgeführt werden, die für die Implementierung von Microsoft Dynamics 365 Finance spezifisch sind. Dieses Thema enthält eine Zusammenfassung dieser Funktionen.

## <a name="list-of-supported-functions"></a>Liste der unterstützten Funktionen

| Funktion| Beschreibung |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | Diese Funktion gibt den Wert *String* zurück, der eine Gläubigerreferenz als MOD10-Ausdruck basierend auf den Ziffern der angegebenen Rechnungsnummer darstellt. |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | Diese Funktion gibt den Wert *String* zurück, der eine einzelne Finanzdimensions-ID darstellt, die der angegebenen Zeichenfolge entnommen wird. Die angegebene Zeichenfolge zeigt alle Dimensionen als durch Kommata getrennte ID-Listen an. |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | Diese Funktion gibt den Wert *Real* zurück, der das Konvertieren des angegebenen Geldbetrags aus der angegebenen Ausgangswährung in die angegebene Zielwährung darstellt, indem die Einstellungen des angegebenen Unternehmens am angegebenen Datum verwendet werden. |
| [CurCredRef](er-functions-other-curcredref.md) | Diese Funktion gibt den Wert *String* zurück, der eine Gläubigerreferenz basierend auf den Ziffern der angegebenen Rechnungsnummer darstellt. |
| [FA_Balance](er-functions-other-fabalance.md) | Diese Funktion gibt den Wert *Container (Datensatz)* zurück, der aus Daten für den Anlagensaldo für die angegebene Anlagenposition, dem Wertmodellcode, dem Berichtsjahr und dem Berichtsdatum besteht. |
| [FA_Sum](er-functions-other-fasum.md) | Diese Funktion gibt den Wert *Container (Datensatz)* zurück, der aus Daten für die Anlagenbeträge für die angegebene Anlagenposition, dem Wertmodellcode und den Datumszeiträumen besteht. |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | Diese Funktion gibt den Wert *String* zurück, der den Code für die juristische Person (Unternehmen) darstellt, bei dem ein Benutzer derzeit angemeldet ist. |
| [ISOCredRef](er-functions-other-isocredref.md) | Diese Funktion gibt den Wert *String* zurück, der eine Gläubigerreferenz der Internationale Organisation für Normung (ISO) basierend auf den Ziffern und alphabetischen Symbolen der angegebenen Rechnungsnummer darstellt. |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | Diese Funktion gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Zeichenfolge eine gültige internationale Bankkontonummer (IBAN) darstellt. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück. |
| [Mod_97](er-functions-other-mod97.md) | Diese Funktion gibt den Wert *String* zurück, der eine Gläubigerreferenz als MOD97-Ausdruck basierend auf den Ziffern der angegebenen Rechnungsnummer darstellt. |
| [NumSeqValue](er-functions-other-numseqvalue.md) | Diese Funktion gibt den Wert *String* zurück, der den neu generierten Wert einer Zahlenfolge basierend auf der angegebenen Zahlenfolge, dem Gültigkeitsbereich und der Gültigkeitsbereichskennung darstellt. Die Bereichs-ID entspricht dem Buchungscode, der von dem Kontext bereitgestellt wird, in dem das EB-Format ausgeführt wird. |
| [RoundAmount](er-functions-other-roundamount.md) | Diese Funktion gibt den Wert *Real* zurück, der das Ergebnis der Rundung des angegebenen Betrags auf die angegebene Anzahl von Dezimalstellen gemäß der angegebenen Rundungsregel darstellt. |
| [TableName2ID](er-functions-other-tablename2id.md) | Diese Funktion gibt eine numerische Darstellung der Tabellen-ID für den angegebenen Tabellennamen mit dem Wert *Ganzzahl* zurück. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)
