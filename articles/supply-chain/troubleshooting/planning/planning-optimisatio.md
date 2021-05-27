---
title: Die geplante Einkaufsbestellung wird erstellt, wenn ein Kauf innerhalb negativer Tage vorliegt
description: Wenn das Dispositionsverfahren Min/Max lautet, erstellt die Planungsoptimierung eine geplante Einkaufsbestellung, wenn ein Kauf innerhalb negativer Tage vorliegt.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026547"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Die geplante Einkaufsbestellung wird erstellt, wenn ein Kauf innerhalb negativer Tage vorliegt

KB-Nummer: 4614298

## <a name="symptoms"></a>Symptome

Wenn das Dispositionsverfahren *Min/Max* lautet, erstellt die Planungsoptimierung eine geplante Einkaufsbestellung, wenn ein Kauf innerhalb negativer Tage vorliegt.

## <a name="resolution"></a>Lösung

Die Planungsoptimierung unterstützt negative Tage nicht. Es wird jedoch immer sichergestellt, dass geplante Bestellungen nicht innerhalb der Vorlaufzeit im Verhältnis zum aktuellen Datum geplant werden. Beispielsweise beträgt die Vorlaufzeit für den Kauf 10 Tage, und eine Bestellung wird voraussichtlich in acht Tagen ab heute eintreffen. In diesem Fall wird die Bestellung als Angebot für die Nachfrage verwendet, die fünf Tage ab heute liegt.

Wir empfehlen daher, dass Sie Ihre Vorlaufzeiten anpassen, um alle (oder fast alle) Ihrer Szenarien abzudecken.
