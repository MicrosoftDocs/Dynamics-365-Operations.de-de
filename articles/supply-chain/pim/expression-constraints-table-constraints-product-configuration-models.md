---
title: Ausdruckseinschränkungen und Tabelleneinschränkungen in Produktkonfigurationsmodellen
description: In diesem Thema wird die Verwendung von Ausdruckseinschränkungen und Tabelleneinschränkungen beschrieben. Einschränkungen steuern die Attributwerte, die Sie auswählen können, wenn Sie Produkte für einen Auftrag, ein Verkaufsangebot, eine Bestellung oder einen Produktionsauftrag konfigurieren. Sie können Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be9d9ae48d21db077928ba7bd5615fea47ea5181
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428901"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="e33c2-105">Ausdruckseinschränkungen und Tabelleneinschränkungen in Produktkonfigurationsmodellen</span><span class="sxs-lookup"><span data-stu-id="e33c2-105">Expression constraints and table constraints in product configuration models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e33c2-106">In diesem Thema wird die Verwendung von Ausdruckseinschränkungen und Tabelleneinschränkungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e33c2-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="e33c2-107">Einschränkungen steuern die Attributwerte, die Sie auswählen können, wenn Sie Produkte für einen Auftrag, ein Verkaufsangebot, eine Bestellung oder einen Produktionsauftrag konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e33c2-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="e33c2-108">Sie können Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="e33c2-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="e33c2-109">Einschränkungen steuern die Attributwerte, die Sie auswählen können, wenn Sie Produkte für einen Auftrag, ein Verkaufsangebot, eine Bestellung oder einen Produktionsauftrag konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e33c2-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="e33c2-110">Sie können Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="e33c2-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="e33c2-111">Was sind Ausdruckseinschränkungen?</span><span class="sxs-lookup"><span data-stu-id="e33c2-111">What are expression constraints?</span></span>
<span data-ttu-id="e33c2-112">Ausdruckseinschränkungen werden durch einen Ausdruck bezeichnet, der arithmetische und boolesche Operatoren und Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e33c2-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="e33c2-113">Eine Ausdruckseinschränkung wird für eine bestimmte Komponente in einem Produktkonfigurationsmodell geschrieben.</span><span class="sxs-lookup"><span data-stu-id="e33c2-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="e33c2-114">Sie können nicht von einer anderen Komponente wiederverwendet oder für sie freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e33c2-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="e33c2-115">Die Ausdruckseinschränkungen für eine Komponente können jedoch auf Attribute der Unterkomponenten der Komponente verweisen.</span><span class="sxs-lookup"><span data-stu-id="e33c2-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="e33c2-116">Was sind Tabelleneinschränkungen?</span><span class="sxs-lookup"><span data-stu-id="e33c2-116">What are table constraints?</span></span>
<span data-ttu-id="e33c2-117">Tabelleneinschränkungen listen die Kombinationen von Werten auf, die für Attribute zulässig sind, wenn Sie ein Produkt konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e33c2-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="e33c2-118">Tabelleneinschränkungsdefinitionen können generisch verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e33c2-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="e33c2-119">Wenn Sie eine Tabelleneinschränkung für eine Komponente in einem Produktkonfigurationsmodell erstellen, wählen Sie eine Tabelleneinschränkungsdefinition aus.</span><span class="sxs-lookup"><span data-stu-id="e33c2-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="e33c2-120">Um die Kombinationen zu erstellen, die zulässig sind, fügen Sie Attribute bestimmter Arten den Komponenten hinzu.</span><span class="sxs-lookup"><span data-stu-id="e33c2-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="e33c2-121">Jeder Attributtyp hat einen bestimmten Wert.</span><span class="sxs-lookup"><span data-stu-id="e33c2-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="e33c2-122">Beispiel einer Tabelleneinschränkung</span><span class="sxs-lookup"><span data-stu-id="e33c2-122">Example of a table constraint</span></span>

