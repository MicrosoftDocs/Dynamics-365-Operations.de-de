---
title: "Ausdruckseinschränkungen und Tabelleneinschränkungen in Produktkonfigurationsmodellen"
description: "In diesem Thema wird die Verwendung von Ausdruckseinschränkungen und Tabelleneinschränkungen beschrieben. Einschränkungen steuern die Attributwerte, die Sie auswählen können, wenn Sie Produkte für einen Auftrag, ein Verkaufsangebot, eine Bestellung oder einen Produktionsauftrag konfigurieren. Sie können Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 66d5ec61c1d69ebc8a8fc10d0b9b2a4b174729ee
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2017

---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="7f994-105">Ausdruckseinschränkungen und Tabelleneinschränkungen in Produktkonfigurationsmodellen</span><span class="sxs-lookup"><span data-stu-id="7f994-105">Expression constraints and table constraints in product configuration models</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7f994-106">In diesem Thema wird die Verwendung von Ausdruckseinschränkungen und Tabelleneinschränkungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7f994-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="7f994-107">Einschränkungen steuern die Attributwerte, die Sie auswählen können, wenn Sie Produkte für einen Auftrag, ein Verkaufsangebot, eine Bestellung oder einen Produktionsauftrag konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7f994-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="7f994-108">Sie können Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="7f994-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="7f994-109">Einschränkungen steuern die Attributwerte, die Sie auswählen können, wenn Sie Produkte für einen Auftrag, ein Verkaufsangebot, eine Bestellung oder einen Produktionsauftrag konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7f994-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="7f994-110">Sie können Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="7f994-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="7f994-111">Was sind Ausdruckseinschränkungen?</span><span class="sxs-lookup"><span data-stu-id="7f994-111">What are expression constraints?</span></span>
<span data-ttu-id="7f994-112">Ausdruckseinschränkungen werden durch einen Ausdruck bezeichnet, der arithmetische und boolesche Operatoren und Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f994-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="7f994-113">Eine Ausdruckseinschränkung wird für eine bestimmte Komponente in einem Produktkonfigurationsmodell geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7f994-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="7f994-114">Sie können nicht von einer anderen Komponente wiederverwendet oder für sie freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7f994-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="7f994-115">Die Ausdruckseinschränkungen für eine Komponente können jedoch auf Attribute der Unterkomponenten der Komponente verweisen.</span><span class="sxs-lookup"><span data-stu-id="7f994-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="7f994-116">Was sind Tabelleneinschränkungen?</span><span class="sxs-lookup"><span data-stu-id="7f994-116">What are table constraints?</span></span>
<span data-ttu-id="7f994-117">Tabelleneinschränkungen listen die Kombinationen von Werten auf, die für Attribute zulässig sind, wenn Sie ein Produkt konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7f994-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="7f994-118">Tabelleneinschränkungsdefinitionen können generisch verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f994-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="7f994-119">Wenn Sie eine Tabelleneinschränkung für eine Komponente in einem Produktkonfigurationsmodell erstellen, wählen Sie eine Tabelleneinschränkungsdefinition aus.</span><span class="sxs-lookup"><span data-stu-id="7f994-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="7f994-120">Um die Kombinationen zu erstellen, die zulässig sind, fügen Sie Attribute bestimmter Arten den Komponenten hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f994-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="7f994-121">Jeder Attributtyp hat einen bestimmten Wert.</span><span class="sxs-lookup"><span data-stu-id="7f994-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="7f994-122">Beispiel einer Tabelleneinschränkung</span><span class="sxs-lookup"><span data-stu-id="7f994-122">Example of a table constraint</span></span>

