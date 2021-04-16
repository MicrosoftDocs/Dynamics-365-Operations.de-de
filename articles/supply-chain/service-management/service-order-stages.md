---
title: Serviceauftragsphasen
description: Wenn Sie die Phasen für einen Serviceauftrag definieren und diese den Arbeitskräften zuweisen, können Sie den Ablauf eines Serviceauftrags durch die Aufgaben steuern, die verschiedene Personen in der Serviceorganisation ausführen.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c46d4bb43c8f59a0ef55963ac9b453491a6112b0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817508"
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

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]