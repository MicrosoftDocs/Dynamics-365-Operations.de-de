---
title: Produktsuche und Debitorensuche in der Verkaufsstelle (POS)
description: Dieses Thema bietet einen Überblick über die Verbesserungen der Produkt- und Debitorensuchfunktion in Dynamics 365 Commerce.
author: ShalabhjainMSFT
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: d562f97ecc3c442be4231470167a0aae86f84fe5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345159"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Produktsuche und Debitorensuche in der Verkaufsstelle (POS)

[!include [banner](includes/banner.md)]

Moderne Verkaufsstellen (MPOS) und Cloud-Verkaufsstellen (CPOS) bieten eine benutzerfreundliche Suchfunktion für Produkte und Debitoren. Da die Suchleiste immer oben in den MPOS- und CPOS-Fenstern angezeigt wird, können Mitarbeiter Produkte und Debitoren schnell finden.

Mitarbeiter können nach Produkten in den Sortimenten und Katalogen suchen, die der aktuellen Filiale zugeordnet sind. Sie können auch in den Sortimenten und Katalogen suchen, die irgendeiner anderen Filiale im Unternehmen zugeordnet sind. Daher können Kassierer Produkte außerhalb des Filialsortiments verkaufen und zurückgeben. Entsprechend können Mitarbeiter nach Debitoren suchen, die der aktuellen Filiale oder einer anderen Filiale im Unternehmen zugeordnet sind. Außerdem können Mitarbeiter nach Debitoren suchen, die einem anderen Unternehmen in der übergeordneten Organisation zugeordnet sind.

## <a name="product-search"></a>Produktsuche

Standardmäßig werden Produktsuchen im Filialsortiment ausgeführt. Diese Form der Suche wird als *lokale Produktsuche* bezeichnet. Allerdings können Mitarbeiter ganz einfach zu einem mit dem aktuellen Shop verknüpften Katalog wechseln oder in verschiedenen Shops suchen. Diese Form der Suche wird als *Remote-Produktsuche* bezeichnet. Um den Katalog zu ändern, wählen Sie auf der linke Seite die Schaltfläche **Kategorien** aus. Wählen Sie oben im angezeigten Bereich die Schaltfläche **Katalog ändern** und dann einen der verfügbaren Kataloge aus, um in diesem zu suchen. Das System durchsucht den ausgewählten Katalog nach Produkten.

Auf der Seite **Katalog ändern** können Mitarbeiter jeden beliebigen Shop auswählen oder Shop-übergreifend nach Produkten suchen.

![Den Katalog ändern.](./media/Changecatalog.png "Den Katalog ändern")

Bei der lokalen Produktsuche wird in den folgenden Produkteigenschaften gesucht:

- Produktnummer
- Produktname
- Beschreibung
- Dimensionen
- Strichcode
- Suchbegriff

### <a name="additional-local-product-search-capabilities"></a>Zusätzliche Funktionen für die lokale Produktsuche

- Für Suchen mit mehreren Schlüsselwörtern (also Suchen mit Suchbegriffen) können Einzelhändler konfigurieren, ob die Suchergebnisse Ergebnisse enthalten, die mit *irgendeinem* Suchbegriff oder mit *allen* Suchbegriffen übereinstimmen. Die Einstellung für diese Funktion ist im POS-Funktionsprofil in einer neuen Gruppe namens **Produktsuche** verfügbar. Die Standardeinstellung ist **Alle beliebigen Suchbegriffe abgleichen**. Diese Einstellung ist auch die empfohlene Einstellung. Wenn die Einstellung **Jeden beliebigen Suchbegriff abgleichen** verwendet wird, werden alle Produkte, die vollständige oder teilweise mit einem oder mehreren Suchbegriffen übereinstimmen als Ergebnisse zurückgegeben. Diese Ergebnisse werden automatisch in aufsteigender Reihenfolge von Produkten sortiert, die die meisten Schlüsselwortübereinstimmungen haben (vollständig oder teilweise).

    Die Einstellung **Alle Suchbegriffe abgleichen** gibt nur die Produkte zurück, die mit allen Suchbegriffen (ganz oder teilweise) übereinstimmen. Diese Einstellung ist bei langen Produktnamen hilfreich und wenn Mitarbeiter nur begrenzte Produkte in den Sucherergebnissen haben möchten. Für diesen Suchtyp gelten jedoch zwei Einschränkungen:

    - Die Suche wird auf Basis einzelner Produkteigenschaften durchgeführt. Beispielsweise werden nur Produkte zurückgegeben, die alle Suchbegriffe in mindestens einer Produkteigenschaft haben.
    - Dimensionen werden nicht durchsucht.

