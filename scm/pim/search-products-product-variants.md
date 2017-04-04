---
title: Die Suche nach Produkten und Produktvarianten bei der Auftragserfassung
description: "Verwenden Sie das Feld <strong>Artikelnummer </strong>, um nach Produkten und Produktvarianten zu suchen, wenn Sie manuell eine Auftragsposition oder eine Bestellposition erstellen.  Dadurch können Sie schnell Produktvarianten suchen, wenn Ihnen nur die Konfigurationszeichenfolge oder eine der Produktdimensionen zur Verfügung steht."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, SalesTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 5b0f3c1a853f8f5e61dedaf588b6f9d2da3a53b5
ms.lasthandoff: 03/31/2017


---

# <a name="search-for-products-and-product-variants-during-order-entry"></a>Die Suche nach Produkten und Produktvarianten bei der Auftragserfassung

Verwenden Sie das Feld <strong>Artikelnummer </strong>, um nach Produkten und Produktvarianten zu suchen, wenn Sie manuell eine Auftragsposition oder eine Bestellposition erstellen.  Dadurch können Sie schnell Produktvarianten suchen, wenn Ihnen nur die Konfigurationszeichenfolge oder eine der Produktdimensionen zur Verfügung steht.

Manchmal zu viel von einigen ist zu haben nicht die beste Situation, um unter an, und dies ist besonders erfüllt, wenn einige Produkte verkaufen, die ähnlich sind, und Sie versuchen, die Produktsuchenamen Artikelnummern oder an zu erinnern, um das rechte Produkte, um einen Auftrag zu sperren. Sie können das ** Artikelnummer ** Feld in einer Auftragsposition oder einer Bestellposition als Suchfelds verwenden. Sie können einen beliebigen Teil eines Produktnamens, einer Zahl oder Dimension eingeben und eine Auswahlliste erhalten, bei der alle Artikel angezeigt werden, die mit dem Suchbegriff übereinstimmen.

## <a name="how-search-works"></a>Funktionsweise der Suche
Wenn Sie nach Produkten oder Produktvarianten suchen, ist es wichtig zu verstehen, wie mit der Suchfunktion die Produkte gefunden werden, die mit dem Text, den Sie eingeben, übereinstimmen. Dies sind die wichtigsten Suchregeln, um Suchergebnisse zu erhalten:

-   Die Suchergebnisse geben jeden beliebigen übereinstimmenden Datensatz zurück. Das Feld, in das der Suchtext eingegeben wird, bleibt dabei unberücksichtigt.
-   Der Suchtext muss im übereinstimmenden Datensatz in seiner vollen Länge vorhanden sein.
-   Eine Übereinstimmung tritt auch auf, wenn der Suchtext in der Mitte einer Textzeichenfolge im übereinstimmenden Datensatz gefunden wird. Er muss nicht am Anfang der Textzeichenfolge erscheinen.
-   Der Suchtext wird als einzelne Textzeichenfolge behandelt, selbst wenn er Leerzeichen enthält.

### <a name="examples"></a>Beispiele

In den folgenden Beispielen werden Produkte und Produktvarianten verwendet, um zu zeigen, wie die Suche in unterschiedlichen Szenarien gehandhabt wird. ** Voraussetzung: ** Darunter ** Vertriebs-und Marketing &gt; Einstellungs-Suchen-Suchenparameter &gt; ** ** &gt; Suchentyp **, wählen Sie die vollständige Übereinstimmung ** ** Option aus.

| Produkttyp     | Produktname    | Produktnummer anzeigen | Artikelnummer | Variante |
|------------------|-----------------|------------------------|-------------|---------------|
| Eindeutig identifizierbares Produkt | SpeakerMidRange | D0001                  | D0001       | N/Z            |
| Produktvariante  | Aktiver Lautsprecher  | D0010:::Schwarz:         | D0010       | 000005        |
| Produktvariante  | Aktiver Lautsprecher  | D0010:::Weiß:         | D0010       | Weiß         |

Wenn Sie im Feld **Artikelnummer** "sprech" eingeben, erhalten Sie alle oben genannten Produkte als Ergebnis in der Auswahlliste. Wenn Sie im Feld **Artikelnummer** "schwarz" eingeben, erhalten Sie das zweite Produkt als Ergebnis, da es den Text "schwarz" in der Anzeigeproduktnummer hat. Diese beiden Beispiele veranschaulichen, dass die Suche nicht nur am Anfang des Felds erfolgt. Eine Übereinstimmung tritt sogar auf, wenn der Suchtext in der Mitte einer Textzeichenfolge im übereinstimmenden Datensatz gefunden wird.  

Wenn Sie "05 "eingeben, erhalten Sie nur die zweite Produktvariante als Ergebnis, da sie "05" in der Konfiguration hat. Dies zeigt an, dass die Suche über alle aktivierten Felder auf der Seite **Suchkriterien** hinweg erfolgt.  

Wenn Sie "sprech 05" eingeben, erhalten Sie keine Ergebnisse. Das liegt daran, weil die Suche nach dem vollständigen Text sucht, der eingegeben wird. Die Suche versucht nicht, "sprech" zu finden und dann die Ergebnisse auf diejenigen einzuengen, die "05" enthalten.  

