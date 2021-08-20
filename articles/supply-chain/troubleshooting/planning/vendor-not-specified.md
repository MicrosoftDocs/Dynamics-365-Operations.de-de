---
title: Kreditor wird beim Fixieren geplanter Aufträge nicht angegeben
description: Wenn Sie versuchen, geplante Aufträge zu fixieren, erhalten Sie eine Fehlermeldung, die besagt, dass kein Kreditor angegeben ist.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4d523d57a862f67fcd40edd60a0fabf40ea7dabcf058f2d11af1fe003c9e304b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741979"
---
# <a name="vendor-isnt-specified-when-planned-orders-are-firmed"></a>Kreditor wird beim Fixieren geplanter Aufträge nicht angegeben

Fehlercode: SYS23532

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, geplante Aufträge zu fixieren, erhalten Sie die folgende Fehlermeldung:

> Lieferant ist nicht angegeben

## <a name="resolution"></a>Lösung

Gehen Sie folgendermaßen vor, um einen Kreditor anzugeben.

1. Öffnen Sie den geplanter Auftrag, in dem ein Kreditor fehlt.
1. Wählen Sie auf dem Inforegister **Geplanter Vorrat** im Feld **Lieferant** einen Kreditor aus.
