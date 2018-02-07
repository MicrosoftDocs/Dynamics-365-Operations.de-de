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
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 3206e53c4f2659c6d9b9be64b01ac28cdd17bc88
ms.contentlocale: de-de
ms.lasthandoff: 02/07/2018

---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="d56b3-105">Ausdruckseinschränkungen und Tabelleneinschränkungen in Produktkonfigurationsmodellen</span><span class="sxs-lookup"><span data-stu-id="d56b3-105">Expression constraints and table constraints in product configuration models</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d56b3-106">In diesem Thema wird die Verwendung von Ausdruckseinschränkungen und Tabelleneinschränkungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d56b3-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="d56b3-107">Einschränkungen steuern die Attributwerte, die Sie auswählen können, wenn Sie Produkte für einen Auftrag, ein Verkaufsangebot, eine Bestellung oder einen Produktionsauftrag konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d56b3-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="d56b3-108">Sie können Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="d56b3-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="d56b3-109">Einschränkungen steuern die Attributwerte, die Sie auswählen können, wenn Sie Produkte für einen Auftrag, ein Verkaufsangebot, eine Bestellung oder einen Produktionsauftrag konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d56b3-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="d56b3-110">Sie können Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="d56b3-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="d56b3-111">Was sind Ausdruckseinschränkungen?</span><span class="sxs-lookup"><span data-stu-id="d56b3-111">What are expression constraints?</span></span>
<span data-ttu-id="d56b3-112">Ausdruckseinschränkungen werden durch einen Ausdruck bezeichnet, der arithmetische und boolesche Operatoren und Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d56b3-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="d56b3-113">Eine Ausdruckseinschränkung wird für eine bestimmte Komponente in einem Produktkonfigurationsmodell geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d56b3-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="d56b3-114">Sie können nicht von einer anderen Komponente wiederverwendet oder für sie freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d56b3-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="d56b3-115">Die Ausdruckseinschränkungen für eine Komponente können jedoch auf Attribute der Unterkomponenten der Komponente verweisen.</span><span class="sxs-lookup"><span data-stu-id="d56b3-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="d56b3-116">Was sind Tabelleneinschränkungen?</span><span class="sxs-lookup"><span data-stu-id="d56b3-116">What are table constraints?</span></span>
<span data-ttu-id="d56b3-117">Tabelleneinschränkungen listen die Kombinationen von Werten auf, die für Attribute zulässig sind, wenn Sie ein Produkt konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d56b3-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="d56b3-118">Tabelleneinschränkungsdefinitionen können generisch verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d56b3-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="d56b3-119">Wenn Sie eine Tabelleneinschränkung für eine Komponente in einem Produktkonfigurationsmodell erstellen, wählen Sie eine Tabelleneinschränkungsdefinition aus.</span><span class="sxs-lookup"><span data-stu-id="d56b3-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="d56b3-120">Um die Kombinationen zu erstellen, die zulässig sind, fügen Sie Attribute bestimmter Arten den Komponenten hinzu.</span><span class="sxs-lookup"><span data-stu-id="d56b3-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="d56b3-121">Jeder Attributtyp hat einen bestimmten Wert.</span><span class="sxs-lookup"><span data-stu-id="d56b3-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="d56b3-122">Beispiel einer Tabelleneinschränkung</span><span class="sxs-lookup"><span data-stu-id="d56b3-122">Example of a table constraint</span></span>

<span data-ttu-id="d56b3-123">Dieses Beispiel verdeutlicht, wie Sie die Konfiguration eines Lautsprechers auf bestimmte Gehäuseoberflächen und Frontseiten einschränken können.</span><span class="sxs-lookup"><span data-stu-id="d56b3-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="d56b3-124">Die erste Tabelle enthält die Oberflächen und die Frontseiten, die allgemein zur Konfiguration verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d56b3-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="d56b3-125">Die Werte werden für die **Gehäuseoberfläche**-**Vordergerippe**-Attributtypen definiert.</span><span class="sxs-lookup"><span data-stu-id="d56b3-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="d56b3-126">Attributtyp</span><span class="sxs-lookup"><span data-stu-id="d56b3-126">Attribute type</span></span> | <span data-ttu-id="d56b3-127">Werte</span><span class="sxs-lookup"><span data-stu-id="d56b3-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="d56b3-128">Gehäuseoberfläche</span><span class="sxs-lookup"><span data-stu-id="d56b3-128">Cabinet finish</span></span> | <span data-ttu-id="d56b3-129">Schwarz, Eiche, Rosenholz, Weiß</span><span class="sxs-lookup"><span data-stu-id="d56b3-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="d56b3-130">Vordergerippe</span><span class="sxs-lookup"><span data-stu-id="d56b3-130">Front grill</span></span>    | <span data-ttu-id="d56b3-131">Schwarz, Metall, Weiß</span><span class="sxs-lookup"><span data-stu-id="d56b3-131">Black, Metal, White</span></span>         |