Sie können die Anzahl von Suchergebnissen begrenzen, indem Sie das ** Nummer Ergebnisse ** Feld auf der Vermarkten ** Vertrieb und von Einstellungs-Suchen-Suchenparametern &gt; ** Seite. Wenn Sie dieses Feld auf 0 festlegen, werden alle Suchergebnisse zurückgegeben. Wenn Sie es beispielsweise auf 10 festlegen, wird es maximal 10 Suchergebnisse zurückgeben.

## <a name="configure-the-product-search"></a>Die Produktsuche konfigurieren
Bevor Sie die Produkt- und Produktvarianten-Suchfunktion verwenden können, folgen Sie diesen Schritten, um die Produktsuche zu konfigurieren. [![3 vor, um die Produktsuche\_zu konfigurieren AXAppFall] ". /media/3-steps-to-configure-product-search_axappfall.png)]". /media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1-include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>Schritt 1: Schließen Sie alle relevanten Produkt- und Produktvariantenbezeichner und -dimensionen in die Suchkriterien ein

Beispiele für Produkt- und Produktvariantenbezeichner und -dimensionen, anhand derer Sie suchen können, sind **Produktname, Artikelnummer**, **Anzeigeproduktnummer, Konfiguration, Farbe, Größe, Stil, Suchbegriff usw.**  

Wechseln Vertriebs-und ** Marketing &gt; Einstellungs-Suchen-Suchkriterien &gt; ** Seite. Auf der Seite **Suchkriterien** können Sie Kriterien für Kunden, Interessenten und die Produktsuche definieren. Stellen Sie sicher, dass Sie die Seite mithilfe von Produktsuchkriterien filtern. Dies können Sie, indem Sie auf **Produkt** im Menü der Seite wechseln.  

Um der Anzeigenproduktnummer die Suchkriterien hinzufügen möchten, klicken Sie erneut ** ** im Menü der Seite. Hierdurch wird einem neuen Datensatzes im ** Suchkriterien ** Raster hinzu. Öffnen Sie die Spalten-Auswahlliste **Feldname** und wählen Sie **DisplayProductNumber** aus. Damit die Konfiguration des Fertigprodukts die Suchkriterien hinzufügen, erstellen eines neuen Datensatzes im ** Suchkriterien ** Raster und wählt ** configId ** ** ** Feldname in der Spalte aus. Auf die gleiche Weise erstellen Sie einen Datensatz mit **Feldname** **InventColorId** für die Farbdimension, **InventSizeId** für die Größendimension und **InventStyleId** für die Stildimension.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>Schritt 2: Füllen Sie die Datenbanktabelle auf, die für die Produktsuche verwendet wird

Auf der Seite **Suchkriterien** klicken Sie auf die Schaltfläche **Suchdaten aktualisieren**. Stellen Sie im Dialogfeld **Suchdaten aktualisieren** sicher, dass **Quelle** auf **Produkt** festgelegt ist, und klicken Sie dann auf **OK**. Das System zusammengefasst in einer Tabelle alle ausgewählten Suchkriterien, die in Schritt 1 angegeben werden. Wenn Sie viele Produkte und Produktvarianten verfügen, kann der Arbeitsgang langatmig ziemlich sein und Sie haben möglicherweise eine Warnung. Wir empfehlen, dass Sie die Suchtabellenauffüllung auf dem Stapelverarbeitungsserver für einen Zeitpunkt planen, an dem der Server nicht zu sehr beschäftigt ist.  

Bis die Tabelle aufgefüllt ist, stellt die Produktsuche keine korrekten Ergebnisse bereit. Wenn Sie keine Suchergebnisse erhalten, stellen Sie sicher, dass diese Tabelle aufgefüllt ist.  

Die Tabelle muss nur aufgefüllt werden, wenn die Suchkriterien geändert werden. Neu veröffentlichte Produkte und Varianten werden automatisch der Tabelle hinzugefügt. Gelöschte Produkte und Varianten werden automatisch von der Tabelle entfernt.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>Schritt 3: Aktivieren Sie die Auswahlliste für die Produktsuche bei Vertrieb und Bestellpositionen

Sie können diese Funktion aktivieren, indem Sie gelangen ** Vertrieb und Vermarkten &gt; von Einstellungs-Suchen-Suchenparametern &gt; ** ** und aktivieren Sie zum Suchen nach ** ** Ja ** auf die Registerkarte Allgemein ** ** festlegen.  

Bei einem Auftragspositionseintrag besteht das Standardverhalten darin, die Seite **Produktsuche** zu öffnen, wenn Sie damit beginnen, Eingaben in das Feld **Artikelnummer** vorzunehmen, und dann auf die **TABULATORTASTE** zu drücken. Die Seite **Produktsuche** ändert den Kontext während der Auftragspositionserstellung und wird möglicherweise als unnötig aufdringlich betrachtet. Wenn Sie es bevorzugen, die Suchergebnisse in einer Auswahlliste zu erhalten und nicht den Kontext während des Auftragspositionseintrags zu verlieren, können Sie stattdessen die Suchauswahlliste verwenden. Wenn Sie nach einem Produkt oder einer Produktvariante suchen, aber Sie nichts in der Auswahlliste auswählen und die Taste **Registerkarte** drücken, wird die Seite **Produktsuche** angezeigt.


