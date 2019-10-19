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
ms.openlocfilehash: 035f6e3b0268f8ee4c9006ca5f0527133cf2771c
ms.sourcegitcommit: 69f8233e86b32347474a25d83b4ac5920f60407d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/02/2019
ms.locfileid: "2538477"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="22297-103">Einrichten von vordatierten Schecks</span><span class="sxs-lookup"><span data-stu-id="22297-103">Set up postdated checks</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22297-104">In diesem Thema wird erläutert, wie angegeben wird, ob Journaleinträge für vordatierte Schecks gebucht werden sollen, und welche Erfassungen für das Verrechnen von Einträgen und von Kreditorenzahlungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="22297-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="22297-105">Sie können auch Verrechnungskonten für ausgestellte Schecks, erhaltene Schecks oder für die Quellensteuer angeben.</span><span class="sxs-lookup"><span data-stu-id="22297-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="22297-106">Vordatierte Schecks sind Schecks, die ausgestellt werden, um Zahlungen zu einem späteren Datum leisten oder erhalten zu können.</span><span class="sxs-lookup"><span data-stu-id="22297-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="22297-107">Sie können angeben, ob der Scheck vor seinem Fälligkeitsdatum in Ihren Kontoblättern widergespiegelt sein muss.</span><span class="sxs-lookup"><span data-stu-id="22297-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="22297-108">Die Rolle dieser Prozedur ist "Finanzverwalter".</span><span class="sxs-lookup"><span data-stu-id="22297-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="22297-109">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="22297-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="22297-110">Einrichten von vordatierten Schecks</span><span class="sxs-lookup"><span data-stu-id="22297-110">Set up postdated checks</span></span>
1. <span data-ttu-id="22297-111">Wechseln Sie zu "Kasse und Bankverwaltung > Einstellungen > Parameter für Kasse- und Bankverwaltung.</span><span class="sxs-lookup"><span data-stu-id="22297-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="22297-112">Klicken Sie auf die Registerkarte "Vordatierte Schecks".</span><span class="sxs-lookup"><span data-stu-id="22297-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="22297-113">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Vordatierte Schecks aktivieren".</span><span class="sxs-lookup"><span data-stu-id="22297-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="22297-114">Aktivieren bzw. deaktivieren Sie die Beitragsjournaleinträge für Kontrollkästchen der vordatierten Schecks.</span><span class="sxs-lookup"><span data-stu-id="22297-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="22297-115">Geben Sie im Feld Verrechnungskonto die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="22297-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="22297-116">Geben Sie im Feld Verrechnungskonto für erhaltene Schecks die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="22297-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="22297-117">In der allgemeinen Erfassung für das Vorbereiten des Eintrags felds, geben Sie einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="22297-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="22297-118">Geben Sie im Feld "Vordatierte Schecks in diese Kreditoren-Zahlungserfassung übertragen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="22297-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="22297-119">Geben Sie im Feld Verrechnungskonto für Quellensteuer die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="22297-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="22297-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="22297-120">Click Save.</span></span>
11. <span data-ttu-id="22297-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="22297-121">Close the page.</span></span>
12. <span data-ttu-id="22297-122">Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".</span><span class="sxs-lookup"><span data-stu-id="22297-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="22297-123">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="22297-123">Click New.</span></span>
14. <span data-ttu-id="22297-124">Geben Sie im Feld "Zahlungsmethode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="22297-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="22297-125">Markieren Sie das Kontrollkästchen , um anzugeben, dass der Scheckbetrag zu einem Verrechnungskonto gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="22297-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="22297-126">Wählen Sie im Feld "Kontotyp" "Bank" aus.</span><span class="sxs-lookup"><span data-stu-id="22297-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="22297-127">Das Gegenkonto der Zahlungsmethode ist eine Bank.</span><span class="sxs-lookup"><span data-stu-id="22297-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="22297-128">Geben Sie im Feld "Zahlungskonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="22297-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="22297-129">Wählen Sie das Bankkonto aus, das zum Abziehen des Rechnungsbetrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22297-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="22297-130">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="22297-130">Click Save.</span></span>
19. <span data-ttu-id="22297-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="22297-131">Close the page.</span></span>

