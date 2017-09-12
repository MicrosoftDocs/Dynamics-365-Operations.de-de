---
title: Dispositionseinstellungen
description: Diese Deckungseinstellungen werden beim Produktprogrammplanungslauf zum Berechnen des Artikelbedarfs verwendet.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fb11a470d98a9742749daaac3244a5bb0d3a689c
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---

# <a name="coverage-settings"></a><span data-ttu-id="3d243-103">Dispositionseinstellungen</span><span class="sxs-lookup"><span data-stu-id="3d243-103">Coverage settings</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3d243-104">Diese Deckungseinstellungen werden beim Produktprogrammplanungslauf zum Berechnen des Artikelbedarfs verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d243-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="3d243-105">Sie können Deckungseinstellungen auf verschiedene Arten angeben:</span><span class="sxs-lookup"><span data-stu-id="3d243-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="3d243-106">Angeben von Dispositionseinstellungen für eine Dispositionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3d243-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="3d243-107">Sie haben die Möglichkeit zum Erstellen einer Deckungsgruppe mit Einstellungen für alle Produkte, die mit der Deckungsgruppe verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="3d243-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="3d243-108">Klicken Sie auf **Masterplan&gt; Einrichten &gt; Abdeckung &gt; Abdeckungsgruppen**, um eine Abdeckungsgruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3d243-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="3d243-109">Sie können eine Deckungsgruppe mit einem Produkt verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="3d243-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="3d243-110">Wenn der Link für einen bestimmten Standort, Lagerort oder eine Produktdimension bestimmt ist, verwenden Sie auf der Seite **Artikeldeckung** das Feld **Dispositionssteuerungsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="3d243-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="3d243-111">Wenn es ein generischer Link ist, verwenden Sie unabhängig von den Produktdimensionen die **Dispositionssteuerungsgruppe** auf dem Inforegister **Plan** der Seite **Produktdetails**.</span><span class="sxs-lookup"><span data-stu-id="3d243-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="3d243-112">Wenn Sie eine Dispositionssteuerungsgruppe nicht mit einem Produkt verknüpfen, verwendet der Produktprogrammplan nicht die **Allgemeine Dispositionssteuerungsgruppe**, die auf der Seite **Produktprogrammplanungsparameter** als Standard angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3d243-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="3d243-113">Angeben der Dispositionseinstellungen für ein Produkt.</span><span class="sxs-lookup"><span data-stu-id="3d243-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="3d243-114">Sie haben die Möglichkeit zum Erstellen von Deckungseinstellungen für ein bestimmtes Produkt.</span><span class="sxs-lookup"><span data-stu-id="3d243-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="3d243-115">Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="3d243-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="3d243-116">Wählen Sie das Produkt im **Aktivitätenbereich**, in der Registerkarte **Plan** in der **Abdeckungsgruppe**, klicken Sie auf **Artikelabdeckung**, um die Seite **Artikelabdeckung** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3d243-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="3d243-117">Ist das Produkt bereits mit einer Dispositionsgruppe verknüpft, können die Einstellungen der Deckungsgruppe mithilfe des Felds **Überschreiben** überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3d243-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="3d243-118">Die Dispositionseinstellungen auf der Seite **Artikeldeckung** haben Vorrang vor den Einstellungen auf der Seite **Dispositionssteuerungsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="3d243-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="3d243-119">Angeben der Deckungseinstellungen für ein Produkt mithilfe eines Assistenten.</span><span class="sxs-lookup"><span data-stu-id="3d243-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="3d243-120">Bei dem Assistenten handelt es sich um eine schrittweise Anleitung zum Einrichten der primären Artikeldeckungsparameter.</span><span class="sxs-lookup"><span data-stu-id="3d243-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="3d243-121">Klicken Sie auf der Seite **Artikeldeckung** auf **Assistent**, um den **Artikeldeckungs-Assistent** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3d243-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

-   <span data-ttu-id="3d243-122">Angeben von Deckungseinstellungen für eine Dimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3d243-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="3d243-123">Klicken Sie auf **Produktinformationsverwaltung &gt;Allgemein &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="3d243-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="3d243-124">Auf der Seite **freigegebene Produktedetails** auf der Registerkarte **Allgemein**in der Gruppe **Administration** klicken Sie auf den Link **Lagerdimensionsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="3d243-124">On the **Released product detail **page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="3d243-125">Wählen Sie auf der Seite **Lagerdimensionsgruppe** das Feld **Disposition nach Dimensionen** aus, um die Deckungseinstellungen für eine Dimension in der Lagerdimensionsgruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3d243-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="3d243-126">Für jede Produktdimension, wie Konfiguration, Farbe, Größe, Stil, muss das Feld **Abdeckungsplan nach Dimensionn**  ausgewählt sein.</span><span class="sxs-lookup"><span data-stu-id="3d243-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="3d243-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d243-127">See also</span></span>
--------

[<span data-ttu-id="3d243-128">Masterpläne</span><span class="sxs-lookup"><span data-stu-id="3d243-128">Master plans</span></span>](master-plans.md)




