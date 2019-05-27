---
title: Eine Bedarfsplanung manuell ändern
description: Im folgenden Verfahren wird gezeigt, wie Sie die Planung für einen Artikel ändern.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 063554c98b8a6261ebe69073f214a8e45850c623
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560735"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="490ca-103">Eine Bedarfsplanung manuell ändern</span><span class="sxs-lookup"><span data-stu-id="490ca-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="490ca-104">Im folgenden Verfahren wird gezeigt, wie Sie die Planung für einen Artikel ändern.</span><span class="sxs-lookup"><span data-stu-id="490ca-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="490ca-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="490ca-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="490ca-106">Diese Aufzeichnung ist für den Produktionsplaner vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="490ca-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="490ca-107">Ändern der Planung für einen Artikel</span><span class="sxs-lookup"><span data-stu-id="490ca-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="490ca-108">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="490ca-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="490ca-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="490ca-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="490ca-110">Wählen Sie den Artikel aus, für den Sie die Planung ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="490ca-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="490ca-111">Sie können beispielsweise Artikel "D0001" auswählen.</span><span class="sxs-lookup"><span data-stu-id="490ca-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="490ca-112">Klicken Sie im Aktivitätsbereich auf "Plan".</span><span class="sxs-lookup"><span data-stu-id="490ca-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="490ca-113">Klicken Sie auf "Bedarfsplanung".</span><span class="sxs-lookup"><span data-stu-id="490ca-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="490ca-114">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="490ca-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="490ca-115">Wenn keine Planungspositionen vorhanden sind, erstellen Sie eine neue Position nach  .</span><span class="sxs-lookup"><span data-stu-id="490ca-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="490ca-116">Klicken Sie neu auf der App-Leiste.</span><span class="sxs-lookup"><span data-stu-id="490ca-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="490ca-117">Geben Sie im Feld "Verkaufsmenge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="490ca-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="490ca-118">Diese Zahl gibt die prognostizierte Menge des Artikels wieder.</span><span class="sxs-lookup"><span data-stu-id="490ca-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="490ca-119">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="490ca-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="490ca-120">Ändern der Planung in Excel</span><span class="sxs-lookup"><span data-stu-id="490ca-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="490ca-121">Klicken Sie in Microsoft Office auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="490ca-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="490ca-122">Klicken Sie auf "Bedarfsplanung in Excel anpassen".</span><span class="sxs-lookup"><span data-stu-id="490ca-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="490ca-123">In Excel können Sie Bedarfsplanungspositionen hinzufügen, löschen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="490ca-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="490ca-124">Wenn die Daten in Excel nicht angezeigt werden können, müssen Sie sich mit aktivierter Option "Angemeldet bleiben" in Microsoft Dynamics 365 for Finance and Operations Enterprise Edition anmelden und der Datenverbindungs-App vertrauen.</span><span class="sxs-lookup"><span data-stu-id="490ca-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

