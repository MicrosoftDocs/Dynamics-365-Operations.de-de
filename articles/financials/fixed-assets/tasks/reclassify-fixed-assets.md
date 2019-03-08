---
title: Anlagen umgliedern
description: Wenn Sie eine Anlage umgliedern möchten, müssen Sie sie in eine neue Anlagengruppe übertragen oder ihr eine neue Anlagennummer in der gleichen Gruppe zuordnen.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8e289e2c18fd28829fb4b749933ae1d84e0b631
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "323294"
---
# <a name="reclassify-fixed-assets"></a>Anlagen umgliedern

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