<span data-ttu-id="d56b3-132">In der folgenden Tabelle werden die Kombinationen angezeigt, die von der Tabelleneinschränkung **Farbe und Oberfläche** definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d56b3-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="d56b3-133">Mithilfe dieser Tabelleneinschränkung können Sie einen Lautsprecher konfigurieren, der ein Eichenoberfläche und einen schwarzen Grill, eine Rosenholzoberfläche und ein weißer Grill usw. hat.</span><span class="sxs-lookup"><span data-stu-id="d56b3-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="d56b3-134">Fertig stellen</span><span class="sxs-lookup"><span data-stu-id="d56b3-134">Finish</span></span>         | <span data-ttu-id="d56b3-135">Grill</span><span class="sxs-lookup"><span data-stu-id="d56b3-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="d56b3-136">Eiche</span><span class="sxs-lookup"><span data-stu-id="d56b3-136">Oak</span></span>            | <span data-ttu-id="d56b3-137">Schwarz</span><span class="sxs-lookup"><span data-stu-id="d56b3-137">Black</span></span>                       |
| <span data-ttu-id="d56b3-138">Rosenholz</span><span class="sxs-lookup"><span data-stu-id="d56b3-138">Rosewood</span></span>       | <span data-ttu-id="d56b3-139">Weiß</span><span class="sxs-lookup"><span data-stu-id="d56b3-139">White</span></span>                       |
| <span data-ttu-id="d56b3-140">Weiß</span><span class="sxs-lookup"><span data-stu-id="d56b3-140">White</span></span>          | <span data-ttu-id="d56b3-141">Schwarz</span><span class="sxs-lookup"><span data-stu-id="d56b3-141">Black</span></span>                       |
| <span data-ttu-id="d56b3-142">Weiß</span><span class="sxs-lookup"><span data-stu-id="d56b3-142">White</span></span>          | <span data-ttu-id="d56b3-143">Weiß</span><span class="sxs-lookup"><span data-stu-id="d56b3-143">White</span></span>                       |
| <span data-ttu-id="d56b3-144">Schwarz</span><span class="sxs-lookup"><span data-stu-id="d56b3-144">Black</span></span>          | <span data-ttu-id="d56b3-145">Schwarz</span><span class="sxs-lookup"><span data-stu-id="d56b3-145">Black</span></span>                       |
| <span data-ttu-id="d56b3-146">Schwarz</span><span class="sxs-lookup"><span data-stu-id="d56b3-146">Black</span></span>          | <span data-ttu-id="d56b3-147">Metall</span><span class="sxs-lookup"><span data-stu-id="d56b3-147">Metal</span></span>                       | 

