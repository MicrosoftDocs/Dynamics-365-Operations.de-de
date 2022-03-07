---
title: Parameter für den Masterplan sind nicht vorhanden
description: Wenn Sie versuchen, einen geplanter Auftrag zu fixieren, erhalten Sie eine Fehlermeldung, die besagt, dass keine Parameter für den Masterplan vorhanden sind.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294085"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a>Parameter für den Masterplan sind nicht vorhanden

Fehlercode: SYS25368

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, einen geplanten Auftrag zu fixieren, erhalten Sie die folgende Fehlermeldung:

> Parameter für Produktprogrammplan '%1' sind nicht vorhanden.

## <a name="cause"></a>Ursache

Aufgrund von Konfigurationsproblemen kann das System die Einstellungen für den angegebenen Plan nicht finden.

## <a name="resolution"></a>Lösung

- Gehen Sie zu **Produktprogrammplanung \> Einrichten \> Pläne \> Masterpläne**, und stellen Sie sicher, dass ein Plan mit dem angegebenen Namen vorhanden ist.
