---
title: Produktsuche und Debitorensuche in POS
description: "Dieses Thema bietet einen Überblick über die Verbesserungen der Produkt- und Debitorensuchfunktion in Dynamics 365 for Retail."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 08/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: bd563610616fa72a610e0b134371765cc1edacc6
ms.contentlocale: de-de
ms.lasthandoff: 03/07/2018

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a>Überblick über Produkt- und Debitorensuche in der Verkaufsstelle

[!include[banner](includes/banner.md)]

Moderne Verkaufsstellen (MPOS) und Cloud-Verkaufsstellen (CPOS) bieten eine benutzerfreundliche Suchfunktion, mit der Shopmitarbeitern Produkte und Debitoren schnell finden können. Die Suchleiste wird immer oben auf den MPOS und CPOS angezeigt, sodass Mitarbeiter Produkte und Debitoren schnell finden können.

Mitarbeiter können nach Produkten in Sortimenten und Katalogen suchen, die mit dem aktuellen Shop verknüpft sind und in den Sortimenten und Katalogen, die mit anderen Shops im Unternehmen verknüpft sind. Daher können Kassierer Produkte außerhalb des Filialsortiments verkaufen und zurückgeben. Entsprechend können Mitarbeiter nach Debitoren suchen, die mit dem aktuellen Shop oder einem anderen Shop im Unternehmen verknüpft sind. Außerdem können Mitarbeiter nach Debitoren suchen, die mit einem anderen Unternehmen in der übergeordneten Organisation verknüpft sind.

## <a name="product-search"></a>Produktsuche 

Standardmäßig wird eine Produktsuche im Shopsortiment ausgeführt. Diese Form der Suche wird als *lokale Produktsuche* bezeichnet. Allerdings können Mitarbeiter ganz einfach zu einem mit dem aktuellen Shop verknüpften Katalog wechseln oder in verschiedenen Shops suchen. Diese Form der Suche wird als *Remote-Produktsuche* bezeichnet. Um den Katalog zu ändern, wählen Sie auf der linke Seite die Schaltfläche **Kategorien** aus. Wählen Sie oben im angezeigten Bereich die Schaltfläche **Katalog ändern** und dann einen der verfügbaren Kataloge aus, um in diesem zu suchen. Das System durchsucht den ausgewählten Katalog nach Produkten.

Auf der Seite **Katalog ändern** können Mitarbeiter jeden beliebigen Shop auswählen oder Shop-übergreifend nach Produkten suchen.

![Ändern des Katalogs](./media/Changecatalog.png "Ändern des Katalogs")
 
Bei der lokalen Produktsuche wird innerhalb folgender Produktattribute gesucht:

- Produktnummer
- Produktname
- Beschreibung
- Dimensionen
- Strichcode
- Suchbegriff

### <a name="enhancements-to-local-product-searches"></a>Erweiterungen von lokalen Produktsuchen

Die Benutzererfahrung bei der lokalen Produktsuche ist optimiert worden. Folgende Verbesserungen wurden vorgenommen:

- Produkt- und Debitorendropdownmenüs wurden zur Suchleiste hinzugefügt, sodass Mitarbeiter vor einer Suche entweder **Produkt** oder **Debitor** auswählen können. Standardmäßig ist **Produkt** ausgewählt, wie in der folgenden Abbildung gezeigt.
- Für Suchen mit mehreren Keywords (also Suchen mit Suchbegriffen) können Einzelhändler konfigurieren, ob die Suchergebnisse Ergebnisse enthalten, die mit einem Suchbegriff oder mit allen Suchbegriffen übereinstimmen. Diese Einstellung ist im POS-Funktionsprofil unter einer neuen Gruppe namens **Produktsuche** verfügbar. Die Standardeinstellung ist **Alle beliebigen Suchbegriffe abgleichen**. Diese Einstellung ist auch die empfohlene Einstellung. Wenn die Einstellung **Alle beliebigen Suchbegriffe abgleichen** verwendet wird, werden alle Produkte die ganz oder teilweise mit einem oder mehreren Suchbegriffen übereinstimmen, als Ergebnis zurückgegeben. Die Ergebnisse werden automatisch in aufsteigender Reihenfolge sortiert. Produkte mit den meisten Suchbegriffübereinstimmungen (ganz oder teilweise) stehen ganz oben.

    Die Einstellung **Alle Suchbegriffe abgleichen** gibt nur die Produkte zurück, die mit allen Suchbegriffen (ganz oder teilweise) übereinstimmen. Diese Einstellung ist bei langen Produktnamen hilfreich und wenn Mitarbeiter nur begrenzte Produkte in den Sucherergebnissen haben möchten. Für diesen Suchtyp gelten jedoch zwei Einschränkungen:

    - Die Suche wird auf Basis einzelner Produkteigenschaften durchgeführt. Beispielsweise werden nur Produkte zurückgegeben, die alle Suchbegriffe in mindestens einer Produkteigenschaft haben.
    - Dimensionen werden nicht durchsucht.

