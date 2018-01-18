--- 
title: Produktkonfigurationsmodell erstellen
description: Im folgenden Verfahren wird gezeigt, wie ein Produktkonfigurationsmodell erstellt wird und grundlegende Informationen wie Attribute und Unterkomponenten eingegeben werden.
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: d494a20ba6f1f9c33a3935779b4bd3a8eefce26a
ms.contentlocale: de-de
ms.lasthandoff: 11/14/2017

---
# <a name="create-a-product-configuration-model"></a>Produktkonfigurationsmodell erstellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Im folgenden Verfahren wird gezeigt, wie ein Produktkonfigurationsmodell erstellt wird und grundlegende Informationen wie Attribute und Unterkomponenten eingegeben werden. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-a-product-model"></a>Erstellen eines Produktmodells
1. Klicken Sie auf "Produktvariantenmodell-Definition".
2. Klicken Sie auf "Produktkonfigurationsmodelle".
3. Klicken Sie auf Neu.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Geben Sie im Feld "Beschreibung" einen Wert ein.
6. Wählen Sie im Feld "Solver-Strategie" eine Option aus.
    * Die Solver-Strategie bestimmt, wie die Einschränkungen in einem einschränkungsbasierten Produktkonfigurationsmodell verarbeitet werden. Diese Auswahl kann Auswirkungen auf die Leistung des Produktkonfigurationsmodells haben.  
7. Geben Sie im Feld "Name" einen Wert ein.
    * Die Stammkomponente stellt das Produktkonfigurationsmodell dar, kann jedoch auch in anderen Produktmodellen verwendet werden.  
8. Klicken Sie auf "OK".
9. Wählen Sie im Feld "Konfigurationen wiederverwenden" eine Option aus.
    * Wenn der Parameter "Konfigurationen wiederverwenden" auf "Ja" festgelegt wird, prüft das System nach jeder Konfigurationssitzung auf identische Konfigurationen und verwendet sie erneut , wenn eine komplette Übereinstimmung gefunden wird.  

## <a name="add-attributes"></a>Attribute hinzufügen
1. Erweitern Sie den Abschnitt "Attribute".
2. Klicken Sie auf Hinzufügen.
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Geben Sie im Feld "Solver-Name" einen Wert ein.
    * Der Solver-Name wird vom Einschränkungswandler des Variantenkonfigurators verwendet. Er darf keine Leerzeichen oder Sonderzeichen mit Ausnahme von _ (Unterstrich) enthalten.  
6. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Der Beschreibungstext wird dem Konfigurationsbenutzer angezeigt und kann somit als Hilfe im Auswählen des richtigen Attributwerts dienen.  
7. Geben Sie im Feld "Attribut" einen Wert ein, oder wählen Sie einen Wert aus.
    * Der Attributtyp bestimmt, welche Werte für das Attribut verfügbar sind.  
8. Wählen Sie das Kontrollkästchen "In Wiederverwendung einbeziehen".
    * Diese Option ist nur verfügbar, wenn die Option "Konfigurationen wiederverwenden" ausgewählt wurde. Wenn Sie die Attribute für das Kontrollkästchen "In Wiederverwendung einbeziehen" aktivieren, wird dieses Attribut berücksichtigt, wenn das System nach einer kompletten Übereinstimmung sucht.  

## <a name="add-subcomponents"></a>Unterkomponenten hinzufügen
1. Erweitern Sie den Abschnitt "Unterkomponenten".
2. Klicken Sie auf Hinzufügen.
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Geben Sie im Feld "Solver-Name" einen Wert ein.
6. Geben Sie im Feld "Beschreibung" einen Wert ein.
7. Geben Sie im Feld ''Komponente" einen Wert ein, oder wählen Sie einen Wert aus.
    * Jede Unterkomponente muss auf eine Komponentendefinition verweisen. Dieser Entwurf unterstützt wiederverwendbare Komponenten und stellt sicher, dass eine Komponente, nachdem sie einmal definiert wurde, in vielen Produktmodellen verwendet werden kann.  
8. Klicken Sie auf "Speichern".
9. Klicken Sie auf "Stücklistenpositionsdetails".
    * Das Formular "Stücklistenpositionsdetail"ermöglicht dem Benutzer, die erforderlichen Eigenschaften für die Unterkomponente auszuwählen. Jeder Eigenschaft kann ein fester Wert oder ein Attribute zugewiesen werden. Die Zuordnung zu einem Attribut führt dazu, dass der Stücklistenabrechnungscode, verschiedene Werte abhängig von der Konfigurationsauswahl abruft.  
10. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
    * Jede Unterkomponente stellt einen konfigurierbaren Produktmaster mit einschränkungsbasierten Konfigurationtechnologie dar. Die Referenz wird durch die Artikelnummer vorgenommen.  
11. Wählen Sie das Kontrollkästchen "Festlegen" aus.
12. Wählen Sie "Ja" im Feld "Berechnung" aus.
    * Das Festlegen der Berechnungsoption stellt sicher, dass das Produkt enthalten ist, wenn eine Kostenberechnung für das Produkt ausgeführt wird.  
13. Klicken Sie auf die Registerkarte "Einstellungen".
14. Wählen Sie das Kontrollkästchen "Festlegen" aus.
15. Geben Sie im Feld "Menge" eine Zahl ein.
    * Das Feld "Menge" bestimmt, wie viel von diesem Produkt im konfigurierten Produkt verbraucht wird.  
16. Wählen Sie das Kontrollkästchen "Festlegen" aus.
17. Geben Sie im Feld "Pro Serie" eine Zahl ein.
18. Klicken Sie auf "OK".


