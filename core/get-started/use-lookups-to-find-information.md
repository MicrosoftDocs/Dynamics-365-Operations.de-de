---
title: Verwendungssuchen, um Informationen zu suchen
description: "In Microsoft Dynamics 365 für Arbeitsgänge, haben zahlreiche Felder Suchen, die einfach können Ihnen dabei helfen, das richtige oder den gewünschten Wert zu suchen. Einige Erweiterungen sind zu Suchvorgängen hinzugefügt, die verwendbarer diese Elemente erstellen und Benutzer produktiver vornehmen. In diesem Thema erhalten Sie über diese neuen und die Suchfunktion erhalten mehrere Tipps hilfreich, die optimale Nutzung aus Suchen im System aus abgerufen."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 6a25593632575dcd71fa4a3c9cf5b83c9f8ecd39
ms.lasthandoff: 03/31/2017


---

# <a name="use-lookups-to-find-information"></a>Verwendungssuchen, um Informationen zu suchen

In Microsoft Dynamics 365 für Arbeitsgänge, haben zahlreiche Felder Suchen, die einfach können Ihnen dabei helfen, das richtige oder den gewünschten Wert zu suchen. Einige Erweiterungen sind zu Suchvorgängen hinzugefügt, die verwendbarer diese Elemente erstellen und Benutzer produktiver vornehmen. In diesem Thema erhalten Sie über diese neuen und die Suchfunktion erhalten mehrere Tipps hilfreich, die optimale Nutzung aus Suchen im System aus abgerufen.  

<a name="responsive-lookups"></a>Suchen Reagierende
------------------

In älteren Versionen von Microsoft Dynamics 365 für Arbeitsgänge als, interagierend mit einem Suchensteuerelement, ein Benutzer expliziten Maßnahmen ergreifen steht, müssen das Dropdownmenü zu öffnen. Dies war z, indem einem Sternchen (\*) im Steuerelement hatte, um die Auswahlliste auf dem aktuellen Wert des Steuerelements zu filtern und auf die Dropdownschaltfläche klicken oder indem ** ALT **+** unten Pfeil ** Tastenkombination verwendet wird. Suchenkontrollen sind folgendermaßen geändert wurden, um mit aktuellen Internet-Methoden besser einzuhalten:

-   Suchendropdownmenüs öffnen nun sich automatisch nach einer Pause geringfügige beim Eingeben, wenn die Dropdownmenüinhalte auf Basis des Suchen steuer gefiltert sind.
    -   Beachten Sie, dass die alte Verhalten der automatischen Eröffnung des Dropdowns, nachdem sie einem Sternchen (\*) handelt es überflüssig wurde eingegeben worden wäre.
-   Nachdem das Suchendropdownmenü sich geöffnet hat, tritt folgende Schritte aus:
    -   Der Cursor muss im Suchensteuerelement (anstelle des Ziels, das in das Dropdownmenü bewegt), sodass Sie fortfahren, um Änderungen am Wert des Steuer vorzunehmen. Allerdings kann der Benutzer noch verwenden ** so Pfeil ** und ** unten Pfeil ** Zeilen im Dropdownmenü ändern und gibt an, in der die aktuelle Zeile im Dropdownmenü auswählen.
    -   Der Inhalt des Dropdownmenüs anpassen, nachdem Änderungen am Wert des Suchen steuer vorgenommen werden.

Hierzu werden ein Nachschlagefeld als bezeichnet ** ** Ort. 

Wenn auf dem Ziel ** Ort ** Feld ist, kann das Suchen des Orts, indem Sie den gewünschten, mehreren Buchstaben eingeben, wie "Col" beginnen.  Nachdem nach dem Anhalten eingeben, wird die Suche, automatisch gefiltert nach die Orte, die mit "Col." beginnen. 

![typeaheadLookupExample ([]. /media/typeaheadlookupexample.png)]". /media/typeaheadlookupexample.png) 

Zu diesem Zeitpunkt wird der Cursor noch im Suchfeld. Wenn Sie die Eingabe fortgesetzt werden, damit der Wert "Spalte ist, die anpassen" Sucheninhalte automatisch, um den letzten Wert Steuerelement im widerzuspiegeln. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

