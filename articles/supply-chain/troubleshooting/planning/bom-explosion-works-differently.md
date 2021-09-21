---
title: Stücklistenauflösung verhält sich für umgewandelte und vorkalkulierte Produktionsaufträge unterschiedlich
description: Die Stücklistenauflösung verhält sich für umgewandelte Produktionsaufträge und für vorkalkulierte Produktionsaufträge für manuell erstellte Arbeiten unterschiedlich.
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476441"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>Stücklistenauflösung verhält sich für umgewandelte und vorkalkulierte Produktionsaufträge unterschiedlich

## <a name="symptoms"></a>Symptome

Wenn ein Produktionsauftrag umgewandelt ist, werden die Elemente nicht aufgelöst, wenn Sie die Stückliste auflösen. Wenn Sie jedoch einen Arbeitsauftrag manuell erstellen und dann den Produktionsauftrag schätzen, werden die Elemente aufgelöst.

### <a name="resolution"></a>Lösung

Die Auflösung, die erfolgt, wenn der Produktionsauftrag umgewandelt wird, zeigt auf den Planauftrag, aber es scheint nicht so, als ob der Planauftrag in diesem Fall aktuell umgewandelt ist. Wenn der Produktionsauftrag jedoch geschätzt wurde, wird die Auflösung vom freigegebenen Produktionsauftrag ausgelöst, wenn kein Planauftrag vorhanden ist.
