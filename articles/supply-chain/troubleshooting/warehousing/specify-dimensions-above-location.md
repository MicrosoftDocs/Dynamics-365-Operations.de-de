---
title: Eine Ladung kann für eine Teilmenge mit Charge oberhalb der Reservierungshierarchie nicht freigegeben werden
description: Bei Verwendung eines Artikels mit der Reservierungshierarchie Charge oberhalb müssen die Ladezeilen- Dimensionen über dem Lagerplatz angeben, damit der Lagerbestand zugeordnet werden kann.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476419"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>Eine Ladung kann für eine Teilmenge mit „Charge oberhalb“ der Reservierungshierarchie nicht freigegeben werden

## <a name="symptoms"></a>Symptome

Wenn Sie einen Artikel verwenden, der eine Reservierungshierarchie *Charge oberhalb* hat, funktioniert der Befehl **An Lager freigeben** auf der Seite **Ladungsplanungs-Workbench** nicht, wenn Sie eine Ladung für eine Teilmenge freigeben möchten. Sie erhalten die folgende Fehlermeldung:

> Um einer Welle zugewiesen zu werden, müssen Ladungszeilen die Dimensionen oberhalb des Lagerplatzes angeben werden. Um diese Dimensionen zuzuweisen, reservieren Sie und erstellen Sie die Ladelinie neu.

Wenn Sie jedoch einen Artikel verwenden, das eine Reservierungshierarchie *Charge unterhalb* hat, können Sie auf der Seite **Ladungsplanungs-Workbench** für eine Teilmenge eine Ladung freigeben.

## <a name="cause"></a>Ursache

Wenn in der Reservierungshierarchie eine Dimension oberhalb der Dimension **Lagerplatz** vorhanden ist, muss diese vor der Freigabe zum Lagerort angegeben werden. Der Bestand kann nur dann erfolgreich zugeteilt werden, wenn in den Dimensionen oberhalb des Lagerplatzes keine Lücken vorhanden sind.

## <a name="resolution"></a>Lösung

Stellen Sie sicher, dass alle Dimensionen über dem **Standort** durch Reservieren und Neuerstellen der Lastlinie zugewiesen wurden.
