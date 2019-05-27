---
title: Erstellen eines Kreditorenkontos
description: Im folgenden Verfahren, wie ein Kreditorenkonto erstellt und eine Adresse und Kontaktinformationen unter.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22c7a1a2b7468f00aa25a67a2c5f62b088e2fe7c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546178"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="f844b-103">Erstellen eines Kreditorenkontos</span><span class="sxs-lookup"><span data-stu-id="f844b-103">Create a vendor account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f844b-104">Im folgenden Verfahren, wie ein Kreditorenkonto erstellt und eine Adresse und Kontaktinformationen unter.</span><span class="sxs-lookup"><span data-stu-id="f844b-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="f844b-105">Das Verfahren wird nicht angezeigt, wie alle Felder für den Einkauf und die Finanzzwecke aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="f844b-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="f844b-106">Weitere Informationen über diese Felder zu ermitteln, lesen Sie in den Feldbeschreibungen.</span><span class="sxs-lookup"><span data-stu-id="f844b-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="f844b-107">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="f844b-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="f844b-108">Kreditorenkonten sind normalerweise von einem Beschaffungsspezialisten oder von Debitoren mitarbeitern erstellt.</span><span class="sxs-lookup"><span data-stu-id="f844b-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="f844b-109">Erstellen eines Kreditorenkontos</span><span class="sxs-lookup"><span data-stu-id="f844b-109">Create a vendor account</span></span>
1. <span data-ttu-id="f844b-110">Klicken Sie auf "Beschaffung" > "Kreditoren" > "Alle Kreditoren".</span><span class="sxs-lookup"><span data-stu-id="f844b-110">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="f844b-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f844b-111">Click New.</span></span>
3. <span data-ttu-id="f844b-112">Geben Sie im Feld "Kreditorenkonto" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f844b-112">In the Vendor account field, type a value.</span></span>
    * <span data-ttu-id="f844b-113">Der Wert wird automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f844b-113">The value may be populated automatically.</span></span> <span data-ttu-id="f844b-114">In diesem Fall können Sie diesen Schritt übergehen.</span><span class="sxs-lookup"><span data-stu-id="f844b-114">If so, you can skip this step.</span></span>  
    * <span data-ttu-id="f844b-115">Sie können Kreditor erstellen für eine Person oder eine Organisation.</span><span class="sxs-lookup"><span data-stu-id="f844b-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="f844b-116">Dies wirkt sich darauf aus, welche Felder verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f844b-116">This will affect which fields are available.</span></span> <span data-ttu-id="f844b-117">In diesem Beispiel erstellen wir ein Händlerkonto für eine Organisation.</span><span class="sxs-lookup"><span data-stu-id="f844b-117">In this example, we’ll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="f844b-118">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f844b-118">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="f844b-119">Wenn Ihr Kreditor bereits eine erfasste Partei im System ist, die verwendet werden ablegen unten und wählen Sie diese in diesem Feld aus und das neue Kreditorenkonto erbt die Adresse und die Kontaktinformationen, die bereits erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="f844b-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that’s already registered.</span></span>  
5. <span data-ttu-id="f844b-120">Geben Sie im Feld "Gruppe" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f844b-120">In the Group field, enter or select a value.</span></span>
    * <span data-ttu-id="f844b-121">Die Händlergruppe wird verwendet, um Händler zu gruppieren, die mindestens einen der folgenden Parameter gemeinsam haben: Zahlungsbedingungen, Abrechnungszeitraum, Lagerbuchungssachkonten – einschließlich der Mehrwertsteuergruppe, Standardsachkonten, Produktfiltercodes oder Beschaffungsplanungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f844b-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment , settle period,  inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>  
6. <span data-ttu-id="f844b-122">Geben Sie im Feld "Anzahl der Mitarbeiter" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f844b-122">In the Number of employees field, enter a number.</span></span>
7. <span data-ttu-id="f844b-123">Geben Sie im Feld "Organisationsnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f844b-123">In the Organization number field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="f844b-124">Adresse hinzufügen</span><span class="sxs-lookup"><span data-stu-id="f844b-124">Add an address</span></span>
1. <span data-ttu-id="f844b-125">Erweitern Sie den Abschnitt Adressen.</span><span class="sxs-lookup"><span data-stu-id="f844b-125">Expand the Addresses section.</span></span>
2. <span data-ttu-id="f844b-126">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f844b-126">Click Add.</span></span>
3. <span data-ttu-id="f844b-127">Geben Sie im Feld "Zweck" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f844b-127">In the Purpose field, enter or select a value.</span></span>
    * <span data-ttu-id="f844b-128">Sie können eine Position oder mehrere Zwecke auswählen.</span><span class="sxs-lookup"><span data-stu-id="f844b-128">You can select one or more purposes.</span></span> <span data-ttu-id="f844b-129">Diese werden verwendet, um die korrekte Adresse für einen bestimmten Zweck auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f844b-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="f844b-130">Wenn beispielsweise der Zweck "Rechnung" lautet, wird diese Adresse verwendet, wenn Sie Rechnungen senden.</span><span class="sxs-lookup"><span data-stu-id="f844b-130">For example, if the purpose is “Invoice” that address will be used when you send invoices.</span></span>  
4. <span data-ttu-id="f844b-131">Geben Sie im Feld "Name oder Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f844b-131">In the Name or description field, type a value.</span></span>
5. <span data-ttu-id="f844b-132">Wählen Sie im Feld Name/Region einen Wert aus oder geben Sie ihn ein«».</span><span class="sxs-lookup"><span data-stu-id="f844b-132">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="f844b-133">Geben Sie die Informationen zur Adresse ein.</span><span class="sxs-lookup"><span data-stu-id="f844b-133">Enter the address details.</span></span> <span data-ttu-id="f844b-134">Das Land/die Region, das Sie bestimmen die Felder ausgewählt haben, die Sie mit dargestellt werden, entsprechend dem Adressformat für Land/Region.</span><span class="sxs-lookup"><span data-stu-id="f844b-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span>   
6. <span data-ttu-id="f844b-135">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f844b-135">Click OK.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="f844b-136">Kontaktinformationen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="f844b-136">Add contact information</span></span>
1. <span data-ttu-id="f844b-137">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f844b-137">Click Add.</span></span>
2. <span data-ttu-id="f844b-138">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f844b-138">In the Description field, type a value.</span></span>
3. <span data-ttu-id="f844b-139">Wählen Sie im Feld "Typ" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="f844b-139">In the Type field, select an option.</span></span>
4. <span data-ttu-id="f844b-140">Geben Sie im Feld "Kontaktnummer/-adresse" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f844b-140">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="f844b-141">Sie können das Kontrollkästchen "Primär" auswählen, wenn dies der primäre Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="f844b-141">You can select the Primary check box if this is the primary contact.</span></span>  
5. <span data-ttu-id="f844b-142">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f844b-142">Click Save.</span></span>
6. <span data-ttu-id="f844b-143">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f844b-143">Close the page.</span></span>
7. <span data-ttu-id="f844b-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f844b-144">Close the page.</span></span>

