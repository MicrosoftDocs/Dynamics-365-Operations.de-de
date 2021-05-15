---
title: Quarantänezonen für Qualitätsmängel
description: Dieses Thema beschreibt, wie Sie Quarantänezonen für Qualitätsmängel erstellen und verwenden.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ca74ec4586fffa3b9156aadab887629283b98a
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956673"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="fe477-103">Quarantänezonen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="fe477-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe477-104">Dieses Thema beschreibt, wie Sie Quarantänezonen für Qualitätsmängel erstellen und verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe477-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="fe477-105">Sie verwenden die Seite **Quarantänezonen**, um Zonen zu definieren, die Qualitätsmängeln zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="fe477-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="fe477-106">Wenn Sie einen Qualitätsmangel erstellen, können Sie die Felder **Quarantänezone** und **Quarantänetyp** auf der Registerkarte **Allgemein** der Seite **Nichtkonformitäten** festlegen.</span><span class="sxs-lookup"><span data-stu-id="fe477-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="fe477-107">Das Feld **Quarantänezone** gibt normalerweise den Bereich oder Lagerplatz an, in dem sich das Element befindet.</span><span class="sxs-lookup"><span data-stu-id="fe477-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="fe477-108">Das Feld **Quarantänetyp** definiert das Element entweder als *Eingeschränkte Verwendung* oder *Unverwendbar*.</span><span class="sxs-lookup"><span data-stu-id="fe477-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="fe477-109">Wenn Sie einen Bericht über Qualitätsmängel oder Korrekturen für einen Qualitätsmangel drucken, können Sie die Quarantänezone anzeigen, in der sich das Element befindet.</span><span class="sxs-lookup"><span data-stu-id="fe477-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="fe477-110">Sie können auch ein Etikett für einen Qualitätsmangel drucken.</span><span class="sxs-lookup"><span data-stu-id="fe477-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="fe477-111">Dieser Bericht zeigt die zugewiesene Quarantänezone und Informationen über die Verwendung an, um Anhaltspunkte für den Umgang mit defektem Material zu geben.</span><span class="sxs-lookup"><span data-stu-id="fe477-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="fe477-112">Die Quarantänezonen können Lagerplätzen oder Vorgängen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fe477-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="fe477-113">Beispiele für Quarantänezonen</span><span class="sxs-lookup"><span data-stu-id="fe477-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="fe477-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe477-114">Example 1</span></span>

<span data-ttu-id="fe477-115">Sie arbeiten bei einer Firma, die Elektronik herstellt und Fernsehgeräte, Lautsprecher und Media Player produziert und vertreibt.</span><span class="sxs-lookup"><span data-stu-id="fe477-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="fe477-116">In diesem Fall können Sie eine Quarantänezone konfigurieren, die jeden Produkttyp repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="fe477-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="fe477-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fe477-117">Example 2</span></span>

<span data-ttu-id="fe477-118">Drei Behälter und zwei Regale dienen zur Aufbewahrung von Elementen, die nicht den Qualitätsanforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fe477-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="fe477-119">In diesem Fall können Sie fünf Quarantänezonen konfigurieren, eine für jeden Behälter und jedes Regal.</span><span class="sxs-lookup"><span data-stu-id="fe477-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="fe477-120">Erstellen Sie eine Quarantänezone</span><span class="sxs-lookup"><span data-stu-id="fe477-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="fe477-121">Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätsmanagement \> Quarantänezonen**.</span><span class="sxs-lookup"><span data-stu-id="fe477-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="fe477-122">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe477-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="fe477-123">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="fe477-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="fe477-124">**Quarantänezone** – Geben Sie eine eindeutige ID oder einen Namen für die Quarantänezone ein.</span><span class="sxs-lookup"><span data-stu-id="fe477-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="fe477-125">**Beschreibung** – Geben Sie eine detaillierte Beschreibung der Quarantänezone ein.</span><span class="sxs-lookup"><span data-stu-id="fe477-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="fe477-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fe477-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe477-127">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fe477-127">Additional resources</span></span>

- [<span data-ttu-id="fe477-128">Qualitätsmanagement – Übersicht</span><span class="sxs-lookup"><span data-stu-id="fe477-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="fe477-129">Qualitäts- und Qualitätsmangel-Management aktivieren</span><span class="sxs-lookup"><span data-stu-id="fe477-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="fe477-130">Mitarbeiter, der für die Genehmigung von Qualitätsmängeln verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="fe477-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="fe477-131">Problemtypen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="fe477-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="fe477-132">Diagnosetypen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="fe477-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="fe477-133">Qualitätsbelastungen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="fe477-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="fe477-134">Vorgänge für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="fe477-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="fe477-135">Qualitätsmanagement für Lagerortprozesse</span><span class="sxs-lookup"><span data-stu-id="fe477-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
