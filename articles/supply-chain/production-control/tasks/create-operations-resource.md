--- 
title: Erstellen einer betrieblichen Ressource
description: "Eine betriebliche Ressource führt die Aktivitäten eines Projekts oder eines Produktionsprozesses aus."
author: sorenva
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: aa80e4b22d116c8f580c9aefe7c114cfe1d19cc8
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---
# <a name="create-an-operations-resource"></a>Erstellen einer betrieblichen Ressource

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Eine betriebliche Ressource führt die Aktivitäten eines Projekts oder eines Produktionsprozesses aus. Diese Prozedur zeigt Ihnen an, wie eine betriebliche Ressource definiert wird. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.

1. Wechseln Sie zu "Ressourcen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Ressource" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.

## <a name="define-capacity-and-consumption-parameters"></a>Kapazitäts- und Verbrauchsparameter definieren
1. Erweitern Sie den Abschnitt "Arbeitstang".
2. Geben Sie im Feld "Ausschuss" eine Zahl ein.
3. Geben Sie im Feld "Rüstkostenkategorie" einen Wert ein oder wählen Sie einen Wert aus.
    * Geben Sie die Kostenkategorie an, die definiert, wie die Kosten der Einstellung berücksichtigt werden sollen.  
4. Geben Sie im Feld "Ausführungszeitkategorie" einen Wert ein oder wählen Sie einen Wert aus.
    * Geben Sie die Kostenkategorie an, die definiert, wie die Kosten der Laufzeit berücksichtigt werden sollen.  
5. Geben Sie im Feld "Stückkostenkategorie" einen Wert ein oder wählen Sie einen Wert aus.
    * Geben Sie die Kostenkategorie an, die definiert, wie die Ressourcenkosten, basierend auf der Ausgabemenge, berücksichtigt werden sollen.  
6. Wählen Sie im Feld "Kapazitätseinheit" eine Option aus.
    * Geben Sie die Einheit an, in der die Kapazität der betrieblichen Ressource ausgedrückt wird.  
7. Geben Sie im Feld "Kapazität" eine Zahl ein.
8. Geben Sie im Feld "Effizienzgrad" eine Zahl ein.
    * Geben Sie die Effizienz an, die Sie von der betrieblichen Ressource erwarten. Mit dem Effizienzgrad wird der Durchsatz einer betrieblichen Ressource angepasst und er wirkt sich somit auch auf die für die Ressource reservierte Zeit aus.  
9. Geben Sie im Feld "Grobterminierungsprozentsatz" eine Zahl ein.
    * Geben Sie den maximalen Prozentsatz der Kapazität der betrieblichen Ressource an, die sie für die Grobterminierung verwendet möchten.  
10. Wählen Sie "Ja" im Feld "Begrenzte Kapazität" aus.
    * Legen Sie diese Option auf "Ja" fest, wenn die betriebliche Ressource auf Basis der tatsächlichen Kapazität, die verfügbar ist, geplant werden soll, und wenn vorhandene Kapazitätsreservierungen berücksichtigt werden sollen. Wenn die Option auf "Nein" festgelegt ist, wird angenommen, dass die betriebliche Ressource unbegrenzte Kapazität hat, und die Ressource kann möglicherweise überbucht werden.  
11. Wählen Sie "Ja" im Feld "Engpassressource" aus.

## <a name="define-working-times"></a>Arbeitszeiten definieren
1. Erweitern Sie den Abschnitt "Kalender".
2. Klicken Sie auf Hinzufügen.
3. Geben Sie im Feld "Kalender" einen Wert ein oder wählen Sie einen Wert aus.
    * Geben Sie den Arbeitszeitkalender an, der die Kapazität (in Stunden) der Ressource definiert.  
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="define-resource-capabilities"></a>Ressourcenfähigkeiten definieren
1. Erweitern Sie den Abschnitt "Funktionen".
2. Klicken Sie auf Hinzufügen.
    * Eine Funktion ist die Fähigkeit einer betrieblichen Ressource, eine bestimmte Aktivität auszuführen. Das Planungsmodul weist Ressourcen zu, indem die Ressourcenanforderungen jeder Aktivität mit den Funktionen der verfügbaren betrieblichen Ressourcen abgeglichen werden.  
3. Geben Sie im Feld "Funktion" einen Wert ein, oder wählen Sie einen Wert aus.
4. Geben Sie im Feld "Ebene" eine Zahl ein.
    * Geben Sie den Grad der Effizienz an, mit der die Ressource die Funktion verarbeitet.  
5. Geben Sie im Feld "Priorität" eine Zahl ein.
    * Geben Sie die Priorität der betrieblichen Ressource hinsichtlich der Funktion an. Bei der Planung nach Priorität, wird die betriebliche Ressource mit der höchsten Priorität (also mit dem niedrigsten numerischen Wert) zuerst ausgewählt.  

## <a name="assign-resource-to-resource-group"></a>Einer Ressourcengruppe eine Ressource zuweisen
1. Erweitern Sie den Abschnitt "Ressourcengruppen".
2. Klicken Sie auf Hinzufügen.
    * Die Ressourcengruppe definiert den Standort-, Produktionseinheits- und Lagerortkontext für betriebliche Ressourcen. Die betriebliche Ressource kann nur eingeplant werden, wenn sie einer Ressourcengruppe zugewiesen ist, und zwar nur an dem Standort, an dem sich die Ressourcengruppe befinden.  
3. Geben Sie im Feld "Ressourcengruppe" einen Wert ein oder wählen Sie einen Wert aus.
4. Geben Sie im Feld "Lagerplatz für Wareneingang" einen Wert ein, oder wählen Sie einen Wert aus.
    * Geben Sie den Lagerort an, von dem aus die betriebliche Ressource Material verbraucht.  


