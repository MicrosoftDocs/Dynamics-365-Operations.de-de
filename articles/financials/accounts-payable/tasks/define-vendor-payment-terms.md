--- 
title: Kreditorenzahlungsbedingungen definieren
description: "Zahlungsbedingungen für Kreditorenrechnungen einrichten"
author: abruer
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 6d9eaf271220437869ff90610e9953a6e2f8a474
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2018

---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="449ee-103">Kreditorenzahlungsbedingungen definieren</span><span class="sxs-lookup"><span data-stu-id="449ee-103">Define vendor payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="449ee-104">Zahlungsbedingungen für Kreditorenrechnungen einrichten</span><span class="sxs-lookup"><span data-stu-id="449ee-104">Set up payment terms for vendor invoices.</span></span> <span data-ttu-id="449ee-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="449ee-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="449ee-106">Wechseln Sie zu Kreditoren > Zahlungseinstellungen > Zahlungsbedingungen.</span><span class="sxs-lookup"><span data-stu-id="449ee-106">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="449ee-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="449ee-107">Click New.</span></span>
    * <span data-ttu-id="449ee-108">Die Seite "Zahlungsbedingungen" wird verwendet, um zu definieren, wie das Fälligkeitsdatum berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="449ee-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="449ee-109">Sie wird nicht verwendet, um zu definieren, wie das Skontodatum berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="449ee-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="449ee-110">Geben Sie im Feld "Zahlungsbedingungen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="449ee-110">In the Terms of payment field, type a value.</span></span>
4. <span data-ttu-id="449ee-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="449ee-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="449ee-112">Geben Sie im Feld "Tage" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="449ee-112">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="449ee-113">Die Zahl, die hier eingegeben wird, wird verwendet, um sie dem Fälligkeitsdatum oder dem Ende der Periode, die in der Zahlungsmethode angegeben ist, hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="449ee-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="449ee-114">Wenn Sie zum Beispiel "Netto" auswählen, wird die Zahl zum Fälligkeitsdatum addiert.</span><span class="sxs-lookup"><span data-stu-id="449ee-114">For example, if you select Net, the number will be added to the due date.</span></span> <span data-ttu-id="449ee-115">Wenn Sie "Aktueller Monat" auswählen, wird die Zahl dem letzten Tag des aktuellen Monats hinzugefügt, um das Fälligkeitsdatum zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="449ee-115">If you select Current month, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="449ee-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="449ee-116">Click Save.</span></span>
7. <span data-ttu-id="449ee-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="449ee-117">Close the page.</span></span>
8. <span data-ttu-id="449ee-118">Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Skonti".</span><span class="sxs-lookup"><span data-stu-id="449ee-118">Go to Accounts payable > Payment setup > Cash discounts.</span></span>
9. <span data-ttu-id="449ee-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="449ee-119">Click New.</span></span>
10. <span data-ttu-id="449ee-120">Geben Sie im Feld "Skonto" eine Kennung ein.</span><span class="sxs-lookup"><span data-stu-id="449ee-120">In the Cash discount field, enter an ID.</span></span>
11. <span data-ttu-id="449ee-121">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="449ee-121">In the Description field, type a value.</span></span>
12. <span data-ttu-id="449ee-122">Wenn der Kreditor einen gestaffelten Rabatt anbietet, wählen Sie das nächste Skonto aus, nachdem das aktuelle abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="449ee-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="449ee-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="449ee-123">Close the page.</span></span>
14. <span data-ttu-id="449ee-124">Geben Sie im Feld "Tage" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="449ee-124">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="449ee-125">Die Menge, die im Feld "Tag" eingegeben wird, wird verwendet, um das "Skontodatum" zu berechnen, basierend darauf, welche Option im Feld "Netto/Aktuell" ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="449ee-125">The quantity entered in the Days field will be used to calculate the Cash discount date, based on what option was selected in the Net/Current field.</span></span> <span data-ttu-id="449ee-126">Wenn "Netto" ausgewählt wurde, wird die Menge zum Rechnungsdatum hinzugefügt, um das Skontodatum zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="449ee-126">If Net was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="449ee-127">Wenn "Aktueller Monat" ausgewählt wurde, wird die Menge zum Ende des Währungsmonats hinzugefügt, um das Skontodatum zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="449ee-127">If Current month was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="449ee-128">Geben Sie im Feld "Rabatt" den Prozentsatz des Skontos ein.</span><span class="sxs-lookup"><span data-stu-id="449ee-128">Enter the percentage of the cash discount in the Discount field.</span></span> 
16. <span data-ttu-id="449ee-129">Geben Sie das Hauptkonto ein, zu dem der Skonto für Debitorenrechnungen gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="449ee-129">Enter the main account to which the cash discount will be posted for customer invoices.</span></span>
17. <span data-ttu-id="449ee-130">Geben Sie das Hauptkonto ein, zu dem der Skonto für Kreditorenrechnungen gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="449ee-130">Enter the main account to which the cash discount will be posted for vendor invoices.</span></span>
    * <span data-ttu-id="449ee-131">Wenn "Rabattgegenkonten" auf "Hauptkonto für Kreditorenrabatt verwenden" festgelegt wird, dann wird das "Hauptkonto" verwendet.</span><span class="sxs-lookup"><span data-stu-id="449ee-131">If 'Discount offset accounts' is set to Use main account for vendor discount, then the Main account will be used.</span></span>  <span data-ttu-id="449ee-132">Wenn die Option auf "Konten zu den Rechnungspositionen" festgelegt ist, wird der Skonto zu den Anlagen-/Ausgabenkonten auf den Rechnungspositionen gebucht.</span><span class="sxs-lookup"><span data-stu-id="449ee-132">If the option is set to Accounts on the invoice lines, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
18. <span data-ttu-id="449ee-133">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="449ee-133">Click Save.</span></span>


