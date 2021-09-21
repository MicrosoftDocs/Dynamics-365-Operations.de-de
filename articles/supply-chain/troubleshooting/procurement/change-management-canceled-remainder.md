---
title: Das Stornieren der Restliefermenge versetzt die Bestellung in den Status „Bestätigt“.
description: Wenn eine Restliefermenge für eine Bestellung storniert wird, für die das Änderungsmanagement aktiviert ist, wechselt die Bestellung in den Status „Bestätigt“.
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
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476456"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>Das Stornieren der Restliefermenge versetzt die Bestellung in den Status „Bestätigt“.

## <a name="symptoms"></a>Symptome

Bei einer Bestellung, die dem Änderungsmanagement unterliegt, wird die Bestellung, wenn die einzige angeforderte Änderung die Stornierung einer verbleibenden Liefermenge bei einer oder mehreren Positionen ist, direkt an den Zustand *Bestätigt* weitergeleitet, wann sie genehmigt wurde, und es wird kein Journal erstellt.

## <a name="resolution"></a>Lösung

Die Stornierung einer verbleibenden Liefermenge hat keine Auswirkungen auf den Inhalt des Bestätigungsjournals. Diese Funktionalität sollte verwendet werden, wenn die Position teilweise zugegangen ist, und die verbleibende Liefermenge sollte im Prozessschritt storniert werden, nachdem die Bestellung beim Lieferanten bestätigt wurde.

Sollte dies in der Bestellbestätigung berücksichtigt werden, sollte die Menge in der Bestellposition angepasst werden, sodass die Bestätigung erforderlich ist. Wenn alternativ nichts in der Position empfangen wurde, kann die Menge entfernt werden. In diesem Fall ist eine erneute Bestätigung erforderlich.
