---
title: Einem Produktkonfigurationsmodell eine Ausdruckseinschränkung hinzufügen
description: Im folgenden Verfahren sehen Sie, wie Sie einen neuen Einschränkungsausdruck einem Produktkonfigurationsmodell hinzufügen können.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56f94b82f8b2642b12a993bde7d6bb323da79f98
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547147"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="df18b-103">Einem Produktkonfigurationsmodell eine Ausdruckseinschränkung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="df18b-103">Add an expression constraint to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df18b-104">Im folgenden Verfahren sehen Sie, wie Sie einen neuen Einschränkungsausdruck einem Produktkonfigurationsmodell hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="df18b-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="df18b-105">Es zeigt, wie Sie vorgeben, dass der "Eckschutz" an einem Lautsprecher angebracht werden muss, wenn der Benutzer einen vorderen Metallgrill ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="df18b-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="df18b-106">Das Verfahren verwendet die Komponente "High end speaker" im Vorführungsunternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="df18b-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="df18b-107">Erstellen einer Ausdruckseinschränkung</span><span class="sxs-lookup"><span data-stu-id="df18b-107">Create an expression constraint</span></span>
1. <span data-ttu-id="df18b-108">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="df18b-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="df18b-109">Klicken Sie auf "Produktkonfigurationsmodelle".</span><span class="sxs-lookup"><span data-stu-id="df18b-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="df18b-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="df18b-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="df18b-111">Diese Beispiel verwendet das Spitzenlautsprechermodell.</span><span class="sxs-lookup"><span data-stu-id="df18b-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="df18b-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="df18b-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="df18b-113">Erweitern Sie den Abschnitt "Einschränkungen".</span><span class="sxs-lookup"><span data-stu-id="df18b-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="df18b-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="df18b-114">Click Add.</span></span>
7. <span data-ttu-id="df18b-115">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="df18b-115">Click Create.</span></span>
8. <span data-ttu-id="df18b-116">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="df18b-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="df18b-117">Ausdruck eingeben</span><span class="sxs-lookup"><span data-stu-id="df18b-117">Enter expression</span></span>
1. <span data-ttu-id="df18b-118">Klicken Sie auf "Ausdruck bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="df18b-118">Click Edit expression.</span></span>
    * <span data-ttu-id="df18b-119">Wenn Sie die Benutzeroberfläche in der Aufgabe "Aufzeichung" in dieser Phase entsperren, können Sie IntelliSense und die Liste der Symbole verwenden, um die "Ausdruckseinschränkung" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="df18b-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="df18b-120">Geben Sie im Feld "ConstraintBody" "Implies[FrontGrill=="Metal", CornerProtection] " ein.</span><span class="sxs-lookup"><span data-stu-id="df18b-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="df18b-121">Dieser logische Ausdruck besagt: Wenn der vordere Grill aus Metall ist, muss die Option "Eckschutz" ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="df18b-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="df18b-122">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="df18b-122">Click Validate.</span></span>
    * <span data-ttu-id="df18b-123">Die Validierungsfunktion wird durch den Einschränkungsausdruck und Überprüfungen auf Syntaxfehler ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df18b-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="df18b-124">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="df18b-124">Click Close.</span></span>
5. <span data-ttu-id="df18b-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="df18b-125">Click OK.</span></span>

