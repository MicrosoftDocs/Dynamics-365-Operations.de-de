---
title: Buchung (Definitionen)
description: Dieser Artikel enthält Informationen zu Buchungsdefinitionen und erläutert, wie sie definiert und verknüpft werden. Für unterstützte Buchungstypen und Dokumente können Sie Buchungsdefinitionen anstelle von Buchungsprofilen verwenden, um Hauptkonten und Finanzdimensionen in Buchhaltungseinträge zu klassifizieren.
author: ShylaThompson
manager: AnnBe
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22a7b0acae02738e4f14905edb13fac1da0d0213
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770596"
---
# <a name="posting-definitions"></a><span data-ttu-id="d44c6-104">Buchung (Definitionen)</span><span class="sxs-lookup"><span data-stu-id="d44c6-104">Posting definitions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d44c6-105">Dieser Artikel enthält Informationen zu Buchungsdefinitionen und erläutert, wie sie definiert und verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="d44c6-105">This article provides information about posting definitions, and how to define and link them.</span></span>
<span data-ttu-id="d44c6-106">Für unterstützte Buchungstypen und Dokumente können Sie Buchungsdefinitionen anstelle von Buchungsprofilen verwenden, um Hauptkonten und Finanzdimensionen in Buchhaltungseinträge zu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="d44c6-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="d44c6-107">Sie können die unterstützten Dokumente und die Buchungstypen auf der Seite **Buchung - Definitionen** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d44c6-107">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="d44c6-108">Um Buchungsdefinitionen zu verwenden, aktivieren Sie die Option**Buchungsdefinitionen verwenden** auf der Seite **Hauptbuchparameter**.</span><span class="sxs-lookup"><span data-stu-id="d44c6-108">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="d44c6-109">Auch wenn Buchungsdefinitionen verwendet werden, müssen Sie immer noch Buchungsprofile für die Ursprungseinträge und nicht unterstützte Buchungstypen und ‑dokumente definieren.</span><span class="sxs-lookup"><span data-stu-id="d44c6-109">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="d44c6-110">Sie müssen Buchungsdefinitionen verwenden, um einen Belastungsverarbeitungsprozess für Bestellungen und Prozesse zur Verarbeitung von Vorabbelastungen für Bestellanforderungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d44c6-110">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="d44c6-111">Buchungsdefinitionen definieren</span><span class="sxs-lookup"><span data-stu-id="d44c6-111">Defining posting definitions</span></span>
<span data-ttu-id="d44c6-112">Verwenden Sie die Seite**Buchung (Definitionen)**, um die Übereinstimmungskriterien anzugeben und die Einträge zu definieren, die generiert werden sollen, wenn eine Übereinstimmung auftritt.</span><span class="sxs-lookup"><span data-stu-id="d44c6-112">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="d44c6-113">Die Übereinstimmungskriterien werden für die ursprünglichen Posten als Buchhaltungsverteilungen ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="d44c6-113">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="d44c6-114">Auf der Seite **Buchung (Definitionen)** können Sie Erfassungspositionen auch Prioritätsnummern zuweisen, um die Reihenfolge für die Auswertung der Positionen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="d44c6-114">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="d44c6-115">Die Positionen, die die niedrigste Prioritätsnummer haben, werden zuerst ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="d44c6-115">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="d44c6-116">Beispielsweise werden alle Positionen ausgewertet, die eine Priorität von 1 haben, und dann Positionen, die über eine Priorität von 2 verfügen, usw.</span><span class="sxs-lookup"><span data-stu-id="d44c6-116">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="d44c6-117">Wenn eine Übereinstimmung gefunden wird, werden die anderen Übereinstimmungskriterien ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d44c6-117">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="d44c6-118">Zudem wird nur für die Kriterien in der Gruppe, die mit der Ursprungsbuchung übereinstimmen, ein Eintrag generiert.</span><span class="sxs-lookup"><span data-stu-id="d44c6-118">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="d44c6-119">Sie können Ihre Buchungsdefinitionen überprüfen, mithilfe des Assistenten zum **Testen von Buchungsdefinitionen**.</span><span class="sxs-lookup"><span data-stu-id="d44c6-119">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="d44c6-120">Nachdem Sie ein Beispiel definieren, welche Eintrag für eine Buchungsdefinition auslöst, finden Sie die generierten Einträge.</span><span class="sxs-lookup"><span data-stu-id="d44c6-120">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="d44c6-121">Sie können Versionen von Buchungsdefinitionen zusammen mit Gültigkeitsdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="d44c6-121">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="d44c6-122">Erstellen Sie z. B. eine künftige Version einer Buchungsdefinition, um in einem neuen Geschäftsjahr Buchungen in ein anderes Sachkonto vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="d44c6-122">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="d44c6-123">Verwenden Sie die Seite **Buchung – Definitionen**, um Buchungsdefinitionen Transaktionstypen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="d44c6-123">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="d44c6-124">Buchungsdefinitionen verknüpfen</span><span class="sxs-lookup"><span data-stu-id="d44c6-124">Linking posting definitions</span></span>
<span data-ttu-id="d44c6-125">Beim Erstellen von Buchungsdefinitionen können Sie Buchungsdefinitionen miteinander verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d44c6-125">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="d44c6-126">Die Kriterien der verknüpften Definition werden dann zusätzlich zu den Kriterien der aktuellen Buchungsdefinition berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d44c6-126">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="d44c6-127">Mit dieser Funktion können Sie Zeit sparen, da auf der Seite **Buchung (Definitionen)** auf dem Inforegister **Einträge** keine neuen Kriterien für die aktuelle Buchungsdefinition erstellt werden müssen, wenn diese Positionen bereits für eine andere Buchungsdefinition eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="d44c6-127">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="d44c6-128">Schließen Sie in Diagrammen und Tabellen Verknüpfungen ein, die Sie vielleicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="d44c6-128">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="d44c6-129">Um Konflikte mit der aktuellen Buchungsdefinition zu vermeiden, stellen Sie sicher, dass die Positionen in Buchungsdefinitionen, zu denen Sie eine Verknüpfung erstellen, eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="d44c6-129">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="d44c6-130">Die folgenden Einschränkungen gelten für das Erstellen von Verknüpfungen in Buchungsdefinitionen:</span><span class="sxs-lookup"><span data-stu-id="d44c6-130">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="d44c6-131">Eine bestimmte Buchungsdefinition kann jeweils nur in einer Richtung mit einer anderen Buchungsdefinition verknüpft sein oder in beide Richtungen.</span><span class="sxs-lookup"><span data-stu-id="d44c6-131">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="d44c6-132">Eine Buchungsdefinition kann jedoch in mit mehreren Buchungsdefinitionen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="d44c6-132">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="d44c6-133">Verknüpfungen können nur zwischen Buchungsdefinitionen im selben Modul eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="d44c6-133">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="d44c6-134">Sie können eine Buchungsdefinition jeder beliebigen Buchungsart zuweisen, diese muss sich jedoch im selben Modul wie die Buchungsdefinition befinden.</span><span class="sxs-lookup"><span data-stu-id="d44c6-134">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="d44c6-135">Verwenden Sie die Seite **Buchung - Definitionen**, um festzustellen, aus welchem Modul eine Buchungsart ist.</span><span class="sxs-lookup"><span data-stu-id="d44c6-135">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="d44c6-136">Weitere Informationen finden Sie unter [Buchungsdefinitionsbeispiele](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="d44c6-136">For more information, see [Posting definition examples](example-posting-definitions.md).</span></span> 


