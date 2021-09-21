---
title: Es ist ein Fehler bei der Gesamtgutmenge beim Versuch aufgetreten, einen Aauftrag zu beenden
description: Wenn Sie versuchen, einen Produktionsauftrag zu beenden und als abgeschlossen zu melden, erhalten Sie möglicherweise einen Fehler für die Gesamtwarenmenge. Auf dieser Seite wird erklärt, warum und wie das Problem behoben werden kann.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5f0c2c2ca64ada9d72c0ebd04e7de561aaa52039
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476434"
---
# <a name="total-good-quantity-error-when-trying-to-end-a-production-order"></a>Es ist ein Fehler bei der Gesamtgutmenge beim Versuch aufgetreten, einen Produktionsauftrag zu beenden

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, einen Bericht als fertiggestellte Erfassung auf einen Produktionsauftrag zu buchen, erhalten Sie die folgende Fehlermeldung:

> Gesamte als fertig gemeldete Gutmenge für die Produktion wird %1 sein. Die Rückmeldung für den letzten Vorgang ist insgesamt 0,00.

## <a name="cause"></a>Ursache

Dieses Problem tritt auf, wenn die Mengen, die in den letzten Vorgängen gebucht wurden, falsch waren. Wenn z.B. die Produktion gestartet wird, aber die Menge, die gestartet werden muss, nicht zugeordnet ist, wird die Arbeitsplan-Erfassung ohne Zeilen gebucht. Um die Situation zu bestätigen, öffnen Sie den Produktionsauftrag, und wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Ansicht** die Option **Arbeitsplan**.

## <a name="resolution"></a>Lösung

Sie können dieses Problem beheben, indem Sie zusätzliche Erfassungen für die Vorgänge buchen, für die die Erfassungen nicht korrekt gebucht wurden. Starten Sie den Produktionsauftrag neu und wählen Sie, um die zusätzlichen Erfassungen zu buchen. Durch diese Aktion wird der Produktionsauftrag nicht gestartet, aber die Erfassungen werden gebucht. Der Arbeitsplan sollte dann die gebuchten Mengen anzeigen, und Sie sollten die Produktionsaufträge erfolgreich beenden können.
