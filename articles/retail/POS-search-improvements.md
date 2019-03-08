---
title: Produktsuche und Debitorensuche in der Verkaufsstelle (POS)
description: Dieses Thema bietet einen Überblick über die Verbesserungen der Produkt- und Debitorensuchfunktion in Microsoft Dynamics 365 for Retail.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 1fa38002377fac24a5f3e25bd5924ecb23fec70a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "313588"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Produktsuche und Debitorensuche in der Verkaufsstelle (POS)

[!include [banner](includes/banner.md)]

Moderne Verkaufsstellen (MPOS) und Cloud-Verkaufsstellen (CPOS) bieten eine benutzerfreundliche Suchfunktion für Produkte und Debitoren. Da die Suchleiste immer oben in den MPOS- und CPOS-Fenstern angezeigt wird, können Mitarbeiter Produkte und Debitoren schnell finden.

Mitarbeiter können nach Produkten in den Sortimenten und Katalogen suchen, die der aktuellen Filiale zugeordnet sind. Sie können auch in den Sortimenten und Katalogen suchen, die irgendeiner anderen Filiale im Unternehmen zugeordnet sind. Daher können Kassierer Produkte außerhalb des Filialsortiments verkaufen und zurückgeben. Entsprechend können Mitarbeiter nach Debitoren suchen, die der aktuellen Filiale oder einer anderen Filiale im Unternehmen zugeordnet sind. Außerdem können Mitarbeiter nach Debitoren suchen, die einem anderen Unternehmen in der übergeordneten Organisation zugeordnet sind.

## <a name="product-search"></a>Produktsuche

Standardmäßig werden Produktsuchen im Filialsortiment ausgeführt. Diese Form der Suche wird als *lokale Produktsuche* bezeichnet. Allerdings können Mitarbeiter ganz einfach zu einem mit dem aktuellen Shop verknüpften Katalog wechseln oder in verschiedenen Shops suchen. Diese Form der Suche wird als *Remote-Produktsuche* bezeichnet. Um den Katalog zu ändern, wählen Sie auf der linke Seite die Schaltfläche **Kategorien** aus. Wählen Sie oben im angezeigten Bereich die Schaltfläche **Katalog ändern** und dann einen der verfügbaren Kataloge aus, um in diesem zu suchen. Das System durchsucht den ausgewählten Katalog nach Produkten.

Auf der Seite **Katalog ändern** können Mitarbeiter jeden beliebigen Shop auswählen oder Shop-übergreifend nach Produkten suchen.

![Ändern des Katalogs](./media/Changecatalog.png "Ändern des Katalogs")
 
Bei der lokalen Produktsuche wird in den folgenden Produkteigenschaften gesucht:

- Produktnummer
- Produktname
- Beschreibung
- Dimensionen
- Strichcode
- Suchbegriff

### <a name="enhancements-to-local-product-searches"></a>Erweiterungen von lokalen Produktsuchen

Die Benutzererfahrung bei der lokalen Produktsuche ist jetzt benutzerfreundlicher. Folgende Verbesserungen wurden vorgenommen:

- Produkt- und Debitorendropdownmenüs wurden zur Suchleiste hinzugefügt, sodass Mitarbeiter vor einer Suche entweder **Produkt** oder **Debitor** auswählen können. Standardmäßig ist **Produkt** ausgewählt, wie in der folgenden Abbildung gezeigt.
- Für Suchen mit mehreren Schlüsselwörtern (also Suchen mit Suchbegriffen) können Einzelhändler konfigurieren, ob die Suchergebnisse Ergebnisse enthalten, die mit *irgendeinem* Suchbegriff oder mit *allen* Suchbegriffen übereinstimmen. Diese Einstellung ist im POS-Funktionsprofil in einer neuen Gruppe namens **Produktsuche** verfügbar. Die Standardeinstellung ist **Alle beliebigen Suchbegriffe abgleichen**. Diese Einstellung ist auch die empfohlene Einstellung. Wenn die Einstellung **Jeden beliebigen Suchbegriff abgleichen** verwendet wird, werden alle Produkte, die vollständige oder teilweise mit einem oder mehreren Suchbegriffen übereinstimmen als Ergebnisse zurückgegeben. Diese Ergebnisse werden automatisch in aufsteigender Reihenfolge von Produkten sortiert, die die meisten Schlüsselwortübereinstimmungen haben (vollständig oder teilweise).

    Die Einstellung **Alle Suchbegriffe abgleichen** gibt nur die Produkte zurück, die mit allen Suchbegriffen (ganz oder teilweise) übereinstimmen. Diese Einstellung ist bei langen Produktnamen hilfreich und wenn Mitarbeiter nur begrenzte Produkte in den Sucherergebnissen haben möchten. Für diesen Suchtyp gelten jedoch zwei Einschränkungen:

    - Die Suche wird auf Basis einzelner Produkteigenschaften durchgeführt. Beispielsweise werden nur Produkte zurückgegeben, die alle Suchbegriffe in mindestens einer Produkteigenschaft haben.
    - Dimensionen werden nicht durchsucht.

