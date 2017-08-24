--- 
title: "Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen"
description: Kostenverhalten ist die Klassifizierung von Kosten, entweder als fix oder als variabel.
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4190fde8c587475f34e5e3fdf6e2d32d59a26022
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kostenverhalten ist die Klassifizierung von Kosten, entweder als fix oder als variabel. Eine Richtlinie und die entsprechenden Regeln müssen einer Kostenkontrollesteuereinheit zugewiesen werden, sodass die Richtlinie gültig wird. Gehen Sie folgendermaßen vor, um eine Kostenzuweisungsrichtlinie und die entsprechenden Regeln zu einer Kostenkontrollesteuereinheit zu erstellen und zuzuweisen.


## <a name="create-a-cost-behavior-hierarchy"></a>Erstellen Sie eine Kosten-Verhaltenshierarchie
1. Wechseln Sie zu Kostenrechnung > Dimensionen > Dimensionshierarchien.
2. Klicken Sie auf "Neu".
3. Klicken Sie auf "Erstellen".
4. Im Dimensionshierarchienamengebiet geben Sie " Kostenverhaltenshierarchie "ein.
5. Geben Sie im Feld Dimension einen Wert ein, oder wählen Sie einen Wert aus.
    * Kostenelement auswählen.  
6. Klicken Sie auf "Speichern".
7. Klicken Sie auf "Hierarchie anzeigen".
8. Klicken Sie auf "Neu".
9. Geben Sie im Feld "Knotenname" einen Wert ein.
    * Fixkosten eingeben.  
10. Wählen Sie in der Strukturdarstellung "Kostenverhaltenshierarchie " aus.
11. Klicken Sie auf "Neu".
12. Geben Sie im Feld "Knotenname" einen Wert ein.
    * Variable Kosten eingeben.  
13. Klicken Sie auf "Speichern".
14. Wählen Sie in der Strukturdarstellung Kostenverhaltenshierarchie\Fixkosten aus.
15. Klicken Sie auf "Neu".
16. Markieren Sie in der Liste die ausgewählte Zeile.
17. Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.
    * Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.  
18. Geben Sie im Feld "Dimensionsmitglied" einen Wert ein, oder wählen Sie einen Wert aus.
    * Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.  
19. Wählen Sie in der Strukturdarstellung Kostenverhaltenshierarchie\Variable Kosten aus.
20. Klicken Sie auf "Neu".
21. Markieren Sie in der Liste die ausgewählte Zeile.
22. Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.
    * Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.  
23. Geben Sie im Feld "Dimensionsmitglied" einen Wert ein, oder wählen Sie einen Wert aus.
    * Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder nicht überschneiden.  
24. Klicken Sie auf "Speichern".

## <a name="create-the-policy-and-rules"></a>Erstellen von Richtlinien und Regeln
1. Wechseln Sie zu Kostenaufteilung > Richtlinien > Kostenverhaltensrichtlinien.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Richtliniennamen" einen Wert ein.
4. Geben Sie im Feld "Kostenelementdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie die Richtlinienhierarchie aus, die Sie soeben erstellt haben.  
5. Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.
    * Organisation auswählen  
6. Klicken Sie auf "Speichern".
7. Klicken Sie auf "Neu".
8. Markieren Sie in der Liste die ausgewählte Zeile.
9. Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.
    * Gesamte Hierarchie erweitern, um variable Kosten auszuwählen.  
10. Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.
    * Standardmäßig ist der variable Prozentsatz 100 Prozent.  
11. Richtlinienzuweisungen für Kostensteuerungseinheit.
12. Klicken Sie auf "Neu".
13. Markieren Sie in der Liste die ausgewählte Zeile.
14. Geben Sie ein Datum in das Feld "Gültig ab Datum" ein.
    * Die Regeln sind Datum-effektiv und eine Regel kann von einem Benutzer oder vom System gestrichcen werde, wenn eine neuere Version erstellt wird.  
15. Geben Sie im Feld "Kostenkontrolleinheit" einen Wert ein oder wählen Sie einen Wert aus.
16. Klicken Sie auf "Speichern".


