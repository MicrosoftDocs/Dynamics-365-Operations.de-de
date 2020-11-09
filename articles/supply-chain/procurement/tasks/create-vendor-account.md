---
title: Erstellen eines Kreditorenkontos
description: Im folgenden Verfahren, wie ein Kreditorenkonto erstellt und eine Adresse und Kontaktinformationen unter.
author: mkirknel
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd8cd2bb7b03c0415a5c5656f0e3ffada961973e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017206"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="5c2dd-103">Erstellen eines Kreditorenkontos</span><span class="sxs-lookup"><span data-stu-id="5c2dd-103">Create a vendor account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5c2dd-104">Im folgenden Verfahren, wie ein Kreditorenkonto erstellt und eine Adresse und Kontaktinformationen unter.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="5c2dd-105">Das Verfahren wird nicht angezeigt, wie alle Felder für den Einkauf und die Finanzzwecke aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="5c2dd-106">Weitere Informationen über diese Felder zu ermitteln, lesen Sie in den Feldbeschreibungen.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="5c2dd-107">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="5c2dd-108">Kreditorenkonten sind normalerweise von einem Beschaffungsspezialisten oder von Debitoren mitarbeitern erstellt.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="5c2dd-109">Ein Kreditorenkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="5c2dd-109">Create a vendor account</span></span>
1. <span data-ttu-id="5c2dd-110">Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Kreditoren > Alle Kreditoren**.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-110">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="5c2dd-111">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-111">Click **New**.</span></span>
3. <span data-ttu-id="5c2dd-112">Geben Sie im Feld **Lieferantenkonto** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-112">In the **Vendor account** field, type a value.</span></span>
    - <span data-ttu-id="5c2dd-113">Der Wert wird automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-113">The value may be populated automatically.</span></span> <span data-ttu-id="5c2dd-114">In diesem Fall können Sie diesen Schritt übergehen.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-114">If so, you can skip this step.</span></span>  
    - <span data-ttu-id="5c2dd-115">Sie können Kreditor erstellen für eine Person oder eine Organisation.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="5c2dd-116">Dies wirkt sich darauf aus, welche Felder verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-116">This will affect which fields are available.</span></span> <span data-ttu-id="5c2dd-117">In diesem Beispiel erstellen wir ein Lieferantenkonto für eine Organisation.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-117">In this example, we'll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="5c2dd-118">Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-118">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="5c2dd-119">Wenn Ihr Lieferant bereits eine erfasste Partei im System ist, können Sie das Dropdown-Menü verwenden und sie im Feld auswählen. Das neue Kreditorenkonto erbt die Adresse und die Kontaktinformationen, die bereits erfasst ist.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that's already registered.</span></span>
5. <span data-ttu-id="5c2dd-120">Geben Sie im Feld **Gruppe** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-120">In the **Group** field, enter or select a value.</span></span> <span data-ttu-id="5c2dd-121">Die Lieferantengruppe wird verwendet, um Lieferanten zu gruppieren, die mindestens einen der folgenden Parameter gemeinsam haben: Zahlungsbedingungen, Abrechnungszeitraum, Lagerbuchungssachkonten – einschließlich der Mehrwertsteuergruppe, Standardsachkonten, Produktfiltercodes oder Beschaffungsplanungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment, settle period, inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>
6. <span data-ttu-id="5c2dd-122">Geben Sie im Feld **Anzahl der Mitarbeiter** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-122">In the **Number of employees** field, enter a number.</span></span>
7. <span data-ttu-id="5c2dd-123">Geben Sie im Feld **Organisationsnummer** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-123">In the **Organization number** field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="5c2dd-124">Adresse hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5c2dd-124">Add an address</span></span>
1. <span data-ttu-id="5c2dd-125">Erweitern Sie den Abschnitt **Adressen**.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-125">Expand the **Addresses** section.</span></span>
2. <span data-ttu-id="5c2dd-126">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-126">Click **Add**.</span></span>
3. <span data-ttu-id="5c2dd-127">Geben Sie im Feld **Zweck** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-127">In the **Purpose** field, enter or select a value.</span></span> <span data-ttu-id="5c2dd-128">Sie können eine Position oder mehrere Zwecke auswählen.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-128">You can select one or more purposes.</span></span> <span data-ttu-id="5c2dd-129">Diese werden verwendet, um die korrekte Adresse für einen bestimmten Zweck auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="5c2dd-130">Wenn beispielsweise der Zweck „Rechnung“ lautet, wird diese Adresse verwendet, wenn Sie Rechnungen senden.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-130">For example, if the purpose is "Invoice" that address will be used when you send invoices.</span></span>
4. <span data-ttu-id="5c2dd-131">Geben Sie in das Feld **Name oder Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-131">In the **Name or description** field, type a value.</span></span>
5. <span data-ttu-id="5c2dd-132">Wählen Sie im Feld **Land/Region** einen Wert aus, oder geben Sie einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-132">In the **Country/region** field, enter or select a value.</span></span> <span data-ttu-id="5c2dd-133">Geben Sie die Informationen zur Adresse ein.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-133">Enter the address details.</span></span> <span data-ttu-id="5c2dd-134">Das Land/die Region, das Sie bestimmen die Felder ausgewählt haben, die Sie mit dargestellt werden, entsprechend dem Adressformat für Land/Region.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span> 
6. <span data-ttu-id="5c2dd-135">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-135">Click **OK**.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="5c2dd-136">Kontaktinformationen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5c2dd-136">Add contact information</span></span>
1. <span data-ttu-id="5c2dd-137">Erweitern Sie den Abschnitt **Kontaktinformationen**.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-137">Expand the **Contact information** section.</span></span>
2. <span data-ttu-id="5c2dd-138">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-138">Click **Add**.</span></span>
3. <span data-ttu-id="5c2dd-139">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-139">In the **Description** field, type a value.</span></span>
4. <span data-ttu-id="5c2dd-140">Wählen Sie im Feld **Typ** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-140">In the **Type** field, select an option.</span></span>
5. <span data-ttu-id="5c2dd-141">Geben Sie im Feld **Kontaktnummer/-adresse** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-141">In the **Contact number/address** field, type a value.</span></span> <span data-ttu-id="5c2dd-142">Sie können das Kontrollkästchen "Primär" auswählen, wenn dies der primäre Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-142">You can select the Primary check box if this is the primary contact.</span></span>  
6. <span data-ttu-id="5c2dd-143">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-143">Click **Save**.</span></span>
7. <span data-ttu-id="5c2dd-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-144">Close the page.</span></span>
8. <span data-ttu-id="5c2dd-145">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-145">Close the page.</span></span>

