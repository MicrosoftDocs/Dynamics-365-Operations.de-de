---
title: Einrichten von vordatierten Schecks
description: In diesem Thema wird erläutert, wie angegeben wird, ob Journaleinträge für vordatierte Schecks gebucht werden sollen, und welche Erfassungen für das Verrechnen von Einträgen und von Kreditorenzahlungen verwendet werden sollen.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d4afd74f9a0f9018629fa92ab6595bfa94f973
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026204"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="fbdfd-103">Einrichten von vordatierten Schecks</span><span class="sxs-lookup"><span data-stu-id="fbdfd-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fbdfd-104">In diesem Thema wird erläutert, wie angegeben wird, ob Journaleinträge für vordatierte Schecks gebucht werden sollen, und welche Erfassungen für das Verrechnen von Einträgen und von Kreditorenzahlungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="fbdfd-105">Sie können auch Verrechnungskonten für ausgestellte Schecks, erhaltene Schecks oder für die Quellensteuer angeben.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="fbdfd-106">Vordatierte Schecks sind Schecks, die ausgestellt werden, um Zahlungen zu einem späteren Datum leisten oder erhalten zu können.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="fbdfd-107">Sie können angeben, ob der Scheck vor seinem Fälligkeitsdatum in Ihren Kontoblättern widergespiegelt sein muss.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="fbdfd-108">Die Rolle dieser Prozedur ist "Finanzverwalter".</span><span class="sxs-lookup"><span data-stu-id="fbdfd-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="fbdfd-109">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="fbdfd-110">Einrichten von vordatierten Schecks</span><span class="sxs-lookup"><span data-stu-id="fbdfd-110">Set up postdated checks</span></span>
1. <span data-ttu-id="fbdfd-111">Wechseln Sie zu "Kasse und Bankverwaltung > Einstellungen > Parameter für Kasse- und Bankverwaltung.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="fbdfd-112">Klicken Sie auf die Registerkarte "Vordatierte Schecks".</span><span class="sxs-lookup"><span data-stu-id="fbdfd-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="fbdfd-113">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Vordatierte Schecks aktivieren".</span><span class="sxs-lookup"><span data-stu-id="fbdfd-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="fbdfd-114">Aktivieren bzw. deaktivieren Sie die Beitragsjournaleinträge für Kontrollkästchen der vordatierten Schecks.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="fbdfd-115">Geben Sie im Feld Verrechnungskonto die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="fbdfd-116">Geben Sie im Feld Verrechnungskonto für erhaltene Schecks die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="fbdfd-117">In der allgemeinen Erfassung für das Vorbereiten des Eintrags felds, geben Sie einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="fbdfd-118">Geben Sie im Feld "Vordatierte Schecks in diese Kreditoren-Zahlungserfassung übertragen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="fbdfd-119">Geben Sie im Feld Verrechnungskonto für Quellensteuer die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="fbdfd-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="fbdfd-120">Click Save.</span></span>
11. <span data-ttu-id="fbdfd-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-121">Close the page.</span></span>
12. <span data-ttu-id="fbdfd-122">Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".</span><span class="sxs-lookup"><span data-stu-id="fbdfd-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="fbdfd-123">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fbdfd-123">Click New.</span></span>
14. <span data-ttu-id="fbdfd-124">Geben Sie im Feld "Zahlungsmethode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="fbdfd-125">Markieren Sie das Kontrollkästchen , um anzugeben, dass der Scheckbetrag zu einem Verrechnungskonto gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="fbdfd-126">Wählen Sie im Feld "Kontotyp" "Bank" aus.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="fbdfd-127">Das Gegenkonto der Zahlungsmethode ist eine Bank.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="fbdfd-128">Geben Sie im Feld "Zahlungskonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="fbdfd-129">Wählen Sie das Bankkonto aus, das zum Abziehen des Rechnungsbetrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="fbdfd-130">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-130">Click Save.</span></span>
19. <span data-ttu-id="fbdfd-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-131">Close the page.</span></span>
> [!NOTE]
> <span data-ttu-id="fbdfd-132">Um einen vordatierten Scheck auf ein Bankkonto buchen zu können, wenn das Sitzungsdatum höher oder gleich dem Fälligkeitsdatum ist, müssen Sie die Funktion **Validierung des Fälligkeitsdatums der Buchung der Zahlungserfassung mit vordatiertem Schecks auf das Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-132">To be able to post a postdated check to a bank account when the session date is greater than or equal to the maturity date, you must enable the feature **Maturity date validation of posting payment journal with postdated checks to bank account**.</span></span> <span data-ttu-id="fbdfd-133">Mit dieser Funktion können Sie Zahlungserfassungen für Kreditoren und Debitoren mit vordatierten Schecks buchen, wenn das Sitzungsdatum höher oder gleich dem Fälligkeitsdatum ist.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-133">This feature allows you to post payment journals for vendors or customers with postdated checks, when the session date is greater than or equal to the maturity date.</span></span>
> 
> <span data-ttu-id="fbdfd-134">Füllen Sie beim Festlegen der **Zahlungmethode** (**Kreditorenkonto > Zahlungssetup > Zahlungsmethoden**) **Transferkonto** nicht aus.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-134">When setting the **Method of payment** (**Accounts payable > Payment setup > Methods of payment**), do not fill in **Bridging account**.</span></span> <span data-ttu-id="fbdfd-135">In diesem Fall wird als Gegenkonto das Bankkonto eingetragen, das unter **Zahlungsmethode** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-135">In this case, the offset account is filled in with the bank account, which is set up in the **Method of payment**.</span></span>
>  
> <span data-ttu-id="fbdfd-136">Wenn die Funktion aktiviert ist und das Sitzungsdatum niedriger ist als das Fälligkeitsdatum, wird beim Buchen einer Zahlungserfassung die folgende Fehlermeldung angezeigt: „Das Fälligkeitsdatum muss niedriger oder gleich dem Sitzungsdatum sein, wenn der Gegenkontotyp die Bank ist“.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-136">When the feature is enabled and the session date is less than the maturity date, the following error message is displayed when posting a payment journal, "Maturity date must be less or equal to the session date if offset account type is Bank".</span></span> <span data-ttu-id="fbdfd-137">Wenn die Funktion nicht aktiviert ist, können Sie eine Zahlungserfassung mit einem vordatierten Scheck buchen, wenn das Sitzungsdatum niedriger ist als das Fälligkeitsdatum.</span><span class="sxs-lookup"><span data-stu-id="fbdfd-137">If the feature is not enabled, you can post a payment journal with a postdated check when the session date is less than the maturity date.</span></span>    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