<span data-ttu-id="e33c2-123">Dieses Beispiel verdeutlicht, wie Sie die Konfiguration eines Lautsprechers auf bestimmte Gehäuseoberflächen und Frontseiten einschränken können.</span><span class="sxs-lookup"><span data-stu-id="e33c2-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="e33c2-124">Die erste Tabelle enthält die Oberflächen und die Frontseiten, die allgemein zur Konfiguration verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e33c2-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="e33c2-125">Die Werte werden für die **Gehäuseoberfläche**-**Vordergerippe**-Attributtypen definiert.</span><span class="sxs-lookup"><span data-stu-id="e33c2-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="e33c2-126">Attributtyp</span><span class="sxs-lookup"><span data-stu-id="e33c2-126">Attribute type</span></span> | <span data-ttu-id="e33c2-127">Werte</span><span class="sxs-lookup"><span data-stu-id="e33c2-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="e33c2-128">Gehäuseoberfläche</span><span class="sxs-lookup"><span data-stu-id="e33c2-128">Cabinet finish</span></span> | <span data-ttu-id="e33c2-129">Schwarz, Eiche, Rosenholz, Weiß</span><span class="sxs-lookup"><span data-stu-id="e33c2-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="e33c2-130">Vordergerippe</span><span class="sxs-lookup"><span data-stu-id="e33c2-130">Front grill</span></span>    | <span data-ttu-id="e33c2-131">Schwarz, Metall, Weiß</span><span class="sxs-lookup"><span data-stu-id="e33c2-131">Black, Metal, White</span></span>         |

<span data-ttu-id="e33c2-132">In der folgenden Tabelle werden die Kombinationen angezeigt, die von der Tabelleneinschränkung **Farbe und Oberfläche** definiert werden.</span><span class="sxs-lookup"><span data-stu-id="e33c2-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="e33c2-133">Mithilfe dieser Tabelleneinschränkung können Sie einen Lautsprecher konfigurieren, der ein Eichenoberfläche und einen schwarzen Grill, eine Rosenholzoberfläche und ein weißer Grill usw. hat.</span><span class="sxs-lookup"><span data-stu-id="e33c2-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="e33c2-134">Fertig stellen</span><span class="sxs-lookup"><span data-stu-id="e33c2-134">Finish</span></span>         | <span data-ttu-id="e33c2-135">Grill</span><span class="sxs-lookup"><span data-stu-id="e33c2-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="e33c2-136">Eiche</span><span class="sxs-lookup"><span data-stu-id="e33c2-136">Oak</span></span>            | <span data-ttu-id="e33c2-137">Schwarz</span><span class="sxs-lookup"><span data-stu-id="e33c2-137">Black</span></span>                       |
| <span data-ttu-id="e33c2-138">Rosenholz</span><span class="sxs-lookup"><span data-stu-id="e33c2-138">Rosewood</span></span>       | <span data-ttu-id="e33c2-139">Weiß</span><span class="sxs-lookup"><span data-stu-id="e33c2-139">White</span></span>                       |
| <span data-ttu-id="e33c2-140">Weiß</span><span class="sxs-lookup"><span data-stu-id="e33c2-140">White</span></span>          | <span data-ttu-id="e33c2-141">Schwarz</span><span class="sxs-lookup"><span data-stu-id="e33c2-141">Black</span></span>                       |
| <span data-ttu-id="e33c2-142">Weiß</span><span class="sxs-lookup"><span data-stu-id="e33c2-142">White</span></span>          | <span data-ttu-id="e33c2-143">Weiß</span><span class="sxs-lookup"><span data-stu-id="e33c2-143">White</span></span>                       |
| <span data-ttu-id="e33c2-144">Schwarz</span><span class="sxs-lookup"><span data-stu-id="e33c2-144">Black</span></span>          | <span data-ttu-id="e33c2-145">Schwarz</span><span class="sxs-lookup"><span data-stu-id="e33c2-145">Black</span></span>                       |
| <span data-ttu-id="e33c2-146">Schwarz</span><span class="sxs-lookup"><span data-stu-id="e33c2-146">Black</span></span>          | <span data-ttu-id="e33c2-147">Metall</span><span class="sxs-lookup"><span data-stu-id="e33c2-147">Metal</span></span>                       | 

