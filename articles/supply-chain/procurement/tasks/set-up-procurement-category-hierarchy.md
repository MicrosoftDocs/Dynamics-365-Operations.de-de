--- 
title: Einrichten einer Beschaffungskategoriehierarchie
description: Dieses Verfahren zeigt Ihnen an, wie neue Knoten in einer Beschaffungskategorie-Hierarchie erstellt und das Einrichten einer in konfiguriert einem Beschaffungsprozess zu verwendende Beschaffungskategorie.
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6ad5c8552a6989e9093d0b1325754bc0f6d19372
ms.openlocfilehash: 4541d029c9c3be3ee42332e5d8ff183dd503f13e
ms.contentlocale: de-de
ms.lasthandoff: 11/06/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a>Einrichten einer Beschaffungskategoriehierarchie

[!include[task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt Ihnen an, wie neue Knoten in einer Beschaffungskategorie-Hierarchie erstellt und das Einrichten einer in konfiguriert einem Beschaffungsprozess zu verwendende Beschaffungskategorie. Diese Aufgaben werden normalerweise von einem Einkaufsleiter ausgeführt. Überprüfen Sie zunächst können, muss es eine Kategoriehierarchie vom Typ Beschaffung geben. Wenn Sie ein Demodatunternehmen verwenden, können Sie diese Prozedur im USMF-Unternehmen ausführen.


## <a name="add-a-new-procurement-category"></a>Neue Beschaffungskategorie hinzufügen
1. Wechseln Sie zu "Beschaffung" > "Beschaffungskategorien".
2. Klicken Sie auf Kategoriehierarchietypen bearbeiten.
    * Die aktuelle Beschaffungskategorie-Hierarchie wird in der linken Seite der Seite angezeigt. Sie sind dabei, die Hierarchie zu ändern.  
3. Klicken Sie auf Neuer Kategorieknoten.
    * Das System wählt den obersten Knoten standardmäßig aus. Wenn Sie dieses Verfahren ausführen, während ein Aufgabenhandbuch, Sie auf die Schaltfläche Entsperren klicken und einen anderen übergeordneten Knoten auswählen kann, um den neuen Knoten in einzufügen. Sobald das getan haben, sperren Sie das Aufgabenhandbuch erneut und klicken Sie anschließend auf Neues Kategorie Knoten.  
4. Geben Sie im Feld "Name" einen Wert ein.
5. Geben Sie im Feld "Beschreibung" einen Wert ein.
6. Geben Sie im Feld "Anzeigename" einen Wert ein.
    * Der Anzeigename ist optional. Er wird in den Kategoriesuchen zusammen mit dem Kategorienamen angezeigt.  
7. Klicken Sie auf "Speichern".

## <a name="add-products-to-your-new-procurement-category"></a>Hinzufügen von Produkten zu Ihrer neuen Beschaffungskategorie
1. Wechseln Sie zu "Beschaffung" > "Beschaffungskategorien".
    * Wählen Sie den Knoten aus, den Sie soeben gelegt haben. Wenn Sie die Prozedur wie ein Aufgabenhandbuch ausführen, müssen Sie möglicherweise auf die Schaltfläche "Entsperren" klicken, bevor Sie den Knoten auswählen können.  
2. Schalten Sie die Erweiterung des Produkt-Abschnitts ein/aus.
3. Klicken Sie auf Mitarbeiterprodukten mit der Beschaffungskategorie hinzufügen.
4. Wählen Sie das Produkt aus, das Sie der Beschaffungskategorie hinzufügen möchten.
5. Klicken Sie auf den Pfeil, um das Produkt auszuwählen.
6. Wählen Sie ein weiteres Produkt aus, das Sie der Beschaffungskategorie hinzufügen möchten.
7. Klicken Sie auf den Pfeil, um das Produkt auszuwählen.
8. Klicken Sie auf "OK".

## <a name="add-approved-and-preferred-vendors"></a>Dient zum Hinzufügen genehmigter und bevorzugter Kreditoren.
1. Schalten Sie die Erweiterung des Abschnitts "Kreditoren" ein/aus.
2. Klicken Sie auf Hinzufügen.
    * Gehen Sie folgendermaßen vor, um einen Kreditor einer Beschaffungskategorie hinzuzufügen und anzugeben, ob ein Kreditor in einer Kategorie bevorzugt verwendet oder gerade genehmigt wird. Wenn Sie einen Kreditor aus einer Kategorie löschen, werden aus der Vergangenheit vorliegende Buchungen mit dem Kreditor nicht aus der Kategorie gelöscht.   
3. Finden Sie den Händler, den Sie der Kategorie hinzufügen möchten.
4. Klicken Sie auf den Pfeil, um den Händler auszuwählen.
5. Klicken Sie auf "OK".
6. Hier können Sie die Händlerzeile auswählen, den Sie ändern möchten.
7. Wählen Sie im Feld "Händlerstatus" eine Option aus.
    * Die Kreditoren-Auswahleinstellung in der Kategorierichtlinien-Regel unterliegt, ob bevorzugt, genehmigt oder alle Kreditoren auf Bestellanforderungen verfügbar sind.   

## <a name="add-additional-information-to-the-category"></a>Weitere Informationen zur Kategorie hinzufügen.
1. Erweitern oder reduzieren Sie den Abschnitt Kriteriengruppen zur Kreditorenbewertung.
    * Diese Registerkarte bietet die Möglichkeit, festlegen, welche Kriterien die Kreditoren in der Beschaffungskategorie bewertet werden sollen mit. Um dies zu tun, klicken Sie auf Hinzufügen und wählen Sie anschließend eine Kreditorenbewertungsgruppe aus, die die Kriterien enthält, gewünschten.  
2. Schalten Sie die Erweiterung des Fragebögen-Abschnitts ein/aus.
    * Diese Registerkarte bietet die Möglichkeit, Fragebögen hinzu, die in der Bestellanforderung angezeigt werden, solange Sie legen den Aktivitätstyp "auf die Anforderung". Die anfordernde Person muss einen Fragebogen dann ergänzen, bevor eine Anforderung für das jeweilige Produkt oder die Produkte in der Beschaffungskategorie senden.  
3. Erweitern oder reduzieren Sie den Abschnitt Artikelverkaufssteuergruppen.
4. Klicken Sie im Feld "Artikel-Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Wählen Sie eine Mehrwertsteuergruppe aus.
6. Schalten Sie die Erweiterung des Abschnitts "Kategorieseite" ein/aus.
    * Kategorieseiten werden in der Kategoriehierarchieseite erstellt. Sie enthalten Informationen über die Beschaffungskategorie, wie etwa zu in einer Kategorie enthaltenen Produkttypen, Bilder von den in einer Kategorie enthaltenen Produkten und Ankündigungen zu Sonderverkäufen oder Rabatten, die in einer Kategorie verfügbar sind. Die Informationen in einer Kategorieseite werden auf Bestellanforderungen angezeigt.  
7. Schließen Sie die Seite.


