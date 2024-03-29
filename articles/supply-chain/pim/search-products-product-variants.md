---
title: Die Suche nach Produkten und Produktvarianten bei der Auftragserfassung
description: Verwenden Sie das Feld **Artikelnummer**, um nach Produkten und Produktvarianten zu suchen, wenn Sie manuell eine Auftragsposition oder eine Bestellposition erstellen. Dadurch können Sie schnell Produktvarianten suchen, wenn Ihnen nur die Konfigurationszeichenfolge oder eine der Produktdimensionen zur Verfügung steht.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, PurchTablePart, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9fea7f82ac7723d4cb83c5c8224251fd6c43a315
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565694"
---
# <a name="search-for-products-and-product-variants-during-order-entry"></a>Die Suche nach Produkten und Produktvarianten bei der Auftragserfassung

[!include [banner](../includes/banner.md)]

Verwenden Sie das Feld **Artikelnummer**, um nach Produkten und Produktvarianten zu suchen, wenn Sie manuell eine Auftragsposition oder eine Bestellposition erstellen.  Dadurch können Sie schnell Produktvarianten suchen, wenn Ihnen nur die Konfigurationszeichenfolge oder eine der Produktdimensionen zur Verfügung steht.

Manchmal ist die Lage nicht optimal, wenn zu viel von einer Sache vorhanden ist. Das gilt insbesondere, wenn Sie eine Anzahl ähnlicher Produkte verkaufen und versuchen, sich die Artikelnummern oder Produktsuchbegriffe zu merken, um das richtige Produkt zu finden, das einem Auftrag hinzugefügt werden soll. Sie können das Feld **Artikelnummer** in einer Auftragsposition oder einer Bestellposition als Suchfeld verwenden. Sie können einen beliebigen Teil eines Produktnamens, einer Zahl oder Dimension eingeben und eine Auswahlliste erhalten, bei der alle Artikel angezeigt werden, die mit dem Suchbegriff übereinstimmen.

## <a name="how-search-works"></a>Funktionsweise der Suche
Bei der Suche nach Produkten oder Produktvarianten sollte man verstehen, wie mit der Suchfunktion die Produkte gefunden werden, die mit dem Text, den Sie eingeben, übereinstimmen. Dies sind die wichtigsten Suchregeln, um Suchergebnisse zu erhalten:

-   Die Suchergebnisse geben jeden beliebigen übereinstimmenden Datensatz zurück. Das Feld, in das der Suchtext eingegeben wird, bleibt dabei unberücksichtigt.
-   Der Suchtext muss im übereinstimmenden Datensatz in seiner vollen Länge vorhanden sein.
-   Eine Übereinstimmung tritt auch auf, wenn der Suchtext in der Mitte einer Textzeichenfolge im übereinstimmenden Datensatz gefunden wird. Er muss nicht am Anfang der Textzeichenfolge erscheinen.
-   Der Suchtext wird als einzelne Textzeichenfolge behandelt, selbst wenn er Leerzeichen enthält.

### <a name="examples"></a>Beispiele

In den folgenden Beispielen werden Produkte und Produktvarianten verwendet, um zu zeigen, wie die Suche in unterschiedlichen Szenarien gehandhabt wird. **Voraussetzung**: Wählen Sie unter **Vertrieb und Marketing &gt; Setup &gt; Suche &gt; Suchparameter &gt; Suchtyp** die Option **Vollständige Übereinstimmung** aus.

| Produkttyp     | Produktname    | Produktnummer anzeigen | Artikelnummer | Variante |
|------------------|-----------------|------------------------|-------------|---------------|
| Eindeutig identifizierbares Produkt | SpeakerMidRange | D0001                  | D0001       | N/Z            |
| Produktvariante  | Aktiver Lautsprecher  | D0010:::Schwarz:         | D0010       | 000005        |
| Produktvariante  | Aktiver Lautsprecher  | D0010:::Weiß:         | D0010       | Weiß         |

Wenn Sie im Feld **Artikelnummer** „sprech“ eingeben, erhalten Sie alle oben genannten Produkte als Ergebnis in der Auswahlliste. Wenn Sie im Feld **Artikelnummer** "schwarz" eingeben, erhalten Sie das zweite Produkt als Ergebnis, da es den Text "schwarz" in der Anzeigeproduktnummer hat. Diese beiden Beispiele veranschaulichen, dass die Suche nicht nur am Anfang des Felds erfolgt. Eine Übereinstimmung tritt sogar dann auf, wenn der Suchtext in der Mitte einer Textzeichenfolge im übereinstimmenden Datensatz gefunden wird.  

Wenn Sie "05 "eingeben, erhalten Sie nur die zweite Produktvariante als Ergebnis, da sie "05" in der Konfiguration hat. Dies zeigt an, dass die Suche über alle aktivierten Felder auf der Seite **Suchkriterien** hinweg erfolgt.  

Wenn Sie "sprech 05" eingeben, erhalten Sie keine Ergebnisse. Das liegt daran, dass nach dem vollständigen Text gesucht wird, den Sie eingeben. Die Suche versucht nicht, "sprech" zu finden und dann die Ergebnisse auf diejenigen einzuengen, die "05" enthalten.  

