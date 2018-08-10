---
title: Einen Produktionsauftrag starten
description: "Diese Prozedur zeigt an, wie Sie Produktionsaufträge für die Produktion starten."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 3b5657e5eb2719702eae3a3c5178b3a04f7545e3
ms.contentlocale: de-de
ms.lasthandoff: 02/06/2018

---
# <a name="start-a-production-order"></a>Einen Produktionsauftrag starten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt an, wie Sie Produktionsaufträge für die Produktion starten. Zeit und Materialverbrauch werden in diesem Prozess gemeldet. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Dies ist die fünfte Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.


## <a name="start-a-production-order"></a>Einen Produktionsauftrag starten
1. Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".
    * Wählen Sie einen Produktionsauftrag aus, der den Status "Freigegeben" aufweist.  
2. Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".
3. Klicken Sie auf "Start".
    * Auf dieser Seite können Sie den Beginn des Produktionsauftrags bestätigen.  
4. Klicken Sie auf die Registerkarte "Allgemein".
5. Im Feld "Von Arbeitsgangnr." Nr. geben Sie "10 " ein.
6. Wählen Sie im Feld "Automatische Arbeitsplanrückmeldung" "Immer" aus.
7. Klicken Sie auf das Kontrollkästchen "Arbeitsplanliste jetzt buchen".
8. Wählen Sie im Feld "Soll=Istrückmeldung Material" "immer" aus.
9. Klicken Sie auf das Kontrollkästchen "Kommissionierliste jetzt buchen".
10. Klicken Sie auf das Kontrollkästchen "Kommissionierliste drucken".
11. Klicken Sie auf "OK".
    * Dies ist die gedruckte Kommissionierliste, in der die Materialien angezeigt werden, die für den Produktionsauftrag verwendet werden.  
12. Schließen Sie die Seite.

## <a name="validate-the-picking-list"></a>Kommissionierliste überprüfen
1. Klicken Sie im Aktivitätsbereich auf "Anzeigen".
2. Klicken Sie auf "Kommissionierliste".
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie auf "Bearbeiten".
6. Geben Sie im Feld "Verbrauch" eine Zahl ein.
7. Klicken Sie auf "Buchen".
8. Klicken Sie auf "OK".
    * In der Kommissionierlistenerfassung werden die Materialien, die für den Produktionsauftrag verbraucht werden, gebucht. Bevor Sie die Erfassung buchen, können Sie Anpassungen vornehmen, wenn sich die vorkalkulierte Menge und die tatsächlich verbrauchte Menge von einander unterscheiden.  
9. Klicken Sie auf die Registerkarte "GridPanel".
10. Schließen Sie die Seite.

## <a name="verify-the-route-card-journal"></a>Arbeitsplanlistenerfassung überprüfen
1. Klicken Sie im Aktivitätsbereich auf "Anzeigen".
2. Klicken Sie auf Arbeitsplanliste.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie auf "Bearbeiten".
6. Geben Sie im Feld "Stunden" eine Zahl ein.
7. Klicken Sie auf "Buchen".
8. Klicken Sie auf "OK".
    * In der Arbeitsplanlisten-Erfassung wird die Zeit, die für die Dauer der einzelnen Arbeitsgänge aufgewendet wird, erfasst. Gut- und Ausschussmengen können auch gemeldet werden.  

