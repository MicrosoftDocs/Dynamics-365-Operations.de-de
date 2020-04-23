---
title: Produktionsauftrag beenden
description: Diese Prozedur zeigt, wie ein Produktionsauftrag beendet wird.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fade659c320e0ea1059644324859c9a3cb273c96
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207070"
---
# <a name="end-a-production-order"></a><span data-ttu-id="c76a4-103">Produktionsauftrag beenden</span><span class="sxs-lookup"><span data-stu-id="c76a4-103">End a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c76a4-104">Diese Prozedur zeigt, wie ein Produktionsauftrag beendet wird.</span><span class="sxs-lookup"><span data-stu-id="c76a4-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="c76a4-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="c76a4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c76a4-106">Dies ist die abschließende Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.</span><span class="sxs-lookup"><span data-stu-id="c76a4-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="c76a4-107">Produktionsauftrag beenden</span><span class="sxs-lookup"><span data-stu-id="c76a4-107">End a production order</span></span>
1. <span data-ttu-id="c76a4-108">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="c76a4-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="c76a4-109">Wählen Sie einen Produktionsauftrag aus, der den Status "Fertig gemeldet" hat.</span><span class="sxs-lookup"><span data-stu-id="c76a4-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="c76a4-110">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="c76a4-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="c76a4-111">Klicken Sie auf "Beenden".</span><span class="sxs-lookup"><span data-stu-id="c76a4-111">Click End.</span></span>
    * <span data-ttu-id="c76a4-112">Auf dieser Seite können Sie das Beenden des Produktionsauftrags bestätigen.</span><span class="sxs-lookup"><span data-stu-id="c76a4-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="c76a4-113">Klicken Sie auf die Registerkarte "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="c76a4-113">Click the General tab.</span></span>
5. <span data-ttu-id="c76a4-114">Geben Sie ein Datum in das Feld "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="c76a4-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="c76a4-115">Wählen Sie im Feld "Ausschussmethode" "Zuordnung" aus.</span><span class="sxs-lookup"><span data-stu-id="c76a4-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="c76a4-116">Wenn Sie die Zuordnungsmethode auswählen, werden die Kosten des Ausschusses zu den Fertigerzeugnissen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c76a4-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="c76a4-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c76a4-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="c76a4-118">Berechnungergebnisse überprüfen</span><span class="sxs-lookup"><span data-stu-id="c76a4-118">Validate calculation results</span></span>
1. <span data-ttu-id="c76a4-119">Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".</span><span class="sxs-lookup"><span data-stu-id="c76a4-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="c76a4-120">Klicken Sie auf "Kostenvergleich anzeigen".</span><span class="sxs-lookup"><span data-stu-id="c76a4-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="c76a4-121">Nachdem Sie den Produktionsauftrag abgeschlossen haben, können Sie den vorkalkulierten Einstandspreis mit dem realisierten Einstandspreis vergleichen, um einen Überblick über die Produktionsabweichungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c76a4-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  
