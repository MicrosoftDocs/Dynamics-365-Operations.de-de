---
title: Transportverwaltung - Sonstige Kosten
description: In diesem Thema wird erklärt, wie die durch den Transport erzeugten Gebühren mit einem Gebührencode verknüpft werden müssen.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2020
ms.locfileid: "4429173"
---
# <a name="transportation-management-miscellaneous-charges"></a>Transportverwaltung - Sonstige Kosten

[!include [banner](../includes/banner.md)]

Wie alle anderen Gebühren müssen auch die vom Transport erzeugten Gebühren mit einem Gebührencode verknüpft werden. Andernfalls werden sie dem Auftrag nicht als sonstige Kosten hinzugefügt. Der **Gebührencode** bestimmt, wie die Gebühr in Bezug auf den Auftrag und die Auftragszeile, in der sie hinzugefügt wird, verbucht wird.

Gehen Sie zu **Transportverwaltung > Einrichten > Bewertung > Diverse Gebühren**, um die Qualifizierungskriterien zu definieren, die bestimmen, wann ein bestimmter **Gebührencode** auf eine Gebühr angewendet wird.

Sie sollten mindestens eine Einrichtung für jede relevante **Gebührenmodul**-Einstellung (*Kunde* und *Lieferant*) haben, bei der die **Gebührenart Sonstiges** auf *Keine* festgelegt ist. Fehlt diese Angabe, wird die Zusatzgebühr *nicht* zur Bestellung hinzugefügt.
