---
title: Element kann keine Stückliste oder Formel haben
description: Wenn Sie versuchen, einen Auftrag zu fixieren, erhalten Sie während der Positionsvalidierung eine Fehlermeldung. Sie besagt, dass das Element keine Stückliste oder Formel haben kann.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1e946adc3a04db60bf15ac7bb44163085e1c19802872964877d3929b1f79bf7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730105"
---
# <a name="item-cant-have-a-bom-or-formula"></a>Element kann keine Stückliste oder Formel haben

Fehlercode: PRO2614

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, einen Auftrag zu fixieren, erhalten Sie während der Positionsvalidierung die folgende Fehlermeldung:

> Element kann keine Stückliste oder Formel haben

## <a name="resolution"></a>Lösung

Elemente, die eine Stückliste oder eine Formel haben, müssen vom Typ *Planungselement*, *Stückliste* oder *Formel* sein. Um den Typ eines Elements zu ändern, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Öffnen Sie das entsprechende Produkt.
1. Legen Sie auf dem Inforegister **Ingenieur** das Feld **Produktionstyp** auf *Planungselement*, *Stückliste* oder *Formel* fest.
