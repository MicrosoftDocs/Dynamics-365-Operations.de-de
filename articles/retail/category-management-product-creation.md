---
title: Verwalten von Produktkategorien (Retail) und Produkten
description: In diesem Thema wird beschrieben, wie Verkaufmanager Produktkategorien (Retail) verwenden können, um Beziehungen zwischen der Produkthierarchie (Retail) und freigegebenen Produktdetails zu verwalten.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0bcc5989edd9913fce414c0c24068f111d8c1aeb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "344684"
---
# <a name="manage-retail-product-categories-and-products"></a><span data-ttu-id="aae24-103">Verwalten von Produktkategorien (Retail) und Produkten</span><span class="sxs-lookup"><span data-stu-id="aae24-103">Manage Retail product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="aae24-104">Dieses Thema beschreibt eine erweiterte Art, Retail-Produktkategorien und -Produkte in Microsoft Dynamics 365 for Retail zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="aae24-104">This topic describes an enhanced way to manage Retail product categories and products in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="aae24-105">Mit diesen Erweiterungen können Verkaufsmanager eine Struktur von Produkteigenschaften anzeigen, die von der Produkthierarchie (Retail) und freigegebenen Produktdetails geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="aae24-105">The enhancements let merchandising managers view a structure of product properties that is shared between the Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="aae24-106">Um mehr darüber zu erfahren, wie Produktkategorien (Retail) im Arbeitsbereich **Kategorie und Produktverwaltung** verwaltet werden, wählen Sie die Kachel **Produkthierarchie (Retail)** aus.</span><span class="sxs-lookup"><span data-stu-id="aae24-106">To learn more about how to manage Retail product categories, in the **Category and product management** workspace, select the **Retail product hierarchy** tile.</span></span>

<span data-ttu-id="aae24-107">Beachten Sie die erweiterte Struktur auf der Seite **Produkthierarchie (Retail)**, die angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="aae24-107">Notice the enhanced structure of the **Retail product hierarchy** page that appears.</span></span> <span data-ttu-id="aae24-108">In älteren Versionen von Retail wurden Produkteigenschaften in *Produktgrundeigenschaften* und *Produkteigenschaften (Retail)*, basierend auf dem Umfang ihrer Anwendbarkeit aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="aae24-108">In previous versions of Retail, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="aae24-109">Produkteigenschaften (Retail) sind *global* in ihrem Umfang der Anwendbarkeit.</span><span class="sxs-lookup"><span data-stu-id="aae24-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="aae24-110">Das bedeutet, dass für eine gegebene Produkteigenschaft (Retail) derselbe Wert für alle juristischen Personen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aae24-110">In other words, for a given Retail product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="aae24-111">Produktgrundeigenschaften sind jedoch jeweils *für juristische Personen spezifisch*.</span><span class="sxs-lookup"><span data-stu-id="aae24-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="aae24-112">Das bedeutet, dass für eine gegebene Produktgrundeigenschaft der Wert je nach juristischer Person verschieden sein kann, basierend auf den einzelne geschäftlichen Anforderungen jeder juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="aae24-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="aae24-113">In der erweiterten Produktkategoriestruktur (Retail) werden Produkteigenschaften logisch getrennt, basierend auf ihrer Anwendbarkeit in einer Gruppe, um die Struktur der Formularstruktur für freigegebene Produktdetails widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="aae24-113">In the enhanced Retail product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Felder, die auf Grundlage des Umfangs der Anwendbarkeit der Eigenschaften gruppiert sind](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="aae24-115">Sie können zwischen dem Verwalten von Eigenschaften, die für juristische Personen spezifisch sind, über alle juristischen Personen hinweg und dem Verwalten davon für eine bestimmte juristische Person wechseln.</span><span class="sxs-lookup"><span data-stu-id="aae24-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="aae24-116">Um Eigenschaften für alle juristischen Personen zu verwaltet, wählen Sie **Ansicht für alle juristischen Personen** (oder **Bearbeiten für alle juristischen Personen**) aus.</span><span class="sxs-lookup"><span data-stu-id="aae24-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Anzeigen/Bearbeiten für alle juristische Personen](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="aae24-118">Um Eigenschaften für eine bestimmte juristische Person zu verwalten, wählen Sie **Ansicht für eine bestimmte juristische Person** (oder **Bearbeiten für eine bestimmte juristische Person**) aus.</span><span class="sxs-lookup"><span data-stu-id="aae24-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Anzeigen/Bearbeiten für eine bestimmte juristische Person](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="aae24-120">In der erweiterten Produktkategoriestruktur kann darüber hinaus ein Verkaufsmanager jetzt Standardwerte für einen zusätzlichen Satz Produktattribute auf der Ebene einer einzelnen Kategorie definieren.</span><span class="sxs-lookup"><span data-stu-id="aae24-120">Additionally, in the enhanced Retail product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="aae24-121">Wenn dann die Produkt erstellt werden, erben sie die Standardwerte für ihre Produkteigenschaften basierend auf der Zuordnung dieser Eigenschaften mit einer einzelnen Kategorie in der Produkthierarchie (Retail).</span><span class="sxs-lookup"><span data-stu-id="aae24-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in Retail product hierarchy.</span></span> <span data-ttu-id="aae24-122">Diese geerbten Produkteigenschaften können auch für jedes Produkt geändert werden, um einzelnen geschäftlichen Bedarf abzudecken.</span><span class="sxs-lookup"><span data-stu-id="aae24-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a><span data-ttu-id="aae24-123">Auswählen von Eigenschaften zum Aktualisieren von Produkten auf der Seite „Produkthierarchie (Retail)”.</span><span class="sxs-lookup"><span data-stu-id="aae24-123">Selecting properties to update products on the Retail product hierarchy page</span></span>

<span data-ttu-id="aae24-124">Sie können die neue erweiterte Struktur für Produkteigenschaften verwenden, um aktualisierte Produkteigenschaften auszuwählen, die an die zugeordneten Produkte mit Push übertragen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="aae24-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="aae24-125">Wählen Sie auf der Seite **Produkthierarchie (Retail)** im Aktivitätsbereich die Option **Kategorie** aus, und wählen Sie dann **Produkte aktualisieren**, um das Dialogfeld **Produkte aktualisieren** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aae24-125">On the **Retail product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Das Produktedialogfeld aktualisieren](media/NewUpdateProductsEnhancedView.PNG)
