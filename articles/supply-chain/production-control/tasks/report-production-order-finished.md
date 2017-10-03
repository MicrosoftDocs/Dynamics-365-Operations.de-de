--- 
title: Einen Produktionsauftrag als abgeschlossen melden
description: Diese Prozedur zeigt an, wie ein Produktionsauftrag als abgeschlossen gemeldet wird.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ff651be006b4bbe205aa9937bd7927e37a83a558
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="report-a-production-order-as-finished"></a>Einen Produktionsauftrag als abgeschlossen melden

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt an, wie ein Produktionsauftrag als abgeschlossen gemeldet wird. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Dies ist die sechste Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.


## <a name="report-a-production-order-as-finished"></a>Einen Produktionsauftrag als abgeschlossen melden
1. Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".
    * Wählen Sie einen Produktionsauftrag aus, der den Status "Gestartet" aufweist.  
2. Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".
3. Klicken Sie auf "Fertigmeldung".
    * Auf dieser Seite können Sie die Menge der als fertig gestellt zu meldenden Fertigproduktionen bestätigen.  
4. Klicken Sie auf die Registerkarte "Allgemein".
5. Legen Sie "Gutmenge" auf "18" fest.
6. Legen Sie "Ausschussmenge" auf "2" fest.
7. Wählen Sie im Feld "Fehlerursache" " Material "aus.
8. Aktivieren oder deaktivieren Sie das Kontrollkästchen "Enddurchlauf".
9. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Fehler akzeptieren".
10. Klicken Sie auf "OK".

## <a name="verify-the-report-as-finished-journal"></a>Die Erfassung "Fertigmeldung" überprüfen
1. Klicken Sie im Aktivitätsbereich auf "Anzeigen".
2. Klicken Sie auf "Fertigmeldung".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Die Erfassung "Fertigmeldung" wurde gebucht. Wenn Sie Regulierungen in der Erfassung vornehmen möchten, können Sie manuell eine neue Erfassung erstellen, in der Sie Änderungen vornehmen können.  


