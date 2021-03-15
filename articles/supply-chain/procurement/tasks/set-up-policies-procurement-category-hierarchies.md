---
title: Richtlinien für Beschaffungskategoriehierarchien einrichten
description: Verwenden Sie dieses Verfahren, um Regeln zum Bestellen von Produkten in einer Kategorie einzurichten.
author: RichardLuan
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fc01793ee83444e5c7097021c19aeda80a132e6
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017092"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Richtlinien für Beschaffungskategoriehierarchien einrichten

[!include [banner](../../includes/banner.md)]

Verwenden Sie dieses Verfahren, um Regeln zum Bestellen von Produkten in einer Kategorie einzurichten. Die Regeln werden für eine bestimmte Einkaufsrichtlinie definiert. Die Kategoriezugriffsregel steuert, auf welche Beschaffungskategorien Mitarbeiter Zugriff haben, wenn sie eine Anforderung erstellen. Wenn eine Anforderung erstellt wird, werden die Einkaufsrichtlinie und Kategoriezugriffsregel, die angewendet werden sollten, durch die juristische Person und die Organisationseinheit bestimmt, der der Mitarbeiter angehört. Sie können diese Prozedur im Demodatunternehmen USMF verwenden. In der Regel wird diese Aufgabe von einem Einkaufsleiter ausgeführt.


## <a name="find-the-procurement-policy"></a>Die Beschaffungsrichtlinie suchen
1. Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Einstellungen > Richtlinien > Einkaufsrichtlinien**.
2. Klicken Sie auf den Link der Richtlinie „Beschaffungsrichtlinie USMF“. Dies ist die Richtlinie, zu der Sie eine Regel hinzufügen werden. Es muss eine aktive Richtlinie sein.  

## <a name="create-a-category-access-rule"></a>Erstellen einer Kategoriezugriffsregel
1. Erweitern Sie das Inforegister **Richtlinienregeln**.
2. Wählen Sie in der Liste **Richtlinienregeltyp** die Option **Richtlinienregel für Kategoriezugriff** aus. Wenn die Schaltfläche **Richtlinienregel erstellen** abgeblendet ist, liegt das daran, dass bereits eine aktive Richtlinienregel für den Kategoriezugriff vorhanden ist. Überprüfen Sie die Felder **Gültig** und **Ablauf**, um zu bestimmen, welches es ist; wählen Sie es dann aus, und klicken Sie auf **Richtlinienregel zurückziehen**. Wenn die Schaltfläche **Richtlinienregel erstellen** verfügbar ist, müssen Sie nichts unternehmen.  
3. Klicken Sie auf **Richtlinienregel erstellen**.
4. Geben Sie im Feld **Gültigkeitsdatum** ein Datum und eine Uhrzeit ein. Die Zeit darf sich nicht mit einer anderen Regel überschneiden, die bereits aktiv ist.  
5. Wählen Sie eine Kategorie aus, für die die Regel gilt. Notieren Sie sich, welche Kategorie das ist – Sie benötigen sie später. Wenn Sie eine Kategorie auswählen, werden ihre übergeordnete(n) Kategorie(n) ebenfalls der Liste "Ausgewählte Kategorien" hinzugefügt. Wenn Sie möchten, dass die Regel für alle Unterkategorien der ausgewählten Kategorie gilt, aktivieren Sie das Kontrollkästchen **Unterkategorien einbeziehen**.
6. Klicken Sie auf den Nach-rechts-Pfeil, einen Eintrag der Liste **Ausgewählte Kategorien** hinzuzufügen.  
4. Klicken Sie auf **OK**. Wenn Sie die Option **Übergeordnete Regel einschließen** auf „Ja“ festlegen, wird die Richtlinienregel, die Sie für eine übergeordnete Kategorie definieren, ebenfalls deren untergeordneten Kategorien zugewiesen, wenn für die untergeordneten Kategorien keine Richtlinienregel definiert wurde.

## <a name="create-a-category-policy-rule"></a>Erstellen einer Kategorierichtlinienregel
1. Wählen Sie in der Liste **Richtlinienregeltyp** die Option **Kategorierichtlinienregel** aus. Wenn die Schaltfläche **Richtlinienregel erstellen** abgeblendet ist, wählen Sie die aktive Richtlinienregel aus, und klicken Sie dann auf **Richtlinienregel zurückziehen**.  
2. Klicken Sie auf **Richtlinienregel erstellen**.
3. Geben Sie im Feld **Gültigkeitsdatum** ein Datum und eine Uhrzeit ein.
4. Klicken Sie auf **Hinzufügen**.
5. Wählen Sie im Feld **Kategorie** dieselbe Kategorie aus, die Sie für die **Kategoriezugriffsregel** verwendet haben.
6. Wählen Sie im Feld **Kreditorenauswahl** eine Option aus. Wählen Sie eine Regel aus, um zu steuern, welche Art von Kreditoren für die Kategorie ausgewählt werden können, wenn Anforderungen erstellt werden.  
7. Klicken Sie auf **Schließen**. Die Richtlinienregeln, die Sie definiert haben, sind für die Anforderungen des Typs "Verbrauch" gewesen. Sollten Sie Richtlinien für Anforderungen des Typs „Wiederbeschaffung“ definieren wollen, würden Sie eine Regel für den Richtlinienregeltyp mit der Bezeichnung „Wiederbeschaffungskategorie-Zugriffsrichtlinienregel“ erstellen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]