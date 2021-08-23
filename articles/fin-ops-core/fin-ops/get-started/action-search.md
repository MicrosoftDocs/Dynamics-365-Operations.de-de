---
title: Aktivitätssuche
description: Dieser Artikel beschreibt die Aktivitätssuchfunktion. Mit der Aktivitätssuche finden Sie Aktivitäten auf einer Seite und können diese ausführen.
author: jasongre
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 190cfc8f4509ad3c61057c66ec0b920408c3c421e19c5147987892a918311537
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734639"
---
# <a name="action-search"></a>Aktivitätssuche

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Aktivitätssuchfunktion. Mit der Aktivitätssuche finden Sie Aktivitäten auf einer Seite und können diese ausführen.

## <a name="introduction"></a>Einführung

Seiten enthalten hauptsächlich Befehle in Aktivitätsbereichen, sowohl im Standardaktivitätsbereich am Anfang einer Seite als auch auf den Symbolleisten, die in verschiedenen Bereichen der Seite angezeigt werden. In den Vorgängerversionen konnte mit einer Tippfunktion schnell auf jede Schaltfläche im Aktivitätsbereich zugegriffen werden, indem Sie die Taste ALT und eine Reihe von Buchstaben drückten.

[![keyTipsAX6.](./media/keytipsax6.png)](./media/keytipsax6.png)

Die Funktion „Aktivitätssuche“ ersetzt die entscheidenden Tipps, die nicht mehr verfügbar sind. Mit dieser neuen Funktion können Sie schnell nach einer Schaltfläche suchen und sie von jedem sichtbaren Aktivitätsbereich ausführen.

## <a name="using-action-search"></a>Verwenden der Aktivitätssuche

Um die Funktion „Aktivitätssuche“ zu verwenden, führen Sie die folgenden Schritte aus:

1. Klicken Sie im Aktivitätsbereich auf das Feld **Aktivitätssuche**. (Das Feld **Aktivitätssuche** enthält ein Lupensymbol.)
2. Geben Sie den vollständigen Namen oder einen Teil des Namens der Schaltfläche ein, die Sie ausführen möchten. Sie können auch suchen, indem Sie Wörter von der Schaltfläche "Pfad" verwenden. (Weitere Informationen, finden Sie im nächsten Abschnitt dieses Artikels). Normalerweise wird die Schaltfläche in der Nähe der Ergebnisliste angezeigt, nachdem Sie zwei bis zu vier Zeichen eingegeben haben.
3. Suchen Sie die Schaltfläche in der Ergebnisliste, und führen Sie sie aus (mithilfe der Maus oder Tastatur).

Nachdem die Schaltfläche ausgeführt wird, kehrt der Fokus auf Ihre letzte Position auf der Seite zurück, sodass Sie mit der Arbeit fortfahren können.

[![Suchfeld „Aktivität“.](./media/action-search-field.png)](./media/action-search-field.png)

Sie können die Aktivitätssuche auch starten, indem Sie Strg+/ oder ALT+Q drücken. Drücken Sie die Tastenkombination erneut, um den Fokus zu Ihrer letzten Position auf der Seite zurückzukehren.

## <a name="understanding-the-results-list"></a>Verstehen der Ergebnisliste

Oft müssen Sie die Position und den Kontext einer Schaltfläche kennen, um den Zweck dieser Schaltfläche vollständig zu verstehen. Daher werden zusätzliche Information in der Ergebnisliste angezeigt, um genau zu veranschaulichen, welche Schaltflächen in der Liste angezeigt werden. Insbesondere wird der „Pfad“ der Schaltfläche angezeigt. Dieser Pfad kann möglicherweise die Beschriftungen der folgenden Benutzeroberflächenelemente enthalten, wie relevant:

- Registerkarte (Aktivitätsbereich)
- Schaltflächengruppe
- Menüschaltfläche (wenn die Schaltfläche innerhalb einer Menüschaltfläche ist)
- Menütrennzeichen (wenn die Schaltfläche innerhalb einer benannten Gruppe innerhalb einer Menüschaltfläche ist)
- Gruppe oder Registerkarte auf der Seite (beispielsweise der Name eines Inforegisters)

Beispielsweise haben Sie **tot** in das Feld **Aktivitätssuche** eingegeben und überprüfen nun die Ergebnisliste. Der erste Eintrag, für eine Schaltfläche mit der Bezeichnung **Summen** wird markiert. Ein Schaltflächenpfad der **Ansicht** &gt; **Auftrag** wird auch angezeigt. Der Teil **Auftrag** des Pfades entspricht der Registerkarte **Auftrag** im Aktivitätsbereich **Ansicht**, und der Teil des Pfades entspricht der Gruppe **Ansicht** auf dieser Registerkarte. Ebenso informiert Sie der Pfad der Schaltfläche **Rechnungsrabatt** (**Verkaufen** &gt; **Berechnen**), dass die Schaltfläche in der Gruppe **Berechnen** auf der Registerkarte **Verkaufen** im Aktivitätsbereich ist. Daher können diese Informationen Ihnen genau veranschaulichen, welche Schaltfläche nach Aktivitätssuche ausgelöst wird (falls diese Schaltfläche in der Ergebnisliste ausgewählt ist).

[![Feld „Aktivitätssuche“ mit Daten.](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)

Im vorherigen Beispiel ergibt sich die angezeigte Aktivitätssuche vom Standardaktivitätsbereich oben einer Seite. Allerdings zeigt die Aktivitätssuche auch Ergebnisse aus sichtbaren Symbolleisten an, die sich an anderen Stellen auf der Seite befinden. So finden Sie die Schaltfläche für **Verfügbarer Lagerbestand**, die auf dem Inforegister **Auftragspositionen** ist. In diesem Fall informiert der Schaltflächenpfad in der Ergebnisliste (**Auftragspositionen** &gt; **Lager** &gt; **Ansicht**) Sie, dass die Schaltfläche unter Überschrift **Ansicht** in der Menüschaltfläche **Bestand** im Inforegister **Auftragspositionen** ist.

[![Verfügbarer Lagerbestand.](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

> [!NOTE]
> Es gibt einige Schaltflächen, die in der Aktionssuche nicht angezeigt werden. Dazu gehören Schaltflächen für den Drop-Dialog und Schaltflächen aus Unterformularen. 

## <a name="action-search-vs-navigation-search"></a>Aktivitätssuche im Vergleich zur Navigationssuche

Während die Aktivitätssuche vorgesehen ist, um Aktivitäten auf einer Seite zu suchen und auszuführen, gibt es einen separaten Suchenmechanismus für die Suche und zum Navigieren zu Seiten. Weitere Informationen zu dieser Funktion finden Sie im Artikel [Navigationssuche](navigation-search.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]