---
title: Konfigurieren paralleler Aktivitäten in einem Workflow
description: Führen Sie im Workflow-Editor die folgenden Schritte aus, um eine parallele Aktivität zu konfigurieren.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 450420d44ad4aab233afc5a116369e993aa7a15b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570613"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>Konfigurieren paralleler Aktivitäten in einem Workflow

[!include [banner](../includes/banner.md)]

Führen Sie im Workflow-Editor die folgenden Schritte aus, um eine parallele Aktivität zu konfigurieren.

Eine parallele Aktivität besteht aus Workflowverzweigungen, die gleichzeitig ausgeführt werden.

## <a name="name-a-parallel-activity"></a>Name der Parallelaktivität

Gehen Sie folgendermaßen vor, um einen Namen für die parallele Aktivität einzugeben.

1. Klicken Sie mit der rechten Maustaste auf die parallele Aktivität, und klicken Sie anschließend auf **Eigenschaften**, um das Formular **Eigenschaften** zu öffnen.
2. Klicken Sie im linken Bereich auf **Grundeinstellungen**.
3. Geben Sie im Feld **Name** einen eindeutigen Namen für die parallele Aktivität ein.
4. Klicken Sie auf **Schließen**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Konfigurieren der Verzweigungen der parallelen Aktivität

Gehen Sie folgendermaßen vor, um die Verzweigungen dieser parallelen Aktivität hinzuzufügen und zu konfigurieren.

1. Doppelklicken Sie auf die parallele Aktivität, um die Verzweigungen der parallelen Aktivität anzuzeigen.
2. Ziehen Sie zum Hinzufügen einer Zweigstelle das Element **Zweigstelle** aus dem Bereich **Elemente** hinzu. Die folgende Abbildung zeigt einen Einfügepunkt.

    ![Einfügepunkt](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > Die Reihenfolge der Verzweigungen ist nicht relevant, da alle Verzweigungen einer parallelen Aktivität gleichzeitig ausgeführt werden.

3. Informationen zum Konfigurieren jeder Zweigstelle finden Sie unter [Konfigurieren paralleler Verzweigungen in einem Workflow](configure-parallel-branch-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]