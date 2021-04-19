---
title: Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen
description: Kostenaufteilungsregeln werden verwendet, um Kosten zu verteilen, die wertmäßig für eine Kollektivkostenstelle gezählt wurden.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 736b537958f65fb54d0829cfbcc819fd315b530c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810125"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Eine Kostenverteilungsrichtlinie für eine Kostenkontrollsteuereinheit erstellen und zuweisen

[!include [banner](../../includes/banner.md)]

Kostenaufteilungsregeln werden verwendet, um Kosten zu verteilen, die wertmäßig für eine Kollektivkostenstelle gezählt wurden. Der Kosten-Buchhalter stird sichergestellt, dass die Kosten den Kostenstellen verteilt sind, auf Grundlage der ausgewählten Verrechnungsgrundlage. Eine Richtlinie und die entsprechenden Regeln werden einer Kostenkontrollsteuereinheit zugewiesen. Dieser Aufgabenleitfaden verwendet ein Beispiel, um anzuzeigen, wie eine Kostenaufteilungsrichtlinie und die entsprechenden Regeln erstellt werden.


## <a name="create-a-policy"></a>Eine Richtlinie erstellen
1. Wechseln Sie zu Kostenbuchhaltung > Richtlinien > Kostenverteilungsrichtlinien.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Richtliniennamen" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.
    * Organisation auswählen  
6. Geben Sie im Feld "Kostenelementdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie CDS P/L aus.  
7. Geben Sie im Feld "Statistische Dimension" einen Wert ein, oder wählen Sie einen Wert aus.
    * Statistische Elemente auswählen.  
8. Klicken Sie auf "Speichern".

## <a name="create-rules-for-the-policy"></a>Erstellen von Richtlinienregeln
1. Klicken Sie auf "Neu".
2. Markieren Sie in der Liste die ausgewählte Zeile.
3. Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.
    * Gesamte Hierarchie erweitern, um 094 auszuwählen.  
4. Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie weitere Betriebskosten und wählen Sie dann 605110 Reinigung.  
5. Wählen Sie im Feld Kostenverhalten eine Option aus.
    * Wählen Sie Fixkosten.  
6. Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.
7. Klicken Sie auf "Neu".
8. Markieren Sie in der Liste die ausgewählte Zeile.
9. Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.
    * Gesamte Hierarchie erweitern, um 094 auszuwählen.  
10. Geben Sie im Feld "Kostenelementdimensionshierarchie-Knoten" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie weitere Betriebskosten und wählen Sie dann 605150 Miete.  
11. Wählen Sie im Feld Kostenverhalten eine Option aus.
    * Wählen Sie Fixkosten.  
12. Geben Sie im Feld ''Zuteilungsbasis" einen Wert ein, oder wählen Sie einen Wert aus.
13. Klicken Sie auf "Speichern".

## <a name="assign-rules-to-a-cost-control-unit"></a>Weisen Sie einer Kostenkontrollesteuereinheit Regeln zu
1. Richtlinienzuweisungen für Kostensteuerungseinheit.
2. Klicken Sie auf "Neu".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie ein Datum in das Feld "Gültig ab Datum" ein.
    * Wählen Sie 1. September im gültigen Geschäftsjahr aus.  
5. Geben Sie im Feld "Kostenkontrolleinheit" einen Wert ein oder wählen Sie einen Wert aus.
6. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]