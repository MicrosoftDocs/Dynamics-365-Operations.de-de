---
title: Kanban-Mengen-Berechnungsrichtlinie zu einer Kanban-Regel hinzufügen
description: Der Schwerpunkt dieser Prozedur liegt auf dem Erstellen einer Richtlinie zur Kanban-Mengenberechnung und dem Hinzufügen dieser zu einer Kanban-Regel, mit der die Kanban-Größe und -menge optimiert wird.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93f0c2024e7fbe7d9c6525d41207b788032e763a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147203"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Kanban-Mengen-Berechnungsrichtlinie zu einer Kanban-Regel hinzufügen

[!include [banner](../../includes/banner.md)]

Der Schwerpunkt dieser Prozedur liegt auf dem Erstellen einer Richtlinie zur Kanban-Mengenberechnung und dem Hinzufügen dieser zu einer Kanban-Regel, mit der die Kanban-Größe und -menge optimiert wird. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Vorgehensweise ist für den Wertstrommanager vorgesehen. Dieses Verfahren wird für die Erstellung des Verfahrens "Kanban-Mengenvorschläge berechnen" vorausgesetzt. 


## <a name="create-a-kanban-quantity-calculation-policy"></a>Richtlinie zur Kanban-Mengenberechnung erstellen
1. Wechseln Sie zu "Produktionssteuerung" > "Periodische Aufgaben" > "Kanban-Mengenberechnung" > "Richtlinien zur Kanban-Mengenberechnung".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein.
    * Geben Sie beispielsweise "Speaker2016" ein.  
4. Klicken Sie im Feld "Produktprogrammplan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie "StaticPlan" aus, um Bedarf zu berechnen.  
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Klicken Sie auf "Speichern".
8. Geben Sie im Feld "Kanban-Mindestmenge" "1"ein.
    * Dies ist die zusätzliche Anzahl von Kanbans, die in die Kanban-Mengenberechnung einbezogen wird.  
9. Legen Sie den Sicherheitsfaktor auf "1" fest.
    * Dies ist der Faktor, der zum Berechnen der zusätzlichen Menge des Sicherheitslagerbestands verwendet wird.  
10. Geben Sie im Feld "Tage voraus" den Wert "30" ein.
    * Dies ist die Anzahl der Tage vor dem Datum der Kanban-Mengenberechnung, für die der Bedarf in die Berechnung einbezogen wird.  
11. Geben Sie im Feld "Tage zurück" den Wert "30" ein.
    * Dies ist die Anzahl der Tage ab dem Datum der Kanban-Mengenberechnung, für die der Bedarf in die Berechnung einbezogen wird.  Die Formel, die für die Berechnung verwendet wird, wird mit den Istwerten angezeigt. Beispiel: Kanban-Menge = ((Durchschnittlicher Tagesbedarf x Durchlaufzeit x 2.00)/Produktmenge pro Handhabungseinheit) + 1  
12. Schließen Sie die Seite.

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Richtlinie zur Kanban-Mengenberechnung zu einer Kanban-Regel hinzufügen
1. Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie Kanban-Regel 000020 für diese Prozedur aus.  
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Schalten Sie die Erweiterung des Abschnitts "Richtlinien zur Kanban-Mengenberechnung" ein/aus.
5. Klicken Sie auf Hinzufügen.
    * Fügen Sie die Richtlinie zur Kanban-Mengenberechnung hinzu, die Sie in der vorherigen Unteraufgabe erstellt haben.  
6. Markieren Sie in der Liste die ausgewählte Zeile.
7. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie die Speaker2016-Richtlinie aus, die Sie in der vorherigen Unteraufgabe erstellt haben.  

