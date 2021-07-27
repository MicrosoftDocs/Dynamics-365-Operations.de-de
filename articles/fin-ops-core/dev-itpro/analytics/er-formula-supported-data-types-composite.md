---
title: Unterstützte zusammengesetzte Datentypen für elektronische Berichtsformeln
description: Dieses Thema enthält Informationen zu den zusammengesetzte Datentypen, die in Formeln für die elektronische Berichterstellung (EB) unterstützt werden.
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2593f3128ec103248e109f3c80f48b9d7a035f54
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355345"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>Unterstützte zusammengesetzte Datentypen für elektronische Berichtsformeln

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zu den zusammengesetzte Datentypen, die in Ausdrücke für die [elektronische Berichterstellung (EB)](general-electronic-reporting.md) unterstützt werden. Die zusammengesetzten Datentypen sind [Klasse](#class), [Container](#container), [Datensatz](#record), [Datensatzliste](#record-list), und [Objekt](#object).

## <a name="class"></a><a name="class"></a>Klasse

Der Datentyp *Klasse* bezieht sich auf eine öffentliche Anwendungsklasse. In ER wird es als [*Datensatz*](#record) dargestellt, der für jede öffentliche Methode der referenzierten Klasse ein eigenes Feld enthält. Wenn der Aufruf der Methode parametrisiert ist, müssen Sie auch die erforderlichen Argumente der entsprechenden Typen in einem ER-Ausdruck angeben, der für den Aufruf der Methode konfiguriert ist.

In den EB_Komponenten [Mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) und [Format](general-electronic-reporting.md#FormatComponentOutbound) können Sie die Datenquelle **Klasse**, die als Datenquelle dargestellt wird und einen Wert des Typs *Klasse* zurückgibt. Diese Datenquelle macht öffentliche Methoden der Klasse verfügbar, die zur Laufzeit aufgerufen werden können.

> [!NOTE]
> Aus ER-Ausdrücken können nur Methoden aufgerufen werden, die einen Wert zurückgeben.
>
> Nur Methoden mit einem Bereich von null bis acht Argumenten können von EB-Ausdrücken aufgerufen werden.

Der Standardwert einer *Klasse* ist **Null**.

Die folgende Abbildung zeigt, wie die Datenquelle **Systeminformationen (xInfo)** des Typs **Klasse** hinzugefügt wird, um die Instanz der Anwendungsklasse **xInfo** und rufen Sie ihre Methode **Produktname()** auf, um den Namen der aktuellen Anwendung zu erhalten. Der Name der aktuellen Anwendung wird zur Laufzeit durch Ausführung der `xInfo.productName`-Bindung abgerufen, die für das Feld **Softwarename (Softwarename)** des EB-Datenmodells konfiguriert wurde. Diese Bindung ruft die `productName()`-Methode der Anwendungsklasse **xInfo**, die in der aktuellen Modellzuordnung als Datenquelle **Systeminformationen (xInfo)** dargestellt wird.

[![Konfigurieren einer Klassendatenquelle im EB-Modellzuordnungsdesigner.](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

Die folgende Abbildung zeigt, wie das EB-Format konfiguriert ist, um den bereitgestellten Anwendungsnamen in generierte Dokumente einzufügen. Das Feld **Softwarename (Softwarename)** des verwendeten Datenmodells war an die Komponente **Zeichenfolge** geknüpft, die unter dem XML-Element **SoftwareGebraucht** des EB-Formats verschachtelt ist. Der Name der aktuellen Anwendung wird also zur Laufzeit an das XML-Element **softwareUsed** eines generierten Dokuments im XML-Format.

[![Struktur eines elektronischen Ausgangsdokuments im EB-Formatdesigner konfigurieren.](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>Container

Der Datentyp *Container* enthält binären Inhalt. Ein *Container*-Wert kann verwendet werden, um bestimmte Informationen aus dem Speicher an ein generiertes Dokument zu übergeben. Im EB-Framework wird dieser Datentyp häufig verwendet, um Medieninhalte wie ein Firmenlogo in generierte Dokumente einzufügen.

> [!NOTE]
> Obwohl jedes Medienelement als *Container*-Wert dargestellt werden kann, steht nicht jeder *Container*-Wert für ein Medienelement. Wenn Sie daher ein EB-Format so konfigurieren, dass es einen *Container* verwendet, um ein Bild in generierte Dokumente einzufügen, aber der referenzierte *Container* keinen Medieninhalt zurückgibt, kann eine Ausnahme ausgelöst werden, die dem folgenden Beispiel ähnelt: „Fehler beim Ausführen von Code: Binär (Objekt), Methode constructFromContainer mit ungültigen Parametern aufgerufen.“

Der Standardwert einer *Container* ist **Null**.

Die folgende Abbildung zeigt, wie das Feld **Bitmap(Bild)** vom Typ *Container* an das Datenmodellfeld **Logo** vom Typ **Container** in der Modellzuordnung **Verkaufsrechnung** gebunden ist. Diese Bindung macht das Firmenlogo für jedes EB-Format verfügbar, das für die **Verkaufsrechnung**-Root-Definition gedacht ist und verwendet diese Modellzuordnung zur Laufzeit.

[![Binden eines Felds vom Typ Container an den EB-Modellzuordnungsdesigner.](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>Aufzeichnen

Ein *Datensatz* ist eine Sammlung benannter Felder, von denen jedes mit einem Wert von entweder einem [primitiven](er-formula-supported-data-types-primitive.md) Datentyp oder einem zusammengesetzten Datentyp zugeordnet ist. Normalerweise wird ein *Datensatz* verwendet, um einen einzelnen Datensatz einer Datensatzliste darzustellen. In diesem Fall repräsentiert jedes Element einzelne Felder, Methoden und Beziehungen.

Der Standardwert eines *Datensatzes* ist **leer**.

> [!NOTE]
> Wenn Sie den Wert eines Feldes eines leeren *Datensatzes* erhalten, wird der Standardwert des entsprechenden Datentyps zurückgegeben.

Ein *Datensatz* kann mit folgenden Funktionen abgerufen werden:

- [FIRST](er-functions-list-first.md)
- [FIRSTORNULL](er-functions-list-firstornull.md)
- [EMPTYRECORD](er-functions-record-emptyrecord.md)
- [NULLCONTAINER](er-functions-record-nullcontainer.md)

Weitere Informationen zur Transformation von *Datensatz* werten, siehe [Liste der EB-Funktionen in der Listenkategorie](er-functions-category-list.md).

## <a name="record-list"></a><a name="record-list"></a>Datensatzliste

Eine *Datensatzlistr* ist eine Liste von Artikeln vom Typ *Datensatz*. Normalerweise, wird eine *Datensatzliste* verwendet, um die Liste der Datensätze darzustellen, die aus einer Datenbanktabelle abgerufen wurden.

Standardmäßig werden Datensätze einer *Datensatzliste* sequenziell aufgerufen. Um auf einen bestimmten Datensatz zuzugreifen, können Sie die [INDEX](er-functions-list-index.md)-Funktion verwenden und den *Integer*-Index spezifizieren.

Der Standardwert einer *Datensatzliste* ist **leer**. Sie können die [ISEMPTY](/er-functions-list-isempty.md)-Funktion verwenden, um auszuwerten, ob eine *Datensatzliste* leer ist.

> [!NOTE]
> Wenn eine *Datensatzliste* leer ist, bewirkt jeder Versuch, einen Feldwert für einen *Datensatz* darin abzurufen, dass zur Laufzeit eine Ausnahme ausgelöst wird. Informationen dazu, wie Sie Laufzeitausnahmen dieses Typs verhindern können, finden Sie unter [Berücksichtigung von Leerlistenfällen](er-components-inspections.md#i9).

Eine *Datensatzliste* kann mit folgenden Funktionen initiiert werden:

- [ALLITEMS](er-functions-list-allitems.md)
- [ALLITEMSQUERY](er-functions-list-allitemsquery.md)
- [EMPTYLIST](er-functions-list-emptylist.md)
- [LIST](er-functions-list-list.md)
- [LISTDISTINCT](er-functions-list-listdistinct.md)

Weitere Informationen zur Transformation von *Datensatzlisten* werten, siehe [Liste der EB-Funktionen in der Listenkategorie](er-functions-category-list.md). Um zu lernen, wie man Artikel aus *Datensatzlisten* einführt, füllen Sie sie mit Anwendungsdaten und verwenden Sie die Daten dann, um Geschäftsdokumente zu generieren, siehe [Entwerfen Sie eine neue EB-Lösung zum Drucken eines benutzerdefinierten Berichts](er-quick-start1-new-solution.md).

## <a name="object"></a><a name="object"></a>Objekt

Ein *Objekt* verweist auf eine zustandsbehaftete Instanz von einer *Klasse*. Normalerweise wird ein *Objekt* im Quellcode initiiert. Es wird dann an eine EB-Modellzuordnung übergeben und liefert Details zum Ausführungskontext.

Der Standardwert eines *Objekts* ist **Null**.

Die folgende Abbildung zeigt, wie die Datenquelle **ReportDataContract** vom Typ *Objekt* hinzugefügt wird, um Informationen über eine generierte Rechnung aus dem Quellcode an die Modellzuordnung **Projektrechnung**. Beispielsweise wird der Rechnungsinstanztext als Teil des Ausführungskontexts übergeben. Dieser Text wird zur Laufzeit durch die Ausführung der `ReportDataContract.parmInvoiceInstanceText`-Bindung abgerufen, die für das Feld **Hinweis** des EB-Datenmodells konfiguriert wurde. Diese Bindung ruft die `parmInvoiceInstanceText()`-Methode der Anwendungsklasse **PSAProjInvoiceContract**, die in der aktuellen Modellzuordnung als Datenquelle **ReportDataContract** dargestellt wird.

[![Konfigurieren einer Objektdatenquelle im EB-Modellzuordnungsdesigner.](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

Informationen zum Übergeben von Details des Ausführungskontexts vom Quellcode an die ausgeführte EB-Lösung finden Sie unter [Anwendungsartefakte entwickeln, um den entworfenen Bericht aufzurufen](er-quick-start1-new-solution.md#DevelopCustomCode).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
- [Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)
- [Unterstützte prmitive Datentypen](er-formula-supported-data-types-primitive.md)
