---
title: Liste der EB-Funktionen in der Listenkategorie
description: Dieses Thema enthält Informationen zu den Listenfunktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2e708c59bceebf845ee78c98057133bb2892cf9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686174"
---
# <a name="list-of-er-functions-in-the-list-category"></a>Liste der EB-Funktionen in der Listenkategorie

[!include [banner](../includes/banner.md)]

Mithilfe der Listenfunktionen für die elektronische Berichterstellung (EB) können Informationen aus den Datenquellen der Datentypen *Datensatzliste* und *Container (Datensatz)* extrahiert werden. Dieses Thema enthält eine Zusammenfassung dieser Funktionen.

## <a name="list-of-supported-functions"></a>Liste der unterstützten Funktionen

| Funktion | Beschreibung |
|----------|-------------|
| [AllItems](er-functions-list-allitems.md)                 | Diese Funktion wurde als Auswahl im Arbeitsspeicher ausgeführt. Es wird ein neuer vereinfachter Wert von *Datensatzliste* zurückgegeben, der aus einer Liste von Datensätzen besteht, die alle Elemente darstellen, die dem angegebenen Pfad entsprechen. |
| [AllItemsQuery](er-functions-list-allitemsquery.md)       | Diese Funktion wird als verknüpfte SQL-Abfrage ausgeführt. Es wird ein neuer vereinfachter Wert von *Datensatzliste* zurückgegeben, der aus einer Liste von Datensätzen besteht, die alle Elemente darstellen, die dem angegebenen Pfad entsprechen. |
| [Anzahl](er-functions-list-count.md)                       | Diese Funktion gibt den Wert *Ganzzahl* zurück, der die Anzahl der Datensätze in der angegebenen Liste darstellt, wenn die Liste nicht leer ist. Wenn die Liste leer ist, gibt diese Funktion **0** (Null) zurück. |
| [EmptyList](er-functions-list-emptylist.md)               | Diese Funktion gibt den Wert *Datensatzliste* zurück, indem eine angegebene Liste als Quelle für die Listenstruktur verwendet wird.|
| [Aufzählung](er-functions-list-enumerate.md)               | Diese Funktion gibt einen neuen Wert von *Datensatzliste* zurück, der aus Aufzählungsdatensätzen der angegebenen Liste besteht. |
| [Filtern](er-functions-list-filter.md)                     | Diese Funktion gibt die angegebene Liste als Wert *Datensatzliste* zurück, nachdem die Abfrage so geändert wurde, dass sie nach der angegebenen Bedingung filtert. |
| [Zuerst](er-functions-list-first.md)                       | Diese Funktion gibt den ersten Datensatz der angegebenen Liste mit dem Wert *Container (Datensatz)* zurück, wenn diese Liste nicht leer ist. Wenn die Liste leer ist, löst diese Funktion eine Ausnahme aus. |
| [FirstOrNull](er-functions-list-firstornull.md)           | Diese Funktion gibt den ersten Datensatz der angegebenen Liste mit dem Wert *Container (Datensatz)* zurück, wenn dieser Datensatz nicht leer ist. Wenn der Datensatz leer ist, gibt diese Funktion den Wert null für *Container (Datensatz)* zurück. |
| [Index](er-functions-list-index.md)                       | Diese Funktion gibt den Wert *Container (Datensatz)* zurück, der unter Verwendung des angegebenen numerischen Index in der angegebenen Liste ausgewählt wird. Diese Funktion löst eine Ausnahme aus, wenn der Index außerhalb des Bereichs der Datensätze in der angegebenen Liste liegt. |
| [IsEmpty](er-functions-list-isempty.md)                   | Diese Funktion gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Liste keine Datensätze enthält. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück. |
| [Liste](er-functions-list-list.md)                         | Diese Funktion gibt den Wert *Datensatzliste* zurück, der aus einer neuen Liste besteht, die anhand der angegebenen Argumente erstellt wird.|
| [ListDistinct](er-functions-list-listdistinct.md)         | Diese Funktion berechnet den angegebenen Ausdruck als Selektor für jeden Datensatz der angegebenen Liste. Es wird ein neuer Wert *Datensatzliste*, der einen einzelnen Datensatz für jeden eindeutigen Auswahlwert enthält.|
| [ListJoin](er-functions-list-listjoin.md)                 | Diese Funktion gibt den Wert *Datensatzliste* zurück, der eine Liste darstellt, die anhand der angegebenen Argumente erstellt wird.|
| [ListOfFields](er-functions-list-listoffields.md)         | Diese Funktion gibt den Wert *Datensatzliste* zurück, der basierend auf der Struktur des angegebenen Arguments des Typs *Aufzählung* oder *Container (Datensatz)* erstellt wird. |
| [ListOfFirstItem](er-functions-list-listoffirstitem.md)   | Diese Funktion gibt den Wert *Datensatz* zurück, der nur aus dem ersten Datensatz der angegebenen Liste besteht.|
| [OrderBy](er-functions-list-orderby.md)                   | Diese Funktion gibt die angegebene Liste mit dem Wert *Datensatzliste* zurück, nachdem sie nach den angegebenen Argumenten sortiert wurde. Diese Argumente können als Ausdrücke definiert werden. |
| [Stornieren](er-functions-list-reverse.md)                   | Diese Funktion gibt die angegebene Liste mit dem Wert *Datensatzliste* in umgekehrter Sortierreihenfolge zurück. |
| [Teilen](er-functions-list-split.md)                       | Diese Funktion teilt die angegebene Eingabezeichenfolge in Teilzeichenfolgen auf und gibt das Ergebnis als neuen Wert *Datensatzliste* zurück. |
| [SplitList](er-functions-list-splitlist.md)               | Diese Funktion teilt die angegebene Liste in Unterlisten (oder Batches), die jeweils die angegebene Anzahl von Datensätzen enthalten. Sie gibt dann das Ergebnis als neuen Wert *Datensatzliste* zurück, der aus den Batches besteht. |
| [SplitListByLimit](er-functions-list-splitlistbylimit.md) | Diese Funktion teilt die angegebene Liste in eine neue Liste von Unterlisten (Batches) auf. Die Anzahl der Datensätze in jedem Batch wird dynamisch berechnet. Die Funktion gibt dann das Ergebnis als neuen Wert *Datensatzliste* zurück, der aus den Batches besteht. |
| [StringJoin](er-functions-list-stringjoin.md)             | Diese Funktion gibt den Wert *String* zurück, der aus verketteten Werten des angegebenen Feldes aus der angegebenen Liste besteht. Die Werte können durch das angegebene Trennzeichen getrennt werden. |
| [Wobei](er-functions-list-where.md)                       | Diese Funktion gibt die angegebene Liste mit dem Wert *Datensatzliste* zurück, nachdem sie gemäß der angegebenen Bedingung gefiltert wurde. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)
