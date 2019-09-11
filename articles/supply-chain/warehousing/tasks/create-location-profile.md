---
title: Lagerplatzprofil erstellen
description: In diesem Thema wird erläutert, wie ein Lagerplatzprofil in Dynamics 365 for Finance and Operations erstellt wird.
author: ShylaThompson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46aa1001c21ae39c158062444303ca02c0f41a45
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866978"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="14cc6-103">Lagerplatzprofil erstellen</span><span class="sxs-lookup"><span data-stu-id="14cc6-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14cc6-104">In diesem Thema wird erläutert, wie ein Lagerplatzprofil in Dynamics 365 for Finance and Operations erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="14cc6-104">This topic explains how to create a location profile in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="14cc6-105">Jeder Standort in den Lagerortanforderungen musst ein Lagerplatzprofil zugeordnet haben, das die Eigenschaften des Lagerplatzes beschreibt, beispielsweise ob der Lagerplatz Mischartikel zulässt.</span><span class="sxs-lookup"><span data-stu-id="14cc6-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="14cc6-106">In diesem Verfahren erstellen wir ein Profil für einen Lagerplatz, der nicht über Ladungsträger gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="14cc6-106">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="14cc6-107">Wir aktivieren Mischartikel und Mischbestandsstatus und ermöglichen die permanente Inventur.</span><span class="sxs-lookup"><span data-stu-id="14cc6-107">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="14cc6-108">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="14cc6-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="14cc6-109">Wechseln Sie im Navigationsbereich zu **Module > Lagerortverwaltung > Einstellungen > Lagerort > Lagerplatzprofile**.</span><span class="sxs-lookup"><span data-stu-id="14cc6-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="14cc6-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="14cc6-110">Select **New**.</span></span>
3. <span data-ttu-id="14cc6-111">Geben Sie im Feld **Lagerort-Profil-ID** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="14cc6-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="14cc6-112">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="14cc6-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="14cc6-113">Geben Sie im Feld **Lagerplatzformat** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="14cc6-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="14cc6-114">Geben Sie im Feld **Lagerplatztyp** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="14cc6-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="14cc6-115">Geben Sie im Feld **Rampenverwaltungsprofil-Kennung** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="14cc6-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="14cc6-116">Wählen Sie **Ja** im Feld **Gemischte Artikel zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="14cc6-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="14cc6-117">Wählen Sie **Ja** im Feld **Gemischte Bestandstatus zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="14cc6-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="14cc6-118">Wählen Sie **Ja** im Feld **Permanente Inventur zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="14cc6-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="14cc6-119">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="14cc6-119">Select **Save**.</span></span>

