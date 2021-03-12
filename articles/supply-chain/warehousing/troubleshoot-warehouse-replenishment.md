---
title: Fehlerbehebung bei der Wiederbeschaffung im Lagerort
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Arbeit mit der Lagerort-Wiederbeschaffung in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7748a18d2b6f612b3ac9ac1a75efb6ae5f13859a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993876"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="be724-103">Fehlerbehebung bei der Lagerort-Wiederbeschaffung</span><span class="sxs-lookup"><span data-stu-id="be724-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be724-104">In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Arbeit mit der Lagerort-Wiederbeschaffung in Microsoft Dynamics 365 Supply Chain Management auftreten können.</span><span class="sxs-lookup"><span data-stu-id="be724-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="be724-105">Ich erhalte die folgende Fehlermeldung: „Arbeit %1 kann nicht entsperrt werden, da sie nicht beendete Wiederbeschaffung hat.“</span><span class="sxs-lookup"><span data-stu-id="be724-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="be724-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="be724-106">Issue description</span></span>

<span data-ttu-id="be724-107">Die Entnahmearbeiten sind wegen abhängiger Wiederbeschaffung blockiert.</span><span class="sxs-lookup"><span data-stu-id="be724-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="be724-108">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="be724-108">Issue resolution</span></span>

<span data-ttu-id="be724-109">Wenn Sie die Nachschubwelle verwenden und ein Lagerplatz wiederbeschafft werden muss, um den Bedarf des Quellauftrags zu erfüllen, erstellt das System sowohl die Wiederbeschaffungsarbeit als auch die Entnahmearbeiten.</span><span class="sxs-lookup"><span data-stu-id="be724-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="be724-110">Es blockiert jedoch die Entnahmearbeiten, bis die Wiederbeschaffung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="be724-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="be724-111">Dieses Verhalten ist beabsichtigt, da der Lagerplatz nicht über genügend Bestand verfügt, solange die Wiederbeschaffung nicht abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="be724-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="be724-112">Schließen Sie die Wiederbeschaffung ab, und verarbeiten Sie dann die Entnahmearbeiten.</span><span class="sxs-lookup"><span data-stu-id="be724-112">Complete the replenishment work, and then process the picking work.</span></span>
