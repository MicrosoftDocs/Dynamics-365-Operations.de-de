---
title: Einrichten von vordatierten Schecks
description: In diesem Thema wird erläutert, wie angegeben wird, ob Journaleinträge für vordatierte Schecks gebucht werden sollen, und welche Erfassungen für das Verrechnen von Einträgen und von Kreditorenzahlungen verwendet werden sollen.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8696aeccee651368a036ab8d90980e9ed9cea6b3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841872"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="e3bb6-103">Einrichten von vordatierten Schecks</span><span class="sxs-lookup"><span data-stu-id="e3bb6-103">Set up postdated checks</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e3bb6-104">In diesem Thema wird erläutert, wie angegeben wird, ob Journaleinträge für vordatierte Schecks gebucht werden sollen, und welche Erfassungen für das Verrechnen von Einträgen und von Kreditorenzahlungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="e3bb6-105">Sie können auch Verrechnungskonten für ausgestellte Schecks, erhaltene Schecks oder für die Quellensteuer angeben.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="e3bb6-106">Vordatierte Schecks sind Schecks, die ausgestellt werden, um Zahlungen zu einem späteren Datum leisten oder erhalten zu können.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="e3bb6-107">Sie können angeben, ob der Scheck vor seinem Fälligkeitsdatum in Ihren Kontoblättern widergespiegelt sein muss.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="e3bb6-108">Die Rolle dieser Prozedur ist "Finanzverwalter".</span><span class="sxs-lookup"><span data-stu-id="e3bb6-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="e3bb6-109">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="e3bb6-110">Einrichten von vordatierten Schecks</span><span class="sxs-lookup"><span data-stu-id="e3bb6-110">Set up postdated checks</span></span>
1. <span data-ttu-id="e3bb6-111">Wechseln Sie zu "Kasse und Bankverwaltung > Einstellungen > Parameter für Kasse- und Bankverwaltung.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="e3bb6-112">Klicken Sie auf die Registerkarte "Vordatierte Schecks".</span><span class="sxs-lookup"><span data-stu-id="e3bb6-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="e3bb6-113">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Vordatierte Schecks aktivieren".</span><span class="sxs-lookup"><span data-stu-id="e3bb6-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="e3bb6-114">Aktivieren bzw. deaktivieren Sie die Beitragsjournaleinträge für Kontrollkästchen der vordatierten Schecks.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="e3bb6-115">Geben Sie im Feld Verrechnungskonto die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="e3bb6-116">Geben Sie im Feld Verrechnungskonto für erhaltene Schecks die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="e3bb6-117">In der allgemeinen Erfassung für das Vorbereiten des Eintrags felds, geben Sie einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="e3bb6-118">Geben Sie im Feld "Vordatierte Schecks in diese Kreditoren-Zahlungserfassung übertragen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="e3bb6-119">Geben Sie im Feld Verrechnungskonto für Quellensteuer die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="e3bb6-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e3bb6-120">Click Save.</span></span>
11. <span data-ttu-id="e3bb6-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-121">Close the page.</span></span>
12. <span data-ttu-id="e3bb6-122">Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".</span><span class="sxs-lookup"><span data-stu-id="e3bb6-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="e3bb6-123">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e3bb6-123">Click New.</span></span>
14. <span data-ttu-id="e3bb6-124">Geben Sie im Feld "Zahlungsmethode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="e3bb6-125">Markieren Sie das Kontrollkästchen , um anzugeben, dass der Scheckbetrag zu einem Verrechnungskonto gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="e3bb6-126">Wählen Sie im Feld "Kontotyp" "Bank" aus.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="e3bb6-127">Das Gegenkonto der Zahlungsmethode ist eine Bank.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="e3bb6-128">Geben Sie im Feld "Zahlungskonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="e3bb6-129">Wählen Sie das Bankkonto aus, das zum Abziehen des Rechnungsbetrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="e3bb6-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-130">Close the page.</span></span>
19. <span data-ttu-id="e3bb6-131">Wechseln Sie zu "Debitoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".</span><span class="sxs-lookup"><span data-stu-id="e3bb6-131">Go to Accounts receivable > Payment setup > Methods of payment</span></span>
20. <span data-ttu-id="e3bb6-132">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e3bb6-132">Click New.</span></span>
21. <span data-ttu-id="e3bb6-133">Geben Sie im Feld "Zahlungsmethode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-133">In the Method of payment field, type a value.</span></span>
22. <span data-ttu-id="e3bb6-134">Markieren Sie das Kontrollkästchen , um anzugeben, dass der Scheckbetrag zu einem Verrechnungskonto gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-134">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
23. <span data-ttu-id="e3bb6-135">Wählen Sie im Feld "Kontotyp" "Bank" aus.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-135">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="e3bb6-136">Das Gegenkonto der Zahlungsmethode ist eine Bank.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-136">The offset account of the payment method will be a bank.</span></span>  
24. <span data-ttu-id="e3bb6-137">Geben Sie im Feld "Zahlungskonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-137">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="e3bb6-138">Wählen Sie das Bankkonto aus, das zum Abziehen des Rechnungsbetrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-138">Select the bank account that is used to deduct the invoice amount.</span></span>  
25. <span data-ttu-id="e3bb6-139">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e3bb6-139">Close the page.</span></span>

