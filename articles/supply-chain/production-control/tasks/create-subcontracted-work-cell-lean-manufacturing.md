---
title: Eine Fremdarbeitszelle für Lean Manufacturing erstellen
description: Um Arbeit für Lean Manufacturing zu modellieren, müssen Sie eine Fertigungszelle erstellen, die dem Kreditor zugeordnet ist, der die Arbeit bereitstellt.
author: cvocph
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86838eb81f42b0f930f3989f7edfa5ee724bd05e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006890"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a>Eine Fremdarbeitszelle für Lean Manufacturing erstellen

[!include [banner](../../includes/banner.md)]

Um Arbeit für Lean Manufacturing zu modellieren, müssen Sie eine Fertigungszelle erstellen, die dem Kreditor zugeordnet ist, der die Arbeit bereitstellt. Eine Fertigungszelle wird an den Kreditor über die Zuordnung eine Ressource vom Kreditorentyps verknüpft. Wenn Sie dieser Buchung im USMF-Vorführungsunternehmen wiedergeben, können Sie Kreditorenkontokennung 1002 und 1. Standort auswählen.


## <a name="create-a-vendor-resource"></a>Erstellen einer Ressourcengruppe
1. Wechseln Sie zu "Ressourcen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Ressource" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie im Feld Kreditor den Typ aus.
6. Klicken Sie im Feld "Händler" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.

## <a name="create-the-resource-group"></a>Ressourcengruppe erstellen
1. Wechseln Sie zu "Ressourcengruppen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Ressourcengruppe" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie den Standort aus, dem die Fertigungszelle zugeordnet werden soll. In der Theorie kann ein Standort einen einzelnen Standort darstellen, der von einem Kreditor bearbeitet wird. Allerdings werden in den meisten Fällen Ressourcen aktuell dem Standort zugeordnet, der die Aufträge in  Fremdarbeit ausführt. Beachten Sie, dass die von Eingangs- und Ausgangslagerorte geregelten Fertigungszellen demselben Standort entsprechen müssen.  
6. Geben Sie im Feld "Standort" einen Wert ein.
7. @SysTaskRecorder:_RequestClose
8. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen Arbeitsgruppe.
9. Klicken Sie im Feld "Eingangslagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie den Lagerort und Lagerplatz aus, die das Material für die Kreditor-verwaltete Arbeitsgruppe verwendet werden. In vielen Fällen werden der Lagerort und der Lagerplatz modelliert, indem Sie einen separaten Lagerort pro Lieferant und pro Fertigungszelle für einen Lagerplatz verwenden.  
10. Klicken Sie im Feld "Lagerplatz für Wareneingang" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Klicken Sie im Feld "Ausgangslagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Definieren Sie den Lagerort und Lagerplatz, an dem das Material gebucht wird, wenn die von gesetzlichen Bestimmungen unterliegenden Aktivitäten der Fertigungszelle gebucht werden. Der Lagerort und der Ort können am Kreditorenstandort sein, wenn der Kreditor an die Kanban-Einzelvorgänge berichtet. Alternativ kann der Lagerort und der Lagerplatz der empfangende Speicherort sein, der mit dem nächsten Schritt des Produktionsflusses verknüpft ist.  
12. Klicken Sie im Feld "Lagerplatz für Warenausgang" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
13. Erweitern oder reduzieren Sie den Abschnitt "Kalender".
14. Klicken Sie auf Hinzufügen.
15. Klicken Sie im Feld "Kalender" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie den Kalender aus, der die Arbeitszeit der angegebenen Arbeitsgruppe darstellt. Für wichtige Ressourcen empfehlen wir jedoch, die bestimmten Kalender zu definieren, die die Ausführung für die  Arbeitszeiten und die zugehörigen Fertigungszelle- oder Kapazitäten des Kreditorenstandorts darstellen.  
16. Erweitern oder reduzieren Sie den Abschnitt Ressourcen.
17. Klicken Sie auf Hinzufügen.
    * Eine Ressourcengruppe muss eine zugehörige Ressource des Kreditorentyps haben, der die Ressourcengruppe auf dem Kreditorenkonto zugeordnet hat.  
18. Klicken Sie im Feld Ressourcen auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie die Kreditorenressource aus, die Sie in der vorherigen Unteraufgabe erstellt haben.  
19. Erweitern oder reduzieren Sie den Abschnitt "Arbeisgruppenkapazität".
20. Klicken Sie auf Hinzufügen.
    * Eine Fertigungszelle muss eine festgelegte Kapazität verfügen. In diesem Beispiel erstellen wir eine Durchsatzkapazität von 100 Stück pro Standardarbeitstag.  
21. Klicken Sie im Feld "Produktionsflussmodell" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
22. Wählen Sie im Feld "Kapazitätsperiode" eine Option aus.
23. Geben Sie im Feld "Durchschnittliche Durchsatzmenge" eine Zahl ein.
24. Klicken Sie im Feld "Einheit" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
25. "Auflösen" verändert die Einheit.

