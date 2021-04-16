---
title: Kuppelprodukte aus einer vorhandenen Formel kopieren
description: Diese Prozedur zeigt Ihnen an, wie Sie Co-Produkte aus einer vorhandenen Formelversion zu einer anderen Formelversion für ein freigegebenes Produkt kopieren.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cbcf2abc37441f9ff23e2b180c261831dfb79369
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829281"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="f85ba-103">Kuppelprodukte aus einer vorhandenen Formel kopieren</span><span class="sxs-lookup"><span data-stu-id="f85ba-103">Copy co-products from an existing formula version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f85ba-104">Diese Prozedur zeigt Ihnen an, wie Sie Co-Produkte aus einer vorhandenen Formelversion zu einer anderen Formelversion für ein freigegebenes Produkt kopieren.</span><span class="sxs-lookup"><span data-stu-id="f85ba-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="f85ba-105">Es ist eine Voraussetzung, dass es mindestens eine Formelversion gibt, die Co-Produkten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f85ba-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="f85ba-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USP2.</span><span class="sxs-lookup"><span data-stu-id="f85ba-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="f85ba-107">Suchen eines freigegebenen Produktes</span><span class="sxs-lookup"><span data-stu-id="f85ba-107">Find a released product</span></span>
1. <span data-ttu-id="f85ba-108">Wechseln Sie zu "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="f85ba-108">Go to Released products.</span></span>
2. <span data-ttu-id="f85ba-109">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="f85ba-109">Click Show filters.</span></span>
    * <span data-ttu-id="f85ba-110">Sie sind im Begriff, das Feld "Produktionstyp" im Filterdialogfeld hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f85ba-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="f85ba-111">Klicken Sie auf "Einen Filter hinzufügen", um das Feld "Produktionstyp" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f85ba-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="f85ba-112">Im nächsten Schritt müssen Sie manuell "Formel" im Feld "Produktionstyp" eingeben, bevor Sie "Anwenden" auswählen.</span><span class="sxs-lookup"><span data-stu-id="f85ba-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="f85ba-113">Dies legt den Filter auf der Liste der freigegebenen Produkte fest.</span><span class="sxs-lookup"><span data-stu-id="f85ba-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="f85ba-114">Geben Sie manuell "Formel" im Feld "Produktionstyp" ein.</span><span class="sxs-lookup"><span data-stu-id="f85ba-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="f85ba-115">Klicken Sie auf Übernehmen.</span><span class="sxs-lookup"><span data-stu-id="f85ba-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="f85ba-116">Wählen eines freigegebenen Produktes</span><span class="sxs-lookup"><span data-stu-id="f85ba-116">Select a released product</span></span>
1. <span data-ttu-id="f85ba-117">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f85ba-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="f85ba-118">Klicken Sie auf "Formelversionen".</span><span class="sxs-lookup"><span data-stu-id="f85ba-118">Click Formula versions.</span></span>
    * <span data-ttu-id="f85ba-119">Klicken Sie im Aktivitätsbereich "Konstruktion" auf "Formelversionen".</span><span class="sxs-lookup"><span data-stu-id="f85ba-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="f85ba-120">Kopieren von Kuppelprodukten</span><span class="sxs-lookup"><span data-stu-id="f85ba-120">Copy co-products</span></span>
1. <span data-ttu-id="f85ba-121">Klicken Sie im Aktivitätsbereich auf "Formelversionen".</span><span class="sxs-lookup"><span data-stu-id="f85ba-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="f85ba-122">Klicken Sie auf Kuppelprodukte.</span><span class="sxs-lookup"><span data-stu-id="f85ba-122">Click Co-products.</span></span>
3. <span data-ttu-id="f85ba-123">Klicken Sie auf Kopieren.</span><span class="sxs-lookup"><span data-stu-id="f85ba-123">Click Copy.</span></span>
4. <span data-ttu-id="f85ba-124">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f85ba-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="f85ba-125">Geben Sie im Feld "Formelversion" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f85ba-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="f85ba-126">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f85ba-126">Click OK.</span></span>
7. <span data-ttu-id="f85ba-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f85ba-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]