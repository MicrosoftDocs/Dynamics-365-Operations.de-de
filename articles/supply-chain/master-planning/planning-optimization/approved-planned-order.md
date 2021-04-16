---
title: Bestellvorschläge genehmigen
description: In diesem Thema wird die Genehmigung von Planaufträgen beschrieben, die in der Planungsoptimierung unterstützt werden.
author: ChristianRytt
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 6c215a89403f16336caae5c62cde6df469c4091c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825890"
---
# <a name="approve-planned-orders"></a>Bestellvorschläge genehmigen

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Informationen zum Aktualisieren des Status von Planaufträgen in der Planungsoptimierung.

Beachten Sie, dass die Genehmigung von Planaufträgen ein optionaler Schritt ist, um aus einem Planauftrag einen festen Auftrag zu erstellen. Es wird empfohlen, geänderte Planaufträge zu genehmigen, da sonst die Änderungen beim nächsten Planungslauf ignoriert und überschrieben werden.

![Flow des Bestellvorschlags](media/approved-planned-orders-1.png)

Das **Status**-Feld hilft Ihnen dabei, Ihren Fortschritt anhand der folgenden Werte zu steuern:

- **Offen:** Wenn vom Produktprogrammplanungslauf Bestellvorschläge generiert wurden, weisen die Bestellvorschläge den Status *Offen* auf. Planaufträge mit diesem Status werden beim nächsten Planungslauf gelöscht.
- **Abgeschlossen:** Wenn Sie einen Planauftrag nicht festlegen möchten, können Sie den Status in *Abgeschlossen* ändern , um anzuzeigen, dass Sie die Bewertung dieses geplanten Auftrags abgeschlossen haben. Beachten Sie, dass ein Status von *Offen* und *Abgeschlossen* vom System gleich behandelt wird.
- **Genehmigt:** Wenn Sie Änderungen beibehalten möchten oder eine geplante Bestellung festlegen möchten, ändern Sie den Status in *Genehmigt*. Planaufträge mit dem Status *Genehmigt* gelten als festgelegt und erwarten eine Lieferung von der Produktprogrammplanung, so dass sie bei einer späteren Ausführung der Produktprogrammplanung nicht geändert oder gelöscht werden. Um dies zu erreichen, kopiert die Planungslogik während der Produktplanung die *genehmigten* Planaufträge aus der alten Planversion in die neue Planversion. Beachten Sie, dass *Genehmigte* Planaufträge nur als Lieferung innerhalb der jeweiligen Produktprogrammplanung gelten.

Sie können Bestellvorschläge aus dem Arbeitsbereich **Produktprogrammplanung**, aus der Liste **Bestellvorschlag**, oder aus den Listen **Geplante Produktionsaufträge**, **Geplante Einkaufsbestellungen** und **Geplante Umlagerung** verwalten.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]