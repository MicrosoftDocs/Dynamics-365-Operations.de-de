--- 
title: "Zahlungsnachlässe verarbeiten"
description: "Diese Verfahren zeigt, wie genehmigte und verarbeiteten Debitorenrückvergütungen zu den Gutschriften konvertiert."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 791ec304b9ea7c49fbea506d73c4daffd4478739
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="a8300-103">Zahlungsnachlässe verarbeiten</span><span class="sxs-lookup"><span data-stu-id="a8300-103">Process rebates for payment</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8300-104">Diese Verfahren zeigt, wie genehmigte und verarbeiteten Debitorenrückvergütungen zu den Gutschriften konvertiert.</span><span class="sxs-lookup"><span data-stu-id="a8300-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="a8300-105">Sie können diese Anleitung im Demodatenunternehmen USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8300-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="a8300-106">Die Vorbedingung für dieses Handbuch ist, eine oder mehrere Rückvergütungsansprüche zu haben, die einen Status der Markierung haben.</span><span class="sxs-lookup"><span data-stu-id="a8300-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="a8300-107">Wenn Sie USMF verwenden, sollten Sie das "generieren und verarbeiten Kundenrabatt" Handbuch ausführen, bevor Sie dieses Handbuch starten.</span><span class="sxs-lookup"><span data-stu-id="a8300-107">If you’re using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="a8300-108">Konvertieren Sie Rückvergütungsansprüche zur Gutschrift</span><span class="sxs-lookup"><span data-stu-id="a8300-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="a8300-109">Dient zum Zusammenführen aller Debitoren.</span><span class="sxs-lookup"><span data-stu-id="a8300-109">Go to All customers.</span></span>
2. <span data-ttu-id="a8300-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="a8300-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a8300-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a8300-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a8300-112">Klicken Sie im Aktivitätsbereich auf "Sammeln".</span><span class="sxs-lookup"><span data-stu-id="a8300-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="a8300-113">Klicken Sie auf Transaktionen ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="a8300-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="a8300-114">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a8300-114">Click Functions.</span></span>
7. <span data-ttu-id="a8300-115">Einrichten des Rückvergütungsprogramms</span><span class="sxs-lookup"><span data-stu-id="a8300-115">Click Rebate program.</span></span>
    * <span data-ttu-id="a8300-116">Die Rückvergütungsseite werden die Rückvergütungsansprüche aufgeführt, die im Kundenrabattwerktisch verarbeitet haben und die in Status Markieren sind.</span><span class="sxs-lookup"><span data-stu-id="a8300-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="a8300-117">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="a8300-117">Click Edit.</span></span>
    * <span data-ttu-id="a8300-118">Legen Sie Häkchen im Markengebiet für die Ansprüche fest, die Sie in Gutschrift einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a8300-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="a8300-119">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a8300-119">Click Functions.</span></span>
10. <span data-ttu-id="a8300-120">Klicken Sie, um die Gutschrift zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8300-120">Click Create credit note.</span></span>
    * <span data-ttu-id="a8300-121">Eine Meldung, Sie zu informieren, dass eine Erfassung gebucht wurde (dies ist die Debitoren-Verbrauchserfassung, wie in der Debitorenparameterseite angegeben).</span><span class="sxs-lookup"><span data-stu-id="a8300-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="a8300-122">Dies führt dazu den tatsächlichen Betrag der Passivposten (Haben), auf den Debitorensaldo verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="a8300-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="a8300-123">Auf dieser Stufe ist das Nachlassabgrenzungskonto belastet worden, und dem Nachlassausgabenkonto ist gutgeschrieben worden.</span><span class="sxs-lookup"><span data-stu-id="a8300-123">This means that the customer’s account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="a8300-124">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a8300-124">Close the page.</span></span>
12. <span data-ttu-id="a8300-125">Klicken Sie auf "Abbrechen".</span><span class="sxs-lookup"><span data-stu-id="a8300-125">Click Cancel.</span></span>
    * <span data-ttu-id="a8300-126">Dieses aktualisiert die Seite, um die Aktualisierungen finden können.</span><span class="sxs-lookup"><span data-stu-id="a8300-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="a8300-127">Klicken Sie im Aktivitätsbereich auf "Sammeln".</span><span class="sxs-lookup"><span data-stu-id="a8300-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="a8300-128">Klicken Sie auf Transaktionen ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="a8300-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="a8300-129">Beachten Sie, dass eine Buchung für einen negativen Betrag, der gesamte Nachlassbetrag, ohne Rechnungsreferenz darstellend zum Debitorensaldo hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="a8300-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="a8300-130">Klicken Sie auf "Abbrechen".</span><span class="sxs-lookup"><span data-stu-id="a8300-130">Click Cancel.</span></span>


