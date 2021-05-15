---
title: Einem Produktkonfigurationsmodell eine Ausdruckseinschränkung hinzufügen
description: Im folgenden Verfahren sehen Sie, wie Sie einen neuen Einschränkungsausdruck einem Produktkonfigurationsmodell hinzufügen können.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920880"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="b8471-103">Einem Produktkonfigurationsmodell eine Ausdruckseinschränkung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="b8471-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8471-104">Im folgenden Verfahren sehen Sie, wie Sie einen neuen Einschränkungsausdruck einem Produktkonfigurationsmodell hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="b8471-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="b8471-105">Es zeigt, wie Sie vorgeben, dass der "Eckschutz" an einem Lautsprecher angebracht werden muss, wenn der Benutzer einen vorderen Metallgrill ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="b8471-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="b8471-106">Das Verfahren verwendet die Komponente "High end speaker" im Vorführungsunternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="b8471-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="b8471-107">Erstellen einer Ausdruckseinschränkung</span><span class="sxs-lookup"><span data-stu-id="b8471-107">Create an expression constraint</span></span>

1. <span data-ttu-id="b8471-108">Wechseln Sie zu **Produktinformationsmanagement \> Produkte \> Produktkonfigurationsmodelle**.</span><span class="sxs-lookup"><span data-stu-id="b8471-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="b8471-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b8471-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b8471-110">Diese Beispiel verwendet das Spitzenlautsprechermodell.</span><span class="sxs-lookup"><span data-stu-id="b8471-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="b8471-111">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b8471-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="b8471-112">Erweitern Sie den Abschnitt **Einschränkungen**.</span><span class="sxs-lookup"><span data-stu-id="b8471-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="b8471-113">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="b8471-113">Select **Add**.</span></span>
7. <span data-ttu-id="b8471-114">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="b8471-114">Select **Create**.</span></span>
8. <span data-ttu-id="b8471-115">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b8471-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="b8471-116">Ausdruck eingeben</span><span class="sxs-lookup"><span data-stu-id="b8471-116">Enter expression</span></span>

1. <span data-ttu-id="b8471-117">Wählen Sie **Ausdruck bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="b8471-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="b8471-118">Wenn Sie die Benutzeroberfläche in der Aufgabe "Aufzeichung" in dieser Phase entsperren, können Sie IntelliSense und die Liste der Symbole verwenden, um die "Ausdruckseinschränkung" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8471-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="b8471-119">Geben Sie im Feld **ConstraintBody** 'Implies[FrontGrill=="Metal", CornerProtection] ' ein.</span><span class="sxs-lookup"><span data-stu-id="b8471-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="b8471-120">Dieser logische Ausdruck besagt: Wenn der vordere Grill aus Metall ist, muss die Option "Eckschutz" ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="b8471-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="b8471-121">Wählen Sie **Überprüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="b8471-121">Select **Validate**.</span></span>
    * <span data-ttu-id="b8471-122">Die Validierungsfunktion wird durch den Einschränkungsausdruck und Überprüfungen auf Syntaxfehler ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8471-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="b8471-123">Wählen Sie **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="b8471-123">Select **Close**.</span></span>
5. <span data-ttu-id="b8471-124">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8471-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]