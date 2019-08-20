---
title: Lagerplatzprofil erstellen
description: Jeder Standort in den Lagerortanforderungen musst ein Lagerplatzprofil zugeordnet haben, das die Eigenschaften des Lagerplatzes beschreibt, beispielsweise ob der Lagerplatz Mischartikel zulässt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: a9e1217a1105e1d53fc937f927e066e392f1ef14
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847326"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="f3c0c-103">Lagerplatzprofil erstellen</span><span class="sxs-lookup"><span data-stu-id="f3c0c-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3c0c-104">Jeder Standort in den Lagerortanforderungen musst ein Lagerplatzprofil zugeordnet haben, das die Eigenschaften des Lagerplatzes beschreibt, beispielsweise ob der Lagerplatz Mischartikel zulässt.</span><span class="sxs-lookup"><span data-stu-id="f3c0c-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="f3c0c-105">In diesem Verfahren erstellen wir ein Profil für einen Lagerplatz, der nicht über Ladungsträger gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="f3c0c-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="f3c0c-106">Wir aktivieren Mischartikel und Mischbestandsstatus und ermöglichen die permanente Inventur.</span><span class="sxs-lookup"><span data-stu-id="f3c0c-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="f3c0c-107">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3c0c-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="f3c0c-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f3c0c-108">Click New.</span></span>
2. <span data-ttu-id="f3c0c-109">Geben Sie im Feld "Lagerort-Profil-ID" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f3c0c-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="f3c0c-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f3c0c-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f3c0c-111">Geben Sie im Feld "Lagerplatzformat" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f3c0c-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="f3c0c-112">Geben Sie im Feld "Lagerplatztyp" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f3c0c-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="f3c0c-113">Geben Sie im Feld "Rampenverwaltungsprofil-Kennung" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f3c0c-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="f3c0c-114">Wählen Sie "Ja" im Feld "Gemischte Artikel zulassen" aus.</span><span class="sxs-lookup"><span data-stu-id="f3c0c-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="f3c0c-115">Wählen Sie "Ja" im Feld "Gemischte Bestandstatus zulassen" aus.</span><span class="sxs-lookup"><span data-stu-id="f3c0c-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="f3c0c-116">Wählen Sie "Ja" im Feld "Permanente Inventur zulassen" aus.</span><span class="sxs-lookup"><span data-stu-id="f3c0c-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="f3c0c-117">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f3c0c-117">Click Save.</span></span>
11. <span data-ttu-id="f3c0c-118">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerort" > "Lagerplatzprofile".</span><span class="sxs-lookup"><span data-stu-id="f3c0c-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