- Einzelhändler können die Produktsuche so konfigurieren, dass Suchvorschläge angezeigt werden, wenn Produktnamen eingegeben werden. Eine neue Einstellung für diese Funktion ist im POS-Funktionsprofil in einer Gruppe namens **Produktsuche** verfügbar. Die Einstellung hat die Bezeichnung **Beim Eingeben Vorschläge anzeigen**. Diese Funktion ermöglicht Mitarbeitern, schnell das gesuchte Produkt zu finden, da sie nicht den ganzen Namen eingeben müssen.
- Der Produktsuchalgorithmus sucht nun auch in der **Suchbegriff**-Eigenschaft des Produkts nach den Suchbegriffen.

![Produktvorschläge.](./media/Productsuggestions.png "Produktvorschläge")

## <a name="customer-search"></a>Debitorensuche

Die Debitorensuche wird verwendet, um Debitoren für verschiedene Zwecke zu suchen. So möchten Kassierer möglicherweise den Wunschzettel oder die Kaufhistorie eines Debitors anzeigen oder den Debitor zu einer Transaktion hinzufügen. Der Suchenalgorithmus passt die Suchbegriffe mit den Werten an, die in den folgenden Debitoreneigenschaften vorhanden sind:

- Name
- E-Mail-Adresse
- Telefonnummer
- Treuekartennummer
- Anschrift
- Kontonummer

Durch diesen Eigenschaften enthält der Name die besonders Flexibilität für Mehrfach-Schlüsselwortsuchen, da der Algorithmus alle Debitoren zurückgibt, die mit einem gefundenen Suchbegriff übereinstimmen. Die Debitoren, die den meisten Suchbegriffen entsprechen, oben in den Ergebnissen angezeigt. Dieses Verhalten unterstützt Kassierer in Situationen, in denen sie eine Suche durch Eingabe des vollständigen Namens durchführen, und Nachname sowie Vorname bei der ursprünglichen Dateneingabe vertauscht wurden. Aus Leistungsgründen behalten alle anderen Eigenschaften die Reihenfolge der Suchbegriffe bei. Wenn der Auftrag per Suchbegriffe nicht dem Auftrag entspricht, der die Daten speichert, werden keine Ergebnisse zurückgegeben.

Standardmäßig wird eine Debitorensuche in den Debitorenadressbüchern durchgeführt, die mit dem Shop verknüpft sind. Diese Form der Suche wird als *lokale Debitorensuche* bezeichnet. Allerdings können Mitarbeiter auch global nach Debitoren suchen. Sie können also auch in den Shops des Unternehmens und in allen anderen juristischen Personen eine Suche durchführen. Diese Form der Suche wird als *Remote-Debitorensuche* bezeichnet.

Für eine globale Suche können Mitarbeiter die Schaltfläche **Filterergebnisse** am unteren Seitenrand auswählen und dann die Option **Alle Shops durchsuchen**, wie in der folgenden Abbildung gezeigt. In diesem Fall werden nicht nur Debitoren zurückgegeben. Alle Arten von Parteien, die Teil eines Adressbuchs in den Zentralverwaltungen sind, werden ebenfalls zurückgegeben. Zu diesen Parteien zählen Arbeitskräfte, Kreditoren, Mitbewerber und Kontakte.

> [!NOTE]
> Für eine Remote-Debitorensuche müssen mindestens vier Zeichen eingegeben werden.

Bei einer Remote-Debitorensuche wird die Debitorenkennung nicht für Debitoren angezeigt, die von anderen juristischen Personen abgefragt wurden, da für diese Parteien im aktuellen Unternehmen keine Debitorenkennung angelegt wurde. Wenn ein Mitarbeiter jedoch die Debitorendetailseite öffnet, generiert das System automatisch eine Debitorenkennung für die Partei und verknüpft das Debitorenadressbuch des Shops mit dem Debitor. Daher wird der Debitor bei späteren lokalen Shopsuchen angezeigt.

![Globale Debitorensuche.](./media/Globalcustomersearch.png "Globale Debitorensuche")

