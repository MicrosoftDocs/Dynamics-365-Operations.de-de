---
title: Ersatz-Kanban-Regel erstellen
description: Diese Prozedur konzentriert sich auf das Ersetzen einer vorhandenen Kanban-Regel durch eine neue Kanban-Regel an einem bestimmten Datum.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: de048577ac372474b72728d7774e3159a159afc9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221822"
---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="894bd-103">Ersatz-Kanban-Regel erstellen</span><span class="sxs-lookup"><span data-stu-id="894bd-103">Create a replacement kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="894bd-104">Diese Prozedur konzentriert sich auf das Ersetzen einer vorhandenen Kanban-Regel durch eine neue Kanban-Regel an einem bestimmten Datum.</span><span class="sxs-lookup"><span data-stu-id="894bd-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="894bd-105">Dies ist hilfreich, wenn Änderungen im Produktionsfluss oder bei den Auffüllungsregeln koordiniert und geplant werden müssen.</span><span class="sxs-lookup"><span data-stu-id="894bd-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="894bd-106">Das Demodatenunternehmen in der Prozedur ist USMF.</span><span class="sxs-lookup"><span data-stu-id="894bd-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="894bd-107">Diese Prozedur ist für den Fertigungsplaner oder den Wertstrommanager vorgesehen, wenn dieser die Produktion für einen geänderten Produktionsfluss oder eine neue Auffüllungsregel vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="894bd-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="894bd-108">Diese Aufgabe ersetzt Kanban-Regel 000022 durch eine neue Regel und erhöht die Höchstmenge von 48 auf 100 für die neue Regel.</span><span class="sxs-lookup"><span data-stu-id="894bd-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="894bd-109">Wählen Sie eine Kanban-Regel aus, die ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="894bd-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="894bd-110">Wechseln Sie zu Kanban-Regeln.</span><span class="sxs-lookup"><span data-stu-id="894bd-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="894bd-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="894bd-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="894bd-112">Wählen Sie Kanban-Regel "000022" aus.</span><span class="sxs-lookup"><span data-stu-id="894bd-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="894bd-113">Ersatz-Kanban-Regel erstellen</span><span class="sxs-lookup"><span data-stu-id="894bd-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="894bd-114">Klicken Sie auf "Kanban-Regel ersetzen".</span><span class="sxs-lookup"><span data-stu-id="894bd-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="894bd-115">Geben Sie im Feld "Gültigkeitsdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="894bd-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="894bd-116">Wählen Sie ein Datum in der Zukunft aus, wie in einer Woche ab jetzt.</span><span class="sxs-lookup"><span data-stu-id="894bd-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="894bd-117">Dies ist das Datum und die Uhrzeit, zu der die neue Kanban-Regel aktiv wird und die alte Kanban-Regel ersetzt.</span><span class="sxs-lookup"><span data-stu-id="894bd-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="894bd-118">Wenn die Kanban-Regel den Pfad des Produktionsflusses ändert, kann eine andere Aktivität ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="894bd-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="894bd-119">In dieser Prozedur halten wir die Aktivität nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="894bd-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="894bd-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="894bd-120">Click OK.</span></span>
    * <span data-ttu-id="894bd-121">Beachten Sie, dass eine neue Kanban-Regel erstellt wird, um Kanban-Regel 000022 zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="894bd-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="894bd-122">Das Gültigkeitsdatum wird gemäß dem ausgewählten Datum festgelegt, wenn Sie die Kanban-Regel ersetzen.</span><span class="sxs-lookup"><span data-stu-id="894bd-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="894bd-123">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="894bd-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="894bd-124">Wählen Sie die ersetzte Kanban-Regel "000022" aus.</span><span class="sxs-lookup"><span data-stu-id="894bd-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="894bd-125">Beachten Sie, dass die ersetzte Kanban-Regel dasselbe Datum wie das "Ablaufdatum" hat, da dies das Datum ist, an dem sie abläuft.</span><span class="sxs-lookup"><span data-stu-id="894bd-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="894bd-126">Wählen Sie in der Liste die Zeile "1" aus.</span><span class="sxs-lookup"><span data-stu-id="894bd-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="894bd-127">Wählen Sie die neue Kanban-Regel über der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="894bd-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="894bd-128">Dies ist die Kanban-Regel mit der höchsten Kanban-Regel-Nummer.</span><span class="sxs-lookup"><span data-stu-id="894bd-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="894bd-129">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="894bd-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="894bd-130">Klicken Sie auf die Kanban-Regel-Nummer, um die Kanban-Regel zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="894bd-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="894bd-131">Ändern Sie "Höchstmenge" für die Ersatz-Kanban-Regel</span><span class="sxs-lookup"><span data-stu-id="894bd-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="894bd-132">Legen Sie "Höchstmenge" auf "100" fest.</span><span class="sxs-lookup"><span data-stu-id="894bd-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="894bd-133">Erweitern Sie das Inforegister "Mengen", um das Feld "Höchstmenge" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="894bd-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="894bd-134">Das Ändern der Höchstmenge auf 100 ermöglicht es, dass bis zu 100 Kanbans verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="894bd-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="894bd-135">Dies ist der letzte Schritt in dieser Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="894bd-135">This is the last step in this task.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]