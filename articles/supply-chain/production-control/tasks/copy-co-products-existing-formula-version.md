---
title: Kuppelprodukte aus einer vorhandenen Formel kopieren
description: Diese Prozedur zeigt Ihnen an, wie Sie Co-Produkte aus einer vorhandenen Formelversion zu einer anderen Formelversion für ein freigegebenes Produkt kopieren.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 626c0fc8a60eeb84060d7279833de583d55a95a2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838750"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="aa2d6-103">Kuppelprodukte aus einer vorhandenen Formel kopieren</span><span class="sxs-lookup"><span data-stu-id="aa2d6-103">Copy co-products from an existing formula version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa2d6-104">Diese Prozedur zeigt Ihnen an, wie Sie Co-Produkte aus einer vorhandenen Formelversion zu einer anderen Formelversion für ein freigegebenes Produkt kopieren.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="aa2d6-105">Es ist eine Voraussetzung, dass es mindestens eine Formelversion gibt, die Co-Produkten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="aa2d6-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USP2.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="aa2d6-107">Suchen eines freigegebenen Produktes</span><span class="sxs-lookup"><span data-stu-id="aa2d6-107">Find a released product</span></span>
1. <span data-ttu-id="aa2d6-108">Wechseln Sie zu "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="aa2d6-108">Go to Released products.</span></span>
2. <span data-ttu-id="aa2d6-109">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="aa2d6-109">Click Show filters.</span></span>
    * <span data-ttu-id="aa2d6-110">Sie sind im Begriff, das Feld "Produktionstyp" im Filterdialogfeld hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="aa2d6-111">Klicken Sie auf "Einen Filter hinzufügen", um das Feld "Produktionstyp" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="aa2d6-112">Im nächsten Schritt müssen Sie manuell "Formel" im Feld "Produktionstyp" eingeben, bevor Sie "Anwenden" auswählen.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="aa2d6-113">Dies legt den Filter auf der Liste der freigegebenen Produkte fest.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="aa2d6-114">Geben Sie manuell "Formel" im Feld "Produktionstyp" ein.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="aa2d6-115">Klicken Sie auf Übernehmen.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="aa2d6-116">Wählen eines freigegebenen Produktes</span><span class="sxs-lookup"><span data-stu-id="aa2d6-116">Select a released product</span></span>
1. <span data-ttu-id="aa2d6-117">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="aa2d6-118">Klicken Sie auf "Formelversionen".</span><span class="sxs-lookup"><span data-stu-id="aa2d6-118">Click Formula versions.</span></span>
    * <span data-ttu-id="aa2d6-119">Klicken Sie im Aktivitätsbereich "Konstruktion" auf "Formelversionen".</span><span class="sxs-lookup"><span data-stu-id="aa2d6-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="aa2d6-120">Kopieren von Kuppelprodukten</span><span class="sxs-lookup"><span data-stu-id="aa2d6-120">Copy co-products</span></span>
1. <span data-ttu-id="aa2d6-121">Klicken Sie im Aktivitätsbereich auf "Formelversionen".</span><span class="sxs-lookup"><span data-stu-id="aa2d6-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="aa2d6-122">Klicken Sie auf Kuppelprodukte.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-122">Click Co-products.</span></span>
3. <span data-ttu-id="aa2d6-123">Klicken Sie auf Kopieren.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-123">Click Copy.</span></span>
4. <span data-ttu-id="aa2d6-124">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="aa2d6-125">Geben Sie im Feld "Formelversion" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="aa2d6-126">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="aa2d6-126">Click OK.</span></span>
7. <span data-ttu-id="aa2d6-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="aa2d6-127">Close the page.</span></span>

