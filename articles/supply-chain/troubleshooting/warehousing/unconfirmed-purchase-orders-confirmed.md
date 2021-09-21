---
title: Produkteingänge aktualisieren bestätigt unbestätigte Bestellungen
description: Nachdem Sie Produkteingänge aktualisieren ausgeführt haben, bestätigt das System unbestätigte Bestellungen mit dem Status Registriert. Erfahren Sie mehr über die Funktion, die dieses Problem behebt.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476409"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>Unbestätigte Bestellungen werden nach dem Ausführen von „Produktzugänge aktualisieren“ bestätigt

## <a name="symptoms"></a>Symptome

Nachdem Sie die periodische Aufgabe *Produkteingänge aktualisieren* ausgeführt haben, bestätigt das System automatisch unbestätigte Einkaufsbestellungen, die einen Bestandstransaktionsstatus von *Registriert* haben.

## <a name="resolution"></a>Lösung

Eine neue Funktion zur Behandlung eingehender Ladungen, *Übernahme von Ladungsmengen*, behebt dieses Problem. Um diese Funktion einzuschalten, gehen Sie zum Arbeitsbereich [Funktionsverwaltung](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) und schalten Sie die folgenden Funktionen in der Reihenfolge, in der sie aufgelistet sind, ein:

1. Zuordnung von Bestellbestandsbuchungen zur Ladung
2. Zu hoher Zugang bei Auslastungsmengen

Weitere Informationen finden Sie unter [Registrierte Produktmengen gegen Einkaufsbestellungen verbuchen](/dynamics365/supply-chain/warehousing/inbound-load-handling).
