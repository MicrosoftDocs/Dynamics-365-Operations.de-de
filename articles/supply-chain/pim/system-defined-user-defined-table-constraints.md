---
title: Systemdefinierte und benutzerdefinierte Tabelleneinschränkungen
description: 'Dieser Artikel beschreibt die zwei Arten von Tabelleneinschränkungen für Komponenten in einem Produktkonfigurationsmodell: benutzerdefiniert und systemdefiniert. Tabelleneinschränkungen stellen Matrizes der zulässigen Attributkombinationen dar, in denen jede Zeile einen Satz möglicher Attributwerte definiert.'
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3fb1395859b5abd06539e07ada3d968b2e9c9147
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428719"
---
# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="00040-104">Systemdefinierte und benutzerdefinierte Tabelleneinschränkungen</span><span class="sxs-lookup"><span data-stu-id="00040-104">System-defined and user-defined table constraints</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00040-105">Dieser Artikel beschreibt die zwei Arten von Tabelleneinschränkungen für Komponenten in einem Produktkonfigurationsmodell: benutzerdefiniert und systemdefiniert.</span><span class="sxs-lookup"><span data-stu-id="00040-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="00040-106">Tabelleneinschränkungen stellen Matrizes der zulässigen Attributkombinationen dar, in denen jede Zeile einen Satz möglicher Attributwerte definiert.</span><span class="sxs-lookup"><span data-stu-id="00040-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="00040-107">Tabelleneinschränkungen stellen Matrizen aus Kombinationen von Attribute dar, die für Komponenten in einem Produktkonfigurationsmodell zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="00040-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="00040-108">Jede Zeile in der Tabelle definiert einen Satz möglicher Attributwerte.</span><span class="sxs-lookup"><span data-stu-id="00040-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="00040-109">Sie können zwei Typen von Einschränkungen in einem Produktmodell deklarieren:</span><span class="sxs-lookup"><span data-stu-id="00040-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="00040-110">**Ausdruckseinschränkung** – Verwenden Sie Ausdruckseinschränkungen, um Beziehungen zwischen Attributen auszudrücken und sicherzustellen, dass bei der Produktkonfiguration nur kompatible Werte ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="00040-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="00040-111">**Tabelleneinschränkung** – Erstellen Sie eine Tabelle, die alle Kombinationen definiert, die für einen angegebenen Satz Attribute zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="00040-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="00040-112">Zwei Arten von Tabelleneinschränkungen sind verfügbar: benutzerdefinierte Tabelleneinschränkungen und systemdefinierte Tabelleneinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="00040-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="00040-113">In diesem Artikel werden Tabelleneinschränkungen beschrieben, die benutzerdefiniert und für Komponenten in einem Produktkonfigurationsmodell systemdefiniert sind.</span><span class="sxs-lookup"><span data-stu-id="00040-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="00040-114">Benutzerdefinierte Tabelleneinschränkungen</span><span class="sxs-lookup"><span data-stu-id="00040-114">User-defined table constraints</span></span>
<span data-ttu-id="00040-115">Eine benutzerdefinierte Tabelleneinschränkung ist eine Art Matrix, der verwendet wird, um den Satz der Kombinationen für die Attributwerte zu beschreiben, die von Attributtypen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="00040-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="00040-116">Wenn Sie zum Beispiel Lautsprecher herstellen, können Sie Spalten für die Oberfläche und den Grill in die benutzerdefinierte Tabelleneinschränkung einschließen.</span><span class="sxs-lookup"><span data-stu-id="00040-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="00040-117">Der Attributtyp für die Oberfläche besitzt vier Werte, und der Attributtyp für den Grill hat drei Werte.</span><span class="sxs-lookup"><span data-stu-id="00040-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="00040-118">Wenn keine Einschränkungen verwendet werden, gibt es 4 × 3 = 12 Kombinationen.</span><span class="sxs-lookup"><span data-stu-id="00040-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="00040-119">In diesem Beispiel werden jedoch nur sechs Kombinationen zugelassen (wie in der folgenden Tabelle dargestellt)</span><span class="sxs-lookup"><span data-stu-id="00040-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="00040-120">Diese Informationen werden auf der Registerkarte **Zulässige Kombinationen** auf der Seite **Tabelleneinschränkung bearbeiten** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="00040-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="00040-121">Gehäuseoberfläche</span><span class="sxs-lookup"><span data-stu-id="00040-121">Cabinet finish</span></span> | <span data-ttu-id="00040-122">Vordergerippe</span><span class="sxs-lookup"><span data-stu-id="00040-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="00040-123">Schwarz</span><span class="sxs-lookup"><span data-stu-id="00040-123">Black</span></span>          | <span data-ttu-id="00040-124">Schwarz</span><span class="sxs-lookup"><span data-stu-id="00040-124">Black</span></span>       |
| <span data-ttu-id="00040-125">Schwarz</span><span class="sxs-lookup"><span data-stu-id="00040-125">Black</span></span>          | <span data-ttu-id="00040-126">Metall</span><span class="sxs-lookup"><span data-stu-id="00040-126">Metal</span></span>       |
| <span data-ttu-id="00040-127">Eiche</span><span class="sxs-lookup"><span data-stu-id="00040-127">Oak</span></span>            | <span data-ttu-id="00040-128">Schwarz</span><span class="sxs-lookup"><span data-stu-id="00040-128">Black</span></span>       |
| <span data-ttu-id="00040-129">Rosenholz</span><span class="sxs-lookup"><span data-stu-id="00040-129">Rosewood</span></span>       | <span data-ttu-id="00040-130">Weiß</span><span class="sxs-lookup"><span data-stu-id="00040-130">White</span></span>       |
| <span data-ttu-id="00040-131">Weiß</span><span class="sxs-lookup"><span data-stu-id="00040-131">White</span></span>          | <span data-ttu-id="00040-132">Schwarz</span><span class="sxs-lookup"><span data-stu-id="00040-132">Black</span></span>       |
| <span data-ttu-id="00040-133">Weiß</span><span class="sxs-lookup"><span data-stu-id="00040-133">White</span></span>          | <span data-ttu-id="00040-134">Weiß</span><span class="sxs-lookup"><span data-stu-id="00040-134">White</span></span>       |

