---
title: "Aktivitätssuche"
description: "In diesem Artikel wird beschrieben die Aktivitätssuchenfunktionen in Microsoft Dynamics 365 für Arbeitsgänge. Aktivitätssuche können Sie Aktivitäten, wenn eine Palette suchen und auszuführen."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 689d8f9fb0501c5007db21d41f126737af77b89e
ms.lasthandoff: 03/31/2017


---

# <a name="action-search"></a>Aktivitätssuche

In diesem Artikel wird beschrieben die Aktivitätssuchenfunktionen in Microsoft Dynamics 365 für Arbeitsgänge. Aktivitätssuche können Sie Aktivitäten, wenn eine Palette suchen und auszuführen.

<a name="introduction"></a>Einführung
------------

Seiten in Microsoft Dynamics 365 für Arbeitsgänge vornehmen hauptsächlich Befehle auf Aktivitätsbereichen, der Standardaktivitätsbereich xxxx_4, der am Anfang einer Seite und der Symbolleisten wird, die in verschiedenen Bereichen der Seite angezeigt werden. In den Vorgängerversionen Bereich eine entscheidende Tippfunktion schnell jede Schaltfläche im Aktivitätsbereich zugreifen, indem Sie die Schlüssel und anschließend von Buchstaben drückte. 

![keyTipsAX6 ([]. /media/keytipsax6.png)]". /media/keytipsax6.png), Jedoch in der aktuellen Version von Microsoft Dynamics 365 für Arbeitsgänge, Tasteninfos sind nicht mehr verfügbar, werden jedoch durch die AktivitätsSuchfunktion ersetzt. Mit dieser neuen Funktion können Sie schnell nach einer Schaltfläche suchen und sie von jedem sichtbaren Aktivitätsbereich ausführen.

## <a name="using-action-search"></a>Verwenden der Aktivitätssuche
Um die Funktion „Aktivitätssuche“ zu verwenden, führen Sie die folgenden Schritte aus:

1.  Klicken Sie im Aktivitätsbereich auf das Feld **Aktivitätssuche**. (Das Feld **Aktivitätssuche** enthält ein Lupensymbol.)
2.  Geben Sie alle oder einen Teil des Namens der Schaltfläche ein, die Sie ausführen möchten. Sie können auch nach Arbeitskräften suchen, indem Sie Wörter verwenden vom Pfad der Schaltfläche "Löschen". (Weitere Informationen, finden Sie im nächsten Abschnitt dieses Artikels). Normalerweise wird die Schaltfläche nach der Spitze der Ergebnisliste, nachdem Sie zwei bis zu vier Zeichen eingegeben haben.
3.  Suchen Sie die Schaltfläche in der Ergebnisliste, und führen Sie sie aus (mithilfe der Maus oder Tastatur).

Nachdem die Schaltfläche ausgeführt wird, kehrt der Fokus auf Ihre letzte Position auf der Seite zurück, sodass Sie mit der Arbeit fortfahren können. 

![Aktivität-SucheFeld( [] . /media/action-search-field.png)]". /media/action-search-field.png)

Sie können die Aktivitätssuche auch starten, indem Sie Strg+/ oder ALT+Q drücken. Drücken Sie die Tastenkombination erneut, um den Fokus zu Ihrer letzten Position auf der Seite zurückzukehren.

## <a name="understanding-the-results-list"></a>Verstehen der Ergebnisliste
Häufig in Dynamics 365 für Arbeitsgänge, müssen Sie dessen Position und den Kontext einer Schaltfläche kennen, um den Zweck dieser Schaltfläche vollständig zu verstehen. Daher wird zusätzliche Information für jeden Artikel der Ergebnisliste angezeigt, um Sie zu unterstützen, genau zu veranschaulichen, welche Schaltflächen in der Liste angezeigt werden. Insbesondere wird der „Pfad“ der Schaltfläche angezeigt. Dieser Pfad kann möglicherweise die Beschriftungen der folgenden Benutzeroberflächenelemente enthalten, wie relevant:

-   Registerkarte (Aktivitätsbereich)
-   Schaltflächengruppe
-   Menüschaltfläche (wenn die Schaltfläche innerhalb einer Menüschaltfläche ist)
-   Menütrennzeichen (wenn die Schaltfläche innerhalb einer benannten Gruppe innerhalb einer Menüschaltfläche ist)
-   Gruppe oder Registerkarte auf der Seite (beispielsweise der Name eines Inforegisters)

Beispielsweise haben Sie **tot** in das Feld **Aktivitätssuche** eingegeben und überprüfen nun die Ergebnisliste. Der erste Eintrag, für eine Schaltfläche, die Bezeichnung ** Summen **, wird markiert. Ein Schaltflächenpfad ** Auftrag ** &gt; ** der Ansicht ** wird auch angezeigt. ** Der Auftrag ** Teil des Pfades entspricht der Reihenfolge ** ** Registerkarte im Aktivitätsbereich, und der Ansicht ** ** Teil des Pfades entspricht der Ansicht ** ** Gruppe auf dieser Registerkarte. Ebenso informiert der Pfad der Rechnungsrabatt ** ** Schaltfläche (** Verkauf &gt; ** ** berechnen Sie **) Sie, dass die Schaltfläche in ist ** berechnen ** Gruppe auf Verkauf ** ** Registerkarte des Aktivitätsbereichs. Daher können diese Informationen, Ihnen genau zu veranschaulichen, die Schaltfläche nach Aktivitätssuche ausgelöst wird (falls diese Schaltfläche in der Ergebnisliste ausgewählt). 

![Aktivität-Suche-Feld-mitDaten( [] . /media/action-search-field-with-data.png)]". /media/action-search-field-with-data.png) 

Im vorherigen Beispiel ergibt sich die angezeigte Aktivitätssuche vom Standardaktivitätsbereich oben einer Seite. Allerdings zeigt die Aktivitätssuche auch Ergebnisse aus sichtbaren Symbolleisten an, die sich an anderen Stellen auf der Seite befinden. So finden Sie die für ** verfügbarer Lagerbestand ** Schaltfläche, die auf dem Inforegister ** Auftragspositionen ** ist. In diesem Fall wird in der Schaltflächenpfad in der Ergebnisliste (**Auftragspositionen ** &gt; ** Lager ** &gt; ** Ansicht ** ) Sie, dass die Schaltfläche unter der Ansicht ** ** Überschrift ** der auf Lager ** Menüschaltfläche im ** Auftragspositionen ** Inforegister werden. 

[] (![verfügbare Lagerbestand. -/media/onhand - inventory.png)]". -/media/onhand - inventory.png)

## <a name="action-search-vs-navigation-search"></a>Aktivitätssuche im Vergleich zur Navigationssuche
Während Aktivitätssuche bezieht, um zu suchen und Ausführungsaktivitäten auf einer Seite, es einen separaten Suchenmechanismus für die Suche und zum Navigieren zu Seiten in Dynamics 365 für Arbeitsgänge vorhanden sind. Weitere Informationen zu dieser Funktion finden Sie Navigationssuche, [](), navigation-search.md, Artikel.


