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
ms.openlocfilehash: 7a2fd383944a96a073f12399e1a29d0fcf520e3c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812642"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="32761-103">Einem Produktkonfigurationsmodell eine Ausdruckseinschränkung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="32761-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="32761-104">Im folgenden Verfahren sehen Sie, wie Sie einen neuen Einschränkungsausdruck einem Produktkonfigurationsmodell hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="32761-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="32761-105">Es zeigt, wie Sie vorgeben, dass der "Eckschutz" an einem Lautsprecher angebracht werden muss, wenn der Benutzer einen vorderen Metallgrill ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="32761-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="32761-106">Das Verfahren verwendet die Komponente "High end speaker" im Vorführungsunternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="32761-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="32761-107">Erstellen einer Ausdruckseinschränkung</span><span class="sxs-lookup"><span data-stu-id="32761-107">Create an expression constraint</span></span>
1. <span data-ttu-id="32761-108">Klicken Sie auf "Produktvariantenmodell-Definition".</span><span class="sxs-lookup"><span data-stu-id="32761-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="32761-109">Klicken Sie auf "Produktkonfigurationsmodelle".</span><span class="sxs-lookup"><span data-stu-id="32761-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="32761-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="32761-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="32761-111">Diese Beispiel verwendet das Spitzenlautsprechermodell.</span><span class="sxs-lookup"><span data-stu-id="32761-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="32761-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="32761-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="32761-113">Erweitern Sie den Abschnitt "Einschränkungen".</span><span class="sxs-lookup"><span data-stu-id="32761-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="32761-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="32761-114">Click Add.</span></span>
7. <span data-ttu-id="32761-115">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="32761-115">Click Create.</span></span>
8. <span data-ttu-id="32761-116">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="32761-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="32761-117">Ausdruck eingeben</span><span class="sxs-lookup"><span data-stu-id="32761-117">Enter expression</span></span>
1. <span data-ttu-id="32761-118">Klicken Sie auf "Ausdruck bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="32761-118">Click Edit expression.</span></span>
    * <span data-ttu-id="32761-119">Wenn Sie die Benutzeroberfläche in der Aufgabe "Aufzeichung" in dieser Phase entsperren, können Sie IntelliSense und die Liste der Symbole verwenden, um die "Ausdruckseinschränkung" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="32761-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="32761-120">Geben Sie im Feld "ConstraintBody" "Implies[FrontGrill=="Metal", CornerProtection] " ein.</span><span class="sxs-lookup"><span data-stu-id="32761-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="32761-121">Dieser logische Ausdruck besagt: Wenn der vordere Grill aus Metall ist, muss die Option "Eckschutz" ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="32761-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="32761-122">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="32761-122">Click Validate.</span></span>
    * <span data-ttu-id="32761-123">Die Validierungsfunktion wird durch den Einschränkungsausdruck und Überprüfungen auf Syntaxfehler ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32761-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="32761-124">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="32761-124">Click Close.</span></span>
5. <span data-ttu-id="32761-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="32761-125">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]