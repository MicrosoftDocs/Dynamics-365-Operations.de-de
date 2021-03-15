---
title: Eine Kostenaufschlüsselungsrichtlinie erstellen
description: Dieses Verfahren zeigt, wie eine Rollup-Kostenrichtlinie und Regeln für die Richtlinie erstellt werden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0a648984a8b4aaa314707e72a615f516116a193
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990741"
---
# <a name="create-a-cost-rollup-policy"></a>Eine Kostenaufschlüsselungsrichtlinie erstellen

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]