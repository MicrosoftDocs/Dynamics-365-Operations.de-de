---
title: Physisch eingegangene Bestellungen werden nicht im Bestandsabschlussbericht angezeigt
description: Physisch eingegangene Bestellungen werden nicht im Bestandsabschlussbericht „Prüfen auf offene Mengen“ angezeigt.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026541"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a>Physisch eingegangene Bestellungen werden nicht im Bestandsabschlussbericht angezeigt

KB-Nummer: 4612595

## <a name="symptoms"></a>Symptome

Physisch eingegangene Bestellungen werden nicht im Bestandsabschlussbericht **Prüfen auf offene Mengen** angezeigt.

## <a name="resolution"></a>Lösung

Der Bericht **Prüfen auf offene Mengen** zeigt Abgangsbuchung an, die zum ausgewählten Abschlussdatum nicht mit finanziell aktualisierten Bestandsbelegen abgerechnet werden können. Sie können festlegen, dass physische Belege in den Bericht aufgenommen werden. In diesem Fall werden physische Belege angezeigt, wenn sie die nicht abwickelbaren Abgangsbuchung abdecken können. Weitere Informationen finden Sie unter [Vorbereiten des Bestandsabschlusses](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).