<span data-ttu-id="7f994-123">Dieses Beispiel verdeutlicht, wie Sie die Konfiguration eines Lautsprechers auf bestimmte Gehäuseoberflächen und Frontseiten einschränken können.</span><span class="sxs-lookup"><span data-stu-id="7f994-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="7f994-124">Die erste Tabelle enthält die Oberflächen und die Frontseiten, die allgemein zur Konfiguration verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7f994-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="7f994-125">Die Werte werden für die **Gehäuseoberfläche**-**Vordergerippe**-Attributtypen definiert.</span><span class="sxs-lookup"><span data-stu-id="7f994-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="7f994-126">Attributtyp</span><span class="sxs-lookup"><span data-stu-id="7f994-126">Attribute type</span></span> | <span data-ttu-id="7f994-127">Werte</span><span class="sxs-lookup"><span data-stu-id="7f994-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="7f994-128">Gehäuseoberfläche</span><span class="sxs-lookup"><span data-stu-id="7f994-128">Cabinet finish</span></span> | <span data-ttu-id="7f994-129">Schwarz, Eiche, Rosenholz, Weiß</span><span class="sxs-lookup"><span data-stu-id="7f994-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="7f994-130">Vordergerippe</span><span class="sxs-lookup"><span data-stu-id="7f994-130">Front grill</span></span>    | <span data-ttu-id="7f994-131">Schwarz, Metall, Weiß</span><span class="sxs-lookup"><span data-stu-id="7f994-131">Black, Metal, White</span></span>         |

<span data-ttu-id="7f994-132">In der folgenden Tabelle werden die Kombinationen angezeigt, die von der Tabelleneinschränkung **Farbe und Oberfläche** definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7f994-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="7f994-133">Mithilfe dieser Tabelleneinschränkung können Sie einen Lautsprecher konfigurieren, der ein Eichenoberfläche und einen schwarzen Grill, eine Rosenholzoberfläche und ein weißer Grill usw. hat.</span><span class="sxs-lookup"><span data-stu-id="7f994-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="7f994-134">Fertig stellen</span><span class="sxs-lookup"><span data-stu-id="7f994-134">Finish</span></span>         | <span data-ttu-id="7f994-135">Grill</span><span class="sxs-lookup"><span data-stu-id="7f994-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="7f994-136">Eiche</span><span class="sxs-lookup"><span data-stu-id="7f994-136">Oak</span></span>            | <span data-ttu-id="7f994-137">Schwarz</span><span class="sxs-lookup"><span data-stu-id="7f994-137">Black</span></span>                       |
| <span data-ttu-id="7f994-138">Rosenholz</span><span class="sxs-lookup"><span data-stu-id="7f994-138">Rosewood</span></span>       | <span data-ttu-id="7f994-139">Weiß</span><span class="sxs-lookup"><span data-stu-id="7f994-139">White</span></span>                       |
| <span data-ttu-id="7f994-140">Weiß</span><span class="sxs-lookup"><span data-stu-id="7f994-140">White</span></span>          | <span data-ttu-id="7f994-141">Schwarz</span><span class="sxs-lookup"><span data-stu-id="7f994-141">Black</span></span>                       |
| <span data-ttu-id="7f994-142">Weiß</span><span class="sxs-lookup"><span data-stu-id="7f994-142">White</span></span>          | <span data-ttu-id="7f994-143">Weiß</span><span class="sxs-lookup"><span data-stu-id="7f994-143">White</span></span>                       |
| <span data-ttu-id="7f994-144">Schwarz</span><span class="sxs-lookup"><span data-stu-id="7f994-144">Black</span></span>          | <span data-ttu-id="7f994-145">Schwarz</span><span class="sxs-lookup"><span data-stu-id="7f994-145">Black</span></span>                       |
| <span data-ttu-id="7f994-146">Schwarz</span><span class="sxs-lookup"><span data-stu-id="7f994-146">Black</span></span>          | <span data-ttu-id="7f994-147">Metall</span><span class="sxs-lookup"><span data-stu-id="7f994-147">Metal</span></span>                       | 

