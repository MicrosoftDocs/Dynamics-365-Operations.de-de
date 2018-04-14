--- 
title: "Anlagenabschreibung über juristische Personen hinweg berechnen"
description: "Dieses Verfahren beschreibt, wie Sie den Abschreibungsprozess für mehrere juristische Personen einrichten und ausführen können."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 662554b1b6bed63e5017aad3a292dad7a2f0bcea
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="2d528-103">Anlagenabschreibung über juristische Personen hinweg berechnen</span><span class="sxs-lookup"><span data-stu-id="2d528-103">Calculate fixed asset depreciation across legal entities</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d528-104">Anlagenabschreibung kann über juristische Personen hinweg in einem Einzelschritt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2d528-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="2d528-105">Dieses Verfahren beschreibt, wie Sie den Prozess für mehrere juristische Personen einrichten und ausführen können.</span><span class="sxs-lookup"><span data-stu-id="2d528-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="2d528-106">Es verwendet die Buchhalterrolle.</span><span class="sxs-lookup"><span data-stu-id="2d528-106">It uses the accountant role.</span></span>  

<span data-ttu-id="2d528-107">Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d528-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="2d528-108">Schritt(16) Unteraufgabe: Einrichten unternehmensübergreifender Abschreibungs-Ausführungserfassungen.</span><span class="sxs-lookup"><span data-stu-id="2d528-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="2d528-109">Zunächst müssen Sie die in der unternehmensübergreifenden Abschreibung zu verwendenden Erfassungen einrichten, die in jeder juristischen Person ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d528-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="2d528-110">Wechseln Sie zu "Anlagen" > "Einstellungen" > "Anlagenparameter".</span><span class="sxs-lookup"><span data-stu-id="2d528-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="2d528-111">Erweitern Sie den Anlagenvorschlagsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="2d528-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="2d528-112">Erstellen Sie einen Datensatz mit dem für jede Buchungsebene in der juristischen Person zu verwendenden Journal.</span><span class="sxs-lookup"><span data-stu-id="2d528-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="2d528-113">Wenn Bücher nicht im Hauptbuch gebucht werden, sollte keine die Buchungsebene mit dem zugeordneten Journal ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="2d528-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="2d528-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2d528-114">Click Add.</span></span> 
4. <span data-ttu-id="2d528-115">Geben Sie im Feld 'Buchungsebene' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2d528-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="2d528-116">Geben Sie im Feld 'Journal' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2d528-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="2d528-117">Wiederholen die Erfassungseinrichtung auf der Anlagenparameterseite in jeder juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="2d528-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="2d528-118">Unteraufgabe: Abschreibung berechnen.</span><span class="sxs-lookup"><span data-stu-id="2d528-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="2d528-119">Verwenden Sie die Seite Abschreibungsvorschlag, um die Abschreibung zu starten, die zu den juristischen Personen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d528-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="2d528-120">Wechseln Sie zu "Anlagen" > "Erfassungseinträge" > "Abschreibungsvorschlag" erstellen.</span><span class="sxs-lookup"><span data-stu-id="2d528-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="2d528-121">Geben Sie im Feld 'Buchungsebene' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2d528-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="2d528-122">Der Journalname ist standardmäßig von den Anlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="2d528-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="2d528-123">Er kann für die aktuelle juristische Person hier geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2d528-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="2d528-124">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="2d528-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="2d528-125">Dient zum Auswählen der in der Abschreibungsausführung einzubeziehenden juristischen Personen.</span><span class="sxs-lookup"><span data-stu-id="2d528-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="2d528-126">Nur juristische Personen mit Erfassungen, die für Anlagenvorschläge auf der Anlagenparameterseite eingerichtet werden, werden in der Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2d528-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="2d528-127">Wenn dieser Schlüssel aktiviert ist, wird die Beitragserfassungsoption automatisch die Abschreibungserfassungen, wenn sie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2d528-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="2d528-128">Wenn sie nicht ausgewählt ist, werden Erfassungen erstellt, aber nicht gebucht, sodass Sie die Details prüfen, bevor sie gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="2d528-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="2d528-129">Wählen Sie "Ja" im Feld "Erfassungen buchen" aus.</span><span class="sxs-lookup"><span data-stu-id="2d528-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="2d528-130">Filterungsfelder enthalten alle Anlagen und Bücher, Gruppen für die juristischen Personen, die für diese Abschreibungsausführung ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="2d528-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="2d528-131">Die Stapelverarbeitungsoption ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2d528-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="2d528-132">Wenn diese Option aktiviert ist, werden die Abschreibungserfassungserstellung und Buchung im Hintergrund ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d528-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="2d528-133">Klicken Sie auf "Erfassung erstellen".</span><span class="sxs-lookup"><span data-stu-id="2d528-133">Click Create journal.</span></span> 
10. <span data-ttu-id="2d528-134">Sie müssen die Abschreibungserfassungen anzeigen, die in der entsprechenden juristischen Personen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2d528-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="2d528-135">Wechseln Sie zu "Anlagen" > "Journaleinträge" > "Anlagenerfassung".</span><span class="sxs-lookup"><span data-stu-id="2d528-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

