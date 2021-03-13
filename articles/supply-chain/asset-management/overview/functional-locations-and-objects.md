---
title: Funktionale Standorte und Anlagen
description: In diesem Thema werden funktionale Standorte und Anlagen in Asset Management beschrieben. Asset Management ist ein erweitertes Modul für die Verwaltung von Anlagen und Wartungsaufgaben in Dynamics 365 Supply Chain Management.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f93a68f19b0b952eb2964b404bb957865c625cd
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018045"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="01115-104">Funktionale Standorte und Anlagen</span><span class="sxs-lookup"><span data-stu-id="01115-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="01115-105">In diesem Thema werden funktionale Standorte und Anlagen in Asset Management beschrieben.</span><span class="sxs-lookup"><span data-stu-id="01115-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="01115-106">Asset Management ist ein erweitertes Modul für die Verwaltung von Anlagen und Wartungsaufgaben in Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="01115-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="01115-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="01115-107">Overview</span></span>

<span data-ttu-id="01115-108">Anlagenmanagement ist nahtlos in mehrere Module in anderen Finance and Operations Apps integriert.</span><span class="sxs-lookup"><span data-stu-id="01115-108">Asset Management is integrated seamlessly with several modules with other Finance and Operations apps.</span></span> <span data-ttu-id="01115-109">Die folgende Abbildung zeigt die Schnittstellen mit anderen Modulen.</span><span class="sxs-lookup"><span data-stu-id="01115-109">The following illustration shows the interfaces with other modules.</span></span>

![Diagramm, das die Anlagenmanagement-Schnittstellen mit anderen Modulen zeigt](media/01-overview-image.png)

<span data-ttu-id="01115-111">Mit Asset Management können Sie effizient alle Aufgaben verwalten und ausführen, die mit dem Verwalten und der Wartung von viele Arten von Ausrüstung in Ihrem Unternehmen zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="01115-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="01115-112">Zu diesen Ausrüstungsgegenständen zählen Maschinen, Produktionsanlagen und Fahrzeuge.</span><span class="sxs-lookup"><span data-stu-id="01115-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="01115-113">Asset Management unterstützt außerdem Lösungen über zahlreiche Branchen hinweg.</span><span class="sxs-lookup"><span data-stu-id="01115-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="01115-114">Die folgende Abbildung zeigt einen Überblick über die Hauptfunktionen von Asset Management.</span><span class="sxs-lookup"><span data-stu-id="01115-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Diagramm, das die Hauptfunktionen in Anlagenmanagement anzeigt](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="01115-116">Funktionale Standorte und Anlagen</span><span class="sxs-lookup"><span data-stu-id="01115-116">Functional locations and assets</span></span>

<span data-ttu-id="01115-117">Funktionale Standorte werden verwendet, um Anlagen an Standorten zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="01115-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="01115-118">Zu dieser Verwaltung gehört das Nachverfolgen von Anlagenkosten an funktionalen Standorten.</span><span class="sxs-lookup"><span data-stu-id="01115-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="01115-119">Funktionale Standorte werden hierarchisch strukturiert, und Standorte können untergeordnete Standorte haben.</span><span class="sxs-lookup"><span data-stu-id="01115-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="01115-120">Die Struktur funktionaler Standorte ist statisch.</span><span class="sxs-lookup"><span data-stu-id="01115-120">The structure of functional locations is static.</span></span> <span data-ttu-id="01115-121">Dies bedeutet, das Standorte den Ort nicht ändern können.</span><span class="sxs-lookup"><span data-stu-id="01115-121">In other words, locations can't change place.</span></span> <span data-ttu-id="01115-122">Anlagen können an funktionalen Standorten installiert sein und können bei Bedarf später an anderen funktionalen Standorten installiert werden.</span><span class="sxs-lookup"><span data-stu-id="01115-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="01115-123">Anlagenkosten folgen immer dem Standort der Anlage.</span><span class="sxs-lookup"><span data-stu-id="01115-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="01115-124">Dies bedeutet Folgendes: Wenn Sie eine Anlage an einem neuen funktionalen Standort einrichten, verwendet die Anlage automatisch die Finanzdimensionen, die sich auf den neuen funktionalen Standort beziehen.</span><span class="sxs-lookup"><span data-stu-id="01115-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="01115-125">Daher beziehen sich Anlagenkosten immer auf den funktionalen Standort, an dem die Anlage derzeit installiert ist.</span><span class="sxs-lookup"><span data-stu-id="01115-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="01115-126">Diese automatische Handhabung von Finanzdimensionen gewährleistet die Nachverfolgung von Kosten beim Durchführen von Projekt-Controlling und -Reporting für funktionale Standorte.</span><span class="sxs-lookup"><span data-stu-id="01115-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="01115-127">Die Art, wie Sie die Hierarchie der funktionalen Standorte erstellen, hängt von den Unternehmensanforderungen für die Verwaltung der internen Ausrüstung oder die Wartung der Ausrüstung von Kunden ab.</span><span class="sxs-lookup"><span data-stu-id="01115-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="01115-128">Die folgende Abbildung zeigt ein Beispiel für funktionale Standorte, die auf geografischen Standorten basieren.</span><span class="sxs-lookup"><span data-stu-id="01115-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Diagramm, das die funktionalen Standorte auf Grundlage der geografischen Standorte anzeigt](media/03-overview-image.png)

<span data-ttu-id="01115-130">Die folgende Abbildung zeigt ein Beispiel für funktionale Standorte, die auf Kunden basieren.</span><span class="sxs-lookup"><span data-stu-id="01115-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Diagramm, das die funktionalen Standorte auf Grundlage der Kunden anzeigt](media/04-overview-image.png)
