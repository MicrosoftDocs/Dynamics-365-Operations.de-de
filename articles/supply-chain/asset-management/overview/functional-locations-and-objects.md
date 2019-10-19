---
title: Funktionale Standorte und Anlagen
description: In diesem Thema werden funktionale Standorte und Anlagen in Asset Management beschrieben. Asset Management ist ein erweitertes Modul für die Verwaltung von Anlagen und Wartungsaufgaben in Dynamics 365 Supply Chain Management.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5271b673d758608cae8e43d72b7e75b259d5f142
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024613"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="25bc0-104">Funktionale Standorte und Anlagen</span><span class="sxs-lookup"><span data-stu-id="25bc0-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="25bc0-105">In diesem Thema werden funktionale Standorte und Anlagen in Asset Management beschrieben.</span><span class="sxs-lookup"><span data-stu-id="25bc0-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="25bc0-106">Asset Management ist ein erweitertes Modul für die Verwaltung von Anlagen und Wartungsaufgaben in Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25bc0-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="25bc0-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="25bc0-107">Overview</span></span>

<span data-ttu-id="25bc0-108">Asset-Management ist nahtlos in mehrere Module aus dem Bereich Finance and Operations integriert.</span><span class="sxs-lookup"><span data-stu-id="25bc0-108">Asset Management is integrated seamlessly with several modules in Finance and Operations.</span></span> <span data-ttu-id="25bc0-109">Die folgende Abbildung zeigt die Schnittstellen mit anderen Modulen.</span><span class="sxs-lookup"><span data-stu-id="25bc0-109">The following illustration shows the interfaces with other modules.</span></span>

![Abbildung 1](media/01-overview-image.png)

<span data-ttu-id="25bc0-111">Mit Asset Management können Sie effizient alle Aufgaben verwalten und ausführen, die mit dem Verwalten und der Wartung von viele Arten von Ausrüstung in Ihrem Unternehmen zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="25bc0-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="25bc0-112">Zu diesen Ausrüstungsgegenständen zählen Maschinen, Produktionsanlagen und Fahrzeuge.</span><span class="sxs-lookup"><span data-stu-id="25bc0-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="25bc0-113">Asset Management unterstützt außerdem Lösungen über zahlreiche Branchen hinweg.</span><span class="sxs-lookup"><span data-stu-id="25bc0-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="25bc0-114">Die folgende Abbildung zeigt einen Überblick über die Hauptfunktionen von Asset Management.</span><span class="sxs-lookup"><span data-stu-id="25bc0-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Abbildung 2](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="25bc0-116">Funktionale Standorte und Anlagen</span><span class="sxs-lookup"><span data-stu-id="25bc0-116">Functional locations and assets</span></span>

<span data-ttu-id="25bc0-117">Funktionale Standorte werden verwendet, um Anlagen an Standorten zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="25bc0-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="25bc0-118">Zu dieser Verwaltung gehört das Nachverfolgen von Anlagenkosten an funktionalen Standorten.</span><span class="sxs-lookup"><span data-stu-id="25bc0-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="25bc0-119">Funktionale Standorte werden hierarchisch strukturiert, und Standorte können untergeordnete Standorte haben.</span><span class="sxs-lookup"><span data-stu-id="25bc0-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="25bc0-120">Die Struktur funktionaler Standorte ist statisch.</span><span class="sxs-lookup"><span data-stu-id="25bc0-120">The structure of functional locations is static.</span></span> <span data-ttu-id="25bc0-121">Dies bedeutet, das Standorte den Ort nicht ändern können.</span><span class="sxs-lookup"><span data-stu-id="25bc0-121">In other words, locations can't change place.</span></span> <span data-ttu-id="25bc0-122">Anlagen können an funktionalen Standorten installiert sein und können bei Bedarf später an anderen funktionalen Standorten installiert werden.</span><span class="sxs-lookup"><span data-stu-id="25bc0-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="25bc0-123">Anlagenkosten folgen immer dem Standort der Anlage.</span><span class="sxs-lookup"><span data-stu-id="25bc0-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="25bc0-124">Dies bedeutet Folgendes: Wenn Sie eine Anlage an einem neuen funktionalen Standort einrichten, verwendet die Anlage automatisch die Finanzdimensionen, die sich auf den neuen funktionalen Standort beziehen.</span><span class="sxs-lookup"><span data-stu-id="25bc0-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="25bc0-125">Daher beziehen sich Anlagenkosten immer auf den funktionalen Standort, an dem die Anlage derzeit installiert ist.</span><span class="sxs-lookup"><span data-stu-id="25bc0-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="25bc0-126">Diese automatische Handhabung von Finanzdimensionen gewährleistet die Nachverfolgung von Kosten beim Durchführen von Projekt-Controlling und -Reporting für funktionale Standorte.</span><span class="sxs-lookup"><span data-stu-id="25bc0-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="25bc0-127">Die Art, wie Sie die Hierarchie der funktionalen Standorte erstellen, hängt von den Unternehmensanforderungen für die Verwaltung der internen Ausrüstung oder die Wartung der Ausrüstung von Kunden ab.</span><span class="sxs-lookup"><span data-stu-id="25bc0-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="25bc0-128">Die folgende Abbildung zeigt ein Beispiel für funktionale Standorte, die auf geografischen Standorten basieren.</span><span class="sxs-lookup"><span data-stu-id="25bc0-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Abbildung 3](media/03-overview-image.png)

<span data-ttu-id="25bc0-130">Die folgende Abbildung zeigt ein Beispiel für funktionale Standorte, die auf Kunden basieren.</span><span class="sxs-lookup"><span data-stu-id="25bc0-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Abbildung 4](media/04-overview-image.png)
