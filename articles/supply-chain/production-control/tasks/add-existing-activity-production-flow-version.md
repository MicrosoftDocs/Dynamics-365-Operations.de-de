---
title: Eine vorhandene Aktivität zu einer Produktionsflussversion hinzufügen
description: Wenn Sie neue Versionen von Produktionsflüssen erstellen, können Sie Aktivitäten hinzuzufügen, die für die Vorgängerversionen der neuen Version erstellt werden.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8dc890462ac44f0471882e65b928563415aceaea
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212433"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>Eine vorhandene Aktivität zu einer Produktionsflussversion hinzufügen

[!include [banner](../../includes/banner.md)]

Wenn Sie neue Versionen von Produktionsflüssen erstellen, können Sie Aktivitäten hinzuzufügen, die für die Vorgängerversionen der neuen Version erstellt werden. Dieses Verfahren zeigt, wie Sie eine neue Version für einen vorhandenen Produktionsfluss erstellen, ohne die Aktivitäten zu kopieren. Im nächsten Schritt wird einer vorhandenen Aktivität der neuen Version hinzugefügt. 

Diese Aufgabe erfordert einen Produktionsfluss mit der Version und Aktivitäten, die bereits erstellt werden.


## <a name="create-a-new-production-flow-version"></a>Neue Produktionsflussversion erstellen
1. Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie auf Bearbeiten.
5. Markieren Sie in der Liste die ausgewählte Zeile.
6. Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.
    * Prüfen Sie das Ablaufdatum und der Ablaufuhrzeit der aktiven Version bevor Sie eine neue Produktionsflussversion erstellen. Die neue Version wird mit einem effektiven Startdatum erstellt, das zum Ablaufdatum der ausgewählten Version passt.  
7. Klicken Sie auf Hinzufügen.
8. Wählen Sie "Nein" im Feld "Von Version kopieren" aus.
    * Wählen Sie auf "Nein" aus, um ohne Version zu starten, wenn die Mehrheit der Aktivitäten die kopierte Version nach neue Aktivitäten ersetzt werden. Fügen Sie den unveränderten Aktivitäten zur "Vorhandenes Element hinzufügen"-Funktion im Aktivitätsformular manuell hinzu.  
9. Wählen Sie "Nein" im Feld "Kanban-Regeln duplizieren" aus.
    * Werden die Aktivitäten nicht in die neue Version kopiert werden, ist es nicht möglich Kanban-Regeln zum Zeitpunkt der Erstellung der neuen Version zu kopieren.   Verwenden Sie stattdessen die "Kanban-Ersetzung"-Funktion später im Kanban-Regel-Formular, um die Kanban-Regeln der alten Produktionsflussversion durch Kanban-Regeln mit der Aktivitäten der neuen Version zu ersetzen.  
10. Klicken Sie auf "OK".
11. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.

## <a name="add-an-existing-activity"></a>Vorhandene Aktivität hinzufügen
1. Klicken Sie auf "Aktivitäten".
2. Klicken Sie auf "Vorhandenes Element hinzufügen", um das Ablagedialogfeld zu öffnen.
    * Suchen Sie eine bestehende Aktivität aus, die der neuen Produktionsflussversion hinzugefügt werden soll und wählen Sie sie aus.  Beachten Sie, dass die Liste alle Aktivitäten anzeigt, die für den Produktionsfluss für alle vorherigen Versionen Datenfluss erstellt wurden.  
3. Geben Sie im Feld 'Aktivität' einen Wert ein, oder wählen Sie einen Wert aus.
4. Klicken Sie auf "OK".

