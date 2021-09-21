---
title: Die Menge ist für Einheit %1 nicht gültig, wenn eine aufgeteilte Entnahme durchgeführt wird.
description: Wenn Sie eine aufgeteilte Entnahme über mehrere Chargen hinweg durchführen, erhalten Sie möglicherweise eine Fehlermeldung, dass die Menge für Einheit %1 nicht gültig ist. Diese Seite hilft, dieses Problem zu lösen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4627db7400d6ccd81f25f100de4696058ce35c42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476401"
---
# <a name="quantity-is-not-valid-when-performing-a-split-pick-across-multiple-batches"></a>Die Menge ist nicht gültig, wenn Sie eine aufgeteilte Entnahme über mehrere Chargen hinweg durchführen.

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, eine *aufgeteilte Entnahme* über mehrere Chargen hinweg durchzuführen, erhalten Sie folgende Fehlermeldung:

> Die Menge ist für Einheit %1 ungültig.

## <a name="resolution"></a>Lösung

Die Arbeitskraft im Lager muss den Prozess *Kurzes Entnehmen* in der Warehouse Management Mobile App verwenden. Wenn Sie versuchen, mehrere Chargen vom selben Lagerplatz zu entnehmen, können Sie auch die Option **Voll** in der Warehouse Management Mobile App verwenden.
