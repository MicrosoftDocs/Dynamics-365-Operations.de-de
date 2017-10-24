--- 
title: "Richtlinien für Beschaffungskategoriehierarchien einrichten"
description: Verwenden Sie dieses Verfahren, um Regeln zum Bestellen von Produkten in einer Kategorie einzurichten.
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 50764f99be04d27e04047824f870e724336cb452
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Richtlinien für Beschaffungskategoriehierarchien einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Verwenden Sie dieses Verfahren, um Regeln zum Bestellen von Produkten in einer Kategorie einzurichten. Die Regeln werden für eine bestimmte Einkaufsrichtlinie definiert. Die Kategoriezugriffsregel steuert, auf welche Beschaffungskategorien Mitarbeiter Zugriff haben, wenn sie eine Anforderung erstellen. Wenn eine Anforderung erstellt wird, werden die Einkaufsrichtlinie und Kategoriezugriffsregel, die angewendet werden sollten, durch die juristische Person und die Organisationseinheit bestimmt, der der Mitarbeiter angehört. Sie können diese Prozedur im Demodatunternehmen USMF verwenden. In der Regel wird diese Aufgabe von einem Einkaufsleiter ausgeführt.


## <a name="find-the-procurement-policy"></a>Die Beschaffungsrichtlinie suchen
1. Wechseln Sie zu Beschaffung > Einstellungen > Richtlinien > Beschaffungsrichtlinien.
2. Klicken Sie auf den Link auf der USMF-Richtlinie "Beschaffungsrichtlinie".
    * Dies ist die Richtlinie, zu der Sie eine Regel hinzufügen werden. Es muss eine aktive Richtlinie sein.  

## <a name="create-a-category-access-rule"></a>Erstellen einer Kategoriezugriffsregel
1. Wählen Sie die Kategoriezugriffs-Richtlinienregel aus.
    * Wenn die Schaltfläche "Richtlinienregel erstellen" ausgegraut ist, liegt das daran, dass bereits eine aktive Richtlinienregel für den Kategoriezugriff vorhanden ist. Überprüfen Sie die Felder "Gültigkeit" und "Ablaufdatum", um zu bestimmen, welches es ist und wählen Sie es dann aus und klicken Sie auf "Richtlinienregel außer Kraft setzen". Wenn die Schaltfläche "Richtlinienregel erstellen" verfügbar ist, müssen Sie nichts unternehmen.  
2. Klicken Sie auf "Richtlinienregel erstellen".
3. Geben Sie im Feld "Gültigkeitsdatum" ein Datum und eine Uhrzeit ein.
    * Die Zeit darf sich nicht mit einer anderen Regel überschneiden, die bereits aktiv ist.  
    * Wählen Sie eine Kategorie aus, für die die Regel gilt. Notieren Sie sich, welche Kategorie das ist – Sie benötigen sie später. Wenn Sie eine Kategorie auswählen, werden ihre übergeordnete(n) Kategorie(n) ebenfalls der Liste "Ausgewählte Kategorien" hinzugefügt.  
    * Wenn Sie möchten, dass die Regel für alle Unterkategorien der ausgewählten Kategorie gilt, aktivieren Sie das Kontrollkästchen "Unterkategorien einschließen".  
4. Klicken Sie auf Hinzufügen.
    * Wenn Sie die Option "Übergeordnete Regel einschließen" auf "Ja" festlegen, wird die Richtlinienregel, die Sie für eine übergeordnete Kategorie definieren, ebenfalls deren untergeordneten Kategorien zugewiesen, wenn für die untergeordneten Kategorien keine Richtlinienregel definiert wurde.  
5. Klicken Sie auf "OK".

## <a name="create-a-category-policy-rule"></a>Erstellen einer Kategorierichtlinienregel
1. Die Kategorierichtlinienregel auswählen
    * Wenn die Schaltfläche "Richtlinienregel erstellen" ausgegraut ist, wählen Sie die aktive Richtlinienregel aus und klicken Sie dann auf "Richtlinienregel außer Kraft setzen".  
2. Klicken Sie auf "Richtlinienregel erstellen".
3. Geben Sie im Feld "Gültigkeitsdatum" ein Datum und eine Uhrzeit ein.
4. Klicken Sie auf Hinzufügen.
5. Wählen Sie dieselbe Kategorie aus, die Sie für die "Kategoriezugriffsregel" verwendeten.
6. Wählen Sie im Feld "Kreditorenauswahl" eine Option aus.
    * Wählen Sie eine Regel aus, um zu steuern, welche Art von Kreditoren für die Kategorie ausgewählt werden können, wenn Anforderungen erstellt werden.  
7. Klicken Sie auf "Schließen".
    * Die Richtlinienregeln, die Sie definiert haben, sind für die Anforderungen des Typs "Verbrauch" gewesen. Sollten Sie Richtlinien für Anforderungen des Typs "Wiederbeschaffung" definieren wollen, würden Sie eine Regel für den Richtlinienregeltyp mit der Bezeichnung "Wiederbeschaffungskategorie-Zugriffsrichtlinienregel" erstellen.  