<span data-ttu-id="7f994-148">Sie können die systemdefinierte und benutzerdefinierte Tabelleneinschränkungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="7f994-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="7f994-149">Weitere Informationen finden Sie unter [Systemdefinierte und benutzerdefinierte Tabelleneinschränkungen](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="7f994-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="7f994-150">Welche Syntax soll verwendet werden, um Einschränkungen in  aufzuheben?</span><span class="sxs-lookup"><span data-stu-id="7f994-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="7f994-151">Sie müssen Optimization Modeling Language (OML)-Syntax verwenden, wenn Sie die Einschränkungen schreiben.</span><span class="sxs-lookup"><span data-stu-id="7f994-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="7f994-152">Das System verwendet Microsoft Solver Foundation-Einschränkungswandler, um die Einschränkungen zu beheben.</span><span class="sxs-lookup"><span data-stu-id="7f994-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="7f994-153">Soll ich Tabelleneinschränkungen oder Ausdruckseinschränkungen verwenden?</span><span class="sxs-lookup"><span data-stu-id="7f994-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="7f994-154">Sie können entweder Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="7f994-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="7f994-155">Sie bauen eine Tabelleneinschränkung als Matrix auf, während eine Ausdruckseinschränkung ein einzelner Auszug ist.</span><span class="sxs-lookup"><span data-stu-id="7f994-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="7f994-156">Wenn Sie ein Produkt konfigurieren, ist es nicht von Bedeutung, welche Art von Einschränkung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f994-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="7f994-157">Im folgenden Beispiel werden die Unterschiede der zwei zur Verfügung stehenden Optionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7f994-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="7f994-158">Wenn Sie ein Produkt konfigurieren, indem Sie die folgenden Einschränkungseinstellungen verwenden, sind diese Kombinationen zulässig:</span><span class="sxs-lookup"><span data-stu-id="7f994-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="7f994-159">Ein Produkt in der Farbe Schwarz und mit Größe 30 oder 50</span><span class="sxs-lookup"><span data-stu-id="7f994-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="7f994-160">Ein Produkt in der Farbe Rot und mit Größe 20</span><span class="sxs-lookup"><span data-stu-id="7f994-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="7f994-161">Tabelleneinschränkungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="7f994-161">Table constraint setup</span></span>

| <span data-ttu-id="7f994-162">Farbe</span><span class="sxs-lookup"><span data-stu-id="7f994-162">Color</span></span> | <span data-ttu-id="7f994-163">Größe</span><span class="sxs-lookup"><span data-stu-id="7f994-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="7f994-164">Schwarz</span><span class="sxs-lookup"><span data-stu-id="7f994-164">Black</span></span> | <span data-ttu-id="7f994-165">30</span><span class="sxs-lookup"><span data-stu-id="7f994-165">30</span></span>   |
| <span data-ttu-id="7f994-166">Schwarz</span><span class="sxs-lookup"><span data-stu-id="7f994-166">Black</span></span> | <span data-ttu-id="7f994-167">50</span><span class="sxs-lookup"><span data-stu-id="7f994-167">50</span></span>   |
| <span data-ttu-id="7f994-168">Rot</span><span class="sxs-lookup"><span data-stu-id="7f994-168">Red</span></span>   | <span data-ttu-id="7f994-169">20</span><span class="sxs-lookup"><span data-stu-id="7f994-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="7f994-170">Einrichtung von Ausdruckseinschränkungen</span><span class="sxs-lookup"><span data-stu-id="7f994-170">Expression constraint setup</span></span>