Sie können die Anzahl der Suchergebnisse eingrenzen, indem Sie das Feld **Anzahl von Ergebnissen** auf der Seite **Vertrieb und Marketing &gt; Setup &gt; Suche &gt; Suchparamter** verwenden. Wenn Sie dieses Feld auf 0 festlegen, werden alle Suchergebnisse zurückgegeben. Wenn Sie es beispielsweise auf 10 festlegen, wird es maximal 10 Suchergebnisse zurückgeben.

## <a name="configure-the-product-search"></a>Konfigurieren der Produktsuche
Bevor Sie die Suchfunktion für Produkte und Produktvarianten verwenden können, befolgen Sie diese Schritte, um die Produktsuche zu konfigurieren. [![3 Schritte, um die Produktsuche\_AXAppFall zu konfigurieren.](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1-include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>Schritt 1: Schließen Sie alle relevanten Bezeichner und Dimensionen für Produkte und Produktvarianten in die Suchkriterien ein.

Beispiele für Bezeichner und Dimensionen für Produkte und Produktvarianten, anhand derer Sie suchen können, sind **Produktname, Artikelnummer**, **Anzeigeproduktnummer, Konfiguration, Farbe, Größe, Stil, Suchbegriff usw.**  

Wechseln Sie zur Seite **Vertrieb und Marketing &gt; Setup &gt; Suche &gt; Suchkriterien**. Auf der Seite **Suchkriterien** können Sie Kriterien für Kunden, Interessenten und die Produktsuche definieren. Stellen Sie sicher, dass Sie die Seite mithilfe von Produktsuchkriterien filtern. Wechseln Sie hierfür im Menü der Seite auf **Produkt**.  

Um der Anzeigenproduktnummer die Suchkriterien hinzufügen möchten, klicken Sie **Neu** im Menü der Seite. Hierdurch wird einem neuen Datensatzes im **Suchkriterien** Raster hinzu. Öffnen Sie die Spalten-Auswahlliste **Feldname** und wählen Sie **DisplayProductNumber** aus. Um die Konfiguration des Produkts den Suchkriterien hinzuzufügen, erstellen Sie einen neuen Datensatz im Raster **Suchkriterien** und wählen Sie **configId** in der Spalte **Feldname** aus. Auf die gleiche Weise erstellen Sie einen Datensatz mit **Feldname** **InventColorId** für die Farbdimension, **InventSizeId** für die Größendimension und **InventStyleId** für die Stildimension.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>Schritt 2: Füllen Sie die Datenbanktabelle auf, die für die Produktsuche verwendet wird

Auf der Seite **Suchkriterien** klicken Sie auf die Schaltfläche **Suchdaten aktualisieren**. Stellen Sie im Dialogfeld **Suchdaten aktualisieren** sicher, dass **Quelle** auf **Produkt** festgelegt ist, und klicken Sie dann auf **OK**. Das System zusammengefasst in einer Tabelle alle ausgewählten Suchkriterien, die in Schritt 1 angegeben werden. Bei einer großen Anzahl von Produkten und Produktvarianten kann dieser Vorgang recht langwierig sein und es wird eventuell eine Warnung angezeigt. Wir empfehlen, dass Sie die Suchtabellenauffüllung auf dem Stapelverarbeitungsserver für einen Zeitpunkt planen, an dem der Server nicht zu sehr beschäftigt ist.  

Bis die Tabelle aufgefüllt ist, stellt die Produktsuche keine korrekten Ergebnisse bereit. Wenn Sie keine Suchergebnisse erhalten, stellen Sie sicher, dass diese Tabelle aufgefüllt ist.  

Die Tabelle muss nur aufgefüllt werden, wenn die Suchkriterien geändert werden. Neu veröffentlichte Produkte und Varianten werden automatisch der Tabelle hinzugefügt. Gelöschte Produkte und Varianten werden automatisch von der Tabelle entfernt.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>Schritt 3: Aktivieren Sie die Auswahlliste für die Produktsuche bei Vertrieb und Bestellpositionen

Sie können diese Funktion aktivieren, indem Sie zu **Vertrieb und Marketing &gt; Setup &gt; Suche &gt; Suchparameter** wechseln und die Option **Auswahlliste für Suche aktivieren** auf **Ja** in der Registerkarte **Allgemein** festlegen.  

Bei einem Auftragspositionseintrag wird standardmäßig die Seite **Produktsuche** geöffnet, wenn Sie mit einer Eingabe in das Feld **Artikelnummer** beginnen und dann die **Tabulatortaste** drücken. Die Seite **Produktsuche** ändert den Kontext während der Auftragspositionserstellung und wird möglicherweise als unnötig aufdringlich betrachtet. Wenn Sie es bevorzugen, die Suchergebnisse in einer Auswahlliste zu erhalten und nicht den Kontext während des Auftragspositionseintrags zu verlieren, können Sie stattdessen die Suchauswahlliste verwenden. Wenn Sie nach einem Produkt oder einer Produktvariante suchen, in der Auswahlliste jedoch keine Auswahl vornehmen und dann die **Tabulatortaste** drücken, wird die Seite **Produktsuche** angezeigt.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]