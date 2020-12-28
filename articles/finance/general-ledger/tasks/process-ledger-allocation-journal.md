---
title: Sachkonto-Zuordnungserfassung verarbeiten
description: In diesem Thema wird erläutert, wie Sie unter Dynamics 365 Finance eine Zuordnungsanforderung bearbeiten.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 33e989d3641ae1eaa28a55398fcf51674ac1ed72
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443600"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="0c4f7-103">Sachkonto-Zuordnungserfassung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="0c4f7-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c4f7-104">In diesem Thema wird erläutert, wie Sie eine Zuordnungsanforderung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="0c4f7-105">Mithilfe der Seite "Zuordnungsanforderung verarbeiten" können Sie eine Zuordnungserfassung erstellen, die vor der Buchung im Hauptbuch geprüft und genehmigt oder direkt im Hauptbuch gebucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="0c4f7-106">Vor der Erstellung einer Zuordnungserfassung muss mindesten eine Sachkontozuordnungsregel erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="0c4f7-107">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="0c4f7-108">Gehen Sie im Navigationsbereich zu **Module > Hauptbuch > Zuordnungen > Prozessverrechnungsanforderung**.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="0c4f7-109">Wählen Sie im Feld **Regel** den gewünschten Datensatz im Dropdown-Menü aus.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="0c4f7-110">Geben Sie im Feld **Als Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="0c4f7-111">Das **Als Datum** ist sehr wichtig, wenn das Ledger die Datenquelle für die Regel ist.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="0c4f7-112">Dieses Datum steuert, welche Sachkonto für die Zuweisung genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="0c4f7-113">Im Feld **Nullquelle** wählen Sie **Stop**.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="0c4f7-114">Dadurch wird der Zuordnungsprozess gestoppt und eine Meldung angezeigt, die besagt, dass ein Betrag von Null ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="0c4f7-115">Wählen Sie im Feld **Vorschlagsoptionen** **Nur Vorschlag**.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="0c4f7-116">Wählen Sie **Nur Vorschlag**, um das Ergebnis in Allokationsbüchern zu überprüfen und optional zu genehmigen, bevor Sie die Allokation ins Hauptbuch buchen.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="0c4f7-117">Geben Sie im Feld "Datum für Sachkontobuchung" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="0c4f7-118">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-118">Select **OK**.</span></span>
7. <span data-ttu-id="0c4f7-119">Gehen Sie im Navigationsbereich zu **Module > Hauptbuch > Zuordnungen > Zuordnungen > Zuordnungsjournale**.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="0c4f7-120">Wählen Sie **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-120">Select **Lines**.</span></span>
9. <span data-ttu-id="0c4f7-121">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-121">Select **Post**.</span></span>
10. <span data-ttu-id="0c4f7-122">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="0c4f7-122">Select **Post**.</span></span>

