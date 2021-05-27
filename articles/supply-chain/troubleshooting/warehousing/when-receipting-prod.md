---
title: Auf einem Beleg wird nur eine Beschriftung für mehrere Arbeitsköpfe gedruckt
description: Auf einem Beleg wird nur eine Beschriftung für mehrere Arbeitsköpfe gedruckt.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026540"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="df0be-103">Auf einem Beleg wird nur eine Beschriftung für mehrere Arbeitsköpfe gedruckt</span><span class="sxs-lookup"><span data-stu-id="df0be-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="df0be-104">KB-Nummer: 4614667</span><span class="sxs-lookup"><span data-stu-id="df0be-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="df0be-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="df0be-105">Symptoms</span></span>

<span data-ttu-id="df0be-106">Im Rahmen eines einzelnen Empfangsereignisses in der Lagerort-App werden mehrere Arbeitsköpfe für den gleichen Zielladungsträger erstellt.</span><span class="sxs-lookup"><span data-stu-id="df0be-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="df0be-107">Bei Erhalt des Produkts wird jedoch nur eine Ladungsträgerbeschriftung gedruckt.</span><span class="sxs-lookup"><span data-stu-id="df0be-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="df0be-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="df0be-108">Resolution</span></span>

<span data-ttu-id="df0be-109">Das System verhält sich wie vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="df0be-109">The system is behaving as designed.</span></span>

<span data-ttu-id="df0be-110">Im aktuellen Design wird unabhängig von der Anzahl der vorhandenen Kombinationen aus Arbeitskopf und Arbeitsposition immer nur eine Ladungsträgerbeschriftung generiert.</span><span class="sxs-lookup"><span data-stu-id="df0be-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="df0be-111">Die generierte Beschriftung enthält die Informationen für nur eine Kombination.</span><span class="sxs-lookup"><span data-stu-id="df0be-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="df0be-112">Stellen Sie zur Umgehung dieses Problems sicher, dass die Erstellung des Arbeitskopfs immer nur einem Zielladungsträger zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="df0be-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
