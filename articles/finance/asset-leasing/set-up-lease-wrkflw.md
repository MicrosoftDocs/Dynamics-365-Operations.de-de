---
title: Leasinggenehmigungs-Workflows einrichten
description: In diesem Thema wird erläutert, wie Sie einen Genehmigungs-Workflow einrichten, der ausgeführt wird, wenn ein neuer Mietvertrag erstellt wird.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 58c0fd781710b7ab8efeaa7a6874f412279a5924
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4443763"
---
# <a name="set-up-lease-approval-workflows"></a>Leasinggenehmigungs-Workflows einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie einen Genehmigungs-Workflow einrichten, der ausgeführt wird, wenn ein neuer Mietvertrag erstellt wird. Informationen zum Verwenden des Workflows finden Sie unter [Verwenden von Workflows für die Leasinggenehmigung](use-create-lease-wrkflw.md). 

1. Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Leasing-Workflow**.
2. Wählen Sie auf der Seite **Leasing-Workflow** die Option **Neu** aus.
3. Im daraufhin angezeigten Dialogfeld unter **Workflow-Typ** wählen Sie die **Leaseing-Workflow**-Verknüpfung aus.

    Die Anwendung wird geöffnet. Melden Sie sich nach der Ausführung bei Azure Active Directory (Azure AD) an, um zur Workflow-Anwendung weitergeleitet zu werden.

4. Ziehen Sie das **Leasing-Workflow-Genehmigung**-Element in den Workflow.
5. Verbinden Sie einen Knoten von **Start** mit **Leasing-Workflow-Genehmigung**. Verbinden Sie dann **Leasing-Workflow-Genehmigung** mit **Ende**.
6. Klicken Sie zweimal auf **Leasing-Workflow-Genehmigung**.
7. Wählen Sie **Eigenschaften** und geben Sie dann unter **Grundeinstellungen** einen Namen für den Workflow ein.

    Auf dieser Seite können Sie auch weitere Parameter für den Workflow festlegen. Wenn Sie **Automatische Aktionen** eingeschaltet haben, ergreift das System automatisch eine bestimmte Aktion. Benachrichtigungen können gesendet werden, wenn sie auf der Registerkarte **Benachrichtigungen** angegeben sind. Auf der Registerkarte **Erweiterte Einstellungen** können Sie eine endgültige genehmigende Person angeben, ein Zeitlimit festlegen und bestimmte Aktionen festlegen, die ausgeführt werden müssen.

8. Wenn Sie die Workflow-Parameter eingestellt haben, wählen Sie **Schließen**.
9. Wählen Sie **Schritt 1** und dann **Eigenschaften** aus.
10. Geben Sie unter **Grundeinstellungen** einen Namen für den Schritt ein, erstellen Sie eine Betreffzeile für die Genehmigung und geben Sie Anweisungen für die Genehmigung an.
11. Auf der **Zuweisung**-Seite wählen Sie den Zuweisungstyp aus.
12. Um der Genehmigung bestimmte Benutzer zuzuweisen, wählen Sie **Benutzer** aus, wählen Sie die Benutzer aus, die Mietverträge genehmigen, und wählen Sie dann **Schließen**.
13. Wählen Sie **Speichern und schließen**, um den Workflow zu erstellen. Wenn Sie dazu aufgefordert werden, wählen Sie **OK**.
14. Wählen Sie auf der Seite **Workflow erstellen** die Option **Erstellen** aus.
14. Wählen Sie den neuen Workflow aus und wählen Sie dann **Versionen**. Wählen Sie dann **Aktivieren**, um sicherzustellen, dass der Workflow aktiv ist.
15. Wählen Sie **Schließen** aus. Die neue aktive Version wird angezeigt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]