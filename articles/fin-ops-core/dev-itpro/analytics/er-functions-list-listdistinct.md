---
title: LISTDISTINCT EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der LISTDISTINCT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 7/30/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: d2f8e3a9d077493df3c3b7628608d31834f43f8a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876804"
---
# <a name="listdistinct-er-function"></a>LISTDISTINCT EB-Funktion

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Die `LISTDISTINCT`-Funktion berechnet den angegebenen Ausdruck als Selektor für jeden Datensatz der angegebenen Liste. Es wird ein neuer Wert *Datensatzliste*, der einen einzelnen Datensatz für jeden eindeutigen Auswahlwert enthält.

## <a name="syntax"></a>Syntax

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

`selector`: *Primitiver Datentyp*

Ein gültiger Ausdruck, mit dem ein Auswahlwert für jeden Datensatz in der angegebenen Liste berechnet wird.

Die folgenden Datentypen werden für diesen Parameter unterstützt:

- Aktiv
- Datum
- DateTime
- GUID
- Ganzzahl
- Int64
- Gleitkommazahl
- Zeichenfolge

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

Die Struktur der erstellten Liste entspricht der Struktur der angegebenen Liste.

Der gleiche Auswahlwert kann für mehrere Datensätze in der angegebenen Liste berechnet werden. In diesem Fall entsprechen die Feldwerte des entsprechenden Datensatzes in der erstellten Liste den Werten des ersten Datensatzes aus der angegebenen Liste, für die der Auswahlwert berechnet wird.

Die Ausführung dieser Funktion erfolgt auf jedem [Elektronische Berichterstattung (EB)](general-electronic-reporting.md) Datenquelle des Typs *Datensatzliste*, der im Speicher vorhanden ist.

Die Datenquelle **GROUPBY** kann auch verwendet werden, um die Liste der Datensätze zu generieren, für die der Selektor mit unterschiedlichen Werten berechnet wird. Aus Sicht der Leistung und des Speicherverbrauchs ist es jedoch besser, die Funktion `LISTDISTINCT` zu verwenden als die Datenquelle **GROUPBY**, da die Ausführung der Funktion im Speicher erfolgt.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie Sie die Liste der eindeutigen Kundenkontonummern abrufen können, für die in einem bestimmten Zeitraum mindestens eine Verkaufs- oder Projektrechnung ausgestellt wurden.

1. Geben Sie die Datenquelle **SalesInvoice** des Typs `Record list` ein, der sich auf die Anwendungstabelle **CustInvoiceJour** und Filterverkaufsrechnungen für bestimmte Zeiträume bezieht.

    Im Feld `InvoiceAccount` dieser Datenquelle wird die Kontonummer eines fakturierten Kunden angegeben.

2. Geben Sie die Datenquelle **ProjectInvoice** des Typs `Record list` ein, der sich auf die Anwendungstabelle **ProjInvoiceJour** und Filterprojektrechnungen für bestimmte Zeiträume bezieht.

    Im Feld `InvoiceAccount` dieser Datenquelle wird die Kontonummer eines fakturierten Kunden angegeben.

3. Konfigurieren Sie die Datenquelle **AllInvoices** des Typs `Calculated field`, der den Ausdruck `LISTJOIN(SalesInvoice, ProjectInvoice)` enthält.

    Diese Datenquelle gibt die verknüpfte Liste der Verkaufsrechnungen und Projektrechnungen zurück.

4. Konfigurieren Sie die Datenquelle **InvoicedCustomer** des Typs `Record list`, der den Ausdruck `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)` enthält.

    Diese Datenquelle gibt eine neue Liste zurück, die einen einzelnen Datensatz für jeden einzelnen Kunden enthält, der während des definierten Zeitraums in Rechnung gestellt wurde. Das Feld `InvoiceAccount` dieser Liste enthält eine Kundenkontonummer.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]