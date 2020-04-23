---
title: Voraussetzungen für die Standardkostenübersicht
description: In diesem Thema werden die grundlegenden Schritte zur Verwendung von Standardkosten beschrieben.
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f66f7061c608379689016e3c0b9c5ba4ad23dc9e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214511"
---
# <a name="prerequisites-for-standard-costs-overview"></a><span data-ttu-id="b1f1c-103">Voraussetzungen für die Standardkostenübersicht</span><span class="sxs-lookup"><span data-stu-id="b1f1c-103">Prerequisites for standard costs overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1f1c-104">In diesem Thema werden die grundlegenden Schritte zur Verwendung von Standardkosten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="b1f1c-105">Die weiteren Schritte hängen von den Arbeitsgängen des Unternehmens ab.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="b1f1c-106">Diese Schritte unterscheiden sich beispielsweise bei einer Umgebung ohne Produktion, bei einer Produktionsumgebung, in der keine Routings verwendet werden, und bei einer Produktionsumgebung mit Routings.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="b1f1c-107">Gehen Sie zum Einrichten von Standardkosten folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="b1f1c-108">**1. Erstellen Sie eine Artikelmodellgruppe für Standardkosten.**</span><span class="sxs-lookup"><span data-stu-id="b1f1c-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="b1f1c-109">Erstellen Sie mithilfe der Seite **Artikelmodellgruppe** eine neue Gruppe für Standardkosten, und weisen Sie ein Lagermodell vom Typ **Standardkosten** zu.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="b1f1c-110">Geben Sie für die Artikelmodellgruppe einen aussagekräftigen Bezeichner, wie beispielsweise **Standardkosten** an.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="b1f1c-111">Legen Sie durch Aktivieren der Kontrollkästchen fest, dass für die Gruppe wertmäßig negativer Bestand, das Buchen physischen Bestands sowie das Buchen wertmäßigen Bestands zulässig sein soll.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="b1f1c-112">Diese Standardkostengruppe wird Artikeln zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="b1f1c-113">**2. Definieren Sie Sachkonten, die sich auf Standardkostenabweichungen beziehen.**</span><span class="sxs-lookup"><span data-stu-id="b1f1c-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="b1f1c-114">Definieren Sie mithilfe der Seite **Kontenplan** Sachkonten, die sich auf Standardkostenabweichungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="b1f1c-115">Diese Sachkonten müssen zunächst definiert werden, damit sie auf der Seite **Buchung** zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="b1f1c-116">Sachkonten können sowohl für Artikelgruppen als auch für Kostengruppen stehen.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="b1f1c-117">**3. Weisen Sie Artikelbuchungen, die sich auf Standardkostenabweichungen beziehen, Sachkonten zu.**</span><span class="sxs-lookup"><span data-stu-id="b1f1c-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="b1f1c-118">Weisen Sie mithilfe der Seite **Buchung** die Sachkonten zu, die sich auf Standardkostenabweichungen beziehen.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="b1f1c-119">Sie können das Sachkonto einer Abweichung gemäß Artikel (oder Artikelgruppe) und Kostengruppe (oder Kostengruppentyp) angeben, oder Sie können angeben, dass das Sachkonto für alle Artikel und Kostengruppen gilt.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="b1f1c-120">Diese Optionen entsprechen den Kostenbeziehungen für „Tabellen”, „Gruppen” oder „Alle”.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="b1f1c-121">Bevor Sie die Artikelbuchungsregeln definieren, verwenden Sie die Seite **Buchungskombinationen**, um Kostenbeziehungen (für Tabellen, Gruppen und Alle) zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="b1f1c-122">**4. Definieren Sie Lagerparameter, die sich auf Standardkosten beziehen.**</span><span class="sxs-lookup"><span data-stu-id="b1f1c-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="b1f1c-123">Definieren Sie mithilfe der Registerkarte **Bestandbuchhaltung** auf der Seite **Bestandbuchhaltungsrichtlinie einrichten > Parameter** zwei Kostensteuerungsparameter, die sich auf Standardkosten beziehen.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-123">Use the **Inventory accounting** tab on the **Inventory accounting policies setup > Parameters** page to define two cost control parameters that are related to standard costs.</span></span>

    -  <span data-ttu-id="b1f1c-124">Wählen Sie im Feld **Kostenaufschlüsselung** die Option **Keine** oder **Untergeordnetes Sachkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="b1f1c-125">Wenn Sie **Untergeordnetes Sachkonto** auswählen, ist die Kostenaufschlüsselung eine *aktive* Kostenaufschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="b1f1c-126">Eine aktive Kostenaufschlüsselung ist von entscheidender Bedeutung für die übergreifende Berechnung, Beibehaltung und Anzeige der Kostengruppensegmentierung in einer mehrstufigen Produktstruktur für Standardkostenartikel.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="b1f1c-127">Bei aktiver Kostenaufschlüsselung lassen sich Lagerbestand, Umlaufbestand (Ressourcen in Fertigung, RIF) sowie Wareneinsatz (Cost Of Goods Sold, COGS) pro Kostengruppe in einem einstufigen, mehrstufigen oder in einem Gesamtformat melden und analysieren.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="b1f1c-128">Sofern die Kostenaufschlüsselung aktiv ist, wenn Sie die Kosten eines produzierten Artikels aktivieren, wird die Kostengruppensegmentierung im Kostendatensatz des Artikels gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="b1f1c-129">Wenn Sie **Keine** auswählen, wird die Kostengruppensegmentierung für Standardkostenartikel nicht verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="b1f1c-130">Das bedeutet, dass die Standardkosten eines produzierten Artikels als einzelner Betrag berechnet und verwaltet werden, ohne Kostengruppensegmentierung.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="b1f1c-131">Die Kostenbeiträge produzierter Komponenten werden in einem einzelnen Betrag zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="b1f1c-132">Wählen Sie im Feld **Abweichungen vom Standard** die Option **Zusammengefasst** oder **Pro Kostengruppe** aus.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="b1f1c-133">Wenn Sie die Option **Pro Kostengruppe** auswählen, können Sie Einkaufspreisabweichungen und Produktionsabweichungen nach Kostengruppe identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="b1f1c-134">Sie können auch die vier Arten von Produktionsabweichungen identifizieren: die Losgröße, Menge, Preis und Ersatzabweichungen.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="b1f1c-135">Bei Auswahl von **Zusammengefasst** sind keine Abweichungen nach Kostengruppe ersichtlich, und auch die Erkennung der vier Typen von Produktionsabweichungen ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="b1f1c-136">Sie können lediglich eine zusammengefasste Produktionsabweichung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="b1f1c-137">Die Richtlinie für Abweichungen vom Standard ist unabhängig von der Richtlinie für die Kostenaufschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="b1f1c-138">Anders ausgedrückt können Sie eine Kostenaufschlüsselungsrichtlinie von **Keine** auswählen und Abweichungen pro Kostengruppe auswählen, sodass die Produktionsabweichungen pro Kostengruppe immer noch erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="b1f1c-139">**5. Erstellen Sie Nachkalkulationsversionen für Standardkosten.**</span><span class="sxs-lookup"><span data-stu-id="b1f1c-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="b1f1c-140">Erstellen Sie mithilfe der Seite **Nachkalkulationsversionssetup** mindestens eine Nachkalkulationsversion für Standardkosten.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="b1f1c-141">Jede Nachkalkulationsversion muss mit dem Nachkalkulationstyp **Standardkosten** versehen werden. Darüber hinaus muss für den Inhalt die Berücksichtigung von Kostendaten ermöglicht werden.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="b1f1c-142">**6. Bereiten Sie für einen vorhandenen Kunden die Verwendung von Standardkosten vor.**</span><span class="sxs-lookup"><span data-stu-id="b1f1c-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="b1f1c-143">Kunden, die ihre vorhandenen Artikel auf ein Lagermodell vom Typ „Standardkosten” umstellen möchten, benötigen dafür die Seite **Standardkostenumrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="b1f1c-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="b1f1c-144">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="b1f1c-144">Related topics</span></span>
--------

[<span data-ttu-id="b1f1c-145">Standardkostenumrechnung – Überblick</span><span class="sxs-lookup"><span data-stu-id="b1f1c-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)

### <a name="blogs"></a><span data-ttu-id="b1f1c-146">Blogs</span><span class="sxs-lookup"><span data-stu-id="b1f1c-146">Blogs</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="b1f1c-147">Communityblogs</span><span class="sxs-lookup"><span data-stu-id="b1f1c-147">Community blogs</span></span>

- [<span data-ttu-id="b1f1c-148">So richten SieStandardkosten für Direktmaterialien in Dynamics 365 for Finance and Operations ein</span><span class="sxs-lookup"><span data-stu-id="b1f1c-148">How to set up standard costs for direct materials in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [<span data-ttu-id="b1f1c-149">Standardmäßige direkte Lohnkosten in Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1f1c-149">Standard direct labor costs in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)
