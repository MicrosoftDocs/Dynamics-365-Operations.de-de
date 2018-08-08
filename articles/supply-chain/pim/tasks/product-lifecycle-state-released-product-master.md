--- 
title: Ein Produktlebensyklusstatus einem freigegebenen Produktmaster zuweisen
description: Diese Prozedur zeigt, wie ein Produktlebenszyklus-Status einem freigegebenen Produktmaster und seinen Varianten zugewiesen wird.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: dd9d40bb331b9e024617c8be55330dfce8ba1cc6
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="8ce04-103">Ein Produktlebensyklusstatus einem freigegebenen Produktmaster zuweisen</span><span class="sxs-lookup"><span data-stu-id="8ce04-103">Assign a product lifecycle state to a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ce04-104">Diese Prozedur zeigt, wie ein Produktlebenszyklus-Status einem freigegebenen Produktmaster und seinen Varianten zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8ce04-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="8ce04-105">Voraussetzung: Sie müssen zuerst den Aufgabenleitfaden wiedergeben „Einen neuen Produktlebenszyklus-Status erstellen”, um sicherzustellen, dass mindestens ein Produktlebenszyklus-Status erstellt wird, bevor Sie diesen Aufgabenleitfaden wiedergeben können.</span><span class="sxs-lookup"><span data-stu-id="8ce04-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="8ce04-106">Einen freigegebenen Produktmaster suchen</span><span class="sxs-lookup"><span data-stu-id="8ce04-106">Find a released product master</span></span>
1. <span data-ttu-id="8ce04-107">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="8ce04-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="8ce04-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8ce04-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="8ce04-109">Ein Produktmaster hat den Produktuntertyp-Produktmaster.</span><span class="sxs-lookup"><span data-stu-id="8ce04-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="8ce04-110">Den Lebenszyklusstatus aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8ce04-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="8ce04-111">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8ce04-111">Click Edit.</span></span>
2. <span data-ttu-id="8ce04-112">Geben Sie im Feld „Produktlebenszyklus-Status” einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8ce04-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="8ce04-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8ce04-113">Click Save.</span></span>
4. <span data-ttu-id="8ce04-114">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="8ce04-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="8ce04-115">Wenn „Ja” ausgewählt ist, werden alle zugeordneten freigegebenen Produktvarianten, die denselben ursprünglichen Status wie der freigegebene Produktmaster haben, ebenfalls auf den neuen Produktlebenszyklus-Status aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8ce04-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="8ce04-116">Wenn „Nein” ausgewählt ist, behalten alle Varianten ihren tatsächlichen Status.</span><span class="sxs-lookup"><span data-stu-id="8ce04-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="8ce04-117">Varianten, die einen anderen Produktlebenszyklus-Status als der freigegebene Produktmaster haben, werden nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8ce04-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="8ce04-118">Den Lebenszyklusstatus der Varianten überprüfen</span><span class="sxs-lookup"><span data-stu-id="8ce04-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="8ce04-119">Klicken Sie auf Varianten für freigegebenes Produkt.</span><span class="sxs-lookup"><span data-stu-id="8ce04-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="8ce04-120">Beachten Sie, dass alle Varianten den ausgewählten Lebenszyklusstatus vom freigegebenen Produktmaster geerbt haben.</span><span class="sxs-lookup"><span data-stu-id="8ce04-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="8ce04-121">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="8ce04-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="8ce04-122">Geben Sie im Feld „Produktlebenszyklus-Status” einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8ce04-122">In the Product lifecycle state field, enter or select a value.</span></span>


