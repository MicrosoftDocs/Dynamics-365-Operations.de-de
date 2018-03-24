--- 
title: "Ein Produktlebenszyklusstatus erstellen, um Produkte vom Produktprogrammplan auszuschließen"
description: "In dieser Prozedur wird gezeigt, wie ein neuer Produktlebenszyklus-Status erstellt wird, bei dem Produkte vom Produktprogrammplan und der Stücklistenberechnung ausgeschlossen werden."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 1685e8eb706e29ef5b195e9163bf19345fee78b6
ms.contentlocale: de-de
ms.lasthandoff: 02/07/2018

---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="c6e13-103">Ein Produktlebenszyklusstatus erstellen, um Produkte vom Produktprogrammplan auszuschließen</span><span class="sxs-lookup"><span data-stu-id="c6e13-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6e13-104">In dieser Prozedur wird gezeigt, wie ein neuer Produktlebenszyklus-Status erstellt wird, bei dem Produkte vom Produktprogrammplan und der Stücklistenberechnung ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="c6e13-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="c6e13-105">Einen veralteten Status erstellen</span><span class="sxs-lookup"><span data-stu-id="c6e13-105">Create an obsolete state</span></span>
1. <span data-ttu-id="c6e13-106">Wechseln Sie zu Produktinformationsverwaltung > Einstellungen > Produktlebenszyklus-Status.</span><span class="sxs-lookup"><span data-stu-id="c6e13-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="c6e13-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c6e13-107">Click New.</span></span>
3. <span data-ttu-id="c6e13-108">Geben Sie im Feld „Status” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c6e13-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="c6e13-109">Wählen Sie „Nein” im Feld „Ist aktiv für Planung” aus.</span><span class="sxs-lookup"><span data-stu-id="c6e13-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="c6e13-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c6e13-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="c6e13-111">Den veralteten Status einem freigegebenen Produkt zuordnen</span><span class="sxs-lookup"><span data-stu-id="c6e13-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="c6e13-112">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c6e13-112">Close the page.</span></span>
2. <span data-ttu-id="c6e13-113">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="c6e13-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="c6e13-114">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c6e13-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c6e13-115">Filtern Sie beispielsweise im Feld „Name suchen” mit einem Wert von „M00”.</span><span class="sxs-lookup"><span data-stu-id="c6e13-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="c6e13-116">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="c6e13-116">Click Edit.</span></span>
5. <span data-ttu-id="c6e13-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c6e13-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="c6e13-118">Geben Sie im Feld „Produktlebenszyklus-Status” einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c6e13-118">In the Product lifecycle state field, enter or select a value.</span></span>

