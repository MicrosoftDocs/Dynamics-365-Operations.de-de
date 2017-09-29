---
title: Lagerortarbeitsrichtlinien
description: "Lagerortarbeitsrichtlinien steuern, ob Lagerortarbeit nach Lagerortprozesse in der Fertigung auf Grundlage Arbeitsauftragstyp, Lagerplatz für Lagerbestand und Produkt erstellt wird."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ec7dd3b91851729e866bc90ca85a118839f9d71d
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---

# <a name="warehouse-work-policies"></a><span data-ttu-id="457f8-103">Lagerortarbeitsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="457f8-103">Warehouse work policies</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="457f8-104">Lagerortarbeitsrichtlinien in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition steuern, ob Lagerortarbeit nach Lagerortprozesse in der Fertigung auf Grundlage Arbeitsauftragstyp, Lagerplatz für Lagerbestand und Produkt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="457f8-104">Warehouse work policies in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="457f8-105">Diese Arbeitsrichtlinie steuert, ob Lagerortarbeit für Lagerortprozesse in der Fertigung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="457f8-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="457f8-106">Sie können die Arbeitsrichtlinie einrichten, indem Sie eine Kombination von **Arbeitsauftragstypen**, einen **Bestandslagerbestand** und ein **Produkt** verwenden.</span><span class="sxs-lookup"><span data-stu-id="457f8-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="457f8-107">Beispielsweise wird Produkt L0101 dem Ausgangslagerplatz 001 als fertig gemeldet.</span><span class="sxs-lookup"><span data-stu-id="457f8-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="457f8-108">Das Endprodukt wird später in einem anderen Produktionsauftrag an Ausgangslagerplatz 001 verbraucht.</span><span class="sxs-lookup"><span data-stu-id="457f8-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="457f8-109">In diesem Fall können Sie eine Arbeitsrichtlinie einrichten, um zu verhindern, dass fertige eingelagerte Waren erstellt werden, wenn Sie Produkt L0101 dem Ausgangslagerort 001 als fertig melden.</span><span class="sxs-lookup"><span data-stu-id="457f8-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="457f8-110">Die Arbeitsrichtlinie ist eine einzelne Entität, die durch die folgenden Informationen beschrieben werden kann:</span><span class="sxs-lookup"><span data-stu-id="457f8-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="457f8-111">**Arbeitsrichtlinienname**(der eindeutige Bezeichner der Arbeitsrichtlinie)</span><span class="sxs-lookup"><span data-stu-id="457f8-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="457f8-112">**Arbeitsauftragstypen** und **Arbeitserstellungsmethode**</span><span class="sxs-lookup"><span data-stu-id="457f8-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="457f8-113">**Lagerplätze für Lagerbestand**</span><span class="sxs-lookup"><span data-stu-id="457f8-113">**Inventory locations**</span></span>
-   <span data-ttu-id="457f8-114">**Produkte**</span><span class="sxs-lookup"><span data-stu-id="457f8-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="457f8-115">Arbeitsauftragstypen</span><span class="sxs-lookup"><span data-stu-id="457f8-115">Work order types</span></span>
<span data-ttu-id="457f8-116">Sie können die folgenden Arbeitsauftragstypen auswählen:</span><span class="sxs-lookup"><span data-stu-id="457f8-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="457f8-117">Einlagerung von Fertigerzeugnissen</span><span class="sxs-lookup"><span data-stu-id="457f8-117">Finished goods put away</span></span>
-   <span data-ttu-id="457f8-118">Einlagerung von Kuppel- und Nebenprodukten</span><span class="sxs-lookup"><span data-stu-id="457f8-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="457f8-119">Rohmaterialentnahme</span><span class="sxs-lookup"><span data-stu-id="457f8-119">Raw material picking</span></span>

