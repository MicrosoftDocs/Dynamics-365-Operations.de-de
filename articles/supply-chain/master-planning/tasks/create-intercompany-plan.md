---
title: Intercompany-Plan erstellen
description: Dieses Verfahren zeigt, wie ein Intercompany-Plan erstellt wird.
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8cf4ed879b6b2202d0b0f1f45052f5e21452967
ms.sourcegitcommit: 9b07d536b4bd8addfbdba42d2429c9fedb664635
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867349"
---
# <a name="create-an-intercompany-plan"></a>Intercompany-Plan erstellen

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie ein Intercompany-Plan erstellt wird. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.

## <a name="set-up-an-intercompany-planning-group"></a>Intercompany-Planungsgruppe einrichten

1. Gehen Sie im **Navigationsbereich** zu **Module > Produktprogrammplanung > Einstellungen > Intercompany-Planungsgruppen**.
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Name" mit einem Wert "10".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Wählen Sei **Löschen**. Dieser Schritt ist erforderlich, um die Intercompany-Planung zu verkürzen.   Die Intercompany-Planung für die Produktprogrammplanung in allen Unternehmen in einer aus Planungsgruppe aus (ab dem niedrigsten Nummernkreis).  
5. Wählen Sie **Ja** aus.
6. Schließen Sie die Seite.

## <a name="create-an-intercompany-master-plan"></a>Einen Intercompany-Masterplan erstellen

1. Gehen Sie im **Navigationsbereich** zu **Module > Produktprogrammplanung > Arbeitsbereiche > Produktprogrammplanung**.
2. Wählen Sie **Intercompany-Produktprogrammplanungslauf** aus.  
3. Wählen Sie im Feld **Intercompany-Planungsgruppe** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.
4. Wählen Sie in der Liste den Link in der ausgewählten Zeile. Wählen Sie die Intercompany-Planungsgruppe 10.  
5. Geben Sie im Feld **Anzahl der Intercompany-Planungsiterationen** '2' ein. Intercompany-Planungsgruppe 10 hat zwei Mitglieder. Um die Verzögerungen aus dem Ausgangsunternehmen (USMF) an das Kundenunternehmen (DEMF) weiterzugeben, müssen Sie Intercompany in beiden Unternehmen einmal ausführen. Der erste Durchlauf gibt den Bedarf weiter und identifiziert die Verzögerungen im Quellunternehmen (USMF). Der zweite Durchlauf gibt die Verzögerungen von USMF an DEMF weiter.  
6. Wählen Sie im Feld **Erste Iteration** 'Neu erzeugen' aus.
7. Wählen Sie im Feld **Nachfolgende Iterationen** 'Neu erzeugen' aus.
8. Geben Sie im Feld **Anzahl von Threads** eine Zahl ein. Dies stellt die Anzahl von parallelen Threads für die Planung dar.  
9. Wählen Sie **OK**.

## <a name="view-the-result-of-the-plan"></a>Ergebnis der Planung anzeigen

1. Wählen Sie im Feld **Plan** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.
2. Wählen Sie in der Liste den Link in der ausgewählten Zeile. Wählen Sie den Link für StaticPlan aus. Sie müssen im Unternehmen USMF sein.  
3. Wählen Sie **Bestellvorschläge** aus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]