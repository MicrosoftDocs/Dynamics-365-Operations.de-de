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
ms.openlocfilehash: d039b79684f87e7791fb9dae7cbdc6ced220bc092d9a0ab624616c1c345986da
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756774"
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
