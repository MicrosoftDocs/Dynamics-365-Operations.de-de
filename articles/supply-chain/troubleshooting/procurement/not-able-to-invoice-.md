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
ms.openlocfilehash: 30c485be79be5ebbec8b51272b8bbe6e0c7df9d81bbaaaef316dbfede03abf68
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756750"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Sie können einen Kundenauftrag nicht in Rechnung stellen

KB-Nummer: 4611793

## <a name="symptoms"></a>Symptome

Sie können den ursprünglichen Kundenauftrag und die ursprüngliche Direktlieferungsbestellung nicht mehr in Rechnung stellen, nachdem Sie die Option **Rechnung automatisch buchen** auf der Seite **Intercompany** für einen Kreditor aktiviert haben.

## <a name="resolution"></a>Lösung

Das Synchronisationsverhalten für Intercompany- und Direktlieferungsbestellungs-Rechnungen wird durch die in [Einrichten von Parametern zum Buchen eines Intercompany-Auftrags](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order) beschriebenen Parameter gesteuert und erzwungen.

Nachdem Sie diese Parameter festgelegt haben, müssen Sie zuerst den Intercompany-Auftrag in Rechnung stellen. Die ursprünglichen Aufträge und Bestellungen werden dann synchronisiert.
