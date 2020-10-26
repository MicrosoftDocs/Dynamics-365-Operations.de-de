---
title: Eine Kostenzuweisungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen
description: Gehen Sie folgendermaßen vor, um eine Kostenzuweisungsrichtlinie und die entsprechenden Regeln zu einer Kostenkontrollesteuereinheit zu erstellen und zuzuweisen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad95752ce40faaa84747dac9bfbf2887f7a5af42
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976210"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Eine Kostenzuweisungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen

[!include [banner](../../includes/banner.md)]

Gehen Sie folgendermaßen vor, um eine Kostenzuweisungsrichtlinie und die entsprechenden Regeln zu einer Kostenkontrollesteuereinheit zu erstellen und zuzuweisen. Für diese Aufzeichnung wird das Demo-Datenunternehmen USP2 verwendet.


## <a name="create-a-policy"></a>Eine Richtlinie erstellen
1. Wechseln Sie zu Kostenbuchhaltung > Richtlinien > Kostenverteilungsrichtlinien.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Richtliniennamen" einen Wert ein.
4. Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.
    * Organisation auswählen  
5. Geben Sie im Feld "Statistische Dimension" einen Wert ein, oder wählen Sie einen Wert aus.
6. Klicken Sie auf "Speichern".

## <a name="create-allocation-rules"></a>Zuordnungsregel erstellen
1. Klicken Sie auf "Neu".
2. Markieren Sie in der Liste die ausgewählte Zeile.
3. Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.
4. Im Feld Kostenverhalten wählen Sie Total aus.
5. Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.
6. Klicken Sie auf "Neu".
7. Markieren Sie in der Liste die ausgewählte Zeile.
8. Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.
9. Im Feld Kostenverhalten wählen Sie Total aus.
10. Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.
11. Klicken Sie auf "Neu".
12. Markieren Sie in der Liste die ausgewählte Zeile.
13. Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.
14. Im Feld Kostenverhalten wählen Sie Total aus.
15. Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.
    * Fahren Sie fort, bis Sie alle Regeln erstellt haben.  
16. Klicken Sie auf "Speichern".

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Die Richtlinie einer Kostensteuerungseinheit zuweisen
1. Richtlinienzuweisungen für Kostensteuerungseinheit.
2. Klicken Sie auf "Neu".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie ein Datum in das Feld "Gültig ab Datum" ein.
    * Die Regeln sind Gültigkeitsdaten. Ein Benutzer oder das System kann die Regeln ablaufen lassen, wenn eine neuere Version erstellt wird.  
5. Geben Sie im Feld "Kostenkontrolleinheit" einen Wert ein oder wählen Sie einen Wert aus.
6. Klicken Sie auf "Speichern".

