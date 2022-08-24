---
title: Liste der EB-Funktionen in der Datenerfassungskategorie
description: Dieser Artikel enthält Informationen zu den Datenerfassungsfunktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: e01bed49646ffe344004f9eb51e9013e1b4c5430
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286148"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>Liste der EB-Funktionen in der Datenerfassungskategorie

[!include [banner](../includes/banner.md)]

Datenerfassungsfunktionen für die elektronische Berichterstellung (EB) werden verwendet, um basierend auf den Daten der Ausgabe, die bereits im Format **Text** oder **Xml** generiert wurden, in einem EB-Format zu zählen und zu summieren, das gerade ausgeführt wird. Dieser Ansatz wird verwendet, um die Leistung eines ausgeführten EB-Formats zu verbessern, um Werte für laufende Summen in generierte Dokumente sowie für andere Zwecke einzugeben. Dieser Artikel enthält eine Zusammenfassung dieser Funktionen.

## <a name="list-of-supported-functions"></a>Liste der unterstützten Funktionen

| Funktion | Beschreibung |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | Diese Funktion gibt den Wert *Datensatzliste* zurück, der die Liste der Werte enthält, die von der Eigenschaft **Gesammelter Datenschlüsselwert** des Formatelements zurückgegeben und erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebenen Bedingungen erfüllt. Jede Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert. |
| [CountIF](er-functions-datacollection-countif.md) | Diese Funktion gibt den Wert *Ganzzahl* zurück, der die Anzahl der Formatelemente darstellt, die erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebene Bedingung erfüllt. Die Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert. |
| [CountIFs](er-functions-datacollection-countifs.md) | Diese Funktion gibt den Wert *Ganzzahl* zurück, der die Anzahl der Formatelemente darstellt, die erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebenen Bedingungen erfüllt. Jede Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert. |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | Diese Funktion gibt den Wert *String* zurück, der den Namen des aktuellen EB-Formatelements darstellt. |
| [SumIF](er-functions-datacollection-sumif.md) | Diese Funktion gibt den Wert *Real* zurück, der die Summe der Werte darstellt, die bei Bindungen der Formatelemente zurückgegeben und erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebene Bedingung erfüllt. Die Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert. |
| [SumIFs](er-functions-datacollection-sumifs.md) | Diese Funktion gibt den Wert *Real* zurück, der die Summe der Werte darstellt, die bei Bindungen der Formatelemente zurückgegeben und erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebenen Bedingungen erfüllt. Jede Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
