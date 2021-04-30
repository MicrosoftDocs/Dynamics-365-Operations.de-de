---
title: Manuelles Ändern einer Bedarfsplanung
description: In dem Thema wird beschrieben, wie Sie die Planung für einen Artikel ändern
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889023"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="f0cd3-103">Manuelles Ändern einer Bedarfsplanung</span><span class="sxs-lookup"><span data-stu-id="f0cd3-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0cd3-104">Im folgenden Verfahren wird gezeigt, wie Sie die Planung für einen Artikel ändern.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="f0cd3-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f0cd3-106">Diese Prozedur ist für den Produktionsplaner vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="f0cd3-107">Die Planung für einen ausgewählten Artikel ändern</span><span class="sxs-lookup"><span data-stu-id="f0cd3-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="f0cd3-108">Um die Planung für einen ausgewählten Artikel zu ändern:</span><span class="sxs-lookup"><span data-stu-id="f0cd3-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="f0cd3-109">Gehen Sie zu **Module \> Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="f0cd3-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="f0cd3-111">Wählen Sie den Artikel aus, für den Sie die Planung ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="f0cd3-112">Öffnen Sie im Aktivitätsbereich die Registerkarte **Planen** und dann **Bedarfsplanung**.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="f0cd3-113">Wählen Sie in der Liste eine Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-113">In the list, select a row.</span></span> <span data-ttu-id="f0cd3-114">Wenn es keine Planungspositionen gibt, erstellen Sie eine neue Position, indem Sie im Aktivitätsbereich **Neu** auswählen.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="f0cd3-115">Geben Sie im Feld **Verkaufsmenge** eine positive Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="f0cd3-116">Diese Zahl gibt die prognostizierte Menge des Artikels wieder.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="f0cd3-117">Ein Fehler wird angezeigt, wenn Sie eine negative Zahl eingeben.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="f0cd3-118">Füllen Sie bei Bedarf die anderen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="f0cd3-119">Wählen Sie **Speichern** im Aktivitätsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="f0cd3-120">Die Planung für einen oder mehrere Artikel in Microsoft Excel ändern</span><span class="sxs-lookup"><span data-stu-id="f0cd3-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="f0cd3-121">Um die Planung für einen oder mehrere Artikel in Microsoft Excel zu ändern:</span><span class="sxs-lookup"><span data-stu-id="f0cd3-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="f0cd3-122">Führen Sie einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f0cd3-122">Do one of the following:</span></span>
    - <span data-ttu-id="f0cd3-123">Öffnen Sie die Seite **Bedarfsplanung** für einen Artikel (egal welchen) wie im vorherigen Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="f0cd3-124">Wechseln Sie zu **Produktprogrammplan \> Planung \> Planung manuell eintragen \> Bedarfsplanungspositionen**.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="f0cd3-125">Wählen Sie im Aktivitätsbereich **In Microsoft Office öffnen \> Bedarfsplanungseinträge**.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="f0cd3-126">Wählen Sie einen Download-Speicherort aus, speichern Sie die Datei und öffnen Sie die heruntergeladene Datei in Excel.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="f0cd3-127">Wenn Sie eine Warnung sehen, wählen Sie **Bearbeitung aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="f0cd3-128">Melden Sie sich in Excel bei Supply Chain Management über den Aufgabenbereich Microsoft Dynamics an.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="f0cd3-129">Sie müssen sich mit der Option **Angemeldet bleiben** anmelden und Sie müssen der Datenverbindungs-App vertrauen.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="f0cd3-130">In der Excel-Tabelle werden jetzt alle aktuellen Bedarfsplanungspositionen für Ihr Unternehmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="f0cd3-131">Sie können Bedarfsplanungspositionen nach Bedarf hinzufügen, löschen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="f0cd3-132">Wählen Sie **Veröffentlichen** im Aufgabenbereich von Microsoft Dynamics, um Ihre Änderungen wieder in Supply Chain Management hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="f0cd3-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
