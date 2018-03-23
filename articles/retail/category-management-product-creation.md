---
title: Produktkategorieverwaltung
description: "In diesem Thema wird beschrieben, wie Verkaufmanager Produktkategorien (Einzelhandel) verwenden können, um Beziehungen zwischen Produkthierarchie (Einzelhandel) und freigegebenen Produktdetails zu verwalten."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: de-de
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="20899-103">Verbesserte Kategorie- und Produktverwaltung</span><span class="sxs-lookup"><span data-stu-id="20899-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="20899-104">Dieses Thema beschreibt eine erweiterte Art, Produktkategorien (Einzelhandel) und Produkte in Dynamics 365 for Retail zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="20899-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="20899-105">Mit diesen Erweiterungen können Verkaufmanager eine Wechselbeziehung zwischen Produkthierarchie (Einzelhandel) und freigegebenen Produktdetails haben.</span><span class="sxs-lookup"><span data-stu-id="20899-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="20899-106">Um mehr über das Verwalten von Produktkategorien (Retail) zu ermitteln, gehen sie zu**Produkthierarchie (Retail)** im Arbeitsbereich **Kategorie und Produktverwaltung** und beachten die erweiterte Struktur der Seite **Produktkategorie (Retail)**.</span><span class="sxs-lookup"><span data-stu-id="20899-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![Kategorie- und Produktverwaltungs-Areitsbereich](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="20899-108">In älteren Versionen wurden Produktattribute in **Grundeigenschaften** und P**roduktattribute Einzelhandel**, basierend auf dem Bereich der Anwendbarkeit aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="20899-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="20899-109">**Einzelhandelsprodukteigenschaften** sind nach Bereich *global* der Anwendbarkeit, was bedeutet, dass für eine gegebene **Produkteigenschaft Einzelhandel** der gleiche Wert für alle juristischen Personen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="20899-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="20899-110">**Grundprodukteigenschaften** sind *juristische Personen spezifisch*.</span><span class="sxs-lookup"><span data-stu-id="20899-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="20899-111">Das bedeutet, dass eine gegebene **Grund-Produkteigenschaft** in den juristischen Personen verschieden sein kann, basierend auf den einzelne geschäftlichen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="20899-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="20899-112">Mithilfe dieser Erweiterungen für Produktattribute in der Produktkategorie Einzelhandel trennen wir weiterhin die Felder, die auf der Grundlage ihrer Anwendbarkeit innerhalb einer Gruppe basieren, um die Details für freigegebene Produkte der Formularstruktur widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="20899-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![Gruppierung der Felder auf der Grundlage ihres jeweiligen Bereich der Anwendbarkeit](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="20899-114">Sie können zwischen dem Verwalten bestimmter Eigenschaften der Entität für alle juristischen Personen und dem Verwalten für eine bestimmte juristische Person wechseln.</span><span class="sxs-lookup"><span data-stu-id="20899-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="20899-115">Wählen Sie einfach **Für alle juristischen Personen anzeigen/bearbeiten** oder **Für eine bestimmte juristische Person anzeigen/bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="20899-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![Toggle-Ansicht zwischen einer Person und allen juristischen Personen](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Toggle-Ansicht zwischen einer Person und allen juristischen Personen](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="20899-118">Verglichen zu älteren Versionen können in der neuen Produktkategorie-Struktur ein Verkaufsmanager Standardwerte für einen zusätzlichen Satz Produktattribute für eine einzelne Kategorien auch definieren.</span><span class="sxs-lookup"><span data-stu-id="20899-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="20899-119">Zum Zeitpunkt der Produkterstellung werden diese Standardprodukteigenschaftswerte durch ein Produkt, basierend auf deren Zuordnung zu einer bestimmten Kategorie in der Produkthierarchie (Einzelhandel) übernommen.</span><span class="sxs-lookup"><span data-stu-id="20899-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="20899-120">Verkaufmanager können diese übernommenen Produktattribute für die einzelnen Produkte ändern, um einzelnen geschäftlichen Bedarf abzudecken.</span><span class="sxs-lookup"><span data-stu-id="20899-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="20899-121">Wählen Eigenschaften aus, um Produkte im Formular Produktkategorie (Einzelhandel) zu aktualisieren</span><span class="sxs-lookup"><span data-stu-id="20899-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="20899-122">Sie können diese neue erweiterte Struktur für Produktattribute verwenden, um auszuwählen, welche aktualisierten Produktattribute für die zugehörigen Produkte aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="20899-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![Neue erweiterte Ansicht von Aktualisierungsprodukten](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="20899-124">Verkaufmanager können diese übernommenen Produktattribute für die einzelnen Produkte ändern, um einzelnen geschäftlichen Bedarf abzudecken.</span><span class="sxs-lookup"><span data-stu-id="20899-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


