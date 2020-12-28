---
title: Transportverwaltung Zonenmaster
description: Dieses Thema erklärt, wie Sie mit der Transportverwaltung geografische Lagerplätze in Zonen einteilen können.
author: Henrikan
manager: ''
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSZoneMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2112e7131281cd485b580fd71536981c1ba4aefd
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2020
ms.locfileid: "4429170"
---
# <a name="transportation-management-zone-master"></a><span data-ttu-id="0bfa2-103">Transportverwaltung Zonenmaster</span><span class="sxs-lookup"><span data-stu-id="0bfa2-103">Transportation management zone master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bfa2-104">Mit der Transportverwaltung können Sie geografische Lagerplätze in Zonen einteilen.</span><span class="sxs-lookup"><span data-stu-id="0bfa2-104">Transport management lets you divide geographic locations into zones.</span></span> <span data-ttu-id="0bfa2-105">Die Einteilung von Lagerplätzen in Zonen kann helfen:</span><span class="sxs-lookup"><span data-stu-id="0bfa2-105">Dividing locations into zones can help to:</span></span>

- <span data-ttu-id="0bfa2-106">**Vereinfachung der Transportpreisgestaltung** - Eine zonenweise Preisgestaltung kann einfacher sein als eine Preisgestaltung auf Basis einzelner Lagerplätze, besonders wenn die Transportplätze verstreut sind.</span><span class="sxs-lookup"><span data-stu-id="0bfa2-106">**Simplify transportation pricing** – Zone-wise pricing can be simpler than individual location-based pricing, especially when transportation locations are scattered.</span></span>
- <span data-ttu-id="0bfa2-107">**Ladungsplanung optimieren** - Durch die Konsolidierung von Ladungen nach Zonen.</span><span class="sxs-lookup"><span data-stu-id="0bfa2-107">**Optimize load planning** – By consolidating loads by zones.</span></span>
- <span data-ttu-id="0bfa2-108">**Optimieren Sie die Arbeitspläne** - Indem Sie bestimmte Arbeitspläne bestimmten Zonen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="0bfa2-108">**Optimize route planning** – By assigning specific route plans to specific zones.</span></span>

<span data-ttu-id="0bfa2-109">Sie definieren Zonen basierend auf den Werten der Metadatenfelder (wie Land, Postleitzahlenbereich oder Spediteur), die jede Zone qualifizieren.</span><span class="sxs-lookup"><span data-stu-id="0bfa2-109">You define zones based on the metadata field values (such as country, zip code range, or carrier service) that qualify each zone.</span></span> <span data-ttu-id="0bfa2-110">Zonendefinitionen sind nicht erforderlich, wenn Ihre Transportpreise kein Zonenkonzept verwenden.</span><span class="sxs-lookup"><span data-stu-id="0bfa2-110">Zone definitions aren't required if your transportation pricing doesn't employ a zone concept.</span></span>
