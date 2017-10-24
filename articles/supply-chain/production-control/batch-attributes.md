---
title: Chargenattribute
description: "Dieser Artikel enthält Informationen zu Chargenattributen. Chargenattribute sind Merkmale von Rohmaterialien und Fertigprodukten, aus denen sich die Lagerchargen zusammensetzen. Der Artikel beschreibt ausserdem, wie Chargenattribute zugeordnet und wie sie durchsucht werden können, wenn Sie Chargen reservieren."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0c3f5115377178941984e53749c18cc1c9179812
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="batch-attributes"></a><span data-ttu-id="a5d48-105">Chargenattribute</span><span class="sxs-lookup"><span data-stu-id="a5d48-105">Batch attributes</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a5d48-106">Dieser Artikel enthält Informationen zu Chargenattributen.</span><span class="sxs-lookup"><span data-stu-id="a5d48-106">This article provides information about batch attributes.</span></span> <span data-ttu-id="a5d48-107">Chargenattribute sind Merkmale von Rohmaterialien und Fertigprodukten, aus denen sich die Lagerchargen zusammensetzen.</span><span class="sxs-lookup"><span data-stu-id="a5d48-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="a5d48-108">Der Artikel beschreibt ausserdem, wie Chargenattribute zugeordnet und wie sie durchsucht werden können, wenn Sie Chargen reservieren.</span><span class="sxs-lookup"><span data-stu-id="a5d48-108">The article also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="a5d48-109">Chargenattribute sind Merkmale von Rohmaterialien und Fertigprodukten, aus denen sich die Lagerchargen zusammensetzen.</span><span class="sxs-lookup"><span data-stu-id="a5d48-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="a5d48-110">Chargenattribute können sich abhängig von verschiedenen Faktoren unterscheiden, wie etwa den Umgebungsbedingungen, der Qualität des für die Produktion der Charge verwendeten Rohmaterials oder des Ergebnisses des fertigen Produkts.</span><span class="sxs-lookup"><span data-stu-id="a5d48-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="a5d48-111">Die Anzahl und Typen der verwendeten Chargenattribute sind stark branchenabhängig.</span><span class="sxs-lookup"><span data-stu-id="a5d48-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="a5d48-112">Nachfolgend finden Sie zwei Beispiele zur Verwendung von Chargenattributen:</span><span class="sxs-lookup"><span data-stu-id="a5d48-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="a5d48-113">Bei der Käseherstellung werden der Milch als einem der Rohstoffe zur Herstellung von Käse Attribute wie Fettgehalt und Gewichtsanteil des Fetts in Prozent zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a5d48-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="a5d48-114">Dem mithilfe der Milch hergestellten Käse können zusätzliche Attribute wie Feuchtigkeit und Alter zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a5d48-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="a5d48-115">In der stahlverarbeitenden Industrie besitzt das produzierte Eisen möglicherweise Attribute wie die prozentualen Magnesium-, Silber- und Zinkanteile.</span><span class="sxs-lookup"><span data-stu-id="a5d48-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="a5d48-116">Um die Anzahl und Typen von Attributen besser zu verwalten, können Sie Chargenattributgruppen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a5d48-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="a5d48-117">Auf diese Weise müssen Sie nicht jedes Attribut einzeln hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a5d48-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="a5d48-118">Zuweisen von Chargenattributen</span><span class="sxs-lookup"><span data-stu-id="a5d48-118">Assign batch attributes</span></span>
<span data-ttu-id="a5d48-119">Chargenattribute können einzelnen Produkten, die sich in Lagerchargen befinden, oder Produkten zugewiesen werden, die bestimmten Debitoren zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a5d48-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="a5d48-120">Ein Chargenattribut kann erst auf Debitorenebene zugeordnet werden, wenn es auf Produktebene zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="a5d48-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="a5d48-121">Für das Produkt muss die Chargendimension in der Rückverfolgungsangabengruppe **Aktiv** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a5d48-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="a5d48-122">Weisen Sie ein Chargenattribut zu einem einzelnen Produkt mithilfe der produktspezifischen Seite zu.</span><span class="sxs-lookup"><span data-stu-id="a5d48-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="a5d48-123">Ist das Attribut spezifisch für ein Produkt eines Debitors, verwenden Sie die debitorenspezifische Seite.</span><span class="sxs-lookup"><span data-stu-id="a5d48-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="a5d48-124">Beim Hinzufügen eines Attributs zu einem Produkt legen Sie außerdem folgende Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="a5d48-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="a5d48-125">Nachfolgend finden Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="a5d48-125">Here are some examples:</span></span>

-   <span data-ttu-id="a5d48-126">Die Bereiche für Mindest- und Höchstwerte für ein Attribut vom Typ **Ganze Zahl** oder **Bruch**.</span><span class="sxs-lookup"><span data-stu-id="a5d48-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="a5d48-127">Die Toleranzaktionen für Attribute vom Typ **Ganze Zahl** oder **Bruch**.</span><span class="sxs-lookup"><span data-stu-id="a5d48-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="a5d48-128">Die von Ihnen ausgewählte Aktivität kann eine Warnmeldung oder eine Fehlermeldung sein, falls das Attribut nicht im Bereich für Mindest- und Höchstwerte liegt.</span><span class="sxs-lookup"><span data-stu-id="a5d48-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="a5d48-129">Der Zielwert des Attributs.</span><span class="sxs-lookup"><span data-stu-id="a5d48-129">The target value for the attribute.</span></span> <span data-ttu-id="a5d48-130">Dieser Wert ist der optimale Wert des Attributs. Er gilt für alle Attributtypen.</span><span class="sxs-lookup"><span data-stu-id="a5d48-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="a5d48-131">Sie können auf diese Seiten für Produkte zugreifen, die Sie auf der Seite **Freigegebene Produkte** unter Produktinformationsverwaltung auswählen.</span><span class="sxs-lookup"><span data-stu-id="a5d48-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="a5d48-132">Nach dem Zuweisen von Chargenattributen zu einem Produkt können Sie den Attributen auf der Seite **Lagerchargenattribute** bestimmte Werte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a5d48-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="a5d48-133">Reservieren von Chargen</span><span class="sxs-lookup"><span data-stu-id="a5d48-133">Reserve batches</span></span>
<span data-ttu-id="a5d48-134">Sie können nach Chargenattributen suchen, wenn Sie Stapelreservierungen zur Erfüllung eines Debitorenauftrags vornehmen oder wenn Sie Chargen für einen Produktionsauftrag entnehmen und reservieren.</span><span class="sxs-lookup"><span data-stu-id="a5d48-134">You can search on batch attributes when you do batch reservations for a sales order to fullfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="a5d48-135">Mit dieser Suche können Sie eine Lagercharge ausfindig machen, die das Produkt mit den gewünschten Chargenattributen enthält.</span><span class="sxs-lookup"><span data-stu-id="a5d48-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="a5d48-136">Nachdem Sie die Charge oder Chargen gefunden haben, können Sie das Produkt in der erstellten Lagerbuchungsposition reservieren.</span><span class="sxs-lookup"><span data-stu-id="a5d48-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>




