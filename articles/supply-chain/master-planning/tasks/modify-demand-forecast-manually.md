---
title: 'Anleitung: Manuelles Ändern einer Bedarfsplanung'
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
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224009"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="8a23a-103">Anleitung: Manuelles Ändern einer Bedarfsplanung</span><span class="sxs-lookup"><span data-stu-id="8a23a-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a23a-104">Im folgenden Verfahren wird gezeigt, wie Sie die Planung für einen Artikel ändern.</span><span class="sxs-lookup"><span data-stu-id="8a23a-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="8a23a-105">Diese Prozedur ist für den Produktionsplaner vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="8a23a-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="8a23a-106">Die Planung für einen ausgewählten Artikel ändern</span><span class="sxs-lookup"><span data-stu-id="8a23a-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="8a23a-107">Um die Planung für einen ausgewählten Artikel zu ändern:</span><span class="sxs-lookup"><span data-stu-id="8a23a-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="8a23a-108">Gehen Sie zu **Module \> Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="8a23a-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8a23a-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8a23a-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="8a23a-110">Wählen Sie den Artikel aus, für den Sie die Planung ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="8a23a-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="8a23a-111">Öffnen Sie im Aktivitätsbereich die Registerkarte **Planen** und dann **Bedarfsplanung**.</span><span class="sxs-lookup"><span data-stu-id="8a23a-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="8a23a-112">Wählen Sie in der Liste eine Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="8a23a-112">In the list, select a row.</span></span> <span data-ttu-id="8a23a-113">Wenn es keine Planungspositionen gibt, erstellen Sie eine neue Position, indem Sie im Aktivitätsbereich **Neu** auswählen.</span><span class="sxs-lookup"><span data-stu-id="8a23a-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="8a23a-114">Geben Sie im Feld **Verkaufsmenge** eine positive Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8a23a-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="8a23a-115">Diese Zahl gibt die prognostizierte Menge des Artikels wieder.</span><span class="sxs-lookup"><span data-stu-id="8a23a-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="8a23a-116">Ein Fehler wird angezeigt, wenn Sie eine negative Zahl eingeben.</span><span class="sxs-lookup"><span data-stu-id="8a23a-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="8a23a-117">Füllen Sie bei Bedarf die anderen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="8a23a-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="8a23a-118">Wählen Sie **Speichern** im Aktivitätsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="8a23a-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="8a23a-119">Die Planung für einen oder mehrere Artikel in Microsoft Excel ändern</span><span class="sxs-lookup"><span data-stu-id="8a23a-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="8a23a-120">So ändern Sie die Planung für einen oder mehrere Artikel in Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="8a23a-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="8a23a-121">Führen Sie einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="8a23a-121">Do one of the following:</span></span>
    - <span data-ttu-id="8a23a-122">Öffnen Sie die Seite **Bedarfsplanung** für einen Artikel (egal welchen) wie im vorherigen Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8a23a-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="8a23a-123">Wechseln Sie zu **Produktprogrammplan \> Planung \> Planung manuell eintragen \> Bedarfsplanungspositionen**.</span><span class="sxs-lookup"><span data-stu-id="8a23a-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="8a23a-124">Wählen Sie im Aktivitätsbereich **In Microsoft Office öffnen \> Bedarfsplanungseinträge**.</span><span class="sxs-lookup"><span data-stu-id="8a23a-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="8a23a-125">Wählen Sie einen Download-Speicherort aus, speichern Sie die Datei und öffnen Sie die heruntergeladene Datei in Excel.</span><span class="sxs-lookup"><span data-stu-id="8a23a-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="8a23a-126">Wenn Sie eine Warnung sehen, wählen Sie **Bearbeitung aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="8a23a-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="8a23a-127">Melden Sie sich in Excel bei Supply Chain Management über den Aufgabenbereich Microsoft Dynamics an.</span><span class="sxs-lookup"><span data-stu-id="8a23a-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="8a23a-128">Sie müssen sich mit der Option **Angemeldet bleiben** anmelden und Sie müssen der Datenverbindungs-App vertrauen.</span><span class="sxs-lookup"><span data-stu-id="8a23a-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="8a23a-129">In der Excel-Tabelle werden jetzt alle aktuellen Bedarfsplanungspositionen für Ihr Unternehmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8a23a-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="8a23a-130">Sie können Bedarfsplanungspositionen nach Bedarf hinzufügen, löschen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8a23a-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="8a23a-131">Wählen Sie **Veröffentlichen** im Aufgabenbereich von Microsoft Dynamics, um Ihre Änderungen wieder in Supply Chain Management hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="8a23a-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
