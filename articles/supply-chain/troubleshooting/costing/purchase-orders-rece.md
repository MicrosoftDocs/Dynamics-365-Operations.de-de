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
ms.openlocfilehash: 49faa2c68d496c5c0d8c7e4abfd93d9a917857220dd23c09a050fa3436e1d49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746866"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a>Physisch eingegangene Bestellungen werden nicht im Bestandsabschlussbericht angezeigt

KB-Nummer: 4612595

## <a name="symptoms"></a>Symptome

Physisch eingegangene Bestellungen werden nicht im Bestandsabschlussbericht **Prüfen auf offene Mengen** angezeigt.

## <a name="resolution"></a>Lösung

Der Bericht **Prüfen auf offene Mengen** zeigt Abgangsbuchung an, die zum ausgewählten Abschlussdatum nicht mit finanziell aktualisierten Bestandsbelegen abgerechnet werden können. Sie können festlegen, dass physische Belege in den Bericht aufgenommen werden. In diesem Fall werden physische Belege angezeigt, wenn sie die nicht abwickelbaren Abgangsbuchung abdecken können. Weitere Informationen finden Sie unter [Vorbereiten des Bestandsabschlusses](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).