### <a name="additional-local-customer-search-capabilities"></a>Zusätzliche Funktionen für die lokale Debitorensuche

Sucht ein Benutzer nach einer Telefonnummer, ignoriert das System Sonderzeichen (wie Leerzeichen, Bindestriche und Klammern), die möglicherweise hinzugefügt wurden, wenn der Debitor erstellt wurde. Daher müssen Kassierer sich keine Sorgen über das Telefonnummernformat machen, wenn sie suchen. Wurde beispielsweise die Telefonnummer eines Debitors in der Form **123-456-7890** eingegeben, kann ein Kassierer nach dem Debitor suchen, indem er **1234567890** oder indem er nur die ersten Zahlen einer Telefonnummer eingibt.

> [!NOTE]
> Ein Debitor kann mehrere Telefonnummern und mehrere E-Mails haben. Der Debitorensuchalgorithmus durchsucht auch diese sekundären E-Mails und Telefonnummern, aber auf der Ergebnisseite der Debitorensuche werden nur die primären E-Mails und Telefonnummern angezeigt. Dies kann zu Verwirrung führen, da in den Debitorenergebnissen die gesuchte E-Mail-Adresse oder Telefonnummer nicht angezeigt wird. In einem zukünftigen Release planen wir, die Anzeige der Debitorensuchergebnisse zu verbessern, um diese Informationen anzuzeigen.

Die herkömmliche Debitorensuche kann zeitaufwendig sein, da sie über mehrere Felder hinweg sucht. Stattdessen können Kassierer in einer einzelnen benutzerdefinierten Eigenschaft, wie Name, E-Mail-Adresse oder Telefonnummer suchen. Die Eigenschaften, die der Debitorensuchalgorithmus verwendet, werden zusammen als *Debitorensuchkriterien* bezeichnet. Der Systemadministrator kann einfach ein oder mehrere Kriterien als Verknüpfungen konfigurieren, die in der POS angezeigt werden. Da die Suche auf ein einziges Kriterium eingeschränkt ist, werden nur die relevanten Suchergebnisse angezeigt, und die Leistung ist viel besser, als die Leistung bei einer standardmäßigen Debitorensuche. Die folgende Abbildung zeigt die Debitorensuchverknüpfungen in POS an.

![Kundensuchkriterien Shortcuts.](./media/SearchShortcutsPOS.png "Kundensuchkriterien Shortcuts")

Um Suchkriterien als Verknüpfungen festzulegen, muss der Administrator die Seite **Commerce Parameter** in Commerce öffnen und dann auf der Registerkarte **POS-Suchkriterien** alle Kriterien auswählen, die als Verknüpfungen angezeigt werden sollen.

![Shortcuts für die Suche konfigurieren.](./media/ConfigureShortcutsAX.png "Shortcuts für die Suche konfigurieren")

> [!NOTE]
> Wenn Sie zu viele Verknüpfungen hinzufügen, wird das Dropdownmenü in der Suchleiste in POS überladen, und die Sucherfahrung des Mitarbeiters kann beeinträchtigt werden. Es wird empfohlen, dass Sie nur so viele Verknüpfungen hinzufügen, wie Sie benötigen.

Das Feld **Reihenfolge anzeigen** bestimmt die Reihenfolge, in der Verknüpfungen in POS angezeigt werden. Die angezeigten Kriterien sind die vorkonfigurierten Eigenschaften, die der Debitorensuchalgorithmus verwendet, um nach Debitoren zu suchen. Allerdings können Partner benutzerdefinierte Eigenschaften als Suchenverknüpfungen hinzufügen. Um benutzerdefinierte Eigenschaften als Suchverknüpfungen hinzuzufügen, muss der Systemadministrator die erweiterbare Enumeration (Enum), die für die Debitorensuchkriterien verwendet wird, erweitern und dann die benutzerdefinierten Eigenschaften des Partners als Verknüpfungen markieren. Partner sind dafür zuständig, den Code zu schreiben, um die Ergebnisse zu finden, wenn ihre benutzerdefinierten Verknüpfungen für Suchen verwendet werden.

