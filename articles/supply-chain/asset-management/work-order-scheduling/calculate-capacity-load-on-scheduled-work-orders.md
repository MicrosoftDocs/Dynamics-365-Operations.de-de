---
title: Berechnen der Kapazitätsauslastung für geplante Arbeitsaufträge
description: In diesem Thema wird erläutert, wie die Kapazitätsauslastung für geplante Arbeitsaufträge in der Anlagenverwaltung berechnet wird.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7b7e4a20ed56b1eac29d16d527693d6e455cdc37
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021653"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Berechnen der Kapazitätsauslastung für geplante Arbeitsaufträge

[!include [banner](../../includes/banner.md)]

 

Sie können die Kapazitätsauslastung für geplante Arbeitsaufträge berechnen, um eine Übersicht der Arbeitsauslastung von Ressourcen für einen bestimmten Zeitraum zu erhalten. Berechnungen können für die folgenden Ressourcen vorgenommen werden: Wartungsarbeiter, Arbeitskraftgruppen, Werkzeuge und Anlagen.

1. Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Planung** > **Kapazitätsauslastung**.

2. Wählen Sie im Dialogfeld **Kapazitätsauslastung berechnen** > **Anzeigen** aus, welchen Auslastungstyp Sie berechnen möchten: **Kapazität**, **Reserviert** oder **Rest**.

3. Wählen Sie **Ja** auf der Umschaltfläche **Null überspringen** aus, wenn keine Ergebnisse mit Null angezeigt werden sollen.

4. Wählen Sie die Ressourcentypen aus, für die Sie die Kapazitätsauslastung berechnen möchten, indem Sie **Ja** auf den relevanten Umschaltschaltflächen auswählen: **Arbeitskraft**, **Wartungsarbeitergruppe**, **Werkzeug** und **Anlage**.

5. Wählen Sie das Startdatum für die Berechnung im Feld **Von Datum** aus.

6. Im Feld **Intervalltyp** wählen Sie das Intervall für die Kalkulation aus: **Tag**, **Woche**, **Monat** oder **Quartal**.

7. Fügen Sie im Feld **Periodenhäufigkeit** die Anzahl der Intervalle ein, für die Sie eine Kalkulation ausführen möchten. Wenn Sie beispielsweise **Tag** als Intervalltyp ausgewählt haben und Sie die Zahl „5“ in diesem Feld eingeben, wird eine Berechnung von fünf Tagen ab dem Startdatum vorgenommen.

8. Klicken Sie auf **OK**, um die Berechnung zu starten.

Die Abbildung unten zeigt das Ergebnis einer Berechnung, die drei Wochen abdeckt, für den Auslastungstyp **Reserviert**.

![Abbildung 1](media/08-work-order-scheduling.png)

[!NOTE]
Wenn Sie Auslastungstypen **Kapazität** oder **Rest** für die Berechnung auswählen, wird dasselbe Ergebnis angezeigt, wenn keine Reservierungen für die Ressourcen in der ausgewählten Periode vorgenommen wurden.

Weitere Informationen darüber, wie die Kapazitätsauslastung für Wartungsplanpositionen und nicht geplante Arbeitsaufträge berechnet wird, finden Sie unter [Berechnen der Kapazitätsauslastung](../capacity-planning/calculate-capacity-load.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]