---
title: Intercompany-Plan erstellen
description: Dieses Verfahren zeigt, wie ein Intercompany-Plan erstellt wird.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d378a89bbb4de6d67db0019dc72a27945d50c4e9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555976"
---
# <a name="create-an-intercompany-plan"></a>Intercompany-Plan erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie ein Intercompany-Plan erstellt wird. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Intercompany-Planungsgruppe einrichten 
1. Wechseln Sie zu Intercompany-Planungsgruppen.
    * "Produktprogrammplan" > "Einrichten" > "Intercompany-Planungsgruppen"  
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Name" mit einem Wert "10".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Klicken Sie auf Löschen.
    * Dieser Schritt ist erforderlich, um die Intercompany-Planung zu verkürzen.   Die Intercompany-Planung für die Produktprogrammplanung in allen Unternehmen in einer aus Planungsgruppe aus (ab dem niedrigsten Nummernkreis).  
5. Klicken Sie auf "Ja".
6. Schließen Sie die Seite.

## <a name="create-an-intercompany-plan"></a>Intercompany-Plan erstellen
1. Klicken Sie auf "Intercompany-Produktprogrammplanungslauf".
    * Dies ist auf dem Produktprogrammplanungsarbeitsbereich.  
2. Klicken Sie im Feld "Intercompany-Planungsgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie die Intercompany-Planungsgruppe 10.  
4. Geben Sie im Feld "Anzahl der Intercompany-Planungsiterationen" 2 ein.
    * Intercompany-Planungsgruppe 10 hat zwei Mitglieder. Um die Verzögerungen aus dem Ausgangsunternehmen (USMF) an das Kundenunternehmen (DEMF) weiterzugeben, müssen Sie Intercompany in beiden Unternehmen einmal ausführen. Der erste Durchlauf gibt den Bedarf weiter und identifiziert die Verzögerungen im Quellunternehmen (USMF). Der zweite Durchlauf gibt die Verzögerungen von USMF an DEMF weiter.  
5. Wählen Sie im Feld 'Erste Iteration' eine Option aus.
6. Wählen Sie im Feld 'Erste Iteration' "Neu erzeugen" aus.
7. Wählen Sie im Feld 'Nachfolgende Iterationen' "Neu erzeugen" aus.
8. Geben Sie im Feld "Anzahl von Threads" eine Zahl ein.
    * Dies stellt die Anzahl von parallelen Threads für die Planung dar.  
9. Klicken Sie auf "OK".

## <a name="view-the-result-of-the-plan"></a>Ergebnis der Planung anzeigen
1. Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
2. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Klicken Sie auf den Link für StaticPlan. Sie müssen im Unternehmen USMF sein.  
3. Klicken Sie auf "Bestellvorschläge".