> [!NOTE]
> Eine benutzerdefinierte Eigenschaft, die der Enumeration hinzugefügt wird, wirkt sich nicht den standardmäßigen Debitorensuchenalgorithmus aus. Das bedeutet, dass der Debitorensuchalgorithmus nicht in der Debitoreneigenschaft suchen wird. Benutzer können nur eine benutzerdefinierte Eigenschaft für Suchvorgänge verwenden, wenn diese benutzerdefinierte Eigenschaft als Verknüpfung hinzugefügt ist oder wenn der Standardsuchenalgorithmus überschrieben wird.

Einzelhändler können auch den Standard-Debitorensuchmodus in POS auf **Alle Shops durchsuchen** einstellen. Diese Konfiguration kann in Szenarios hilfreich sein, bei denen Debitoren, die außerhalb POS erstellt wurden, umgehend gefunden werden müssen (zum Beispiel selbst bevor der Verteilungseinzelvorgang ausgeführt wird). Der Einzelhändler muss dazu die Option **Standard-Debitorensuchmodus** im POS-Funktionsprofil aktivieren. Jede Debitorensuche führt einen Echtzeitanruf an die Zentralverwaltungen durch, sobald die Option auf **Ja** gesetzt ist.

Um unerwartete Leistungsabgänge zu verhindern, ist diese nach Konfiguration hinter einer Flight-Markierung verborgen, die lautet **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING** Um die Einstellungen **Standarddebitoren-Suchenmodus** der Benutzerschnittstelle anzuzeigen, sollte der Einzelhändler ein Supportticket für die Benutzerakzeptanztests (UAT) und die Produktumgebung erstellen. Nachdem das Ticket empfangen wurde, arbeitet das Technikteam bei dem Einzelhändler, um sicherzustellen, dass der Einzelhändler Tests in der Nicht-Produktionsumgebung durchführt, um die Leistung zu ermitteln und alle Optimierungen zu implementieren, die erforderlich sind.

## <a name="cloud-powered-customer-search"></a>Cloudbasierte Debitorensuche

Die öffentliche Vorschauversion der Debitorensuchfunktion mithilfe des Azure Cognitive Search-Dienstes wurde als Teil der Commerce-Version 10.0.18 veröffentlicht. Neben Leistungsverbesserungen profitieren Benutzer des Dienstes auch von einer umfassenden Verfeinerung und verbesserten Relevanzfunktionen. Die Leistungsverbesserungen werden besonders deutlich, wenn die globale Suchfunktion („Alle Shops durchsuchen“) in POS verwendet wird. Dies liegt daran, dass Suchergebnisse aus dem Azure-Suchindex abgerufen werden, anstatt von den Daten in der Commerce-Zentralverwaltung abgefragt zu werden. 

### <a name="enable-the-cloud-powered-search-feature"></a>Die cloudbasierte Suchfunktion aktivieren

> [!NOTE]
> Es ist erforderlich, dass sowohl die Commerce-Zentralverwaltung als auch die Commerce Scale Unit auf Version 10.0.18 aktualisiert werden. Eine Aktualisierung von POS ist nicht erforderlich.

Führen Sie die folgenden Schritte aus, um die cloudbasierte Suchfunktion in der Commerce-Zentralverwaltung zu aktivieren.

1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Funktionsverwaltung**.
1. Suchen und wählen Sie die Funktion **(Vorschau) Cloudbasierte Debitorensuche** und anschließend **Jetzt aktivieren** aus.
1. Rufen Sie **Retail und Commerce > Zentralverwaltungseinrichtung > Commerce-Planer > Commerce-Planer initialisieren** auf, und wählen Sie **OK** aus, um den neuen Einzelvorgang **1010_CustomerSearch** im Formular **Vertriebsplan** anzuzeigen.
1. Rufen Sie **Retail und Commerce > Retail und Commerce IT > Vertriebsplan** auf.
1. Führen Sie den Einzelvorgang **1010_CustomerSearch** aus. Dieser Job veröffentlicht das Datum im Azure-Suchindex. Wenn die Veröffentlichung des Index abgeschlossen ist, wird der Status des Einzelvorgangs auf **Angewendet** gesetzt.
1. Sobald der Status des Einzelvorgangs **1010_CustomerSearch** auf **Angewendet** gesetzt ist, führen Sie den Einzelvorgang **1110 – globale Konfiguration** aus, um die POS-Kanäle der neu aktivierten Funktion in der **Funktionsverwaltung** zu aktualisieren.
1. Führen Sie anschließend in regelmäßigen Abständen den Einzelvorgang **1010_CustomerSearch** aus, um Debitorenaktualisierungen an den Suchindex zu senden.

