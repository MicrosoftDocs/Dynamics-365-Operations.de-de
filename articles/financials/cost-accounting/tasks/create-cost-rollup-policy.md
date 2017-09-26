--- 
title: "Eine Kostenaufschlüsselungsrichtlinie erstellen"
description: "Dieses Verfahren zeigt, wie eine Rollup-Kostenrichtlinie und Regeln für die Richtlinie erstellt werden."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 51fabc8fe17a45d104be5da806d7076bcf9c5dbb
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-cost-rollup-policy"></a>Eine Kostenaufschlüsselungsrichtlinie erstellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie eine Rollup-Kostenrichtlinie und Regeln für die Richtlinie erstellt werden. Die Demodaten, die verwendet werden, um diese Prozedur zu erstellen, sind USP2.


## <a name="create-a-policy"></a>Eine Richtlinie erstellen
1. Wechseln Sie zu Kostenbuchhaltung > Richtlinien > Kostenrollup-Richtlinien.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Richtliniennamen" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.
    * Kostenkategorie wählen  
6. Geben Sie im Feld "Kostenelementdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.
    * Kostenkategorie wählen  
7. Klicken Sie auf "Speichern".

## <a name="create-rules-for-the-cost-rollup-policy"></a>Erstellen von Kostenrollup-Richtlinien
1. Klicken Sie auf "Neu".
2. Markieren Sie in der Liste die ausgewählte Zeile.
3. Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie 007 aus.  
4. Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.
    * Kostenkategorie CE wählen  
5. Geben Sie im Feld „Sekundäres Kostenelement” einen Wert ein oder wählen Sie einen Wert aus.
    * In vorliegenden Beispiel ordnen Sie das sekundäre Element CC-007 der Kostenstelle zu.  
6. Klicken Sie auf "Neu".
7. Markieren Sie in der Liste die ausgewählte Zeile.
8. Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie 008 aus.  
9. Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.
    * Kostenkategorie CE wählen  
10. Geben Sie im Feld „Sekundäres Kostenelement” einen Wert ein oder wählen Sie einen Wert aus.
    * In vorliegenden Beispiel ordnen Sie das sekundäre Element CC-008 der Kostenstelle zu.  
11. Klicken Sie auf "Neu".
12. Markieren Sie in der Liste die ausgewählte Zeile.
13. Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie 009 aus.  
14. Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.
    * Kostenkategorie CE wählen  
15. Geben Sie im Feld „Sekundäres Kostenelement” einen Wert ein oder wählen Sie einen Wert aus.
    * In vorliegenden Beispiel ordnen Sie das sekundäre Element CC-009 der Kostenstelle zu.  
    * Fahren Sie fort, bis alle Kostenstellen den entsprechenden sekundären Kostenfaktoren zugeordnet sind.  
16. Klicken Sie auf "Speichern".