- Einzelhändler können die Produktsuche nun so konfigurieren, dass Suchvorschläge angezeigt werden, wenn Produktnamen eingegeben werden. Eine neue Einstellung für diese Funktion ist im POS-Funktionsprofil unter einer Gruppe namens **Produktsuche** verfügbar. Die Einstellung hat die Bezeichnung **Beim Eingeben Vorschläge anzeigen**. Diese Funktion ermöglicht Mitarbeitern, schnell das gesuchte Produkt zu finden, da sie nicht den ganzen Namen eingeben müssen.
- Der Produktsuchalgorithmus sucht nun auch in der **Suchbegriff**-Eigenschaft des Produkts nach den Suchbegriffen.

![Produktvorschläge](./media/Productsuggestions.png "Produktvorschläge")

## <a name="customer-search"></a>Debitorensuche

Die Debitorensuche wird verwendet, um Debitoren für verschiedene Zwecke zu suchen. So möchten Kassierer möglicherweise den Wunschzettel oder die Kaufhistorie eines Debitors anzeigen oder den Debitor zu einer Transaktion hinzufügen. Bei Suchen mit mehreren Suchbegriffen gibt der Debitorensuchalgorithmus alle Debitoren zurück, die mit einem der Suchbegriffe übereinstimmen. Allerdings werden die Debitoren, die den meisten Suchbegriffen entsprechen, oben in den Ergebnissen angezeigt. Dieses Verfahren ist identisch mit dem anderer Suchmaschinen. Sie zeigen als erstes die Ergebnisse, die den am meisten gesuchten Begriffen entsprechen, und anschließend die Ergebnisse, die teilweise mit dem Suchbegriffen übereinstimmen. Dies hilft Kassierern in Situationen, in denen Sie mehrere Suchbegriffe in Ihre Suche einschließen, aber ein Suchbegriff einen Rechtschreibfehler aufweist.

Standardmäßig wird eine Debitorensuche in den Debitorenadressbüchern durchgeführt, die mit dem Shop verknüpft sind. Diese Form der Suche wird als *lokale Debitorensuche* bezeichnet. Allerdings können Mitarbeiter auch global nach Debitoren suchen. Sie können also auch in den Shops des Unternehmens und in allen anderen juristischen Personen eine Suche durchführen. Diese Form der Suche wird als *Remote-Debitorensuche* bezeichnet.

Für eine globale Suche können Mitarbeiter die Schaltfläche **Filterergebnisse** am unteren Seitenrand auswählen und dann die Option **Alle Shops durchsuchen**, wie in der folgenden Abbildung gezeigt. In diesem Fall werden nicht nur Debitoren zurückgegeben. Alle Arten von Parteien, die Teil eines Adressbuchs in den Zentralverwaltungen sind, werden ebenfalls zurückgegeben. Zu diesen Parteien zählen Arbeitskräfte, Kreditoren, Mitbewerber und Kontakte.

> [!NOTE]
> Für eine Remote-Debitorensuche müssen mindestens vier Zeichen eingegeben werden.

Bei einer Remote-Debitorensuche wird die Debitorenkennung nicht für Debitoren anderer juristischer Personen angezeigt, da für diese Parteien im aktuellen Unternehmen keine Debitorenkennung angelegt wurde. Wenn ein Mitarbeiter jedoch die Debitorendetailseite öffnet, generiert das System automatisch eine Debitorenkennung für die Partei und verknüpft das Debitorenadressbuch des Shops mit dem Debitor. Daher wird der Debitor bei späteren lokalen Shopsuchen angezeigt.

![Globale Debitorensuche](./media/Globalcustomersearch.png "Globale Debitorensuche")

### <a name="enhancements-to-local-customer-searches"></a>Erweiterungen für lokale Debitorensuchen

Lokale Debitorensuchen helfen Mitarbeitern, schnell Debitoren anhand deren Telefonnummer zu finden. Mitarbeiter müssen keine Sonderzeichen eingeben, die der Telefonnummer eines Debitors hinzugefügt wurden, beispielsweise Leerzeichen, Klammern oder Bindestriche. Obwohl Kassierer Telefonnummern in beliebigem Format speichern können (sie können beispielsweise Klammern, Bindestriche, Symbole usw. einschließen), können Sie nach Debitoren suchen, indem Sie einfach einen Teil einer Telefonnummer eingeben. Wenn ein Kassierer Sonderzeichen eingeschlossen hat, als die Telefonnummer eingegeben wurde, können andere Kassierer den Debitor finden, indem Sie die Zahlen nach den Sonderzeichen eingeben. Wurde beispielsweise die Telefonnummer eines Debitors in der Form **123-456-7890** eingegeben, kann ein Kassierer nach dem Debitor suchen, indem er **123**, **456**, **7890** oder **1234567890** eingibt oder indem er nur die ersten Nummern einer Telefonnummer eingibt.

