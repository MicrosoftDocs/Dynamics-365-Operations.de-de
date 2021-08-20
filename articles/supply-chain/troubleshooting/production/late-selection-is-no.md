---
title: Eine späte Auswahl wird nicht berücksichtigt, wenn Produktionsaufträge über einen Stapelverarbeitungsauftrag zurückgesetzt werden
description: Wenn Sie einen wiederkehrenden Stapelverarbeitungsauftrag verwenden, um den Status eines Produktionsauftrags zurückzusetzen, wird eine späte Auswahl nicht berücksichtigt.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8800ec411ddd7ae73c5ac159592620a07b50c1e87938f823274ec24062c9a71a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741955"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>Eine späte Auswahl wird nicht berücksichtigt, wenn Produktionsaufträge über einen Stapelverarbeitungsauftrag zurückgesetzt werden

KB-Nummer: 4614634

## <a name="symptoms"></a>Symptome

Wenn Sie einen wiederkehrenden Stapelverarbeitungsauftrag verwenden, um den Status eines Produktionsauftrags zurückzusetzen, wird eine späte Auswahl nicht berücksichtigt.

## <a name="resolution"></a>Lösung

Der wird die Verwendung einer späten Auswahl für den Prozess *Status zurücksetzen* nicht unterstützt.
