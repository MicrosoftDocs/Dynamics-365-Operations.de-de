---
title: Intercompany-Plan erstellen
description: Dieses Verfahren zeigt, wie ein Intercompany-Plan erstellt wird.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ae3d8a7c437ffd41a4864bd8548aa84c8ab8f32
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428563"
---
# <a name="create-an-intercompany-plan"></a>Intercompany-Plan erstellen

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie ein Intercompany-Plan erstellt wird. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Intercompany-Planungsgruppe einrichten 
1. Gehen Sie im **Navigationsbereich** zu **Module > Produktprogrammplanung > Einstellungen > Intercompany-Planungsgruppen**. 
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Name" mit einem Wert "10".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Klicken Sie auf **Löschen**. Dieser Schritt ist erforderlich, um die Intercompany-Planung zu verkürzen.   Die Intercompany-Planung für die Produktprogrammplanung in allen Unternehmen in einer aus Planungsgruppe aus (ab dem niedrigsten Nummernkreis).  
5. Klicken Sie auf **Ja**.
6. Schließen Sie die Seite.

## <a name="create-an-intercompany-plan"></a>Intercompany-Plan erstellen
1. Gehen Sie im **Navigationsbereich** zu **Module > Produktprogrammplanung > Arbeitsbereiche > Produktprogrammplanung**.
2. Klicken Sie auf **Intercompany-Produktprogrammplanungslauf**.  
3. Klicken Sie im Feld **Intercompany-Planungsgruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile. Wählen Sie die Intercompany-Planungsgruppe 10.  
5. Geben Sie im Feld **Anzahl der Intercompany-Planungsiterationen** '2' ein. Intercompany-Planungsgruppe 10 hat zwei Mitglieder. Um die Verzögerungen aus dem Ausgangsunternehmen (USMF) an das Kundenunternehmen (DEMF) weiterzugeben, müssen Sie Intercompany in beiden Unternehmen einmal ausführen. Der erste Durchlauf gibt den Bedarf weiter und identifiziert die Verzögerungen im Quellunternehmen (USMF). Der zweite Durchlauf gibt die Verzögerungen von USMF an DEMF weiter.  
6. Wählen Sie im Feld **Erste Iteration** 'Neu erzeugen' aus.
7. Wählen Sie im Feld **Nachfolgende Iterationen** 'Neu erzeugen' aus.
8. Geben Sie im Feld **Anzahl von Threads** eine Zahl ein. Dies stellt die Anzahl von parallelen Threads für die Planung dar.  
9. Klicken Sie auf **OK**.

## <a name="view-the-result-of-the-plan"></a>Ergebnis der Planung anzeigen
1. Klicken Sie im Feld **Plan** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
2. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile. Klicken Sie auf den Link für StaticPlan. Sie müssen im Unternehmen USMF sein.  
3. Klicken Sie auf **Bestellvorschläge**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]