---
title: Kanban-Planungsgruppen definieren
description: Lean Schedule-Gruppen werden zur Gruppierung von Einzelprodukten in der Kanban-Planung verwendet.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4187381b838825b21a354eeecdf48693d919975b07a881ba32d234135694ad06
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754583"
---
# <a name="define-lean-schedule-groups"></a>Kanban-Planungsgruppen definieren

[!include [banner](../../includes/banner.md)]

Lean Schedule-Gruppen werden zur Gruppierung von Einzelprodukten in der Kanban-Planung verwendet. Die Gruppierung kann als generische Zuordnung pro Unternehmen oder für eine Arbeitsgruppe ausgeführt werden. Jede Gruppe hat den Farbcode, der zur optische Anzeige auf der Kanbanplanung-Listenseite zugewiesen ist. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="define-lean-scheduling-group"></a>Definieren einer Lean Schedule-Gruppen
1. Wechseln Sie zu "Produktinformationsverwaltung" > "Lean-Manufacturing" > "Lean-Schedule-Gruppen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Schedule-Gruppe" einen Wert ein.
    * Eine Schedule-Gruppe kann als globale Gruppe oder für eine bestimmte Arbeitsgruppe definiert werden. In diesem Beispiel definieren wir eine globale Gruppe und die Arbeitsgruppe bleibt leer. Die Einstellungen dieser Gruppe gelten für alle Arbeitsgruppen, die keine speziellen Schedule-Gruppen haben.  
4. Wählen Sie eine Farbe aus der Farbauswahl aus.
    * Die Farben werden verwendet, um die Einzelvorgänge der Seite "Kanbanzeitplanlisten" auf der Kanbanprozesskarte hervorzuheben.  
5. Markieren Sie in der Liste die ausgewählte Zeile.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="associate-product"></a>Produkt zuordnen
1. Zuordnen eines bestimmtes Produkts
    * Es gibt zwei Möglichkeiten, um Produkte den Lean Schedule-Gruppe zuzuordnen. Entweder als bestimmtes Produkt (Artikelrelationstyp = Artikel) oder als Teil eines Artikelverteilungsschlüssels (Artikelrelationstyp = Gruppe).    
2. Wählen Sie im Feld "Artikelrelation" "Artikel" aus.
3. Geben Sie im Feld "Artikelnummer" einen Wert ein.
4. Geben Sie im Feld "Durchsatzverhältnis" eine Zahl ein.
    * Das standardmäßige Durchsatzverhältnis ist 1, was bedeutet, dass die zugehörigen Produkte exakt die Kapazität verbraucht werden, die in den Verarbeitungsaktivitäten der Produktionsflüsse angegeben ist. Ein Durchsatzverhältnis > 1 definiert einen höheren Ressourcenverbrauch, Durchsatzverhältnis > 1 definiert den geringeren Ressourcenverbrauch. Das Verhältnis wird in der Kostenberechnung und bei der Berechnung des Kanban-Einzelvorgangsverbrauchs verwendet.  

## <a name="associate-item-allocation-key"></a>Zuordnen eines Artikelverteilungsschlüssels
1. Zuordnen eines Artikelverteilungsschlüssels
    * Fügen Sie einem Artikelverteilungsschlüssel eine Zuordnung hinzu, indem Sie die Artikelrelationstyp "Gruppe" verwenden.   Beachten Sie das Sie für diesen Prozess einen Planungsartikelzuordnungsschlüssel in Ihren Daten benötigen.  
2. Wählen Sie im Feld "Artikelrelation" "Gruppe" aus.
3. Klicken Sie im Feld "Artikelzuteilungsschlüssel" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]