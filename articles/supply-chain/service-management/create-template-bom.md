---
title: Erstellen einer Vorlagenstückliste
description: Eine Vorlagenstückliste kann auf viele Arten erstellt werden.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c5d45ac27a8678c51fb63c0326c2802a094596
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "320994"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="2c430-103">Erstellen einer Vorlagenstückliste</span><span class="sxs-lookup"><span data-stu-id="2c430-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2c430-104">Eine Vorlagenstückliste kann auf folgende Arten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2c430-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="2c430-105">Bei allen Verfahren gilt: Die Felder **Von Datum** und **Bis datum** sind optional und nur zu Informationszwecken vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2c430-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="2c430-106">Manuelles Erstellen einer Vorlagenstückliste</span><span class="sxs-lookup"><span data-stu-id="2c430-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="2c430-107">Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Serviceobjekte** \> **Vorlagenstücklisten**.</span><span class="sxs-lookup"><span data-stu-id="2c430-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="2c430-108">Drücken Sie STRG+N, um das Formular **Vorlagenstückliste erstellen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c430-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="2c430-109">Wählen Sie unter **Stücklistenpositionen aus Referenz kopieren** die Option **Manuell** aus.</span><span class="sxs-lookup"><span data-stu-id="2c430-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="2c430-110">Geben Sie im Feld **Artikelnummer** einen Artikel des Typs **Stückliste** ein.</span><span class="sxs-lookup"><span data-stu-id="2c430-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="2c430-111">Geben Sie im Feld **Name** einen Namen für die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="2c430-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="2c430-112">Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** ein Datumsintervall an, in dem die Vorlagenstückliste aktiv sein soll.</span><span class="sxs-lookup"><span data-stu-id="2c430-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="2c430-113">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c430-113">Click **OK**.</span></span>

<span data-ttu-id="2c430-114">Eine neue leere Vorlagenstückliste wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c430-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="2c430-115">Erstellen einer Vorlagenstückliste auf Basis einer anderen Vorlagenstückliste</span><span class="sxs-lookup"><span data-stu-id="2c430-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="2c430-116">Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Serviceobjekte** \> **Vorlagenstücklisten**.</span><span class="sxs-lookup"><span data-stu-id="2c430-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="2c430-117">Drücken Sie STRG+N, um das Formular **Vorlagenstückliste erstellen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c430-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="2c430-118">Wählen Sie unter **Stücklistenpositionen aus Referenz kopieren** die Option **Vorlagenstückliste** aus.</span><span class="sxs-lookup"><span data-stu-id="2c430-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="2c430-119">Wählen Sie im Feld **Referenznummer** eine vorhandene Vorlagenstückliste aus, die in die neue Vorlagenstückliste kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c430-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="2c430-120">Geben Sie im Feld **Name** einen Namen für die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="2c430-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="2c430-121">Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** ein Datumsintervall an, in dem die Vorlagenstückliste aktiv sein soll.</span><span class="sxs-lookup"><span data-stu-id="2c430-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="2c430-122">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c430-122">Click **OK**.</span></span>

<span data-ttu-id="2c430-123">Eine neue Vorlagenstückliste wird erstellt. Diese enthält die gleichen Positionen wie die ursprüngliche Vorlagenstückliste.</span><span class="sxs-lookup"><span data-stu-id="2c430-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="2c430-124">Erstellen einer Vorlagenstückliste auf Basis einer Artikelstückliste</span><span class="sxs-lookup"><span data-stu-id="2c430-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="2c430-125">Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Serviceobjekte** \> **Vorlagenstücklisten**.</span><span class="sxs-lookup"><span data-stu-id="2c430-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="2c430-126">Drücken Sie STRG+N, um das Formular **Vorlagenstückliste erstellen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c430-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="2c430-127">Wählen Sie unter die **Stücklistenpositionen aus Referenz kopieren** **Stückliste** aus.</span><span class="sxs-lookup"><span data-stu-id="2c430-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="2c430-128">Wählen Sie im Feld **Referenznummer** eine Stücklistenversion wählen Sie aus.</span><span class="sxs-lookup"><span data-stu-id="2c430-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="2c430-129">Ein Artikel vom Typ "Stückliste" wird in das Feld **Artikelnummer** kopiert.</span><span class="sxs-lookup"><span data-stu-id="2c430-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="2c430-130">Geben Sie im Feld **Name** einen Namen für die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="2c430-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="2c430-131">Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** ein Datumsintervall an, in dem die Vorlagenstückliste aktiv sein soll.</span><span class="sxs-lookup"><span data-stu-id="2c430-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="2c430-132">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c430-132">Click **OK**.</span></span>

<span data-ttu-id="2c430-133">Eine neue Vorlagenstückliste erstellt. Diese enthält die gleichen Positionen, die auch in der unter **Stücklisten** aufgeführten Stückliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2c430-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="2c430-134">Erstellen einer Vorlagenstückliste auf Basis einer Produktionsstückliste</span><span class="sxs-lookup"><span data-stu-id="2c430-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="2c430-135">Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Serviceobjekte** \> **Vorlagenstücklisten**.</span><span class="sxs-lookup"><span data-stu-id="2c430-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="2c430-136">Drücken Sie STRG+N, um das Formular **Vorlagenstückliste erstellen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c430-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="2c430-137">Wählen Sie unter die **Stücklistenpositionen aus Referenz kopieren** **Produktion** aus.</span><span class="sxs-lookup"><span data-stu-id="2c430-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="2c430-138">Wählen Sie im Feld **Referenznummer** eine Produktions-Stücklistenversion aus.</span><span class="sxs-lookup"><span data-stu-id="2c430-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="2c430-139">Geben Sie im Feld **Name** einen Namen für die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="2c430-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="2c430-140">Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** ein Datumsintervall an, in dem die Vorlagenstückliste aktiv sein soll.</span><span class="sxs-lookup"><span data-stu-id="2c430-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="2c430-141">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c430-141">Click **OK**.</span></span>

<span data-ttu-id="2c430-142">Eine neue Vorlagenstückliste erstellt. Diese enthält die gleichen Positionen, die auch in der unter **Stückliste** aufgeführten Stückliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2c430-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c430-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c430-143">See also</span></span>

[<span data-ttu-id="2c430-144">Vorlagenstücklisten</span><span class="sxs-lookup"><span data-stu-id="2c430-144">Template BOMs</span></span>](template-boms.md)

  


