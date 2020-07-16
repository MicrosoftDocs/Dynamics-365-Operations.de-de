---
title: Prozessautomatisierung
description: Dieses Thema enthält Details dazu, wie die Prozessautomatisierung die einfache Planung von Prozessen ermöglicht, die vom Batch-Server ausgeführt werden.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508184"
---
# <a name="process-automation"></a><span data-ttu-id="f0308-103">Prozessautomatisierung</span><span class="sxs-lookup"><span data-stu-id="f0308-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f0308-104">Prozessautomatisierung ermöglicht die einfache Planung von Prozessen, die vom Batch-Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f0308-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="f0308-105">Die aktualisierte Kalenderansicht der geplanten Arbeit ermöglicht es Endbenutzern, geplante und abgeschlossene Arbeiten anzuzeigen und Maßnahmen zu ergreifen.</span><span class="sxs-lookup"><span data-stu-id="f0308-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="f0308-106">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="f0308-106">Administration</span></span>

<span data-ttu-id="f0308-107">Die zentrale Administrationsseite für alle Prozessautomatisierungen finden Sie im Systemadministrationsmodul im Menü **Einrichtung**.</span><span class="sxs-lookup"><span data-stu-id="f0308-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="f0308-108">Diese Seite listet alle automatisierten Prozesse (Serien) auf, die im System eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="f0308-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="f0308-109">Außerdem können Sie direkt von dieser Seite aus neue Prozessautomatisierungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f0308-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="f0308-110">Nachdem eine Serie eingerichtet wurde, können Sie jede Serie aus dieser Liste verwalten.</span><span class="sxs-lookup"><span data-stu-id="f0308-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="f0308-111">Sie können die gesamte Serie bearbeiten, löschen, alle Vorkommen in einer Listenansicht anzeigen oder die Serie deaktivieren, wenn Sie die geplante Arbeit für einen bestimmten Zeitraum anhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="f0308-111">You can chose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a period of time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="f0308-112">Kalenderansicht</span><span class="sxs-lookup"><span data-stu-id="f0308-112">Calendar view</span></span> 
<span data-ttu-id="f0308-113">Einer der Hauptvorteile der Prozessautomatisierung ist die Möglichkeit, die geplanten Arbeiten in einer einfachen Kalenderansicht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f0308-113">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="f0308-114">In dieser Ansicht können Sie die Arbeit für jeweils eine Woche anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f0308-114">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="f0308-115">Sie sehen diese Ansicht auf der rechten Seite der Seite **Prozessautomatisierung**.</span><span class="sxs-lookup"><span data-stu-id="f0308-115">You will see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="f0308-116">Sie wird mit der geplanten Arbeit für die ausgewählte Serie gefüllt.</span><span class="sxs-lookup"><span data-stu-id="f0308-116">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="f0308-117">[![Prozessautomatisierungskalender](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="f0308-117">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="f0308-118">Vorkommensänderungen</span><span class="sxs-lookup"><span data-stu-id="f0308-118">Occurrence changes</span></span>
<span data-ttu-id="f0308-119">Jedes Vorkommen kann geändert werden, ohne dass dies Auswirkungen auf andere Vorkommen hat, die durch die Serie definiert sind, aus der sie stammen.</span><span class="sxs-lookup"><span data-stu-id="f0308-119">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="f0308-120">Vorkommen geplanter Arbeiten können in der Kalenderansicht bearbeitet werden, indem die Schaltfläche **Anzeigen/Bearbeiten** und **Vorkommen** ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="f0308-120">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="f0308-121">Auf diese Weise können Sie auf alle Einstellungen zugreifen, die ursprünglich im Serien-Setup-Assistenten angezeigt wurden, und Sie können eine einmalige Änderung für das ausgewählte Vorkommen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="f0308-121">This allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="f0308-122">Das Vorkommen geplanter Arbeiten kann auch deaktiviert werden, indem die Schaltfläche **Deaktivieren** in der Kalenderansicht ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="f0308-122">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span> 

## <a name="developer-documentation"></a><span data-ttu-id="f0308-123">Entwicklerdokumentation</span><span class="sxs-lookup"><span data-stu-id="f0308-123">Developer documentation</span></span> 
<span data-ttu-id="f0308-124">Derzeit wird eine Entwicklerdokumentation geschrieben, mit der Entwickler das Framework für die Prozessautomatisierung erweitern können.</span><span class="sxs-lookup"><span data-stu-id="f0308-124">Developer documentation is currently being written to allow developers to extend the process automation framework.</span></span> <span data-ttu-id="f0308-125">Diese Dokumentation enthält Informationen darüber, wie Sie benutzerdefinierte Prozesse erstellen können, die von dem mit dem Prozessautomatisierungsassistenten geplanten Batch-Server ausgeführt werden müssen und automatisch in der Kalenderansicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f0308-125">This documentation will provide information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>
