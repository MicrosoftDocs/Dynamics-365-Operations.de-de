---
title: Serviceauftragsphasen
description: "Wenn Sie die Phasen für einen Serviceauftrag definieren und diese den Arbeitskräften zuweisen, können Sie den Ablauf eines Serviceauftrags durch die Aufgaben steuern, die verschiedene Personen in der Serviceorganisation ausführen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9aa90dfcfc4b30d6cb4fa7ed4e6faaf505548d41
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="service-order-stages"></a>Serviceauftragsphasen   

[!include [banner](../includes/banner.md)]


Sie können Phasen für einen Serviceauftrag einrichten, um die Aufgaben zu definieren, die abgeschlossen werden müssen, die Reihenfolge, in der sie ausgeführt werden, und die Arbeitskräfte, die für ihre Ausführung zuständig sind. Wenn Sie die Phasen für einen Serviceauftrag definieren und diese den Arbeitskräften zuweisen, können Sie den Ablauf eines Serviceauftrags durch die Aufgaben steuern, die verschiedene Personen in der Serviceorganisation ausführen. Die Sequenz der Phasen muss eine Anfangsphase enthalten.

Sie können auch die Aktivitäten festlegen, die in jeder Stufe zulässig sind. Beispiel: Wird das Kontrollkästchen **Buchen** mit Ausnahme der letzten Phase für alle Phasen deaktiviert, können Serviceaufträge erst gebucht werden, nachdem sie die Phasen vollständig durchlaufen haben.

## <a name="branching-in-service-order-stages"></a>Verzweigung in Phasen des Serviceauftrags

Wenn Sie eine Servicephase einrichten, können Sie mehrere Optionen oder Verzweigungen erstellen, aus denen für die nächste Servicephase ausgewäht werden kann. Alle Verzweigungen, die Sie erstellen, können ausgewählt werden, wenn die Anfangsphase abgeschlossen ist. Beispielsweise richten Sie **Planung** als Anfangsphase ein. Sie erstellen zwei Phasen, die **In Bearbeitung** und **Abbrechen** benannt sind, und wählen dann **Planung** als das übergeordnete Element für sie aus. Sie weisen die Phase **Planung** dem Auftrag zu. Wenn die Planungsphase für den Auftrag abgeschlossen ist, können Sie die Phase **In Bearbeitung** auswählen, wenn der Auftrag für die Bearbeitung bereit ist, oder Sie können die Phase **Abbrechen** auswählen, wenn der Auftrag storniert wird.

## <a name="see-also"></a>Siehe auch

[Serviceauftragsphasen einrichten](set-up-service-order-stages.md)

[Ändern der Phase eines Serviceauftrags](change-service-order-stage.md)

  



