---
title: Kapazitätsauslastung berechnen
description: In diesem Thema wird erläutert, wie die Kapazitätsauslastung in der Anlagenverwaltung berechnet wird.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5015955338a4cbc2b51585d6297756f20dccee8b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428821"
---
# <a name="calculate-capacity-load"></a>Kapazitätsauslastung berechnen

[!include [banner](../../includes/banner.md)]


In Anlagenmanagement können Sie die Kapazitätsauslastung berechnen für

- Wartungszeitplanpositionen  
- Arbeitsaufträge, die noch nicht geplant wurden  
- Geplante Arbeitsaufträge

Dies ist hilfreich, wenn Sie einen Überblick über die erwarteten Kapazitätsauslastung während einer bestimmten Periode erhalten möchten. Die Berechnung der Kapazitätsauslastung kann für alle oder ausgewählte Anlagen ausgeführt werden. Sie können auch eine Berechnung für Wartungsausfallzeitaktivitäten oder Arbeitsauftragspools erstellen.

1. Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Kapazitätsauslastung** oder **Anlagenverwaltung** > **Allgemein** > **Arbeitsauftragspools** > **Alle Arbeitsauftragspools** / **Aktive Arbeitsauftragspools** > Arbeitsauftragspool in der Liste auswählen > Schaltfläche **Kapazitätsauslastung** oder **Anlagenverwaltung** > **Allgemein** > **Wartungsausfallzeitaktivitäten** > **Alle Wartungsausfallzeitaktivitäten** / **Aktive Wartungsausfallzeitaktivitäten** > Wartungsausfallzeitaktivität in der Liste auswählen > Schaltfläche **Kapazitätsauslastung**.

2. Wählen Sie im Dialogfeld **Kapazitätsauslastung berechnen** eine Periode für die Berechnung in den Feldern **Startdatum/-uhrzeit** und **Enddatum/-uhrzeit** aus.

3. Wählen Sie „Ja“ auf der Umschaltschaltfläche **Wartungszeitplan einbeziehen** aus, wenn Sie Wartungszeitplanpositionen in die Berechnung einbeziehen möchten.

4. Wählen Sie „Ja“ auf der Umschaltschaltfläche **Arbeitsauftrag einbeziehen** aus, wenn Sie Arbeitsauftragspositionen in die Berechnung einbeziehen möchten.

5. Sie können das Feld **Ebene** verwenden, um anzugeben, wie detailliert die Kapazitätsauslastungspositionen bezüglich funktionaler Standorte sein sollen. 

    Wenn Sie beispielsweise die Zahl „1“ im Feld einfügen und eine funktionale Standortstruktur auf mehreren Ebenen haben, werden alle Wartungszeitplanpositionen und Arbeitsaufträge für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher werden die Stunden in einer Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt. 
    
    Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Wartungszeitplanpositionen und allen Arbeitsaufträgen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.

6. Klicken Sie auf **OK**, um die Berechnung zu starten.

7. In den Gruppen **Gruppieren nach…** klicken Sie auf die entsprechenden Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen. Im Screenshot unten werden die ausgewählten **Gruppieren nach**-Schaltflächen in blauer Farbe hervorgehoben. Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.

    ![Abbildung 1](media/01-capacity-planning.png)

>[!NOTE]
>Wenn Sie sich nur auf die Kapazitätsplanung bezüglich geplanter Arbeitsaufträge konzentrieren möchten, finden Sie Informationen unter [Berechnen der Kapazitätsauslastung für geplante Arbeitsaufträge](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).

