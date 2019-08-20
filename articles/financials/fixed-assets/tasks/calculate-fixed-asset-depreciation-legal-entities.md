---
title: Anlagenabschreibung über juristische Personen hinweg berechnen
description: Anlagenabschreibung kann über juristische Personen hinweg in einem Einzelschritt ausgeführt werden.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 500aa71e57f9c1ac8d1a2a080468381bc248741c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840096"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="838e3-103">Anlagenabschreibung über juristische Personen hinweg berechnen</span><span class="sxs-lookup"><span data-stu-id="838e3-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="838e3-104">Anlagenabschreibung kann über juristische Personen hinweg in einem Einzelschritt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="838e3-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="838e3-105">Dieses Verfahren beschreibt, wie Sie den Prozess für mehrere juristische Personen einrichten und ausführen können.</span><span class="sxs-lookup"><span data-stu-id="838e3-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="838e3-106">Dabei werden die Buchhalterrolle und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="838e3-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="838e3-107">Einrichten unternehmensübergreifender Abschreibungs-Ausführungserfassungen</span><span class="sxs-lookup"><span data-stu-id="838e3-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="838e3-108">Wechseln Sie zu "Anlagen" > "Einstellungen" > "Anlagenparameter".</span><span class="sxs-lookup"><span data-stu-id="838e3-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="838e3-109">Erweitern Sie den Anlagenvorschlagsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="838e3-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="838e3-110">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="838e3-110">Click Add.</span></span>
4. <span data-ttu-id="838e3-111">Geben Sie im Feld 'Buchungsebene' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="838e3-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="838e3-112">Geben Sie im Feld 'Journal' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="838e3-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="838e3-113">Wiederholen die Erfassungseinrichtung auf der Anlagenparameterseite in jeder juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="838e3-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="838e3-114">Abschreibungsausführung</span><span class="sxs-lookup"><span data-stu-id="838e3-114">Depreciation run</span></span>
1. <span data-ttu-id="838e3-115">Wechseln Sie zu "Anlagen" > "Erfassungseinträge" > "Abschreibungsvorschlag" erstellen.</span><span class="sxs-lookup"><span data-stu-id="838e3-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="838e3-116">Geben Sie im Feld 'Buchungsebene' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="838e3-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="838e3-117">Der Journalname ist standardmäßig von den Anlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="838e3-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="838e3-118">Er kann für die aktuelle juristische Person hier geändert werden.</span><span class="sxs-lookup"><span data-stu-id="838e3-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="838e3-119">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="838e3-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="838e3-120">Dient zum Auswählen der in der Abschreibungsausführung einzubeziehenden juristischen Personen.</span><span class="sxs-lookup"><span data-stu-id="838e3-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="838e3-121">Nur juristische Personen mit Erfassungen, die für Anlagenvorschläge auf der Anlagenparameterseite eingerichtet werden, werden in der Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="838e3-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="838e3-122">Wählen Sie "Ja" im Feld "Erfassungen buchen" aus.</span><span class="sxs-lookup"><span data-stu-id="838e3-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="838e3-123">Filterungsfelder enthalten alle Anlagen und Bücher, Gruppen für die juristischen Personen, die für diese Abschreibungsausführung ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="838e3-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="838e3-124">Die Stapelverarbeitungsoption ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="838e3-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="838e3-125">Wenn diese Option aktiviert ist, werden die Abschreibungserfassungserstellung und Buchung im Hintergrund ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="838e3-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="838e3-126">Klicken Sie auf "Erfassung erstellen".</span><span class="sxs-lookup"><span data-stu-id="838e3-126">Click Create journal.</span></span>
6. <span data-ttu-id="838e3-127">Wechseln Sie zu "Anlagen" > "Journaleinträge" > "Anlagenerfassung".</span><span class="sxs-lookup"><span data-stu-id="838e3-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

