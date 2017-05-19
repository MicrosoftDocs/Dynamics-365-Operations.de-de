---
title: "Aktivitätssuche"
description: "Dieser Artikel beschreibt die Aktivitätssuchfunktion in Microsoft Dynamics 365 for Operations.. Mit der Aktivitätssuche finden Sie Aktivitäten auf einer Seite und können diese ausführen."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2ff12088d432d3e8693dfd9662cb0ead82fd0191
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="action-search"></a>Aktivitätssuche

[!include[banner](../includes/banner.md)]


Dieser Artikel beschreibt die Aktivitätssuchfunktion in Microsoft Dynamics 365 for Operations.. Mit der Aktivitätssuche finden Sie Aktivitäten auf einer Seite und können diese ausführen.

<a name="introduction"></a>Einführung
------------

Seiten in Microsoft Dynamics 365 for Operations enthalten hauptsächlich Befehle auf Aktivitätsbereichen, sowohl auf dem Standardaktivitätsbereich am Anfang einer Seite und auf den Symbolleisten wird, die in verschiedenen Bereichen der Seite angezeigt werden. In den Vorgängerversionen konnte mit einer Tippfunktion schnell auf jede Schaltfläche im Aktivitätsbereich zugegriffen werden, indem Sie die Taste ALT und eine Reihe von Buchstaben drückten. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) Allerdings sind in der aktuellen Version von Microsoft Dynamics 365 for Operations Tastenkombinationen nicht mehr verfügbar, wurden jedoch durch die Funktion Aktivitätssuche ersetzt. Mit dieser neuen Funktion können Sie schnell nach einer Schaltfläche suchen und sie von jedem sichtbaren Aktivitätsbereich ausführen.

## <a name="using-action-search"></a>Verwenden der Aktivitätssuche
Um die Funktion „Aktivitätssuche“ zu verwenden, führen Sie die folgenden Schritte aus:

1.  Klicken Sie im Aktivitätsbereich auf das Feld **Aktivitätssuche**. (Das Feld **Aktivitätssuche** enthält ein Lupensymbol.)
2.  Geben Sie den vollständigen Namen oder einen Teil des Namens der Schaltfläche ein, die Sie ausführen möchten. Sie können auch suchen, indem Sie Wörter von der Schaltfläche "Pfad" verwenden. (Weitere Informationen, finden Sie im nächsten Abschnitt dieses Artikels). Normalerweise wird die Schaltfläche in der Nähe der Ergebnisliste angezeigt, nachdem Sie zwei bis zu vier Zeichen eingegeben haben.
3.  Suchen Sie die Schaltfläche in der Ergebnisliste, und führen Sie sie aus (mithilfe der Maus oder Tastatur).

Nachdem die Schaltfläche ausgeführt wird, kehrt der Fokus auf Ihre letzte Position auf der Seite zurück, sodass Sie mit der Arbeit fortfahren können. 

[![Suchfeld Aktivität](./media/action-search-field.png)](./media/action-search-field.png)

Sie können die Aktivitätssuche auch starten, indem Sie Strg+/ oder ALT+Q drücken. Drücken Sie die Tastenkombination erneut, um den Fokus zu Ihrer letzten Position auf der Seite zurückzukehren.

## <a name="understanding-the-results-list"></a>Verstehen der Ergebnisliste
In Dynamics 365 for Operations müssen Sie oft die Position und den Kontext einer Schaltfläche kennen, um den Zweck dieser Schaltfläche vollständig zu verstehen. Daher werden zusätzliche Information für jeden Artikel der Ergebnisliste angezeigt, um Sie zu unterstützen, genau zu veranschaulichen, welche Schaltflächen in der Liste angezeigt werden. Insbesondere wird der „Pfad“ der Schaltfläche angezeigt. Dieser Pfad kann möglicherweise die Beschriftungen der folgenden Benutzeroberflächenelemente enthalten, wie relevant:

-   Registerkarte (Aktivitätsbereich)
-   Schaltflächengruppe
-   Menüschaltfläche (wenn die Schaltfläche innerhalb einer Menüschaltfläche ist)
-   Menütrennzeichen (wenn die Schaltfläche innerhalb einer benannten Gruppe innerhalb einer Menüschaltfläche ist)
-   Gruppe oder Registerkarte auf der Seite (beispielsweise der Name eines Inforegisters)

Beispielsweise haben Sie **tot** in das Feld **Aktivitätssuche** eingegeben und überprüfen nun die Ergebnisliste. Der erste Eintrag, für eine Schaltfläche mit der Bezeichnung **Summen** wird markiert. Ein Schaltflächenpfad der **Ansicht** &gt; **Auftrag** wird auch angezeigt. Der Teil des **Auftrags** des Pfads, der der Registerkarte **Auftrag** im Aktivitätsbereich entspricht und der Teil **Ansicht** des Pfads, der der Gruppe auf der Registerkarte **Ansicht** entspricht. Ebenso informiert der Pfad der Schaltfläche **Rechnungsrabatt** (**Verkauf** &gt; **berechnen**) Sie, dass sich die Schaltfläche in der Gruppe  **Berechnen** auf der Registerkarte des Aktivitätsbereichs **Verkauf** befindet. Daher können diese Informationen Ihnen genau veranschaulichen, welche Schaltfläche nach Aktivitätssuche ausgelöst wird (falls diese Schaltfläche in der Ergebnisliste ausgewählt ist). 

[![Aktivität-Suche-Feld-mit Daten](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

Im vorherigen Beispiel ergibt sich die angezeigte Aktivitätssuche vom Standardaktivitätsbereich oben einer Seite. Allerdings zeigt die Aktivitätssuche auch Ergebnisse aus sichtbaren Symbolleisten an, die sich an anderen Stellen auf der Seite befinden. So finden Sie die Schaltfläche für **Verfügbarer Lagerbestand**, die auf dem Inforegister **Auftragspositionen**** ist. In diesem Fall wird im Schaltflächenpfad in der Ergebnisliste (**Auftragspositionen** &gt; **Lager** &gt; **Ansicht**) Sie informieren, dass die Schaltfläche unter Überschrift **Ansicht** in der Menüschaltfläche **Bestand** im Inforegister **Auftragsposition** ist. 

[![Verfügbarer Lagerbestand](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Aktivitätssuche im Vergleich zur Navigationssuche
Während die Aktivitätssuche vorgesehen ist, um Aktivitäten auf einer Seite zu suchen und auszuführen, gibt es einen separaten Suchenmechanismus für die Suche und zum Navigieren zu Seiten in Dynamics 365 for Operations gibt. Weitere Informationen zu dieser Funktion finden Sie im Artikel [Navigationssuche](navigation-search.md)




