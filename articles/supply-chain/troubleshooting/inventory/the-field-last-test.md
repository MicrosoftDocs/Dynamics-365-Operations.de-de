---
title: Das Feld „Datum des letzten Tests“ wird nicht aktualisiert, wenn mehrere Qualitätsprüfungsaufträge erstellt werden
description: Das Feld „Datum des letzten Tests“ wird nicht aktualisiert, wenn mehrere Qualitätsprüfungsaufträge erstellt werden.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026552"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="88ce9-103">Das Feld „Datum des letzten Tests“ wird nicht aktualisiert, wenn mehrere Qualitätsprüfungsaufträge erstellt werden</span><span class="sxs-lookup"><span data-stu-id="88ce9-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="88ce9-104">KB-Nummer: 4612803</span><span class="sxs-lookup"><span data-stu-id="88ce9-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="88ce9-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="88ce9-105">Symptoms</span></span>

<span data-ttu-id="88ce9-106">Das Feld **Datum des letzten Tests** wird nicht aktualisiert, wenn mehrere Qualitätsprüfungsaufträge erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="88ce9-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="88ce9-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="88ce9-107">Resolution</span></span>

<span data-ttu-id="88ce9-108">Das System verhält sich wie vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="88ce9-108">The system is behaving as designed.</span></span> <span data-ttu-id="88ce9-109">Das Datum des letzten Tests bezieht sich nicht auf Qualitätsprüfungsaufträge.</span><span class="sxs-lookup"><span data-stu-id="88ce9-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="88ce9-110">Es speichert das Datum, an dem die Fertigartikel zum ersten Mal gekauft oder hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="88ce9-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="88ce9-111">Dieses Datum wird verwendet, um das Haltbarkeitsdatum zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="88ce9-111">This date is used to calculate the shelf life advice date.</span></span>