<span data-ttu-id="457f8-120">Das Feld **Arbeitserstellungsmethode** hat den Wert **Nie**.</span><span class="sxs-lookup"><span data-stu-id="457f8-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="457f8-121">Dieser Wert gibt an, dass die Arbeitsrichtlinie verhindert, dass Lagerortarbeit für den ausgewählten Arbeitsauftragstyp erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="457f8-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="457f8-122">Lagerplätze für Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="457f8-122">Inventory locations</span></span>
<span data-ttu-id="457f8-123">Sie können einen Lagerplatz auswählen, für den die Arbeitsrichtlinie gilt.</span><span class="sxs-lookup"><span data-stu-id="457f8-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="457f8-124">Wenn keinem Lagerplatz eine Arbeitsrichtlinie zugeordnet wird, gilt die Arbeitsrichtlinie für keine Prozesse.</span><span class="sxs-lookup"><span data-stu-id="457f8-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="457f8-125">Auf der Seite **Lagerplätze** können Sie die Auswahl der Arbeitsrichtlinie für einen bestimmten Lagerplatz auswählen oder stornieren.</span><span class="sxs-lookup"><span data-stu-id="457f8-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="457f8-126">Produkte</span><span class="sxs-lookup"><span data-stu-id="457f8-126">Products</span></span>
<span data-ttu-id="457f8-127">Sie können ein Produkt auswählen, für den die Arbeitsrichtlinie gilt.</span><span class="sxs-lookup"><span data-stu-id="457f8-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="457f8-128">Sie können die Arbeitsrichtlinie entweder auf alle oder auf ausgewählte Produkte anwenden.</span><span class="sxs-lookup"><span data-stu-id="457f8-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="457f8-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="457f8-129">Example</span></span>
<span data-ttu-id="457f8-130">Im folgenden Beispiel gibt es zwei Produktionsaufträge, PRD-001 und PRD-00*2*.</span><span class="sxs-lookup"><span data-stu-id="457f8-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="457f8-131">Produktionsauftrag PRD-001 hat einen Arbeitsgang, der als **Montage** bezeichnet wird, wo Produkt SC1 an Lagerplatz O1 als fertig gestellt gemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="457f8-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="457f8-132">Produktionsauftrag PRD-002 hat einen Arbeitsgang, der als **Anstrich** bezeichnet wird und bei dem Produkt SC1 von Lagerplatz O1 verbraucht wird.</span><span class="sxs-lookup"><span data-stu-id="457f8-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="457f8-133">Produktionsauftrag PRD-002 verbraucht auch Rohmaterial RM1 von Lagerplatz O1.</span><span class="sxs-lookup"><span data-stu-id="457f8-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="457f8-134">RM1 wird am Lagerort BULK-001 gespeichert und wird an Lagerplatz O1 durch Lagerortarbeit für Rohmaterialentnahme entnommen.</span><span class="sxs-lookup"><span data-stu-id="457f8-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="457f8-135">Die Entnahmearbeit wird generiert, wenn die Produktion PRD-002 freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="457f8-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="457f8-136">[![Lagerortarbeitsrichtlinien](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="457f8-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="457f8-137">Wenn Sie planen, eine Lagerort-Arbeitsrichtlinie dieses Szenarios zu konfigurieren, sollten Sie die folgenden Informationen berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="457f8-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="457f8-138">Lagerortarbeit für die Einlagerung von Fertigerzeugnissen ist nicht erforderlich, wenn Sie Produkt SC1 aus Produktionsauftrag PRD-001 zum Lagerplatz O1 als fertig gestellt melden.</span><span class="sxs-lookup"><span data-stu-id="457f8-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="457f8-139">Dies liegt daran, dass beim Arbeitsgang **Anstrich** für Produktionsauftrag PRD-002 das Produkt SC1 am selben Lagerplatz benutzt wird.</span><span class="sxs-lookup"><span data-stu-id="457f8-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="457f8-140">Lagerortarbeit für Rohmaterialentnahme ist erforderlich, um Rohmaterial RM1 vom Lagerort BULK-001 zum Lagerplatz O1 zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="457f8-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="457f8-141">Hier ist ein Beispiel der Arbeitsrichtlinie, die Sie einrichten können, basierend auf diesen Überlegungen.</span><span class="sxs-lookup"><span data-stu-id="457f8-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
|<span data-ttu-id="457f8-142">**Name für Arbeitsrichtlinien**</span><span class="sxs-lookup"><span data-stu-id="457f8-142">**Work policy name**</span></span><br>                 |<span data-ttu-id="457f8-143">**Arbeitsauftragstypen**</span><span class="sxs-lookup"><span data-stu-id="457f8-143">**Work order types**</span></span><br>                               |
| <span data-ttu-id="457f8-144">Kein Einlagern von 01     \`</span><span class="sxs-lookup"><span data-stu-id="457f8-144">No put away 01     \`</span></span>                    |<span data-ttu-id="457f8-145">- Einlagerung von Fertigerzeugnissen</span><span class="sxs-lookup"><span data-stu-id="457f8-145">- Finished good put away</span></span><br>                           |
|                                         |<span data-ttu-id="457f8-146">**Lagerplätze**</span><span class="sxs-lookup"><span data-stu-id="457f8-146">**Locations**</span></span><br>                                      |
|                                         |<span data-ttu-id="457f8-147">- O1</span><span class="sxs-lookup"><span data-stu-id="457f8-147">- O1</span></span>   |                                               |
|                                         |<span data-ttu-id="457f8-148">**Produkte**</span><span class="sxs-lookup"><span data-stu-id="457f8-148">**Products**</span></span> <br>                                      |
|                                         |<span data-ttu-id="457f8-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="457f8-149">- SC1</span></span>                                                  |

<span data-ttu-id="457f8-150">Die folgenden Prozeduren bieten Schritt-für-Schritt-Anweisungen zum Einrichten der Lagerort-Arbeitsrichtlinie für dieses Szenario.</span><span class="sxs-lookup"><span data-stu-id="457f8-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="457f8-151">Ein Beispielsetup, das zeigt, wie ein Produktionsauftrag an einen Lagerplatz als fertig gestellt gemeldet wird, der nicht kennzeichengesteuert ist, wird ebenfalls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="457f8-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="457f8-152">Eine Lagerort-Arbeitsrichtlinie einrichten</span><span class="sxs-lookup"><span data-stu-id="457f8-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="457f8-153">Lagerortprozesse enthalten nicht immer Lagerortarbeit.</span><span class="sxs-lookup"><span data-stu-id="457f8-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="457f8-154">Wenn Sie eine Arbeitsrichtlinie definieren, können Sie die Erstellung von Arbeit für Rohmaterialentnahme sowie die Einlagerung fertiger Waren für einen Satz von Produkten an bestimmten Lagerplätzen verhindern.</span><span class="sxs-lookup"><span data-stu-id="457f8-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="457f8-155">Das Demodatenunternehmen USMF wurde verwendet, um diese Prozedur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="457f8-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="457f8-156">SCHRITTE (21)</span><span class="sxs-lookup"><span data-stu-id="457f8-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="457f8-157">1.</span><span class="sxs-lookup"><span data-stu-id="457f8-157">1.</span></span>  | <span data-ttu-id="457f8-158">Wechseln Sie zu "Lagerortverwaltung" &gt; "Einstellungen" &gt; "Arbeit" &gt; "Arbeitsrichtlinien".</span><span class="sxs-lookup"><span data-stu-id="457f8-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="457f8-159">2.</span><span class="sxs-lookup"><span data-stu-id="457f8-159">2.</span></span>  | <span data-ttu-id="457f8-160">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="457f8-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="457f8-161">3.</span><span class="sxs-lookup"><span data-stu-id="457f8-161">3.</span></span>  | <span data-ttu-id="457f8-162">Geben Sie im Feld "Arbeitsrichtlinienname" die Bezeichnung "Keine Einlagerungsarbeit" ein.</span><span class="sxs-lookup"><span data-stu-id="457f8-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="457f8-163">4.</span><span class="sxs-lookup"><span data-stu-id="457f8-163">4.</span></span>  | <span data-ttu-id="457f8-164">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="457f8-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="457f8-165">5.</span><span class="sxs-lookup"><span data-stu-id="457f8-165">5.</span></span>  | <span data-ttu-id="457f8-166">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="457f8-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="457f8-167">6.</span><span class="sxs-lookup"><span data-stu-id="457f8-167">6.</span></span>  | <span data-ttu-id="457f8-168">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="457f8-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="457f8-169">7.</span><span class="sxs-lookup"><span data-stu-id="457f8-169">7.</span></span>  | <span data-ttu-id="457f8-170">Wählen Sie im Feld "Arbeitsauftragstyp" die Option "Einlagerung fertiger Waren" aus.</span><span class="sxs-lookup"><span data-stu-id="457f8-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="457f8-171">8.</span><span class="sxs-lookup"><span data-stu-id="457f8-171">8.</span></span>  | <span data-ttu-id="457f8-172">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="457f8-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="457f8-173">9.</span><span class="sxs-lookup"><span data-stu-id="457f8-173">9.</span></span>  | <span data-ttu-id="457f8-174">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="457f8-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="457f8-175">10.</span><span class="sxs-lookup"><span data-stu-id="457f8-175">10.</span></span> | <span data-ttu-id="457f8-176">Wählen Sie im Feld "Arbeitsauftragstyp" die Option "Einlagerung von Co-Produkt und Nebenprodukt" aus.</span><span class="sxs-lookup"><span data-stu-id="457f8-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="457f8-177">11.</span><span class="sxs-lookup"><span data-stu-id="457f8-177">11.</span></span> | <span data-ttu-id="457f8-178">Erweitern Sie den Abschnitt "Lagerplätze für Lagerbestand".</span><span class="sxs-lookup"><span data-stu-id="457f8-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="457f8-179">12.</span><span class="sxs-lookup"><span data-stu-id="457f8-179">12.</span></span> | <span data-ttu-id="457f8-180">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="457f8-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="457f8-181">13</span><span class="sxs-lookup"><span data-stu-id="457f8-181">13.</span></span> | <span data-ttu-id="457f8-182">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="457f8-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="457f8-183">14.</span><span class="sxs-lookup"><span data-stu-id="457f8-183">14.</span></span> | <span data-ttu-id="457f8-184">In der Lagerortliste geben Sie "51" ein.</span><span class="sxs-lookup"><span data-stu-id="457f8-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="457f8-185">15.</span><span class="sxs-lookup"><span data-stu-id="457f8-185">15.</span></span> | <span data-ttu-id="457f8-186">Geben Sie im Feld "Lagerplatz" den Wert "001" ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="457f8-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="457f8-187">16.</span><span class="sxs-lookup"><span data-stu-id="457f8-187">16.</span></span> | <span data-ttu-id="457f8-188">Erweitern Sie den Abschnitt Produkte.</span><span class="sxs-lookup"><span data-stu-id="457f8-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="457f8-189">17.</span><span class="sxs-lookup"><span data-stu-id="457f8-189">17.</span></span> | <span data-ttu-id="457f8-190">Wählen Sie im Feld "Produktauswahl" die Option "Ausgewählt" aus.</span><span class="sxs-lookup"><span data-stu-id="457f8-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="457f8-191">18.</span><span class="sxs-lookup"><span data-stu-id="457f8-191">18.</span></span> | <span data-ttu-id="457f8-192">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="457f8-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="457f8-193">19.</span><span class="sxs-lookup"><span data-stu-id="457f8-193">19.</span></span> | <span data-ttu-id="457f8-194">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="457f8-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="457f8-195">20.</span><span class="sxs-lookup"><span data-stu-id="457f8-195">20.</span></span> | <span data-ttu-id="457f8-196">Geben Sie im Feld "Artikelnummer" den Wert "L0101" ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="457f8-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="457f8-197">21.</span><span class="sxs-lookup"><span data-stu-id="457f8-197">21.</span></span> | <span data-ttu-id="457f8-198">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="457f8-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="457f8-199">Einen Produktionsauftrag an einen Lagerplatz, der nicht kennzeichengesteuert ist, als fertig gestellt melden</span><span class="sxs-lookup"><span data-stu-id="457f8-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="457f8-200">Diese Prozedur zeigt ein Beispiel der Berichterstellung als beendet zu einem Lagerplatz an, der nicht kennzeichengesteuert ist.</span><span class="sxs-lookup"><span data-stu-id="457f8-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="457f8-201">Eine anwendbare Arbeitsrichtlinie ist die Voraussetzung für diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="457f8-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="457f8-202">Die vorherige Prozedur zeigt das Setup der Arbeitsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="457f8-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="457f8-203">SCHRITTE (25)</span><span class="sxs-lookup"><span data-stu-id="457f8-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="457f8-204"><strong>Unteraufgabe: Richten Sie einen Ausgabelagerplatz ein</strong></span><span class="sxs-lookup"><span data-stu-id="457f8-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="457f8-205">Wechseln Sie zu Organisationsverwaltung &gt; Ressourcen &gt; Ressourcengruppen.</span><span class="sxs-lookup"><span data-stu-id="457f8-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="457f8-206">Wählen Sie in der Liste Ressourcengruppe "5102" aus.</span><span class="sxs-lookup"><span data-stu-id="457f8-206">In the list, select resource group '5102'.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="457f8-207">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="457f8-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="457f8-208">Geben Sie im Feld "Ausgangslagerort" den Wert "51" ein.</span><span class="sxs-lookup"><span data-stu-id="457f8-208">In the Output warehouse field, enter '51'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="457f8-209">Geben Sie im Feld "Ausgangslagerplatz" den Wert "001" ein.</span><span class="sxs-lookup"><span data-stu-id="457f8-209">In the Output location field, enter '001'.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="457f8-210">Lagerplatz 001 ist kein kennzeichengesteuerter Lagerplatz.</span><span class="sxs-lookup"><span data-stu-id="457f8-210">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="457f8-211">Sie können einen Ausgabelagerplatz ohne Kennzeichen nur einrichten, wenn eine anwendbare Arbeitsrichtlinie für den Lagerplatz vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="457f8-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="457f8-212"><strong>Unteraufgabe: Erstellen Sie einen Produktionsauftrag und melden Sie ihn als abgeschlossen</strong></span><span class="sxs-lookup"><span data-stu-id="457f8-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="457f8-213">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="457f8-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="457f8-214">Wechseln Sie zu "Produktionssteuerung" &gt; "Produktionsaufträge" &gt; "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="457f8-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="457f8-215">Klicken Sie auf "Neuer Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="457f8-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="457f8-216">Geben Sie im Feld "Artikelnummer" den Wert "L0101" ein.</span><span class="sxs-lookup"><span data-stu-id="457f8-216">In the Item number field, enter 'L0101'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="457f8-217">Klicken Sie auf Erstellen.</span><span class="sxs-lookup"><span data-stu-id="457f8-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="457f8-218">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="457f8-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="457f8-219">Klicken Sie auf "Vorkalkulation".</span><span class="sxs-lookup"><span data-stu-id="457f8-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="457f8-220">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="457f8-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="457f8-221">Klicken Sie auf "Start".</span><span class="sxs-lookup"><span data-stu-id="457f8-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="457f8-222">Klicken Sie auf die Registerkarte Allgemeines.</span><span class="sxs-lookup"><span data-stu-id="457f8-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="457f8-223">Wählen Sie im Feld "Stücklistenverbrauch" die Option "Nie" aus.</span><span class="sxs-lookup"><span data-stu-id="457f8-223">In the Automatic BOM consumption field, select 'Never'.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="457f8-224">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="457f8-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="457f8-225">Klicken Sie auf Fertigmeldung.</span><span class="sxs-lookup"><span data-stu-id="457f8-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="457f8-226">Klicken Sie auf die Registerkarte Allgemeines.</span><span class="sxs-lookup"><span data-stu-id="457f8-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="457f8-227">Wählen Sie "Ja" im Feld "Fehler akzeptieren" aus.</span><span class="sxs-lookup"><span data-stu-id="457f8-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="457f8-228">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="457f8-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="457f8-229">Klicken Sie im Aktivitätsbereich auf "Lagerort".</span><span class="sxs-lookup"><span data-stu-id="457f8-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="457f8-230">Klicken Sie auf "Arbeitsdetails".</span><span class="sxs-lookup"><span data-stu-id="457f8-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="457f8-231">Wenn der Produktionsauftrag als fertig gemeldet wurde, wurde keine Arbeit für die Einlagerung generiert.</span><span class="sxs-lookup"><span data-stu-id="457f8-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="457f8-232">Dies tritt auf, weil eine Arbeitsrichtlinie definiert ist, die verhindert, dass Arbeit generiert wird, wenn Produkt L0101 als fertig nach Lagerplatz 001 gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="457f8-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>




