--- 
title: Erstellen von Sachkonto-Abgrenzungsbuchungen
description: "Dieser Aufgabenleitfaden führt Sie durch die Generierung von Sachkontoabgrenzungsbuchungen, die auf Abgrenzungsschemata basieren."
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: f9d2d1fe36f53a70e5ae91b4c194d4a468f3ee54
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2018

---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="625d8-103">Erstellen von Sachkonto-Abgrenzungsbuchungen</span><span class="sxs-lookup"><span data-stu-id="625d8-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="625d8-104">Dieser Aufgabenleitfaden führt Sie durch die Generierung von Sachkontoabgrenzungsbuchungen, die auf Abgrenzungsschemata basieren.</span><span class="sxs-lookup"><span data-stu-id="625d8-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="625d8-105">Wechseln Sie zu "Hauptbuch" > "Journaleinträge" > "Allgemeine Erfassungen".</span><span class="sxs-lookup"><span data-stu-id="625d8-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="625d8-106">Suchen Sie in der Liste die gewünschte Erfassung oder erstellen Sie eine neue.</span><span class="sxs-lookup"><span data-stu-id="625d8-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="625d8-107">Klicken Sie, um dem Link im Feld "Lfd. Nummer" zu folgen.</span><span class="sxs-lookup"><span data-stu-id="625d8-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="625d8-108">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="625d8-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="625d8-109">Geben Sie im Feld "Konto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="625d8-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="625d8-110">In diesem Beispiel definieren wir die Aufwendungen für die Versicherung.</span><span class="sxs-lookup"><span data-stu-id="625d8-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="625d8-111">Es ist treten regelmäßige Ausgabenbeträge auf.</span><span class="sxs-lookup"><span data-stu-id="625d8-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="625d8-112">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="625d8-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="625d8-113">Geben Sie im Feld "Soll" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="625d8-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="625d8-114">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="625d8-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="625d8-115">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="625d8-115">Click Functions.</span></span>
10. <span data-ttu-id="625d8-116">Klicken Sie auf "Sachkontoabgrenzungen".</span><span class="sxs-lookup"><span data-stu-id="625d8-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="625d8-117">Klicken Sie im Feld "Abgrenzungskennung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="625d8-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="625d8-118">Suchen Sie in der Liste das anzuwendende Abgrenzungsschema und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="625d8-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="625d8-119">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="625d8-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="625d8-120">Geben Sie im Feld "Startdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="625d8-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="625d8-121">Klicken Sie auf "Transaktionen".</span><span class="sxs-lookup"><span data-stu-id="625d8-121">Click Transactions.</span></span>
16. <span data-ttu-id="625d8-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="625d8-122">Close the page.</span></span>
17. <span data-ttu-id="625d8-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="625d8-123">Click OK.</span></span>
18. <span data-ttu-id="625d8-124">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="625d8-124">Click Post.</span></span>


