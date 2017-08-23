--- 
title: "Ausführen eines Berichts, der Finanzdimensionen als Datenquelle für elektronische Berichterstellung (ER) verwendet"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f07e640d4b2a7f67d48df4c081819a55e7e68cda
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Ausführen eines Berichts, der Finanzdimensionen als Datenquelle für elektronische Berichterstellung (ER) verwendet

[!include[task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann. Diese Schritte können im DEMF-Unternehmen ausgeführt werden.

Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren "ER - Finanzdimensionen als Datenquelle nutzen (Teil 3: Design des Berichts)" ausführen. Sie müssen außerdem Standarddokumenttypen der elektronischen Berichterstellungsparameterseite konfigurieren. Standarddokumenttypen werden auch festgelegt, wenn Sie alle ER-Konfiguration herunterladen und importieren. 


## <a name="run-report"></a>Berichte ausführen
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Erweitern Sie in der Struktur "Finanzdimensions-Beispielmodell".
3. Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell\Sachkontoerfassungsbericht".
4. Klicken Sie auf Ausführen.
5. Wählen Sie im Dimensionsnamen-Feld eine Option aus oder geben Sie einen Wert ein.
    * Um alle Dimensionen im aktuellen Unternehmen auszuwählen, geben Sie Folgendes ein: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
6. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
7. Klicken Sie auf "Filter".
8. Wählen Sie die Zeile für die Sachkontoerfassungstabelle und das Feld Erfassungschargennummer aus.
9. Geben Sie im Feld "Kriterien" den Wert "00057" ein.
10. Klicken Sie auf "OK".
11. Klicken Sie auf "OK".
    * Prüfen Sie das generierte Ergebnis. Beachten Sie, das für jede Buchung der ausgewählten Charge, die Finanzdimensionen aus den entsprechenden Dimensionssatz dargestellt werden. Führen Sie diesen Bericht aus und wählen Sie unterschiedliche Dimensionen aus, um zu sehen, dass der Bericht nicht von der Anzahl der ausgewählten Dimensionen oder aus der Anzahl der Dimensionen abhängt, die in Dynamics 365 for Finance and Operations, Enterprise Edition für diese Instanz konfiguriert werden.  


