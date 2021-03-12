---
title: Definieren von Kreditorenzahlungsbedingungen
description: In diesem Thema wird erläutert, wie Zahlungsbedingungen für Kreditorenrechnungen eingerichtet werden.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b69b505996b5536088578885c11a7e8c27f4975
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971852"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="f6ed0-103">Definieren von Kreditorenzahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="f6ed0-103">Define vendor payment terms</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6ed0-104">In diesem Thema wird erläutert, wie Zahlungsbedingungen für Kreditorenrechnungen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="f6ed0-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="f6ed0-106">Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Zahlungseinstellungen > Zahlungsbedingungen**.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="f6ed0-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-107">Select **New**.</span></span> <span data-ttu-id="f6ed0-108">Die Seite "Zahlungsbedingungen" wird verwendet, um zu definieren, wie das Fälligkeitsdatum berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="f6ed0-109">Sie wird nicht verwendet, um zu definieren, wie das Skontodatum berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="f6ed0-110">Geben Sie im Feld **Zahlungsbedingungen** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="f6ed0-111">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="f6ed0-112">Geben Sie im Feld **Tage** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="f6ed0-113">Die Zahl, die hier eingegeben wird, wird verwendet, um sie dem Fälligkeitsdatum oder dem Ende der Periode, die in der Zahlungsmethode angegeben ist, hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="f6ed0-114">Wenn Sie zum Beispiel **Netto** auswählen, wird die Zahl zum Fälligkeitsdatum addiert.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="f6ed0-115">Wenn Sie **Aktueller Monat** auswählen, wird die Zahl dem letzten Tag des aktuellen Monats hinzugefügt, um das Fälligkeitsdatum zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="f6ed0-116">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-116">Select **Save**.</span></span>
7. <span data-ttu-id="f6ed0-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-117">Close the page.</span></span>
8. <span data-ttu-id="f6ed0-118">Wechseln Sie zu **Kreditoren > Zahlungseinstellungen > Skonti**.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="f6ed0-119">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-119">Select **New**.</span></span>
10. <span data-ttu-id="f6ed0-120">Geben Sie im Feld **Skonto** eine Kennung ein.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="f6ed0-121">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="f6ed0-122">Wenn der Kreditor einen gestaffelten Rabatt anbietet, wählen Sie das nächste Skonto aus, nachdem das aktuelle abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="f6ed0-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-123">Close the page.</span></span>
14. <span data-ttu-id="f6ed0-124">Geben Sie im Feld **Tage** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="f6ed0-125">Die Menge, die im Feld **Tage** eingegeben wird, wird verwendet, um das Skontodatum zu berechnen, basierend darauf, welche Option im Feld **Netto/Aktuell** ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="f6ed0-126">Wenn **Netto** ausgewählt wurde, wird die Menge zum Rechnungsdatum hinzugefügt, um das Skontodatum zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="f6ed0-127">Wenn **Aktueller Monat** ausgewählt wurde, wird die Menge zum Ende des Währungsmonats hinzugefügt, um das Skontodatum zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="f6ed0-128">Geben Sie im Feld **Rabatt** den Prozentsatz des Skontos ein.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="f6ed0-129">Geben Sie das Hauptkonto ein, in das der Skonto für Debitorenrechnungen gebucht wird. Geben Sie dann das Hauptkonto ein, in das der Skonto für Kreditorenrechnungen gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="f6ed0-130">Wenn **Rabattgegenkonten** auf **Hauptkonto für Kreditorenrabatte verwenden** festgelegt wird, dann wird das „Hauptkonto“ verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="f6ed0-131">Wenn die Option auf **Konten in den Rechnungspositionen** festgelegt ist, wird der Skonto zu den Anlagen-/Ausgabenkonten auf den Rechnungspositionen gebucht.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="f6ed0-132">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f6ed0-132">Select **Save**.</span></span>

