---
title: Sie können einen Kundenauftrag nicht in Rechnung stellen
description: Sie können den ursprünglichen Kundenauftrag und die ursprüngliche Direktlieferungsbestellung nicht mehr in Rechnung stellen, nachdem Sie die Option „Rechnung automatisch buchen“ aktiviert haben.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026537"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Sie können einen Kundenauftrag nicht in Rechnung stellen

KB-Nummer: 4611793

## <a name="symptoms"></a>Symptome

Sie können den ursprünglichen Kundenauftrag und die ursprüngliche Direktlieferungsbestellung nicht mehr in Rechnung stellen, nachdem Sie die Option **Rechnung automatisch buchen** auf der Seite **Intercompany** für einen Kreditor aktiviert haben.

## <a name="resolution"></a>Lösung

Das Synchronisationsverhalten für Intercompany- und Direktlieferungsbestellungs-Rechnungen wird durch die in [Einrichten von Parametern zum Buchen eines Intercompany-Auftrags](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order) beschriebenen Parameter gesteuert und erzwungen.

Nachdem Sie diese Parameter festgelegt haben, müssen Sie zuerst den Intercompany-Auftrag in Rechnung stellen. Die ursprünglichen Aufträge und Bestellungen werden dann synchronisiert.