Obwohl Ziel noch im Suchensteuerelement ist, können Sie so ** Pfeil ** ** oder unten Pfeil ** die Schlüssel auch verwenden, um die Zeile hervorzuheben, die Sie auswählen möchten. Wenn Sie drücken ** Eingeben ** die hervorgehobene Zeile wird von der Suche ausgewählt und der Steuer wird aktualisiert. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Eingabe in mehrere IDs
Wenn von Daten eingibt, ist es für Benutzer natürliche zu versuchen, eine Entität, wie Debitor oder Kreditor, in Bezug auf den Namen anstatt eine Kennung zu ermitteln, welche die Entität darstellt. In der aktuellen Version von Microsoft Dynamics 365 für Arbeitsgänge, können viele (jedoch nicht alle) Suchen nun kontextabhängige Dateneingabe. Diese leistungsstarke Funktion ermöglicht dem Benutzer, dass der Kennung oder des entsprechenden Namen in das Suchensteuerelement einzugeben. 

Hierzu werden das Debitorenkonto ** ** Feld, wenn Sie einen Auftrag erstellen. Dieses Feld enthält ** Konto-ID ** für den Debitor angezeigt, aber ein Benutzer ist normalerweise lieber, ** Kontenbezeichnung ** anstelle ** Konto-ID ** für dieses Feld eingeben, wenn, einen Auftrag, z Gesamtstruktur dienen, "Großhandel verkauft" anstelle von "US-003."

Wenn der Benutzer, der Start ist, erzielt ** Konto-ID ** in das Suchensteuerelement eingeben, das Dropdownmenü wird automatisch geöffnet werden sollen, wie im vorherigen Abschnitt und Benutzer in beschrieben die Suche wie weiter unten finden wird.

[kontextabhängige Suche ![wenn eine eingegeben wird Debitorenkontokennung] ". /media/howtocontextuallookups-1.png)]". /media/howtocontextuallookups-1.png)

Allerdings kann der Benutzer auch den Anfang von nun auch eingeben ** Kontenbezeichnung **. Wenn dieses realisiert wird, dann wird für den Benutzer die nächste Suche. Beachten Sie, wie die Spalte Name ** ** bewegt wird, um die erste Spalte in die Suche werden sollen und wie die zum Suchen in der Spalte Name ** ** sortiert und gefiltert wird.

[kontextabhängige Suche ![wenn ein Debitorenname] "eingegeben wird. /media/howtocontextuallookups-2.png)]". /media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Verwenden der spaltenüberschriften Raster für erweiterte Filter- und Sortieren
Die Suchenerweiterungen, die in früheren beiden Abschnitten verbessern erörterten erheblichen, die Möglichkeit eines Benutzers, Zeilen in einer Auswahlliste auf Basis zu navigieren "beginnt mit" Suche bei ** Kennung ** oder ** Name ** Feld Suche. Allerdings besteht Situationen, in denen (erweiterte Filter- oder Sortieren" erforderlich ist, um die korrekte Zeile zu suchen. In solchen Fällen besteht die Nutzerbedarfe und Sortierfunktionen gewünschten, die in den Rasterspaltenüberschriften innerhalb der Suche verwendet werden soll. Hierzu werden einen Mitarbeiter, welche eine Auftragsposition eingibt, die das rechte "Kabel" als das Produkt suchen muss. "Kabel" in das ** Artikelnummer ** Steuerelement einzugeben ist nicht hilfreich, da keine Produktnamen gibt, die mit "beginnen Kabel." 

![emptyitemlookup](./media/emptyitemlookup.png) 

Stattdessen öffnen, die Nutzerbedarfe den Wert aus dem Suchensteuerelement zu löschen, das Suchendropdownmenü und filtern Über das Dropdownmenü können mithilfe der Rasterspaltenüberschrift, wie weiter unten). Ein Benutzer der Maus "Schritt" kann oder (oder Note) in jeder Spaltenüberschrift einfach klicken, um die gewünschten für diese Berichtsspalte und Sortierfunktionen zuzugreifen. Für einen Tastaturbenutzer muss der Benutzer einfach ** ALT **+** unten ** ** Pfeil ** ein zweites Mal, Ziel in das Dropdownmenü zu verschieben, nachdem er Registerkarte können zur richtigen Spalte, und ** STRG **+G dann an die Rasterspaltenüberschriftdropdownmenü ** um das zu öffnen. 

![gridfilteritemlookup ([]. /media/gridfilteritemlookup.png)]". /media/gridfilteritemlookup.png) 

Nachdem der Filter (siehe Bild unten), Übernommenes wurde, kann der Benutzer die Zeile wie gewohnt suchen und auswählen. 

![filtereditemlookup](./media/filtereditemlookup.png)


