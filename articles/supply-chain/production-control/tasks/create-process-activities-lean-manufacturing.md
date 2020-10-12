---
title: Verarbeitungsaktivitäten für Lean Manufacturing erstellen
description: Erstellen Sie eine Prozessaktivität für Lean Manufacturing.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb8068012453fd4a8b06dea8cc8e5067d6968fe3
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826598"
---
# <a name="create-process-activities-for-lean-manufacturing"></a>Verarbeitungsaktivitäten für Lean Manufacturing erstellen

[!include [banner](../../includes/banner.md)]

Erstellen Sie eine Prozessaktivität für Lean Manufacturing. 

Voraussetzungen: 

1. Ein Produktionsfluss und eine Version, die nicht aktiv ist, müssen erstellt werden.

2. Eine Arbeitsgruppe muss erstellt werden.


## <a name="find-the-production-flow-version"></a>Produktionsflussversion suchen
1. Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="create-a-new-activity"></a>Neue Aktivität erstellen
1. Klicken Sie auf "Aktivitäten".
    * Stellen Sie sicher, dass der ausgewählte Produktionsfluss eine Version im Entwurf hat und wählen Sie diese Version aus.  
2. Klicken Sie auf "Neue Planaktivität erstellen".
3. Klicken Sie auf Weiter.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Geben Sie im Feld "Name" einen Wert ein.
    * Beachten Sie, dass der Name für einen angegebenen Produktionsfluss für alle Versionen eindeutig sein muss.  
6. Geben Sie im Feld "Verarbeitungsmenge" eine Zahl ein.
    * Beachten Sie, dass, egal welche Einzelvorgangsmenge verarbeitet wird, dies die Mindestmenge pro Einzelvorgang ist, um die Lohnkosten zu berechnen. Wenn Einzelvorgangsmengen von dieser Menge abweichen, wird eine Lohnkostenabweichung erstellt.  
7. Klicken Sie auf Weiter.

## <a name="select-the-work-cell"></a>Arbeitsgruppe auswählen.
1. Klicken Sie im Feld "Arbeitsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
2. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="define-the-inventory-updates"></a>Lageraktualisierungen definieren
1. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Zugang zum verfügbaren Lagerbestand aktualisieren".
    * Wenn "Aktualisierung am Lager = kein" ist, können Sie die Aktivität definieren, um ein Halbfertigprodukt anzunehmen (diese Aktivität erreicht nicht die nächste Stücklistenebene).    Sie können auch auswählen, ob Sie Halbfertigprodukte verbrauchen wollen.  

## <a name="define-the-picking-activities"></a>Entnahmeaktivitäten definieren
1. Klicken Sie auf Weiter.
2. Markieren Sie in der Liste die ausgewählte Zeile.
    * Eine standardmäßige Entnahmeaktivität wird für den Wareneingang der ausgewählten Arbeitsgruppe erstellt.  
3. Klicken Sie auf Hinzufügen.
    * Sie können zusätzliche Kommissionieraktivitäten für bestimmte Produkte, die nicht in der Arbeitsgruppeneingabeaktivität bereitgestellt werden, erstellen.  
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Geben Sie im Feld "Artikelnummer" einen Wert ein.
6. Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Mit dieser Definition werden alle Materialien, die in der Aktivität verbraucht werden, dem standardmäßigen Eingangslagerort und Lagerplatz entnommen, mit Ausnahme des Artikels, der nicht in der zweiten Entnahmeaktivität definiert ist. Dieser Artikel wird aus einem anderen Lagerort und Lagerplatz entnommen.  
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Ausschuss erfassen".
10. Klicken Sie auf Weiter.

## <a name="define-the-activity-times"></a>Aktivitätszeiten definieren
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Die Definition einer Laufzeit ist erforderlich. Die Laufzeit wird verwendet, um Kosten und die Durchsatzzeiten der Kanban-Einzelvorgänge zu berechnen. Ausführungszeiten werden nicht verwendet, um die Kapazitätsauslastung und Verbrauch zu berechnen. Diese werden nach der Zykluszeit berechnet, abgeleitet aus der Produktionsflussversionsaufgabe.  
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

