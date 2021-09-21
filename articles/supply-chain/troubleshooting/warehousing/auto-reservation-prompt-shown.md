---
title: Die automatische Reservierungsaufforderung wird mit verfügbarem Bestand angezeigt.
description: Wenn Sie einen Artikel in einem Lagerort verwenden, in dem Lagerortprozesse nicht aktiviert sind, wird die Eingabeaufforderung für die automatische Reservierung angezeigt. Geben Sie alle Dimensionen über dem Lagerplatz an.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a15502ce8c5bc61d37cedd746985176408a2f362
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476481"
---
# <a name="auto-reservation-prompt-for-batch-number-is-shown-even-with-available-inventory"></a>Die automatische Reservierungsaufforderung für die Chargennummer wird selbst mit verfügbarem Bestand angezeigt.

## <a name="symptoms"></a>Symptome

Wenn Sie einen Artikel mit einer Reservierungshierarchie *Charge oberhalb* in einem Lagerort verwenden, in dem Lagerortprozesse nicht aktiviert wurde und die automatische Reservierung aktiviert ist, wird die automatische Reservierungsaufforderung für eine Chargennummer angezeigt, auch wenn nur eine Charge zur Entnahme verfügbar ist.

Wenn Sie jedoch denselben Artikel in einem Lagerort verwenden, in dem Lagerortprozesse aktiviert sind, wird die Eingabeaufforderung für die automatische Reservierung nicht angezeigt.

## <a name="resolution"></a>Lösung

Wenn eine Reservierungshierarchie als *Charge oberhalb* oder *Serie oberhalb* definiert ist, müssen die referenzierte Dimension (**Chargennummer** oder **Seriennummer**) immer auf Bedarfsaufträgen angegeben werden. Lagerortprozesse können die Informationen möglicherweise vervollständigen, wenn eine einzelne Chargen- oder Seriennummer verfügbar ist. Da der Lagerort jedoch nicht für Lagerortprozesse aktiviert ist, muss der Benutzer immer alle oben genannten Dimensionen oberhalb von **Lagerplatz** angeben.
