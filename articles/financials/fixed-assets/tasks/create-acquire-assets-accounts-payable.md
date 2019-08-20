---
title: Anlagen von "Kreditoren" erstellen und anschaffen
description: Diese Aufgabenanleitung führt Sie Schritt für Schritt durch die Erstellung und Anschaffung einer Anlage mit dem Einkaufsprozess.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2626877c907994d03cdae960c8501a858ca214bd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840024"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="63bce-103">Anlagen von "Kreditoren" erstellen und anschaffen</span><span class="sxs-lookup"><span data-stu-id="63bce-103">Create and acquire assets from Accounts payable</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63bce-104">Diese Aufgabenanleitung führt Sie Schritt für Schritt durch die Erstellung und Anschaffung einer Anlage mit dem Einkaufsprozess.</span><span class="sxs-lookup"><span data-stu-id="63bce-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="63bce-105">Dabei werden der "Buchhalter" und die "Sachbearbeiter Kreditorenkonten" und das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="63bce-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="63bce-106">Anlagenparametern festlegen</span><span class="sxs-lookup"><span data-stu-id="63bce-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="63bce-107">Wechseln Sie zu "Anlagen" > "Einstellungen" > "Anlagenparameter".</span><span class="sxs-lookup"><span data-stu-id="63bce-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="63bce-108">Erweitern oder reduzieren Sie den Abschnitt "Bestellung".</span><span class="sxs-lookup"><span data-stu-id="63bce-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="63bce-109">Aktivieren Sie das Kontrollkästchen "Anlagenanschaffung aus Einkauf zulassen".</span><span class="sxs-lookup"><span data-stu-id="63bce-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="63bce-110">Aktivieren Sie das Kontrollkästchen "Anlage bei Buchung von Produktzugang oder Rechnung erstellen".</span><span class="sxs-lookup"><span data-stu-id="63bce-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="63bce-111">Eine neue Kreditorenrechnung erstellen</span><span class="sxs-lookup"><span data-stu-id="63bce-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="63bce-112">Wechseln Sie zu "Kreditoren" > "Arbeitsbereiche" > "Kreditorenrechnungseintrag".</span><span class="sxs-lookup"><span data-stu-id="63bce-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="63bce-113">Klicken Sie auf "Neue Kreditorenrechnung".</span><span class="sxs-lookup"><span data-stu-id="63bce-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="63bce-114">Klicken Sie im Feld "Rechnungskonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="63bce-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="63bce-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="63bce-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="63bce-116">Geben Sie im Feld "Zahl" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="63bce-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="63bce-117">Geben Sie im Feld "Buchungsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="63bce-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="63bce-118">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="63bce-118">Click Add line.</span></span>
8. <span data-ttu-id="63bce-119">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="63bce-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="63bce-120">Entweder nicht gelagerte Artikel oder Beschaffungskategorien können für Anlagenanschaffung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63bce-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="63bce-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="63bce-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="63bce-122">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="63bce-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="63bce-123">Eine Rechnungsposition erstellt nur eine Anlage, unabhängig von Menge.</span><span class="sxs-lookup"><span data-stu-id="63bce-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="63bce-124">Der Rechnungsmengen-Feldwert wird zur Anlagenmenge übertragen.</span><span class="sxs-lookup"><span data-stu-id="63bce-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="63bce-125">Geben Sie im Feld "Preis je Einheit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="63bce-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="63bce-126">Erweitern oder reduzieren Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="63bce-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="63bce-127">Klicken Sie auf die Registerkarte "Anlagen".</span><span class="sxs-lookup"><span data-stu-id="63bce-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="63bce-128">Aktivieren Sie das Kontrollkästchen "Neue Anlage erstellen".</span><span class="sxs-lookup"><span data-stu-id="63bce-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="63bce-129">Klicken Sie im Feld "Anlagengruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="63bce-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="63bce-130">Wählen Sie in der Liste die Anlagengruppe aus, die beim Erstellen der neuen Anlage zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="63bce-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="63bce-131">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="63bce-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="63bce-132">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="63bce-132">Click Post.</span></span>
    * <span data-ttu-id="63bce-133">Die Anlage wird erstellt und abgerufen, wann die Rechnung gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="63bce-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

