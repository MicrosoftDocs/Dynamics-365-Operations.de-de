---
title: Ein Bestellungsbeleg enthält nicht alle Gebühren
description: Ein Bestellungsbeleg enthält nicht alle Gebühren
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
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476402"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Ein Bestellungsbeleg enthält nicht alle Gebühren

## <a name="symptoms"></a>Symptome

Wenn Sie eine Bestellung erhalten, sind nicht alle Gebühren in der Quittung enthalten.

### <a name="reproduce-the-issue"></a>Reproduzieren Sie das Problem

Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.

1. Stellen Sie auf der **Beschaffungs- und Ursprungsparameter**-Seite auf der Registerkarte **Lieferung** sicher, dass die **Auf Produktbeleg Gebühren generieren**-Option auf *Ja* festgelegt ist.
1. Erstellen einer Bestellung, die Gebühren enthält.
1. Bestätigen Sie die Bestellung.
1. Erhalten Sie die Bestellung.
1. Sehen Sie sich die Quittungssumme an und vergleichen Sie sie mit der erwarteten Gesamtsumme.
1. Beachten Sie, dass nicht alle Gebühren auf dem Bestellbeleg enthalten sind.

## <a name="resolution"></a>Lösung

Die Auflösung hängt davon ab, wie die verschiedenen Gebühren eingerichtet wurden. Informationen zum Einrichten verschiedener Gebühren zur Erfüllung Ihrer Anforderungen finden Sie im folgenden Blogbeitrag: [Sonstiges Gebühren zum Zeitpunkt des Produkteingangs buchen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