- Einzelhändler können die Produktsuche nun so konfigurieren, dass Suchvorschläge angezeigt werden, wenn Produktnamen eingegeben werden. Eine neue Einstellung für diese Funktion ist im POS-Funktionsprofil in einer Gruppe namens **Produktsuche** verfügbar. Die Einstellung hat die Bezeichnung **Beim Eingeben Vorschläge anzeigen**. Diese Funktion ermöglicht Mitarbeitern, schnell das gesuchte Produkt zu finden, da sie nicht den ganzen Namen eingeben müssen.
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

### <a name="enhancements-to-local-customer-search"></a>Erweiterungen für lokale Debitorensuche

Suchen, die auf der Telefonnummer basieren, sind vereinfacht worden. Diese Suchen ignorieren nun Sonderzeichen, wie Leerzeichen, Bindestriche und Klammern, die möglicherweise hinzugefügt wurden, wenn der Debitor erstellt wurde. Daher müssen Kassierer sich keine Sorgen über das Telefonnummernformat machen, wenn sie suchen. Sie können auch nach Debitoren suchen, indem sie eine unvollständige Telefonnummer eingeben. Wenn eine Telefonnummer Sonderzeichen enthält, kann sie auch gefunden werden, indem nach den Zahlen gesucht wird, die nach den Sonderzeichen angezeigt werden. Wurde beispielsweise die Telefonnummer eines Debitors in der Form **123-456-7890** eingegeben, kann ein Kassierer nach dem Debitor suchen, indem er **123**, **456**, **7890** oder **1234567890** eingibt oder indem er nur die ersten Zahlen einer Telefonnummer eingibt.

Die herkömmliche Debitorensuche kann zeitaufwendig sein, da sie über mehrere Felder hinweg sucht. Stattdessen können Kassierer jetzt in einer einzigen benutzerdefinierten Eigenschaft, wie Name, E-Mail-Adresse oder Telefonnummer suchen. Die Eigenschaften, die der Debitorensuchalgorithmus verwendet, werden zusammen als *Debitorensuchkriterien* bezeichnet. Der Systemadministrator kann einfach ein oder mehrere Kriterien als Verknüpfungen konfigurieren, die in der POS angezeigt werden. Da die Suche auf ein einziges Kriterium eingeschränkt ist, werden nur die relevanten Suchergebnisse angezeigt, und die Leistung ist viel besser, als die Leistung bei einer standardmäßigen Debitorensuche. Die folgende Abbildung zeigt die Debitorensuchverknüpfungen in POS an.

![Debitorensuchverknüpfungen](./media/SearchShortcutsPOS.png "Debitorensuchverknüpfungen")

Um Suchkriterien als Verknüpfungen festzulegen, muss der Administrator die Seite **Einzelhandelsparameter** in Microsoft Dynamics 365 for Finance and Operations öffnen und dann auf der Registerkarte **POS-Suchkriterien** alle Kriterien auswählen, die als Verknüpfungen angezeigt werden sollen.

![Suchverknüpfungen konfigurieren](./media/ConfigureShortcutsAX.png "Suchverknüpfungen konfigurieren")

> [!NOTE]
> Wenn Sie zu viele Verknüpfungen hinzufügen, wird das Dropdownmenü in der Suchleiste in POS überladen, und die Sucherfahrung des Mitarbeiters kann beeinträchtigt werden. Es wird empfohlen, dass Sie nur so viele Verknüpfungen hinzufügen, wie Sie benötigen.

Das Feld **Reihenfolge anzeigen** bestimmt die Reihenfolge, in der Verknüpfungen in POS angezeigt werden. Die angezeigten Kriterien sind die vorkonfigurierten Eigenschaften, die der Debitorensuchalgorithmus verwendet, um nach Debitoren zu suchen. Allerdings können Partner benutzerdefinierte Eigenschaften als Suchenverknüpfungen hinzufügen. Um benutzerdefinierte Eigenschaften als Suchverknüpfungen hinzuzufügen, muss der Systemadministrator die erweiterbare Enumeration (Enum), die für die Debitorensuchkriterien verwendet wird, erweitern und dann die benutzerdefinierten Eigenschaften des Partners als Verknüpfungen markieren. Partner sind dafür zuständig, den Code zu schreiben, um die Ergebnisse zu finden, wenn ihre benutzerdefinierten Verknüpfungen für Suchen verwendet werden.

> [!NOTE]
> Eine benutzerdefinierte Eigenschaft, die der Enumeration hinzugefügt wird, wirkt sich nicht den standardmäßigen Debitorensuchenalgorithmus aus. Das bedeutet, dass der Debitorensuchalgorithmus nicht in der Debitoreneigenschaft suchen wird. Benutzer können nur eine benutzerdefinierte Eigenschaft für Suchvorgänge verwenden, wenn diese benutzerdefinierte Eigenschaft als Verknüpfung hinzugefügt ist oder wenn der Standardsuchenalgorithmus überschrieben wird.
