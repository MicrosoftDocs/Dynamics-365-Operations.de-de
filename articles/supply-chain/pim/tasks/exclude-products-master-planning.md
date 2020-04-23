---
title: Ein Produktlebenszyklusstatus erstellen, um Produkte vom Produktprogrammplan auszuschließen
description: In dieser Prozedur wird gezeigt, wie ein neuer Produktlebenszyklus-Status erstellt wird, bei dem Produkte vom Produktprogrammplan und der Stücklistenberechnung ausgeschlossen werden.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 999702b9a14965271b1ed350cda752e715a22a25
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203594"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="87a6e-103">Ein Produktlebenszyklusstatus erstellen, um Produkte vom Produktprogrammplan auszuschließen</span><span class="sxs-lookup"><span data-stu-id="87a6e-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="87a6e-104">In dieser Prozedur wird gezeigt, wie ein neuer Produktlebenszyklus-Status erstellt wird, bei dem Produkte vom Produktprogrammplan und der Stücklistenberechnung ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="87a6e-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="87a6e-105">Einen veralteten Status erstellen</span><span class="sxs-lookup"><span data-stu-id="87a6e-105">Create an obsolete state</span></span>
1. <span data-ttu-id="87a6e-106">Wechseln Sie zu Produktinformationsverwaltung > Einstellungen > Produktlebenszyklus-Status.</span><span class="sxs-lookup"><span data-stu-id="87a6e-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="87a6e-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="87a6e-107">Click New.</span></span>
3. <span data-ttu-id="87a6e-108">Geben Sie im Feld „Status” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="87a6e-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="87a6e-109">Wählen Sie „Nein” im Feld „Ist aktiv für Planung” aus.</span><span class="sxs-lookup"><span data-stu-id="87a6e-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="87a6e-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="87a6e-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="87a6e-111">Den veralteten Status einem freigegebenen Produkt zuordnen</span><span class="sxs-lookup"><span data-stu-id="87a6e-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="87a6e-112">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="87a6e-112">Close the page.</span></span>
2. <span data-ttu-id="87a6e-113">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="87a6e-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="87a6e-114">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="87a6e-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="87a6e-115">Filtern Sie beispielsweise im Feld „Name suchen” mit einem Wert von „M00”.</span><span class="sxs-lookup"><span data-stu-id="87a6e-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="87a6e-116">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="87a6e-116">Click Edit.</span></span>
5. <span data-ttu-id="87a6e-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="87a6e-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="87a6e-118">Geben Sie im Feld „Produktlebenszyklus-Status” einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="87a6e-118">In the Product lifecycle state field, enter or select a value.</span></span>

