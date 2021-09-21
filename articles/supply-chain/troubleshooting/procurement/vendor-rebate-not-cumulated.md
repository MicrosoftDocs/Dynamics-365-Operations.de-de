---
title: Ein Lieferantenrabatt wird nicht auf der Grundlage von Rechnungen kumuliert
description: Ein Lieferantenrabatt wird nicht auf der Grundlage von Rechnungen kumuliert
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 9d4596a7351969bf181982a24ea1dcc6f5732831
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476487"
---
# <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Ein Lieferantenrabatt wird nicht auf der Grundlage von Rechnungen kumuliert

## <a name="symptoms"></a>Symptome

Wenn gebuchte Rechnungen unterschiedliche Fälligkeitstermine haben, werden diese Rechnungen nicht in Lieferantenrabatten berücksichtigt, die daraus generiert werden.

## <a name="resolution"></a>Lösung

Das Fälligkeitsdatum wird bei der Berechnung des Lieferantenrabattes nicht berücksichtigt. Ziehen Sie in Betracht, das System so anzupassen, dass das Fälligkeitsdatum und die Beziehung zur Rechnung in Bezug auf den tatsächlichen Lieferantenrabatt deutlicher werden.
