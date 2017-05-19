---
title: "Konfigurieren einer parallelen Aktivität in einem Workflow"
description: "Führen Sie im Workflow-Editor die folgenden Schritte aus, um eine parallele Aktivität zu konfigurieren."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ce3fca9d2dbca046232365b1375bfd920d5b10fd
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Konfigurieren einer parallelen Aktivität in einem Workflow

[!include[banner](../includes/banner.md)]


Führen Sie im Workflow-Editor die folgenden Schritte aus, um eine parallele Aktivität zu konfigurieren.

Eine parallele Aktivität besteht aus Workflowverzweigungen, die gleichzeitig ausgeführt werden.

## <a name="name-a-parallel-activity"></a>Name der Parallelaktivität
Gehen Sie folgendermaßen vor, um einen Namen für die parallele Aktivität einzugeben.
1.  Klicken Sie mit der rechten Maustaste auf die parallele Aktivität, und klicken Sie anschließend auf **Eigenschaften**, um das Formular **Eigenschaften** zu öffnen.
2.  Klicken Sie im linken Bereich auf **Grundeinstellungen**.
3.  Geben Sie im Feld **Name** einen eindeutigen Namen für die parallele Aktivität ein.
4.  Klicken Sie auf **Schließen**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Konfigurieren der Verzweigungen der parallelen Aktivität
Gehen Sie folgendermaßen vor, um die Verzweigungen dieser parallelen Aktivität hinzuzufügen und zu konfigurieren.
1.  Doppelklicken Sie auf die parallele Aktivität, um die Verzweigungen der parallelen Aktivität anzuzeigen.
2.  Ziehen Sie zum Hinzufügen einer Zweigstelle das Element **Zweigstelle** aus dem Bereich **Elemente** hinzu. Die folgende Abbildung zeigt einen Einfügepunkt.![Einfügepunkt](./media/workflow_insertionpoint.gif)
    | **Hinweis**                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | Die Reihenfolge der Verzweigungen ist nicht relevant, da alle Verzweigungen einer parallelen Aktivität gleichzeitig ausgeführt werden. |

3.  Informationen zum Konfigurieren jeder Zweigstelle finden Sie unter [Konfigurieren einer parallelen Zweigstelle](configure-parallel-branch-workflow.md).






