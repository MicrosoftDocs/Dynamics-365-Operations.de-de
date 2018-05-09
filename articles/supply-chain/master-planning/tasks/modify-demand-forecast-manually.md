--- 
title: "Eine Bedarfsplanung manuell ändern"
description: "Im folgenden Verfahren wird gezeigt, wie Sie die Planung für einen Artikel ändern."
author: YuyuScheller
manager: AnnBe
ms.date: 11/15/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e655a5ffa44aa06200aabc8c00ee477aaf286290
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="25d7d-103">Eine Bedarfsplanung manuell ändern</span><span class="sxs-lookup"><span data-stu-id="25d7d-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25d7d-104">Im folgenden Verfahren wird gezeigt, wie Sie die Planung für einen Artikel ändern.</span><span class="sxs-lookup"><span data-stu-id="25d7d-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="25d7d-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="25d7d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="25d7d-106">Diese Aufzeichnung ist für den Produktionsplaner vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="25d7d-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="25d7d-107">Ändern der Planung für einen Artikel</span><span class="sxs-lookup"><span data-stu-id="25d7d-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="25d7d-108">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="25d7d-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="25d7d-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="25d7d-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="25d7d-110">Wählen Sie den Artikel aus, für den Sie die Planung ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="25d7d-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="25d7d-111">Sie können beispielsweise Artikel "D0001" auswählen.</span><span class="sxs-lookup"><span data-stu-id="25d7d-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="25d7d-112">Klicken Sie im Aktivitätsbereich auf "Plan".</span><span class="sxs-lookup"><span data-stu-id="25d7d-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="25d7d-113">Klicken Sie auf "Bedarfsplanung".</span><span class="sxs-lookup"><span data-stu-id="25d7d-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="25d7d-114">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="25d7d-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="25d7d-115">Wenn keine Planungspositionen vorhanden sind, erstellen Sie eine neue Position nach  .</span><span class="sxs-lookup"><span data-stu-id="25d7d-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="25d7d-116">Klicken Sie neu auf der App-Leiste.</span><span class="sxs-lookup"><span data-stu-id="25d7d-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="25d7d-117">Geben Sie im Feld "Verkaufsmenge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="25d7d-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="25d7d-118">Diese Zahl gibt die prognostizierte Menge des Artikels wieder.</span><span class="sxs-lookup"><span data-stu-id="25d7d-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="25d7d-119">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="25d7d-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="25d7d-120">Ändern der Planung in Excel</span><span class="sxs-lookup"><span data-stu-id="25d7d-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="25d7d-121">Klicken Sie auf "In Microsoft Office öffnen".</span><span class="sxs-lookup"><span data-stu-id="25d7d-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="25d7d-122">Klicken Sie auf "Bedarfsplanung in Excel anpassen".</span><span class="sxs-lookup"><span data-stu-id="25d7d-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="25d7d-123">In Excel können Sie Bedarfsplanungspositionen hinzufügen, löschen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="25d7d-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="25d7d-124">Wenn die Daten in Excel nicht angezeigt werden können, müssen Sie sich mit aktivierter Option "Angemeldet bleiben" in Microsoft Dynamics 365 for Finance and Operations Enterprise Edition anmelden und der Datenverbindungs-App vertrauen.</span><span class="sxs-lookup"><span data-stu-id="25d7d-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  


