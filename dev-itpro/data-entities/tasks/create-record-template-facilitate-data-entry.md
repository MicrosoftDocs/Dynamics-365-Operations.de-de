--- 
title: Eine Datensatzvorlage erstellen, um die Dateneingabe zu erleichtern
description: "Diese Prozedur zeigt, wie eine Datensatzvorlge erstellt wird, sodass Feldwerte, die oft verwendet werden, nicht explizit für jeden neuen Datensatz eingegeben werden müssen."
author: sericks007
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6f8d804133f8e9c6f47420d41df8d9430381e2fe
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="f7b29-103">Eine Datensatzvorlage erstellen, um die Dateneingabe zu erleichtern</span><span class="sxs-lookup"><span data-stu-id="f7b29-103">Create a record template to facilitate data entry</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7b29-104">Diese Prozedur zeigt, wie eine Datensatzvorlge erstellt wird, sodass Feldwerte, die oft verwendet werden, nicht explizit für jeden neuen Datensatz eingegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f7b29-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="f7b29-105">In dieser Prozedur erstellen Sie einen neuen Datensatz für neuen Laptops, die den Anlagen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7b29-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="f7b29-106">Für diese Prozedur wird das Beispielunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7b29-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="f7b29-107">Wechseln Sie zu Anlagen > Anlagen > Anlagen.</span><span class="sxs-lookup"><span data-stu-id="f7b29-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="f7b29-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f7b29-108">Click New.</span></span>
3. <span data-ttu-id="f7b29-109">Geben Sie im Feld "Anlagengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f7b29-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="f7b29-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f7b29-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f7b29-111">Geben Sie zum Beispiel „Laptop des potenziellen Firmenkunden” ein.</span><span class="sxs-lookup"><span data-stu-id="f7b29-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="f7b29-112">Geben Sie im Feld „Suchname” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f7b29-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="f7b29-113">Geben Sie beispielsweise „Laptop” ein.</span><span class="sxs-lookup"><span data-stu-id="f7b29-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="f7b29-114">Erweitern Sie den Abschnitt „Technische Informationen”.</span><span class="sxs-lookup"><span data-stu-id="f7b29-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="f7b29-115">Geben Sie im Feld „Marke” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f7b29-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="f7b29-116">Geben Sie im Feld „Modell” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f7b29-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="f7b29-117">Geben Sie im Feld „Modelljahr” einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f7b29-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="f7b29-118">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="f7b29-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="f7b29-119">Klicken Sie auf „Datensatzinfo”.</span><span class="sxs-lookup"><span data-stu-id="f7b29-119">Click Record info.</span></span>
12. <span data-ttu-id="f7b29-120">Klicken Sie auf „Benutzervorlage”.</span><span class="sxs-lookup"><span data-stu-id="f7b29-120">Click User template.</span></span>
13. <span data-ttu-id="f7b29-121">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f7b29-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f7b29-122">Geben Sie zum Beispiel „Firmenlaptop” ein.</span><span class="sxs-lookup"><span data-stu-id="f7b29-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="f7b29-123">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f7b29-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="f7b29-124">Geben Sie zum Beispiel „Firmenlaptop” ein.</span><span class="sxs-lookup"><span data-stu-id="f7b29-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="f7b29-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f7b29-125">Click OK.</span></span>
16. <span data-ttu-id="f7b29-126">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="f7b29-126">Click Close.</span></span>


