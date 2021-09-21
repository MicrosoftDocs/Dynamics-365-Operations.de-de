---
title: Die Einkaufsvertrags-Höchstgrenze gilt nicht für eine Bestellanforderung
description: Die Einkaufsvertrags-Höchstgrenze gilt nicht für eine Bestellanforderung
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
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476422"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>Die Einkaufsvertrags-Höchstgrenze gilt nicht für eine Bestellanforderung

## <a name="symptoms"></a>Symptome

Wenn eine Bestellanforderung mit einem Kaufvertrag verknüpft ist, gilt das maximale Limit aus dem Kaufvertrag nicht für die Bestellanforderung. Die Standardpreisinformationen werden korrekt eingegeben, es kann jedoch mehr als das maximale Limit aus dem Kaufvertrag in der Bestellanforderung bestellt werden.

## <a name="resolution"></a>Lösung

Dieses Verhalten wird erwartet. Da Anforderungen nicht immer genehmigt werden, sollte eine Menge oder ein Betrag nicht im Kaufvertrag reserviert werden. Daher werden Sie das Höchstlimit aus dem Kaufvertrag nicht erreichen.