> [!NOTE]
> Für die erste Indexveröffentlichung kann der Einzelvorgang **1010_CustomerSearch** einige Stunden dauern, da alle Debitorendatensätze an den Azure-Suchindex gesendet werden. Nachfolgende Aktualisierungen sollten einige Minuten dauern. In dem Zeitraum, in dem die cloudbasierte Suchfunktion aktiviert, aber die Indexveröffentlichung noch nicht abgeschlossen ist, wird bei der Debitorensuche aus POS standardmäßig die vorhandene SQL-basierte Suche verwendet. Dies stellt sicher, dass es keine Unterbrechungen bei Shopvorgängen gibt.

### <a name="functional-differences-from-the-existing-search"></a>Funktionale Unterschiede zur bestehenden Suche

Die folgende Liste zeigt, wie sich die cloudbasierte Debitorensuchfunktion von der vorhandenen Suchfunktion unterscheidet. 

- Debitoren, die in der Commerce-Zentralverwaltung erstellt und bearbeitet wurden, werden an den Azure-Suchindex gesendet, wenn der Einzelvorgang **1010_CustomerSearch** ausgeführt wird. Diese Aktualisierungen benötigen mindestens 15 bis 20 Minuten, um den Index zu aktualisieren. POS-Benutzer können etwa 15 bis 20 Minuten nach den Aktualisierungen in der Commerce-Zentralverwaltung nach neuen Debitoren suchen (oder anhand aktualisierter Informationen suchen). Wenn Ihr Geschäftsprozess es erfordert, dass Debitoren, die in der Commerce-Zentralverwaltung erstellt wurden, sofort in POS gesucht werden können, ist dieser Dienst möglicherweise nicht der richtige für Sie.
- In POS erstellte neue Debitoren werden von der Commerce Scale Unit an den Azure-Suchindex gesendet und können sofort in jedem Shop gesucht werden. Wenn die asynchrone Debitorenerstellungsfunktion aktiviert ist, werden neue Debitorendatensätze nicht im Azure-Suchindex von der Commerce Scale Unit veröffentlicht und können erst in POS gesucht werden, wenn die Debitoreninformationen mit der Commerce-Zentralverwaltung synchronisiert und Debitorenkennungen für asynchrone Debitoren generiert wurden. Der Einzelvorgang **1010_CustomerSearch** kann dann die asynchronen Debitorendatensätze an den Azure-Suchindex senden. Im Durchschnitt dauert es ungefähr 30 Minuten, bis neu erstellte asynchrone Debitoren in POS gesucht werden können. Diese Schätzung geht davon aus, dass die Einzelvorgänge **1010_CustomerSearch**, **P-Einzelvorgang** und **Debitoren und Geschäftspartner im asynchronen Modus synchronisieren** alle 15 Minuten ausgeführt werden.
- Die cloudbasierte Suche sucht auch nach sekundären E-Mails und Telefonnummern von Debitoren. Derzeit werden in den Debitorensuchergebnissen jedoch nur die primäre Telefonnummer und die primäre E-Mail-Adresse der Kunden angezeigt. Auf den ersten Blick scheint es, dass irrelevante Suchergebnisse zurückgegeben wurden. Wenn Sie jedoch die sekundäre E-Mail-Adresse und Telefonnummer eines Debitoren in den Suchergebnissen überprüfen, können Sie verifizieren, ob das gesuchte Keyword zu einer Debitorenübereinstimmung geführt hat. Um solche Verwirrung zu vermeiden, ist geplant, die Suchergebnisseite zu verbessern, damit Benutzer leichter nachvollziehen können, warum ein Suchergebnis zurückgegeben wurde.
- Die Anforderung, bei einer globalen Suche mit mindestens 4 Zeichen zu suchen („Alle Shops durchsuchen“), gilt nicht für diesen Dienst.

> [!NOTE]
> Die Debitorensuchfunktion mit dem Azure Cognitive Search-Dienst ist in begrenzten Regionen für die Vorschauversion verfügbar. Die Debitorensuchfunktion ist *nicht* in folgenden Regionen verfügbar:
> - Brasilien
> - Indien
> - Kanada
> - Vereinigtes Königreich

[!INCLUDE[footer-include](../includes/footer-banner.md)]
