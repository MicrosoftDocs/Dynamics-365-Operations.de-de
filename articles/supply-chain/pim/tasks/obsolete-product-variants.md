--- 
title: Suchen von veralteten Produktvarianten
description: Diese Prozedur zeigt, wie Sie veraltete freigegebene Produkte oder Produktvarianten finden und wie Sie den veralteten Produkten einen Produktlebenszyklus-Status zuordnen.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: 3a59f988de5290d1d69d013b762f87d0cce10e39
ms.contentlocale: de-de
ms.lasthandoff: 02/08/2018

---
# <a name="find-obsolete-product-variants"></a>Suchen von veralteten Produktvarianten 

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie Sie veraltete freigegebene Produkte oder Produktvarianten finden und wie Sie den veralteten Produkten einen Produktlebenszyklus-Status zuordnen. Voraussetzung: Sie müssen mindestens ein Produktlebenszyklus-Status definieren, der für die Planung inaktiv ist, bevor Sie dieses Aufgabenleitfaden wiedergeben können.


## <a name="run-a-simulation"></a>Eine Simulation ausführen
1. Wechseln Sie zu „Produktinformationsverwaltung > Periodische Aufgaben >Lebenszyklusstatus für veraltete Produkte ändern.
2. Geben Sie im Feld „Neuer Produktlebenszyklus-Status” einen Wert ein, oder wählen Sie einen Wert aus.
3. Wählen Sie „Ja” im Feld „Simulation ausführen, ohne Produktdaten zu aktualisieren” aus.
4. Geben Sie im Feld „Innerhalb dieser Zahl von Tagen erstellte Produkte ausschließen” eine Zahl ein.
5. Geben Sie im Feld „Produkte ausschließen, die in Transaktionen verwendet werden (in Anzahl von Tagen)” eine Zahl ein.
6. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
7. Klicken Sie auf "Filter".
8. Markieren Sie in der Liste die ausgewählte Zeile.
9. Geben Sie im Feld "Kriterien" einen Wert ein.
10. Klicken Sie auf "OK".
11. Klicken Sie auf "OK".

> [!NOTE]
> Es wird empfohlen, die Simulation in einer Charge auszuführen, wenn Sie erwarten, eine große Anzahl von Produkten zu durchsuchen. Stellen Sie außerdem sicher, dass die Simulation nicht während der aktivsten Arbeitszeit des Unternehmens ausgeführt wird.  

## <a name="review-the-simulation-results"></a>Die Simulationsergebnisse überprüfen
1. Wechseln Sie zu Produktinformationsverwaltung > Abfragen und Berichte > Wartungsverlauf des Produktlebenszyklus-Status.
   
> [!NOTE]
> Auf dieser Seite können Sie die Simulationsergebnisse überprüfen und eine Bewertung dazu vornehmen, wie viele Produkte und Produktvarianten einem neuen Produktlebenszyklus-Status zugeordnet werden, wenn das Update ohne Simulation ausgeführt wird.  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a>Das Update des Produktlebenszyklus-Status für veraltete Produkte ausführen
1. Schließen Sie die Seite.
2. Wechseln Sie zu „Produktinformationsverwaltung > Periodische Aufgaben >Lebenszyklusstatus für veraltete Produkte ändern.
3. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".

> [!NOTE]
> Beachten Sie, dass die letzte Auswahl gespeichert wurde.  

4. Wählen Sie „Nein” im Feld „Simulation ausführen, ohne Produktdaten zu aktualisieren” aus.
5. Erweitern Sie den Abschnitt "Ausführen im Hintergrund".

> [!NOTE]
> Abhängig davon, wie viele Produkte und Produktvarianten betroffen sind, sollten Sie erwägen, diesen Einzelvorgang in einer Charge auszuführen. Stellen Sie sicher, dass Sie keinen großen Aktualisierungseinzelvorgang während der aktivsten Arbeitsstunden im Unternehmen ausführen.  

6. Klicken Sie auf "OK".
7. Wechseln Sie zu Produktinformationsverwaltung > Abfragen und Berichte > Wartungsverlauf des Produktlebenszyklus-Status.

> [!NOTE]
> Überprüfen Sie die geänderten freigegebenen Produkte und Produktvarianten.  

8. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.


