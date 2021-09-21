---
title: Laufende Einzelvorgänge werden beendet, wenn eine Teilmenge des letzten Einzelvorgangs gemeldet wird.
description: Wenn das Jobkartengerät verwendet wird, um eine Teilmenge für den letzten Auftrag in einem Produktionsauftrag zu melden, werden alle vorherigen Einzelvorgänge mit dem Status „In Bearbeitung“ beendet.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 11511d4ac7524facdd0d647e9bc38fe09c282be1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476486"
---
# <a name="previous-in-progress-jobs-are-ended-when-reporting-partial-quantity-on-last-job"></a>Vorherige laufende Einzelvorgänge werden beendet, wenn eine Teilmenge des letzten Einzelvorgangs gemeldet wird.

## <a name="symptoms"></a>Symptome

Wenn das Jobkartengerät verwendet wird, um eine Teilmenge für den letzten Auftrag in einem Produktionsauftrag zu melden, werden alle vorherigen Einzelvorgänge in diesem Auftrag mit dem Status „In Bearbeitung“ automatisch beendet.

## <a name="resolution"></a>Lösung

Dieses Verhalten ist beabsichtigt. Auf der Seite **Produktionsauftragsstandards** gibt es auf der Registerkarte **Als beendet melden** die Option **Arbeitsplan beenden**. Wenn dieses Thema auf *Ja* festgelegt ist, wird eine Erfassung für den Arbeitsplan erstellt, wenn eine Arbeitskraft das Jobkartengerät oder das Jobkartenterminal verwendet, um den letzten Vorgang zu melden. Diese Erfassung kennzeichnet alle Vorgänge als abgeschlossen und beendet alle Produktionsaufträge. Wenn die Option **Arbeitsplan beenden** auf *Ja* festgelegt ist, berücksichtigt das System nicht den Status des Einzelvorgangs, den die Arbeitskraft ausgewählt hat, als sie den letzten Vorgang meldete. Das System berücksichtigt auch nicht, ob die Arbeitskraft eine volle oder eine Teilmenge meldet.
