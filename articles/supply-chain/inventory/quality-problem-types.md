---
title: Problemtypen für Qualitätsmängel
description: Dieses Thema beschreibt, wie Sie Problemtypen für Qualitätsmängel erstellen und verwenden.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 742edec8570610efe41a2c627efd1df586e0733e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022155"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="dde2b-103">Problemtypen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="dde2b-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dde2b-104">Dieses Thema beschreibt, wie Sie Problemtypen für Qualitätsmängel erstellen und verwenden.</span><span class="sxs-lookup"><span data-stu-id="dde2b-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="dde2b-105">Sie verwenden die Seite **Problemtypen**, um eine Klassifizierung der Qualitätsprobleme zu definieren, die bei den verschiedenen Qualitätsmangel-Typen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="dde2b-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="dde2b-106">Für jeden Problemtyp, den Sie erstellen, müssen Sie die Arten von Qualitätsmängeln angeben, mit denen der Problemtyp verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dde2b-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="dde2b-107">Sie können die folgenden Arten von Qualitätsmängeln festlegen:</span><span class="sxs-lookup"><span data-stu-id="dde2b-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="dde2b-108">**Intern** – Qualitätsmängel dieses Typs beziehen sich auf den Lagerbestand (z. B. Qualitätsprüfungsaufträge oder Quarantäneaufträge).</span><span class="sxs-lookup"><span data-stu-id="dde2b-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="dde2b-109">**Kunde** – Qualitätsmängel dieser Art beziehen sich auf Kundenaufträge.</span><span class="sxs-lookup"><span data-stu-id="dde2b-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="dde2b-110">**Lieferant** – Qualitätsmängel dieser Art beziehen sich auf Einkaufsbestellungen.</span><span class="sxs-lookup"><span data-stu-id="dde2b-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="dde2b-111">**Serviceanfrage** – Qualitätsmängel dieser Art beziehen sich auf Serviceaufträge.</span><span class="sxs-lookup"><span data-stu-id="dde2b-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="dde2b-112">**Produktion** – Qualitätsmängel dieser Art beziehen sich auf Batch-Aufträge oder Produktionsaufträge.</span><span class="sxs-lookup"><span data-stu-id="dde2b-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="dde2b-113">**Kuppelprodukt-Produktion** – Qualitätsmängel dieser Art beziehen sich auf Batch-Aufträge für Kuppelprodukte.</span><span class="sxs-lookup"><span data-stu-id="dde2b-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="dde2b-114">Wenn Sie einen neuen Problemtyp erstellen, wählen Sie **Qualitätsmangel-Typen** im Aktivitätsbereich, um eine Liste mit einem oder mehreren Qualitätsmangel-Typen zu erstellen, die für den Problemtyp zugelassen sind.</span><span class="sxs-lookup"><span data-stu-id="dde2b-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="dde2b-115">Ein Problemtyp, der sich auf einen Fehlercode bezieht, kann beispielsweise für alle Qualitätsmängel gelten.</span><span class="sxs-lookup"><span data-stu-id="dde2b-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="dde2b-116">Ein Problemtyp, der sich auf Reklamationen von Debitor bezieht, kann jedoch nur für die Typen **Kunde** und **Serviceanfrage** Qualitätsmangel gelten.</span><span class="sxs-lookup"><span data-stu-id="dde2b-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="dde2b-117">Beispiele für Problemtypen</span><span class="sxs-lookup"><span data-stu-id="dde2b-117">Examples of problem types</span></span>

<span data-ttu-id="dde2b-118">Hier sind einige Beispiele für Szenarien für Problemtypen, die mit den verschiedenen Qualitätsmängeln verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="dde2b-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="dde2b-119">**Kunde:** Ein Kunde hat eine Beschwerde eingereicht, ein Kunde hat eine Rücksendung gemacht, oder die Qualitätsvorgaben wurden nicht erfüllt.</span><span class="sxs-lookup"><span data-stu-id="dde2b-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="dde2b-120">**Lieferant:** Das Produkt war beschädigt, die Qualitätsspezifikationen wurden nicht erfüllt oder es wurde das falsche Produkt geliefert.</span><span class="sxs-lookup"><span data-stu-id="dde2b-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="dde2b-121">**Serviceanfrage:** Qualitätsvorgaben wurden nicht eingehalten, ein Kunde hat sich beschwert oder eine Maschinenwartung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dde2b-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="dde2b-122">**Produktion:** Die Qualitätsvorgaben wurden nicht erfüllt, eine Maschinenwartung ist erforderlich oder das Produkt wurde beschädigt.</span><span class="sxs-lookup"><span data-stu-id="dde2b-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="dde2b-123">**Kuppelprodukt-Produktion:** Die Qualitätsvorgaben wurden nicht eingehalten, eine Maschinenwartung ist erforderlich oder das Produkt wurde beschädigt.</span><span class="sxs-lookup"><span data-stu-id="dde2b-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="dde2b-124">Erstellen Sie einen Problemtyp und ordnen Sie ihn Qualitätsmängeln zu</span><span class="sxs-lookup"><span data-stu-id="dde2b-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="dde2b-125">Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätsmanagement \> Problemtypen**.</span><span class="sxs-lookup"><span data-stu-id="dde2b-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="dde2b-126">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dde2b-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="dde2b-127">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="dde2b-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="dde2b-128">**Problemtyp** – Geben Sie eine eindeutige ID oder einen Namen für den Problemtyp ein.</span><span class="sxs-lookup"><span data-stu-id="dde2b-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="dde2b-129">**Beschreibung** – Geben Sie eine detaillierte Beschreibung des Problemtyps ein.</span><span class="sxs-lookup"><span data-stu-id="dde2b-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="dde2b-130">Während die neue Zeile noch ausgewählt ist, wählen Sie **Nicht konforme Typen** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="dde2b-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="dde2b-131">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dde2b-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="dde2b-132">Legen Sie dann für die neue Zeile das Feld **Qualitätsmangel-Typ** auf den Qualitätsmangel-Typ fest, den Sie für den Problemtyp zulassen wollen.</span><span class="sxs-lookup"><span data-stu-id="dde2b-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="dde2b-133">Wiederholen Sie den vorherigen Schritt für jede zusätzliche Qualitätsmangel-Art, die Sie für die Problemart zulassen wollen.</span><span class="sxs-lookup"><span data-stu-id="dde2b-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="dde2b-134">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="dde2b-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dde2b-135">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dde2b-135">Additional resources</span></span>

- [<span data-ttu-id="dde2b-136">Qualitätsmanagement – Übersicht</span><span class="sxs-lookup"><span data-stu-id="dde2b-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="dde2b-137">Qualitäts- und Qualitätsmangel-Management aktivieren</span><span class="sxs-lookup"><span data-stu-id="dde2b-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="dde2b-138">Mitarbeiter, der für die Genehmigung von Qualitätsmängeln verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="dde2b-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="dde2b-139">Quarantänezonen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="dde2b-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="dde2b-140">Diagnosetypen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="dde2b-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="dde2b-141">Qualitätsbelastungen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="dde2b-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="dde2b-142">Vorgänge für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="dde2b-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="dde2b-143">Qualitätsmanagement für Lagerortprozesse</span><span class="sxs-lookup"><span data-stu-id="dde2b-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
