---
title: Die Produktprogrammplanung generiert geplante Aufträge für Phantomprodukte
description: Nach Durchführung der Produktprogrammplanung werden geplante Aufträge für Phantomprodukte generiert.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026548"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Die Produktprogrammplanung generiert geplante Aufträge für Phantomprodukte

KB-Nummer: 4614729

## <a name="symptoms"></a>Symptome

Nach Durchführung der Produktprogrammplanung werden geplante Aufträge für Phantomprodukte generiert.

## <a name="resolution"></a>Lösung

Die Einstellung der Option **Phantom** für freigegebene Produkte bestimmt den standardmäßigen Positionstyp in der Stückliste. Wenn die Option **Phantom** auf *Ja* gesetzt ist, erstellt das System weiterhin geplante Aufträge für den Artikel, aber die Option **Direkt abgeleitete Anforderung** wird für jeden geplanten Auftrag auf *Ja* gesetzt. Daher kann der geplante Produktionsauftrag nicht allein umgewandelt werden. Stattdessen wird er immer automatisch aufgenommen, wenn der übergeordnete Produktionsauftrag bestätigt wird. Zusätzlich werden die Stücklistenpositionen des geplanten Phantomauftrags in die Stückliste des übergeordneten Produktionsauftrags aufgenommen.