<span data-ttu-id="7f994-171">(Farbe == "Schwarz" & (Größe == "30" | Größe == "50")) | (Farbe == "Rot" & Größe = "20")</span><span class="sxs-lookup"><span data-stu-id="7f994-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="7f994-172">Muss ich Operatoren oder Infixschreibweise verwenden, wenn ich Ausdruckseinschränkungen schreibe?</span><span class="sxs-lookup"><span data-stu-id="7f994-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="7f994-173">Sie können eine Ausdruckseinschränkung schreiben, indem Sie entweder die verfügbaren Präfixoperatoren oder die Infixschreibweise verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f994-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="7f994-174">Für die Operatoren **Min**, **Max** und **Abs** können Sie die Infixschreibweise nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f994-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="7f994-175">Diese Operatoren sind als Standard in den meisten Programmiersprachen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="7f994-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="7f994-176">Welche Operatoren und Infixschreibweise kann ich verwenden, wenn ich Ausdruckseinschränkungen schreibe?</span><span class="sxs-lookup"><span data-stu-id="7f994-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="7f994-177">In den folgenden Tabellen werden die Operatoren und Infixschreibweise aufgelistet, die Sie verwenden können, wenn Sie eine Ausdruckseinschränkung für eine Komponente in einem Produktkonfigurationsmodell schreiben.</span><span class="sxs-lookup"><span data-stu-id="7f994-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="7f994-178">Den Beispielen in dieser ersten Tabelle können Sie entnehmen, wie Sie einen Ausdruck schreiben, indem Sie entweder Infixschreibweise oder Operatoren verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f994-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f994-179">Bediener</span><span class="sxs-lookup"><span data-stu-id="7f994-179">Operator</span></span></th>
<th><span data-ttu-id="7f994-180">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f994-180">Description</span></span></th>
<th><span data-ttu-id="7f994-181">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f994-181">Syntax</span></span></th>
<th><span data-ttu-id="7f994-182">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f994-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f994-183">Bedeutet</span><span class="sxs-lookup"><span data-stu-id="7f994-183">Implies</span></span></td>
<td><span data-ttu-id="7f994-184">Dies gilt, wenn die erste Bedingung nicht zutrifft, die zweite Bedingung erfüllt wird, oder beide.</span><span class="sxs-lookup"><span data-stu-id="7f994-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="7f994-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="7f994-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="7f994-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="7f994-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="7f994-187"><strong>Infixschreibweise:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="7f994-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f994-188">Und</span><span class="sxs-lookup"><span data-stu-id="7f994-188">And</span></span></td>
<td><span data-ttu-id="7f994-189">Dies gilt nur, wenn alle Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="7f994-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="7f994-190">Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>Wahr</strong>.</span><span class="sxs-lookup"><span data-stu-id="7f994-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="7f994-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="7f994-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="7f994-192"><strong>Operator:</strong> Und[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="7f994-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="7f994-193"><strong>Infixschreibweise:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="7f994-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f994-194">Oder</span><span class="sxs-lookup"><span data-stu-id="7f994-194">Or</span></span></td>
<td><span data-ttu-id="7f994-195">Dies trifft zu, wenn jede Bedingung wahr ist.</span><span class="sxs-lookup"><span data-stu-id="7f994-195">This is true if any condition is true.</span></span> <span data-ttu-id="7f994-196">Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>Falsch</strong>.</span><span class="sxs-lookup"><span data-stu-id="7f994-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="7f994-197">Oder[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="7f994-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="7f994-198"><strong>Operator:</strong> Oder[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="7f994-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="7f994-199"><strong>Infixschreibweise:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="7f994-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f994-200">Plus</span><span class="sxs-lookup"><span data-stu-id="7f994-200">Plus</span></span></td>
<td><span data-ttu-id="7f994-201">Dies summiert die Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="7f994-201">This sums its conditions.</span></span> <span data-ttu-id="7f994-202">Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="7f994-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="7f994-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="7f994-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="7f994-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="7f994-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="7f994-205"><strong>Infixschreibweise</strong>: x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="7f994-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f994-206">Minus</span><span class="sxs-lookup"><span data-stu-id="7f994-206">Minus</span></span></td>
<td><span data-ttu-id="7f994-207">Dies negiert das Argument.</span><span class="sxs-lookup"><span data-stu-id="7f994-207">This negates its argument.</span></span> <span data-ttu-id="7f994-208">Dies muss genau eine Bedingung haben.</span><span class="sxs-lookup"><span data-stu-id="7f994-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="7f994-209">Minus[expr], Infix: -expr</span><span class="sxs-lookup"><span data-stu-id="7f994-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="7f994-210"><strong>Operator:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="7f994-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="7f994-211"><strong>Infixschreibweise:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="7f994-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f994-212">Abs</span><span class="sxs-lookup"><span data-stu-id="7f994-212">Abs</span></span></td>
<td><span data-ttu-id="7f994-213">Dies nimmt den absoluten Wert der Bedingung.</span><span class="sxs-lookup"><span data-stu-id="7f994-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="7f994-214">Dies muss genau eine Bedingung haben.</span><span class="sxs-lookup"><span data-stu-id="7f994-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="7f994-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="7f994-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="7f994-216"><strong>Operator:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="7f994-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f994-217">Zeiten</span><span class="sxs-lookup"><span data-stu-id="7f994-217">Times</span></span></td>
<td><span data-ttu-id="7f994-218">Dies nimmt das Produkt der Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="7f994-218">This takes the product of its conditions.</span></span> <span data-ttu-id="7f994-219">Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="7f994-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="7f994-220">Times[args], infix: a * b * ... * z</span><span class="sxs-lookup"><span data-stu-id="7f994-220">Times[args], infix: a * b * ... * z</span></span></td>
<td><ul>
<li><span data-ttu-id="7f994-221"><strong>Operator:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="7f994-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="7f994-222"><strong>Infixschreibweise</strong>: x * y * 2 == z</span><span class="sxs-lookup"><span data-stu-id="7f994-222"><strong>Infix notation:</strong> x * y * 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f994-223">Antriebskraft</span><span class="sxs-lookup"><span data-stu-id="7f994-223">Power</span></span></td>
<td><span data-ttu-id="7f994-224">Dies nimmt einen exponentiellen Wert.</span><span class="sxs-lookup"><span data-stu-id="7f994-224">This takes an exponential.</span></span> <span data-ttu-id="7f994-225">Dies wendet die Exponenten von rechts nach links an.</span><span class="sxs-lookup"><span data-stu-id="7f994-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="7f994-226">(Das bedeutet, dass dies rechtsverknüpfend ist.) Deshalb P<strong>Power[a, b, c]</strong> ist gleich <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="7f994-226">(In other words, it's right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="7f994-227"><strong>Power</strong> kann nur mit einer positiven Konstante als Exponent verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f994-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="7f994-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="7f994-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="7f994-229"><strong>Operator:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="7f994-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="7f994-230"><strong>Infixschreibweise:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="7f994-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f994-231">Max.</span><span class="sxs-lookup"><span data-stu-id="7f994-231">Max</span></span></td>
<td><span data-ttu-id="7f994-232">Dies produziert die umfangreichste Bedingung.</span><span class="sxs-lookup"><span data-stu-id="7f994-232">This produces the largest condition.</span></span> <span data-ttu-id="7f994-233">Wenn die Anzahl der Bedingungen 0 (Null) ist, produziert dies <strong>Unendlich</strong>.</span><span class="sxs-lookup"><span data-stu-id="7f994-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="7f994-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="7f994-234">Max[args]</span></span></td>
<td><span data-ttu-id="7f994-235"><strong>Operator:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="7f994-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f994-236">Min.</span><span class="sxs-lookup"><span data-stu-id="7f994-236">Min</span></span></td>
<td><span data-ttu-id="7f994-237">Dies produziert die kleinste Bedingung.</span><span class="sxs-lookup"><span data-stu-id="7f994-237">This produces the smallest condition.</span></span> <span data-ttu-id="7f994-238">Wenn die Anzahl der Bedingungen 0 (Null) ist, produziert dies <strong>Unendlich</strong>.</span><span class="sxs-lookup"><span data-stu-id="7f994-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="7f994-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="7f994-239">Min[args]</span></span></td>
<td><span data-ttu-id="7f994-240"><strong>Operator:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="7f994-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f994-241">Nicht</span><span class="sxs-lookup"><span data-stu-id="7f994-241">Not</span></span></td>
<td><span data-ttu-id="7f994-242">Dies produziert die logische Umkehrung der Bedingung.</span><span class="sxs-lookup"><span data-stu-id="7f994-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="7f994-243">Dies muss genau eine Bedingung haben.</span><span class="sxs-lookup"><span data-stu-id="7f994-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="7f994-244">Not[expr], Infix: !expr</span><span class="sxs-lookup"><span data-stu-id="7f994-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="7f994-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="7f994-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="7f994-246"><strong>Infixschreibweise:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="7f994-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7f994-247">Die Beispiele in der nächsten Tabellen zeigen, wie eine Infixnotation geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7f994-247">The examples in the next table show how to write infix notation.</span></span>

| <span data-ttu-id="7f994-248">Infixschreibweise</span><span class="sxs-lookup"><span data-stu-id="7f994-248">Infix notation</span></span>    | <span data-ttu-id="7f994-249">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f994-249">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f994-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="7f994-250">x + y + z</span></span>         | <span data-ttu-id="7f994-251">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="7f994-251">Addition</span></span>                                                                                      |
| <span data-ttu-id="7f994-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="7f994-252">x \* y \* z</span></span>       | <span data-ttu-id="7f994-253">Multiplikation</span><span class="sxs-lookup"><span data-stu-id="7f994-253">Multiplication</span></span>                                                                                |
| <span data-ttu-id="7f994-254">x - y</span><span class="sxs-lookup"><span data-stu-id="7f994-254">x - y</span></span>             | <span data-ttu-id="7f994-255">Die binäre Subtraktion wird auf die gleiche Weise wie die binäre Addition bei einer negierten Sekunde übersetzt.</span><span class="sxs-lookup"><span data-stu-id="7f994-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
| <span data-ttu-id="7f994-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="7f994-256">x ^ y ^ z</span></span>         | <span data-ttu-id="7f994-257">Exponenten mit Rechtsverknüpfung</span><span class="sxs-lookup"><span data-stu-id="7f994-257">Exponentiation that has right associativity</span></span>                                                   |
| <span data-ttu-id="7f994-258">!x</span><span class="sxs-lookup"><span data-stu-id="7f994-258">!x</span></span>                | <span data-ttu-id="7f994-259">Boolesches not</span><span class="sxs-lookup"><span data-stu-id="7f994-259">Boolean not</span></span>                                                                                   |
| <span data-ttu-id="7f994-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="7f994-260">x -: y</span></span>            | <span data-ttu-id="7f994-261">Boolesche Auswirkung</span><span class="sxs-lookup"><span data-stu-id="7f994-261">Boolean implication</span></span>                                                                           |
| <span data-ttu-id="7f994-262"> -</span><span class="sxs-lookup"><span data-stu-id="7f994-262">x</span></span> | <span data-ttu-id="7f994-263">y</span><span class="sxs-lookup"><span data-stu-id="7f994-263">y</span></span> | <span data-ttu-id="7f994-264">z</span><span class="sxs-lookup"><span data-stu-id="7f994-264">z</span></span>         | <span data-ttu-id="7f994-265">Boolesches or</span><span class="sxs-lookup"><span data-stu-id="7f994-265">Boolean or</span></span>                                                                                    |
| <span data-ttu-id="7f994-266">x & y & z</span><span class="sxs-lookup"><span data-stu-id="7f994-266">x & y & z</span></span>         | <span data-ttu-id="7f994-267">Boolesches and</span><span class="sxs-lookup"><span data-stu-id="7f994-267">Boolean and</span></span>                                                                                   |
| <span data-ttu-id="7f994-268">x == y == z</span><span class="sxs-lookup"><span data-stu-id="7f994-268">x == y == z</span></span>       | <span data-ttu-id="7f994-269">Gleichheit</span><span class="sxs-lookup"><span data-stu-id="7f994-269">Equality</span></span>                                                                                      |
| <span data-ttu-id="7f994-270">x != y != z</span><span class="sxs-lookup"><span data-stu-id="7f994-270">x != y != z</span></span>       | <span data-ttu-id="7f994-271">Getrennt</span><span class="sxs-lookup"><span data-stu-id="7f994-271">Distinct</span></span>                                                                                      |
| <span data-ttu-id="7f994-272">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="7f994-272">x &lt; y &lt; z</span></span>   | <span data-ttu-id="7f994-273">Kleiner als</span><span class="sxs-lookup"><span data-stu-id="7f994-273">Less than</span></span>                                                                                     |
| <span data-ttu-id="7f994-274">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="7f994-274">x &gt; y &gt; z</span></span>   | <span data-ttu-id="7f994-275">Größer als</span><span class="sxs-lookup"><span data-stu-id="7f994-275">Greater than</span></span>                                                                                  |
| <span data-ttu-id="7f994-276">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="7f994-276">x &lt;= y &lt;= z</span></span> | <span data-ttu-id="7f994-277">Kleiner oder gleich</span><span class="sxs-lookup"><span data-stu-id="7f994-277">Less than or equal to</span></span>                                                                         |
| <span data-ttu-id="7f994-278">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="7f994-278">x &gt;= y &gt;= z</span></span> | <span data-ttu-id="7f994-279">Größer oder gleich</span><span class="sxs-lookup"><span data-stu-id="7f994-279">Greater than or equal to</span></span>                                                                      |
| <span data-ttu-id="7f994-280">(x)</span><span class="sxs-lookup"><span data-stu-id="7f994-280">(x)</span></span>               | <span data-ttu-id="7f994-281">Klammern setzten die standardmäßige Rangfolge außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="7f994-281">Parentheses override default precedence.</span></span>                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="7f994-282">Warum werden meine Ausdruckseinschränkungen nicht ordnungsgemäß validiert?</span><span class="sxs-lookup"><span data-stu-id="7f994-282">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="7f994-283">Sie können reservierte Schlüsselwörter nicht als Wandlernamen für Attribute, Komponenten oder Unterkomponenten in einem Produktkonfigurationsmodell verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f994-283">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="7f994-284">Die folgende Tabelle enthält eine Liste der reservierten Schlüsselwörter, die Sie nicht verwenden dürfen.</span><span class="sxs-lookup"><span data-stu-id="7f994-284">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="7f994-285">Decke</span><span class="sxs-lookup"><span data-stu-id="7f994-285">Ceiling</span></span>
-   <span data-ttu-id="7f994-286">Element</span><span class="sxs-lookup"><span data-stu-id="7f994-286">Element</span></span>
-   <span data-ttu-id="7f994-287">Gleich</span><span class="sxs-lookup"><span data-stu-id="7f994-287">Equal</span></span>
-   <span data-ttu-id="7f994-288">Stockwerk</span><span class="sxs-lookup"><span data-stu-id="7f994-288">Floor</span></span>
-   <span data-ttu-id="7f994-289">Falls</span><span class="sxs-lookup"><span data-stu-id="7f994-289">If</span></span>
-   <span data-ttu-id="7f994-290">Kleiner</span><span class="sxs-lookup"><span data-stu-id="7f994-290">Less</span></span>
-   <span data-ttu-id="7f994-291">Größer</span><span class="sxs-lookup"><span data-stu-id="7f994-291">Greater</span></span>
-   <span data-ttu-id="7f994-292">Bedeutet</span><span class="sxs-lookup"><span data-stu-id="7f994-292">Implies</span></span>
-   <span data-ttu-id="7f994-293">Protokoll</span><span class="sxs-lookup"><span data-stu-id="7f994-293">Log</span></span>
-   <span data-ttu-id="7f994-294">Max.</span><span class="sxs-lookup"><span data-stu-id="7f994-294">Max</span></span>
-   <span data-ttu-id="7f994-295">Min.</span><span class="sxs-lookup"><span data-stu-id="7f994-295">Min</span></span>
-   <span data-ttu-id="7f994-296">Minus</span><span class="sxs-lookup"><span data-stu-id="7f994-296">Minus</span></span>
-   <span data-ttu-id="7f994-297">Plus</span><span class="sxs-lookup"><span data-stu-id="7f994-297">Plus</span></span>
-   <span data-ttu-id="7f994-298">Antriebskraft</span><span class="sxs-lookup"><span data-stu-id="7f994-298">Power</span></span>
-   <span data-ttu-id="7f994-299">Zeiten</span><span class="sxs-lookup"><span data-stu-id="7f994-299">Times</span></span>
-   <span data-ttu-id="7f994-300">Zeitrahmen</span><span class="sxs-lookup"><span data-stu-id="7f994-300">Slot</span></span>
-   <span data-ttu-id="7f994-301">Modell</span><span class="sxs-lookup"><span data-stu-id="7f994-301">Model</span></span>
-   <span data-ttu-id="7f994-302">Entscheidung</span><span class="sxs-lookup"><span data-stu-id="7f994-302">Decision</span></span>
-   <span data-ttu-id="7f994-303">Ziel</span><span class="sxs-lookup"><span data-stu-id="7f994-303">Goal</span></span>


<a name="see-also"></a><span data-ttu-id="7f994-304">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f994-304">See also</span></span>
--------

<span data-ttu-id="7f994-305">[Eine Einschränkung eines Ausdrucks erstellen (Aufgabenleitfaden)(/dynamics365/unified-operations/supply-chain/pim/tasks/add-expression-constraint-product-configuration-model)</span><span class="sxs-lookup"><span data-stu-id="7f994-305">[Create an expression constraint (Task guide)(/dynamics365/unified-operations/supply-chain/pim/tasks/add-expression-constraint-product-configuration-model)</span></span>

[<span data-ttu-id="7f994-306">Berechnung zu einem Produktkonfigurationsmodell hinzufügen (Aufgabenleitfaden)</span><span class="sxs-lookup"><span data-stu-id="7f994-306">Add a calculation to a product configuration model (Task guide)</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/add-calculation-product-configuration-model)




