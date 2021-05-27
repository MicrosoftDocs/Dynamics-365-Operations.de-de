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
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a><span data-ttu-id="31db7-103">Eine späte Auswahl wird nicht berücksichtigt, wenn Produktionsaufträge über einen Stapelverarbeitungsauftrag zurückgesetzt werden</span><span class="sxs-lookup"><span data-stu-id="31db7-103">Late selection isn't respected when production orders are reset via a batch job</span></span>

<span data-ttu-id="31db7-104">KB-Nummer: 4614634</span><span class="sxs-lookup"><span data-stu-id="31db7-104">KB number: 4614634</span></span>

## <a name="symptoms"></a><span data-ttu-id="31db7-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="31db7-105">Symptoms</span></span>

<span data-ttu-id="31db7-106">Wenn Sie einen wiederkehrenden Stapelverarbeitungsauftrag verwenden, um den Status eines Produktionsauftrags zurückzusetzen, wird eine späte Auswahl nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="31db7-106">When you use a recurring batch job to reset the status of a production order, late selections aren't respected.</span></span>

## <a name="resolution"></a><span data-ttu-id="31db7-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="31db7-107">Resolution</span></span>

<span data-ttu-id="31db7-108">Der wird die Verwendung einer späten Auswahl für den Prozess *Status zurücksetzen* nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="31db7-108">The current design doesn't support the use of late selections for the *Reset status* process.</span></span>
