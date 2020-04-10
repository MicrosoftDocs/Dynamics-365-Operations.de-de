---
title: Ein Kreditorenbankkonto erstellen
description: Diese Prozedur zeigt Ihnen, wie Sie ein Bankkonto für einen Kreditor erstellen.
author: mkirknel
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be06343aba974ff23a7f328d2175f00768a76465
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149572"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="eec23-103">Ein Kreditorenbankkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="eec23-103">Create a vendor bank account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eec23-104">Diese Prozedur zeigt Ihnen, wie Sie ein Bankkonto für einen Kreditor erstellen.</span><span class="sxs-lookup"><span data-stu-id="eec23-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="eec23-105">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="eec23-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="eec23-106">Wechseln Sie zu **Navigationsbereich > Module > Beschaffung > Kreditoren > Alle Kreditoren**.</span><span class="sxs-lookup"><span data-stu-id="eec23-106">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="eec23-107">Wählen Sie den Kreditor aus, für den Sie ein Bankkonto erstellen möchten, und klicken Sie dann auf den Link im Feld **Kreditorkontenkennung**.</span><span class="sxs-lookup"><span data-stu-id="eec23-107">Select the vendor that you want to create a bank account for, and then click the link on the **Vendor account ID** field.</span></span>
3. <span data-ttu-id="eec23-108">Klicken Sie im **Aktivitätsbereich** auf **Händler**.</span><span class="sxs-lookup"><span data-stu-id="eec23-108">On the **Action pane**, click **Vendor**.</span></span>
4. <span data-ttu-id="eec23-109">Klicken Sie auf **Bankkonten**.</span><span class="sxs-lookup"><span data-stu-id="eec23-109">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="eec23-110">Klicken Sie im **Aktivitätsbereich** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="eec23-110">On the **Action pane**, click **New**.</span></span>
6. <span data-ttu-id="eec23-111">Geben Sie im Feld **Bankkonto** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="eec23-111">In the **Bank account** field, type a value.</span></span> <span data-ttu-id="eec23-112">Diese Kennung wird verwendet, um das Bankkonto im Kreditorendatensatz zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="eec23-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="eec23-113">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="eec23-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="eec23-114">Geben Sie im Feld **Bankgruppen** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="eec23-114">In the **Bank groups** field, enter or select a value.</span></span>
9. <span data-ttu-id="eec23-115">Wählen Sie im Feld **Bankleitzahltyp** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="eec23-115">In the **Routing number type** field, select an option.</span></span> <span data-ttu-id="eec23-116">Das ist der Bankleitzahltyp, der für die internationalen Zahlungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eec23-116">This is the type of routing number that's used for international payments.</span></span>  
10. <span data-ttu-id="eec23-117">Geben Sie im Feld **Bankkontonummer** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="eec23-117">In the **Bank account number** field, type a value.</span></span>
11. <span data-ttu-id="eec23-118">Geben Sie im Feld **SWIFT-Code** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="eec23-118">In the **SWIFT code** field, type a value.</span></span>
12. <span data-ttu-id="eec23-119">Geben Sie im Feld **IBAN** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="eec23-119">In the **IBAN** field, type a value.</span></span>
    - <span data-ttu-id="eec23-120">Die IBAN-Nummer muss im korrekten Format sein.</span><span class="sxs-lookup"><span data-stu-id="eec23-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="eec23-121">Sie könnten zum Beispiel "DE89370400440532013000" verwenden.</span><span class="sxs-lookup"><span data-stu-id="eec23-121">For example, you could use DE89370400440532013000.</span></span>  
    - <span data-ttu-id="eec23-122">Der Status des Bankkontos ist "Aktiv", wenn das "Aktives Datum" erreicht worden ist, und das "Ablaufdatum" noch nicht überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="eec23-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="eec23-123">Es ist auch aktiv, wenn die Felder „Aktives Datum“ und „Ablaufdatum“ leer sind.</span><span class="sxs-lookup"><span data-stu-id="eec23-123">It's also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="eec23-124">Wenn die Datumsangaben sowohl im Feld "Aktives Datum" als auch im Feld "Ablaufdatum" in der Zukunft liegen, sind elektronische Zahlungen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eec23-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="eec23-125">Andere Zahlungstypen sind verfügbar, und das Bankkonto ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="eec23-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="eec23-126">Erweitern Sie den Abschnitt **Einrichtung**.</span><span class="sxs-lookup"><span data-stu-id="eec23-126">Expand the **Setup** section.</span></span>
14. <span data-ttu-id="eec23-127">Geben Sie im Feld **Textcode** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="eec23-127">In the **Text code** field, type a value.</span></span> <span data-ttu-id="eec23-128">Dieses Feld gibt einen Code an, der auf dem Bankauszug des Empfängers angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="eec23-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="eec23-129">Geben Sie im Feld **Nachricht an die Bank** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="eec23-129">In the **Message to bank** field, type a value.</span></span>
16. <span data-ttu-id="eec23-130">Geben Sie im Feld **Wechselkursreferenz** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="eec23-130">In the **Exchange reference** field, type a value.</span></span> <span data-ttu-id="eec23-131">Das ist die Referenznummer für einen beliebigen Terminwechselkurs oder festen Wechselkurs.</span><span class="sxs-lookup"><span data-stu-id="eec23-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>
17. <span data-ttu-id="eec23-132">Geben Sie im Feld **Währung** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="eec23-132">In the **Currency** field, enter or select a value.</span></span> <span data-ttu-id="eec23-133">Wenn Testtransaktionen ausgestellt werden, stellt dieser Abschnitt einen Überblick über ihren Status (ausstehend oder genehmigt) bereit.</span><span class="sxs-lookup"><span data-stu-id="eec23-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="eec23-134">Erweitern Sie den Abschnitt **Adresse**.</span><span class="sxs-lookup"><span data-stu-id="eec23-134">Expand the **Address** section.</span></span>
19. <span data-ttu-id="eec23-135">Erweitern Sie den Abschnitt **Testtransaktionen**.</span><span class="sxs-lookup"><span data-stu-id="eec23-135">Expand the **Prenotes** section.</span></span>
20. <span data-ttu-id="eec23-136">Erweitern Sie den Abschnitt **Kontaktinformationen**.</span><span class="sxs-lookup"><span data-stu-id="eec23-136">Expand the **Contact information** section.</span></span>
21. <span data-ttu-id="eec23-137">Geben Sie im Feld **Telefon** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="eec23-137">In the **Telephone** field, type a value.</span></span>
22. <span data-ttu-id="eec23-138">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="eec23-138">Close the page.</span></span>
23. <span data-ttu-id="eec23-139">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="eec23-139">Click **Edit**.</span></span>
24. <span data-ttu-id="eec23-140">Erweitern Sie den Abschnitt **Zahlung**.</span><span class="sxs-lookup"><span data-stu-id="eec23-140">Expand the **Payment** section.</span></span>
25. <span data-ttu-id="eec23-141">Wählen Sie im Feld **Bankkonto** das Konto aus, dass Sie gerade erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="eec23-141">In the **Bank account** field, select the account that you've just created.</span></span>
26. <span data-ttu-id="eec23-142">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="eec23-142">Click **Save**.</span></span> <span data-ttu-id="eec23-143">Die Adresse wird möglicherweise von der Bankgruppe geerbt, wenn eine angegeben ist, oder Sie können sie hier hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="eec23-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  