<span data-ttu-id="d56b3-148">Sie können die systemdefinierte und benutzerdefinierte Tabelleneinschränkungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="d56b3-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="d56b3-149">Weitere Informationen finden Sie unter [Systemdefinierte und benutzerdefinierte Tabelleneinschränkungen](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="d56b3-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="d56b3-150">Welche Syntax soll verwendet werden, um Einschränkungen in  aufzuheben?</span><span class="sxs-lookup"><span data-stu-id="d56b3-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="d56b3-151">Sie müssen Optimization Modeling Language (OML)-Syntax verwenden, wenn Sie die Einschränkungen schreiben.</span><span class="sxs-lookup"><span data-stu-id="d56b3-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="d56b3-152">Das System verwendet Microsoft Solver Foundation-Einschränkungswandler, um die Einschränkungen zu beheben.</span><span class="sxs-lookup"><span data-stu-id="d56b3-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="d56b3-153">Soll ich Tabelleneinschränkungen oder Ausdruckseinschränkungen verwenden?</span><span class="sxs-lookup"><span data-stu-id="d56b3-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="d56b3-154">Sie können entweder Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="d56b3-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="d56b3-155">Sie bauen eine Tabelleneinschränkung als Matrix auf, während eine Ausdruckseinschränkung ein einzelner Auszug ist.</span><span class="sxs-lookup"><span data-stu-id="d56b3-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="d56b3-156">Wenn Sie ein Produkt konfigurieren, ist es nicht von Bedeutung, welche Art von Einschränkung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d56b3-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="d56b3-157">Im folgenden Beispiel werden die Unterschiede der zwei zur Verfügung stehenden Optionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d56b3-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="d56b3-158">Wenn Sie ein Produkt konfigurieren, indem Sie die folgenden Einschränkungseinstellungen verwenden, sind diese Kombinationen zulässig:</span><span class="sxs-lookup"><span data-stu-id="d56b3-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="d56b3-159">Ein Produkt in der Farbe Schwarz und mit Größe 30 oder 50</span><span class="sxs-lookup"><span data-stu-id="d56b3-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="d56b3-160">Ein Produkt in der Farbe Rot und mit Größe 20</span><span class="sxs-lookup"><span data-stu-id="d56b3-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="d56b3-161">Tabelleneinschränkungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="d56b3-161">Table constraint setup</span></span>

| <span data-ttu-id="d56b3-162">Farbe</span><span class="sxs-lookup"><span data-stu-id="d56b3-162">Color</span></span> | <span data-ttu-id="d56b3-163">Größe</span><span class="sxs-lookup"><span data-stu-id="d56b3-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="d56b3-164">Schwarz</span><span class="sxs-lookup"><span data-stu-id="d56b3-164">Black</span></span> | <span data-ttu-id="d56b3-165">30</span><span class="sxs-lookup"><span data-stu-id="d56b3-165">30</span></span>   |
| <span data-ttu-id="d56b3-166">Schwarz</span><span class="sxs-lookup"><span data-stu-id="d56b3-166">Black</span></span> | <span data-ttu-id="d56b3-167">50</span><span class="sxs-lookup"><span data-stu-id="d56b3-167">50</span></span>   |
| <span data-ttu-id="d56b3-168">Rot</span><span class="sxs-lookup"><span data-stu-id="d56b3-168">Red</span></span>   | <span data-ttu-id="d56b3-169">20</span><span class="sxs-lookup"><span data-stu-id="d56b3-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="d56b3-170">Einrichtung von Ausdruckseinschränkungen</span><span class="sxs-lookup"><span data-stu-id="d56b3-170">Expression constraint setup</span></span>

