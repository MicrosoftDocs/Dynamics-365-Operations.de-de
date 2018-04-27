--- 
title: "Übertragungsaktivitäten für Lean Manufacturing erstellen"
description: "Erstellen Sie eine Umlagerungsaktivität für Lean Manufacturing."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 010ac08fa96ead49b6ecbbe083e59fb96427e29e
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>Übertragungsaktivitäten für Lean Manufacturing erstellen

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Erstellen Sie eine Umlagerungsaktivität für Lean Manufacturing. 

Voraussetzungen: 

1. Ein Produktionsfluss und eine Version, die nicht aktiv ist, müssen erstellt werden.

2. "Von und Nach-Lagerort und Lagerplatz" muss erstellt werden. Optional sollte die Wiederbeschaffung oder die auffüllende Arbeitsgruppe erstellt werden.


## <a name="find-the-production-flow-version"></a>Produktionsflussversion suchen
1. Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Beachten Sie, dass der Produktionsfluss eine Version im Status "Entwurf" aufweisen muss.  
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="create-a-new-activity"></a>Neue Aktivität erstellen
1. Klicken Sie auf "Aktivitäten".
    * Stellen Sie sicher, dass der ausgewählte Produktionsfluss eine Version im Entwurf hat und wählen Sie diese Version aus.  
2. Klicken Sie auf "Neue Planaktivität erstellen".
3. Klicken Sie auf Weiter.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Wählen Sie im Feld "Aktivitätstyp" "Übertragen"aus.
6. Geben Sie im Feld "Verarbeitungsmenge" eine Zahl ein.
7. Klicken Sie auf Weiter.

## <a name="select-the-work-cells"></a>Arbeitsgruppen auswählen
1. Klicken Sie im Feld "Wiederbeschaffung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie eine Arbeitsgruppe, um den Ausgangslagerplatz der Arbeitsgruppe und das Formular "Lagerplatz" in der Umlagerungsaktivität zu nutzen. Das Gleiche kann mit der ergänzten Arbeitsgruppe erfolgen, um den Zielort der Umlagerungsaktivität festzulegen.  
2. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="define-the-inventory-updates"></a>Lageraktualisierungen definieren
1. Wählen Sie im Feld "Produkttyp" eine Option aus.
    * Beachten Sie, dass eine Umlagerung nicht den Typ des Produkts ändert. Sie können Fertigprodukte oder Halbfertigprodukte umlagern (Umlagerung zwischen zwei Aktivitäten eines Produktionsflusses und u. U. des Kanban-Flusses).     Wenn Sie Fertigprodukte übertragen, können Sie auswählen, ob die Entnahme oder das Empfangen zu einer Lagerbuchung führt.  

## <a name="define-the-transfer-locations"></a>Umlagerungsorte definieren
1. Klicken Sie auf Weiter.
2. Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie im Feld "Lagerplatz" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Im Feld "Verfrachtet von" wählen Sie "Versender" aus.
    * Folgende Optionen stehen zur Auswahl: Versender - die Organisation, die den Versandlagerort betreibt, Empfänger - die Organisation, die den empfangenden Lagerort betreibt, Spediteur - ein Drittanbieter. Wenn die Betreiber-Organisation ein Kreditor ist, benötigt die Umlagerungsaktivität eine Fremdarbeitsereinbarung.  
8. Klicken Sie auf Weiter.

## <a name="define-the-activity-times"></a>Aktivitätszeiten definieren
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Die Definition einer Laufzeit ist erforderlich. Die Ausführungszeit wird verwendet, um Kosten und die Durchlaufzeiten der Kanban-Einzelvorgänge zu berechnen. Ausführungszeiten werden nicht verwendet, um die Kapazitätsauslastung und den Verbrauch zu berechnen. Diese werden nach der Zykluszeit berechnet, abgeleitet aus der Produktionsflussversionsaufgabe.  
2. Geben Sie im Feld "Zeit" eine Zahl ein.
3. Geben Sie im Feld "Einheiten" einen Wert ein.
4. Wählen Sie die Zeiteinheit aus.
5. Geben Sie im Feld "Nach Menge" eine Zahl ein.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wartezeiten sind optional.  
7. Geben Sie im Feld "Zeit" eine Zahl ein.
8. Geben Sie im Feld "Einheiten" einen Wert ein.
9. Wählen Sie die Zeiteinheit aus.
10. Geben Sie im Feld "Nach Menge" eine Zahl ein.
11. Klicken Sie auf Weiter.
12. Klicken Sie auf Fertig stellen.
13. Schließen Sie die Seite.


