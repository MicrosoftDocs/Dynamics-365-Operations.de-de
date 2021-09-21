---
title: Sie können nicht mehrere Produktzugänge in einer einzigen Bestellung zusammenfassen.
description: Sie können nicht mehrere Produktzugänge in einer Bestellung zusammenfassen, wenn die verschiedenen Produktzugangspositionen unterschiedliche Abrechnungsdaten haben.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476413"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Sie können nicht mehrere Produktzugänge in einer einzigen Bestellung zusammenfassen.

## <a name="symptoms"></a>Symptome

Sie können nicht mehrere Produktzugänge in einer Bestellung zusammenfassen, wenn die verschiedenen Produktzugangspositionen unterschiedliche Abrechnungsdaten haben.

## <a name="resolution"></a>Lösung

In früheren Versionen von Dynamics 365 Supply Chain Management war in dieser Situation eine Konsolidierung zulässig. Die Praxis ist jedoch fehleranfällig. Das Abrechnungsdatum in den erstellten Bestellpositionen sollte nicht vom Abrechnungsdatum in den Produktzugangspositionen abweichen, aus denen diese Bestellpositionen erstellt wurden. (Das Abrechnungsdatum in den Bestellpositionen stimmt mit dem Abrechnungsdatum im Bestellkopf überein.) Daher ist die Konsolidierung mehrerer Produkteingänge zu einer einzigen Bestellung nicht mehr zulässig.

Das Abrechnungsdatum wird beispielsweise für Budgetreservierungen und Belastungen verwendet. Daher sollte es beim Übergang vom Produktzugang zur Bestellung beibehalten werden.
