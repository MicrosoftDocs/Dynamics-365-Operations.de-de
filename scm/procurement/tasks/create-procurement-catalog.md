--- 
title: Beschaffungskatalog erstellen
description: Dieser Leitfaden zeigt Ihnen, wie ein Beschaffungskatalog erstellt wird.
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 19d053a0bdbdcc764b3361fe5a326e8c68cdc682
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-procurement-catalog"></a>Beschaffungskatalog erstellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Dieser Leitfaden zeigt Ihnen, wie ein Beschaffungskatalog erstellt wird. Diese Aufgabe wird normalerweise von einem Prokuristen ausgeführt. Sie erfahren auch, wie Mitarbeiter den Katalog verwenden können, wenn sie eine Anforderung erstellen. Bevor Sie einen Katalog erstellen können, muss es in Ihrem System eine Beschaffungskategoriehierarchie geben. Die Hierarchie wird vom neuen Katalog zusammen mit allen Produkten geerbt, die sich in der Hierarchie befinden. Sie können diesen Leitfaden im Demodatenunternehmen USMF verwenden, in dem die Beschaffungskategoriehierarchie verfügbar ist, sowie die Beispiele, die in den Prozedurschritten verwendet werden.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Sicherstellen, dass eine Beschaffungskategoriehierarchie vorhanden ist
1. Wechseln Sie zu "Beschaffung" > "Beschaffungskategorien".
    * Eine Beschaffungskategoriehierarchie ist im USMF-Demodatenunternehmen verfügbar und Produkte sind der Kategorie "Bürogeräte/Computer" hinzugefügt worden. Wenn Sie diese Prozedur als Aufgabenleitfaden ausführen, müssen Sie den Leitfaden entsperren, wenn Sie die Kategorie durchsuchen möchten. Wenn eine Hierarchie nicht verfügbar wäre, würden Sie sie erstellen, indem Sie auf "Neu" klicken. Dies kann nur einmal ausgeführt werden.  
2. Schließen Sie die Seite.

## <a name="create-a-catalog"></a>Einen Katalog erstellen
1. Wechseln Sie zu Beschaffung > Kataloge > Beschaffungskataloge.
2. Klicken Sie auf "Neuer Beschaffungskatalog" um das Ablagedialogfeld zu öffnen
3. Geben Sie im Feld "Name" einen Wert ein.
4. Klicken Sie auf "OK".
5. Im Baum erweitern Sie "UNTERNEHMENSBESCHAFFUNGSKATEGORIEN".
6. Erweitern Sie "BÜROGERÄTE" im Baum.
7. Wählen Sie im Baum "Computer" aus.
    * Die Produkte aus der Beschaffungskategorie werden in der Liste angezeigt. Wenn Sie ein Produkt der Kategorie hinzufügen möchten, müssen Sie dies auf der Seite "Beschaffungskategoriehierarchie" oder auf der Seite "Artikeldetails" erledigen.  
    * Der standardmäßige Aktualisierungstyp bestimmt, ob neue Produkte, die der Beschaffungskategoriehierarchie hinzugefügt wurden, im Katalog sofort sichtbar sind. Wenn der Aktualisierungstyp auf "Dynamisch" festgelegt ist, sind Änderungen sofort sichtbar. Wenn der Aktualisierungstyp auf "Statisch" festgelegt ist, sind neue Produkte nur sichtbar, wenn Personen den Katalog benutzen, nachdem der Katalog erneut veröffentlicht wurde. Die Aktivität "Veröffentlichen" ist im Aktionsbereich oben auf der Seite verfügbar. Wenn Produkte von der Beschaffungskategoriehierarchie entfernt werden, ist die Änderung sofort sichtbar, unabhängig vom Wert im Feld "Standardmäßiger Aktualisierungstyp".  
8. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
9. Klicken Sie auf "Ausblenden".
10. Klicken Sie im Aktionsbereich auf "Kategorienavigation".
11. Klicken Sie auf "Deaktivieren".
12. Klicken Sie im Aktionsbereich auf "Kategorienavigation".
13. Klicken Sie auf Aktivieren.
14. Klicken Sie auf "Katalog aktivieren".
15. Schließen Sie die Seite.

## <a name="make-the-catalog-visible"></a>Den Katalog sichtbar machen
1. Wechseln Sie zu Beschaffung > Einstellungen > Richtlinien > Beschaffungsrichtlinien.
2. Wählen Sie die "Beschaffungsrichtlinie USMF" aus.
    * Sie müssen die Einkaufsrichtlinie für die juristische Person auswählen, in der die Arbeitskraft, der mit Ihrem Benutzerprofil verbunden ist, Produkte bestellen darf. In den USMF-Demodaten ist der Benutzer "Administrator" mit der Arbeitskraft mit Namen Julia Funderburk verbunden und sie bestellt standardmäßig Produkte in USMF.  
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Wählen Sie den Katalog aus, das Sie soeben erstellt haben.
5. Klicken Sie auf "OK".
6. Schließen Sie die Seite.
7. Schließen Sie die Seite.

## <a name="use-the-catalog"></a>Den Katalog verwenden
1. Wechseln Sie zu Beschaffung > Bestellanforderungen > Alle Bestellanforderungen.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein.
4. Klicken Sie auf "OK".
5. Klicken Sie auf Produkte hinzufügen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Sie können die Kategoriehierarchie auf der linken Seite oder den Filter oben an der Liste verwenden, um die Produkte zu filtern.  
7. Zu Positionen hinzufügen
8. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
9. Zu Positionen hinzufügen
10. Klicken Sie auf "OK".


