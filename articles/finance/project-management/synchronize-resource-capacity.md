---
title: Ressourcenkapazität synchronisieren
description: Dieses Thema enthält Informationen zum Synchronisieren der Kapazität einer Ressource über Kalender und Projekte hinweg.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760552"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="41fcc-103">Ressourcenkapazität synchronisieren</span><span class="sxs-lookup"><span data-stu-id="41fcc-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41fcc-104">Die Prozesse für die Ressourcensynchronisierung stellen sicher, dass die Kalender- und Basiskalenderinformationen zur Projekteinsatzplanung passen.</span><span class="sxs-lookup"><span data-stu-id="41fcc-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="41fcc-105">Wenn der Kalender geändert wird, nehmen die Prozesse die erforderlichen Aktualisierungen der Planung von Projektbetriebsmitteln vor.</span><span class="sxs-lookup"><span data-stu-id="41fcc-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="41fcc-106">Die Verfahren helfen außerdem, die Leistung zu verbessern, da die Ressourceninformationen des Kalenders vorab synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="41fcc-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="41fcc-107">Deshalb werden Aktualisierungen der Einsatzplanungsinformationen schneller durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="41fcc-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="41fcc-108">Es wird empfohlen, die Prozesse als Stapelverarbeitung und nicht einzeln zu planen.</span><span class="sxs-lookup"><span data-stu-id="41fcc-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="41fcc-109">Andernfalls besteht das Risiko, das jemand die inklusiven Datumsangaben bei der letzten Synchronisierung der Information vergisst.</span><span class="sxs-lookup"><span data-stu-id="41fcc-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="41fcc-110">Wenn keine inklusiven Datumsangaben verwendet werden, können Lücken während der Datumssynchronisierung auftreten.</span><span class="sxs-lookup"><span data-stu-id="41fcc-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalendersynchronisierung](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="41fcc-112">Ressourcenkapazitätszusammenfassungen synchronisieren</span><span class="sxs-lookup"><span data-stu-id="41fcc-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="41fcc-113">Der Synchronisierungsprozess wurde entworfen, um alle Ressourcenkalenderinformationen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="41fcc-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="41fcc-114">Dazu gehören Basiskalenderinformationen zu Änderungen an der Ressourcenkalenderkapazitätstabelle des Projekts.</span><span class="sxs-lookup"><span data-stu-id="41fcc-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="41fcc-115">Wenn neue Ressourcen zum Projekt hinzugefügt werden, stellen die Synchronisierungshilfen sicher, dass die aktualisierten Kalenderdaten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="41fcc-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="41fcc-116">Es Synchronisierung kann jederzeit durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="41fcc-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="41fcc-117">Es wird empfohlen, eine Stapelverarbeitung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="41fcc-117">We recommend that you use a batch.</span></span> <span data-ttu-id="41fcc-118">Die Optionen sind verfügbar, wenn Sie Kapazitätsreservierungen synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="41fcc-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="41fcc-119">Wählen Sie **Projektverwaltung und -buchhaltung** &gt; **Periodisch** &gt; **Kapazitätssynchronisierung** &gt; **Ressourcenkapazitätszusammenfassungen synchronisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="41fcc-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="41fcc-120">Legen Sie die Optionen in der folgenden Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="41fcc-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="41fcc-121">Option</span><span class="sxs-lookup"><span data-stu-id="41fcc-121">Option</span></span>      | <span data-ttu-id="41fcc-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41fcc-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="41fcc-123">Periodencode</span><span class="sxs-lookup"><span data-stu-id="41fcc-123">Period code</span></span> | <span data-ttu-id="41fcc-124">Wählen Sie optional den Hauptbuch-Datumsintervallcode aus, um das Start-und Enddatum für den Synchronisierungsprozess für die Ressourcenkapazitätszusammenfassungen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="41fcc-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="41fcc-125">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="41fcc-125">Start date</span></span>  | <span data-ttu-id="41fcc-126">Geben Sie das Startdatum für die Synchronisierung der Ressourcenkapazitätszusammenfassungen ein.</span><span class="sxs-lookup"><span data-stu-id="41fcc-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="41fcc-127">Enddatum</span><span class="sxs-lookup"><span data-stu-id="41fcc-127">End date</span></span>    | <span data-ttu-id="41fcc-128">Geben Sie das Enddatum für die Synchronisierung der Ressourcenkapazitätszusammenfassungen ein.</span><span class="sxs-lookup"><span data-stu-id="41fcc-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="41fcc-129">[![Synchronisierungsprozess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="41fcc-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
