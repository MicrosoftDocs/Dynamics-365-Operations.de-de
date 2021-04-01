---
title: Berechnen einer Stückliste mithilfe einer Struktur mit mehreren Ebenen (Februar 2016)
description: Diese Prozedur zeigt, wie die Kosten eines fertigen Produkts berechnet werden, indem eine Auflösung mit mehreren Ebene verwendet wird, die auf dem Nachkalkulationsbogen beruht.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bbbc1e3c7941fd12991f1f6eaec4e9daf35fde9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239503"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="dd27c-103">Berechnen einer Stückliste mithilfe einer Struktur mit mehreren Ebenen (Februar 2016)</span><span class="sxs-lookup"><span data-stu-id="dd27c-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd27c-104">Diese Prozedur zeigt, wie die Kosten eines fertigen Produkts berechnet werden, indem eine Auflösung mit mehreren Ebene verwendet wird, die auf dem Nachkalkulationsbogen beruht.</span><span class="sxs-lookup"><span data-stu-id="dd27c-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="dd27c-105">Es ist die siebente Aufgabe in der Stücklistenberechnungsserie.</span><span class="sxs-lookup"><span data-stu-id="dd27c-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="dd27c-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="dd27c-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="dd27c-107">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="dd27c-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="dd27c-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="dd27c-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dd27c-109">Produkt-BOM_1 auswählen.</span><span class="sxs-lookup"><span data-stu-id="dd27c-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="dd27c-110">Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="dd27c-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="dd27c-111">Klicken Sie auf „Artikelpreis”.</span><span class="sxs-lookup"><span data-stu-id="dd27c-111">Click Item price.</span></span>
5. <span data-ttu-id="dd27c-112">Klicken Sie auf „Artikelkosten berechnen”.</span><span class="sxs-lookup"><span data-stu-id="dd27c-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="dd27c-113">Sie müssen möglicherweise auf die Auslassungspunkte (...) klicken, um diese Option im Hauptmenü anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dd27c-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="dd27c-114">Geben Sie im Feld „Nachkalkulationsversion” einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="dd27c-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="dd27c-115">Wählen Sie die Nachkalkulationsversion 20 aus, da sie ein Geplanter Kostentyp ist, und der Auflösungsmodus ist „Mehrere Ebenen”.</span><span class="sxs-lookup"><span data-stu-id="dd27c-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="dd27c-116">Der Auflösungsmodus „Mehrere Ebenen” ist für geplante Kosten und Simulationen.</span><span class="sxs-lookup"><span data-stu-id="dd27c-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="dd27c-117">Er wird nicht für Standardkosten verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd27c-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="dd27c-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="dd27c-118">Click OK.</span></span>
8. <span data-ttu-id="dd27c-119">Klicken Sie auf Berechnungsdetails anzeigen</span><span class="sxs-lookup"><span data-stu-id="dd27c-119">Click View calculation details.</span></span>
    * <span data-ttu-id="dd27c-120">Sie müssen möglicherweise auf die Auslassungspunkte (...) klicken, um diese Option im Hauptmenü anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dd27c-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="dd27c-121">In diesem Fall beachten Sie, wie BOM_2 berechnet wurde unter Berücksichtigung des Rohmaterials, Prozesses und des Mehraufwands mit einem Gesamtbetrag von 29,40 anstatt der Standardkosten von 10, die in dem ursprünglichen Aufgabenleitfaden in dieser Serie aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="dd27c-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="dd27c-122">Klicken Sie auf die Registerkarte „Nachkalkulationsbogen”.</span><span class="sxs-lookup"><span data-stu-id="dd27c-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="dd27c-123">Durch das Verschieben der Registerkarte „Nachkalkukationsbogen” sind die Summen pro Kostengruppe verschieden im Vergleich zur Berechnung, die im vorherigen Aufgabenleitfaden erfolgten.</span><span class="sxs-lookup"><span data-stu-id="dd27c-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="dd27c-124">Wählen Sie im Feld „Ebene” die Option „Mehrere” aus.</span><span class="sxs-lookup"><span data-stu-id="dd27c-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="dd27c-125">Wenn Sie „Mehrfach” auswählen, werden die Kosten gemäß der Anordnung von BOM_2 klassifiziert, wobei 10 von der M1-Kostengruppe (ITEM_C) abgeleitet ist und 15,60 von der Produktion, wobei die Kostengruppe L2 beträgt.</span><span class="sxs-lookup"><span data-stu-id="dd27c-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="dd27c-126">Indirekte Kosten variieren auch.</span><span class="sxs-lookup"><span data-stu-id="dd27c-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="dd27c-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dd27c-127">Close the page.</span></span>
12. <span data-ttu-id="dd27c-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dd27c-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]