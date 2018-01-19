---
title: Produktkategorieverwaltung und Erstellung
description: "In diesem Thema werden die Erweiterungen beschrieben, die für die Verwaltung von Einzelhandels-Produktkategorien gemacht wurde. Mit diesen Erweiterungen können Verkaufmanager eine Wechselbeziehung zwischen Produkthierarchie (Einzelhandel) und freigegebenen Produktdetails haben."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailCategory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 2aa9f913b7faac393c4b403c6c36b99cc9acc80c
ms.contentlocale: de-de
ms.lasthandoff: 01/19/2018

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="9a7f7-104">Produktkategorieverwaltung und Erstellung</span><span class="sxs-lookup"><span data-stu-id="9a7f7-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="9a7f7-105">Mit den Erweiterungen, die für die Verwaltungserfahrung Produktkategorien für Einzelhandel erstellt wurden, können Verkaufmanager eine Wechselbeziehung zwischen Produkthierarchie (Einzelhandel) und freigegebenen Produktdetails haben.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="9a7f7-106">Klicken Sie zum Anzeigen dieser Erweiterungen auf den Arbeitsbereich **Kategorie und Produktverwaltung.** und wählen Sie **Produkthierarchie (Einzelhandel)** um die Seite  **Neue Struktur die Produktkategorie (Einzelhandel)** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="9a7f7-107">In älteren Versionen wurden Produktattribute in Grundeigenschaften und Produktattribute Einzelhandel, basierend auf dem Bereich der Anwendbarkeit aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="9a7f7-108">Eigenschaften für Einzelhandelsprodukte waren *global*.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-108">Retail product properties were *global*.</span></span> <span data-ttu-id="9a7f7-109">Das bedeutet, dass für eine gegebene Produkteigenschaft derselbe Wert für alle juristischen Personen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="9a7f7-110">Grundprodukteigenschaften waren *entitätsspezifisch*.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="9a7f7-111">Das bedeutet, dass eine gegebene Produkteigenschaft in den juristischen Personen verschieden sein kann, basierend auf den einzelne geschäftlichen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="9a7f7-112">Mithilfe dieser Erweiterungen für Produktattribute in der Produktkategorie Einzelhandel trennen wir weiterhin die Felder, die auf der Grundlage ihrer Anwendbarkeit innerhalb einer Gruppe basieren, um die Details für freigegebene Produkte der Formularstruktur widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="9a7f7-113">Sie können zwischen dem Verwalten bestimmter Eigenschaften der Entität für alle juristischen Personen und dem Verwalten für eine bestimmte juristische Person wechseln.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="9a7f7-114">Wählen Sie einfach **Für alle juristischen Personen anzeigen/bearbeiten** oder **Für eine bestimmte juristische Person anzeigen/bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="9a7f7-115">Verkaufmanager können Standardwerte für einen zusätzlichen Satz Produktattribute auf der Ebene einer einzelnen Kategorie definieren.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="9a7f7-116">Diese Eigenschaftswerte werden durch ein Produkt, basierend auf deren Zuordnung zu einer Kategorie zum Zeitpunkt der Produkterstellung übernommen.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="9a7f7-117">Wählen Eigenschaften aus, um Produkte im Formular Produktkategorie (Einzelhandel) zu aktualisieren</span><span class="sxs-lookup"><span data-stu-id="9a7f7-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="9a7f7-118">Sie können logische Einheiten verwenden, um auszuwählen, welche Produktattribute für die zugehörigen Produkte aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="9a7f7-119">Verkaufmanager können diese übernommenen Produktattribute für die einzelnen Produkte ändern, um einzelnen geschäftlichen Bedarf abzudecken.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

