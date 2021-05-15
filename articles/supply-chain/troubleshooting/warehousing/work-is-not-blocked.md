---
title: Arbeit ist nicht blockiert
description: Arbeit ist nicht blockiert
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924203"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="d8f1f-103">Arbeit ist nicht blockiert</span><span class="sxs-lookup"><span data-stu-id="d8f1f-103">Work isn't blocked</span></span>

<span data-ttu-id="d8f1f-104">Fehlercode: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="d8f1f-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="d8f1f-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="d8f1f-105">Symptoms</span></span>

<span data-ttu-id="d8f1f-106">Das System zeigt die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="d8f1f-106">The system shows the following error message:</span></span>

> <span data-ttu-id="d8f1f-107">Arbeit mit Id %1 ist nicht blockiert.</span><span class="sxs-lookup"><span data-stu-id="d8f1f-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="d8f1f-108">Ursache</span><span class="sxs-lookup"><span data-stu-id="d8f1f-108">Cause</span></span>

<span data-ttu-id="d8f1f-109">Die Option **Blockierte Welle** auf der Welle wird auf *Nein* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d8f1f-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="d8f1f-110">Die Arbeit kann nicht entsperrt werden, da sie derzeit nicht gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="d8f1f-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="d8f1f-111">Lösung</span><span class="sxs-lookup"><span data-stu-id="d8f1f-111">Resolution</span></span>

 <span data-ttu-id="d8f1f-112">Nur Arbeiten, bei denen die Option **Blockierte Welle** auf *Ja* festgelegt ist, können entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="d8f1f-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
