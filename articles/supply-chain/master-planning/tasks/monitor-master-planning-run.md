---
title: Einen Produktprogrammplanungslauf überwachen
description: Der Produktionsplaner möchte sehen, ob ein Produktprogrammplanungslauf in Bearbeitung ist.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c2e158d8cbad1f5d4f377f6a8eb43487b34ffdc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "367500"
---
# <a name="monitor-a-master-planning-run"></a>Einen Produktprogrammplanungslauf überwachen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Der Produktionsplaner möchte sehen, ob ein Produktprogrammplanungslauf in Bearbeitung ist. Verwenden Sie das Demodatenunternehmen USMF, um diese Prozedur abzuschließen.


## <a name="run-master-planning"></a>Produktprogrammplanung ausführen
1. Klicken Sie auf "Produktprogrammplanung".
    * Sie finden dies auf dem Standard-Dashboard.  
2. Geben Sie im Feld "Plan" einen Wert ein, oder wählen Sie einen Wert aus.
    * Beispiel: StaticPlan  
3. Klicken Sie auf "Ausführen".
4. Wählen Sie "Ja" im Feld "Verarbeitungszeit nachverfolgen" aus.
    * Wenn das Feld bereits ausgewählt ist, überspringen Sie diesen Schritt.  
5. Geben Sie im Feld "Anzahl von Threads" eine Zahl ein.
6. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
7. Klicken Sie auf "Filter".
8. Markieren Sie in der Liste die ausgewählte Zeile.
    * Markieren Sie die Zeile, in der "Feld = Artikelnummer" ist.  
9. Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.
    * Beispiel: T0001  
10. Klicken Sie auf "OK".
11. Klicken Sie auf "OK".

## <a name="monitor-the-master-planning-run"></a>Überwachen Sie den Produktprogrammplanungslauf
1. Klicken Sie auf "Historie".
2. Klicken Sie auf Abfragen.
3. Klicken Sie auf "Prozessaufgabendauer".
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Für jeden Artikel können Sie einen Überblick darüber erhalten, wie lange es gedauert hat, um jeden Planungsschritt abzuschließen.  

