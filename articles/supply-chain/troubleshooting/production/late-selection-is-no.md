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
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026535"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>Eine späte Auswahl wird nicht berücksichtigt, wenn Produktionsaufträge über einen Stapelverarbeitungsauftrag zurückgesetzt werden

KB-Nummer: 4614634

## <a name="symptoms"></a>Symptome

Wenn Sie einen wiederkehrenden Stapelverarbeitungsauftrag verwenden, um den Status eines Produktionsauftrags zurückzusetzen, wird eine späte Auswahl nicht berücksichtigt.

## <a name="resolution"></a>Lösung

Der wird die Verwendung einer späten Auswahl für den Prozess *Status zurücksetzen* nicht unterstützt.