<span data-ttu-id="e33c2-148">Sie können die systemdefinierte und benutzerdefinierte Tabelleneinschränkungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="e33c2-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="e33c2-149">Weitere Informationen finden Sie unter [Systemdefinierte und benutzerdefinierte Tabelleneinschränkungen](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="e33c2-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="e33c2-150">Welche Syntax soll verwendet werden, um Einschränkungen in aufzuheben?</span><span class="sxs-lookup"><span data-stu-id="e33c2-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="e33c2-151">Sie müssen Optimization Modeling Language (OML)-Syntax verwenden, wenn Sie die Einschränkungen schreiben.</span><span class="sxs-lookup"><span data-stu-id="e33c2-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="e33c2-152">Das System verwendet Microsoft Solver Foundation Einschränkungswandler, um die Einschränkungen zu beheben.</span><span class="sxs-lookup"><span data-stu-id="e33c2-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="e33c2-153">Soll ich Tabelleneinschränkungen oder Ausdruckseinschränkungen verwenden?</span><span class="sxs-lookup"><span data-stu-id="e33c2-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="e33c2-154">Sie können entweder Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="e33c2-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="e33c2-155">Sie bauen eine Tabelleneinschränkung als Matrix auf, während eine Ausdruckseinschränkung ein einzelner Auszug ist.</span><span class="sxs-lookup"><span data-stu-id="e33c2-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="e33c2-156">Wenn Sie ein Produkt konfigurieren, ist es nicht von Bedeutung, welche Art von Einschränkung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e33c2-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="e33c2-157">Im folgenden Beispiel werden die Unterschiede der zwei zur Verfügung stehenden Optionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e33c2-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="e33c2-158">Wenn Sie ein Produkt konfigurieren, indem Sie die folgenden Einschränkungseinstellungen verwenden, sind diese Kombinationen zulässig:</span><span class="sxs-lookup"><span data-stu-id="e33c2-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="e33c2-159">Ein Produkt in der Farbe Schwarz und mit Größe 30 oder 50</span><span class="sxs-lookup"><span data-stu-id="e33c2-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="e33c2-160">Ein Produkt in der Farbe Rot und mit Größe 20</span><span class="sxs-lookup"><span data-stu-id="e33c2-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="e33c2-161">Tabelleneinschränkungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="e33c2-161">Table constraint setup</span></span>

| <span data-ttu-id="e33c2-162">Farbe</span><span class="sxs-lookup"><span data-stu-id="e33c2-162">Color</span></span> | <span data-ttu-id="e33c2-163">Größe</span><span class="sxs-lookup"><span data-stu-id="e33c2-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="e33c2-164">Schwarz</span><span class="sxs-lookup"><span data-stu-id="e33c2-164">Black</span></span> | <span data-ttu-id="e33c2-165">30</span><span class="sxs-lookup"><span data-stu-id="e33c2-165">30</span></span>   |
| <span data-ttu-id="e33c2-166">Schwarz</span><span class="sxs-lookup"><span data-stu-id="e33c2-166">Black</span></span> | <span data-ttu-id="e33c2-167">50</span><span class="sxs-lookup"><span data-stu-id="e33c2-167">50</span></span>   |
| <span data-ttu-id="e33c2-168">Rot</span><span class="sxs-lookup"><span data-stu-id="e33c2-168">Red</span></span>   | <span data-ttu-id="e33c2-169">20</span><span class="sxs-lookup"><span data-stu-id="e33c2-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="e33c2-170">Einrichtung von Ausdruckseinschränkungen</span><span class="sxs-lookup"><span data-stu-id="e33c2-170">Expression constraint setup</span></span>

