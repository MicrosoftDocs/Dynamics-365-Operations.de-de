---
title: Eine Arbeitsklasse erstellen
description: Dieses Verfahren zeigt Ihnen an, wie ein Arbeitsklasse eingerichtet wird.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkClass
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed9b72d891df4d40213d4854da6b09bd9876effa
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429061"
---
# <a name="create-a-work-class"></a><span data-ttu-id="84f34-103">Eine Arbeitsklasse erstellen</span><span class="sxs-lookup"><span data-stu-id="84f34-103">Create a work class</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84f34-104">Dieses Verfahren zeigt Ihnen an, wie ein Arbeitsklasse eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="84f34-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="84f34-105">Arbeitsklassen werden verwendet, um den Typ der Arbeitsauftragspositionen zuzuweisen und/oder einzuschränken, die ein Lagerarbeiter auf einem mobilen Gerät verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="84f34-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="84f34-106">Die Positionen, die eine Arbeitskraft verarbeiten kann, werden von Arbeitsklassen auf Menüeinträge des mobilen Geräts, auf denen der Lagerarbeiter Zugriff hat und der Arbeitsklasse ermittelt, die für die Arbeitspositionen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="84f34-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that's specified on the work lines.</span></span> <span data-ttu-id="84f34-107">Arbeitsklassen können auch verwendet werden, um den gesetzten Lagerplatz für eine Arbeitsauftragsposition zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="84f34-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="84f34-108">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.</span><span class="sxs-lookup"><span data-stu-id="84f34-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="84f34-109">Diese Prozedur ist für die Lagerverwaltung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="84f34-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="84f34-110">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Arbeit" > "Arbeitsklassen".</span><span class="sxs-lookup"><span data-stu-id="84f34-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="84f34-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="84f34-111">Click New.</span></span>
3. <span data-ttu-id="84f34-112">Geben Sie im Feld "Arbeitsklassenkennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="84f34-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="84f34-113">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="84f34-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="84f34-114">Wählen Sie im Feld "Arbeitsauftragstyp" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="84f34-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="84f34-115">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="84f34-115">Click New.</span></span>
7. <span data-ttu-id="84f34-116">Geben Sie im Feld "Typ Standort" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="84f34-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="84f34-117">Wenn Sie einen Lagerplatztyp auswählen, wird eine Einschränkung festgelegt, wohin die Artikel eingelagert werden können, nachdem sie entnommen wurden.</span><span class="sxs-lookup"><span data-stu-id="84f34-117">If you select a location type, this sets a restriction on where items can be put after they've been picked.</span></span> <span data-ttu-id="84f34-118">Diese Einstellung wird verwendet, wenn Lagerplatzdirektive versuchen, den Lagerplatz aufzulösen, oder ob ein Lagerarbeiter manuell den Speicherort für die Menüoption des mobilen Geräts bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="84f34-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="84f34-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="84f34-119">Close the page.</span></span>

