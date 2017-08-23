--- 
title: Anlagen umgliedern
description: "Wenn Sie eine Anlage umgliedern möchten, müssen Sie sie in eine neue Anlagengruppe übertragen oder ihr eine neue Anlagennummer in der gleichen Gruppe zuordnen."
author: saraschi2
manager: AnnBe
ms.date: 06/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: dcad2c2e225a07bf9e9eb7fe7bbec605f668f8f5
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="reclassify-fixed-assets"></a>Anlagen umgliedern

[!include[task guide banner](../../includes/task-guide-banner.md)]

Wenn Sie eine Anlage umgliedern möchten, müssen Sie sie in eine neue Anlagengruppe übertragen oder ihr eine neue Anlagennummer in der gleichen Gruppe zuordnen. 

Wenn eine Anlage neu klassifiziert wird:

• Alle Wertmodelle für die vorhandene Anlage werden für die neue Anlage erstellt. Alle für die ursprüngliche Anlage eingerichteten Daten werden in die neue Anlage kopiert. Der Status der Wertmodelle für die ursprüngliche Anlage lautet „Geschlossen”. 

• Bei den neuen Wertmodellen der neuen Anlage ist das Neuklassifizierungsdatum im Feld „Anschafungsdatum” enthalten. Das Datum im Feld „Ausführungsdatum der Abschreibung” stammt aus den ursprünglichen Informationen der Anlage. Hat die Abschreibung bereits begonnen, zeigt das Feld „Datum der letzten Abschreibung” das Datum der letzten Neuklassifizierung an. 

• Die vorhandenen Anlagenbuchungen für die ursprüngliche Anlage werden storniert und für die neue Anlage neu generiert.

1. Wechseln Sie zu „Anlagen” > „Periodische Aufgaben” > „Neuklassifizierung”.
2. Wählen Sie im Feld „Anlagengruppe” die Gruppe aus, die neu klassifiziert werden soll.
3. Wählen Sie im Feld „Anlagennummer” die Anlage aus, die neu klassifiziert werden soll.
4. Wählen Sie im Feld „Neue Anlagengruppe” eine Gruppe aus, an die die Anlage übertragen werden soll.
    * Wenn die neue Anlagengruppe einem Nummernkreis zugeordnet ist, wird das Feld „Neue Anlagennummer” mit der Nummer aus dem Nummernkreis für die neue Anlagengruppe aktualisiert. Anderenfalls wird das Feld „Neue Anlagennummer” mit der Nummer aus dem Nummernkreis aktualisiert, der auf der Seite „Anlagenparameter” eingerichtet wird. Wenn ein Nummernkreis nicht auf der Seite Anlagenparameter eingerichtet ist, geben Sie eine Nummer im Feld „Neue Anlagennummer” ein.  
5. Geben Sie im Feld „Neuklassifizierungsdatum” ein Datum ein.
6. Geben Sie im Feld "Belegserie" einen Wert ein, oder wählen Sie einen Wert aus.
7. Klicken Sie auf "OK".