<span data-ttu-id="d56b3-171">(Farbe == "Schwarz" & (Größe == "30" | Größe == "50")) | (Farbe == "Rot" & Größe = "20")</span><span class="sxs-lookup"><span data-stu-id="d56b3-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="d56b3-172">Muss ich Operatoren oder Infixschreibweise verwenden, wenn ich Ausdruckseinschränkungen schreibe?</span><span class="sxs-lookup"><span data-stu-id="d56b3-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="d56b3-173">Sie können eine Ausdruckseinschränkung schreiben, indem Sie entweder die verfügbaren Präfixoperatoren oder die Infixschreibweise verwenden.</span><span class="sxs-lookup"><span data-stu-id="d56b3-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="d56b3-174">Für die Operatoren **Min**, **Max** und **Abs** können Sie die Infixschreibweise nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="d56b3-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="d56b3-175">Diese Operatoren sind als Standard in den meisten Programmiersprachen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="d56b3-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="d56b3-176">Welche Operatoren und Infixschreibweise kann ich verwenden, wenn ich Ausdruckseinschränkungen schreibe?</span><span class="sxs-lookup"><span data-stu-id="d56b3-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="d56b3-177">In den folgenden Tabellen werden die Operatoren und Infixschreibweise aufgelistet, die Sie verwenden können, wenn Sie eine Ausdruckseinschränkung für eine Komponente in einem Produktkonfigurationsmodell schreiben.</span><span class="sxs-lookup"><span data-stu-id="d56b3-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="d56b3-178">Den Beispielen in dieser ersten Tabelle können Sie entnehmen, wie Sie einen Ausdruck schreiben, indem Sie entweder Infixschreibweise oder Operatoren verwenden.</span><span class="sxs-lookup"><span data-stu-id="d56b3-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d56b3-179">Bediener</span><span class="sxs-lookup"><span data-stu-id="d56b3-179">Operator</span></span></th>
<th><span data-ttu-id="d56b3-180">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d56b3-180">Description</span></span></th>
<th><span data-ttu-id="d56b3-181">Syntax</span><span class="sxs-lookup"><span data-stu-id="d56b3-181">Syntax</span></span></th>
<th><span data-ttu-id="d56b3-182">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d56b3-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d56b3-183">Bedeutet</span><span class="sxs-lookup"><span data-stu-id="d56b3-183">Implies</span></span></td>
<td><span data-ttu-id="d56b3-184">Dies gilt, wenn die erste Bedingung nicht zutrifft, die zweite Bedingung erfüllt wird, oder beide.</span><span class="sxs-lookup"><span data-stu-id="d56b3-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="d56b3-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="d56b3-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="d56b3-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="d56b3-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="d56b3-187"><strong>Infixschreibweise:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="d56b3-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d56b3-188">Und</span><span class="sxs-lookup"><span data-stu-id="d56b3-188">And</span></span></td>
<td><span data-ttu-id="d56b3-189">Dies gilt nur, wenn alle Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="d56b3-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="d56b3-190">Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>Wahr</strong>.</span><span class="sxs-lookup"><span data-stu-id="d56b3-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="d56b3-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="d56b3-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="d56b3-192"><strong>Operator:</strong> Und[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="d56b3-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="d56b3-193"><strong>Infixschreibweise:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="d56b3-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d56b3-194">Oder</span><span class="sxs-lookup"><span data-stu-id="d56b3-194">Or</span></span></td>
<td><span data-ttu-id="d56b3-195">Dies trifft zu, wenn jede Bedingung wahr ist.</span><span class="sxs-lookup"><span data-stu-id="d56b3-195">This is true if any condition is true.</span></span> <span data-ttu-id="d56b3-196">Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>Falsch</strong>.</span><span class="sxs-lookup"><span data-stu-id="d56b3-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="d56b3-197">Oder[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="d56b3-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="d56b3-198"><strong>Operator:</strong> Oder[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="d56b3-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="d56b3-199"><strong>Infixschreibweise:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="d56b3-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d56b3-200">Plus</span><span class="sxs-lookup"><span data-stu-id="d56b3-200">Plus</span></span></td>
<td><span data-ttu-id="d56b3-201">Dies summiert die Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="d56b3-201">This sums its conditions.</span></span> <span data-ttu-id="d56b3-202">Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="d56b3-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="d56b3-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="d56b3-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="d56b3-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="d56b3-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="d56b3-205"><strong>Infixschreibweise</strong>: x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="d56b3-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d56b3-206">Minus</span><span class="sxs-lookup"><span data-stu-id="d56b3-206">Minus</span></span></td>
<td><span data-ttu-id="d56b3-207">Dies negiert das Argument.</span><span class="sxs-lookup"><span data-stu-id="d56b3-207">This negates its argument.</span></span> <span data-ttu-id="d56b3-208">Dies muss genau eine Bedingung haben.</span><span class="sxs-lookup"><span data-stu-id="d56b3-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="d56b3-209">Minus[expr], Infix: -expr</span><span class="sxs-lookup"><span data-stu-id="d56b3-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="d56b3-210"><strong>Operator:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="d56b3-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="d56b3-211"><strong>Infixschreibweise:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="d56b3-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d56b3-212">Abs</span><span class="sxs-lookup"><span data-stu-id="d56b3-212">Abs</span></span></td>
<td><span data-ttu-id="d56b3-213">Dies nimmt den absoluten Wert der Bedingung.</span><span class="sxs-lookup"><span data-stu-id="d56b3-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="d56b3-214">Dies muss genau eine Bedingung haben.</span><span class="sxs-lookup"><span data-stu-id="d56b3-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="d56b3-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="d56b3-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="d56b3-216"><strong>Operator:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="d56b3-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d56b3-217">Zeiten</span><span class="sxs-lookup"><span data-stu-id="d56b3-217">Times</span></span></td>
<td><span data-ttu-id="d56b3-218">Dies nimmt das Produkt der Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="d56b3-218">This takes the product of its conditions.</span></span> <span data-ttu-id="d56b3-219">Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="d56b3-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="d56b3-220">Times[args], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="d56b3-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="d56b3-221"><strong>Operator:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="d56b3-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="d56b3-222"><strong>Infixschreibweise</strong>: x * y * 2 == z</span><span class="sxs-lookup"><span data-stu-id="d56b3-222"><strong>Infix notation:</strong> x * y * 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d56b3-223">Antriebskraft</span><span class="sxs-lookup"><span data-stu-id="d56b3-223">Power</span></span></td>
<td><span data-ttu-id="d56b3-224">Dies nimmt einen exponentiellen Wert.</span><span class="sxs-lookup"><span data-stu-id="d56b3-224">This takes an exponential.</span></span> <span data-ttu-id="d56b3-225">Dies wendet die Exponenten von rechts nach links an.</span><span class="sxs-lookup"><span data-stu-id="d56b3-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="d56b3-226">(Das bedeutet, dass dies rechtsverknüpfend ist.) Deshalb P<strong>Power[a, b, c]</strong> ist gleich <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="d56b3-226">(In other words, it's right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="d56b3-227"><strong>Power</strong> kann nur mit einer positiven Konstante als Exponent verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d56b3-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="d56b3-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="d56b3-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="d56b3-229"><strong>Operator:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="d56b3-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="d56b3-230"><strong>Infixschreibweise:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="d56b3-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d56b3-231">Max.</span><span class="sxs-lookup"><span data-stu-id="d56b3-231">Max</span></span></td>
<td><span data-ttu-id="d56b3-232">Dies produziert die umfangreichste Bedingung.</span><span class="sxs-lookup"><span data-stu-id="d56b3-232">This produces the largest condition.</span></span> <span data-ttu-id="d56b3-233">Wenn die Anzahl der Bedingungen 0 (Null) ist, produziert dies <strong>Unendlich</strong>.</span><span class="sxs-lookup"><span data-stu-id="d56b3-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="d56b3-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="d56b3-234">Max[args]</span></span></td>
<td><span data-ttu-id="d56b3-235"><strong>Operator:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="d56b3-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d56b3-236">Min.</span><span class="sxs-lookup"><span data-stu-id="d56b3-236">Min</span></span></td>
<td><span data-ttu-id="d56b3-237">Dies produziert die kleinste Bedingung.</span><span class="sxs-lookup"><span data-stu-id="d56b3-237">This produces the smallest condition.</span></span> <span data-ttu-id="d56b3-238">Wenn die Anzahl der Bedingungen 0 (Null) ist, produziert dies <strong>Unendlich</strong>.</span><span class="sxs-lookup"><span data-stu-id="d56b3-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="d56b3-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="d56b3-239">Min[args]</span></span></td>
<td><span data-ttu-id="d56b3-240"><strong>Operator:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="d56b3-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d56b3-241">Nicht</span><span class="sxs-lookup"><span data-stu-id="d56b3-241">Not</span></span></td>
<td><span data-ttu-id="d56b3-242">Dies produziert die logische Umkehrung der Bedingung.</span><span class="sxs-lookup"><span data-stu-id="d56b3-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="d56b3-243">Dies muss genau eine Bedingung haben.</span><span class="sxs-lookup"><span data-stu-id="d56b3-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="d56b3-244">Not[expr], Infix: !expr</span><span class="sxs-lookup"><span data-stu-id="d56b3-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="d56b3-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="d56b3-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="d56b3-246"><strong>Infixschreibweise:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="d56b3-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d56b3-247">Die Beispiele in der nächsten Tabellen zeigen, wie eine Infixnotation geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="d56b3-247">The examples in the next table show how to write infix notation.</span></span>

| <span data-ttu-id="d56b3-248">Infixschreibweise</span><span class="sxs-lookup"><span data-stu-id="d56b3-248">Infix notation</span></span>    | <span data-ttu-id="d56b3-249">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d56b3-249">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d56b3-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="d56b3-250">x + y + z</span></span>         | <span data-ttu-id="d56b3-251">Hinzufügung</span><span class="sxs-lookup"><span data-stu-id="d56b3-251">Addition</span></span>                                                                                      |
| <span data-ttu-id="d56b3-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="d56b3-252">x \* y \* z</span></span>       | <span data-ttu-id="d56b3-253">Multiplikation</span><span class="sxs-lookup"><span data-stu-id="d56b3-253">Multiplication</span></span>                                                                                |
| <span data-ttu-id="d56b3-254">x - y</span><span class="sxs-lookup"><span data-stu-id="d56b3-254">x - y</span></span>             | <span data-ttu-id="d56b3-255">Die binäre Subtraktion wird auf die gleiche Weise wie die binäre Addition bei einer negierten Sekunde übersetzt.</span><span class="sxs-lookup"><span data-stu-id="d56b3-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
| <span data-ttu-id="d56b3-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="d56b3-256">x ^ y ^ z</span></span>         | <span data-ttu-id="d56b3-257">Exponenten mit Rechtsverknüpfung</span><span class="sxs-lookup"><span data-stu-id="d56b3-257">Exponentiation that has right associativity</span></span>                                                   |
| <span data-ttu-id="d56b3-258">!x</span><span class="sxs-lookup"><span data-stu-id="d56b3-258">!x</span></span>                | <span data-ttu-id="d56b3-259">Boolesches not</span><span class="sxs-lookup"><span data-stu-id="d56b3-259">Boolean not</span></span>                                                                                   |
| <span data-ttu-id="d56b3-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="d56b3-260">x -: y</span></span>            | <span data-ttu-id="d56b3-261">Boolesche Auswirkung</span><span class="sxs-lookup"><span data-stu-id="d56b3-261">Boolean implication</span></span>                                                                           |
| <span data-ttu-id="d56b3-262"> -</span><span class="sxs-lookup"><span data-stu-id="d56b3-262">x</span></span> | <span data-ttu-id="d56b3-263">y</span><span class="sxs-lookup"><span data-stu-id="d56b3-263">y</span></span> | <span data-ttu-id="d56b3-264">z</span><span class="sxs-lookup"><span data-stu-id="d56b3-264">z</span></span>         | <span data-ttu-id="d56b3-265">Boolesches or</span><span class="sxs-lookup"><span data-stu-id="d56b3-265">Boolean or</span></span>                                                                                    |
| <span data-ttu-id="d56b3-266">x & y & z</span><span class="sxs-lookup"><span data-stu-id="d56b3-266">x & y & z</span></span>         | <span data-ttu-id="d56b3-267">Boolesches and</span><span class="sxs-lookup"><span data-stu-id="d56b3-267">Boolean and</span></span>                                                                                   |
| <span data-ttu-id="d56b3-268">x == y == z</span><span class="sxs-lookup"><span data-stu-id="d56b3-268">x == y == z</span></span>       | <span data-ttu-id="d56b3-269">Gleichheit</span><span class="sxs-lookup"><span data-stu-id="d56b3-269">Equality</span></span>                                                                                      |
| <span data-ttu-id="d56b3-270">x != y != z</span><span class="sxs-lookup"><span data-stu-id="d56b3-270">x != y != z</span></span>       | <span data-ttu-id="d56b3-271">Getrennt</span><span class="sxs-lookup"><span data-stu-id="d56b3-271">Distinct</span></span>                                                                                      |
| <span data-ttu-id="d56b3-272">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="d56b3-272">x &lt; y &lt; z</span></span>   | <span data-ttu-id="d56b3-273">Kleiner als</span><span class="sxs-lookup"><span data-stu-id="d56b3-273">Less than</span></span>                                                                                     |
| <span data-ttu-id="d56b3-274">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="d56b3-274">x &gt; y &gt; z</span></span>   | <span data-ttu-id="d56b3-275">Größer als</span><span class="sxs-lookup"><span data-stu-id="d56b3-275">Greater than</span></span>                                                                                  |
| <span data-ttu-id="d56b3-276">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="d56b3-276">x &lt;= y &lt;= z</span></span> | <span data-ttu-id="d56b3-277">Kleiner oder gleich</span><span class="sxs-lookup"><span data-stu-id="d56b3-277">Less than or equal to</span></span>                                                                         |
| <span data-ttu-id="d56b3-278">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="d56b3-278">x &gt;= y &gt;= z</span></span> | <span data-ttu-id="d56b3-279">Größer oder gleich</span><span class="sxs-lookup"><span data-stu-id="d56b3-279">Greater than or equal to</span></span>                                                                      |
| <span data-ttu-id="d56b3-280">(x)</span><span class="sxs-lookup"><span data-stu-id="d56b3-280">(x)</span></span>               | <span data-ttu-id="d56b3-281">Klammern setzten die standardmäßige Rangfolge außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="d56b3-281">Parentheses override default precedence.</span></span>                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="d56b3-282">Warum werden meine Ausdruckseinschränkungen nicht ordnungsgemäß validiert?</span><span class="sxs-lookup"><span data-stu-id="d56b3-282">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="d56b3-283">Sie können reservierte Schlüsselwörter nicht als Wandlernamen für Attribute, Komponenten oder Unterkomponenten in einem Produktkonfigurationsmodell verwenden.</span><span class="sxs-lookup"><span data-stu-id="d56b3-283">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="d56b3-284">Die folgende Tabelle enthält eine Liste der reservierten Schlüsselwörter, die Sie nicht verwenden dürfen.</span><span class="sxs-lookup"><span data-stu-id="d56b3-284">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="d56b3-285">Decke</span><span class="sxs-lookup"><span data-stu-id="d56b3-285">Ceiling</span></span>
-   <span data-ttu-id="d56b3-286">Element</span><span class="sxs-lookup"><span data-stu-id="d56b3-286">Element</span></span>
-   <span data-ttu-id="d56b3-287">Gleich</span><span class="sxs-lookup"><span data-stu-id="d56b3-287">Equal</span></span>
-   <span data-ttu-id="d56b3-288">Stockwerk</span><span class="sxs-lookup"><span data-stu-id="d56b3-288">Floor</span></span>
-   <span data-ttu-id="d56b3-289">Falls</span><span class="sxs-lookup"><span data-stu-id="d56b3-289">If</span></span>
-   <span data-ttu-id="d56b3-290">Kleiner</span><span class="sxs-lookup"><span data-stu-id="d56b3-290">Less</span></span>
-   <span data-ttu-id="d56b3-291">Größer</span><span class="sxs-lookup"><span data-stu-id="d56b3-291">Greater</span></span>
-   <span data-ttu-id="d56b3-292">Bedeutet</span><span class="sxs-lookup"><span data-stu-id="d56b3-292">Implies</span></span>
-   <span data-ttu-id="d56b3-293">Protokoll</span><span class="sxs-lookup"><span data-stu-id="d56b3-293">Log</span></span>
-   <span data-ttu-id="d56b3-294">Max.</span><span class="sxs-lookup"><span data-stu-id="d56b3-294">Max</span></span>
-   <span data-ttu-id="d56b3-295">Min.</span><span class="sxs-lookup"><span data-stu-id="d56b3-295">Min</span></span>
-   <span data-ttu-id="d56b3-296">Minus</span><span class="sxs-lookup"><span data-stu-id="d56b3-296">Minus</span></span>
-   <span data-ttu-id="d56b3-297">Plus</span><span class="sxs-lookup"><span data-stu-id="d56b3-297">Plus</span></span>
-   <span data-ttu-id="d56b3-298">Antriebskraft</span><span class="sxs-lookup"><span data-stu-id="d56b3-298">Power</span></span>
-   <span data-ttu-id="d56b3-299">Zeiten</span><span class="sxs-lookup"><span data-stu-id="d56b3-299">Times</span></span>
-   <span data-ttu-id="d56b3-300">Zeitrahmen</span><span class="sxs-lookup"><span data-stu-id="d56b3-300">Slot</span></span>
-   <span data-ttu-id="d56b3-301">Modell</span><span class="sxs-lookup"><span data-stu-id="d56b3-301">Model</span></span>
-   <span data-ttu-id="d56b3-302">Entscheidung</span><span class="sxs-lookup"><span data-stu-id="d56b3-302">Decision</span></span>
-   <span data-ttu-id="d56b3-303">Ziel</span><span class="sxs-lookup"><span data-stu-id="d56b3-303">Goal</span></span>


<a name="see-also"></a><span data-ttu-id="d56b3-304">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d56b3-304">See also</span></span>
--------

<span data-ttu-id="d56b3-305">[Eine Ausdruckseinschränkung erstellen (Aufgabenleitfaden)(tasks/add-expression-constraint-product-configuration-model.md)</span><span class="sxs-lookup"><span data-stu-id="d56b3-305">[Create an expression constraint (Task guide)(tasks/add-expression-constraint-product-configuration-model.md)</span></span>

[<span data-ttu-id="d56b3-306">Berechnung zu einem Produktkonfigurationsmodell hinzufügen (Aufgabenleitfaden)</span><span class="sxs-lookup"><span data-stu-id="d56b3-306">Add a calculation to a product configuration model (Task guide)</span></span>](tasks/add-calculation-product-configuration-model.md)




