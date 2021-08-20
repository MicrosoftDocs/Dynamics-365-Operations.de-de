---
title: Transportverwaltung - Sonstige Kosten
description: In diesem Thema wird erklärt, wie die durch den Transport erzeugten Gebühren mit einem Gebührencode verknüpft werden müssen.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6d334a1ac290ab258964df2f146d9cbe30eb766f4002c8bae856cbe5499181b3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769514"
---
# <a name="transportation-management-miscellaneous-charges"></a>Transportverwaltung - Sonstige Kosten

[!include [banner](../includes/banner.md)]

Wie alle anderen Gebühren müssen auch die vom Transport erzeugten Gebühren mit einem Gebührencode verknüpft werden. Andernfalls werden sie dem Auftrag nicht als sonstige Kosten hinzugefügt. Der **Gebührencode** bestimmt, wie die Gebühr in Bezug auf den Auftrag und die Auftragszeile, in der sie hinzugefügt wird, verbucht wird.

Gehen Sie zu **Transportverwaltung > Einrichten > Bewertung > Diverse Gebühren**, um die Qualifizierungskriterien zu definieren, die bestimmen, wann ein bestimmter **Gebührencode** auf eine Gebühr angewendet wird.

Sie sollten mindestens eine Einrichtung für jede relevante **Gebührenmodul**-Einstellung (*Kunde* und *Lieferant*) haben, bei der die **Gebührenart Sonstiges** auf *Keine* festgelegt ist. Fehlt diese Angabe, wird die Zusatzgebühr *nicht* zur Bestellung hinzugefügt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]