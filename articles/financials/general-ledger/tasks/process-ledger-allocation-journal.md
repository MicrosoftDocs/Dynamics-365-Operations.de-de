---
title: Sachkonto-Zuordnungserfassung verarbeiten
description: Mithilfe der Seite "Zuordnungsanforderung verarbeiten" können Sie eine Zuordnungserfassung erstellen, die vor der Buchung im Hauptbuch geprüft und genehmigt oder direkt im Hauptbuch gebucht werden kann.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 087bd4f203e8762447e823b19076b79296a390d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846366"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="803f7-103">Sachkonto-Zuordnungserfassung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="803f7-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="803f7-104">Mithilfe der Seite "Zuordnungsanforderung verarbeiten" können Sie eine Zuordnungserfassung erstellen, die vor der Buchung im Hauptbuch geprüft und genehmigt oder direkt im Hauptbuch gebucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="803f7-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="803f7-105">Vor der Erstellung einer Zuordnungserfassung muss mindesten eine Sachkontozuordnungsregel erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="803f7-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="803f7-106">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="803f7-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="803f7-107">Wechseln Sie zu "Hauptbuch" > "Zuteilungen" > "Zuteilungsanforderung verarbeiten".</span><span class="sxs-lookup"><span data-stu-id="803f7-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="803f7-108">Klicken Sie im Feld "Regel" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="803f7-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="803f7-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="803f7-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="803f7-110">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="803f7-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="803f7-111">Geben Sie im Feld "Per Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="803f7-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="803f7-112">Das Anfangsdatum ist außerordentlich wichtig, wenn das Sachkonto die Datenquelle für die Regel ist.</span><span class="sxs-lookup"><span data-stu-id="803f7-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="803f7-113">Dieses Datum steuert, welche Sachkonto für die Zuweisung genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="803f7-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="803f7-114">Wählen Sie im Feld "Keine Quelle" "Beenden".</span><span class="sxs-lookup"><span data-stu-id="803f7-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="803f7-115">Dies beendet den Zuordnungsprozess und eine Fehlermeldung mit dem Hinweis wird angezeigt, dass ein Ausgangsbetrag mit dem Wert "Null" ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="803f7-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="803f7-116">Wählen Sie im Feld "Vorschlagsoptionen" "nur Vorschlag" aus.</span><span class="sxs-lookup"><span data-stu-id="803f7-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="803f7-117">Wählen Sie "Nur Vorschlag" aus, um das Ergebnis in den Zuordnungserfassungen vor dem Buchen der Zuordnung in das Hauptbuch zu prüfen und optional zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="803f7-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="803f7-118">Geben Sie im Feld "Datum für Sachkontobuchung" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="803f7-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="803f7-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="803f7-119">Click OK.</span></span>
9. <span data-ttu-id="803f7-120">Wechseln Sie zu "Hauptbuch" > "Zuteilungen" > "Zuteilungserfassungen".</span><span class="sxs-lookup"><span data-stu-id="803f7-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="803f7-121">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="803f7-121">Click Lines.</span></span>
11. <span data-ttu-id="803f7-122">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="803f7-122">Click Post.</span></span>
12. <span data-ttu-id="803f7-123">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="803f7-123">Click Post.</span></span>

