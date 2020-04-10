---
title: Richten Sie Lagerortarbeitsrichtlinien ein (Anwendung, im Mai 2016)
description: Lagerortprozesse enthalten nicht immer Lagerortarbeit.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca54cceb83425c43b5d124cd6d11be0cdef4d63a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145915"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="4e304-103">Richten Sie Lagerortarbeitsrichtlinien ein (Anwendung, im Mai 2016)</span><span class="sxs-lookup"><span data-stu-id="4e304-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e304-104">Lagerortprozesse enthalten nicht immer Lagerortarbeit.</span><span class="sxs-lookup"><span data-stu-id="4e304-104">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="4e304-105">Wenn Sie eine Arbeitsrichtlinie definieren, können Sie die Erstellung von Arbeit für Rohmaterialentnahme sowie die Einlagerung fertiger Waren für einen Satz von Produkten an bestimmten Lagerplätzen verhindern.</span><span class="sxs-lookup"><span data-stu-id="4e304-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="4e304-106">Das Demodatenunternehmen USMF wurde dazu verwendet, diese Aufzeichnung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e304-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="4e304-107">Dieser Aufgabenleitfaden erfordert eine Dynamics AX-Anwendung der Version 7.0.1 oder später.</span><span class="sxs-lookup"><span data-stu-id="4e304-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="4e304-108">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Arbeit" > "Arbeitsrichtlinien".</span><span class="sxs-lookup"><span data-stu-id="4e304-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="4e304-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="4e304-109">Click New.</span></span>
3. <span data-ttu-id="4e304-110">Geben Sie im Feld "Arbeitsrichtlinienname" die Bezeichnung "Keine Einlagerungsarbeit" ein.</span><span class="sxs-lookup"><span data-stu-id="4e304-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="4e304-111">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="4e304-111">Click Save.</span></span>
5. <span data-ttu-id="4e304-112">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4e304-112">Click Add.</span></span>
6. <span data-ttu-id="4e304-113">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="4e304-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="4e304-114">Wählen Sie im Feld "Arbeitsauftragstyp" die Option "Einlagerung fertiger Waren" aus.</span><span class="sxs-lookup"><span data-stu-id="4e304-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="4e304-115">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4e304-115">Click Add.</span></span>
9. <span data-ttu-id="4e304-116">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="4e304-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="4e304-117">Wählen Sie im Feld "Arbeitsauftragstyp" die Option "Einlagerung von Co-Produkt und Nebenprodukt" aus.</span><span class="sxs-lookup"><span data-stu-id="4e304-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="4e304-118">Erweitern Sie den Abschnitt "Lagerplätze für Lagerbestand".</span><span class="sxs-lookup"><span data-stu-id="4e304-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="4e304-119">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4e304-119">Click Add.</span></span>
13. <span data-ttu-id="4e304-120">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="4e304-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="4e304-121">In der Lagerortliste geben Sie "51" ein.</span><span class="sxs-lookup"><span data-stu-id="4e304-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="4e304-122">Geben Sie im Feld "Lagerplatz" den Wert "001" ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4e304-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="4e304-123">Erweitern Sie den Abschnitt Produkte.</span><span class="sxs-lookup"><span data-stu-id="4e304-123">Expand the Products section.</span></span>
17. <span data-ttu-id="4e304-124">Wählen Sie im Feld "Produktauswahl" die Option "Ausgewählt" aus.</span><span class="sxs-lookup"><span data-stu-id="4e304-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="4e304-125">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4e304-125">Click Add.</span></span>
19. <span data-ttu-id="4e304-126">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="4e304-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="4e304-127">Geben Sie im Feld "Artikelnummer" den Wert "L0101" ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4e304-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="4e304-128">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="4e304-128">Click Save.</span></span>

