--- 
title: "Berechnen einer Stückliste mithilfe einer Struktur mit einer Ebene (nur Februar 2016)"
description: "Diese Prozedur zeigt, wie die Kosten eines fertigen Produkts berechnet werden, indem eine Auflösung mit einer einzelnen Ebene verwendet wird, die auf dem Nachkalkulationsbogen beruht."
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1def2baf6a42ae4f8d117b4c06f402397b83bf88
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a><span data-ttu-id="02371-103">Berechnen einer Stückliste mithilfe einer Struktur mit einer Ebene (nur Februar 2016)</span><span class="sxs-lookup"><span data-stu-id="02371-103">Calculate a BOM by using a single level structure (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="02371-104">Diese Prozedur zeigt, wie die Kosten eines fertigen Produkts berechnet werden, indem eine Auflösung mit einer einzelnen Ebene verwendet wird, die auf dem Nachkalkulationsbogen beruht.</span><span class="sxs-lookup"><span data-stu-id="02371-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="02371-105">Dies ist die sechste Aufgabe in der Stücklistenberechnungsserie.</span><span class="sxs-lookup"><span data-stu-id="02371-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="02371-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="02371-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="02371-107">Wechseln Sie zu "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="02371-107">Go to Released products.</span></span>
2. <span data-ttu-id="02371-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="02371-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="02371-109">Produkt-BOM_1 auswählen.</span><span class="sxs-lookup"><span data-stu-id="02371-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="02371-110">Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="02371-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="02371-111">Klicken Sie auf „Artikelpreis”.</span><span class="sxs-lookup"><span data-stu-id="02371-111">Click Item price.</span></span>
5. <span data-ttu-id="02371-112">Klicken Sie auf „Artikelkosten berechnen”.</span><span class="sxs-lookup"><span data-stu-id="02371-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="02371-113">Sie müssen möglicherweise auf die Auslassungspunkte (...) klicken, um diese Option im Hauptmenü anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="02371-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="02371-114">Klicken Sie im Feld „Nachkalkulationsversion” auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="02371-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="02371-115">Wählen Sie für diese Demo 10 aus.</span><span class="sxs-lookup"><span data-stu-id="02371-115">For this demo, select 10.</span></span> <span data-ttu-id="02371-116">Dies ist die gleiche Nachkalkulationsversion, die zum Hinzufügen des Einstandspreis zu den Komponenten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="02371-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="02371-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="02371-117">Click OK.</span></span>
8. <span data-ttu-id="02371-118">Klicken Sie auf Berechnungsdetails anzeigen</span><span class="sxs-lookup"><span data-stu-id="02371-118">Click View calculation details.</span></span>
    * <span data-ttu-id="02371-119">Sie müssen möglicherweise auf die Auslassungspunkte (...) klicken, um diese Option im Hauptmenü anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="02371-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="02371-120">Hier ist die Zusammenstellung der Kosten:   •    10 ist von ARTIKEL_A, 10 % von ARTIKEL_B, 10 % von BOM_2 berechnet.</span><span class="sxs-lookup"><span data-stu-id="02371-120">Here's the composition of the cost:  •    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="02371-121">In diesem Fall gibt es keine Details für BOM_2, da sie als Standardkosten von 10 eingegeben wurde, aber es erfolgte nicht durch Berechnung.</span><span class="sxs-lookup"><span data-stu-id="02371-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="02371-122">•  7 ist von der Rüstzeit abgeleitet, welche konstante Kosten sind und zusätzliche 7 sind vom Laufzeitvorgang (Prozess) abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="02371-122">•  7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="02371-123">•   Es gibt auch andere Beträge, die den indirekten Kosten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="02371-123">•   There are also other amounts that correspond to indirect costs.</span></span>  
9. @SysTaskRecorder:_RequestClose


