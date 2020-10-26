---
title: Aktivitätsrelation erstellen -  Nachfolger
description: Der Ablauf von Aktivitäten in einem Leanproduktionsfluss wird durch Aktivitätsrelationen dokumentiert.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91e1535ab6b53ad60394967d0377606a0cd27d01
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983445"
---
# <a name="create-activity-relation---successor"></a>Aktivitätsrelation erstellen -  Nachfolger

[!include [banner](../../includes/banner.md)]

Der Ablauf von Aktivitäten in einem Leanproduktionsfluss wird durch Aktivitätsrelationen dokumentiert. Diese Aufzeichnung zeigt, wie Sie eine Aktivitätsrelation erstellen.

Voraussetzungen:

- Ein Produktionsfluss und eine Version im Entwurfsmodus. 

- Zwei Aktivitäten, die im Produktionsfluss aufeinander folgen, werden erstellt, sind aber nicht verknüpft.


## <a name="find-the-production-flow-version"></a>Produktionsflussversion suchen 
1. Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Markieren Sie in der Liste die ausgewählte Zeile.
5. Wählen Sie in der Liste ein Entwurfsversion aus.
    * Aktivitätsrelationen können zum Entwurf oder zu aktiven Versionen eines Produktionsflusses hinzugefügt werden.  

## <a name="open-the-activity-overview"></a>Aktivitätsüberblick öffnen
1. Klicken Sie auf "Aktivitäten".
    * Beachten Sie, dass im Formular alle Aktivitäten des Produktionsflusses angezeigt werden, die der Version der Produktionsflüsse zugeordnet sind, in der Sie arbeiten.  

## <a name="add-a-successor"></a>Eine Folgeaktivität hinzufügen
1. Klicken Sie "Folgeaktivität hinzufügen".
2. Klicken Sie im Feld "Aktivität" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Markieren Sie das Kontrollkästchen "Einschränkung".
6. Geben Sie eine Zahl in das Feld 'Einschränkungswert' ein.
    * Die Einschränkungszeit ist die Zeit, die zwischen dem geplanten Enddatum der vorherigen Aktivität (Fälligkeitsdatum und Uhrzeit) und dem geplantem Start der Folgeaktivität eingeplant wird.  
7. Geben Sie im Feld "Einheit" einen Wert ein.
8. Geben Sie im Feld "Zykluszeitanteil" eine Zahl ein.
    * Wenn beide Aktionen am gleichen Takt ausgeführt werden, sollte der Zykluszeitanteil 1 sein. Wenn die vorherige Aktivität die doppelten Geschwindigkeit der Folgeaktivität ausgeführt wird, sollte das Verhältnis 2 sein.   Anhand des Anteils werden die durchschnittlichen Zykluszeiten für alle Aktivitäten des Produktionsflusses berechnet.  
9. Klicken Sie auf "OK".
10. Schließen Sie die Seite.
11. Klicken Sie auf die Registerkarte "GridPanel".
12. Schließen Sie die Seite.
13. Aktualisieren Sie die Seite.

