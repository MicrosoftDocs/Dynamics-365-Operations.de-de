--- 
title: Kostenelemente erstellen
description: "Es gibt mehrere Möglichkeiten, Kostenfaktoren in der Kostenrechnung zu erstellen."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1e665fc53455e457a2488f4ec28ebb5b715d90eb
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-cost-elements"></a><span data-ttu-id="708e4-103">Kostenelemente erstellen</span><span class="sxs-lookup"><span data-stu-id="708e4-103">Create cost elements</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="708e4-104">Es gibt mehrere Möglichkeiten, Kostenfaktoren in der Kostenrechnung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="708e4-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="708e4-105">Dieses Verfahren zeigt, wie Kostenfaktoren erstellt werden, indem Hauptkonten über einen Datenkonnektor importiert werden.</span><span class="sxs-lookup"><span data-stu-id="708e4-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="708e4-106">Das USMF-Demodatenunternehmen wurde verwendet, um diese Prozedur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="708e4-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="708e4-107">Diese Prozedur ist für eine Kostenbuchhaltungs-Funktion, die in Microsoft Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="708e4-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="708e4-108">Klicken Sie auf "Neue Kostenelemente erstellen".</span><span class="sxs-lookup"><span data-stu-id="708e4-108">Create new cost elements</span></span>
1. <span data-ttu-id="708e4-109">Wechseln Sie zu den Kostenrechnung > Dimensionen > Kostenelementdimensionen.</span><span class="sxs-lookup"><span data-stu-id="708e4-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="708e4-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="708e4-110">Click New.</span></span>
3. <span data-ttu-id="708e4-111">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="708e4-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="708e4-112">Geben Sie im Feld "Datenkonnektor für Dimensionsmitglieder" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="708e4-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="708e4-113">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="708e4-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="708e4-114">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="708e4-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="708e4-115">Den Datenkonnektor konfigurieren</span><span class="sxs-lookup"><span data-stu-id="708e4-115">Configure the data connector</span></span>
1. <span data-ttu-id="708e4-116">Klicken Sie auf "Dimensionselementanbieter konfigurieren".</span><span class="sxs-lookup"><span data-stu-id="708e4-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="708e4-117">Geben Sie im Feld "Kontenplan" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="708e4-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="708e4-118">Wählen Sie "Gemeinsam", um den freigegebenen Kontenplan zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="708e4-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="708e4-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="708e4-119">Click New.</span></span>
4. <span data-ttu-id="708e4-120">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="708e4-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="708e4-121">Sie können Filter auf Konten anwenden, um die Kriterien zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="708e4-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="708e4-122">Geben Sie im Feld "Aus Hauptkonto" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="708e4-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="708e4-123">Geben Sie im Feld 'An Hauptkonto' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="708e4-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="708e4-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="708e4-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="708e4-125">Hauptkonten importieren</span><span class="sxs-lookup"><span data-stu-id="708e4-125">Import main accounts</span></span>
1. <span data-ttu-id="708e4-126">Klicken Sie auf "Dimensionsmitglieder importieren".</span><span class="sxs-lookup"><span data-stu-id="708e4-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="708e4-127">Hauptkonten werden in die Kostenrechnung importiert und als Kostenfaktoren verwendet.</span><span class="sxs-lookup"><span data-stu-id="708e4-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="708e4-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="708e4-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="708e4-129">Anzeigen der importierten Konten als an Kostenfaktoren</span><span class="sxs-lookup"><span data-stu-id="708e4-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="708e4-130">Klicken Sie auf "Dimensionsmitglieder anzeigen".</span><span class="sxs-lookup"><span data-stu-id="708e4-130">Click View dimension members.</span></span>
    * <span data-ttu-id="708e4-131">Zeigen Sie die importierten Sachkonten als Kostenfaktoren in Ihrem Unternehmen an, in dass Kosten fließen können.</span><span class="sxs-lookup"><span data-stu-id="708e4-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  


