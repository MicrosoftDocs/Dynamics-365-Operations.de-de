---
title: Anlagen umgliedern
description: Wenn Sie eine Anlage umgliedern möchten, müssen Sie sie in eine neue Anlagengruppe übertragen oder ihr eine neue Anlagennummer in der gleichen Gruppe zuordnen.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944711"
---
# <a name="reclassify-fixed-assets"></a>Anlagen umgliedern

[!include [banner](../../includes/banner.md)]

Wenn Sie eine Anlage umgliedern möchten, müssen Sie sie in eine neue Anlagengruppe übertragen oder ihr eine neue Anlagennummer in der gleichen Gruppe zuordnen. 

Wenn eine Anlage neu klassifiziert wird:

- Alle Bücher für die vorhandene Anlage werden für die neue Anlage erstellt. Alle für die ursprüngliche Anlage eingerichteten Daten werden in die neue Anlage kopiert. Der Status der Bücher für die ursprüngliche Anlage lautet „Geschlossen“. 

- Die neuen Bücher für die neue Anlage enthalten das Datum der Umgliederung im Feld **Anschaffungsdatum**. Das Datum im Feld **Ausführungsdatum der Abschreibung** stammt aus den ursprünglichen Informationen der Anlage. Hat die Abschreibung bereits begonnen, zeigt das Feld **Datum der letzten Abschreibung** das Datum der letzten Neuklassifizierung an. 

- Die vorhandenen Anlagenbuchungen für die ursprüngliche Anlage werden storniert und für die neue Anlage neu generiert.

- Wenn eine Anlage mit einer Transfertransaktion umklassifiziert wurde, zeigt das System eine Nachricht im **Aktionscenter** an, um darauf hinzuweisen, dass eine Transfertransaktion während des Umklassifizierungsprozesses nicht abgeschlossen wurde. Es ist notwendig, eine Transfer-Transaktion durchzuführen, um die vorhandenen Umgliederungstransaktionen in die entsprechenden finanziellen Dimensionen zu verschieben. 

   Während des Umgliederungsprozesses führt das System die folgenden Aktionen aus, um den Vermögenssaldo vom ursprünglichen Vermögen in das neue Vermögen umzugliedern. 
   
   - Der Umgliederungsprozess kopiert die Daten aus dem ursprünglichen Anlagenbuch in das neue Anlagenbuch.

   - Die Umgliederungstransaktion verwendet Informationen aus dem ursprünglich gebuchten Zugang, die Informationen zur finanziellen Dimension enthalten, die in der Zugangstransaktion enthalten sind.  
   
   - Gleichzeitig macht der Umgliederungsprozess die ursprüngliche Transaktion des Anlagenerwerbs und -transfers rückgängig. 

Das folgende Diagramm und die Prozedur zeigen ein Beispiel für den Umgliederungsprozess. 

[![Diagramm zur Neuklassifizierung](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)

Gehen Sie folgendermaßen vor, um eine Anlage neu zu klassifizieren:

1. Wechseln Sie zu **Anlagen > Periodische Aufgaben > Neuklassifizierung**.
2. Wählen Sie im Feld **Anlagengruppe** die Gruppe aus, die neu klassifiziert werden soll.
3. Wählen Sie im Feld **Anlagennummer** die Anlage aus, die neu klassifiziert werden soll.
4. Wählen Sie im Feld **Neue Anlagengruppe** eine Gruppe aus, an die die Anlage übertragen werden soll.
    * Wenn die neue Anlagengruppe einem Nummernkreis zugeordnet ist, wird das Feld **Neue Anlagennummer** mit der Nummer aus dem Nummernkreis für die neue Anlagengruppe aktualisiert. Anderenfalls wird das Feld **Neue Anlagennummer** mit der Nummer aus dem Nummernkreis aktualisiert, der auf der Seite **Anlagenparameter** eingerichtet wird. Wenn ein Nummernkreis nicht auf der Seite **Anlagenparameter** eingerichtet ist, geben Sie eine Nummer im Feld **Neue Anlagennummer** ein.  
5. Geben Sie im Feld **Neuklassifizierungsdatum** ein Datum ein.
6. Geben Sie im Feld **Belegserie** einen Wert ein, oder wählen Sie einen Wert aus.
7. Wählen Sie **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
