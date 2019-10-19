---
title: Anlagen und Arbeitsaufträge
description: In diesem Thema werden Anlagen und Arbeitsaufträge in Asset Management beschrieben.
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
ms.openlocfilehash: 24d75000e2c4b604e1acee94e9581291e156fa5d
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017410"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="c804b-103">Anlagen und Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="c804b-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c804b-104">In diesem Thema werden Anlagen und Arbeitsaufträge in Asset Management beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c804b-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="c804b-105">Anlagen und Arbeitsaufträge sind die zentralen Teile von Asset Management.</span><span class="sxs-lookup"><span data-stu-id="c804b-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="c804b-106">Eine *Anlage* ist eine Maschine oder ein Maschinenteil, die bzw. das fortlaufende Wartung und kontinuierlichen Service benötigt.</span><span class="sxs-lookup"><span data-stu-id="c804b-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="c804b-107">Anlagen können in einer hierarchischen Struktur erstellt werden, und sie können funktionalen Standorten zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="c804b-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="c804b-108">Wartungsaufträge können auf allen Ebenen der Anlagenstruktur geplant werden.</span><span class="sxs-lookup"><span data-stu-id="c804b-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="c804b-109">Verschiedene Daten wie z. B. Produktinformationen und Anlagenspezifikationen sowie erforderliche Wartungspläne werden für jede Anlage eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="c804b-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="c804b-110">Die folgende Abbildung zeigt einen Überblick über Anlagendaten und die Zugehörigkeit von Anlagen zu Einzelvorgangstypen.</span><span class="sxs-lookup"><span data-stu-id="c804b-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="c804b-111">Roter Text wird für Beispiele verwendet, die Vererbung und Abhängigkeiten zeigen.</span><span class="sxs-lookup"><span data-stu-id="c804b-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![Abbildung 1](media/05-overview-image.png)

<span data-ttu-id="c804b-113">Jeder Arbeitsauftrag hat einen Arbeitsauftragstyp, wie z. B. vorbeugende Wartung, korrektive Wartung oder Inspektion.</span><span class="sxs-lookup"><span data-stu-id="c804b-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="c804b-114">Der Arbeitsauftrag enthält einen oder mehrere Arbeitsauftragseinzelvorgänge.</span><span class="sxs-lookup"><span data-stu-id="c804b-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="c804b-115">Jeder Arbeitsauftragseinzelvorgang definiert einen Einzelvorgang, der für eine Anlage ausgeführt werden muss, und einen zugehörigen Einzelvorgangstyp.</span><span class="sxs-lookup"><span data-stu-id="c804b-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="c804b-116">Beispiele für zugehörige Einzelvorgangstypen sind 10.000 km, 50.000 km, Überholung nach 1 Jahr und Sicherheitsprüfung.</span><span class="sxs-lookup"><span data-stu-id="c804b-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="c804b-117">Ein Arbeitsauftrag kann mehreren Anlagen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c804b-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="c804b-118">Die folgende Abbildung zeigt einen Überblick über die wichtigsten Daten in einem Arbeitsauftrag.</span><span class="sxs-lookup"><span data-stu-id="c804b-118">The following illustration shows an overview of the key data in a work order.</span></span>

![Abbildung 2](media/06-overview-image.png)

<span data-ttu-id="c804b-120">Ein Arbeitsauftrag kann einem anderen Arbeitsauftrag zugeordnet werden, und Einzelvorgangstypen können aufeinander folgende Einzelvorgänge enthalten, die einen Arbeitsauftrag bilden.</span><span class="sxs-lookup"><span data-stu-id="c804b-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="c804b-121">Im Allgemeinen gibt es keine Abhängigkeiten zwischen Arbeitsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="c804b-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="c804b-122">Daher kann sich ihr Arbeitsauftrags-Lebenszyklusstatus ändern und sie können unabhängig voneinander geplant werden.</span><span class="sxs-lookup"><span data-stu-id="c804b-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="c804b-123">Arbeitsaufträge können auf verschiedene Weise erstellt werden, die der korrektiven, vorbeugenden oder reagierenden Wartung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c804b-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="c804b-124">Sie können Arbeitsaufträge auch manuell erstellen.</span><span class="sxs-lookup"><span data-stu-id="c804b-124">You can also create work orders manually.</span></span> <span data-ttu-id="c804b-125">Die folgende Abbildung zeigt einen Überblick über den Prozess der automatischen oder manuellen Erstellung von Arbeitsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="c804b-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![Abbildung 3](media/07-overview-image.png)

<span data-ttu-id="c804b-127">Mehrere Schritte müssen ausgeführt werden, wenn Sie einen Wartungsauftrag für einen Arbeitsauftrag planen und ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="c804b-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="c804b-128">Die folgende Abbildung zeigt einen Überblick über die Verarbeitung eines Arbeitsauftrags.</span><span class="sxs-lookup"><span data-stu-id="c804b-128">The following illustration shows an overview of the processing for a work order.</span></span>

![Abbildung 4](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="c804b-130">Wenn Sie in Dynamics 365 Supply Chain Management und dem Modul **Asset Management** arbeiten, wählen Sie normalerweise **Neu**, um einen neuen Datensatz zu erstellen, **Bearbeiten**, um einen vorhandenen Datensatz zu aktualisieren, und **Speichern**, um die neuen oder bearbeiteten Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c804b-130">In general, when you work in Dynamics 365 Supply Chain Management and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>
