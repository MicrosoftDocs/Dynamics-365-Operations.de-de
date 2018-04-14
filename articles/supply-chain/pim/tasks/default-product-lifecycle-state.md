--- 
title: "Erstellen eines standardmäßigen Produktlebenszyklus-Status"
description: "Diese Prozedur zeigt, wie ein standardmäßiger Produktlebenszyklus-Status erstellt wird und wie der standardmäßige Status den freigegebenen Produkten zugeordnet wird."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 099adbbb9cdb32e0db2daf13f83dc748b09fc61c
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="44a14-103">Erstellen eines standardmäßigen Produktlebenszyklus-Status</span><span class="sxs-lookup"><span data-stu-id="44a14-103">Create a default product lifecycle state</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="44a14-104">Diese Prozedur zeigt, wie ein standardmäßiger Produktlebenszyklus-Status erstellt wird und wie der standardmäßige Status den freigegebenen Produkten zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="44a14-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="44a14-105">Erstellen eines standardmäßigen Lebenszyklusstatus</span><span class="sxs-lookup"><span data-stu-id="44a14-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="44a14-106">Wechseln Sie zu Produktinformationsverwaltung > Einstellungen > Produktlebenszyklus-Status.</span><span class="sxs-lookup"><span data-stu-id="44a14-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="44a14-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="44a14-107">Click New.</span></span>
3. <span data-ttu-id="44a14-108">Geben Sie im Feld „Status” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44a14-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="44a14-109">Wählen Sie „Ja” im Feld „Standard, wenn für juristische Person freigegeben” aus.</span><span class="sxs-lookup"><span data-stu-id="44a14-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="44a14-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44a14-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="44a14-111">Wählen Sie „Nein” im Feld „Ist aktiv für Planung” aus.</span><span class="sxs-lookup"><span data-stu-id="44a14-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="44a14-112">Wenn ein neues freigegebenes Produkt nicht in den Produktprogrammplan einbezogen werden soll, wählen Sie „Nein” aus.</span><span class="sxs-lookup"><span data-stu-id="44a14-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="44a14-113">Wenn es in den Produktprogrammplan einbezogen werden soll, belassen Sie das Steuerelement beim Standardwert „Ja”.</span><span class="sxs-lookup"><span data-stu-id="44a14-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="44a14-114">Neues freigegebenes Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="44a14-114">Create a new released product</span></span>
1. <span data-ttu-id="44a14-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="44a14-115">Close the page.</span></span>
2. <span data-ttu-id="44a14-116">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="44a14-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="44a14-117">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="44a14-117">Click New.</span></span>
4. <span data-ttu-id="44a14-118">Geben Sie im Feld "Produktnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44a14-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="44a14-119">Geben Sie im Feld "Produktname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44a14-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="44a14-120">Geben Sie im Feld „Suchname” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44a14-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="44a14-121">Geben Sie im Feld "Artikelmodellgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="44a14-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="44a14-122">Geben Sie im Feld "Artikelgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="44a14-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="44a14-123">Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="44a14-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="44a14-124">Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="44a14-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="44a14-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="44a14-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="44a14-126">Der standardmäßige Produktlebenszyklus-Status ist eine globale Definition.</span><span class="sxs-lookup"><span data-stu-id="44a14-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="44a14-127">Produkt zu aktivem Status ändern</span><span class="sxs-lookup"><span data-stu-id="44a14-127">Change the product to an active state</span></span>
1. <span data-ttu-id="44a14-128">Geben Sie im Feld „Produktlebenszyklus-Status” einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="44a14-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="44a14-129">Angenommen, Sie haben einen aktiven Status eingerichtet, dann können Sie jetzt den aktiven Status auswählen, um zuzulassen, dass das Produkt im Produktprogrammplan und der Stücklistenberechnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44a14-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="44a14-130">Offensichtlich ist dies nur sinnvoll, wenn alle Produktdetails, die für eine konsistente Planung erforderlich sind, angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="44a14-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  


