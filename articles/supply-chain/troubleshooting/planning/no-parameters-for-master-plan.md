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
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="bd6de-103">Parameter für den Masterplan sind nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="bd6de-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="bd6de-104">Fehlercode: SYS25368</span><span class="sxs-lookup"><span data-stu-id="bd6de-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="bd6de-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="bd6de-105">Symptoms</span></span>

<span data-ttu-id="bd6de-106">Wenn Sie versuchen, einen geplanten Auftrag zu fixieren, erhalten Sie die folgende Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="bd6de-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="bd6de-107">Parameter für Produktprogrammplan '%1' sind nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bd6de-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="bd6de-108">Ursache</span><span class="sxs-lookup"><span data-stu-id="bd6de-108">Cause</span></span>

<span data-ttu-id="bd6de-109">Aufgrund von Konfigurationsproblemen kann das System die Einstellungen für den angegebenen Plan nicht finden.</span><span class="sxs-lookup"><span data-stu-id="bd6de-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="bd6de-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="bd6de-110">Resolution</span></span>

- <span data-ttu-id="bd6de-111">Gehen Sie zu **Produktprogrammplanung \> Einrichten \> Pläne \> Masterpläne**, und stellen Sie sicher, dass ein Plan mit dem angegebenen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bd6de-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
