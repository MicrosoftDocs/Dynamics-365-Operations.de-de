--- 
title: Anlagen von Kreditoren erstellen und erwerben
description: "Diese Aufgabenanleitung führt Sie Schritt für Schritt durch die Erstellung und Anschaffung einer Anlage mit dem Einkaufsprozess."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9149378047fc22efbd401b7af86df07c1403e4f5
ms.openlocfilehash: cfe920b2ef493ab3ae36a9557001086ed99c3e4e
ms.contentlocale: de-de
ms.lasthandoff: 10/05/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="d5306-103">Anlagen von Kreditoren erstellen und erwerben</span><span class="sxs-lookup"><span data-stu-id="d5306-103">Create and acquire assets from accounts payable</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5306-104">Diese Aufgabenanleitung führt Sie Schritt für Schritt durch die Erstellung und Anschaffung einer Anlage mit dem Einkaufsprozess.</span><span class="sxs-lookup"><span data-stu-id="d5306-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span> <span data-ttu-id="d5306-105">Dabei werden der "Buchhalter" und die "Sachbearbeiter Kreditorenkonten" und das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="d5306-105">It uses the Accountant and Accounts payable clerks and the demo company USMF.</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="d5306-106">Anlagenparametern festlegen</span><span class="sxs-lookup"><span data-stu-id="d5306-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="d5306-107">Wechseln Sie zu "Anlagen" > "Einstellungen" > "Anlagenparameter".</span><span class="sxs-lookup"><span data-stu-id="d5306-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="d5306-108">Erweitern oder reduzieren Sie den Abschnitt "Bestellung".</span><span class="sxs-lookup"><span data-stu-id="d5306-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="d5306-109">Aktivieren Sie das Kontrollkästchen "Anlagenanschaffung aus Einkauf zulassen".</span><span class="sxs-lookup"><span data-stu-id="d5306-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="d5306-110">Aktivieren Sie das Kontrollkästchen "Anlage bei Buchung von Produktzugang oder Rechnung erstellen".</span><span class="sxs-lookup"><span data-stu-id="d5306-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="d5306-111">Eine neue Kreditorenrechnung erstellen</span><span class="sxs-lookup"><span data-stu-id="d5306-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="d5306-112">Wechseln Sie zu "Kreditoren" > "Arbeitsbereiche" > "Kreditorenrechnungseintrag".</span><span class="sxs-lookup"><span data-stu-id="d5306-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="d5306-113">Klicken Sie auf "Neue Kreditorenrechnung".</span><span class="sxs-lookup"><span data-stu-id="d5306-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="d5306-114">Klicken Sie im Feld "Rechnungskonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d5306-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d5306-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d5306-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d5306-116">Geben Sie im Feld "Zahl" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d5306-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="d5306-117">Geben Sie im Feld "Buchungsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="d5306-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="d5306-118">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="d5306-118">Click Add line.</span></span>
8. <span data-ttu-id="d5306-119">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d5306-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d5306-120">Entweder nicht gelagerte Artikel oder Beschaffungskategorien können für Anlagenanschaffung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5306-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="d5306-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d5306-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d5306-122">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d5306-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="d5306-123">Eine Rechnungsposition erstellt nur eine Anlage, unabhängig von Menge.</span><span class="sxs-lookup"><span data-stu-id="d5306-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="d5306-124">Der Rechnungsmengen-Feldwert wird zur Anlagenmenge übertragen.</span><span class="sxs-lookup"><span data-stu-id="d5306-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="d5306-125">Geben Sie im Feld "Preis je Einheit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d5306-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="d5306-126">Erweitern oder reduzieren Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="d5306-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="d5306-127">Klicken Sie auf die Registerkarte "Anlagen".</span><span class="sxs-lookup"><span data-stu-id="d5306-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="d5306-128">Aktivieren Sie das Kontrollkästchen "Neue Anlage erstellen".</span><span class="sxs-lookup"><span data-stu-id="d5306-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="d5306-129">Klicken Sie im Feld "Anlagengruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d5306-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="d5306-130">Wählen Sie in der Liste die Anlagengruppe aus, die beim Erstellen der neuen Anlage zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="d5306-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="d5306-131">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d5306-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="d5306-132">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="d5306-132">Click Post.</span></span>
    * <span data-ttu-id="d5306-133">Die Anlage wird erstellt und abgerufen, wann die Rechnung gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="d5306-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  


