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
ms.openlocfilehash: f3170bcb723e2d7483258bb0ecf786e62f2aa3d196745074c2ac554bc212ec55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742003"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Die Produktprogrammplanung generiert geplante Aufträge für Phantomprodukte

KB-Nummer: 4614729

## <a name="symptoms"></a>Symptome

Nach Durchführung der Produktprogrammplanung werden geplante Aufträge für Phantomprodukte generiert.

## <a name="resolution"></a>Lösung

Die Einstellung der Option **Phantom** für freigegebene Produkte bestimmt den standardmäßigen Positionstyp in der Stückliste. Wenn die Option **Phantom** auf *Ja* gesetzt ist, erstellt das System weiterhin geplante Aufträge für den Artikel, aber die Option **Direkt abgeleitete Anforderung** wird für jeden geplanten Auftrag auf *Ja* gesetzt. Daher kann der geplante Produktionsauftrag nicht allein umgewandelt werden. Stattdessen wird er immer automatisch aufgenommen, wenn der übergeordnete Produktionsauftrag bestätigt wird. Zusätzlich werden die Stücklistenpositionen des geplanten Phantomauftrags in die Stückliste des übergeordneten Produktionsauftrags aufgenommen.
