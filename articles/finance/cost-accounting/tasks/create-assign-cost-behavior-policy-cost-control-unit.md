---
title: Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen
description: Kostenverhalten ist die Klassifizierung von Kosten, entweder als fix oder als variabel.
author: twheeloc
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 653bfb69c4ca118c700755cb95a6b349d2c6bbad
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735141"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Eine Kostenverhaltensrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen

[!include [banner](../../includes/banner.md)]

Kostenverhalten ist die Klassifizierung von Kosten, entweder als fix oder als variabel. Eine Richtlinie und die entsprechenden Regeln müssen einer Kostenkontrollesteuereinheit zugewiesen werden, sodass die Richtlinie gültig wird. Gehen Sie folgendermaßen vor, um eine Kostenzuweisungsrichtlinie und die entsprechenden Regeln zu einer Kostenkontrollesteuereinheit zu erstellen und zuzuweisen.


## <a name="create-a-cost-behavior-hierarchy"></a>Erstellen Sie eine Kosten-Verhaltenshierarchie
1. Wechseln Sie zu **Kostenrechnung > Dimensionen > Dimensionshierarchien**.
2. Klicken Sie auf **Neu**.
3. Klicken Sie auf **Erstellen**.
4. Im Feld **Dimensionshierarchiename** geben Sie „Kostenverhaltenshierarchie“ ein.
5. Geben Sie im Feld **Dimension** einen Wert ein, oder wählen Sie einen Wert aus.
    * Kostenelement auswählen.  
6. Klicken Sie auf **Speichern**.
7. Klicken Sie auf **Hierarchie anzeigen**.
8. Klicken Sie auf **Neu**.
9. Geben Sie im Feld **Knotenname** einen Wert ein.
    * Fixkosten eingeben.  
10. Wählen Sie in der Strukturdarstellung "Kostenverhaltenshierarchie " aus.
11. Klicken Sie auf **Neu**.
12. Geben Sie im Feld **Knotenname** einen Wert ein.
    * Variable Kosten eingeben.  
13. Klicken Sie auf **Speichern**.
14. Wählen Sie in der Strukturdarstellung Kostenverhaltenshierarchie\Fixkosten aus.
15. Klicken Sie auf **Neu**.
16. Markieren Sie in der Liste die ausgewählte Zeile.
17. Geben Sie im Feld **Von Dimensionsmitglied** einen Wert ein oder wählen Sie einen Wert aus.
    * Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder sich nicht überschneiden.  
18. Geben Sie im Feld **Dimensionsmitglied** einen Wert ein, oder wählen Sie einen Wert aus.
    * Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder sich nicht überschneiden.  
19. Wählen Sie in der Strukturdarstellung Kostenverhaltenshierarchie\Variable Kosten aus.
20. Klicken Sie auf **Neu**.
21. Markieren Sie in der Liste die ausgewählte Zeile.
22. Geben Sie im Feld **Von Dimensionsmitglied** einen Wert ein oder wählen Sie einen Wert aus.
    * Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder sich nicht überschneiden.  
23. Geben Sie im Feld **Dimensionsmitglied** einen Wert ein, oder wählen Sie einen Wert aus.
    * Der Bereich von Dimensionsmitgliedern kann Lücken enthalten, jedoch können die Mitglieder sich nicht überschneiden.  
24. Klicken Sie auf **Speichern**.

## <a name="create-the-policy-and-rules"></a>Erstellen von Richtlinien und Regeln
1. Wechseln Sie zu **Kostenrechnung > Richtlinien > Kostenverhaltensrichtlinien**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Richtlinienname** einen Wert ein.
4. Geben Sie im Feld **Kostenelement-Dimensionshierarchie** einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie die Richtlinienhierarchie aus, die Sie soeben erstellt haben.  
5. Geben Sie im Feld **Kostenobjekt-Dimensionshierarchie** einen Wert ein oder wählen Sie einen Wert aus.
    * Organisation auswählen  
6. Klicken Sie auf **Speichern**.
7. Klicken Sie auf **Neu**.
8. Markieren Sie in der Liste die ausgewählte Zeile.
9. Geben Sie im Feld **Kostenelement-Dimensionshierarchieknoten** einen Wert ein oder wählen Sie einen Wert aus.
    * Gesamte Hierarchie erweitern, um variable Kosten auszuwählen.  
10. Geben Sie im Feld **Kostenobjekt-Dimensionshierarchieknoten** einen Wert ein oder wählen Sie einen Wert aus.
    * Standardmäßig ist der variable Prozentsatz 100 Prozent.  
11. Klicken Sie auf **Richtlinienzuweisungen für Kostenkontrolleinheit**.
12. Klicken Sie auf **Neu**.
13. Markieren Sie in der Liste die ausgewählte Zeile.
14. Geben Sie ein Datum in das Feld **Gültigkeit ab Abschlussstichtag** ein.
    * Die Regeln sind Datum-effektiv und eine Regel kann von einem Benutzer oder vom System gestrichcen werde, wenn eine neuere Version erstellt wird.  
15. Geben Sie im Feld **Kostenkontrolleinheit** einen Wert ein oder wählen Sie einen Wert aus.
16. Klicken Sie auf **Speichern**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