<span data-ttu-id="00040-135">Benutzerdefinierte Tabelleneinschränkungen werden durch die statische eingegebene Tabelle definiert, die genauso wie eine Ausdruckseinschränkung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="00040-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="00040-136">Wenn Sie eine benutzerdefinierte Tabelleneinschränkung verwenden, ist der Vorteil, dass Tabellen oftmals einfacher zu erstellen zu verstehen und verwalten sind als lange Ausdruckseinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="00040-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="00040-137">Vom System definierte Tabelleneinschränkungen</span><span class="sxs-lookup"><span data-stu-id="00040-137">System-defined table constraints</span></span>
<span data-ttu-id="00040-138">Eine systemdefinierte Tabelleneinschränkung schafft eine dynamische Verknüpfung zwischen einem Attributtyp und einem Feld in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="00040-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="00040-139">Wenn eine systemdefinierte Tabelleneinschränkung in einem Produktkonfigurationsmodell enthalten ist, stellt Zuordnung sicher, dass die Daten in der Tabelle anstelle der Werte des Attributtyps angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="00040-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="00040-140">Das Ergebnis ist eine dynamische Einschränkung, da die Tabelleninhalte bearbeitet werden können (z. B. über andere Module).</span><span class="sxs-lookup"><span data-stu-id="00040-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="00040-141">Wenn Sie eine systemdefinierte Tabelleneinschränkung erstellen, wählen Sie eine Tabelle aus, definieren die optional zu verwendende Abfrage, und ordnen Attributtypen den Feldern in der ausgewählten Tabelle zu.</span><span class="sxs-lookup"><span data-stu-id="00040-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="00040-142">Die Typen der Felder müssen mit den Typen der Attributtypen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="00040-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="00040-143">Bevor sich eine Tabelleneinschränkung auf ein Produktkonfigurationsmodell auswirken kann, muss die Tabelleneinschränkung in einer Einschränkung für eine der Komponenten des Modells einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="00040-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="00040-144">Dazu muss eine neue Einschränkung erstellt und dann erst der Tabelleneinschränkungstyp und anschließend die Tabelleneinschränkungsdefinition gewählt werden, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00040-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="00040-145">Schließlich müssen alle Felder in der Tabelleneinschränkung zu den Attributen im Produktkonfigurationsmodell zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="00040-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

<a name="additional-resources"></a><span data-ttu-id="00040-146">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="00040-146">Additional resources</span></span>
--------

[<span data-ttu-id="00040-147">Produktkonfigurationsmodelle – Überblick</span><span class="sxs-lookup"><span data-stu-id="00040-147">Product configuration models overview</span></span>](product-configuration-models.md)



