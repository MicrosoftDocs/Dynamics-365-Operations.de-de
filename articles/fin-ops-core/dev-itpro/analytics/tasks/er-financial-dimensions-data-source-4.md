---
title: 'ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 4: Berichtsausführung)'
description: In diesem Thema wird beschrieben, wie Sie ein EB-Modell (elektronische Berichterstellung) konfigurieren, um Finanzdimensionen als Datenquelle für EB-Berichte zu verwenden. (Teil 4)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1fe332de84339d3369ba495ca13f50c4901f366
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092274"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a>ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 4: Berichtsausführung)

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann. Diese Schritte können im DEMF-Unternehmen ausgeführt werden.

Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren „ER - Finanzdimensionen als Datenquelle nutzen (Teil 3: Design des Berichts)“ ausführen. Sie müssen außerdem Standarddokumenttypen der elektronischen Berichterstellungsparameterseite konfigurieren. Standarddokumenttypen werden auch festgelegt, wenn Sie alle ER-Konfiguration herunterladen und importieren. 


## <a name="run-report"></a>Berichte ausführen
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Erweitern Sie in der Struktur "Finanzdimensions-Beispielmodell".
3. Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell\Sachkontoerfassungsbericht".
4. Klicken Sie auf Ausführen.
![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run1.png)
5. Geben Sie im Feld 'Dimensionsname' einen Wert ein, oder wählen Sie einen Wert aus.
    * Um alle Dimensionen im aktuellen Unternehmen auszuwählen, geben Sie folgende Informationen ein: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run2.png)
6. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
7. Klicken Sie auf "Filter".
8. Wählen Sie die Zeile für die Sachkontoerfassungstabelle und das Feld Erfassungschargennummer aus.
9. Geben Sie im Feld "Kriterien" den Wert "00057" ein.
10. Klicken Sie auf "OK".
11. Klicken Sie auf "OK".
![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run3.png)
    * Prüfen Sie das generierte Ergebnis. Für jede Buchung der ausgewählten Charge werden die Finanzdimensionen aus den entsprechenden Dimensionssatz dargestellt. Führen Sie diesen Bericht aus und wählen Sie unterschiedliche Dimensionen aus, um zu sehen, dass der Bericht nicht von der Anzahl der ausgewählten Dimensionen oder aus der Anzahl der Dimensionen abhängt, die für diese Instanz konfiguriert werden.  
![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run4.png)
