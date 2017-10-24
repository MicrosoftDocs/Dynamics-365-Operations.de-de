--- 
title: Einrichten der vorzeitigen Abschreibung
description: Die folgende Prozedur zeigt, wie ein Sonderabschreibungsbetrag erstellt wird und es einem Anlagenbuch zuordnet wird.
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7e6ebb13084626b477b6e0b24acdc09e2c0d3d6d
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="83147-103">Einrichten der vorzeitigen Abschreibung</span><span class="sxs-lookup"><span data-stu-id="83147-103">Set up bonus depreciation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="83147-104">Die folgende Prozedur zeigt, wie ein Sonderabschreibungsbetrag erstellt wird und es einem Anlagenbuch zuordnet wird.</span><span class="sxs-lookup"><span data-stu-id="83147-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="83147-105">Dabei werden die Buchhalterrolle und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="83147-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="83147-106">Eine Sonderabschreibung erstellen</span><span class="sxs-lookup"><span data-stu-id="83147-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="83147-107">Wechseln Sie zu "Anlagen" > "Einstellungen" > "Sonderabschreibung".</span><span class="sxs-lookup"><span data-stu-id="83147-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="83147-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="83147-108">Click New.</span></span>
3. <span data-ttu-id="83147-109">Geben Sie im Feld "Sonderabschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="83147-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="83147-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="83147-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="83147-111">Geben Sie im Feld "Prozentsatz" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="83147-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="83147-112">Wen ein Betrag nicht festgelegt ist, legen Sie einen Betrag fest.</span><span class="sxs-lookup"><span data-stu-id="83147-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="83147-113">Eine Sonderabschreibung einem Anlagengruppenbuch zuordnen</span><span class="sxs-lookup"><span data-stu-id="83147-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="83147-114">Wechseln Sie zu Anlagen > Einstellungen > Anlagengruppen.</span><span class="sxs-lookup"><span data-stu-id="83147-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="83147-115">Wählen Sie in der Liste die Anlagengruppe aus, die der Sonderabschreibung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="83147-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="83147-116">Klicken Sie auf Bücher.</span><span class="sxs-lookup"><span data-stu-id="83147-116">Click Books.</span></span>
4. <span data-ttu-id="83147-117">Wählen Sie in der Liste das Buch aus, die der Sonderabschreibung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="83147-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="83147-118">Klicken Sie auf "Sonderabschreibung".</span><span class="sxs-lookup"><span data-stu-id="83147-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="83147-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="83147-119">Click New.</span></span>
7. <span data-ttu-id="83147-120">Geben Sie im Feld "Sonderabschreibung" einen Wert ein oder wählen Sie einen aus.</span><span class="sxs-lookup"><span data-stu-id="83147-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="83147-121">Der Prozentsatz oder Betrag wird standardmäßig aus der Sonderabschreibungseinstellung übernommen.</span><span class="sxs-lookup"><span data-stu-id="83147-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="83147-122">Geben Sie im Feld "Priorität" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="83147-122">In the Priority field, enter a number.</span></span>