<span data-ttu-id="e33c2-171">(Farbe == "Schwarz" & (Größe == "30" | Größe == "50")) | (Farbe == "Rot" & Größe = "20")</span><span class="sxs-lookup"><span data-stu-id="e33c2-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="e33c2-172">Muss ich Operatoren oder Infixschreibweise verwenden, wenn ich Ausdruckseinschränkungen schreibe?</span><span class="sxs-lookup"><span data-stu-id="e33c2-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="e33c2-173">Sie können eine Ausdruckseinschränkung schreiben, indem Sie entweder die verfügbaren Präfixoperatoren oder die Infixschreibweise verwenden.</span><span class="sxs-lookup"><span data-stu-id="e33c2-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="e33c2-174">Für die Operatoren **Min**, **Max** und **Abs** können Sie die Infixschreibweise nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="e33c2-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="e33c2-175">Diese Operatoren sind als Standard in den meisten Programmiersprachen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="e33c2-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="e33c2-176">Welche Operatoren und Infixschreibweise kann ich verwenden, wenn ich Ausdruckseinschränkungen schreibe?</span><span class="sxs-lookup"><span data-stu-id="e33c2-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="e33c2-177">In den folgenden Tabellen werden die Operatoren und Infixschreibweise aufgelistet, die Sie verwenden können, wenn Sie eine Ausdruckseinschränkung für eine Komponente in einem Produktkonfigurationsmodell schreiben.</span><span class="sxs-lookup"><span data-stu-id="e33c2-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="e33c2-178">Den Beispielen in dieser ersten Tabelle können Sie entnehmen, wie Sie einen Ausdruck schreiben, indem Sie entweder Infixschreibweise oder Operatoren verwenden.</span><span class="sxs-lookup"><span data-stu-id="e33c2-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e33c2-179">Bediener</span><span class="sxs-lookup"><span data-stu-id="e33c2-179">Operator</span></span></th>
<th><span data-ttu-id="e33c2-180">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e33c2-180">Description</span></span></th>
<th><span data-ttu-id="e33c2-181">Syntax</span><span class="sxs-lookup"><span data-stu-id="e33c2-181">Syntax</span></span></th>
<th><span data-ttu-id="e33c2-182">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e33c2-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e33c2-183">Bedeutet</span><span class="sxs-lookup"><span data-stu-id="e33c2-183">Implies</span></span></td>
<td><span data-ttu-id="e33c2-184">Dies gilt, wenn die erste Bedingung nicht zutrifft, die zweite Bedingung erfüllt wird, oder beide.</span><span class="sxs-lookup"><span data-stu-id="e33c2-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="e33c2-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="e33c2-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="e33c2-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="e33c2-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="e33c2-187"><strong>Infixschreibweise:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="e33c2-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e33c2-188">Und</span><span class="sxs-lookup"><span data-stu-id="e33c2-188">And</span></span></td>
<td><span data-ttu-id="e33c2-189">Dies gilt nur, wenn alle Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="e33c2-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="e33c2-190">Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>Wahr</strong>.</span><span class="sxs-lookup"><span data-stu-id="e33c2-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="e33c2-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="e33c2-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="e33c2-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="e33c2-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="e33c2-193"><strong>Infixschreibweise:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="e33c2-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e33c2-194">Oder</span><span class="sxs-lookup"><span data-stu-id="e33c2-194">Or</span></span></td>
<td><span data-ttu-id="e33c2-195">Dies trifft zu, wenn jede Bedingung wahr ist.</span><span class="sxs-lookup"><span data-stu-id="e33c2-195">This is true if any condition is true.</span></span> <span data-ttu-id="e33c2-196">Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>Falsch</strong>.</span><span class="sxs-lookup"><span data-stu-id="e33c2-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="e33c2-197">Or[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="e33c2-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="e33c2-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="e33c2-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="e33c2-199"><strong>Infixschreibweise:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="e33c2-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e33c2-200">Plus</span><span class="sxs-lookup"><span data-stu-id="e33c2-200">Plus</span></span></td>
<td><span data-ttu-id="e33c2-201">Dies summiert die Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="e33c2-201">This sums its conditions.</span></span> <span data-ttu-id="e33c2-202">Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="e33c2-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="e33c2-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="e33c2-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="e33c2-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="e33c2-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="e33c2-205"><strong>Infixschreibweise</strong>: x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="e33c2-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e33c2-206">Minus</span><span class="sxs-lookup"><span data-stu-id="e33c2-206">Minus</span></span></td>
<td><span data-ttu-id="e33c2-207">Dies negiert das Argument.</span><span class="sxs-lookup"><span data-stu-id="e33c2-207">This negates its argument.</span></span> <span data-ttu-id="e33c2-208">Dies muss genau eine Bedingung haben.</span><span class="sxs-lookup"><span data-stu-id="e33c2-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="e33c2-209">Minus[expr], infix: -expr</span><span class="sxs-lookup"><span data-stu-id="e33c2-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="e33c2-210"><strong>Operator:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="e33c2-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="e33c2-211"><strong>Infixschreibweise:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="e33c2-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e33c2-212">Abs</span><span class="sxs-lookup"><span data-stu-id="e33c2-212">Abs</span></span></td>
<td><span data-ttu-id="e33c2-213">Dies nimmt den absoluten Wert der Bedingung.</span><span class="sxs-lookup"><span data-stu-id="e33c2-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="e33c2-214">Dies muss genau eine Bedingung haben.</span><span class="sxs-lookup"><span data-stu-id="e33c2-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="e33c2-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="e33c2-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="e33c2-216"><strong>Operator:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="e33c2-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e33c2-217">Zeiten</span><span class="sxs-lookup"><span data-stu-id="e33c2-217">Times</span></span></td>
<td><span data-ttu-id="e33c2-218">Dies nimmt das Produkt der Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="e33c2-218">This takes the product of its conditions.</span></span> <span data-ttu-id="e33c2-219">Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="e33c2-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="e33c2-220">Times[args], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="e33c2-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="e33c2-221"><strong>Operator:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="e33c2-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="e33c2-222"><strong>Infixschreibweise</strong>: x \* y \* 2 == z</span><span class="sxs-lookup"><span data-stu-id="e33c2-222"><strong>Infix notation:</strong> x \* y \* 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e33c2-223">Antriebskraft</span><span class="sxs-lookup"><span data-stu-id="e33c2-223">Power</span></span></td>
<td><span data-ttu-id="e33c2-224">Dies nimmt einen exponentiellen Wert.</span><span class="sxs-lookup"><span data-stu-id="e33c2-224">This takes an exponential.</span></span> <span data-ttu-id="e33c2-225">Dies wendet die Exponenten von rechts nach links an.</span><span class="sxs-lookup"><span data-stu-id="e33c2-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="e33c2-226">(Mit anderen Worten, &#39;ist rechts-assoziativ.) Daher ist <strong>Power[a, b, c]</strong> äquivalent zu <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="e33c2-226">(In other words, it&#39;s right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="e33c2-227"><strong>Power</strong> kann nur mit einer positiven Konstante als Exponent verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e33c2-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="e33c2-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="e33c2-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="e33c2-229"><strong>Operator:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="e33c2-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="e33c2-230"><strong>Infixschreibweise:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="e33c2-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e33c2-231">Max.</span><span class="sxs-lookup"><span data-stu-id="e33c2-231">Max</span></span></td>
<td><span data-ttu-id="e33c2-232">Dies produziert die umfangreichste Bedingung.</span><span class="sxs-lookup"><span data-stu-id="e33c2-232">This produces the largest condition.</span></span> <span data-ttu-id="e33c2-233">Wenn die Anzahl der Bedingungen 0 (Null) ist, produziert dies <strong>Unendlich</strong>.</span><span class="sxs-lookup"><span data-stu-id="e33c2-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="e33c2-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="e33c2-234">Max[args]</span></span></td>
<td><span data-ttu-id="e33c2-235"><strong>Operator:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="e33c2-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e33c2-236">Min.</span><span class="sxs-lookup"><span data-stu-id="e33c2-236">Min</span></span></td>
<td><span data-ttu-id="e33c2-237">Dies produziert die kleinste Bedingung.</span><span class="sxs-lookup"><span data-stu-id="e33c2-237">This produces the smallest condition.</span></span> <span data-ttu-id="e33c2-238">Wenn die Anzahl der Bedingungen 0 (Null) ist, produziert dies <strong>Unendlich</strong>.</span><span class="sxs-lookup"><span data-stu-id="e33c2-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="e33c2-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="e33c2-239">Min[args]</span></span></td>
<td><span data-ttu-id="e33c2-240"><strong>Operator:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="e33c2-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e33c2-241">Nicht</span><span class="sxs-lookup"><span data-stu-id="e33c2-241">Not</span></span></td>
<td><span data-ttu-id="e33c2-242">Dies produziert die logische Umkehrung der Bedingung.</span><span class="sxs-lookup"><span data-stu-id="e33c2-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="e33c2-243">Dies muss genau eine Bedingung haben.</span><span class="sxs-lookup"><span data-stu-id="e33c2-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="e33c2-244">Not[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="e33c2-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="e33c2-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="e33c2-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="e33c2-246"><strong>Infixschreibweise:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="e33c2-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e33c2-247">Die Beispiele in der nächsten Tabellen zeigen, wie eine Infixnotation geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e33c2-247">The examples in the next table show how to write infix notation.</span></span>


|  <span data-ttu-id="e33c2-248">Infixschreibweise</span><span class="sxs-lookup"><span data-stu-id="e33c2-248">Infix notation</span></span>   |                                          <span data-ttu-id="e33c2-249">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e33c2-249">Description</span></span>                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     <span data-ttu-id="e33c2-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="e33c2-250">x + y + z</span></span>     |                                           <span data-ttu-id="e33c2-251">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="e33c2-251">Addition</span></span>                                            |
|    <span data-ttu-id="e33c2-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="e33c2-252">x \* y \* z</span></span>    |                                        <span data-ttu-id="e33c2-253">Multiplikation</span><span class="sxs-lookup"><span data-stu-id="e33c2-253">Multiplication</span></span>                                         |
|       <span data-ttu-id="e33c2-254">x - y</span><span class="sxs-lookup"><span data-stu-id="e33c2-254">x - y</span></span>       | <span data-ttu-id="e33c2-255">Die binäre Subtraktion wird auf die gleiche Weise wie die binäre Addition bei einer negierten Sekunde übersetzt.</span><span class="sxs-lookup"><span data-stu-id="e33c2-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
|     <span data-ttu-id="e33c2-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="e33c2-256">x ^ y ^ z</span></span>     |                          <span data-ttu-id="e33c2-257">Exponenten mit Rechtsverknüpfung</span><span class="sxs-lookup"><span data-stu-id="e33c2-257">Exponentiation that has right associativity</span></span>                          |
|        <span data-ttu-id="e33c2-258">!x</span><span class="sxs-lookup"><span data-stu-id="e33c2-258">!x</span></span>         |                                          <span data-ttu-id="e33c2-259">Boolesches not</span><span class="sxs-lookup"><span data-stu-id="e33c2-259">Boolean not</span></span>                                          |
|      <span data-ttu-id="e33c2-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="e33c2-260">x -: y</span></span>       |                                      <span data-ttu-id="e33c2-261">Boolesche Auswirkung</span><span class="sxs-lookup"><span data-stu-id="e33c2-261">Boolean implication</span></span>                                      |
|         <span data-ttu-id="e33c2-262">x</span><span class="sxs-lookup"><span data-stu-id="e33c2-262">x</span></span>         |                                               <span data-ttu-id="e33c2-263">y</span><span class="sxs-lookup"><span data-stu-id="e33c2-263">y</span></span>                                               |
|     <span data-ttu-id="e33c2-264">x & y & z</span><span class="sxs-lookup"><span data-stu-id="e33c2-264">x & y & z</span></span>     |                                          <span data-ttu-id="e33c2-265">Boolesches and</span><span class="sxs-lookup"><span data-stu-id="e33c2-265">Boolean and</span></span>                                          |
|    <span data-ttu-id="e33c2-266">x == y == z</span><span class="sxs-lookup"><span data-stu-id="e33c2-266">x == y == z</span></span>    |                                           <span data-ttu-id="e33c2-267">Gleichheit</span><span class="sxs-lookup"><span data-stu-id="e33c2-267">Equality</span></span>                                            |
|    <span data-ttu-id="e33c2-268">x != y != z</span><span class="sxs-lookup"><span data-stu-id="e33c2-268">x != y != z</span></span>    |                                           <span data-ttu-id="e33c2-269">Getrennt</span><span class="sxs-lookup"><span data-stu-id="e33c2-269">Distinct</span></span>                                            |
|  <span data-ttu-id="e33c2-270">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="e33c2-270">x &lt; y &lt; z</span></span>  |                                           <span data-ttu-id="e33c2-271">Kleiner als</span><span class="sxs-lookup"><span data-stu-id="e33c2-271">Less than</span></span>                                           |
|  <span data-ttu-id="e33c2-272">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="e33c2-272">x &gt; y &gt; z</span></span>  |                                         <span data-ttu-id="e33c2-273">Größer als</span><span class="sxs-lookup"><span data-stu-id="e33c2-273">Greater than</span></span>                                          |
| <span data-ttu-id="e33c2-274">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="e33c2-274">x &lt;= y &lt;= z</span></span> |                                     <span data-ttu-id="e33c2-275">Kleiner oder gleich</span><span class="sxs-lookup"><span data-stu-id="e33c2-275">Less than or equal to</span></span>                                     |
| <span data-ttu-id="e33c2-276">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="e33c2-276">x &gt;= y &gt;= z</span></span> |                                   <span data-ttu-id="e33c2-277">Größer oder gleich</span><span class="sxs-lookup"><span data-stu-id="e33c2-277">Greater than or equal to</span></span>                                    |
|        <span data-ttu-id="e33c2-278">(x)</span><span class="sxs-lookup"><span data-stu-id="e33c2-278">(x)</span></span>        |                           <span data-ttu-id="e33c2-279">Klammern setzten die standardmäßige Rangfolge außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="e33c2-279">Parentheses override default precedence.</span></span>                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="e33c2-280">Warum werden meine Ausdruckseinschränkungen nicht ordnungsgemäß validiert?</span><span class="sxs-lookup"><span data-stu-id="e33c2-280">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="e33c2-281">Sie können reservierte Schlüsselwörter nicht als Wandlernamen für Attribute, Komponenten oder Unterkomponenten in einem Produktkonfigurationsmodell verwenden.</span><span class="sxs-lookup"><span data-stu-id="e33c2-281">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span><span data-ttu-id="e33c2-282">Die folgende Tabelle enthält eine Liste der reservierten Schlüsselwörter, die Sie nicht verwenden dürfen.</span><span class="sxs-lookup"><span data-stu-id="e33c2-282"> Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="e33c2-283">Decke</span><span class="sxs-lookup"><span data-stu-id="e33c2-283">Ceiling</span></span>
-   <span data-ttu-id="e33c2-284">Element</span><span class="sxs-lookup"><span data-stu-id="e33c2-284">Element</span></span>
-   <span data-ttu-id="e33c2-285">Gleich</span><span class="sxs-lookup"><span data-stu-id="e33c2-285">Equal</span></span>
-   <span data-ttu-id="e33c2-286">Stockwerk</span><span class="sxs-lookup"><span data-stu-id="e33c2-286">Floor</span></span>
-   <span data-ttu-id="e33c2-287">Falls</span><span class="sxs-lookup"><span data-stu-id="e33c2-287">If</span></span>
-   <span data-ttu-id="e33c2-288">Kleiner</span><span class="sxs-lookup"><span data-stu-id="e33c2-288">Less</span></span>
-   <span data-ttu-id="e33c2-289">Größer</span><span class="sxs-lookup"><span data-stu-id="e33c2-289">Greater</span></span>
-   <span data-ttu-id="e33c2-290">Bedeutet</span><span class="sxs-lookup"><span data-stu-id="e33c2-290">Implies</span></span>
-   <span data-ttu-id="e33c2-291">Protokoll</span><span class="sxs-lookup"><span data-stu-id="e33c2-291">Log</span></span>
-   <span data-ttu-id="e33c2-292">Max.</span><span class="sxs-lookup"><span data-stu-id="e33c2-292">Max</span></span>
-   <span data-ttu-id="e33c2-293">Min.</span><span class="sxs-lookup"><span data-stu-id="e33c2-293">Min</span></span>
-   <span data-ttu-id="e33c2-294">Minus</span><span class="sxs-lookup"><span data-stu-id="e33c2-294">Minus</span></span>
-   <span data-ttu-id="e33c2-295">Plus</span><span class="sxs-lookup"><span data-stu-id="e33c2-295">Plus</span></span>
-   <span data-ttu-id="e33c2-296">Antriebskraft</span><span class="sxs-lookup"><span data-stu-id="e33c2-296">Power</span></span>
-   <span data-ttu-id="e33c2-297">Zeiten</span><span class="sxs-lookup"><span data-stu-id="e33c2-297">Times</span></span>
-   <span data-ttu-id="e33c2-298">Zeitrahmen</span><span class="sxs-lookup"><span data-stu-id="e33c2-298">Slot</span></span>
-   <span data-ttu-id="e33c2-299">Modell</span><span class="sxs-lookup"><span data-stu-id="e33c2-299">Model</span></span>
-   <span data-ttu-id="e33c2-300">Entscheidung</span><span class="sxs-lookup"><span data-stu-id="e33c2-300">Decision</span></span>
-   <span data-ttu-id="e33c2-301">Ziel</span><span class="sxs-lookup"><span data-stu-id="e33c2-301">Goal</span></span>


<a name="additional-resources"></a><span data-ttu-id="e33c2-302">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e33c2-302">Additional resources</span></span>
--------

[<span data-ttu-id="e33c2-303">Erstellen einer Ausdruckseinschränkung</span><span class="sxs-lookup"><span data-stu-id="e33c2-303">Create an expression constraint</span></span>](tasks/add-expression-constraint-product-configuration-model.md)

[<span data-ttu-id="e33c2-304">Berechnung zu einem Produktkonfigurationsmodell hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e33c2-304">Add a calculation to a product configuration model</span></span>](tasks/add-calculation-product-configuration-model.md)



